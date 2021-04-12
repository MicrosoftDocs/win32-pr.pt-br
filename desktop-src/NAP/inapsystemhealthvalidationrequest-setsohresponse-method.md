---
title: Método INapSystemHealthValidationRequest SetSoHResponse (NapSystemHealthValidator. h)
description: Permite que os SHVs (validadores da integridade do sistema) definam o SoHResponse a ser enviado para seu equivalente de SHA (agente de integridade do sistema) no lado do cliente.
ms.assetid: 250b90ac-ce8f-4771-9d20-84c491adfb2c
keywords:
- Método SetSoHResponse NAP
- Método SetSoHResponse NAP, interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, método SetSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.SetSoHResponse
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b818218ef4f8601ecf4927f5e8b90f93e5386b56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369814"
---
# <a name="inapsystemhealthvalidationrequestsetsohresponse-method"></a>Método INapSystemHealthValidationRequest:: SetSoHResponse

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSystemHealthValidationRequest:: SetSoHResponse** permite que os SHVs (validadores da integridade do sistema) definam o [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) a ser enviado à sua contraparte do agente de integridade do sistema (SHA) no lado do cliente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetSoHResponse(
  [in] const SoHResponse *sohResponse
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sohResponse* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operação bem-sucedida.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                    |
| parâmetro<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





