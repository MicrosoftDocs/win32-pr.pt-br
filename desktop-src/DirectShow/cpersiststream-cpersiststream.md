---
description: Construtor de CPersistStream. CPersistStream-método de construtor.
ms.assetid: 48143a61-5ba7-4bf9-bffa-244f2769144d
title: Construtor CPersistStream. CPersistStream (pStream. h)
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
ms.openlocfilehash: 9e3be9233d76929ebfcb79121c60ef6c1af35b56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085604"
---
# <a name="cpersiststreamcpersiststream-constructor"></a>Construtor CPersistStream. CPersistStream

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CPersistStream(
   IUnknown *pUnk,
   HRESULT  *phr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pUnk* 
</dt> <dd>

Ponteiro para a interface **IUnknown** do objeto de delegação.

</dd> <dt>

*phr* 
</dt> <dd>

Ponteiro para o valor de retorno de COM geral. Esse valor só será alterado se essa função falhar.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PStream. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




