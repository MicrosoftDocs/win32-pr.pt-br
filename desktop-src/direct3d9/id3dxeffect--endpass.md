---
description: Encerrar uma passagem ativa.
ms.assetid: e20b3e0f-db9f-48e8-ab4e-761a5861f3ce
title: 'Método ID3DXEffect:: endpass (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.EndPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5cdba799f282e56bbe4565a4792906fd835e5c6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298651"
---
# <a name="id3dxeffectendpass-method"></a>Método ID3DXEffect:: endpass

Encerrar uma passagem ativa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EndPass();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Esse método sempre retorna o valor S \_ OK.

## <a name="remarks"></a>Comentários

Um aplicativo sinaliza o fim de renderizar uma passagem ativa chamando **ID3DXEffect:: endpass**. Cada **ID3DXEffect:: endpass** deve fazer parte de um par correspondente de chamadas [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) e **ID3DXEffect:: endpass** .

Cada par correspondente de chamadas [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) e **ID3DXEffect:: endpass** deve estar localizado em um par correspondente de [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) e [**ID3DXEffect:: End**](id3dxeffect--end.md) calls.

Se o aplicativo alterar qualquer estado de efeito usando qualquer um dos métodos [**Effect:: setx**](id3dxeffect.md) dentro de um par [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) / **ID3DXEffect:: endpass** correspondente, o aplicativo deverá chamar [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) antes de qualquer chamada DrawxPrimitive para propagar as alterações de estado para o dispositivo antes da renderização.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




