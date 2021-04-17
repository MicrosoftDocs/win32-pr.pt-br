---
title: Método Uninitialize do INapSystemHealthAgentBinding (NapSystemHealthAgent. h)
description: Faz com que o NapAgent libere todas as suas referências aos ponteiros COM do agente de integridade do sistema.
ms.assetid: 8b9fabc9-7453-41fe-a1e7-2ec5fa275a3a
keywords:
- Método Uninitialize NAP
- Método Uninitialize NAP, interface INapSystemHealthAgentBinding
- INapSystemHealthAgentBinding interface NAP, método Uninitialize
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a863e9d742610ab764a3b7a00966e8e112278317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754749"
---
# <a name="inapsystemhealthagentbindinguninitialize-method"></a>Método INapSystemHealthAgentBinding:: Uninitialize

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSystemHealthAgentBinding:: Uninitialize** faz com que o NapAgent libere todas as suas referências aos ponteiros de com do agente de integridade do sistema.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

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

O NapAgent bloqueia a execução dessa chamada de método até que todas as chamadas existentes nas interfaces de ligação e retorno de chamada sejam concluídas.

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

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





