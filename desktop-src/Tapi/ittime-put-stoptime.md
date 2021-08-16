---
description: O método put StopTime define o valor de hora final \_ de NTP (protocolo NTP). Se a hora de término for zero, a sessão não será limitada.
ms.assetid: 6f07054c-5fb2-4ee4-9025-3acf9b51ddbd
title: Método ITTime::p ut_StopTime (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e3aa32615988e52ccaa845a8fb7ec52f2e863c7193ee393d7d184e2b3002f59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762378"
---
# <a name="ittimeput_stoptime-method"></a>Método StopTime::p ut \_

\[As interfaces e controles de Conferência de Telefonia IP de reunião não estão disponíveis para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método \_ put StopTime** define o valor de hora final de NTP (protocolo NTP). Se a hora de término for zero, a sessão não será limitada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_StopTime(
  [in] DOUBLE Time
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Hora* \[ Em\]
</dt> <dd>

Hora de parada da sessão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O *parâmetro Time* não é válido.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Erro não especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                  |



 

## <a name="remarks"></a>Comentários

Essa função pode enviar dados pela transmissão em formato não criptografado; portanto, alguém que está escutando na rede pode conseguir ler os dados. O risco de segurança de enviar os dados em texto não claro deve ser considerado antes de usar esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITTime**](ittime.md)
</dt> <dt>

[**ITTime::get \_ StopTime**](ittime-get-stoptime.md)
</dt> </dl>

 

 




