---
description: Visão geral do sistema DirectShow
ms.assetid: aea1ab83-4c48-4b61-8a20-0ee6ad62ebe3
title: Visão geral do sistema DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833fed4031c95ddb4ecbf91e7bb27c27741acc18
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500184"
---
# <a name="directshow-system-overview"></a><span data-ttu-id="c8b49-103">Visão geral do sistema DirectShow</span><span class="sxs-lookup"><span data-stu-id="c8b49-103">DirectShow System Overview</span></span>

<span data-ttu-id="c8b49-104">**O desafio do multimídia**</span><span class="sxs-lookup"><span data-stu-id="c8b49-104">**The Challenge of Multimedia**</span></span>

<span data-ttu-id="c8b49-105">Trabalhar com multimídia apresenta vários desafios importantes:</span><span class="sxs-lookup"><span data-stu-id="c8b49-105">Working with multimedia presents several major challenges:</span></span>

-   <span data-ttu-id="c8b49-106">Os fluxos de multimídia contêm grandes quantidades de dados, que devem ser processados muito rapidamente.</span><span class="sxs-lookup"><span data-stu-id="c8b49-106">Multimedia streams contain large amounts of data, which must be processed very quickly.</span></span>
-   <span data-ttu-id="c8b49-107">Áudio e vídeo devem ser sincronizados para que sejam iniciados e interrompidos ao mesmo tempo e sejam reproduzidos na mesma taxa.</span><span class="sxs-lookup"><span data-stu-id="c8b49-107">Audio and video must be synchronized so that it starts and stops at the same time, and plays at the same rate.</span></span>
-   <span data-ttu-id="c8b49-108">Os dados podem vir de várias fontes, incluindo arquivos locais, redes de computador, difusões de televisão e câmeras de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c8b49-108">Data can come from many sources, including local files, computer networks, television broadcasts, and video cameras.</span></span>
-   <span data-ttu-id="c8b49-109">Os dados vêm em uma variedade de formatos, como Audio-Video intercalado (AVI), ASF (Advanced Streaming Format), MPEG (Motion Picture Experts Group) e DV (Digital Video).</span><span class="sxs-lookup"><span data-stu-id="c8b49-109">Data comes in a variety of formats, such as Audio-Video Interleaved (AVI), Advanced Streaming Format (ASF), Motion Picture Experts Group (MPEG), and Digital Video (DV).</span></span>
-   <span data-ttu-id="c8b49-110">O programador não sabe com antecedência quais dispositivos de hardware estarão presentes no sistema do usuário final.</span><span class="sxs-lookup"><span data-stu-id="c8b49-110">The programmer does not know in advance what hardware devices will be present on the end-user's system.</span></span>

<span data-ttu-id="c8b49-111">**A solução do DirectShow**</span><span class="sxs-lookup"><span data-stu-id="c8b49-111">**The DirectShow Solution**</span></span>

<span data-ttu-id="c8b49-112">O DirectShow foi projetado para atender a cada um desses desafios.</span><span class="sxs-lookup"><span data-stu-id="c8b49-112">DirectShow is designed to address each of these challenges.</span></span> <span data-ttu-id="c8b49-113">Sua principal meta de design é simplificar a tarefa de criar aplicativos de mídia digital na plataforma Windows, isolando aplicativos das complexidades de transportes de dados, diferenças de hardware e sincronização.</span><span class="sxs-lookup"><span data-stu-id="c8b49-113">Its main design goal is to simplify the task of creating digital media applications on the Windows platform, by isolating applications from the complexities of data transports, hardware differences, and synchronization.</span></span>

<span data-ttu-id="c8b49-114">Para obter a taxa de transferência necessária para transmitir vídeo e áudio, o DirectShow usa Direct3D e DirectSound sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="c8b49-114">To achieve the throughput needed to stream video and audio, DirectShow uses Direct3D and DirectSound whenever possible.</span></span> <span data-ttu-id="c8b49-115">Essas tecnologias renderizam dados com eficiência para as placas gráficas e som do usuário.</span><span class="sxs-lookup"><span data-stu-id="c8b49-115">These technologies render data efficiently to the user's sound and graphics cards.</span></span> <span data-ttu-id="c8b49-116">O DirectShow sincroniza a reprodução ao encapsular dados de mídia em amostras com carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="c8b49-116">DirectShow synchronizes playback by encapsulating media data in time-stamped samples.</span></span> <span data-ttu-id="c8b49-117">Para lidar com a variedade de fontes, formatos e dispositivos de hardware que são possíveis, o DirectShow usa uma arquitetura modular, na qual o aplicativo combina e corresponde a diferentes componentes de software chamados *filtros*.</span><span class="sxs-lookup"><span data-stu-id="c8b49-117">To handle the variety of sources, formats, and hardware devices that are possible, DirectShow uses a modular architecture, in which the application mixes and matches different software components called *filters*.</span></span>

<span data-ttu-id="c8b49-118">O DirectShow fornece filtros que dão suporte à captura e ao ajuste de dispositivos baseados no Windows Driver Model (WDM), bem como filtros que dão suporte a placas de captura VfW (vídeo mais antigo para Windows) e codecs escritos para as interfaces do Gerenciador de compactação de áudio (ACM) e do Gerenciador de compactação de vídeo (VCM).</span><span class="sxs-lookup"><span data-stu-id="c8b49-118">DirectShow provides filters that support capture and tuning devices based on the Windows Driver Model (WDM), as well as filters that support older Video for Windows (VfW) capture cards, and codecs written for the Audio Compression Manager (ACM) and Video Compression Manager (VCM) interfaces.</span></span>

<span data-ttu-id="c8b49-119">O diagrama a seguir mostra a relação entre um aplicativo, os componentes do DirectShow e alguns dos componentes de hardware e software que o DirectShow suporta.</span><span class="sxs-lookup"><span data-stu-id="c8b49-119">The following diagram shows the relationship between an application, the DirectShow components, and some of the hardware and software components that DirectShow supports.</span></span>

![arquitetura de alto nível](images/arch-oview2.png)

<span data-ttu-id="c8b49-121">Conforme ilustrado aqui, os filtros do DirectShow se comunicam com, e controlam, uma ampla variedade de dispositivos, incluindo o sistema de arquivos local, o sintonizador de TV e os cartões de captura de vídeo, os codecs VfW, a tela de vídeo (por meio do DirectDraw ou GDI) e a placa de som (por meio do DirectSound).</span><span class="sxs-lookup"><span data-stu-id="c8b49-121">As illustrated here, DirectShow filters communicate with, and control, a wide variety of devices, including the local file system, TV tuner and video capture cards, VfW codecs, the video display (through DirectDraw or GDI), and the sound card (through DirectSound).</span></span> <span data-ttu-id="c8b49-122">Portanto, o DirectShow isola o aplicativo de muitas das complexidades desses dispositivos.</span><span class="sxs-lookup"><span data-stu-id="c8b49-122">Thus, DirectShow insulates the application from many of the complexities of these devices.</span></span> <span data-ttu-id="c8b49-123">O DirectShow também fornece filtros nativos de compactação e descompactação para determinados formatos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c8b49-123">DirectShow also provides native compression and decompression filters for certain file formats.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8b49-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c8b49-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8b49-125">Sobre o DirectShow</span><span class="sxs-lookup"><span data-stu-id="c8b49-125">About DirectShow</span></span>](about-directshow.md)
</dt> </dl>

 

 



