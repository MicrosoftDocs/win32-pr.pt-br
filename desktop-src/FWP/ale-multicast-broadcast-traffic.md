---
title: Tráfego multicast/difusão ALE
description: Todo o tráfego de multicast e difusão de entrada nas camadas de ALE (Imposição de Camada de Aplicativo) é mapeado para um fluxo ALE global.
ms.assetid: b10b9758-8fce-4256-a25d-917e01336456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2849f7277cc9ada580bca22fa5a4fdf618d959d255b442607963047dd2a37bba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315606"
---
# <a name="ale-multicastbroadcast-traffic"></a>Tráfego multicast/difusão ALE

Todo o tráfego de multicast e difusão de entrada nas camadas de ALE (Imposição de Camada de Aplicativo) é mapeado para um fluxo [ALE global.](ale-stateful-filtering.md) O tráfego de resposta para pacotes de difusão e multicast de entrada é classificado na camada [**FWPM \_ LAYER \_ \_ ALE AUTH \_ CONNECT \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) e fluxos ALE separados são criados para cada resposta.

O multicast de saída e o tráfego de difusão nas camadas ALE cria um fluxo ALE de 4 segundos. Por padrão, a autorização de um pacote ALE de difusão ou multicast de saída permitirá o tráfego de entrada, seja unicast, multicast ou difusão, de qualquer endereço remoto por até 4 segundos. Esse fluxo ALE só pode ser atualizado ou mantido vivo pelo tráfego de saída subsequente que corresponde ao fluxo ALE.

> [!Note]  
> O tempo de vida de 4 segundos é especificado pelo texto explicação [**FWPM \_ callout set \_ options \_ \_ AUTH \_ CONNECT LAYER \_ \_ V{4 \| 6}**](built-in-callout-identifiers.md). Para alterar o tempo de vida padrão de 4 segundos, adicione um filtro que faz referência ao texto explicação set **\_ options \_ \_ \_ AUTH \_ CONNECT LAYER \_ \_ V{4 \| 6} do FWPM.** Confira [Personalização Flow ALE](ale-flow-customization.md) para obter mais informações.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Imposição de camada de aplicativo (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Camadas ALE](ale-layers.md)
</dt> <dt>

[Filtragem com estado ALE](ale-stateful-filtering.md)
</dt> <dt>

[Reautorização de ALE](ale-re-authorization.md)
</dt> <dt>

[Personalização de Flow ALE](ale-flow-customization.md)
</dt> </dl>

 

 




