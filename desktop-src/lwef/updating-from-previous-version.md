---
title: Atualizando da versão anterior
description: Atualizando da versão anterior
ms.assetid: a3f0c0bb-8c12-4907-8e49-49b098449c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7860e2cf49fbe21c2522226ec61ab57c93d9df27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761205"
---
# <a name="updating-from-previous-version"></a><span data-ttu-id="44ab0-103">Atualizando da versão anterior</span><span class="sxs-lookup"><span data-stu-id="44ab0-103">Updating from Previous Version</span></span>

<span data-ttu-id="44ab0-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="44ab0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="44ab0-105">Aplicativos compilados e compilados com a versão 1,5 anterior do Microsoft Agent devem ser executados sem modificação na nova versão 2,0.</span><span class="sxs-lookup"><span data-stu-id="44ab0-105">Applications built and compiled with the previous 1.5 version of Microsoft Agent should run without modification under the new 2.0 version.</span></span> <span data-ttu-id="44ab0-106">A propriedade [**Connected**](connected-property.md) não pode mais ser definida como **false**; algumas propriedades do objeto SpeechInput que foram substituídas ainda existem, mas não transformam mais nenhum valor, e o servidor não dispara mais os eventos de [**reinicialização**](https://www.bing.com/search?q=**Restart**) e [**desligamento**](https://www.bing.com/search?q=**Shutdown**) .</span><span class="sxs-lookup"><span data-stu-id="44ab0-106">The [**Connected**](connected-property.md) property can no longer be set to **False**; certain properties of the SpeechInput object that have been replaced still exist, but no longer turn any values, and the server no longer fires the [**Restart**](https://www.bing.com/search?q=**Restart**) and [**Shutdown**](https://www.bing.com/search?q=**Shutdown**) events.</span></span>

<span data-ttu-id="44ab0-107">No entanto, se você atualizar seus aplicativos para usar o controle do agente 2,0, talvez seja necessário modificar seu código.</span><span class="sxs-lookup"><span data-stu-id="44ab0-107">However, if you update your applications to use the Agent 2.0 control, you may have to modify your code.</span></span> <span data-ttu-id="44ab0-108">Se você tiver instalado a versão 2,0 do Microsoft Agent e carregar um projeto de Visual Basic usar a versão anterior do controle do agente, Visual Basic incluirá uma opção que exibirá automaticamente uma mensagem indicando que ela detectou uma nova versão do controle.</span><span class="sxs-lookup"><span data-stu-id="44ab0-108">If you have installed the 2.0 version of Microsoft Agent and load a Visual Basic project use the earlier version of the Agent control, Visual Basic includes an option that will automatically display a message indicating that it detected a new version of the control.</span></span> <span data-ttu-id="44ab0-109">Para garantir a operação adequada do seu aplicativo, sempre escolha usar a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="44ab0-109">To ensure proper operation of your application, always choose to use the later version.</span></span>

<span data-ttu-id="44ab0-110">Para outras linguagens de programação (como 97 Microsoft Office VBA), para atualizar o controle, talvez você precise primeiro remover o controle do agente 1,5 e salvar seu código.</span><span class="sxs-lookup"><span data-stu-id="44ab0-110">For other programming languages (such as Microsoft Office 97 VBA), to update the control, you may have to first remove the 1.5 Agent control and save your code.</span></span> <span data-ttu-id="44ab0-111">Em seguida, saia do ambiente de programação, reinicie o ambiente de programação, recarregue o código e insira o novo controle.</span><span class="sxs-lookup"><span data-stu-id="44ab0-111">Then, quit the programming environment, restart the programming environment, reload your code and insert the new control.</span></span> <span data-ttu-id="44ab0-112">Evite editar um aplicativo habilitado para agente 2,0 na mesma instância do ambiente de programação em que você está editando um aplicativo habilitado para agente 1,5 no.</span><span class="sxs-lookup"><span data-stu-id="44ab0-112">Avoid editing an Agent 2.0-enabled application in the same instance of the programming environment that you are editing an Agent 1.5-enabled application in.</span></span> <span data-ttu-id="44ab0-113">Alguns ambientes de programação podem não lidar com as diferenças entre as duas versões de controles.</span><span class="sxs-lookup"><span data-stu-id="44ab0-113">Some programming environments may not handle the differences between the two versions of controls.</span></span>

<span data-ttu-id="44ab0-114">Você deve ser capaz de desinstalar a versão do agente 1,5 no sistema depois de instalar a versão 2,0 do agente.</span><span class="sxs-lookup"><span data-stu-id="44ab0-114">You should be able to uninstall the Agent 1.5 release on your system after installing the Agent 2.0 release.</span></span> <span data-ttu-id="44ab0-115">No entanto, se o Agent 1,5 estiver instalado na versão 2,0, talvez seja necessário reinstalar o 2,0.</span><span class="sxs-lookup"><span data-stu-id="44ab0-115">However, if Agent 1.5 is installed over the 2.0 release, you may have to reinstall 2.0.</span></span>

 

 




