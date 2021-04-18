---
title: Tráfego de difusão/multicast ALE
description: Todo o tráfego de difusão e multicast de entrada nas camadas de aplicação da camada de aplicativo (EPA) é mapeado para um fluxo de ALE global.
ms.assetid: b10b9758-8fce-4256-a25d-917e01336456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30b56a6e2a27a209baf66d34948b704ae321644
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292116"
---
# <a name="ale-multicastbroadcast-traffic"></a>Tráfego de difusão/multicast ALE

Todo o tráfego de difusão e multicast de entrada nas camadas de aplicação da camada de aplicativo (EPA) é mapeado para um [fluxo de Ale](ale-stateful-filtering.md)global. O tráfego de resposta para multicast de entrada e pacotes de difusão é classificado na camada [**FWPM \_ camada de \_ \_ autenticação Ale \_ Connect \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) e os fluxos Ale separados são criados para cada resposta.

O tráfego de difusão e multicast de saída nas camadas ALE cria um fluxo ALE de 4 segundos. Por padrão, a autorização de um pacote de multicast de saída ou de difusão permitirá o tráfego de entrada, seja unicast, multicast ou difusão, de qualquer endereço remoto por até 4 segundos. Tal fluxo ALE só pode ser atualizado ou mantido ativo pelo tráfego de saída subsequente que corresponda ao fluxo da EPA.

> [!Note]  
> O tempo de vida de 4 segundos é especificado pelo texto explicativo [**FWPM de texto \_ explicativo interno \_ definir \_ Opções da camada de \_ \_ conexão autenticação \_ \_ V {4 \| 6}**](built-in-callout-identifiers.md). Para alterar o tempo de vida padrão de 4 segundos, adicione um filtro que referencie o texto explicativo **FWPM \_ \_ definir \_ opções \_ auth \_ Connect \_ Layer \_ V {4 \| 6}** . Consulte [personalização de fluxo Ale](ale-flow-customization.md) para obter mais informações.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicação da camada de aplicativo (EPA)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Camadas ALE](ale-layers.md)
</dt> <dt>

[Filtragem de estado de ALE](ale-stateful-filtering.md)
</dt> <dt>

[Reautorização de ALE](ale-re-authorization.md)
</dt> <dt>

[Personalização de fluxo ALE](ale-flow-customization.md)
</dt> </dl>

 

 




