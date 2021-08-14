---
title: Método INapSystemHealthAgentBinding GetSystemIsolationInfo (NapSystemHealthAgent. h)
description: É chamado por SHAs para determinar o estado de isolamento do sistema.
ms.assetid: 0401a846-0da2-4975-87bc-3e9fe8b5b67d
keywords:
- Método GetSystemIsolationInfo NAP
- Método GetSystemIsolationInfo NAP, interface INapSystemHealthAgentBinding
- INapSystemHealthAgentBinding interface NAP, método GetSystemIsolationInfo
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.GetSystemIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9058b78bcff60b27bb27f25f11b785a8cd341f9addafe1829c1e8a7f3fb02a15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939553"
---
# <a name="inapsystemhealthagentbindinggetsystemisolationinfo-method"></a>Método INapSystemHealthAgentBinding:: GetSystemIsolationInfo

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSystemHealthAgentBinding:: GetSystemIsolationInfo** é chamado por SHAs para determinar o estado de isolamento do sistema.

> [!Note]  
> Use [**INapSystemHealthAgentBinding2:: GetSystemIsolationInfoEx**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) para determinar o estado de isolamento estendido do sistema.

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*isolationInfo* \[ fora\]
</dt> <dd>

Um ponteiro para um ponteiro para uma estrutura [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) que contém o estado de isolamento do sistema para conexões conhecidas. *isolationInfoindicates* se o sistema estiver em um estado de acesso restrito, experiência ou acesso irrestrito.

</dd> <dt>

*unknownConnections* \[ fora\]
</dt> <dd>

Um ponteiro para um **bool** que será **verdadeiro** se qualquer conexão estiver em um estado desconhecido e **false** caso contrário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                             | Descrição                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Êxito na operação.<br/>                                                                                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Erro de permissões, acesso negado.<br/>                                                                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | O limite de recursos do sistema não pôde executar a operação.<br/>                                                             |
| <dl> <dt>**NAP \_ E \_ não \_ inicializado**</dt> </dl> | O SHA não foi inicializado anteriormente.<br/>                                                                        |
| <dl> <dt>**RPC \_ E \_ desconectado**</dt> </dl>     | O NapAgent foi interrompido. Este objeto será recuperado automaticamente e reassociado ao NapAgent, depois que ele for reiniciado.<br/> |



 

## <a name="remarks"></a>Comentários

O SHA deve chamar [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) antes de chamar este método ou qualquer outro método da interface [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





