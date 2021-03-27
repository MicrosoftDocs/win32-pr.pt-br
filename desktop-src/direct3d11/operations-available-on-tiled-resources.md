---
title: Operações disponíveis em recursos ao lado
description: Esta seção lista as operações que você pode executar em recursos de lado.
ms.assetid: 1CF42A18-B6EA-4BA9-BEDE-9A8CC083CBAF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45d051943816502fd0bafb77e67241026f31498
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005942"
---
# <a name="operations-available-on-tiled-resources"></a>Operações disponíveis em recursos ao lado

Esta seção lista as operações que você pode executar em recursos de lado.

-   void [**ID3D11DeviceContext2:: UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) e [**ID3D11DeviceContext2:: CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) Operations – esses locais de blocos de ponto de operações em um recurso de lado do bloco para locais em pools de blocos, ou para NULL, ou para ambos. Essas operações podem atualizar um subconjunto separado dos ponteiros de blocos.
-   \*Operações Copy () e update \* () – todas as APIs que podem copiar dados de e para uma superfície de pool padrão (por exemplo, [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) e [**ID3D11DeviceContext1:: UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)) funcionam para recursos de lado. Leitura de blocos não mapeados produz 0 e as gravações em blocos não mapeados são ignoradas.
-   Operações [**ID3D11DeviceContext2:: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) e [**ID3D11DeviceContext2:: UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles) – essas operações existem para copiar os blocos em uma granularidade de 64 KB de e para qualquer recurso de bloco e um recurso de buffer em um layout de memória canônica. O driver de vídeo e o hardware executam qualquer "swizzling" de memória necessária para o recurso de lado.
-   As associações de pipeline do Direct3D e as criações/associações de modo de exibição que funcionariam em recursos que não são de lado do ladrilho também funcionam em recursos de lado.

Os controles de blocos estão disponíveis em contextos de imediatos ou adiados (assim como atualizações de recursos típicos), e durante a execução afetam os acessos subsequentes aos blocos de (operações não enviadas anteriormente).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando recursos em ladrilhos](creating-tiled-resources.md)
</dt> </dl>

 

 




