---
title: Método INapServerManagement UnregisterSystemHealthValidator (NapServerManagement. h)
description: É usado para cancelar o registro de um SHV com o servidor NAP.
ms.assetid: f4148df1-a230-4845-ac8b-9e04be9e0d6c
keywords:
- Método UnregisterSystemHealthValidator NAP
- Método UnregisterSystemHealthValidator NAP, interface INapServerManagement
- INapServerManagement interface NAP, método UnregisterSystemHealthValidator
topic_type:
- apiref
api_name:
- INapServerManagement.UnregisterSystemHealthValidator
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0715445504b862d9ae9e8478b543f8e80378f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499658"
---
# <a name="inapservermanagementunregistersystemhealthvalidator-method"></a>Método INapServerManagement:: UnregisterSystemHealthValidator

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapServerManagement:: UnregisterSystemHealthValidator** é usado para cancelar o registro de um SHV com o servidor NAP.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UnregisterSystemHealthValidator(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ID* \[ em\]
</dt> <dd>

Um [**SystemHealthEntityId**](nap-type-constants.md) que contém o identificador exclusivo do SHV para cancelar o registro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operação bem-sucedida.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

Se houver qualquer chamada assíncrona pendente no SHV, elas serão concluídas posteriormente e serão descartadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                               |
| parâmetro<br/>                   | <dl> <dt>NapServerManagement. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapServerManagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapServerManagement**](inapservermanagement.md)
</dt> </dl>

 

 





