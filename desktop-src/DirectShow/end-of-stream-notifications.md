---
description: Notificações de fim de fluxo
ms.assetid: cf2b13bc-5b54-4ac7-8a33-7434126fdf31
title: Notificações de fim de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53fcdfef1225aa5b93b56aeaa0d8ae9d0a8550c9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163849"
---
# <a name="end-of-stream-notifications"></a>Notificações de fim de fluxo

Quando um filtro de origem é feito enviando dados, ele chama o método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) no pino de entrada downstream. O filtro downstream propaga a chamada para o próximo filtro e assim por diante. Quando a chamada **EndOfStream** atinge o renderizador, o processador envia um evento de [**\_ conclusão do EC**](ec-complete.md) para o Gerenciador do grafo de filtro. Se o renderizador tiver vários Pins de entrada, ele entregará o evento de conclusão do EC \_ depois que todo o PIN de entrada tiver recebido a notificação de fim de fluxo.

Um filtro deve serializar chamadas [**EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) com outras chamadas de streaming, como [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive). (Em outras palavras, o filtro downstream sempre deve receber as chamadas na ordem correta.)

Em alguns casos, um filtro downstream pode detectar o final do fluxo antes de o filtro de origem. (Por exemplo, o filtro downstream pode estar analisando o fluxo.) Nesse caso, o filtro downstream pode enviar a notificação de fim de fluxo; nesse caso, ele deve retornar S \_ false de [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) até que o grafo Pare ou libere. O \_ valor de retorno S false informa ao filtro de origem para interromper o envio de dados.

### <a name="default-handling-of-ec_complete"></a>Manuseio padrão do EC \_ concluído

Por padrão, o Gerenciador do grafo de filtro não encaminha todos \_ os eventos de conclusão do EC para o aplicativo. Em vez disso, ele aguarda até que todos os fluxos tenham sido sinalizados \_ por EC e, em seguida, envia um evento de conclusão de um único EC \_ . Assim, o aplicativo recebe o evento após a conclusão de cada fluxo.

Para determinar o número de fluxos, o Gerenciador de gráfico de filtro conta o número de filtros que dão suporte à busca (por meio de [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) ou [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)) e têm um pino de entrada *renderizado* , que é definido como um PIN de entrada sem saídas correspondentes. O Gerenciador de gráfico de filtro determina se um PIN é renderizado de uma das duas maneiras:

-   O método [**IPin:: QueryInternalConnections**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) do PIN retorna zero no parâmetro *nPin* .
-   O filtro expõe a interface [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags) e retorna os \_ sinalizadores diversos de filtro am \_ \_ \_ \_ . sinalizador de renderizador.

### <a name="end-of-stream-notifications-in-pull-mode"></a>Notificações de fim de fluxo no modo de pull

Em uma conexão [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) , o filtro de origem não envia uma notificação de fim de fluxo. Instread, isso é feito pelo filtro downstream, que normalmente é um filtro do analisador. O analisador envia a chamada [**EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) de downstream. Ele não envia um upstream para o filtro de origem.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Entregando o fim do fluxo](delivering-the-end-of-stream.md)
</dt> </dl>

 

 



