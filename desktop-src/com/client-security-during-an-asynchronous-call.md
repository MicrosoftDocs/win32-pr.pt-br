---
title: Client Security durante uma chamada assíncrona
description: Client Security durante uma chamada assíncrona
ms.assetid: 26d1f2c2-cb08-49f1-8beb-b99b029f0d8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bea2f83bf6341704dd0265a37ec2f64b79e9b2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636714"
---
# <a name="client-security-during-an-asynchronous-call"></a>Client Security durante uma chamada assíncrona

O Gerenciador de proxy criado pelo MIDL para objetos que usam marshaling padrão implementa a interface [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) . Os clientes podem gerenciar a segurança de chamadas com marshaling consultando **IClientSecurity** no objeto de chamada e obtendo ou alterando as configurações de segurança.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fazendo uma chamada assíncrona](making-an-asynchronous-call.md)
</dt> </dl>

 

 




