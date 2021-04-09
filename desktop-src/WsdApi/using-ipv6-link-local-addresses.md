---
description: O endereçamento de link local IPv6 em mensagens SOAP fornece um desafio exclusivo, pois os endereços de link local IPv6 exigem uma ID de escopo significativa, mas a ID do escopo tem significado apenas para o computador local.
ms.assetid: 63495335-e447-4564-b669-0896c7aac63f
title: Usando endereços de link local IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c89356042e8a71b0af19337b7013b8abd1e8a354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090991"
---
# <a name="using-ipv6-link-local-addresses"></a>Usando endereços de link local IPv6

O endereçamento de link local IPv6 em mensagens SOAP fornece um desafio exclusivo, pois os endereços de link local IPv6 exigem uma ID de escopo significativa, mas a ID do escopo tem significado apenas para o computador local. Todas as implementações de cliente e dispositivo devem remover a ID de escopo antes de enviar um endereço de link local IPv6 em uma mensagem SOAP. Além disso, quando um endereço de link local IPv6 é recebido em uma mensagem, a interface em que a mensagem foi recebida deve ser conhecida para que o endereço local do link completo com a ID de escopo possa ser reconstruído.

 

 



