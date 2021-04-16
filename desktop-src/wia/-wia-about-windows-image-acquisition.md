---
description: A interface de aquisição de imagens do Windows (WIA) é uma API e uma DDI (interface de driver de dispositivo).
ms.assetid: 725543f8-6e33-4e22-904c-95cbec0388c8
title: Sobre a aquisição de imagens do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80eed6289f7a30476ea6889c947577ad003b656e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772510"
---
# <a name="about-windows-image-acquisition"></a><span data-ttu-id="9ae32-103">Sobre a aquisição de imagens do Windows</span><span class="sxs-lookup"><span data-stu-id="9ae32-103">About Windows Image Acquisition</span></span>

<span data-ttu-id="9ae32-104">A interface de aquisição de imagens do Windows (WIA) é uma API e uma DDI (interface de driver de dispositivo).</span><span class="sxs-lookup"><span data-stu-id="9ae32-104">The Windows Image Acquisition (WIA) interface is both an API and a device driver interface (DDI).</span></span> <span data-ttu-id="9ae32-105">A API WIA foi projetada para permitir que os aplicativos:</span><span class="sxs-lookup"><span data-stu-id="9ae32-105">The WIA API is designed to allow applications to:</span></span>

-   <span data-ttu-id="9ae32-106">Execute em um ambiente robusto e estável.</span><span class="sxs-lookup"><span data-stu-id="9ae32-106">Run in a robust and stable environment.</span></span>
-   <span data-ttu-id="9ae32-107">Minimizar problemas de interoperabilidade.</span><span class="sxs-lookup"><span data-stu-id="9ae32-107">Minimize interoperability problems.</span></span>
-   <span data-ttu-id="9ae32-108">Enumere os dispositivos de aquisição de imagem disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9ae32-108">Enumerate available image acquisition devices.</span></span>
-   <span data-ttu-id="9ae32-109">Crie conexões a vários dispositivos simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="9ae32-109">Create connections to multiple devices simultaneously.</span></span>
-   <span data-ttu-id="9ae32-110">Consultar Propriedades de dispositivos de maneira padrão e expansível.</span><span class="sxs-lookup"><span data-stu-id="9ae32-110">Query properties of devices in a standard and expandable manner.</span></span>
-   <span data-ttu-id="9ae32-111">Adquira dados de dispositivo usando mecanismos de transferência padrão e de alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="9ae32-111">Acquire device data using standard and high performance transfer mechanisms.</span></span>
-   <span data-ttu-id="9ae32-112">Manter Propriedades de imagem entre transferências de dados.</span><span class="sxs-lookup"><span data-stu-id="9ae32-112">Maintain image properties across data transfers.</span></span>
-   <span data-ttu-id="9ae32-113">Seja notificado sobre uma ampla variedade de eventos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ae32-113">Be notified of a wide variety of device events.</span></span>

<span data-ttu-id="9ae32-114">O WIADDI foi projetado para minimizar a quantidade de código que um fornecedor de hardware deve escrever, mantendo a flexibilidade para criar soluções individuais.</span><span class="sxs-lookup"><span data-stu-id="9ae32-114">The WIADDI is designed to minimize the amount of code a hardware vendor must write, while maintaining the flexibility to craft individual solutions.</span></span> <span data-ttu-id="9ae32-115">Isso é feito por:</span><span class="sxs-lookup"><span data-stu-id="9ae32-115">This is accomplished by:</span></span>

-   <span data-ttu-id="9ae32-116">Fornecer uma biblioteca de serviço de dispositivo padrão que executa a maioria das operações de driver.</span><span class="sxs-lookup"><span data-stu-id="9ae32-116">Providing a standard device service library that performs most driver operations.</span></span>
-   <span data-ttu-id="9ae32-117">Promover padrões de comunicação de dispositivos do setor para que um driver WIA dê suporte à maioria dos dispositivos WIA.</span><span class="sxs-lookup"><span data-stu-id="9ae32-117">Promoting industry device communications standards so that one WIA driver supports most WIA devices.</span></span> <span data-ttu-id="9ae32-118">Por exemplo, o PTP (protocolo de transferência de imagem).</span><span class="sxs-lookup"><span data-stu-id="9ae32-118">For example, Picture Transfer Protocol (PTP).</span></span>
-   <span data-ttu-id="9ae32-119">Permitir que o driver de dispositivo dê suporte a interfaces personalizadas, embora não exija que ela use a biblioteca de serviço de dispositivo padrão.</span><span class="sxs-lookup"><span data-stu-id="9ae32-119">Allowing the device driver to support custom interfaces, while not requiring that it use the standard device service library.</span></span> <span data-ttu-id="9ae32-120">No entanto, os drivers ainda precisam implementar as interfaces WIA padrão.</span><span class="sxs-lookup"><span data-stu-id="9ae32-120">However, drivers still need to implement the standard WIA interfaces.</span></span>

<span data-ttu-id="9ae32-121">Esta seção apresenta uma breve visão geral da interface WIA nas seguintes áreas:</span><span class="sxs-lookup"><span data-stu-id="9ae32-121">This section presents a brief overview of the WIA interface in the following areas:</span></span>

-   [<span data-ttu-id="9ae32-122">Arquitetura WIA</span><span class="sxs-lookup"><span data-stu-id="9ae32-122">WIA Architecture</span></span>](-wia-wia-architecture.md)
-   [<span data-ttu-id="9ae32-123">Compatibilidade do STI</span><span class="sxs-lookup"><span data-stu-id="9ae32-123">STI Compatibility</span></span>](-wia-sti-compatibility.md)
-   [<span data-ttu-id="9ae32-124">Compatibilidade com TWAIN</span><span class="sxs-lookup"><span data-stu-id="9ae32-124">TWAIN Compatibility</span></span>](-wia-twain-compatibility.md)
-   [<span data-ttu-id="9ae32-125">Gerenciador de Dispositivos WIA</span><span class="sxs-lookup"><span data-stu-id="9ae32-125">WIA Device Manager</span></span>](-wia-wia-device-manager.md)
-   [<span data-ttu-id="9ae32-126">Biblioteca de serviço minidriver WIA</span><span class="sxs-lookup"><span data-stu-id="9ae32-126">WIA Minidriver Service Library</span></span>](-wia-wia-minidriver-service-library.md)
-   [<span data-ttu-id="9ae32-127">Minidriver WIA</span><span class="sxs-lookup"><span data-stu-id="9ae32-127">WIA Minidriver</span></span>](-wia-wia-minidriver.md)

 

 



