---
description: O WoW64 agora é um recurso opcional para o Server Core
ms.assetid: 9a918cd3-60a0-4231-975a-bee12de5c812
title: Status do WoW64 no Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fad947dac85707d3c9c89a2cffea38c4a4850a6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084044"
---
# <a name="wow64-is-now-an-optional-feature-for-server-core"></a><span data-ttu-id="5d0d8-103">O WoW64 agora é um recurso opcional para o Server Core</span><span class="sxs-lookup"><span data-stu-id="5d0d8-103">WoW64 Is Now an Optional Feature for Server Core</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="5d0d8-104">Plataformas afetadas</span><span class="sxs-lookup"><span data-stu-id="5d0d8-104">Affected Platforms</span></span>

<span data-ttu-id="5d0d8-105">**Servidores** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5d0d8-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="5d0d8-106">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="5d0d8-106">Feature Impact</span></span>

 <span data-ttu-id="5d0d8-107">**Severidade** -baixa</span><span class="sxs-lookup"><span data-stu-id="5d0d8-107">**Severity** - Low</span></span>  
<span data-ttu-id="5d0d8-108">**Frequência** -baixa</span><span class="sxs-lookup"><span data-stu-id="5d0d8-108">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="5d0d8-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d0d8-109">Description</span></span>

<span data-ttu-id="5d0d8-110">A opção de instalação Server Core para o Windows Server 2008 R2 permite que você desinstale o WoW64.</span><span class="sxs-lookup"><span data-stu-id="5d0d8-110">The Server Core installation option for Windows Server 2008 R2 allows you to uninstall WoW64.</span></span> <span data-ttu-id="5d0d8-111">O WoW64 agora é um recurso opcional que você pode desinstalar se não for necessário executar o código de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="5d0d8-111">WoW64 is now an optional feature that you can uninstall if it is not necessary to run 32-bit code.</span></span>

<span data-ttu-id="5d0d8-112">Além disso, as funções Active Directory e serviços AD LDS exigem o WoW64 para serem executadas no Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="5d0d8-112">In addition, the Active Directory and Active Directory Lightweight Directory Services roles require WoW64 in order to run in Windows Server 2008 R2.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="5d0d8-113">Manifestação do impacto</span><span class="sxs-lookup"><span data-stu-id="5d0d8-113">Manifestation of Impact</span></span>

<span data-ttu-id="5d0d8-114">Se você desinstalar o WoW64, os administradores que executam o código de 32 bits no Server Core receberão uma mensagem de erro informando que o aplicativo não pode ser executado.</span><span class="sxs-lookup"><span data-stu-id="5d0d8-114">If you uninstall WoW64, Administrators running 32-bit code on Server Core will receive an error message that the application cannot be executed.</span></span> <span data-ttu-id="5d0d8-115">Se os administradores tentarem executar Active Directory e serviços AD LDS, eles receberão uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="5d0d8-115">If Administrators attempt to run Active Directory and Active Directory Lightweight Directory Services, they will receive an error message.</span></span>

## <a name="mitigation"></a><span data-ttu-id="5d0d8-116">Atenuação</span><span class="sxs-lookup"><span data-stu-id="5d0d8-116">Mitigation</span></span>

<span data-ttu-id="5d0d8-117">Instale o WoW64.</span><span class="sxs-lookup"><span data-stu-id="5d0d8-117">Install WoW64.</span></span>

## <a name="solution"></a><span data-ttu-id="5d0d8-118">Solução</span><span class="sxs-lookup"><span data-stu-id="5d0d8-118">Solution</span></span>

<span data-ttu-id="5d0d8-119">A solução preferida é fornecer uma versão de 64 bits do código para permitir que ele seja executado no Server Core sem precisar do WoW64.</span><span class="sxs-lookup"><span data-stu-id="5d0d8-119">The preferred solution is to provide a 64-bit version of the code to enable it to run on Server Core without needing WoW64.</span></span>

<span data-ttu-id="5d0d8-120">No mínimo, forneça a documentação do usuário indicando que, para executar o código de 32 bits, eles devem instalar o WoW64.</span><span class="sxs-lookup"><span data-stu-id="5d0d8-120">At a minimum, provide user documentation noting that to run 32-bit code they must install WoW64.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="5d0d8-121">Compatibilidade, desempenho, confiabilidade e teste de usabilidade</span><span class="sxs-lookup"><span data-stu-id="5d0d8-121">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="5d0d8-122">Verifique se todo o código usado é de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5d0d8-122">Verify that all code used is 64-bit.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="5d0d8-123">Links para outros recursos</span><span class="sxs-lookup"><span data-stu-id="5d0d8-123">Links to Other Resources</span></span>

-   [<span data-ttu-id="5d0d8-124">Detalhes da implementação do WOW64</span><span class="sxs-lookup"><span data-stu-id="5d0d8-124">WOW64 Implementation Details</span></span>](../winprog64/wow64-implementation-details.md)
-   [<span data-ttu-id="5d0d8-125">Depurando WOW64</span><span class="sxs-lookup"><span data-stu-id="5d0d8-125">Debugging WOW64</span></span>](../winprog64/debugging-wow64.md)
-   <span data-ttu-id="5d0d8-126">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5d0d8-126">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span></span>

 

 
