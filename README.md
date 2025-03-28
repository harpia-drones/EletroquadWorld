## Tutorial de como importar o mundo no Gazebo harmonic

1. Acesse a pasta onde ficam os mundos no diretório da PX4

    ```bash
    cd /root/PX4-Autopilot/Tools/simulation/gz/worlds
    ```

2. Clone esse repositório dentro dessa pasta

    ```bash
    git clone git@github.com:harpia-drones/EletroquadWorld.git
    ```

3. Mova o conteudo da pasta EletroquadWorld que acabou de ser clonada para o diretório PX4-Autopilot/.../worlds

    ```bash
    cp -r EletroquadWorld/models .
    cp -r EletroquadWorld/eletroquad.sdf .
    rm -rf EletroquadWorld
    ```

4. Teste se o modelo foi devidamente importado

    ```bash
    cd /root/PX4-Autopilot && make px4_sitl gz_x500 PX4_GZ_WORLD=eletroquad
    ```
