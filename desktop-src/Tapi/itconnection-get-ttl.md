---
description: O \_ método Get TTL Obtém o escopo TTL (vida útil) para transmissões nos endereços.
ms.assetid: ea3c22d8-476e-4b4b-98c6-f1075e704f3d
title: 'Método ITConnection:: get_Ttl (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88f4810eeefc19647e6ed5601b3a6b88870f1e9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759471"
---
# <a name="itconnectionget_ttl-method"></a>Método ITConnection:: get \_ TTL

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get \_ TTL** Obtém o escopo [*TTL (vida útil)*](t-tapgloss.md) para transmissões nos endereços.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Ttl(
  [out] unsigned char *pTtl
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTtl* \[ fora\]
</dt> <dd>

Escopo TTL.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                         | Significado                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *pTtl* não é um ponteiro válido.<br/>         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**E \_ falha**</dt> </dl>        | Erro não especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 

 




