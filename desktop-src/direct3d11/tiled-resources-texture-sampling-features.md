---
title: Recursos de amostragem de textura de recursos ao lado
description: Esta seção descreve os recursos de amostragem de textura de recursos com ladrilhos.
ms.assetid: E56737CE-C468-4D3C-84EE-E8EB2AB6F505
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd46c96219e54aea6990e91de8e340fdca5e32b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641456"
---
# <a name="tiled-resources-texture-sampling-features"></a>Recursos de amostragem de textura de recursos ao lado

Esta seção descreve os recursos de amostragem de textura de recursos com ladrilhos.

## <a name="requirements-of-tiled-resources-texture-sampling-features"></a>Requisitos de recursos de amostra de textura de características de ladrilho

Os recursos de amostragem de textura descritos aqui exigem o nível da [camada 2](tier-2.md) de suporte a recursos de ladrilhos.

## <a name="shader-feedback-about-mapped-areas"></a>Comentários do sombreador sobre áreas mapeadas

Qualquer instrução de sombreador que lê e/ou grava em um recurso de lado-a-xadrez faz com que as informações de status sejam registradas. Esse status é exposto como um valor de retorno extra opcional em cada instrução de acesso do recurso que entra em um registro temporário de 32 bits. O conteúdo do valor de retorno é opaco. Ou seja, leitura direta pelo programa de sombreador não é permitida. Mas, você pode usar a função [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) para extrair as informações de status.

## <a name="fully-mapped-check"></a>Seleção totalmente mapeada

A função [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) interpreta o status retornado de um acesso de memória e indica se todos os dados que estão sendo acessados foram mapeados no recurso. **CheckAccessFullyMapped** retorna true (0xFFFFFFFF) se os dados foram mapeados ou false (0x00000000) se os dados não foram não mapeados.

Durante as operações de filtragem, às vezes, o peso de um determinado texel acaba sendo 0,0. Um exemplo é uma amostra linear com coordenadas de textura que se enquadram diretamente em um centro de texel: 3 outros texels (os quais podem variar por hardware) contribuem para o filtro, mas com peso 0. Esses texels de peso 0 não contribuem em nada com o resultado do filtro, sendo assim, se eles se encontrarem em blocos **NULL**, eles não serão contados como um acesso não mapeado. Observe que a mesma garantia se aplica aos filtros de textura que incluem diversos níveis de mip; se os texels em um dos mipmaps não for mapeado mas o peso desses texels for 0, esses texels não serão contados como acesso não mapeado.

Quando a amostragem é de um formato que tem menos de 4 componentes (como \_ UNORM de R8 de formato dxgi \_ \_ ), qualquer texels que se enquadrar em blocos **nulos** resultará em um acesso mapeado **nulo** que está sendo relatado independentemente de quais componentes o sombreador realmente examina no resultado. Por exemplo, a leitura de \_ UNORM de R8 e mascaramento do resultado de leitura no sombreador com. GBA/. yzw não pareceria precisar ler a textura. Mas, se o endereço do texel for um bloco mapeado **NULL**, a operação ainda conta como um acesso de mapa **NULL**.

O sombreador pode verificar o status e buscar qualquer curso de ação desejado em caso de falha. Por exemplo, um curso de ação pode ser o registro de "erros" (por exemplo, via gravação UAV) e/ou a emissão de outra leitura fixada a um LOD áspero conhecido por estar mapeado. Um aplicativo pode querer controlar acessos bem-sucedidos também para obter uma noção de qual parte do conjunto de blocos mapeado foi acessado.

Uma complicação para registrar em log é que não existe nenhum mecanismo para relatar o conjunto exato de blocos que teria sido acessado. O aplicativo pode fazer palpites conservadores com base em conhecer as coordenadas usadas para acesso, bem como usar a instrução LOD (por exemplo, [**tex2Dlod**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-tex2dlod)) que retorna o que é o cálculo de LOD de hardware.

Outra complicação é que muitos acessos ocorrerão nos mesmos blocos, portanto, ocorrerão muitos registros em log redundantes e possivelmente uma contenção de memória. Ele pode ser conveniente se o hardware puder ter a opção de não precisar relatar os acessos de bloco se eles tiverem sido relatados em outro lugar antes. Talvez o estado de tal rastreamento pudesse ser redefinido na API (provavelmente nos limites do quadro).

## <a name="per-sample-minlod-clamp"></a>Clamp de MinLOD por amostra

Para ajudar os sombreadores a evitar áreas em recursos de lado mipmapped que são conhecidos como não mapeados, a maioria das instruções de sombreador que envolvem o uso de uma amostra (filtragem) tem um novo modo que permite ao sombreador passar um parâmetro float32 MinLOD fixe adicional para o exemplo de textura. Esse valor encontra-se no espaço numérico do modo de exibição mipmap, em oposição ao recurso subjacente.

O hardware executa o [**Max**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-max)(FShaderMinLODClamp, fComputedLOD) no mesmo local no cálculo de LOD em que ocorre o fixe por recurso MinLOD, que também é um **Max**().

Se o resultado da aplicação do clamp LOD por amostra e quaisquer outros clamps LOD definidos na amostra for de um conjunto vazio, o resultado será o mesmo resultado de acesso sem limites que o clamp minLOD por recurso: 0 para componentes no formato de superfície e padrões para os componentes que estão faltando.

A instrução LOD (por exemplo, [**tex2Dlod**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-tex2dlod)), que é o ponto de minLOD por amostra fixe descrito aqui, retorna clamped e unclamped LOD. O LOD vinculado retornado dessa instrução LOD reflete todas as vinculações, incluindo a vinculação por recurso, mas não uma vinculação por amostra. A vinculação por amostra é controlada e conhecida pelo sombreador de qualquer maneira, portanto, o autor do sombreador pode aplicar manualmente essa vinculação ao valor de retorno da instrução LOD, se desejado.

## <a name="minmax-reduction-filtering"></a>Filtragem de redução mínima/máxima

Os aplicativos podem optar por gerenciar suas próprias estruturas de dados que informam sobre o que os mapeamentos se parecem para um recurso de lado. Um exemplo seria uma superfície que contém um Texel para reter informações para cada bloco em um recurso de lado. Um pode armazenar o primeiro LOD que é mapeado em um determinado local de bloco. Por amostragem cuidadosa dessa estrutura de dados de uma forma semelhante à qual o recurso de azulejos deve ser amostrado, alguém pode descobrir qual será o mínimo de LOD que está totalmente mapeado para uma superfície de filtro de textura inteira. Para ajudar a facilitar esse processo, o Direct3D 11.2 apresenta um novo modo de amostra de finalidade geral, a filtragem min/max

O utilitário de filtragem min/max para o rastreamento LOD pode ser útil para outras finalidades, como, por exemplo, a filtragem de superfícies de profundidade.

A filtragem de redução min/max é um modo em amostras que busca o mesmo conjunto de texels que um filtro de textura normal buscaria. Mas, em vez de mesclar os valores para produzir uma resposta, ele retorna o min() ou max() de texels buscados, em uma base por componente (por exemplo, o mínimo de todos os valores de R, separadamente do mínimo de todos os valores de G e assim por diante).

As operações de min/max seguem regras de precisão aritmética de Direct3D. A ordem das comparações não importa.

Durante as operações de filtragem que não são min/max, às vezes, o peso de um determinado texel acaba sendo 0,0. Um exemplo é um exemplo linear com coordenadas de textura que se enquadram diretamente em um Texel Center-3 texels (que podem variar de acordo com o hardware) contribuem para o filtro, mas com 0 peso. Para qualquer um desses texels que teria peso 0 em um filtro sem a função min/max, se o filtro for min/max, esses texels ainda não contribuem para o resultado (e os pesos não afetam de outra forma a operação de filtro min/max).

A lista completa de modos de filtro é mostrada na enumeração de [**\_ filtro D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_filter) com mínimo e máximo nos valores de enumeração.

O suporte para esse recurso depende do suporte de [camada 2](tier-2.md) para recursos de lado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acesso ao pipeline para recursos lado a lado](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 