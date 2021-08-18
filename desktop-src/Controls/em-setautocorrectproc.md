---
title: Mensagem de EM_SETAUTOCORRECTPROC (RichEdit. h)
description: Define o procedimento de retorno de chamada da AutoCorreção atual.
ms.assetid: 2FA48CFC-0D7C-41EF-8207-5EDC644FF3BC
keywords:
- controles de Windows de mensagem de EM_SETAUTOCORRECTPROC
topic_type:
- apiref
api_name:
- EM_SETAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b46e838cf18a345272b7983de1522a0c55a2565c5df3e11e3c89cd820653fb73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958715"
---
# <a name="em_setautocorrectproc-message"></a>\_Mensagem em SETAUTOCORRECTPROC

Define o procedimento de retorno de chamada da AutoCorreção atual.


```C++
#define EM_SETAUTOCORRECTPROC       (WM_USER + 234)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A função de retorno de chamada [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) .

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a operação for concluída com sucesso, o valor de retorno será zero. Se a operação falhar, o valor de retorno será um valor diferente de zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[**em \_ CALLAUTOCORRECTPROC**](em-callautocorrectproc.md)
</dt> <dt>

[**em \_ GETAUTOCORRECTPROC**](em-getautocorrectproc.md)
</dt> </dl>

 

 





