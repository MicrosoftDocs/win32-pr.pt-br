---
description: O método DisplayTypeInfo exibe informações de tipo de mídia durante a depuração.
ms.assetid: fd10d37b-57f5-4246-8ca3-f4bc59911445
title: Método CBasePin.DisplayTypeInfo (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisplayTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10b4535950a46fa55aba0ea7d808a075186f074cc829be0d3225dc887512ad47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916446"
---
# <a name="cbasepindisplaytypeinfo-method"></a>Método CBasePin.DisplayTypeInfo

O `DisplayTypeInfo` método exibe informações de tipo de mídia durante a depuração.

## <a name="syntax"></a>Sintaxe


```C++
void DisplayTypeInfo(
         IPin       *pPin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPin* 
</dt> <dd>

Ignorado.

</dd> <dt>

*Pgto* 
</dt> <dd>

Ponteiro para um [**objeto CMediaType**](cmediatype.md) que especifica o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Em builds de depuração, esse método chama a [**função DbgLog**](dbglog.md) para exibir o tipo de mídia especificado. Em builds de varejo, esse método não faz nada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




