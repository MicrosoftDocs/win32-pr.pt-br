---
title: Exemplo de textura de volume DDS
description: Para uma textura de volume, use o \_ volume complexo DDSCAPS, DDSCAPS2 \_ , DDSD \_ , flags e set e dwDepth. Uma textura de volume é uma extensão de uma textura padrão para o Direct3D 9; uma textura de volume pode ser definida com ou sem mipmaps.
ms.assetid: c1675a6d-129a-4e95-993f-e1be905781cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03d82faa8041f2b5c99ef57ee2386ff5de84d787
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105812306"
---
# <a name="dds-volume-texture-example"></a>Exemplo de textura de volume DDS

Para uma textura de volume, use o \_ volume complexo DDSCAPS, DDSCAPS2 \_ , DDSD \_ , flags e set e dwDepth. Uma textura de volume é uma extensão de uma textura padrão para o Direct3D 9; uma textura de volume pode ser definida com ou sem mipmaps.

Para volumes sem mipmaps, cada fatia de profundidade é gravada no arquivo em ordem. Se mipmaps forem incluídas, todas as fatias de profundidade para um determinado nível de mipmap serão escritas em conjunto, com cada nível contendo metade de fatias do nível anterior, com um mínimo de 1.

Por exemplo, um mapa de volume 64-por-64-by-4 usando um formato de pixel de R8G8B8 (3 bytes por pixel) com todos os níveis de mipmap teria o seguinte:



| Componentes do DDS                      | \# Bytes    |
|-------------------------------------|-------------|
| header                              | 128 bytes   |
| 64-por-64 fatia 1 de 4 imagem principal.   | 12288 bytes |
| 64-por-64 fatia 2 de 4 imagem principal.   | 12288 bytes |
| 64-por-64 fatia 3 de 4 imagem principal.   | 12288 bytes |
| 64-por-64 fatia 4 de 4 imagem principal.   | 12288 bytes |
| 32-por-32 fatia 1 de 2 mipmap imagem. | 3072 bytes  |
| 32-por-32 fatia 2 de 2 mipmap Image. | 3072 bytes  |
| 16-por-16 fatia 1 de 1 imagem mipmap. | 768 bytes   |
| 8-por-8 fatia 1 de 1 imagem de mipmap.   | 192 bytes   |
| 4-by-4 fatia 1 de 1 imagem mipmap.   | 48 bytes    |
| 2-por-2 fatia 1 de 1 imagem mipmap.   | 12 bytes    |
| 1-por-1 fatia 1 de 1 imagem mipmap.   | 3 bytes     |



 

Observe que o menor nível de mipmap é de apenas 3 bytes porque o BitCount é 24 e não há nenhuma compactação adicional nesse nível.

O suporte para texturas de volume foi adicionado no DirectX 8.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para DDS](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




