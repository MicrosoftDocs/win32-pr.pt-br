---
description: Além das informações discutidas nas seções anteriores, uisample.msi também contém dados para uma interface do usuário de exemplo.
ms.assetid: 7e4ae4b8-e7b2-49b3-97b7-374b69006a2f
title: Importando o Interface do Usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2678eb2c6fb1c53f0d052c6bb1553af0f3d773b75d057969c66d74a39e499f35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043635"
---
# <a name="importing-the-user-interface"></a>Importando o Interface do Usuário

Além das informações discutidas nas seções anteriores, uisample.msi também contém dados para uma interface do usuário de exemplo. Se você tiver mesclado uisample.msi em MNP2000.msi seção Importando um banco de dados em branco [,](importing-a-blank-database.md)essas informações também MNP2000.msi presentes. As informações da interface do usuário de exemplo estão nas tabelas a seguir.

-   [Tabela ActionText](actiontext-table.md)
-   [Tabela binária](binary-table.md)
-   [Tabela de controle](control-table.md)
-   [Tabela ControlEvent](controlevent-table.md)
-   [Tabela de diálogo](dialog-table.md)
-   [Tabela de erros](error-table.md)
-   [Tabela EventMapping](eventmapping-table.md)
-   [Tabela RadioButton](radiobutton-table.md)
-   [Tabela TextStyle](textstyle-table.md)
-   [Tabela UIText](uitext-table.md)

O editor de banco de dados Orca fornecido com o instalador inclui uma opção de visualização de caixa de diálogo que você pode usar para visualizar as caixas de diálogo da interface do usuário especificada pelos dados nas tabelas acima.

O pacote de instalação de exemplo MNP2000.msi agora está pronto para validação do pacote. Sempre execute a validação em um novo pacote antes de tentar instalar o pacote pela primeira vez. Isso é discutido em Validando o exemplo de instalação.

Se você não quiser incluir a interface do usuário no pacote de exemplo, omita ou remova todas as informações nas tabelas mostradas acima, exceto a tabela [TextStyle](textstyle-table.md) (que é necessária para definir a propriedade [**DefaultUIFont).**](defaultuifont.md) Você também deve remover as propriedades da interface do usuário da [Tabela de Propriedades](property-table.md). Uma tabela property de exemplo para o Bloco de notas, sem uma interface do usuário, é mostrada abaixo. Não reutilizar os GUIDs mostrados na tabela se você copiar este exemplo.

[Tabela de propriedades](property-table.md)



| Propriedade                                   | Valor                                  |
|--------------------------------------------|----------------------------------------|
| [**DefaultUIFont**](defaultuifont.md)     | DlgFont8                               |
| [**INSTALLLEVEL**](installlevel.md)       | 3                                      |
| [**LIMITUI**](limitui.md)                 | 1                                      |
| [**Fabricante**](manufacturer.md)       | Microsoft                              |
| [**ProductCode**](productcode.md)         | {18A9233C-0B34-4127-A966-C257386270BC} |
| [**ProductLanguage**](productlanguage.md) | 1046                                   |
| [**Productname**](productname.md)         | MNP2000                                |
| [**Productversion**](productversion.md)   | 01.40.0000                             |
| [**Upgradecode**](upgradecode.md)         | {908E378A-9551-4772-BF1D-5CFAF6FD9CB4} |



 

Um pacote sem uma interface do usuário pode ser instalado na linha de comando ou em um programa. Para instalar um pacote da linha de comando, use os métodos descritos em [Opções de Linha de Comando](command-line-options.md). Para instalar um pacote de um programa, use os métodos descritos em [Usando funções do instalador](using-installer-functions.md). Sempre execute a validação em um novo pacote antes de tentar instalar um novo pacote pela primeira vez.

[Continuar](validating-an-installation-database.md)

 

 



