---
description: .
ms.assetid: f91c4604-b2d6-41e5-be66-bbc8a4f0e28e
title: Subconjunto do .NET 2,0 agora no Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e0f836ca7afaef920429df17ef8be845ce92e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172311"
---
# <a name="subset-of-net-20-now-on-server-core"></a><span data-ttu-id="d536c-103">Subconjunto do .NET 2,0 agora no Server Core</span><span class="sxs-lookup"><span data-stu-id="d536c-103">Subset of .NET 2.0 Now on Server Core</span></span>

## <a name="platform"></a><span data-ttu-id="d536c-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="d536c-104">Platform</span></span>

<span data-ttu-id="d536c-105">**Servidores** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d536c-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="d536c-106">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="d536c-106">Feature Impact</span></span>

 <span data-ttu-id="d536c-107">**Severidade** -baixa</span><span class="sxs-lookup"><span data-stu-id="d536c-107">**Severity** - Low</span></span>  
<span data-ttu-id="d536c-108">**Frequência** -baixa</span><span class="sxs-lookup"><span data-stu-id="d536c-108">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="d536c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d536c-109">Description</span></span>

<span data-ttu-id="d536c-110">A opção de instalação Server Core para o Windows Server 2008 R2 agora inclui um subconjunto do .NET Framework 2,0.</span><span class="sxs-lookup"><span data-stu-id="d536c-110">The Server Core installation option for Windows Server 2008 R2 now includes a subset of the .NET Framework 2.0.</span></span> <span data-ttu-id="d536c-111">O subconjunto é a funcionalidade no .NET 2,0 que se alinha com a funcionalidade no Server Core; nenhum binário foi adicionado à base do Server Core para permitir que qualquer parte do .NET 2,0 funcione.</span><span class="sxs-lookup"><span data-stu-id="d536c-111">The subset is the functionality in .NET 2.0 that aligns with the functionality in Server Core; no binaries were added to the Server Core base to allow any portion of .NET 2.0 to function.</span></span>

<span data-ttu-id="d536c-112">Não havia suporte ao .NET na opção de instalação do Server Core para o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="d536c-112">There was no .NET support in the Server Core installation option for Windows Server 2008.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="d536c-113">Manifestação do impacto</span><span class="sxs-lookup"><span data-stu-id="d536c-113">Manifestation of Impact</span></span>

<span data-ttu-id="d536c-114">Isso permite que alguns aplicativos baseados em .NET 2,0 sejam executados no Server Core no Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="d536c-114">This allows some .NET 2.0 based-applications to run on Server Core in Windows Server 2008 R2.</span></span>

## <a name="testing"></a><span data-ttu-id="d536c-115">Teste</span><span class="sxs-lookup"><span data-stu-id="d536c-115">Testing</span></span>

<span data-ttu-id="d536c-116">Verifique se as classes .NET usadas pelo seu código estão incluídas no Server Core.</span><span class="sxs-lookup"><span data-stu-id="d536c-116">Verify that the .NET classes your code uses is included in Server Core.</span></span> <span data-ttu-id="d536c-117">Teste também todos os aplicativos que executam esse código no Server Core.</span><span class="sxs-lookup"><span data-stu-id="d536c-117">Also test any applications that run this code on Server Core.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="d536c-118">Links para outros recursos</span><span class="sxs-lookup"><span data-stu-id="d536c-118">Links to Other Resources</span></span>

-   <span data-ttu-id="d536c-119">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d536c-119">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span></span>
-   [<span data-ttu-id="d536c-120">Blog do Server Core</span><span class="sxs-lookup"><span data-stu-id="d536c-120">Server Core Blog</span></span>](https://blogs.technet.com/server_core/archive/2008/11/25/net-2-0-and-server-core-in-windows-server-2008-r2.aspx)
-   <span data-ttu-id="d536c-121">*Consulte também* a seção Server Core do *SDK do Windows Server 2008 R2* quando ele se tornar disponível</span><span class="sxs-lookup"><span data-stu-id="d536c-121">*See also* the Server Core section of the *Windows Server 2008 R2 SDK* when it becomes available</span></span>

> [!Note]  
> <span data-ttu-id="d536c-122">Esses recursos podem não estar disponíveis em alguns idiomas e países/regiões.</span><span class="sxs-lookup"><span data-stu-id="d536c-122">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
