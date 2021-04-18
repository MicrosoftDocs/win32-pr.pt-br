---
description: Cria uma nova malha e a preenche com os dados de uma malha carregada anteriormente.
ms.assetid: 2ce39982-abc0-444b-bc6f-24508f76fe31
title: 'Método ID3DX10Mesh:: CloneMesh (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CloneMesh
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0f007475ea9f6aeaa6dc0c01bbd721c4a5103adf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791611"
---
# <a name="id3dx10meshclonemesh-method"></a>Método ID3DX10Mesh:: CloneMesh

Cria uma nova malha e a preenche com os dados de uma malha carregada anteriormente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CloneMesh(
  [in]        UINT                     Flags,
  [in]        LPCSTR                   pPosSemantic,
  [in]  const D3D10_INPUT_ELEMENT_DESC *pDesc,
  [in]        UINT                     DeclCount,
  [out]       ID3DX10Mesh              **ppCloneMesh
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Sinalizadores de criação a serem aplicados à nova malha. Consulte [**\_ malha D3DX10**](d3dx10-mesh.md).

</dd> <dt>

*pPosSemantic* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

O nome semântico dos dados da posição.

</dd> <dt>

*pDesc* \[ no\]
</dt> <dd>

Tipo: **const [**d3d10 \_ de \_ elemento \_ de entrada desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***

Matriz de \_ estruturas desc de elemento de entrada d3d10 \_ \_ , que descreve o formato de vértice para a malha retornada. Consulte [**o \_ elemento de entrada d3d10 \_ \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).

</dd> <dt>

*DeclCount* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O número de elementos na matriz pDesc.

</dd> <dt>

*ppCloneMesh* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***

A nova malha.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
