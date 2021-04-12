---
title: Orientação de texto e fonte internacional
description: Orientação de texto e fonte internacional
ms.assetid: 0540C9AD-8774-4F0F-B013-48C3EAE59BF2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2f9d94c53e4db45666d28a7c23a0e883043ba27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366032"
---
# <a name="international-text-and-font-guidance"></a><span data-ttu-id="a16f4-103">Orientação de texto e fonte internacional</span><span class="sxs-lookup"><span data-stu-id="a16f4-103">International text and font guidance</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="a16f4-104">Plataformas afetadas</span><span class="sxs-lookup"><span data-stu-id="a16f4-104">Affected Platforms</span></span>

<dl> <span data-ttu-id="a16f4-105">Clientes-Windows 8 \| Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a16f4-105">Clients - Windows 8 \| Windows 8.1</span></span>  
<span data-ttu-id="a16f4-106">Servidores-Windows Server 2012 \| Windows server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a16f4-106">Servers - Windows Server 2012 \| Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="a16f4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a16f4-107">Description</span></span>

<span data-ttu-id="a16f4-108">Desde antes do Windows 2000, o suporte à exibição de texto para novos scripts foi adicionado em cada versão principal do Windows.</span><span class="sxs-lookup"><span data-stu-id="a16f4-108">Since before Windows 2000, text-display support for new scripts has been added in each major release of Windows.</span></span> <span data-ttu-id="a16f4-109">Você pode encontrar descrições das alterações feitas em cada versão principal no artigo [suporte de script e fonte para o Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx) no centro de [desenvolvimento global go](https://msdn.microsoft.com/goglobal/default).</span><span class="sxs-lookup"><span data-stu-id="a16f4-109">You can find descriptions of the changes made in each major release in the [Script and Font Support for Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx) article at the [Go Global Development Center](https://msdn.microsoft.com/goglobal/default).</span></span>

<span data-ttu-id="a16f4-110">Observe que o suporte para um script pode exigir certas alterações em componentes de pilha de texto, bem como alterações em fontes.</span><span class="sxs-lookup"><span data-stu-id="a16f4-110">Note that support for a script may require certain changes to text stack components as well as changes to fonts.</span></span> <span data-ttu-id="a16f4-111">O sistema operacional Windows tem muitos componentes de pilha de texto: DirectWrite, GDI, Uniscribe, GDI+, WPF, RichEdit, ComCtl32 e outros.</span><span class="sxs-lookup"><span data-stu-id="a16f4-111">The Windows operating system has many text stack components: DirectWrite, GDI, Uniscribe, GDI+, WPF, RichEdit, ComCtl32, and others.</span></span> <span data-ttu-id="a16f4-112">As informações fornecidas pertencem principalmente a GDI e DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="a16f4-112">The information provided pertains primarily to GDI and DirectWrite.</span></span> <span data-ttu-id="a16f4-113">Ele também é geralmente aplicável a estruturas de interface do usuário, como RichEdit ou o agente de renderização MSHTML usado para aplicativos da Windows 8 Store e para renderização de conteúdo da Web, embora esses componentes possam apresentar determinadas diferenças.</span><span class="sxs-lookup"><span data-stu-id="a16f4-113">It is also generally applicable to UI frameworks such as RichEdit or the MSHTML rendering agent used for Windows 8 Store apps and for rendering web content, though those components may exhibit certain differences.</span></span>

## <a name="best-practices"></a><span data-ttu-id="a16f4-114">Práticas Recomendadas</span><span class="sxs-lookup"><span data-stu-id="a16f4-114">Best Practices</span></span>

<span data-ttu-id="a16f4-115">**Diretrizes de tipografia para desenvolvedores**</span><span class="sxs-lookup"><span data-stu-id="a16f4-115">**Typography guidance for developers**</span></span>

<span data-ttu-id="a16f4-116">A tipografia é o coração da linguagem de design da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a16f4-116">Typography is at the heart of the Microsoft design language.</span></span> <span data-ttu-id="a16f4-117">Cada um dos princípios de design da Microsoft reforça a importância da tipografia.</span><span class="sxs-lookup"><span data-stu-id="a16f4-117">Each of the Microsoft design principles reinforces the importance of typography.</span></span> <span data-ttu-id="a16f4-118">Pela primeira vez, os desenvolvedores de aplicativos têm um conjunto de estruturas que dão suporte a recursos tipográficos avançados.</span><span class="sxs-lookup"><span data-stu-id="a16f4-118">For the first time, app developers have a set of frameworks that support advanced typographic features.</span></span> <span data-ttu-id="a16f4-119">Vá para [exibindo e editando texto](/previous-versions/windows/apps/hh465442(v=win.10)) para obter informações sobre como usar JavaScript e HTML para exibir e editar texto em aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="a16f4-119">Go to [Displaying and editing text](/previous-versions/windows/apps/hh465442(v=win.10)) for information about how to use JavaScript and HTML to display and edit text in Windows Store apps.</span></span>

<span data-ttu-id="a16f4-120">**Métricas de fonte**</span><span class="sxs-lookup"><span data-stu-id="a16f4-120">**Font metrics**</span></span>

<span data-ttu-id="a16f4-121">As métricas de fonte são uma área de importância específica para os desenvolvedores de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="a16f4-121">Font metrics are an area of particular importance to application developers.</span></span> <span data-ttu-id="a16f4-122">Os arquivos de fonte contêm vários valores relacionados a métricas verticais e horizontais.</span><span class="sxs-lookup"><span data-stu-id="a16f4-122">Font files contain various values related to vertical and horizontal metrics.</span></span> <span data-ttu-id="a16f4-123">Esses valores são documentados na [especificação OpenType](https://www.microsoft.com/typography/otspec/) e são expostos por meio de uma variedade de APIs encontradas [na \_ \_ estrutura de métricas de fonte DWRITE](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) e na [estrutura TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica).</span><span class="sxs-lookup"><span data-stu-id="a16f4-123">These values are documented in the [OpenType specification](https://www.microsoft.com/typography/otspec/) and these are exposed via a variety of APIs found at [DWRITE\_FONT\_METRICS structure](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) and at [TEXTMETRIC Structure](/windows/win32/api/wingdi/ns-wingdi-textmetrica).</span></span>

## <a name="resources"></a><span data-ttu-id="a16f4-124">Recursos</span><span class="sxs-lookup"><span data-stu-id="a16f4-124">Resources</span></span>

-   [<span data-ttu-id="a16f4-125">Suporte a scripts e fontes para Windows</span><span class="sxs-lookup"><span data-stu-id="a16f4-125">Script and Font Support for Windows</span></span>](https://msdn.microsoft.com/goglobal/bb688099.aspx)
-   [<span data-ttu-id="a16f4-126">Ir para o centro de desenvolvimento global</span><span class="sxs-lookup"><span data-stu-id="a16f4-126">Go Global Development Center</span></span>](https://msdn.microsoft.com/goglobal/default)
-   <span data-ttu-id="a16f4-127">[Exibindo e editando texto](/previous-versions/windows/apps/hh465442(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="a16f4-127">[Displaying and editing text](/previous-versions/windows/apps/hh465442(v=win.10))</span></span>
-   [<span data-ttu-id="a16f4-128">Especificação de OpenType</span><span class="sxs-lookup"><span data-stu-id="a16f4-128">OpenType specification</span></span>](https://www.microsoft.com/typography/otspec/)
-   [<span data-ttu-id="a16f4-129">\_Estrutura de \_ métricas de fonte DWRITE</span><span class="sxs-lookup"><span data-stu-id="a16f4-129">DWRITE\_FONT\_METRICS structure</span></span>](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)
-   [<span data-ttu-id="a16f4-130">Estrutura TEXTMETRIC</span><span class="sxs-lookup"><span data-stu-id="a16f4-130">TEXTMETRIC Structure</span></span>](/windows/win32/api/wingdi/ns-wingdi-textmetrica)

 

 