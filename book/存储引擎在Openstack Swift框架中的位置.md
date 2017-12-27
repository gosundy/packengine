存储引擎在Openstack Swift框架中的位置

![swift](./img/swift.png)

用户通过Openstack swift提供的[Object Storage API](https://developer.openstack.org/api-ref/object-store/)向proxy投递对象操作请求，proxy转发请求到存储该对象的存储节点ObjectServer，ObjectServer调用存储引擎将该对象存储到磁盘。objectEngine是负责将对象存储到磁盘，以及对象在文件系统里的存储组织结构。