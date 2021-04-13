---
title: Método INapSystemHealthAgentCallback GetSoHRequest (NapSystemHealthAgent. h)
description: É chamado pelo NapAgent para consultar a solicitação SoH do agente de integridade do sistema.
ms.assetid: 4161a3e7-2f7a-40d1-b973-47f991bba5d0
keywords:
- Método GetSoHRequest NAP
- Método GetSoHRequest NAP, interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP, método GetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0fd95ce79587b5e7e259323286cfce138dd2df2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369705"
---
# <a name="inapsystemhealthagentcallbackgetsohrequest-method"></a>Método INapSystemHealthAgentCallback:: GetSoHRequest

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSystemHealthAgentCallback:: GetSoHRequest** é chamado pelo NapAgent para consultar a solicitação soh do agente de integridade do sistema.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSoHRequest(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*solicitação* \[ do no\]
</dt> <dd>

Um ponteiro COM para um objeto [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) que identifica o objeto de solicitação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor



| Código de retorno                                                                                                                      | Descrição                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                             | Indica êxito.<br/>                                                                                                                      |
| <dl> <dt>**HRESULT \_ do \_ Win32 ( \_ servidor RPC \_ S \_ indisponível)**</dt> </dl> | Se esse código for retornado pela sua implementação, o NapAgent removerá o SHA da lista Bound-SHA e liberará sua entrada de cache.<br/> |



 

Quando qualquer valor de retorno (exceto **HRESULT \_ do \_ Win32 ( \_ servidor RPC S \_ \_ indisponível)**) é RETORNADO pela sua implementação, o sistema NAP constrói e retorna um [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) para o SHV correspondente com os seguintes tipos de atributo e valores:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = <de código de erro>

## <a name="remarks"></a>Comentários

Esse método de retorno de chamada é declarado pelo sistema NAP e deve ser implementado pelo gravador SHA.

Esse método deve processar a solicitação e retornar imediatamente. Atrasar o retorno desse método afeta negativamente o desempenho e a capacidade de resposta do sistema e pode fazer com que outras partes do sistema operacional expirem o tempo limite.

O monitoramento do estado de integridade não deve ser feito como parte dessa chamada, especialmente se for de computação intensiva e demorar muito. O monitoramento do estado de integridade e a computação SoH devem ser executados em um thread ou serviço separado. A única função desse método deve ser definir a SoH e o retorno do SHA.

Se levará muito tempo para que o SHA gere uma SoH, a SoH armazenada em cache deverá ser retornada ao NapAgent. Se não houver nenhuma SoH armazenada em cache para retornar, o SHA deverá retornar imediatamente uma SoH com os seguintes tipos de atributo e valores:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientCommunication**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **NAP \_ E \_ nenhum \_ \_ soh armazenado em cache**](nap-error-constants.md)

Quando a SoH é gerada, o SHA deve chamar [**INapSystemHealthAgentBinding:: NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) para notificar o NapAgent da alteração de integridade do sistema.

O NapAgent chama esse método para consultar o SoHRequest do agente de integridade do sistema. O SHA pode consultar o objeto [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) passado para parâmetros que ele precisa para calcular o SoHRequest. O SHA deve definir o SoHRequest calculado no objeto de solicitação. O SHA não deve manter referências ao objeto de solicitação depois que essa chamada for concluída.

Quando esse método é chamado, se houver uma SoH no cache do NapAgent, ele será definido no objeto de solicitação. O SHA pode consultá-lo usando **GetSoHRequest**. Se o SHA não definir uma nova SoH, o armazenado em cache será usado.

Para SHAs não associados que são registrados com o sistema, o sistema NAP constrói e envia um SoHRequest para o SHV correspondente com os seguintes tipos de atributo e valores:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **NAP \_ E \_ não \_ inicializado**](nap-error-constants.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                |
| parâmetro<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





