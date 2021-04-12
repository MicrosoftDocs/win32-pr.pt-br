---
title: Verificações de kernel de drivers não-WHQL assinados
description: Para dispositivos que limpam a instalação do Windows 10 e onde a inicialização segura está ativada (Observe que esse é o padrão para todos os novos dispositivos desde o lançamento do Windows 8,0), todos os novos drivers devem ser assinados pelo WHQL/Sysdev, em vez de usar certificados cruzados com assinatura cruzada.
ms.assetid: D2A13F91-BA44-4044-B1F4-54393A9F1063
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582db864627a2945debca33c8e75ac74fb20acc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364283"
---
# <a name="kernel-checks-for-non-whql-signed-drivers"></a><span data-ttu-id="8ac4d-103">Verificações de kernel de drivers não-WHQL assinados</span><span class="sxs-lookup"><span data-stu-id="8ac4d-103">Kernel checks for non-WHQL signed drivers</span></span>

<span data-ttu-id="8ac4d-104">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="8ac4d-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8ac4d-105">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="8ac4d-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8ac4d-106">Para dispositivos que limpam a instalação do Windows 10 e onde a inicialização segura está ativada (Observe que esse é o padrão para todos os novos dispositivos desde o lançamento do Windows 8,0), todos os novos drivers devem ser assinados pelo WHQL/Sysdev, em vez de usar certificados cruzados com assinatura cruzada.</span><span class="sxs-lookup"><span data-stu-id="8ac4d-106">For devices that clean install Windows 10, and where Secure Boot is on (note that this is standard for all new devices since the release of Windows 8.0), all new drivers must be signed by WHQL/Sysdev rather than just use cross-signed certificates.</span></span> <span data-ttu-id="8ac4d-107">Dispositivos que são atualizados e casos em que os drivers foram assinados com um certificado cruzado antes que essa política entrasse em vigor são excluídos desta política para garantir a compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="8ac4d-107">Devices that are upgraded and cases where drivers have been signed with a cross-cert before this policy went into effect are excluded from this policy to ensure backwards compatibility.</span></span> <span data-ttu-id="8ac4d-108">Essa política foi anunciada em abril de 2015, no entanto, ela será imposta com a edição de aniversário do Windows, lançada em agosto de 2016.</span><span class="sxs-lookup"><span data-stu-id="8ac4d-108">This policy was announced April 2015, however it will be enforced with the Windows Anniversary Edition, released August 2016.</span></span>

<span data-ttu-id="8ac4d-109">Nos casos em que um driver não está assinado corretamente, ele será manifestado como uma notificação do PCA de que os drivers são bloqueados quando não forem aprovados nos requisitos de assinatura.</span><span class="sxs-lookup"><span data-stu-id="8ac4d-109">In cases where a driver is not signed correctly, it will manifest as a PCA notification that the driver(s) is blocked when it doesn’t pass signature requirements.</span></span> <span data-ttu-id="8ac4d-110">Isso impede que uma experiência de usuário desconectada posteriormente do driver seja bloqueada no kernel de forma transparente.</span><span class="sxs-lookup"><span data-stu-id="8ac4d-110">This prevents a later disconnected user experience of the driver being blocked in kernel transparently.</span></span>

<span data-ttu-id="8ac4d-111">Para obter mais informações, consulte [esta postagem de blog](https://techcommunity.microsoft.com/t5/Windows-Hardware-Certification/bg-p/WindowsHardwareCertification/), que anuncia a alteração de assinatura de driver.</span><span class="sxs-lookup"><span data-stu-id="8ac4d-111">For more information, please refer to [this blog post](https://techcommunity.microsoft.com/t5/Windows-Hardware-Certification/bg-p/WindowsHardwareCertification/), which announces the driver signing change.</span></span>

 

 




