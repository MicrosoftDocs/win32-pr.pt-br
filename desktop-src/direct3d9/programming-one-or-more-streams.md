---
description: Esta seção descreve os sombreadores que podem ser usados para o modelo de fluxo programável.
ms.assetid: 800aaa27-e1e6-4d35-8de4-7ac94d646870
title: Programando um ou mais fluxos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43210823911648ed11227faef44d980b60d0a335
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105791052"
---
# <a name="programming-one-or-more-streams-direct3d-9"></a>Programando um ou mais fluxos (Direct3D 9)

Esta seção descreve os sombreadores que podem ser usados para o modelo de fluxo programável.

## <a name="using-streams"></a>Usando fluxos

O DirectX 8 introduziu a noção de um fluxo para associar dados a registros de entrada para uso por sombreadores. Um fluxo é uma matriz uniforme de dados de componente, onde cada componente consiste em um ou mais elementos que representam uma única entidade, como posição, normal, cor e assim por diante. Os fluxos permitem que os chips gráficos executem um acesso direto à memória a partir de vários buffers de vértice em paralelo e também forneçam um mapeamento mais natural dos dados do aplicativo. Eles também habilitam multitextura trivial versus MultiPASS. Considere o seguinte:

-   Um vértice é composto por n fluxos.
-   Um fluxo é composto por elementos m.
-   Um elemento é \[ posição, cor, normal, coordenada de textura \] .

O método [**IDirect3DDevice9:: Setstreamname**](/windows/desktop/api) associa um buffer de vértice a um fluxo de dados do dispositivo, criando uma associação entre os dados de vértice e uma das várias portas de fluxo de dados que alimentam as funções de processamento primitivo. As referências reais aos dados de fluxo não ocorrem até que um método de desenho, como [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), seja chamado.

O mapeamento dos elementos de vértice de entrada para os registros de entrada de vértice para sombreadores de vértice programáveis é definido na declaração de sombreador, mas os elementos de vértice de entrada não têm semântica específica sobre seu uso. A interpretação dos elementos de vértice de entrada é programada usando as instruções do sombreador. A função de sombreador de vértice é definida por uma matriz de instruções que são aplicadas a cada vértice. Os registros de saída de vértice são gravados explicitamente no, usando instruções na função de sombreador.

Para essa discussão, no entanto, esteja menos preocupado com o mapeamento semântico de elementos para registros e mais preocupados com o motivo do uso de fluxos e qual problema é resolvido usando fluxos. O principal benefício dos fluxos é que eles removem os custos de dados de vértice associados anteriormente ao multitexturing. Antes dos fluxos, um usuário tinha que duplicar conjuntos de dados de vértice para manipular o caso único e multitextura sem nenhum elemento de dados não utilizado ou transportar elementos de dados que não seriam usados, exceto no caso multitextura.

Aqui está um exemplo de como usar dois conjuntos de dados de vértice, um para textura única e outro para multitexturing.


```
struct CUSTOMVERTEX_TEX1
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_1, tv_1;   // Texture coordinates for a single texture
};
 
struct CUSTOMVERTEX_TEX2
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_2, tv_2;   // Texture coordinates for multitexturing
};
```



A alternativa era ter um único elemento Vertex que contivesse ambos os conjuntos de coordenadas de textura.


```
struct CUSTOMVERTEX_TEX2
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_1, tv_1;   // Texture coordinates for a single texture
    float tu_2, tv_2;   // Texture coordinates for multitexturing
};
```



Com esses dados de vértice, apenas uma cópia dos dados de posição e cor é realizada na memória, às custas de carregar os dois conjuntos de coordenadas de textura para renderização, mesmo no caso de textura única.

Agora que a compensação está clara, os fluxos fornecem uma correção elegante para esse dilema. Aqui está um conjunto de definições de vértice para dar suporte a três fluxos: um com posição e cor, um com o primeiro conjunto de coordenadas de textura e outro com o segundo conjunto de coordenadas de textura.


```
// Multistream vertex
// Stream 0, pos, diffuse, specular
struct POSCOLORVERTEX
{
    FLOAT x, y, z;
    DWORD diffColor, specColor;
};
#define D3DFVF_POSCOLORVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|D3DFVF_SPECULAR)
// Stream 1, tex coord 0
struct TEXC0VERTEX
{
    FLOAT tu1, tv1;
};
#define D3DFVF_TEXC0VERTEX (D3DFVF_TEX1)

// Stream 2, tex coord 1
struct TEXC1VERTEX
{
    FLOAT tu2, tv2;
};
#define D3DFVF_TEXC1VERTEX (D3DFVF_TEX0)
```



A declaração de vértice seria a seguinte:


```
// Multitexture - multistream

D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},
    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},
    {2,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 1},
    D3DDECL_END()
};
```



Agora, crie o objeto de declaração de vértice e defina-o como mostrado:


```
LPDIRECT3DVERTEXDECLARATION9 m_pVertexDeclaration;
g_d3dDevice->CreateVertexDeclaration(dwDecl3, &m_pVertexDeclaration);

m_pd3dDevice->SetVertexDeclaration(m_pVertexDeclaration);
```



## <a name="examples-of-combinations"></a>Exemplos de combinações

### <a name="one-stream-diffuse-color"></a>Cor difusa de um fluxo

A declaração de vértice e as configurações de fluxo para renderização de cores difusas teriam a seguinte aparência:


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0,  0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12,  D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0 ,
    {0, 16,  D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},
    D3DDECL_END()
};
   m_pd3dDevice->SetStreamSource(0, m_pVBVertexShader0, 0,
                                      sizeof(CUSTOMVERTEX));
   m_pd3dDevice->SetStreamSource(1, NULL, 0, 0);
   m_pd3dDevice->SetStreamSource(2, NULL, 0, 0);
```



### <a name="two-streams-with-color-and-texture"></a>Dois fluxos com cor e textura

A declaração de vértice e as configurações de fluxo para renderização de textura única teriam a seguinte aparência:


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},

    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},

    D3DDECL_END()
};
   m_pd3dDevice->SetStreamSource(0, m_pVBPosColor, 0,
                                           sizeof(POSCOLORVERTEX));
   m_pd3dDevice->SetStreamSource(1, m_pVBTexC0, 0,
                                           sizeof(TEXC0VERTEX));
   m_pd3dDevice->SetStreamSource(2, NULL, 0, 0);
```



### <a name="two-streams-with-color-and-two-textures"></a>Dois fluxos com cores e duas texturas

A declaração de vértice e as configurações de fluxo para renderização de várias texturas de duas texturas teriam a seguinte aparência:


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},

    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},

    {2,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 1},
    
    D3DDECL_END()
};
 
m_pd3dDevice->SetStreamSource(0, m_pVBPosColor, 0, 
                                          sizeof(POSCOLORVERTEX));
m_pd3dDevice->SetStreamSource(1, m_pVBTexC0, 0, 
                                          sizeof(TEXC0VERTEX));
m_pd3dDevice->SetStreamSource(2, m_pVBTexC1, 0, 
                                          sizeof(TEXC1VERTEX));
```



Em todos os casos, o seguinte [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) invocação é suficiente.


```
       m_pd3dDevice->DrawPrimitive(D3DPT_TRIANGLEFAN, 0, NUM_TRIS);
```



Isso mostra a flexibilidade dos fluxos para resolver o problema de duplicação de dados/transmissão de dados redundantes pelo barramento (ou seja, de desperdício de largura de banda).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Declaração de vértice](vertex-declaration.md)
</dt> </dl>

 

 
