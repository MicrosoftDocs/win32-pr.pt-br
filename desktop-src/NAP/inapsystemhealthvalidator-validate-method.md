---
title: Método de validação de INapSystemHealthValidator (NapSystemHealthValidator. h)
description: O sistema NAP para validar o SoHRequest recebido de um cliente.
ms.assetid: d67dc2c8-f18c-4e06-a51e-a538ca75c3f1
keywords:
- Validar método NAP
- Validar método NAP, interface INapSystemHealthValidator
- INapSystemHealthValidator interface NAP, método Validate
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
ms.openlocfilehash: 4f7589a67b9a3b1454e3c65b17ad6f584ce0e655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779610"
---
# <a name="inapsystemhealthvalidatorvalidate-method"></a>Método INapSystemHealthValidator:: Validate

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSystemHealthValidator:: Validate** é definido pelo desenvolvedor SHV e chamado pelo sistema NAP para validar o [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) recebido de um cliente.

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

*solicitação* \[ do no\]
</dt> <dd>

Um ponteiro COM para um objeto [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) que identifica o objeto de solicitação de validação.

</dd> <dt>

*hintTimeOutInMsec* \[ no\]
</dt> <dd>

A duração, em milissegundos, do período de tempo limite de comunicação. O SHV (validador da integridade do sistema) deve responder dentro desse período de tempo; caso contrário, a resposta será descartada.

> [!Note]  
> O tempo limite padrão para todos os SHVs é de 2000 milissegundos. Usar um valor diferente do padrão irá alterar o tempo limite de todos os SHVs registrados.

 

</dd> <dt>

*retorno de chamada* \[ no\]
</dt> <dd>

Um ponteiro para o objeto de retorno de chamada [**INapServerCallback**](inapservercallback.md). Esse ponteiro de retorno de chamada é usado pelos SHVs quando eles retornam **E \_ pendentes** da chamada para **INapSystemHealthValidator:: Validate**. Isso é usado para validação assíncrona. Espera-se que os SHVs respondam dentro do horário *hintTimeOutInMsec* ou que a resposta seja descartada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se qualquer outro código de erro for retornado, o sistema assumirá que ocorreu uma falha serverComponent e o mapeamento apropriado será feito para ser aprovado/reprovado.



| Código de retorno                                                                                                | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Indica que o validador definiu um SoHResponse no objeto ' request '.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**E \_ pendente**</dt> </dl>                  | Indica que OnComplete () será chamado em um thread separado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>**\_servidor RPC \_ S \_ não disponível**</dt> </dl> | Indica que o processo do validador da integridade do sistema (SHV) foi encerrado sem o NapServer de fato liberar uma referência a ele. O NapServer tentará recriar uma nova referência para o SHV e executará novamente a chamada Validate uma vez. Se a criação do objeto ou a validação de reexecução falhar, o SHV será removido da lista de SHVs carregados. A única maneira de que esse SHV agora pode ser recarregado é cancelar o registro e registrar novamente o SHV novamente ou quando o NapServer é reiniciado<br/> |



 

## <a name="remarks"></a>Comentários

Para dar suporte à detecção de intrusão, os SHVs serão solicitados a validar o computador cliente, independentemente de o cliente ter enviado um [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) destinado ao SHV.

O SHV deve fazer o seguinte:

-   Recupere o [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) da *solicitação* chamando [**solicitação. GetSoHRequest ()**](inapsystemhealthvalidationrequest-getsohrequest-method.md).
-   Se o pacote [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) for nulo:
    -   Se o SHV for um sistema de detecção de intrusão, preencha um pacote [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) com o [**código de erro NAP**](nap-error-constants.md) apropriado para o motivo pelo qual o computador cliente é mal-intencionado.
    -   Todos os outros SHVs devem preencher um pacote [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) com um código de erro de [**NAP \_ E \_ faltando \_ soh**](nap-error-constants.md).
-   Se *napSystemGenerated* for **true** da chamada a [**Request. GetSoHRequest ()**](inapsystemhealthvalidationrequest-getsohrequest-method.md), o SHV deve esperar um pacote [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) com os seguintes 3 TLVs: [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md), **sohAttributeTypeFailureCategory**, **sohAttributeTypeErrorCodes**. Esse **SoHRequest** é gerado pelo NapAgent em nome do Sha (agente de integridade do sistema), já que houve um erro na recuperação de um pacote de solicitação do Sha.
-   Valide o pacote [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) .
    -   Se o [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) estiver malformado, construa um pacote **SoHResponse** com código de erro [**NAP \_ E \_ \_ pacote inválido**](nap-error-constants.md).
    -   Se o SHV estiver usando apenas informações armazenadas em cache para validar o pacote [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) (ou seja, nenhuma e/s é executada), ele poderá construir o **SoHResponse**, defini-lo no objeto na *solicitação* e retornar **S \_ OK**.
    -   Se o SHV estiver executando e/s para se comunicar com seus servidores back-end para validar a integridade do cliente, ele deverá enfileirar a e/s e retornar essa função com **E \_ pendente**. Nesse caso, o SHV deve chamar o [**retorno de chamada. OnComplete ()**](inapservercallback-oncomplete-method.md) em um thread separado dentro do período de tempo limite, *hintTimeOutInMsec*. Caso contrário, a resposta do SHV será descartada.
-   Não retornar outro erro além daqueles listados acima. Se qualquer outro código de erro for retornado pelo SHV (por exemplo, algum erro do sistema), o pacote será Descartado.

Um SHV deve retornar um TLV **sohAttributeTypeComplianceResultCodes** ou **SohAttributeTypeFailureCategory** em seu [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).

-   [**TLV sohAttributeTypeComplianceResultCodes**](sohattributetype-enum.md): se o SHV puder validar a integridade do cliente (ou seja, íntegro ou não íntegro), esse TLV será retornado.
-   [**TLV sohAttributeTypeFailureCategory**](sohattributetype-enum.md): se houvesse alguma falha de componente ou de comunicação no cliente ou servidor, ele deve ser indicado por esse TLV. Esse TLV será mapeado para ser íntegro ou não íntegro dependendo da configuração do SHV. Para obter mais detalhes, consulte a interface [**INapServerManagement**](inapservermanagement.md) e a estrutura [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) .

O SHV não deve manter referências a *solicitação* ou *retorno* de chamada quando a chamada asyncronous for concluída.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                    |
| parâmetro<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSystemHealthValidator**](inapsystemhealthvalidator.md)
</dt> </dl>

 

 





