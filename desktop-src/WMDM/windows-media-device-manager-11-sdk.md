---
title: SDK do Windows Media Gerenciador de Dispositivos 11
description: SDK do Windows Media Gerenciador de Dispositivos 11
ms.assetid: 9c0c9a96-1335-4ae2-9393-bfab0dfe24c6
keywords:
- Windows Media Gerenciador de Dispositivos, sobre
- Gerenciador de Dispositivos, sobre
- MTP (protocolo de transferência de mídia)
- MTP (protocolo de transferência de mídia)
- Classe de armazenamento em massa (MSC)
- MSC (classe de armazenamento em massa)
- Windows Media Gerenciador de Dispositivos, aplicativos de área de trabalho
- Gerenciador de Dispositivos, aplicativos de área de trabalho
- aplicativos de área de trabalho, sobre
- Windows Media Gerenciador de Dispositivos, provedores de serviços
- Gerenciador de Dispositivos, provedores de serviços
- provedores de serviço, sobre
- Gerenciador de Dispositivos de mídia do Windows, plug-ins
- Gerenciador de Dispositivos, plug-Insp
- plug-ins, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b167e8244fb6f03a584dfb71255eabfa359c8e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104366844"
---
# <a name="windows-media-device-manager-11-sdk"></a><span data-ttu-id="637f5-118">SDK do Windows Media Gerenciador de Dispositivos 11</span><span class="sxs-lookup"><span data-stu-id="637f5-118">Windows Media Device Manager 11 SDK</span></span>

> [!IMPORTANT]
> <span data-ttu-id="637f5-119">As APIs do Windows Media Gerenciador de Dispositivos agora estão incluídas no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="637f5-119">The Windows Media Device Manager APIs are now included in the Windows SDK.</span></span> <span data-ttu-id="637f5-120">Nenhum download adicional do SDK é necessário.</span><span class="sxs-lookup"><span data-stu-id="637f5-120">No additional SDK downloads are required.</span></span>

 

<span data-ttu-id="637f5-121">O SDK (Software Development Kit) do Microsoft Windows Media Gerenciador de Dispositivos permite que você crie aplicativos e componentes de área de trabalho que podem se comunicar com dispositivos portáteis conectados.</span><span class="sxs-lookup"><span data-stu-id="637f5-121">The Microsoft Windows Media Device Manager Software Development Kit (SDK) enables you to build desktop applications and components that can communicate with connected portable devices.</span></span> <span data-ttu-id="637f5-122">O Windows Media Gerenciador de Dispositivos permite que seu aplicativo ou componente enumere, explore e troque arquivos com um dispositivo, consulte metadados e solicite informações de contagem de reprodução.</span><span class="sxs-lookup"><span data-stu-id="637f5-122">Windows Media Device Manager enables your application or component to enumerate, explore, and exchange files with a device, query for metadata, and request play count information.</span></span> <span data-ttu-id="637f5-123">Aplicativos ou componentes criados no Windows Media Gerenciador de Dispositivos têm uma API consistente para se comunicar com uma ampla gama de dispositivos, incluindo o MTP (Media Transfer Protocol), o MSC (classe de armazenamento em massa), o RAPI e outros dispositivos criados nas versões mais recentes e anteriores da tecnologia Windows Media.</span><span class="sxs-lookup"><span data-stu-id="637f5-123">Applications or components built on Windows Media Device Manager have a consistent API for communicating with a wide range of devices including Media Transfer Protocol (MTP), Mass Storage Class (MSC), RAPI, and other devices built on both the latest and previous versions of Windows Media technology.</span></span>

<span data-ttu-id="637f5-124">Você pode criar os seguintes itens usando o SDK do Windows Media Gerenciador de Dispositivos:</span><span class="sxs-lookup"><span data-stu-id="637f5-124">You can build the following items using the Windows Media Device Manager SDK:</span></span>

-   <span data-ttu-id="637f5-125">Aplicativos de área de trabalho, como players de mídia personalizados.</span><span class="sxs-lookup"><span data-stu-id="637f5-125">Desktop applications, such as custom media players.</span></span> <span data-ttu-id="637f5-126">Toda a comunicação entre um aplicativo e um dispositivo portátil deve passar pelo Windows Media Gerenciador de Dispositivos, que atua como um agente entre o aplicativo, o sistema Microsoft Digital Rights Management e o provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="637f5-126">All communication between an application and a portable device must go through Windows Media Device Manager, which acts as a broker between the application, the Microsoft digital rights management system, and the service provider.</span></span>
-   <span data-ttu-id="637f5-127">Provedores de serviços, que atuam como o link de comunicação entre um dispositivo personalizado e um aplicativo de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="637f5-127">Service providers, which act as the communication link between a custom device and a desktop application.</span></span> <span data-ttu-id="637f5-128">Embora a Microsoft forneça vários provedores de serviços que podem se comunicar com a maioria dos dispositivos prontos para uso, você pode criar um provedor de serviços personalizado para personalizar a comunicação entre um dispositivo e um aplicativo de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="637f5-128">Although Microsoft provides a number of service providers that can communicate with most devices out of the box, you can build a custom service provider to customize the communication between a device and a desktop application.</span></span>
-   <span data-ttu-id="637f5-129">Plug-ins, que podem executar tarefas como solicitar e registrar contas de reprodução em dispositivos.</span><span class="sxs-lookup"><span data-stu-id="637f5-129">Plug-ins, which can perform tasks such as requesting and logging play counts on devices.</span></span> <span data-ttu-id="637f5-130">Esses plug-ins podem ser anexados a outros aplicativos de área de trabalho, como o Windows Media Player, para enviar informações aos provedores de conteúdo para lidar com pagamentos de royalties para artistas.</span><span class="sxs-lookup"><span data-stu-id="637f5-130">These plug-ins can be attached to other desktop applications, such as the Windows Media Player to send information to content providers to handle royalty payments to artists.</span></span>

<span data-ttu-id="637f5-131">Para baixar o SDK do Windows Media Gerenciador de Dispositivos, consulte [a página de download do Windows Media](https://msdn.microsoft.com/windows/desktop/aa904949) no site do MSDN.</span><span class="sxs-lookup"><span data-stu-id="637f5-131">To download the Windows Media Device Manager SDK, see [the Windows Media Download page](https://msdn.microsoft.com/windows/desktop/aa904949) on the MSDN Web site.</span></span>

<span data-ttu-id="637f5-132">Este SDK é um componente do Microsoft Windows Media Software Development Kit.</span><span class="sxs-lookup"><span data-stu-id="637f5-132">This SDK is a component of the Microsoft Windows Media Software Development Kit.</span></span> <span data-ttu-id="637f5-133">Outros componentes incluem o SDK do Windows Media Format, o SDK do Windows Media Services, o Windows Media Encoder SDK, o SDK do Windows Media Rights Manager e o SDK do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="637f5-133">Other components include the Windows Media Format SDK, the Windows Media Services SDK, the Windows Media Encoder SDK, the Windows Media Rights Manager SDK, and the Windows Media Player SDK.</span></span>

<span data-ttu-id="637f5-134">Esta documentação inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="637f5-134">This documentation includes the following sections.</span></span>



| <span data-ttu-id="637f5-135">Seção</span><span class="sxs-lookup"><span data-stu-id="637f5-135">Section</span></span>                                            | <span data-ttu-id="637f5-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="637f5-136">Description</span></span>                                                                                                                                                                                                                                                     |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="637f5-137">Introdução</span><span class="sxs-lookup"><span data-stu-id="637f5-137">Getting Started</span></span>](getting-started.md)             | <span data-ttu-id="637f5-138">Descreve o que há de novo nesta versão do Windows Media Gerenciador de Dispositivos, fornece uma visão geral de como funciona o Windows Media Gerenciador de Dispositivos, descreve o que será necessário para desenvolver um aplicativo ou provedor de serviços e explica os exemplos fornecidos com o SDK.</span><span class="sxs-lookup"><span data-stu-id="637f5-138">Describes what is new in this version of Windows Media Device Manager, gives an overview of how Windows Media Device Manager works, describes what will be needed to develop an application or service provider, and explains the samples shipped with the SDK.</span></span> |
| [<span data-ttu-id="637f5-139">Guia de programação</span><span class="sxs-lookup"><span data-stu-id="637f5-139">Programming Guide</span></span>](programming-guide.md)         | <span data-ttu-id="637f5-140">Discute como criar aplicativos e provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="637f5-140">Discusses how to build applications and service providers.</span></span>                                                                                                                                                                                                      |
| [<span data-ttu-id="637f5-141">Referência de programação</span><span class="sxs-lookup"><span data-stu-id="637f5-141">Programming Reference</span></span>](programming-reference.md) | <span data-ttu-id="637f5-142">Fornece informações de referência de C++ para as interfaces, métodos, classes e estruturas com suporte no SDK do Windows Media Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="637f5-142">Provides C++ reference information for the interfaces, methods, classes, and structures supported by the Windows Media Device Manager SDK.</span></span>                                                                                                                      |
| [<span data-ttu-id="637f5-143">*Glossário*</span><span class="sxs-lookup"><span data-stu-id="637f5-143">*Glossary*</span></span>](wmdm-glossary.md)                    | <span data-ttu-id="637f5-144">Define os termos usados nesta documentação.</span><span class="sxs-lookup"><span data-stu-id="637f5-144">Defines terms used in this documentation.</span></span>                                                                                                                                                                                                                       |



 

 

 




