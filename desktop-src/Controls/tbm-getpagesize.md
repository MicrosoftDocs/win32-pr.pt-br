---
title: TBM_GETPAGESIZE mensagem (Commctrl.h)
description: Recupera o número de posições lógicas que o controle deslizante da barra de faixa move em resposta à entrada do teclado, como as teclas ou ou a entrada do mouse, como cliques no canal da barra de faixa.
ms.assetid: f0c5feac-2723-440e-96c0-dac37b0531ed
keywords:
- TBM_GETPAGESIZE controles Windows mensagem
topic_type:
- apiref
api_name:
- TBM_GETPAGESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1aa3ef3412fd00c18972b62d4d868ff1dbc97cb4787693b3746281b4884706e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046496"
---
# <a name="tbm_getpagesize-message"></a>Mensagem \_ GETPAGESIZE do TBM

Recupera o número de posições lógicas que o controle deslizante da barra de faixa move em resposta à entrada do teclado, como as teclas ou ou a entrada do mouse, como cliques no canal da barra de faixa. As posições lógicas são os incrementos inteiros no intervalo da barra de faixa de posições mínimas para máximas do controle deslizante.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor de 32 bits que especifica o tamanho da página para a barra de faixas.

## <a name="remarks"></a>Comentários

A barra de faixa também envia uma mensagem [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) com os códigos de notificação PAGEUP e PAGEDOWN de TB para sua janela pai quando recebe uma entrada do teclado ou mouse que rola a \_ \_ página.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TBM \_ SETPAGESIZE**](tbm-setpagesize.md)
</dt> </dl>

 

 





