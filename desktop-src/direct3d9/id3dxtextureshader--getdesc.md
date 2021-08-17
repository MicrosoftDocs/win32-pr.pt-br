---
description: 'Método ID3DXTextureShader:: GetDesc – Obtém uma descrição da tabela de constantes.'
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
ms.openlocfilehash: 06619730ceaa03dfdc812c669726bcde032caf7380ce4a7736085ee3a62b9d4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729019"
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

## <a name="return-value"></a>Valor retornado

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

 

 




