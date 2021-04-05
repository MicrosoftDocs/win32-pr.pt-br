---
description: A tabela InstallExecuteSequence lista as ações que são executadas quando o instalador executa a ação de instalação de nível superior. Confira o grupo tabelas de procedimentos de instalação, usando uma tabela de sequência e o exemplo de tabela de sequência detalhado.
ms.assetid: cdd4f02a-cfe6-4a23-9fc2-f4cb810379aa
title: Importando o InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8e4728b0a59c92dcc0d007fc816fd298455e049
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922136"
---
# <a name="importing-the-installexecutesequence"></a>Importando o InstallExecuteSequence

A [tabela InstallExecuteSequence](installexecutesequence-table.md) lista as ações que são executadas quando o instalador executa a [ação de instalação](install-action.md)de nível superior. Confira o [grupo tabelas de procedimentos de instalação](installation-procedure-tables-group.md), [usando uma tabela de sequência](using-a-sequence-table.md)e o exemplo de tabela de [sequência detalhado](sequence-table-detailed-example.md).

Se na seção [importando um banco de dados em branco](importing-a-blank-database.md) usado uisample.msi do SDK do Windows Installer, as tabelas de sequência em sua cópia do MNP2000.msi já contêm as sequências de ações sugeridas descritas em [usando uma tabela de sequência](using-a-sequence-table.md). Nenhuma alteração nessas sequências é necessária para criar o pacote de instalação do bloco de notas.

Use o editor de banco de dados para abrir MNP2000.msi e insira os dados a seguir na tabela InstallExecuteSequence.

[Tabela InstallExecuteSequence](installexecutesequence-table.md)



| Ação                   | Condição     | Sequência |
|--------------------------|---------------|----------|
| AllocateRegistrySpace    | NÃO instalado | 1550     |
| AppSearch                |               | 400      |
| BindImage                |               | 4300     |
| CCPSearch                | NÃO instalado | 500      |
| CostFinalize             |               | 1000     |
| CostInitialize           |               | 800      |
| Createfolders            |               | 3700     |
| Createatalhos          |               | 4500     |
| Excluirservices           | VersionNT     | 2000     |
| DuplicateFiles           |               | 4210     |
| Custo de                 |               | 900      |
| FindRelatedProducts      |               | 200      |
| InstallFiles             |               | 4000     |
| InstallFinalize          |               | 6600     |
| InstallInitialize        |               | 1500     |
| InstallODBC              |               | 5400     |
| Instalarservices          | VersionNT     | 5800     |
| InstallValidate          |               | 1.400     |
| LaunchConditions         |               | 100      |
| MigrateFeatureStates     |               | 1200     |
| MoveFile                |               | 3800     |
| PatchFiles               |               | 4090     |
| ProcessComponents        |               | 1600     |
| PublishComponents        |               | 6200     |
| PublishFeatures          |               | 6300     |
| PublishProduct           |               | 6400     |
| RegisterClassInfo        |               | 4600     |
| RegisterComPlus          |               | 5700     |
| RegisterExtensionInfo    |               | 4700     |
| RegisterFonts            |               | 5300     |
| RegisterMIMEInfo         |               | 4900     |
| RegisterProduct          |               | 6100     |
| RegisterProgIdInfo       |               | 4800     |
| RegisterTypeLibraries    |               | 5500     |
| RegisterUser             |               | 6000     |
| RemoveDuplicateFiles     |               | 3400     |
| RemoveEnvironmentStrings |               | 3.300     |
| RemoveExistingProducts   |               | 6700     |
| Removes              |               | 3500     |
| RemoveFolders            |               | 3600     |
| RemoveIniValues          |               | 3100     |
| RemoveODBC               |               | 2400     |
| RemoveRegistryValues     |               | 2600     |
| RemoveShortcuts          |               | 3200     |
| RMCCPSearch              | NÃO instalado | 600      |
| SelfRegModules           |               | 5600     |
| SelfUnregModules         |               | 2200     |
| SetODBCFolders           |               | 1100     |
| Iniciarservices            | VersionNT     | 5900     |
| Pararservices             | VersionNT     | 1900     |
| UnpublishComponents      |               | 1.700     |
| UnpublishFeatures        |               | 1800     |
| UnregisterClassInfo      |               | 2700     |
| UnregisterComPlus        |               | 2.100     |
| UnregisterExtensionInfo  |               | 2800     |
| UnregisterFonts          |               | 2500     |
| UnregisterMIMEInfo       |               | 3000     |
| UnregisterProgIdInfo     |               | 2900     |
| UnregisterTypeLibraries  |               | 2300     |
| ValidateProductID        |               | 700      |
| WriteEnvironmentStrings  |               | 5200     |
| WriteIniValues           |               | 5100     |
| WriteRegistryValues      |               | 5.000     |



 

[Continuar](importing-the-installuisequence.md)

 

 



