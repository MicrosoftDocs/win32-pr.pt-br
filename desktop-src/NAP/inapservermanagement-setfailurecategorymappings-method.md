---
title: Método INapServerManagement SetFailureCategoryMappings (NapServerManagement.h)
description: É usado para definir os mapeamentos de categoria de falha do SHV.
ms.assetid: be482f82-c79c-405c-b619-9bcb9b4dc349
keywords:
- Método NAP SetFailureCategoryMappings
- Método NAP SetFailureCategoryMappings, interface INapServerManagement
- INapServerManagement interface NAP , método SetFailureCategoryMappings
topic_type:
- apiref
api_name:
- INapServerManagement.SetFailureCategoryMappings
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c22bc51edf887d26bf34f59932248c62bfca86199771a2b971a10e9c1b323eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939610"
---
# <a name="inapservermanagementsetfailurecategorymappings-method"></a>Método INapServerManagement::SetFailureCategoryMappings

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método INapServerManagement::SetFailureCategoryMappings** é usado para definir os mapeamentos de categoria de falha do SHV.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetFailureCategoryMappings(
  [in]       SystemHealthEntityId   id,
  [in] const FailureCategoryMapping mapping
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ID* \[ em\]
</dt> <dd>

Um [**SystemHealthEntityId**](nap-type-constants.md) que contém o identificador exclusivo do SHV.

</dd> <dt>

*mapeamento* \[ Em\]
</dt> <dd>

Uma [**estrutura FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) que contém os dados de mapeamento de categoria de falha.

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

[**INapServerManagement**](inapservermanagement.md)
</dt> </dl>

 

 





