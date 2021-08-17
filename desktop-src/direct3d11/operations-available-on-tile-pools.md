---
title: Operações disponíveis em pools de blocos
description: Esta seção lista as operações que você pode executar em pools de partes.
ms.assetid: 69CF182B-9161-43B7-89A5-0468E1BBD6B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5c72e15ebe9a8fd2f6725451268d3d03fb7b181442907248d0db44860560aff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098318"
---
# <a name="operations-available-on-tile-pools"></a>Operações disponíveis em pools de blocos

Esta seção lista as operações que você pode executar em pools de partes.

-   O tempo de vida dos pools de blocos funciona como qualquer outro Recurso direct3D, apoiado pela contagem de referência, incluindo, nesse caso, o acompanhamento de mapeamentos de recursos lado a lado. Quando o app não faz referência a um pool de blocos e todos os mapeamentos de blocos na memória são apagados e os acessos à unidade de processamento gráfico (GPU) são concluídos, o sistema operacional desalocará o pool de blocos.
-   As APIs relacionadas ao compartilhamento de superfície e à sincronização funcionam para pools de blocos (mas não diretamente em recursos lado a lado). Semelhante ao comportamento dos pools de blocos oferecidos, os comandos do Direct3D que acessam recursos lado a lado que apontam para um pool de blocos serão descartados se o pool de blocos tiver sido compartilhado e atualmente adquirido por outro dispositivo e processo.
-   [**Operação ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)
-   [**Operações IDXGIDevice2::OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) e [**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) – essas APIs para gerar memória temporariamente para o sistema operam em todo o pool de blocos (e não estão disponíveis para recursos lado a lado individuais). Se um recurso lado a lado aponta para um bloco em um pool de blocos oferecido, o recurso lado a lado se comporta como se fosse oferecido (por exemplo, o runtime descarta comandos que o referenciam).

Os dados não podem ser copiados de e para a memória diretamente do pool de blocos. Os acessos à memória são sempre feitos por meio de recursos lado a lado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando recursos lado a lado](creating-tiled-resources.md)
</dt> </dl>

 

 