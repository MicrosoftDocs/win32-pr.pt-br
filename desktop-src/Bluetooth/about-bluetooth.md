---
title: Sobre o Bluetooth
description: O Bluetooth é um protocolo padrão do setor que permite a conectividade sem fio para uma infinidade de dispositivos, incluindo computadores, impressoras, celulares e dispositivos portáteis.
ms.assetid: 424168a1-e55c-4947-9a80-8594b4d83bbd
keywords:
- Bluetooth com Bluetooth, descrito
- Bluetooth Bluetooth, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b704bb3245adcd75948f7f9fbb411697c7c45f0
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104007159"
---
# <a name="about-bluetooth"></a><span data-ttu-id="a2b98-105">Sobre o Bluetooth</span><span class="sxs-lookup"><span data-stu-id="a2b98-105">About Bluetooth</span></span>

<span data-ttu-id="a2b98-106">O Bluetooth é um protocolo padrão do setor que permite a conectividade sem fio para uma infinidade de dispositivos, incluindo computadores, impressoras, celulares e dispositivos portáteis.</span><span class="sxs-lookup"><span data-stu-id="a2b98-106">Bluetooth is an industry-standard protocol that enables wireless connectivity for a multitude of devices, including computers, printers, mobile phones, and handheld devices.</span></span>

<span data-ttu-id="a2b98-107">Os principais recursos do Bluetooth incluem:</span><span class="sxs-lookup"><span data-stu-id="a2b98-107">Key Bluetooth features include:</span></span>

-   <span data-ttu-id="a2b98-108">Um protocolo sem fio de consumo de baixo custo e baixa energia com suporte padrão do setor e aceitação mundial.</span><span class="sxs-lookup"><span data-stu-id="a2b98-108">A low-cost, low-power consumption wireless protocol with industry-standard support and worldwide acceptance.</span></span>
-   <span data-ttu-id="a2b98-109">Uma interface de programação definida e familiar que os desenvolvedores podem usar para desenvolver ou portar aplicativos rapidamente.</span><span class="sxs-lookup"><span data-stu-id="a2b98-109">A defined and familiar programming interface that developers can use to quickly develop or port applications.</span></span>
-   <span data-ttu-id="a2b98-110">Um site oficial e uma organização cooperativa em todo o setor que explica, promove e padroniza a tecnologia Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="a2b98-110">An official Web site and an industry-wide cooperative organization that explains, promotes, and standardizes Bluetooth technology.</span></span> <span data-ttu-id="a2b98-111">Para obter mais informações, consulte [www.Bluetooth.com](https://www.bluetooth.com/).</span><span class="sxs-lookup"><span data-stu-id="a2b98-111">For more information, see [www.bluetooth.com](https://www.bluetooth.com/).</span></span>

<span data-ttu-id="a2b98-112">O Bluetooth no Windows fornece serviços principais que são semelhantes àqueles expostos pelo protocolo de controle de transmissão (a parte TCP do TCP/IP).</span><span class="sxs-lookup"><span data-stu-id="a2b98-112">Bluetooth on Windows provides core services that are similar to those exposed by Transmission Control Protocol (the TCP part of TCP/IP).</span></span> <span data-ttu-id="a2b98-113">Como muitos protocolos e serviços de rede, a conectividade Bluetooth e a transferência de dados são programadas por meio de chamadas de função do Windows Sockets, usando técnicas comuns de programação do Windows Sockets e extensões Bluetooth específicas.</span><span class="sxs-lookup"><span data-stu-id="a2b98-113">Like many networking protocols and services, Bluetooth connectivity and data transfer are programmed through Windows Sockets function calls, using common Windows Sockets programming techniques and specific Bluetooth extensions.</span></span> <span data-ttu-id="a2b98-114">No entanto, como existem diferenças significativas entre uma rede fixa e com fio e uma rede ad hoc sem fio, o Bluetooth fornece extensões como descoberta de serviço/dispositivo e notificação que permitem que os aplicativos operem corretamente no ambiente sem fio.</span><span class="sxs-lookup"><span data-stu-id="a2b98-114">However, because significant differences exist between a wired, fixed network and a wireless ad-hoc network, Bluetooth provides extensions such as service/device discovery and notification that enable applications to operate properly in the wireless environment.</span></span> <span data-ttu-id="a2b98-115">Essas extensões também abrem a maneira de portar simples para tecnologias semelhantes, como IrDA ou transportes de sem fio futuros.</span><span class="sxs-lookup"><span data-stu-id="a2b98-115">These extensions also pave the way for simple porting to similar technologies, such as IrDA, or future wireless transports.</span></span>

<span data-ttu-id="a2b98-116">A Microsoft oferece suporte para Bluetooth no Windows XP com Service Pack 1 (SP1) e posterior, no Windows XP Embedded com Service Pack 2 e no Windows CE.</span><span class="sxs-lookup"><span data-stu-id="a2b98-116">Microsoft provides support for Bluetooth on Windows XP with Service Pack 1 (SP1) and later, on Windows XP Embedded with Service Pack 2, and on Windows CE.</span></span> <span data-ttu-id="a2b98-117">Os aplicativos Bluetooth executados no Windows XP devem ser capazes de serem executados em uma imagem de tempo de execução baseada no Windows XP Embedded que inclui as dependências necessárias.</span><span class="sxs-lookup"><span data-stu-id="a2b98-117">Bluetooth applications that run on Windows XP should be able to run on a Windows XP Embedded-based run-time image that includes the required dependencies.</span></span> <span data-ttu-id="a2b98-118">Para obter mais informações sobre o Windows XP Embedded, consulte a documentação da ajuda do Windows XP Embedded no MSDN.</span><span class="sxs-lookup"><span data-stu-id="a2b98-118">For more information about Windows XP Embedded, see the Windows XP Embedded Help documentation on MSDN.</span></span> <span data-ttu-id="a2b98-119">Para obter mais informações sobre a programação de Windows CE, consulte o SDK do Windows CE.</span><span class="sxs-lookup"><span data-stu-id="a2b98-119">For more information about Windows CE programming, consult the Windows CE SDK.</span></span>

<span data-ttu-id="a2b98-120">A Microsoft fornece duas abordagens para a programação de Bluetooth no Windows:</span><span class="sxs-lookup"><span data-stu-id="a2b98-120">Microsoft provides two approaches for programming Bluetooth on Windows:</span></span>

-   <span data-ttu-id="a2b98-121">Usando a interface do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="a2b98-121">Using the Windows Sockets interface</span></span>
-   <span data-ttu-id="a2b98-122">Gerenciando dispositivos diretamente usando interfaces Bluetooth de não soquete</span><span class="sxs-lookup"><span data-stu-id="a2b98-122">Managing devices directly by using nonsocket Bluetooth interfaces</span></span>

<span data-ttu-id="a2b98-123">Esta seção fornece informações de visão geral sobre essas duas abordagens nos tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="a2b98-123">This section provides overview information about both of these approaches in the following topics.</span></span> <span data-ttu-id="a2b98-124">Para obter mais informações sobre como usar elementos da API do Windows Sockets para programar Bluetooth, consulte [programação Bluetooth com Windows Sockets](bluetooth-programming-with-windows-sockets.md).</span><span class="sxs-lookup"><span data-stu-id="a2b98-124">For more information about using Windows Sockets API elements to program Bluetooth, see [Bluetooth Programming with Windows Sockets](bluetooth-programming-with-windows-sockets.md).</span></span>



| <span data-ttu-id="a2b98-125">Seção</span><span class="sxs-lookup"><span data-stu-id="a2b98-125">Section</span></span>                                                                                | <span data-ttu-id="a2b98-126">Conteúdo</span><span class="sxs-lookup"><span data-stu-id="a2b98-126">Content</span></span>                                                           |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="a2b98-127">Suporte do Windows Sockets para Bluetooth</span><span class="sxs-lookup"><span data-stu-id="a2b98-127">Windows Sockets Support for Bluetooth</span></span>](windows-sockets-support-for-bluetooth.md)     | <span data-ttu-id="a2b98-128">Descreve a relação entre o Bluetooth e o Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="a2b98-128">Describes the relationship between Bluetooth and Windows Sockets.</span></span> |
| [<span data-ttu-id="a2b98-129">Gerenciando dispositivos e serviços Bluetooth</span><span class="sxs-lookup"><span data-stu-id="a2b98-129">Managing Bluetooth Devices and Services</span></span>](managing-bluetooth-devices-and-services.md) | <span data-ttu-id="a2b98-130">Descreve como gerenciar dispositivos e serviços Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="a2b98-130">Describes how to manage Bluetooth devices and services.</span></span>           |



 

 

 




