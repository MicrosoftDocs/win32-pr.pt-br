---
description: As propriedades de Windows Installer são variáveis globais que o instalador usa durante uma instalação.
ms.assetid: 1c59939b-de0f-4bf4-ab1f-4f1aa2488bfa
title: Especificando propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cd4294f35595e723491398172dc4c73337a1416
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752634"
---
# <a name="specifying-properties"></a>Especificando propriedades

As propriedades de Windows Installer são variáveis globais que o instalador usa durante uma instalação. Consulte as seções em [Propriedades](properties.md). Se na seção [importando um banco de dados em branco](importing-a-blank-database.md) que você usou uisample.msi do SDK do Windows Installer, a [tabela de propriedades](property-table.md) em sua cópia do MNP2000.msi já contém muitas propriedades que são usadas pela interface do usuário. Nesta seção, você adiciona informações adicionais à tabela de propriedades específica à instalação do exemplo do bloco de notas. Consulte também o [grupo tabelas de informações do programa](program-information-tables-group.md).

Há cinco propriedades que são necessárias em todos os pacotes de instalação, e elas devem ser atualizadas para o exemplo do bloco de notas na [tabela de propriedades](property-table.md) de MNP2000.msi:

-   [**ProductCode**](productcode.md)
-   [**ProductLanguage**](productlanguage.md)
-   [**Manufacturer**](manufacturer.md)
-   [**ProductVersion**](productversion.md)
-   [**ProductName**](productname.md)

Embora não seja exigido por todos os pacotes de instalação, os aplicativos que podem, no futuro, receber uma atualização também devem ter uma propriedade [**UpgradeCode**](upgradecode.md) . Consulte [preparando um aplicativo para atualizações importantes futuras](preparing-an-application-for-future-major-upgrades.md).

Use o editor de banco de dados para abrir MNP2000.msi e insira os dados a seguir na tabela de propriedades. A lista fornece links para os tópicos de referência para as propriedades internas do instalador. Os nomes de propriedade que não são links são propriedades definidas pelo autor. Muitas das propriedades importadas de uisample.msi são para a interface do usuário de exemplo. A interface do usuário da seção posterior para o exemplo de instalação aborda a interface do usuário.

[Tabela de propriedades](property-table.md)



| Propriedade                                         | Valor                                     |
|--------------------------------------------------|-------------------------------------------|
| [**ARPHELPLINK**](arphelplink.md)               | https://www.microsoft.com/management       |
| BannerBitmap                                     | bannrbmp                                  |
| ButtonText \_ voltar                                 | < &de volta                                |
| ButtonText \_ procurar                               | Br&owse                                   |
| ButtonText \_ cancelar                               | Cancelar                                    |
| ButtonText \_ sair                                 | &sair                                     |
| ButtonText \_ concluir                               | &concluir                                   |
| \_Ignorar ButtonText                               | Ignorar &                                   |
| ButtonText \_ instalar                              | &instalar                                  |
| ButtonText \_ próximo                                 | &próximo >                                |
| ButtonText \_ não                                   | &não                                       |
| ButtonText \_ OK                                   | OK                                        |
| ButtonText \_ remover                               | &remover                                   |
| Redefinição de ButtonText \_                                | Redefinição de &                                    |
| Retomar ButtonText \_                               | Retomar &                                   |
| Repetição de ButtonText \_                                | Tentar novamente &                                    |
| ButtonText \_ retornar                               | &retornar                                   |
| ButtonText \_ Sim                                  | &Sim                                      |
| CompleteSetupIcon                                | completo                                  |
| ComponentDownload                                | ftp://anonymous@microsoft.com/components/ |
| CustomSetupIcon                                  | custicon                                  |
| [**DefaultUIFont**](defaultuifont.md)           | DlgFont8                                  |
| DialogBitmap                                     | dlgbmp                                    |
| DlgTitleFont                                     | {&DlgFontBold8}                           |
| ErrorDialog                                      | ErrorDlg                                  |
| ExclamationIcon                                  | exclamated                                  |
| Falso                                            | 0                                         |
| Iagree                                           | No                                        |
| InfoIcon                                         | informações                                      |
| InstallerIcon                                    | insticon                                  |
| [**INSTALLLEVEL**](installlevel.md)             | 3                                         |
| InstallMode                                      | Típico                                   |
| [**Manufacturer**](manufacturer.md)             | Microsoft                                 |
| [**PIDTemplate**](pidtemplate.md)               | 12345<\#\#\#-%%%%%%%>@@@@@          |
| [**ProductCode**](productcode.md)               | {18A9233C-0B34-4127-A966-C257386270BC}    |
| [**ProductID**](productid.md)                   | nenhum                                      |
| [**ProductLanguage**](productlanguage.md)       | 1046                                      |
| [**ProductName**](productname.md)               | MNP2000                                   |
| [**ProductVersion**](productversion.md)         | 01.40.0000                                |
| Progress1                                        | Instalando                                |
| Progress2                                        | installs                                  |
| [**PROMPTROLLBACKCOST**](promptrollbackcost.md) | P                                         |
| RemoveIcon                                       | removico                                  |
| RepairIcon                                       | de reparo                                  |
| Instalação                                            | Instalação                                     |
| True                                             | 1                                         |
| [**UpgradeCode**](upgradecode.md)               | {908E378A-9551-4772-BF1D-5CFAF6FD9CB4}    |
| Assistente                                           | Assistente para Instalação                              |



 

[Continuar](importing-the-installexecutesequence.md)

 

 



