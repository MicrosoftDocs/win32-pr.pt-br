---
title: Método INapSystemHealthValidationRequest GetPrivateData (NapSystemHealthValidator.h)
description: Permite que o NapServer recupere informações de estado.
ms.assetid: f85026ca-852b-4eb1-9a8c-7e03cd1765f2
keywords:
- NAP do método GetPrivateData
- Método GetPrivateData NAP, interface INapSystemHealthValidationRequest
- Interface NAP INapSystemHealthValidationRequest , método GetPrivateData
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetPrivateData
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ea94e3f03b3816cfb62f51263d5a5f9c67cf903b7e24991fa7a0f5d06427a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780756"
---
# <a name="inapsystemhealthvalidationrequestgetprivatedata-method"></a>Método INapSystemHealthValidationRequest::GetPrivateData

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método INapSystemHealthValidationRequest::GetPrivateData** permite que o NapServer recupere informações de estado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*privateData* \[ out\]
</dt> <dd>

Um ponteiro para um ponteiro para o blob de dados opaco [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) que contém informações de estado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos do COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Êxito na operação.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite de recursos do sistema, não foi possível executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

Somente o NapServer pode interpretar o blob de dados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                               |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                    |
| Cabeçalho<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





