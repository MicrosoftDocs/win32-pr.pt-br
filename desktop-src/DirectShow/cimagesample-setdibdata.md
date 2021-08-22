---
description: O método SetDIBData especifica informações sobre o bitmap independente de dispositivo (DIB) GDI que esse objeto está gerenciando. Chame esse método para inicializar o objeto CImageSample.
ms.assetid: 850fa16b-d4b9-4fe6-b202-7b54c49a4589
title: Método CImageSample. SetDIBData (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.SetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 367fed37545e9498f9f6e753a57a7eeeb2ce8767779241284be9109676fafd38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655520"
---
# <a name="cimagesamplesetdibdata-method"></a>Método CImageSample. SetDIBData

O `SetDIBData` método especifica informações sobre o DIB (bitmap independente de dispositivo) GDI que esse objeto está gerenciando. Chame esse método para inicializar o objeto **CImageSample** .

## <a name="syntax"></a>Sintaxe


```C++
void SetDIBData(
   DIBDATA *pDibData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDibData* 
</dt> <dd>

Ponteiro para uma estrutura [**DIBDATA**](dibdata.md) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageSample**](cimagesample.md)
</dt> </dl>

 

 




