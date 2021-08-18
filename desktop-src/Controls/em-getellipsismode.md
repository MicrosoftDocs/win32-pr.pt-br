---
title: EM_GETELLIPSISMODE mensagem (Richedit.h)
description: Recupera o modo de reellipse atual.
ms.assetid: 01A755F3-6C6E-4974-9866-76BF15E0F3AD
keywords:
- EM_GETELLIPSISMODE controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_GETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6706c2b6ee75852fd0b3ee7a1a9d18b25d20d242d72068ba073d1bb025ff8ed5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019694"
---
# <a name="em_getellipsismode-message"></a>Mensagem EM \_ GETELLIPSISMODE

Recupera o modo de reellipse atual. Quando habilitada, uma reellipse ( ) é exibida para o texto que não se ajusta à janela de exibição. As reellipses só são usadas quando o controle não está ativo. Quando ativas, as barras de rolagem são usadas para revelar texto que não se ajusta à janela de exibição.


```C++
#define EM_GETELLIPSISMODE       (WM_USER + 305)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para um DWORD que recebe um dos valores a seguir.



| Valor                                                                                                                                                         | Significado                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <dt>**REELLIPSIS \_ NONE**</dt> </dl> | Nenhuma reellipse é usada.<br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <dt>**FIM DAS \_ REELLIPSES**</dt> </dl>    | Reellipses no final (quebra forçada).<br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <dt>**PALAVRA DE \_ RELIPSIS**</dt> </dl> | Reellipse no final (quebra de palavra).<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se wparam for 0 e lparam não for NULL, o valor de retorno será igual a TRUE; caso contrário, o valor de retorno será igual a FALSE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EM \_ SETELLIPSISMODE**](em-setellipsismode.md)
</dt> <dt>

[**EM \_ GETELLIPSISSTATE**](em-getellipsisstate.md)
</dt> </dl>

 

 





