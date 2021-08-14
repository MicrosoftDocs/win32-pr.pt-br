---
description: Os estados de transformação 256-511 são reservados para armazenar até 256 matrizes que podem ser indexadas usando índices de 8 bits.
ms.assetid: 4c15cfc5-afdf-48d4-8fd1-b10cbe596a1c
title: Usando a mesclagem de vértice indexada (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2d14e66fd934e2eaa8b403d694d203edddb229aab0795fa4a396b8baf367ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519471"
---
# <a name="using-indexed-vertex-blending-direct3d-9"></a>Usando a mesclagem de vértice indexada (Direct3D 9)

Os estados de transformação 256-511 são reservados para armazenar até 256 matrizes que podem ser indexadas usando índices de 8 bits. Use a macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) para mapear índices de 0 a 255 para os estados de transformação correspondentes. O exemplo de código a seguir mostra como usar o método [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) para definir a matriz no número de estado de transformação 256 para uma matriz de identidade.


```
D3DMATRIX matBlend1;
D3DXMatrixIdentity( &matBlend1 );
m_pD3DDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matBlend );
```



Para habilitar ou desabilitar a combinação de vértices indexados, de definir o estado de \_ renderização INDEXEDVERTEXBLENDENABLE D3DRS como **TRUE.** Quando o estado de renderização estiver habilitado, você deverá passar índices de matriz como DWORDs empacotados com cada vértice. Quando esse estado de renderização é desabilitado e a combinação de vértices está habilitada, é equivalente a ter os índices de matriz 0, 1, 2 e 3 em cada vértice. O exemplo de código abaixo usa o [**método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) para habilitar a combinação de vértices indexados.


```
m_pD3DDevice->SetRenderState( D3DRS_INDEXEDVERTEXBLENDENABLE, TRUE );
```



Para habilitar ou desabilitar a combinação de vértices, defina o estado de renderização [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) como um valor diferente de D3DRS DISABLE do tipo \_ enumerado [**D3DVERTEXBLENDFLAGS.**](./d3dvertexblendflags.md) Se esse estado de renderização não estiver definido como D3DRS DISABLE, você deverá passar o número necessário de \_ pesos para cada vértice. O exemplo de código a seguir usa **IDirect3DDevice9::SetRenderState** para habilitar a combinação de vértices com três pesos para cada vértice.


```
m_pD3DDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_3WEIGHTS );
```



## <a name="determining-indexed-vertex-blending-support"></a>Determinando o suporte à combinação de vértices indexados

Para determinar o tamanho máximo da matriz de mesclagem de vértice indexada, verifique o membro MaxVertexBlendMatrixIndex da estrutura [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) O exemplo de código a seguir usa [**o método IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) para recuperar esse tamanho.


```
D3DCAPS9 d3dCaps;
    
m_pD3DDevice->GetDeviceCaps( &d3dCaps );
IndexedMatrixMaxSize = d3dCaps.MaxVertexBlendMatrixIndex;
```



Se o valor definido em MaxVertexBlendMatrixIndex for 0, o dispositivo não dá suporte a matrizes indexadas.

> [!Note]  
> Quando o processamento de vértice de software é usado, 256 matrizes podem ser usadas para mesclagem de vértice indexada, com ou sem mesclagem normal.

 

## <a name="passing-matrix-indices-to-direct3d"></a>Passando índices de matriz para o Direct3D

Índices de matriz mundial podem ser passados para Direct3D usando sombreadores de vértice herdados – FVF – ou declarações.

O exemplo de código a seguir mostra como usar sombreadores de vértice herdado.


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
};
    
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZB2 | D3DFVF_LASTBETA_UBYTE4 |
                             D3DFVF_NORMAL);
```



Quando um sombreador de vértice herdado é usado, os índices de matriz são passados junto com posições de vértice usando sinalizadores XYZBn D3DFVF. \_ Os índices de matriz são passados como bytes dentro de um DWORD e devem estar presentes imediatamente após o último peso do vértice. Os pesos de vértice também são passados usando D3DFVF \_ XYZBn. Uma DWORD empacotada contém index3, index2, index1 e index0, em que index0 está localizado no byte mais baixo do DWORD. O número de índices de matriz mundial usados é igual ao número passado para o número de matrizes usadas para mesclagem, conforme definido por [**\_ VERTEXBLEND D3DRS**](./d3drenderstatetype.md).

Quando uma declaração é usada, D3DVSDE BLENDINDICES define o registro de vértice de entrada do qual \_ obter índices de matriz. Os índices de matriz devem ser passados como D3DVSDT \_ UBYTE4.

O exemplo de código a seguir mostra como usar declarações. Observe que a ordem dos componentes não é mais importante, a menos que use um sombreador de vértice de função fixa.

Aqui está a declaração de vértice.


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
}
```



Aqui está a declaração de registro correspondente.


```
// Create the shader declaration.
D3DVERTEXELEMENT9 decl[] = 
{
    { 0, 0,  D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
    { 0, 12, D3DDECLTYPE_FLOAT1, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BLENDWEIGHT, 0 },
    { 0, 16, D3DDECLTYPE_UBYTE4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BLENDINDICES, 0 },
    { 0, 20, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0 },
    D3DDECL_END()
};
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mesclagem de vértice indexada](indexed-vertex-blending.md)
</dt> </dl>

 

 
