---
title: Método INapSystemHealthAgentRequest SetSoHRequest (NapSystemHealthAgent. h)
description: É usado pelos agentes de integridade para gravar sua solicitação SoH resultante da chamada para INapSystemHealthAgentCallback GetSoHRequest.
ms.assetid: 76471cf2-e5df-4e07-b872-ccac0fd45998
keywords:
- Método SetSoHRequest NAP
- Método SetSoHRequest NAP, interface INapSystemHealthAgentRequest
- INapSystemHealthAgentRequest interface NAP, método SetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.SetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0fd1dcccad2a402d8455bcdf4f66052d41160b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105751414"
---
# <a name="inapsystemhealthagentrequestsetsohrequest-method"></a>Método INapSystemHealthAgentRequest:: SetSoHRequest

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSystemHealthAgentRequest:: SetSoHRequest** é usado pelos agentes de integridade para gravar sua solicitação soh resultante da chamada para [**INapSystemHealthAgentCallback:: GetSoHRequest**](inapsystemhealthagentcallback-getsohrequest-method.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetSoHRequest(
  [in] const SoHRequest *sohRequest,
  [in]       BOOL       cacheSohForLaterUse
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sohRequest* \[ no\]
</dt> <dd>

Um ponteiro para um pacote [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) .

</dd> <dt>

*cacheSohForLaterUse* \[ no\]
</dt> <dd>

Um **bool** que é **verdadeiro** se o NapAgent deve armazenar em cache a [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) e **false** caso contrário.

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
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                |
| parâmetro<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





