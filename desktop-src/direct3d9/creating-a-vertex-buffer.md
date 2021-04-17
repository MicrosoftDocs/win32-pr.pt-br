---
description: 'Você cria um objeto de buffer de vértice chamando o método IDirect3DDevice9:: CreateVertexBuffer, que aceita cinco parâmetros.'
ms.assetid: 95116ef5-af88-47e7-abf7-1ade9735e2a7
title: Criando um buffer de vértice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ffc831ab508f14d61b8e42861f75422ff6a04bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780666"
---
# <a name="creating-a-vertex-buffer-direct3d-9"></a><span data-ttu-id="32288-103">Criando um buffer de vértice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="32288-103">Creating a Vertex Buffer (Direct3D 9)</span></span>

<span data-ttu-id="32288-104">Você cria um objeto de buffer de vértice chamando o método [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) , que aceita cinco parâmetros.</span><span class="sxs-lookup"><span data-stu-id="32288-104">You create a vertex buffer object by calling the [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) method, which accepts five parameters.</span></span> <span data-ttu-id="32288-105">O primeiro parâmetro especifica o tamanho do buffer de vértice, em bytes.</span><span class="sxs-lookup"><span data-stu-id="32288-105">The first parameter specifies the vertex buffer length, in bytes.</span></span> <span data-ttu-id="32288-106">Use o operador sizeof para determinar o tamanho de um formato de vértice, em bytes.</span><span class="sxs-lookup"><span data-stu-id="32288-106">Use the sizeof operator to determine the size of a vertex format, in bytes.</span></span> <span data-ttu-id="32288-107">Considere o seguinte formato de vértice personalizado.</span><span class="sxs-lookup"><span data-stu-id="32288-107">Consider the following custom vertex format.</span></span>


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



<span data-ttu-id="32288-108">Para criar um buffer de vértice para conter quatro estruturas CUSTOMVERTEX, especifique \[ 4 \* sizeof (CustomVertex) \] para o parâmetro *Length* .</span><span class="sxs-lookup"><span data-stu-id="32288-108">To create a vertex buffer to hold four CUSTOMVERTEX structures, specify \[4\*sizeof(CUSTOMVERTEX)\] for the *Length* parameter.</span></span>

<span data-ttu-id="32288-109">O segundo parâmetro é um conjunto de controles de uso.</span><span class="sxs-lookup"><span data-stu-id="32288-109">The second parameter is a set of usage controls.</span></span> <span data-ttu-id="32288-110">Entre outras coisas, seu valor determina se o buffer de vértice é capaz de conter informações de recorte-na forma de sinalizadores de clipes – para vértices que existem fora da área de exibição.</span><span class="sxs-lookup"><span data-stu-id="32288-110">Among other things, its value determines whether the vertex buffer is capable of containing clipping information - in the form of clip flags - for vertices that exist outside the viewing area.</span></span> <span data-ttu-id="32288-111">Para criar um buffer de vértice que não pode conter sinalizadores de clipe, inclua o \_ sinalizador D3DUSAGE DONOTCLIP para o parâmetro *Usage* .</span><span class="sxs-lookup"><span data-stu-id="32288-111">To create a vertex buffer that cannot contain clip flags, include the D3DUSAGE\_DONOTCLIP flag for the *Usage* parameter.</span></span> <span data-ttu-id="32288-112">O \_ sinalizador D3DUSAGE DONOTCLIP é aplicado somente se você também indicar que o buffer de vértice conterá vértices transformados – o \_ sinalizador D3DFVF XYZRHW está incluído no parâmetro *FVF* .</span><span class="sxs-lookup"><span data-stu-id="32288-112">The D3DUSAGE\_DONOTCLIP flag is applied only if you also indicate that the vertex buffer will contain transformed vertices - the D3DFVF\_XYZRHW flag is included in the *FVF* parameter.</span></span> <span data-ttu-id="32288-113">O método [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) ignora o sinalizador D3DUSAGE \_ DONOTCLIP se você indicar que o buffer conterá vértices não transformados (o \_ sinalizador D3DFVF XYZ).</span><span class="sxs-lookup"><span data-stu-id="32288-113">The [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) method ignores the D3DUSAGE\_DONOTCLIP flag if you indicate that the buffer will contain untransformed vertices (the D3DFVF\_XYZ flag).</span></span> <span data-ttu-id="32288-114">Os sinalizadores de recorte ocupam memória adicional, tornando um buffer de vértice com capacidade de recorte ligeiramente maior do que um buffer de vértice incapaz de conter sinalizadores de recorte.</span><span class="sxs-lookup"><span data-stu-id="32288-114">Clipping flags occupy additional memory, making a clipping-capable vertex buffer slightly larger than a vertex buffer incapable of containing clipping flags.</span></span> <span data-ttu-id="32288-115">Como esses recursos são alocados quando o buffer de vértice é criado, você deve solicitar um buffer de vértice com capacidade de recorte antes do tempo.</span><span class="sxs-lookup"><span data-stu-id="32288-115">Because these resources are allocated when the vertex buffer is created, you must request a clipping-capable vertex buffer ahead of time.</span></span>

<span data-ttu-id="32288-116">O terceiro parâmetro, *FVF*, é uma combinação de [D3DFVF](d3dfvf.md) que descreve o formato de vértice do buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="32288-116">The third parameter, *FVF*, is a combination of [D3DFVF](d3dfvf.md) that describe the vertex format of the vertex buffer.</span></span> <span data-ttu-id="32288-117">Se você especificar 0 para esse parâmetro, o buffer de vértice será um buffer de vértice não FVF.</span><span class="sxs-lookup"><span data-stu-id="32288-117">If you specify 0 for this parameter, then the vertex buffer is a non-FVF vertex buffer.</span></span> <span data-ttu-id="32288-118">Para obter mais informações, consulte [buffers de vértices do FVF (Direct3D 9)](fvf-vertex-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="32288-118">For more information, see [FVF Vertex Buffers (Direct3D 9)](fvf-vertex-buffers.md).</span></span> <span data-ttu-id="32288-119">O quarto parâmetro descreve a classe de memória na qual posicionar o buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="32288-119">The fourth parameter describes the memory class into which to place the vertex buffer.</span></span>

<span data-ttu-id="32288-120">O parâmetro final que [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) aceita é o endereço de uma variável que será preenchida com um ponteiro para a nova interface [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) do objeto de buffer de vértice, se a chamada for realizada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="32288-120">The final parameter that [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) accepts is the address of a variable that will be filled with a pointer to the new [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) interface of the vertex buffer object, if the call succeeds.</span></span>

<span data-ttu-id="32288-121">Você não pode produzir sinalizadores de clipe para um buffer de vértice que foi criado sem suporte para eles.</span><span class="sxs-lookup"><span data-stu-id="32288-121">You cannot produce clip flags for a vertex buffer that was created without support for them.</span></span>

<span data-ttu-id="32288-122">O exemplo de código C++ a seguir mostra como a criação de um buffer de vértice pode ser semelhante ao código.</span><span class="sxs-lookup"><span data-stu-id="32288-122">The following C++ code example shows what creating a vertex buffer might look like in code.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="32288-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="32288-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32288-124">Buffers de vértice</span><span class="sxs-lookup"><span data-stu-id="32288-124">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 
