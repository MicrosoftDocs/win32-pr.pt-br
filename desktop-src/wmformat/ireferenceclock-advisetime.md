---
title: Método Aconselhetime IReferenceClock
description: O método Aconselhetime solicita uma notificação assíncrona que um tempo decorreu.
ms.assetid: 8f3f8713-b53c-4110-ac7a-724bbc49368e
keywords:
- Método aconselhetime Windows Media Format
- Método aconselhetime Windows Media Format, interface IReferenceClock
- Formato de mídia do Windows da interface IReferenceClock, método Aconselhetime
topic_type:
- apiref
api_name:
- IReferenceClock.AdviseTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3fa91338b4bff8f925f00e7159a36089e0de0aa8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105772732"
---
# <a name="ireferenceclockadvisetime-method"></a>Método IReferenceClock:: AdviseTime

O método **aconselhetime** solicita uma notificação assíncrona que um tempo decorreu.

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

*rtBaseTime* \[ no\]
</dt> <dd>

Tempo de referência base, em unidades de 100 a nanossegundos.

</dd> <dt>

*rtStreamTime* \[ no\]
</dt> <dd>

Tempo de deslocamento de fluxo, em unidades de 100 a nanossegundos.

</dd> <dt>

*hEvent* \[ no\]
</dt> <dd>

Identificador para um evento, criado pelo chamador. Esse evento será sinalizado quando o tempo especificado for decorrido.

</dd> <dt>

*pdwAdviseCookie* \[ fora\]
</dt> <dd>

Ponteiro para uma variável que recebe um identificador para a solicitação. Isso é usado para identificar essa chamada para o **aconselhetime** no futuro, por exemplo, para cancelar a solicitação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                               | Descrição                                             |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | O método foi bem-sucedido.<br/>                        |
| <dl> <dt>**\_ponteiro E**</dt> </dl> | O parâmetro *pdwAdviseCookie* é **nulo**.<br/> |
| <dl> <dt>**E \_ falha**</dt> </dl>    | Falha não especificada.<br/>                         |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IReferenceClock**](ireferenceclock.md)
</dt> </dl>

 

 





