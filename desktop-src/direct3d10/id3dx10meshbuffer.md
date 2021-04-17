---
description: Um buffer de malha é um buffer que contém dados sobre uma malha.
ms.assetid: a9fdfa22-531d-4da0-89f0-8766c2635e20
title: Interface ID3DX10MeshBuffer (D3DX10. h)
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
ms.openlocfilehash: 42076393c3be5443688ec4db954131935b62f696
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105752817"
---
# <a name="id3dx10meshbuffer-interface"></a>Interface ID3DX10MeshBuffer

Um buffer de malha é um buffer que contém dados sobre uma malha. Ele pode conter um dos cinco tipos diferentes de dados: dados de vértice, dados de índice, dados de adjacência, dados de atributo ou dados de representante de ponto. A estrutura é usada para acessar esses cinco tipos de dados por meio das cinco APIs a seguir: [**ID3DX10Mesh:: GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), [**ID3DX10Mesh:: GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), [**ID3DX10Mesh:: GetAdjacencyBuffer**](id3dx10mesh-getadjacencybuffer.md), [**ID3DX10Mesh:: GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md)ou [**ID3DX10Mesh:: GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md).

## <a name="members"></a>Membros

A interface **ID3DX10MeshBuffer** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10MeshBuffer** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX10MeshBuffer** tem esses métodos.



| Método                                       | Descrição                                                                |
|:---------------------------------------------|:---------------------------------------------------------------------------|
| [**GetSize**](id3dx10meshbuffer-getsize.md) | Obtenha o tamanho do buffer de malha, em bytes.<br/>                      |
| [**Mapeamento**](id3dx10meshbuffer-map.md)         | Obtenha um ponteiro para a memória do buffer de malha para modificar seu conteúdo.<br/> |
| [**Desmapear**](id3dx10meshbuffer-unmap.md)     | Cancelar o mapeamento de um buffer.<br/>                                                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
