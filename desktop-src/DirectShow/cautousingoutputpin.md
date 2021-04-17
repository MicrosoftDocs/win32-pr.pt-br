---
description: A classe CAutoUsingOutputPin Obtém e libera o acesso a um objeto CDynamicOutputPin.
ms.assetid: 4ded5d18-4b14-4574-ad1f-73b886a51fac
title: Classe CAutoUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b664267ce2ff0dbbeeba8bc74708c9c67e185ae4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755368"
---
# <a name="cautousingoutputpin-class"></a>Classe CAutoUsingOutputPin

A classe **CAutoUsingOutputPin** Obtém e libera o acesso a um objeto [**CDynamicOutputPin**](cdynamicoutputpin.md) .

**CAutoUsingOutputPin** tem estes tipos de membros:



| Métodos públicos                                                           | Descrição                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [**CAutoUsingOutputPin**](cautousingoutputpin-cautousingoutputpin.md)   | Método de construtor. Obtém acesso ao PIN especificado. |
| [**~ CAutoUsingOutputPin**](cautousingoutputpin--cautousingoutputpin.md) | Método destruidor. Obtém acesso ao PIN especificado.  |



 

## <a name="remarks"></a>Comentários

Quando determinados métodos são chamados em [**CDynamicOutputPin**](cdynamicoutputpin.md), o chamador deve obter acesso ao PIN e, em seguida, liberar esse acesso. Para obter acesso, o chamador usa o método [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) . Para liberar o acesso, ele chama o método [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) . A classe **CAutoUsingOutputPin** é uma classe auxiliar que manipula essas tarefas em seus métodos de construtor e destruidor. O exemplo de código a seguir mostra como usar essa classe:


```
CDynamicOutputPin *pPin;
HRESULT hr = S_OK;  // Important! Initialize to S_OK.

// TODO: Obtain a pointer to the pin (not shown).

// Scope for lock.
{
    // Hold lock on pin.
    CAutoUsingOutputPin UsingPin(pPin, &hr)

    if (SUCCEEDED(hr)) 
    {

        // Safe to use the pin.
        hr = pPin->Deliver(pSample);

    }

} // Object goes out of scope here.

// No longer safe to use the pin.
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência de classe base](base-class-reference.md)
</dt> </dl>

 

 




