---
description: O método GetDIBData recupera informações sobre o DIB (bitmap independente de dispositivo) do GDI que esse objeto está gerenciando.
ms.assetid: ec337336-69ec-47ff-a522-42c0388f9bc0
title: Método CImageSample. GetDIBData (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.GetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fd198152e7c0042a6d48cf942a48745540960d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786989"
---
# <a name="cimagesamplegetdibdata-method"></a>Método CImageSample. GetDIBData

O `GetDIBData` método recupera informações sobre o DIB (bitmap independente de dispositivo) do GDI que esse objeto está gerenciando.

## <a name="syntax"></a>Sintaxe


```C++
DIBDATA* GetDIBData();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um ponteiro para uma estrutura [**DIBDATA**](dibdata.md) .

## <a name="remarks"></a>Comentários

O chamador deve inicializar a estrutura **DIBDATA** antes de chamar esse método; Verifique o valor de **CImageSample:: m \_ bInit**. Para inicializar a estrutura, chame o método [**CImageSample:: SetDIBData**](cimagesample-setdibdata.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageSample**](cimagesample.md)
</dt> </dl>

 

 




