---
description: Para determinar se o Direct3D dá suporte à interpolação de vértice, verifique o \_ sinalizador de interpolação D3DVTXPCAPS no membro VertexProcessingCaps da estrutura D3DCAPS9.
ms.assetid: b60c7f96-3752-4703-9059-486d9906c508
title: Usando a interpolação de vértice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ca56cc521b5bff01a5d6af5c2d4ab6b02cd49e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825705"
---
# <a name="using-vertex-tweening-direct3d-9"></a>Usando a interpolação de vértice (Direct3D 9)

Para determinar se o Direct3D dá suporte à interpolação de vértice, verifique o \_ sinalizador de interpolação D3DVTXPCAPS no membro VertexProcessingCaps da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) . O exemplo de código a seguir usa o método [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) para determinar se há suporte para a interpolação.


```
// This example assumes that m_pD3DDevice is 
// a valid pointer to a IDirect3DDevice9 interface.
//
D3DCAPS9 d3dCaps;

m_pD3DDevice->GetDeviceCaps( &d3dCaps );
if( 0 != (d3dCaps.VertexProcessingCaps & D3DVTXPCAPS_TWEENING) )
    // Vertex tweening is supported.
```



Para usar a interpolação de vetores, primeiro você deve configurar um tipo de vértice personalizado que usa uma segunda posição normal ou segunda. O exemplo de código a seguir mostra uma declaração de exemplo que inclui um segundo ponto e uma segunda posição.


```
struct TEX_VERTEX
{
    D3DVECTOR position;
    D3DVECTOR normal;
    D3DVECTOR position2;
    D3DVECTOR normal2;
};

//Create a vertex buffer with the type TEX_VERTEX.
```



A próxima etapa é definir a declaração atual. O exemplo de código a seguir mostra como fazer isso.


```
// Create the shader declaration.
D3DVERTEXELEMENT9 decl[] = 
{
    { 0, 0,  D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
    { 0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0 },
    { 0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 1 },
    { 0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 1 },
    D3DDECL_END()
};
```



Para obter mais informações sobre como criar um tipo de vértice personalizado e um buffer de vértice, consulte [criando um buffer de vértice (Direct3D 9)](creating-a-vertex-buffer.md).

> [!Note]  
> Quando a interpolação de vértices está habilitada, uma segunda posição ou um segundo normal deve estar presente na declaração atual.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interpolação de vértice](vertex-tweening.md)
</dt> </dl>

 

 
