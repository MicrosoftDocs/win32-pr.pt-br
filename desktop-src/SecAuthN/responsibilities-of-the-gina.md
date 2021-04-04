---
description: Lista e explica as responsabilidades da GINA.
ms.assetid: 5cffe4a6-6475-441e-bf81-f3cbcf1fee3f
title: Responsabilidades da GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c3481aea9f5a92a485c42fb00b43d7062012d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010980"
---
# <a name="responsibilities-of-the-gina"></a><span data-ttu-id="12648-103">Responsabilidades da GINA</span><span class="sxs-lookup"><span data-stu-id="12648-103">Responsibilities of the GINA</span></span>

> [!Note]  
> <span data-ttu-id="12648-104">As DLLs GINAs são ignoradas no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="12648-104">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="12648-105">Uma dll [*Gina*](../secgloss/g-gly.md) tem as seguintes responsabilidades:</span><span class="sxs-lookup"><span data-stu-id="12648-105">A [*GINA*](../secgloss/g-gly.md) DLL has the following responsibilities:</span></span>

-   <span data-ttu-id="12648-106">Monitoramento de SAS</span><span class="sxs-lookup"><span data-stu-id="12648-106">SAS monitoring</span></span>

    <span data-ttu-id="12648-107">A GINA é responsável por reconhecer uma SAS ( [*sequência de atenção segura*](../secgloss/s-gly.md) ), o monitoramento de eventos de SAS e a notificação do Winlogon quando ocorre uma SAS.</span><span class="sxs-lookup"><span data-stu-id="12648-107">The GINA is responsible for recognizing a [*secure attention sequence*](../secgloss/s-gly.md) (SAS), monitoring for SAS events, and notifying Winlogon when a SAS has occurred.</span></span> <span data-ttu-id="12648-108">Observe que pode haver mais de uma SAS definida, e o conjunto de SASs definido pode mudar ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="12648-108">Note that there can be more than one SAS defined, and the set of defined SASs can change over time.</span></span> <span data-ttu-id="12648-109">Por exemplo, pode haver um conjunto de SASs quando o [*Winlogon*](../secgloss/w-gly.md) está no estado conectado e outro definido quando está no estado conectado.</span><span class="sxs-lookup"><span data-stu-id="12648-109">For example, there can be one set of SASs when [*Winlogon*](../secgloss/w-gly.md) is in the logged-off state and another set when it is in the logged-on state.</span></span>

    <span data-ttu-id="12648-110">O Winlogon fornece serviços para ajudar a GINA no uso da SAS CTRL + ALT + DEL.</span><span class="sxs-lookup"><span data-stu-id="12648-110">Winlogon provides services to assist the GINA in using the CTRL+ALT+DEL SAS.</span></span>

-   <span data-ttu-id="12648-111">Processamento de SAS</span><span class="sxs-lookup"><span data-stu-id="12648-111">SAS processing</span></span>

    <span data-ttu-id="12648-112">Um motivo para fazer a GINAção substituível é fornecer mecanismos alternativos de identificação e autenticação.</span><span class="sxs-lookup"><span data-stu-id="12648-112">One reason for making the GINA replaceable is to provide alternative identification and authentication mechanisms.</span></span> <span data-ttu-id="12648-113">Para fazer isso, a GINA deve apresentar todas as interfaces de usuário resultantes do reconhecimento de uma SAS.</span><span class="sxs-lookup"><span data-stu-id="12648-113">To do this, the GINA must present all user interfaces resulting from the recognition of a SAS.</span></span> <span data-ttu-id="12648-114">Quando nenhum usuário está conectado, o GINA é responsável por apresentar as opções de identificação e autenticação, bem como outras opções permitidas que não são autenticadas.</span><span class="sxs-lookup"><span data-stu-id="12648-114">When no user is logged on, the GINA is responsible for presenting identification and authentication options as well as any other permissible options that are not authenticated.</span></span> <span data-ttu-id="12648-115">Quando um usuário está conectado, a GINA é responsável por apresentar as opções relevantes para o usuário, bem como pegar quaisquer ações que sejam consideradas apropriadas.</span><span class="sxs-lookup"><span data-stu-id="12648-115">When a user is logged on, the GINA is responsible for presenting the relevant options to the user as well as taking whatever actions are deemed appropriate.</span></span> <span data-ttu-id="12648-116">Por exemplo, em um sistema que inclui um [*cartão inteligente*](../secgloss/s-gly.md), pode ser apropriado bloquear a estação de trabalho automaticamente se o usuário remover o cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="12648-116">For example, in a system that includes a [*smart card*](../secgloss/s-gly.md), it may be appropriate to automatically lock the workstation if the user removes the smart card.</span></span>

-   <span data-ttu-id="12648-117">Ativação do Shell</span><span class="sxs-lookup"><span data-stu-id="12648-117">Shell activation</span></span>

    <span data-ttu-id="12648-118">Quando um usuário faz logon, a GINA é responsável por criar um ou mais processos iniciais para esse usuário.</span><span class="sxs-lookup"><span data-stu-id="12648-118">When a user logs on, the GINA is responsible for creating one or more initial processes for that user.</span></span> <span data-ttu-id="12648-119">(Nesta documentação, supõe-se que esses processos iniciais apresentem uma interface para o usuário.</span><span class="sxs-lookup"><span data-stu-id="12648-119">(In this documentation, it is assumed that these initial processes present an interface to the user.</span></span> <span data-ttu-id="12648-120">No entanto, os processos podem realmente ser qualquer processo e não precisam necessariamente interagir com o usuário.) Esses processos são chamados de shell do *usuário* ou apenas do *shell*.</span><span class="sxs-lookup"><span data-stu-id="12648-120">However, the processes can actually be any processes and do not necessarily have to interact with the user.) These processes are referred to as the *user shell* or just the *shell*.</span></span> <span data-ttu-id="12648-121">Como parte da ativação do Shell, a GINA deve atribuir o token do usuário conectado recentemente aos processos.</span><span class="sxs-lookup"><span data-stu-id="12648-121">As part of shell activation, the GINA must assign the newly logged-on user's token to the processes.</span></span> <span data-ttu-id="12648-122">O Winlogon fornece um serviço para ajudar a GINA na atribuição do token.</span><span class="sxs-lookup"><span data-stu-id="12648-122">Winlogon provides a service to assist the GINA in assigning the token.</span></span>

 

 
