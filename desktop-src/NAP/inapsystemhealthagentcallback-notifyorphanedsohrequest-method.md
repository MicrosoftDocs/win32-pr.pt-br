---
title: Método INapSystemHealthAgentCallback NotifyOrphanedSoHRequest (NapSystemHealthAgent. h)
description: É chamado se um SoHRequest foi consultado a partir do SHA, mas a resposta nunca voltou.
ms.assetid: 9e6fac6c-fb23-4725-ae0f-28ef8a6c4ea6
keywords:
- Método NotifyOrphanedSoHRequest NAP
- Método NotifyOrphanedSoHRequest NAP, interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP, método NotifyOrphanedSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.NotifyOrphanedSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 171191c266ae3fd59ab1ba8f55acd73eb143e9aa220fb3d2989a7ced9f716513
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621177"
---
# <a name="inapsystemhealthagentcallbacknotifyorphanedsohrequest-method"></a>Método INapSystemHealthAgentCallback:: NotifyOrphanedSoHRequest

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSystemHealthAgentCallback:: NotifyOrphanedSoHRequest** é chamado se um [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) foi consultado a partir do Sha, mas a resposta nunca voltou.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT NotifyOrphanedSoHRequest(
  [in] const CorrelationId *correlationId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CorrelationId* \[ no\]
</dt> <dd>

Um ponteiro para a estrutura exclusiva de [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) que identifica o [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)órfão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                          | Descrição                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Indica êxito.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método de retorno de chamada é declarado pelo sistema NAP e deve ser implementado pelo gravador SHA.

Esse método pode ser chamado pelo sistema nos seguintes casos:

-   Um [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) não pôde ser enviado na conexão.
-   Um [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) foi enviado na conexão, mas nenhum **SoHResponse** voltou, ou seja, o imforçador esgotou o tempo limite ou não havia um SHV correspondente no lado do servidor.
-   A conexão foi desativada ou um aplicador ficou offline.

Essa é apenas uma notificação de melhor esforço, portanto, os SHAs não devem confiar nessas informações para limpar o estado. Há várias situações em que um SHA não será notificado:

-   Se um imposição se comportar, ou seja, ele não notifica o SHA quando o estado da conexão está inativo.
-   Se um aplicador falhar.
-   Em condições de erro, ou seja, o NapAgent está sem memória.

Os SHAs podem receber algumas notificações falsas quando eles se ligam pela primeira vez ao NapAgent, por exemplo, se uma troca de SoH estiver em andamento quando o SHA estiver ligado e expirar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                |
| parâmetro<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





