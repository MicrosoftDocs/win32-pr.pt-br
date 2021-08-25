---
description: Essa interface encapsula a funcionalidade de malha de patch.
ms.assetid: c70c0fe0-b695-4ad9-b0c6-7854cf8f7593
title: Interface ID3DXPatchMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44899ccee6f13aa25b01e284df5a892196d657610c3f89d546fc0b646eeaa069
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856276"
---
# <a name="id3dxpatchmesh-interface"></a>Interface ID3DXPatchMesh

Essa interface encapsula a funcionalidade de malha de patch.

## <a name="members"></a>Membros

A interface **ID3DXPatchMesh** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXPatchMesh** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXPatchMesh** tem esses métodos.



| Método                                                                           | Descrição                                                                                     |
|:---------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**CloneMesh**](id3dxpatchmesh--clonemesh.md)                                   | Cria uma nova malha de patch com a declaração de vértice especificada.<br/>                      |
| [**GenerateAdjacency**](id3dxpatchmesh--generateadjacency.md)                   | Gere uma lista de bordas de malha e os patches que compartilham cada borda.<br/>                  |
| [**GetControlVerticesPerPatch**](id3dxpatchmesh--getcontrolverticesperpatch.md) | Obtém o número de vértices de controle por patch.<br/>                                       |
| [**Getdeclaration**](id3dxpatchmesh--getdeclaration.md)                         | Obtém a declaração de vértice.<br/>                                                         |
| [**GetDevice**](id3dxpatchmesh--getdevice.md)                                   | Obtém o dispositivo que criou a malha.<br/>                                               |
| [**GetDisplaceParam**](id3dxpatchmesh--getdisplaceparam.md)                     | Obtém os parâmetros de deslocamento da geometria de malha.<br/>                                          |
| [**GetIndexBuffer**](id3dxpatchmesh--getindexbuffer.md)                         | Obtém o buffer do índice de malha.<br/>                                                          |
| [**GetNumPatches**](id3dxpatchmesh--getnumpatches.md)                           | Obtém o número de patches na malha.<br/>                                              |
| [**GetNumVertices**](id3dxpatchmesh--getnumvertices.md)                         | Obtém o número de vértices na malha.<br/>                                             |
| [**Getoptions**](id3dxpatchmesh--getoptions.md)                                 | Obtém o tipo de patch.<br/>                                                              |
| [**GetPatchInfo**](id3dxpatchmesh--getpatchinfo.md)                             | Obtém os atributos do patch.<br/>                                                    |
| [**GetTessSize**](id3dxpatchmesh--gettesssize.md)                               | Obtém o tamanho da malha mosaico, dado um nível de mosaico.<br/>                   |
| [**GetVertexBuffer**](id3dxpatchmesh--getvertexbuffer.md)                       | Obtém o buffer de vértice de malha.<br/>                                                         |
| [**LockAttributeBuffer**](id3dxpatchmesh--lockattributebuffer.md)               | Bloqueia o buffer de atributo.<br/>                                                          |
| [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md)                       | Bloquear o buffer de índice.<br/>                                                               |
| [**LockVertexBuffer**](id3dxpatchmesh--lockvertexbuffer.md)                     | Bloquear o buffer de vértice.<br/>                                                              |
| [**Otimizar**](id3dxpatchmesh--optimize.md)                                     | Otimiza a malha de patches para mosaico eficiente.<br/>                                 |
| [**SetDisplaceParam**](id3dxpatchmesh--setdisplaceparam.md)                     | Define os parâmetros de deslocamento de geometria de malha.<br/>                                          |
| [**Incluí**](id3dxpatchmesh--tessellate.md)                                 | Executa mosaico uniforme com base no nível de mosaico.<br/>                       |
| [**TessellateAdaptive**](id3dxpatchmesh--tessellateadaptive.md)                 | Executa mosaico adaptável com base no critério de mosaico adaptável baseado em z.<br/> |
| [**UnlockAttributeBuffer**](id3dxpatchmesh--unlockattributebuffer.md)           | Desbloqueie o buffer de atributo.<br/>                                                         |
| [**UnlockIndexBuffer**](id3dxpatchmesh--unlockindexbuffer.md)                   | Desbloqueie o buffer de índice.<br/>                                                             |
| [**UnlockVertexBuffer**](id3dxpatchmesh--unlockvertexbuffer.md)                 | Desbloqueie o buffer de vértice.<br/>                                                            |



 

## <a name="remarks"></a>Comentários

Uma malha de patch é uma malha que consiste em uma série de patches.

Para obter a interface **ID3DXPatchMesh** , chame a função [**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md) .

O tipo LPD3DXPATCHMESH é definido como um ponteiro para a interface **ID3DXPatchMesh** , da seguinte maneira:


```
typedef struct ID3DXPatchMesh *LPD3DXPATCHMESH;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
