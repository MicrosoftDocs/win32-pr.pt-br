---
description: Além das informações discutidas nas seções anteriores, uisample.msi também contém dados para uma interface do usuário de exemplo.
ms.assetid: 7e4ae4b8-e7b2-49b3-97b7-374b69006a2f
title: Importando a interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2957dbec645bb85121c9748de83bc5c96ad04b05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827349"
---
# <a name="importing-the-user-interface"></a>Importando a interface do usuário

Além das informações discutidas nas seções anteriores, uisample.msi também contém dados para uma interface do usuário de exemplo. Se você mesclou uisample.msi em MNP2000.msi na seção [importando um banco de dados em branco](importing-a-blank-database.md), essas informações também estão presentes no MNP2000.msi. As informações para a interface do usuário de exemplo estão nas tabelas a seguir.

-   [Tabela ActionText](actiontext-table.md)
-   [Tabela binária](binary-table.md)
-   [Tabela de controle](control-table.md)
-   [Tabela ControlEvent,](controlevent-table.md)
-   [Tabela de diálogo](dialog-table.md)
-   [Tabela de erros](error-table.md)
-   [Tabela EventMappings](eventmapping-table.md)
-   [Tabela de botões de opção](radiobutton-table.md)
-   [Tabela TextStyle](textstyle-table.md)
-   [Tabela UIText](uitext-table.md)

O editor de banco de dados Orca fornecido com o instalador inclui uma opção de visualização de diálogo que você pode usar para visualizar as caixas de diálogo da interface do usuário que é especificada pelos dados nas tabelas acima.

O pacote de instalação de exemplo MNP2000.msi agora está pronto para a validação do pacote. Sempre execute a validação em um novo pacote antes de tentar instalar o pacote pela primeira vez. Isso é discutido na validação do exemplo de instalação.

Se você não quiser incluir a interface do usuário no pacote de exemplo, omita ou remova todas as informações nas tabelas mostradas acima, exceto a [tabela TextStyle](textstyle-table.md) (que é necessária para definir a propriedade [**DefaultUIFont**](defaultuifont.md) ). Você também deve remover as propriedades da interface do usuário da [tabela de propriedades](property-table.md). Uma tabela de propriedades de exemplo para o exemplo do bloco de notas, sem uma interface do usuário, é mostrada abaixo. Não reutilize os GUIDs mostrados na tabela se você copiar este exemplo.

[Tabela de propriedades](property-table.md)



| Propriedade                                   | Valor                                  |
|--------------------------------------------|----------------------------------------|
| [**DefaultUIFont**](defaultuifont.md)     | DlgFont8                               |
| [**INSTALLLEVEL**](installlevel.md)       | 3                                      |
| [**LIMITUI**](limitui.md)                 | 1                                      |
| [**Manufacturer**](manufacturer.md)       | Microsoft                              |
| [**ProductCode**](productcode.md)         | {18A9233C-0B34-4127-A966-C257386270BC} |
| [**ProductLanguage**](productlanguage.md) | 1046                                   |
| [**ProductName**](productname.md)         | MNP2000                                |
| [**ProductVersion**](productversion.md)   | 01.40.0000                             |
| [**UpgradeCode**](upgradecode.md)         | {908E378A-9551-4772-BF1D-5CFAF6FD9CB4} |



 

Um pacote sem uma interface do usuário pode ser instalado a partir da linha de comando ou de um programa. Para instalar um pacote da linha de comando, use os métodos descritos em [Opções de linha de comando](command-line-options.md). Para instalar um pacote de um programa, use os métodos descritos em [usando as funções do instalador](using-installer-functions.md). Sempre execute a validação em um novo pacote antes de tentar instalar um novo pacote pela primeira vez.

[Continuar](validating-an-installation-database.md)

 

 



