---
title: Acesso remoto
description: Use o serviço de acesso remoto (RAS) para criar aplicativos cliente.
ms.assetid: 4e6c04d4-f989-4248-901f-ec15f61582da
keywords:
- RAS do serviço de acesso remoto
- RAS RAS
- RAS do serviço de acesso remoto, página inicial
- RAS do RAS, consulte acesso remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a4b1c06656b51395c8c4fc666e59d6115bd839
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104084372"
---
# <a name="remote-access"></a><span data-ttu-id="5724e-107">Acesso remoto</span><span class="sxs-lookup"><span data-stu-id="5724e-107">Remote Access</span></span>

## <a name="purpose"></a><span data-ttu-id="5724e-108">Finalidade</span><span class="sxs-lookup"><span data-stu-id="5724e-108">Purpose</span></span>

<span data-ttu-id="5724e-109">Use o serviço de acesso remoto (RAS) para criar aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="5724e-109">Use Remote Access Service (RAS) to create client applications.</span></span> <span data-ttu-id="5724e-110">Esses aplicativos exibem caixas de diálogo comuns de RAS, gerenciam dispositivos e conexões de acesso remoto e manipulam entradas de catálogo telefônico.</span><span class="sxs-lookup"><span data-stu-id="5724e-110">These applications display RAS common dialog boxes, manage remote access connections and devices, and manipulate phone-book entries.</span></span> <span data-ttu-id="5724e-111">O RAS também fornece a próxima geração de funcionalidade de servidor para o RAS (serviço de acesso remoto) para Windows.</span><span class="sxs-lookup"><span data-stu-id="5724e-111">RAS also provides the next generation of server functionality for the Remote Access Service (RAS) for Windows.</span></span> <span data-ttu-id="5724e-112">A funcionalidade de servidor RRAS segue e se baseia no serviço de acesso remoto (RAS).</span><span class="sxs-lookup"><span data-stu-id="5724e-112">The RRAS server functionality follows and builds upon the Remote Access Service (RAS).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="5724e-113">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="5724e-113">Where applicable</span></span>

<span data-ttu-id="5724e-114">O serviço de acesso remoto é aplicável em qualquer ambiente computacional que usa um link WAN (rede de longa distância) ou uma VPN (rede virtual privada).</span><span class="sxs-lookup"><span data-stu-id="5724e-114">The Remote Access Service is applicable in any computing environment that uses a Wide Area Network (WAN) link or a Virtual Private Network (VPN).</span></span> <span data-ttu-id="5724e-115">O RAS torna possível conectar um computador cliente remoto a um servidor de rede por meio de um link WAN ou VPN.</span><span class="sxs-lookup"><span data-stu-id="5724e-115">RAS makes it possible to connect a remote client computer to a network server over a WAN link or a VPN.</span></span> <span data-ttu-id="5724e-116">O computador remoto, em seguida, funciona na LAN do servidor como se o computador remoto estivesse conectado diretamente à LAN.</span><span class="sxs-lookup"><span data-stu-id="5724e-116">The remote computer then functions on the server's LAN as though the remote computer was connected to the LAN directly.</span></span> <span data-ttu-id="5724e-117">A API RAS permite que os programadores acessem os recursos do RAS de forma programática.</span><span class="sxs-lookup"><span data-stu-id="5724e-117">The RAS API enables programmers to access the features of RAS programmatically.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="5724e-118">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="5724e-118">Developer audience</span></span>

<span data-ttu-id="5724e-119">A API de RAS foi projetada para uso por programadores C/C++.</span><span class="sxs-lookup"><span data-stu-id="5724e-119">The RAS API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="5724e-120">Os programadores do Microsoft Visual Basic também podem encontrar a API útil.</span><span class="sxs-lookup"><span data-stu-id="5724e-120">Microsoft Visual Basic programmers may also find the API useful.</span></span> <span data-ttu-id="5724e-121">Os programadores devem estar familiarizados com os conceitos de rede.</span><span class="sxs-lookup"><span data-stu-id="5724e-121">Programmers should be familiar with networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="5724e-122">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="5724e-122">Run-time requirements</span></span>

<span data-ttu-id="5724e-123">Algumas das funções na API RAS têm suporte apenas em servidores de rede e outras funções têm suporte apenas em clientes de rede.</span><span class="sxs-lookup"><span data-stu-id="5724e-123">Some of the functions in the RAS API are supported only on network servers and other functions are supported only on network clients.</span></span> <span data-ttu-id="5724e-124">Para obter informações mais específicas sobre quais sistemas operacionais dão suporte a uma função específica, consulte as seções de requisitos na documentação do.</span><span class="sxs-lookup"><span data-stu-id="5724e-124">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

<span data-ttu-id="5724e-125">A [funcionalidade avançada de Ras](function-comparison-windows-2000-versus-rras-redistributable.md) do RRAS está disponível para o Windows NT Server 4,0 Instalando o [RRAS redistribuível](https://www.microsoft.com/ntserver/nts/downloads/winfeatures/rras/rrasdown.asp).</span><span class="sxs-lookup"><span data-stu-id="5724e-125">The [enhanced RAS functionality](function-comparison-windows-2000-versus-rras-redistributable.md) of RRAS is available for Windows NT Server 4.0 by installing the [RRAS redistributable](https://www.microsoft.com/ntserver/nts/downloads/winfeatures/rras/rrasdown.asp).</span></span> <span data-ttu-id="5724e-126">Toda a funcionalidade do RRAS é incorporada ao Windows 2000 Server, ao Windows Server 2003 e ao Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="5724e-126">All the functionality of RRAS is incorporated into Windows 2000 Server, Windows Server 2003, and Windows Server 2008.</span></span> <span data-ttu-id="5724e-127">Os aplicativos RRAS não podem ser executados no Windows NT Workstation 4,0 ou em sistemas operacionais cliente, como o Windows 95.</span><span class="sxs-lookup"><span data-stu-id="5724e-127">RRAS applications cannot run on Windows NT Workstation 4.0 or on client operating systems, such as Windows 95.</span></span> <span data-ttu-id="5724e-128">Para obter informações mais específicas sobre quais sistemas operacionais dão suporte a uma função específica, consulte as seções de requisitos na documentação do.</span><span class="sxs-lookup"><span data-stu-id="5724e-128">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5724e-129">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="5724e-129">In this section</span></span>



| <span data-ttu-id="5724e-130">Tópico</span><span class="sxs-lookup"><span data-stu-id="5724e-130">Topic</span></span>                                                                                             | <span data-ttu-id="5724e-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="5724e-131">Description</span></span>                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5724e-132">Serviço de acesso remoto</span><span class="sxs-lookup"><span data-stu-id="5724e-132">Remote Access Service</span></span>](about-remote-access-service.md)<br/>                               | <span data-ttu-id="5724e-133">O RAS (serviço de acesso remoto) fornece recursos de acesso remoto a aplicativos cliente em computadores que executam o Windows.</span><span class="sxs-lookup"><span data-stu-id="5724e-133">Remote Access Service (RAS) provides remote access capabilities to client applications on computers running Windows.</span></span><br/>                                                                                          |
| [<span data-ttu-id="5724e-134">Administração do serviço de acesso remoto</span><span class="sxs-lookup"><span data-stu-id="5724e-134">Remote Access Service Administration</span></span>](about-remote-access-service-administration.md)<br/> | <span data-ttu-id="5724e-135">A administração do serviço de acesso remoto fornece um conjunto de funções para administrar permissões e portas de usuário em servidores RAS.</span><span class="sxs-lookup"><span data-stu-id="5724e-135">Remote Access Service Administration provides a set of functions for administering user permissions and ports on RAS servers.</span></span> <span data-ttu-id="5724e-136">Usando essas funções, você pode desenvolver um aplicativo de administração de servidor RAS.</span><span class="sxs-lookup"><span data-stu-id="5724e-136">Using these functions, you can develop a RAS server administration application.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="5724e-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5724e-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5724e-138">Roteamento</span><span class="sxs-lookup"><span data-stu-id="5724e-138">Routing</span></span>](routing-start-page.md)
</dt> <dt>

[<span data-ttu-id="5724e-139">Protocolos de roteamento</span><span class="sxs-lookup"><span data-stu-id="5724e-139">Routing Protocols</span></span>](routing-protocols-start-page.md)
</dt> </dl>

 

 





