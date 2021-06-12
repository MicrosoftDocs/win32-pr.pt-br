---
title: Saiba mais sobre o DirectShow no SDK do Windows Media Format 11, uma arquitetura de streaming de dados de alto nível, modular, extensível para a plataforma Windows.
description: Sobre o DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- DirectShow,sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a76d7c8971c452f01176be7472e313181eb2831
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011289"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="a42a5-107">Sobre o DirectShow (Windows Media Format SDK 11)</span><span class="sxs-lookup"><span data-stu-id="a42a5-107">About DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="a42a5-108">O DirectShow é uma arquitetura de streaming de dados de alto nível, modular, extensível para a plataforma Windows.</span><span class="sxs-lookup"><span data-stu-id="a42a5-108">DirectShow is a high-level, modular, extensible, data-streaming architecture for the Windows platform.</span></span> <span data-ttu-id="a42a5-109">Ele fornece os componentes de software subjacentes e as APIs (interfaces de programação de aplicativo) para uma ampla variedade de aplicativos digitais de áudio e vídeo no mercado atualmente.</span><span class="sxs-lookup"><span data-stu-id="a42a5-109">It provides the underlying software components and application programming interfaces (APIs) for a wide variety of digital audio and video applications on the market today.</span></span> <span data-ttu-id="a42a5-110">O DirectShow está disponível como parte do Microsoft DirectX Software Development Kit.</span><span class="sxs-lookup"><span data-stu-id="a42a5-110">DirectShow is available as part of the Microsoft DirectX Software Development Kit.</span></span> <span data-ttu-id="a42a5-111">Para saber mais sobre o DirectShow, confira o SDK da Plataforma Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a42a5-111">To learn more about DirectShow, see the Microsoft Platform SDK.</span></span>

<span data-ttu-id="a42a5-112">No DirectShow, todos os componentes de streaming de dados são chamados de *filtros*.</span><span class="sxs-lookup"><span data-stu-id="a42a5-112">In DirectShow, all data streaming components are called *filters*.</span></span> <span data-ttu-id="a42a5-113">Um filtro pode representar um dispositivo de hardware, um codificador ou decodificador de software, um renderador de áudio ou vídeo ou qualquer capacidade de processamento de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="a42a5-113">A filter may represent a hardware device, a software encoder or decoder, an audio or video renderer, or any audio-video processing capability.</span></span> <span data-ttu-id="a42a5-114">Para permitir que aplicativos baseados em DirectShow leiam e escrevam conteúdo Windows Media Format, incluindo conteúdo protegido pelo DRM (Digital Rights Management), a Microsoft fornece dois filtros que encapsulam partes do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="a42a5-114">To enable DirectShow–based applications to read and write Windows Media Format content, including content protected by Digital Rights Management (DRM), Microsoft provides two filters that encapsulate portions of the Windows Media Format SDK.</span></span> <span data-ttu-id="a42a5-115">Estes são o [Leitor do WM ASF](wm-asf-reader-filter.md) e o [Wm ASF Writer.](wm-asf-writer-filter.md)</span><span class="sxs-lookup"><span data-stu-id="a42a5-115">These are the [WM ASF Reader](wm-asf-reader-filter.md) and the [WM ASF Writer](wm-asf-writer-filter.md).</span></span> <span data-ttu-id="a42a5-116">Esses filtros e as interfaces que eles expõem são coletivamente chamados de componentes qaSF, após a DLL na qual eles são empacotados.</span><span class="sxs-lookup"><span data-stu-id="a42a5-116">These filters and the interfaces they expose are collectively referred to as the QASF components, after the DLL in which they are packaged.</span></span> <span data-ttu-id="a42a5-117">(O Q significa Ltda, um nome de código antecipado para DirectShow.)</span><span class="sxs-lookup"><span data-stu-id="a42a5-117">(The Q stands for Quartz, an early code name for DirectShow.)</span></span>

> [!Note]  
> <span data-ttu-id="a42a5-118">O uso dos codecs do Windows Media Audio and Video 9 Series por meio dos componentes qaSF do DirectShow requer o Microsoft Windows Millennium Edition ou posterior ou o DirectX 8.0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="a42a5-118">The use of the Windows Media Audio and Video 9 Series codecs through the DirectShow QASF components requires Microsoft Windows Millennium Edition or later, or DirectX 8.0 or later.</span></span>

 

<span data-ttu-id="a42a5-119">O diagrama a seguir mostra um grafo de filtro do DirectShow para reprodução de arquivos de Vídeo de Mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="a42a5-119">The following diagram shows a DirectShow filter graph for playing back Windows Media Video files.</span></span>

![grafo de reprodução de vídeo de mídia do Windows](images/wmv-wmasfreader.png)

<span data-ttu-id="a42a5-121">O [Leitor do WM ASF](wm-asf-reader-filter.md) é um componente qaSF, os decodificadores são componentes do SDK do Windows Media Format hospedados no filtro wrapper do DMO (um componente QASF) e os renderadores são componentes do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="a42a5-121">The [WM ASF Reader](wm-asf-reader-filter.md) is a QASF component, the decoders are Windows Media Format SDK components hosted in the DMO Wrapper filter (a QASF component), and the renderers are DirectShow components.</span></span>

 

 




