---
description: O \_ método Put StopTime define o valor de hora de término do NTP (protocolo NTP). Se a hora de término for zero, a sessão não será vinculada.
ms.assetid: 6f07054c-5fb2-4ee4-9025-3acf9b51ddbd
title: 'ITTime: método de ut_StopTime de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53446ea1d7ee93589987c42b005d7a84e7e728ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764764"
---
# <a name="ittimeput_stoptime-method"></a>ITTime::p o \_ método UT StopTime

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Put \_ StopTime** define o valor de hora de término do NTP (protocolo NTP). Se a hora de término for zero, a sessão não será vinculada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_StopTime(
  [in] DOUBLE Time
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Tempo* \[ no\]
</dt> <dd>

Hora de parada para a sessão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro de *tempo* não é válido.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**E \_ falha**</dt> </dl>        | Erro não especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                  |



 

## <a name="remarks"></a>Comentários

Essa função pode enviar dados pela transmissão em formato não criptografado; Portanto, alguém que está interceptando na rede pode ser capaz de ler os dados. O risco de segurança de enviar os dados em texto não criptografado deve ser considerado antes de usar esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITTime**](ittime.md)
</dt> <dt>

[**ITTime:: obter \_ StopTime**](ittime-get-stoptime.md)
</dt> </dl>

 

 




