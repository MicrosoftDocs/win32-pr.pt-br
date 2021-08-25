---
title: Método GetTime IReferenceClock
description: O método GetTime recupera a hora de referência atual.
ms.assetid: 9bf5050a-ae09-4a72-a3f2-3df8339d99b9
keywords:
- Formato de mídia do windows do método GetTime
- Formato de mídia do windows do método GetTime, interface IReferenceClock
- Formato de mídia da interface IReferenceClock, método GetTime
topic_type:
- apiref
api_name:
- IReferenceClock.GetTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f7756240e8987199e1f1b5d79e3f0b676d4808520781fbac18dfa18dd75e88d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055436"
---
# <a name="ireferenceclockgettime-method"></a>Método IReferenceClock::GetTime

O **método GetTime** recupera a hora de referência atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTime(
  [out] REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTime* \[ out\]
</dt> <dd>

Ponteiro para uma variável que recebe a hora atual, em unidades de 100 nanossegundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                               | Descrição                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | O método foi bem-sucedido.<br/>              |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl> | O *parâmetro pTime* é **NULL.**<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IReferenceClock Interface**](ireferenceclock.md)
</dt> </dl>

 

 





