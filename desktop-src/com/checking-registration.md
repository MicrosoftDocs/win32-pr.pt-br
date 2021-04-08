---
title: Verificando registro
description: Verificando registro
ms.assetid: 7df63955-d838-4518-8473-0c1a24e90f69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee215fd052ffc242900eead069a8b72fd25b31d5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916087"
---
# <a name="checking-registration"></a><span data-ttu-id="6c512-103">Verificando registro</span><span class="sxs-lookup"><span data-stu-id="6c512-103">Checking Registration</span></span>

<span data-ttu-id="6c512-104">Cada vez que um aplicativo é carregado, ele deve verificar seu registro para determinar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6c512-104">Each time an application loads, it should check its registration to determine the following:</span></span>

-   <span data-ttu-id="6c512-105">Se os CLSIDs estão presentes no registro.</span><span class="sxs-lookup"><span data-stu-id="6c512-105">Whether the CLSIDs are present in the registry.</span></span> <span data-ttu-id="6c512-106">Se eles não estiverem presentes, o aplicativo deverá ser registrado como a configuração original.</span><span class="sxs-lookup"><span data-stu-id="6c512-106">If they are not present, the application should register as the original setup.</span></span>
-   <span data-ttu-id="6c512-107">Se os CLSIDs do aplicativo estão presentes no registro, mas não têm informações relacionadas a OLE 2.</span><span class="sxs-lookup"><span data-stu-id="6c512-107">Whether the application's CLSIDs are present in the register but have no OLE 2-related information in them.</span></span> <span data-ttu-id="6c512-108">Se esse for o caso, o aplicativo deverá ser registrado como a configuração original.</span><span class="sxs-lookup"><span data-stu-id="6c512-108">If this is the case, the application should register as the original setup.</span></span>
-   <span data-ttu-id="6c512-109">Se o caminho que contém entradas de servidor ([LocalServer](localserver.md) e [LocalServer32](localserver32.md), [InprocServer](inprocserver.md) e [InprocServer32](inprocserver32.md)e [DefaultIcon](defaulticon.md)) aponta para o local em que o aplicativo está instalado no momento.</span><span class="sxs-lookup"><span data-stu-id="6c512-109">Whether the path containing server entries ([LocalServer](localserver.md) and [LocalServer32](localserver32.md), [InprocServer](inprocserver.md) and [InprocServer32](inprocserver32.md), and [DefaultIcon](defaulticon.md)) points to the location at which the application is currently installed.</span></span> <span data-ttu-id="6c512-110">Se o caminho não tiver, regrave as entradas de caminho para apontar para o local atual.</span><span class="sxs-lookup"><span data-stu-id="6c512-110">If the path does not, rewrite the path entries to point to the current location.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c512-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6c512-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c512-112">Registrando aplicativos COM</span><span class="sxs-lookup"><span data-stu-id="6c512-112">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 




