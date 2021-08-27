---
description: Remova um pau.
ms.assetid: efb88108-5c76-47c8-b8ce-1ba29cb18ba4
title: Método ID3DX10SkinInfo::RemoveBone (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemoveBone
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8f26a19c0903056c6de62ae72852b19557b0926fe5b2616adfa8d77bd945cba4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119936"
---
# <a name="id3dx10skininforemovebone-method"></a>Método ID3DX10SkinInfo::RemoveBone

Remova um pau.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RemoveBone(
  [in] UINT Index
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Índice* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Um índice que especifica qual valor deve ser removido. Deve estar entre 0 e o valor retornado por [**ID3DX10SkinInfo::GetNumBones.**](id3dx10skininfo-getnumbones.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser: E \_ INVALIDARG.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
