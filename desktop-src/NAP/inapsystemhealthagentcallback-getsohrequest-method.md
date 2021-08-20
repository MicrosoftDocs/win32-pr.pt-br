---
title: Método GetSoHRequest INapSystemHealthAgentCallback (NapSystemHealthAgent.h)
description: É chamado pelo NapAgent para consultar a solicitação soH do agente de saúde do sistema.
ms.assetid: 4161a3e7-2f7a-40d1-b973-47f991bba5d0
keywords:
- NAP do método GetSoHRequest
- Método GetSoHRequest NAP, interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP , método GetSoHRequest
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
ms.openlocfilehash: d6c9203a782be34be66e84fa8238a678647a4359df8cde3408aa8de99e73fcce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133765"
---
# <a name="inapsystemhealthagentcallbackgetsohrequest-method"></a>Método INapSystemHealthAgentCallback::GetSoHRequest

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método INapSystemHealthAgentCallback::GetSoHRequest** é chamado pelo NapAgent para consultar a solicitação soH do agente de saúde do sistema.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSoHRequest(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*solicitação* \[ Em\]
</dt> <dd>

Um ponteiro COM para um [**objeto INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) que identifica o objeto de solicitação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado



| Código de retorno                                                                                                                      | Descrição                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                             | Indica êxito.<br/>                                                                                                                      |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(RPC \_ S \_ SERVER \_ UNAVAILABLE)**</dt> </dl> | Se esse código for retornado pela implementação, o NapAgent removerá o SHA da lista bound-SHA e liberará sua entrada de cache.<br/> |



 

Quando qualquer valor retornado (exceto **HRESULT \_ FROM \_ WIN32(RPC \_ S SERVER \_ \_ UNAVAILABLE)**) é retornado pela sua implementação, o sistema NAP constrói e retorna um [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) para o SHV correspondente com os seguintes tipos de atributo e valores:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = <código de erro>

## <a name="remarks"></a>Comentários

Esse método de retorno de chamada é declarado pelo sistema NAP e deve ser implementado pelo sha writer.

Esse método deve processar a solicitação e retornar imediatamente. Atrasar o retorno desse método afeta negativamente o desempenho e a capacidade de resposta do sistema e pode fazer com que outras partes do sistema operacional se desesperem.

O monitoramento do estado de saúde não deve ser feito como parte dessa chamada, especialmente se for de computação intensiva e levar muito tempo. O monitoramento de estado de saúde e a computação soH devem ser executados em um thread ou serviço separado. A única função desse método deve ser definir o SoH do SHA e retornar.

Se levar muito tempo para o SHA gerar um SoH, o SoH armazenado em cache deverá ser retornado para o NapAgent. Se não houver nenhum SoH armazenado em cache para retornar, o SHA deverá retornar imediatamente um SoH com os seguintes tipos de atributo e valores:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientCommunication**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **NAP \_ E NO CACHE \_ \_ \_ SOH**](nap-error-constants.md)

Quando o SoH tiver sido gerado, o SHA deverá chamar [**INapSystemHealthAgentBinding::NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) para notificar o NapAgent sobre a alteração de saúde do sistema.

O NapAgent chama esse método para consultar SoHRequest do agente de saúde do sistema. O SHA pode consultar o objeto [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) passado para os parâmetros necessários para calcular o SoHRequest. O SHA deve definir o SoHRequest computado no objeto de solicitação. O SHA não deve conter referências ao objeto de solicitação depois que essa chamada é concluída.

Quando esse método é chamado, se houver um SoH no cache do NapAgent, ele será definido no objeto de solicitação. O SHA pode consultar por ele usando **GetSoHRequest.** Se o SHA não definir um novo SoH, o armazenado em cache será usado.

Para SHAs não correspondentes registrados no sistema, o sistema NAP constrói e envia um SoHRequest para o SHV correspondente com os seguintes tipos de atributo e valores:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **NAP \_ E NÃO \_ \_ INICIALIZADO**](nap-error-constants.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





