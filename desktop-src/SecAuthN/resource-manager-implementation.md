---
description: O gerenciador de recursos é executado como um serviço confiável em um único processo. Todas as solicitações de acesso de cartão inteligente são feitas ao gerenciador de recursos, que as encaminha para o leitor que contém o cartão de o alvo.
ms.assetid: 4a62588a-14d9-43dc-9572-25a9cbcd0efd
title: Resource Manager implementação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d0dfd21ed7da466f84e867a6d28b0e826fc5c4733f24d2f5e1f0562f1b4156
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919145"
---
# <a name="resource-manager-implementation"></a>Resource Manager implementação

O [*gerenciador de recursos*](../secgloss/r-gly.md) é executado como um serviço confiável em um único processo. Todas as solicitações [*de acesso de cartão*](../secgloss/s-gly.md) inteligente são feitas ao gerenciador de recursos, que as encaminha para o [*leitor*](../secgloss/r-gly.md) que contém o cartão de o alvo.

Cartões inteligentes geralmente são usados em conjunto com segurança e privacidade pessoal. Sempre que possível, o gerenciador de recursos usa os mecanismos de segurança existentes no sistema operacional subjacente ao acessar um leitor ou cartão inteligente.

 

 
