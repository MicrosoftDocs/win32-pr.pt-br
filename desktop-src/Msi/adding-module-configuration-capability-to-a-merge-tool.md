---
description: Windows Installer desenvolvedores podem criar ferramentas que permitem que os usuários finais usem módulos de mesclagem configuráveis.
ms.assetid: 5857b788-f1dd-41d0-b0ee-0872494e3c2c
title: Adicionando a funcionalidade de configuração de módulo a uma ferramenta de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba04d297ad93cffc553670c648577f650cd21407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662073"
---
# <a name="adding-module-configuration-capability-to-a-merge-tool"></a><span data-ttu-id="e11d6-103">Adicionando a funcionalidade de configuração de módulo a uma ferramenta de mesclagem</span><span class="sxs-lookup"><span data-stu-id="e11d6-103">Adding Module Configuration Capability to a Merge Tool</span></span>

<span data-ttu-id="e11d6-104">Para permitir que os usuários finais usem módulos de mesclagem configuráveis, você pode criar ferramentas de mesclagem e configuração para fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e11d6-104">To enable end users to use configurable merge modules, you can author merge and configuration tools to do the following:</span></span>

-   <span data-ttu-id="e11d6-105">As ferramentas de mesclagem devem chamar as funções no Mergemod.dll versão 2,0 para mesclar o módulo.</span><span class="sxs-lookup"><span data-stu-id="e11d6-105">Merge tools should call the functions in Mergemod.dll version 2.0 to merge the module.</span></span> <span data-ttu-id="e11d6-106">As versões anteriores do Mergemod.dll não podem ser usadas para configurar módulos de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="e11d6-106">Earlier versions of Mergemod.dll cannot be used to configure merge modules.</span></span>
-   <span data-ttu-id="e11d6-107">Os aplicativos de configuração do cliente devem interagir com o usuário do módulo de mesclagem para coletar as seleções do usuário para itens configuráveis.</span><span class="sxs-lookup"><span data-stu-id="e11d6-107">Client configuration applications should interact with the merge module user to collect the user selections for configurable items.</span></span>
-   <span data-ttu-id="e11d6-108">As ferramentas de mesclagem devem expor informações de configuração criadas no módulo de mesclagem para o aplicativo cliente para que o cliente possa usar essas informações para consultar o usuário.</span><span class="sxs-lookup"><span data-stu-id="e11d6-108">Merge tools should expose configuration information authored into the merge module to the client application so that the client can use this information to query the user.</span></span>
-   <span data-ttu-id="e11d6-109">Quando uma ferramenta de mesclagem encontra um item configurável durante uma mesclagem, ela deve chamar a ferramenta de configuração do cliente para obter informações de personalização obtidas do usuário.</span><span class="sxs-lookup"><span data-stu-id="e11d6-109">When a merge tool encounters a configurable item during a merge, it should call the client configuration tool for customization information obtained from the user.</span></span> <span data-ttu-id="e11d6-110">A ferramenta de mesclagem deve fazer as alterações especificadas no módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="e11d6-110">The merge tool should make the specified changes to the merge module.</span></span>
-   <span data-ttu-id="e11d6-111">Os aplicativos de configuração devem permitir que o usuário forneça opções para itens configuráveis, mas todas as opções possíveis não precisam ser reveladas ao usuário.</span><span class="sxs-lookup"><span data-stu-id="e11d6-111">Configuration applications should enable the user to provide choices for configurable items, but all the possible choices do not need to be revealed to the user.</span></span> <span data-ttu-id="e11d6-112">A ferramenta de mesclagem pode usar valores padrão para itens configuráveis que o usuário não seleciona.</span><span class="sxs-lookup"><span data-stu-id="e11d6-112">The merge tool can use default values for configurable items that the user does not select.</span></span>
-   <span data-ttu-id="e11d6-113">Se um usuário não fornecer informações de personalização, as ferramentas de mesclagem deverão usar os valores de configuração padrão especificados no módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="e11d6-113">If a user does not provide customization information, merge tools should use the default configuration values that are specified in the merge module.</span></span>
-   <span data-ttu-id="e11d6-114">Depois que um usuário fornece as seleções específicas da ferramenta de configuração, a ferramenta de mesclagem chama Mergemod.dll para executar a mesclagem.</span><span class="sxs-lookup"><span data-stu-id="e11d6-114">After a user gives the configuration tool specific selections, the merge tool calls Mergemod.dll to perform the merge.</span></span>

 

 



