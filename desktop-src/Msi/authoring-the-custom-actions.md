---
description: 'A tabela a seguir lista as cinco ações personalizadas usadas para atender às especificações de exemplo: ProcessAccounts, UninstallAccounts, accounts, RemoveAccounts e RollbackAccounts.'
ms.assetid: 389ec652-243e-4392-aec9-3a7eb90e6c68
title: Criando as ações personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb6880f95b0468a495653057a9a5802af671c55b18b025c38a3191a4792e7558
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381171"
---
# <a name="authoring-the-custom-actions"></a>Criando as ações personalizadas

A tabela a seguir lista as cinco ações personalizadas usadas para atender às especificações de exemplo: ProcessAccounts, UninstallAccounts, accounts, RemoveAccounts e RollbackAccounts. Todas essas ações personalizadas estão em [bibliotecas de vínculo dinâmico](dynamic-link-libraries.md) armazenadas na [tabela binária](binary-table.md). o código-fonte do C++ para as bibliotecas de vínculo dinâmico que contêm as ações personalizadas de exemplo é fornecido no SDK do Windows Installer. ProcessAccounts e UninstallAccounts estão no arquivo Process. cpp. CreateAccount está no arquivo Create. cpp. RemoveAccount e RollbackAccount estão no arquivo Remove. cpp. Esses arquivos de origem podem ser usados para criar os arquivos Process.dll, Create.dll e Remove.dll.

Como a criação ou remoção de uma conta de usuário requer privilégios elevados, [ações personalizadas de execução adiada](deferred-execution-custom-actions.md) que são executadas no contexto do sistema devem ser usadas para criar, remover ou reverter contas de usuário. As ações personalizadas de execução imediata, ProcessAccounts e UninstallAccounts, geram as ações personalizadas adiadas que criam, removem ou revertem contas de usuário: CreateAccount, RemoveAccount e RollbackAccount.

Como as ações personalizadas adiadas não podem ler informações em tabelas de banco de dados, ProcessAccounts e UninstallUserAccouts devem definir uma propriedade CustomActionData para passar as informações na tabela accounts para as ações personalizadas adiadas, conforme descrito em [obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md). Quando o instalador executa o script de execução, as ações personalizadas adiadas lidam com as contas de usuário de acordo com as informações na propriedade CustomActionData.

Como todas as ações personalizadas estão em bibliotecas de vínculo dinâmico armazenadas na tabela binária, todas elas incluem as constantes msidbCustomActionTypeDll e msidbCustomActionTypeBinaryData em seu tipo numérico base. ProcessAccounts e UninstallAccounts são exemplos de [tipo de ação personalizada pura 1](custom-action-type-1.md). Para obter informações sobre outros tipos de ação personalizada, consulte a [lista de Resumo de todos os tipos de ação personalizados](summary-list-of-all-custom-action-types.md).

CreateAccount e RemoveAccount são [ações personalizadas de execução adiada](deferred-execution-custom-actions.md) que não permitem que os serviços representem usuários específicos. Essas ações personalizadas incluem as constantes msidbCustomActionTypeInScript e msidbCustomActionTypeNoImpersonate para especificar essas [Opções de execução em script de ação personalizada](custom-action-in-script-execution-options.md).

RollbackAccount é uma [ação personalizada de reversão](rollback-custom-actions.md) que remove apenas contas de usuário durante uma [instalação de reversão](rollback-installation.md). RollbackAccount inclui as constantes msidbCustomActionTypeInScript e msidbCustomActionTypeRollback para especificar essas [Opções de execução em script de ação personalizada](custom-action-in-script-execution-options.md).

Essas ações personalizadas podem lidar com dados confidenciais, como senhas de usuário, que não devem ser gravadas no arquivo de log. As ações personalizadas adiadas devem, portanto, incluir msidbCustomActionTypeHideTarget no tipo de ação personalizada. Os nomes das ações personalizadas adiadas também precisam ser adicionados à lista de propriedades [**MsiHiddenProperties**](msihiddenproperties.md) na [tabela de propriedades](property-table.md) devido à maneira como as ações personalizadas imediatas passam dados para ações personalizadas adiadas usando a propriedade CustomActionData.



| Ação personalizada     | Ponto de entrada de DLL                       | Tipo de ação personalizada                                                                                                                                                         |
|-------------------|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ProcessAccounts   | ProcessUserAccounts em Process.dll.   | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData = 1                                                                                                             |
| UninstallAccounts | UninstallUserAccounts em Process.dll. | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData = 1                                                                                                             |
| CreateAccount     | CreateUserAccount em Create.dll.      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate + msidbCustomActionTypeHideTarget = 11265. |
| RemoveAccount     | RemoveUserAccount em Remove.dll.      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate + msidbCustomActionTypeHideTarget = 11265. |
| RollbackAccount   | RemoveUserAccount em Remove.dll.      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeInScript + msidbCustomActionTypeRollback + msidbCustomActionTypeHideTarget = 9473.       |



 

Continue a [criar a tabela CustomAction](authoring-the-customaction-table.md).

 

 



