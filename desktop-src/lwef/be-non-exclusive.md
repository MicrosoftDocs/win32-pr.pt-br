---
title: Ser não exclusivo
description: Ser não exclusivo
ms.assetid: 7a44840d-6bf9-4c12-ba14-66d7067a984d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b637bcf0860ccc4917b1af344664f9828b0da8d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363830"
---
# <a name="be-non-exclusive"></a><span data-ttu-id="48af8-103">Ser não exclusivo</span><span class="sxs-lookup"><span data-stu-id="48af8-103">Be Non-Exclusive</span></span>

<span data-ttu-id="48af8-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="48af8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="48af8-105">Os caracteres interativos podem ser empregados na interface do usuário como assistentes, guias, entretenimentos, histórias, agentes de vendas ou em uma variedade de outras funções.</span><span class="sxs-lookup"><span data-stu-id="48af8-105">Interactive characters can be employed in the user interface as assistants, guides, entertainers, storytellers, sales agents, or in a variety of other roles.</span></span> <span data-ttu-id="48af8-106">Um caractere que executa ou ajuda automaticamente não deve ser projetado ao contrário do princípio de design para manter o usuário no controle.</span><span class="sxs-lookup"><span data-stu-id="48af8-106">A character that automatically performs or assists should not be designed contrary to the design principle of keeping the user in control.</span></span> <span data-ttu-id="48af8-107">Ao adicionar um caractere à interface de um site ou aplicativo convencional, use o caractere como um aprimoramento, em vez de uma substituição de, a interface primária.</span><span class="sxs-lookup"><span data-stu-id="48af8-107">When adding a character to the interface of a website or conventional application, use the character as an enhancement, rather than a replacement of, the primary interface.</span></span> <span data-ttu-id="48af8-108">Evite implementar qualquer recurso ou operação que exija exclusivamente um caractere.</span><span class="sxs-lookup"><span data-stu-id="48af8-108">Avoid implementing any feature or operation that exclusively requires a character.</span></span>

<span data-ttu-id="48af8-109">Da mesma forma, permita que o usuário escolha quando deseja interagir com seu caractere.</span><span class="sxs-lookup"><span data-stu-id="48af8-109">Similarly, let the user choose when they want to interact with your character.</span></span> <span data-ttu-id="48af8-110">Um usuário deve ser capaz de ignorar o caractere e retorná-lo somente com a permissão do usuário.</span><span class="sxs-lookup"><span data-stu-id="48af8-110">A user should be able to dismiss the character and have it return only with the user's permission.</span></span> <span data-ttu-id="48af8-111">Forçar a interação de caracteres em usuários pode ter um sério efeito negativo.</span><span class="sxs-lookup"><span data-stu-id="48af8-111">Forcing character interaction on users can have a serious negative effect.</span></span> <span data-ttu-id="48af8-112">Para dar suporte ao controle de usuário da interação de caracteres, o Microsoft Agent inclui automaticamente os comandos ocultar e mostrar.</span><span class="sxs-lookup"><span data-stu-id="48af8-112">To support user control of character interaction, Microsoft Agent automatically includes Hide and Show commands.</span></span> <span data-ttu-id="48af8-113">A API do Microsoft Agent também dá suporte a esses métodos, de modo que você pode incluir suporte para essas funções em sua própria interface.</span><span class="sxs-lookup"><span data-stu-id="48af8-113">The Microsoft Agent API also supports these methods, so you can include support for these functions in your own interface.</span></span> <span data-ttu-id="48af8-114">Além disso, a interface do usuário do Microsoft Agent inclui propriedades globais que permitem ao usuário substituir determinadas opções de saída de caracteres.</span><span class="sxs-lookup"><span data-stu-id="48af8-114">In addition, Microsoft Agent's user interface includes global properties that enable the user to override certain character output options.</span></span> <span data-ttu-id="48af8-115">Para garantir que as preferências do usuário sejam mantidas, essas propriedades não podem ser substituídas por meio da API.</span><span class="sxs-lookup"><span data-stu-id="48af8-115">To ensure that the user's preferences are maintained, these properties cannot be overridden through the API.</span></span>

 

 




