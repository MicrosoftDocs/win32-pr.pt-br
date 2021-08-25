---
title: EM_CALLAUTOCORRECTPROC mensagem (Richedit.h)
description: Chama a função de retorno de chamada de correção automática armazenada pela mensagem EM SETAUTOCORRECTPROC, desde que o texto anterior ao ponto de inserção seja candidato \_ à correção automática.
ms.assetid: 93116467-B345-4FD9-9162-3E01CF3C6F20
keywords:
- EM_CALLAUTOCORRECTPROC controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_CALLAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ad76ec66018b4e673913c433ce16a1294944f69c9d33a5dbaedb85ba21f985a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916076"
---
# <a name="em_callautocorrectproc-message"></a>Mensagem EM \_ CALLAUTOCORRECTPROC

Chama a função de retorno de chamada de correção automática armazenada pela mensagem [**EM \_ SETAUTOCORRECTPROC,**](em-setautocorrectproc.md) desde que o texto anterior ao ponto de inserção seja candidato à correção automática.


```C++
#define EM_CALLAUTOCORRECTPROC       (WM_USER + 255)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um caractere do tipo **WCHAR.** Se esse caractere for uma guia (U+0009) e o caractere que precede o ponto de inserção não for uma guia, o caractere que precede o ponto de inserção será tratado como parte da cadeia de caracteres candidata de correção automática em vez de como um separador de cadeia de caracteres; caso contrário, *wParam* não terá nenhum efeito.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno será zero se a mensagem for bem-sucedida ou não zero se ocorrer um erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[**EM \_ GETAUTOCORRECTPROC**](em-getautocorrectproc.md)
</dt> <dt>

[**EM \_ SETAUTOCORRECTPROC**](em-setautocorrectproc.md)
</dt> </dl>

 

 





