---
description: Os aplicativos usam os métodos da interface ID3DXBaseMesh para manipular e consultar malha e objetos de malha progressiva.
ms.assetid: ec4ccd77-e370-470c-9325-3d794a8f7f16
title: Interface ID3DXBaseMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 58029639852b30f5de357bb2643583615c45485c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298655"
---
# <a name="id3dxbasemesh-interface"></a>Interface ID3DXBaseMesh

Os aplicativos usam os métodos da interface **ID3DXBaseMesh** para manipular e consultar malha e objetos de malha progressiva.

## <a name="members"></a>Membros

A interface **ID3DXBaseMesh** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXBaseMesh** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXBaseMesh** tem esses métodos.



| Método                                                                            | Descrição                                                                                                                                                                                                           |
|:----------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CloneMesh**](id3dxbasemesh--clonemesh.md)                                     | Clona uma malha usando um Declarador.<br/>                                                                                                                                                                          |
| [**CloneMeshFVF**](id3dxbasemesh--clonemeshfvf.md)                               | Clona uma malha usando um código de formato de vértice flexível (FVF).<br/>                                                                                                                                                   |
| [**ConvertAdjacencyToPointReps**](id3dxbasemesh--convertadjacencytopointreps.md) | Converte informações de adjacência de malha em uma matriz de representantes de ponto.<br/>                                                                                                                                  |
| [**ConvertPointRepsToAdjacency**](id3dxbasemesh--convertpointrepstoadjacency.md) | Converte dados representativos de ponto em informações de adjacência de malha.<br/>                                                                                                                                          |
| [**DrawSubset**](id3dxbasemesh--drawsubset.md)                                   | Desenha um subconjunto de uma malha.<br/>                                                                                                                                                                                  |
| [**GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)                     | Gere uma lista de bordas de malha, bem como uma lista de faces que compartilham cada borda.<br/>                                                                                                                            |
| [**Getattributetable**](id3dxbasemesh--getattributetable.md)                     | Recupera uma tabela de atributos para uma malha ou o número de entradas armazenadas em uma tabela de atributos para uma malha.<br/>                                                                                          |
| [**Getdeclaration**](id3dxbasemesh--getdeclaration.md)                           | Recupera uma declaração que descreve os vértices na malha.<br/>                                                                                                                                               |
| [**GetDevice**](id3dxbasemesh--getdevice.md)                                     | Recupera o dispositivo associado à malha.<br/>                                                                                                                                                             |
| [**GetFVF**](id3dxbasemesh--getfvf.md)                                           | Obtém o valor de vértice da função fixa.<br/>                                                                                                                                                                      |
| [**GetIndexBuffer**](id3dxbasemesh--getindexbuffer.md)                           | Recupera os dados em um buffer de índice.<br/>                                                                                                                                                                     |
| [**GetNumBytesPerVertex**](id3dxbasemesh--getnumbytespervertex.md)               | Obtém o número de bytes por vértice.<br/>                                                                                                                                                                       |
| [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)                                 | Recupera o número de faces na malha.<br/>                                                                                                                                                                 |
| [**GetNumVertices**](id3dxbasemesh--getnumvertices.md)                           | Recupera o número de vértices na malha.<br/>                                                                                                                                                              |
| [**Getoptions**](id3dxbasemesh--getoptions.md)                                   | Recupera as opções de malha habilitadas para esta malha no momento da criação.<br/>                                                                                                                                         |
| [**GetVertexBuffer**](id3dxbasemesh--getvertexbuffer.md)                         | Recupera o buffer de vértice associado à malha.<br/>                                                                                                                                                      |
| [**LockIndexBuffer**](id3dxbasemesh--lockindexbuffer.md)                         | Bloqueia um buffer de índice e Obtém um ponteiro para a memória do buffer de índice.<br/>                                                                                                                                    |
| [**LockVertexBuffer**](id3dxbasemesh--lockvertexbuffer.md)                       | Bloqueia um buffer de vértice e Obtém um ponteiro para a memória de buffer de vértice.<br/>                                                                                                                                   |
| [**UnlockIndexBuffer**](id3dxbasemesh--unlockindexbuffer.md)                     | Desbloqueia um buffer de índice.<br/>                                                                                                                                                                                   |
| [**UnlockVertexBuffer**](id3dxbasemesh--unlockvertexbuffer.md)                   | Desbloqueia um buffer de vértice.<br/>                                                                                                                                                                                   |
| [**UpdateSemantics**](id3dxbasemesh--updatesemantics.md)                         | Esse método permite que o usuário altere a declaração de malha sem alterar o layout de dados do buffer de vértice. A chamada será válida somente se os formatos de declaração antigo e novo tiverem o mesmo tamanho de vértice.<br/> |



 

## <a name="remarks"></a>Comentários

Uma malha é um objeto composto por um conjunto de rostos Polygons. Uma malha define um conjunto de vértices e um conjunto de faces (as faces são definidas em termos de vértices e normais da malha).

O tipo LPD3DXBASEMESH é definido como um ponteiro para a interface **ID3DXBaseMesh** .


```
typedef struct ID3DXBaseMesh *LPD3DXBASEMESH;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
