---
title: Publicando com o serviço de nome RPC
description: Os serviços RPC podem publicar seus identificadores em um namespace usando as APIs do serviço de nomes RPC (RpcNs).
ms.assetid: 0c8e1207-daeb-4dc8-b83a-a54cd59a46a7
ms.tgt_platform: multiple
keywords:
- Publicando com o serviço de nome RPC AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b672eec6308d709fe2f4cbc64ad22ecf0d6edd
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007300"
---
# <a name="publishing-with-the-rpc-name-service"></a>Publicando com o serviço de nome RPC

Os serviços RPC podem publicar seus identificadores em um namespace usando as APIs do serviço de nomes RPC (RpcNs). As APIs de RpcNs no Windows 2000 publicam as entradas RPC em Active Directory Domain Services. Os serviços criam associações RPC e as publicam no namespace como entradas de servidor RPC nomeadas com atributos, incluindo a ID de interface exclusiva, um GUID reconhecido por clientes. Um cliente pode então Pesquisar servidores RPC que ofereçam a interface desejada, importar a associação e conectar-se ao servidor.

Para obter mais informações sobre como publicar um serviço RPC, consulte [associação no lado do servidor](/windows/desktop/Rpc/server-side-binding).

 

 