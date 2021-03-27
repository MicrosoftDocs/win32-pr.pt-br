---
description: O Windows GDI+ é uma API baseada em classe para programadores C/C++.
ms.assetid: ed1396b2-2fc5-4a77-bea2-7bcc971214ae
title: GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac0dac72d27ba52071797b51573141506d5b0ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090330"
---
# <a name="gdi"></a><span data-ttu-id="6cdb5-103">GDI+</span><span class="sxs-lookup"><span data-stu-id="6cdb5-103">GDI+</span></span>

## <a name="purpose"></a><span data-ttu-id="6cdb5-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="6cdb5-104">Purpose</span></span>

<span data-ttu-id="6cdb5-105">O Windows GDI+ é uma API baseada em classe para programadores C/C++.</span><span class="sxs-lookup"><span data-stu-id="6cdb5-105">Windows GDI+ is a class-based API for C/C++ programmers.</span></span> <span data-ttu-id="6cdb5-106">Ele permite que os aplicativos usem gráficos e texto formatado na tela de vídeo e na impressora.</span><span class="sxs-lookup"><span data-stu-id="6cdb5-106">It enables applications to use graphics and formatted text on both the video display and the printer.</span></span> <span data-ttu-id="6cdb5-107">Os aplicativos baseados na API do Microsoft Win32 não acessam o hardware de gráficos diretamente.</span><span class="sxs-lookup"><span data-stu-id="6cdb5-107">Applications based on the Microsoft Win32 API do not access graphics hardware directly.</span></span> <span data-ttu-id="6cdb5-108">Em vez disso, a GDI+ interage com drivers de dispositivo em nome dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6cdb5-108">Instead, GDI+ interacts with device drivers on behalf of applications.</span></span> <span data-ttu-id="6cdb5-109">O GDI+ também tem suporte do Microsoft Win64.</span><span class="sxs-lookup"><span data-stu-id="6cdb5-109">GDI+ is also supported by Microsoft Win64.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="6cdb5-110">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="6cdb5-110">Where applicable</span></span>

<span data-ttu-id="6cdb5-111">Não há suporte para funções e classes GDI+ para uso em um serviço do Windows.</span><span class="sxs-lookup"><span data-stu-id="6cdb5-111">GDI+ functions and classes are not supported for use within a Windows service.</span></span> <span data-ttu-id="6cdb5-112">A tentativa de usar essas funções e classes de um serviço do Windows pode gerar problemas inesperados, como desempenho de serviço reduzido e erros ou exceções de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="6cdb5-112">Attempting to use these functions and classes from a Windows service may produce unexpected problems, such as diminished service performance and run-time exceptions or errors.</span></span>

> [!Note]  
> <span data-ttu-id="6cdb5-113">Ao usar a API GDI+, você nunca deve permitir que seu aplicativo Baixe fontes arbitrárias de fontes não confiáveis.</span><span class="sxs-lookup"><span data-stu-id="6cdb5-113">When you use the GDI+ API, you must never allow your application to download arbitrary fonts from untrusted sources.</span></span> <span data-ttu-id="6cdb5-114">O sistema operacional requer privilégios elevados para garantir que todas as fontes instaladas sejam confiáveis.</span><span class="sxs-lookup"><span data-stu-id="6cdb5-114">The operating system requires elevated privileges to assure that all installed fonts are trusted.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="6cdb5-115">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="6cdb5-115">Developer audience</span></span>

<span data-ttu-id="6cdb5-116">A interface baseada em classe GDI+ C++ foi projetada para ser usada por programadores C/C++.</span><span class="sxs-lookup"><span data-stu-id="6cdb5-116">The GDI+ C++ class-based interface is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="6cdb5-117">É necessário ter familiaridade com a interface gráfica do usuário do Windows e com a arquitetura controlada por mensagem.</span><span class="sxs-lookup"><span data-stu-id="6cdb5-117">Familiarity with the Windows graphical user interface and message-driven architecture is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="6cdb5-118">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="6cdb5-118">Run-time requirements</span></span>

<span data-ttu-id="6cdb5-119">O GDI+ pode ser usado em todos os aplicativos baseados no Windows.</span><span class="sxs-lookup"><span data-stu-id="6cdb5-119">GDI+ can be used in all Windows-based applications.</span></span> <span data-ttu-id="6cdb5-120">O GDI+ foi introduzido no Windows XP e no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6cdb5-120">GDI+ was introduced in Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="6cdb5-121">Para obter informações sobre quais sistemas operacionais são necessários para usar uma classe ou um método específico, consulte a seção mais informações da documentação para a classe ou o método.</span><span class="sxs-lookup"><span data-stu-id="6cdb5-121">For information about which operating systems are required to use a particular class or method, see the More Information section of the documentation for the class or method.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6cdb5-122">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="6cdb5-122">In this section</span></span>

| <span data-ttu-id="6cdb5-123">Tópico</span><span class="sxs-lookup"><span data-stu-id="6cdb5-123">Topic</span></span>                                                    | <span data-ttu-id="6cdb5-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="6cdb5-124">Description</span></span>                                           |
|----------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="6cdb5-125">Visão geral</span><span class="sxs-lookup"><span data-stu-id="6cdb5-125">Overview</span></span>](-gdiplus-about-gdi--about.md)<br/>     | <span data-ttu-id="6cdb5-126">Informações gerais sobre GDI+.</span><span class="sxs-lookup"><span data-stu-id="6cdb5-126">General information about GDI+.</span></span><br/>            |
| [<span data-ttu-id="6cdb5-127">Usando</span><span class="sxs-lookup"><span data-stu-id="6cdb5-127">Using</span></span>](-gdiplus-using-gdi--use.md)<br/>          | <span data-ttu-id="6cdb5-128">Tarefas e exemplos usando o GDI+.</span><span class="sxs-lookup"><span data-stu-id="6cdb5-128">Tasks and examples using GDI+.</span></span><br/>             |
| [<span data-ttu-id="6cdb5-129">Referência</span><span class="sxs-lookup"><span data-stu-id="6cdb5-129">Reference</span></span>](-gdiplus-class-gdi-reference.md)<br/> | <span data-ttu-id="6cdb5-130">Documentação da API baseada em classe do GDI+ C++.</span><span class="sxs-lookup"><span data-stu-id="6cdb5-130">Documentation of GDI+ C++ class-based API.</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="6cdb5-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6cdb5-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cdb5-132">GDI do Windows</span><span class="sxs-lookup"><span data-stu-id="6cdb5-132">Windows GDI</span></span>](../gdi/windows-gdi.md)
</dt> <dt>

<span data-ttu-id="6cdb5-133">[DirectX](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="6cdb5-133">[DirectX](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="6cdb5-134">Aquisição de imagem do Windows</span><span class="sxs-lookup"><span data-stu-id="6cdb5-134">Windows Image Acquisition</span></span>](../wia/-wia-startpage.md)
</dt> <dt>

[<span data-ttu-id="6cdb5-135">OpenGL</span><span class="sxs-lookup"><span data-stu-id="6cdb5-135">OpenGL</span></span>](../opengl/opengl.md)
</dt> <dt>

[<span data-ttu-id="6cdb5-136">Multimídia do Windows</span><span class="sxs-lookup"><span data-stu-id="6cdb5-136">Windows Multimedia</span></span>](../multimedia/windows-multimedia-start-page.md)
</dt> </dl>
