---
description: Aplicativo WpdServicesApiSample
ms.assetid: 857753f7-bca1-4f4a-a8f9-0b2232e2f0dc
title: Aplicativo WpdServicesApiSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54cbf6c6e4647744ae45f43b5d4139cbf7f9dc55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755493"
---
# <a name="wpdservicesapisample-application"></a><span data-ttu-id="fb1dd-103">Aplicativo WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="fb1dd-103">WpdServicesApiSample Application</span></span>

<span data-ttu-id="fb1dd-104">Um serviço de dispositivo é uma extensão de um objeto funcional: além de agrupar logicamente os recursos do dispositivo, um serviço de dispositivo fornece aos aplicativos a capacidade de descobrir programaticamente esses recursos.</span><span class="sxs-lookup"><span data-stu-id="fb1dd-104">A device service is an extension of a functional object: In addition to logically grouping device capabilities, a device service provides applications with the ability to programmatically discover those capabilities.</span></span>

<span data-ttu-id="fb1dd-105">O aplicativo de exemplo WpdServicesApiSample é um aplicativo de área de trabalho de linha de comando que você pode usar para explorar os serviços de contatos em dispositivos conectados ao seu computador.</span><span class="sxs-lookup"><span data-stu-id="fb1dd-105">The WpdServicesApiSample sample application is a command-line desktop application that you can use to explore Contacts services on devices attached to your computer.</span></span> <span data-ttu-id="fb1dd-106">Você pode explorar esses serviços por meio da listagem com suporte: formatos, eventos, métodos e serviços abstratos.</span><span class="sxs-lookup"><span data-stu-id="fb1dd-106">You can explore these services by listing supported: formats, events, methods, and abstract services.</span></span> <span data-ttu-id="fb1dd-107">Você também pode usar esse aplicativo para recuperar as propriedades em um determinado serviço de contato e para invocar métodos com suporte nesse serviço.</span><span class="sxs-lookup"><span data-stu-id="fb1dd-107">You can also use this application retrieve the properties on a given Contact service and to invoke methods supported by that service.</span></span>

<span data-ttu-id="fb1dd-108">Se você ainda não tiver um dispositivo que dê suporte a serviços de contatos, ainda poderá executar o WpdServicesApiSample se instalar primeiro o WpdServiceSampleDriver que está incluído no kit de driver do Windows.</span><span class="sxs-lookup"><span data-stu-id="fb1dd-108">If you don't yet have a device that supports Contacts services, you can still run the WpdServicesApiSample if you first install the WpdServiceSampleDriver that is included in the Windows Driver Kit.</span></span>

<span data-ttu-id="fb1dd-109">O aplicativo de exemplo WpdServicesApiSample inclui os seguintes arquivos:</span><span class="sxs-lookup"><span data-stu-id="fb1dd-109">The WpdServicesApiSample sample application includes the following files:</span></span>



| <span data-ttu-id="fb1dd-110">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="fb1dd-110">**File**</span></span>                | <span data-ttu-id="fb1dd-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fb1dd-111">**Description**</span></span>                                                                                                                                                                                           |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb1dd-112">ContentEnumeration. cpp</span><span class="sxs-lookup"><span data-stu-id="fb1dd-112">ContentEnumeration.cpp</span></span>  | <span data-ttu-id="fb1dd-113">Contém métodos que enumeram o conteúdo em um determinado serviço Contacts.</span><span class="sxs-lookup"><span data-stu-id="fb1dd-113">Contains methods that enumerate the content on a given Contacts service.</span></span>                                                                                                                                  |
| <span data-ttu-id="fb1dd-114">Contentproperties. cpp</span><span class="sxs-lookup"><span data-stu-id="fb1dd-114">ContentProperties.cpp</span></span>   | <span data-ttu-id="fb1dd-115">Contém métodos que lêem e gravam Propriedades em um determinado serviço de contatos.</span><span class="sxs-lookup"><span data-stu-id="fb1dd-115">Contains methods that read and write properties on a given Contacts service.</span></span>                                                                                                                              |
| <span data-ttu-id="fb1dd-116">Percapabilities. cpp</span><span class="sxs-lookup"><span data-stu-id="fb1dd-116">ServiceCapabilities.cpp</span></span> | <span data-ttu-id="fb1dd-117">Contém os métodos que recuperam os formatos com suporte, os eventos e os serviços abstratos que são suportados por um determinado serviço de contatos.</span><span class="sxs-lookup"><span data-stu-id="fb1dd-117">Contains the methods that retrieve the supported formats, events, and abstract services that are supported by a given Contacts service.</span></span>                                                                   |
| <span data-ttu-id="fb1dd-118">O inenumeration. cpp</span><span class="sxs-lookup"><span data-stu-id="fb1dd-118">ServiceEnumeration.cpp</span></span>  | <span data-ttu-id="fb1dd-119">Contém as funções auxiliares que recuperam informações do dispositivo, como o nome amigável do dispositivo ou os serviços de contatos com suporte.</span><span class="sxs-lookup"><span data-stu-id="fb1dd-119">Contains the helper functions that retrieve device information such as the device-friendly name or the supported Contacts services.</span></span>                                                                       |
| <span data-ttu-id="fb1dd-120">Permethods. cpp</span><span class="sxs-lookup"><span data-stu-id="fb1dd-120">ServiceMethods.cpp</span></span>      | <span data-ttu-id="fb1dd-121">Contém os métodos que recuperam e invocam métodos com suporte de um determinado serviço de contatos.</span><span class="sxs-lookup"><span data-stu-id="fb1dd-121">Contains the methods that retrieve and invoke methods supported by a given Contacts service.</span></span>                                                                                                              |
| <span data-ttu-id="fb1dd-122">Stdafx.cpp</span><span class="sxs-lookup"><span data-stu-id="fb1dd-122">Stdafx.cpp</span></span>              | <span data-ttu-id="fb1dd-123">Inclui os arquivos padrão.</span><span class="sxs-lookup"><span data-stu-id="fb1dd-123">Includes the standard files.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="fb1dd-124">WpdServiceApiSample. cpp</span><span class="sxs-lookup"><span data-stu-id="fb1dd-124">WpdServiceApiSample.cpp</span></span> | <span data-ttu-id="fb1dd-125">Hospeda a função de inicialização **\_ tmain** , que chama a função **domenu** local, que exibe uma lista de dispositivos e tarefas disponíveis e chama a função apropriada para a seleção de menu do usuário.</span><span class="sxs-lookup"><span data-stu-id="fb1dd-125">Hosts the **\_tmain** startup function, which calls the local **DoMenu** function, which displays a list of available devices and tasks and calls the function appropriate for the user's menu selection.</span></span> |



 


## <a name="related-topics"></a><span data-ttu-id="fb1dd-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fb1dd-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb1dd-127">Amostras</span><span class="sxs-lookup"><span data-stu-id="fb1dd-127">Samples</span></span>](sample.md)
</dt> </dl>

 

 



