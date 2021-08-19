---
title: Publicando com o serviço de nome RPC
description: Os serviços RPC podem publicar seus identificadores em um namespace usando as APIs do serviço de nomes RPC (RpcNs).
ms.assetid: 0c8e1207-daeb-4dc8-b83a-a54cd59a46a7
ms.tgt_platform: multiple
keywords:
- Publicando com o serviço de nome RPC AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd53922bd4ce952c18c58d1b71cb485887bdc0fd020f4113679eb114b32b6f3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025364"
---
# <a name="publishing-with-the-rpc-name-service"></a>Publicando com o serviço de nome RPC

Os serviços RPC podem publicar seus identificadores em um namespace usando as APIs do serviço de nomes RPC (RpcNs). as APIs de RpcNs no Windows 2000 publicam as entradas de RPC no Active Directory Domain Services. Os serviços criam associações RPC e as publicam no namespace como entradas de servidor RPC nomeadas com atributos, incluindo a ID de interface exclusiva, um GUID reconhecido por clientes. Um cliente pode então Pesquisar servidores RPC que ofereçam a interface desejada, importar a associação e conectar-se ao servidor.

Para obter mais informações sobre como publicar um serviço RPC, consulte [associação no lado do servidor](/windows/desktop/Rpc/server-side-binding).

 

 