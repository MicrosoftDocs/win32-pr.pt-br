---
description: Recuperar características de fonte.
ms.assetid: ef7e0d18-492b-476b-945a-bfc0232a939a
title: 'Método ID3DX10Font:: GetTextMetrics (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetTextMetrics
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 97cbddc59dd84d0a5b83610212fe94e87a49757da0430d64cb420280c815d9cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047044"
---
# <a name="id3dx10fontgettextmetrics-method"></a>Método ID3DX10Font:: GetTextMetrics

Recuperar características de fonte.

## <a name="syntax"></a>Sintaxe


```C++
BOOL GetTextMetrics(
  [in] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTextMetrics* \[ no\]
</dt> <dd>

Tipo: **TEXTMETRIC \***

Ponteiro para uma estrutura [TEXTMETRIC](/previous-versions//ms534202(v=vs.85)) , que contém propriedades de fonte. Se o Unicode for definido, a função retornará uma estrutura TEXTMETRICW. Caso contrário, a função retorna uma estrutura textmetrica.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Diferente de zero se a função for bem-sucedida; caso contrário, 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
