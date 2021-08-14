---
title: Método INapSystemHealthAgentCallback ProcessSoHResponse (NapSystemHealthAgent. h)
description: É chamado quando o NapAgent recebe um SoHResponse destinado a esse agente de integridade.
ms.assetid: 860b1012-7df8-456f-8f21-eb0e1abd2b3b
keywords:
- Método ProcessSoHResponse NAP
- Método ProcessSoHResponse NAP, interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP, método ProcessSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.ProcessSoHResponse
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f5aaca7833560dbb53422da08ced158bb172610c3bacef931866d74d416fcce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367751"
---
# <a name="inapsystemhealthagentcallbackprocesssohresponse-method"></a>INapSystemHealthAgentCallback: método rocessSoHResponse de:P

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSystemHealthAgentCallback::P rocesssohresponse** é chamado quando o NapAgent recebe um [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destinado a esse agente de integridade.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ProcessSoHResponse(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*solicitação* \[ do no\]
</dt> <dd>

Um ponteiro COM para um objeto [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) que identifica o objeto de solicitação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                            | Descrição                                                                              |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Indica êxito.<br/>                                                            |
| <dl> <dt>**\_pacote NAP E \_ inválido \_**</dt> </dl> | Retornado por essa implementação se a resposta não estiver no formato correto.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método de retorno de chamada é declarado pelo sistema NAP e deve ser implementado pelo gravador SHA.

Quando o NapAgent recebe um [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destinado a esse agente de integridade, ele invoca esse método. O agente de integridade deve consultar o SoHResponse do objeto de solicitação. Ele não deve manter referências ao objeto de solicitação depois que essa chamada for concluída.

O método **INapSystemHealthAgentCallback::P rocesssohresponse** não deve bloquear. Se qualquer processamento de correção for necessário, qualquer implementação de **ProcessSoHResponse** deverá iniciar um novo thread para executar o processamento de correção. O NapAgent deve chamar [**INapSystemHealthAgentCallBack:: GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) para determinar o status de correção do Sha.

Esse método deve retornar **um \_ \_ \_ pacote NAP E inválido** se a resposta não estiver no formato correto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





