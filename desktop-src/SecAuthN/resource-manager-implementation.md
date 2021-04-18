---
description: O Gerenciador de recursos é executado como um serviço confiável em um único processo. Todas as solicitações de acesso ao cartão inteligente são feitas ao Gerenciador de recursos, que as roteia para o leitor que contém o cartão de destino.
ms.assetid: 4a62588a-14d9-43dc-9572-25a9cbcd0efd
title: Implementação do Resource Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ec653f999b74bb9851893b11e1fa49120a7bd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752224"
---
# <a name="resource-manager-implementation"></a>Implementação do Resource Manager

O [*Gerenciador de recursos*](../secgloss/r-gly.md) é executado como um serviço confiável em um único processo. Todas as solicitações de acesso ao [*cartão inteligente*](../secgloss/s-gly.md) são feitas ao Gerenciador de recursos, que as roteia para o [*leitor*](../secgloss/r-gly.md) que contém o cartão de destino.

Os cartões inteligentes são frequentemente usados em conjunto com segurança e privacidade pessoal. Sempre que possível, o Gerenciador de recursos usa os mecanismos de segurança existentes no sistema operacional subjacente ao acessar um leitor ou cartão inteligente.

 

 
