---
description: Solicita a desalocação de um objeto de contêiner de malha.
ms.assetid: 7a976ba8-6972-4857-b0a9-4ea7a88dc8ac
title: Método ID3DXAllocateHierarchy::D mentoyMeshContainer (D3dx9fastm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.DestroyMeshContainer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8c24b4dee9490c55644ceab4670cda1109dcc4e1cfde65c661bbe9b3fbc64f01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094605"
---
# <a name="id3dxallocatehierarchydestroymeshcontainer-method"></a>Método ID3DXAllocateHierarchy::D yMeshContainer

Solicita a desalocação de um objeto de contêiner de malha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DestroyMeshContainer(
  [in] LPD3DXMESHCONTAINER pMeshContainerToFree
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMeshContainerToFree* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**

Ponteiro para o objeto de contêiner de malha a ser desaloqueado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Os valores de retorno desse método são implementados por um programador de aplicativos. Em geral, se nenhum erro ocorrer, programe o método para retornar D3D \_ OK. Caso contrário, programe o método para retornar uma mensagem de erro apropriada de D3DERR ou D3DXERR, pois isso fará com que [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) falhe também e retorne o erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAllocateHierarchy](id3dxallocatehierarchy.md)
</dt> </dl>

 

 




