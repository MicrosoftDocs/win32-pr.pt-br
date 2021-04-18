---
description: Um código FVF descreve o conteúdo dos vértices armazenados intercalados em um único fluxo de dados.
ms.assetid: 1a616f42-ec24-44ab-872f-7ea43646dd00
title: Fixos códigos de FVF de função (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd10b655c0692881e5d93b6c716ec9bcd8a76c45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105764537"
---
# <a name="fixed-function-fvf-codes-direct3d-9"></a>Fixos códigos de FVF de função (Direct3D 9)

Um código FVF descreve o conteúdo dos vértices armazenados intercalados em um único fluxo de dados. Geralmente, especifica os dados a serem processados pelo pipeline de processamento de vértice de função fixa. Esta é uma declaração de vértice de estilo mais antigo; para ver o estilo de declaração de vértice atual, consulte [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

Os aplicativos do Direct3D podem definir vértices de modelo de várias maneiras diferentes. O suporte para definições de vértice flexíveis, também conhecido como formatos de vértice flexíveis ou códigos de formato de vértice flexível, possibilita que seu aplicativo use apenas os componentes de vértice de que precisa, eliminando os componentes que não são usados. Usando apenas os componentes de vértice necessários, seu aplicativo pode conservar memória e minimizar a largura de banda de processamento necessária para renderizar modelos. Você descreve como seus vértices são formatados usando uma combinação de códigos [D3DFVF](d3dfvf.md) .

A especificação FVF inclui formatos de tamanho de ponto, especificados por D3DFVF \_ PSIZE. Esse tamanho é expresso em unidades de espaço da câmera para vértices não transformados e iluminados (TL) e em unidades de espaço do dispositivo para os vértices do TL.

Os métodos de renderização da interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) fornecem aplicativos C++ com métodos que aceitam uma combinação desses sinalizadores e os usam para determinar como renderizar primitivos. Basicamente, esses sinalizadores informam ao sistema quais componentes de vértice-posição, pesos de mistura de vértice, normal, cores e o número e formato de coordenadas de textura – seu aplicativo usa e, indiretamente, quais partes do pipeline de renderização você deseja que o Direct3D aplique a eles. Além disso, a presença ou a ausência de um sinalizador de formato de vértice específico se comunica com o sistema que os campos de componente de vértice estão presentes na memória e que você omitiu.

Para determinar as limitações do dispositivo, você pode consultar um dispositivo para obter os valores de D3DFVFCAPS \_ DONOTSTRIPELEMENTS e D3DFVFCAPS \_ TEXCOORDCOUNTMASK no membro FVFCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

As coordenadas de textura podem ser declaradas em formatos diferentes, permitindo que as texturas sejam tratadas usando apenas uma coordenada ou até quatro coordenadas de textura (para coordenadas de textura projetadas em 2D). Para obter mais informações, consulte [formatos de coordenadas de textura (Direct3D 9)](texture-coordinate-formats.md). Use o conjunto de macros [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) para criar padrões de bits que identifiquem os formatos de coordenadas de textura que seu formato de vértice usa.

Nenhum aplicativo usará todos os componentes. Os campos de normal homogêneo W (RHW) e Vertex são mutuamente exclusivos. Nem a maioria dos aplicativos tentará usar todos os oito conjuntos de coordenadas de textura, mas o Direct3D tem essa capacidade. Há várias restrições sobre quais sinalizadores você pode usar com outros sinalizadores. Por exemplo, você não pode usar os \_ sinalizadores D3DFVF XYZ e D3DFVF \_ XYZRHW juntos, já que isso indicaria que seu aplicativo está descrevendo a posição de um vértice com vértices não transformados e transformaram.

Para usar a mesclagem de vértices indexados, o \_ sinalizador D3DFVF LASTBETA \_ UBYTE4 deve aparecer no final da declaração FVF. A presença desse sinalizador indica que o quinto peso de mesclagem será tratado como um DWORD em vez de float. Para obter mais informações, consulte a [combinação de vértices indexados (Direct3D 9)](indexed-vertex-blending.md).

Os exemplos de código a seguir mostram a diferença entre um código FVF que usa \_ o \_ sinalizador D3DFVF LASTBETA UBYTE4 e outro que não faz isso. O sinalizador D3DFVF \_ XYZB3 está presente quando quatro índices de mesclagem são usados porque você sempre subtrai a soma dos três primeiros do número um para obter a quarta (Blend ₄ = 1-(Blend ₁ + Blend ₂ + Blend ₃)).


```
#define D3DFVF_BLENDVERTEX (D3DFVF_XYZB3|D3DFVF_NORMAL|D3DFVF_TEX1)

struct BLENDVERTEX
{
    D3DXVECTOR3 v;       // Referenced as v0 in the vertex shader
    FLOAT       blend1;  // Referenced as v1.x in the vertex shader
    FLOAT       blend2;  // Referenced as v1.y in the vertex shader
    FLOAT       blend3;  // Referenced as v1.z in the vertex shader
                         // v1.w = 1.0 - (v1.x + v1.y + v1.z)
    D3DXVECTOR3 n;       // Referenced as v3 in the vertex shader
    FLOAT       tu, tv;  // Referenced as v7 in the vertex shader
};
```



O FVF definido abaixo usa o \_ sinalizador D3DFVF Last \_ UBYTE4.


```
#define D3DFVF_BLENDVERTEX (D3DFVF_XYZB4 | D3DFVF_LASTBETA_UBYTE4 |D3DFVF_NORMAL|D3DFVF_TEX1)

struct BLENDVERTEX
{
    D3DXVECTOR3 v;       // Referenced as v0 in the vertex shader
    FLOAT       blend1;  // Referenced as v1.x in the vertex shader
    FLOAT       blend2;  // Referenced as v1.y in the vertex shader
    FLOAT       blend3;  // Referenced as v1.z in the vertex shader
                         // v1.w = 1.0 - (v1.x + v1.y + v1.z)
    DWORD       indices; // Referenced as v2.xyzw in the vertex shader 
    D3DXVECTOR3 n;       // Referenced as v3 in the vertex shader
    FLOAT       tu, tv;  // Referenced as v7 in the vertex shader
};
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Declaração de vértice](vertex-declaration.md)
</dt> </dl>

 

 
