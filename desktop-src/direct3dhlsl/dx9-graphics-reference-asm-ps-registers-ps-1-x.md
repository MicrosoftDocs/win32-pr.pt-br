---
title: Registros de ps_1_1__ps_1_2__ps_1_3__ps_1_4
description: Sombreadores de pixel dependem de registros para obter dados de vértice, para saída de dados de pixel, para manter resultados temporários durante cálculos e para identificar estágios de amostragem de textura.
ms.assetid: ca25a030-b4da-4893-b9f3-e3bb12f18d83
keywords:
- Registra-ps_1_1 para ps_1_4
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 291f78b8bf74a20dfecf4a74ed65173a895bcc1b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998633"
---
# <a name="ps_1_1__ps_1_2__ps_1_3__ps_1_4-registers"></a>PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 PS 1 \_ \_ \_ \_ 3 \_ \_ PS \_ 1 \_ 4 registros

Sombreadores de pixel dependem de registros para obter dados de vértice, para saída de dados de pixel, para manter resultados temporários durante cálculos e para identificar estágios de amostragem de textura. Há vários tipos de registradores, cada um com uma funcionalidade exclusiva. Esta seção contém informações de referência para os registros de entrada e saída implementados pelo pixel shader versão 1 \_ X.

Registra os dados de retenção para uso pelo sombreador de pixel. Os registros são totalmente descritos nas seções a seguir.

-   Os tipos de registro descrevem os quatro tipos de registros disponíveis e suas finalidades.
-   O limite de porta de leitura detalha as restrições sobre o uso de vários registros em uma única instrução.
-   Read Only Read Write descreve quais registros podem ser usados para leitura, gravação ou ambos.
-   Intervalo detalha o intervalo dos dados do componente.

## <a name="register-types"></a>Tipos de registro



|      |                    | Versões |      |      |              |
|------|--------------------|----------|------|------|--------------|
| Nome | Type               | 1\_1     | 1\_2 | 1 \_ 3 | 1\_4         |
| c\#  | Registro constante  | 8        | 8    | 8    | 8            |
| d\#  | Registro temporário | 2        | 2    | 2    | 6            |
| t\#  | Registro de textura   | 4        | 4    | 4    | 6            |
| l\#  | Registro de cores     | 2        | 2    | 2    | 2 na fase 2 |



 

-   Os registros constantes contêm dados constantes. Os dados podem ser carregados em um registro constante usando [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) ou podem ser definidos usando [def-PS](def---ps.md). Os registros constantes não podem ser usados por instruções de endereço de textura. A única exceção é a instrução [texm3x3spec-PS](texm3x3spec---ps.md) , que usa um registro constante para fornecer um vetor de raio de olho.
-   Os registros temporários são usados para armazenar resultados intermediários. R0 adicionalmente serve como a saída do sombreador de pixel. O valor em R0 no final do sombreador é a cor de pixel do sombreador.

    A validação do sombreador falhará [**CreatePixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader) em qualquer sombreador que tentar ler de um registro temporário que não tenha sido gravado por uma instrução anterior. [**D3DXAssembleShader**](/windows/desktop/direct3d9/d3dxassembleshader) falhará da mesma forma, supondo que a validação esteja habilitada (não use D3DXSHADER \_ SKIPVALIDATION).

-   Registros de textura

    Para o sombreador de pixel versão 1 \_ 1 a 1 \_ 3, os registros de textura contêm dados de textura ou coordenadas de textura. Os dados de textura são carregados em um registro de textura quando uma textura é amostrada. A amostragem de textura usa coordenadas de textura para pesquisar ou obter um valor de cor nas coordenadas especificadas (u, v, w, q) ao levar em conta os atributos de estado do estágio de textura. Os dados de coordenadas de textura são interpolados dos dados de coordenadas de textura de vértice e associados a um estágio de textura específico. Há uma associação um-para-um padrão entre o número de estágio de textura e a ordem de declaração de coordenada de textura. Por padrão, o primeiro conjunto de coordenadas de textura definido no formato de vértice é associado ao estágio 0 de textura.

    Para essas versões de sombreador de pixel, os registros de textura se comportam exatamente como registros temporários quando usados por instruções aritméticas.

    Para o sombreador de pixel versão 1 \_ 4, os registros de textura (t \# ) contêm dados de coordenadas de textura somente leitura. Isso significa que o conjunto de coordenadas de textura e o número de estágio de textura são independentes um do outro. O número de estágio de textura (a partir do qual uma textura é amostrada) é determinado pelo número de registro de destino (R0 para R5). Para a instrução texld, o conjunto de coordenadas de textura é determinado pelo registro de origem (T0 para T5), portanto, o conjunto de coordenadas de textura pode ser mapeado para qualquer estágio de textura. Além disso, o registro de origem (especificando coordenadas de textura) para texld também pode ser um registro temporário (r \# ), caso em que o conteúdo do registro temporário é usado como coordenadas de textura.

-   Os registros de cores contêm valores de cor por pixel. Os valores são obtidos por iteração por pixel dos valores de cor difuso e especular nos dados do vértice. Para sombreador de pixel versão 1 \_ 4, os registros de cor estão disponíveis somente durante a segunda fase.

    Se o modo de sombreamento for definido como D3DSHADE \_ , a iteração das cores de vértice (difusa e especular) será desabilitada. Independentemente do modo de sombreamento, a neblina ainda será iterada pelo pipeline se a sombra de pixel estiver habilitada. Tenha em mente que a neblina é aplicada posteriormente no pipeline do que o PixelShader.

    É comum carregar o registro V0 com os dados de cores difusas do vértice. Também é comum carregar o registro v1 com os dados de cores especulares de vértice.

    Os valores de dados de cor de entrada são clamped (saturados) para o intervalo de 0 a 1 porque esse é o intervalo de entrada válido para registros de cor no sombreador de pixel.

    Os sombreadores de pixel têm acesso somente leitura aos registros de cores. O conteúdo desses registros são valores iterados, mas a iteração pode ser executada em uma precisão muito menor do que as coordenadas de textura.

## <a name="read-port-limit"></a>Limite de porta de leitura

O limite da porta de leitura especifica o número de registros diferentes de cada tipo de registro que pode ser usado como um registro de origem em uma única instrução.



|      |                    | Versões |      |      |              |
|------|--------------------|----------|------|------|--------------|
| Nome | Type               | 1\_1     | 1\_2 | 1 \_ 3 | 1\_4         |
| c\#  | Registro constante  | 2        | 2    | 2    | 2            |
| d\#  | Registro temporário | 2        | 2    | 2    | 3            |
| t\#  | Registro de textura   | 2        | 3    | 3    | 1            |
| l\#  | Registro de cores     | 2        | 2    | 2    | 2 na fase 2 |



 

Por exemplo, a cor registrada para quase todas as versões tem um limite de porta de leitura de dois. Isso significa que uma única instrução pode usar um máximo de dois registros de cores diferentes (V0 e V1, por exemplo) como registros de origem. Este exemplo mostra dois registros de cor que estão sendo usados na mesma instrução:


```
mad r0, v1, c2, v0
```



## <a name="read-only-readwrite"></a>Somente leitura, leitura/gravação

Os tipos de registro são identificados de acordo com a capacidade somente leitura (RO) ou o recurso de leitura/gravação (RW) na tabela a seguir. Registros somente leitura podem ser usados somente como registros de origem em uma instrução; Eles nunca podem ser usados como um registro de destino.



|      |                    | Versões |      |      |                    |
|------|--------------------|----------|------|------|--------------------|
| Nome | Type               | 1\_1     | 1\_2 | 1 \_ 3 | 1\_4               |
| c\#  | Registro constante  | RO       | RO   | RO   | RO                 |
| d\#  | Registro temporário | RW       | RW   | RW   | RW                 |
| t\#  | Registro de textura   | RW       | RW   | RW   | Consulte a observação a seguir |
| l\#  | Registro de cores     | RO       | RO   | RO   | RO                 |



 

Os registros que têm capacidade de RW podem ser usados para armazenar resultados intermediários. Isso inclui os registros temporários e os registros de textura para algumas das versões do sombreador.

> [!Note]  
>
> -   Para o sombreador de pixel versão 1 \_ 4, os registros de textura são ro para instruções de endereçamento de textura e os registros de textura não podem ser lidos nem gravados por instruções aritméticas. Além disso, como os registros de textura se tornaram registros de coordenadas de textura, ter acesso à RO não é uma regressão da funcionalidade anterior.

 

## <a name="range"></a>Intervalo

O intervalo é o valor de dados de registro máximo e mínimo. Os intervalos variam de acordo com o tipo de registro. Os intervalos para alguns dos registros podem ser consultados a partir das tampas do dispositivo usando [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps).



| Nome | Type               | Intervalo                                               | Versões     |
|------|--------------------|-----------------------------------------------------|--------------|
| c\#  | Registro constante  | -1 a + 1                                            | Todas as versões |
| d\#  | Registro temporário | \- PixelShader1xMaxValue a + PixelShader1xMaxValue | Todas as versões |
| t\#  | Registro de textura   | \- MaxTextureRepeat a + MaxTextureRepeat           | Todas as versões |
| l\#  | Registro de cores     | 0 a 1                                              | Todas as versões |



 

O hardware do sombreador de pixel inicial representa dados em registros usando um número de ponto fixo. Isso limita a precisão a um máximo de aproximadamente oito bits para a parte fracionária de um número. Tenha isso em mente ao criar um sombreador.

Para o sombreador de pixel versão 1 \_ 1 a 1 \_ 3, MaxTextureRepeat deve ser um mínimo de um. Para 1 \_ 4, MaxTextureRepeat deve ser um mínimo de oito.

Consulte [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) para obter mais informações sobre PixelShader1xMaxValue.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 
