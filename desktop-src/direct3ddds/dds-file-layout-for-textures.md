---
title: Exemplo de textura DDS
description: Para uma textura não compactada, use os \_ sinalizadores DDSD pitch e DDPF \_ RGB; para uma textura compactada, use os \_ sinalizadores DDSD LINEARSIZE e DDPF \_ FOURCC.
ms.assetid: 5bf54e8d-1dc5-4782-96c1-132d258fb560
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbaa6f86dddc7e60d7f41fc34d7c9fe994d50e4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105788670"
---
# <a name="dds-texture-example"></a>Exemplo de textura DDS

Para uma textura não compactada, use os \_ sinalizadores DDSD pitch e DDPF \_ RGB; para uma textura compactada, use os \_ sinalizadores DDSD LINEARSIZE e DDPF \_ FOURCC. Para uma textura mipmapped, use os \_ sinalizadores DDSD MIPMAPCOUNT, DDSCAPS \_ MIPMAP e DDSCAPS \_ Complex também, bem como o membro de contagem MIPMAP. Se mipmaps forem gerados, todos os níveis de até 1-por-1 serão normalmente gravados.

Para uma textura compactada, o tamanho de cada imagem de nível de mipmap normalmente é um quarto do tamanho do anterior, com um mínimo de 8 (DXT1) ou 16 (DXT2-5) bytes (para texturas quadradas). Use a fórmula a seguir para calcular o tamanho de cada nível de uma textura não quadrada:


```
max(1, ( (width + 3) / 4 ) ) x max(1, ( (height + 3) / 4 ) ) x 8(DXT1) or 16(DXT2-5)
```



Esta tabela lista a quantidade de espaço ocupado por cada camada para uma textura de 256 por 256 R8G8B8, sem usar a compactação.



| Componentes do DDS          | \# Bytes |
|-------------------------|----------|
| header                  | 128      |
| imagem principal de 256 por-256   | 196608   |
| imagem de 128 por 128 mipmap | 49152    |
| imagem de 64 por 64 mipmap   | 12288    |
| imagem de 32 por 32 mipmap   | 3072     |
| imagem de 16 por 16 mipmap   | 768      |
| imagem de 8 por 8 mipmap     | 192      |
| imagem mipmap de 4 por 4     | 48       |
| imagem 2-por-2 mipmap     | 12       |
| imagem 1-por-1 mipmap     | 3        |



 

Esta tabela lista a quantidade de espaço ocupado por cada camada para a mesma textura usando a compactação (DXT1).



| Componentes do DDS         | \# Bytes |
|------------------------|----------|
| header                 | 128      |
| imagem principal de 256 por-64   | 8192     |
| imagem de 128 por 32 mipmap | 2.048     |
| imagem de 64 por 16 mipmap  | 512      |
| imagem de 32 por 8 mipmap   | 128      |
| imagem mipmap de 16 por 4   | 32       |
| imagem de 8 por 2 mipmap    | 16       |
| imagem 4-por-1 mipmap    | 8        |
| imagem 2-por-1 mipmap    | 8        |
| imagem 1-por-1 mipmap    | 8        |



 

Esta tabela lista a quantidade de espaço ocupado por cada camada para a mesma textura usando um formato de compactação DXGI (nesse caso \_ , BC3 UNORM) que, portanto, requer o cabeçalho estendido:



| Componentes do DDS                                                | \# Bytes |
|---------------------------------------------------------------|----------|
| Header (FourCC definido como "DX10")                                 | 128      |
| cabeçalho estendido (formato DXGI definido como \_ formato dxgi \_ BC3 \_ UNORM) | 20       |
| imagem principal de 256 por-64                                          | 16384    |
| imagem de 128 por 32 mipmap                                        | 4096     |
| imagem de 64 por 16 mipmap                                         | 1024     |
| imagem de 32 por 8 mipmap                                          | 256      |
| imagem mipmap de 16 por 4                                          | 64       |
| imagem de 8 por 2 mipmap                                           | 32       |
| imagem 4-por-1 mipmap                                           | 16       |
| imagem 2-por-1 mipmap                                           | 16       |
| imagem 1-por-1 mipmap                                           | 16       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para DDS](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




