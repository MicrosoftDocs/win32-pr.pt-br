---
title: LB_SETITEMHEIGHT mensagem (Winuser.h)
description: Define a altura, em pixels, dos itens em uma caixa de listagem. Se a caixa de listagem tiver o estilo LBS OWNERDRAWVARIABLE, essa mensagem define a altura do \_ item especificado pelo parâmetro wParam. Caso contrário, essa mensagem define a altura de todos os itens na caixa de listagem.
ms.assetid: 3ac8e935-6de8-465f-a525-1f493b06ee7c
keywords:
- LB_SETITEMHEIGHT controles Windows mensagem
topic_type:
- apiref
api_name:
- LB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bcd661c9fb32d2cbe0763f8c138d133f8a32b46d17201b33033b832aeb8cb49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119433866"
---
# <a name="lb_setitemheight-message"></a>Mensagem \_ LB SETITEMHEIGHT

Define a altura, em pixels, dos itens em uma caixa de listagem. Se a caixa de listagem tiver o estilo [**\_ LBS OWNERDRAWVARIABLE,**](list-box-styles.md) essa mensagem define a altura do item especificado pelo *parâmetro wParam.* Caso contrário, essa mensagem define a altura de todos os itens na caixa de listagem.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o índice baseado em zero do item na caixa de listagem. Use esse parâmetro somente se a caixa de listagem tiver o estilo [**LBS \_ OWNERDRAWVARIABLE;**](list-box-styles.md) caso contrário, de definido como zero.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica a altura, em pixels, do item. A altura máxima é de 255 pixels.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o índice ou a altura for inválido, o valor de retorno será LB \_ ERR.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LB \_ GETITEMHEIGHT**](lb-getitemheight.md)
</dt> </dl>

 

 





