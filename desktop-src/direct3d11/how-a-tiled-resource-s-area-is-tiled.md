---
title: Como a área de um recurso lado a lado é lado a lado
description: Quando você cria um recurso lado a lado, as dimensões, o tamanho do elemento de formato e o número de mipmaps e/ou fatias de matriz (se aplicável) determinam o número de blocos necessários para fazer o back de toda a área da superfície.
ms.assetid: 834E317F-CFFD-460C-9F89-793081BA1853
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75feaa7852a7bc2567d7b4983ff4d59d12b516f5feb4be2886f93294f77bd6c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633216"
---
# <a name="how-a-tiled-resources-area-is-tiled"></a>Como a área de um recurso lado a lado é lado a lado

Quando você cria um recurso lado a lado, as dimensões, o tamanho do elemento de formato e o número de mipmaps e/ou fatias de matriz (se aplicável) determinam o número de blocos necessários para fazer o back de toda a área da superfície. O layout de pixel/bytes dentro de blocos é determinado pela implementação. O número de pixels que se enquadram em um bloco, dependendo do tamanho do elemento de formato, é fixo e idêntico se você usa um padrão com swizzling ou não.

O número de blocos que serão usados por uma largura de elemento de tamanho e formato de superfície fornecida é bem definido e previsível com base nas tabelas das seções a seguir. Para recursos que contêm mipmaps ou casos em que as dimensões de superfície não preenchem um lado, algumas restrições existem e são discutidas no [empacotamento de Mipmap.](mipmap-packing.md)

Diferentes recursos lado a lado podem apontar para uma memória idêntica com formatos diferentes, desde que os aplicativos não dependam dos resultados da escrita na memória com um formato e leitura com outro. Mas, em circunstâncias restritas, os aplicativos podem contar com os resultados da escrita na memória com um formato e leitura com outro se os formatos estão na mesma família de formato (ou seja, eles têm o mesmo formato pai sem tipo). Por exemplo, DXGI \_ FORMAT \_ R8G8B8A8 UNORM e DXGI FORMAT R8G8B8A8 UINT são compatíveis entre si, mas não com \_ \_ \_ \_ DXGI \_ FORMAT \_ R16G16 \_ UNORM. Um aplicativo deve corresponder a todas as propriedades de recurso para reinterpretar dados entre duas texturas, pois os padrões de peça são muito indefinido de forma muito conservadora. No entanto, obviamente, o formato é mais inativo. Os formatos só precisam ser compatíveis, conforme ilustrado acima. Uma exceção é onde o sangramento de dados de suavização de um formato para outro está bem definido: se um bloco completamente contém 0 para todos os seus bits, esse bloco pode ser usado com qualquer formato que interpreta esses conteúdos de memória como 0 (independentemente do layout de memória). Portanto, um azul poderia ser limpo para 0x00 com o formato DXGI FORMAT R8 UNORM e, em seguida, usado com um formato como DXGI FORMAT R32G32 FLOAT e pareceria que o conteúdo ainda está \_ \_ \_ \_ \_ \_ (0,0f,0,0f).

O layout dos dados dentro de um só lugar pode depender das propriedades do recurso, da sub-fonte na qual eles residem e do local do seu local dentro da sub-fonte. As principais exceções são ilustradas acima: formatos compatíveis com outras propriedades de recurso que são iguais e quando todos os texels são o mesmo padrão.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                             | Descrição                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sub-recursos lado a lado de Texture2D e Texture2DArray](texture2d-and-texture2darray-subresource-tiling.md)<br/> | Essas tabelas mostram como as sub-recursos [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) são lado a lado. <br/>                                                                                                          |
| [Sub-recursos lado a lado de Texture3D](texture3d-subresource-tiling.md)<br/>                                       | Esta tabela mostra como as sub-recursos [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) são lado a lado. <br/>                                                                                                                                                                            |
| [Buffers colocados lado a lado](buffer-tiling.md)<br/>                                                                     | Um [recurso](overviews-direct3d-11-resources-buffers.md) de buffer é dividido em blocos de 64KB, com algum espaço vazio no último bloco se o tamanho não for um múltiplo de 64KB.<br/>                                                                                                  |
| [Compactação de mapas MIP](mipmap-packing.md)<br/>                                                                   | Dependendo da [](tiled-resources-features-tiers.md) camada de suporte a recursos lado a lado, os mipmaps com determinadas dimensões não seguem as formas de bloco padrão e são considerados todos empacotados entre si de maneira opaca para o aplicativo. <br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando recursos lado a lado](creating-tiled-resources.md)
</dt> </dl>

 

