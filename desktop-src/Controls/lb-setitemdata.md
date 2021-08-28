---
title: LB_SETITEMDATA mensagem (Winuser.h)
description: Define um valor associado ao item especificado em uma caixa de listagem.
ms.assetid: df974fa2-114a-43ef-b0ac-0451c31d95cd
keywords:
- LB_SETITEMDATA controles Windows mensagem
topic_type:
- apiref
api_name:
- LB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd9a705014ef770edba5b540a7acbd2512b685d5ebf8ca913df8fa329dc6058a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085326"
---
# <a name="lb_setitemdata-message"></a>Mensagem LB \_ SETITEMDATA

Define um valor associado ao item especificado em uma caixa de listagem.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o índice baseado em zero do item. Se esse valor for -1, o *valor lParam* se aplicará a todos os itens na caixa de listagem.

Windows 95/Windows 98/Windows Edition DaNium (Windows Me): o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica o valor a ser associado ao item.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se ocorrer um erro, o valor de retorno será LB \_ ERR.

## <a name="remarks"></a>Comentários

Se o item estiver em uma caixa de listagem desenhada pelo proprietário criada sem o estilo [**\_ HASSTRINGS do LBS,**](list-box-styles.md) essa mensagem substituirá o valor contido no parâmetro *lParam* da mensagem [**LB \_ ADDSTRING**](lb-addstring.md) ou [**LB \_ INSERTSTRING**](lb-insertstring.md) que adicionou o item à caixa de listagem.

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

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ GETITEMDATA**](lb-getitemdata.md)
</dt> <dt>

[**LB \_ INSERTSTRING**](lb-insertstring.md)
</dt> </dl>

 

 





