---
description: Liga ou desliga toda a saída de depuração D3DX.
ms.assetid: e35cbfd2-401e-47ec-9f5b-e2ed63ea1fcd
title: Função D3DXDebugMute (D3dx9core.h)
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
ms.openlocfilehash: c2bde5446e6e41568c1f9d6aa8408dacc276ab82112a176cf8a038536dd4d992
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045074"
---
# <a name="d3dxdebugmute-function"></a>Função D3DXDebugMute

Liga ou desliga toda a saída de depuração D3DX.

## <a name="syntax"></a>Sintaxe


```C++
BOOL D3DXDebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Mute* \[ Em\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Se **TRUE**, a saída do depurador será interrompida; se **FALSE**, a saída de depuração está habilitada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Retorna o valor anterior de Mute.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Uso Geral funções](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
