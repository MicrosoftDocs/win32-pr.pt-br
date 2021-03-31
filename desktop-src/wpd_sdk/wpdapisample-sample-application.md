---
description: Aplicativo WpdApiSample
ms.assetid: 854a6304-5d62-4f00-9366-8c2244568250
title: Aplicativo WpdApiSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c384d542c9b93ac733c91ee249938d744e40ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647070"
---
# <a name="wpdapisample-application"></a><span data-ttu-id="c26f1-103">Aplicativo WpdApiSample</span><span class="sxs-lookup"><span data-stu-id="c26f1-103">WpdApiSample Application</span></span>

<span data-ttu-id="c26f1-104">O aplicativo de exemplo WpdApiSample é um aplicativo de área de trabalho de linha de comando que permite enumerar dispositivos conectados, explorar dispositivos, consultar objetos para propriedades e atributos, enviar e recuperar objetos e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="c26f1-104">The WpdApiSample sample application is a command-line desktop application that enables you to enumerate connected devices, explore devices, query objects for properties and attributes, send and retrieve objects, and so on.</span></span> <span data-ttu-id="c26f1-105">Na inicialização, o aplicativo abre uma janela de comando que lista as tarefas que você pode executar.</span><span class="sxs-lookup"><span data-stu-id="c26f1-105">On startup, the application opens a command window that lists the tasks you can perform.</span></span>

<span data-ttu-id="c26f1-106">O aplicativo de exemplo WpdApiSample inclui os seguintes arquivos:</span><span class="sxs-lookup"><span data-stu-id="c26f1-106">The WpdApiSample sample application includes the following files:</span></span>



| <span data-ttu-id="c26f1-107">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="c26f1-107">**File**</span></span>               | <span data-ttu-id="c26f1-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c26f1-108">**Description**</span></span>                                                                                                                                                                                           |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c26f1-109">ContentEnumeration. cpp</span><span class="sxs-lookup"><span data-stu-id="c26f1-109">ContentEnumeration.cpp</span></span> | <span data-ttu-id="c26f1-110">Contém funções que enumeram todos os objetos em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c26f1-110">Contains functions that enumerate all the objects on a device.</span></span>                                                                                                                                            |
| <span data-ttu-id="c26f1-111">Contentproperties. cpp</span><span class="sxs-lookup"><span data-stu-id="c26f1-111">ContentProperties.cpp</span></span>  | <span data-ttu-id="c26f1-112">Contém funções que lêem e gravam Propriedades de objeto e fazem solicitações set/get de propriedade em massa.</span><span class="sxs-lookup"><span data-stu-id="c26f1-112">Contains functions that read and write object properties and make bulk property set/get requests.</span></span>                                                                                                         |
| <span data-ttu-id="c26f1-113">ContentTransfer. cpp</span><span class="sxs-lookup"><span data-stu-id="c26f1-113">ContentTransfer.cpp</span></span>    | <span data-ttu-id="c26f1-114">Contém funções que transferem conteúdo de ou para o dispositivo, leem requisitos de tipo de objeto e criam uma pasta no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c26f1-114">Contains functions that transfer content to or from the device, read object type requirements, and create a folder on the device.</span></span>                                                                         |
| <span data-ttu-id="c26f1-115">DeviceCapabilities. cpp</span><span class="sxs-lookup"><span data-stu-id="c26f1-115">DeviceCapabilities.cpp</span></span> | <span data-ttu-id="c26f1-116">Contém funções para listar os tipos de objeto funcional no dispositivo, listar os tipos de conteúdo com suporte em cada tipo de objeto funcional e exibir perfis de objeto de renderização.</span><span class="sxs-lookup"><span data-stu-id="c26f1-116">Contains functions to list the functional object types on the device, list the content types supported by each functional object type, and display rendering object profiles.</span></span>                             |
| <span data-ttu-id="c26f1-117">DeviceEnumeration. cpp</span><span class="sxs-lookup"><span data-stu-id="c26f1-117">DeviceEnumeration.cpp</span></span>  | <span data-ttu-id="c26f1-118">Lista os nomes amigáveis, fabricantes e descrições de todos os dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="c26f1-118">Lists the friendly names, manufacturers, and descriptions of all connected devices.</span></span>                                                                                                                       |
| <span data-ttu-id="c26f1-119">DeviceEvents. cpp</span><span class="sxs-lookup"><span data-stu-id="c26f1-119">DeviceEvents.cpp</span></span>       | <span data-ttu-id="c26f1-120">Contém funções que registram eventos de dispositivo e seus parâmetros sempre que os eventos são acionados.</span><span class="sxs-lookup"><span data-stu-id="c26f1-120">Contains functions that log device events and their parameters whenever events are fired.</span></span>                                                                                                                 |
| <span data-ttu-id="c26f1-121">Stdafx.cpp</span><span class="sxs-lookup"><span data-stu-id="c26f1-121">Stdafx.cpp</span></span>             | <span data-ttu-id="c26f1-122">Inclui os arquivos padrão.</span><span class="sxs-lookup"><span data-stu-id="c26f1-122">Includes the standard files.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="c26f1-123">WpdApiSample. cpp</span><span class="sxs-lookup"><span data-stu-id="c26f1-123">WpdApiSample.cpp</span></span>       | <span data-ttu-id="c26f1-124">Hospeda a função de inicialização **\_ tmain** , que chama a função **domenu** local, que exibe uma lista de dispositivos e tarefas disponíveis e chama a função apropriada para a seleção de menu do usuário.</span><span class="sxs-lookup"><span data-stu-id="c26f1-124">Hosts the **\_tmain** startup function, which calls the local **DoMenu** function, which displays a list of available devices and tasks and calls the function appropriate for the user's menu selection.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c26f1-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c26f1-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c26f1-126">Amostra</span><span class="sxs-lookup"><span data-stu-id="c26f1-126">Sample</span></span>](sample.md)
</dt> </dl>

 

 



