---
description: Habilitar ou desabilitar mensagens de depuração.
ms.assetid: 5c2aa3cf-ee6a-40fd-b300-67cb6ce691b6
title: Função D3DX10DebugMute (D3DX10Core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DebugMute
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f4cd6a7ade60bc59cb1e6cbd9d3a447fac5cb7364db1ca85dcf704acedaa645c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128378"
---
# <a name="d3dx10debugmute-function"></a>Função D3DX10DebugMute

Habilitar ou desabilitar mensagens de depuração.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10DebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Mute* \[ Em\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Definido como **TRUE para** habilitar mensagens de depuração; definido como **FALSE para** desabilitar mensagens de depuração.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados em Códigos de Retorno [do Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentários

Use essa função para desabilitar mensagens de erro para APIs D3DX10 durante a depuração; O uso dessa função deve ser protegido pela opção do \_ compilador DEBUG D3D10.


```
#ifdef D3D10_DEBUG
  BOOL WINAPI D3DX10DebugMute(BOOL Mute);  
#endif
```



O estado padrão é **TRUE para** um build de depuração.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Uso Geral funções](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
