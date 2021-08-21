---
title: Método GetMachineName de INapSystemHealthValidationRequest (NapSystemHealthValidator. h)
description: É usado por SHVs (validadores da integridade do sistema) para recuperar o nome do computador do cliente NAP. Em seguida, o SHV registra essas informações.
ms.assetid: 2ea6a65d-1579-4a05-b5bc-aebf6421e46a
keywords:
- Método GetMachineName NAP
- Método GetMachineName NAP, interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, método GetMachineName
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetMachineName
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7229dd71dd9638de1eaf09ccdcf111e562d4ae346d528d7f2133d3d48d010d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799171"
---
# <a name="inapsystemhealthvalidationrequestgetmachinename-method"></a>Método INapSystemHealthValidationRequest:: GetMachineName

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSystemHealthValidationRequest:: GetMachineName** é usado pelos SHVs (validadores da integridade do sistema) para recuperar o nome do computador do cliente NAP. Em seguida, o SHV registra essas informações.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetMachineName(
  [out] CountedString **machineName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MachineName* \[ fora\]
</dt> <dd>

Um ponteiro para um ponteiro para uma estrutura de [**contadostring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contém o nome do computador do cliente NAP.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Êxito na operação.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

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

 

 





