---
description: Todos os dados de um fluxo específico foram renderizados.
ms.assetid: 46037d53-085d-4fd0-91a0-408702cbfce5
title: EC_COMPLETE (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a3bb02275862e2cfaea88de5bad0ae545a257efc4d352506d284b83150032f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998196"
---
# <a name="ec_complete"></a>EC \_ COMPLETE

Todos os dados de um fluxo específico foram renderizados.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

(**HRESULT**) Status do fluxo após a conclusão. Se nenhum erro tiver ocorrido durante a reprodução, o valor será S \_ OK.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**IUnknown** \* ) Zero ou um ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do renderdor.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

Por padrão, o gerenciador de grafo de filtro não encaminha esse evento para o aplicativo. No entanto, depois de todos os fluxos no relatório de grafo **EC \_ COMPLETE**, o gerenciador de grafo de filtro posta um evento **EC \_ COMPLETE** separado para o aplicativo.

Se a ação padrão estiver desabilitada para esse evento, o aplicativo receberá todos os eventos **EC \_ COMPLETE** dos renderadores.

## <a name="remarks"></a>Comentários

Um filtro de renderização envia esse evento quando ele recebe um aviso de fim de fluxo. (O fim do fluxo é sinalizado por meio do [**método IPin::EndOfStream.)**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) O filtro envia exatamente um **evento EC \_ COMPLETE** para cada fluxo. O filtro deve processar todas as amostras pendentes antes de enviar o evento. Parar um renderador redefine qualquer estado de fim de fluxo que foi armazenado em cache.

Se o renderador estiver em pausa, ele não **enviará EC \_ COMPLETE** até que o [**método IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) seja chamado. Além disso, ele continua a enviar **eventos EC \_ COMPLETE** para cada transição de pausa para ser executado, até que o filtro seja interrompido ou liberado.

Os filtros *configuram o parâmetro lParam2* como um [**ponteiro IBaseFilter.**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) Se a ação padrão estiver habilitada, o gerenciador de grafo de filtro define esse parâmetro como zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de notificação de eventos](event-notification-codes.md)
</dt> <dt>

[Notificação de eventos DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Renderadores de vídeo alternativos](alternative-video-renderers.md)
</dt> </dl>

 

 




