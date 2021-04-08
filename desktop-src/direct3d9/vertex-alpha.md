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
# <a name="vertex-alpha-direct3d-9"></a>Vértice alfa (Direct3D 9)

Os dados alfa podem ser fornecidos nos dados de vértice. Para habilitar o vértice alfa, defina D3DRS \_ DiffuseMaterialSource como D3DMCS \_ COLOR1 para que o tempo de execução do Direct3D leve o valor difuso da cor difusa em vez do material.


```
m_pd3dDevice->SetRenderState( D3DRS_DIFFUSEMATERIALSOURCE,  
                                D3DMCS_COLOR1 );
```



Em seguida, forneça valores Alfa na cor difusa. A função AddAlphaToASphere, adiciona alfa aos vértices de uma esfera. Aqui está um exemplo de como fornecer as informações de alfa para a função.


```
AddAlphaToASphere( m_pObstacleVertices, 12,  
                    D3DRGBA(light.dcvDiffuse.r, light.dcvDiffuse.g, 
                            light.dcvDiffuse.b, vAlpha ));
```



Essa é a aparência da função.


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



AddAlphaToASphere simplesmente modifica o membro de cor de cada vértice, que são do tipo D3DLVERTEX, para incluir as informações alfa.

D3DLVERTEX é semelhante a este.


```
 
// Lit vertex
typedef struct {
    D3DVALUE x, y, z;
    DWORD dwReserved;
    D3DCOLOR color, specular;
    D3DVALUE tu, tv;
} D3DLVERTEX, *LPD3DLVERTEX;
```



Desenhando a esfera,


```
#define D3DFVF_LVERTEX ( D3DFVF_XYZ | D3DFVF_DIFFUSE | D3DFVF_SPECULAR | \
                        D3DFVF_TEX0 )

//...

// Draw the lit sphere
m_pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, D3DFVF_LVERTEX,
                                    m_pObstacleVertices, m_dwNumObstacleVertices,
                                    m_pObstacleIndices,  m_dwNumObstacleIndices, 0 );
```



resulta em uma esfera transparente usando o vértice alfa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mesclagem alfa](alpha-blending.md)
</dt> </dl>

 

 



