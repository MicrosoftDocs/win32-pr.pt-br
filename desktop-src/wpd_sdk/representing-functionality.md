---
description: Representando a funcionalidade
ms.assetid: 34a4a015-614d-4fac-98d8-29ae43165798
title: Representando a funcionalidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101614592224a1a5ac079b1f9c3dc89cea9afefe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829082"
---
# <a name="representing-functionality"></a><span data-ttu-id="443d5-103">Representando a funcionalidade</span><span class="sxs-lookup"><span data-stu-id="443d5-103">Representing Functionality</span></span>

<span data-ttu-id="443d5-104">Existem objetos funcionais para identificar ou agrupar logicamente os recursos de recurso de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="443d5-104">Functional objects exist to identify or logically group feature capabilities of a device.</span></span> <span data-ttu-id="443d5-105">Por exemplo, um aplicativo pode ver que um dispositivo dá suporte ao SMS procurando o objeto funcional do SMS.</span><span class="sxs-lookup"><span data-stu-id="443d5-105">For example, an application can see that a device supports SMS by looking for the SMS functional object.</span></span> <span data-ttu-id="443d5-106">Da mesma forma, o aplicativo pode ver que um dispositivo tem recursos de câmera procurando o objeto funcional de captura de imagem ainda.</span><span class="sxs-lookup"><span data-stu-id="443d5-106">Similarly, the application can see that a device has camera capabilities by looking for the Still Image Capture functional object.</span></span>

<span data-ttu-id="443d5-107">Essa representação de objeto flexível ajuda a habilitar o suporte fácil para dispositivos com recursos de várias funções.</span><span class="sxs-lookup"><span data-stu-id="443d5-107">This flexible object representation helps enable easy support for devices with multi-function capabilities.</span></span> <span data-ttu-id="443d5-108">Os drivers podem simplesmente expor quaisquer objetos funcionais que representam seu dispositivo, o que é mais granular do que usar classes de dispositivo tradicionais.</span><span class="sxs-lookup"><span data-stu-id="443d5-108">Drivers can simply expose whatever functional objects represent their device, which is more granular than using traditional device classes.</span></span> <span data-ttu-id="443d5-109">A representação do objeto também ajuda a isolar partes funcionais sobrepostas; por exemplo, alguns telefones podem ter duas câmeras ou quatro armazenamentos.</span><span class="sxs-lookup"><span data-stu-id="443d5-109">The object representation also helps isolate overlapping functional pieces; for example, some phones may have two cameras or four storages.</span></span>

<span data-ttu-id="443d5-110">No sistema operacional Windows 7, os serviços estendem objetos funcionais fornecendo consultas avançadas de recursos e um agrupamento abstrato de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="443d5-110">In the Windows 7 operating system, services extend functional objects by providing rich queries of capabilities and an abstract grouping of content.</span></span> <span data-ttu-id="443d5-111">Os aplicativos podem usar os serviços para descobrir recursos do dispositivo e interagir com o conteúdo com mais eficiência.</span><span class="sxs-lookup"><span data-stu-id="443d5-111">Applications can use services to discover device capabilities and to interact with content more efficiently.</span></span> <span data-ttu-id="443d5-112">Por exemplo, um aplicativo pode ver que um dispositivo dá suporte aos recursos de sincronização de contatos procurando por um objeto de serviço de contatos e pode localizar todos os contatos como objetos filho do objeto de serviço, sem precisar pesquisar recursivamente a hierarquia de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="443d5-112">For example, an application can see that a device supports the contacts-synchronization capabilities by looking for a Contacts service object, and can find all contacts as child objects of the service object, without having to recursively search the storage hierarchy.</span></span>

<span data-ttu-id="443d5-113">Os serviços também permitem que os aplicativos descubram e invoquem o comportamento personalizado em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="443d5-113">Services also allow applications to discover and invoke custom behavior on a device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="443d5-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="443d5-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="443d5-115">**Visão geral do aplicativo**</span><span class="sxs-lookup"><span data-stu-id="443d5-115">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



