---
title: Sistema de cores do Windows
description: Os esquemas de gerenciamento de cores são implementados nos sistemas operacionais Microsoft Windows para melhorar a renderização de conteúdo de cores em todas as formas de comunicação digital. O esquema de gerenciamento de cores que é usado começando com o Windows 2000, o Windows XP e o Windows Server 2003 é chamado de ICM (Image Color Management) 2,0. O esquema de gerenciamento de cores que é usado a partir do Windows Vista é chamado de WCS (sistema de cores do Windows) 1,0. O esquema de gerenciamento de cores WCS 1,0 é um superconjunto de APIs e funcionalidades do ICM 2,0.
ms.assetid: 9e8b7c38-3c4f-4537-a7e1-6ad0daa39497
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 558ccb84caa4ff10ab4c97115b9759730cd0ef26
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105791115"
---
# <a name="windows-color-system"></a><span data-ttu-id="616c2-105">Sistema de cores do Windows</span><span class="sxs-lookup"><span data-stu-id="616c2-105">Windows Color System</span></span>

## <a name="purpose"></a><span data-ttu-id="616c2-106">Finalidade</span><span class="sxs-lookup"><span data-stu-id="616c2-106">Purpose</span></span>

<span data-ttu-id="616c2-107">Os esquemas de gerenciamento de cores são implementados nos sistemas operacionais Microsoft Windows para melhorar a renderização de conteúdo de cores em todas as formas de comunicação digital.</span><span class="sxs-lookup"><span data-stu-id="616c2-107">Color management schemes are implemented in Microsoft Windows operating systems to improve the rendering of color content in all forms of digital communication.</span></span>

<span data-ttu-id="616c2-108">O esquema de gerenciamento de cores que é usado começando com o Windows 2000, o Windows XP e o Windows Server 2003 é chamado de ICM (Image Color Management) 2,0.</span><span class="sxs-lookup"><span data-stu-id="616c2-108">The color management scheme that's used starting with Windows 2000, Windows XP, and Windows Server 2003 is called Image Color Management (ICM) 2.0.</span></span> <span data-ttu-id="616c2-109">O esquema de gerenciamento de cores que é usado a partir do Windows Vista é chamado de WCS (sistema de cores do Windows) 1,0.</span><span class="sxs-lookup"><span data-stu-id="616c2-109">The color management scheme that's used starting with Windows Vista is called Windows Color System (WCS) 1.0.</span></span> <span data-ttu-id="616c2-110">O esquema de gerenciamento de cores WCS 1,0 é um superconjunto de APIs e funcionalidades do ICM 2,0.</span><span class="sxs-lookup"><span data-stu-id="616c2-110">The WCS 1.0 color management scheme is a superset of ICM 2.0 APIs and functionality.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="616c2-111">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="616c2-111">Where applicable</span></span>

<span data-ttu-id="616c2-112">O ICM pode ser usado em todos os aplicativos no Windows 2000 e em sistemas operacionais posteriores.</span><span class="sxs-lookup"><span data-stu-id="616c2-112">ICM can be used in all applications on Windows 2000 and later operating systems.</span></span> <span data-ttu-id="616c2-113">O WCS pode ser usado em todos os aplicativos no Windows Vista e em sistemas operacionais posteriores.</span><span class="sxs-lookup"><span data-stu-id="616c2-113">WCS can be used in all applications on Windows Vista and later operating systems.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="616c2-114">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="616c2-114">Developer audience</span></span>

<span data-ttu-id="616c2-115">A API WCS foi projetada para uso por programadores C/C++.</span><span class="sxs-lookup"><span data-stu-id="616c2-115">The WCS API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="616c2-116">É necessário estar familiarizado com a interface gráfica do usuário do Windows, a arquitetura orientada por mensagem e um conhecimento prático dos conceitos de gerenciamento de cores.</span><span class="sxs-lookup"><span data-stu-id="616c2-116">Familiarity with the Windows graphical user interface, message-driven architecture, and a working knowledge of color management concepts are required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="616c2-117">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="616c2-117">Run-time requirements</span></span>

<span data-ttu-id="616c2-118">Os aplicativos que usam a API ICM exigem o Windows 2000 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="616c2-118">Applications that use the ICM API require Windows 2000 or later.</span></span> <span data-ttu-id="616c2-119">Os aplicativos que usam a API WCS exigem o Windows Vista ou posterior.</span><span class="sxs-lookup"><span data-stu-id="616c2-119">Applications that use the WCS API require Windows Vista or later.</span></span> <span data-ttu-id="616c2-120">Para obter informações específicas de tempo de execução em uma função, consulte a seção requisitos da página de referência para essa função.</span><span class="sxs-lookup"><span data-stu-id="616c2-120">For specific run-time information on a function, see the Requirements section of the reference page for that function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="616c2-121">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="616c2-121">In this section</span></span>

-   [<span data-ttu-id="616c2-122">Considerações de segurança: sistema de cores do Windows</span><span class="sxs-lookup"><span data-stu-id="616c2-122">Security Considerations: Windows Color System</span></span>](security-considerations--windows-color-system.md)
-   [<span data-ttu-id="616c2-123">Conceitos básicos de gerenciamento de cores</span><span class="sxs-lookup"><span data-stu-id="616c2-123">Basic color management concepts</span></span>](basic-color-management-concepts.md)
-   [<span data-ttu-id="616c2-124">Algoritmos e esquemas do sistema de cores do Windows</span><span class="sxs-lookup"><span data-stu-id="616c2-124">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
-   [<span data-ttu-id="616c2-125">Sobre o sistema de cores do Windows versão 1.0</span><span class="sxs-lookup"><span data-stu-id="616c2-125">About Windows Color System Version 1.0</span></span>](about-windows-color-system-version-1-0.md)
-   [<span data-ttu-id="616c2-126">Uso do WCS 1.0</span><span class="sxs-lookup"><span data-stu-id="616c2-126">Using WCS 1.0</span></span>](using-wcs-1-0.md)
-   [<span data-ttu-id="616c2-127">Referência</span><span class="sxs-lookup"><span data-stu-id="616c2-127">Reference</span></span>](reference.md)
-   [<span data-ttu-id="616c2-128">Glossário do WCS 1.0</span><span class="sxs-lookup"><span data-stu-id="616c2-128">WCS 1.0 Glossary</span></span>](wcs-1-0-glossary.md)

## <a name="related-topics"></a><span data-ttu-id="616c2-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="616c2-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="616c2-130">OpenGL</span><span class="sxs-lookup"><span data-stu-id="616c2-130">OpenGL</span></span>](../opengl/introduction-to-opengl.md)
</dt> <dt>

[<span data-ttu-id="616c2-131">Multimídia do Windows</span><span class="sxs-lookup"><span data-stu-id="616c2-131">Windows Multimedia</span></span>](../multimedia/windows-multimedia-start-page.md)
</dt> <dt>

[<span data-ttu-id="616c2-132">GDI do Windows</span><span class="sxs-lookup"><span data-stu-id="616c2-132">Windows GDI</span></span>](../gdi/windows-gdi.md)
</dt> </dl>

 

 