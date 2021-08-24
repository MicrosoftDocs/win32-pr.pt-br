---
description: Define uma chave de evento que altera a hora local de uma faixa de animação.
ms.assetid: b527e960-8ab9-42a0-bb4d-bea5aaf83424
title: Método ID3DXAnimationController::KeyTrackPosition (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9e66bac7b5aaa8da87b0cb88e3bfd12469d8aa8b6ec755eaa47268c70da5eadf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791226"
---
# <a name="id3dxanimationcontrollerkeytrackposition-method"></a>Método ID3DXAnimationController::KeyTrackPosition

Define uma chave de evento que altera a hora local de uma faixa de animação.

## <a name="syntax"></a>Sintaxe


```C++
D3DXEVENTHANDLE KeyTrackPosition(
  [in] UINT   Track,
  [in] DOUBLE NewPosition,
  [in] DOUBLE StartTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Acompanhar* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificador da faixa a ser modificado.

</dd> <dt>

*NewPosition* \[ Em\]
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Nova hora local da faixa de animação.

</dd> <dt>

*StartTime* \[ Em\]
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Chave de tempo global. Especifica a hora global em que a alteração ocorrerá.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Alça de evento para o evento priority blend. **NULL** será retornado se Track for inválido ou se nenhum evento gratuito estiver disponível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
