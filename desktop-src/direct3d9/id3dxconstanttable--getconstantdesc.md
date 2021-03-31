---
description: Obtém um ponteiro para uma matriz de descrições constantes na tabela de constantes.
ms.assetid: bd407fd6-b1cc-4197-ae98-1c2ca74d2ad0
title: 'Método ID3DXConstantTable:: GetConstantDesc (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5574c72fabd7561da0c60c903ae815faaebbfd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930616"
---
# <a name="id3dxconstanttablegetconstantdesc-method"></a>Método ID3DXConstantTable:: GetConstantDesc

Obtém um ponteiro para uma matriz de descrições constantes na tabela de constantes.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetConstantDesc(
  [in]      D3DXHANDLE        hConstant,
  [in, out] D3DXCONSTANT_DESC *pDesc,
  [in, out] UINT              *pCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hConstant* \[ no\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador exclusivo para uma constante. Consulte [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).

</dd> <dt>

*pDesc* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXCONSTANT \_ desc**](d3dxconstant-desc.md)\***

Retorna um ponteiro para uma matriz de descrições. Consulte [**D3DXCONSTANT \_ desc**](d3dxconstant-desc.md).

</dd> <dt>

*pCount* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

A entrada fornecida deve ser o tamanho máximo da matriz. A saída é o número de elementos que são preenchidos na matriz quando a função retorna.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentários

**ID3DXConstantTable:: GetConstantDesc** às vezes retornará um [**D3DXCONSTANT \_ desc**](d3dxconstant-desc.md) com uma \_ contagem de registro de 0. Isso ocorrerá com uma constante exibida em mais de um conjunto de registros \_ , mas não tem espaço no conjunto de registros alocado.

Como um amostra pode aparecer mais de uma vez em uma tabela constante, esse método pode retornar uma matriz de descrições, cada uma com um índice de registro diferente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> <dt>

[**ID3DXConstantTable:: GetDesc**](id3dxconstanttable--getdesc.md)
</dt> </dl>

 

 
