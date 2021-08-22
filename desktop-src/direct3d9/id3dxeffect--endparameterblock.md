---
description: Parar a captura de alterações de estado de parâmetro de efeito.
ms.assetid: b6ca2917-2df0-4f3a-9ee3-23e9d2501ff4
title: 'Método ID3DXEffect:: EndParameterBlock (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.EndParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b1d68aa1bd716ee106a5d1588a7a7060adb851185115e97d2f5f2a5d7f857c02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494226"
---
# <a name="id3dxeffectendparameterblock-method"></a>Método ID3DXEffect:: EndParameterBlock

Parar a captura de alterações de estado de parâmetro de efeito.

## <a name="syntax"></a>Sintaxe


```C++
D3DXHANDLE EndParameterBlock();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Retorna um identificador para o bloco de estado do parâmetro.

## <a name="remarks"></a>Comentários

Todos os parâmetros de efeito que alteram o estado (depois de chamar BeginParameterBlock e antes de chamar EndParameterBlock) serão salvos em um bloco de estado de parâmetro de efeito. Use ApplyParameterBlock para aplicar esse bloco de alterações de estado ao sistema de efeitos. Quando você terminar com um bloco de estado, use DeleteParameterBlock para liberar a memória.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect::BeginParameterBlock**](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[**ID3DXEffect::ApplyParameterBlock**](id3dxeffect--applyparameterblock.md)
</dt> <dt>

[**ID3DXEffect::D eleteParameterBlock**](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




