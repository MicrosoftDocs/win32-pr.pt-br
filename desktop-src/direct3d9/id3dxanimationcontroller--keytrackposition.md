---
description: Define uma chave de evento que altera a hora local de uma faixa de animação.
ms.assetid: b527e960-8ab9-42a0-bb4d-bea5aaf83424
title: 'Método ID3DXAnimationController:: KeyTrackPosition (D3dx9anim. h)'
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
ms.openlocfilehash: d027069efa9fb49cad3d2344da593eae4c3c844c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298751"
---
# <a name="id3dxanimationcontrollerkeytrackposition-method"></a>Método ID3DXAnimationController:: KeyTrackPosition

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

*Acompanhar* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificador da faixa a ser modificada.

</dd> <dt>

*NewPosition* \[ no\]
</dt> <dd>

Tipo: **[ **duplo**](../winprog/windows-data-types.md)**

Nova hora local da faixa de animação.

</dd> <dt>

*StartTime* \[ no\]
</dt> <dd>

Tipo: **[ **duplo**](../winprog/windows-data-types.md)**

Chave de tempo global. Especifica a hora global em que a alteração ocorrerá.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento para o evento de mesclagem de prioridade. **NULL** será retornado se Track for inválido ou se nenhum evento gratuito estiver disponível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
