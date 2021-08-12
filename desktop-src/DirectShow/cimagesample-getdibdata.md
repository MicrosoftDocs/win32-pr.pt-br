---
description: O método GetDIBData recupera informações sobre o DIB (bitmap independente de dispositivo) GDI que esse objeto está gerenciando.
ms.assetid: ec337336-69ec-47ff-a522-42c0388f9bc0
title: Método CImageSample.GetDIBData (Winutil.h)
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
ms.openlocfilehash: 894d75512c6c7909f617e13999e7290efea663fa843bf64424aad8371965de75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655595"
---
# <a name="cimagesamplegetdibdata-method"></a>Método CImageSample.GetDIBData

O método recupera informações sobre o DIB (bitmap independente de `GetDIBData` dispositivo) GDI que esse objeto está gerenciando.

## <a name="syntax"></a>Sintaxe


```C++
DIBDATA* GetDIBData();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um ponteiro para uma [**estrutura DIBDATA.**](dibdata.md)

## <a name="remarks"></a>Comentários

O chamador deve inicializar a estrutura **DIBDATA** antes de chamar esse método; verifique o valor de **CImageSample::m \_ bInit**. Para inicializar a estrutura, chame o [**método CImageSample::SetDIBData.**](cimagesample-setdibdata.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageSample**](cimagesample.md)
</dt> </dl>

 

 




