---
title: texkill-PS
description: Cancela a renderização do pixel atual se qualquer um dos três primeiros componentes (UVW) das coordenadas de textura for menor que zero.
ms.assetid: 7641aef8-8931-4a19-827a-75ab17e901ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4da9c6b59a3c16eeecb8755f2f19542df6ee8a7b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293551"
---
# <a name="texkill---ps"></a>texkill-PS

Cancela a renderização do pixel atual se qualquer um dos três primeiros componentes (UVW) das coordenadas de textura for menor que zero.

## <a name="syntax"></a>Syntax



| texkill DST |
|-------------|



 

onde

-   o DST é um registro de destino

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texkill               | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Essa instrução corresponde à função de [**clipe**](dx-graphics-hlsl-clip.md) do HLSL.

texkill não faz amostragem de nenhuma textura. Ele opera nos três primeiros componentes das coordenadas de textura dadas pelo número de registro de destino. Para o PS \_ 1 \_ 4, o texkill opera nos dados nos três primeiros componentes do registro de destino.

Você pode usar essa instrução para implementar planos de corte arbitrários no rasterizador.

Ao usar sombreadores de vértice, o aplicativo é responsável por aplicar a transformação de perspectiva. Isso pode causar problemas para os planos de recorte arbitrários porque, se ele contiver fatores de escala anisomorphic, os planos de corte também precisam ser transformados. Portanto, é melhor fornecer uma posição de vértice não projetada para uso no Clipper arbitrário, que é o conjunto de coordenadas de textura identificado pelo operador texkill.

Essa instrução é usada da seguinte maneira:

<dl> texkill TN  
O mascaramento de pixels é feito da seguinte maneira:  
If (os componentes x, y, z de TextureCoordinates (estágio n)<sub>UVWQ</sub>< 0)  
cancelar renderização de pixel
</dl>

Para o sombreador de pixel 1 \_ 1, 1 \_ 2 e 1 \_ 3, texkill opera no conjunto de coordenadas de textura fornecido pelo número de registro de destino. No \_ entanto, na versão 1 4, o texkill opera nos dados contidos no TN ( [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) ) ou no registro temporário (RN) que foi especificado como o destino.

Quando a multiamostragem está habilitada, qualquer efeito de suavização obtido nas bordas do polígono devido a uma multiamostração não será Obtido em qualquer borda que tenha sido gerada pelo texkill. O sombreador de pixel é executado uma vez por pixel.

Este exemplo é apenas uma ilustração.

Este exemplo mascara os pixels que têm coordenadas de textura negativas. As cores de pixel são interpoladas das cores de vértice fornecidas nos dados do vértice.


```
ps_1_1       // Version instruction
texkill t0   // Mask out pixel using texture coordinates from stage 0
mov r0, v0   // Move the diffuse color in v0 to r0

// The rendered output from the pixel shader is shown below
```



As coordenadas de textura variam de-0,5 a 0,5 em u e 0,0 a 1,0 em v. Essa instrução faz com que os valores de u negativos sejam mascarados. A primeira ilustração abaixo mostra a cor do vértice aplicada ao Quad sem a instrução texkill aplicada. A segunda ilustração abaixo mostra o resultado da instrução texkill. As cores de pixel das coordenadas de textura abaixo de 0 (em que x vai de-0,5 a 0,0) são mascaradas. A cor do plano de fundo (branco) é usada onde a cor do pixel é mascarada.

![ilustração da saída com a cor do vértice aplicada ao Quad sem a instrução texkill](images/pstexkill-in.jpg)![ilustração da saída com a instrução texkill aplicada](images/pstexkill-out.jpg)

Os dados de coordenadas de textura são declarados na declaração de dados de vértice neste exemplo.


```
   
struct CUSTOMVERTEX
{
    FLOAT x, y, z;
    DWORD color;
    FLOAT tu1, tv1;
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|D3DFVF_TEX1|D3DTEXCOORD2(0))

static CUSTOMVERTEX g_Vertices[]=
{
    //  x      y     z    color         u1,    v1  
    { -1.0f, -1.0f, 0.0f, 0xffff0000, -0.5f,  1.0f, },
    {  1.0f, -1.0f, 0.0f, 0xff00ff00,  0.5f,  1.0f, },
    {  1.0f,  1.0f, 0.0f, 0xff0000ff,  0.5f,  0.0f, },
    { -1.0f,  1.0f, 0.0f, 0xffffffff, -0.5f,  0.0f, },

};
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




