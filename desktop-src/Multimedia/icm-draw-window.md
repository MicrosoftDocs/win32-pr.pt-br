---
title: Mensagem de ICM_DRAW_WINDOW (VFW. h)
description: A \_ mensagem de janela ICM Draw \_ Notifica um driver de renderização de que a janela especificada para a mensagem de início de empate do ICM \_ \_ precisa ser redesenhada.
ms.assetid: 4df1b9a7-8d61-4e79-8f43-1e7ee266375c
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_WINDOW
topic_type:
- apiref
api_name:
- ICM_DRAW_WINDOW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 290b123fadcaf46a315c42e3ce9a530c5d5d36c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454988"
---
# <a name="icm_draw_window-message"></a>Mensagem de janela de \_ desenho ICM \_

A mensagem de **\_ \_ janela ICM Draw** notifica um driver de renderização de que a janela especificada para a mensagem de [**início de \_ empate \_ do ICM**](icm-draw-begin.md) precisa ser redesenhada. A janela foi movida ou tornou-se temporariamente obscurecida. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawWindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) .


```C++
ICM_DRAW_WINDOW 
wParam = (DWORD_PTR) (LPVOID) prc; 
lParam = 0; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*popular*
</dt> <dd>

Ponteiro para o retângulo de destino em coordenadas de tela. Se esse parâmetro apontar para um retângulo vazio, o desenho deverá ser desativado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Essa mensagem é suportada por hardware que executa sua própria descompactação assíncrona, tempo e desenho.

Os drivers de sobreposição de vídeo usam essa mensagem para desenhar quando a janela é obscurecida ou movida. Quando uma janela especificada para o [**ICM \_ draw \_ begin**](icm-draw-begin.md) é completamente ocultada por outras janelas, o retângulo de destino está vazio. Os drivers devem desligar o hardware de sobreposição de vídeo quando essa condição ocorrer.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Gerenciador de compactação de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensagens de compactação de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





