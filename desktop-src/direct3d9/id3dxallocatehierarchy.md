---
description: Essa interface é implementada pelo aplicativo para alocar ou liberar objetos de contêiner de quadro e malha. Os métodos sobre isso são chamados durante o carregamento e destruição de hierarquias de quadros.
ms.assetid: b2c4ecb7-3655-4120-b957-724a754e948a
title: Interface ID3DXAllocateHierarchy (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ec7fb2da335ecd84889b75e81c850d16368f31eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012166"
---
# <a name="id3dxallocatehierarchy-interface"></a>Interface ID3DXAllocateHierarchy

Essa interface é implementada pelo aplicativo para alocar ou liberar objetos de contêiner de quadro e malha. Os métodos sobre isso são chamados durante o carregamento e destruição de hierarquias de quadros.

## <a name="members"></a>Membros

A interface **ID3DXAllocateHierarchy** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXAllocateHierarchy** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXAllocateHierarchy** tem esses métodos.



| Método                                                                       | Descrição                                                  |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------|
| [**CreateFrame**](id3dxallocatehierarchy--createframe.md)                   | Solicita a alocação de um objeto de quadro.<br/>            |
| [**CreateMeshContainer**](id3dxallocatehierarchy--createmeshcontainer.md)   | Solicita a alocação de um objeto de contêiner de malha.<br/>   |
| [**DestroyFrame**](id3dxallocatehierarchy--destroyframe.md)                 | Solicita a desalocação de um objeto de quadro.<br/>          |
| [**DestroyMeshContainer**](id3dxallocatehierarchy--destroymeshcontainer.md) | Solicita a desalocação de um objeto de contêiner de malha.<br/> |



 

## <a name="remarks"></a>Comentários

O tipo LPD3DXALLOCATEHIERARCHY é definido como um ponteiro para essa interface.


```
typedef interface ID3DXAllocateHierarchy ID3DXAllocateHierarchy;
typedef interface ID3DXAllocateHierarchy *LPD3DXALLOCATEHIERARCHY;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
