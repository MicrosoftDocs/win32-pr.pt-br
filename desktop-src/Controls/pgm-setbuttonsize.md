---
title: Mensagem de PGM_SETBUTTONSIZE (commctrl. h)
description: Define o tamanho do botão atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetButtons do pager.
ms.assetid: b31960f8-87c2-4209-8213-df75ac883e11
keywords:
- Controles de PGM_SETBUTTONSIZE de mensagens do Windows
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
ms.openlocfilehash: ecf8c164ed960675c1a68be36acfe0eff40f972f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499330"
---
# <a name="pgm_setbuttonsize-message"></a>\_Mensagem de SETbuttons do PGM

Define o tamanho do botão atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetButtons do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor do tipo **int** que contém o novo tamanho do botão, em pixels.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **int** que contém o tamanho do botão anterior, em pixels.

## <a name="remarks"></a>Comentários

Se o controle de pager tiver o estilo [**PGS \_ na horizontal**](pager-control-styles.md) , o tamanho do botão determinará a largura dos botões da paginação. Se o controle de pager tiver o estilo [**\_ vertical PGS**](pager-control-styles.md) , o tamanho do botão determinará a altura dos botões da paginação. Por padrão, o controle de pager define seu tamanho de botão como três quartos da largura da barra de rolagem.

Há um tamanho mínimo para o botão de pager, no momento, 12 pixels. No entanto, isso pode ser alterado, portanto, você não deve depender desse valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**getbuttons do PGM \_**](pgm-getbuttonsize.md)
</dt> </dl>

 

 





