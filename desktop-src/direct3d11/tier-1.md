---
title: Camada 1
description: Esta seção descreve o suporte de nível 1.
ms.assetid: 8E2907D2-EFCB-4F97-9B40-6835A65D3DE5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4111fa48dafa7f38a26d5ca09f95898eacef6f55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641761"
---
# <a name="tier-1"></a>Camada 1

Esta seção descreve o suporte de nível 1.

-   Hardware em nível de recurso mínimo 11.0.
-   Não há suporte para quilting.
-   Não há suporte para Texture1D ou Texture3D.
-   Não há suporte para suavização multisample (MSAA) para 2, 8 ou 16 amostras. Somente 4x é necessário, exceto nenhum formato de 128 bpp.
-   Nenhum padrão swizzle (o layout em blocos de 64 KB e na compactação MIP final depende do fornecedor de hardware).
-   Limitações de como os blocos podem ser acessados quando há mapeamentos duplicados, descritos em [limitações de acesso de bloco com mapeamentos duplicados](tile-access-limitations-with-duplicate-mappings-.md).

### <a name="limitations-affecting-tier-1-only"></a>Limitações que afetam apenas a camada 1

-   Os recursos em ladrilho podem ter mapeamentos **nulos** , mas lê-los ou gravá-los produz resultados indefinidos, incluindo o dispositivo removido. Os aplicativos podem resolver isso mapeando uma única página fictícia para todas as áreas vazias. Tome cuidado se você gravar e renderizar em uma página mapeada para vários locais de destino de renderização porque a ordem das gravações será indefinida.
-   As instruções do sombreador para fixação de nível de detalhe e feedback de status mapeado não estão disponíveis. Para obter mais informações, consulte [exposição de recursos de lado HLSL](hlsl-tiled-resources-exposure.md).
-   Restrições de alinhamento para formas de bloco padrão: é garantido apenas que MIPS (a partir do melhor) cujas dimensões são todos os múltiplos do tamanho de bloco padrão que dão suporte às formas de bloco padrão e podem ter blocos individuais arbitrariamente mapeados/não mapeados. O primeiro mipmap em um recurso de lado e quadro que tem qualquer dimensão, não um múltiplo de tamanho de bloco padrão, junto com todos os mipmapss mais esparsos, pode ter uma forma de divisão não padrão, ajustando-se em N blocos de 64 KB para esse conjunto de MIPS de uma vez (N relatado ao aplicativo). Esses blocos N são considerados compactados como uma unidade, que deve ser totalmente mapeada ou totalmente desmapeada pelo aplicativo a qualquer momento, embora os mapeamentos de cada um dos blocos N possam ser em locais arbitrariamente separados em um pool de blocos.
-   Os recursos de blocos gráficos com qualquer mipmaps não um múltiplo de tamanho de bloco padrão em todas as dimensões não têm permissão para ter um tamanho de matriz maior do que 1.
-   Para alternar entre os blocos de referência em um pool de blocos por meio de um recurso de [buffer](overviews-direct3d-11-resources-buffers.md) para referenciar os mesmos blocos por meio de um recurso de [textura](overviews-direct3d-11-resources-textures.md) , ou vice-versa, a chamada mais recente para [**UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) ou [**CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) que define os mapeamentos para esses blocos de pool de blocos deve ser para a mesma dimensão de recurso (buffer versus textura \* ) que a dimensão de recurso que será usada para acessar os Caso contrário, o comportamento será indefinido, incluindo a possibilidade de redefinição do dispositivo. Portanto, por exemplo, chamar **UpdateTileMappings** para definir mapeamentos de bloco para um buffer, então **UpdateTileMappings** para os mesmos blocos no pool de blocos por meio de um recurso [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) , então acessar os blocos por meio do buffer é inválido. As operações alternativas são redefinir os mapeamentos de blocos para um recurso ao alternar entre Buffer e Texture (ou vice-versa) compartilhando os blocos ou simplesmente nunca compartilhar blocos de um pool entre recursos Buffer e recursos Texture.
-   Não há suporte para a filtragem de redução mínima/máxima. Para obter informações sobre a filtragem de redução mín./máx., consulte recursos de [amostragem de textura de recursos de lado](tiled-resources-texture-sampling-features.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos de azulejos recursos camadas](tiled-resources-features-tiers.md)
</dt> </dl>

 

 