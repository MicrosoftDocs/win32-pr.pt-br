---
title: Usando os dados de recurso do Direct3D 11 para complementar os níveis de recursos do Direct3D
description: Descubra como verificar o suporte ao dispositivo para recursos opcionais, incluindo recursos que foram adicionados em versões recentes do Windows.
ms.assetid: 91D9706A-47C5-4220-8AC7-167095E74F74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dcc770812281ea89e8ebb68065aa68a00e1887d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294212"
---
# <a name="using-direct3d-11-feature-data-to-supplement-direct3d-feature-levels"></a>Usando os dados de recurso do Direct3D 11 para complementar os níveis de recursos do Direct3D

Descubra como verificar o suporte ao dispositivo para recursos opcionais, incluindo recursos que foram adicionados em versões recentes do Windows.

[Os níveis de recurso do Direct3D](overviews-direct3d-11-devices-downlevel-intro.md) indicam conjuntos bem definidos de funcionalidade de GPU que correspondem aproximadamente a diferentes gerações de hardware de gráficos. Isso simplifica muito a tarefa de verificar capaibilities de hardware e também fornece uma experiência consistente em uma ampla gama de dispositivos diferentes.

Para considerar algumas das variações entre diferentes implementações de hardware, incluindo hardware herdado, hardware móvel e hardware moderno, alguns recursos são considerados opcionais. O suporte para esses recursos pode ser determinado chamando [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) e fornecendo a estrutura de dados de recurso D3D11 relevante \_ \_ \_ \* . Este tópico descreve os vários recursos opcionais do Direct3D 11, como alguns deles funcionam em conjunto e como você pode evitar a verificação de cada recurso opcional.

## <a name="how-to-check-for-optional-feature-support"></a>Como verificar o suporte a recursos opcionais

Chame [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport), fornecendo a estrutura que representa o recurso opcional que você gostaria de usar. Se o método retornar **S \_ OK**, isso significa que você está em uma versão do tempo de execução do Direct3D que dá suporte ao recurso opcional. Se ele retornar **e \_ INVALIDARG**, isso significa que você está em uma versão do tempo de execução do Direct3D 11 de antes que o recurso opcional tenha sido adicionado-isso significa que o recurso opcional não está disponível, juntamente com quaisquer outros recursos opcionais introduzidos na mesma versão do Direct3D 11 ou posterior.

## <a name="can-i-minimize-the-work-required-for-feature-support-checks"></a>Posso minimizar o trabalho necessário para verificações de suporte a recursos?

Além de ter o tempo de execução do Direct3D 11 correto (geralmente associado a uma versão do Windows), o driver de gráficos também deve ser recente o suficiente para oferecer suporte ao recurso opcional. As especificações do WDDM exigem que recursos opcionais sejam suportados se o hardware puder dar suporte a ele. Assim, quando um driver de gráficos dá suporte a um dos recursos opcionais que foram adicionados em uma versão específica do Windows, isso geralmente significa que o driver de gráficos dá suporte aos outros recursos adicionados nessa versão do Windows. Por exemplo, se um driver de dispositivo der suporte a sombras no nível de recurso 9, você saberá que o driver de dispositivo é pelo menos o WDDM 1,2.

**Observação**    Se um dispositivo Microsoft Direct3D oferecer suporte ao [nível de recurso](overviews-direct3d-11-devices-downlevel-intro.md) 11,1, todos os recursos opcionais indicados pelas opções de [**\_ D3D11 de dados de recurso \_ \_ \_ D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) serão automaticamente suportados, exceto **SAD4ShaderInstructions** e **ExtendedDoublesShaderInstructions**.

O tempo de execução sempre define os seguintes agrupamentos de membros de forma idêntica. Ou seja, todos os valores em um agrupamento são **verdadeiros** ou **falsos** juntos:

-   **DiscardAPIsSeenByDriver** e **FlagsForUpdateAndCopySeenByDriver**
-   **Clearview**, **CopyWithOverlap**, **ConstantBufferPartialUpdate**, **ConstantBufferOffsetting** e **MapNoOverwriteOnDynamicConstantBuffer**
-   **MapNoOverwriteOnDynamicBufferSRV** e **MultisampleRTVWithForcedSampleCountOne**

**Opções de nível de recurso 11,2 ([**D3D11 \_ Feature \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature)):** os recursos opcionais indicados por esse campo são independentes e devem ser verificados individualmente.

### <a name="feature-support-on-windows-rt-81-and-windows-phone-81-devices"></a>Suporte a recursos em dispositivos Windows RT 8,1 e Windows Phone 8,1

Os dispositivos Tablet Windows RT podem dar suporte a uma variedade de níveis de recursos e recursos opcionais, são otimizados para reduzir o consumo de energia e usar gráficos integrados em vez de GPUs discretas. Os aplicativos da Windows Store para dispositivos ARM devem dar suporte ao nível de recurso 9,1. Os aplicativos DirectX para Windows RT devem aproveitar os recursos opcionais que podem economizar energia e ciclos, como instanciação simples – quando estão disponíveis.

Windows Phone 8 dispositivos móveis dão suporte ao nível de recurso 9,3 com recursos opcionais específicos. Consulte [nível de recurso do Direct3D 9 \_ 3 para Windows Phone 8](/previous-versions/windows/apps/jj714085(v=vs.105)).

## <a name="what-are-the-direct3d-11-optional-features"></a>Quais são os recursos opcionais do Direct3D 11?

O restante deste artigo descreve os recursos opcionais disponíveis no Direct3D 11,2. Os recursos são descritos em ordem cronológica por quando eles foram adicionados para que você possa ter uma noção de quais recursos estão em versões diferentes do Direct3D 11.

## <a name="optional-compute-shader-support-for-feature-level-10"></a>Suporte opcional para sombreador de computação para nível de recurso 10

O recurso a seguir está sempre disponível para dispositivos de nível 10 de recurso:

**[**D3D11 \_ Dados de recurso \_ \_ d3d10 \_ X \_ \_ Opções de hardware**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options):** se isso for **verdadeiro**, o dispositivo dará suporte a sombreadores de computação. Isso inclui suporte para buffers brutos e estruturados.

Quando o dispositivo de nível de recurso 10 \_ 0 ou 10 \_ 1 dá suporte a esse recurso, o dispositivo não tem a garantia de oferecer suporte ao sombreador de computação 4,1. Os aplicativos devem estar preparados para fazer fallback para um sombreador de computação 4,0 se [**ID3D11Device:: CreateComputeShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader) lançar uma exceção com um programa compute shader 4,1.

## <a name="optional-capabilities-for-feature-level-9"></a>Recursos opcionais para o nível de recurso 9

Os recursos a seguir são adicionados para o nível de recurso 9 a partir do Windows 8:

**[**\_ Opções de \_ \_ d3d9 de \_ dados de recurso D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options):** indica suporte para endereçamento de textura de encapsulamento com texturas não Power-of-2. Se houver suporte, o \_ modo de endereço de textura de D3D11 \_ \_ \_ Wrap poderá ser usado com tais texturas.

**[**\_ \_ \_ \_ \_ Suporte à sombra de d3d9 de dados de recursos do D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support):** indica suporte para amostragens de comparação no modelo de sombreador 4,0 de sombreadores de nível de recurso \_ . Isso é usado para testes de profundidade em sombreadores de pixel, permitindo suporte para técnicas comuns, como mapeamento de sombra e estênceis.

O recurso a seguir foi adicionado para dispositivos de nível 9 de recursos, começando no Windows 8.1:

**[**\_ Suporte a \_ \_ \_ \_ instanciação \_ simples de dados de recursos do D3D11 d3d9**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support):** indica suporte para recursos de instanciação simples que podem estar disponíveis no hardware de nível DirectX 9. Instanciação simples significa que todos os membros do **InstanceDataStepRate** das estruturas [**Desc do \_ \_ elemento \_ de entrada D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_input_element_desc) usados para definir o layout de entrada devem ser iguais a 1. Os dispositivos que dão suporte ao nível de recurso 9,3 ou superior já incluem suporte completo para instanciação.

## <a name="optional-floating-point-precision-support-for-shader-programs"></a>Suporte a precisão de ponto flutuante opcional para programas de sombreador

**[**\_ \_ \_ \_ \_ \_ Suporte mínimo à precisão do sombreador de dados de recurso D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support):** os campos nessa estrutura indicam o comprimento dos números de ponto flutuante quando a precisão mínima é habilitada ou 0 se houver suporte apenas para precisão de ponto flutuante de 32 bits completo.

Para dispositivos de nível de recurso 9, a precisão mínima para o sombreador de vértice pode ser diferente do sombreador de pixel. A precisão para o sombreador de vértice é indicada no campo **AllOtherShaderStagesMinPrecision** .

**[**\_ \_ \_ Duplos dados de recurso D3D11: os**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles)** dispositivos de nível 11 de recurso podem dar suporte a cálculos de precisão dupla nos programas do Shader Model 5,0. O suporte para cálculos de precisão dupla dentro do sombreador significa que os floats podem ser convertidos em duplos no programa de sombreador de computação, fornecendo o benefício da computação de precisão mais alta em cada passagem de sombreador. Os números de precisão dupla devem ser convertidos de volta para floats antes de serem gravados no buffer de saída. Observe que a divisão de precisão dupla não é necessariamente suportada.

## <a name="additional-capabilities-for-direct3d-112"></a>Recursos adicionais para o Direct3D 11,2

O Direct3D 11,2 adiciona quatro novos recursos opcionais que podem ser suportados pelos dispositivos do Direct3D 11. Esses recursos estão na estrutura [**D3D11 de \_ dados do recurso \_ \_ D3D11 \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) :

**TiledResourcesTier:** Indica suporte para recursos ao lado do ladrilho e indica o nível de camada com suporte.

**MinMaxFiltering:** Indica suporte para D3D11 \_ filtro \_ mínimo \_ \* e D3D11 \_ filtro \_ máximo \_ \* Opções de filtragem, que comparam o resultado da filtragem ao valor mínimo (ou máximo). Consulte [**\_ filtro D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_filter).

**ClearViewAlsoSupportsDepthOnlyFormats:** Indica suporte para limpeza de exibições de recurso de buffer de profundidade.

**MapOnDefaultBuffers:** Indica suporte para mapeamento de buffers de destino de renderização criados com o sinalizador **\_ \_ padrão de uso de D3D11** .

## <a name="tile-based-rendering"></a>Renderização baseada em bloco

**[**\_ Informações de \_ \_ arquitetura de \_ dados de recurso D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info):** indica se o dispositivo de gráficos executa em lotes os comandos de renderização e realiza renderização baseada em bloco por padrão. Isso pode ser usado como uma dica para otimização do mecanismo de gráficos.

## <a name="optional-features-for-development-and-debugging"></a>Recursos opcionais para desenvolvimento e depuração

**D3D11 \_ Opções de D3D11 de dados de recurso \_ \_ \_ ::D iscardapisseenbydriver:** você pode monitorar esse membro durante o desenvolvimento para eliminar os drivers herdados no hardware em que [**DiscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) e [**DiscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) podem ter sido benéficos de outra forma.

**[**\_ \_ \_ \_ Suporte ao marcador de dados de recurso D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_marker_support):** isso é suportado se o hardware e o driver dão suporte à marcação de dados para a criação de perfil de GPU.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 