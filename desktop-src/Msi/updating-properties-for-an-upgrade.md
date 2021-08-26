---
description: Como a atualização altera o nome do arquivo .msi e altera o código do componente de alguns componentes, o código do produto da atualização deve ser alterado do produto original.
ms.assetid: ebb1a217-fce6-43f0-9139-c0f4422c8fc4
title: Atualizando propriedades para uma atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d340f56eaf78c585e28a52dc7b310bf1af047d7530e61b841267bc0b83251a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039176"
---
# <a name="updating-properties-for-an-upgrade"></a>Atualizando propriedades para uma atualização

Como a atualização altera o nome do arquivo .msi e altera o código do componente de alguns componentes, o código do produto da atualização deve ser alterado do produto original. Para ver uma descrição dos casos em que uma atualização é necessária para alterar a [**propriedade ProductCode,**](productcode.md) consulte [Alterando o código do produto](changing-the-product-code.md). Uma atualização que altera o ProductCode é conhecida como atualização [principal.](major-upgrades.md)

A propriedade [**ProductName**](productname.md) do pacote de atualização, a propriedade [**ProductVersion,**](productversion.md) a propriedade [**ProductLanguage**](productlanguage.md) e a propriedade [**UpgradeCode**](upgradecode.md) podem ser alteradas ou deixadas inalteradas do produto original. Com base nos valores dessas propriedades, Windows Instalador pode determinar se os pacotes de atualização futuros serão aplicados à atualização atual.

A propriedade especificada na coluna ActionProperty da tabela [Upgrade](upgrade-table.md) deve ser adicionada à [**propriedade SecureCustomProperties.**](securecustomproperties.md)

Use o editor de banco de dados para MNP2001.msi e insira os dados a seguir na [tabela Propriedade](property-table.md). A lista fornece links para os tópicos de referência para propriedades do instalador internos. Os nomes de propriedade que não são links são propriedades definidas pelo autor. Muitas das propriedades foram importadas do Uisample.msi que vem com o SDK. Para obter detalhes, [consulte Importando o Interface do Usuário](importing-the-user-interface.md).

[Tabela de propriedades](property-table.md)



| Propriedade                                         | Valor                                     |
|--------------------------------------------------|-------------------------------------------|
| [**ARPHELPLINK**](arphelplink.md)               | https://www.microsoft.com/management       |
| BannerBitmap                                     | bannrbmp                                  |
| ButtonText \_ Back                                 | < &Voltar                                |
| ButtonText \_ Browse                               | Br&owse                                   |
| ButtonText \_ Cancel                               | Cancelar                                    |
| Saída \_ de ButtonText                                 | &sair                                     |
| ButtonText \_ Finish                               | &concluir                                   |
| ButtonText \_ Ignore                               | &Ignorar                                   |
| Instalação \_ de ButtonText                              | &instalação                                  |
| ButtonText \_ Next                                 | &próximo >                                |
| ButtonText \_ Não                                   | &Não                                       |
| ButtonText \_ OK                                   | OK                                        |
| ButtonText \_ Remove                               | &Remover                                   |
| ButtonText \_ Reset                                | &redefinição                                    |
| ButtonText \_ Resume                               | &retomar                                   |
| ButtonText \_ Retry                                | &repetir                                    |
| Retorno \_ de ButtonText                               | &retorno                                   |
| ButtonText \_ Sim                                  | &Sim                                      |
| CompleteSetupIcon                                | completi                                  |
| ComponentDownload                                | ftp://anonymous@microsoft.com/components/ |
| CustomSetupIcon                                  | custicon                                  |
| [**DefaultUIFont**](defaultuifont.md)           | DlgFont8                                  |
| DialogBitmap                                     | dlgbmp                                    |
| DlgTitleFont                                     | {&DlgFontBold8}                           |
| ErrorDialog                                      | ErrorDlg                                  |
| ExclamationIcon                                  | exclama                                  |
| Falso                                            | 0                                         |
| Iagree                                           | Não                                        |
| InfoIcon                                         | informações                                      |
| InstallerIcon                                    | insticon                                  |
| [**INSTALLLEVEL**](installlevel.md)             | 3                                         |
| InstallMode                                      | Típico                                   |
| [**Fabricante**](manufacturer.md)             | Microsoft                                 |
| [**PIDTemplate**](pidtemplate.md)               | 12345<\#\#\#-%%%%%%%>@@@@@          |
| [**ProductCode**](productcode.md)               | {34CF587C-1D8F-4DD5-ADFE-440F4B593987}    |
| [**Productid**](productid.md)                   | nenhum                                      |
| [**ProductLanguage**](productlanguage.md)       | 1046                                      |
| [**Productname**](productname.md)               | MNP2001                                   |
| [**Productversion**](productversion.md)         | 01.50.0000                                |
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

 

 



