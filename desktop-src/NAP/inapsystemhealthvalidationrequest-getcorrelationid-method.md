---
title: Método CorrelationId INapSystemHealthValidationRequest (NapSystemHealthValidator. h)
description: É usado por SHVs (validadores da integridade do sistema) para recuperar a ID de correlação. Em seguida, o SHV deve registrar essas informações.
ms.assetid: 72603d24-219e-4bb0-9b2b-b58d42939da8
keywords:
- Método CorrelationId NAP
- Método CorrelationId NAP, interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, método CorrelationId
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetCorrelationId
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1095a2c3eec90ff33613b6d37b43f31fdabd107
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455063"
---
# <a name="inapsystemhealthvalidationrequestgetcorrelationid-method"></a>Método INapSystemHealthValidationRequest:: CorrelationId

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSystemHealthValidationRequest:: CorrelationId** é usado pelos SHVs (validadores da integridade do sistema) para recuperar a ID de correlação. Em seguida, o SHV deve registrar essas informações.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CorrelationId* \[ fora\]
</dt> <dd>

Um ponteiro para uma [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) exclusiva para a troca soh.

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

 

 





