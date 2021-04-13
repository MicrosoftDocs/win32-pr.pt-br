---
title: Mensagem de WM_CAP_SET_SCROLL (VFW. h)
description: A \_ mensagem de \_ rolagem definir limite do WM \_ define a parte do quadro de vídeo a ser exibida na janela de captura.
ms.assetid: 545605e4-6b1f-403a-a3ab-0fd6750ae776
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_SCROLL
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCROLL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812b76bdcad166b9f766957032f232293d4083c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455925"
---
# <a name="wm_cap_set_scroll-message"></a>\_Mensagem de \_ rolagem de conjunto de Cap do WM \_

A mensagem de **\_ \_ \_ rolagem definir limite do WM** define a parte do quadro de vídeo a ser exibida na janela de captura. Essa mensagem define o canto superior esquerdo da área do cliente da janela de captura para as coordenadas de um pixel especificado dentro do quadro de vídeo. Você pode enviar essa mensagem explicitamente ou usando a macro [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) .


```C++
WM_CAP_SET_SCROLL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPPOINT) (lpP); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpP"></span><span id="lpp"></span><span id="LPP"></span>*lpP*
</dt> <dd>

Endereço para conter a posição de rolagem desejada.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

A posição de rolagem afeta a imagem nos modos de visualização e de sobreposição.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensagens de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





