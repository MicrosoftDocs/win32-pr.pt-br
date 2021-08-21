---
description: Recupera características de fonte que são identificadas em uma estrutura TEXTMETRIC. Esse método dá suporte às configurações de compilador ANSI e Unicode.
ms.assetid: 37788281-5bb0-45bb-b6d4-bdc4d811e3af
title: 'Método ID3DXFont:: GetTextMetrics (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetTextMetrics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9254ec9d5224f9041079f36bc95d68ea7346cf6dac2aecb81e7a6009496675e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987406"
---
# <a name="id3dxfontgettextmetrics-method"></a>Método ID3DXFont:: GetTextMetrics

Recupera características de fonte que são identificadas em uma estrutura [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) . Esse método dá suporte às configurações de compilador ANSI e Unicode.

## <a name="syntax"></a>Sintaxe


```C++
BOOL GetTextMetrics(
  [out] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTextMetrics* \[ fora\]
</dt> <dd>

Tipo: **[ **TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)\***

Ponteiro para uma estrutura [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) , que contém propriedades de fonte.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Diferente de zero se a função for bem-sucedida; caso contrário, 0.

## <a name="remarks"></a>Comentários

A configuração do compilador também determina o tipo de estrutura. Se o Unicode for definido, a função retornará uma estrutura TEXTMETRICW. Caso contrário, a chamada de função retorna uma estrutura textmetrica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
