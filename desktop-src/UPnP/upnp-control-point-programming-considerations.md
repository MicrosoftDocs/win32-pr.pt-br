---
title: Considerações de programação de ponto de controle
description: Os desenvolvedores que criam aplicativos baseados em UPnP (ou pontos de controle) devem usar esses aplicativos de um \_ cliente coinit APARTMENTTHREADED. Há problemas conhecidos ao usar a API do ponto de controle de um \_ cliente de vários threads coinit em execução sob estresse.
ms.assetid: a5d79a29-4192-40af-b75d-a31f1f46149c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76955177f9fc0c3b164d84998547c1afdfbfb4bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822892"
---
# <a name="control-point-programming-considerations"></a><span data-ttu-id="99850-104">Considerações de programação de ponto de controle</span><span class="sxs-lookup"><span data-stu-id="99850-104">Control Point Programming Considerations</span></span>

<span data-ttu-id="99850-105">Os desenvolvedores que criam aplicativos baseados em UPnP (ou pontos de controle) devem usar esses aplicativos de um \_ cliente coinit APARTMENTTHREADED.</span><span class="sxs-lookup"><span data-stu-id="99850-105">Developers who create UPnP-based applications (or control points) must use these applications from a COINIT\_APARTMENTTHREADED client.</span></span> <span data-ttu-id="99850-106">Há problemas conhecidos ao usar a API do ponto de controle de um \_ cliente de vários threads coinit em execução sob estresse.</span><span class="sxs-lookup"><span data-stu-id="99850-106">There are known problems when using the Control Point API from a COINIT\_MULTITHREADED client running under stress.</span></span>

 

 




