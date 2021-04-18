---
description: Define uma chave de evento que altera a taxa de reprodução de uma faixa de animação.
ms.assetid: 217d3a2d-0fb7-4995-86ec-7a4e8420e338
title: 'Método ID3DXAnimationController:: KeyTrackSpeed (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackSpeed
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 09705dd03e7767e94b1508cf4951186a509a3c5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105814133"
---
# <a name="id3dxanimationcontrollerkeytrackspeed-method"></a>Método ID3DXAnimationController:: KeyTrackSpeed

Define uma chave de evento que altera a taxa de reprodução de uma faixa de animação.

## <a name="syntax"></a>Sintaxe


```C++
D3DXEVENTHANDLE KeyTrackSpeed(
  [in] UINT                Track,
  [in] FLOAT               NewSpeed,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Acompanhar* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificador da faixa a ser modificada.

</dd> <dt>

*NewSpeed* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Nova velocidade da faixa de animação.

</dd> <dt>

*StartTime* \[ no\]
</dt> <dd>

Tipo: **[ **duplo**](../winprog/windows-data-types.md)**

Chave de tempo global. Especifica a hora global em que a alteração ocorrerá.

</dd> <dt>

*Duração* \[ no\]
</dt> <dd>

Tipo: **[ **duplo**](../winprog/windows-data-types.md)**

Tempo de transição, que especifica por quanto tempo a transição suave levará para ser concluída.

</dd> <dt>

*Transição* \[ no\]
</dt> <dd>

Tipo: **[ **\_ tipo de D3DXTRANSITION**](./d3dxtransition-type.md)**

Especifica o tipo de transição usado para fazer a transição entre velocidades. Consulte [**\_ tipo de D3DXTRANSITION**](./d3dxtransition-type.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento para o evento de mesclagem de prioridade. **NULL** será retornado se um ou mais dos parâmetros de entrada forem inválidos ou se nenhum evento gratuito estiver disponível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
