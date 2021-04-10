---
title: Método INapServerManagement RegisterSystemHealthValidator (NapServerManagement. h)
description: Registra um SHV.
ms.assetid: 23f147d5-3c4e-48ca-940a-c4350ad6ecb3
keywords:
- Método RegisterSystemHealthValidator NAP
- Método RegisterSystemHealthValidator NAP, interface INapServerManagement
- INapServerManagement interface NAP, método RegisterSystemHealthValidator
topic_type:
- apiref
api_name:
- INapServerManagement.RegisterSystemHealthValidator
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2abd8d42da196caa804a8919c6425fda9fcb950c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163630"
---
# <a name="inapservermanagementregistersystemhealthvalidator-method"></a>Método INapServerManagement:: RegisterSystemHealthValidator

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapServerManagement:: RegisterSystemHealthValidator** registra um SHV.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RegisterSystemHealthValidator(
  [in] const NapComponentRegistrationInfo *validator,
  [in] const CLSID                        *validatorClsid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*validador* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que contém as informações de registro de SHV.

</dd> <dt>

*validatorClsid* \[ no\]
</dt> <dd>

Um ponteiro para o CLSID da classe COM que implementa a interface [**INapSystemHealthValidator**](inapsystemhealthvalidator.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                            | Descrição                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Operação bem-sucedida.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | O limite de recursos do sistema não pôde executar a operação.<br/> |
| <dl> <dt>**NAP \_ E \_ ID conflitante \_**</dt> </dl> | A ID de SHV já está registrada.<br/>                           |



 

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

 

 





