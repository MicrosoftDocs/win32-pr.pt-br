---
description: Um filtro de captura é um elemento de um aplicativo NPP que instrui o driver de Monitor de Rede (Nmnt.sys) quais quadros de dados de rede serão retidos e quais quadros serão ignorados.
ms.assetid: 6ab17e18-bd97-42a8-b569-b205ac19ffd1
title: Sobre filtros de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7226bb7dc5bc214ab2e09504cc232e1bf591840f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766852"
---
# <a name="about-capture-filters"></a><span data-ttu-id="22a00-103">Sobre filtros de captura</span><span class="sxs-lookup"><span data-stu-id="22a00-103">About Capture Filters</span></span>

<span data-ttu-id="22a00-104">Um filtro de captura é um elemento de um aplicativo NPP que instrui o driver de Monitor de Rede (Nmnt.sys) quais quadros de dados de rede serão retidos e quais quadros serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="22a00-104">A capture filter is an element of an NPP application that instructs the Network Monitor driver (Nmnt.sys) which frames of network data to retain and which frames to ignore.</span></span> <span data-ttu-id="22a00-105">A vantagem de definir um filtro de captura é maior eficiência.</span><span class="sxs-lookup"><span data-stu-id="22a00-105">The advantage of setting a capture filter is greater efficiency.</span></span> <span data-ttu-id="22a00-106">Você não precisa examinar os quadros capturados; o driver de Monitor de Rede os examina.</span><span class="sxs-lookup"><span data-stu-id="22a00-106">You do not have to examine captured frames; the Network Monitor driver examines them.</span></span> <span data-ttu-id="22a00-107">Essa abordagem elimina a cópia de quadros, que fornece uma vantagem de uso de memória.</span><span class="sxs-lookup"><span data-stu-id="22a00-107">This approach eliminates frame copying, which provides a memory use advantage.</span></span>

## <a name="capture-filter-structure"></a><span data-ttu-id="22a00-108">Capturar estrutura do filtro</span><span class="sxs-lookup"><span data-stu-id="22a00-108">Capture Filter Structure</span></span>

<span data-ttu-id="22a00-109">Os filtros de captura consistem em três elementos:</span><span class="sxs-lookup"><span data-stu-id="22a00-109">Capture filters consist of three elements:</span></span>

-   <span data-ttu-id="22a00-110">Configurações de ETYPE/SAP</span><span class="sxs-lookup"><span data-stu-id="22a00-110">Etype/SAP settings</span></span>
-   <span data-ttu-id="22a00-111">Endereço</span><span class="sxs-lookup"><span data-stu-id="22a00-111">Address</span></span>
-   <span data-ttu-id="22a00-112">Correspondência de padrões</span><span class="sxs-lookup"><span data-stu-id="22a00-112">Pattern match</span></span>

<span data-ttu-id="22a00-113">Juntos, esses elementos avaliam logicamente quais quadros incluir ou excluir, durante a operação de um aplicativo NPP.</span><span class="sxs-lookup"><span data-stu-id="22a00-113">Together, these elements logically evaluate which frames to include, or exclude, during the operation of an NPP application.</span></span> <span data-ttu-id="22a00-114">O filtro de captura fornece correspondências complexas e exclusões de elementos de quadro para o aplicativo NPP.</span><span class="sxs-lookup"><span data-stu-id="22a00-114">The capture filter supplies complex matches and exclusions of frame elements to the NPP application.</span></span>

<span data-ttu-id="22a00-115">Monitor de Rede implementa o filtro de captura por meio de uma estrutura de dados, [**CAPTUREFILTER**](the-capturefilter-structure.md), passado para o NPP e, em seguida, passado para o driver de monitor de rede quando a captura é iniciada.</span><span class="sxs-lookup"><span data-stu-id="22a00-115">Network Monitor implements the capture filter through a data structure, [**CAPTUREFILTER**](the-capturefilter-structure.md), passed to the NPP and then passed on to the Network Monitor driver when the capture starts.</span></span>

<span data-ttu-id="22a00-116">Para obter mais informações sobre operações NPP e funcionalidade de BLOB, consulte [provedores de pacotes de rede](network-packet-providers.md) e [blobs de monitor de rede](network-monitor-blobs.md).</span><span class="sxs-lookup"><span data-stu-id="22a00-116">For more information about NPP operations and BLOB functionality, see [Network Packet Providers](network-packet-providers.md) and [Network Monitor BLOBS](network-monitor-blobs.md).</span></span>

 

 



