---
title: Propriedade KeyboardShortcut
description: A Propriedade KeyboardShortcut descreve uma combinação de chave ou chave que ativa um objeto acessível especificado.
ms.assetid: 42587468-f069-4ef1-868e-ac6a285e1715
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002c925151f3f1acc136190d7807d7bc814d30b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159840"
---
# <a name="keyboardshortcut-property"></a>Propriedade KeyboardShortcut

A propriedade **KeyboardShortcut** descreve uma combinação de chave ou chave que ativa um objeto acessível especificado.

A propriedade **KeyboardShortcut** é recuperada chamando [**IAccessible:: get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut).

A cadeia de caracteres recuperada descreve uma *tecla de atalho* (também chamada de *acelerador de teclado*) ou uma chave de *acesso* (também chamada de *mnemônico*). Uma tecla de acesso é um caractere sublinhado no texto de um menu, item de menu ou rótulo de um controle, como um botão de ação.

A cadeia de caracteres recuperada deve conter o nome da chave junto com as chaves ou teclas de modificador. A cadeia de caracteres deve estar no seguinte formato para que os clientes possam analisá-lo facilmente: \[ \[ chave de modificador \] + \[ ... \] + \] nome da chave.

Os exemplos incluem ALT + F, CTRL + ALT + 4, WIN + F1, CTRL + ALT + SHIFT + BACKSPACE ou simplesmente Backspace.

A tabela a seguir lista as teclas modificadoras.



| Tecla modificadora | Descrição                        |
|--------------|------------------------------------|
| ALT          | Tecla modificador alternativo             |
| CTRL         | Tecla de modificador de controle               |
| ALTERNÂNCIA        | Tecla modificador de deslocamento                 |
| VENCEU          | Tecla de logotipo do Windows                   |
| FN           | Chave de função em computadores portáteis |



 

Não Localize cadeias de caracteres de atalho de teclado.

## <a name="handling-objects-that-have-both-key-types"></a>Manipulando objetos que têm os dois tipos de chave

Se um objeto tiver uma tecla de atalho e uma tecla de acesso, a propriedade **KeyboardShortcut** retornará a tecla de acesso. A chave de acesso é aquela que um usuário deve pressionar quando o objeto ou o pai do objeto tem o foco do teclado. Por exemplo, o item de menu **Imprimir** pode ter uma tecla de atalho (Ctrl + P) e uma tecla de acesso (P). Se um usuário pressionar CTRL + P enquanto o menu estiver ativo, nada acontecerá. Mas se um usuário pressionar P enquanto o menu estiver ativo, ele invocará a caixa de diálogo **Imprimir** do aplicativo. Nesse caso, a propriedade **KeyboardShortcut** é "P" para refletir o que o usuário deve pressionar quando o menu tem o foco do teclado.

 

 




