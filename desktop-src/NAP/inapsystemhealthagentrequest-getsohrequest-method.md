---
title: Método INapSystemHealthAgentRequest GetSoHRequest (NapSystemHealthAgent. h)
description: Pode ser usado por SHAs Get SoHs anteriormente armazenado em cache pelo NapAgent.
ms.assetid: 187a4513-79db-45cb-8d64-6a92a2d3b004
keywords:
- Método GetSoHRequest NAP
- Método GetSoHRequest NAP, interface INapSystemHealthAgentRequest
- INapSystemHealthAgentRequest interface NAP, método GetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab52e52c952c2dc1f891098e10c3ecb688052295
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009694"
---
# <a name="inapsystemhealthagentrequestgetsohrequest-method"></a>Método INapSystemHealthAgentRequest:: GetSoHRequest

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSystemHealthAgentRequest:: GetSoHRequest** pode ser usado por SHAs Get SoHs armazenado em cache anteriormente pelo NapAgent.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sohRequest* \[ fora\]
</dt> <dd>

Um ponteiro para um ponteiro para um [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                            | Descrição                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Operação bem-sucedida.<br/>                                        |
| <dl> <dt>**NAP \_ E \_ nenhum \_ soh armazenado em cache \_**</dt> </dl> | A SoH não foi encontrada; NapAgent não tem uma cópia armazenada em cache.<br/> |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Erro de permissões, acesso negado.<br/>                           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | O limite de recursos do sistema não pôde executar a operação.<br/>     |



 

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

 

 





