---
title: CB_SETITEMDATA mensagem (Winuser.h)
description: Um aplicativo envia uma mensagem CB SETITEMDATA para definir o valor associado ao \_ item especificado em uma caixa de combinação.
ms.assetid: 8be9eb57-a635-4c52-9838-556368813c74
keywords:
- CB_SETITEMDATA controles de Windows mensagem
topic_type:
- apiref
api_name:
- CB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7abd50db9050178bc5d8d3b8ff556bce90f340fdb8d6692a514b0348aceeeab3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089006"
---
# <a name="cb_setitemdata-message"></a>Mensagem CB \_ SETITEMDATA

Um aplicativo envia uma **mensagem CB \_ SETITEMDATA** para definir o valor associado ao item especificado em uma caixa de combinação.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o índice baseado em zero do item.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica o novo valor a ser associado ao item.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se ocorrer um erro, o valor de retorno será CB \_ ERR.

## <a name="remarks"></a>Comentários

Se o item especificado estiver em uma caixa de combinação desenhada pelo proprietário criada sem o estilo [**\_ CBS HASSTRINGS,**](combo-box-styles.md) essa mensagem substituirá o valor no parâmetro *lParam* da mensagem [**CB \_ ADDSTRING**](cb-addstring.md) ou [**CB \_ INSERTSTRING**](cb-insertstring.md) que adicionou o item à caixa de combinação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**CB \_ GETITEMDATA**](cb-getitemdata.md)
</dt> <dt>

[**CB \_ INSERTSTRING**](cb-insertstring.md)
</dt> </dl>

 

 





