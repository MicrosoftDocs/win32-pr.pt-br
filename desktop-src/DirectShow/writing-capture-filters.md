---
description: Gravando filtros de captura
ms.assetid: 7dfd1009-da09-49dc-a200-3d7a9f1c70c1
title: Gravando filtros de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de1a64de2b56dbc0728432307036fc46387f539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105767663"
---
# <a name="writing-capture-filters"></a><span data-ttu-id="a3319-103">Gravando filtros de captura</span><span class="sxs-lookup"><span data-stu-id="a3319-103">Writing Capture Filters</span></span>

<span data-ttu-id="a3319-104">Não é recomendável escrever um filtro de captura de áudio ou vídeo para o DirectShow.</span><span class="sxs-lookup"><span data-stu-id="a3319-104">Writing an audio or video capture filter for DirectShow is not recommended.</span></span> <span data-ttu-id="a3319-105">Em vez disso, o DirectShow fornece suporte automático para dispositivos de captura de áudio e vídeo, usando filtros de wrapper e o [enumerador de dispositivo do sistema](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="a3319-105">Instead, DirectShow provides automatic support for audio and video capture devices, using wrapper filters and the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="a3319-106">Para obter mais informações sobre como implementar um driver de dispositivo, consulte a documentação do Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="a3319-106">For more information about implementing a device driver, refer to the Windows Driver Kit (WDK) documentation.</span></span>

<span data-ttu-id="a3319-107">Esta seção destina-se apenas a desenvolvedores que precisam capturar algum tipo de dados personalizados de um dispositivo de hardware incomum.</span><span class="sxs-lookup"><span data-stu-id="a3319-107">This section is intended only for developers who need to capture some kind of custom data from an unusual hardware device.</span></span>

<span data-ttu-id="a3319-108">Este artigo inclui as seções a seguir:</span><span class="sxs-lookup"><span data-stu-id="a3319-108">This article contains the following sections:</span></span>

-   [<span data-ttu-id="a3319-109">Requisitos de PIN para filtros de captura</span><span class="sxs-lookup"><span data-stu-id="a3319-109">Pin Requirements for Capture Filters</span></span>](pin-requirements-for-capture-filters.md)
-   [<span data-ttu-id="a3319-110">Implementando um PIN de visualização (opcional)</span><span class="sxs-lookup"><span data-stu-id="a3319-110">Implementing a Preview Pin (Optional)</span></span>](implementing-a-preview-pin--optional.md)
-   [<span data-ttu-id="a3319-111">Produzindo dados em um filtro de captura</span><span class="sxs-lookup"><span data-stu-id="a3319-111">Producing Data in a Capture Filter</span></span>](producing-data-in-a-capture-filter.md)

## <a name="related-topics"></a><span data-ttu-id="a3319-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a3319-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3319-113">Gravando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="a3319-113">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



