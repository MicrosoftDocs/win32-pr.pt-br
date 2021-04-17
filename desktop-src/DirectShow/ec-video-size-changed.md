---
description: O tamanho do vídeo nativo foi alterado.
ms.assetid: 276f37b3-f981-4a01-bb37-1ee77248668f
title: EC_VIDEO_SIZE_CHANGED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29a70ceab583d8dfc51b417fb701a2988b2e96f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754765"
---
# <a name="ec_video_size_changed"></a>tamanho de vídeo do EC \_ \_ \_ alterado

O tamanho do vídeo nativo foi alterado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**DWORD**) PALAVRA de ordem inferior Especifica a nova largura, em pixels; PALAVRA de ordem superior especifica a nova altura, em pixels.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

Nenhum.

## <a name="remarks"></a>Comentários

Os renderizadores de vídeo poderão enviar esse evento se detectarem uma alteração no tamanho do vídeo nativo.

O [processador de mixagem de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7) e o [processador de mixagem de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9) enviam esse evento em modo de janela, mas não em modo sem janela ou em modo não processado. Para obter mais informações sobre o modo de janela no VMR, consulte [renderização de vídeo](video-rendering.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de notificação de eventos](event-notification-codes.md)
</dt> <dt>

[Notificação de eventos no DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




