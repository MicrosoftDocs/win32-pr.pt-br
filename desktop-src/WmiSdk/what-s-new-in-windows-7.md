---
description: Novidades no Windows 7
ms.assetid: C3FE15EF-CBF0-4A5D-ADCC-108795F8CE7A
ms.tgt_platform: multiple
title: Novidades no Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 000a3460366855df65096333a8b847a6d2c0c0a48a89c91f6791db3286d634fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502856"
---
# <a name="whats-new-in-windows-7"></a>Novidades no Windows 7

## <a name="new-security-feature-in-windows-7"></a>Novo recurso de segurança no Windows 7

A seguir, é possível listar o novo recurso de segurança WMI (Instrumentação de Gerenciamento de Windows) que está disponível no Windows 7.

<dl> <dt>

<span id="Controlling_provider_security"></span><span id="controlling_provider_security"></span><span id="CONTROLLING_PROVIDER_SECURITY"></span>Controlando a segurança do provedor
</dt> <dd>

Alterações para aprimorar a segurança do processo de host do provedor compartilhado WMI (wmiprvse.exe). Essas alterações introduzem três novas políticas de grupo e dois modos de execução para o host compartilhado WMI, que são chamados de modos seguros e compatíveis. Para obter mais informações, consulte [Chaves do Registro para controlar a segurança do provedor.](registry-keys-for-controlling-provider-security-.md)

</dd> </dl>

## <a name="other-new-or-updated-features-in-windows-7"></a>Outros recursos novos ou atualizados no Windows 7

A lista a seguir lista os novos recursos WMI disponíveis no Windows 7.

<dl> <dt>

<span id="CIM_schema_compatibility"></span><span id="cim_schema_compatibility"></span><span id="CIM_SCHEMA_COMPATIBILITY"></span>Compatibilidade de esquema CIM
</dt> <dd>

A partir Windows 7, o WMI é compatível com o esquema CIM (modelo CIM) versão 2.17.1. Para obter mais informações, consulte [Cim Schema Compatibility](cim-schema-compatibility.md).

</dd> <dt>

<span id="Cross-namespace_association_traversal"></span><span id="cross-namespace_association_traversal"></span><span id="CROSS-NAMESPACE_ASSOCIATION_TRAVERSAL"></span>Travessia de associação entre namespaces
</dt> <dd>

O WMI implementou um mecanismo padrão para descobrir perfis usando o esquema CIM. Para obter mais informações, consulte [Cross Namespace Association Traversal](cross-namespace-association-traversal.md).

</dd> <dt>

<span id="Association_providers"></span><span id="association_providers"></span><span id="ASSOCIATION_PROVIDERS"></span>Provedores de associação
</dt> <dd>

Informações sobre como escrever e registrar um provedor de associação. Provedores de associação são usados para expor perfis padrão, como um perfil de energia. Para obter mais informações, consulte [Escrevendo um provedor de associação para interop](writing-an-association-provider-for-interop.md).

</dd> <dt>

<span id="Optional_feature_status"></span><span id="optional_feature_status"></span><span id="OPTIONAL_FEATURE_STATUS"></span>Status do recurso opcional
</dt> <dd>

O WMI implementou [**a \_ classe OptionalFeature do Win32.**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) Essa classe consulta e retorna o status dos recursos opcionais que estão presentes em um computador. Para consultas de exemplo usando Windows PowerShell, consulte [Consultando o status de recursos opcionais](querying-the-status-of-optional-features.md).

</dd> <dt>

<span id="Changing_the_default_behavior_for_the_AutoRestore_repository_feature"></span><span id="changing_the_default_behavior_for_the_autorestore_repository_feature"></span><span id="CHANGING_THE_DEFAULT_BEHAVIOR_FOR_THE_AUTORESTORE_REPOSITORY_FEATURE"></span>Alterando o comportamento padrão para o recurso de repositório AutoRestore
</dt> <dd>

O WMI tem uma nova chave do Registro para habilitar ou desabilitar o recurso de repositório AutoRestore. Para obter mais informações, consulte [Chave do Registro para configuração do repositório](registry-key-for-repository-configuration.md).

</dd> <dt>

<span id="New__PowerShell_command_classes"></span><span id="new__powershell_command_classes"></span><span id="NEW__POWERSHELL_COMMAND_CLASSES"></span>Novas classes Windows PowerShell comando
</dt> <dd>

Windows PowerShell cmdlets permitem que os usuários concluam as tarefas de ponta a ponta necessárias para gerenciar computadores locais e remotos. Para obter mais informações, consulte [Referência gerenciada para classes de comando do PowerShell WMI](managed-reference-for-wmi-powershell-command-classes.md).

</dd> <dt>

<span id="New_mechanism_to_connect_to_remote_computers"></span><span id="new_mechanism_to_connect_to_remote_computers"></span><span id="NEW_MECHANISM_TO_CONNECT_TO_REMOTE_COMPUTERS"></span>Novo mecanismo para se conectar a computadores remotos
</dt> <dd>

Windows PowerShell fornece um mecanismo simples para se conectar ao WMI em um computador remoto. Para obter mais informações, [consulte Conectando-se ao WMI em um computador remoto usando o PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).

</dd> <dt>

<span id="Changes_to_the_software_licensing_classes"></span><span id="changes_to_the_software_licensing_classes"></span><span id="CHANGES_TO_THE_SOFTWARE_LICENSING_CLASSES"></span>Alterações nas classes de licenciamento de software
</dt> <dd>

As [classes de licenciamento de software](/previous-versions/windows/desktop/sppwmi/software-license-provider-) têm novos métodos e propriedades para fornecer mais dados de licenciamento de software. Além disso, a [**classe SoftwareLicensingTokenActivationLicense**](/previous-versions/windows/desktop/sppwmi/softwarelicensingtokenactivationlicense) foi adicionada.

</dd> <dt>

<span id="New_power_metering_and_budgeting_classes"></span><span id="new_power_metering_and_budgeting_classes"></span><span id="NEW_POWER_METERING_AND_BUDGETING_CLASSES"></span>Novas classes de medição de energia e orçamento
</dt> <dd>

[As classes de medição](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-) de energia e orçamento são a interface principal para a consulta de informações de PMI (Interface do Power Meter) de medidores de energia subjacentes no sistema.

</dd> <dt>

<span id="New_power_policy_classes"></span><span id="new_power_policy_classes"></span><span id="NEW_POWER_POLICY_CLASSES"></span>Novas classes de política de energia
</dt> <dd>

[As classes de política de](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-) energia permitem o gerenciamento remoto de todas as infraestruturas de política de energia.

</dd> <dt>

<span id="Changes_to_the_Win32_ServerFeature_class"></span><span id="changes_to_the_win32_serverfeature_class"></span><span id="CHANGES_TO_THE_WIN32_SERVERFEATURE_CLASS"></span>Alterações na [**classe \_ ServerFeature do Win32**](win32-serverfeature.md)
</dt> <dd>

A **propriedade ID** do [**Win32 \_ ServerFeature**](win32-serverfeature.md) foi atualizada.

</dd> </dl>

Para obter mais informações sobre novos recursos em versões anteriores do sistema operacional, consulte [Novidades no Windows Vista](what-s-new-in-windows-vista.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o WMI](about-wmi.md)
</dt> </dl>

 

 
