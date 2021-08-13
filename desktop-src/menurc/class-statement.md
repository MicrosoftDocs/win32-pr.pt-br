---
title: Instrução CLASS
description: Define a classe da caixa de diálogo.
ms.assetid: 7c4325fe-66a4-4bb2-9c99-04b3ff590e7a
keywords:
- Menus de instrução CLASS e outros recursos
topic_type:
- apiref
api_name:
- CLASS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a71485603944dc8b7eaf1a3a773051096776e6538aecdd8fb01396a3f0ea5fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118734646"
---
# <a name="class-statement"></a>Instrução CLASS

Define a classe da caixa de diálogo.

A **instrução CLASS** aparece na seção opcional antes da [**principal**](dialog-resource.md) de uma instrução DIALOG. Se nenhuma classe for dada, a classe de diálogo padrão será usada.

``` syntax
CLASS class
```

<dl> <dt>

<span id="class"></span><span id="CLASS"></span>*Classe*
</dt> <dd>

Um inteiro sem sinal de 16 bits ou uma cadeia de caracteres, entre aspas duplas ("), que identifica a classe da caixa de diálogo. Se o procedimento de janela para a classe não processar uma mensagem enviada a ela, ela deverá chamar a função [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) para garantir que todas as mensagens sejam tratadas corretamente para a caixa de diálogo. Uma classe privada pode usar **DefDlgProc como** o procedimento de janela padrão. A classe deve ser registrada com **o membro cbWndExtra** da estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) definida como **DLGWINDOWEXTRA.**

</dd> </dl>

## <a name="remarks"></a>Comentários

A **instrução CLASS** só deve ser usada com casos especiais, pois substitui o processamento normal de uma caixa de diálogo. A **instrução CLASS** converte uma caixa de diálogo em uma janela da classe especificada; dependendo da classe , isso pode dar resultados indesejáveis. Não use os nomes de classe de controle redefinidos com essa instrução.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso da **instrução CLASS:**

``` syntax
CLASS "myclass" 
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**Diálogo**](dialog-resource.md)
</dt> </dl>

 

 