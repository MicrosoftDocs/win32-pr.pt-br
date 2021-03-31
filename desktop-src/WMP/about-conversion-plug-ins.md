---
title: Sobre plug-ins de conversão
description: Sobre plug-ins de conversão
ms.assetid: bd6d1020-e8e1-492e-9c76-9f3cf04190de
keywords:
- Windows Media Player, plug-ins de conversão
- Plug-ins do Windows Media Player, conversão
- plug-ins, conversão
- plug-ins de conversão, sobre
- Advanced Systems Format (ASF)
- ASF (formato de sistemas avançados)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada6e2a8fa41b657a593dc03082f871503b53eba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635086"
---
# <a name="about-conversion-plug-ins"></a><span data-ttu-id="80ae9-109">Sobre plug-ins de conversão</span><span class="sxs-lookup"><span data-stu-id="80ae9-109">About Conversion Plug-ins</span></span>

<span data-ttu-id="80ae9-110">Você pode criar um plug-in do Windows Media Player para converter arquivos de mídia digital criados usando tecnologias não fornecidas pela Microsoft no formato ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="80ae9-110">You can create a Windows Media Player plug-in to convert digital media files that are created using technologies not provided by Microsoft, into Advanced Systems Format (ASF).</span></span>

<span data-ttu-id="80ae9-111">Os plug-ins de conversão são objetos de Component Object Model (COM) que são empacotados e distribuídos como arquivos executáveis (. exe).</span><span class="sxs-lookup"><span data-stu-id="80ae9-111">Conversion plug-ins are Component Object Model (COM) objects that are packaged and distributed as executable (.exe) files.</span></span> <span data-ttu-id="80ae9-112">O Windows Media Player instancia os plug-ins de conversão para converter formatos de mídia digital de terceiros nos seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="80ae9-112">Windows Media Player instantiates conversion plug-ins to convert third-party digital media formats in the following scenarios:</span></span>

-   <span data-ttu-id="80ae9-113">O conteúdo de mídia digital é copiado para o computador de um dispositivo portátil.</span><span class="sxs-lookup"><span data-stu-id="80ae9-113">Digital media content is copied to the computer from a portable device.</span></span>
-   <span data-ttu-id="80ae9-114">O conteúdo de mídia digital é adicionado à biblioteca usando **IWMPMediaCollection:: Add**.</span><span class="sxs-lookup"><span data-stu-id="80ae9-114">Digital media content is added to the library by using **IWMPMediaCollection::add**.</span></span>
-   <span data-ttu-id="80ae9-115">O conteúdo de mídia digital é adicionado à biblioteca usando o recurso de pesquisa do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="80ae9-115">Digital media content is added to the library by using the search feature of Windows Media Player.</span></span>
-   <span data-ttu-id="80ae9-116">O conteúdo de mídia digital é adicionado à biblioteca pelo recurso de monitoramento de pasta do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="80ae9-116">Digital media content is added to the library by the folder monitoring feature of Windows Media Player.</span></span>
-   <span data-ttu-id="80ae9-117">O conteúdo de mídia digital é adicionado à lista de sincronização quando o usuário arrasta e descarta um arquivo.</span><span class="sxs-lookup"><span data-stu-id="80ae9-117">Digital media content is added to the sync list when the user drags and drops a file.</span></span>

<span data-ttu-id="80ae9-118">Depois que o Windows Media Player cria uma instância de um plug-in de conversão, o plug-in deve converter o arquivo fornecido em ASF ou WMA e adicionar metadados relevantes.</span><span class="sxs-lookup"><span data-stu-id="80ae9-118">After Windows Media Player creates an instance of a conversion plug-in, the plug-in must convert the supplied file to ASF or WMA and add relevant metadata.</span></span> <span data-ttu-id="80ae9-119">(Não use o plug-in de conversão para transcodificar o arquivo.) O plug-in deve copiar o arquivo convertido para a pasta especificada e retornar o caminho para o novo arquivo para o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="80ae9-119">(Do not use the conversion plug-in to transcode the file.) The plug-in must then copy the converted file to the specified folder and return the path to the new file to Windows Media Player.</span></span>

<span data-ttu-id="80ae9-120">Os plug-ins de conversão devem implementar a interface **IWMPConvert** .</span><span class="sxs-lookup"><span data-stu-id="80ae9-120">Conversion plug-ins must implement the **IWMPConvert** interface.</span></span> <span data-ttu-id="80ae9-121">Consulte [referência de programação de plug-ins de conversão](conversion-plug-ins-programming-reference.md).</span><span class="sxs-lookup"><span data-stu-id="80ae9-121">See [Conversion Plug-ins Programming Reference](conversion-plug-ins-programming-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="80ae9-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="80ae9-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80ae9-123">**Sobre o processo de conversão**</span><span class="sxs-lookup"><span data-stu-id="80ae9-123">**About the Conversion Process**</span></span>](about-the-conversion-process.md)
</dt> <dt>

[<span data-ttu-id="80ae9-124">**Adicionando metadados a arquivos convertidos**</span><span class="sxs-lookup"><span data-stu-id="80ae9-124">**Adding Metadata to Converted Files**</span></span>](adding-metadata-to-converted-files.md)
</dt> <dt>

[<span data-ttu-id="80ae9-125">**Plug-ins de conversão do Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="80ae9-125">**Windows Media Player Conversion Plug-ins**</span></span>](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




