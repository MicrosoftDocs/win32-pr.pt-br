---
title: Sobre o DirectShow (SDK do Windows Media Format 11)
description: Sobre o DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- SDK do Windows Media Format, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- DirectShow, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd77507643edb220bc71a029779c88fe56760eae
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008749"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="b9442-107">Sobre o DirectShow (SDK do Windows Media Format 11)</span><span class="sxs-lookup"><span data-stu-id="b9442-107">About DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="b9442-108">O DirectShow é uma arquitetura de streaming de dados de alto nível, modular e extensível para a plataforma Windows.</span><span class="sxs-lookup"><span data-stu-id="b9442-108">DirectShow is a high-level, modular, extensible, data-streaming architecture for the Windows platform.</span></span> <span data-ttu-id="b9442-109">Ele fornece componentes de software subjacentes e APIs (interfaces de programação de aplicativo) para uma ampla variedade de aplicativos de áudio e vídeo digital no mercado atualmente.</span><span class="sxs-lookup"><span data-stu-id="b9442-109">It provides the underlying software components and application programming interfaces (APIs) for a wide variety of digital audio and video applications on the market today.</span></span> <span data-ttu-id="b9442-110">O DirectShow está disponível como parte do Microsoft DirectX Software Development Kit.</span><span class="sxs-lookup"><span data-stu-id="b9442-110">DirectShow is available as part of the Microsoft DirectX Software Development Kit.</span></span> <span data-ttu-id="b9442-111">Para saber mais sobre o DirectShow, consulte o SDK da plataforma Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b9442-111">To learn more about DirectShow, see the Microsoft Platform SDK.</span></span>

<span data-ttu-id="b9442-112">No DirectShow, todos os componentes de streaming de dados são chamados de *filtros*.</span><span class="sxs-lookup"><span data-stu-id="b9442-112">In DirectShow, all data streaming components are called *filters*.</span></span> <span data-ttu-id="b9442-113">Um filtro pode representar um dispositivo de hardware, um codificador ou decodificador de software, um processador de áudio ou vídeo ou qualquer recurso de processamento de vídeo de áudio.</span><span class="sxs-lookup"><span data-stu-id="b9442-113">A filter may represent a hardware device, a software encoder or decoder, an audio or video renderer, or any audio-video processing capability.</span></span> <span data-ttu-id="b9442-114">Para permitir que aplicativos baseados no DirectShow leiam e gravem conteúdo de formato de mídia do Windows, incluindo conteúdo protegido por DRM (Rights Management digital), a Microsoft fornece dois filtros que encapsulam partes do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="b9442-114">To enable DirectShow–based applications to read and write Windows Media Format content, including content protected by Digital Rights Management (DRM), Microsoft provides two filters that encapsulate portions of the Windows Media Format SDK.</span></span> <span data-ttu-id="b9442-115">Esses são os [leitores ASF do WM](wm-asf-reader-filter.md) e o [gravador ASF do WM](wm-asf-writer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="b9442-115">These are the [WM ASF Reader](wm-asf-reader-filter.md) and the [WM ASF Writer](wm-asf-writer-filter.md).</span></span> <span data-ttu-id="b9442-116">Esses filtros e as interfaces que eles expõem são coletivamente chamados de componentes QASF, após a DLL na qual eles são empacotados.</span><span class="sxs-lookup"><span data-stu-id="b9442-116">These filters and the interfaces they expose are collectively referred to as the QASF components, after the DLL in which they are packaged.</span></span> <span data-ttu-id="b9442-117">(O Q significa o Quartz, um nome de código inicial para o DirectShow.)</span><span class="sxs-lookup"><span data-stu-id="b9442-117">(The Q stands for Quartz, an early code name for DirectShow.)</span></span>

> [!Note]  
> <span data-ttu-id="b9442-118">O uso dos codecs do Windows Media Audio e vídeo 9 Series por meio dos componentes do QASF do DirectShow requer o Microsoft Windows Millennium Edition ou posterior, ou o DirectX 8,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="b9442-118">The use of the Windows Media Audio and Video 9 Series codecs through the DirectShow QASF components requires Microsoft Windows Millennium Edition or later, or DirectX 8.0 or later.</span></span>

 

<span data-ttu-id="b9442-119">O diagrama a seguir mostra um grafo de filtro do DirectShow para reproduzir arquivos de vídeo de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="b9442-119">The following diagram shows a DirectShow filter graph for playing back Windows Media Video files.</span></span>

![Grafo de reprodução de vídeo do Windows Media](images/wmv-wmasfreader.png)

<span data-ttu-id="b9442-121">O [leitor de ASF do WM](wm-asf-reader-filter.md) é um componente do QASF, os decodificadores são componentes do Windows Media Format SDK hospedados no filtro de invólucro do DMO (um componente QASF) e os renderizadores são componentes do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="b9442-121">The [WM ASF Reader](wm-asf-reader-filter.md) is a QASF component, the decoders are Windows Media Format SDK components hosted in the DMO Wrapper filter (a QASF component), and the renderers are DirectShow components.</span></span>

 

 




