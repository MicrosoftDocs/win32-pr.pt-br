---
description: O Windows Sockets 2 (Winsock) permite que os programadores criem aplicativos avançados de Internet, intranet e outros com capacidade de rede para transmitir dados de aplicativos pela conexão, independentemente do protocolo de rede que está sendo usado.
ms.assetid: 1ec8758a-40fd-4c98-b839-c2409ef712d6
title: Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df253572d2fca117dbc8b45b451f8c3bacc2f360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091001"
---
# <a name="windows-sockets-2"></a><span data-ttu-id="120de-103">Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="120de-103">Windows Sockets 2</span></span>

## <a name="purpose"></a><span data-ttu-id="120de-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="120de-104">Purpose</span></span>

<span data-ttu-id="120de-105">O Windows Sockets 2 (Winsock) permite que os programadores criem aplicativos avançados de Internet, intranet e outros com capacidade de rede para transmitir dados de aplicativos pela conexão, independentemente do protocolo de rede que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="120de-105">Windows Sockets 2 (Winsock) enables programmers to create advanced Internet, intranet, and other network-capable applications to transmit application data across the wire, independent of the network protocol being used.</span></span> <span data-ttu-id="120de-106">Com o Winsock, os programadores recebem acesso a recursos de rede avançados do Microsoft® Windows®, como multicast e QoS (qualidade de serviço).</span><span class="sxs-lookup"><span data-stu-id="120de-106">With Winsock, programmers are provided access to advanced Microsoft® Windows® networking capabilities such as multicast and Quality of Service (QoS).</span></span>

<span data-ttu-id="120de-107">O Winsock segue o modelo de arquitetura do sistema aberto do Windows (WOSA); Ele define uma SPI (interface de provedor de serviços) padrão entre a API (interface de programação de aplicativo), com suas funções exportadas e as pilhas de protocolo.</span><span class="sxs-lookup"><span data-stu-id="120de-107">Winsock follows the Windows Open System Architecture (WOSA) model; it defines a standard service provider interface (SPI) between the application programming interface (API), with its exported functions and the protocol stacks.</span></span> <span data-ttu-id="120de-108">Ele usa o paradigma de soquetes que foi mais popular pela Berkeley Software Distribution (BSD) UNIX.</span><span class="sxs-lookup"><span data-stu-id="120de-108">It uses the sockets paradigm that was first popularized by Berkeley Software Distribution (BSD) UNIX.</span></span> <span data-ttu-id="120de-109">Ele foi adaptado posteriormente para Windows no Windows Sockets 1,1, com o qual os aplicativos do Windows Sockets 2 são compatíveis com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="120de-109">It was later adapted for Windows in Windows Sockets 1.1, with which Windows Sockets 2 applications are backward compatible.</span></span> <span data-ttu-id="120de-110">Programação do Winsock centrada anteriormente em volta do TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="120de-110">Winsock programming previously centered around TCP/IP.</span></span> <span data-ttu-id="120de-111">Algumas práticas de programação que funcionaram com TCP/IP não funcionam com todos os protocolos.</span><span class="sxs-lookup"><span data-stu-id="120de-111">Some programming practices that worked with TCP/IP do not work with every protocol.</span></span> <span data-ttu-id="120de-112">Como resultado, a API do Windows Sockets 2 adiciona funções onde for necessário para lidar com vários protocolos.</span><span class="sxs-lookup"><span data-stu-id="120de-112">As a result, the Windows Sockets 2 API adds functions where necessary to handle several protocols.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="120de-113">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="120de-113">Developer audience</span></span>

<span data-ttu-id="120de-114">O Windows Sockets 2 foi projetado para ser usado por programadores C/C++.</span><span class="sxs-lookup"><span data-stu-id="120de-114">Windows Sockets 2 is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="120de-115">É necessário ter familiaridade com a rede do Windows.</span><span class="sxs-lookup"><span data-stu-id="120de-115">Familiarity with Windows networking is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="120de-116">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="120de-116">Run-time requirements</span></span>

<span data-ttu-id="120de-117">O Windows Sockets 2 pode ser usado em todas as plataformas Windows.</span><span class="sxs-lookup"><span data-stu-id="120de-117">Windows Sockets 2 can be used on all Windows platforms.</span></span> <span data-ttu-id="120de-118">Quando determinadas implementações ou recursos de restrições de plataforma do Windows Sockets 2 existem, eles são claramente indicados na documentação.</span><span class="sxs-lookup"><span data-stu-id="120de-118">Where certain implementations or capabilities of Windows Sockets 2 platform restrictions do exist, they are clearly noted in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="120de-119">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="120de-119">In this section</span></span>



| <span data-ttu-id="120de-120">Tópico</span><span class="sxs-lookup"><span data-stu-id="120de-120">Topic</span></span>                                                                                             | <span data-ttu-id="120de-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="120de-121">Description</span></span>                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="120de-122">Novidades para Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="120de-122">What's New for Windows Sockets</span></span>](what-s-new-for-windows-sockets-2.md)<br/>                 | <span data-ttu-id="120de-123">Informações sobre os novos recursos do Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="120de-123">Information on new features for Windows Sockets.</span></span><br/>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="120de-124">Suporte ao protocolo de rede Winsock no Windows</span><span class="sxs-lookup"><span data-stu-id="120de-124">Winsock Network Protocol Support in Windows</span></span>](network-protocol-support-in-windows.md)<br/> | <span data-ttu-id="120de-125">Informações sobre o suporte de protocolo de rede para Windows Sockets em diferentes versões do Windows.</span><span class="sxs-lookup"><span data-stu-id="120de-125">Information on network protocol support for Windows Sockets on different versions of Windows.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="120de-126">Sobre o Winsock</span><span class="sxs-lookup"><span data-stu-id="120de-126">About Winsock</span></span>](about-winsock.md)<br/>                                                     | <span data-ttu-id="120de-127">Informações gerais sobre considerações, arquitetura e recursos de programação do Windows Sockets disponíveis para desenvolvedores.</span><span class="sxs-lookup"><span data-stu-id="120de-127">General information on Windows Sockets programming considerations, architecture, and capabilities available to developers.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="120de-128">Usando o Winsock</span><span class="sxs-lookup"><span data-stu-id="120de-128">Using Winsock</span></span>](using-winsock.md)<br/>                                                     | <span data-ttu-id="120de-129">Procedimentos e técnicas de programação usados com o Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="120de-129">Procedures and programming techniques used with Windows Sockets.</span></span> <span data-ttu-id="120de-130">Esta seção inclui técnicas básicas de programação do Winsock, como [introdução com o Winsock](getting-started-with-winsock.md), bem como técnicas avançadas úteis para desenvolvedores de Winsock experientes.</span><span class="sxs-lookup"><span data-stu-id="120de-130">This section includes basic Winsock programming techniques, such as [Getting Started With Winsock](getting-started-with-winsock.md), as well as advanced techniques useful for experienced Winsock developers.</span></span><br/> |
| [<span data-ttu-id="120de-131">Referência do Winsock</span><span class="sxs-lookup"><span data-stu-id="120de-131">Winsock Reference</span></span>](winsock-reference.md)<br/>                                             | <span data-ttu-id="120de-132">Documentação da API do Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="120de-132">Documentation of the Windows Sockets API.</span></span><br/>                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="120de-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="120de-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="120de-134">Auxiliar de IP</span><span class="sxs-lookup"><span data-stu-id="120de-134">IP Helper</span></span>](../iphlp/ip-helper-start-page.md)
</dt> <dt>

[<span data-ttu-id="120de-135">Qualidade de Serviço</span><span class="sxs-lookup"><span data-stu-id="120de-135">Quality of Service</span></span>](/previous-versions/windows/desktop/qos/qos-start-page)
</dt> </dl>

 

 
