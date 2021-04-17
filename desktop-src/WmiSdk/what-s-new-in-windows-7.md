---
description: O que há de novo no Windows 7
ms.assetid: C3FE15EF-CBF0-4A5D-ADCC-108795F8CE7A
ms.tgt_platform: multiple
title: O que há de novo no Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682e4f125fcc11a1b6679af7df78fddba5a766ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812248"
---
# <a name="whats-new-in-windows-7"></a>O que há de novo no Windows 7

## <a name="new-security-feature-in-windows-7"></a>Novo recurso de segurança no Windows 7

O seguinte lista o novo recurso de segurança Instrumentação de Gerenciamento do Windows (WMI) que está disponível no Windows 7.

<dl> <dt>

<span id="Controlling_provider_security"></span><span id="controlling_provider_security"></span><span id="CONTROLLING_PROVIDER_SECURITY"></span>Controlando a segurança do provedor
</dt> <dd>

Alterações para aprimorar a segurança do processo de host do provedor compartilhado WMI (wmiprvse.exe). Essas alterações apresentam três novas políticas de grupo e dois modos de execução para o host compartilhado WMI, que são chamados de modos seguros e compatíveis. Para obter mais informações, consulte [chaves do registro para controlar a segurança do provedor](registry-keys-for-controlling-provider-security-.md).

</dd> </dl>

## <a name="other-new-or-updated-features-in-windows-7"></a>Outros recursos novos ou atualizados no Windows 7

A lista a seguir lista os novos recursos do WMI que estão disponíveis no Windows 7.

<dl> <dt>

<span id="CIM_schema_compatibility"></span><span id="cim_schema_compatibility"></span><span id="CIM_SCHEMA_COMPATIBILITY"></span>Compatibilidade do esquema CIM
</dt> <dd>

A partir do Windows 7, o WMI é compatível com a versão de esquema do modelo CIM (CIM) 2.17.1. Para obter mais informações, consulte [compatibilidade do esquema CIM](cim-schema-compatibility.md).

</dd> <dt>

<span id="Cross-namespace_association_traversal"></span><span id="cross-namespace_association_traversal"></span><span id="CROSS-NAMESPACE_ASSOCIATION_TRAVERSAL"></span>Passagem de associação entre namespaces
</dt> <dd>

O WMI implementou um mecanismo padrão para descobrir perfis usando o esquema CIM. Para obter mais informações, consulte [passagem de associação de namespace cruzado](cross-namespace-association-traversal.md).

</dd> <dt>

<span id="Association_providers"></span><span id="association_providers"></span><span id="ASSOCIATION_PROVIDERS"></span>Provedores de associação
</dt> <dd>

Informações sobre como gravar e registrar um provedor de associação. Provedores de associação são usados para expor perfis padrão, como um perfil de energia. Para obter mais informações, consulte [escrevendo um provedor de associação para interoperabilidade](writing-an-association-provider-for-interop.md).

</dd> <dt>

<span id="Optional_feature_status"></span><span id="optional_feature_status"></span><span id="OPTIONAL_FEATURE_STATUS"></span>Status de recurso opcional
</dt> <dd>

O WMI implementou a classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) . Essa classe consulta e retorna o status dos recursos opcionais que estão presentes em um computador. Por exemplo, consultas usando o Windows PowerShell, consulte [consultando o status de recursos opcionais](querying-the-status-of-optional-features.md).

</dd> <dt>

<span id="Changing_the_default_behavior_for_the_AutoRestore_repository_feature"></span><span id="changing_the_default_behavior_for_the_autorestore_repository_feature"></span><span id="CHANGING_THE_DEFAULT_BEHAVIOR_FOR_THE_AUTORESTORE_REPOSITORY_FEATURE"></span>Alterando o comportamento padrão para o recurso repositório de autorestore
</dt> <dd>

O WMI tem uma nova chave do registro para habilitar ou desabilitar o recurso repositório de autorestore. Para obter mais informações, consulte [chave do registro para configuração do repositório](registry-key-for-repository-configuration.md).

</dd> <dt>

<span id="New__PowerShell_command_classes"></span><span id="new__powershell_command_classes"></span><span id="NEW__POWERSHELL_COMMAND_CLASSES"></span>Novas classes de comando do Windows PowerShell
</dt> <dd>

Os cmdlets do Windows PowerShell permitem que os usuários concluam as tarefas de ponta a ponta necessárias para gerenciar computadores locais e remotos. Para obter mais informações, consulte [referência gerenciada para classes de comando do PowerShell do WMI](managed-reference-for-wmi-powershell-command-classes.md).

</dd> <dt>

<span id="New_mechanism_to_connect_to_remote_computers"></span><span id="new_mechanism_to_connect_to_remote_computers"></span><span id="NEW_MECHANISM_TO_CONNECT_TO_REMOTE_COMPUTERS"></span>Novo mecanismo para se conectar a computadores remotos
</dt> <dd>

O Windows PowerShell fornece um mecanismo simples para se conectar ao WMI em um computador remoto. Para obter mais informações, consulte [conectando-se ao WMI em um computador remoto usando o PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).

</dd> <dt>

<span id="Changes_to_the_software_licensing_classes"></span><span id="changes_to_the_software_licensing_classes"></span><span id="CHANGES_TO_THE_SOFTWARE_LICENSING_CLASSES"></span>Alterações nas classes de licenciamento de software
</dt> <dd>

As [classes de licenciamento de software](/previous-versions/windows/desktop/sppwmi/software-license-provider-) têm novos métodos e propriedades para fornecer mais dados de licenciamento de software. Além disso, a classe [**SoftwareLicensingTokenActivationLicense**](/previous-versions/windows/desktop/sppwmi/softwarelicensingtokenactivationlicense) foi adicionada.

</dd> <dt>

<span id="New_power_metering_and_budgeting_classes"></span><span id="new_power_metering_and_budgeting_classes"></span><span id="NEW_POWER_METERING_AND_BUDGETING_CLASSES"></span>Novas classes de medição de energia e orçamento
</dt> <dd>

As [classes de medição de energia e de orçamento](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-) são a interface principal para a consulta de informações de PMI (interface do Power medidor) de medidores de energia subjacentes no sistema.

</dd> <dt>

<span id="New_power_policy_classes"></span><span id="new_power_policy_classes"></span><span id="NEW_POWER_POLICY_CLASSES"></span>Novas classes de política de energia
</dt> <dd>

As [classes de política de energia](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-) habilitam o gerenciamento remoto de todas as infraestruturas de política de energia.

</dd> <dt>

<span id="Changes_to_the_Win32_ServerFeature_class"></span><span id="changes_to_the_win32_serverfeature_class"></span><span id="CHANGES_TO_THE_WIN32_SERVERFEATURE_CLASS"></span>Alterações na classe [**Win32 \_ ServerFeature**](win32-serverfeature.md)
</dt> <dd>

A propriedade **ID** do [**\_ ServerFeature Win32**](win32-serverfeature.md) foi atualizada.

</dd> </dl>

Para obter mais informações sobre os novos recursos nas versões anteriores do sistema operacional, consulte [What ' s New in Windows Vista](what-s-new-in-windows-vista.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o WMI](about-wmi.md)
</dt> </dl>

 

 
