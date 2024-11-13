# CycloneFormatSwBomGen
This is a python tool which uses cycloneDX python lib to generate the Cyclone format SW BOM in JSON or XML. It reads from a easy manual handling csv format input, and makes thing easy.

# Background
Nowadays a SW BOM is always requested by customers, and better to be a Cyclone JSON foramt. But different languages may not fully supported by Cyclone DX tools. So our target is simple, only use mandatory tags defined in Cyclone specs:
1. BOM Metadata:
* BOM format: Sepcify CycloneDX as the format
* Version: CycloneDX Version, like "1.4"
* Timestamp: Date and time of BOM generation
2. Component Information:
* Name: The name of the SW component or module(eg., Library name)
* Version: Version of the component
* Component Type: The type of the component, such as library, application or framework
* BOM Ref: A unique identifier for each component, which helps in tracking and linking dependcies within the SBOM. This shall be managed by tool automatically
3. Licenses:
* License Information: License type used like MIT, GPL 3.0 etc. If it is close source then "Proprietary" is recommended
4. Supplier:
* Supplier Name: The entity that provides the component.
* Contract information: Not necessary.
