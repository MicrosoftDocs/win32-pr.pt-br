---
description: Obtém o valor de escala Stipple-Pattern.
ms.assetid: cf80ae8c-493d-4f35-b4f9-5981e64cc842
title: 'Método ID3DXLine:: GetPatternScale (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.GetPatternScale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 14a9919ede81eb64b844e1882725e37359ad6738
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104371022"
---
# <a name="id3dxlinegetpatternscale-method"></a>Método ID3DXLine:: GetPatternScale

Obtém o valor de escala Stipple-Pattern.

## <a name="syntax"></a>Sintaxe


```C++
FLOAT GetPatternScale();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Retorna o valor usado para dimensionar o Stipple-Pattern. 1.0 f é o valor padrão e não representa dimensionamento. Um valor menor que 1,0 f reduz o padrão e um valor maior que 1,0 amplia o padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> <dt>

[**ID3DXLine::SetPatternScale**](id3dxline--setpatternscale.md)
</dt> </dl>

 

 
