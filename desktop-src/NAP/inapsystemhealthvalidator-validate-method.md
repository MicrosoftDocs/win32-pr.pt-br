---
title: Método Validate INapSystemHealthValidator (NapSystemHealthValidator.h)
description: O sistema NAP para validar o SoHRequest recebido de um cliente.
ms.assetid: d67dc2c8-f18c-4e06-a51e-a538ca75c3f1
keywords:
- Validar NAP do método
- Validar o método NAP, interface INapSystemHealthValidator
- INapSystemHealthValidator interface NAP , método Validate
topic_type:
- apiref
api_name:
- INapSystemHealthValidator.Validate
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c200e96024075d0c2880b294c197938a5ec0a6f3e1da4cb019d5ecd3ed32b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802766"
---
# <a name="inapsystemhealthvalidatorvalidate-method"></a>Método INapSystemHealthValidator::Validate

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método INapSystemHealthValidator::Validate** é definido pelo desenvolvedor shv e chamado pelo sistema NAP para validar o [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) recebido de um cliente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Validate(
  [in] INapSystemHealthValidationRequest *request,
  [in] UINT32                            hintTimeOutInMsec,
  [in] INapServerCallback                *callback
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*solicitação* \[ Em\]
</dt> <dd>

Um ponteiro COM para um [**objeto INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) que identifica o objeto de solicitação de validação.

</dd> <dt>

*hintTimeOutInMsec* \[ Em\]
</dt> <dd>

A duração, em milissegundos, do período de tempo de tempo de comunicação. O SHV (Validador de Saúde do Sistema) deve responder dentro desse período de tempo; caso contrário, a resposta será descartado.

> [!Note]  
> O tempo de vida padrão para todos os SHVs é de 2.000 milissegundos. O uso de um valor diferente do padrão alterará o tempo máximo de todas as SHVs registradas.

 

</dd> <dt>

*retorno de chamada* \[ Em\]
</dt> <dd>

Um ponteiro para o objeto de retorno de chamada [**INapServerCallback**](inapservercallback.md). Esse ponteiro de retorno de chamada é usado pelos SHVs quando **retornam E \_ PENDING** da chamada para **INapSystemHealthValidator::Validate**. Isso é usado para validação assíncrona. Espera-se que os SHVs respondam *dentro do horário hintTimeOutInMsec* ou a resposta será descartado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se qualquer outro código de erro for retornado, o sistema assumirá que ocorreu uma falha de serverComponent e o mapeamento apropriado será feito para passar/falhar.



| Código de retorno                                                                                                | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Indica que o validador definiu um SoHResponse no objeto 'request'.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**E \_ PENDENTE**</dt> </dl>                  | Indica que OnComplete() será chamado em um thread separado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>**SERVIDOR RPC \_ S \_ \_ INDISPONÍVEL**</dt> </dl> | Indica que o processo de SHV (Validador de Saúde do Sistema) foi encerrado sem o NapServer realmente liberar uma referência a ele. O NapServer tentará criar novamente uma nova referência para o SHV e reexecute a chamada Validar uma vez. Se a criação do objeto ou a Validação executada de novo falhar, o SHV será removido da lista de SHVs carregados. A única maneira de recarregar esse SHV agora é desregulamentar e fazer o registro novamente do SHV ou quando o NapServer for reiniciado<br/> |



 

## <a name="remarks"></a>Comentários

Para dar suporte à detecção de intrusão, os SHVs serão solicitados a validar o computador cliente, independentemente de o cliente ter enviado um [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) destinado ao SHV.

O SHV deve fazer o seguinte:

-   Recupere o [**SoHRequest da solicitação**](/windows/win32/api/naptypes/ns-naptypes-soh) *chamando* [**solicitação. GetSoHRequest().**](inapsystemhealthvalidationrequest-getsohrequest-method.md)
-   Se o [**pacote SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) for nulo:
    -   Se o SHV for um sistema de detecção de intrusão, preencha um pacote [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) com o código de erro [**NAP**](nap-error-constants.md) apropriado para saber por que o computador cliente é mal-intencionado.
    -   Todos os outros SHVs devem preencher um pacote [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) com um código de erro [**NAP E MISSING \_ \_ \_ SOH**](nap-error-constants.md).
-   Se *napSystemGenerated* for **TRUE** da chamada à [**solicitação. GetSoHRequest()**](inapsystemhealthvalidationrequest-getsohrequest-method.md), o SHV deve esperar um pacote [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) com os três TLVs a seguir: [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md), **sohAttributeTypeFailureCategory**, **sohAttributeTypeErrorCodes**. Esse **SoHRequest** é gerado pelo NapAgent em nome do SHA (Agente de Saúde do Sistema), pois houve um erro ao recuperar um pacote de solicitação do SHA.
-   Valide o [**pacote SoHRequest.**](/windows/win32/api/naptypes/ns-naptypes-soh)
    -   Se o [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) estiver malformado, construa um pacote **SoHResponse** com o código de erro [**NAP E INVALID \_ \_ \_ PACKET**](nap-error-constants.md).
    -   Se o SHV estiver usando apenas informações armazenadas em cache para validar o pacote [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) (ou seja, nenhuma E/S  é executada), ele poderá construir o **SoHResponse**, defini-lo no objeto na solicitação e retornar **S \_ OK.**
    -   Se o SHV estiver executando E/S para se falar com seus servidores de back-end para validar a saúde do cliente, ele deverá enfilfilar a E/S e retornar essa função **com E \_ PENDENTE.** Nesse caso, o SHV deve chamar [**o retorno de chamada. OnComplete() em**](inapservercallback-oncomplete-method.md) um thread separado dentro do período de tempoout, *hintTimeOutInMsec.* Caso contrário, a resposta do SHV será descartado.
-   Não retorne nenhum outro erro diferente daqueles listados acima. Se qualquer outro código de erro for retornado pelo SHV (por exemplo, algum erro do sistema), o pacote será descartado.

Um SHV deve retornar um **sohAttributeTypeComplianceResultCodes** ou **sohAttributeTypeFailureCategory** TLV em [**seu SoHRequest.**](/windows/win32/api/naptypes/ns-naptypes-soh)

-   [**sohAttributeTypeComplianceResultCodes TLV:**](sohattributetype-enum.md)se o SHV puder validar a saúde do cliente (ou seja, health ou unhealthy), esse TLV será retornado.
-   [**sohAttributeTypeFailureCategory TLV:**](sohattributetype-enum.md)se houve alguma falha de comunicação ou componente no cliente ou servidor, ele deve ser indicado por esse TLV. Esse TLV será mapeado ainda mais para healthy ou unhealthy, dependendo da configuração do SHV. Para obter mais detalhes, consulte a interface [**INapServerManagement**](inapservermanagement.md) e a [**estrutura FailureCategoryMapping.**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping)

O SHV não deve conter referências para *solicitar ou* retorno *de chamada* depois que a chamada assíncrona for concluída.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                               |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                    |
| Cabeçalho<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSystemHealthValidator**](inapsystemhealthvalidator.md)
</dt> </dl>

 

 





