---
description: Remoção do Windows Movie Maker
ms.assetid: af55e570-0f24-4376-905a-3b879d5f3a1c
title: Remoção do Windows Movie Maker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36df5ffe4498e05de9fcbbaadf49f8fc32c91b0f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116264"
---
# <a name="removal-of-windows-movie-maker"></a><span data-ttu-id="e9f56-103">Remoção do Windows Movie Maker</span><span class="sxs-lookup"><span data-stu-id="e9f56-103">Removal of Windows Movie Maker</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="e9f56-104">Plataformas afetadas</span><span class="sxs-lookup"><span data-stu-id="e9f56-104">Affected Platforms</span></span>

<span data-ttu-id="e9f56-105">**Clientes** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="e9f56-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="e9f56-106">**Servidores** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e9f56-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="e9f56-107">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="e9f56-107">Feature Impact</span></span>

 <span data-ttu-id="e9f56-108">**Severidade** -alta</span><span class="sxs-lookup"><span data-stu-id="e9f56-108">**Severity** - High</span></span>  
<span data-ttu-id="e9f56-109">**Frequência** -média</span><span class="sxs-lookup"><span data-stu-id="e9f56-109">**Frequency** - Medium</span></span>  


## <a name="description"></a><span data-ttu-id="e9f56-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e9f56-110">Description</span></span>

<span data-ttu-id="e9f56-111">A Microsoft está preterindo e removendo o utilitário Windows Movie Maker.</span><span class="sxs-lookup"><span data-stu-id="e9f56-111">Microsoft is deprecating and removing the Windows Movie Maker utility.</span></span> <span data-ttu-id="e9f56-112">Isso inclui:</span><span class="sxs-lookup"><span data-stu-id="e9f56-112">This includes:</span></span>

-   <span data-ttu-id="e9f56-113">Todos os pontos de entrada para o Windows Movie Maker (por exemplo, menu Iniciar, iniciar > executar)</span><span class="sxs-lookup"><span data-stu-id="e9f56-113">All entry points to Windows Movie Maker (for example, Start Menu, Start > Run)</span></span>
-   <span data-ttu-id="e9f56-114">Todos os binários que foram usados pelo Windows Movie Maker (tudo que estava em% ProgramFiles% \\ Movie Maker)</span><span class="sxs-lookup"><span data-stu-id="e9f56-114">All binaries that were used by Windows Movie Maker (everything that was in %ProgramFiles%\\Movie Maker)</span></span>

<span data-ttu-id="e9f56-115">No entanto, os arquivos de projeto do Movie Maker do usuário permanecerão no sistema e poderão ser acessados por outros aplicativos que dão suporte a esse formato de arquivo.</span><span class="sxs-lookup"><span data-stu-id="e9f56-115">However, a user's Movie Maker project files will remain on the system and be accessible to other applications that support this file format.</span></span>

## <a name="manifestation"></a><span data-ttu-id="e9f56-116">Manifestação</span><span class="sxs-lookup"><span data-stu-id="e9f56-116">Manifestation</span></span>

<span data-ttu-id="e9f56-117">A remoção do Windows Movie Maker resulta no seguinte:</span><span class="sxs-lookup"><span data-stu-id="e9f56-117">Remove of Windows Movie Maker results in the following:</span></span>

-   <span data-ttu-id="e9f56-118">Qualquer tentativa de iniciar o Windows Movie Maker com seus argumentos de linha de comando falhará</span><span class="sxs-lookup"><span data-stu-id="e9f56-118">Any attempt to launch Windows Movie Maker with its command line arguments will fail</span></span>
-   <span data-ttu-id="e9f56-119">Os plug-ins que foram instalados para habilitar novas transformações e animações permanecerão instalados, mas não serão expostos ao usuário final</span><span class="sxs-lookup"><span data-stu-id="e9f56-119">Any plug-ins that were installed to enable new transforms and animations will remain installed but will not be exposed to the end user</span></span>

## <a name="solution"></a><span data-ttu-id="e9f56-120">Solução</span><span class="sxs-lookup"><span data-stu-id="e9f56-120">Solution</span></span>

<span data-ttu-id="e9f56-121">Para ter essa funcionalidade no futuro, um usuário precisará instalar um aplicativo semelhante da Microsoft ou de outro provedor de software.</span><span class="sxs-lookup"><span data-stu-id="e9f56-121">To have such functionality in the future, a user will need to install a similar application from Microsoft or another software provider.</span></span>

 

 



