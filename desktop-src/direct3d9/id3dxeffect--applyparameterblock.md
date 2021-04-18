---
description: Aplique os valores em um bloco de estado ao estado atual do sistema de efeito.
ms.assetid: f228e2a2-64fa-4354-9f49-42d1d3b12d50
title: 'Método ID3DXEffect:: ApplyParameterBlock (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.ApplyParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 12af672b929822180c4dba681ca333692a9174ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105785289"
---
# <a name="id3dxeffectapplyparameterblock-method"></a>Método ID3DXEffect:: ApplyParameterBlock

Aplique os valores em um bloco de estado ao estado atual do sistema de efeito.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ApplyParameterBlock(
  [in] D3DXHANDLE  hParameterBlock
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

 *hParameterBlock* \[ no\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Um identificador para o bloco de parâmetro. Esse é o identificador retornado por [**ID3DXEffect:: EndParameterBlock**](id3dxeffect--endparameterblock.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentários

Capturar alterações de estado de parâmetro de efeito em um bloco de parâmetro chamando BeginParameterBlock; Pare a captura de alterações de estado chamando EndParameterBlock. Essas alterações de estado incluem qualquer alteração de parâmetro de efeito que ocorra dentro de uma técnica (incluindo aquelas fora de uma passagem). Depois de concluir o bloco de parâmetro, chame DeleteParameterBlock para recuperar a memória.

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

[**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md)
</dt> <dt>

[**ID3DXEffect::D eleteParameterBlock**](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




