---
title: Usando precisão mínima de HLSL
description: A partir do Windows 8, os drivers gráficos podem implementar os tipos de dados escalares HLSL mínimos de precisão usando qualquer precisão maior ou igual à precisão de bit especificada.
ms.assetid: 422B0C45-5CEB-4235-AD05-62D36C36CFC6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7f66f35aef3e870edb4e8564a280be89ce34be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641316"
---
# <a name="using-hlsl-minimum-precision"></a>Usando precisão mínima de HLSL

A partir do Windows 8, os drivers gráficos podem implementar os [tipos de dados escalares HLSL](dx-graphics-hlsl-scalar.md) mínimos de precisão usando qualquer precisão maior ou igual à precisão de bit especificada. Quando o código do sombreador de precisão mínima do HLSL é usado em hardware que implementa a precisão mínima do HLSL, você usa menos largura de banda de memória e, como resultado, você também usa menos energia do sistema.

Você pode consultar o suporte mínimo de precisão que o driver de gráficos fornece chamando [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) com o valor de [**\_ \_ \_ \_ \_ suporte mínimo de precisão do recurso do D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) . Para obter mais informações, consulte [suporte mínimo de precisão do HLSL](/windows/desktop/direct3d11/direct3d-11-1-features).

-   [Declarar variáveis com tipos de dados de precisão mínima](#declare-variables-with-minimum-precision-data-types)
-   [Testando seu código de sombreador de precisão mínimo](#testing-your-minimum-precision-shader-code)
-   [Tópicos relacionados](#related-topics)

## <a name="declare-variables-with-minimum-precision-data-types"></a>Declarar variáveis com tipos de dados de precisão mínima

Para usar a precisão mínima no código do sombreador HLSL, declare variáveis individuais com tipos como **min16float** (**min16float4** para um vetor), **min16int**, **min10float** e assim por diante. Com essas variáveis, o código do sombreador indica que ele não requer mais precisão do que as variáveis indicam. Mas o hardware pode ignorar os indicadores de precisão mínima e executar com precisão de 32 bits cheia. Quando o código do sombreador é usado em hardware que aproveita a precisão mínima, você usa menos largura de banda de memória e, como resultado, você também usa menos energia do sistema, desde que o código do sombreador não espere mais precisão do que o especificado.

Você não precisa criar vários sombreadores que não usam a precisão mínima. Em vez disso, crie sombreadores com precisão mínima, e as variáveis de precisão mínimas se comportarão na precisão de 32 bits completa se o driver de gráficos relatar que ele não dá suporte a precisão mínima. Os sombreadores de precisão mínima do HLSL não funcionam em sistemas operacionais anteriores ao Windows 8, portanto, se você planeja direcionar sistemas operacionais anteriores, precisará criar vários sombreadores, alguns dos outros que não usam precisão mínima.

> [!Note]  
> Não faça alternâncias de dados entre diferentes níveis de precisão em um sombreador porque esses tipos de conversões são desperdícios e reduzem o desempenho. A exceção é que as constantes do sombreador ainda são sempre de 32 bits, mas os fornecedores podem criar um hardware de gráficos que pode fazer a conversão livremente para qualquer precisão menor que a leitura da instrução HLSL possa usar.

 

Usando a precisão mínima, você pode controlar a precisão dos cálculos em várias partes do seu código de sombreador.

As regras de precisão mínima de HLSL são semelhantes ao C/C++, em que os tipos em uma expressão determinam a precisão da operação, e não o tipo que está sendo eventualmente gravado.

## <a name="testing-your-minimum-precision-shader-code"></a>Testando seu código de sombreador de precisão mínimo

O rasterizador de referência [**( \_ \_ \_ referência de tipo de driver D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type)) fornece uma ideia aproximada de como o mínimo de precisão no código do sombreador HLSL se comporta ao quantificar cada instrução HLSL para a precisão especificada. Isso ajuda a descobrir o código que pode depender acidentalmente de mais do que a precisão mínima. O rasterizador de referência não é executado mais rapidamente quando o código do sombreador HLSL usa a precisão mínima, mas você pode usá-lo para verificar a exatidão do seu código. [Warp](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-warp) ([**tipo de driver do D3D \_ \_ \_ Warp**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type)) não dá suporte ao uso da precisão mínima no código do sombreador HLSL; WARP executa apenas uma precisão de 32 bits cheia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 