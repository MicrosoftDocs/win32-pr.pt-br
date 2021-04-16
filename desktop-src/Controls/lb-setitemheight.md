---
title: Mensagem de LB_SETITEMHEIGHT (WinUser. h)
description: Define a altura, em pixels, de itens em uma caixa de listagem. Se a caixa de listagem tiver o \_ estilo de lbs OwnerDrawVariable, essa mensagem definirá a altura do item especificado pelo parâmetro wParam. Caso contrário, essa mensagem define a altura de todos os itens na caixa de listagem.
ms.assetid: 3ac8e935-6de8-465f-a525-1f493b06ee7c
keywords:
- Controles de LB_SETITEMHEIGHT de mensagens do Windows
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
ms.openlocfilehash: 9985c5131a9eb1c8f0c45b6ab399b9e270f962cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455754"
---
# <a name="lb_setitemheight-message"></a>SETITEMHEIGHT de mensagens de LB \_

Define a altura, em pixels, de itens em uma caixa de listagem. Se a caixa de listagem tiver o estilo de [**lbs \_ OwnerDrawVariable**](list-box-styles.md) , essa mensagem definirá a altura do item especificado pelo parâmetro *wParam* . Caso contrário, essa mensagem define a altura de todos os itens na caixa de listagem.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o índice de base zero do item na caixa de listagem. Use esse parâmetro somente se a caixa de listagem tiver o estilo de [**lbs \_ OwnerDrawVariable**](list-box-styles.md) ; caso contrário, defina-o como zero.

Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica a altura, em pixels, do item. A altura máxima é de 255 pixels.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o índice ou a altura for inválido, o valor de retorno será um erro de LB \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_GETITEMHEIGHT lb**](lb-getitemheight.md)
</dt> </dl>

 

 





