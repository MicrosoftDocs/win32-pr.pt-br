---
description: Ocasionalmente, você pode precisar determinar se seu aplicativo está sendo executado em um Tablet PC porque talvez você queira que seus aplicativos aproveitem os recursos inerentes de tinta, reconhecimento e caneta.
ms.assetid: 86a3eddb-6541-4b73-b2ca-6adedad1a1e5
title: Determinando se um PC é um Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c793d5531d6091d4bce73d99bfa32d100c2b9304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793843"
---
# <a name="determining-whether-a-pc-is-a-tablet-pc"></a><span data-ttu-id="e0479-103">Determinando se um PC é um Tablet PC</span><span class="sxs-lookup"><span data-stu-id="e0479-103">Determining Whether a PC is a Tablet PC</span></span>

<span data-ttu-id="e0479-104">Ocasionalmente, você pode precisar determinar se seu aplicativo está sendo executado em um Tablet PC porque talvez você queira que seus aplicativos aproveitem os recursos inerentes de tinta, reconhecimento e caneta.</span><span class="sxs-lookup"><span data-stu-id="e0479-104">You may occasionally need to determine whether your application is running on a Tablet PC because you may want your applications to take advantage of inherent ink, recognition, and pen capabilities.</span></span> <span data-ttu-id="e0479-105">Para ajudá-lo a determinar se seu aplicativo tem acesso aos recursos do Tablet PC, você pode usar a chamada à API do Windows GetSystemMetrics () conforme descrito neste tópico.</span><span class="sxs-lookup"><span data-stu-id="e0479-105">To help you determine whether your application has access to the Tablet PC features, you can use the GetSystemMetrics() Windows API call as described in this topic.</span></span>

## <a name="client-side-applications"></a><span data-ttu-id="e0479-106">Client-Side aplicativos</span><span class="sxs-lookup"><span data-stu-id="e0479-106">Client-Side Applications</span></span>

<span data-ttu-id="e0479-107">Você pode usar as seguintes técnicas para determinar se o seu código está sendo executado em um Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="e0479-107">You can use the following techniques to determine whether your code is running on a Tablet PC.</span></span>

-   [<span data-ttu-id="e0479-108">Usando GetSystemMetrics (SM \_ Tablet)</span><span class="sxs-lookup"><span data-stu-id="e0479-108">Using GetSystemMetrics (SM\_TABLETPC)</span></span>](/windows)
-   [<span data-ttu-id="e0479-109">Usando a presença de binários da plataforma Tablet</span><span class="sxs-lookup"><span data-stu-id="e0479-109">Using the Presence of Tablet Platform Binaries</span></span>](#using-the-presence-of-tablet-platform-binaries)
-   [<span data-ttu-id="e0479-110">Aplicativos baseados na Web</span><span class="sxs-lookup"><span data-stu-id="e0479-110">Web-Based Applications</span></span>](#web-based-applications)

### <a name="using-getsystemmetrics-sm_tabletpc"></a><span data-ttu-id="e0479-111">Usando GetSystemMetrics (SM \_ Tablet)</span><span class="sxs-lookup"><span data-stu-id="e0479-111">Using GetSystemMetrics (SM\_TABLETPC)</span></span>

### <a name="windows-xp-tablet-pc-edition"></a><span data-ttu-id="e0479-112">Windows XP Tablet PC Edition</span><span class="sxs-lookup"><span data-stu-id="e0479-112">Windows XP Tablet PC Edition</span></span>

<span data-ttu-id="e0479-113">No Microsoft Windows XP Tablet PC Edition, use a função GetSystemMetrics (SM \_ Tablet) para determinar se um computador é um Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="e0479-113">In Microsoft Windows XP Tablet PC Edition, use the GetSystemMetrics(SM\_TABLETPC) function to determine whether a computer is a Tablet PC.</span></span> <span data-ttu-id="e0479-114">GetSystemMetrics (SM Tablet \_ ) foi projetado para retornar true em um computador que executa o Windows XP Notebook PC Edition.</span><span class="sxs-lookup"><span data-stu-id="e0479-114">GetSystemMetrics(SM\_TABLETPC) is designed to return TRUE on a computer running Windows XP Tablet PC Edition.</span></span>

### <a name="windows-vista"></a><span data-ttu-id="e0479-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0479-115">Windows Vista</span></span>

<span data-ttu-id="e0479-116">No Windows Vista, não há mais um SDK do Tablet PC distinto.</span><span class="sxs-lookup"><span data-stu-id="e0479-116">In Windows Vista, there is no longer a distinct Tablet PC SDK.</span></span> <span data-ttu-id="e0479-117">O SDK do Windows agora contém uma seção chamada "Tablet PC e Touch Technology" e a lógica do GetSystemMetrics (SM Tablet \_ ) foi alterada para refletir isso.</span><span class="sxs-lookup"><span data-stu-id="e0479-117">The Windows SDK now contains a section called "Tablet PC and Touch Technology" and the logic of GetSystemMetrics(SM\_TABLETPC) has been changed to reflect this.</span></span> <span data-ttu-id="e0479-118">GetSystemMetrics (SM \_ Tablet) agora retornará true se todas as seguintes opções forem verdadeiras:</span><span class="sxs-lookup"><span data-stu-id="e0479-118">GetSystemMetrics(SM\_TABLETPC) now returns true if all of the following are true:</span></span>

-   <span data-ttu-id="e0479-119">Há um digitalizador integrado, uma caneta ou um toque, no sistema.</span><span class="sxs-lookup"><span data-stu-id="e0479-119">There is an integrated digitizer, either pen or touch, on the system.</span></span>
-   <span data-ttu-id="e0479-120">O componente opcional do Tablet PC está instalado.</span><span class="sxs-lookup"><span data-stu-id="e0479-120">The Tablet PC optional component is installed.</span></span> <span data-ttu-id="e0479-121">Este componente contém recursos como painel de entrada do Tablet PC e diário do Windows.</span><span class="sxs-lookup"><span data-stu-id="e0479-121">This component contains features such as Tablet PC Input Panel and Windows Journal.</span></span>
-   <span data-ttu-id="e0479-122">O computador está licenciado para usar o componente opcional.</span><span class="sxs-lookup"><span data-stu-id="e0479-122">The computer is licensed to use the optional component.</span></span> <span data-ttu-id="e0479-123">As versões Premium do Windows Vista, como o Windows Vista Home Premium, o Windows Vista Small Business, o Windows Vista Professional, o Windows Vista Enterprise e o Windows Vista Ultimate, são licenciadas para usar o componente opcional.</span><span class="sxs-lookup"><span data-stu-id="e0479-123">Premium versions of Windows Vista—such as Windows Vista Home Premium, Windows Vista Small Business, Windows Vista Professional, Windows Vista Enterprise, and Windows Vista Ultimate—are licensed to use the optional component.</span></span>
-   <span data-ttu-id="e0479-124">O serviço de entrada do Tablet PC está em execução.</span><span class="sxs-lookup"><span data-stu-id="e0479-124">Tablet PC Input Service is running.</span></span> <span data-ttu-id="e0479-125">O serviço de entrada do Tablet PC é um novo serviço do Windows Vista que controla a entrada do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="e0479-125">Tablet PC Input Service is a new service for Windows Vista that controls Tablet PC input.</span></span>

<span data-ttu-id="e0479-126">Com essa maior precisão, GetSystemMetrics (SM \_ Tablet) continua sendo a maneira recomendada de determinar se um computador que executa o Windows Vista é um Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="e0479-126">With this increased accuracy, GetSystemMetrics(SM\_TABLETPC) continues to be the recommended way to determine whether a computer running Windows Vista is a Tablet PC.</span></span>

### <a name="using-the-presence-of-tablet-platform-binaries"></a><span data-ttu-id="e0479-127">Usando a presença de binários da plataforma Tablet</span><span class="sxs-lookup"><span data-stu-id="e0479-127">Using the Presence of Tablet Platform Binaries</span></span>

<span data-ttu-id="e0479-128">No Windows XP Tablet PC Edition e no Windows Vista, você pode procurar a presença dos binários de tinta, como inkobj.dll e Microsoft.Ink.dll, e usar sua funcionalidade com suporte, se estiverem presentes.</span><span class="sxs-lookup"><span data-stu-id="e0479-128">In both Windows XP Tablet PC Edition and Windows Vista, you can search for the presence of the ink binaries—such as inkobj.dll and Microsoft.Ink.dll—and use their supported functionality if they are present.</span></span>

<span data-ttu-id="e0479-129">No Windows Vista, os binários da plataforma Tablet PC são instalados em todas as versões de cliente por padrão.</span><span class="sxs-lookup"><span data-stu-id="e0479-129">In Windows Vista, the Tablet PC Platform binaries are installed on all client versions by default.</span></span> <span data-ttu-id="e0479-130">A funcionalidade de entrada e de tinta está disponível nessas versões.</span><span class="sxs-lookup"><span data-stu-id="e0479-130">Input and inking functionality are available on those versions.</span></span> <span data-ttu-id="e0479-131">O reconhecimento está disponível apenas nas versões Premium do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e0479-131">Recognition is available only in premium versions of Windows Vista.</span></span>

### <a name="web-based-applications"></a><span data-ttu-id="e0479-132">Web-Based aplicativos</span><span class="sxs-lookup"><span data-stu-id="e0479-132">Web-Based Applications</span></span>

<span data-ttu-id="e0479-133">No Windows Vista, a cadeia de caracteres do agente do usuário relatada pelo Internet Explorer inclui "Tablet PC 2,0" se, de acordo com GetSystemMetrics (SM Tablet \_ ), o dispositivo for um Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="e0479-133">In Windows Vista, the user-agent string reported by Internet Explorer includes "Tablet PC 2.0" if, according to GetSystemMetrics(SM\_TABLETPC), the device is a Tablet PC.</span></span>

<span data-ttu-id="e0479-134">No Windows XP Tablet PC Edition 2005, a cadeia de caracteres do agente do usuário inclui o Tablet PC 1,7.</span><span class="sxs-lookup"><span data-stu-id="e0479-134">In Windows XP Tablet PC Edition 2005, the user-agent string includes Tablet PC 1.7.</span></span> <span data-ttu-id="e0479-135">A cadeia de caracteres do agente do usuário é semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="e0479-135">The user-agent string looks something like the following:</span></span>

`Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1; .NET CLR 1.0.3705; Tablet PC 2.0)`

<span data-ttu-id="e0479-136">Use esse valor para determinar se o computador cliente é um Tablet PC e dá suporte a controles de tinta baseados na Web.</span><span class="sxs-lookup"><span data-stu-id="e0479-136">Use this value to determine whether the client computer is a Tablet PC and supports Web-based inking controls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0479-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e0479-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0479-138">**GetSystemMetrics**</span><span class="sxs-lookup"><span data-stu-id="e0479-138">**GetSystemMetrics**</span></span>](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> </dl>

 

 
