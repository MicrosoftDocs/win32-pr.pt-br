---
description: Estende os aplicativos escritos usando tecnologias baseadas em COM.
ms.assetid: b21a6b08-c17c-4fcc-bc60-39037bc9902f
title: COM+ (serviços de componentes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b778c31957ddfe3f71db23b2f5be2a3ee681fde0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920337"
---
# <a name="com-component-services"></a><span data-ttu-id="7b60f-103">COM+ (serviços de componentes)</span><span class="sxs-lookup"><span data-stu-id="7b60f-103">COM+ (Component Services)</span></span>

## <a name="purpose"></a><span data-ttu-id="7b60f-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="7b60f-104">Purpose</span></span>

<span data-ttu-id="7b60f-105">O COM+ é uma evolução do Microsoft Component Object Model (COM) e do Microsoft Transaction Server (MTS).</span><span class="sxs-lookup"><span data-stu-id="7b60f-105">COM+ is an evolution of Microsoft Component Object Model (COM) and Microsoft Transaction Server (MTS).</span></span> <span data-ttu-id="7b60f-106">O COM+ baseia-se em e estende os aplicativos escritos usando COM, MTS e outras tecnologias baseadas em COM.</span><span class="sxs-lookup"><span data-stu-id="7b60f-106">COM+ builds on and extends applications written using COM, MTS, and other COM-based technologies.</span></span> <span data-ttu-id="7b60f-107">O COM+ lida com muitas das tarefas de gerenciamento de recursos que você tinha que programar por conta própria, como a alocação e a segurança de threads.</span><span class="sxs-lookup"><span data-stu-id="7b60f-107">COM+ handles many of the resource management tasks that you previously had to program yourself, such as thread allocation and security.</span></span> <span data-ttu-id="7b60f-108">O COM+ também torna seus aplicativos mais escalonáveis fornecendo pooling de threads, pooling de objetos e ativação de objeto just-in-time.</span><span class="sxs-lookup"><span data-stu-id="7b60f-108">COM+ also makes your applications more scalable by providing thread pooling, object pooling, and just-in-time object activation.</span></span> <span data-ttu-id="7b60f-109">O COM+ também ajuda a proteger a integridade dos seus dados, fornecendo suporte a transações, mesmo se uma transação abranger vários bancos de dados em uma rede.</span><span class="sxs-lookup"><span data-stu-id="7b60f-109">COM+ also helps protect the integrity of your data by providing transaction support, even if a transaction spans multiple databases over a network.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="7b60f-110">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="7b60f-110">Where applicable</span></span>

<span data-ttu-id="7b60f-111">O COM+ pode ser usado para desenvolver aplicativos corporativos e de missão crítica e de toda a empresa para Windows.</span><span class="sxs-lookup"><span data-stu-id="7b60f-111">COM+ can be used to develop enterprise-wide, mission-critical, distributed applications for Windows.</span></span>

<span data-ttu-id="7b60f-112">Se você for um administrador de sistema, estará instalando, implantando e Configurando aplicativos COM+ e seus componentes.</span><span class="sxs-lookup"><span data-stu-id="7b60f-112">If you are a system administrator, you will be installing, deploying, and configuring COM+ applications and their components.</span></span> <span data-ttu-id="7b60f-113">Se você for um programador de aplicativos, estará escrevendo componentes e integrando-os como aplicativos.</span><span class="sxs-lookup"><span data-stu-id="7b60f-113">If you are an application programmer, you will be writing components and integrating them as applications.</span></span> <span data-ttu-id="7b60f-114">Se você for um fornecedor de ferramentas, estará desenvolvendo ou modificando ferramentas para trabalhar no ambiente COM+.</span><span class="sxs-lookup"><span data-stu-id="7b60f-114">If you are a tools vendor, you will be developing or modifying tools to work in the COM+ environment.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="7b60f-115">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="7b60f-115">Developer audience</span></span>

<span data-ttu-id="7b60f-116">O COM+ foi projetado principalmente para desenvolvedores de Microsoft Visual C++ e do Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7b60f-116">COM+ is designed primarily for Microsoft Visual C++ and Microsoft Visual Basic developers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="7b60f-117">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="7b60f-117">Run-time requirements</span></span>

<span data-ttu-id="7b60f-118">A versão 1,5 do COM+ está incluída no Windows a partir do Windows XP e do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7b60f-118">COM+ version 1.5 is included in Windows starting with Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="7b60f-119">A versão 1,0 do COM+ está incluída no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="7b60f-119">COM+ version 1.0 is included in Windows 2000.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7b60f-120">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="7b60f-120">In this section</span></span>

-   [<span data-ttu-id="7b60f-121">O que há de novo no COM+ 1,5</span><span class="sxs-lookup"><span data-stu-id="7b60f-121">What's New in COM+ 1.5</span></span>](what-s-new-in-com--1-5.md)
-   [<span data-ttu-id="7b60f-122">Visão geral dos desenvolvedores de COM+</span><span class="sxs-lookup"><span data-stu-id="7b60f-122">COM+ Developers Overview</span></span>](com--developers-overview.md)
-   [<span data-ttu-id="7b60f-123">Serviços COM+</span><span class="sxs-lookup"><span data-stu-id="7b60f-123">COM+ Services</span></span>](com--services.md)
-   [<span data-ttu-id="7b60f-124">Tarefas gerais do COM+</span><span class="sxs-lookup"><span data-stu-id="7b60f-124">COM+ General Tasks</span></span>](com--general-tasks.md)
-   [<span data-ttu-id="7b60f-125">Referência do COM+</span><span class="sxs-lookup"><span data-stu-id="7b60f-125">COM+ Reference</span></span>](com--reference.md)

## <a name="related-topics"></a><span data-ttu-id="7b60f-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7b60f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b60f-127">COM</span><span class="sxs-lookup"><span data-stu-id="7b60f-127">COM</span></span>](/windows/desktop/com/component-object-model--com--portal)
</dt> </dl>

 

 
