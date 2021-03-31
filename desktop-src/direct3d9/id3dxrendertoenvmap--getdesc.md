---
description: Recupera a descrição da superfície de renderização.
ms.assetid: 3c2612fa-540d-4d7a-9821-bf37fa3b6da4
title: 'Método ID3DXRenderToEnvMap:: GetDesc (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d0b9faf5bdd4c57f7320749aef2010f457dd682e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103663988"
---
# <a name="id3dxrendertoenvmapgetdesc-method"></a>Método ID3DXRenderToEnvMap:: GetDesc

Recupera a descrição da superfície de renderização.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDesc(
  [out] D3DXRTE_DESC *pDesc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDesc* \[ fora\]
</dt> <dd>

Tipo: **[ **D3DXRTE \_ desc**](d3dxrte-desc.md)\***

Ponteiro para uma [**estrutura \_ desc de D3DXRTE**](d3dxrte-desc.md) que descreve a superfície de renderização.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 




