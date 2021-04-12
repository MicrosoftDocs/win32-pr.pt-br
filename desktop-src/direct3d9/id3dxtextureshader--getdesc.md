---
description: Obtém uma descrição da tabela de constantes.
ms.assetid: 91b537bb-5f7a-448b-a21f-c0ddf66d7238
title: 'Método ID3DXTextureShader:: GetDesc (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 97302b7e0f8c9f05e6229e20c2c9c158173ed944
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173028"
---
# <a name="id3dxtextureshadergetdesc-method"></a>Método ID3DXTextureShader:: GetDesc

Obtém uma descrição da tabela de constantes.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDesc(
  [in] D3DXCONSTANTTABLE_DESC *pDesc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDesc* \[ no\]
</dt> <dd>

Tipo: **[ **D3DXCONSTANTTABLE \_ desc**](d3dxconstanttable-desc.md)\***

Os atributos da tabela de constantes. Consulte [**D3DXCONSTANTTABLE \_ desc**](d3dxconstanttable-desc.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 




