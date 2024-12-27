# Projet de Robot - Citrus Yield

Ce projet est dédié au développement d'un robot agricole autonome pour la capture des video et prediction de rendement

## Prérequis

Assurez-vous d'avoir ROS2 installé sur votre machine. Vous pouvez suivre les instructions d'installation de ROS2 [ici](https://index.ros.org/doc/ros2/Installation/).

## Installation des Dépendances

1. Remplacez `<ton distro ros>` par la distribution ROS2 que vous utilisez (par exemple, `humble`, `foxy`, etc.).

2. Installez les dépendances nécessaires en exécutant les commandes suivantes dans un terminal :

```bash
DISTRO=<ton distro ros>  # Remplacez <ton distro ros> par votre distribution ROS2
sudo apt install ros-${DISTRO}-ros2-control ros-jazzy-ros2-controllers
sudo apt install ros-${DISTRO}-xacro  # Pour ROS2 Jazzy
sudo apt install ros-${DISTRO}-twist-mux

    Clonez le dépôt du projet dans votre répertoire src :

cd ~/ros2_ws/src  # Accédez à votre répertoire de workspace ROS2
git clone https://github.com/Abdrahamane123/citrus_yield.git

    Construisez le projet avec colcon :

cd ~/ros2_ws  # Assurez-vous d'être dans votre workspace ROS2
colcon build

    Sourcez l'environnement pour que ROS2 reconnaisse les nouveaux packages :

source install/setup.bash

Lancer le Robot

Pour démarrer le robot, utilisez la commande suivante :

ros2 launch citrus_yield launch_robot.launch.py

Cela lancera le robot et ses différents composants en fonction de la configuration définie dans le fichier launch_robot.launch.py.
