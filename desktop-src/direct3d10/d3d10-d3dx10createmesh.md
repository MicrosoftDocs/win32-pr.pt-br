---
description: Cria um objeto de malha usando um Declarador.
ms.assetid: 50e09378-2935-4b18-8fc9-5e58eaadae44
title: Função D3DX10CreateMesh (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateMesh
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2b00addb152fe18db448364fcc784c2044b10d23
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105811091"
---
# <a name="d3dx10createmesh-function"></a>Função D3DX10CreateMesh

Cria um objeto de malha usando um Declarador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10CreateMesh(
  _In_        ID3D10Device             *pDevice,
  _In_  const D3D10_INPUT_ELEMENT_DESC *pDeclaration,
  _In_        UINT                     DeclCount,
  _In_        LPCSTR                   pPositionSemantic,
  _In_        UINT                     VertexCount,
  _In_        UINT                     FaceCount,
  _In_        UINT                     Options,
  _Out_       ID3DX10Mesh              **ppMesh
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Ponteiro para uma [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device), o objeto de dispositivo a ser associado à malha.

</dd> <dt>

*pDeclaration* \[ no\]
</dt> <dd>

Tipo: **const [**d3d10 \_ de \_ elemento \_ de entrada desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***

Matriz de [**elementos \_ \_ \_ desc de elemento de entrada d3d10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) , que descreve o formato de vértice para a malha retornada. Esse parâmetro deve ser mapeado diretamente para um formato de vértice flexível (FVF).

</dd> <dt>

*DeclCount* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O número de elementos em pDeclaration.

</dd> <dt>

*pPositionSemantic* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Semântica que identifica qual parte da declaração de vértice contém informações de posição.

</dd> <dt>

*Contagemdevértice* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de vértices para a malha. Esse parâmetro deve ser maior que 0.

</dd> <dt>

*FaceCount* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de faces para a malha. O intervalo válido para esse número é maior que 0 e um menor que o DWORD (normalmente 65534), pois o último índice é reservado.

</dd> <dt>

*Opções* \[ do no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Combinação de um ou mais sinalizadores da [**\_ malha D3DX10**](d3dx10-mesh.md), especificando as opções para a malha.

</dd> <dt>

*ppMesh* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***

Endereço de um ponteiro para uma [**interface ID3DX10Mesh**](id3dx10mesh.md), que representa o objeto de malha criado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[Funções D3DX](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 
