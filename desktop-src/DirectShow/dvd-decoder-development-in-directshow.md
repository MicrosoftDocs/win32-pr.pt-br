---
description: Desenvolvimento de decodificador de DVD no DirectShow
ms.assetid: c00ff132-fee1-47b5-8a8a-df7cb920ad89
title: Desenvolvimento de decodificador de DVD no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3de64b3c1d91dbf5f22ba3e4b4ae8fe78edda5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456802"
---
# <a name="dvd-decoder-development-in-directshow"></a><span data-ttu-id="b7551-103">Desenvolvimento de decodificador de DVD no DirectShow</span><span class="sxs-lookup"><span data-stu-id="b7551-103">DVD Decoder Development in DirectShow</span></span>

<span data-ttu-id="b7551-104">Esta seção contém ponteiros para as páginas de referência de todos os conjuntos de propriedades e interfaces do DirectShow que são específicos de DVD ou mais usados extensivamente na decodificação de DVD.</span><span class="sxs-lookup"><span data-stu-id="b7551-104">This section contains pointers to the reference pages for all the DirectShow property sets and interfaces that are either DVD-specific or else used extensively in DVD decoding.</span></span> <span data-ttu-id="b7551-105">Além do que está listado aqui, um decodificador e seus PINs também devem oferecer suporte às interfaces de filtro do DirectShow genérico, conforme descrito em [escrevendo filtros do DirectShow](writing-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="b7551-105">In addition to what is listed here, a decoder and its pins must also support the generic DirectShow filter interfaces as described in [Writing DirectShow Filters](writing-directshow-filters.md).</span></span>

<span data-ttu-id="b7551-106">Esta seção contém os seguintes tópicos.</span><span class="sxs-lookup"><span data-stu-id="b7551-106">This section contains the following topics.</span></span>

-   [<span data-ttu-id="b7551-107">Controle de volume do decodificador</span><span class="sxs-lookup"><span data-stu-id="b7551-107">Decoder Volume Control</span></span>](decoder-volume-control.md)
-   [<span data-ttu-id="b7551-108">Suporte à alteração da região do DVD no Windows</span><span class="sxs-lookup"><span data-stu-id="b7551-108">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)

<span data-ttu-id="b7551-109">Consulte também:</span><span class="sxs-lookup"><span data-stu-id="b7551-109">See also:</span></span>

-   [<span data-ttu-id="b7551-110">**Conjunto de propriedades de karaokê de DVD**</span><span class="sxs-lookup"><span data-stu-id="b7551-110">**DVD Karaoke Property Set**</span></span>](dvd-karaoke-property-set.md)
-   [<span data-ttu-id="b7551-111">**Conjunto de propriedades da proteção contra cópia de DVD**</span><span class="sxs-lookup"><span data-stu-id="b7551-111">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   [<span data-ttu-id="b7551-112">**Conjunto de propriedades de subimagem de DVD**</span><span class="sxs-lookup"><span data-stu-id="b7551-112">**DVD Subpicture Property Set**</span></span>](dvd-subpicture-property-set.md)
-   [<span data-ttu-id="b7551-113">Conjunto de propriedades de PIN</span><span class="sxs-lookup"><span data-stu-id="b7551-113">Pin Property Set</span></span>](pin-property-set.md)
-   [<span data-ttu-id="b7551-114">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="b7551-114">**IKsPropertySet**</span></span>](ikspropertyset.md)
-   <span data-ttu-id="b7551-115">[**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) (somente decodificadores de hardware)</span><span class="sxs-lookup"><span data-stu-id="b7551-115">[**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) (hardware decoders only)</span></span>
-   <span data-ttu-id="b7551-116">[**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) (somente decodificadores de hardware)</span><span class="sxs-lookup"><span data-stu-id="b7551-116">[**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) (hardware decoders only)</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7551-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b7551-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7551-118">Interfaces e especificações do decodificador</span><span class="sxs-lookup"><span data-stu-id="b7551-118">Decoder Interfaces and Specifications</span></span>](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 



