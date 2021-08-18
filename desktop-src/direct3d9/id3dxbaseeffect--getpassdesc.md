---
description: Obtém uma descrição de passagem.
ms.assetid: 44c65a82-bcf4-49f5-9312-8320e133bb2f
title: 'Método ID3DXBaseEffect:: GetPassDesc (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 74106bc38367e13cd70af94d0ad12016165aaae24693f19386e69ebe1d7a5cb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987746"
---
# <a name="id3dxbaseeffectgetpassdesc-method"></a>Método ID3DXBaseEffect:: GetPassDesc

Obtém uma descrição de passagem.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetPassDesc(
  [in]  D3DXHANDLE    hPass,
  [out] D3DXPASS_DESC *pDesc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPass* \[ no\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Ponteiro de passagem. Consulte [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pDesc* \[ fora\]
</dt> <dd>

Tipo: **[ **D3DXPASS \_ desc**](d3dxpass-desc.md)\***

Retorna uma descrição da passagem especificada. Consulte [**D3DXPASS \_ desc**](d3dxpass-desc.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

> [!Note]  
> Se um efeito for criado com [D3DXFX \_ não \_ clonável](d3dxfx.md), esse método retornará ponteiros **nulos** (em [**D3DXPASS \_ desc**](d3dxpass-desc.md)) para as funções de sombreador.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 




