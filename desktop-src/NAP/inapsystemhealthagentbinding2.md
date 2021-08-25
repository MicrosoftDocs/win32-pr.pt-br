---
title: Interface INapSystemHealthAgentBinding2 (NapSystemHealthAgent. h)
description: Os SHAs usam para se comunicar com o NapAgent. | Interface INapSystemHealthAgentBinding2 (NapSystemHealthAgent. h)
ms.assetid: 2b087d79-a738-42d6-a8f2-4698ab844446
keywords:
- INapSystemHealthAgentBinding2 da interface NAP
- INapSystemHealthAgentBinding2 interface NAP, descrita
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c42db59c23826855ca6cda7529eb9dcbbadfb2a1ee2a5aa93d9bd45587c45a87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780926"
---
# <a name="inapsystemhealthagentbinding2-interface"></a>Interface INapSystemHealthAgentBinding2

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O **INapSystemHealthAgentBinding2** fornece métodos que os SHAs usam para se comunicar com o NapAgent.

> [!Note]  
> Essa interface herda todos os métodos de [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md) e deve ser usada em seu lugar.

 

## <a name="members"></a>Membros

A interface **INapSystemHealthAgentBinding2** herda de [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md). **INapSystemHealthAgentBinding2** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapSystemHealthAgentBinding2** tem esses métodos.



| Método                                                                                                                    | Descrição                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) | Chamado por SHAs para determinar o estado de isolamento do sistema e o estado de isolamento estendido.<br/> |



 

## <a name="remarks"></a>Comentários

Todas as APIs nesta interface retornarão **RPC \_ E \_ desconectadas** se o NapAgent for interrompido. Este objeto será recuperado automaticamente e reassociado ao NapAgent, depois que ele for reiniciado.

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
</dt> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referência de NAP](nap-reference.md)
</dt> </dl>

 

 





