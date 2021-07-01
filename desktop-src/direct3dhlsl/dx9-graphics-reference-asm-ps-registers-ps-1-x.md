---
title: ps_1_1__ps_1_2__ps_1_3__ps_1_4 registros
description: Os sombreadores de pixel dependem de registros para obter dados de vértice, para saída de dados de pixel, para manter resultados temporários durante cálculos e identificar estágios de amostragem de textura.
ms.assetid: ca25a030-b4da-4893-b9f3-e3bb12f18d83
keywords:
- Registros – ps_1_1 para ps_1_4
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 68e3645c3e634c4e9cd886600977882dcc3e2018
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129854"
---
# <a name="ps_1_1__ps_1_2__ps_1_3__ps_1_4-registers"></a>ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ 1 \_ 4 Registros

Os sombreadores de pixel dependem de registros para obter dados de vértice, para saída de dados de pixel, para manter resultados temporários durante cálculos e identificar estágios de amostragem de textura. Há vários tipos de registros, cada um com uma funcionalidade exclusiva. Esta seção contém informações de referência para os registros de entrada e saída implementados pelo sombreador de pixel versão 1 \_ X.

Registra os dados de espera para uso pelo sombreador de pixel. Os registros são totalmente descritos nas seções a seguir.

-   Registrar Tipos descreve os quatro tipos de registros disponíveis e suas finalidades.
-   Ler Limite de Porta detalha as restrições de uso de vários registros em uma única instrução.
-   Leitura somente Leitura Gravação descreve quais registros podem ser usados para leitura, gravação ou ambos.
-   O intervalo detalha o intervalo dos dados do componente.

## <a name="register-types"></a>Registrar tipos



| Nome |  Tipo              | Versão 1 \_ 1 | Versão 1 \_ 2      | Versão 1 \_ 3     | Versão 1 \_ 4             |
|------|--------------------|----------|------|------|--------------|
| c\#  | Registro constante  | 8        | 8    | 8    | 8            |
| R\#  | Registro temporário | 2        | 2    | 2    | 6            |
| T\#  | Registro de textura   | 4        | 4    | 4    | 6            |
| V\#  | Registro de cores     | 2        | 2    | 2    | 2 na fase 2 |



 

-   Os registros constantes contêm dados constantes. Os dados podem ser carregados em um registro constante usando [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) ou podem ser definidos [usando def - ps](def---ps.md). Registros constantes não podem ser usáveis por instruções de endereço de textura. A única exceção é a [instrução texm3x3spec - ps,](texm3x3spec---ps.md) que usa um registro constante para fornecer um vetor de raio ocular.
-   Registros temporários são usados para armazenar resultados intermediários. R0 também serve como a saída do sombreador de pixel. O valor em r0 no final do sombreador é a cor do pixel para o sombreador.

    A validação do sombreador [**falhará em CreatePixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader) em qualquer sombreador que tentar ler de um registro temporário que não tenha sido gravado por uma instrução anterior. [**D3DXAssembleShader**](/windows/desktop/direct3d9/d3dxassembleshader) falhará da mesma forma, supondo que a validação está habilitada (não use D3DXSHADER \_ SKIPVALIDATION).

-   Registros de textura

    Para o sombreador de pixel versão \_ 1 1 a 1 3, os registros de textura contêm dados de textura \_ ou coordenadas de textura. Os dados de textura são carregados em um registro de textura quando uma textura é amostrada. A amostragem de textura usa coordenadas de textura para procurar ou amostrar um valor de cor nas coordenadas especificadas (u,v,w,q) ao levar em conta os atributos de estado do estágio de textura. Os dados de coordenadas de textura são interpolados dos dados de coordenadas de textura de vértice e estão associados a um estágio de textura específico. Há uma associação padrão de um para um entre o número do estágio de textura e a ordem de declaração da coordenada de textura. Por padrão, o primeiro conjunto de coordenadas de textura definido no formato de vértice é associado ao estágio de textura 0.

    Para essas versões do sombreador de pixel, os registros de textura se comportam como registros temporários quando usados por instruções aritméticas.

    Para o sombreador de pixel versão 1 4, os registros de textura \_ (t \# ) contêm dados de coordenada de textura somente leitura. Isso significa que o conjunto de coordenadas de textura e o número do estágio de textura são independentes uns dos outros. O número do estágio de textura (do qual amostrar uma textura) é determinado pelo número do registro de destino (r0 a r5). Para a instrução texld, o conjunto de coordenadas de textura é determinado pelo registro de origem (t0 a t5), para que o conjunto de coordenadas de textura possa ser mapeado para qualquer estágio de textura. Além disso, o registro de origem (especificando coordenadas de textura) para o texld também pode ser um registro temporário (r), caso em que o conteúdo do registro temporário é usado como \# coordenadas de textura.

-   Os registros de cores contêm valores de cor por pixel. Os valores são obtidos pela iteração por pixel dos valores de cor difusa e especular nos dados de vértice. Para sombreadores de pixel versão 1 4, os registros de cores estão \_ disponíveis somente durante a segunda fase.

    Se o modo de sombreamento for definido como D3DSHADE FLAT, a iteração de ambas as cores de \_ vértice (difusa e especular) será desabilitada. Independentemente do modo de sombreagem, a caixa ainda será iterada pelo pipeline se o pixel estiver habilitado. Tenha em mente que o cco é aplicado posteriormente no pipeline do que o pixelshader.

    É comum carregar o registro v0 com os dados de cor difusa do vtex. Também é comum carregar o registro v1 com os dados de cor especular do vértice.

    Os valores de dados de cor de entrada são fixados (saturados) para o intervalo de 0 a 1 porque esse é o intervalo de entrada válido para registros de cores no sombreador de pixel.

    Sombreadores de pixel têm acesso somente leitura a registros de cores. O conteúdo desses registros são valores iterados, mas a iteração pode ser executada com precisão muito menor do que as coordenadas de textura.

## <a name="read-port-limit"></a>Limite de porta de leitura

O limite de porta de leitura especifica o número de registros diferentes de cada tipo de registro que podem ser usados como um registro de origem em uma única instrução.



| Nome     | Tipo                   | Versão 1 \_ 1 | Versão 1 \_ 2      | Versão 1 \_ 3     | Versão 1 \_ 4             |
|------|--------------------|----------|------|------|--------------|
| c\#  | Registro constante  | 2        | 2    | 2    | 2            |
| R\#  | Registro temporário | 2        | 2    | 2    | 3            |
| T\#  | Registro de textura   | 2        | 3    | 3    | 1            |
| V\#  | Registro de cores     | 2        | 2    | 2    | 2 na fase 2 |



 

Por exemplo, os registros de cores para quase todas as versões têm um limite de porta de leitura de duas. Isso significa que uma única instrução pode usar um máximo de dois registros de cores diferentes (v0 e v1, por exemplo) como registros de origem. Este exemplo mostra dois registros de cores sendo usados na mesma instrução:


```
mad r0, v1, c2, v0
```



## <a name="read-only-readwrite"></a>Somente leitura, leitura/gravação

Os tipos de registro são identificados de acordo com a funcionalidade RO (somente leitura) ou a funcionalidade de leitura/gravação (RW) na tabela a seguir. Os registros somente leitura podem ser usados apenas como registros de origem em uma instrução; eles nunca podem ser usados como um registro de destino.



| Nome     |  Tipo                  | Versão 1 \_ 1 | Versão 1 \_ 2     | Versão 1 \_ 3     | Versão 1 \_ 4 |
|------|--------------------|----------|------|------|--------------------|
| Nome | Tipo               | 1\_1     | 1\_2 | 1 \_ 3 | 1\_4               |
| c\#  | Registro constante  | RO       | RO   | RO   | RO                 |
| R\#  | Registro temporário | RW       | RW   | RW   | RW                 |
| T\#  | Registro de textura   | RW       | RW   | RW   | Consulte a observação a seguir |
| V\#  | Registro de cores     | RO       | RO   | RO   | RO                 |



 

Registros que são capazes de RW podem ser usados para armazenar resultados intermediários. Isso inclui registros temporários e registros de textura para algumas das versões do sombreador.

> [!Note]  
>
> -   Para o sombreador de pixel versão 1 4, os registros de textura são RO para instruções de endereçamento de textura e os registros de textura não podem ser lidos nem gravados por instruções \_ aritméticas. Além disso, como os registros de textura se tornaram registros de coordenadas de textura, ter acesso a RO não é uma regressão da funcionalidade anterior.

 

## <a name="range"></a>Intervalo

O intervalo é o valor de dados de registro máximo e mínimo. Os intervalos variam de acordo com o tipo de registro. Os intervalos para alguns dos registros podem ser consultados nos limites do dispositivo usando [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps).



| Nome | Tipo               | Intervalo                                               | Versões     |
|------|--------------------|-----------------------------------------------------|--------------|
| c\#  | Registro constante  | -1 a +1                                            | Todas as versões |
| R\#  | Registro temporário | \- PixelShader1xMaxValue para + PixelShader1xMaxValue | Todas as versões |
| T\#  | Registro de textura   | \- MaxTextureRepeat para + MaxTextureRepeat           | Todas as versões |
| V\#  | Registro de cores     | 0 a 1                                              | Todas as versões |



 

O hardware do sombreador de pixel inicial representa dados em registros usando um número de ponto fixo. Isso limita a precisão a um máximo de aproximadamente oito bits para a parte fracionada de um número. Tenha isso em mente ao criar um sombreador.

Para o sombreador de pixel versão \_ 1 1 a \_ 1 3, MaxTextureRepeat deve ser, no mínimo, um. Para 1 \_ 4, MaxTextureRepeat deve ser, no mínimo, oito.

Consulte [**D3DCAPS9 para**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) obter mais informações sobre PixelShader1xMaxValue.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 
