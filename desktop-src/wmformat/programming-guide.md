---
title: Guia de programação do Windows Media Format SDK
description: Guia de programação do Windows Media Format SDK
ms.assetid: 9b382c88-e4a9-4aed-a250-250fabface44
keywords:
- SDK do Windows Media Format, guia de programação
- SDK do Windows Media Format, formato de sistemas avançados (ASF)
- ASF (Advanced Systems Format), guia de programação
- ASF (formato de sistemas avançados), guia de programação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4ea4f6819a31693d7c9d149717324ef6dcc65a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105764464"
---
# <a name="windows-media-format-sdk-programming-guide"></a><span data-ttu-id="1ad95-107">Guia de programação do Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="1ad95-107">Windows Media Format SDK Programming Guide</span></span>

<span data-ttu-id="1ad95-108">O guia de programação destina-se a ajudá-lo a aprender a usar o SDK (Software Development Kit) do Microsoft Windows Media Format para criar aplicativos que funcionam com arquivos usando o ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="1ad95-108">The Programming Guide is intended to help you learn how to use the Microsoft Windows Media Format Software Development Kit (SDK) to build applications that work with files using the Advanced Systems Format (ASF).</span></span>

<span data-ttu-id="1ad95-109">Você pode usar o Windows Media Format SDK para criar aplicativos que gravam fluxos de mídia digital e ler fluxos de arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="1ad95-109">You can use the Windows Media Format SDK to create applications that write digital media streams to and read streams from ASF files.</span></span> <span data-ttu-id="1ad95-110">Esse SDK também dá suporte à edição de metadados em arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="1ad95-110">This SDK also supports the editing of metadata in ASF files.</span></span> <span data-ttu-id="1ad95-111">Além disso, esse SDK pode ser usado para ler e manipular metadados em arquivos MP3.</span><span class="sxs-lookup"><span data-stu-id="1ad95-111">In addition, this SDK can be used to read and manipulate metadata in MP3 files.</span></span>

<span data-ttu-id="1ad95-112">As seções a seguir explicam detalhadamente as etapas necessárias para gravar, ler e editar arquivos ASF usando esse SDK.</span><span class="sxs-lookup"><span data-stu-id="1ad95-112">The following sections explain in detail the steps required to write, read, and edit ASF files by using this SDK.</span></span>



| <span data-ttu-id="1ad95-113">Seção</span><span class="sxs-lookup"><span data-stu-id="1ad95-113">Section</span></span>                                                                            | <span data-ttu-id="1ad95-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ad95-114">Description</span></span>                                                                                                       |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ad95-115">Introdução</span><span class="sxs-lookup"><span data-stu-id="1ad95-115">Getting Started</span></span>](getting-started.md)                                             | <span data-ttu-id="1ad95-116">Fornece informações gerais sobre como preparar-se para usar este SDK.</span><span class="sxs-lookup"><span data-stu-id="1ad95-116">Provides general information about getting ready to use this SDK.</span></span>                                                 |
| [<span data-ttu-id="1ad95-117">Usando os métodos de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="1ad95-117">Using the Callback Methods</span></span>](using-the-callback-methods.md)                       | <span data-ttu-id="1ad95-118">Descreve os métodos de retorno de chamada usados em muitas tarefas diferentes.</span><span class="sxs-lookup"><span data-stu-id="1ad95-118">Describes the callback methods used in many different tasks.</span></span>                                                      |
| [<span data-ttu-id="1ad95-119">Trabalhando com perfis</span><span class="sxs-lookup"><span data-stu-id="1ad95-119">Working with Profiles</span></span>](working-with-profiles.md)                                 | <span data-ttu-id="1ad95-120">Descreve como usar, editar e criar perfis.</span><span class="sxs-lookup"><span data-stu-id="1ad95-120">Describes how to use, edit, and create profiles.</span></span>                                                                  |
| [<span data-ttu-id="1ad95-121">Gravando arquivos ASF</span><span class="sxs-lookup"><span data-stu-id="1ad95-121">Writing ASF Files</span></span>](writing-asf-files.md)                                         | <span data-ttu-id="1ad95-122">Descreve como usar o objeto Writer para criar arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="1ad95-122">Describes how to use the writer object to create ASF files.</span></span>                                                       |
| [<span data-ttu-id="1ad95-123">Lendo arquivos ASF</span><span class="sxs-lookup"><span data-stu-id="1ad95-123">Reading ASF Files</span></span>](reading-asf-files.md)                                         | <span data-ttu-id="1ad95-124">Descreve como receber conteúdo de arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="1ad95-124">Describes how to receive content from ASF files.</span></span>                                                                  |
| [<span data-ttu-id="1ad95-125">Trabalhando com metadados</span><span class="sxs-lookup"><span data-stu-id="1ad95-125">Working with Metadata</span></span>](working-with-metadata.md)                                 | <span data-ttu-id="1ad95-126">Descreve como gerenciar o conteúdo da seção de cabeçalho de um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="1ad95-126">Describes how to manage the contents of the header section of an ASF file.</span></span>                                        |
| [<span data-ttu-id="1ad95-127">Trabalhando com índices</span><span class="sxs-lookup"><span data-stu-id="1ad95-127">Working with Indexes</span></span>](working-with-indexes.md)                                   | <span data-ttu-id="1ad95-128">Descreve como trabalhar com índices.</span><span class="sxs-lookup"><span data-stu-id="1ad95-128">Describes how to work with indexes.</span></span>                                                                               |
| [<span data-ttu-id="1ad95-129">Trabalhando com perfis</span><span class="sxs-lookup"><span data-stu-id="1ad95-129">Working with Profiles</span></span>](working-with-profiles.md)                                 | <span data-ttu-id="1ad95-130">Descreve como usar, editar e criar perfis.</span><span class="sxs-lookup"><span data-stu-id="1ad95-130">Describes how to use, edit, and create profiles.</span></span>                                                                  |
| [<span data-ttu-id="1ad95-131">Usando comandos de script</span><span class="sxs-lookup"><span data-stu-id="1ad95-131">Using Script Commands</span></span>](using-script-commands.md)                                 | <span data-ttu-id="1ad95-132">Descreve como usar comandos de script em seus arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="1ad95-132">Describes how to use script commands in your ASF files.</span></span>                                                           |
| [<span data-ttu-id="1ad95-133">Copiando dados de um arquivo para outro</span><span class="sxs-lookup"><span data-stu-id="1ad95-133">Copying Data from One File to Another</span></span>](copying-data-from-one-file-to-another.md) | <span data-ttu-id="1ad95-134">Descreve como copiar dados de um arquivo ASF para outro, com sem decodificação e codificação.</span><span class="sxs-lookup"><span data-stu-id="1ad95-134">Describes how to copy data from one ASF file to another, with without decoding and encoding.</span></span>                      |
| [<span data-ttu-id="1ad95-135">Habilitando o suporte a DRM</span><span class="sxs-lookup"><span data-stu-id="1ad95-135">Enabling DRM Support</span></span>](enabling-drm-support.md)                                   | <span data-ttu-id="1ad95-136">Descreve como habilitar o suporte para reprodução de arquivos ASF protegidos por DRM.</span><span class="sxs-lookup"><span data-stu-id="1ad95-136">Describes how to enable support for playback of DRM-protected ASF files.</span></span>                                          |
| [<span data-ttu-id="1ad95-137">Implementando a funcionalidade de rede</span><span class="sxs-lookup"><span data-stu-id="1ad95-137">Implementing Network Functionality</span></span>](implementing-network-functionality.md)       | <span data-ttu-id="1ad95-138">Descreve o uso desse SDK para executar as operações de rede que são essenciais para a mídia de streaming bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1ad95-138">Describes the use of this SDK to perform the network operations that are essential to successful streaming media.</span></span> |
| [<span data-ttu-id="1ad95-139">Tópicos avançados</span><span class="sxs-lookup"><span data-stu-id="1ad95-139">Advanced Topics</span></span>](advanced-topics.md)                                             | <span data-ttu-id="1ad95-140">Descreve como usar alguns dos recursos avançados deste SDK em seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="1ad95-140">Describes how to use some of the advanced features of this SDK in your applications.</span></span>                              |
| [<span data-ttu-id="1ad95-141">DirectShow e Windows Media</span><span class="sxs-lookup"><span data-stu-id="1ad95-141">DirectShow and Windows Media</span></span>](directshow-and-windows-media.md)                   | <span data-ttu-id="1ad95-142">Descreve como você pode usar o Microsoft DirectShow para criar e ler arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="1ad95-142">Describes how you can use Microsoft DirectShow to create and read ASF files.</span></span>                                      |
| [<span data-ttu-id="1ad95-143">Considerações sobre o projeto</span><span class="sxs-lookup"><span data-stu-id="1ad95-143">Project Considerations</span></span>](project-considerations.md)                               | <span data-ttu-id="1ad95-144">Fornece detalhes sobre como concluir e distribuir seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="1ad95-144">Provides details about finishing and distributing your applications.</span></span>                                              |



 

## <a name="related-topics"></a><span data-ttu-id="1ad95-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1ad95-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ad95-146">**Sobre o SDK do Windows Media Format**</span><span class="sxs-lookup"><span data-stu-id="1ad95-146">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> <dt>

[<span data-ttu-id="1ad95-147">**SDK do Windows Media Format 11**</span><span class="sxs-lookup"><span data-stu-id="1ad95-147">**Windows Media Format 11 SDK**</span></span>](windows-media-format-11-sdk.md)
</dt> </dl>

 

 




