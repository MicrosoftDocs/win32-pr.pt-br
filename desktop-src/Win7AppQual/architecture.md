---
description: O LCIE (Internet Explorer com acoplamento flexível) melhora a confiabilidade do navegador, separando seus componentes e soltando sua interdependência.
ms.assetid: 7609090E-7E2B-4B1F-80FF-192B30A40244
title: Arquitetura (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6edd27246b7b19765288a280bd467de86d2fe50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663349"
---
# <a name="architecture-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="4bb8f-103">Arquitetura (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)</span><span class="sxs-lookup"><span data-stu-id="4bb8f-103">Architecture (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

<span data-ttu-id="4bb8f-104">O LCIE ( *Internet Explorer com acoplamento flexível* ) melhora a confiabilidade do navegador, separando seus componentes e soltando sua interdependência.</span><span class="sxs-lookup"><span data-stu-id="4bb8f-104">*Loosely-coupled Internet Explorer* (LCIE) improves the browser’s reliability by separating its components and loosening their interdependence.</span></span>

<span data-ttu-id="4bb8f-105">Em particular, o LCIE tenta isolar o quadro do Windows Internet Explorer e suas guias em processos separados.</span><span class="sxs-lookup"><span data-stu-id="4bb8f-105">In particular, LCIE tries to isolate the Windows Internet Explorer frame and its tabs into separate processes.</span></span> <span data-ttu-id="4bb8f-106">No Windows Internet Explorer 8, esse isolamento melhora o desempenho e a escalabilidade.</span><span class="sxs-lookup"><span data-stu-id="4bb8f-106">In Windows Internet Explorer 8, this isolation improves performance and scalability.</span></span> <span data-ttu-id="4bb8f-107">Essa alteração de arquitetura pode afetar a compatibilidade de extensões e Complementos, incluindo controles ActiveX, BHOs (navegador Helper Objects) e componentes da barra de ferramentas da interface do usuário criados usando técnicas de programação mais antigas.</span><span class="sxs-lookup"><span data-stu-id="4bb8f-107">This architectural change might affect the compatibility of extensions and add-ons, including ActiveX Controls, Browser Helper Objects (BHOs), and UI toolbar components that are built by using older programming techniques.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4bb8f-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4bb8f-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bb8f-109">Atualizações de design que afetam a compatibilidade entre navegadores</span><span class="sxs-lookup"><span data-stu-id="4bb8f-109">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 



