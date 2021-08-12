---
description: Um buffer de malha é um buffer que contém dados sobre uma malha.
ms.assetid: a9fdfa22-531d-4da0-89f0-8766c2635e20
title: Interface ID3DX10MeshBuffer (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a2aeabcd6dd3cc711636d0e275f76ab48537953671559e244cf341e270783fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540150"
---
# <a name="id3dx10meshbuffer-interface"></a>Interface ID3DX10MeshBuffer

Um buffer de malha é um buffer que contém dados sobre uma malha. Ele pode conter um dos cinco tipos diferentes de dados: dados de vértice, dados de índice, dados de adjacency, dados de atributo ou dados de representante de ponto. A estrutura é usada para acessar essas cinco partes de dados por meio das seguintes cinco APIs: [**ID3DX10Mesh::GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), [**ID3DX10Mesh::GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), [**ID3DX10Mesh::GetAdjacencyBuffer**](id3dx10mesh-getadjacencybuffer.md), [**ID3DX10Mesh::GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md)ou [**ID3DX10Mesh::GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md).

## <a name="members"></a>Membros

A interface **ID3DX10MeshBuffer** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10MeshBuffer** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX10MeshBuffer** tem esses métodos.



| Método                                       | Descrição                                                                |
|:---------------------------------------------|:---------------------------------------------------------------------------|
| [**Getsize**](id3dx10meshbuffer-getsize.md) | Obter o tamanho do buffer de malha, em bytes.<br/>                      |
| [**Map**](id3dx10meshbuffer-map.md)         | Obter um ponteiro para a memória do buffer de malha para modificar seu conteúdo.<br/> |
| [**Desmapear**](id3dx10meshbuffer-unmap.md)     | Desmmape um buffer.<br/>                                                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
