---
description: O \_ método Get SessionID Obtém o valor de NTP (protocolo NTP) de 32 bits que serve como o identificador de sessão. Isso é gerado automaticamente quando a sessão é criada.
ms.assetid: 5177f120-4b93-40bc-9481-aedf65a8dee9
title: 'Método ITSdp:: get_SessionId (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad593b61f4c935a220e59383ae170569f04af54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767748"
---
# <a name="itsdpget_sessionid-method"></a>Método ITSdp:: get \_ SessionID

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get \_ SessionID** Obtém o valor de NTP (protocolo NTP) de 32 bits que serve como o identificador de sessão. Isso é gerado automaticamente quando a sessão é criada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_SessionId(
  [out] DOUBLE *pSessionId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSessionId* \[ fora\]
</dt> <dd>

Ponteiro para o identificador de sessão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *pSessionId* não é válido.<br/>             |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *pSessionId* não é um ponteiro válido.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**E \_ falha**</dt> </dl>        | Erro não especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                  |



 

## <a name="remarks"></a>Comentários

O valor de retorno desse método pode ser **ULONG**, mas Visual Basic não dá suporte ao tipo **ULONG** . Um **Double** é o próximo menor tipo que abrange todo o intervalo de valores necessário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> </dl>

 

 




