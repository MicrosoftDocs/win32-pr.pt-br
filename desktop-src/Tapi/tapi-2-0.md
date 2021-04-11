---
description: A TAPI 2,0 fornece um pequeno número de aprimoramentos para a funcionalidade básica da TAPI 1,4.
ms.assetid: f3a319b4-5e82-4bf9-bd89-a027d58ad126
title: TAPI 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34a3503916c6ec90c3a90e648ac3622c271d810
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296734"
---
# <a name="tapi-20"></a><span data-ttu-id="149f8-103">TAPI 2,0</span><span class="sxs-lookup"><span data-stu-id="149f8-103">TAPI 2.0</span></span>

<span data-ttu-id="149f8-104">A TAPI 2,0 fornece um pequeno número de aprimoramentos para a funcionalidade básica da TAPI 1,4.</span><span class="sxs-lookup"><span data-stu-id="149f8-104">TAPI 2.0 provides a small number of enhancements to the basic TAPI 1.4 functionality.</span></span> <span data-ttu-id="149f8-105">No entanto, houve algumas grandes alterações arquitetônicas que melhoraram muito sua estabilidade.</span><span class="sxs-lookup"><span data-stu-id="149f8-105">However, there were some major architectural changes that greatly improved its stability.</span></span> <span data-ttu-id="149f8-106">A maioria das alterações foram as alterações fundamentais necessárias para colocar a TAPI no Windows NT 4,0 e aproveitar seus recursos (suporte completo a 32 bits, serviços e Unicode).</span><span class="sxs-lookup"><span data-stu-id="149f8-106">Most of the changes were fundamental changes necessary to bring TAPI to Windows NT 4.0 and take advantage of its features (full 32-bit support, services, and Unicode).</span></span> <span data-ttu-id="149f8-107">No entanto, essas alterações eram internas à TAPI e tinham pouco efeito em aplicativos TAPI.</span><span class="sxs-lookup"><span data-stu-id="149f8-107">However, these changes were internal to TAPI and had little effect on TAPI applications.</span></span>

<span data-ttu-id="149f8-108">Os aplicativos que dão suporte a TAPI 1,3 e 1,4 (aplicativos de 16 bits por meio de uma camada de conversão) funcionam bem em sistemas operacionais Windows Server 2003, Windows XP, Windows 2000 e Windows NT.</span><span class="sxs-lookup"><span data-stu-id="149f8-108">Applications that support TAPI 1.3 and 1.4 (16-bit applications by way of a thunking layer) work well on Windows Server 2003 operating systems, Windows XP, Windows 2000, and Windows NT.</span></span> <span data-ttu-id="149f8-109">No entanto, o efeito nos desenvolvedores do provedor de serviços era significativo.</span><span class="sxs-lookup"><span data-stu-id="149f8-109">However, the effect on service-provider developers was significant.</span></span> <span data-ttu-id="149f8-110">Os provedores de serviço para esses sistemas operacionais devem ser DLLs Unicode de 32 bits que podem ser executadas no contexto de TAPISRV, não no contexto do aplicativo TAPI (como fazia todas as TSPs anteriores baseadas em Win16).</span><span class="sxs-lookup"><span data-stu-id="149f8-110">Service providers for these operating systems must be fully 32-bit Unicode DLLs that can run in the context of TAPISRV, not in the context of the TAPI application (as did all earlier Win16-based TSPs).</span></span> <span data-ttu-id="149f8-111">O TSPs desenvolvido para TAPI 1,4 não funciona em sistemas operacionais Windows Server 2003, Windows XP, Windows 2000 ou Windows NT.</span><span class="sxs-lookup"><span data-stu-id="149f8-111">TSPs designed for TAPI 1.4 do not work on Windows Server 2003 operating systems, Windows XP, Windows 2000, or Windows NT.</span></span>

<span data-ttu-id="149f8-112">A TAPI 2,0 também adiciona os recursos importantes do suporte ao Call Center e ao suporte de QOS (qualidade de serviço).</span><span class="sxs-lookup"><span data-stu-id="149f8-112">TAPI 2.0 also adds the important features of call center support and Quality of Service (QOS) support.</span></span>

<span data-ttu-id="149f8-113">Os binários do sistema TAPI fornecidos com o Windows oferecem suporte a TAPI versões 1,3 e 1,4 para todos os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="149f8-113">The TAPI system binaries that come with Windows support TAPI versions 1.3 and 1.4 for all applications.</span></span> <span data-ttu-id="149f8-114">No entanto, os aplicativos de 16 bits não podem usar a TAPI 2,0 e não é possível usar um TSP 2. x de TAPI de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="149f8-114">However, 16-bit applications cannot use TAPI 2.0, and you cannot use a 16-bit TAPI 2.x TSP.</span></span>

 

 



