# COMANDOS BÁSICOS

#### Iniciar máquina virtual:
```minikube start --vm-driver=virtualbox```

#### Buscar pods:
```kubectl get pods```

#### Descreve comandos com saída detalhada
```kubectl describe pods <nome-pod>```

#### Executar pod de forma iterativa:
```kubectl exec -it <nome-pod> -- bash```

#### Referências
```https://kubernetes.io/pt/docs/reference/kubectl/cheatsheet/```

# DEFINIÇÕES

#### Pod:
Um ou mais containers implantados em um nó. O pod é o menor e mais simples objeto do Kubernetes.

#### Serviço:
Maneira de expor como serviço de rede uma aplicação executada em um conjunto de pods. Ele dissocia as definições de trabalho dos pods.

#### Nós:
Máquinas que realizam as tarefas solicitadas, atribuídas pelo plano de controle.

#### ClusterIP
Expõe o serviço em um IP interno do cluster. A escolha desse valor torna o serviço acessível apenas de dentro do cluster. Este é o ServiceType padrão

#### NodePort
Expõe o serviço no IP de cada nó em uma porta estática (o NodePort). Um serviço ClusterIP, para o qual o serviço NodePort será roteado, é criado automaticamente. Você poderá entrar em contato com o serviço NodePort, de fora do cluster, solicitando NodeIP:NodePort.

#### LoadBalancer
Expõe o serviço externamente usando o balanceador de carga de um provedor de nuvem. Os serviços NodePort e ClusterIP, para os quais o balanceador de carga externo irá rotear, são criados automaticamente.