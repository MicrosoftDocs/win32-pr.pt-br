---
title: Direct2D não dá suporte à renderização para metaarquivos avançados no Internet Explorer 9
description: Direct2D não dá suporte à renderização para metaarquivos avançados no Internet Explorer 9
ms.assetid: D106FBD6-F05E-41A6-B8F8-569EB9810E2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed5ab00b12a85f62a7ff65bbc6034227ac7a5129
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "105772641"
---
# <a name="direct2d-does-not-support-rendering-to-rich-metafiles-in-internet-explorer-9"></a><span data-ttu-id="91f2e-103">Direct2D não dá suporte à renderização para metaarquivos avançados no Internet Explorer 9</span><span class="sxs-lookup"><span data-stu-id="91f2e-103">Direct2D does not support rendering to rich metafiles in Internet Explorer 9</span></span>

## <a name="platforms"></a><span data-ttu-id="91f2e-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="91f2e-104">Platforms</span></span>

<span data-ttu-id="91f2e-105">**Clientes** – Windows Vista Windows \| 7 Windows \| 8</span><span class="sxs-lookup"><span data-stu-id="91f2e-105">**Clients** – Windows Vista \| Windows 7 \| Windows 8</span></span>  
<span data-ttu-id="91f2e-106">**Servidores** – windows Server 2008 \| Windows Server 2008 R2 \| Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="91f2e-106">**Servers** – Windows Server 2008 \| Windows Server 2008 R2 \| Windows Server 2012</span></span>  




## <a name="description"></a><span data-ttu-id="91f2e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="91f2e-107">Description</span></span>

<span data-ttu-id="91f2e-108">Devido a alterações de renderização internas no Internet Explorer 9, as APIs [IHTMLElementRender::D rawtodc](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85)) e [IViewObject::D RAW](/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw) agora criarão um metarquivo contendo um único bitmap que representa o conteúdo da Web em vez de um metarquivo avançado contendo informações de texto e vetor.</span><span class="sxs-lookup"><span data-stu-id="91f2e-108">Due to internal rendering changes in Internet Explorer 9, the [IHTMLElementRender::DrawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85)) and [IViewObject::Draw](/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw) APIs will now create a metafile containing a single bitmap that represents the web content instead of a rich metafile containing text and vector info.</span></span> <span data-ttu-id="91f2e-109">Essa alteração ocorreu devido à mudança do processamento de GDI para a renderização de Direct2D (D2D) acelerada por hardware.</span><span class="sxs-lookup"><span data-stu-id="91f2e-109">This change was due to the move from GDI rendering to hardware-accelerated Direct2D (D2D) rendering.</span></span>

<span data-ttu-id="91f2e-110">Essa alteração afeta os aplicativos que usam essas APIs e dependem do texto ou das informações de vetor no metarquivo.</span><span class="sxs-lookup"><span data-stu-id="91f2e-110">This change affects apps that use these APIs and rely on text or vector info in the metafile.</span></span>

## <a name="manifestation"></a><span data-ttu-id="91f2e-111">Manifestação</span><span class="sxs-lookup"><span data-stu-id="91f2e-111">Manifestation</span></span>

<span data-ttu-id="91f2e-112">Dependendo do aplicativo que é afetado por essa alteração, os usuários poderão ver o comportamento corrompido ou incorreto em seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="91f2e-112">Depending on the app that is affected by this change, users might see broken or incorrect behavior in their apps.</span></span>

## <a name="mitigation"></a><span data-ttu-id="91f2e-113">Atenuação</span><span class="sxs-lookup"><span data-stu-id="91f2e-113">Mitigation</span></span>

<span data-ttu-id="91f2e-114">Os aplicativos que só precisam extrair informações de texto de um documento da Web (sem informações de posicionamento) podem usar a propriedade [InnerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85)) para extrair o texto.</span><span class="sxs-lookup"><span data-stu-id="91f2e-114">Apps that only need to extract text info from a web document (without positioning info) can use the [innerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85)) property to extract text.</span></span>

<span data-ttu-id="91f2e-115">Os aplicativos que usam IViewObject::D RAW podem usar o [recurso \_ IVIEWOBJECTDRAW \_ DMLT9 \_ com \_ ](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85)) a chave de controle de recurso GDI para reverter para a renderização GDI se o modo de documento:</span><span class="sxs-lookup"><span data-stu-id="91f2e-115">Apps that use IViewObject::Draw can use the [FEATURE\_IVIEWOBJECTDRAW\_DMLT9\_WITH\_GDI](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85)) feature control key to revert to GDI rendering if the document mode:</span></span>

-   <span data-ttu-id="91f2e-116">É menor ou igual a 8</span><span class="sxs-lookup"><span data-stu-id="91f2e-116">Is less or equal to 8</span></span>
-   <span data-ttu-id="91f2e-117">O FCK autoriza esse host a usar o GDI</span><span class="sxs-lookup"><span data-stu-id="91f2e-117">The FCK authorizes that host to use GDI</span></span>
-   <span data-ttu-id="91f2e-118">E um DC de metarquivo é passado para a API</span><span class="sxs-lookup"><span data-stu-id="91f2e-118">And a metafile DC is passed to the API</span></span>

## <a name="resources"></a><span data-ttu-id="91f2e-119">Recursos</span><span class="sxs-lookup"><span data-stu-id="91f2e-119">Resources</span></span>

-   <span data-ttu-id="91f2e-120">[IHTMLElementRender::D rawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="91f2e-120">[IHTMLElementRender::DrawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85))</span></span>
-   [<span data-ttu-id="91f2e-121">IViewObject::D bruto</span><span class="sxs-lookup"><span data-stu-id="91f2e-121">IViewObject::Draw</span></span>](/windows/win32/api/oleidl/nf-oleidl-iviewobject-draw)
-   <span data-ttu-id="91f2e-122">[Propriedade IHTMLElement:: innerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="91f2e-122">[IHTMLElement::innerText Property](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85))</span></span>
-   <span data-ttu-id="91f2e-123">[Controles de recursos da Internet (I... Debug](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="91f2e-123">[Internet Feature Controls (I..L)](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85))</span></span>

 

 