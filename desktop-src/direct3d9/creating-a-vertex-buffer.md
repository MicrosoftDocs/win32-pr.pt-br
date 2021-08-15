---
description: Crie um objeto de buffer de vértice chamando o método IDirect3DDevice9::CreateVertexBuffer, que aceita cinco parâmetros.
ms.assetid: 95116ef5-af88-47e7-abf7-1ade9735e2a7
title: Criando um buffer de vértice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c12cb50d7879ef73d4c760ac61a0698651cb9ed7d334c90475bd2e8ee4148db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527670"
---
# <a name="creating-a-vertex-buffer-direct3d-9"></a>Criando um buffer de vértice (Direct3D 9)

Crie um objeto de buffer de vértice chamando o método [**IDirect3DDevice9::CreateVertexBuffer,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) que aceita cinco parâmetros. O primeiro parâmetro especifica o comprimento do buffer de vértice, em bytes. Use o operador sizeof para determinar o tamanho de um formato de vértice, em bytes. Considere o seguinte formato de vértice personalizado.


```
struct CUSTOMVERTEX {
        FLOAT x, y, z;
        FLOAT rhw;
        DWORD color;
        FLOAT tu, tv;   // Texture coordinates
};

// Custom flexible vertex format (FVF) describing the custom vertex structure
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW | D3DFVF_DIFFUSE | D3DFVF_TEX1)
```



Para criar um buffer de vértice para conter quatro estruturas CUSTOMVERTEX, especifique \[ 4 \* sizeof(CUSTOMVERTEX) \] para o *parâmetro* Length.

O segundo parâmetro é um conjunto de controles de uso. Entre outras coisas, seu valor determina se o buffer de vértice é capaz de conter informações de recorte – na forma de sinalizadores de clipe – para vértices que existem fora da área de exibição. Para criar um buffer de vértice que não pode conter sinalizadores de clipe, inclua o sinalizador D3DUSAGE \_ DONOTCLIP para o *parâmetro* Usage. O sinalizador D3DUSAGE DONOTCLIP será aplicado somente se você também indicar que o buffer de vértice conterá vértices transformados – o sinalizador \_ XYZRHW D3DFVF está incluído no parâmetro \_ *FVF.* O método [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) ignorará o sinalizador D3DUSAGE DONOTCLIP se você indicar que o buffer conterá vértices nãotransformados (o sinalizador \_ XYZ D3DFVF). \_ Os sinalizadores de recorte ocupam memória adicional, tornando um buffer de vértice com capacidade de recorte um pouco maior do que um buffer de vértice incapaz de conter sinalizadores de recorte. Como esses recursos são alocados quando o buffer de vértice é criado, você deve solicitar um buffer de vértice com capacidade de recorte com antecedência.

O terceiro parâmetro, *FVF*, é uma combinação de [D3DFVF](d3dfvf.md) que descreve o formato de vértice do buffer de vértice. Se você especificar 0 para esse parâmetro, o buffer de vértice será um buffer de vértice não FVF. Para obter mais informações, consulte [Buffers de vértice FVF (Direct3D 9)](fvf-vertex-buffers.md). O quarto parâmetro descreve a classe de memória na qual colocar o buffer de vértice.

O parâmetro final que [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) aceita é o endereço de uma variável que será preenchida com um ponteiro para a nova interface [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) do objeto de buffer de vértice, se a chamada for bem-sucedida.

Você não pode produzir sinalizadores de clipe para um buffer de vértice que foi criado sem suporte para eles.

O exemplo de código C++ a seguir mostra a aparência da criação de um buffer de vértice no código.


```
   
// d3dDevice contains the address of an IDirect3DDevice9 interface
// g_pVB is a variable of type LPDIRECT3DVERTEXBUFFER9 

// The custom vertex type
struct CUSTOMVERTEX {
    FLOAT x, y, z;
    FLOAT rhw;
    DWORD color;
    FLOAT tu, tv;   // The texture coordinates
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW | D3DFVF_DIFFUSE | D3DFVF_TEX1)

// Create a clipping-capable vertex buffer. Allocate enough memory 
// in the default memory pool to hold three CUSTOMVERTEX 
// structures

    if( FAILED( d3dDevice->CreateVertexBuffer( 3*sizeof(CUSTOMVERTEX),
            0 /*Usage*/, D3DFVF_CUSTOMVERTEX, D3DPOOL_DEFAULT, &g_pVB, NULL ) ) )
        return E_FAIL;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffers de vértice](vertex-buffers.md)
</dt> </dl>

 

 
