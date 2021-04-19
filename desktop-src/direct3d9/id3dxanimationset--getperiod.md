---
description: Obtém o período do conjunto de animações.
ms.assetid: 0bb19ec1-c918-44b6-83b0-4fdbb4e1a485
title: 'Método ID3DXAnimationSet:: getperiod (D3dx9anim. h)'
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
ms.openlocfilehash: 5f6eafbfe802afc8ff3084c49acf31addca66cef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105783799"
---
# <a name="id3dxanimationsetgetperiod-method"></a>Método ID3DXAnimationSet:: getperiod

Obtém o período do conjunto de animações.

## <a name="syntax"></a>Sintaxe


```C++
DOUBLE GetPeriod();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **[ **duplo**](../winprog/windows-data-types.md)**

Período do conjunto de animações.

## <a name="remarks"></a>Comentários

O período é o intervalo de tempo em que os quadros de chave de animação são válidos. Para animações em loop, esse é o período do loop. As unidades de tempo em que os quadros-chave são especificados (por exemplo, segundos) são determinadas pelo aplicativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
