---
title: PGM_SETBUTTONSIZE mensagem (Commctrl.h)
description: Define o tamanho atual do botão para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a \_ macro Pager SetButtonSize.
ms.assetid: b31960f8-87c2-4209-8213-df75ac883e11
keywords:
- PGM_SETBUTTONSIZE controles de Windows mensagem
topic_type:
- apiref
api_name:
- PGM_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b120ed4bd6b7090621e09dd24b9e6a23b037fb5aed83e7ac6fc43254393330e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046786"
---
# <a name="pgm_setbuttonsize-message"></a>Mensagem PGM \_ SETBUTTONSIZE

Define o tamanho atual do botão para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a macro [**\_ Pager SetButtonSize.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor do tipo **int** que contém o novo tamanho do botão, em pixels.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor int** que contém o tamanho do botão anterior, em pixels.

## <a name="remarks"></a>Comentários

Se o controle pager tiver o estilo [**\_ PGS HORZ,**](pager-control-styles.md) o tamanho do botão determinará a largura dos botões do pager. Se o controle pager tiver o [**estilo \_ PGS VERT,**](pager-control-styles.md) o tamanho do botão determinará a altura dos botões do pager. Por padrão, o controle de pager define o tamanho do botão como três quartos da largura da barra de rolagem.

Há um tamanho mínimo para o botão de pager, atualmente 12 pixels. No entanto, isso pode mudar para que você não dependa desse valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PGM \_ GETBUTTONSIZE**](pgm-getbuttonsize.md)
</dt> </dl>

 

 





