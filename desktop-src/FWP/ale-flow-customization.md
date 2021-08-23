---
title: personalização de Flow ALE
description: a filtragem de rede nas camadas ALE (imposição de camada de aplicativo) da WFP (plataforma de filtragem de Windows) pode ser personalizada com a adição de filtros com opções de classificação específicas.
ms.assetid: 123af237-cf42-410b-8a2f-c011cb5f4f19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbe42a6df32bc69ba454226eb113cb43756224daaf752c3925f1f2d3bacd7650
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951365"
---
# <a name="ale-flow-customization"></a>personalização de Flow ALE

a filtragem de rede nas camadas ALE (imposição de camada de aplicativo) da WFP (plataforma de filtragem de Windows) pode ser personalizada com a adição de filtros com opções de classificação específicas.

## <a name="multicastbroadcast-traffic"></a>Tráfego multicast/difusão

Para bloquear o tráfego de entrada com base em Estados de difusão ou multicast de saída, adicione um filtro que autorize o tráfego de difusão e multicast de saída e que tenha a opção de [**\_ classificação de opção fwp classificar de \_ \_ \_ estado multicast**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) definida como o **valor da \_ opção fwp \_ \_ negar \_ \_ estado multicast**.

## <a name="remote-peers"></a>Pares remotos

Para adicionar pacotes de resposta de pares diferentes ao mesmo fluxo de ALE, adicione um filtro que tenha a opção de classificação do fwp opção de [**\_ \_ \_ \_ \_ mapeamento de fonte flexível**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) definida como o **valor da \_ opção fwp habilitar o \_ \_ \_ \_ \_ mapeamento de origem flexível**.

Consulte [usando opções de classificação](using-classify-options.md) para o exemplo de código.

## <a name="ale-flow-lifetime"></a>tempo de vida de Flow ALE

Para modificar os valores de tempo limite de ociosidade para um fluxo de ALE, adicione um filtro que tenha a opção [**fwp de \_ classificação \_ \_ mcast \_ BCAST \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) e/ou a opção de tempo de **\_ \_ \_ \_ vida unicast da opção fwp classificar** definida para o valor de timeout de ociosidade desejado.

Consulte [usando opções de classificação](using-classify-options.md) para um exemplo de código.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicação da camada de aplicativo (EPA)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Camadas ALE](ale-layers.md)
</dt> <dt>

[Filtragem de estado de ALE](ale-stateful-filtering.md)
</dt> <dt>

[Tráfego de difusão/multicast ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Reautorização de ALE](ale-re-authorization.md)
</dt> <dt>

[Usando opções de classificação](using-classify-options.md)
</dt> </dl>

 

 




