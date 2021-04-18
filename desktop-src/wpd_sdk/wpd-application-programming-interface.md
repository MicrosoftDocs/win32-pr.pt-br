---
description: Interface de programação de aplicativo WPD
ms.assetid: 3e2be15f-7af7-4e76-89b1-f9bc591c4f1b
title: Interface de programação de aplicativo WPD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c44dbcf731aa46941599b99766e52fa67a5c5a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791310"
---
# <a name="wpd-application-programming-interface"></a><span data-ttu-id="b31d0-103">Interface de programação de aplicativo WPD</span><span class="sxs-lookup"><span data-stu-id="b31d0-103">WPD Application Programming Interface</span></span>

<span data-ttu-id="b31d0-104">Aplicativos criados em dispositivos portáteis do Windows podem explorar um dispositivo, enviar e receber conteúdo e até mesmo controlar o dispositivo, por exemplo, tirar uma foto ou enviar uma mensagem de texto.</span><span class="sxs-lookup"><span data-stu-id="b31d0-104">Applications built on Windows Portable Devices can explore a device, send and receive content, and even control the device, for example, take a picture or send a text message.</span></span> <span data-ttu-id="b31d0-105">O sistema foi projetado para ser flexível, de modo que muitos tipos de dispositivos possam ser explorados e extensíveis para que os desenvolvedores de driver possam definir propriedades e comandos personalizados para dispositivos personalizados.</span><span class="sxs-lookup"><span data-stu-id="b31d0-105">The system is designed to be flexible so that many types of devices can be explored, and extensible so that driver developers can define custom properties and commands for custom devices.</span></span>

<span data-ttu-id="b31d0-106">A tabela a seguir descreve os principais tópicos desta documentação.</span><span class="sxs-lookup"><span data-stu-id="b31d0-106">The following table describes the main topics of this documentation.</span></span>



| <span data-ttu-id="b31d0-107">Tópico</span><span class="sxs-lookup"><span data-stu-id="b31d0-107">Topic</span></span>                                                                                                                  | <span data-ttu-id="b31d0-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b31d0-108">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b31d0-109">Requisitos gerais para o desenvolvimento de aplicativos</span><span class="sxs-lookup"><span data-stu-id="b31d0-109">General Requirements for Application Development</span></span>](general-requirements-for-application-development.md)               | <span data-ttu-id="b31d0-110">Requisitos de hardware e software para desenvolver drivers e aplicativos usando dispositivos portáteis do Windows.</span><span class="sxs-lookup"><span data-stu-id="b31d0-110">Hardware and software requirements to develop drivers and applications using Windows Portable Devices.</span></span>     |
| [<span data-ttu-id="b31d0-111">Requisitos para aplicativos do Windows Media DRM-Enabled</span><span class="sxs-lookup"><span data-stu-id="b31d0-111">Requirements for Windows Media DRM-Enabled Applications</span></span>](requirements-for-windows-media-drm-enabled-applications.md) | <span data-ttu-id="b31d0-112">Propriedades que são necessárias para habilitar transferências de conteúdo protegidas por DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b31d0-112">Properties that are required to enable Windows Media DRM-protected content transfers.</span></span>                      |
| [<span data-ttu-id="b31d0-113">Amostras</span><span class="sxs-lookup"><span data-stu-id="b31d0-113">Samples</span></span>](sample.md)                                                                                                  | <span data-ttu-id="b31d0-114">Descrição de dois aplicativos de área de trabalho de linha de comando que são fornecidos com essa Software Development Kit.</span><span class="sxs-lookup"><span data-stu-id="b31d0-114">Description of two command-line desktop applications that are supplied with this software development kit.</span></span> |
| [<span data-ttu-id="b31d0-115">Visão geral do aplicativo</span><span class="sxs-lookup"><span data-stu-id="b31d0-115">Application Overview</span></span>](application-overview.md)                                                                       | <span data-ttu-id="b31d0-116">Conceitos principais usados em dispositivos portáteis do Windows.</span><span class="sxs-lookup"><span data-stu-id="b31d0-116">Key concepts used in Windows Portable Devices.</span></span>                                                             |
| [<span data-ttu-id="b31d0-117">Guia de programação</span><span class="sxs-lookup"><span data-stu-id="b31d0-117">Programming Guide</span></span>](programming-guide.md)                                                                             | <span data-ttu-id="b31d0-118">As principais tarefas que um aplicativo executará com instruções passo a passo e trechos de código.</span><span class="sxs-lookup"><span data-stu-id="b31d0-118">Key tasks that an application will perform, with step-by-step instructions and code snippets.</span></span>              |
| [<span data-ttu-id="b31d0-119">Referência de programação</span><span class="sxs-lookup"><span data-stu-id="b31d0-119">Programming Reference</span></span>](programming-reference.md)                                                                     | <span data-ttu-id="b31d0-120">Guia de referência para as interfaces e os tipos de dados definidos por dispositivos portáteis do Windows.</span><span class="sxs-lookup"><span data-stu-id="b31d0-120">Reference guide to the interfaces and data types defined by Windows Portable Devices.</span></span>                      |



 

<span data-ttu-id="b31d0-121">Aplicativos criados no Windows Media Gerenciador de Dispositivos ou aquisição de imagem do Windows podem acessar dispositivos portáteis do Windows por meio de uma camada de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="b31d0-121">Applications built on Windows Media Device Manager or Windows Image Acquisition can access Windows Portable Devices through a compatibility layer.</span></span>

<span data-ttu-id="b31d0-122">A Microsoft fornece vários drivers para protocolos e dispositivos padrão, incluindo dispositivos MTP (protocolo de transporte de mídia) e dispositivos MSC (classe de armazenamento em massa).</span><span class="sxs-lookup"><span data-stu-id="b31d0-122">Microsoft provides several drivers for standard protocols and devices, including Media Transport Protocol (MTP) devices and Mass Storage Class (MSC) devices.</span></span> <span data-ttu-id="b31d0-123">Se você estiver familiarizado com a estrutura de driver User-Mode, poderá desenvolver seus próprios drivers para dispositivos personalizados.</span><span class="sxs-lookup"><span data-stu-id="b31d0-123">If you are familiar with the User-Mode Driver Framework, you can develop your own drivers for custom devices.</span></span>

 

 



