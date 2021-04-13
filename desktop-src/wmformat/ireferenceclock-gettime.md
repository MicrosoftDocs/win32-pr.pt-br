---
title: Método getTime IReferenceClock
description: O método getTime recupera o tempo de referência atual.
ms.assetid: 9bf5050a-ae09-4a72-a3f2-3df8339d99b9
keywords:
- Método getTime Windows Media Format
- Método getTime Windows Media Format, interface IReferenceClock
- IReferenceClock Interface formato Windows Media, método getTime
topic_type:
- apiref
api_name:
- IReferenceClock.GetTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c679ce0adbbc6cc7ddc014c12f1b0ace4be6b4b0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104365035"
---
# <a name="ireferenceclockgettime-method"></a>Método IReferenceClock:: getTime

O método **getTime** recupera o tempo de referência atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTime(
  [out] REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTime* \[ fora\]
</dt> <dd>

Ponteiro para uma variável que recebe a hora atual, em unidades de 100 a nanossegundos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                               | Descrição                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | O método foi bem-sucedido.<br/>              |
| <dl> <dt>**\_ponteiro E**</dt> </dl> | O parâmetro *pTime* é **nulo**.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IReferenceClock**](ireferenceclock.md)
</dt> </dl>

 

 





