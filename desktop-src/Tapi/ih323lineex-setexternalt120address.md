---
description: O método SetExternalT120Address é chamado por um aplicativo para configurar um endereço T. 120 externo para troca de dados.
ms.assetid: 094b43b9-eb15-468a-9986-86313490e1c3
title: 'Método IH323LineEx:: SetExternalT120Address (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09756aaf77ba36497b3059f7e93829d7d6a57b42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760345"
---
# <a name="ih323lineexsetexternalt120address-method"></a>Método IH323LineEx:: SetExternalT120Address

\[O **SetExternalT120Address** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **SetExternalT120Address** é chamado por um aplicativo para configurar um endereço T. 120 externo para troca de dados. A funcionalidade T. 120 será anunciada durante a negociação H. 245 e o endereço será usado na confirmação do canal de lógica aberta para que o outro ponto de extremidade possa configurar sessões T. 120 com o serviço de escuta nesse endereço. Se essa função não for chamada, o provedor de serviços H. 323 não anunciará a funcionalidade T. 120.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetExternalT120Address(
  [in] BOOL  fEnable,
  [in] DWORD dwIP,
  [in] WORD  wPort
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fEnable* \[ no\]
</dt> <dd>

**True** para habilitar a funcionalidade T. 120; **False** para desabilitar a funcionalidade T. 120.

</dd> <dt>

*dwIP* \[ no\]
</dt> <dd>

**DWORD** que contém o endereço IP na ordem de bytes do host do serviço externo T. 120.

</dd> <dt>

*wPort* \[ no\]
</dt> <dd>

O **Word** que contém a porta do serviço T. 120 externo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                          | Descrição                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 




