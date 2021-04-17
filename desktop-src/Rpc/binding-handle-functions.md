---
title: Funções de identificador de associação
description: A tabela a seguir contém a lista de rotinas de tempo de execução RPC que operam em identificadores de associação e especifica o tipo de identificador de associação permitido.
ms.assetid: 16effe59-ebe2-48c3-b97a-90656b6d3b51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e00b3cbb2d5fc5637b9414d6f009cfb2e4ade4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105790000"
---
# <a name="binding-handle-functions"></a>Funções de identificador de associação

A tabela a seguir contém a lista de rotinas de tempo de execução RPC que operam em identificadores de associação e especifica o tipo de identificador de associação permitido.



| Rotina                                                            | Argumento de entrada   | Argumento de saída |
|--------------------------------------------------------------------|------------------|-----------------|
| [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy)                           | Servidor           | Servidor          |
| [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree)                           | Servidor           | Nenhum            |
| [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) | Nenhum             | Servidor          |
| [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)         | Cliente           | Nenhum            |
| [**RpcBindingInqAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)             | Servidor           | Nenhum            |
| [**RpcBindingInqObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqobject)                 | Servidor ou cliente | Nenhum            |
| [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)                         | Servidor           | Nenhum            |
| [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)             | Servidor           | Nenhum            |
| [**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)                 | Servidor           | Nenhum            |
| [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)     | Servidor ou cliente | Nenhum            |
| [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree)               | Servidor           | Nenhum            |
| [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)                   | Servidor           | Nenhum            |
| [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)           | Nenhum             | Servidor          |
| [**RpcNsBindingLookupNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)           | Nenhum             | Servidor          |
| [**RpcNsBindingSelect**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingselect)                   | Servidor           | Servidor          |
| [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings)               | Nenhum             | Servidor          |



 

 

 




