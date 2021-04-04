---
title: Método INapSystemHealthAgentRequest GetSoHResponse (NapSystemHealthAgent. h)
description: É usado pelo agente de integridade para recuperar seu blob SoHResponse quando o NapAgent chama INapSystemHealthAgentCallback ProcessSoHResponse.
ms.assetid: 60319256-d5c2-46cc-a59b-f81732e21a7f
keywords:
- Método GetSoHResponse NAP
- Método GetSoHResponse NAP, interface INapSystemHealthAgentRequest
- INapSystemHealthAgentRequest interface NAP, método GetSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHResponse
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d593ff897e69b86b554365561e43308adead5250
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085370"
---
# <a name="inapsystemhealthagentrequestgetsohresponse-method"></a>Método INapSystemHealthAgentRequest:: GetSoHResponse

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSystemHealthAgentRequest:: GetSoHResponse** é usado pelo agente de integridade para recuperar seu blob SoHResponse quando o NapAgent chama [**INapSystemHealthAgentCallback::P rocesssohresponse**](inapsystemhealthagentcallback-processsohresponse-method.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse,
  [out] UINT8       *flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sohResponse* \[ fora\]
</dt> <dd>

Um ponteiro para um ponteiro para um pacote [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) .

</dd> <dt>

*sinalizadores* \[ de fora\]
</dt> <dd>

Um ponteiro para um sinalizador que habilita a correção pelo SHA se o bit [**shaFixup**](nap-type-constants.md) for definido, caso contrário, a correção será desabilitada.



| Valores possíveis                                                                                                                                                          | Significado                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span><dl> <dt>**shaFixup**</dt> </dl> | Espera-se que o SHA execute a correção com base na resposta. Se esse sinalizador não for definido, o SHA não deverá executar uma correção, mesmo que o [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) indique que ele não está íntegro.<br/> |



 

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

 

 





