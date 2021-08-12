---
title: texkill – ps
description: Cancelará a renderização do pixel atual se qualquer um dos três primeiros componentes (UVW) das coordenadas de textura for menor que zero.
ms.assetid: 7641aef8-8931-4a19-827a-75ab17e901ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 462549a9caba9b4b49ca5b5ac088e41320b3d6f731a78a0251d5191cc601a2e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118284024"
---
# <a name="texkill---ps"></a>texkill – ps

Cancelará a renderização do pixel atual se qualquer um dos três primeiros componentes (UVW) das coordenadas de textura for menor que zero.

## <a name="syntax"></a>Sintaxe



| texkill dst |
|-------------|



 

onde

-   dst é um registro de destino

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texkill               | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Essa instrução corresponde à função de [](dx-graphics-hlsl-clip.md) clipe do HLSL.

O texkill não amostra nenhuma textura. Ele opera nos três primeiros componentes das coordenadas de textura fornecidas pelo número de registro de destino. Para ps \_ 1 4, o texkill opera nos dados \_ nos três primeiros componentes do registro de destino.

Você pode usar essa instrução para implementar planos de clipe arbitrários no rasterizador.

Ao usar sombreadores de vértice, o aplicativo é responsável por aplicar a transformação de perspectiva. Isso pode causar problemas para os planos de recorte arbitrários, pois se ele contiver fatores de escala anisomórficos, os planos de recorte também precisarão ser transformados. Portanto, é melhor fornecer uma posição de vértice não injetada a ser usada no clipper arbitrário, que é o conjunto de coordenadas de textura identificado pelo operador texkill.

Essa instrução é usada da seguinte forma:

<dl> tn de texkill  
O mascaramento de pixel é feito da seguinte forma:  
if ( os componentes x,y,z de TextureCoordinates(stage n)<sub>UVWQ</sub>< 0 )  
cancelar renderização de pixel
</dl>

Para o sombreador de pixel \_ 1 1, \_ 1 2 e 1 3, o texkill opera no conjunto de coordenadas de textura dado pelo \_ número do registro de destino. Na versão 1 4, no entanto, o texkill opera nos dados contidos no TN (Registro de Coordenadas de Textura) ou no registro temporário (rn) que foi especificado como \_ o destino. [](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)

Quando a multisampling estiver habilitada, qualquer efeito de analiação obtido nas bordas de polígono devido à multisampling não será obtido ao longo de nenhuma borda que tenha sido gerada pelo texkill. O sombreador de pixel é executado uma vez por pixel.

Este exemplo é apenas uma ilustração.

Este exemplo mascara pixels que têm coordenadas de textura negativas. As cores de pixel são interpoladas de cores de vértice fornecidas nos dados de vértice.


```
ps_1_1       // Version instruction
texkill t0   // Mask out pixel using texture coordinates from stage 0
mov r0, v0   // Move the diffuse color in v0 to r0

// The rendered output from the pixel shader is shown below
```



As coordenadas de textura variam de -0,5 a 0,5 em u e de 0,0 a 1,0 em v. Essa instrução faz com que os valores u negativos são mascarados. A primeira ilustração abaixo mostra a cor do vértice aplicada ao quad sem a instrução texkill aplicada. A segunda ilustração abaixo mostra o resultado da instrução texkill. As cores de pixel das coordenadas de textura abaixo de 0 (em que x vai de -0,5 a 0,0) são mascaradas. A cor da tela de fundo (branco) é usada em que a cor do pixel é mascarada.

![ilustração da saída com a cor do vértice aplicada ao quad sem a instrução texkill](images/pstexkill-in.jpg)![ilustração da saída com a instrução texkill aplicada](images/pstexkill-out.jpg)

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

 

 




