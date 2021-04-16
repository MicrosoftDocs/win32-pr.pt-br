---
description: O \_ método Get ProtocolVersion Obtém o protocolo de descritor de sessão (SDP; consulte a versão do protocolo RFC 2327).
ms.assetid: 7c62357c-427f-40f9-a9d2-c4e1a8400e97
title: 'Método ITSdp:: get_ProtocolVersion (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652c6c3d6723a10cfe474376cf8b9f1342321db8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768576"
---
# <a name="itsdpget_protocolversion-method"></a>Método ITSdp:: get \_ ProtocolVersion

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get \_ ProtocolVersion** Obtém o protocolo de descritor de sessão (SDP; consulte a versão do protocolo RFC 2327).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_ProtocolVersion(
  [out] unsigned char *pProtocolVersion
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pProtocolVersion* \[ fora\]
</dt> <dd>

Ponteiro para a versão do protocolo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                        |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *pProtocolVersion* não é um ponteiro válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/>     |
| <dl> <dt>**E \_ falha**</dt> </dl>        | Erro não especificado.<br/>                                       |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                      |



 

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

 

 




