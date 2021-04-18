---
title: Carregando o caractere padrão
description: Carregando o caractere padrão
ms.assetid: 4e91aef5-8402-401d-b09f-83be25011027
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 387715b5078c4ec875c9abce47039898e4998cf7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105786133"
---
# <a name="loading-the-default-character"></a><span data-ttu-id="a3b7e-103">Carregando o caractere padrão</span><span class="sxs-lookup"><span data-stu-id="a3b7e-103">Loading the Default Character</span></span>

<span data-ttu-id="a3b7e-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a3b7e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="a3b7e-105">Em vez de carregar apenas um caractere específico diretamente especificando seu nome de arquivo, você pode carregar o *caractere padrão*.</span><span class="sxs-lookup"><span data-stu-id="a3b7e-105">Instead of loading only a specific character directly by specifying its filename, you can load the *default character*.</span></span> <span data-ttu-id="a3b7e-106">O caractere padrão é um serviço destinado a fornecer um assistente do Windows central e compartilhado que o usuário escolhe.</span><span class="sxs-lookup"><span data-stu-id="a3b7e-106">The default character is a service intended to provide a shared, central Windows assistant that the user chooses.</span></span> <span data-ttu-id="a3b7e-107">O Microsoft Agent inclui uma folha de propriedades como parte do serviço de caractere padrão, conhecido como o caractere janela Propriedades, que permite que o usuário altere a seleção do caractere padrão.</span><span class="sxs-lookup"><span data-stu-id="a3b7e-107">Microsoft Agent includes a property sheet as part of the default character service, known as the Character Properties window, which enables the user to change their selection of the default character.</span></span>

<span data-ttu-id="a3b7e-108">A seleção do caractere padrão é limitada a um caractere que dá suporte ao conjunto de animações padrão, garantindo um nível básico de consistência entre os caracteres.</span><span class="sxs-lookup"><span data-stu-id="a3b7e-108">Selection of the default character is limited to a character that supports the standard animation set, ensuring a basic level of consistency across characters.</span></span> <span data-ttu-id="a3b7e-109">Isso não exclui um caractere de ter animações adicionais.</span><span class="sxs-lookup"><span data-stu-id="a3b7e-109">This does not exclude a character from having additional animations.</span></span>

<span data-ttu-id="a3b7e-110">No entanto, como o caractere padrão destina-se ao uso para fins gerais e pode ser compartilhado por outros aplicativos ao mesmo tempo, evite carregar o caractere padrão quando desejar um caractere exclusivamente para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a3b7e-110">However, because the default character is intended for general-purpose use and may be shared by other applications at the same time, avoid loading the default character when you want a character exclusively for your application.</span></span>

<span data-ttu-id="a3b7e-111">Para carregar o caractere padrão, chame o método [**Load**](load-method.md) sem especificar um nome de arquivo ou caminho.</span><span class="sxs-lookup"><span data-stu-id="a3b7e-111">To load the default character, call the [**Load**](load-method.md) method without specifying a filename or path.</span></span> <span data-ttu-id="a3b7e-112">O Microsoft Agent carrega automaticamente o conjunto de caracteres atual como o caractere padrão.</span><span class="sxs-lookup"><span data-stu-id="a3b7e-112">Microsoft Agent automatically loads the current character set as the default character.</span></span> <span data-ttu-id="a3b7e-113">Se o usuário ainda não tiver selecionado um caractere padrão, o Agent selecionará o primeiro caractere que dá suporte ao conjunto de animações padrão.</span><span class="sxs-lookup"><span data-stu-id="a3b7e-113">If the user has not yet selected a default character, Agent will select the first character that supports the standard animation set.</span></span> <span data-ttu-id="a3b7e-114">Se nenhum estiver disponível, o método falhará e relatará a causa.</span><span class="sxs-lookup"><span data-stu-id="a3b7e-114">If none is available, the method will fail and report back the cause.</span></span>

<span data-ttu-id="a3b7e-115">Embora um aplicativo cliente possa consultar a identidade do caractere, apenas um usuário pode alterar suas configurações.</span><span class="sxs-lookup"><span data-stu-id="a3b7e-115">Although a client application can inquire as to the identity of the character, only a user can change its settings.</span></span> <span data-ttu-id="a3b7e-116">Você pode usar o [**ShowDefaultCharacterProperties**](showdefaultcharacterproperties-method.md) para exibir o caractere janela Propriedades.</span><span class="sxs-lookup"><span data-stu-id="a3b7e-116">You can use the [**ShowDefaultCharacterProperties**](showdefaultcharacterproperties-method.md) to display the Character Properties window.</span></span>

<span data-ttu-id="a3b7e-117">O servidor notificará os clientes que carregaram o caractere padrão quando um usuário alterar uma seleção de caracteres e passar o GUID do novo caractere.</span><span class="sxs-lookup"><span data-stu-id="a3b7e-117">The server will notify clients that have loaded the default character when a user changes a character selection, and pass the GUID of the new character.</span></span> <span data-ttu-id="a3b7e-118">O servidor descarrega automaticamente o caractere anterior e recarrega o novo caractere.</span><span class="sxs-lookup"><span data-stu-id="a3b7e-118">The server automatically unloads the former character and reloads the new character.</span></span> <span data-ttu-id="a3b7e-119">As filas de todos os clientes que carregaram o caractere padrão são interrompidas e liberadas.</span><span class="sxs-lookup"><span data-stu-id="a3b7e-119">The queues of any clients that have loaded the default character are halted and flushed.</span></span> <span data-ttu-id="a3b7e-120">No entanto, as filas de clientes que carregaram o caractere explicitamente usando o nome de arquivo do caractere não são afetadas.</span><span class="sxs-lookup"><span data-stu-id="a3b7e-120">However, the queues of clients that have loaded the character explicitly using the character's filename are not affected.</span></span> <span data-ttu-id="a3b7e-121">Se necessário, o servidor também lida automaticamente com a redefinição automática do mecanismo de conversão de texto em fala (TTS) para o novo caractere.</span><span class="sxs-lookup"><span data-stu-id="a3b7e-121">If necessary, the server also handles automatically resetting the text-to-speech (TTS) engine for the new character.</span></span>

 

 




