---
title: Exemplo de mapa de cubos de DDS
description: Para mapas de ambiente cúbico, uma ou mais faces de um cubo são gravadas no arquivo, usando formatos não compactados ou compactados, e todas as faces devem ter o mesmo tamanho.
ms.assetid: a77234f6-ba10-40dd-902f-33e600384aa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235749bc0cf95a2e2120f66f3bcfb8a46e158628
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498734"
---
# <a name="dds-cube-map-example"></a>Exemplo de mapa de cubos de DDS

Para mapas de ambiente cúbico, uma ou mais faces de um cubo são gravadas no arquivo, usando formatos não compactados ou compactados, e todas as faces devem ter o mesmo tamanho. Cada face pode ter mipmaps definido, embora todas as faces devam ter o mesmo número de níveis de mipmap. Se um arquivo contiver um mapa de cubo, DDSCAPS \_ complexo, DDSCAPS2 \_ CUBEMAP e um ou mais de DSCAPS2 \_ CUBEMAP \_ POSITIVEX/y/z e/ou DDSCAPS2 CUBEMAP \_ \_ NEGATIVEX/Y/Z devem ser definidos. As faces são escritas na ordem: x positivo, x negativo, positivo y, negativo y, positivo z, negativo z, com quaisquer rostos ausentes omitidos. Cada face é escrita com sua imagem principal, seguida por qualquer nível de mipmap.

Por exemplo, um mapa de cubo 256-por-256 com rostos x, negativos y e positivo z positivos, um formato de pixel de DXT1 e todos os níveis de mipmap conteriam o seguinte:



| Componentes do DDS                                      | \# Bytes |
|-----------------------------------------------------|----------|
| header                                              | 128      |
| imagem principal x 256-por-256 positivo                    | 32768    |
| imagem de mipmap x positiva de 128 por 128                  | 8192     |
| imagem de mipmap x positiva de 64 por 64                    | 2.048     |
| imagem de mipmap x positiva de 32 por 32                    | 512      |
| imagem x mipmap de 16 por 16 positivos                    | 128      |
| imagem x mipmap de 8 por 8 positivos                      | 32       |
| imagem x mipmap de 4 por 4 positivo                      | 8        |
| imagem 2-por-2 positivo x mipmap                      | 8        |
| imagem 1-por-1 positivo x mipmap                      | 8        |
| Repita as 9 camadas anteriores para a imagem y mipmap | 43704    |
| Repita as 9 camadas anteriores para a imagem z mipmap | 43704    |



 

A partir do DirectX 8, um mapa de cubo é armazenado com todas as faces definidas.

## <a name="dxgi-cube-maps"></a>Mapas de cubo DXGI

Os mapas de ambiente cúbico no Direct3D 10. x e no Direct3D 11 são equivalentes a uma matriz de textura 2D com 6 imagens e podem ser armazenados em arquivos DDS como tal. Com o Direct3D 10,1 e o Direct3D 11, o hardware também pode dar suporte a matrizes de cubemaps que são, por si, matrizes de textura 2D com várias de 6 imagens (6, 12, 18, 24 etc.).

Por exemplo, aqui está um cubemap de 256 por 256 com níveis de mipmap armazenados em um formato BC6H como uma matriz de textura 2D:



| Componentes do DDS                                                                                                                                                                                                  | \# Bytes |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|
| Header (FourCC de "DX10")                                                                                                                                                                                       | 128      |
| cabeçalho estendido (formato DXGI definido como \[ 95 \_ \_ UF16 de formato dxgi BC6H \_ \] , valor de dimensão de 3 \[ D3Dxx de dimensão de \_ recurso \_ \_ TEXTURE2D \] , tamanho da matriz de 6, sinalizadores diversos do D3Dxx de recursos TEXTURECUBE de 0x4 \[ \_ \_ \_ \] ) | 20       |
| 256-por-256 entrada de matriz 0 (x positivo) imagem principal                                                                                                                                                                | 65536    |
| 128-by-128 entrada de matriz 0 (x positivo) imagem mipmap                                                                                                                                                              | 16384    |
| 64-by-64 entrada de matriz 0 (x positivo) imagem mipmap                                                                                                                                                                | 4096     |
| 32-by-32 entrada de matriz 0 (x positivo) imagem mipmap                                                                                                                                                                | 1024     |
| imagem de entrada de matriz de 16 por 16 0 (x positivo) mipmap                                                                                                                                                                | 256      |
| imagem de entrada de matriz de 8 por 8 0 (x positivo) mipmap                                                                                                                                                                  | 64       |
| imagem da entrada de matriz 4 por 4 (x positivo) mipmap                                                                                                                                                                  | 16       |
| imagem 2-por-2 da entrada de matriz 0 (x positivo) mipmap                                                                                                                                                                  | 16       |
| 1-por-1 entrada de matriz 0 (x positivo) imagem mipmap                                                                                                                                                                  | 16       |
| Repita as 9 camadas anteriores para a entrada de matriz 1 (negativo x) mipmap imagem                                                                                                                                        | 87408    |
| repetir as 9 camadas anteriores para a entrada de matriz 2 (y positivo) imagem mipmap                                                                                                                                        | 87408    |
| Repita as 9 camadas anteriores para a entrada de matriz 3 (y negativo) mipmap imagem                                                                                                                                        | 87408    |
| Repita as 9 camadas anteriores para a entrada de matriz 4 (z positivo) imagem mipmap                                                                                                                                        | 87408    |
| Repita as 9 camadas anteriores para a entrada de matriz 5 (z negativo) imagem mipmap                                                                                                                                        | 87408    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para DDS](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




