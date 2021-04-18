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
# <a name="resource-manager-implementation"></a><span data-ttu-id="40b30-104">Implementação do Resource Manager</span><span class="sxs-lookup"><span data-stu-id="40b30-104">Resource Manager Implementation</span></span>

<span data-ttu-id="40b30-105">O [*Gerenciador de recursos*](../secgloss/r-gly.md) é executado como um serviço confiável em um único processo.</span><span class="sxs-lookup"><span data-stu-id="40b30-105">The [*resource manager*](../secgloss/r-gly.md) runs as a trusted service in a single process.</span></span> <span data-ttu-id="40b30-106">Todas as solicitações de acesso ao [*cartão inteligente*](../secgloss/s-gly.md) são feitas ao Gerenciador de recursos, que as roteia para o [*leitor*](../secgloss/r-gly.md) que contém o cartão de destino.</span><span class="sxs-lookup"><span data-stu-id="40b30-106">All requests for [*smart card*](../secgloss/s-gly.md) access are made to the resource manager, which routes them to the [*reader*](../secgloss/r-gly.md) that contains the targeted card.</span></span>

<span data-ttu-id="40b30-107">Os cartões inteligentes são frequentemente usados em conjunto com segurança e privacidade pessoal.</span><span class="sxs-lookup"><span data-stu-id="40b30-107">Smart cards are often used in conjunction with security and personal privacy.</span></span> <span data-ttu-id="40b30-108">Sempre que possível, o Gerenciador de recursos usa os mecanismos de segurança existentes no sistema operacional subjacente ao acessar um leitor ou cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="40b30-108">Wherever possible, the resource manager uses the security mechanisms existing within the underlying operating system when accessing a reader or smart card.</span></span>

 

 
