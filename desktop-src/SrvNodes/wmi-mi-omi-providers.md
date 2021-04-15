---
description: A WMI (infraestrutura de gerenciamento do Windows), a MI (Instrumentação de gerenciamento) e a OMI (infraestrutura de gerenciamento aberta) usam arquivos MOF (Management Object Format) para descrever as informações disponibilizadas por meio de seus respectivos provedores.
ms.assetid: 5ec3c6a2-df23-446d-a4da-b8e207eeb6f6
title: Provedores WMI/MI/OMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505a0853d9df7d9cf6f2371f6342b77f61f536b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753705"
---
# <a name="wmimiomi-providers"></a>Provedores WMI/MI/OMI

A WMI (infraestrutura de gerenciamento do Windows), a MI (Instrumentação de gerenciamento) e a OMI (infraestrutura de gerenciamento aberta) usam arquivos MOF (Management Object Format) para descrever as informações disponibilizadas por meio de seus respectivos provedores.

<dl> <dt>

<span id="Active_Directory"></span><span id="active_directory"></span><span id="ACTIVE_DIRECTORY"></span>[Active Directory](/previous-versions/windows/desktop/dsprov/active-directory-provider)
</dt> <dd>

O provedor de Active Directory, também conhecido como provedor de serviços de diretório (DS), mapeia Active Directory objetos para o WMI. Ao acessar o namespace LDAP (Lightweight Directory Access Protocol) no WMI, você pode referenciar ou transformar um objeto em um alias no Active Directory.

</dd> <dt>

<span id="Application_Inventory"></span><span id="application_inventory"></span><span id="APPLICATION_INVENTORY"></span>[Inventário de aplicativos](/previous-versions/windows/desktop/appdevinvprov/applicationanddeviceinventory-portal)
</dt> <dd>

As classes WMI para o inventário de aplicativos habilitam a descoberta dos aplicativos Win32 instalados e dos aplicativos da Windows Store em um sistema Windows.

</dd> <dt>

<span id="Application_Proxy"></span><span id="application_proxy"></span><span id="APPLICATION_PROXY"></span>[Proxy de aplicativo](/previous-versions/windows/desktop/appproxypsprov/application-proxy-wmi-provider-portal)
</dt> <dd>

O provedor WMI de proxy de aplicativo permite que os desenvolvedores acessem o serviço de proxy de aplicativo Web para que os administradores possam publicar aplicativos para acesso externo. O proxy de aplicativo Web é um proxy reverso para Serviços de Federação do Active Directory (AD FS) (AD FS).

</dd> <dt>

<span id="BitLocker_Drive_Encryption__BDE_"></span><span id="bitlocker_drive_encryption__bde_"></span><span id="BITLOCKER_DRIVE_ENCRYPTION__BDE_"></span>[Criptografia de Unidade de Disco BitLocker (BDE)](/windows/desktop/SecProv/bitlocker-drive-encryption-provider)
</dt> <dd>

Fornece configuração e gerenciamento de uma área de armazenamento em uma unidade de disco rígido, representada por uma instância do [**Win32 \_ EncryptableVolume**](/windows/desktop/SecProv/win32-encryptablevolume), que pode ser protegida usando criptografia.

</dd> <dt>

<span id="BITS"></span><span id="bits"></span>[BITS](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> <dd>

O Serviço de Transferência Inteligente em Segundo Plano (BITS) Compact Server com gerenciamento remoto de BITS permite que os administradores autenticados ou aplicativos de controlador criem, modifiquem e gerenciem trabalhos de transferência de BITS remotamente sem usar o serviço de Serviços de Informações da Internet (IIS).

</dd> <dt>

<span id="BizTalk"></span><span id="biztalk"></span><span id="BIZTALK"></span>[BizTalk](https://msdn.microsoft.com/library/ms941491.aspx)
</dt> <dd>

Fornece acesso aos objetos de administração do BizTalk representados por classes WMI.

</dd> <dt>

<span id="Boot_Configuration_Data"></span><span id="boot_configuration_data"></span><span id="BOOT_CONFIGURATION_DATA"></span>[Dados de Configuração da Inicialização](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal)
</dt> <dd>

O provedor de Dados de Configuração da Inicialização (BCD) fornece um repositório que é usado para descrever os aplicativos de inicialização e as configurações do aplicativo de inicialização.

</dd> <dt>

<span id="Boot_Event_Collector"></span><span id="boot_event_collector"></span><span id="BOOT_EVENT_COLLECTOR"></span>[Coletor de eventos de inicialização](/windows/desktop/BEvtColProv/boot-event-collector-wmi-provider-portal)
</dt> <dd>

O provedor WMI do coletor de eventos de inicialização fornece acesso a informações de conexão e configuração para o recurso de coleta de eventos de instalação e inicialização no Windows Server.

</dd> <dt>

<span id="CIMWin32__Win32__Power_Management_Events"></span><span id="cimwin32__win32__power_management_events"></span><span id="CIMWIN32__WIN32__POWER_MANAGEMENT_EVENTS"></span>[CIMWin32, Win32, eventos de gerenciamento de energia](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers)
</dt> <dd>

Os provedores de CIMWin32 dão suporte às classes implementadas no CimWin32.dll e consistem nas principais classes CIM, na implementação do Win32 dessas classes e nos eventos de gerenciamento de energia.

</dd> <dt>

<span id="CIMWin32a"></span><span id="cimwin32a"></span><span id="CIMWIN32A"></span>[CIMWin32a](/previous-versions/windows/desktop/cimwin32a/cimwin32a-provider-classes)
</dt> <dd>

O provedor CIMWin32a estende as classes disponíveis no [CIMWin32](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers).

</dd> <dt>

<span id="DcbQosCim"></span><span id="dcbqoscim"></span><span id="DCBQOSCIM"></span>[DcbQosCim](/previous-versions/windows/desktop/dcbwmiprov/dcb-qos)
</dt> <dd>

O provedor DcbQosCim dá suporte a classes que descrevem dados de configuração de QOS de rede, dados de configuração de controle e dados de configuração de classe de tráfego.

</dd> <dt>

<span id="Distributed_File_System__DFS_"></span><span id="distributed_file_system__dfs_"></span><span id="DISTRIBUTED_FILE_SYSTEM__DFS_"></span>[Sistema de Arquivos Distribuído (DFS)](/previous-versions/windows/desktop/wmipdfs/dfs-provider)
</dt> <dd>

O provedor de DFS fornece funções de DFS programáveis por meio do WMI.

</dd> <dt>

<span id="Distributed_File_System_Replication__DFSR_"></span><span id="distributed_file_system_replication__dfsr_"></span><span id="DISTRIBUTED_FILE_SYSTEM_REPLICATION__DFSR_"></span>[Replicação de Sistema de Arquivos Distribuído (DFSR)](/previous-versions/windows/desktop/dfsr/distributed-file-system-replication--dfsr-)
</dt> <dd>

Cria ferramentas para configurar e monitorar o serviço de [sistema de arquivos distribuído (DFS)](/previous-versions/windows/desktop/dfs/distributed-file-system) . Para obter mais informações, consulte [classes de WMI do DFSR](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes).

</dd> <dt>

<span id="Dfsncimprov"></span><span id="dfsncimprov"></span><span id="DFSNCIMPROV"></span>[Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes)
</dt> <dd>

O provedor [Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes) dá suporte a classes que implementam o acesso de namespace do DFS.

</dd> <dt>

<span id="DhcpServerPSProvider"></span><span id="dhcpserverpsprovider"></span><span id="DHCPSERVERPSPROVIDER"></span>[DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes)
</dt> <dd>

O provedor [DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes) dá suporte a classes que interagem com um servidor DHCP (protocolo de configuração dinâmica de hosts).

</dd> <dt>

<span id="Disk_Quota"></span><span id="disk_quota"></span><span id="DISK_QUOTA"></span>[Cota de disco](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider)
</dt> <dd>

O provedor de cota de disco do Windows permite que os administradores controlem a quantidade de dados que cada usuário armazena em um sistema de arquivos NTFS.

</dd> <dt>

<span id="Distributed_Transaction_Coordinator__DTC_"></span><span id="distributed_transaction_coordinator__dtc_"></span><span id="DISTRIBUTED_TRANSACTION_COORDINATOR__DTC_"></span>[Coordenador de Transações Distribuídas (DTC)](/previous-versions/windows/desktop/msdtcwmi/distributed-transaction-coordinator-wmi-provider-portal)
</dt> <dd>

O provedor DTC permite o gerenciamento do DTC.

</dd> <dt>

<span id="DNS"></span><span id="dns"></span>[DNS](/windows/desktop/DNS/dns-wmi-provider)
</dt> <dd>

Permite que administradores e programadores configurem registros de recursos (RRs) do sistema de nomes de domínio (DNS) e servidores DNS usando o WMI.

</dd> <dt>

<span id="Dnsclientcim_Provider_Classes"></span><span id="dnsclientcim_provider_classes"></span><span id="DNSCLIENTCIM_PROVIDER_CLASSES"></span>[Classes de provedor Dnsclientcim](/previous-versions/windows/desktop/dnsclientcimprov/dns-client-classes)
</dt> <dd>

O provedor Dnsclientcim dá suporte a classes que interagem com um cliente DNS (sistema de nomes de domínio).

</dd> <dt>

<span id="DnsClientPSProvider"></span><span id="dnsclientpsprovider"></span><span id="DNSCLIENTPSPROVIDER"></span>[DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes)
</dt> <dd>

O provedor [DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes) dá suporte a classes WMI que interagem com um cliente DNS.

</dd> <dt>

<span id="DnsServerPSProvider"></span><span id="dnsserverpsprovider"></span><span id="DNSSERVERPSPROVIDER"></span>[DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes)
</dt> <dd>

O provedor [DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes) dá suporte a classes WMI que interagem com um servidor DNS.

</dd> <dt>

<span id="Event_Log"></span><span id="event_log"></span><span id="EVENT_LOG"></span>[Log de eventos](/previous-versions/windows/desktop/eventlogprov/event-log-provider)
</dt> <dd>

O provedor de [log de eventos](/previous-versions/windows/desktop/eventlogprov/event-log-provider) fornece acesso a dados do serviço log de eventos e notificação de eventos.

</dd> <dt>

<span id="Event_Tracing_Management"></span><span id="event_tracing_management"></span><span id="EVENT_TRACING_MANAGEMENT"></span>[Gerenciamento de rastreamento de eventos](/previous-versions/windows/desktop/etwmgmt/event-tracing-management-wmi-provider-portal)
</dt> <dd>

O provedor de gerenciamento de rastreamento de eventos fornece acesso a eventos de rastreamento e configurações de sessão do ETW (rastreamento de eventos para Windows).

</dd> <dt>

<span id="Failover_Cluster-Aware_Updating"></span><span id="failover_cluster-aware_updating"></span><span id="FAILOVER_CLUSTER-AWARE_UPDATING"></span>[Atualização de Cluster-Aware de failover](/previous-versions/windows/desktop/cauwmiv2/failover-cluster-aware-patching-mi-provider-portal)
</dt> <dd>

O provedor de atualização de Cluster-Aware de failover (CAU) dá suporte à coordenação e ao gerenciamento da CAU.

</dd> <dt>

<span id="Failover_Clustering_Hyper-V"></span><span id="failover_clustering_hyper-v"></span><span id="FAILOVER_CLUSTERING_HYPER-V"></span>[Clustering de failover Hyper-V](/previous-versions/windows/desktop/clushyperv/failover-clustering-hyper-v-wmi-provider-portal)
</dt> <dd>

O provedor de clustering de failover do Hyper-V fornece gerenciamento e relatórios do Hyper-V em um ambiente de clustering.

</dd> <dt>

<span id="Failover_Clustering_Storage_QoS"></span><span id="failover_clustering_storage_qos"></span><span id="FAILOVER_CLUSTERING_STORAGE_QOS"></span>[QoS de armazenamento de clustering de failover](/previous-versions/windows/desktop/clusstorageqosprov/failover-clustering-storage-qos-mi-provider-portal)
</dt> <dd>

O provedor de QoS (qualidade de serviço) de armazenamento de clustering de failover fornece gerenciamento e relatórios das políticas de QoS de armazenamento de clustering.

</dd> <dt>

<span id="Failover_Cluster_V1_Provider"></span><span id="failover_cluster_v1_provider"></span><span id="FAILOVER_CLUSTER_V1_PROVIDER"></span>[Provedor de failover de cluster v1](/previous-versions/windows/desktop/cluswmi/failover-cluster-wmi-provider-portal)
</dt> <dd>

O provedor de failover do cluster v1 fornece gerenciamento de um cluster de failover.

</dd> <dt>

<span id="Failover_Cluster_V1_Extensions"></span><span id="failover_cluster_v1_extensions"></span><span id="FAILOVER_CLUSTER_V1_EXTENSIONS"></span>[Extensões v1 do cluster de failover](/previous-versions/windows/desktop/cluswmiext/failover-cluster-wmi-provider-extensions-portal)
</dt> <dd>

O provedor de extensões de cluster de failover fornece gerenciamento adicional de um cluster de failover.

</dd> <dt>

<span id="Gateway_Health_Monitor"></span><span id="gateway_health_monitor"></span><span id="GATEWAY_HEALTH_MONITOR"></span>[Monitor de integridade do gateway](/previous-versions/windows/desktop/gatewayhealthmonprov/gateway-health-monitor-wmi-provider-portal)
</dt> <dd>

O provedor do monitor de integridade do gateway gerencia informações e eventos de monitoramento da integridade do gateway.

</dd> <dt>

<span id="Group_Policy_API"></span><span id="group_policy_api"></span><span id="GROUP_POLICY_API"></span>[API de Política de Grupo](/previous-versions/windows/desktop/Policy/group-policy-start-page)
</dt> <dd>

O provedor de Política de Grupo permite a administração baseada em políticas usando os serviços de diretório do Microsoft Active Directory (AD).

</dd> <dt>

<span id="Host_Guardian_Service"></span><span id="host_guardian_service"></span><span id="HOST_GUARDIAN_SERVICE"></span>[Serviço guardião de host](/previous-versions/windows/desktop/hgsclientwmi/hoster-guardian-service-wmi-provider-portal)
</dt> <dd>

O provedor de serviço guardião de host fornece gerenciamento do serviço guardião de host para VMs blindadas.

</dd> <dt>

<span id="Hyper-V"></span><span id="hyper-v"></span><span id="HYPER-V"></span>[Hyper-V](/previous-versions/windows/desktop/virtual/windows-virtualization-portal)
</dt> <dd>

O provedor do Hyper-V permite que você gerencie e recupere informações sobre máquinas virtuais.

</dd> <dt>

<span id="Hyper-V__V2_"></span><span id="hyper-v__v2_"></span><span id="HYPER-V__V2_"></span>[Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal)
</dt> <dd>

O provedor Hyper-V (v2) estende o provedor do [Hyper-v](/previous-versions/windows/desktop/virtual/windows-virtualization-portal) .

</dd> <dt>

<span id="Internet_Information_Services__IIS_"></span><span id="internet_information_services__iis_"></span><span id="INTERNET_INFORMATION_SERVICES__IIS_"></span>[Serviços de Informações da Internet (IIS)](/previous-versions/iis/6.0-sdk/ms525309(v=vs.90))
</dt> <dd>

Expõe interfaces de programação que podem ser usadas para consultar e configurar a metabase do IIS.

</dd> <dt>

<span id="Internet_Protocol_Address_Management__IPAM__Server"></span><span id="internet_protocol_address_management__ipam__server"></span><span id="INTERNET_PROTOCOL_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>[Servidor de gerenciamento de endereços de protocolo de Internet (IPAM)](/previous-versions/windows/desktop/ipamserverpsprov/internet-protocol-address-management-server-wmi-provider-portal)
</dt> <dd>

O provedor do servidor IPAM permite que os desenvolvedores gerenciem o IPAM por meio do WMI.

</dd> <dt>

<span id="IP_Route_Provider"></span><span id="ip_route_provider"></span><span id="IP_ROUTE_PROVIDER"></span>[Provedor de rotas de IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider)
</dt> <dd>

O provedor de rotas de IP pré-instalado fornece informações de roteamento de rede IPV4, incluindo (mas não se limitando a) as informações disponíveis por meio do comando **Route Print** .

</dd> <dt>

<span id="Intelligent_Platform_Management_Interface__IPMI_"></span><span id="intelligent_platform_management_interface__ipmi_"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE__IPMI_"></span>[IPMI (interface de gerenciamento de plataforma inteligente)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)
</dt> <dd>

Fornece dados de IPMI das operações do controlador BMC.

</dd> <dt>

<span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>[Servidor de destino iSCSI](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)
</dt> <dd>

O provedor do servidor de destino iSCSI dá suporte a uma interface WMI para gerenciar o servidor de destino Microsoft iSCSI, como a criação de discos virtuais e para apresentá-los ao cliente.

</dd> <dt>

<span id="Job_Object"></span><span id="job_object"></span><span id="JOB_OBJECT"></span>[Objeto de trabalho](/previous-versions/windows/desktop/wmipjobobjprov/job-object-provider)
</dt> <dd>

O provedor de objeto de trabalho dá suporte ao acesso a dados sobre objetos de trabalho de kernel nomeados.

</dd> <dt>

<span id="Kernel_Trace"></span><span id="kernel_trace"></span><span id="KERNEL_TRACE"></span>[Rastreamento de kernel](/previous-versions/windows/desktop/krnlprov/kernel-trace-provider)
</dt> <dd>

O provedor de eventos de rastreamento do kernel pré-instalado permite que você veja eventos de rastreamento do kernel na criação do processo, término do processo, criação de threads, término do thread e carregamento do módulo.

</dd> <dt>

<span id="Live_Communications_Server_2003"></span><span id="live_communications_server_2003"></span><span id="LIVE_COMMUNICATIONS_SERVER_2003"></span>[Live Communications Server 2003](/previous-versions/office/developer/office-2003/cc165126(v=office.11))
</dt> <dd>

Fornece classes que criam, registram, configuram e gerenciam aplicativos de SIP (protocolo de iniciação de sessão) personalizados com o [Live Communications Server 2003](/previous-versions/office/aa194012(v=office.11)).

</dd> <dt>

<span id="Management_Tools_Registry"></span><span id="management_tools_registry"></span><span id="MANAGEMENT_TOOLS_REGISTRY"></span>[Registro de ferramentas de gerenciamento](/previous-versions/windows/desktop/mtregprov/managementtools-registry-wmi-provider-portal)
</dt> <dd>

O provedor de registro das ferramentas de gerenciamento fornece acesso remoto ao registro.

</dd> <dt>

<span id="Management_Tools_Task_Manager"></span><span id="management_tools_task_manager"></span><span id="MANAGEMENT_TOOLS_TASK_MANAGER"></span>[Gerenciador de tarefas das ferramentas de gerenciamento](/previous-versions/windows/desktop/mttmprov/management-tools-task-manager-wmi-provider-portal)
</dt> <dd>

O provedor do Gerenciador de tarefas das ferramentas de gerenciamento fornece acesso e gerenciamento dos dados do Gerenciador de tarefas.

</dd> <dt>

<span id="MDM_Application"></span><span id="mdm_application"></span><span id="MDM_APPLICATION"></span>[Aplicativo MDM](/previous-versions/windows/desktop/mdmappprov/mobile-device-management-application-provider-portal)
</dt> <dd>

O provedor de aplicativos de MDM (gerenciamento de dispositivo móvel) gerencia aplicativos em dispositivos que são assinados para o serviço MDM.

</dd> <dt>

<span id="MDM_Bridge"></span><span id="mdm_bridge"></span><span id="MDM_BRIDGE"></span>[Ponte MDM](/windows/desktop/DMWmiBridgeProv/mdm-bridge-wmi-provider-portal)
</dt> <dd>

O provedor de ponte do MDM habilita o gerenciamento de MDM de uma ponte de rede.

</dd> <dt>

<span id="MDM_Settings"></span><span id="mdm_settings"></span><span id="MDM_SETTINGS"></span>[Configurações do MDM](/previous-versions/windows/desktop/mdmsettingsprov/mobile-device-management-settings-provider-portal)
</dt> <dd>

O provedor de configurações do MDM permite o gerenciamento de configurações em dispositivos registrados com um serviço MDM.

</dd> <dt>

<span id="MSFT_PCSVDevice"></span><span id="msft_pcsvdevice"></span><span id="MSFT_PCSVDEVICE"></span>[\_PCSVDEVICE MSFT](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes)
</dt> <dd>

O provedor [MSFT \_ PCSVDevice](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes) expõe uma classe que define uma classe de exibição para um sistema de computador físico.

</dd> <dt>

<span id="MsNetImPlatform"></span><span id="msnetimplatform"></span><span id="MSNETIMPLATFORM"></span>[MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes)
</dt> <dd>

A seção provedor [MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes) fornece informações de referência para classes de provedor MsNetImPlatform implementadas no NdisIMPlatCim.dll.

</dd> <dt>

<span id="NetAdapterCim"></span><span id="netadaptercim"></span><span id="NETADAPTERCIM"></span>[NetAdapterCim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes)
</dt> <dd>

O provedor [NetAdapterCim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes) dá suporte a classes que acessam adaptadores de rede.

</dd> <dt>

<span id="NetDaCim"></span><span id="netdacim"></span><span id="NETDACIM"></span>[NetDaCim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes)
</dt> <dd>

Esta seção fornece informações de referência para classes de provedor [NetDaCim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes) .

</dd> <dt>

<span id="NetNcCim"></span><span id="netnccim"></span><span id="NETNCCIM"></span>[NetNcCim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status)
</dt> <dd>

Fornece informações de referência para classes de provedor [NetNcCim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status) .

</dd> <dt>

<span id="NetPeerDist"></span><span id="netpeerdist"></span><span id="NETPEERDIST"></span>[NetPeerDist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache)
</dt> <dd>

O provedor [NetPeerDist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache) dá suporte a classes que interagem com a infraestrutura de cache de ramificação.

</dd> <dt>

<span id="NetQosCim"></span><span id="netqoscim"></span><span id="NETQOSCIM"></span>[NetQosCim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes)
</dt> <dd>

O provedor [NetQosCim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes) fornece dados para a qualidade de serviço de rede (QoS) e dados de configuração de QoS.

</dd> <dt>

<span id="NetSwitchTeam"></span><span id="netswitchteam"></span><span id="NETSWITCHTEAM"></span>[NetSwitchTeam](/previous-versions/windows/desktop/netswitchteamprov/network-switch-team-classes)
</dt> <dd>

Esta seção fornece informações de referência para classes de provedor NetSwitchTeam declaradas em NetSwitchTeam. mof e implementadas no NetSwitchTeamCim.dll.

</dd> <dt>

<span id="NetTCPIP"></span><span id="nettcpip"></span><span id="NETTCPIP"></span>[Nettcpip](/previous-versions/windows/desktop/nettcpipprov/net-tcpip-classes)
</dt> <dd>

O provedor nettcpip dá suporte a classes que interagem com conexões TCPIP.

</dd> <dt>

<span id="NetTtCim"></span><span id="netttcim"></span><span id="NETTTCIM"></span>[NetTtCim](/previous-versions/windows/desktop/netttcimprov/network-transition-classes)
</dt> <dd>

Esta seção fornece informações de referência para as classes de provedor NetTtCim definidas em NetTtCim. mof e implementadas no NetTtCim.dll.

</dd> <dt>

<span id="NetWNV"></span><span id="netwnv"></span><span id="NETWNV"></span>[NetWNV](/previous-versions/windows/desktop/netwnvprov/net-virtualization-classes)
</dt> <dd>

O provedor NetWNV dá suporte a classes que interagem com as tecnologias de virtualização .net.

</dd> <dt>

<span id="Network_Access_Protection"></span><span id="network_access_protection"></span><span id="NETWORK_ACCESS_PROTECTION"></span>[Proteção de acesso à rede](/previous-versions/windows/desktop/napprov/network-access-protection-wmi-provider-portal)
</dt> <dd>

O provedor de proteção de acesso à rede expõe uma plataforma para acesso protegido a redes privadas.

</dd> <dt>

<span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>[Balanceamento de carga de rede](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-portal)
</dt> <dd>

O provedor NLB (balanceamento de carga de rede) permite o gerenciamento de um cluster NLB.

</dd> <dt>

<span id="NetworkController_Server"></span><span id="networkcontroller_server"></span><span id="NETWORKCONTROLLER_SERVER"></span>[Servidor NetworkController](/previous-versions/windows/desktop/ncserverpsprov/networkcontroller-server-wmi-provider-portal)
</dt> <dd>

O provedor habilita o gerenciamento de um servidor do controlador de rede.

</dd> <dt>

<span id="NFS"></span><span id="nfs"></span>[-](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)
</dt> <dd>

O provedor de NFS permite que você crie ferramentas e scripts para configurar e monitorar o sistema de arquivos de rede do Windows.

</dd> <dt>

<span id="Ping"></span><span id="ping"></span><span id="PING"></span>[Executar](/previous-versions/windows/desktop/wmipicmp/ping-provider)
</dt> <dd>

O provedor de ping fornece acesso às informações de status fornecidas pelo comando ping padrão.

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>[Regras](/previous-versions/windows/desktop/policmanprov/policy-provider)
</dt> <dd>

Fornece extensões para a diretiva de grupo e permite refinamentos na aplicação da política.

</dd> <dt>

<span id="Power_Meter"></span><span id="power_meter"></span><span id="POWER_METER"></span>[Medidor de energia](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-)
</dt> <dd>

O provedor do medidor de energia dá suporte à interface de medição de energia e orçamento (PMB). Essas classes são a interface primária para a consulta de informações de PMI (interface do Power medidor) de medidores de energia subjacentes no sistema.

</dd> <dt>

<span id="Power_Policy"></span><span id="power_policy"></span><span id="POWER_POLICY"></span>[Política de energia](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-)
</dt> <dd>

O provedor de política de energia fornece às classes a capacidade de gerenciar remotamente toda a infraestrutura de diretiva de energia.

</dd> <dt>

<span id="RAMgmtPSProvider"></span><span id="ramgmtpsprovider"></span><span id="RAMGMTPSPROVIDER"></span>[RAMgmtPSProvider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management)
</dt> <dd>

O provedor [RAMgmtPSProvider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management) fornece classes para gerenciar o acesso remoto.

</dd> <dt>

<span id="RAServerPSProvider"></span><span id="raserverpsprovider"></span><span id="RASERVERPSPROVIDER"></span>[RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server)
</dt> <dd>

O provedor [RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server) fornece classes para gerenciar o servidor de acesso remoto.

</dd> <dt>

<span id="ReliabilityMetricsProvider"></span><span id="reliabilitymetricsprovider"></span><span id="RELIABILITYMETRICSPROVIDER"></span>[ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes)
</dt> <dd>

O provedor [ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes) expõe as métricas de confiabilidade do log de eventos do sistema e do Windows.

</dd> <dt>

<span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>[Serviços de Área de Trabalho Remota](/windows/desktop/TermServ/terminal-services-wmi-provider)
</dt> <dd>

Habilita a administração de servidor consistente em um ambiente Serviços de Área de Trabalho Remota.

</dd> <dt>

<span id="Reporting_Services"></span><span id="reporting_services"></span><span id="REPORTING_SERVICES"></span>[Reporting Services](https://msdn.microsoft.com/library/Aa226200.aspx)
</dt> <dd>

Define classes que permitem que você escreva scripts e código para modificar as configurações do servidor de relatório e o Gerenciador de Relatórios.

</dd> <dt>

<span id="Resultant_Set_of_Policy__RSoP_"></span><span id="resultant_set_of_policy__rsop_"></span><span id="RESULTANT_SET_OF_POLICY__RSOP_"></span>[Conjunto de políticas resultante (RSoP)](/previous-versions/windows/desktop/Policy/reporting-group-policy)
</dt> <dd>

Fornece métodos para planejar e depurar configurações de política em uma situação de hipóteses. Esses métodos permitem que os administradores determinem facilmente a combinação de configurações de diretiva que se aplicam ao, ou aplicam-se a um usuário ou computador. Isso é conhecido como conjunto de diretivas resultante (RSoP). Para obter mais informações, consulte [sobre o provedor de método do WMI do RSoP](/previous-versions/windows/desktop/Policy/about-the-rsop-wmi-method-provider) e [classes WMI do RSoP](/previous-versions/windows/desktop/Policy/rsop-wmi-classes).

</dd> <dt>

<span id="Security"></span><span id="security"></span><span id="SECURITY"></span>[Segurança](/previous-versions/windows/desktop/secrcw32prov/security-provider)
</dt> <dd>

Recupera ou altera as configurações de segurança que controlam a propriedade, a auditoria e os direitos de acesso a arquivos, diretórios e compartilhamentos.

</dd> <dt>

<span id="ServerManager.DeploymentProvider"></span><span id="servermanager.deploymentprovider"></span><span id="SERVERMANAGER.DEPLOYMENTPROVIDER"></span>[ServerManager. deploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment)
</dt> <dd>

O [ServerManager. deploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment) expõe a funcionalidade de implantação.

</dd> <dt>

<span id="Session"></span><span id="session"></span><span id="SESSION"></span>[Sessão](/previous-versions/windows/desktop/wmipsess/session-provider)
</dt> <dd>

Gerencia sessões de rede e conexões.

</dd> <dt>

<span id="Shadow_Copy"></span><span id="shadow_copy"></span><span id="SHADOW_COPY"></span>[Cópia de sombra](/previous-versions/windows/desktop/vsswmi/shadow-copy-provider)
</dt> <dd>

Fornece funções de gerenciamento para as cópias de sombra do recurso de pastas compartilhadas.

</dd> <dt>

<span id="Shielded_VM_Provisioning"></span><span id="shielded_vm_provisioning"></span><span id="SHIELDED_VM_PROVISIONING"></span>[Provisionamento de VM blindada](/previous-versions/windows/desktop/mspsprov/shielded-vm-provisioning-wmi-provider-portal)
</dt> <dd>

O provedor de provisionamento de VM blindada permite que um controlador de malha inicie o provisionamento seguro de uma VM blindada em um host Hyper-V.

</dd> <dt>

<span id="Shielded_VM_Provisioning_Service"></span><span id="shielded_vm_provisioning_service"></span><span id="SHIELDED_VM_PROVISIONING_SERVICE"></span>[Serviço de provisionamento de VM blindada](/previous-versions/windows/desktop/mspsserviceprov/shielded-vm-provisioning-service-wmi-provider-portal)
</dt> <dd>

O provedor habilita o provisionamento de uma máquina virtual blindada.

</dd> <dt>

<span id="SMB_Management"></span><span id="smb_management"></span><span id="SMB_MANAGEMENT"></span>[Gerenciamento de SMB](/previous-versions/windows/desktop/smb/smb-management-api-portal)
</dt> <dd>

A API de gerenciamento de SMB fornece classes e métodos para gerenciar compartilhamentos e compartilhar o acesso.

</dd> <dt>

<span id="SNMP"></span><span id="snmp"></span>[Gets](/windows/desktop/WmiSdk/snmp-provider)
</dt> <dd>

Mapeia objetos SNMP (Simple Network Management Protocol) que são definidos em objetos de esquema da MIB (base de informações de gerenciamento) para classes. Para obter mais informações, consulte [Configurando o ambiente WMI SNMP](/windows/desktop/WmiSdk/setting-up-the-wmi-snmp-environment).

</dd> <dt>

<span id="Software_Inventory_Logging"></span><span id="software_inventory_logging"></span><span id="SOFTWARE_INVENTORY_LOGGING"></span>[Log de inventário de software](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)
</dt> <dd>

O provedor de log de inventário de software coleta dados de licenciamento sobre o software instalado em um servidor Windows e fornece acesso remoto aos dados para que eles possam ser agregados facilmente por um datacenter.

</dd> <dt>

<span id="Software_Licensing_for_"></span><span id="software_licensing_for_"></span><span id="SOFTWARE_LICENSING_FOR_"></span>[Licenciamento de software para Windows Vista](/previous-versions/windows/desktop/slwmiprov/software-licensing-classes-for-windows-vista)
</dt> <dd>

[Classes de licenciamento de software](/previous-versions/windows/desktop/sppwmi/software-license-provider-) usadas para o Windows Vista.

</dd> <dt>

<span id="Software_License"></span><span id="software_license"></span><span id="SOFTWARE_LICENSE"></span>[Licença de software](/previous-versions/windows/desktop/sppwmi/software-license-provider-)
</dt> <dd>

O provedor de licenciamento de software recupera dados de licenciamento de software.

</dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>[Volume de armazenamento](/previous-versions/windows/desktop/vdswmi/storage-volume-provider)
</dt> <dd>

O provedor de volume de armazenamento fornece funções de gerenciamento de volume.

</dd> <dt>

<span id="Storage_Replica"></span><span id="storage_replica"></span><span id="STORAGE_REPLICA"></span>[Réplica de armazenamento](/previous-versions/windows/desktop/wvrcimprov/storage-replica-mi-provider-portal)
</dt> <dd>

O provedor habilita o gerenciamento de uma réplica de armazenamento.

</dd> <dt>

<span id="System_Registry"></span><span id="system_registry"></span><span id="SYSTEM_REGISTRY"></span>[Registro do sistema](/previous-versions/windows/desktop/regprov/system-registry-provider)
</dt> <dd>

O provedor de registro do sistema permite que os aplicativos de gerenciamento recuperem e modifiquem dados no registro do sistema e recebam notificações quando ocorrerem alterações.

</dd> <dt>

<span id="System_Restore"></span><span id="system_restore"></span><span id="SYSTEM_RESTORE"></span>[Restauração do sistema](/windows/desktop/sr/system-restore-portal)
</dt> <dd>

Fornece classes que configuram e usam a funcionalidade de restauração do sistema. Para obter mais informações, consulte [Configurando a restauração do sistema](/windows/desktop/sr/configuring-system-restore) e as [classes WMI de restauração do sistema](/windows/desktop/sr/system-restore-wmi-classes).

</dd> <dt>

<span id="Trusted_Platform_Module"></span><span id="trusted_platform_module"></span><span id="TRUSTED_PLATFORM_MODULE"></span>[Trusted Platform Module](/windows/desktop/SecProv/trusted-platform-module-provider)
</dt> <dd>

Fornece acesso a dados sobre um dispositivo de segurança, representado por uma instância [**do \_ TPM do Win32**](/windows/desktop/SecProv/win32-tpm), que é a raiz de confiança para um sistema de computador da plataforma confiável do Microsoft Windows.

</dd> <dt>

<span id="Trustmon"></span><span id="trustmon"></span><span id="TRUSTMON"></span>[Trustmon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider)
</dt> <dd>

O provedor [TrustMon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider) é um provedor de instância que cria classes com informações sobre as relações de confiança entre domínios.

</dd> <dt>

<span id="User_Access_Logging"></span><span id="user_access_logging"></span><span id="USER_ACCESS_LOGGING"></span>[Log de acesso do usuário](/previous-versions/windows/desktop/ual/user-access-logging)
</dt> <dd>

O registro de acesso do usuário (UAL) é uma estrutura comum para funções do Windows Server para relatar suas respectivas métricas de consumo.

</dd> <dt>

<span id="UserProfileProvider"></span><span id="userprofileprovider"></span><span id="USERPROFILEPROVIDER"></span>[Userprofileprovider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes)
</dt> <dd>

O provedor [Userprofileprovider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes) expõe classes que fornecem informações sobre um perfil de usuário em um sistema Windows, bem como o status de integridade de uma pasta de usuário redirecionada.

</dd> <dt>

<span id="User_State_Management"></span><span id="user_state_management"></span><span id="USER_STATE_MANAGEMENT"></span>[Gerenciamento de estado do usuário](/previous-versions/windows/desktop/usm/user-state-management-api-portal)
</dt> <dd>

O provedor de gerenciamento de estado do usuário expõe uma API de gerenciamento e relatórios para cenários empresariais.

</dd> <dt>

<span id="View"></span><span id="view"></span><span id="VIEW"></span>[Exibição](/windows/desktop/WmiSdk/view-provider)
</dt> <dd>

Cria novas instâncias e métodos com base em instâncias de outras classes. Duas versões do provedor de exibição estão disponíveis em plataformas de 64 bits.

</dd> <dt>

<span id="VPNClientPSProvider"></span><span id="vpnclientpsprovider"></span><span id="VPNCLIENTPSPROVIDER"></span>[VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client)
</dt> <dd>

O provedor [VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client) expõe uma plataforma para automatizar a conectividade a um cliente de rede virtual privada.

</dd> <dt>

<span id="WDM"></span><span id="wdm"></span>[WDM](/windows/desktop/WmiCoreProv/wdm-provider)
</dt> <dd>

Fornece acesso às classes, instâncias, métodos e eventos de drivers de hardware que estão em conformidade com o Windows Driver Model (WDM).

</dd> <dt>

<span id="WFasCim"></span><span id="wfascim"></span><span id="WFASCIM"></span>[WFasCim](/previous-versions/windows/desktop/wfascimprov/network-security-classes)
</dt> <dd>

O provedor [WFasCim](/previous-versions/windows/desktop/wfascimprov/network-security-classes) expõe os recursos de filtragem e segurança de rede.

</dd> <dt>

<span id="WhqlProvider"></span><span id="whqlprovider"></span><span id="WHQLPROVIDER"></span>[Whqlprovider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes)
</dt> <dd>

O provedor [whqlprovider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes) expõe informações de assinatura digital sobre drivers.

</dd> <dt>

<span id="Win32ClockProvider"></span><span id="win32clockprovider"></span><span id="WIN32CLOCKPROVIDER"></span>[Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes)
</dt> <dd>

O provedor [Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes) expõe os carimbos de data/hora atuais, locais e UTC em um sistema de computador.

</dd> <dt>

<span id="Windows_Data_Access_Components__WDAC_"></span><span id="windows_data_access_components__wdac_"></span><span id="WINDOWS_DATA_ACCESS_COMPONENTS__WDAC_"></span>[Componentes de acesso a dados do Windows (WDAC)](/previous-versions/windows/desktop/wdacwmiprov/windows-data-access-components-wmi-provider-portal)
</dt> <dd>

Fornece gerenciamento de WDAC.

</dd> <dt>

<span id="Windows_Defender"></span><span id="windows_defender"></span><span id="WINDOWS_DEFENDER"></span>[Windows Defender](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)
</dt> <dd>

O provedor do Windows Defender expõe os recursos de segurança do Windows Defender.

</dd> <dt>

<span id="Windows_Installer"></span><span id="windows_installer"></span><span id="WINDOWS_INSTALLER"></span>[Windows Installer](/previous-versions/windows/desktop/msiprov/windows-installer-provider)
</dt> <dd>

O provedor de Windows Installer, também conhecido como o provedor MSI, permite que os aplicativos acessem informações coletadas de Windows Installer aplicativos compatíveis.

</dd> <dt>

<span id="Windows_Product_Activation"></span><span id="windows_product_activation"></span><span id="WINDOWS_PRODUCT_ACTIVATION"></span>[Ativação do produto Windows](/previous-versions/windows/desktop/licwmiprov/windows-product-activation-provider)
</dt> <dd>

O provedor de ativação de produto do Windows (WPA) é uma tecnologia antipirataria que visa reduzir a cópia casual do software.

</dd> <dt>

<span id="Windows_Server_Manager"></span><span id="windows_server_manager"></span><span id="WINDOWS_SERVER_MANAGER"></span>[Gerenciador do Servidor do Windows](/previous-versions/windows/desktop/mgmtprovider/windows-server-manager-wmi-provider-portal)
</dt> <dd>

O provedor permite o acesso e o gerenciamento da configuração controlada pelo aplicativo Gerenciador do Servidor.

</dd> <dt>

<span id="Windows_Server_Storage_Management__MsftStrgMan_"></span><span id="windows_server_storage_management__msftstrgman_"></span><span id="WINDOWS_SERVER_STORAGE_MANAGEMENT__MSFTSTRGMAN_"></span>[MsftStrgMan (gerenciamento de armazenamento do Windows Server)](/previous-versions/windows/desktop/msftstrgmanprov/windows-storage-management-wmi-provider-portal)
</dt> <dd>

O provedor MsftStrgMan fornece gerenciamento para sistemas de armazenamento em produtos Windows Server.

</dd> <dt>

<span id="Windows_Storage_Management__StrgMgmt_"></span><span id="windows_storage_management__strgmgmt_"></span><span id="WINDOWS_STORAGE_MANAGEMENT__STRGMGMT_"></span>[StrgMgmt (gerenciamento de armazenamento do Windows)](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
</dt> <dd>

O provedor StrgMgmt pode ser usado para gerenciar uma ampla gama de configurações de armazenamento, de tablets a matrizes de armazenamento externo em servidores.

</dd> <dt>

<span id="Windows_System_Assessment_Tool"></span><span id="windows_system_assessment_tool"></span><span id="WINDOWS_SYSTEM_ASSESSMENT_TOOL"></span>[Ferramenta de avaliação do sistema do Windows](/windows/desktop/WinSAT/winsat-mof-classes)
</dt> <dd>

A ferramenta de avaliação de sistema do Windows (WinSAT) expõe várias classes que avaliam as características e os recursos de desempenho de um computador.

</dd> <dt>

<span id="WMI_Core"></span><span id="wmi_core"></span><span id="WMI_CORE"></span>[Núcleo do WMI](/windows/desktop/WmiCoreProv/wmi-core-provider-)
</dt> <dd>

O provedor WMI Core define classes que compõem a funcionalidade básica do WMI.

</dd> <dt>

<span id="Msft_ProviderSubSystem"></span><span id="msft_providersubsystem"></span><span id="MSFT_PROVIDERSUBSYSTEM"></span>[\_ProviderSubSystem MSFT](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-)
</dt> <dd>

O provedor [MSFT \_ ProviderSubSystem](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-) dá suporte a provedores.

</dd> <dt>

<span id="Win32_Perf"></span><span id="win32_perf"></span><span id="WIN32_PERF"></span>[Desempenho do Win32 \_](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov)
</dt> <dd>

A classe abstrata de desempenho do [**\_ Win32**](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov) é a classe base para as classes de contador de desempenho [**Win32 \_ PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) e [**Win32 \_ PerfFormattedData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov). Ele define as propriedades necessárias de carimbo de data/hora e frequência usadas nos algoritmos de tipo de contador para as classes de contadores de desempenho.

</dd> <dt>

<span id="Win32_PerfFormattedData"></span><span id="win32_perfformatteddata"></span><span id="WIN32_PERFFORMATTEDDATA"></span>[**\_PerfFormattedData Win32**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov)
</dt> <dd>

Uma classe base abstrata para as classes de dados previamente instaladas, calculadas.

</dd> <dt>

<span id="Win32_PerfRawData"></span><span id="win32_perfrawdata"></span><span id="WIN32_PERFRAWDATA"></span>[**\_PerfRawData Win32**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov)
</dt> <dd>

A classe de contador de desempenho [**Win32 \_ PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) é a classe base abstrata para todas as classes de contador de desempenho brutos concretos. Para aparecer no monitor do sistema, as classes do contador de desempenho devem ser adicionadas ao namespace "raiz \\ CIMv2" e derivadas do **Win32 \_ PerfRawData**.

</dd> <dt>

<span id="WMIPerfClass"></span><span id="wmiperfclass"></span><span id="WMIPERFCLASS"></span>[WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider)
</dt> <dd>

Cria as [classes do contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes)WMI. Os dados são fornecidos dinamicamente para essas classes de desempenho pelo provedor WMIPerfInst.

</dd> <dt>

<span id="WmiPerfInst"></span><span id="wmiperfinst"></span><span id="WMIPERFINST"></span>[WmiPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider)
</dt> <dd>

Fornece dados de contador de desempenho brutos e formatados dinamicamente das definições de [classe do contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes) .

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>[Pastas de trabalho](/previous-versions/windows/desktop/syncshareservermgmt/sync-share-server-management-portal)
</dt> <dd>

As pastas de trabalho são usadas para sincronizar arquivos com vários computadores e dispositivos móveis.

</dd> </dl>

 

 
