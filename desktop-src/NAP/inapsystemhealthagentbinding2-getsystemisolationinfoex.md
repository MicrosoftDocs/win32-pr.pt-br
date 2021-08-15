---
title: Método INapSystemHealthAgentBinding2 GetSystemIsolationInfoEx (NapSystemHealthAgent.h)
description: É chamado por SHAs para determinar o estado de isolamento do sistema e o estado de isolamento estendido.
ms.assetid: 237e5539-889c-457d-8db0-bf3379f28b85
keywords:
- Nap do método GetSystemIsolationInfoEx
- Método GetSystemIsolationInfoEx NAP, interface INapSystemHealthAgentBinding2
- INapSystemHealthAgentBinding2 interface NAP , método GetSystemIsolationInfoEx
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ac81d00bb953ddf3ab415e90724adcca34b302d8cc268699d8f2a820e0f34ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367824"
---
# <a name="inapsystemhealthagentbinding2getsystemisolationinfoex-method"></a>Método INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx** é chamado por SHAs para determinar o estado de isolamento do sistema e o estado de isolamento estendido.

> [!Note]  
> Use [**INapSystemHealthAgentBinding::GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) para determinar apenas o estado de isolamento do sistema.

 

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

Um ponteiro para um ponteiro para uma estrutura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) que contém o estado de isolamento estendido do sistema para conexões conhecidas. *isolationInfo* indica se o sistema está em um estado de acesso restrito, isolamento ou acesso irrestrito, bem como informações de [**ExtendedIsolationState.**](/windows/win32/api/naptypes/ne-naptypes-extendedisolationstate)

</dd> <dt>

*unknownConnections* \[ out\]
</dt> <dd>

Um ponteiro para um **BOOL** que será **TRUE se** qualquer conexão estiver em um estado desconhecido e **FALSE** caso contrário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos do COM também podem ser retornados.



| Código de retorno                                                                                             | Descrição                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Êxito na operação.<br/>                                                                                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Erro de permissões, acesso negado.<br/>                                                                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Limite de recursos do sistema, não foi possível executar a operação.<br/>                                                             |
| <dl> <dt>**NAP \_ E \_ NÃO \_ INICIALIZADO**</dt> </dl> | O SHA não foi inicializado anteriormente.<br/>                                                                        |
| <dl> <dt>**RPC \_ E \_ DESCONECTADO**</dt> </dl>     | O NapAgent foi interrompido. Esse objeto será recuperado automaticamente e reabinado ao NapAgent, depois que ele for reiniciado.<br/> |



 

## <a name="remarks"></a>Comentários

O SHA deve liberar a estrutura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) chamando [**FreeIsolationInfoEx.**](freeisolationinfoex.md)

O SHA deve chamar [**Inicializar**](inapsystemhealthagentbinding-initialize-method.md) antes de chamar esse método ou qualquer outro método da interface [**INapSystemHealthAgentBinding2.**](inapsystemhealthagentbinding2.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)
</dt> </dl>

 

 





