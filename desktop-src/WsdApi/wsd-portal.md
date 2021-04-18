---
description: A API do Microsoft Web Services on Devices (WSDAPI) dá suporte à implementação de dispositivos e serviços controlados pelo cliente e aos hosts de dispositivo em conformidade com o perfil de dispositivos para serviços Web (DPWS).
ms.assetid: 590e0b0b-763c-44fb-a49f-606415f57b26
title: Serviços Web em dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d8b5812983e7102093234458c94b475bb6a503
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763518"
---
# <a name="web-services-on-devices"></a><span data-ttu-id="9736b-103">Serviços Web em dispositivos</span><span class="sxs-lookup"><span data-stu-id="9736b-103">Web Services on Devices</span></span>

## <a name="purpose"></a><span data-ttu-id="9736b-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="9736b-104">Purpose</span></span>

<span data-ttu-id="9736b-105">A API do Microsoft Web Services on Devices (WSDAPI) dá suporte à implementação de dispositivos e serviços controlados pelo cliente e aos hosts de dispositivo em conformidade com o [perfil de dispositivos para serviços Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span><span class="sxs-lookup"><span data-stu-id="9736b-105">The Microsoft Web Services on Devices API (WSDAPI) supports the implementation of client-controlled devices and services, and device hosts conforming to the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="9736b-106">O WSDAPI usa o [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) para descoberta de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9736b-106">WSDAPI uses [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) for device discovery.</span></span>

<span data-ttu-id="9736b-107">O WSDAPI pode ser usado para o desenvolvimento de implementações de cliente e serviço.</span><span class="sxs-lookup"><span data-stu-id="9736b-107">WSDAPI may be used for the development of both client and service implementations.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="9736b-108">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="9736b-108">Where applicable</span></span>

<span data-ttu-id="9736b-109">Os serviços Web em dispositivos permitem que um cliente descubra e acesse um dispositivo remoto e seus serviços associados em uma rede.</span><span class="sxs-lookup"><span data-stu-id="9736b-109">Web Services on Devices allows a client to discover and access a remote device and its associated services across a network.</span></span> <span data-ttu-id="9736b-110">Ele dá suporte à descoberta, descrição, controle e eventos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9736b-110">It supports device discovery, description, control, and eventing.</span></span> <span data-ttu-id="9736b-111">Os desenvolvedores podem criar proxies de cliente WSDAPI e stubs correspondentes para hosts de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9736b-111">Developers can create WSDAPI client proxies and corresponding stubs for device hosts.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="9736b-112">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="9736b-112">Developer audience</span></span>

<span data-ttu-id="9736b-113">A documentação de serviços da Web em dispositivos é destinada a programadores C/C++ e fornecedores de dispositivos que criam produtos compatíveis com DPWS.</span><span class="sxs-lookup"><span data-stu-id="9736b-113">The Web Services on Devices documentation is intended for C/C++ programmers and device vendors creating DPWS-compliant products.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="9736b-114">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="9736b-114">Run-time requirements</span></span>

<span data-ttu-id="9736b-115">Os aplicativos cliente que usam WSDAPI têm suporte a partir do Windows Vista e do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="9736b-115">Client applications that use WSDAPI are supported starting with Windows Vista and Windows Server 2008.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9736b-116">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="9736b-116">In this section</span></span>



| <span data-ttu-id="9736b-117">Tópico</span><span class="sxs-lookup"><span data-stu-id="9736b-117">Topic</span></span>                                                                                  | <span data-ttu-id="9736b-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="9736b-118">Description</span></span>                                                                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9736b-119">Sobre os serviços Web em dispositivos</span><span class="sxs-lookup"><span data-stu-id="9736b-119">About Web Services on Devices</span></span>](about-web-services-for-devices.md)<br/>         | <span data-ttu-id="9736b-120">Arquitetura e informações gerais sobre os serviços da Web em dispositivos.</span><span class="sxs-lookup"><span data-stu-id="9736b-120">Architectural and general information about Web Services on Devices.</span></span><br/>              |
| [<span data-ttu-id="9736b-121">Usando serviços Web em dispositivos</span><span class="sxs-lookup"><span data-stu-id="9736b-121">Using Web Services on Devices</span></span>](using-web-services-on-devices.md)<br/>          | <span data-ttu-id="9736b-122">Informações sobre como gerar código, configurar aplicativos e solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="9736b-122">Information about generating code, configuring applications, and troubleshooting.</span></span><br/> |
| [<span data-ttu-id="9736b-123">Referência de serviços Web em dispositivos</span><span class="sxs-lookup"><span data-stu-id="9736b-123">Web Services on Devices Reference</span></span>](web-services-for-devices-reference.md)<br/> | <span data-ttu-id="9736b-124">Documentação de referência para os serviços Web na API de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="9736b-124">Reference documentation for the Web Services on Devices API.</span></span><br/>                      |



 

## <a name="related-topics"></a><span data-ttu-id="9736b-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9736b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9736b-126">Blog de Dan Driscoll</span><span class="sxs-lookup"><span data-stu-id="9736b-126">Dan Driscoll's Blog</span></span>](/archive/blogs/dandris/)
</dt> </dl>

 

