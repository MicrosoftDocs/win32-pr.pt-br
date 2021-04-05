---
title: APIs de UPnP
description: A estrutura UPnP permite a rede dinâmica de dispositivos inteligentes, computadores sem fio e PCs.
ms.assetid: 1dc05d6e-19ae-45e2-82c2-d3b63b16bf9d
keywords:
- UPnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022ede01a62230194969d7789e0ace70f960debb
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104084975"
---
# <a name="upnp-apis"></a><span data-ttu-id="c5f34-104">APIs de UPnP</span><span class="sxs-lookup"><span data-stu-id="c5f34-104">UPnP APIs</span></span>

## <a name="purpose"></a><span data-ttu-id="c5f34-105">Finalidade</span><span class="sxs-lookup"><span data-stu-id="c5f34-105">Purpose</span></span>

<span data-ttu-id="c5f34-106">A estrutura UPnP permite a rede dinâmica de dispositivos inteligentes, computadores sem fio e PCs.</span><span class="sxs-lookup"><span data-stu-id="c5f34-106">The UPnP  framework enables dynamic networking of intelligent appliances, wireless devices, and PCs.</span></span> <span data-ttu-id="c5f34-107">Há duas APIs para trabalhar com dispositivos certificados para UPnP:</span><span class="sxs-lookup"><span data-stu-id="c5f34-107">There are two APIs for working with UPnP-certified devices:</span></span>

-   <span data-ttu-id="c5f34-108">A API do ponto de controle, que consiste em um conjunto de interfaces COM usadas para localizar e controlar dispositivos.</span><span class="sxs-lookup"><span data-stu-id="c5f34-108">The Control Point API, which consists of a set of COM interfaces used to find and control devices.</span></span>
-   <span data-ttu-id="c5f34-109">A API de host do dispositivo, que consiste em um conjunto de interfaces COM usadas para implementar dispositivos hospedados por um computador.</span><span class="sxs-lookup"><span data-stu-id="c5f34-109">The Device Host API, which consists of a set of COM interfaces used to implement devices that are hosted by a computer.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="c5f34-110">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="c5f34-110">Where applicable</span></span>

<span data-ttu-id="c5f34-111">A API do ponto de controle permite que os desenvolvedores gravem aplicativos que pesquisam e controlam dispositivos com certificação UPnP.</span><span class="sxs-lookup"><span data-stu-id="c5f34-111">The Control Point API enables developers to write applications that search for and control UPnP-certified devices.</span></span> <span data-ttu-id="c5f34-112">A API de host do dispositivo permite que os desenvolvedores implementem a funcionalidade de dispositivos certificados por UPnP e usem o host do dispositivo para gerenciar as funções de descoberta, descrição, controle, apresentação e eventos de um dispositivo certificado por UPnP.</span><span class="sxs-lookup"><span data-stu-id="c5f34-112">The Device Host API enables developers to implement the functionality of UPnP-certified devices, and use the device host to manage the discovery, description, control, presentation, and eventing functions of a UPnP-certified device.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="c5f34-113">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="c5f34-113">Developer audience</span></span>

<span data-ttu-id="c5f34-114">Os desenvolvedores que usam as APIs do ponto de controle e as APIs de host do dispositivo devem estar familiarizados com a arquitetura do dispositivo UPnP.</span><span class="sxs-lookup"><span data-stu-id="c5f34-114">Developers using the Control Point APIs and Device Host APIs must be familiar with the UPnP device architecture.</span></span> <span data-ttu-id="c5f34-115">Para obter mais informações, consulte a [documentação de implementação de UPnP](https://openconnectivity.org/resources/upnpresources.zip) e o [Fórum UPnP](https://openconnectivity.org/).</span><span class="sxs-lookup"><span data-stu-id="c5f34-115">For more information, see the [UPnP Implementation Documentation](https://openconnectivity.org/resources/upnpresources.zip) and the [UPnP Forum](https://openconnectivity.org/).</span></span>

<span data-ttu-id="c5f34-116">Os desenvolvedores que estão usando as APIs de host do dispositivo devem estar familiarizados com as interfaces de Active Template Library (ATL) e COM.</span><span class="sxs-lookup"><span data-stu-id="c5f34-116">Developers who are using the Device Host APIs should be familiar with the Active Template Library (ATL) and COM interfaces.</span></span>

<span data-ttu-id="c5f34-117">As APIs do ponto de controle e as APIs de host do dispositivo são usadas por uma variedade de aplicativos, desde scripts inseridos em páginas HTML até programas completos de C++ e Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c5f34-117">The Control Point APIs and Device Host APIs are used by a variety of applications, from scripts embedded in HTML pages to full-fledged C++ and Microsoft Visual Basic programs.</span></span>

<span data-ttu-id="c5f34-118">Somente a API do ponto de controle dá suporte a Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="c5f34-118">Only the Control Point API supports Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="c5f34-119">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="c5f34-119">Run-time requirements</span></span>

<span data-ttu-id="c5f34-120">A API do ponto de controle é usada em computadores que executam o Microsoft Windows Millennium Edition, o Windows XP, o Windows XP Professional e o Windows CE .NET.</span><span class="sxs-lookup"><span data-stu-id="c5f34-120">The Control Point API is used on computers running Microsoft Windows Millennium Edition, Windows XP, Windows XP Professional, and Windows CE .NET.</span></span>

<span data-ttu-id="c5f34-121">A API de host do dispositivo é usada em computadores que executam o Windows XP, o Windows XP Professional e o Windows CE .NET.</span><span class="sxs-lookup"><span data-stu-id="c5f34-121">The Device Host API is used on computers running Windows XP, Windows XP Professional, and Windows CE .NET.</span></span>

<span data-ttu-id="c5f34-122">Para obter informações mais específicas sobre quais sistemas operacionais dão suporte a uma função específica, consulte "requisitos" na documentação.</span><span class="sxs-lookup"><span data-stu-id="c5f34-122">For more specific information about which operating systems support a particular function, refer to "Requirements" in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c5f34-123">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="c5f34-123">In this section</span></span>



| <span data-ttu-id="c5f34-124">Tópico</span><span class="sxs-lookup"><span data-stu-id="c5f34-124">Topic</span></span>                                                                                          | <span data-ttu-id="c5f34-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5f34-125">Description</span></span>                                                                                        |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5f34-126">Visão geral da arquitetura UPnP</span><span class="sxs-lookup"><span data-stu-id="c5f34-126">Overview of UPnP Architecture</span></span>](overview-of-universal-plug-and-play.md)<br/>            | <span data-ttu-id="c5f34-127">Informações gerais e plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="c5f34-127">General information and background.</span></span><br/>                                                     |
| [<span data-ttu-id="c5f34-128">Visão geral do ponto de controle</span><span class="sxs-lookup"><span data-stu-id="c5f34-128">Control Point Overview</span></span>](control-point-api.md)<br/>                                     | <span data-ttu-id="c5f34-129">Informações gerais sobre a API do ponto de controle.</span><span class="sxs-lookup"><span data-stu-id="c5f34-129">General information about the Control Point API.</span></span><br/>                                        |
| [<span data-ttu-id="c5f34-130">Usando a API do ponto de controle</span><span class="sxs-lookup"><span data-stu-id="c5f34-130">Using the Control Point API</span></span>](using-the-control-point-api-with-upnp-technology.md)<br/> | <span data-ttu-id="c5f34-131">Código de exemplo que mostra como desenvolver aplicativos que controlam dispositivos certificados por UPnP.</span><span class="sxs-lookup"><span data-stu-id="c5f34-131">Sample code that shows how to develop applications that control UPnP-certified devices.</span></span><br/> |
| [<span data-ttu-id="c5f34-132">Referência de API de ponto de controle</span><span class="sxs-lookup"><span data-stu-id="c5f34-132">Control Point API Reference</span></span>](control-point-api-with-upnp-technology-reference.md)<br/> | <span data-ttu-id="c5f34-133">Documentação de interfaces de componente de ponto de controle, métodos e eventos.</span><span class="sxs-lookup"><span data-stu-id="c5f34-133">Documentation of Control Point component interfaces, methods, and events.</span></span><br/>               |
| [<span data-ttu-id="c5f34-134">Visão geral da API de host do dispositivo</span><span class="sxs-lookup"><span data-stu-id="c5f34-134">Device Host API Overview</span></span>](device-host-api.md)<br/>                                     | <span data-ttu-id="c5f34-135">Informações gerais sobre a API de host do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c5f34-135">General information about the Device Host API.</span></span><br/>                                          |
| [<span data-ttu-id="c5f34-136">Usando a API de host do dispositivo</span><span class="sxs-lookup"><span data-stu-id="c5f34-136">Using the Device Host API</span></span>](using-the-device-host-api-with-upnp-technology.md)<br/>     | <span data-ttu-id="c5f34-137">Código de exemplo que mostra como desenvolver um aplicativo para dispositivos certificados por UPnP.</span><span class="sxs-lookup"><span data-stu-id="c5f34-137">Sample code that shows how to develop an application for UPnP-certified devices.</span></span><br/>        |
| [<span data-ttu-id="c5f34-138">Referência da API do host do dispositivo</span><span class="sxs-lookup"><span data-stu-id="c5f34-138">Device Host API Reference</span></span>](device-host-api-with-upnp-technology-reference.md)<br/>     | <span data-ttu-id="c5f34-139">Documentação de interfaces, métodos e eventos do componente de host do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c5f34-139">Documentation of Device Host component interfaces, methods, and events.</span></span><br/>                 |



 

 

 





