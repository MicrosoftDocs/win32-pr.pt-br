---
description: O método get \_ Bandwidth obtém o valor de largura de banda.
ms.assetid: d9020443-d061-4a60-9d54-191144def110
title: Método ITConnection::get_Bandwidth (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5ec8d46b4b57fb4bc3249acd486225e6de2ef108aa82ba3661c2c4ad5840c1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975786"
---
# <a name="itconnectionget_bandwidth-method"></a>Método ITConnection::get \_ Bandwidth

\[As interfaces e controles de Conferência de Telefonia IP de reunião não estão disponíveis para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O método **get \_ Bandwidth** obtém o valor de largura de banda.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Bandwidth(
  [out] DOUBLE *pBandwidth
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pBandwidth* \[ out\]
</dt> <dd>

Valor de largura de banda.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | O *parâmetro pBandwidth* não é um ponteiro válido.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Erro não especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 

 




