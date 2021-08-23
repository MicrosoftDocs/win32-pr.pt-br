---
title: Interface IConnectionBrokerClient (Cbclient.h)
description: Fornece os métodos necessários para usar o Conexão de Área de Trabalho Remota Broker.
ms.assetid: AFFE0157-DEF5-480D-8CE0-D89E9EF70EAF
ms.tgt_platform: multiple
keywords:
- Interface IConnectionBrokerClient Serviços de Área de Trabalho Remota
- Interface IConnectionBrokerClient Serviços de Área de Trabalho Remota , descrita
topic_type:
- apiref
api_name:
- IConnectionBrokerClient
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a87c30729a5ec78e5275a6c2a1c0d9d139b857c3c7ea10f666ba09b7fceed256
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059154"
---
# <a name="iconnectionbrokerclient-interface"></a>Interface IConnectionBrokerClient

Fornece os métodos necessários para usar o Conexão de Área de Trabalho Remota Broker.

Essa interface é implementada pelo sistema. Para obter uma instância dessa interface, use a [**função CBCreateClientInstance.**](cbcreateclientinstance.md)

## <a name="members"></a>Membros

A interface **IConnectionBrokerClient** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IConnectionBrokerClient** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IConnectionBrokerClient** tem esses métodos.



| Método                                                         | Descrição                                                                                          |
|:---------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) | Solicita informações sobre o computador de destino no qual a conexão deve ser redirecionada.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                       |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                             |
| Cabeçalho<br/>                   | <dl> <dt>Cbclient.h</dt> </dl>      |
| Biblioteca<br/>                  | <dl> <dt>Cbclient.lib</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IConnectionBrokerClient é definido como D6818DF2-8338-4EB7-AD77-DE210817987C<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CBCreateClientInstance**](cbcreateclientinstance.md)
</dt> </dl>

 

