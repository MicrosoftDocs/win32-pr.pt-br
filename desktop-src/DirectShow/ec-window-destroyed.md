---
description: O renderador de vídeo foi destruído ou removido do grafo.
ms.assetid: facf35c2-d6a2-4373-bce5-171fd9325116
title: EC_WINDOW_DESTROYED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d7b26224fee4e18d92d16d8f3bfe277c70cf2b260a19c9c7d6438477266c3e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686026"
---
# <a name="ec_window_destroyed"></a>JANELA \_ EC \_ DESTRUÍDA

O renderador de vídeo foi destruído ou removido do grafo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

(**IUnknown** \* ) Ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do renderador de vídeo.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

O gerenciador de grafo de filtro libera essa janela como o foco, por meio da interface [**IResourceManager.**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) Ele não envia a notificação de evento para o aplicativo.

## <a name="remarks"></a>Comentários

O renderador de vídeo envia esse evento quando sai do grafo de filtro, em [**seu método IBaseFilter::JoinFilterGraph.**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) (Enviar o evento quando o filtro é destruído pode ser muito tarde, porque nesse ponto o gerenciador de grafo de filtro também pode ser destruído.)

Esse evento permite que outros filtros adquira recursos que dependem do foco da janela, como dispositivos de áudio.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de notificação de eventos](event-notification-codes.md)
</dt> <dt>

[Notificação de eventos DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




