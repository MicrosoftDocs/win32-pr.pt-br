---
description: Um dispositivo pode potencialmente gerar muitos eventos, e cada evento tem a opção de ser manipulado por um de vários manipuladores diferentes.
ms.assetid: C203B5AB-917C-4543-98D6-EDE02E0B5E49
title: Como registrar um manipulador de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3d786111a80cba455dd3480bdc970bc27009d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967893"
---
# <a name="how-to-register-an-event-handler"></a><span data-ttu-id="ed8db-103">Como registrar um manipulador de eventos</span><span class="sxs-lookup"><span data-stu-id="ed8db-103">How to Register an Event Handler</span></span>

<span data-ttu-id="ed8db-104">Um dispositivo pode potencialmente gerar muitos eventos, e cada evento tem a opção de ser manipulado por um de vários manipuladores diferentes.</span><span class="sxs-lookup"><span data-stu-id="ed8db-104">A device can potentially generate many events, and each event has the option of being handled by one of a number of different handlers.</span></span> <span data-ttu-id="ed8db-105">No Windows XP, os seguintes eventos são definidos:</span><span class="sxs-lookup"><span data-stu-id="ed8db-105">In Windows XP, the following events are defined:</span></span>

-   <span data-ttu-id="ed8db-106">DeviceArrival</span><span class="sxs-lookup"><span data-stu-id="ed8db-106">DeviceArrival</span></span>
-   <span data-ttu-id="ed8db-107">DeviceRemoval</span><span class="sxs-lookup"><span data-stu-id="ed8db-107">DeviceRemoval</span></span>
-   <span data-ttu-id="ed8db-108">MediaArrival</span><span class="sxs-lookup"><span data-stu-id="ed8db-108">MediaArrival</span></span>
-   <span data-ttu-id="ed8db-109">MediaRemoval</span><span class="sxs-lookup"><span data-stu-id="ed8db-109">MediaRemoval</span></span>

## <a name="instructions"></a><span data-ttu-id="ed8db-110">Instruções</span><span class="sxs-lookup"><span data-stu-id="ed8db-110">Instructions</span></span>


<span data-ttu-id="ed8db-111">Os manipuladores de eventos são definidos sob a chave **EventHandlers** .</span><span class="sxs-lookup"><span data-stu-id="ed8db-111">Event handlers are defined under the **EventHandlers** key.</span></span> <span data-ttu-id="ed8db-112">Os valores de uma chave de manipulador de eventos são os nomes de cada manipulador que o usuário deve escolher quando o evento é detectado.</span><span class="sxs-lookup"><span data-stu-id="ed8db-112">An event handler key's values are the names of each handler that the user must choose from when the event is detected.</span></span> <span data-ttu-id="ed8db-113">Não há nenhum valor de dados associado a essas entradas.</span><span class="sxs-lookup"><span data-stu-id="ed8db-113">There is no data value associated with these entries.</span></span> <span data-ttu-id="ed8db-114">Veja a seguir um exemplo de definição para um manipulador de eventos personalizado chamado **MyNewRemovalEventHandler**, que apresenta essas possibilidades de manipulador para o usuário:</span><span class="sxs-lookup"><span data-stu-id="ed8db-114">Following is an example definition for a custom event handler called **MyNewRemovalEventHandler**, which presents these handler possibilities to the user:</span></span>

-   <span data-ttu-id="ed8db-115">Um manipulador a ser usado se o evento for detectado em um dispositivo feito pela empresa chamada contoso, Inc.</span><span class="sxs-lookup"><span data-stu-id="ed8db-115">A handler to use if the event is detected on a device made by the company named Contoso, Inc.</span></span>
-   <span data-ttu-id="ed8db-116">Um manipulador a ser usado se o evento for detectado em um dispositivo feito pela empresa chamada Fabrikam, Inc.</span><span class="sxs-lookup"><span data-stu-id="ed8db-116">A handler to use if the event is detected on a device made by the company named Fabrikam, Inc.</span></span>
-   <span data-ttu-id="ed8db-117">Um manipulador a ser usado em todos os outros casos.</span><span class="sxs-lookup"><span data-stu-id="ed8db-117">A handler to use in all other cases.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     EventHandlers
                        MyNewRemovalEventHandler
                           CompanyContosoHandler [REG_SZ]
                           CompanyFabrikamHandler [REG_SZ]
                           MyRemovalHandler [REG_SZ]
```

<span data-ttu-id="ed8db-118">Depois que um manipulador de eventos é definido, ele deve ser registrado com um manipulador de dispositivo para uma das possibilidades de evento: DeviceArrival, DeviceRemoval, MediaArrival ou MediaRemoval.</span><span class="sxs-lookup"><span data-stu-id="ed8db-118">After an event handler is defined, it must be registered with a device handler for one of the event possibilities: DeviceArrival, DeviceRemoval, MediaArrival, or MediaRemoval.</span></span> <span data-ttu-id="ed8db-119">MyNewRemovalEventHandler, definido anteriormente, é usado para DeviceRemoval em um manipulador de dispositivo personalizado chamado MyDeviceHandler e é definido para essa finalidade no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="ed8db-119">MyNewRemovalEventHandler, defined earlier, is used for DeviceRemoval under a custom device handler named MyDeviceHandler and is defined for that purpose in the following example.</span></span> <span data-ttu-id="ed8db-120">Novamente, o valor do registro não tem nenhum componente de dados.</span><span class="sxs-lookup"><span data-stu-id="ed8db-120">Again, the registry value has no data component.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceHandlers
                        EventHandlers
                           DeviceRemoval
                              MyNewRemovalEventHandler
```

<span data-ttu-id="ed8db-121">O Windows XP Predefine o seguinte conjunto de EventHandlers.</span><span class="sxs-lookup"><span data-stu-id="ed8db-121">Windows XP predefines the following set of EventHandlers.</span></span> 

| <span data-ttu-id="ed8db-122">Chave EventHandlers</span><span class="sxs-lookup"><span data-stu-id="ed8db-122">EventHandlers key</span></span>        | <span data-ttu-id="ed8db-123">Mídia ou tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="ed8db-123">Media or file type</span></span>                             |
|--------------------------|------------------------------------------------|
| <span data-ttu-id="ed8db-124">HandleCDBurningOnArrival</span><span class="sxs-lookup"><span data-stu-id="ed8db-124">HandleCDBurningOnArrival</span></span> | <span data-ttu-id="ed8db-125">CD-R/CD-RW em branco</span><span class="sxs-lookup"><span data-stu-id="ed8db-125">Blank CD-R/CD-RW</span></span>                               |
| <span data-ttu-id="ed8db-126">ShowPicturesOnArrival</span><span class="sxs-lookup"><span data-stu-id="ed8db-126">ShowPicturesOnArrival</span></span>    | <span data-ttu-id="ed8db-127">Arquivos de imagem</span><span class="sxs-lookup"><span data-stu-id="ed8db-127">Picture files</span></span>                                  |
| <span data-ttu-id="ed8db-128">PlayMusicFilesOnArrival</span><span class="sxs-lookup"><span data-stu-id="ed8db-128">PlayMusicFilesOnArrival</span></span>  | <span data-ttu-id="ed8db-129">Arquivos de música</span><span class="sxs-lookup"><span data-stu-id="ed8db-129">Music files</span></span>                                    |
| <span data-ttu-id="ed8db-130">PlayVideoFilesOnArrival</span><span class="sxs-lookup"><span data-stu-id="ed8db-130">PlayVideoFilesOnArrival</span></span>  | <span data-ttu-id="ed8db-131">Arquivos de vídeo</span><span class="sxs-lookup"><span data-stu-id="ed8db-131">Video files</span></span>                                    |
| <span data-ttu-id="ed8db-132">PlayCDAudioOnArrival</span><span class="sxs-lookup"><span data-stu-id="ed8db-132">PlayCDAudioOnArrival</span></span>     | <span data-ttu-id="ed8db-133">CD de áudio (CD de formato REDBOOK com faixas de áudio)</span><span class="sxs-lookup"><span data-stu-id="ed8db-133">Audio CD (REDBOOK format CD with Audio tracks)</span></span> |
| <span data-ttu-id="ed8db-134">PlayDVDMovieOnArrival</span><span class="sxs-lookup"><span data-stu-id="ed8db-134">PlayDVDMovieOnArrival</span></span>    | <span data-ttu-id="ed8db-135">Filmes em DVD</span><span class="sxs-lookup"><span data-stu-id="ed8db-135">DVD movies</span></span>                                     |



 

<span data-ttu-id="ed8db-136">O Windows Vista Predefine o seguinte conjunto de EventHandlers, além daqueles acima.</span><span class="sxs-lookup"><span data-stu-id="ed8db-136">Windows Vista predefines the following set of EventHandlers in addition to those above.</span></span> 

| <span data-ttu-id="ed8db-137">Chave EventHandlers</span><span class="sxs-lookup"><span data-stu-id="ed8db-137">EventHandlers key</span></span>              | <span data-ttu-id="ed8db-138">Mídia ou tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="ed8db-138">Media or file type</span></span>   |
|--------------------------------|----------------------|
| <span data-ttu-id="ed8db-139">PlaySuperVideoCDMovieOnArrival</span><span class="sxs-lookup"><span data-stu-id="ed8db-139">PlaySuperVideoCDMovieOnArrival</span></span> | <span data-ttu-id="ed8db-140">Filmes de super VideoCD</span><span class="sxs-lookup"><span data-stu-id="ed8db-140">Super VideoCD movies</span></span> |
| <span data-ttu-id="ed8db-141">PlayVideoCDMovieOnArrival</span><span class="sxs-lookup"><span data-stu-id="ed8db-141">PlayVideoCDMovieOnArrival</span></span>      | <span data-ttu-id="ed8db-142">Filmes do VideoCD</span><span class="sxs-lookup"><span data-stu-id="ed8db-142">VideoCD movies</span></span>       |



 

 

 



