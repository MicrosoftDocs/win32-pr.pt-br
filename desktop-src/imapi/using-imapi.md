---
title: Usando o IMAPi
description: Os tópicos a seguir demonstram o uso da API de mestre de imagem.
ms.assetid: c42043db-612f-488f-a6ae-a8caea8ac42b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccd44d01e925d07d251e93a29c5268cc7e9c5076
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823034"
---
# <a name="using-imapi"></a><span data-ttu-id="09b51-103">Usando o IMAPi</span><span class="sxs-lookup"><span data-stu-id="09b51-103">Using IMAPI</span></span>

<span data-ttu-id="09b51-104">Os tópicos a seguir demonstram o uso da API de mestre de imagem.</span><span class="sxs-lookup"><span data-stu-id="09b51-104">The following topics demonstrate the use of the image mastering API.</span></span>

## <a name="usage-scenarios"></a><span data-ttu-id="09b51-105">Cenários de uso</span><span class="sxs-lookup"><span data-stu-id="09b51-105">Usage Scenarios</span></span>

<span data-ttu-id="09b51-106">A documentação a seguir fornece orientações detalhadas para cenários comuns de IMAPi.</span><span class="sxs-lookup"><span data-stu-id="09b51-106">The following documentation provides detailed guidance for common IMAPI scenarios.</span></span>



| <span data-ttu-id="09b51-107">Cenário</span><span class="sxs-lookup"><span data-stu-id="09b51-107">Scenario</span></span>                                                                                                         | <span data-ttu-id="09b51-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="09b51-108">Description</span></span>                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09b51-109">Verificando o suporte à unidade</span><span class="sxs-lookup"><span data-stu-id="09b51-109">Checking Drive Support</span></span>](checking-drive-support.md)                                                             | <span data-ttu-id="09b51-110">Demonstra a detecção de suporte para uma unidade de mídia.</span><span class="sxs-lookup"><span data-stu-id="09b51-110">Demonstrates the detection of support for a media drive.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="09b51-111">Verificando o suporte de mídia</span><span class="sxs-lookup"><span data-stu-id="09b51-111">Checking Media Support</span></span>](checking-media-support.md)                                                             | <span data-ttu-id="09b51-112">Demonstra a detecção de suporte para mídia.</span><span class="sxs-lookup"><span data-stu-id="09b51-112">Demonstrates the detection of support for media.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="09b51-113">Gravando uma imagem de disco</span><span class="sxs-lookup"><span data-stu-id="09b51-113">Burning a Disc Image</span></span>](burning-a-disc.md)                                                                       | <span data-ttu-id="09b51-114">Demonstra como dominar (gravar um disco) usando o IMAPi.</span><span class="sxs-lookup"><span data-stu-id="09b51-114">Demonstrates mastering (burning a disc) using IMAPI.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="09b51-115">Adicionando uma imagem de inicialização</span><span class="sxs-lookup"><span data-stu-id="09b51-115">Adding a Boot Image</span></span>](adding-a-boot-image.md)                                                                   | <span data-ttu-id="09b51-116">Baseia-se no exemplo de [gravação de uma imagem de disco](burning-a-disc.md) adicionando código para incluir uma imagem inicializável na seção de inicialização do disco.</span><span class="sxs-lookup"><span data-stu-id="09b51-116">Builds on the [Burning a Disc Image](burning-a-disc.md) example by adding code to include a bootable image in the boot section of the disc.</span></span><br/>               |
| [<span data-ttu-id="09b51-117">Criando um disco de várias sessões</span><span class="sxs-lookup"><span data-stu-id="09b51-117">Creating a Multisession Disc</span></span>](creating-a-multisession-disc.md)                                                 | <span data-ttu-id="09b51-118">Demonstra a criação de um disco de várias sessões usando IMAPi.</span><span class="sxs-lookup"><span data-stu-id="09b51-118">Demonstrates the creation of a multisession disc using IMAPI.</span></span><br/>                                                                                              |
| [<span data-ttu-id="09b51-119">Progresso do monitoramento com eventos</span><span class="sxs-lookup"><span data-stu-id="09b51-119">Monitoring Progress With Events</span></span>](monitoring-progress-with-events.md)                                           | <span data-ttu-id="09b51-120">Demonstra o uso de interfaces específicas para permitir a implementação de um manipulador de eventos para que as informações de progresso possam ser recebidas.</span><span class="sxs-lookup"><span data-stu-id="09b51-120">Demonstrates the use of specific interfaces in order to allow the implementation of an event handler so that progress information may be received.</span></span> <br/>        |
| [<span data-ttu-id="09b51-121">Impedindo o logoff ou a suspensão durante uma gravação</span><span class="sxs-lookup"><span data-stu-id="09b51-121">Preventing Logoff or Suspend During a Burn</span></span>](preventing-logoff-or-suspend-during-a-burn.md)                     | <span data-ttu-id="09b51-122">Contém informações detalhadas sobre o desenvolvimento de aplicativos que devem ser feitas em relação a cenários envolvendo o usuário ' logoff ' e ' suspender ' no Windows.</span><span class="sxs-lookup"><span data-stu-id="09b51-122">Contains information detailing application development considerations to be made in regards to scenarios involving user 'Logoff' and 'Suspend' in Windows.</span></span><br/> |
| [<span data-ttu-id="09b51-123">Fornecendo permissões de usuário para dispositivos de gravação de mídia</span><span class="sxs-lookup"><span data-stu-id="09b51-123">Providing User Permissions for Media Burning Devices</span></span>](providing-user-permissions-for-media-burning-devices.md) | <span data-ttu-id="09b51-124">Detalha o processo necessário para garantir que um usuário tenha as permissões adequadas para utilizar dispositivos de gravação de mídia no Windows XP e no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="09b51-124">Details the process required to ensure a user has adequate permissions to utilize media burning devices on Windows XP and Windows Server 2003.</span></span><br/>             |



 

## <a name="application-compatibility"></a><span data-ttu-id="09b51-125">Compatibilidade de aplicativos</span><span class="sxs-lookup"><span data-stu-id="09b51-125">Application Compatibility</span></span>

<span data-ttu-id="09b51-126">A documentação a seguir contém informações importantes a serem levadas em consideração ao desenvolver um aplicativo que utiliza o IMAPi.</span><span class="sxs-lookup"><span data-stu-id="09b51-126">The following documentation contains important information to take consideration while developing an application that utilizes IMAPI.</span></span>



| <span data-ttu-id="09b51-127">Diretrizes</span><span class="sxs-lookup"><span data-stu-id="09b51-127">Guidance</span></span>                                                   | <span data-ttu-id="09b51-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="09b51-128">Description</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09b51-129">Layout de várias sessões do IMAPi</span><span class="sxs-lookup"><span data-stu-id="09b51-129">IMAPI Multisession Layout</span></span>](imapi-multisession-layout.md) | <span data-ttu-id="09b51-130">Detalha o layout do disco que o IMAPi utiliza para implementar várias sessões.</span><span class="sxs-lookup"><span data-stu-id="09b51-130">Details the disc layout that IMAPI utilizes to implement multisession.</span></span> <span data-ttu-id="09b51-131">Essas informações são usadas para garantir a interoperabilidade entre o IMAPi e outros softwares de gravação, além de permitir a criação de imagens de disco de várias sessões compatíveis com o IMAPi.</span><span class="sxs-lookup"><span data-stu-id="09b51-131">This information is used to ensure interoperability between IMAPI and other burning software, as well as allow the creation of IMAPI-compatible multisession disc images.</span></span><br/> |



 

 

 





