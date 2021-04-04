---
description: Obtém uma descrição da tabela de constantes.
ms.assetid: 3a7396c6-3a3e-44c2-96b7-60339015b376
title: 'Método ID3DXConstantTable:: GetDesc (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71eeb951ec73fbeb9942f52e30ab9ad59e374ee7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837939"
---
# <a name="id3dxconstanttablegetdesc-method"></a>Método ID3DXConstantTable:: GetDesc

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

Descrição da tabela de constantes. Consulte [**D3DXCONSTANTTABLE \_ desc**](d3dxconstanttable-desc.md).

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

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> <dt>

[**ID3DXConstantTable::GetConstantDesc**](id3dxconstanttable--getconstantdesc.md)
</dt> </dl>

 

 




