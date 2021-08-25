---
description: O endereçamento de link local IPv6 em mensagens SOAP fornece um desafio exclusivo, pois os endereços de link local IPv6 exigem uma ID de escopo significativa, mas a ID do escopo tem significado apenas para o computador local.
ms.assetid: 63495335-e447-4564-b669-0896c7aac63f
title: Usando endereços de link local IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10c1719e4e6d374e7afd859b80cd1bc14c4c841cb7dceee149f14d0acb777f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897156"
---
# <a name="using-ipv6-link-local-addresses"></a>Usando endereços de link local IPv6

O endereçamento de link local IPv6 em mensagens SOAP fornece um desafio exclusivo, pois os endereços de link local IPv6 exigem uma ID de escopo significativa, mas a ID do escopo tem significado apenas para o computador local. Todas as implementações de cliente e dispositivo devem remover a ID de escopo antes de enviar um endereço de link local IPv6 em uma mensagem SOAP. Além disso, quando um endereço de link local IPv6 é recebido em uma mensagem, a interface em que a mensagem foi recebida deve ser conhecida para que o endereço local do link completo com a ID de escopo possa ser reconstruído.

 

 



