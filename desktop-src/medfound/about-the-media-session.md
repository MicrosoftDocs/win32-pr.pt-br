---
description: Sobre a sessão de mídia
ms.assetid: 09f50b11-0e0a-42b6-a7bf-bb0135343351
title: Sobre a sessão de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc490e63f623fb3c2d5efde5a80f1988566f9345
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930086"
---
# <a name="about-the-media-session"></a><span data-ttu-id="dcdb6-103">Sobre a sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="dcdb6-103">About the Media Session</span></span>

<span data-ttu-id="dcdb6-104">A sessão de mídia expõe a interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) .</span><span class="sxs-lookup"><span data-stu-id="dcdb6-104">The Media Session exposes the [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface.</span></span> <span data-ttu-id="dcdb6-105">Há duas maneiras de criar a sessão de mídia, dependendo se seu aplicativo oferecerá suporte a conteúdo protegido:</span><span class="sxs-lookup"><span data-stu-id="dcdb6-105">There are two ways to create the Media Session, depending on whether your application will support protected content:</span></span>

-   <span data-ttu-id="dcdb6-106">Se seu aplicativo não oferecer suporte a conteúdo protegido, você poderá criar a sessão de mídia chamando o [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession).</span><span class="sxs-lookup"><span data-stu-id="dcdb6-106">If your application does not support protected content, you can create the Media Session by calling the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession).</span></span> <span data-ttu-id="dcdb6-107">Essa função cria a sessão de mídia dentro do processo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dcdb6-107">This function creates the Media Session inside the application process.</span></span>
-   <span data-ttu-id="dcdb6-108">Para dar suporte ao conteúdo protegido, crie a sessão de mídia chamando [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span><span class="sxs-lookup"><span data-stu-id="dcdb6-108">To support protected content, create the Media Session by calling [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span></span> <span data-ttu-id="dcdb6-109">Essa função cria a sessão de mídia dentro do processo do caminho de mídia protegido (PMP).</span><span class="sxs-lookup"><span data-stu-id="dcdb6-109">This function creates the Media Session inside the Protected Media Path (PMP) process.</span></span> <span data-ttu-id="dcdb6-110">O aplicativo recebe um ponteiro para um objeto proxy que realiza o marshaling de chamadas de método entre o limite do processo.</span><span class="sxs-lookup"><span data-stu-id="dcdb6-110">The application receives a pointer to a proxy object that marshals method calls across the process boundary.</span></span> <span data-ttu-id="dcdb6-111">Observe que a sessão de mídia do PMP pode ser usada para reproduzir conteúdo não criptografado, bem como conteúdo protegido.</span><span class="sxs-lookup"><span data-stu-id="dcdb6-111">Note that the PMP Media Session can be used to play clear content, as well as protected content.</span></span>

<span data-ttu-id="dcdb6-112">Qualquer aplicativo que use a sessão de mídia seguirá estas etapas gerais:</span><span class="sxs-lookup"><span data-stu-id="dcdb6-112">Any application that uses the Media Session will follow these general steps:</span></span>

1.  <span data-ttu-id="dcdb6-113">Crie uma topologia.</span><span class="sxs-lookup"><span data-stu-id="dcdb6-113">Create a topology.</span></span>
2.  <span data-ttu-id="dcdb6-114">Enfileirar a topologia na sessão de mídia chamando [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="dcdb6-114">Queue the topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>
3.  <span data-ttu-id="dcdb6-115">Controle o fluxo de dados chamando [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)ou [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span><span class="sxs-lookup"><span data-stu-id="dcdb6-115">Control the flow of data by calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause), or [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span></span>
4.  <span data-ttu-id="dcdb6-116">Antes de o aplicativo sair, chame [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) para fechar a sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="dcdb6-116">Before the application exits, call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the Media Session.</span></span>
5.  <span data-ttu-id="dcdb6-117">Desligue todas as fontes de mídia criadas pelo aplicativo chamando [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span><span class="sxs-lookup"><span data-stu-id="dcdb6-117">Shut down any media sources that the application created, by calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span>
6.  <span data-ttu-id="dcdb6-118">Desligue a sessão de mídia chamando [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span><span class="sxs-lookup"><span data-stu-id="dcdb6-118">Shut down the Media Session by calling [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span>

<span data-ttu-id="dcdb6-119">Ao usar a sessão de mídia, o aplicativo não deve iniciar, pausar ou parar diretamente a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="dcdb6-119">When using the Media Session, the application should not directly start, pause, or stop the media source.</span></span> <span data-ttu-id="dcdb6-120">Todas as alterações de estado devem ser iniciadas chamando métodos [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) .</span><span class="sxs-lookup"><span data-stu-id="dcdb6-120">All state changes must be initiated by calling [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) methods.</span></span> <span data-ttu-id="dcdb6-121">As alterações de estado na origem da mídia são manipuladas pela sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="dcdb6-121">State changes in the media source are handled by the Media Session.</span></span>

<span data-ttu-id="dcdb6-122">Muitos outros detalhes dependerão da funcionalidade específica do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dcdb6-122">Many other details will depend on the specific functionality of your application.</span></span>

## <a name="protected-content"></a><span data-ttu-id="dcdb6-123">Conteúdo protegido</span><span class="sxs-lookup"><span data-stu-id="dcdb6-123">Protected Content</span></span>

<span data-ttu-id="dcdb6-124">Para reproduzir conteúdo protegido, você deve criar a sessão de mídia dentro do caminho de mídia protegido (PMP), chamando [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span><span class="sxs-lookup"><span data-stu-id="dcdb6-124">To play protected content, you must create the Media Session inside the protected media path (PMP), by calling [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span></span> <span data-ttu-id="dcdb6-125">Essa função cria uma instância da sessão de mídia dentro da PMP e retorna um ponteiro para um objeto proxy que realiza o marshaling das interfaces entre o limite do processo.</span><span class="sxs-lookup"><span data-stu-id="dcdb6-125">This function creates an instance of the Media Session inside the PMP and returns a pointer to a proxy object that marshals interfaces across the process boundary.</span></span>

<span data-ttu-id="dcdb6-126">Na maioria dos aspectos, o uso da sessão de mídia dentro do PMP é transparente para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dcdb6-126">In most respects, using the Media Session inside the PMP is transparent to the application.</span></span> <span data-ttu-id="dcdb6-127">No entanto, o aplicativo pode precisar invocar determinadas ações que permitem ao usuário reproduzir o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="dcdb6-127">However, the application might need to invoke certain actions that enable the user to play the content.</span></span> <span data-ttu-id="dcdb6-128">Por exemplo, o usuário pode precisar obter uma licença de DRM.</span><span class="sxs-lookup"><span data-stu-id="dcdb6-128">For example, the user might need to obtain a DRM license.</span></span> <span data-ttu-id="dcdb6-129">Media Foundation define um mecanismo genérico para essas ações usando a interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) .</span><span class="sxs-lookup"><span data-stu-id="dcdb6-129">Media Foundation defines a generic mechanism for these actions using the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface.</span></span>

<span data-ttu-id="dcdb6-130">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="dcdb6-130">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="dcdb6-131">Caminho de mídia protegido</span><span class="sxs-lookup"><span data-stu-id="dcdb6-131">Protected Media Path</span></span>](protected-media-path.md)
-   [<span data-ttu-id="dcdb6-132">Como reproduzir arquivos de mídia protegidos</span><span class="sxs-lookup"><span data-stu-id="dcdb6-132">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)

## <a name="presentation-clock"></a><span data-ttu-id="dcdb6-133">Relógio de apresentação</span><span class="sxs-lookup"><span data-stu-id="dcdb6-133">Presentation Clock</span></span>

<span data-ttu-id="dcdb6-134">A sessão de mídia gerencia todos os aspectos do relógio de apresentação:</span><span class="sxs-lookup"><span data-stu-id="dcdb6-134">The Media Session manages all aspects of the presentation clock:</span></span>

-   <span data-ttu-id="dcdb6-135">Criando o relógio de apresentação.</span><span class="sxs-lookup"><span data-stu-id="dcdb6-135">Creating the presentation clock.</span></span>

-   <span data-ttu-id="dcdb6-136">Selecionando a fonte de tempo.</span><span class="sxs-lookup"><span data-stu-id="dcdb6-136">Selecting the time source.</span></span>

-   <span data-ttu-id="dcdb6-137">Notificando os coletores de mídia sobre o relógio</span><span class="sxs-lookup"><span data-stu-id="dcdb6-137">Notifying the media sinks about the clock</span></span>

-   <span data-ttu-id="dcdb6-138">Iniciando, parando e pausando o relógio conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="dcdb6-138">Starting, stopping, and pausing the clock as necessary.</span></span>

-   <span data-ttu-id="dcdb6-139">Desligando o relógio.</span><span class="sxs-lookup"><span data-stu-id="dcdb6-139">Shutting down the clock.</span></span>

<span data-ttu-id="dcdb6-140">Para obter um ponteiro para o relógio de apresentação, chame [**IMFMediaSession:: getclock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) na sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="dcdb6-140">To get a pointer to the presentation clock, call [**IMFMediaSession::GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) on the Media Session.</span></span> <span data-ttu-id="dcdb6-141">O relógio de apresentação não retorna um tempo válido até que a sessão de mídia envie o evento [MESessionTopologyStatus](mesessiontopologystatus.md) com o \_ sinalizador MF TOPOSTATUS \_ Ready.</span><span class="sxs-lookup"><span data-stu-id="dcdb6-141">The presentation clock does not return a valid time until the Media Session sends the [MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_READY flag.</span></span> <span data-ttu-id="dcdb6-142">Até lá, **getclock** retorna MF \_ E \_ Clock \_ sem \_ fonte de tempo \_ .</span><span class="sxs-lookup"><span data-stu-id="dcdb6-142">Until then, **GetClock** returns MF\_E\_CLOCK\_NO\_TIME\_SOURCE.</span></span>

<span data-ttu-id="dcdb6-143">Um aplicativo que usa a sessão de mídia nunca deve iniciar, parar ou pausar o relógio de apresentação; alterar a taxa de clock; ou desligue o relógio.</span><span class="sxs-lookup"><span data-stu-id="dcdb6-143">An application that uses the Media Session should never start, stop, or pause the presentation clock; change the clock rate; or shut down the clock.</span></span>

<span data-ttu-id="dcdb6-144">Quando o aplicativo chama [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), a sessão de mídia inicia o relógio de apresentação com uma hora de início igual à posição inicial especificada no método **Start** .</span><span class="sxs-lookup"><span data-stu-id="dcdb6-144">When the application calls [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), the Media Session starts the presentation clock with a starting time equal to the starting position specified in the **Start** method.</span></span> <span data-ttu-id="dcdb6-145">Para obter mais informações sobre a sessão de mídia, consulte [sessão de mídia](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="dcdb6-145">For more information about the Media Session, see [Media Session](media-session.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dcdb6-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dcdb6-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcdb6-147">Sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="dcdb6-147">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 



