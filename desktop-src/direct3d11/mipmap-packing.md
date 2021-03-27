---
title: Compactação de mapas MIP
description: Dependendo da camada de suporte de recursos ao lado dos blocos, mipmaps com determinadas dimensões não seguem as formas de bloco padrão e são consideradas todas reunidas umas com as outras de uma maneira opaca para o aplicativo.
ms.assetid: 3B416324-7656-495F-9BA9-8F5BE475ABC1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db4cd6f70129f46495673dfc82b5d261210ab21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005228"
---
# <a name="mipmap-packing"></a>Compactação de mapas MIP

Dependendo da [camada](tiled-resources-features-tiers.md) de suporte de recursos ao lado dos blocos, mipmaps com determinadas dimensões não seguem as formas de bloco padrão e são consideradas todas reunidas umas com as outras de uma maneira opaca para o aplicativo. Níveis mais altos de suporte têm garantia mais ampla sobre quais tipos de dimensões de superfície se encaixam nas formas de bloco padrão (e, portanto, podem ser mapeados individualmente por apps).

O que pode variar entre as implementações é que, considerando as dimensões, o formato, o número de mipmaps e as fatias de matrizes de um recurso de lado, um número M de MIPS (por fatia de matriz) pode ser empacotado em um número N de blocos. A API [**ID3D11Device2:: GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) existe para permitir que o driver relate ao aplicativo quais são os M e N (entre outros detalhes sobre a superfície que essa API relata que são padrão e não variam de acordo com o fornecedor de hardware). O conjunto de blocos para mips compactados ainda tem 64 KB e pode ser mapeado individualmente em locais diferentes no pool de blocos. No entanto, a forma de pixel dos blocos e como os mipmaps se encaixam no conjunto de blocos é específico de um fornecedor de hardware e muito complexo para expor. Assim, os apps devem mapear todos os blocos designados como compactados ou nenhum deles simultaneamente. Caso contrário, o comportamento para acessar o recurso do lado do xadrez é indefinido.

Para superfícies dispostas, o conjunto de mips compactado e a quantidade de blocos compactados que armazenam esses mips (M e N descrito acima) se aplica individualmente a cada fatia de matriz.

APIs dedicadas para copiar blocos ([**ID3D11DeviceContext2:: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) e [**ID3D11DeviceContext2:: UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)) não podem acessar MIPS empacotadas. Os aplicativos que desejam copiar dados de e para os MIPS empacotados podem fazer isso usando todas as APIs específicas de recursos sem lado do ladrilho para cópia e renderização em superfícies.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como a área de um recurso do lado do ladrilho é colocada](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 




