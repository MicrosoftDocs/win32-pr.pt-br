---
title: Método INapSystemHealthAgentRequest GetStringCorrelationId (NapSystemHealthAgent. h)
description: É usado pelos agentes de integridade do sistema para registrar a ID de correlação.
ms.assetid: 5d6f2392-2ada-474a-b150-31e0583c2ea7
keywords:
- Método GetStringCorrelationId NAP
- Método GetStringCorrelationId NAP, interface INapSystemHealthAgentRequest
- INapSystemHealthAgentRequest interface NAP, método GetStringCorrelationId
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetStringCorrelationId
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f33e98ae4b0fd76d97e85fb3588bcd1f2d33fd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644501"
---
# <a name="inapsystemhealthagentrequestgetstringcorrelationid-method"></a>Método INapSystemHealthAgentRequest:: GetStringCorrelationId

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSystemHealthAgentRequest:: GetStringCorrelationId** é usado pelos agentes de integridade do sistema para registrar a ID de correlação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetStringCorrelationId(
  [out] StringCorrelationId **correlationId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CorrelationId* \[ fora\]
</dt> <dd>

Um ponteiro para um ponteiro para uma [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) exclusiva para essa troca soh.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operação bem-sucedida.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                |
| parâmetro<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





