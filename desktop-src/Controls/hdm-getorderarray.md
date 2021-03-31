---
title: Mensagem de HDM_GETORDERARRAY (commctrl. h)
description: Obtém a ordem da esquerda para a direita atual de itens em um controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetOrderArray do cabeçalho.
ms.assetid: b287d3c1-ae61-41a4-a884-dc008eb24ad8
keywords:
- Controles de HDM_GETORDERARRAY de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_GETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e334b0023ad3441c20048273e9bc58c1b25622b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085586"
---
# <a name="hdm_getorderarray-message"></a>\_Mensagem HDM GETORDERARRAY

Obtém a ordem da esquerda para a direita atual de itens em um controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetOrderArray do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O número de elementos inteiros que o *lParam* pode conter. Esse valor deve ser igual ao número de itens no controle (consulte [**HDM \_ GetItemCount**](hdm-getitemcount.md)).

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma matriz de inteiros que recebe os valores de índice para itens no cabeçalho.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido e o buffer em *lParam* receberá o número do item para cada item no controle de cabeçalho na ordem em que eles aparecem da esquerda para a direita. Caso contrário, a mensagem retornará zero.

## <a name="remarks"></a>Comentários

O número de elementos em *lParam* é especificado em *wParam* e deve ser igual ao número de itens no controle. Por exemplo, o fragmento de código a seguir reservará memória suficiente para manter os valores de índice.


```
int iItems,

    *lpiArray;



// Get memory for buffer.

(iItems = SendMessage(hwndHD, HDM_GETITEMCOUNT, 0,0))!=-1)

    if(!(lpiArray = calloc(iItems,sizeof(int))))

MessageBox(hwnd, "Out of memory.","Error", MB_OK);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





