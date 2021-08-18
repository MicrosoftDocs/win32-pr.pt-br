---
title: LB_GETITEMDATA mensagem (Winuser.h)
description: Obtém o valor definido pelo aplicativo associado ao item de caixa de listagem especificado.
ms.assetid: 3a3f7fa5-ce04-4e95-86e1-5c7de796d1b6
keywords:
- LB_GETITEMDATA controles Windows mensagem
topic_type:
- apiref
api_name:
- LB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bbfdb091fb98c0cf448af1cf5f554f7d0db2b03f53826154f7d62f2f6b27b62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019334"
---
# <a name="lb_getitemdata-message"></a>Mensagem \_ LB GETITEMDATA

Obtém o valor definido pelo aplicativo associado ao item de caixa de listagem especificado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice do item.

Windows 95/Windows 98/Windows Edition DaNium (Windows Me) : o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é o valor associado ao item ou LB \_ ERR se ocorrer um erro. Se o item estiver em uma caixa de listagem desenhada pelo proprietário e tiver sido criado sem o estilo [**\_ HASSTRINGS do LBS,**](list-box-styles.md) esse valor estava no parâmetro *lParam* da mensagem [**LB \_ ADDSTRING**](lb-addstring.md) ou [**LB \_ INSERTSTRING**](lb-insertstring.md) que adicionou o item à caixa de listagem. Caso contrário, será o valor no *lParam* da mensagem [**LB \_ SETITEMDATA.**](lb-setitemdata.md)

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

[**LB \_ INSERTSTRING**](lb-insertstring.md)
</dt> <dt>

[**LB \_ SETITEMDATA**](lb-setitemdata.md)
</dt> </dl>

 

 





