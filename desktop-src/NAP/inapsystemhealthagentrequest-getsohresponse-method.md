---
title: Método GetSoHResponse INapSystemHealthAgentRequest (NapSystemHealthAgent.h)
description: É usado pelo agente de saúde para recuperar seu blob SoHResponse quando o NapAgent chama INapSystemHealthAgentCallback ProcessSoHResponse.
ms.assetid: 60319256-d5c2-46cc-a59b-f81732e21a7f
keywords:
- NAP do método GetSoHResponse
- Método GetSoHResponse NAP, interface INapSystemHealthAgentRequest
- Interface NAP INapSystemHealthAgentRequest , método GetSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHResponse
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d78b67c38f54cfe1e7d342212be897ba1825b619324e6fc4cb5ab9ae4f5c4a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621157"
---
# <a name="inapsystemhealthagentrequestgetsohresponse-method"></a>Método INapSystemHealthAgentRequest::GetSoHResponse

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O método **INapSystemHealthAgentRequest::GetSoHResponse** é usado pelo agente de saúde para recuperar seu blob SoHResponse quando o NapAgent chama [**INapSystemHealthAgentCallback::P rocessSoHResponse**](inapsystemhealthagentcallback-processsohresponse-method.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse,
  [out] UINT8       *flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sohResponse* \[ out\]
</dt> <dd>

Um ponteiro para um ponteiro para um [**pacote SoHResponse.**](/windows/win32/api/naptypes/ns-naptypes-soh)

</dd> <dt>

*sinalizadores* \[ out\]
</dt> <dd>

Um ponteiro para um sinalizador que habilita a correção pelo SHA se o bit [**shaFixup**](nap-type-constants.md) estiver definido; caso contrário, a correção será desabilitada.



| Valores possíveis                                                                                                                                                          | Significado                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span><dl> <dt>**shaFixup**</dt> </dl> | Espera-se que o SHA execute a correção com base na resposta. Se esse sinalizador não estiver definido, o SHA não deverá executar uma correção, mesmo que [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) indique que ele não está ônteco.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos do COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Êxito na operação.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite de recursos do sistema, não foi possível executar a operação.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                |
| parâmetro<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





