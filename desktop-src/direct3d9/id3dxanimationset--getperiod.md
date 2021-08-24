---
description: Obtém o período do conjunto de animação.
ms.assetid: 0bb19ec1-c918-44b6-83b0-4fdbb4e1a485
title: Método ID3DXAnimationSet::GetPeriod (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriod
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d8e984d1593fbbd79561bbb15fb27b62a9961c1830c42465ed529f08c374e180
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118522325"
---
# <a name="id3dxanimationsetgetperiod-method"></a>Método ID3DXAnimationSet::GetPeriod

Obtém o período do conjunto de animação.

## <a name="syntax"></a>Sintaxe


```C++
DOUBLE GetPeriod();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Período do conjunto de animação.

## <a name="remarks"></a>Comentários

O período é o intervalo de tempo em que os quadros-chave de animação são válidos. Para animações de loop, esse é o período do loop. As unidades de tempo em que os quadros-chave são especificados (por exemplo, segundos) são determinadas pelo aplicativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
