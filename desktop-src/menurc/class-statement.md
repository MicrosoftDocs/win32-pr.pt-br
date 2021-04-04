---
title: Declaração de classe
description: Define a classe da caixa de diálogo.
ms.assetid: 7c4325fe-66a4-4bb2-9c99-04b3ff590e7a
keywords:
- Menus de instruções de classe e outros recursos
topic_type:
- apiref
api_name:
- CLASS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d31eba66a1e4527a24a55a24e4623f3c49dc204
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917237"
---
# <a name="class-statement"></a>Declaração de classe

Define a classe da caixa de diálogo.

A instrução **Class** aparece na seção opcional antes de uma instrução de [**caixa de diálogo**](dialog-resource.md) Main. Se nenhuma classe for fornecida, a classe de diálogo padrão será usada.

``` syntax
CLASS class
```

<dl> <dt>

<span id="class"></span><span id="CLASS"></span>*classes*
</dt> <dd>

Um inteiro não assinado de 16 bits ou uma cadeia de caracteres entre aspas duplas ("), que identifica a classe da caixa de diálogo. Se o procedimento de janela da classe não processar uma mensagem enviada a ele, ele deverá chamar a função [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) para garantir que todas as mensagens sejam tratadas corretamente para a caixa de diálogo. Uma classe privada pode usar **DefDlgProc** como o procedimento de janela padrão. A classe deve ser registrada com o membro **cbWndExtra** da estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) definida como **DLGWINDOWEXTRA**.

</dd> </dl>

## <a name="remarks"></a>Comentários

A instrução de **classe** só deve ser usada com casos especiais, porque ela substitui o processamento normal de uma caixa de diálogo. A instrução **Class** converte uma caixa de diálogo em uma janela da classe especificada; dependendo da classe, isso pode dar resultados indesejáveis. Não use os nomes de classe de controle redefinidos com esta instrução.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso da instrução de **classe** :

``` syntax
CLASS "myclass" 
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**'**](dialog-resource.md)
</dt> </dl>

 

 