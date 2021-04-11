---
description: Aplicativos de DVD
ms.assetid: 6f41e0f1-e550-4ca6-9a80-ce4d498289e2
title: Aplicativos de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acaddc683078acff84b7c90689f82becfb7b1d7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104296019"
---
# <a name="dvd-applications"></a><span data-ttu-id="b3851-103">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="b3851-103">DVD Applications</span></span>

<span data-ttu-id="b3851-104">O DirectShow fornece um componente chamado de filtro de origem do [navegador de DVD](dvd-navigator-filter.md) , que simplifica as tarefas de navegação de DVD em C++.</span><span class="sxs-lookup"><span data-stu-id="b3851-104">DirectShow provides a component called the [DVD Navigator](dvd-navigator-filter.md) source filter which simplifies DVD navigation tasks in C++.</span></span> <span data-ttu-id="b3851-105">O navegador de DVD tem todos os recursos que você encontra em um player de DVD autônomo completo, além de recursos adicionais específicos para a reprodução de DVDs em computadores pessoais.</span><span class="sxs-lookup"><span data-stu-id="b3851-105">The DVD Navigator has all the capabilities that you find on a full-featured stand-alone DVD player, plus additional capabilities specific to playing DVDs on personal computers.</span></span> <span data-ttu-id="b3851-106">Usando o DVD Navigator, o C++ e os desenvolvedores de scripts podem criar aplicativos de DVD completos sem referir-se à especificação do DVD.</span><span class="sxs-lookup"><span data-stu-id="b3851-106">Using the DVD Navigator, C++ and scripting developers can create full-featured DVD applications without referring to the DVD specification.</span></span> <span data-ttu-id="b3851-107">O navegador de DVD, em coordenação com os filtros de decodificador, também lida com gerenciamento regional e proteção de direitos autorais (CSS e proteção de cópia analógica), isolando os desenvolvedores de aplicativos desses detalhes.</span><span class="sxs-lookup"><span data-stu-id="b3851-107">The DVD Navigator, in coordination with the decoder filters, also handles regional management and copyright protection (CSS and analog copy protection), isolating application developers from these details.</span></span>

<span data-ttu-id="b3851-108">O filtro de navegador de DVD funciona em um volume DVD-Video inteiro, que consiste nos arquivos no \_ diretório TS de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b3851-108">The DVD Navigator filter works across an entire DVD-Video volume, which consists of the files in the VIDEO\_TS directory.</span></span> <span data-ttu-id="b3851-109">Ao contrário da maioria dos filtros de origem do DirectShow que funcionam com fluxos ou arquivos individuais, o navegador de DVD usa a estrutura DVD-Video de títulos, capítulos e códigos de tempo.</span><span class="sxs-lookup"><span data-stu-id="b3851-109">Unlike most DirectShow source filters that work with individual streams or files, the DVD Navigator uses the DVD-Video structure of titles, chapters, and time codes.</span></span> <span data-ttu-id="b3851-110">Os desenvolvedores que desejam reproduzir arquivos MPEG-2 individuais no DirectShow devem usar o [demultiplexador MPEG-2](mpeg-2-demultiplexer.md) em vez do filtro do navegador de DVD.</span><span class="sxs-lookup"><span data-stu-id="b3851-110">Developers wishing to play individual MPEG-2 files in DirectShow should use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) instead of the DVD Navigator filter.</span></span> <span data-ttu-id="b3851-111">Consulte [suporte a MPEG-2 no DirectShow](mpeg-2-support-in-directshow.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="b3851-111">See [MPEG-2 Support in DirectShow](mpeg-2-support-in-directshow.md) for more information.</span></span>

> [!Note]  
> <span data-ttu-id="b3851-112">Para reproduzir DVDs, o usuário deve ter um decodificador MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="b3851-112">To play DVDs, the user must have an MPEG-2 decoder.</span></span>

 

<span data-ttu-id="b3851-113">Esta seção contém os seguintes tópicos.</span><span class="sxs-lookup"><span data-stu-id="b3851-113">This section contains the following topics.</span></span>

-   [<span data-ttu-id="b3851-114">Recursos de suporte a DVD no DirectShow</span><span class="sxs-lookup"><span data-stu-id="b3851-114">DVD Support Features in DirectShow</span></span>](dvd-support-features-in-directshow.md)
-   [<span data-ttu-id="b3851-115">Noções básicas de DVD</span><span class="sxs-lookup"><span data-stu-id="b3851-115">DVD Basics</span></span>](dvd-basics.md)
-   [<span data-ttu-id="b3851-116">Criando o grafo de filtro de DVD</span><span class="sxs-lookup"><span data-stu-id="b3851-116">Building the DVD Filter Graph</span></span>](building-the-dvd-filter-graph.md)
-   [<span data-ttu-id="b3851-117">Obtendo os ponteiros de interface de DVD</span><span class="sxs-lookup"><span data-stu-id="b3851-117">Obtaining the DVD Interface Pointers</span></span>](obtaining-the-dvd-interface-pointers.md)
-   [<span data-ttu-id="b3851-118">Comandos de DVD</span><span class="sxs-lookup"><span data-stu-id="b3851-118">DVD Commands</span></span>](dvd-commands.md)
-   [<span data-ttu-id="b3851-119">Identificando operações de DVD válidas</span><span class="sxs-lookup"><span data-stu-id="b3851-119">Identifying Valid DVD Operations</span></span>](identifying-valid-dvd-operations.md)
-   [<span data-ttu-id="b3851-120">Sincronizando comandos de DVD</span><span class="sxs-lookup"><span data-stu-id="b3851-120">Synchronizing DVD Commands</span></span>](synchronizing-dvd-commands.md)
-   [<span data-ttu-id="b3851-121">Fluxo de dados no navegador de DVD</span><span class="sxs-lookup"><span data-stu-id="b3851-121">Data Flow in the DVD Navigator</span></span>](data-flow-in-the-dvd-navigator.md)
-   [<span data-ttu-id="b3851-122">Manipulando notificações de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="b3851-122">Handling DVD Event Notifications</span></span>](handling-dvd-event-notifications.md)
-   [<span data-ttu-id="b3851-123">Trabalhando com menus de DVD</span><span class="sxs-lookup"><span data-stu-id="b3851-123">Working With DVD Menus</span></span>](working-with-dvd-menus.md)
-   [<span data-ttu-id="b3851-124">Fluxos de áudio e subimagem</span><span class="sxs-lookup"><span data-stu-id="b3851-124">Audio and Subpicture Streams</span></span>](audio-and-subpicture-streams.md)
-   [<span data-ttu-id="b3851-125">Impondo níveis de gerenciamento de pais</span><span class="sxs-lookup"><span data-stu-id="b3851-125">Enforcing Parental Management Levels</span></span>](enforcing-parental-management-levels.md)
-   [<span data-ttu-id="b3851-126">Salvando e restaurando objetos DvdState</span><span class="sxs-lookup"><span data-stu-id="b3851-126">Saving and Restoring DvdState Objects</span></span>](saving-and-restoring-dvdstate-objects.md)
-   [<span data-ttu-id="b3851-127">Trabalhando com cadeias de caracteres de texto em DVD</span><span class="sxs-lookup"><span data-stu-id="b3851-127">Working with DVD Text Strings</span></span>](working-with-dvd-text-strings.md)
-   [<span data-ttu-id="b3851-128">Reprodução de fluxos de áudio do karaokê</span><span class="sxs-lookup"><span data-stu-id="b3851-128">Playing Karaoke Audio Streams</span></span>](playing-karaoke-audio-streams.md)
-   [<span data-ttu-id="b3851-129">Lidando com Ejetações de disco</span><span class="sxs-lookup"><span data-stu-id="b3851-129">Handling Disc Ejections</span></span>](handling-disc-ejections.md)
-   [<span data-ttu-id="b3851-130">Aprimoramentos na reprodução de DVD no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b3851-130">DVD Playback Enhancements in Windows Vista</span></span>](dvd-playback-enhancements-in-windows-vista.md)
-   [<span data-ttu-id="b3851-131">Configuração de grafo de filtro de DVD</span><span class="sxs-lookup"><span data-stu-id="b3851-131">DVD Filter Graph Configuration</span></span>](dvd-filter-graph-configuration.md)
-   [<span data-ttu-id="b3851-132">Atalhos para páginas de referência de DVD do C++</span><span class="sxs-lookup"><span data-stu-id="b3851-132">Shortcuts to C++ DVD Reference Pages</span></span>](shortcuts-to-c-dvd-reference-pages.md)

<span data-ttu-id="b3851-133">Para obter referências sobre o desenvolvimento de decodificadores de DVD/MPEG2, consulte [desenvolvimento de decodificador de DVD no DirectShow](dvd-decoder-development-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="b3851-133">For references on DVD/MPEG2 decoder development, see [DVD Decoder Development in DirectShow](dvd-decoder-development-in-directshow.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3851-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b3851-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3851-135">Usando o DirectShow</span><span class="sxs-lookup"><span data-stu-id="b3851-135">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



