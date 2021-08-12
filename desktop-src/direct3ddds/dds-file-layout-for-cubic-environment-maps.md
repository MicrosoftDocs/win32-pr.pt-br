---
title: Exemplo de mapa de cubo DDS
description: Para mapas de ambiente cúbica, uma ou mais faces de um cubo são gravados no arquivo, usando formatos descompactados ou compactados e todos os rostos devem ter o mesmo tamanho.
ms.assetid: a77234f6-ba10-40dd-902f-33e600384aa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97a51526570a775eb0cff8ec5ed665ac3dc4b218a876743b29e983bd9c03e9ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118289858"
---
# <a name="dds-cube-map-example"></a>Exemplo de mapa de cubo DDS

Para mapas de ambiente cúbica, uma ou mais faces de um cubo são gravados no arquivo, usando formatos descompactados ou compactados e todos os rostos devem ter o mesmo tamanho. Cada rosto pode ter mipmaps definidos, embora todos os rostos devem ter o mesmo número de níveis de mipmap. Se um arquivo contiver um mapa de cubo, DDSCAPS COMPLEX, DDSCAPS2 CUBEMAP e um ou mais \_ \_ DSCAPS2 \_ CUBEMAP \_ POSITIVEX/Y/Z e/ou DDSCAPS2 \_ CUBEMAP \_ NEGATIVEX/Y/Z deverão ser definidos. As faces são escritas na ordem: x positivo, x negativo, y positivo, y negativo, positivo z, z negativo, com quaisquer rostos ausentes omitidos. Cada face é escrita com sua imagem principal, seguida por quaisquer níveis de mipmap.

Por exemplo, um mapa de cubo 256 por 256 com rostos positivos x, y negativo e positivo z, um formato de pixel DXT1 e todos os níveis de mipmap conteriam o seguinte:



| Componentes do DDS                                      | \# Bytes |
|-----------------------------------------------------|----------|
| header                                              | 128      |
| 256 por 256 positivo x imagem principal                    | 32768    |
| 128 por 128 positivo x imagem mipmap                  | 8192     |
| Imagem de 64 por 64 positivos x mipmap                    | 2.048     |
| Imagem de 32 por 32 positivos x mipmap                    | 512      |
| Imagem de 16 por 16 positivos x mipmap                    | 128      |
| 8 por 8 positivo x imagem mipmap                      | 32       |
| Imagem de 4 por 4 x mipmap positivo                      | 8        |
| 2 por 2 positivo x imagem mipmap                      | 8        |
| 1 por 1 imagem positiva x mipmap                      | 8        |
| repita as 9 camadas anteriores para a imagem y mipmap | 43704    |
| repita as 9 camadas anteriores para a imagem z mipmap | 43704    |



 

A partir do DirectX 8, um mapa de cubo é armazenado com todos os rostos definidos.

## <a name="dxgi-cube-maps"></a>DXGI Cube Mapas

Mapas de ambiente cúbica no Direct3D 10.x e Direct3D 11 são equivalentes a uma matriz de textura 2D com 6 imagens e podem ser armazenados em arquivos DDS como tal. Com o Direct3D 10.1 e o Direct3D 11, o hardware também pode dar suporte a matrizes de cubemaps que são matrizes de textura 2D com várias de 6 imagens (6, 12, 18, 24 etc.).

Por exemplo, aqui está um cubemap 256 por 256 com níveis de mipmap armazenados em um formato BC6H como uma matriz de textura 2D:



| Componentes do DDS                                                                                                                                                                                                  | \# Bytes |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|
| header (FourCC de "DX10")                                                                                                                                                                                       | 128      |
| header estendido (formato DXGI definido como 95 \[ FORMATO DXGI BC6H UF16 , valor da dimensão \_ de \_ \_ \] \[ 3 D3Dxx RESOURCE DIMENSION TEXTURE2D , tamanho da matriz de 6, sinalizadores \_ \_ \_ \] misc de 0x4 \[ D3Dxx \_ RESOURCE \_ MISC \_ TEXTURECUBE \] ) | 20       |
| 256 por 256 entrada de matriz 0 (positivo x) imagem principal                                                                                                                                                                | 65536    |
| 128 por 128 entrada de matriz 0 (x positivo) imagem mipmap                                                                                                                                                              | 16384    |
| 64 por 64 entrada de matriz 0 (positivo x) imagem mipmap                                                                                                                                                                | 4096     |
| 32 por 32 entrada de matriz 0 (positivo x) imagem mipmap                                                                                                                                                                | 1024     |
| 16-by-16 entrada de matriz 0 (positivo x) imagem mipmap                                                                                                                                                                | 256      |
| 8 por 8 entrada de matriz 0 (positivo x) imagem mipmap                                                                                                                                                                  | 64       |
| 4 por 4 entrada de matriz 0 (positivo x) imagem mipmap                                                                                                                                                                  | 16       |
| 2 por 2 entrada de matriz 0 (positivo x) imagem mipmap                                                                                                                                                                  | 16       |
| 1 por 1 entrada de matriz 0 (positivo x) imagem mipmap                                                                                                                                                                  | 16       |
| repita as 9 camadas anteriores para a entrada da matriz 1 (x negativo) imagem mipmap                                                                                                                                        | 87408    |
| repita as 9 camadas anteriores para a entrada de matriz 2 (y positivo) imagem mipmap                                                                                                                                        | 87408    |
| repita as 9 camadas anteriores para a entrada de matriz 3 (y negativo) imagem mipmap                                                                                                                                        | 87408    |
| repita as 9 camadas anteriores para a entrada de matriz 4 (positivo z) imagem mipmap                                                                                                                                        | 87408    |
| repita as 9 camadas anteriores para a entrada da matriz 5 (z negativo) imagem mipmap                                                                                                                                        | 87408    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para DDS](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




