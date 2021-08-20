---
title: Interface INapSystemHealthValidationRequest (NapSystemHealthValidator. h)
description: São usados para dar suporte a validadores de integridade do sistema que são definidos pelo desenvolvedor do aplicativo.
ms.assetid: faa91ff5-49f5-4aec-81d7-02ec59274f23
keywords:
- INapSystemHealthValidationRequest da interface NAP
- INapSystemHealthValidationRequest interface NAP, descrita
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e7b6b2fdc0da8757ddd29b963445c0b984c45d19955c093270cf397fcac14b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133471"
---
# <a name="inapsystemhealthvalidationrequest-interface"></a>Interface INapSystemHealthValidationRequest

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

A interface **INapSystemHealthValidationRequest** fornece métodos que são usados para dar suporte a validadores de integridade do sistema que são definidos pelo desenvolvedor do aplicativo.

> [!Note]  
> [**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) herda todos os métodos dessa interface e deve ser usado em seu lugar.

 

## <a name="members"></a>Membros

A interface **INapSystemHealthValidationRequest** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapSystemHealthValidationRequest** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapSystemHealthValidationRequest** tem esses métodos.



| Método                                                                                                                               | Descrição                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**INapSystemHealthValidationRequest:: CorrelationId**](inapsystemhealthvalidationrequest-getcorrelationid-method.md)             | Usado por validadores para recuperar a ID de correlação. Em seguida, o validador deve registrar essas informações.<br/>           |
| [**INapSystemHealthValidationRequest:: GetMachineName**](inapsystemhealthvalidationrequest-getmachinename-method.md)                 | Usado por validadores para recuperar o nome do computador. Em seguida, o validador deve registrar essas informações.<br/>             |
| [**INapSystemHealthValidationRequest::GetPrivateData**](inapsystemhealthvalidationrequest-getprivatedata-method.md)                 | Permite que o NapServer recupere informações de estado.<br/>                                                        |
| [**INapSystemHealthValidationRequest::GetSoHRequest**](inapsystemhealthvalidationrequest-getsohrequest-method.md)                   | Permite que os validadores recuperem e validem as informações de SoHRequest.<br/>                                     |
| [**INapSystemHealthValidationRequest::GetSoHResponse**](inapsystemhealthvalidationrequest-getsohresponse-method.md)                 | Obtém o objeto SoHResponse.<br/>                                                                               |
| [**INapSystemHealthValidationRequest::GetStringCorrelationId**](inapsystemhealthvalidationrequest-getstringcorrelationid-method.md) | Usado por validadores para recuperar um identificador de troca exclusivo. Em seguida, o validador deve registrar essas informações.<br/> |
| [**INapSystemHealthValidationRequest::SetPrivateData**](inapsystemhealthvalidationrequest-setprivatedata-method.md)                 | Permite que o NapServer armazene informações de estado.<br/>                                                           |
| [**INapSystemHealthValidationRequest::SetSoHResponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md)                 | Permite que os validadores definam o SoHResponse.<br/>                                                                  |



 

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

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referência de NAP](nap-reference.md)
</dt> </dl>

 

