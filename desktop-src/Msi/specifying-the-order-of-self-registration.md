---
description: Observe que você não pode especificar a ordem na qual o instalador registra ou cancela o registro de DLLs de registro automático usando as ações SelfRegModules e SelfUnRegModules.
ms.assetid: 46ee5ea2-35fd-4352-8a45-572d6fb5e080
title: Especificando a ordem de auto-registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb26fbebad3167fbea95679a1ea7a29c28946ae6fa2dd2b014be6ade986e28f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039676"
---
# <a name="specifying-the-order-of-self-registration"></a>Especificando a ordem de auto-registro

Observe que você não pode especificar a ordem na qual o instalador registra ou cancela o registro de DLLs de registro automático usando as ações [SelfRegModules](selfregmodules-action.md) e [SelfUnRegModules](selfunregmodules-action.md) . Essas ações registram todos os módulos listados na [tabela selfreg](selfreg-table.md). O instalador não registra automaticamente .exe arquivos.

Para especificar a ordem na qual o instalador registra ou cancela o registro de módulos, você deve usar duas [ações personalizadas](custom-actions.md) para cada módulo. Uma ação personalizada para DllRegisterServer e um segundo para DllUnregisterServer. Essas ações personalizadas devem então ser criadas na [tabela InstallExecuteSequence](installexecutesequence-table.md) no ponto na sequência onde quer que a dll seja registrada ou cancelada.

O exemplo a seguir ilustra como criar o banco de dados para agendar o auto-registro de uma DLL em um ponto específico na sequência de ação.

[Tabela de arquivos](file-table.md) (parcial)



| Arquivo  | Componente\_ | FileName  | Sequência |
|-------|-------------|-----------|----------|
| mydll | myComponent | Mydll.dll | 13       |



 

[Tabela de componentes](component-table.md) (parcial)



| Componente   | ComponentId | Diretório\_ | KeyPath |
|-------------|-------------|-------------|---------|
| myComponent | {*GUID*}  | myFolder    | mydll   |



 

[Tabela de diretórios](directory-table.md)



| Diretório | Pai do diretório \_ | DefaultDir          |
|-----------|-------------------|---------------------|
| TARGETDIR |                   | SourceDir           |
| myFolder  | TARGETDIR         | Pasta de \| minha pasta |



 

[Tabela CustomAction](customaction-table.md)



| Ação     | Tipo | Fonte   | Destino                                     |
|------------|------|----------|--------------------------------------------|
| mydllREG   | 3170 | myFolder | " \[ SystemFolder \] msiexec"/y " \[ \# myDll \] " |
| mydllUNREG | 3170 | myFolder | " \[ SystemFolder \] msiexec"/z " \[ \# myDll \] " |



 

[Tabela InstallExecuteSequence](installexecutesequence-table.md) (parcial)



| Ação           | Condição         | Sequência |
|------------------|-------------------|----------|
| SelfUnregModules |                   | 2200     |
| mydllUNREG       | $myComponent = 2    | 2201     |
| Removes      |                   | 3500     |
| InstallFiles     |                   | 4000     |
| SelfRegModules   |                   | 6500     |
| mydllREG         | $myComponent>2 | 6501     |



 

 

 



