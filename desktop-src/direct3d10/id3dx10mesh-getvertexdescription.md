---
description: Acesse a descrição do vértice passada para D3DX10CreateMesh. A descrição do vértice descreve o layout dos buffers de vértice da malha.
ms.assetid: e4a4a98a-e131-414c-ad98-21288ff0c61b
title: 'Método ID3DX10Mesh:: GetVertexDescription (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexDescription
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5857b5162cf351a235d9cbecd2e457030820485d37e9aa49062a63b196f95900
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540222"
---
# <a name="id3dx10meshgetvertexdescription-method"></a>Método ID3DX10Mesh:: GetVertexDescription

Acesse a descrição do vértice passada para [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md). A descrição do vértice descreve o layout dos buffers de vértice da malha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetVertexDescription(
  [out] const D3D10_INPUT_ELEMENT_DESC **ppDesc,
  [in]        UINT                     *pDeclCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppDesc* \[ fora\]
</dt> <dd>

Tipo: **const [**d3d10 \_ de \_ elemento \_ de entrada desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \* \***

Matriz de elementos de entrada que descrevem o layout dos buffers de vértice da malha. Consulte [**o \_ elemento de entrada d3d10 \_ \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).

</dd> <dt>

*pDeclCount* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

O número de elementos de entrada em ppDesc.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

 

 
