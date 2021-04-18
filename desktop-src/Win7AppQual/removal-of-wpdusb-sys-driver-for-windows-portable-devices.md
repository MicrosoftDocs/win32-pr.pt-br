---
description: .
ms.assetid: 3ad0c892-8b19-465d-af2f-9207f98e27b7
title: Remoção do driver de WPDUSB.SYS para dispositivos portáteis do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d602c8277a5c256332b3eaec6a383997d5c63d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791528"
---
# <a name="removal-of-wpdusbsys-driver-for-windows-portable-devices"></a><span data-ttu-id="c98aa-103">Remoção do driver de WPDUSB.SYS para dispositivos portáteis do Windows</span><span class="sxs-lookup"><span data-stu-id="c98aa-103">Removal of WPDUSB.SYS Driver for Windows Portable Devices</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="c98aa-104">Plataformas afetadas</span><span class="sxs-lookup"><span data-stu-id="c98aa-104">Affected Platforms</span></span>

<span data-ttu-id="c98aa-105">**Clientes** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="c98aa-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="c98aa-106">**Servidores** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c98aa-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="c98aa-107">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="c98aa-107">Feature Impact</span></span>

 <span data-ttu-id="c98aa-108">**Severidade** -baixa</span><span class="sxs-lookup"><span data-stu-id="c98aa-108">**Severity** - Low</span></span>  
<span data-ttu-id="c98aa-109">**Frequência** -baixa</span><span class="sxs-lookup"><span data-stu-id="c98aa-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="c98aa-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="c98aa-110">Description</span></span>

<span data-ttu-id="c98aa-111">A Microsoft substituiu o componente de modo kernel da pilha de drivers USB do Windows Vista (WPDUSB.SYS) para dispositivos portáteis do Windows (WPD) pelo driver WINUSB.SYS genérico.</span><span class="sxs-lookup"><span data-stu-id="c98aa-111">Microsoft has replaced the kernel mode component of the Windows Vista USB driver stack (WPDUSB.SYS) for Windows Portable Devices (WPD) with the generic WINUSB.SYS driver.</span></span> <span data-ttu-id="c98aa-112">A comunicação com o driver de WPDUSB.SYS original era por meio de códigos de controle de e/s privada (IOCTL); o suporte deles também foi removido.</span><span class="sxs-lookup"><span data-stu-id="c98aa-112">Communication with the original WPDUSB.SYS driver was via private I/O Control (IOCTL) codes; support of these has also been removed.</span></span>

<span data-ttu-id="c98aa-113">Qualquer consumidor desses códigos de IOCTL teria sido responsável por uma interpretação adequada e a implementação do MTP (protocolo de transferência de mídia).</span><span class="sxs-lookup"><span data-stu-id="c98aa-113">Any consumer of these IOCTL codes would have been responsible for proper interpretation and implementation of the Media Transfer Protocol (MTP).</span></span> <span data-ttu-id="c98aa-114">O Windows Vista não oferecia suporte ao uso desses códigos de IOCTL por aplicativos de terceiros.</span><span class="sxs-lookup"><span data-stu-id="c98aa-114">Windows Vista did not support use of these IOCTL codes by third-party applications.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="c98aa-115">Manifestação do impacto</span><span class="sxs-lookup"><span data-stu-id="c98aa-115">Manifestation of Impact</span></span>

<span data-ttu-id="c98aa-116">Qualquer aplicativo que dependa da disponibilidade desses códigos de IOCTL privado não teria mais acesso a dispositivos MTP conectados por USB.</span><span class="sxs-lookup"><span data-stu-id="c98aa-116">Any application that depended on the availability of these private IOCTL codes would no longer have access to USB-connected MTP devices.</span></span>

## <a name="mitigation"></a><span data-ttu-id="c98aa-117">Atenuação</span><span class="sxs-lookup"><span data-stu-id="c98aa-117">Mitigation</span></span>

<span data-ttu-id="c98aa-118">Os usuários de um aplicativo que depende dos códigos de IOCTL privados devem usar um aplicativo diferente (ou uma versão atualizada do aplicativo) para acessar o dispositivo MTP conectado por USB.</span><span class="sxs-lookup"><span data-stu-id="c98aa-118">Users of an application that depends on the private IOCTL codes must use a different application (or an updated version of the application) to access the USB-connected MTP device.</span></span>

## <a name="solution"></a><span data-ttu-id="c98aa-119">Solução</span><span class="sxs-lookup"><span data-stu-id="c98aa-119">Solution</span></span>

<span data-ttu-id="c98aa-120">Os aplicativos devem usar a API de dispositivos portáteis do Windows (WPD) para localizar e interagir com qualquer dispositivo WPD.</span><span class="sxs-lookup"><span data-stu-id="c98aa-120">Applications should use the Windows Portable Devices (WPD) API to find and interact with any WPD Device.</span></span> <span data-ttu-id="c98aa-121">Embora uma porcentagem significativa de dispositivos WPD implemente MTP para comunicação com o PC, o WPD não se limita apenas a dispositivos MTP.</span><span class="sxs-lookup"><span data-stu-id="c98aa-121">Although a significant percentage of WPD devices implement MTP for communication with the PC, WPD is not limited to just MTP devices.</span></span> <span data-ttu-id="c98aa-122">Além disso, em que o acesso direto ao dispositivo por meio de IOCTLs privados teria limitado o aplicativo de comunicação apenas com dispositivos conectados por USB, o uso da API WPD expande a lista de opções de conectividade para outros protocolos de comunicação (por exemplo, Wi-Fi).</span><span class="sxs-lookup"><span data-stu-id="c98aa-122">In addition, where direct access to the device via the private IOCTLs would have limited the application to communication with only USB-connected devices, use of the WPD API expands the list of connectivity options to other communication protocols (for example, Wi-Fi).</span></span> <span data-ttu-id="c98aa-123">Nos casos raros em que o aplicativo deve ser compatível com MTP, a API WPD fornece um mecanismo de passagem para comandos do MTP brutos.</span><span class="sxs-lookup"><span data-stu-id="c98aa-123">In the rare cases when the application must be MTP-aware, the WPD API provides a pass-through mechanism for raw MTP commands.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="c98aa-124">Aproveitando os recursos do recurso</span><span class="sxs-lookup"><span data-stu-id="c98aa-124">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="c98aa-125">A API WPD tem suporte no Windows XP (por meio do Windows Format SDK), do Windows Vista e do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c98aa-125">The WPD API is supported in Windows XP (via the Windows Format SDK), Windows Vista and Windows 7.</span></span> <span data-ttu-id="c98aa-126">A implementação do Windows 7 de WPD adiciona suporte para MTP em Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="c98aa-126">The Windows 7 implementation of WPD adds support for MTP over Bluetooth.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="c98aa-127">Links para outros recursos</span><span class="sxs-lookup"><span data-stu-id="c98aa-127">Links to Other Resources</span></span>

[<span data-ttu-id="c98aa-128">Dispositivos portáteis do Windows</span><span class="sxs-lookup"><span data-stu-id="c98aa-128">Windows Portable Devices</span></span>](../windows-portable-devices.md)

 

 
