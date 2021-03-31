---
title: Reautorização de ALE
description: O tráfego de rede nas camadas ALE (imposição da camada de aplicativo) da WFP (Windows Filtering Platform) é filtrado por fluxos ALE.
ms.assetid: 3cc7f78e-3f9d-4a91-8ea0-9b64c299068a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed05c4c0767d449ec128250f852c365455bd0dc7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103641027"
---
# <a name="ale-reauthorization"></a>Reautorização de ALE

O tráfego de rede nas camadas ALE (imposição da camada de aplicativo) da WFP (Windows Filtering Platform) é filtrado por [fluxos Ale](ale-stateful-filtering.md). Depois que um fluxo ALE tiver sido permitido, todo o tráfego que fizer parte do fluxo ALE será permitido. A reautorização é uma solicitação para validar as permissões do fluxo ALE, normalmente devido a uma alteração na diretiva de rede.

Os fluxos ALE recebem uma direção, entrada ou saída, com base na direção do primeiro pacote que disparou a criação e a autorização do fluxo. Os fluxos ALE de entrada são criados e autorizados na camada [**FWPM de \_ autenticação Ale de camada de saída \_ \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) . Os fluxos de ALE de saída são criados e autorizados na camada **FWPM \_ camada de \_ \_ autenticação Ale \_ Connect \_ V {4 \| 6}** . A direção do fluxo ALE não limita a direção dos pacotes que pertencem ao fluxo. Os fluxos ALE contêm pacotes de entrada e de saída, independentemente da direção do fluxo da EPA em si.

A Reautorização de um fluxo ALE é disparada por:

-   Uma alteração de política na camada em que o fluxo de ALE foi originalmente autorizado ou criado.
-   Uma interface de chegada diferente da interface na qual o fluxo ALE foi originalmente autorizado ou criado.
-   Uma conexão pendente.

A reautorização é diferenciada da autorização inicial pela presença do sinalizador de [**condição fwp ser um sinalizador de \_ \_ \_ \_ reautorização**](filtering-condition-flags-.md) .

A reautorização só pode ocorrer nas camadas [**FWPM da \_ camada de \_ autenticação Ale de \_ \_ recepção \_ \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) e **FWPM \_ Layer \_ Ale \_ \_ Connect \_ v {4 \| 6}** .

### <a name="policy-change-reauthorization"></a>Política – alterar a autorização

Uma alteração de política é implementada como uma adição ou remoção de filtro em uma camada ALE. Depois que uma alteração de política for detectada, o primeiro pacote que atravessa um fluxo ALE criado na camada afetada será especificado para a reautorização para a camada. Portanto, para a reautorização, é totalmente possível que um pacote de saída seja classificado na camada [**FWPM de \_ \_ \_ autenticação Ale auth \_ \_ \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) e que um pacote de entrada seja classificado na camada **\_ \_ \_ \_ \_ v {4 \| 6} de autenticação Ale da camada FWPM** .

Um motivo para essa classificação de direção mista é que pode não haver mais tráfego de rede da direção original (por exemplo, pacote de entrada para o fluxo de entrada ALE). Um exemplo é o streaming UDP unidirecional após um handshake bidirecional inicial. Nesse caso, é mais desejável subdividir o streaming o mais rápido possível.

### <a name="arrival-interface-reauthorization"></a>Reautorização da interface de chegada

A Reautorização da interface de chegada está disponível a partir do Windows Server 2008 e do Windows Vista com Service Pack 1 (SP1).

Os pacotes que pertencem ao mesmo fluxo de ALE podem chegar de várias interfaces. O primeiro pacote a ser fornecido em uma interface diferente da interface original do fluxo ALE é reautorizado.

Em um modelo de host forte, que é o modelo de segurança padrão para a pilha TCP/IP, uma conexão em um adaptador de rede aceita apenas os pacotes que vêm na mesma interface. Portanto, a Reautorização de interface de chegada não é usada em um computador host forte.

Em um modelo de host fraco, uma conexão em um adaptador de rede permite que os pacotes sejam recebidos em qualquer outra interface de rede. A Reautorização de interface de chegada é usada em um computador host fraco para implementar políticas específicas de interface. Para obter mais informações, consulte ["The Cable Guy: modelos de host fortes e fracos".](/previous-versions/technet-magazine/cc137807(v=msdn.10))

Alguns [campos classificáveis](filtering-conditions.md) podem ser desconhecidos durante a reautorização. Por exemplo, se um pacote de saída estiver sendo reautorizado na camada de FWPM de autenticação Ale de camada de entrada de [**\_ \_ \_ \_ recepção \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) , todos os campos pertencentes à interface de chegada serão desconhecidos. Nesse caso, os valores dos campos desconhecidos são indicados como [**fwp \_ vazio**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).

Os campos do tipo [**fwp \_ vazio**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) podem ser correspondidos com [**fwp \_ Match \_ igual**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type). Portanto, uma política pode ser definida para bloquear as reautorizações e subdividir um fluxo ALE quando as solicitações de Reautorização para a chegada do fluxo ALE.

## <a name="pending-connection-reauthorization"></a>Reautorização de conexão pendente

Um driver de texto explicativo pode adiar uma operação de classificação em camadas ALE e concluí-la posteriormente, quando a decisão de filtragem puder ser feita com segurança. A funcionalidade de adiamento/conclusão da ALE tem suporte por meio das funções de modo kernel [FwpsPendOperation0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpspendoperation0) e [FwpsCompleteOperation0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpscompleteoperation0).

A reautorização é disparada imediatamente após a chamada FwpsCompleteOperation0 e permite que o driver de texto explicativo permita ou bloqueie o fluxo.

Somente uma autorização inicial pode ser adiada. Uma chamada para FwpsPendOperation0 falhará se o sinalizador de [**\_ condição fwp for de \_ \_ \_ reautoria**](filtering-condition-flags-.md) definido.

Para obter mais informações, consulte a documentação do [Windows Driver Kit](/windows-hardware/drivers/ddi/_netvista/) .

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

[Personalização de fluxo ALE](ale-flow-customization.md)
</dt> </dl>

 

 