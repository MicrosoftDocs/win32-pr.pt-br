---
title: CB_GETCURSEL mensagem (Winuser.h)
description: Um aplicativo envia uma mensagem CB GETCURSEL para recuperar o índice do item selecionado no momento, se for o caso, na caixa de listagem de \_ uma caixa de combinação.
ms.assetid: 47bf87f6-637f-48e9-849e-b2acbe5a6a7b
keywords:
- CB_GETCURSEL controles de Windows mensagem
topic_type:
- apiref
api_name:
- CB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9bc51f43fd28563be4bc3f024bf6afd35c297648aa6c6cad677aca4582c3737
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089256"
---
# <a name="cb_getcursel-message"></a>Mensagem \_ CB GETCURSEL

Um aplicativo envia uma mensagem **\_ CB GETCURSEL** para recuperar o índice do item selecionado no momento, se for o caso, na caixa de listagem de uma caixa de combinação.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é o índice baseado em zero do item selecionado no momento. Se nenhum item for selecionado, ele será CB \_ ERR.

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

[**CB \_ SELECTSTRING**](cb-selectstring.md)
</dt> <dt>

[**CB \_ SETCURSEL**](cb-setcursel.md)
</dt> </dl>

 

 





