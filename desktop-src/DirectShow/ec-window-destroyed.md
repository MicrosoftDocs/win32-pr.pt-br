---
description: O processador de vídeo foi destruído ou removido do grafo.
ms.assetid: facf35c2-d6a2-4373-bce5-171fd9325116
title: EC_WINDOW_DESTROYED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdd3e641c7fb911a8da10a4c89682fa266e862de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782249"
---
# <a name="ec_window_destroyed"></a>janela do EC \_ \_ destruída

O processador de vídeo foi destruído ou removido do grafo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do processador de vídeo.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

O Gerenciador de gráfico de filtro libera essa janela como o foco, por meio da interface [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) . Ele não envia a notificação de eventos para o aplicativo.

## <a name="remarks"></a>Comentários

O renderizador de vídeo envia esse evento quando deixa o grafo de filtro, em seu método [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) . (O envio do evento quando o filtro é destruído pode ser muito tarde, porque nesse ponto o Gerenciador do grafo de filtro também pode ser destruído.)

Esse evento permite que outros filtros adquiram recursos que dependem do foco da janela, como dispositivos de áudio.

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

 

 




