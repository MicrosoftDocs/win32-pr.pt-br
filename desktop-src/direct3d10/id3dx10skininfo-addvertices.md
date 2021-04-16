---
description: Aloque espaço para vértices adicionais.
ms.assetid: dd6445ea-4754-4ba3-a264-59295325ee08
title: 'Método ID3DX10SkinInfo:: addvértices (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddVertices
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8f126b31c375e4e3463133960c5a1bcfbd995b62
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105750185"
---
# <a name="id3dx10skininfoaddvertices-method"></a>Método ID3DX10SkinInfo:: addvértices

Aloque espaço para vértices adicionais.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddVertices(
  [in] UINT Count
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Contagem* \[ de no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O número de vértices a serem adicionados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se esse método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser: E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
