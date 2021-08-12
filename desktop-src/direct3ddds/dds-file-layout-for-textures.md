---
title: Exemplo de textura DDS
description: Para uma textura descompactada, use os sinalizadores DDSD PITCH e DDPF RGB; para uma textura compactada, use os sinalizadores \_ \_ DDSD \_ LINEARSIZE e DDPF \_ FOURCC.
ms.assetid: 5bf54e8d-1dc5-4782-96c1-132d258fb560
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47fe1d7da71727c2c84bb3745772a10520367ac1cf6e9c4033932548d86c1302
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118289793"
---
# <a name="dds-texture-example"></a>Exemplo de textura DDS

Para uma textura descompactada, use os sinalizadores DDSD PITCH e DDPF RGB; para uma textura compactada, use os sinalizadores \_ \_ DDSD \_ LINEARSIZE e DDPF \_ FOURCC. Para uma textura mapeada, use os sinalizadores DDSD \_ MIPMAPCOUNT, DDSCAPS MIPMAP e DDSCAPS COMPLEX também, bem como o membro de contagem \_ \_ de mipmap. Se mipmaps são gerados, todos os níveis até 1 por 1 geralmente são gravados.

Para uma textura compactada, o tamanho de cada imagem de nível de mipmap normalmente é um quarto do tamanho do anterior, com um mínimo de 8 (DXT1) ou 16 (DXT2-5) bytes (para texturas quadradas). Use a fórmula a seguir para calcular o tamanho de cada nível para uma textura não quadrada:


```
max(1, ( (width + 3) / 4 ) ) x max(1, ( (height + 3) / 4 ) ) x 8(DXT1) or 16(DXT2-5)
```



Esta tabela lista a quantidade de espaço assumida por cada camada para uma textura 256 por 256 R8G8B8, sem usar compactação.



| Componentes do DDS          | \# Bytes |
|-------------------------|----------|
| header                  | 128      |
| Imagem principal 256 por 256   | 196608   |
| Imagem de mipmap 128 por 128 | 49152    |
| Imagem de mipmap 64 por 64   | 12288    |
| Imagem de mipmap de 32 por 32   | 3072     |
| Imagem de mipmap de 16 por 16   | 768      |
| Imagem de 8 por 8 mipmap     | 192      |
| Imagem de mipmap de 4 por 4     | 48       |
| Imagem de mipmap de 2 por 2     | 12       |
| Imagem de mipmap de 1 por 1     | 3        |



 

Esta tabela lista a quantidade de espaço assumida por cada camada para a mesma textura usando compactação (DXT1).



| Componentes do DDS         | \# Bytes |
|------------------------|----------|
| header                 | 128      |
| Imagem principal 256 por 64   | 8192     |
| Imagem de mipmap 128 por 32 | 2.048     |
| Imagem de mipmap 64 por 16  | 512      |
| Imagem de mipmap de 32 por 8   | 128      |
| Imagem de mipmap de 16 por 4   | 32       |
| Imagem de mipmap de 8 por 2    | 16       |
| Imagem de mipmap de 4 por 1    | 8        |
| Imagem de mipmap de 2 por 1    | 8        |
| Imagem de mipmap de 1 por 1    | 8        |



 

Esta tabela lista a quantidade de espaço assumida por cada camada para a mesma textura usando um formato de compactação DXGI (nesse caso, BC3 UNORM) que, portanto, requer o \_ header estendido:



| Componentes do DDS                                                | \# Bytes |
|---------------------------------------------------------------|----------|
| header (FourCC definido como "DX10")                                 | 128      |
| header estendido (formato DXGI definido como DXGI \_ FORMAT \_ BC3 \_ UNORM) | 20       |
| Imagem principal 256 por 64                                          | 16384    |
| Imagem de mipmap 128 por 32                                        | 4096     |
| Imagem de mipmap 64 por 16                                         | 1024     |
| Imagem de mipmap de 32 por 8                                          | 256      |
| Imagem de mipmap de 16 por 4                                          | 64       |
| Imagem de mipmap de 8 por 2                                           | 32       |
| Imagem de mipmap de 4 por 1                                           | 16       |
| Imagem de mipmap de 2 por 1                                           | 16       |
| Imagem de mipmap de 1 por 1                                           | 16       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para DDS](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




