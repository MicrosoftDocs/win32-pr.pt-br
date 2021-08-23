---
description: Inicia uma passagem, dentro da técnica ativa.
ms.assetid: fbb2bf1c-e37a-4117-8c3c-5f5b6a267301
title: 'Método ID3DXEffect:: BeginPass (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.BeginPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9013a67c2d4e0e9760167bc979ac05edd4879c5414ce5c9b9c55528baf3f6a18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987536"
---
# <a name="id3dxeffectbeginpass-method"></a>Método ID3DXEffect:: BeginPass

Inicia uma passagem, dentro da técnica ativa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT BeginPass(
  [in] UINT Pass
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Passar* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Um índice de inteiro baseado em zero na técnica.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentários

Um aplicativo define uma passagem ativa (dentro de uma técnica ativa) no sistema de efeitos chamando **ID3DXEffect:: BeginPass**. Um aplicativo sinaliza o final da passagem ativa chamando [**ID3DXEffect:: endpass**](id3dxeffect--endpass.md). **ID3DXEffect:: BeginPass** e **ID3DXEffect:: endpass** deve ocorrer em um par correspondente, dentro de um par correspondente de [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) e [**ID3DXEffect:: End**](id3dxeffect--end.md) calls.

Se o aplicativo alterar qualquer estado de efeito usando qualquer um dos métodos [**Effect:: setx**](id3dxeffect.md) dentro de um par **ID3DXEffect:: BeginPass** / [**ID3DXEffect:: endpass**](id3dxeffect--endpass.md) correspondente, o aplicativo deverá chamar [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) para definir a atualização do dispositivo com as alterações de estado. Se nenhuma alteração de estado ocorrer em um par **ID3DXEffect:: BeginPass** e **ID3DXEffect:: endpass** correspondente, não será necessário chamar **ID3DXEffect:: CommitChanges**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
