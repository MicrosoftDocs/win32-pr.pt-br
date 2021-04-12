---
description: Obtém uma descrição técnica.
ms.assetid: 12122858-1e54-446c-8f12-20cc62499d74
title: 'Método ID3DXBaseEffect:: GetTechniqueDesc (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechniqueDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6027cf24576a29a1f447e5c20f99634c42adf00d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173181"
---
# <a name="id3dxbaseeffectgettechniquedesc-method"></a>Método ID3DXBaseEffect:: GetTechniqueDesc

Obtém uma descrição técnica.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTechniqueDesc(
  [in]  D3DXHANDLE         hTechnique,
  [out] D3DXTECHNIQUE_DESC *pDesc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hTechnique* \[ no\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Alça de técnica. Consulte [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pDesc* \[ fora\]
</dt> <dd>

Tipo: **[ **D3DXTECHNIQUE \_ desc**](d3dxtechnique-desc.md)\***

Retorna uma descrição da técnica. Consulte [**D3DXTECHNIQUE \_ desc**](d3dxtechnique-desc.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 




