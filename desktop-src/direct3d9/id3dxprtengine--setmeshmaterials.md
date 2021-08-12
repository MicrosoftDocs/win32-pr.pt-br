---
description: Define as propriedades de material de malha na cena 3D. Use este método para especificar os parâmetros de dispersão de subsuperfície.
ms.assetid: 830d73be-bba6-454d-8476-341d291a5b2e
title: 'Método ID3DXPRTEngine:: SetMeshMaterials (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMeshMaterials
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7c24ff96b4582e86580774a1f7ac7cd889547018a5b0f138d5e43685c50e1701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293380"
---
# <a name="id3dxprtenginesetmeshmaterials-method"></a>Método ID3DXPRTEngine:: SetMeshMaterials

Define as propriedades de material de malha na cena 3D. Use este método para especificar os parâmetros de dispersão de subsuperfície.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMeshMaterials(
  [in] const D3DXSHMATERIAL **ppMaterials,
  [in]       UINT           NumMeshes,
  [in]       UINT           NumChannels,
  [in]       BOOL           bSetAlbedo,
  [in]       FLOAT          fLengthScale
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppMaterials* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXSHMATERIAL**](d3dxshmaterial.md) \* \***

Endereço de um ponteiro para as propriedades de material de malha desejadas. Consulte [**D3DXSHMATERIAL**](d3dxshmaterial.md).

</dd> <dt>

*NumMeshes* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice da malha na qual definir as propriedades do material.

</dd> <dt>

*NumChannels* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de canais de cores a serem definidos na malha. Defina como 1 para especificar os materiais em cinza (R = G = B) ou 3 para habilitar os efeitos de sangramento de cor. Se você pretende alterar esse parâmetro, primeiro defina o albedo usando outro método, como [**ID3DXPRTEngine:: SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md) ou [**ID3DXPRTEngine:: SetPerVertexAlbedo**](id3dxprtengine--setpervertexalbedo.md).

</dd> <dt>

*bSetAlbedo* \[ no\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Se **for true**, define o albedo da malha como ppMaterials, substituindo todos os valores existentes de albedo Texel e Vertex. Se **for false**, preservará todos os valores existentes de albedo Texel e Vertex definidos por outros métodos; NumChannels deve corresponder ao parâmetro NumChannels usado para criar o buffer em [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) ou [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md).

</dd> <dt>

*fLengthScale* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Escala da cena 3D em relação a um cubo de 1 mm. Usado para computações de dispersão de subsuperfície.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
