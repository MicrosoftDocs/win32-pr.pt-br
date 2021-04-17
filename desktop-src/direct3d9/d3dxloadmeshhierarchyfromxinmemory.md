---
description: Carrega a primeira hierarquia de quadros de um arquivo. x.
ms.assetid: 428e5cfb-d6a5-4a7f-b082-2d8898e65490
title: Função D3DXLoadMeshHierarchyFromXInMemory (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromXInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 91cf119fc8907701f87ebb5bda1bb0bf45294aba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791558"
---
# <a name="d3dxloadmeshhierarchyfromxinmemory-function"></a>Função D3DXLoadMeshHierarchyFromXInMemory

Carrega a primeira hierarquia de quadros de um arquivo. x.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXLoadMeshHierarchyFromXInMemory(
  _In_  LPCVOID                   pMemory,
  _In_  DWORD                     SizeOfMemory,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHeirarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMemory* \[ no\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Ponteiro para um buffer que contém a hierarquia de malha.

</dd> <dt>

*SizeOfMemory* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Tamanho do buffer pMemory, em bytes.

</dd> <dt>

*Malhas* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de um ou mais sinalizadores da enumeração [**D3DXMESH**](./d3dxmesh.md) que especificam as opções de criação para a malha.

</dd> <dt>

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , o objeto de dispositivo associado à malha.

</dd> <dt>

*pAlloc* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**

Ponteiro para uma interface [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) .

</dd> <dt>

*pUserDataLoader* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**

Interface fornecida pelo aplicativo que permite o carregamento de dados do usuário. Consulte [**ID3DXLoadUserData**](id3dxloaduserdata.md).

</dd> <dt>

*ppFrameHeirarchy* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)\***

Retorna um ponteiro para a hierarquia de quadro carregada. Consulte [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*ppAnimController* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

Retorna um ponteiro para o controlador de animação correspondente à animação no arquivo. x. Isso é criado com rastreamentos e eventos padrão. Consulte [**ID3DXAnimationController**](id3dxanimationcontroller.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Todas as malhas no arquivo serão recolhidas em uma malha de saída. Se o arquivo contiver uma hierarquia de quadros, todas as transformações serão aplicadas à malha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de animação](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
