---
description: Propagar alterações de estado que ocorrem dentro de uma passagem ativa para o dispositivo antes da renderização.
ms.assetid: 3a779b63-c106-4a81-afeb-82bd6e556de4
title: 'Método ID3DXEffect:: CommitChanges (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CommitChanges
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 41516c52b29dfe277cc857e44003de7783282a3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173033"
---
# <a name="id3dxeffectcommitchanges-method"></a>Método ID3DXEffect:: CommitChanges

Propagar alterações de estado que ocorrem dentro de uma passagem ativa para o dispositivo antes da renderização.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CommitChanges();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentários

Se o aplicativo alterar qualquer estado de efeito usando qualquer um dos métodos [**ID3DXEffect:: setx**](id3dxeffect.md) dentro de um par [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) / [**ID3DXEffect:: endpass**](id3dxeffect--endpass.md) correspondente, o aplicativo deverá chamar **ID3DXEffect:: CommitChanges** antes de qualquer chamada DrawxPrimitive para propagar as alterações de estado para o dispositivo antes da renderização. Se nenhuma alteração de estado ocorrer em um par **ID3DXEffect:: BeginPass** e **ID3DXEffect:: endpass** correspondente, não será necessário chamar **ID3DXEffect:: CommitChanges**.

Isso é um pouco diferente para quaisquer parâmetros compartilhados em um efeito clonado. Quando uma técnica está ativa em um efeito clonado (ou seja, quando [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) foi chamado, mas [**ID3DXEffect:: End**](id3dxeffect--end.md) não foi chamado), **ID3DXEffect:: CommitChanges** atualiza os parâmetros que não são compartilhados conforme o esperado. Para atualizar um parâmetro compartilhado (somente para um efeito clonado cuja técnica está ativa), chame **ID3DXEffect:: End** para desativar a técnica e **ID3DXEffect:: Begin** para reativar a técnica antes de chamar **ID3DXEffect:: CommitChanges**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




