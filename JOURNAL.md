# November 18th, 2026: Architected the system
Today, I worked on planning the system architecture for a human movement monitoring platform that utilises millimetre-wave (mmWave) radar technology.

I discerned a problem: cameras are incredibly INVASIVE - especially in aged care settings where people are trying to live peacefully without having video and audio taped. My solution? Researching the logistics of different radar development platforms, evaluating their suitability for tracking human movement, and investigating these fall-like events. No cameras. No wearable devices.

After comparing several options, I selected the Texas Instruments IWR6843ISK-ODS, a 60 GHz FMCW radar development board capable of producing 3D point-cloud measurements. I chose this platform because it provides access to more detailed spatial and motion information than conventional presence-detection sensors.

In addition to this, I investigated different mounting configurations - particularly the differences between ceiling-mounted and wall-mounted arrangements. From what I could deduce, one of the primary challenges was determining how reliably the radar could observe movement close to the floor, especially when furniture and other obstacles partially obstruct its field of view. Ultimately, I opted for the ceiling mounted configuration.

For processing, I selected a Raspberry Pi 5 (8GB) to handle radar data acquisition, local processing, experimental logging and eventually a real-time visualisation interface. It also provides a basis for future expansion! By having this component as a "super-computer" or a "hub", the aim is to use the current components as a basis for what the technology could look like when the coverage is increased across larger buildings/structures per se.

I established the initial hardware requirements and began planning a custom 3D-printed enclosure and adjustable mounting system. These components will allow me to test different sensor orientations while maintaining consistent mounting geometry.

Finally, I created the GitHub repository to document the project architecture, research objectives and development roadmap.


<img width="922" height="280" alt="image" src="https://github.com/user-attachments/assets/6162f1a4-c2cc-4b93-9541-5d10e727e931" />

-----
