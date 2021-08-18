---
title: Reautorização de ALE
description: O tráfego de rede nas camadas de ALE (Imposição de Camada de Aplicativo) do WFP (plataforma Windows filtragem) é filtrado por fluxos ALE.
ms.assetid: 3cc7f78e-3f9d-4a91-8ea0-9b64c299068a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 850cd7f789c1fb1222a0d6820e84a42cf41763dac4e57b96667e7feda364374c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582686"
---
# <a name="ale-reauthorization"></a>Reautorização de ALE

O tráfego de rede nas camadas de ALE (Imposição de Camada de Aplicativo) do WFP (plataforma de filtragem de Windows) é filtrado por [fluxos ALE.](ale-stateful-filtering.md) Depois que um fluxo ALE tiver sido permitido, todo o tráfego que faz parte do fluxo ALE será permitido. A autorização é uma solicitação para validar as permissões do fluxo ALE, normalmente devido a uma alteração na política de rede.

Os fluxos ALE são atribuídos a uma direção, entrada ou saída, com base na direção do primeiro pacote que disparou a criação e a autorização do fluxo. Os fluxos ALE de entrada são criados e autorizados na camada [**\_ \_ \_ \_ RECV \_ ACCEPT \_ V{4 \| 6} da CAMADA FWPM ALE AUTH.**](management-filtering-layer-identifiers-.md) Os fluxos ALE de saída são criados e autorizados na camada **FWPM \_ LAYER \_ \_ ALE AUTH \_ CONNECT \_ V{4 \| 6}.** A direção do fluxo ALE não limita a direção dos pacotes que pertencem ao fluxo. Os fluxos ALE contêm pacotes de entrada e saída, independentemente da direção do fluxo ALE em si.

A autorização de um fluxo ALE é disparada por:

-   Uma alteração de política na camada em que o fluxo ALE foi originalmente autorizado ou criado.
-   Uma interface de chegada diferente da interface em que o fluxo ALE foi originalmente autorizado ou criado.
-   Uma conexão pendente.

A autorização é diferenciada da autorização inicial pela presença do sinalizador [**FWP \_ CONDITION \_ IS \_ \_ REAUTHORIZE.**](filtering-condition-flags-.md)

A autorização pode ocorrer somente nas camadas [**FWPM \_ LAYER \_ \_ ALE AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) e **FWPM \_ LAYER \_ \_ ALE AUTH \_ CONNECT \_ \| V{4 6}.**

### <a name="policy-change-reauthorization"></a>Autorização de alteração de política

Uma alteração de política é implementada como uma adição ou remoção de filtro em uma camada ALE. Depois que uma alteração de política for detectada, o primeiro pacote que percorrer um fluxo ALE criado na camada afetada será especificado para autorização novamente para a camada. Portanto, para a reautorização, é totalmente possível que um pacote de saída seja classificado na camada [**\_ \_ \_ \_ RECV \_ ACCEPT \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) de CAMADA ALE DO FWPM E que um pacote de entrada seja classificado na camada **FWPM \_ LAYER \_ \_ ALE AUTH \_ CONNECT \_ V{4 \| 6}.**

Um motivo para essa classificação de direção misturada é que pode não haver mais tráfego de rede da direção original (por exemplo, pacote de entrada para o fluxo ALE de entrada). Um exemplo é o streaming UDP único após um handshake inicial de duas vias. Nesse caso, é mais desejável destruir o streaming assim que possível.

### <a name="arrival-interface-reauthorization"></a>Reautorização da interface de chegada

A reautorização da interface de chegada está disponível a partir do Windows Server 2008 e Windows Vista com Service Pack 1 (SP1).

Pacotes que pertencem ao mesmo fluxo ALE podem chegar de várias interfaces. O primeiro pacote a entrar em uma interface diferente da interface original do fluxo ALE é autorizado.

Em um modelo de host forte, que é o modelo de segurança padrão para a pilha TCP/IP, uma conexão em um interface de rede aceita apenas pacotes que chegam na mesma interface. Portanto, a reautorização da interface de chegada não é usada em um computador host forte.

Em um modelo de host fraco, uma conexão em um interface de rede permite a entrada de pacotes em qualquer outro interface de rede. A reautorização da interface de chegada é usada em um computador host fraco para implementar políticas específicas da interface. Para obter mais informações, [consulte "O tipo de cabo: modelos de host fortes e fracos".](/previous-versions/technet-magazine/cc137807(v=msdn.10))

Alguns [campos classificáveis](filtering-conditions.md) podem ser desconhecidos durante a autorização. Por exemplo, se um pacote de saída estiver sendo reautorizado na camada [**\_ \_ \_ \_ RECV \_ ACCEPT \_ V{4 \| 6},**](management-filtering-layer-identifiers-.md) todos os campos pertencentes à interface de chegada serão desconhecidos. Nesse caso, os valores dos campos desconhecidos são indicados como [**FWP \_ EMPTY.**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)

Campos do tipo [**FWP \_ EMPTY podem**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) ser corresponder a [**FWP \_ MATCH \_ EQUAL**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type). Portanto, uma política pode ser definida para bloquear as reautorizações e destruir um fluxo ALE quando as solicitações de autorização para o fluxo ALE chegam.

## <a name="pending-connection-reauthorization"></a>Autorização de conexão pendente

Um driver de chamada pode adiar uma operação de classificação em camadas ALE e conclua-a posteriormente, quando a decisão de filtragem puder ser tomada com segurança. A funcionalidade ALE de adiamento/conclusão é suportada por meio das funções de modo kernel [FwpsPendOperation0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpspendoperation0) e [FwpsCompleteOperation0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpscompleteoperation0).

A autorização é disparada imediatamente após a chamada FwpsCompleteOperation0 e permite que o driver de texto explicado permita ou bloqueie o fluxo.

Somente uma autorização inicial pode ser adiada. Uma chamada para FwpsPendOperation0 falhará se o sinalizador [**FWP \_ CONDITION FLAG FOR \_ \_ \_ REAUTHORIZE**](filtering-condition-flags-.md) estiver definido.

Para obter mais informações, consulte a [documentação Windows Kit de Driver.](/windows-hardware/drivers/ddi/_netvista/)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Imposição de camada de aplicativo (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Camadas ALE](ale-layers.md)
</dt> <dt>

[Filtragem com estado ALE](ale-stateful-filtering.md)
</dt> <dt>

[Tráfego multicast/difusão ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Personalização de Flow ALE](ale-flow-customization.md)
</dt> </dl>

 

 