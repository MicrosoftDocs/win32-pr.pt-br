---
description: Define uma chave de evento que altera a taxa de reprodução de uma faixa de animação.
ms.assetid: 217d3a2d-0fb7-4995-86ec-7a4e8420e338
title: Método ID3DXAnimationController::KeyTrackSpeed (D3dx9anim.h)
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
ms.openlocfilehash: 21ad7b0b1423a25ede319a623cad0a8b453af481d4aac5fae4e5bcce252dd31e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791186"
---
# <a name="id3dxanimationcontrollerkeytrackspeed-method"></a>Método ID3DXAnimationController::KeyTrackSpeed

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

*Acompanhar* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificador da faixa a ser modificado.

</dd> <dt>

*NewSpeed* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Nova velocidade da faixa de animação.

</dd> <dt>

*StartTime* \[ Em\]
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Chave de tempo global. Especifica a hora global em que a alteração ocorrerá.

</dd> <dt>

*Duração* \[ Em\]
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Tempo de transição, que especifica quanto tempo a transição suave levará para ser concluída.

</dd> <dt>

*Transição* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DXTRANSITION \_ TYPE**](./d3dxtransition-type.md)**

Especifica o tipo de transição usado para fazer a transição entre velocidades. Consulte [**D3DXTRANSITION \_ TYPE**](./d3dxtransition-type.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Alça de evento para o evento priority blend. **NULL** será retornado se um ou mais dos parâmetros de entrada for inválido ou se nenhum evento gratuito estiver disponível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
