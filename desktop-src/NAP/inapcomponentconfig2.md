---
title: Interface INapComponentConfig2 (NapCommon. h)
description: Fornece métodos de configuração do sistema NAP para SHVs (validadores da integridade do sistema) para configurar uma interface de usuário do servidor de diretivas de rede (NPS) remotamente.
ms.assetid: 35150184-300c-4ea4-bff9-b3c33fa3156b
keywords:
- INapComponentConfig2 da interface NAP
- INapComponentConfig2 interface NAP, descrita
topic_type:
- apiref
api_name:
- INapComponentConfig2
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48a80dfa1a9160b32b6d3c869795c9e23e41a5fdba39e38051bd29376caf8847
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368364"
---
# <a name="inapcomponentconfig2-interface"></a>Interface INapComponentConfig2

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

A interface **INapComponentConfig2** fornece métodos de configuração do sistema NAP para SHVs (validadores da integridade do sistema) para configurar uma interface de usuário do servidor de diretivas de rede (NPS) remotamente.

> [!Note]  
> Essa interface herda todos os métodos de [**INapComponentConfig**](inapcomponentconfig.md) e deve ser usada em seu lugar.

 

## <a name="members"></a>Membros

A interface **INapComponentConfig2** herda de [**INapComponentConfig**](inapcomponentconfig.md). **INapComponentConfig2** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapComponentConfig2** tem esses métodos.



| Método                                                                                                | Descrição                                                                                                                                                                |
|:------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapComponentConfig2::InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md)           | Implementado por SHVs conforme necessário para gerenciar a configuração remota diretamente no computador especificado.<br/>                                                                 |
| [**INapComponentConfig2::InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md)   | Implementado por SHVs conforme necessário para carregar a configuração do computador remoto na memória e para exibir uma interface do usuário que permite a manipulação dos dados de configuração.<br/> |
| [**INapComponentConfig2::IsRemoteConfigSupported**](inapcomponentconfig2-isremoteconfigsupported.md) | Implementado por SHVs para indicar se há suporte para a configuração remota.<br/>                                                                                      |



 

## <a name="remarks"></a>Comentários

Essa interface não deve ser implementada por agentes de integridade do sistema (SHAs) ou clientes de imposição de quarentena (QECs).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referência de NAP](nap-reference.md)
</dt> </dl>

 

 





