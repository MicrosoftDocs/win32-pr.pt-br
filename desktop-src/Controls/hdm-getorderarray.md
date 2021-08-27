---
title: Mensagem de HDM_GETORDERARRAY (commctrl. h)
description: Obtém a ordem da esquerda para a direita atual de itens em um controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetOrderArray do cabeçalho.
ms.assetid: b287d3c1-ae61-41a4-a884-dc008eb24ad8
keywords:
- controles de Windows de mensagem de HDM_GETORDERARRAY
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
ms.openlocfilehash: f374424fe3f1d84c4919c26948486a9bae1660072975556aecaac4b08b85b33b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062826"
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

## <a name="return-value"></a>Valor retornado

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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





