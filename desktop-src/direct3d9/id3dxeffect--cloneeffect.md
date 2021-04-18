---
description: Cria uma cópia de um efeito.
ms.assetid: 6272bce0-b712-4a61-afe2-8f572993b03e
title: 'Método ID3DXEffect:: CloneEffect (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CloneEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: eba2f6248bd1373ebf0aae55cf94103e2c269be7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771441"
---
# <a name="id3dxeffectcloneeffect-method"></a>Método ID3DXEffect:: CloneEffect

Cria uma cópia de um efeito.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CloneEffect(
  [in]  LPDIRECT3DDEVICE9 pDevice,
  [out] LPD3DXEFFECT      *ppEffect
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado ao efeito.

</dd> <dt>

*ppEffect* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***

Ponteiro para uma interface [**ID3DXEffect**](id3dxeffect.md) , que contém o efeito clonado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa função não clonará um efeito se o usuário especificar [D3DXFX \_ não \_ clonável](d3dxfx.md) durante a criação do efeito.

 

Para atualizar parâmetros compartilhados e não compartilhados em uma técnica ativa de um efeito clonado, consulte [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
