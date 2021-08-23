---
title: Método GetFailureCategoryMappings de INapServerInfo (NapServerManagement.h)
description: Recupera os mapeamentos de categoria de falha para um SHA ou SHV especificado.
ms.assetid: 89b89003-40b3-4763-aec8-01cd0c307649
keywords:
- NAP do método GetFailureCategoryMappings
- Método NAP GetFailureCategoryMappings, interface INapServerInfo
- Método NAP da interface INapServerInfo, GetFailureCategoryMappings
topic_type:
- apiref
api_name:
- INapServerInfo.GetFailureCategoryMappings
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13fcd87105eace269d3b8f395392c8a0ba275a135c212863ef69e45e597eb752
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144379"
---
# <a name="inapserverinfogetfailurecategorymappings-method"></a>Método INapServerInfo::GetFailureCategoryMappings

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método INapServerInfo::GetFailureCategoryMappings** recupera os mapeamentos de categoria de falha para um SHA ou SHV especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetFailureCategoryMappings(
  [in]  SystemHealthEntityId   id,
  [out] FailureCategoryMapping *mapping
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ID* \[ em\]
</dt> <dd>

Um [**SystemHealthEntityId**](nap-type-constants.md) que contém o identificador exclusivo do SHA ou do SHV.

</dd> <dt>

*mapeamento* \[ out\]
</dt> <dd>

Um ponteiro para um [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) que contém os dados de mapeamento.

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

[**INapServerInfo**](inapserverinfo.md)
</dt> </dl>

 

 





