---
title: Método INapClientManagement2 GetSystemIsolationInfoEx (NapManagement.h)
description: Recupera informações sobre o estado de isolamento e o estado de isolamento estendido do NapClient.
ms.assetid: 614bcf19-873e-4043-98b2-dcb152bae3e2
keywords:
- Nap do método GetSystemIsolationInfoEx
- Método GetSystemIsolationInfoEx NAP, interface INapClientManagement2
- INapClientManagement2 interface NAP , método GetSystemIsolationInfoEx
topic_type:
- apiref
api_name:
- INapClientManagement2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d03630cbd0647dc177460f92abc28e6aa66cbb663465ba7e9e93eefbc283ac00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621923"
---
# <a name="inapclientmanagement2getsystemisolationinfoex-method"></a>Método INapClientManagement2::GetSystemIsolationInfoEx

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método GetSystemIsolationInfoEx** recupera informações sobre o estado de isolamento e o estado de isolamento estendido do NapClient.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*isolationInfo* \[ out\]
</dt> <dd>

Um ponteiro para um ponteiro para uma estrutura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) que contém informações de estado de isolamento.

</dd> <dt>

*unknownConnections* \[ out\]
</dt> <dd>

Um ponteiro para um BOOL que será **TRUE se** qualquer uma das conexões estiver em um estado desconhecido e **FALSE** caso contrário.

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

O SHA deve liberar a estrutura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) chamando [**FreeIsolationInfoEx.**](freeisolationinfoex.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                         |
| parâmetro<br/>                   | <dl> <dt>NapManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapClientManagement2**](inapclientmanagement2.md)
</dt> </dl>

 

 





