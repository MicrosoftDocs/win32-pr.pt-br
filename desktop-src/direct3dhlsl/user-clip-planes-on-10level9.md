---
title: Planos de corte do usuário no hardware de nível de recurso 9
description: A partir do Windows 8, a linguagem de sombreamento de alto nível (HLSL) da Microsoft oferece suporte a uma sintaxe que você pode usar com a API do Microsoft Direct3D 11 para especificar os planos de clipes de usuário no nível de recurso 9 \_ x e superior.
ms.assetid: C51FB0E5-94C3-4E7F-AC33-E5F0F26EDC11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 968831ca39f2501a44b00f202fd8dfda1f92d1e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294205"
---
# <a name="user-clip-planes-on-feature-level-9-hardware"></a>Planos de corte do usuário no hardware de nível de recurso 9

A partir do Windows 8, a linguagem de sombreamento de alto nível (HLSL) da Microsoft oferece suporte a uma sintaxe que você pode usar com a API do Microsoft Direct3D 11 para especificar os planos de clipes de usuário no [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x e superior. Você pode usar essa sintaxe de recorte de clipes para escrever um sombreador e, em seguida, usar esse objeto Shader com a API do Direct3D 11 para ser executado em todos os níveis de recurso do Direct3D.

-   [Tela de fundo](#background-reading)
-   [Sintaxe](#syntax)
-   [Criando planos de corte no espaço de clipes no nível de recurso 9 e superior](#creating-clip-planes-in-clip-space-on-feature-level-9-and-higher)
    -   [Leitura em segundo plano](#background-reading)
    -   [níveis de recursos do 10Level9](#10level9-feature-levels)
    -   [Matemática do plano de clipe](#clip-plane-math)
    -   [Recorte no espaço de exibição](#clipping-in-view-space)
    -   [Matriz de projeção](#projection-matrix)
    -   [Plano de clipe de espaço de clipe](#clip-space-clip-plane)
-   [Tópicos relacionados](#related-topics)

## <a name="background"></a>Tela de fundo

Você pode acessar os planos de clipes do usuário na API do Microsoft Direct3D 9 por meio dos métodos [**IDirect3DDevice9:: SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane) e [**IDirect3DDevice9:: GetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane) . No Microsoft Direct3D 10 e posterior, você pode acessar os planos de clipes do usuário por meio da semântica de [ \_ ClipDistance de VA](dx-graphics-hlsl-semantics.md) . Mas, antes do Windows 8, \_ o ClipDistance da VA não estava disponível para hardware de [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x nas APIs do Direct3D 10 ou do Direct3D 11. Portanto, antes do Windows 8, a única maneira de acessar os planos de clipes de usuário com \_ o hardware de nível de recurso 9 x foi por meio da API do Direct3D 9. Os aplicativos da Windows Store do Direct3D não podem usar a API do Direct3D 9. Aqui, descrevemos a sintaxe que você pode usar para acessar os planos de clipes do usuário por meio da API do Direct3D 11 no nível de recurso 9 \_ x e superior.

Os aplicativos usam os planos de corte para definir um conjunto de planos invisíveis no mundo 3D que cortam (jogam) todos os primitivos desenhados. O Windows não desenhará nenhum pixel que esteja no lado negativo dos planos de corte. Os aplicativos podem usar os planos de corte para renderizar os reflexos do planar.

## <a name="syntax"></a>Syntax

Use essa sintaxe para declarar os planos de corte como atributos de função em uma [declaração de função](dx-graphics-hlsl-function-syntax.md). Por exemplo, aqui, usamos a sintaxe em um fragmento de sombreador de vértice:

``` syntax
cbuffer ClipPlaneConstantBuffer 
{
       float4 clipPlane1;
       float4 clipPlane2;
};

[clipplanes(clipPlane1,clipPlane2)]
VertexShaderOutput main(VertexShaderInput input)
{
       // the rest of the vertex shader doesn't refer to the clip plane
 
       …
 
       return output;
}
```

Este exemplo para um fragmento de sombreador de vértice denota dois planos de corte. Ele mostra que você precisa colocar o novo atributo **clipplanes** entre colchetes imediatamente antes do valor de retorno do sombreador de vértice. Entre parênteses após o atributo **clipplanes** , você fornece uma lista de até seis constantes **FLOAT4** que definem os coeficientes de plano para cada plano ativo. O exemplo também mostra que você precisa fazer os coeficientes de cada plano residir em um buffer de constantes.

> [!Note]  
> Não há nenhuma sintaxe disponível para desabilitar um plano de corte dinamicamente. Você deve recompilar um sombreador diferente do mesmo sem um atributo **clipplanes** ou seu aplicativo pode definir os coeficientes em seu buffer constante como zero para que o plano não afete mais nenhuma geometria.

 

Essa sintaxe está disponível para qualquer destino de sombreador de vértice 4,0 ou posterior, que inclui vs \_ 4 \_ 0 \_ nível \_ 9 \_ 1 e vs \_ 4 \_ 0 \_ nível \_ 9 \_ 3.

## <a name="creating-clip-planes-in-clip-space-on-feature-level-9-and-higher"></a>Criando planos de corte no espaço de clipes no nível de recurso 9 e superior

Aqui, mostramos como criar planos de corte no espaço de clipes no [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x e superior.

### <a name="background-reading"></a>Leitura em segundo plano

"Introdução à programação de jogos 3D com DirectX 10", de Frank D. Luna, explica o plano de fundo de matemática de gráficos (capítulos 1, 2 e 3) de que você precisa, e os vários espaços e transformações de espaço que ocorrem no sombreador de vértice (seções 5,6 e 5,8).

### <a name="10level9-feature-levels"></a>níveis de recursos do 10Level9

No Direct3D 10 e posterior, você pode recortar qualquer espaço que faça sentido, geralmente no espaço do mundo ou no espaço de exibição. Mas o Direct3D 9 usa o espaço de clipe, que é o espaço de projeção de divisão de perspectiva. Os vetores estão no espaço de clipe quando o sombreador de vértice os passa para os estágios que seguem no [pipeline de gráficos](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline).

Ao escrever um aplicativo da Windows Store, você deve usar os níveis de recurso do 10Level9 ([nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x) para que o aplicativo possa ser executado em um hardware de nível de recurso 9 \_ x e superior. Como seu aplicativo dá suporte ao nível de recurso 9 \_ x e superior, você também deve usar a capacidade comum de aplicar os planos de corte no espaço do clipe.

Quando você compila um sombreador de vértice com vs \_ 4 \_ 0 \_ nível \_ 9 \_ 1 ou posterior, esse sombreador de vértice pode usar o atributo **clipplanes** . Um objeto Direct3D 10 ou posterior tem um produto de ponto do vértice emitido que contém cada uma das constantes globais **FLOAT4** especificadas no atributo. O objeto Direct3D 9 tem metadados suficientes para fazer com que o tempo de execução do 10Level9 emita as chamadas apropriadas para [**IDirect3DDevice9:: SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane).

### <a name="clip-plane-math"></a>Matemática do plano de clipe

Um plano de recorte é definido por um vetor com 4 componentes. Os três primeiros componentes definem um vetor x, y, z que emana da origem no espaço que desejamos cortar. Esse vetor implica em um plano, perpendicular ao vetor e executado por meio da origem. O Windows mantém todos os pixels no lado do vetor do plano e corta todos os pixels por trás do plano. O componente w em diante empurra o plano de volta e faz com que o Windows recorte menos (um negativo w faz com que o Windows recorte mais) ao longo da linha de vetor. Se os componentes x, y, z comporem um vetor de unidade (normalizado), w enviará por push as unidades do plano w de volta.

A matemática que a GPU (unidade de processamento gráfico) executa para determinar o recorte é um produto de ponto simples entre o vetor de vértice (x, y, z, 1) e o vetor de plano de recorte. Essa operação matemática cria um comprimento de projeção no vetor do plano de corte. Um produto de ponto negativo mostra o vértice a ser exibido no lado recortado do plano.

### <a name="clipping-in-view-space"></a>Recorte no espaço de exibição

Aqui está nosso vértice no espaço de exibição:

![vértice no espaço de exibição](images/vertex-clip.png)

Aqui está o nosso plano no espaço de exibição:

![recorte de plano no espaço de exibição](images/clip-plane-view.png)

Este é o produto de ponto do vértice e do plano de recorte no espaço de exibição:

ClipDistance = **v** · **C**  =  *v* ₓ *c* ₓ +*v*<sub>y</sub>*c*<sub>y</sub>  +  *v*<sub>z</sub>*c*<sub>z</sub>  +  *c*<sub>w</sub>

Esta operação matemática funciona para um objeto Direct3D 10 ou posterior, mas não funcionará para um objeto Direct3D 9. Para o Direct3D 9, devemos primeiro obter nossa transformação de projeção no espaço do clipe.

### <a name="projection-matrix"></a>Matriz de projeção

Uma matriz de projeção transforma um vértice do espaço de exibição (onde a origem é o olho do visualizador, + x está à direita, + y está ativo e + z é diretamente à frente) no espaço do clipe. A matriz de projeção lê o vértice para recorte de hardware e o [estágio de rasterização](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage). Aqui está uma matriz de perspectiva padrão (outras projeções exigem matemática diferente):

<dl>    taxa de r de largura/altura da janela  
ângulo de exibição de *α*    
*f*   distância do visualizador até o plano distante  
*n*   distância do visualizador até o plano próximo
</dl>![matriz de projeção](images/projection-matrix.png)

A próxima matriz é uma versão simplificada da matriz anterior. Mostramos a matriz simplificada para que possamos usá-la posteriormente na operação de multiplicação de matriz.

![matriz de projeção simplificada](images/projection-matrix2.png)

Agora, transformamos nosso vértice de espaço de exibição em espaço de clipe com uma multiplicação de matriz:

![multiplicação de matriz](images/matrix-multiply.png)

Em nossa operação de multiplicação de matriz, nossos componentes x e y são apenas ligeiramente ajustados, mas nossos componentes z e w são bastante desconfigurados. Nosso plano de corte não nos dará mais o que desejamos.

### <a name="clip-space-clip-plane"></a>Plano de clipe de espaço de clipe

Aqui, queremos criar um plano de clipe de espaço de clipe cujo produto de ponto com nosso vértice de espaço de clipe nos dê o mesmo valor que o **v · C** na seção [recorte na exibição de espaço](#clipping-in-view-space) .

![plano de recorte](images/clip-space-clip-plane.png)

**v** · **C**  =  **v P** · **C**<sub>P</sub>

*v* ₓ *c* ₓ +*v*<sub>y</sub>*c*<sub>y</sub>  +  *v*<sub>z</sub>*c*<sub>z</sub>  +  *c*<sub>w</sub>  =  *v* ₓ *P* ₓ *C*<sub>P ₓ</sub>  + *v*<sub>y</sub>*P*<sub>y</sub>*c*<sub>p <sub>y</sub></sub>  +  *v*<sub>z</sub>*A*<sub>y</sub>*C*<sub>P <sub>z</sub></sub>  +  *BC*<sub>p <sub>z</sub></sub>  +  *v*<sub>z</sub>*c*<sub>p <sub>w</sub></sub>

Agora, podemos dividir a operação matemática anterior por componente de vértice em quatro equações separadas:

![componente de vértice x do produto do clip plano](images/clip-space-clip-plane-equ1.png)

![componente de vértice y do produto do clip plano](images/clip-space-clip-plane-equ2.png)

![componente de vértice w do produto do clip plano](images/clip-space-clip-plane-equ3.png)

![componente de vértice z do produto do clip plano](images/clip-space-clip-plane-equ4.png)

Nosso plano de espaço de exibição e nossa matriz de projeção derivam e nos fornecem nosso plano de clipes de espaço de clipe.

![plano de clipe de espaço de clipe](images/clip-space-clip-plane-matrix.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para HLSL](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[Sintaxe de declaração da função](dx-graphics-hlsl-function-syntax.md)
</dt> </dl>

 

 