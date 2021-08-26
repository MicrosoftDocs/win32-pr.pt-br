---
title: Recursos de amostragem de textura de recursos lado a lado
description: Esta seção descreve os recursos de amostragem de textura de recursos lado a lado.
ms.assetid: E56737CE-C468-4D3C-84EE-E8EB2AB6F505
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1356b274b5e101a730e3de92a6cdf98b1f293515228fb420a77642f4603757c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119472"
---
# <a name="tiled-resources-texture-sampling-features"></a>Recursos de amostragem de textura de recursos lado a lado

Esta seção descreve os recursos de amostragem de textura de recursos lado a lado.

## <a name="requirements-of-tiled-resources-texture-sampling-features"></a>Requisitos de recursos lado a lado dos recursos de amostragem de textura

Os recursos de amostragem de textura descritos aqui exigem suporte ao nível da Camada [2](tier-2.md) de recursos lado a lado.

## <a name="shader-feedback-about-mapped-areas"></a>Comentários do sombreador sobre áreas mapeadas

Qualquer instrução de sombreador que lê e/ou grava em um recurso lado a lado faz com que as informações de status sejam registradas. Esse status é exposto como um valor de retorno extra opcional em cada instrução de acesso do recurso que entra em um registro temporário de 32 bits. O conteúdo do valor de retorno é opaco. Ou seja, leitura direta pelo programa de sombreador não é permitida. Mas, você pode usar a função [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) para extrair as informações de status.

## <a name="fully-mapped-check"></a>Seleção totalmente mapeada

A função [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) interpreta o status retornado de um acesso de memória e indica se todos os dados que estão sendo acessados foram mapeados no recurso. **CheckAccessFullyMapped** retorna true (0xFFFFFFFF) se os dados foram mapeados ou false (0x00000000) se os dados não foram não mapeados.

Durante as operações de filtragem, às vezes, o peso de um determinado texel acaba sendo 0,0. Um exemplo é uma amostra linear com coordenadas de textura que se enquadram diretamente em um centro de texel: 3 outros texels (os quais podem variar por hardware) contribuem para o filtro, mas com peso 0. Esses texels de peso 0 não contribuem em nada com o resultado do filtro, sendo assim, se eles se encontrarem em blocos **NULL**, eles não serão contados como um acesso não mapeado. Observe que a mesma garantia se aplica aos filtros de textura que incluem diversos níveis de mip; se os texels em um dos mipmaps não for mapeado mas o peso desses texels for 0, esses texels não serão contados como acesso não mapeado.

Ao fazer a amostragem de um formato que tem menos de 4 componentes (como DXGI \_ FORMAT \_ R8 \_ UNORM), quaisquer texels   que se enquadram em blocos NULL resultam em um acesso mapeado NULL sendo relatado, independentemente de quais componentes o sombreador realmente analisa no resultado. Por exemplo, ler de R8 UNORM e mascarar o resultado de leitura no sombreador com .gba/.yzw não pareceria precisar ler a \_ textura. Mas, se o endereço do texel for um bloco mapeado **NULL**, a operação ainda conta como um acesso de mapa **NULL**.

O sombreador pode verificar o status e buscar qualquer curso de ação desejado em caso de falha. Por exemplo, um curso de ação pode ser o registro de "erros" (por exemplo, via gravação UAV) e/ou a emissão de outra leitura fixada a um LOD áspero conhecido por estar mapeado. Um aplicativo pode querer controlar acessos bem-sucedidos também para obter uma noção de qual parte do conjunto de blocos mapeado foi acessado.

Uma complicação para registrar em log é que não existe nenhum mecanismo para relatar o conjunto exato de blocos que teria sido acessado. O aplicativo pode fazer suposições conservadoras com base em conhecer as coordenadas usadas para acesso, bem como usar a instrução LOD (por exemplo, [**tex2Dlod**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-tex2dlod)), que retorna qual é o cálculo de LOD de hardware.

Outra complicação é que muitos acessos ocorrerão nos mesmos blocos, portanto, ocorrerão muitos registros em log redundantes e possivelmente uma contenção de memória. Ele pode ser conveniente se o hardware puder ter a opção de não precisar relatar os acessos de bloco se eles tiverem sido relatados em outro lugar antes. Talvez o estado de tal rastreamento pudesse ser redefinido na API (provavelmente nos limites do quadro).

## <a name="per-sample-minlod-clamp"></a>Clamp de MinLOD por amostra

Para ajudar os sombreadores a evitar áreas em recursos lado a lado mapeados que são conhecidos como não mapeados, a maioria das instruções de sombreador que envolvem o uso de um exemplo (filtragem) tem um novo modo que permite que o sombreador passe um parâmetro de fixação adicional float32 MinLOD para a amostra de textura. Esse valor encontra-se no espaço numérico do modo de exibição mipmap, em oposição ao recurso subjacente.

O hardware executa [**max**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-max)(fShaderMinLODClamp,fComputedLOD) no mesmo local no cálculo lod em que ocorre o fixador MinLOD por recurso, que também é **um máximo**().

Se o resultado da aplicação do clamp LOD por amostra e quaisquer outros clamps LOD definidos na amostra for de um conjunto vazio, o resultado será o mesmo resultado de acesso sem limites que o clamp minLOD por recurso: 0 para componentes no formato de superfície e padrões para os componentes que estão faltando.

A instrução LOD (por exemplo, [**tex2Dlod**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-tex2dlod)), que antecede o fixador minLOD por exemplo descrito aqui, retorna um LOD fixado e sem lacre. O LOD vinculado retornado dessa instrução LOD reflete todas as vinculações, incluindo a vinculação por recurso, mas não uma vinculação por amostra. A vinculação por amostra é controlada e conhecida pelo sombreador de qualquer maneira, portanto, o autor do sombreador pode aplicar manualmente essa vinculação ao valor de retorno da instrução LOD, se desejado.

## <a name="minmax-reduction-filtering"></a>Filtragem de redução mínima/máxima

Os aplicativos podem optar por gerenciar suas próprias estruturas de dados que os informam sobre a aparência dos mapeamentos para um recurso lado a lado. Um exemplo seria uma superfície que contém um texel para manter informações para cada bloco em um recurso lado a lado. Um pode armazenar o primeiro LOD que é mapeado em um determinado local de bloco. Pela amostragem cuidadosa dessa estrutura de dados de maneira semelhante à qual o recurso lado a lado deve ser amostrado, pode-se descobrir qual será o LOD mínimo totalmente mapeado para uma superfície inteira do filtro de textura. Para ajudar a facilitar esse processo, o Direct3D 11.2 apresenta um novo modo de amostra de finalidade geral, a filtragem min/max

O utilitário de filtragem min/max para o rastreamento LOD pode ser útil para outras finalidades, como, por exemplo, a filtragem de superfícies de profundidade.

A filtragem de redução min/max é um modo em amostras que busca o mesmo conjunto de texels que um filtro de textura normal buscaria. Mas, em vez de mesclar os valores para produzir uma resposta, ele retorna o min() ou max() de texels buscados, em uma base por componente (por exemplo, o mínimo de todos os valores de R, separadamente do mínimo de todos os valores de G e assim por diante).

As operações de min/max seguem regras de precisão aritmética de Direct3D. A ordem das comparações não importa.

Durante as operações de filtragem que não são min/max, às vezes, o peso de um determinado texel acaba sendo 0,0. Um exemplo é um exemplo linear com coordenadas de textura que se enquadram diretamente em um centro de texel – três outros texels (que podem variar por hardware) contribuem para o filtro, mas com 0 peso. Para qualquer um desses texels que teria peso 0 em um filtro sem a função min/max, se o filtro for min/max, esses texels ainda não contribuem para o resultado (e os pesos não afetam de outra forma a operação de filtro min/max).

A lista completa de modos de filtro é mostrada na enumeração [**D3D11 \_ FILTER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_filter) com MINIMUM e MAXIMUM nos valores de enumeração.

O suporte para esse recurso depende do [suporte da Camada 2](tier-2.md) para recursos lado a lado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acesso de pipeline a recursos lado a lado](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 