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
# <a name="whats-new-in-windowsvista"></a><span data-ttu-id="9c366-103">O que há de novo no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c366-103">Whats New in Windows�Vista</span></span>

<span data-ttu-id="9c366-104">A partir do Windows Vista, o WMI contém muitos recursos novos com base em solicitações por usuários WMI.</span><span class="sxs-lookup"><span data-stu-id="9c366-104">Starting with Windows Vista, WMI contains many new features based upon requests by WMI users.</span></span>

-   [<span data-ttu-id="9c366-105">Nova ferramenta de solução de problemas</span><span class="sxs-lookup"><span data-stu-id="9c366-105">New Troubleshooting Tool</span></span>](#new-troubleshooting-tool)
-   [<span data-ttu-id="9c366-106">Novos recursos de segurança do Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c366-106">New Security Features in Windows Vista</span></span>](#new-security-features-in-windows-vista)
-   [<span data-ttu-id="9c366-107">Outros novos recursos do Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c366-107">Other New Features in Windows Vista</span></span>](#other-new-features-in-windows-vista)
-   [<span data-ttu-id="9c366-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9c366-108">Related topics</span></span>](#related-topics)

## <a name="new-troubleshooting-tool"></a><span data-ttu-id="9c366-109">Nova ferramenta de solução de problemas</span><span class="sxs-lookup"><span data-stu-id="9c366-109">New Troubleshooting Tool</span></span>

<span data-ttu-id="9c366-110">Uma nova ferramenta de solução de problemas está disponível para download.</span><span class="sxs-lookup"><span data-stu-id="9c366-110">A new troubleshooting tool is available for download.</span></span>

<dl> <dt>

<span data-ttu-id="9c366-111"><span id="WMI_Diagnosis_Utility"></span><span id="wmi_diagnosis_utility"></span><span id="WMI_DIAGNOSIS_UTILITY"></span>Utilitário de Diagnóstico WMI</span><span class="sxs-lookup"><span data-stu-id="9c366-111"><span id="WMI_Diagnosis_Utility"></span><span id="wmi_diagnosis_utility"></span><span id="WMI_DIAGNOSIS_UTILITY"></span>WMI Diagnosis Utility</span></span>
</dt> <dd>

<span data-ttu-id="9c366-112">Esse utilitário examina o estado atual do serviço WMI e os componentes relacionados, as configurações do DCOM e as configurações do registro no computador local.</span><span class="sxs-lookup"><span data-stu-id="9c366-112">This utility examines the current state of the WMI service and related components, DCOM settings, and registry settings on the local computer.</span></span> <span data-ttu-id="9c366-113">O utilitário relata problemas e oferece sugestões de reparo.</span><span class="sxs-lookup"><span data-stu-id="9c366-113">The utility reports problems and offers suggestions for repair.</span></span> <span data-ttu-id="9c366-114">Para obter mais informações e baixar o utilitário, consulte [Utilitário de diagnóstico WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en).</span><span class="sxs-lookup"><span data-stu-id="9c366-114">For more information and to download the utility, see [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en).</span></span>

</dd> </dl>

## <a name="new-security-features-in-windows-vista"></a><span data-ttu-id="9c366-115">Novos recursos de segurança do Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c366-115">New Security Features in Windows Vista</span></span>

<span data-ttu-id="9c366-116">A lista a seguir lista os novos recursos de segurança do WMI que estão disponíveis no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9c366-116">The following list lists the new WMI security features that are available in Windows Vista.</span></span>

<dl> <dt>

<span data-ttu-id="9c366-117"><span id="Tracing_and_logging_events"></span><span id="tracing_and_logging_events"></span><span id="TRACING_AND_LOGGING_EVENTS"></span>Eventos de rastreamento e log</span><span class="sxs-lookup"><span data-stu-id="9c366-117"><span id="Tracing_and_logging_events"></span><span id="tracing_and_logging_events"></span><span id="TRACING_AND_LOGGING_EVENTS"></span>Tracing and logging events</span></span>
</dt> <dd>

<span data-ttu-id="9c366-118">O serviço WMI não usa mais os [arquivos de log do WMI](wmi-log-files.md).</span><span class="sxs-lookup"><span data-stu-id="9c366-118">WMI service no longer uses most of the [WMI Log Files](wmi-log-files.md).</span></span> <span data-ttu-id="9c366-119">Em vez disso, ele usa o ETW ( [rastreamento de eventos](/windows/desktop/ETW/event-tracing-portal) ) e eventos estão disponíveis por meio da interface do usuário do **Visualizador de eventos** ou da ferramenta de linha de comando wevtutil.</span><span class="sxs-lookup"><span data-stu-id="9c366-119">Instead it uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) and events are available through the **Event Viewer** UI or the Wevtutil command line tool.</span></span> <span data-ttu-id="9c366-120">Para obter mais informações, consulte [rastreando a atividade WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="9c366-120">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c366-121"><span id="Setting_WMI_namespace_security_in_the_MOF_file"></span><span id="setting_wmi_namespace_security_in_the_mof_file"></span><span id="SETTING_WMI_NAMESPACE_SECURITY_IN_THE_MOF_FILE"></span>Definindo a segurança do namespace WMI no arquivo MOF</span><span class="sxs-lookup"><span data-stu-id="9c366-121"><span id="Setting_WMI_namespace_security_in_the_MOF_file"></span><span id="setting_wmi_namespace_security_in_the_mof_file"></span><span id="SETTING_WMI_NAMESPACE_SECURITY_IN_THE_MOF_FILE"></span>Setting WMI namespace security in the MOF file</span></span>
</dt> <dd>

<span data-ttu-id="9c366-122">O qualificador **NamespaceSecuritySDDL** pode ser usado para proteger qualquer namespace.</span><span class="sxs-lookup"><span data-stu-id="9c366-122">The **NamespaceSecuritySDDL** qualifier can be used to secure any namespace.</span></span> <span data-ttu-id="9c366-123">Para obter mais informações, consulte [definindo a segurança do namespace quando o namespace é criado](setting-namespace-security-when-the-namespace-is-created.md).</span><span class="sxs-lookup"><span data-stu-id="9c366-123">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c366-124"><span id="Security_Auditing_of_WMI_namespaces"></span><span id="security_auditing_of_wmi_namespaces"></span><span id="SECURITY_AUDITING_OF_WMI_NAMESPACES"></span>Auditoria de segurança de namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="9c366-124"><span id="Security_Auditing_of_WMI_namespaces"></span><span id="security_auditing_of_wmi_namespaces"></span><span id="SECURITY_AUDITING_OF_WMI_NAMESPACES"></span>Security Auditing of WMI namespaces</span></span>
</dt> <dd>

<span data-ttu-id="9c366-125">O WMI usa a SACL (listas de controle de acesso) do sistema de namespace para auditar a atividade do namespace e relatar eventos para o log de eventos de segurança.</span><span class="sxs-lookup"><span data-stu-id="9c366-125">WMI uses the namespace system access control lists (SACL) to audit namespace activity and report events to the Security event log.</span></span> <span data-ttu-id="9c366-126">Para obter mais informações, consulte [acesso aos namespaces do WMI](access-to-wmi-namespaces.md) e [Configurando descritores de segurança de namespace](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="9c366-126">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md) and [Setting Namespace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c366-127"><span id="Get_and_Set_security_descriptor_methods_for_securable_objects"></span><span id="get_and_set_security_descriptor_methods_for_securable_objects"></span><span id="GET_AND_SET_SECURITY_DESCRIPTOR_METHODS_FOR_SECURABLE_OBJECTS"></span>Obter e definir métodos de descritor de segurança para objetos protegíveis</span><span class="sxs-lookup"><span data-stu-id="9c366-127"><span id="Get_and_Set_security_descriptor_methods_for_securable_objects"></span><span id="get_and_set_security_descriptor_methods_for_securable_objects"></span><span id="GET_AND_SET_SECURITY_DESCRIPTOR_METHODS_FOR_SECURABLE_OBJECTS"></span>Get and Set security descriptor methods for securable objects</span></span>
</dt> <dd>

<span data-ttu-id="9c366-128">Novos métodos programáveis para obter e definir descritores de segurança foram adicionados à [**\_ impressora Win32**](/windows/desktop/CIMWin32Prov/win32-printer), [**\_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), [**Win32 \_ DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)e [**\_ \_ SystemSecurity**](--systemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="9c366-128">New scriptable methods to get and set security descriptors have been added to [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer), [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), [**Win32\_DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting), and [**\_\_SystemSecurity**](--systemsecurity.md).</span></span> <span data-ttu-id="9c366-129">Para obter mais informações, consulte [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9c366-129">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c366-130"><span id="Manipulate_Security_Descriptors_in_scripts"></span><span id="manipulate_security_descriptors_in_scripts"></span><span id="MANIPULATE_SECURITY_DESCRIPTORS_IN_SCRIPTS"></span>Manipular descritores de segurança em scripts</span><span class="sxs-lookup"><span data-stu-id="9c366-130"><span id="Manipulate_Security_Descriptors_in_scripts"></span><span id="manipulate_security_descriptors_in_scripts"></span><span id="MANIPULATE_SECURITY_DESCRIPTORS_IN_SCRIPTS"></span>Manipulate Security Descriptors in scripts</span></span>
</dt> <dd>

<span data-ttu-id="9c366-131">A classe [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) tem métodos que permitem que os scripts convertam descritores de segurança binários em objetos protegíveis em objetos do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) ou em cadeias de caracteres da [linguagem de definição do descritor de segurança](/windows/desktop/SecAuthZ/security-descriptor-definition-language) .</span><span class="sxs-lookup"><span data-stu-id="9c366-131">The [**Win32\_SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) class has methods that allow scripts to convert binary security descriptors on securable objects to [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) objects or [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) strings.</span></span> <span data-ttu-id="9c366-132">Para obter mais informações, consulte [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9c366-132">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c366-133"><span id="User_Account_Control"></span><span id="user_account_control"></span><span id="USER_ACCOUNT_CONTROL"></span>Controle de conta de usuário</span><span class="sxs-lookup"><span data-stu-id="9c366-133"><span id="User_Account_Control"></span><span id="user_account_control"></span><span id="USER_ACCOUNT_CONTROL"></span>User Account Control</span></span>
</dt> <dd>

<span data-ttu-id="9c366-134">O UAC (controle de conta de usuário) afeta quais dados do WMI são retornados, acesso remoto e como os scripts devem ser executados.</span><span class="sxs-lookup"><span data-stu-id="9c366-134">User Account Control (UAC) affects what WMI data is returned, remote access, and how scripts must be run.</span></span> <span data-ttu-id="9c366-135">Para obter mais informações, consulte [controle de conta de usuário e WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="9c366-135">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span> <span data-ttu-id="9c366-136">Para obter mais informações sobre o UAC, consulte [introdução com o controle de conta de usuário no Windows Vista](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).</span><span class="sxs-lookup"><span data-stu-id="9c366-136">For more information about UAC, see [Getting Started with User Account Control on Windows Vista](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).</span></span>

</dd> </dl>

## <a name="other-new-features-in-windows-vista"></a><span data-ttu-id="9c366-137">Outros novos recursos do Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c366-137">Other New Features in Windows Vista</span></span>

<span data-ttu-id="9c366-138">A lista a seguir lista os novos recursos do WMI que estão disponíveis no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9c366-138">The following list lists new WMI features that are available in Windows Vista.</span></span>

<dl> <dt>

<span data-ttu-id="9c366-139"><span id="New_performance_counter_data_providers"></span><span id="new_performance_counter_data_providers"></span><span id="NEW_PERFORMANCE_COUNTER_DATA_PROVIDERS"></span>Novos provedores de dados do contador de desempenho</span><span class="sxs-lookup"><span data-stu-id="9c366-139"><span id="New_performance_counter_data_providers"></span><span id="new_performance_counter_data_providers"></span><span id="NEW_PERFORMANCE_COUNTER_DATA_PROVIDERS"></span>New performance counter data providers</span></span>
</dt> <dd>

<span data-ttu-id="9c366-140">O processo de descoberta automática/autolimpeza (ADAP) não transfere mais objetos de contador de desempenho para classes de desempenho WMI no repositório WMI.</span><span class="sxs-lookup"><span data-stu-id="9c366-140">The AutoDiscovery/AutoPurge (ADAP) process no longer transfers performance counter objects into WMI performance classes in the WMI repository.</span></span> <span data-ttu-id="9c366-141">Para obter mais informações, consulte [bibliotecas de desempenho e WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="9c366-141">For more information, see [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span> <span data-ttu-id="9c366-142">O [provedor WMIPerfClass](wmiperfclass-provider.md) cria as classes do contador de desempenho WMI.</span><span class="sxs-lookup"><span data-stu-id="9c366-142">The [WMIPerfClass Provider](wmiperfclass-provider.md) creates the WMI Performance Counter Classes.</span></span> <span data-ttu-id="9c366-143">Os dados são fornecidos dinamicamente para essas classes de desempenho WMI pelo [provedor WMIPerfInst](wmiperfinst-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9c366-143">Data is dynamically supplied to these WMI performance classes by the [WMIPerfInst Provider](wmiperfinst-provider.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c366-144"><span id="Indexer_for_collections"></span><span id="indexer_for_collections"></span><span id="INDEXER_FOR_COLLECTIONS"></span>Indexador para coleções</span><span class="sxs-lookup"><span data-stu-id="9c366-144"><span id="Indexer_for_collections"></span><span id="indexer_for_collections"></span><span id="INDEXER_FOR_COLLECTIONS"></span>Indexer for collections</span></span>
</dt> <dd>

<span data-ttu-id="9c366-145">O método [**SWbemObject. ItemIndex**](swbemobjectset-itemindex.md) retorna o objeto associado a um índice especificado em uma coleção.</span><span class="sxs-lookup"><span data-stu-id="9c366-145">The [**SWbemObject.ItemIndex**](swbemobjectset-itemindex.md) method returns the object associated with a specified index into a collection.</span></span>

</dd> <dt>

<span data-ttu-id="9c366-146"><span id="Support_for_IPv6_and_IPv4"></span><span id="support_for_ipv6_and_ipv4"></span><span id="SUPPORT_FOR_IPV6_AND_IPV4"></span>Suporte para IPv6 e IPv4</span><span class="sxs-lookup"><span data-stu-id="9c366-146"><span id="Support_for_IPv6_and_IPv4"></span><span id="support_for_ipv6_and_ipv4"></span><span id="SUPPORT_FOR_IPV6_AND_IPV4"></span>Support for IPv6 and IPv4</span></span>
</dt> <dd>

<span data-ttu-id="9c366-147">O [provedor de rotas IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) WMI e as classes de rede fornecem dados para endereços IPv4.</span><span class="sxs-lookup"><span data-stu-id="9c366-147">WMI [IP Route Provider](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) and network classes supply data for IPv4 addresses.</span></span> <span data-ttu-id="9c366-148">A partir do Windows Vista, o WMI também fornece suporte limitado para recursos de rede IPv6.</span><span class="sxs-lookup"><span data-stu-id="9c366-148">Starting with Windows Vista, WMI also provides limited support for IPv6 network capabilities.</span></span> <span data-ttu-id="9c366-149">Para obter mais informações, consulte [suporte a IPv6 e IPv4 no WMI](ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="9c366-149">For more information, see [IPv6 and IPv4 Support in WMI](ipv6-and-ipv4-support-in-wmi.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c366-150"><span id="Changes_to_remote_connections"></span><span id="changes_to_remote_connections"></span><span id="CHANGES_TO_REMOTE_CONNECTIONS"></span>Alterações em conexões remotas</span><span class="sxs-lookup"><span data-stu-id="9c366-150"><span id="Changes_to_remote_connections"></span><span id="changes_to_remote_connections"></span><span id="CHANGES_TO_REMOTE_CONNECTIONS"></span>Changes to remote connections</span></span>
</dt> <dd>

<span data-ttu-id="9c366-151">Conectar-se a um namespace do WMI em um computador remoto que executa o Windows Vista pode exigir alterações nas configurações do [Firewall do Windows](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx), controle de [conta de usuário](/previous-versions/aa905108(v=msdn.10))ou DCOM.</span><span class="sxs-lookup"><span data-stu-id="9c366-151">Connecting to a WMI namespace on a remote computer running Windows Vista may require changes to settings for [Windows Firewall](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx), [User Account Control](/previous-versions/aa905108(v=msdn.10)), or DCOM.</span></span> <span data-ttu-id="9c366-152">Para obter mais informações, consulte [conectando-se ao WMI remotamente a partir do vista](connecting-to-wmi-remotely-starting-with-vista.md).</span><span class="sxs-lookup"><span data-stu-id="9c366-152">For more information, see [Connecting to WMI Remotely Starting with Vista](connecting-to-wmi-remotely-starting-with-vista.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c366-153"><span id="Changes_to_________Win32_QuickFixEngineering"></span><span id="changes_to_________win32_quickfixengineering"></span><span id="CHANGES_TO_________WIN32_QUICKFIXENGINEERING"></span>Alterações no [ **Win32 \_ QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)</span><span class="sxs-lookup"><span data-stu-id="9c366-153"><span id="Changes_to_________Win32_QuickFixEngineering"></span><span id="changes_to_________win32_quickfixengineering"></span><span id="CHANGES_TO_________WIN32_QUICKFIXENGINEERING"></span>Changes to [**Win32\_QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)</span></span>
</dt> <dd>

<span data-ttu-id="9c366-154">Para sistemas em execução no sistema operacional Windows Vista e posterior, essa classe retorna apenas as atualizações fornecidas pela CBS (serviço baseado em componente).</span><span class="sxs-lookup"><span data-stu-id="9c366-154">For systems running on the Windows Vista and later operating system, this class returns only the updates supplied by Component Based Servicing (CBS).</span></span> <span data-ttu-id="9c366-155">Essas atualizações não estão listadas no registro.</span><span class="sxs-lookup"><span data-stu-id="9c366-155">These updates are not listed in the registry.</span></span> <span data-ttu-id="9c366-156">As atualizações fornecidas pelo Windows Installer (MSI) ou pelo [Windows Update](https://update.microsoft.com/microsoftupdate/v6/default.aspx?ln=en-us) não são retornadas pelo [**Win32 \_ QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering).</span><span class="sxs-lookup"><span data-stu-id="9c366-156">Updates supplied by Windows Installer (MSI) or the [Windows Update](https://update.microsoft.com/microsoftupdate/v6/default.aspx?ln=en-us) are not returned by [**Win32\_QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering).</span></span>

</dd> <dt>

<span data-ttu-id="9c366-157"><span id="Enabling_and_disabling_a_NIC"></span><span id="enabling_and_disabling_a_nic"></span><span id="ENABLING_AND_DISABLING_A_NIC"></span>Habilitando e desabilitando uma NIC</span><span class="sxs-lookup"><span data-stu-id="9c366-157"><span id="Enabling_and_disabling_a_NIC"></span><span id="enabling_and_disabling_a_nic"></span><span id="ENABLING_AND_DISABLING_A_NIC"></span>Enabling and disabling a NIC</span></span>
</dt> <dd>

<span data-ttu-id="9c366-158">[**Win32 \_ O adaptador**](/windows/desktop/CIMWin32Prov/win32-networkadapter) tem novos métodos para habilitar e desabilitar o adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="9c366-158">[**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) has new methods to enable and disable the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9c366-159"><span id="Windows_Installer_Provider_changes"></span><span id="windows_installer_provider_changes"></span><span id="WINDOWS_INSTALLER_PROVIDER_CHANGES"></span>Alterações do provedor de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="9c366-159"><span id="Windows_Installer_Provider_changes"></span><span id="windows_installer_provider_changes"></span><span id="WINDOWS_INSTALLER_PROVIDER_CHANGES"></span>Windows Installer Provider changes</span></span>
</dt> <dd>

<span data-ttu-id="9c366-160">[**Win32 \_ O produto**](/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)) tem novas propriedades e métodos para fornecer mais dados sobre o produto.</span><span class="sxs-lookup"><span data-stu-id="9c366-160">[**Win32\_Product**](/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)) has new properties and methods to provide more data about the product.</span></span>

</dd> <dt>

<span data-ttu-id="9c366-161"><span id="New_display_monitor_classes"></span><span id="new_display_monitor_classes"></span><span id="NEW_DISPLAY_MONITOR_CLASSES"></span>Novas classes de monitor de exibição</span><span class="sxs-lookup"><span data-stu-id="9c366-161"><span id="New_display_monitor_classes"></span><span id="new_display_monitor_classes"></span><span id="NEW_DISPLAY_MONITOR_CLASSES"></span>New display monitor classes</span></span>
</dt> <dd>

<span data-ttu-id="9c366-162">As [classes de exibição do monitor](/windows/desktop/WmiCoreProv/wmi-core-provider-) contêm dados fornecidos pelo [provedor WDM](/windows/desktop/WmiCoreProv/wdm-provider) que fornece dados sobre monitores de exibição.</span><span class="sxs-lookup"><span data-stu-id="9c366-162">[Monitor Display Classes](/windows/desktop/WmiCoreProv/wmi-core-provider-) contain data supplied by the [WDM Provider](/windows/desktop/WmiCoreProv/wdm-provider) that provides data about display monitors.</span></span>

</dd> <dt>

<span data-ttu-id="9c366-163"><span id="Intelligent_Platform_Management_Interface_provider"></span><span id="intelligent_platform_management_interface_provider"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE_PROVIDER"></span>Provedor de interface de gerenciamento de plataforma inteligente</span><span class="sxs-lookup"><span data-stu-id="9c366-163"><span id="Intelligent_Platform_Management_Interface_provider"></span><span id="intelligent_platform_management_interface_provider"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE_PROVIDER"></span>Intelligent Platform Management Interface provider</span></span>
</dt> <dd>

<span data-ttu-id="9c366-164">O [provedor WMI IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) fornece dados das operações do controlador BMC (Baseboard Management Controller) para o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9c366-164">The WMI [IPMI Provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) supplies data from baseboard management controller (BMC) operations to the operating system.</span></span> <span data-ttu-id="9c366-165">O provedor fornece informações para as classes de informações de gerenciamento de plataforma inteligente, que fornecem dados de sensores e dados de mensagem do SEL (log de eventos do sistema) do BMC.</span><span class="sxs-lookup"><span data-stu-id="9c366-165">The provider supplies information to the Intelligent Platform Management Information Classes, which provide sensors data and BMC System Event Log (SEL) message data.</span></span>

</dd> <dt>

<span data-ttu-id="9c366-166"><span id="Detecting_hyperthreading_and_multicore_processors"></span><span id="detecting_hyperthreading_and_multicore_processors"></span><span id="DETECTING_HYPERTHREADING_AND_MULTICORE_PROCESSORS"></span>Detectando processadores de hyperthreading e vários núcleos</span><span class="sxs-lookup"><span data-stu-id="9c366-166"><span id="Detecting_hyperthreading_and_multicore_processors"></span><span id="detecting_hyperthreading_and_multicore_processors"></span><span id="DETECTING_HYPERTHREADING_AND_MULTICORE_PROCESSORS"></span>Detecting hyperthreading and multicore processors</span></span>
</dt> <dd>

<span data-ttu-id="9c366-167">[**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-computersystem) O [**\_ processador**](/windows/desktop/CIMWin32Prov/win32-processor) de computador e o Win32 têm novas propriedades que permitem que você escreva scripts para determinar se o sistema de computadores tem processadores de vários núcleos ou hyperthreading.</span><span class="sxs-lookup"><span data-stu-id="9c366-167">[**Win32\_ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) and [**Win32\_Processor**](/windows/desktop/CIMWin32Prov/win32-processor) have new properties that enable you to write scripts to determine whether the computer system has multicore or hyperthreading processors.</span></span>

</dd> <dt>

<span data-ttu-id="9c366-168"><span id="Event_messages"></span><span id="event_messages"></span><span id="EVENT_MESSAGES"></span>Mensagens de evento</span><span class="sxs-lookup"><span data-stu-id="9c366-168"><span id="Event_messages"></span><span id="event_messages"></span><span id="EVENT_MESSAGES"></span>Event messages</span></span>
</dt> <dd>

<span data-ttu-id="9c366-169">O Windows Vista tem novas mensagens de evento.</span><span class="sxs-lookup"><span data-stu-id="9c366-169">Windows Vista has new event messages.</span></span> <span data-ttu-id="9c366-170">Para obter mais informações, consulte [eventos WMI](wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="9c366-170">For more information, see [WMI Events](wmi-events.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c366-171"><span id="Inventory_improvements"></span><span id="inventory_improvements"></span><span id="INVENTORY_IMPROVEMENTS"></span>Aprimoramentos de inventário</span><span class="sxs-lookup"><span data-stu-id="9c366-171"><span id="Inventory_improvements"></span><span id="inventory_improvements"></span><span id="INVENTORY_IMPROVEMENTS"></span>Inventory improvements</span></span>
</dt> <dd>

<span data-ttu-id="9c366-172">Muitas classes de hardware tiveram alterações para melhorar o inventário de hardware.</span><span class="sxs-lookup"><span data-stu-id="9c366-172">Many hardware classes have had changes to improve hardware inventory.</span></span> <span data-ttu-id="9c366-173">Por exemplo, uma propriedade de número de série foi adicionada ao [**Win32 \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) e [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive).</span><span class="sxs-lookup"><span data-stu-id="9c366-173">For example, a serial number property was added to [**Win32\_CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) and [**Win32\_DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive).</span></span>

</dd> <dt>

<span data-ttu-id="9c366-174"><span id="New_provider_hosting_models"></span><span id="new_provider_hosting_models"></span><span id="NEW_PROVIDER_HOSTING_MODELS"></span>Novos modelos de Hospedagem de provedor</span><span class="sxs-lookup"><span data-stu-id="9c366-174"><span id="New_provider_hosting_models"></span><span id="new_provider_hosting_models"></span><span id="NEW_PROVIDER_HOSTING_MODELS"></span>New provider hosting models</span></span>
</dt> <dd>

<span data-ttu-id="9c366-175">Novos modelos de Hospedagem de provedor foram adicionados ao Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9c366-175">New provider hosting models have been added for Windows Vista.</span></span> <span data-ttu-id="9c366-176">Para obter mais informações, consulte [provedor de hospedagem e segurança](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="9c366-176">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="9c366-177">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9c366-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c366-178">Sobre o WMI</span><span class="sxs-lookup"><span data-stu-id="9c366-178">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 
