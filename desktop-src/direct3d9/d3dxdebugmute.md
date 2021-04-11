---
description: Ativa ou desativa a saída de depuração de D3DX.
ms.assetid: e35cbfd2-401e-47ec-9f5b-e2ed63ea1fcd
title: Função D3DXDebugMute (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDebugMute
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9259fa43a6a64829e42cbaa661aa7223a958f22d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173007"
---
# <a name="d3dxdebugmute-function"></a>Função D3DXDebugMute

Ativa ou desativa a saída de depuração de D3DX.

## <a name="syntax"></a>Sintaxe


```C++
BOOL D3DXDebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Sem áudio* \[ no\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Se **for true**, a saída do depurador será interrompida; Se for **false**, a saída de depuração será habilitada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Retorna o valor anterior de mudo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de Uso Geral](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
