---
description: Os aplicativos usam os métodos da interface ID3DXMesh para manipular objetos de malha.
ms.assetid: f571fe0b-3f0c-43c9-809c-d1e14f85b720
title: Interface ID3DXMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c2a677edba4bad5e908b6dd69aa21a467b2a245
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298792"
---
# <a name="id3dxmesh-interface"></a>Interface ID3DXMesh

Os aplicativos usam os métodos da interface ID3DXMesh para manipular objetos de malha.

## <a name="members"></a>Membros

A interface **ID3DXMesh** herda de [**ID3DXBaseMesh**](id3dxbasemesh.md). **ID3DXMesh** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXMesh** tem esses métodos.



| Método                                                            | Descrição                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md)     | Bloqueia o buffer de malha que contém os dados de atributo de malha e retorna um ponteiro para ele.<br/>                                   |
| [**Otimizar**](id3dxmesh--optimize.md)                           | Gera uma nova malha com faces e vértices reordenados para otimizar o desempenho do desenho.<br/>                                     |
| [**OptimizeInplace**](id3dxmesh--optimizeinplace.md)             | Gera uma malha com faces e vértices reordenados para otimizar o desempenho do desenho. Esse método reordena a malha existente.<br/> |
| [**SetAttributeTable**](id3dxmesh--setattributetable.md)         | Define a tabela de atributos para uma malha e o número de entradas armazenadas na tabela.<br/>                                          |
| [**UnlockAttributeBuffer**](id3dxmesh--unlockattributebuffer.md) | Desbloqueia um buffer de atributo.<br/>                                                                                                |



 

## <a name="remarks"></a>Comentários

Para obter a interface **ID3DXMesh** , chame a função [**D3DXCreateMesh**](d3dxcreatemesh.md) ou [**D3DXCreateMeshFVF**](d3dxcreatemeshfvf.md) .

Essa interface herda a funcionalidade adicional da interface [**ID3DXBaseMesh**](id3dxbasemesh.md) .

O tipo LPD3DXMESH é definido como um ponteiro para a interface **ID3DXMesh** .


```
typedef struct ID3DXMesh *LPD3DXMESH;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID3DXBaseMesh**](id3dxbasemesh.md)
</dt> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




