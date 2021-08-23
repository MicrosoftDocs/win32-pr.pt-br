---
title: LB_SETCOUNT mensagem (Winuser.h)
description: Define a contagem de itens em uma caixa de listagem criada com o estilo NODATA LBS e não criada com o estilo \_ \_ HASSTRINGS do LBS.
ms.assetid: 3ebc4237-24d3-443f-86d5-bdcd66a31baf
keywords:
- LB_SETCOUNT controles de Windows mensagem
topic_type:
- apiref
api_name:
- LB_SETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e1b3f68a67de2b7caa77cfd7c9e6f2a5b164e20af42100882fef1aad04eca14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119433937"
---
# <a name="lb_setcount-message"></a>Mensagem \_ LB SETCOUNT

Define a contagem de itens em uma caixa de listagem criada com o estilo [**\_ NODATA LBS**](list-box-styles.md) e não criada com o estilo [**\_ HASSTRINGS do LBS.**](list-box-styles.md)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica a nova contagem de itens na caixa de listagem.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se ocorrer um erro, o valor de retorno será LB \_ ERR. Se não houver memória suficiente para armazenar os itens, o valor de retorno será LB \_ ERRSPACE.

## <a name="remarks"></a>Comentários

A **mensagem \_ LB SETCOUNT** tem suporte apenas por caixas de listagem criadas com o estilo [**\_ NODATA lbS**](list-box-styles.md) e não criadas com o estilo [**\_ HASSTRINGS do LBS.**](list-box-styles.md) Todas as outras caixas de listagem retornam \_ LB ERR.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LB \_ GETCOUNT**](lb-getcount.md)
</dt> </dl>

 

 





