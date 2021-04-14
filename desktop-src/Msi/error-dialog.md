---
description: Uma caixa de diálogo de erro é uma caixa de diálogo modal que exibe uma mensagem de erro. Mais de uma caixa de diálogo de erro pode existir em cada instalação.
ms.assetid: 11d4fe8b-ec5f-4576-95e5-c86344f0195c
title: Diálogo de erro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a153f5e6ee38235f830937d794a9ca9b81314583
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502055"
---
# <a name="error-dialog"></a>Diálogo de erro

Uma caixa de diálogo de erro é uma caixa de diálogo modal que exibe uma mensagem de erro. Mais de uma caixa de diálogo de erro pode existir em cada instalação.

É necessário definir uma propriedade ErrorDialog que especifica qual caixa de diálogo deve ser usada. Se essa propriedade não for definida ou não apontar para uma caixa de diálogo de erro válida, as mensagens de erro não serão exibidas. Nesse caso, o erro é registrado apenas com um aviso sobre a caixa de diálogo ausente.

Uma caixa de diálogo de erro deve ter o conjunto de [bits do estilo da caixa de diálogo de erro](error-dialog-style-bit.md) . A caixa de diálogo deve ter um [controle de texto](text-control.md) chamado ErrorText. O registro da caixa de diálogo de erro na [tabela de diálogo](dialog-table.md) deve ter o controle ErrorText inserido no \_ primeiro campo Control.

A caixa de diálogo deve conter sete [Supressãos](pushbutton-control.md). Todos esses botões especificam o [EndDialog](enddialog-controlevent.md) ControlEvent, na [tabela ControlEvent,](controlevent-table.md). Cada botão especifica um dos seguintes atributos: **ErrorAbort**, **ErrorCancel**, **ErrorIgnore**, **ErrorNo**, **ErrorOk**, **ErrorRetry**, **ErrorYes**.

> [!Note]  
> O foco desses controles não deve ser vinculado por meio do uso da \_ próxima coluna de controle na [tabela de controle](control-table.md).

 

Esses botões devem ser colocados em aproximadamente a mesma posição na caixa de diálogo porque, quando ele é criado, apenas um subconjunto desses sete botões é criado, dependendo da mensagem. A coordenada X dos botões é modificada para que os botões exibidos tenham espaçamento uniforme. A coordenada Y, a altura e a largura dos botões são inalteradas. Como os botões são organizados horizontalmente, nenhum outro controle pode ser colocado na mesma região horizontal da caixa de diálogo.

Para uma caixa de diálogo de erro, os campos de controle \_ padrão e de \_ cancelamento de controle na [tabela de diálogo](dialog-table.md) são ignorados. O \_ primeiro campo controlar para uma caixa de diálogo de erro deve especificar o controle ErrorText.

Se um [controle de ícone](icon-control.md) chamado ErrorIcon estiver incluído nessa caixa de diálogo, os seguintes ícones padrão do Windows serão exibidos:

-   \_Erro de Idi em resposta a mensagens imtFatalExit.
-   IDI \_ aviso em resposta às mensagens imtError e imtWarning.
-   IDI \_ informações em resposta a mensagens imtOutOfDiskSpace.

O controle ErrorIcon deve ser criado com o [atributo de controle FixedSize](fixedsize-control-attribute.md) definido para evitar o dimensionamento impróprio dos ícones padrão do Windows.

 

 



