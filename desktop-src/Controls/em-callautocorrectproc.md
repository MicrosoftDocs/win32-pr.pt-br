---
title: Mensagem de EM_CALLAUTOCORRECTPROC (RichEdit. h)
description: Chama a função de retorno de chamada de AutoCorreção armazenada pela \_ mensagem em SETAUTOCORRECTPROC, desde que o texto anterior ao ponto de inserção seja um candidato para correção automática.
ms.assetid: 93116467-B345-4FD9-9162-3E01CF3C6F20
keywords:
- Controles de EM_CALLAUTOCORRECTPROC de mensagens do Windows
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
ms.openlocfilehash: 73109d2499fc01a1d811066dc6059593c7ed5e0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455449"
---
# <a name="em_callautocorrectproc-message"></a>\_Mensagem em CALLAUTOCORRECTPROC

Chama a função de retorno de chamada de AutoCorreção armazenada pela mensagem em [**\_ SETAUTOCORRECTPROC**](em-setautocorrectproc.md) , desde que o texto anterior ao ponto de inserção seja um candidato para correção automática.


```C++
#define EM_CALLAUTOCORRECTPROC       (WM_USER + 255)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um caractere do tipo **WCHAR**. Se esse caractere for uma tabulação (U + 0009) e o caractere que precede o ponto de inserção não for uma guia, o caractere que precede o ponto de inserção será tratado como parte da cadeia de caracteres de candidato à AutoCorreção em vez de como um delimitador de cadeia de caracteres; caso contrário, *wParam* não terá efeito.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno será zero se a mensagem tiver sucesso ou for diferente de zero se ocorrer um erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[**em \_ GETAUTOCORRECTPROC**](em-getautocorrectproc.md)
</dt> <dt>

[**em \_ SETAUTOCORRECTPROC**](em-setautocorrectproc.md)
</dt> </dl>

 

 





