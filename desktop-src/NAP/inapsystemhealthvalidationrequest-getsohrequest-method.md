---
title: Método INapSystemHealthValidationRequest GetSoHRequest (NapSystemHealthValidator.h)
description: Permite que os SHVs (Validadores de Saúde do Sistema) recuperem e validem as informações do SoHRequest enviadas por seus equivalentes do SHA (System Health Agent) no cliente.
ms.assetid: e06e07c6-7305-4171-b94e-19c360e94c67
keywords:
- NAP do método GetSoHRequest
- Método GetSoHRequest NAP, interface INapSystemHealthValidationRequest
- Interface NAP INapSystemHealthValidationRequest , método GetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetSoHRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9c140af202de263e99f0fa8ec72186da6e995ec
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882616"
---
# <a name="inapsystemhealthvalidationrequestgetsohrequest-method"></a>Método INapSystemHealthValidationRequest::GetSoHRequest

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O método **INapSystemHealthValidationRequest::GetSoHRequest** permite que os SHVs (Validadores de Saúde do Sistema) recuperem e validem as informações [**do SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) enviadas por seus equivalentes do SHA (System Health Agent) no cliente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest,
  [out] BOOL       *napSystemGenerated
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sohRequest* \[ out\]
</dt> <dd>

Um ponteiro para um ponteiro para uma [**estrutura SoHRequest.**](/windows/win32/api/naptypes/ns-naptypes-soh)

</dd> <dt>

*napSystemGenerated* \[ out\]
</dt> <dd>

Um **BOOL** que será **TRUE se** o SoH tiver sido criado pelo NapAgent em nome do SHA e **FALSE,** caso contrário. Ele é usado principalmente para indicar uma falha SHA para o SHV.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos do COM também podem ser retornados.



| Código de retorno                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Êxito na operação.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite de recursos do sistema, não foi possível executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

O *parâmetro sohRequest* pode retornar **NULL** se o cliente não enviou um [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) para o SHV. Nesse cenário, o SHV pode popular um **SoHResponse** com o código de erro [**NAP E MISSING \_ \_ \_ SOH**](nap-error-constants.md).

Se o *parâmetro napSystemGenerated* for **TRUE**, o formato *de SoHRequest* será o seguinte:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) =  &lt; Id&gt;
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **&lt; sha-failure-error-code &gt;**](nap-error-constants.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                               |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                    |
| Cabeçalho<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





