---
title: Método IReferenceClock AdviseTime
description: O método AdviseTime solicita uma notificação assíncrona de que um tempo decorrido.
ms.assetid: 8f3f8713-b53c-4110-ac7a-724bbc49368e
keywords:
- Formato de mídia do windows do método AdviseTime
- Formato de mídia do windows do método AdviseTime, interface IReferenceClock
- Formato de mídia da interface IReferenceClock, método AdviseTime
topic_type:
- apiref
api_name:
- IReferenceClock.AdviseTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b648c1c1305503f049b3c02669d1fa3c49be428d31c0cd292801b3541a25cc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655363"
---
# <a name="ireferenceclockadvisetime-method"></a>Método IReferenceClock::AdviseTime

O **método AdviseTime** solicita uma notificação assíncrona de que um tempo decorrido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AdviseTime(
  [in]  REFERENCE_TIME rtBaseTime,
  [in]  REFERENCE_TIME rtStreamTime,
  [in]  HEVENT         hEvent,
  [out] DWORD          *pdwAdviseCookie
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*rtBaseTime* \[ Em\]
</dt> <dd>

Tempo de referência base, em unidades de 100 nanossegundos.

</dd> <dt>

*rtStreamTime* \[ Em\]
</dt> <dd>

Tempo de deslocamento de fluxo, em unidades de 100 nanossegundos.

</dd> <dt>

*hEvent* \[ Em\]
</dt> <dd>

Manipular para um evento, criado pelo chamador. Esse evento será sinalizado quando o tempo especificado ocorrer.

</dd> <dt>

*pdwAdviseCookie* \[ out\]
</dt> <dd>

Ponteiro para uma variável que recebe um identificador para a solicitação. Isso é usado para identificar essa chamada para **AdviseTime** no futuro, por exemplo, para cancelar a solicitação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                               | Descrição                                             |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | O método foi bem-sucedido.<br/>                        |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl> | O *parâmetro pdwAdviseCookie* é **NULL.**<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>    | Falha não especificada.<br/>                         |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IReferenceClock Interface**](ireferenceclock.md)
</dt> </dl>

 

 





