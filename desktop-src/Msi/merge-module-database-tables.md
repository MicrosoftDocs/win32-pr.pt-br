---
description: As tabelas a seguir são necessárias em um módulo de mesclagem padrão.
ms.assetid: 2af6cea0-6d93-4aa5-a708-d305f11986ef
title: Mesclar tabelas do banco de dados do módulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a58240c589297cf2540625bc12180252efa42d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766392"
---
# <a name="merge-module-database-tables"></a>Mesclar tabelas do banco de dados do módulo

As tabelas a seguir são necessárias em um módulo de mesclagem padrão.



| Nome da tabela                                       | Comentário                                                                                          |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Componente](component-table.md)                 | NECESSÁRIA                                                                                       |
| [Diretório](directory-table.md)                 | NECESSÁRIA                                                                                       |
| [FeatureComponents](featurecomponents-table.md) | NECESSÁRIA                                                                                       |
| [Arquivo](file-table.md)                           | NECESSÁRIA                                                                                       |
| [ModuleSignature](modulesignature-table.md)     | NECESSÁRIA Mesclado no banco de dados do instalador. Lista as informações que identificam um módulo de mesclagem. |
| [ModuleComponents](modulecomponents-table.md)   | NECESSÁRIA Mesclado no banco de dados do instalador. Lista todos os componentes no módulo de mesclagem.     |



 

As tabelas a seguir só ocorrem em módulos de mesclagem ou outros bancos de dados do instalador que já foram combinados com um módulo de mesclagem.



| Nome da tabela                                     | Comentário                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [ModuleDependency](moduledependency-table.md) | Mesclado no banco de dados do instalador. Lista outros módulos de mesclagem exigidos por este módulo de mesclagem.                |
| [ModuleExclusion](moduleexclusion-table.md)   | Mesclado no banco de dados do instalador. Lista outros módulos de mesclagem que são incompatíveis com esse módulo de mesclagem. |



 

As tabelas ModuleSequence a seguir só ocorrem em módulos de mesclagem.



| Nome da tabela                                                             | Comentário                                                                                   |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [ModuleAdminUISequence](moduleadminuisequence-table.md)               | Mescla ações na [tabela AdminUISequence](adminuisequence-table.md).               |
| [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)     | Mescla ações na [tabela AdminExecuteSequence](adminexecutesequence-table.md).     |
| [ModuleAdvtUISequence](moduleadvtuisequence-table.md)                 | Não use esta tabela. Para obter detalhes, consulte [tabela AdvtUISequence](advtuisequence-table.md). |
| [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md)       | Mescla ações na [tabela AdvtExecuteSequence](advtexecutesequence-table.md).       |
| [ModuleIgnoreTable](moduleignoretable-table.md)                       | Lista as tabelas no módulo que não são mescladas no arquivo. msi.                        |
| [ModuleInstallUISequence](moduleinstalluisequence-table.md)           | Mescla ações na [tabela InstallUISequence](installuisequence-table.md).           |
| [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) | Mescla ações na [tabela InstallExecuteSequence](installexecutesequence-table.md). |



 

As tabelas a seguir são necessárias em todos os módulos de mesclagem configuráveis. Mergemod.dll 2,0 ou posterior é necessário para criar um módulo de mesclagem configurável. Para obter detalhes, consulte [módulos de mesclagem configuráveis](configurable-merge-modules.md).



| Nome da tabela                                                 | Comentário                                                                                                                                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tabela ModuleSubstitution](modulesubstitution-table.md)   | NECESSÁRIA Essa tabela não é mesclada no banco de dados de instalação de destino. Especifica os campos configuráveis no banco de dados de destino e fornece um modelo para a configuração de cada campo. |
| [Tabela ModuleConfiguration](moduleconfiguration-table.md) | NECESSÁRIA Essa tabela não é mesclada no banco de dados de instalação de destino. Identifica os atributos configuráveis do módulo.                                                                 |



 

As tabelas do instalador a seguir não podem ocorrer em um módulo de mesclagem padrão.

-   [BBControl](bbcontrol-table.md)
-   [Mensagem](billboard-table.md)
-   [CCPSearch](ccpsearch-table.md)
-   [Erro](error-table.md)
-   [Recurso](feature-table.md)
-   [Tabela LaunchCondition](launchcondition-table.md)
-   [Mídia](media-table.md)
-   [Patch](patch-table.md)
-   [Atualizar](upgrade-table.md)

As tabelas do instalador a seguir são opcionais em módulos de mesclagem.

-   [ActionText](actiontext-table.md)
-   [AdminExecuteSequence](adminexecutesequence-table.md)
-   [AdminUISequence](adminuisequence-table.md)
-   [AdvtExecuteSequence](advtexecutesequence-table.md)
-   [AdvtUISequence](advtuisequence-table.md)
-   [AppId](appid-table.md)
-   [AppSearch](appsearch-table.md)
-   [BindImage](bindimage-table.md)
-   [CheckBox](checkbox-table.md)
-   [Classe](class-table.md)
-   [ComboBox](combobox-table.md)
-   [CompLocator](complocator-table.md)
-   [Controle](control-table.md)
-   [ControlCondition](controlcondition-table.md)
-   [CreateFolder](createfolder-table.md)
-   [CustomAction](customaction-table.md)
-   [Diálogo](dialog-table.md)
-   [DrLocator](drlocator-table.md)
-   [Duplicatafile](duplicatefile-table.md)
-   [Ambiente](environment-table.md)
-   [EventMappings](eventmapping-table.md)
-   [Extensão](extension-table.md)
-   [Fonte](font-table.md)
-   [Ícone](icon-table.md)
-   [IniFile](inifile-table.md)
-   [IniLocator](inilocator-table.md)
-   [InstallExecuteSequence](installexecutesequence-table.md)
-   [InstallUISequence](installuisequence-table.md)
-   [ListBox](listbox-table.md)
-   [ListView](listview-table.md)
-   [MIME](mime-table.md)
-   [MoveFile](movefile-table.md)
-   [ODBCattribute](odbcattribute-table.md)
-   [ODBCDataSource](odbcdatasource-table.md)
-   [ODBCDriver](odbcdriver-table.md)
-   [ODBCSourceAttribute](odbcsourceattribute-table.md)
-   [ODBCTranslator](odbctranslator-table.md)
-   [Tabela ProgID](progid-table.md)
-   [Propriedade](property-table.md)
-   [PublishComponent](publishcomponent-table.md)
-   [RadioButton](radiobutton-table.md)
-   [Tabela do registro](registry-table.md)
-   [RegLocator](reglocator-table.md)
-   [RemoveFile](removefile-table.md)
-   [RemoveIniFile](removeinifile-table.md)
-   [RemoveRegistry](removeregistry-table.md)
-   [ReserveCost](reservecost-table.md)
-   [SelfReg](selfreg-table.md)
-   [ServiceControl](servicecontrol-table.md)
-   [Instalar o](serviceinstall-table.md)
-   [Atalho](shortcut-table.md)
-   [Signature](signature-table.md)
-   [Estilo]](textstyle-table.md)
-   [Importação](typelib-table.md)
-   [UIText](uitext-table.md)
-   [Verbo](verb-table.md)

 

 



