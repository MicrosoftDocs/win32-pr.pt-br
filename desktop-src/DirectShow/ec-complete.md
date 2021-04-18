---
description: Todos os dados de um fluxo específico foram renderizados.
ms.assetid: 46037d53-085d-4fd0-91a0-408702cbfce5
title: EC_COMPLETE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cd6d548a56173b9c6ea83426ddab3fa8556e312
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789901"
---
# <a name="ec_complete"></a>EC \_ concluído

Todos os dados de um fluxo específico foram renderizados.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Status do fluxo na conclusão. Se não ocorrerem erros durante a reprodução, o valor será S \_ OK.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**IUnknown** \* ) Zero, ou um ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do processador.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

Por padrão, o Gerenciador de gráfico de filtro não encaminha esse evento para o aplicativo. No entanto, depois que todos os fluxos no gráfico de relatório do grafo forem **\_ concluídos**, o Gerenciador de grafo de filtro posta um evento de **\_ conclusão de EC** separado para o aplicativo.

Se a ação padrão estiver desabilitada para esse evento, o aplicativo receberá todos os eventos de **\_ conclusão do EC** dos renderizadores.

## <a name="remarks"></a>Comentários

Um filtro de renderizador envia esse evento quando recebe um aviso de fim de fluxo. (O fim do fluxo é sinalizado por meio do método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .) O filtro envia exatamente um evento **EC \_ Complete** para cada fluxo. O filtro deve processar quaisquer amostras pendentes antes de enviar o evento. Parar um processador redefine qualquer estado de fim do fluxo que foi armazenado em cache.

Se o renderizador estiver em pausa, ele não enviará o **EC \_ Complete** até que o método [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) seja chamado. Além disso, ele continua enviando eventos de **\_ conclusão do EC** para cada transição de pausa para executar, até que o filtro seja interrompido ou liberado.

Os filtros definem o parâmetro *lParam2* para um ponteiro [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) . Se a ação padrão estiver habilitada, o Gerenciador de gráfico de filtro definirá esse parâmetro como zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de notificação de eventos](event-notification-codes.md)
</dt> <dt>

[Notificação de eventos no DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Renderizadores de vídeo alternativos](alternative-video-renderers.md)
</dt> </dl>

 

 




