---
description: O método \_ get SessionId obtém o valor de protocolo NTP (NTP) de 32 bits que serve como o identificador de sessão. Isso é gerado automaticamente quando a sessão é criada.
ms.assetid: 5177f120-4b93-40bc-9481-aedf65a8dee9
title: Método ITSdp::get_SessionId (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67f7e8ea9bef17e5cb34ca23443b1f16f815c964c3cf76b9b122878e8662d051
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621536"
---
# <a name="itsdpget_sessionid-method"></a>Método ITSdp::get \_ SessionId

\[As interfaces e controles de Conferência de Telefonia IP de reunião não estão disponíveis para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método \_ get SessionId** obtém o valor de protocolo NTP (NTP) de 32 bits que serve como o identificador de sessão. Isso é gerado automaticamente quando a sessão é criada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_SessionId(
  [out] DOUBLE *pSessionId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSessionId* \[ out\]
</dt> <dd>

Ponteiro para o identificador de sessão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O *parâmetro pSessionId* não é válido.<br/>             |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | O *parâmetro pSessionId* não é um ponteiro válido.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Erro não especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                  |



 

## <a name="remarks"></a>Comentários

O valor de retorno desse método pode ser **ULONG,** mas Visual Basic não dá suporte ao **tipo ULONG.** Um **DOUBLE** é o próximo tipo menor que abrange todo o intervalo de valores necessários.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> </dl>

 

 




