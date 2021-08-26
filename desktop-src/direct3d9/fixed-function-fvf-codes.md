---
description: Um código FVF descreve o conteúdo dos vértices armazenados intercalados em um único fluxo de dados.
ms.assetid: 1a616f42-ec24-44ab-872f-7ea43646dd00
title: Códigos FVF de função fixa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ec4fb691192fcc4dbd7dc42c4d6c00829c209f87f68ec32ea42f6c26ff4663c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069186"
---
# <a name="fixed-function-fvf-codes-direct3d-9"></a>Códigos FVF de função fixa (Direct3D 9)

Um código FVF descreve o conteúdo dos vértices armazenados intercalados em um único fluxo de dados. Geralmente, especifica os dados a serem processados pelo pipeline de processamento de vértice de função fixa. Esta é uma declaração de vértice de estilo mais antigo; para ver o estilo de declaração de vértice atual, [**consulte D3DVERTEXELEMENT9**](d3dvertexelement9.md).

Os aplicativos Direct3D podem definir vértices de modelo de várias maneiras diferentes. O suporte para definições de vértice flexíveis, também conhecidas como formatos de vértice flexíveis ou códigos de formato de vértice flexível, possibilita que seu aplicativo use apenas os componentes de vértice necessários, eliminando os componentes que não são usados. Usando apenas os componentes de vértice necessários, seu aplicativo pode conservar memória e minimizar a largura de banda de processamento necessária para renderizar modelos. Você descreve como os vértices são formatados usando uma combinação de códigos [D3DFVF.](d3dfvf.md)

A especificação FVF inclui formatos para o tamanho do ponto, especificados por PSIZE D3DFVF. \_ Esse tamanho é expresso em unidades de espaço da câmera para vértices TL (não transformados e com luz) e em unidades de espaço do dispositivo para vértices TL.

Os métodos de renderização da interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) fornecem aplicativos C++ com métodos que aceitam uma combinação desses sinalizadores e os usam para determinar como renderizar primitivos. Basicamente, esses sinalizadores dizem ao sistema quais componentes de vértice - posição, mesclagem de vértice pesos, normal, cores e o número e o formato de coordenadas de textura - seu aplicativo usa e, indiretamente, quais partes do pipeline de renderização você deseja que o Direct3D aplique a elas. Além disso, a presença ou a ausência de um sinalizador de formato de vértice específico se comunica com o sistema quais campos de componente de vértice estão presentes na memória e que você omitiu.

Para determinar as limitações do dispositivo, você pode consultar um dispositivo para os valores de D3DFVFCAPS \_ DONOTSTRIPELEMENTS e D3DFVFCAPS \_ TEXCOORDCOUNTMASK no membro FVFCaps [**de D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

As coordenadas de textura podem ser declaradas em formatos diferentes, permitindo que as texturas sejam resolvidas usando apenas uma coordenada ou até quatro coordenadas de textura (para coordenadas de textura projetadas em 2D). Para obter mais informações, consulte [Formatos de coordenadas de textura (Direct3D 9)](texture-coordinate-formats.md). Use o conjunto de macros [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) para criar padrões de bits que identificam os formatos de coordenada de textura que seu formato de vértice usa.

Nenhum aplicativo usará todos os componentes. Os campos recíproco homogêneos W (RHW) e vértice normais são mutuamente exclusivos. Nem a maioria dos aplicativos tentará usar todos os oito conjuntos de coordenadas de textura, mas o Direct3D tem essa capacidade. Há várias restrições sobre quais sinalizadores você pode usar com outros sinalizadores. Por exemplo, você não pode usar os sinalizadores XYZ e \_ D3DFVF XYZRHW juntos, pois isso indicaria que seu aplicativo está descrevendo a posição de um vértice com vértices não transformados e \_ transformados.

Para usar a mesclagem de vértice indexada, o sinalizador LASTBETA UBYTE4 D3DFVF deve aparecer no final da \_ \_ declaração FVF. A presença desse sinalizador indica que o quinto peso de mesclagem será tratado como uma DWORD em vez de float. Para obter mais informações, consulte [Indexed Vertex Blending (Direct3D 9)](indexed-vertex-blending.md).

Os exemplos de código a seguir mostram a diferença entre um código FVF que usa o sinalizador D3DFVF \_ LASTBETA UBYTE4 e um que \_ não usa. O sinalizador D3DFVF XYZB3 está presente quando quatro índices de mesclagem são usados porque você sempre subtrai a soma dos três primeiros do número um para obter o quarto \_ (blend = 1 - (blend + blend + blend)).


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



A FVF definida abaixo usa o sinalizador D3DFVF \_ LAST \_ UBYTE4.


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

 

 
