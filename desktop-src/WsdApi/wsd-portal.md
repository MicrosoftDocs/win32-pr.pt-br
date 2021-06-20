---
description: Leia sobre como implementar serviços Web em dispositivos (WSD). Entenda sua finalidade, onde ela é aplicável, o público-alvo do desenvolvedor e os requisitos de tempo de run-time.
ms.assetid: 590e0b0b-763c-44fb-a49f-606415f57b26
title: Serviços Web em dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 267f8dba0fd56c383dd3cecabb3c00959aa0d90c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405749"
---
# <a name="web-services-on-devices"></a><span data-ttu-id="3ded4-104">Serviços Web em dispositivos</span><span class="sxs-lookup"><span data-stu-id="3ded4-104">Web Services on Devices</span></span>

## <a name="purpose"></a><span data-ttu-id="3ded4-105">Finalidade</span><span class="sxs-lookup"><span data-stu-id="3ded4-105">Purpose</span></span>

<span data-ttu-id="3ded4-106">A API WSDAPI (Serviços Web da Microsoft em Dispositivos) dá suporte à implementação de dispositivos e serviços controlados pelo cliente e hosts de dispositivo em conformidade com o DPWS (Perfil de Dispositivos para [Serviços Web).](https://specs.xmlsoap.org/ws/2006/02/devprof/)</span><span class="sxs-lookup"><span data-stu-id="3ded4-106">The Microsoft Web Services on Devices API (WSDAPI) supports the implementation of client-controlled devices and services, and device hosts conforming to the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="3ded4-107">O WSDAPI usa [o WS-Discovery para](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) descoberta de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="3ded4-107">WSDAPI uses [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) for device discovery.</span></span>

<span data-ttu-id="3ded4-108">O WSDAPI pode ser usado para o desenvolvimento de implementações de cliente e serviço.</span><span class="sxs-lookup"><span data-stu-id="3ded4-108">WSDAPI may be used for the development of both client and service implementations.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="3ded4-109">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="3ded4-109">Where applicable</span></span>

<span data-ttu-id="3ded4-110">Os Serviços Web em Dispositivos permitem que um cliente descubra e acesse um dispositivo remoto e seus serviços associados em uma rede.</span><span class="sxs-lookup"><span data-stu-id="3ded4-110">Web Services on Devices allows a client to discover and access a remote device and its associated services across a network.</span></span> <span data-ttu-id="3ded4-111">Ele dá suporte à descoberta, à descrição, ao controle e ao evento do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3ded4-111">It supports device discovery, description, control, and eventing.</span></span> <span data-ttu-id="3ded4-112">Os desenvolvedores podem criar proxies de cliente WSDAPI e stubs correspondentes para hosts de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3ded4-112">Developers can create WSDAPI client proxies and corresponding stubs for device hosts.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="3ded4-113">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="3ded4-113">Developer audience</span></span>

<span data-ttu-id="3ded4-114">A documentação serviços Web em dispositivos destina-se a programadores C/C++ e fornecedores de dispositivos que criam produtos compatíveis com DPWS.</span><span class="sxs-lookup"><span data-stu-id="3ded4-114">The Web Services on Devices documentation is intended for C/C++ programmers and device vendors creating DPWS-compliant products.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="3ded4-115">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="3ded4-115">Run-time requirements</span></span>

<span data-ttu-id="3ded4-116">Há suporte para aplicativos cliente que usam WSDAPI a partir do Windows Vista e do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3ded4-116">Client applications that use WSDAPI are supported starting with Windows Vista and Windows Server 2008.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3ded4-117">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="3ded4-117">In this section</span></span>



| <span data-ttu-id="3ded4-118">Tópico</span><span class="sxs-lookup"><span data-stu-id="3ded4-118">Topic</span></span>                                                                                  | <span data-ttu-id="3ded4-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ded4-119">Description</span></span>                                                                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ded4-120">Sobre serviços Web em dispositivos</span><span class="sxs-lookup"><span data-stu-id="3ded4-120">About Web Services on Devices</span></span>](about-web-services-for-devices.md)<br/>         | <span data-ttu-id="3ded4-121">Informações gerais e arquitetônicas sobre serviços Web em dispositivos.</span><span class="sxs-lookup"><span data-stu-id="3ded4-121">Architectural and general information about Web Services on Devices.</span></span><br/>              |
| [<span data-ttu-id="3ded4-122">Usando serviços Web em dispositivos</span><span class="sxs-lookup"><span data-stu-id="3ded4-122">Using Web Services on Devices</span></span>](using-web-services-on-devices.md)<br/>          | <span data-ttu-id="3ded4-123">Informações sobre como gerar código, configurar aplicativos e solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="3ded4-123">Information about generating code, configuring applications, and troubleshooting.</span></span><br/> |
| [<span data-ttu-id="3ded4-124">Referência de serviços Web em dispositivos</span><span class="sxs-lookup"><span data-stu-id="3ded4-124">Web Services on Devices Reference</span></span>](web-services-for-devices-reference.md)<br/> | <span data-ttu-id="3ded4-125">Documentação de referência para a API de Serviços Web em Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="3ded4-125">Reference documentation for the Web Services on Devices API.</span></span><br/>                      |



 

## <a name="related-topics"></a><span data-ttu-id="3ded4-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3ded4-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ded4-127">Blog de Dan Ltda</span><span class="sxs-lookup"><span data-stu-id="3ded4-127">Dan Driscoll's Blog</span></span>](/archive/blogs/dandris/)
</dt> </dl>

 

