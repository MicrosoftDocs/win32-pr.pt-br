---
title: Comandos de script
description: Comandos de script
ms.assetid: b8d7d4d3-c0d3-4b09-b5dd-1c6bbc3f2020
keywords:
- SDK do Windows Media Format, comandos de script
- ASF (Advanced Systems Format), comandos de script
- ASF (formato de sistemas avançados), comandos de script
- SDK do Windows Media Format, fluxos de script
- ASF (Advanced Systems Format), fluxos de script
- ASF (formato de sistemas avançados), fluxos de script
- SDK do Windows Media Format, fluxos
- ASF (Advanced Systems Format), fluxos
- ASF (formato de sistemas avançados), fluxos
- scripts, comandos
- scripts, fluxos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57ab446a216624dc8f844f54298aeeaee358ac3
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104008570"
---
# <a name="script-commands"></a><span data-ttu-id="40fbf-114">Comandos de script</span><span class="sxs-lookup"><span data-stu-id="40fbf-114">Script Commands</span></span>

<span data-ttu-id="40fbf-115">Os comandos de script com suporte no Windows Media Format SDK são pares de nome e cadeia de caracteres de valor simples.</span><span class="sxs-lookup"><span data-stu-id="40fbf-115">The script commands supported by the Windows Media Format SDK are simple name and value string pairs.</span></span> <span data-ttu-id="40fbf-116">Por exemplo, um comando de script comum é "URL", que é usado pelo Windows Media Player e outros aplicativos de reprodução para abrir páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="40fbf-116">For example, a common script command is "URL", which is used by Windows Media Player and other playing applications to open Web pages.</span></span> <span data-ttu-id="40fbf-117">A outra metade do par de scripts para o comando "URL" contém um Uniform Resource Locator (URL) válido, como `https://www.adatum.com` .</span><span class="sxs-lookup"><span data-stu-id="40fbf-117">The other half of the script pair for "URL" command contains a valid uniform resource locator (URL), such as `https://www.adatum.com`.</span></span> <span data-ttu-id="40fbf-118">Nenhum suporte é fornecido pelos objetos deste SDK para comandos específicos; seu aplicativo deve incluir lógica para lidar com quaisquer comandos que você usar.</span><span class="sxs-lookup"><span data-stu-id="40fbf-118">No support is provided by the objects of this SDK for any specific commands; your application must include logic to handle whatever commands you use.</span></span> <span data-ttu-id="40fbf-119">Você pode usar os comandos com suporte do Windows Media Player para manter a compatibilidade com a maioria dos players.</span><span class="sxs-lookup"><span data-stu-id="40fbf-119">You can use the commands supported by Windows Media Player to maintain compatibility with most players.</span></span>

<span data-ttu-id="40fbf-120">Comandos de script podem ser entregues de uma das duas maneiras: em um fluxo de script ou no cabeçalho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="40fbf-120">Script commands can be delivered in one of two ways: in a script stream or in the file header.</span></span>

## <a name="script-streams"></a><span data-ttu-id="40fbf-121">Fluxos de script</span><span class="sxs-lookup"><span data-stu-id="40fbf-121">Script Streams</span></span>

<span data-ttu-id="40fbf-122">Você pode fornecer comandos de script em seu próprio fluxo em um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="40fbf-122">You can deliver script commands in their own stream in an ASF file.</span></span> <span data-ttu-id="40fbf-123">Cada exemplo em um fluxo de script contém as duas cadeias de caracteres do par nome/valor.</span><span class="sxs-lookup"><span data-stu-id="40fbf-123">Each sample in a script stream contains the two strings of the name/value pair.</span></span> <span data-ttu-id="40fbf-124">A vantagem de usar um fluxo de script é que os comandos serão entregues no momento da apresentação correto.</span><span class="sxs-lookup"><span data-stu-id="40fbf-124">The advantage of using a script stream is that the commands will be delivered at the correct presentation time.</span></span>

## <a name="script-commands-in-the-file-header"></a><span data-ttu-id="40fbf-125">Comandos de script no cabeçalho do arquivo</span><span class="sxs-lookup"><span data-stu-id="40fbf-125">Script Commands in the File Header</span></span>

<span data-ttu-id="40fbf-126">Comandos de script podem ser incluídos no cabeçalho do arquivo para recuperação no momento da reprodução.</span><span class="sxs-lookup"><span data-stu-id="40fbf-126">Script commands can be included in the file header for retrieval at the time of playback.</span></span> <span data-ttu-id="40fbf-127">O aplicativo de reprodução é responsável por executar os comandos de script no momento adequado.</span><span class="sxs-lookup"><span data-stu-id="40fbf-127">The playing application is responsible for executing the script commands at the proper time.</span></span> <span data-ttu-id="40fbf-128">A vantagem de usar comandos de script no cabeçalho do arquivo é que todos os comandos de script estão disponíveis antes de começar a receber exemplos.</span><span class="sxs-lookup"><span data-stu-id="40fbf-128">The advantage of using script commands in the file header is that all of the script commands are available before beginning to receive samples.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40fbf-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="40fbf-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40fbf-130">**Recursos de arquivo ASF**</span><span class="sxs-lookup"><span data-stu-id="40fbf-130">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="40fbf-131">**Usando comandos de script**</span><span class="sxs-lookup"><span data-stu-id="40fbf-131">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




