---
title: Mensagem de TBM_SETPAGESIZE (commctrl. h)
description: Define o número de posições lógicas que o controle deslizante do TrackBar move em resposta à entrada do teclado, como as chaves ou, ou entrada do mouse, como cliques no canal do TrackBar.
ms.assetid: 34edb868-4b6b-4b3f-b315-3ce39346b134
keywords:
- Controles de TBM_SETPAGESIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_SETPAGESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5d8a396bb605b4276346e84e7b46bfbefe0657
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009598"
---
# <a name="tbm_setpagesize-message"></a>TBMr a \_ mensagem de página

Define o número de posições lógicas que o controle deslizante do TrackBar move em resposta à entrada do teclado, como as chaves ou, ou entrada do mouse, como cliques no canal do TrackBar. As posições lógicas são os incrementos inteiros no intervalo de TrackBar de mínimo a máximo de posições do controle deslizante.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Novo tamanho da página.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor de 32 bits que especifica o tamanho da página anterior.

## <a name="remarks"></a>Comentários

O TrackBar também envia uma mensagem do [**WM \_ HSCROLL**](wm-hscroll.md) ou do [**WM \_ VSCROLL**](wm-vscroll.md) com os códigos de notificação de TB \_ PageUp e TB \_ PageDown para sua janela pai quando recebe entrada de teclado ou mouse que rola a página.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TBM \_ GETpagesize**](tbm-getpagesize.md)
</dt> </dl>

 

 





