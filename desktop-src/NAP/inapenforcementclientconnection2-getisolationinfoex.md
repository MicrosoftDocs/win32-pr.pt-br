---
title: Método INapEnforcementClientConnection2 GetIsolationInfoEx (NapEnforcementClient.h)
description: É usado para obter informações de isolamento sobre o cliente.
ms.assetid: ebacd056-5ab8-4096-821c-8f2987d853c4
keywords:
- Nap do método GetIsolationInfoEx
- Método GetIsolationInfoEx NAP, interface INapEnforcementClientConnection2
- INapEnforcementClientConnection2 interface NAP , método GetIsolationInfoEx
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb89cc4a5fed046173ebdef2d5ed38574e52648fddd5cb357d8726c07581f51b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368049"
---
# <a name="inapenforcementclientconnection2getisolationinfoex-method"></a>Método INapEnforcementClientConnection2::GetIsolationInfoEx

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método INapEnforcementClientConnection2::GetIsolationInfoEx** é usado para obter informações de isolamento sobre o cliente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo
) const;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*isolationInfo* \[ out\]
</dt> <dd>

Um ponteiro para um ponteiro para uma estrutura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) que contém a conectividade e as informações de estado estendido do cliente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos do COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Êxito na operação.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite de recursos do sistema, não foi possível executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

Essas informações são definidas pelo NapAgent após o processamento [**de um SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) e não devem ser definidas pelo executor.

O SHA deve liberar a estrutura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) chamando [**FreeIsolationInfoEx.**](freeisolationinfoex.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





