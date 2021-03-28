---
title: Operações disponíveis em pools de blocos
description: Esta seção lista as operações que você pode executar em pools de blocos.
ms.assetid: 69CF182B-9161-43B7-89A5-0468E1BBD6B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6c9ec58e6c9197f107f47cd7fe3513f43030c0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162306"
---
# <a name="operations-available-on-tile-pools"></a>Operações disponíveis em pools de blocos

Esta seção lista as operações que você pode executar em pools de blocos.

-   O tempo de vida dos pools de blocos funciona como qualquer outro recurso do Direct3D, apoiado por contagem de referência, incluindo, nesse caso, o acompanhamento de mapeamentos de recursos lado-a-quadro. Quando o app não faz referência a um pool de blocos e todos os mapeamentos de blocos na memória são apagados e os acessos à unidade de processamento gráfico (GPU) são concluídos, o sistema operacional desalocará o pool de blocos.
-   As APIs relacionadas ao compartilhamento de superfície e ao trabalho de sincronização para pools de blocos (mas não diretamente em recursos de ladrilhos). De forma semelhante ao comportamento dos pools de blocos oferecidos, os comandos do Direct3D que acessam recursos com blocos gráficos que apontam para um pool de peças serão descartados se o pool de blocos tiver sido compartilhado e for atualmente adquirido por outro dispositivo e processo.
-   Operação [**ID3D11DeviceContext2:: ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)
-   Operações [**IDXGIDevice2:: OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) e [**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) -essas APIs para produzir memória temporariamente para o sistema operam em todo o pool de peças (e não estão disponíveis para recursos individuais em blocos gráficos). Se um recurso de bloco de enquadrado apontar para uma peça em um pool de blocos oferecido, o recurso de blocos de lado se comporta como se ele fosse oferecido (por exemplo, o tempo de execução descarta comandos que fazem referência a ele).

Os dados não podem ser copiados de e para a memória diretamente do pool de blocos. Os acessos à memória são sempre feitos por meio de recursos de lado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando recursos em ladrilhos](creating-tiled-resources.md)
</dt> </dl>

 

 