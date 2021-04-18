---
description: Derivando de CBasePin
ms.assetid: ef453bec-e5a9-4185-94e3-f934e748b11f
title: Derivando de CBasePin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82ab56da3ae326be175c9519b5248e53fa02b82f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105778437"
---
# <a name="deriving-from-cbasepin"></a>Derivando de CBasePin

Para implementar um PIN usando [**CBasePin**](cbasepin.md), você deve derivar uma nova classe da classe base e substituir vários de seus métodos. Você deve substituir os seguintes métodos:

-   [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md)
-   [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md)

Provavelmente, você precisará substituir estes métodos adicionais:

-   [**CBasePin:: ativo**](cbasepin-active.md)
-   [**CBasePin::BreakConnect**](cbasepin-breakconnect.md)
-   [**CBasePin::CheckConnect**](cbasepin-checkconnect.md)
-   [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md)
-   [**CBasePin::EndOfStream**](cbasepin-endofstream.md)
-   [**CBasePin:: inativo**](cbasepin-inactive.md)
-   [**CBasePin:: Notify**](cbasepin-notify.md)
-   [**CBasePin:: Run**](cbasepin-run.md)

Por fim, você deve implementar os métodos [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) e [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .

Alguns desses métodos são implementados em classes base que derivam de **CBasePin**, como [**CBaseInputPin**](cbaseinputpin.md) e [**CBaseOutputPin**](cbaseoutputpin.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CBasePin**](cbasepin.md)
</dt> </dl>

 

 



