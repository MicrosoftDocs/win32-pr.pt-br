---
title: Método INapSystemHealthValidationRequest GetPrivateData (NapSystemHealthValidator. h)
description: Permite que o NapServer recupere informações de estado.
ms.assetid: f85026ca-852b-4eb1-9a8c-7e03cd1765f2
keywords:
- Método GetPrivateData NAP
- Método GetPrivateData NAP, interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, método GetPrivateData
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
ms.openlocfilehash: d78cceba42cd503ef8a875ece8f4ed196eaeff8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645111"
---
# <a name="inapsystemhealthvalidationrequestgetprivatedata-method"></a>Método INapSystemHealthValidationRequest:: GetPrivateData

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSystemHealthValidationRequest:: GetPrivateData** permite que o NapServer recupere informações de estado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*privateData* \[ fora\]
</dt> <dd>

Um ponteiro para um ponteiro para [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) blob de dados opaco que contém informações de estado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operação bem-sucedida.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

Somente o NapServer pode interpretar o blob de dados.

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

 

 





