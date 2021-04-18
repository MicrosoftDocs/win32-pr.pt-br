---
title: Internet do Windows
description: A API (interface de programação de aplicativo) do Microsoft Windows Internet (WinINet) permite que os aplicativos acessem protocolos padrão da Internet, como FTP e HTTP. Para facilitar o uso, o WinINet abstrai esses protocolos em uma interface de alto nível.
ms.assetid: 9d1856ac-f281-4582-bb70-83a8ec674914
keywords:
- Windows Internet WinINet
- WinINet WinINet, portal
- Windows Internet WinINet, página inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b5b76fefea900d3f187deb89929d3a09fe3c78
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454248"
---
# <a name="windows-internet"></a><span data-ttu-id="8316e-107">Internet do Windows</span><span class="sxs-lookup"><span data-stu-id="8316e-107">Windows Internet</span></span>

## <a name="purpose"></a><span data-ttu-id="8316e-108">Finalidade</span><span class="sxs-lookup"><span data-stu-id="8316e-108">Purpose</span></span>

<span data-ttu-id="8316e-109">A API (interface de programação de aplicativo) do Microsoft Windows Internet (WinINet) permite que os aplicativos acessem protocolos padrão da Internet, como FTP e HTTP.</span><span class="sxs-lookup"><span data-stu-id="8316e-109">The Microsoft Windows Internet (WinINet) application programming interface (API) enables applications to access standard Internet protocols, such as FTP and HTTP.</span></span> <span data-ttu-id="8316e-110">Para facilitar o uso, o WinINet abstrai esses protocolos em uma interface de alto nível.</span><span class="sxs-lookup"><span data-stu-id="8316e-110">For ease of use, WinINet abstracts these protocols into a high-level interface.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="8316e-111">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="8316e-111">Where applicable</span></span>

<span data-ttu-id="8316e-112">O WinINet não oferece suporte a implementações de servidor.</span><span class="sxs-lookup"><span data-stu-id="8316e-112">WinINet does not support server implementations.</span></span> <span data-ttu-id="8316e-113">Além disso, ele não deve ser usado de um serviço.</span><span class="sxs-lookup"><span data-stu-id="8316e-113">In addition, it should not be used from a service.</span></span> <span data-ttu-id="8316e-114">Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="8316e-114">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="8316e-115">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="8316e-115">Developer audience</span></span>

<span data-ttu-id="8316e-116">O WinINet foi projetado para ser usado por programadores C/C++.</span><span class="sxs-lookup"><span data-stu-id="8316e-116">WinINet is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="8316e-117">Ele requer uma compreensão básica dos protocolos FTP e HTTP.</span><span class="sxs-lookup"><span data-stu-id="8316e-117">It requires a basic understanding of the FTP and HTTP protocols.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="8316e-118">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="8316e-118">Run-time requirements</span></span>

<span data-ttu-id="8316e-119">Os aplicativos que usam a API do WinINet requerem o Windows NT 4,0 ou posterior ou o Windows me/98/95.</span><span class="sxs-lookup"><span data-stu-id="8316e-119">Applications that use the WinINet API require Windows NT 4.0 or later, or Windows Me/98/95.</span></span> <span data-ttu-id="8316e-120">Para obter mais informações sobre quais sistemas operacionais ou componentes são necessários para usar um elemento de programação específico, consulte a seção requisitos da documentação.</span><span class="sxs-lookup"><span data-stu-id="8316e-120">For more information about which operating systems or components are required to use a particular programming element, see the Requirements section of the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8316e-121">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="8316e-121">In this section</span></span>



| <span data-ttu-id="8316e-122">Tópico</span><span class="sxs-lookup"><span data-stu-id="8316e-122">Topic</span></span>                                                          | <span data-ttu-id="8316e-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="8316e-123">Description</span></span>                                                      |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="8316e-124">Sobre o Windows Internet</span><span class="sxs-lookup"><span data-stu-id="8316e-124">About Windows Internet</span></span>](about-wininet.md)<br/>         | <span data-ttu-id="8316e-125">Informações gerais sobre a API de Internet do Windows.</span><span class="sxs-lookup"><span data-stu-id="8316e-125">General information about the Windows Internet API.</span></span><br/>   |
| [<span data-ttu-id="8316e-126">Usando o Windows Internet</span><span class="sxs-lookup"><span data-stu-id="8316e-126">Using Windows Internet</span></span>](using-wininet.md)<br/>         | <span data-ttu-id="8316e-127">Guia de programação para a API de Internet do Windows.</span><span class="sxs-lookup"><span data-stu-id="8316e-127">Programming guide for the Windows Internet API.</span></span><br/>       |
| [<span data-ttu-id="8316e-128">Referência da Internet do Windows</span><span class="sxs-lookup"><span data-stu-id="8316e-128">Windows Internet Reference</span></span>](wininet-reference.md)<br/> | <span data-ttu-id="8316e-129">Documentação de referência para a API de Internet do Windows.</span><span class="sxs-lookup"><span data-stu-id="8316e-129">Reference documentation for the Windows Internet API.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="8316e-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8316e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8316e-131">Microsoft Windows HTTP Services (WinHTTP)</span><span class="sxs-lookup"><span data-stu-id="8316e-131">Microsoft Windows HTTP Services (WinHTTP)</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

