---
description: Enumerando dispositivos e filtros
ms.assetid: 334bba2a-7477-4115-9ce0-d4495c1fc290
title: Enumerando dispositivos e filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69997a4af4f3160f0b338bc9c595adea83a5354
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825922"
---
# <a name="enumerating-devices-and-filters"></a><span data-ttu-id="1e8f4-103">Enumerando dispositivos e filtros</span><span class="sxs-lookup"><span data-stu-id="1e8f4-103">Enumerating Devices and Filters</span></span>

<span data-ttu-id="1e8f4-104">Às vezes, um aplicativo precisa localizar um filtro específico no sistema do usuário.</span><span class="sxs-lookup"><span data-stu-id="1e8f4-104">Sometimes an application needs to locate a particular filter on the user's system.</span></span> <span data-ttu-id="1e8f4-105">Por exemplo, um aplicativo de captura de vídeo pode exibir uma lista de dispositivos de captura disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1e8f4-105">For example, a video capture application might display a list of available capture devices.</span></span> <span data-ttu-id="1e8f4-106">Como o DirectShow usa uma arquitetura baseada em componentes, você não pode saber em tempo de design quais filtros estão instalados no sistema do usuário.</span><span class="sxs-lookup"><span data-stu-id="1e8f4-106">Because DirectShow uses a component-based architecture, you cannot know at design time which filters are installed on the user's system.</span></span> <span data-ttu-id="1e8f4-107">Isso é particularmente verdadeiro para filtros que representam dispositivos de hardware.</span><span class="sxs-lookup"><span data-stu-id="1e8f4-107">This is particularly true for filters that represent hardware devices.</span></span> <span data-ttu-id="1e8f4-108">O DirectShow fornece dois componentes que localizam filtros registrados:</span><span class="sxs-lookup"><span data-stu-id="1e8f4-108">DirectShow provides two components that locate registered filters:</span></span>

-   <span data-ttu-id="1e8f4-109">O [enumerador de dispositivo do sistema](system-device-enumerator.md) localiza filtros por sua categoria.</span><span class="sxs-lookup"><span data-stu-id="1e8f4-109">The [System Device Enumerator](system-device-enumerator.md) finds filters by their category.</span></span>
-   <span data-ttu-id="1e8f4-110">O [mapeador de filtro](filter-mapper.md) localiza filtros de acordo com os critérios de pesquisa fornecidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1e8f4-110">The [Filter Mapper](filter-mapper.md) finds filters according to search criteria supplied by the application.</span></span>

<span data-ttu-id="1e8f4-111">Os enumeradores abordados nesta seção seguem o formulário padrão usado pelas interfaces de enumeração COM.</span><span class="sxs-lookup"><span data-stu-id="1e8f4-111">The enumerators discussed in this section follow the standard form used by COM enumeration interfaces.</span></span> <span data-ttu-id="1e8f4-112">Para obter mais informações, consulte o tópico "IEnumXXXX" no SDK (Software Development Kit) do Microsoft Platform.</span><span class="sxs-lookup"><span data-stu-id="1e8f4-112">For more information, see the "IEnumXXXX" topic in the Microsoft Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="1e8f4-113">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="1e8f4-113">This section contains the following topics:</span></span>

-   [<span data-ttu-id="1e8f4-114">Usando o enumerador de dispositivo do sistema</span><span class="sxs-lookup"><span data-stu-id="1e8f4-114">Using the System Device Enumerator</span></span>](using-the-system-device-enumerator.md)
-   [<span data-ttu-id="1e8f4-115">Usando o mapeador de filtro</span><span class="sxs-lookup"><span data-stu-id="1e8f4-115">Using the Filter Mapper</span></span>](using-the-filter-mapper.md)

## <a name="related-topics"></a><span data-ttu-id="1e8f4-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1e8f4-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e8f4-117">Tarefas básicas do DirectShow</span><span class="sxs-lookup"><span data-stu-id="1e8f4-117">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 



