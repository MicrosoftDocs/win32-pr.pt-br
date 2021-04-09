---
description: Como a atualização altera o nome do arquivo. msi e altera o código do componente de alguns componentes, o código do produto da atualização deve ser alterado do produto original.
ms.assetid: ebb1a217-fce6-43f0-9139-c0f4422c8fc4
title: Atualizando Propriedades para uma atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750c30a75650ff4009dda799b0542f41f535481f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011719"
---
# <a name="updating-properties-for-an-upgrade"></a>Atualizando Propriedades para uma atualização

Como a atualização altera o nome do arquivo. msi e altera o código do componente de alguns componentes, o código do produto da atualização deve ser alterado do produto original. Para obter uma descrição dos casos em que uma atualização é necessária para alterar a propriedade [**ProductCode**](productcode.md) , consulte [alterando o código do produto](changing-the-product-code.md). Uma atualização que altera o ProductCode é conhecida como uma [atualização principal](major-upgrades.md).

A propriedade [**ProductName**](productname.md) do pacote de atualização, a propriedade [**ProductVersion**](productversion.md) , a propriedade [**ProductLanguage**](productlanguage.md) e a propriedade [**UpgradeCode**](upgradecode.md) podem ser alteradas ou deixadas inalteradas, do produto original. Com base nos valores dessas propriedades, Windows Installer pode determinar se deseja aplicar pacotes de atualização futuros à atualização atual.

A propriedade especificada na coluna Actionproperty da tabela de [atualização](upgrade-table.md) deve ser adicionada à propriedade [**SecureCustomProperties**](securecustomproperties.md) .

Use o editor de banco de dados para abrir MNP2001.msi e insira os dados a seguir na [tabela de propriedades](property-table.md). A lista fornece links para os tópicos de referência para as propriedades internas do instalador. Os nomes de propriedade que não são links são propriedades definidas pelo autor. Muitas das propriedades foram importadas de Uisample.msi que acompanham o SDK. Para obter detalhes, consulte [importando a interface do usuário](importing-the-user-interface.md).

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
| [**ProductCode**](productcode.md)               | {34CF587C-1D8F-4DD5-ADFE-440F4B593987}    |
| [**ProductID**](productid.md)                   | nenhum                                      |
| [**ProductLanguage**](productlanguage.md)       | 1046                                      |
| [**ProductName**](productname.md)               | MNP2001                                   |
| [**ProductVersion**](productversion.md)         | 01.50.0000                                |
| Progress1                                        | Instalando                                |
| Progress2                                        | installs                                  |
| [**PROMPTROLLBACKCOST**](promptrollbackcost.md) | P                                         |
| RemoveIcon                                       | removico                                  |
| RepairIcon                                       | de reparo                                  |
| Instalação                                            | Instalação                                     |
| True                                             | 1                                         |
| [**UpgradeCode**](upgradecode.md)               | {908E378A-9551-4772-BF1D-5CFAF6FD9CB4}    |
| Assistente                                           | Assistente para Instalação                              |
| SecureCustomProperties                           | OLDAPPFOUND                               |



 

[Continuar](updating-sequence-tables-for-an-upgrade.md)

 

 



