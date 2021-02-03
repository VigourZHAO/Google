### Object

Pod Spec：

1. [NodeSelector](即：Pod 运行在哪个 Node 上) ：Node & Pod 
2. [NodeName](此字段显示 Pod 是否被调度，一般由调度器负责设置)
3. [HostAliases](定义 Pod 的 hosts 文件里的内容，参考 /etc/hosts)
4. [shareProcessNamespace](True : 开启 Pid NameSpace)

Service ：

1. [Service](user space / iptables / ipvs)
2. [LoadBalance]()
3. [NodePord]()
4. [ExternalName]()

Volume ：

1. [Secret](把 Pod 想要访问的加密数据存放在 Etcd 中)
2. [ConfigMap](与 Secret 类似，但不加密)
3. [DownloadAPI]()
4. [ServiceAccountToken]()

Ingress：

1. [HAProxy Ingress Controller]()
2. [Nginx Ingress Controller]()
3. [Traefik Ingress Controller]()
4. [Kong Ingress Controller]()

Kube-Proxy ：

1. [Userspace]()
2. [iptables]()
3. [ipvs]()

---

### Controller

Replication Controller ： RC

ReplicaSet ： RS

