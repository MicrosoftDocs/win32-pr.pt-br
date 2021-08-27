---
description: Esta seção descreve sombreadores que podem ser usados para o modelo de fluxo programável.
ms.assetid: 800aaa27-e1e6-4d35-8de4-7ac94d646870
title: Programando uma ou mais Fluxos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92440abfb6e343bdd3440f5608d6446c0390b1271e5c4c6686a3a46e578476ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118595"
---
# <a name="programming-one-or-more-streams-direct3d-9"></a>Programando uma ou mais Fluxos (Direct3D 9)

Esta seção descreve sombreadores que podem ser usados para o modelo de fluxo programável.

## <a name="using-streams"></a>Usando Fluxos

O DirectX 8 introduziu a noção de um fluxo para vincular dados a registros de entrada para uso por sombreadores. Um fluxo é uma matriz uniforme de dados de componente, em que cada componente consiste em um ou mais elementos que representam uma única entidade, como posição, normal, cor e assim por diante. Fluxos chips gráficos para executar um acesso direto à memória de vários buffers de vértice em paralelo e também fornecer um mapeamento mais natural dos dados do aplicativo. Eles também habilitam multitexture trivial versus multipass. Pense assim:

-   Um vértice é composto por n fluxos.
-   Um fluxo é composto por elementos m.
-   Um elemento é \[ position, color, normal, texture coordinate \] .

O [**método IDirect3DDevice9::SetStreamSource**](/windows/desktop/api) associa um buffer de vértice a um fluxo de dados do dispositivo, criando uma associação entre os dados de vértice e uma das várias portas de fluxo de dados que alimentam as funções de processamento primitivas. As referências reais aos dados de fluxo não ocorrem até que um método de desenho, como [**IDirect3DDevice9::D rawPrimitive,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)seja chamado.

O mapeamento dos elementos de vértice de entrada para os registros de entrada de vértice para sombreadores de vértice programáveis é definido na declaração do sombreador, mas os elementos de vértice de entrada não têm semântica específica sobre seu uso. A interpretação dos elementos de vértice de entrada é programada usando as instruções do sombreador. A função de sombreador de vértice é definida por uma matriz de instruções que são aplicadas a cada vértice. Os registros de saída de vértice são gravados explicitamente, usando instruções na função de sombreador.

Para essa discussão, no entanto, se preocupe menos com o mapeamento semântico de elementos para registros e mais preocupado com o motivo do uso de fluxos e qual problema é resolvido usando fluxos. O principal benefício dos fluxos é que eles removem os custos de dados de vértice associados anteriormente à multitextagem. Antes dos fluxos, um usuário precisava duplicar conjuntos de dados de vértice para lidar com o caso único e multitexto sem elementos de dados não utilizado ou carregar elementos de dados que não seriam usadas, exceto no caso de multitexto.

Aqui está um exemplo de como usar dois conjuntos de dados de vértice, um para textura única e outro para multitexto.


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



A alternativa era ter um único elemento de vértice que continha ambos os conjuntos de coordenadas de textura.


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



Com esses dados de vértice, apenas uma cópia dos dados de posição e cor é carregada na memória, às custas de carregar ambos os conjuntos de coordenadas de textura para renderização mesmo no caso de textura única.

Agora que a negociação está clara, os fluxos fornecem uma correção elegante para esse esclarecimento. Aqui está um conjunto de definições de vértice para dar suporte a três fluxos: um com posição e cor, um com o primeiro conjunto de coordenadas de textura e outro com o segundo conjunto de coordenadas de textura.


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



Agora, crie o objeto de declaração de vértice e de definido como mostrado:


```
LPDIRECT3DVERTEXDECLARATION9 m_pVertexDeclaration;
g_d3dDevice->CreateVertexDeclaration(dwDecl3, &m_pVertexDeclaration);

m_pd3dDevice->SetVertexDeclaration(m_pVertexDeclaration);
```



## <a name="examples-of-combinations"></a>Exemplos de combinações

### <a name="one-stream-diffuse-color"></a>Cor difusa de um fluxo

A declaração de vértice e as configurações de fluxo para renderização de cor difusa teriam esta aparência:


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



### <a name="two-streams-with-color-and-texture"></a>Dois Fluxos com cor e textura

A declaração de vértice e as configurações de fluxo para renderização de textura única seriam assim:


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



### <a name="two-streams-with-color-and-two-textures"></a>Dois Fluxos com cor e duas texturas

A declaração de vértice e as configurações de fluxo para renderização de várias texturas de duas texturas seriam assim:


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



Em todos os casos, a invocação [**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) a seguir é suficiente.


```
       m_pd3dDevice->DrawPrimitive(D3DPT_TRIANGLEFAN, 0, NUM_TRIS);
```



Isso mostra a flexibilidade dos fluxos para resolver o problema de duplicação de dados/transmissão de dados redundantes no barramento (ou seja, perda de largura de banda).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Declaração de vértice](vertex-declaration.md)
</dt> </dl>

 

 
