---
description: Derivando de CBasePin
ms.assetid: ef453bec-e5a9-4185-94e3-f934e748b11f
title: Derivando de CBasePin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b07eb76fc2913152a69ec729f49826e8b35f1524a3841c5e0d3085ea0634f646
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079256"
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

 

 



