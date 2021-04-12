---
title: Método INapSystemHealthAgentBinding2 GetSystemIsolationInfoEx (NapSystemHealthAgent. h)
description: É chamado por SHAs para determinar o estado de isolamento do sistema e o estado de isolamento estendido.
ms.assetid: 237e5539-889c-457d-8db0-bf3379f28b85
keywords:
- Método GetSystemIsolationInfoEx NAP
- Método GetSystemIsolationInfoEx NAP, interface INapSystemHealthAgentBinding2
- INapSystemHealthAgentBinding2 interface NAP, método GetSystemIsolationInfoEx
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
ms.openlocfilehash: c2643d62afba1a35ebd96b8b39ea2fcf90397576
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499426"
---
# <a name="inapsystemhealthagentbinding2getsystemisolationinfoex-method"></a>Método INapSystemHealthAgentBinding2:: GetSystemIsolationInfoEx

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSystemHealthAgentBinding2:: GetSystemIsolationInfoEx** é chamado por SHAs para determinar o estado de isolamento do sistema e o estado de isolamento estendido.

> [!Note]  
> Use [**INapSystemHealthAgentBinding:: GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) para determinar apenas o estado de isolamento do sistema.

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*isolationInfo* \[ fora\]
</dt> <dd>

Um ponteiro para um ponteiro para uma estrutura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) que contém o estado de isolamento estendido do sistema para conexões conhecidas. *isolationInfo* indica se o sistema está em um estado de acesso restrito, experiência ou acesso irrestrito, bem como informações de [**ExtendedIsolationState**](/windows/win32/api/naptypes/ne-naptypes-extendedisolationstate) .

</dd> <dt>

*unknownConnections* \[ fora\]
</dt> <dd>

Um ponteiro para um **bool** que será **verdadeiro** se qualquer conexão estiver em um estado desconhecido e **false** caso contrário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                             | Descrição                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Operação bem-sucedida.<br/>                                                                                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Erro de permissões, acesso negado.<br/>                                                                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | O limite de recursos do sistema não pôde executar a operação.<br/>                                                             |
| <dl> <dt>**NAP \_ E \_ não \_ inicializado**</dt> </dl> | O SHA não foi inicializado anteriormente.<br/>                                                                        |
| <dl> <dt>**RPC \_ E \_ desconectado**</dt> </dl>     | O NapAgent foi interrompido. Este objeto será recuperado automaticamente e reassociado ao NapAgent, depois que ele for reiniciado.<br/> |



 

## <a name="remarks"></a>Comentários

O SHA deve liberar a estrutura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) chamando [**FreeIsolationInfoEx**](freeisolationinfoex.md).

O SHA deve chamar [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) antes de chamar este método ou qualquer outro método da interface [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                |
| parâmetro<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)
</dt> </dl>

 

 





