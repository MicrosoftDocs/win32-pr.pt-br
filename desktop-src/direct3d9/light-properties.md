---
description: As propriedades Light descrevem o tipo e a cor da fonte de luz.
ms.assetid: b39f1287-c67b-4cbb-b599-4a1b2f4981ac
title: Propriedades de luz (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63239024109327e483ff93c2ee29fe42fc22c922
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087436"
---
# <a name="light-properties-direct3d-9"></a>Propriedades de luz (Direct3D 9)

As propriedades Light descrevem o tipo e a cor da fonte de luz. Dependendo do tipo de luz usado, uma luz pode ter propriedades de atenuação e intervalo ou para efeitos de destaque. Mas nem todos os tipos de luzes usam todas as propriedades. O Direct3D usa a estrutura [**D3DLIGHT9**](d3dlight9.md) para transportar informações sobre as propriedades claras de todos os tipos de fontes de luz. Esta seção contém informações para todas as propriedades de luz. As informações são divididas nos grupos a seguir.

As propriedades de posição, intervalo e atenuação definem o local da luz no espaço do mundo e como a iluminação emitida se comporta à distância. Assim como acontece com todas as propriedades claras que você usa em C++, elas estão contidas na estrutura [**D3DLIGHT9**](d3dlight9.md) de uma luz.

-   [Atenuação de luz](#light-attenuation)
-   [Cor clara](#light-color)
-   [Direção da Luz](#light-direction)
-   [Posição da luz](#light-position)
-   [Intervalo de luz](#light-range)

## <a name="light-attenuation"></a>Atenuação de luz

A atenuação controla como a intensidade da luz diminui em direção à distância máxima especificada pela propriedade do intervalo. Três membros da estrutura [**D3DLIGHT9**](d3dlight9.md) representam atenuação leve: Attenuation0, Attenuation1 e Attenuation2. Esses membros contêm valores de ponto flutuante variando de 0,0 a infinito, controlando a atenuação de uma luz. Alguns apps definem o membro do Atenuação1 como 1,0 e a outros como 0,0, o que resulta em intensidade de luz que muda como 1 / D, onde D é a distância da fonte de luz para o vértice. A intensidade da luz máxima está na origem, diminuindo a distância da luz para 1 / (intervalo da luz). Normalmente, um aplicativo define Attenuation0 como 0,0, Attenuation1 para um valor constante e Attenuation2 para 0,0.

Você pode combinar valores de atenuação para obter efeitos de atenuação mais complexos. Ou você pode defini-los como valores fora do intervalo normal para criar efeitos de atenuação ainda mais incomuns. Entretanto, não é permitido usar valores de atenuação negativos. Consulte [fator de destaque e atenuação (Direct3D 9)](attenuation-and-spotlight-factor.md).

## <a name="light-color"></a>Cor da luz

As luzes no Direct3D emitem três cores que são usadas de forma independente em cálculos de iluminação do sistema: uma cor difusa, uma ambiente e uma especular. Cada uma é incorporada pelo módulo de iluminação do Direct3D e interage com uma parte do material atual a fim de produzir uma cor final usada na renderização. A cor difusa interage com a propriedade de reflexão difusa do material atual, a cor especular com a propriedade de reflexão especular do material e assim por diante. Para obter informações específicas sobre como o Direct3D aplica essas cores, consulte [matemática de iluminação (Direct3D 9)](mathematics-of-lighting.md).

Em um aplicativo C++, a estrutura [**D3DLIGHT9**](d3dlight9.md) inclui três membros para essas cores: difuso, ambiente e especular-cada uma é uma estrutura [**D3DCOLORVALUE**](d3dcolorvalue.md) que define a cor que está sendo emitida.

O tipo de cor que se aplica mais intensamente aos cálculos do sistema é o difuso. A cor difusa mais comum é o branco (R:1,0 G:1,0 B:1,0), mas você pode criar cores conforme necessário para obter os efeitos desejados. Por exemplo, você pode usar a luz vermelha para uma lareira ou verde para um sinal de tráfego definido como "Avançar".

Em geral, você define os componentes de cor da luz como valores entre 0,0 e 1,0, inclusive, mas isso não é um requisito. Por exemplo, você pode definir todos os componentes como 2,0, o que criar uma luz "mais brilhante do que o branco." Esse tipo de configuração pode ser útil ao usar as configurações de atenuação diferentes da constante.

Observe que, embora o Direct3D use valores RGBA para luzes, o componente de cor alfa não é usado.

Em geral, as cores materiais são usadas para iluminação. No entanto, você pode especificar que as cores materiais de emissão, ambiente, difusas e especulares devem ser substituídas pelas cores de vértice difusas ou especulares. Isso é feito chamando [**Setprocessstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) e definindo as variáveis de estado do dispositivo listadas na tabela a seguir.



| Variável de estado do dispositivo         | Significado                                       | Type                   | Padrão          |
|-------------------------------|-----------------------------------------------|------------------------|------------------|
| D3DRS \_ AMBIENTMATERIALSOURCE  | Define onde obter a cor do material de ambiente.  | D3DMATERIALCOLORSOURCE | MATERIAL de D3DMCS \_ |
| D3DRS \_ DiffuseMaterialSource  | Define onde obter a cor do material difuso.  | D3DMATERIALCOLORSOURCE | D3DMCS \_ COLOR1   |
| D3DRS \_ SPECULARMATERIALSOURCE | Define onde obter a cor do material especular. | D3DMATERIALCOLORSOURCE | D3DMCS \_ COLOR2   |
| D3DRS \_ EMISSIVEMATERIALSOURCE | Define onde obter a cor do material emissiva. | D3DMATERIALCOLORSOURCE | MATERIAL de D3DMCS \_ |
| D3DRS \_ COLORVERTEX            | Desabilita ou habilita o uso de cores de vértice.     | BOOL                   | TRUE             |



 

O valor de alfa/transparência sempre vem somente do canal alfa da cor difusa.

O valor de nevoeiro sempre vem somente do canal alfa da cor especular.

D3DMATERIALCOLORSOURCE pode ter os valores a seguir.

-   \_Material de D3DMCS-a cor do material é usada como fonte.
-   D3DMCS \_ COLOR1 – a cor do vértice difuso é usada como fonte.
-   D3DMCS \_ COLOR2 – a cor do vértice especular é usada como fonte.

## <a name="light-direction"></a>Direção da Luz

A propriedade de direção da luz determina a direção em que a luz emitida pelo objeto se desloca no espaço do mundo. A direção é usada apenas por luzes direcionais e destaques, e é descrita com um vetor.

Defina a direção da luz no membro de direção da estrutura [**D3DLIGHT9**](d3dlight9.md) da luz. O membro de direção é do tipo [**D3DVECTOR**](d3dvector.md). Os vetores de direção são descritos como distâncias de uma origem lógica, independentemente da posição da luz em uma cena. Portanto, um destaque que aponta diretamente para uma cena – ao longo do eixo z positivo-tem um vetor de direção de <0, 0, 1> não importa onde sua posição esteja definida como. Da mesma forma, você pode simular a luz solar diretamente em uma cena usando uma luz direcional cuja direção é <0,-1, 0>. Obviamente, você não precisa criar luzes que brilham ao longo dos eixos de coordenadas; Você pode misturar e combinar valores para criar luzes que brilham em ângulos mais interessantes.

> [!Note]  
> Embora não seja necessário normalizar um vetor de direção da luz, verifique sempre se tem magnitude. Em outras palavras, não use um vetor de direção de <0, 0, 0>.

 

## <a name="light-position"></a>Posição da luz

A posição da luz é descrita usando uma estrutura [**D3DVECTOR**](d3dvector.md) no membro position da estrutura [**D3DLIGHT9**](d3dlight9.md) . Presume-se que as coordenadas x-, y-e z estejam no espaço de mundo. As luzes direcionais são o único tipo de luz que não usa a propriedade de posição.

## <a name="light-range"></a>Intervalo de luz

A propriedade de intervalo da luz determina a distância, no espaço do mundo, em que malhas de uma cena não recebem mais luz emitida pelo objeto. O membro do intervalo contém um valor de ponto flutuante que representa o intervalo máximo da luz, no espaço do mundo. As luzes direcionais não usam a propriedade do intervalo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Luzes e materiais](lights-and-materials.md)
</dt> </dl>

 

 
