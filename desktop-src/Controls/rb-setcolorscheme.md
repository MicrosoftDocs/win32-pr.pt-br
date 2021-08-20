---
title: RB_SETCOLORSCHEME mensagem (Commctrl.h)
description: Define as informações do esquema de cores para o controle de barra de rebar.
ms.assetid: ddf8f3e4-66b7-4b53-a04e-b4dd372f71c4
keywords:
- RB_SETCOLORSCHEME controles de Windows mensagem
topic_type:
- apiref
api_name:
- RB_SETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce7715082a371c3632d8accb8fdf60bbac50d8d7d8182732d6a62c2dbb423c34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169272"
---
# <a name="rb_setcolorscheme-message"></a>Mensagem RB \_ SETCOLORSCHEME

Define as informações do esquema de cores para o controle de barra de rebar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) que contém as informações do esquema de cores.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno para essa mensagem não é usado.

## <a name="remarks"></a>Comentários

O controle rebar usa as informações do esquema de cores ao desenhar os elementos 3D no controle e nas faixas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RB \_ GETCOLORSCHEME**](rb-getcolorscheme.md)
</dt> </dl>

 

 





