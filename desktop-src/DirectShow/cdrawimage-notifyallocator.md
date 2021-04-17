---
description: O método NotifyAllocator informa ao objeto CDrawImage se o alocador da conexão é um objeto CImageAllocator.
ms.assetid: cc1604e7-f755-4a7a-9294-6fd06bb434d4
title: Método CDrawImage. NotifyAllocator (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7bab7d1d00b70317a7cbb0b79f8a430a603a757
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789978"
---
# <a name="cdrawimagenotifyallocator-method"></a>Método CDrawImage. NotifyAllocator

O `NotifyAllocator` método informa ao objeto **CDrawImage** se o alocador da conexão é um objeto [**CImageAllocator**](cimageallocator.md) .

## <a name="syntax"></a>Sintaxe


```C++
void NotifyAllocator(
   BOOL bUsingImageAllocator
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bUsingImageAllocator* 
</dt> <dd>

Valor booliano que indica que tipo de alocador está sendo usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O filtro proprietário deve chamar esse método depois que os Pins concordarem com um alocador. Se o filtro souber que o alocador é um objeto **CImageAllocator** , ele deverá chamar esse método com o valor **true**. (Normalmente, o filtro saberá isso somente se ele for proprietário do alocador em questão.) Caso contrário, ele deve chamar esse método com o valor **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::D rawImage**](cdrawimage-drawimage.md)
</dt> </dl>

 

 




