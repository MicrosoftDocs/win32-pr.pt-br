---
description: Os Estados de transformação 256-511 são reservados para armazenar até 256 matrizes que podem ser indexadas usando índices de 8 bits.
ms.assetid: 4c15cfc5-afdf-48d4-8fd1-b10cbe596a1c
title: Usando a mesclagem de vértices indexados (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2d14e66fd934e2eaa8b403d694d203edddb229aab0795fa4a396b8baf367ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519471"
---
# <a name="using-indexed-vertex-blending-direct3d-9"></a>Usando a mesclagem de vértices indexados (Direct3D 9)

Os Estados de transformação 256-511 são reservados para armazenar até 256 matrizes que podem ser indexadas usando índices de 8 bits. Use a macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) para mapear índices 0-255 para os Estados de transformação correspondentes. O exemplo de código a seguir mostra como usar o método [**IDirect3DDevice9:: SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) para definir a matriz no número de estado de transformação 256 para uma matriz de identidade.


```
D3DMATRIX matBlend1;
D3DXMatrixIdentity( &matBlend1 );
m_pD3DDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matBlend );
```



Para habilitar ou desabilitar a mesclagem de vértices indexados, defina o \_ estado de RENDERIZAÇÃO D3DRS INDEXEDVERTEXBLENDENABLE como **true**. Quando o estado de renderização é habilitado, você deve passar índices de matriz como DWORDs empacotados com cada vértice. Quando esse estado de renderização é desabilitado e a mesclagem de vértice é habilitada, é equivalente a ter os índices de matriz 0, 1, 2 e 3 em todos os vértices. O exemplo de código a seguir usa o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) para habilitar a mesclagem de vértices indexados.


```
m_pD3DDevice->SetRenderState( D3DRS_INDEXEDVERTEXBLENDENABLE, TRUE );
```



Para habilitar ou desabilitar a mesclagem de vértice, defina o estado de renderização [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) para um valor diferente de D3DRS \_ Disable do tipo enumerado [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) . Se esse estado de renderização não estiver definido como \_ desabilitação de D3DRS, você deverá passar o número necessário de pesos para cada vértice. O exemplo de código a seguir usa **IDirect3DDevice9:: Setrenderingstate** para habilitar a mesclagem de vértice com três pesos para cada vértice.


```
m_pD3DDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_3WEIGHTS );
```



## <a name="determining-indexed-vertex-blending-support"></a>Determinando o suporte à mesclagem de vértices indexados

Para determinar o tamanho máximo da matriz de mesclagem de vértice indexado, verifique o membro MaxVertexBlendMatrixIndex da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) . O exemplo de código abaixo usa o método [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) para recuperar esse tamanho.


```
D3DCAPS9 d3dCaps;
    
m_pD3DDevice->GetDeviceCaps( &d3dCaps );
IndexedMatrixMaxSize = d3dCaps.MaxVertexBlendMatrixIndex;
```



Se o valor definido em MaxVertexBlendMatrixIndex for 0, o dispositivo não oferecerá suporte a matrizes indexadas.

> [!Note]  
> Quando o processamento de vértice de software é usado, as matrizes 256 podem ser usadas para mesclagem de vértices indexados, com ou sem mesclagem normal.

 

## <a name="passing-matrix-indices-to-direct3d"></a>Passando índices de matriz para o Direct3D

Os índices de matrizes mundiais podem ser passados para o Direct3D usando sombreadores de vértice herdados-FVF-ou declarações.

O exemplo de código abaixo mostra como usar sombreadores de vértice herdados.


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



Quando um sombreador de vértice herdado é usado, os índices de matriz são passados junto com as posições de vértice usando \_ sinalizadores D3DFVF XYZBn. Os índices de matriz são passados como bytes dentro de um DWORD e devem estar presentes imediatamente após o último peso do vértice. Os pesos dos vértices também são passados usando D3DFVF \_ XYZBn. Um DWORD embalado contém index3, index2, index1 e index0, em que index0 está localizado no byte mais baixo da DWORD. O número de índices de matriz mundial usados é igual ao número passado para o número de matrizes usadas para mesclagem, conforme definido por [**D3DRS \_ VERTEXBLEND**](./d3drenderstatetype.md).

Quando uma declaração é usada, D3DVSDE \_ BLENDINDICES define o registro de vértice de entrada para o qual obter índices de matriz. Os índices de matriz devem ser passados como D3DVSDT \_ UBYTE4.

O exemplo de código abaixo mostra como usar declarações. Observe que a ordem dos componentes não é mais importante, a menos que você use um sombreador de vértice de função fixa.

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

[Mesclagem de vértice indexado](indexed-vertex-blending.md)
</dt> </dl>

 

 
