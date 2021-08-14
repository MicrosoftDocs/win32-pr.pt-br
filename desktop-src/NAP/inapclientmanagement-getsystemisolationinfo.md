---
title: Método INapClientManagement GetSystemIsolationInfo (NapManagement.h)
description: Recupera informações sobre o estado de isolamento do NapClient.
ms.assetid: e1f69e66-71ca-402e-9c94-8af159d00b21
keywords:
- Nap do método GetSystemIsolationInfo
- Método GetSystemIsolationInfo NAP, interface INapClientManagement
- INapClientManagement interface NAP , método GetSystemIsolationInfo
topic_type:
- apiref
api_name:
- INapClientManagement.GetSystemIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9414bb5f2d193aa8f7636b94925914afb7eb123d3b497fdc50d20498fa104fc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368700"
---
# <a name="inapclientmanagementgetsystemisolationinfo-method"></a>Método INapClientManagement::GetSystemIsolationInfo

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método GetSystemIsolationInfo** recupera informações sobre o estado de isolamento do NapClient.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
) const;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*isolationInfo* \[ out\]
</dt> <dd>

Um ponteiro para um ponteiro para uma estrutura [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) que contém informações de estado de isolamento.

</dd> <dt>

*unknownConnections* \[ out\]
</dt> <dd>

Um ponteiro para um sinalizador que indica se qualquer uma das conexões está em um estado desconhecido. Se algum deles for, o sinalizador será definido como **TRUE;** caso contrário, o sinalizador será definido como **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um código de status HRESULT, incluindo, mas não limitado a um dos seguintes.



| Código de retorno                                                                                         | Descrição                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Operação concluída com êxito.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Limite de recursos do sistema, não foi possível executar a operação.<br/> |
| <dl> <dt>**RPC \_ E \_ DESCONECTADO**</dt> </dl> | O NapAgent não está em execução.<br/>                            |



 

## <a name="remarks"></a>Comentários

As informações de isolamento recuperadas não refletem estados desconhecidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                         |
| Cabeçalho<br/>                   | <dl> <dt>NapManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 





