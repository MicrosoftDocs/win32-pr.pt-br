---
description: Os dados alfa podem ser fornecidos nos dados de vértice. Para habilitar o vértice alfa, defina D3DRS \_ DiffuseMaterialSource como D3DMCS \_ COLOR1 para que o tempo de execução do Direct3D leve o valor difuso da cor difusa em vez do material.
ms.assetid: 2b0d842d-ee7d-4633-846d-96697153adc7
title: Vértice alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f661c013e324a0bf209b4faca41d1974a41e81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087432"
---
# <a name="vertex-alpha-direct3d-9"></a><span data-ttu-id="e373f-104">Vértice alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e373f-104">Vertex Alpha (Direct3D 9)</span></span>

<span data-ttu-id="e373f-105">Os dados alfa podem ser fornecidos nos dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="e373f-105">Alpha data can be supplied in the vertex data.</span></span> <span data-ttu-id="e373f-106">Para habilitar o vértice alfa, defina D3DRS \_ DiffuseMaterialSource como D3DMCS \_ COLOR1 para que o tempo de execução do Direct3D leve o valor difuso da cor difusa em vez do material.</span><span class="sxs-lookup"><span data-stu-id="e373f-106">To enable vertex alpha, set the D3DRS\_DIFFUSEMATERIALSOURCE to D3DMCS\_COLOR1 so that the Direct3D runtime takes the diffuse value from the diffuse color rather than the material.</span></span>


```
m_pd3dDevice->SetRenderState( D3DRS_DIFFUSEMATERIALSOURCE,  
                                D3DMCS_COLOR1 );
```



<span data-ttu-id="e373f-107">Em seguida, forneça valores Alfa na cor difusa.</span><span class="sxs-lookup"><span data-stu-id="e373f-107">Then, provide alpha values in the diffuse color.</span></span> <span data-ttu-id="e373f-108">A função AddAlphaToASphere, adiciona alfa aos vértices de uma esfera.</span><span class="sxs-lookup"><span data-stu-id="e373f-108">The AddAlphaToASphere function, adds alpha to the vertices of a sphere.</span></span> <span data-ttu-id="e373f-109">Aqui está um exemplo de como fornecer as informações de alfa para a função.</span><span class="sxs-lookup"><span data-stu-id="e373f-109">Here's an example of how to provide the alpha information to the function.</span></span>


```
AddAlphaToASphere( m_pObstacleVertices, 12,  
                    D3DRGBA(light.dcvDiffuse.r, light.dcvDiffuse.g, 
                            light.dcvDiffuse.b, vAlpha ));
```



<span data-ttu-id="e373f-110">Essa é a aparência da função.</span><span class="sxs-lookup"><span data-stu-id="e373f-110">This is what the function looks like.</span></span>


```
 
void AddAlphaToASphere(D3DLVERTEX* pVertices, DWORD dwNumRings, D3DCOLOR lightcolor)
{
    WORD x, y;
    // rings around
    for( y=0; y < dwNumRings; y++ )
        for( x=0; x < (dwNumRings*2)+1; x++ )
            (pVertices++)->color = lightcolor;

    // top and bottom
    (pVertices++)->color = lightcolor;
    (pVertices++)->color = lightcolor;
}
```



<span data-ttu-id="e373f-111">AddAlphaToASphere simplesmente modifica o membro de cor de cada vértice, que são do tipo D3DLVERTEX, para incluir as informações alfa.</span><span class="sxs-lookup"><span data-stu-id="e373f-111">AddAlphaToASphere simply modifies the color member of each vertex, which are of type D3DLVERTEX, to include the alpha information.</span></span>

<span data-ttu-id="e373f-112">D3DLVERTEX é semelhante a este.</span><span class="sxs-lookup"><span data-stu-id="e373f-112">D3DLVERTEX looks like this.</span></span>


```
 
// Lit vertex
typedef struct {
    D3DVALUE x, y, z;
    DWORD dwReserved;
    D3DCOLOR color, specular;
    D3DVALUE tu, tv;
} D3DLVERTEX, *LPD3DLVERTEX;
```



<span data-ttu-id="e373f-113">Desenhando a esfera,</span><span class="sxs-lookup"><span data-stu-id="e373f-113">Drawing the sphere,</span></span>


```
#define D3DFVF_LVERTEX ( D3DFVF_XYZ | D3DFVF_DIFFUSE | D3DFVF_SPECULAR | \
                        D3DFVF_TEX0 )

//...

// Draw the lit sphere
m_pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, D3DFVF_LVERTEX,
                                    m_pObstacleVertices, m_dwNumObstacleVertices,
                                    m_pObstacleIndices,  m_dwNumObstacleIndices, 0 );
```



<span data-ttu-id="e373f-114">resulta em uma esfera transparente usando o vértice alfa.</span><span class="sxs-lookup"><span data-stu-id="e373f-114">results in a transparent sphere using vertex alpha.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e373f-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e373f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e373f-116">Mesclagem alfa</span><span class="sxs-lookup"><span data-stu-id="e373f-116">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 



