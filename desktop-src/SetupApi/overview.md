---
description: A API (interface de programação de aplicativo) da instalação do fornece um conjunto de funções que seu aplicativo de instalação pode chamar para executar operações de instalação. Essas funções de instalação funcionam com arquivos INF do Windows para fornecer a seguinte funcionalidade de instalação.
ms.assetid: 58201596-cb8c-480a-abef-896c1f9ef098
title: Visão geral
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32b99c6079fdb61fd6bfd0033ffccb9ebb7b922
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748381"
---
# <a name="overview"></a><span data-ttu-id="6fd04-104">Visão geral</span><span class="sxs-lookup"><span data-stu-id="6fd04-104">Overview</span></span>

<span data-ttu-id="6fd04-105">A API (interface de programação de aplicativo) da instalação do fornece um conjunto de funções que seu aplicativo de instalação pode chamar para executar operações de instalação.</span><span class="sxs-lookup"><span data-stu-id="6fd04-105">The Setup application programming interface (API) provides a set of functions that your setup application can call to perform installation operations.</span></span> <span data-ttu-id="6fd04-106">Essas funções de instalação funcionam com arquivos INF do Windows para fornecer a seguinte funcionalidade de instalação.</span><span class="sxs-lookup"><span data-stu-id="6fd04-106">These setup functions work with Windows INF files to provide the following setup functionality.</span></span>



| <span data-ttu-id="6fd04-107">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="6fd04-107">For information about</span></span>                       | <span data-ttu-id="6fd04-108">Consulte</span><span class="sxs-lookup"><span data-stu-id="6fd04-108">See</span></span>                                                                                                                                                                         |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fd04-109">Enfileirando arquivos</span><span class="sxs-lookup"><span data-stu-id="6fd04-109">Queuing files</span></span>                               | [<span data-ttu-id="6fd04-110">Filas de arquivos</span><span class="sxs-lookup"><span data-stu-id="6fd04-110">File Queues</span></span>](file-queues.md)                                                                                                                                              |
| <span data-ttu-id="6fd04-111">Instalando arquivos</span><span class="sxs-lookup"><span data-stu-id="6fd04-111">Installing files</span></span>                            | [<span data-ttu-id="6fd04-112">Filas de arquivos</span><span class="sxs-lookup"><span data-stu-id="6fd04-112">File Queues</span></span>](file-queues.md)<br/> [<span data-ttu-id="6fd04-113">Aplicativos de instalação</span><span class="sxs-lookup"><span data-stu-id="6fd04-113">Setup Applications</span></span>](setup-applications.md)<br/> [<span data-ttu-id="6fd04-114">Criando aplicativos de instalação</span><span class="sxs-lookup"><span data-stu-id="6fd04-114">Creating Setup Applications</span></span>](creating-setup-applications.md)<br/> |
| <span data-ttu-id="6fd04-115">Tratamento de erros e solicitação de mídia</span><span class="sxs-lookup"><span data-stu-id="6fd04-115">Handling errors and prompting for media</span></span>     | [<span data-ttu-id="6fd04-116">Solicitação de disco e tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="6fd04-116">Disk Prompting and Error Handling</span></span>](disk-prompting-and-error-handling.md)                                                                                                  |
| <span data-ttu-id="6fd04-117">Atualizando entradas do registro</span><span class="sxs-lookup"><span data-stu-id="6fd04-117">Updating registry entries</span></span>                   | [<span data-ttu-id="6fd04-118">Aplicativos de instalação</span><span class="sxs-lookup"><span data-stu-id="6fd04-118">Setup Applications</span></span>](setup-applications.md)                                                                                                                                |
| <span data-ttu-id="6fd04-119">Registrando arquivos instalados</span><span class="sxs-lookup"><span data-stu-id="6fd04-119">Logging installed files</span></span>                     | [<span data-ttu-id="6fd04-120">Log de arquivo</span><span class="sxs-lookup"><span data-stu-id="6fd04-120">File Log</span></span>](file-log.md)                                                                                                                                                    |
| <span data-ttu-id="6fd04-121">Armazenando os caminhos de origem usados mais recentemente</span><span class="sxs-lookup"><span data-stu-id="6fd04-121">Storing the most recently used source paths</span></span> | [<span data-ttu-id="6fd04-122">Lista de origem MRU</span><span class="sxs-lookup"><span data-stu-id="6fd04-122">MRU Source List</span></span>](mru-source-list.md)                                                                                                                                      |



 

<span data-ttu-id="6fd04-123">As versões Unicode e ANSI estão disponíveis para a maioria das funções de instalação.</span><span class="sxs-lookup"><span data-stu-id="6fd04-123">Unicode and ANSI versions are available for most setup functions.</span></span> <span data-ttu-id="6fd04-124">Os arquivos de texto Unicode devem conter a marca de ordem de byte 0xFEFF padrão para permitir que as funções de instalação identifiquem o arquivo como texto Unicode.</span><span class="sxs-lookup"><span data-stu-id="6fd04-124">Unicode text files should contain the standard 0xFEFF byte-order mark to enable setup functions to identify the file as Unicode text.</span></span>

<span data-ttu-id="6fd04-125">Embora a API de instalação ofereça suporte à solicitação de novas mídias e caixas de diálogo básicas de tratamento de erros, as funções de instalação não fornecem a funcionalidade do assistente ou uma interface de usuário genérica.</span><span class="sxs-lookup"><span data-stu-id="6fd04-125">Although the Setup API supports prompting for new media and basic error-handling dialog boxes, the setup functions do not provide wizard functionality or a generic user interface.</span></span>

<span data-ttu-id="6fd04-126">Os desenvolvedores devem considerar se podem usar [Windows Installer](/windows/desktop/Msi/windows-installer-portal) para instalar seus aplicativos em vez da API de instalação.</span><span class="sxs-lookup"><span data-stu-id="6fd04-126">Developers should consider whether they can use [Windows Installer](/windows/desktop/Msi/windows-installer-portal) to install their applications rather than the Setup API.</span></span> <span data-ttu-id="6fd04-127">Windows Installer reduz o TCO (custo total de propriedade) para seus clientes, permitindo que eles instalem e configurem seus produtos e aplicativos com eficiência.</span><span class="sxs-lookup"><span data-stu-id="6fd04-127">Windows Installer reduces the total cost of ownership (TCO) for your customers by enabling them to efficiently install and configure your products and applications.</span></span> <span data-ttu-id="6fd04-128">O instalador também pode fornecer a seus produtos novos recursos para anunciar recursos sem instalá-los, instalar produtos sob demanda e adicionar personalizações do usuário.</span><span class="sxs-lookup"><span data-stu-id="6fd04-128">The installer can also provide your product with new capabilities to advertise features without installing them, to install products on-demand, and to add user customizations.</span></span>

 

