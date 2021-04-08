---
description: Especifica a espessura da linha.
ms.assetid: cedf9217-2b47-40c3-a64c-9872c1083d71
title: 'Método ID3DXLine:: SetWidth (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetWidth
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d357d7516233caf6ef9206aa2aecc2a98a435cde
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012162"
---
# <a name="id3dxlinesetwidth-method"></a>Método ID3DXLine:: SetWidth

Especifica a espessura da linha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetWidth(
  [in] FLOAT fWidth
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fWidth* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Descreve a largura da linha.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
