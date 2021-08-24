---
description: Construtor CPersistStream.CPersistStream – método construtor.
ms.assetid: 48143a61-5ba7-4bf9-bffa-244f2769144d
title: Construtor CPersistStream.CPersistStream (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.CPersistStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 00745dab5d851f05bf3df99dcdb7b6e8574518a970f8a79466a291cbec13997a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813386"
---
# <a name="cpersiststreamcpersiststream-constructor"></a>Construtor CPersistStream.CPersistStream

Método do construtor.

## <a name="syntax"></a>Sintaxe


```C++
CPersistStream(
   IUnknown *pUnk,
   HRESULT  *phr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Punk* 
</dt> <dd>

Ponteiro para a interface **IUnknown** do objeto de delegação.

</dd> <dt>

*Phr* 
</dt> <dd>

Ponteiro para o valor de retorno COM geral. Esse valor será alterado somente se essa função falhar.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Pstream.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




