---
description: Iniciar a captura de alterações de estado em um bloco de parâmetro.
ms.assetid: cdf6f572-1a21-4c1d-a113-13b48bacd060
title: 'Método ID3DXEffect:: BeginParameterBlock (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.BeginParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b7345a045d152d5637b656bf4e9090b9645baf33645905e5e956737a1e6ede30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494276"
---
# <a name="id3dxeffectbeginparameterblock-method"></a>Método ID3DXEffect:: BeginParameterBlock

Iniciar a captura de alterações de estado em um bloco de parâmetro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT BeginParameterBlock();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentários

Capturar as alterações de estado do parâmetro de efeito até que EndParameterBlock seja chamado. Os parâmetros de efeito incluem qualquer alteração de estado fora de uma passagem. Exclua os blocos de parâmetro se eles não forem mais necessários chamando DeleteParameterBlock.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md)
</dt> <dt>

[**ID3DXEffect::ApplyParameterBlock**](id3dxeffect--applyparameterblock.md)
</dt> <dt>

[**ID3DXEffect::D eleteParameterBlock**](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




