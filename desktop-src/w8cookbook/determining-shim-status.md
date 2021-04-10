---
title: Determinando o status do Shim
description: Determinando o status do Shim
ms.assetid: 8D0B633F-9117-4F90-BF8C-AC5F57FCD30B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b830cbb4579aa2e523dfe2ec1129ed9cd10f37
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292621"
---
# <a name="determining-shim-status"></a><span data-ttu-id="61773-103">Determinando o status do Shim</span><span class="sxs-lookup"><span data-stu-id="61773-103">Determining shim status</span></span>

## <a name="platforms"></a><span data-ttu-id="61773-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="61773-104">Platforms</span></span>

<dl> <span data-ttu-id="61773-105">Clientes-Windows 8</span><span class="sxs-lookup"><span data-stu-id="61773-105">Clients - Windows 8</span></span>  
<span data-ttu-id="61773-106">Servidores-Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61773-106">Servers - Windows Server 2012</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="61773-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="61773-107">Description</span></span>

<span data-ttu-id="61773-108">O Windows 8 registra eventos quando os aplicativos estão sendo corrigido por vários motivos.</span><span class="sxs-lookup"><span data-stu-id="61773-108">Windows 8 logs events when apps are being shimmed for various reasons.</span></span> <span data-ttu-id="61773-109">A maneira mais fácil de determinar se seu aplicativo está sendo corrigido é verificar o Visualizador de eventos.</span><span class="sxs-lookup"><span data-stu-id="61773-109">The easiest way to determine if your app is being shimmed is to check the event viewer.</span></span> <span data-ttu-id="61773-110">Acesse logs de aplicativos e serviços \\ Microsoft Windows Application-Experience \\ telemetria de programa.</span><span class="sxs-lookup"><span data-stu-id="61773-110">Go to Applications and Services Logs\\Microsoft Windows Application-Experience Program\\Telemetry.</span></span>

## <a name="mitigation"></a><span data-ttu-id="61773-111">Atenuação</span><span class="sxs-lookup"><span data-stu-id="61773-111">Mitigation</span></span>

<span data-ttu-id="61773-112">A melhor maneira de se ficar fora do shims é renomear o executável ou aumentar a versão principal em 1 (recompilar o executável).</span><span class="sxs-lookup"><span data-stu-id="61773-112">The best way to get yourself out of shimming is to rename the executable or to increase the major version by 1 (recompile the executable).</span></span>

 

 




