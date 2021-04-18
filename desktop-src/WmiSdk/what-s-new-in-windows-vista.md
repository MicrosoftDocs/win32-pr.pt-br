---
description: A partir do Windows Vista, o WMI contém muitos recursos novos com base em solicitações por usuários WMI.
ms.assetid: 604a86d2-9a8e-4266-93b8-13676f768b29
ms.tgt_platform: multiple
title: O que há de novo no Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee950becb906f89445f9ddfb258f4f7a608ce1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812247"
---
# <a name="whats-new-in-windowsvista"></a>O que há de novo no Windows Vista

A partir do Windows Vista, o WMI contém muitos recursos novos com base em solicitações por usuários WMI.

-   [Nova ferramenta de solução de problemas](#new-troubleshooting-tool)
-   [Novos recursos de segurança do Windows Vista](#new-security-features-in-windows-vista)
-   [Outros novos recursos do Windows Vista](#other-new-features-in-windows-vista)
-   [Tópicos relacionados](#related-topics)

## <a name="new-troubleshooting-tool"></a>Nova ferramenta de solução de problemas

Uma nova ferramenta de solução de problemas está disponível para download.

<dl> <dt>

<span id="WMI_Diagnosis_Utility"></span><span id="wmi_diagnosis_utility"></span><span id="WMI_DIAGNOSIS_UTILITY"></span>Utilitário de Diagnóstico WMI
</dt> <dd>

Esse utilitário examina o estado atual do serviço WMI e os componentes relacionados, as configurações do DCOM e as configurações do registro no computador local. O utilitário relata problemas e oferece sugestões de reparo. Para obter mais informações e baixar o utilitário, consulte [Utilitário de diagnóstico WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en).

</dd> </dl>

## <a name="new-security-features-in-windows-vista"></a>Novos recursos de segurança do Windows Vista

A lista a seguir lista os novos recursos de segurança do WMI que estão disponíveis no Windows Vista.

<dl> <dt>

<span id="Tracing_and_logging_events"></span><span id="tracing_and_logging_events"></span><span id="TRACING_AND_LOGGING_EVENTS"></span>Eventos de rastreamento e log
</dt> <dd>

O serviço WMI não usa mais os [arquivos de log do WMI](wmi-log-files.md). Em vez disso, ele usa o ETW ( [rastreamento de eventos](/windows/desktop/ETW/event-tracing-portal) ) e eventos estão disponíveis por meio da interface do usuário do **Visualizador de eventos** ou da ferramenta de linha de comando wevtutil. Para obter mais informações, consulte [rastreando a atividade WMI](tracing-wmi-activity.md).

</dd> <dt>

<span id="Setting_WMI_namespace_security_in_the_MOF_file"></span><span id="setting_wmi_namespace_security_in_the_mof_file"></span><span id="SETTING_WMI_NAMESPACE_SECURITY_IN_THE_MOF_FILE"></span>Definindo a segurança do namespace WMI no arquivo MOF
</dt> <dd>

O qualificador **NamespaceSecuritySDDL** pode ser usado para proteger qualquer namespace. Para obter mais informações, consulte [definindo a segurança do namespace quando o namespace é criado](setting-namespace-security-when-the-namespace-is-created.md).

</dd> <dt>

<span id="Security_Auditing_of_WMI_namespaces"></span><span id="security_auditing_of_wmi_namespaces"></span><span id="SECURITY_AUDITING_OF_WMI_NAMESPACES"></span>Auditoria de segurança de namespaces do WMI
</dt> <dd>

O WMI usa a SACL (listas de controle de acesso) do sistema de namespace para auditar a atividade do namespace e relatar eventos para o log de eventos de segurança. Para obter mais informações, consulte [acesso aos namespaces do WMI](access-to-wmi-namespaces.md) e [Configurando descritores de segurança de namespace](setting-namespace-security-descriptors.md).

</dd> <dt>

<span id="Get_and_Set_security_descriptor_methods_for_securable_objects"></span><span id="get_and_set_security_descriptor_methods_for_securable_objects"></span><span id="GET_AND_SET_SECURITY_DESCRIPTOR_METHODS_FOR_SECURABLE_OBJECTS"></span>Obter e definir métodos de descritor de segurança para objetos protegíveis
</dt> <dd>

Novos métodos programáveis para obter e definir descritores de segurança foram adicionados à [**\_ impressora Win32**](/windows/desktop/CIMWin32Prov/win32-printer), [**\_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), [**Win32 \_ DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)e [**\_ \_ SystemSecurity**](--systemsecurity.md). Para obter mais informações, consulte [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md).

</dd> <dt>

<span id="Manipulate_Security_Descriptors_in_scripts"></span><span id="manipulate_security_descriptors_in_scripts"></span><span id="MANIPULATE_SECURITY_DESCRIPTORS_IN_SCRIPTS"></span>Manipular descritores de segurança em scripts
</dt> <dd>

A classe [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) tem métodos que permitem que os scripts convertam descritores de segurança binários em objetos protegíveis em objetos do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) ou em cadeias de caracteres da [linguagem de definição do descritor de segurança](/windows/desktop/SecAuthZ/security-descriptor-definition-language) . Para obter mais informações, consulte [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md).

</dd> <dt>

<span id="User_Account_Control"></span><span id="user_account_control"></span><span id="USER_ACCOUNT_CONTROL"></span>Controle de conta de usuário
</dt> <dd>

O UAC (controle de conta de usuário) afeta quais dados do WMI são retornados, acesso remoto e como os scripts devem ser executados. Para obter mais informações, consulte [controle de conta de usuário e WMI](user-account-control-and-wmi.md). Para obter mais informações sobre o UAC, consulte [introdução com o controle de conta de usuário no Windows Vista](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).

</dd> </dl>

## <a name="other-new-features-in-windows-vista"></a>Outros novos recursos do Windows Vista

A lista a seguir lista os novos recursos do WMI que estão disponíveis no Windows Vista.

<dl> <dt>

<span id="New_performance_counter_data_providers"></span><span id="new_performance_counter_data_providers"></span><span id="NEW_PERFORMANCE_COUNTER_DATA_PROVIDERS"></span>Novos provedores de dados do contador de desempenho
</dt> <dd>

O processo de descoberta automática/autolimpeza (ADAP) não transfere mais objetos de contador de desempenho para classes de desempenho WMI no repositório WMI. Para obter mais informações, consulte [bibliotecas de desempenho e WMI](performance-libraries-and-wmi.md). O [provedor WMIPerfClass](wmiperfclass-provider.md) cria as classes do contador de desempenho WMI. Os dados são fornecidos dinamicamente para essas classes de desempenho WMI pelo [provedor WMIPerfInst](wmiperfinst-provider.md).

</dd> <dt>

<span id="Indexer_for_collections"></span><span id="indexer_for_collections"></span><span id="INDEXER_FOR_COLLECTIONS"></span>Indexador para coleções
</dt> <dd>

O método [**SWbemObject. ItemIndex**](swbemobjectset-itemindex.md) retorna o objeto associado a um índice especificado em uma coleção.

</dd> <dt>

<span id="Support_for_IPv6_and_IPv4"></span><span id="support_for_ipv6_and_ipv4"></span><span id="SUPPORT_FOR_IPV6_AND_IPV4"></span>Suporte para IPv6 e IPv4
</dt> <dd>

O [provedor de rotas IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) WMI e as classes de rede fornecem dados para endereços IPv4. A partir do Windows Vista, o WMI também fornece suporte limitado para recursos de rede IPv6. Para obter mais informações, consulte [suporte a IPv6 e IPv4 no WMI](ipv6-and-ipv4-support-in-wmi.md).

</dd> <dt>

<span id="Changes_to_remote_connections"></span><span id="changes_to_remote_connections"></span><span id="CHANGES_TO_REMOTE_CONNECTIONS"></span>Alterações em conexões remotas
</dt> <dd>

Conectar-se a um namespace do WMI em um computador remoto que executa o Windows Vista pode exigir alterações nas configurações do [Firewall do Windows](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx), controle de [conta de usuário](/previous-versions/aa905108(v=msdn.10))ou DCOM. Para obter mais informações, consulte [conectando-se ao WMI remotamente a partir do vista](connecting-to-wmi-remotely-starting-with-vista.md).

</dd> <dt>

<span id="Changes_to_________Win32_QuickFixEngineering"></span><span id="changes_to_________win32_quickfixengineering"></span><span id="CHANGES_TO_________WIN32_QUICKFIXENGINEERING"></span>Alterações no [ **Win32 \_ QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)
</dt> <dd>

Para sistemas em execução no sistema operacional Windows Vista e posterior, essa classe retorna apenas as atualizações fornecidas pela CBS (serviço baseado em componente). Essas atualizações não estão listadas no registro. As atualizações fornecidas pelo Windows Installer (MSI) ou pelo [Windows Update](https://update.microsoft.com/microsoftupdate/v6/default.aspx?ln=en-us) não são retornadas pelo [**Win32 \_ QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering).

</dd> <dt>

<span id="Enabling_and_disabling_a_NIC"></span><span id="enabling_and_disabling_a_nic"></span><span id="ENABLING_AND_DISABLING_A_NIC"></span>Habilitando e desabilitando uma NIC
</dt> <dd>

[**Win32 \_ O adaptador**](/windows/desktop/CIMWin32Prov/win32-networkadapter) tem novos métodos para habilitar e desabilitar o adaptador de rede.

</dd> <dt>

<span id="Windows_Installer_Provider_changes"></span><span id="windows_installer_provider_changes"></span><span id="WINDOWS_INSTALLER_PROVIDER_CHANGES"></span>Alterações do provedor de Windows Installer
</dt> <dd>

[**Win32 \_ O produto**](/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)) tem novas propriedades e métodos para fornecer mais dados sobre o produto.

</dd> <dt>

<span id="New_display_monitor_classes"></span><span id="new_display_monitor_classes"></span><span id="NEW_DISPLAY_MONITOR_CLASSES"></span>Novas classes de monitor de exibição
</dt> <dd>

As [classes de exibição do monitor](/windows/desktop/WmiCoreProv/wmi-core-provider-) contêm dados fornecidos pelo [provedor WDM](/windows/desktop/WmiCoreProv/wdm-provider) que fornece dados sobre monitores de exibição.

</dd> <dt>

<span id="Intelligent_Platform_Management_Interface_provider"></span><span id="intelligent_platform_management_interface_provider"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE_PROVIDER"></span>Provedor de interface de gerenciamento de plataforma inteligente
</dt> <dd>

O [provedor WMI IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) fornece dados das operações do controlador BMC (Baseboard Management Controller) para o sistema operacional. O provedor fornece informações para as classes de informações de gerenciamento de plataforma inteligente, que fornecem dados de sensores e dados de mensagem do SEL (log de eventos do sistema) do BMC.

</dd> <dt>

<span id="Detecting_hyperthreading_and_multicore_processors"></span><span id="detecting_hyperthreading_and_multicore_processors"></span><span id="DETECTING_HYPERTHREADING_AND_MULTICORE_PROCESSORS"></span>Detectando processadores de hyperthreading e vários núcleos
</dt> <dd>

[**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-computersystem) O [**\_ processador**](/windows/desktop/CIMWin32Prov/win32-processor) de computador e o Win32 têm novas propriedades que permitem que você escreva scripts para determinar se o sistema de computadores tem processadores de vários núcleos ou hyperthreading.

</dd> <dt>

<span id="Event_messages"></span><span id="event_messages"></span><span id="EVENT_MESSAGES"></span>Mensagens de evento
</dt> <dd>

O Windows Vista tem novas mensagens de evento. Para obter mais informações, consulte [eventos WMI](wmi-events.md).

</dd> <dt>

<span id="Inventory_improvements"></span><span id="inventory_improvements"></span><span id="INVENTORY_IMPROVEMENTS"></span>Aprimoramentos de inventário
</dt> <dd>

Muitas classes de hardware tiveram alterações para melhorar o inventário de hardware. Por exemplo, uma propriedade de número de série foi adicionada ao [**Win32 \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) e [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive).

</dd> <dt>

<span id="New_provider_hosting_models"></span><span id="new_provider_hosting_models"></span><span id="NEW_PROVIDER_HOSTING_MODELS"></span>Novos modelos de Hospedagem de provedor
</dt> <dd>

Novos modelos de Hospedagem de provedor foram adicionados ao Windows Vista. Para obter mais informações, consulte [provedor de hospedagem e segurança](provider-hosting-and-security.md).

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o WMI](about-wmi.md)
</dt> </dl>

 

 
