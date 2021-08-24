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
ms.openlocfilehash: 3799901d071da08ee1bb0de4994ed330fabe2d8fedf3b59ce556105f0a280e3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675136"
---
# <a name="id3dxlinegetpatternscale-method"></a>Método ID3DXLine:: GetPatternScale

Obtém o valor de escala Stipple-Pattern.

## <a name="syntax"></a>Sintaxe


```C++
FLOAT GetPatternScale();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

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

 

 
