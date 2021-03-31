---
title: Usando comandos de script
description: Usando comandos de script
ms.assetid: be8a2d22-35cb-4b8d-ad00-e8a45bb85b39
keywords:
- SDK do Windows Media Format, comandos de script
- ASF (Advanced Systems Format), comandos de script
- ASF (formato de sistemas avançados), comandos de script
- scripts, comandos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2e840a677e58a1be528e84e4ed1b4be7fe3619
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005601"
---
# <a name="using-script-commands"></a><span data-ttu-id="351e0-107">Usando comandos de script</span><span class="sxs-lookup"><span data-stu-id="351e0-107">Using Script Commands</span></span>

<span data-ttu-id="351e0-108">O SDK do Windows Media Format dá suporte ao uso de comandos de script para comunicar ações de aplicativos em arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="351e0-108">The Windows Media Format SDK supports the use of script commands to communicate application actions in ASF files.</span></span> <span data-ttu-id="351e0-109">Cada comando de script é composto de duas cadeias de caracteres, a primeira cadeia é o tipo de comando, a segunda é os dados de comando.</span><span class="sxs-lookup"><span data-stu-id="351e0-109">Each script command is made up of two strings, the first string is the type of command, the second is the command data.</span></span> <span data-ttu-id="351e0-110">Por exemplo, você pode usar o tipo de script "URL" e passar uma URL de Internet válida como os dados de comando.</span><span class="sxs-lookup"><span data-stu-id="351e0-110">For example, you can use the script type "URL" and pass a valid Internet URL as the command data.</span></span> <span data-ttu-id="351e0-111">Quando um aplicativo de leitura que dá suporte a comandos de script do tipo "URL" receber esse comando, ele abrirá o endereço especificado em uma janela do navegador.</span><span class="sxs-lookup"><span data-stu-id="351e0-111">When a reading application that supports script commands of type "URL" receives this command, it will open the specified address in a browser window.</span></span>

<span data-ttu-id="351e0-112">O SDK do Windows Media Format fornece duas opções para a entrega de script em arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="351e0-112">The Windows Media Format SDK provides two options for delivering script in ASF files.</span></span> <span data-ttu-id="351e0-113">Você pode criar um fluxo de script ou pode incluir comandos de script no cabeçalho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="351e0-113">You can create a script stream or you can include script commands in the header of the file.</span></span> <span data-ttu-id="351e0-114">Fluxos de script são úteis porque os comandos de script são entregues na ordem de tempo da apresentação.</span><span class="sxs-lookup"><span data-stu-id="351e0-114">Script streams are useful because the script commands are delivered in presentation time order.</span></span> <span data-ttu-id="351e0-115">Se você usar comandos de script no cabeçalho do arquivo, seu aplicativo precisará recuperar todos os comandos de script antes de iniciar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="351e0-115">If you use script commands in the file header, your application will need to retrieve all of the script commands before starting playback.</span></span> <span data-ttu-id="351e0-116">Você deve manter o controle dos tempos de apresentação dos comandos de script e respondê-los no momento certo.</span><span class="sxs-lookup"><span data-stu-id="351e0-116">You must keep track of the presentation times of script commands and respond to them at the right time.</span></span>

<span data-ttu-id="351e0-117">As seções a seguir descrevem como incluir comandos de script em um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="351e0-117">The following sections describe how to include script commands in an ASF file.</span></span>



| <span data-ttu-id="351e0-118">Seção</span><span class="sxs-lookup"><span data-stu-id="351e0-118">Section</span></span>                                                                                                                | <span data-ttu-id="351e0-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="351e0-119">Description</span></span>                                                  |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="351e0-120">Para usar um fluxo de script</span><span class="sxs-lookup"><span data-stu-id="351e0-120">To Use a Script Stream</span></span>](to-use-a-script-stream.md)                                                                   | <span data-ttu-id="351e0-121">Descreve como incluir comandos de script em um fluxo de script.</span><span class="sxs-lookup"><span data-stu-id="351e0-121">Describes how to include script commands in a script stream.</span></span> |
| [<span data-ttu-id="351e0-122">Para adicionar dados de script ao cabeçalho</span><span class="sxs-lookup"><span data-stu-id="351e0-122">To Add Script Data to the Header</span></span>](to-add-script-data-to-the-header.md)                                               | <span data-ttu-id="351e0-123">Descreve como incluir comandos de script no cabeçalho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="351e0-123">Describes how to include script commands in the file header.</span></span> |
| [<span data-ttu-id="351e0-124">Usando comandos de script com suporte no Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="351e0-124">Using Script Commands Supported by Windows Media Player</span></span>](using-script-commands-supported-by-windows-media-player.md) | <span data-ttu-id="351e0-125">Descreve os comandos de script usados pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="351e0-125">Describes the script commands used by Windows Media Player.</span></span>  |



 

> [!Note]  
> <span data-ttu-id="351e0-126">Nas versões anteriores do SDK do Windows Media Format, os fluxos de script eram usados para abrir endereços Web correspondentes ao conteúdo de um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="351e0-126">In previous versions of the Windows Media Format SDK, script streams were used to open Web addresses corresponding to the content of an ASF file.</span></span> <span data-ttu-id="351e0-127">Agora você pode usar fluxos da Web para trabalhar com páginas da Web sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="351e0-127">You can now use Web streams to work with synchronized Web pages.</span></span> <span data-ttu-id="351e0-128">Para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="351e0-128">For more information.</span></span> <span data-ttu-id="351e0-129">consulte [fluxos da Web](web-streams.md).</span><span class="sxs-lookup"><span data-stu-id="351e0-129">see [Web Streams](web-streams.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="351e0-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="351e0-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="351e0-131">**Comandos de script**</span><span class="sxs-lookup"><span data-stu-id="351e0-131">**Script Commands**</span></span>](script-commands.md)
</dt> <dt>

[<span data-ttu-id="351e0-132">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="351e0-132">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




