---
title: Como a área de um recurso do lado do ladrilho é colocada
description: Quando você cria um recurso de mosaico, as dimensões, o tamanho do elemento de formato e o número de fatias de mipmaps e/ou matrizes (se aplicável) determinam o número de blocos necessários para fazer o fallback da área de superfície inteira.
ms.assetid: 834E317F-CFFD-460C-9F89-793081BA1853
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ae1bf4ad1ca308fb3c93a36c4b3478aabdb0f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988691"
---
# <a name="how-a-tiled-resources-area-is-tiled"></a>Como a área de um recurso do lado do ladrilho é colocada

Quando você cria um recurso de mosaico, as dimensões, o tamanho do elemento de formato e o número de fatias de mipmaps e/ou matrizes (se aplicável) determinam o número de blocos necessários para fazer o fallback da área de superfície inteira. O layout de pixel/bytes dentro de blocos é determinado pela implementação. O número de pixels que se enquadram em um bloco, dependendo do tamanho do elemento de formato, é fixo e idêntico se você usa um padrão com swizzling ou não.

O número de blocos que serão usados por uma largura de elemento de tamanho e formato de superfície fornecida é bem definido e previsível com base nas tabelas das seções a seguir. Para recursos que contêm mipmaps ou casos em que as dimensões da superfície não preenchem um bloco, existem algumas restrições e são discutidas na [embalagem do mipmap](mipmap-packing.md).

Os diferentes recursos de ladrilhos podem apontar para memória idêntica com formatos diferentes, desde que os aplicativos não dependam dos resultados da gravação na memória com um formato e leitura com outro. Mas, em circunstâncias restritas, os aplicativos podem contar com os resultados da gravação na memória com um formato e leitura com outro se os formatos estiverem na mesma família de formato (ou seja, eles têm o mesmo formato pai sem tipo). Por exemplo, o formato DXGI \_ \_ R8G8B8A8 \_ UNORM e o \_ formato dxgi \_ R8G8B8A8 \_ uint são compatíveis entre si, mas não com o \_ formato dxgi \_ R16G16 \_ UNORM. Um aplicativo deve corresponder conservadormente a todas as propriedades de recurso para reinterpretar dados entre duas texturas, pois os padrões de bloco são indefinidos de forma muito conservadora. No entanto, obviamente, o formato é mais vago. Os formatos só precisam ser compatíveis, conforme ilustrado acima. Uma exceção é onde o sangramento de dados de suavização de um formato para outro está bem definido: se um bloco completamente contém 0 para todos os seus bits, esse bloco pode ser usado com qualquer formato que interpreta esses conteúdos de memória como 0 (independentemente do layout de memória). Portanto, um bloco pode ser limpo para 0x00 com o formato DXGI de \_ formato \_ UNORM de R8 \_ e, em seguida, usado com um formato como o \_ formato dxgi \_ R32G32 \_ float e pareceria que o conteúdo ainda é (0,0 f, 0,0 f).

O layout dos dados em um bloco pode ser dependente das propriedades do recurso, do subrecurso no qual ele reside e do local do bloco dentro do subrecurso. As principais exceções são ilustradas acima: formatos compatíveis com outras propriedades de recurso sendo iguais e quando todos os texels são o mesmo padrão.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                             | Descrição                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sub-recursos lado a lado de Texture2D e Texture2DArray](texture2d-and-texture2darray-subresource-tiling.md)<br/> | Essas tabelas mostram como os subrecursos [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) são colocados ao lado. <br/>                                                                                                          |
| [Sub-recursos lado a lado de Texture3D](texture3d-subresource-tiling.md)<br/>                                       | Esta tabela mostra como os [**SubTexture3Ds**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) de subrecursos são enlados. <br/>                                                                                                                                                                            |
| [Buffers colocados lado a lado](buffer-tiling.md)<br/>                                                                     | Um recurso de [buffer](overviews-direct3d-11-resources-buffers.md) é dividido em blocos de 64 KB, com espaço vazio no último bloco, se o tamanho não for um múltiplo de 64 KB.<br/>                                                                                                  |
| [Compactação de mapas MIP](mipmap-packing.md)<br/>                                                                   | Dependendo da [camada](tiled-resources-features-tiers.md) de suporte de recursos ao lado dos blocos, mipmaps com determinadas dimensões não seguem as formas de bloco padrão e são consideradas todas reunidas umas com as outras de uma maneira opaca para o aplicativo. <br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando recursos em ladrilhos](creating-tiled-resources.md)
</dt> </dl>

 

