---
title: Método INapSystemHealthValidationRequest GetSoHRequest (NapSystemHealthValidator. h)
description: Permite que os SHVs (validadores da integridade do sistema) recuperem e validem as informações de SoHRequest enviadas por seus equivalentes de SHA (agente de integridade do sistema) no cliente.
ms.assetid: e06e07c6-7305-4171-b94e-19c360e94c67
keywords:
- Método GetSoHRequest NAP
- Método GetSoHRequest NAP, interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, método GetSoHRequest
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
ms.openlocfilehash: dc9d9dc3b28aec92b7125dc2cad6bf8b843975945ca89687957d56be0ff562d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367724"
---
# <a name="inapsystemhealthvalidationrequestgetsohrequest-method"></a>Método INapSystemHealthValidationRequest:: GetSoHRequest

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSystemHealthValidationRequest:: GetSoHRequest** permite que os SHVs (validadores da integridade do sistema) recuperem e validem as informações de [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) enviadas por suas contrapartes do Sha (agente de integridade do sistema) no cliente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest,
  [out] BOOL       *napSystemGenerated
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sohRequest* \[ fora\]
</dt> <dd>

Um ponteiro para um ponteiro para uma estrutura [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) .

</dd> <dt>

*napSystemGenerated* \[ fora\]
</dt> <dd>

Um **bool** que é **verdadeiro** se a soh foi criada pelo NAPAGENT em nome do Sha e **false** caso contrário. Ele é usado principalmente para indicar uma falha de SHA para o SHV.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Êxito na operação.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

O parâmetro *sohRequest* pode retornar **NULL** se o cliente não enviou um [**sohRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) para o SHV. Nesse cenário, o SHV pode popular um **SoHResponse** com o código de erro de [**NAP \_ E \_ faltando \_ soh**](nap-error-constants.md).

Se o parâmetro *napSystemGenerated* for **true**, o formato de *SoHRequest* será o seguinte:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **<Sha-falha-erro-código>**](nap-error-constants.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                               |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                    |
| Cabeçalho<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





