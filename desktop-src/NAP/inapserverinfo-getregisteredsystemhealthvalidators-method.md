---
title: Método INapServerInfo GetRegisteredSystemHealthValidators (NapServerManagement.h)
description: Recupera uma lista de SHVs registrados.
ms.assetid: 029c7d5c-b397-415c-a530-0096de1ef771
keywords:
- Método NAP GetRegisteredSystemHealthValidators
- Método NAP GetRegisteredSystemHealthValidators, interface INapServerInfo
- Nap da interface INapServerInfo, método GetRegisteredSystemHealthValidators
topic_type:
- apiref
api_name:
- INapServerInfo.GetRegisteredSystemHealthValidators
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54e096d706107ca812e569e46c980f56cdc7b8eba14f4742530f632570fd3d08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133941"
---
# <a name="inapserverinfogetregisteredsystemhealthvalidators-method"></a>Método INapServerInfo::GetRegisteredSystemHealthValidators

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método INapServerInfo::GetRegisteredSystemHealthValidators** recupera uma lista de SHVs registrados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRegisteredSystemHealthValidators(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **validators,
  [out] CLSID                        **validatorClsids
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*count* \[ out\]
</dt> <dd>

Um ponteiro para [**um SystemHealthEntityCount**](nap-type-constants.md) que contém o número de SHVs registradas.

</dd> <dt>

*validadores* \[ out\]
</dt> <dd>

Um ponteiro para um ponteiro para uma [**estrutura NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que contém as informações de registro shv.

</dd> <dt>

*validatorClsids* \[ out\]
</dt> <dd>

Ponteiro para uma matriz de IDs para os SHVs registrados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos do COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Êxito na operação.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite de recursos do sistema, não foi possível executar a operação.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                               |
| Cabeçalho<br/>                   | <dl> <dt>NapServerManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapServerManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo)
</dt> <dt>

[**INapServerInfo**](inapserverinfo.md)
</dt> </dl>

 

 





