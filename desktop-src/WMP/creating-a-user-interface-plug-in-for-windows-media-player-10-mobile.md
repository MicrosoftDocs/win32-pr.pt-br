---
title: Criando um plug-in de interface do usuário para o Windows Media Player 10 Mobile
description: Criando um plug-in de interface do usuário para o Windows Media Player 10 Mobile
ms.assetid: 050418b7-d99c-49ab-8ce6-6511b194ffe6
keywords:
- Windows Media Player Mobile, plug-ins
- Windows Media Player Mobile, plug-ins de interface do usuário
- Plug-ins móveis do Windows Media Player
- plug-ins, interface do usuário
- plug-ins, Windows Media Player Mobile
- plug-ins de interface do usuário, Windows Media Player Mobile
- Plug-ins de interface do usuário, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d649ef1d8ed1b8fb1e1b54dc7eed106f798b1ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105813177"
---
# <a name="creating-a-user-interface-plug-in-for-windows-media-player-10-mobile"></a><span data-ttu-id="34dc9-110">Criando um plug-in de interface do usuário para o Windows Media Player 10 Mobile</span><span class="sxs-lookup"><span data-stu-id="34dc9-110">Creating a User Interface Plug-in for Windows Media Player 10 Mobile</span></span>

<span data-ttu-id="34dc9-111">O Windows Media Player 10 Mobile usa o mesmo modelo de plug-in de interface do usuário da área de trabalho do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="34dc9-111">Windows Media Player 10 Mobile uses the same UI plug-in model as the desktop Windows Media Player.</span></span> <span data-ttu-id="34dc9-112">No entanto, o Windows Media Player 10 Mobile pode interagir somente com plug-ins de interface do usuário em segundo plano. Devido aos modelos de plug-in semelhantes, as mesmas chamadas à API que se aplicam aos plug-ins de interface do usuário em segundo plano no desktop também se aplicam aos plug-ins de IU em segundo plano em um dispositivo Windows Mobile.</span><span class="sxs-lookup"><span data-stu-id="34dc9-112">However, Windows Media Player 10 Mobile can only interact with background UI plug-ins. Because of the similar plug-in models, the same API calls that apply to background UI plug-ins on the desktop also apply to background UI plug-ins on a Windows Mobile device.</span></span>

<span data-ttu-id="34dc9-113">As seções a seguir descrevem como criar um plug-in de IU em segundo plano usando o código gerado pelo assistente do assistente de plug-in do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="34dc9-113">The following sections describe how to create a background UI plug-in by using wizard-generated code from the Windows Media Player Plug-in Wizard.</span></span>



| <span data-ttu-id="34dc9-114">Seção</span><span class="sxs-lookup"><span data-stu-id="34dc9-114">Section</span></span>                                                                | <span data-ttu-id="34dc9-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="34dc9-115">Description</span></span>                                                                                                                                            |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34dc9-116">Introdução</span><span class="sxs-lookup"><span data-stu-id="34dc9-116">Getting Started</span></span>](getting-started.md)                                 | <span data-ttu-id="34dc9-117">Descreve o que você precisa instalar e como usar o assistente de plug-in do Windows Media Player para ajudar a automatizar a criação de um plug-in de interface do usuário em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="34dc9-117">Describes what you need to install and how to use the Windows Media Player Plug-in Wizard to help automate the creation of a background UI plug-in.</span></span>    |
| [<span data-ttu-id="34dc9-118">Modificando código gerado pelo assistente</span><span class="sxs-lookup"><span data-stu-id="34dc9-118">Modifying Wizard-generated Code</span></span>](modifying-wizard-generated-code.md) | <span data-ttu-id="34dc9-119">Descreve o que você precisa modificar do código gerado pelo assistente criado na seção anterior para que ele funcione com o Windows Media Player 10 Mobile.</span><span class="sxs-lookup"><span data-stu-id="34dc9-119">Describes what you need to modify from the wizard-generated code created in the previous section so that it works with Windows Media Player 10 Mobile.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="34dc9-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="34dc9-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34dc9-121">**Guia de programação de plug-ins de interface do usuário**</span><span class="sxs-lookup"><span data-stu-id="34dc9-121">**User Interface Plug-ins Programming Guide**</span></span>](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




