---
title: O que é o modelo de objeto do ponto de controle
description: A ilustração a seguir mostra o modelo de objeto do ponto de controle básico.
ms.assetid: 6c5a32a1-932e-4868-b4c6-8701e90a7c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e491d3ec89b1074fb09a9f7632a886fb67b59863
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292800"
---
# <a name="what-is-the-control-point-object-model"></a><span data-ttu-id="f8da1-103">O que é o modelo de objeto de ponto de controle?</span><span class="sxs-lookup"><span data-stu-id="f8da1-103">What is the Control Point Object Model?</span></span>

<span data-ttu-id="f8da1-104">A ilustração a seguir mostra o modelo de objeto do ponto de controle básico.</span><span class="sxs-lookup"><span data-stu-id="f8da1-104">The following illustration shows the basic Control Point object model.</span></span>

![modelo de objeto do ponto de controle](images/upnp-object-model.png)

<span data-ttu-id="f8da1-106">A pesquisa de dispositivos com a interface do Device Finder cria uma coleção de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="f8da1-106">Searching for devices with the Device Finder interface creates a Devices collection.</span></span> <span data-ttu-id="f8da1-107">Uma coleção de dispositivos contém zero ou mais objetos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8da1-107">A Devices collection contains zero or more Device objects.</span></span> <span data-ttu-id="f8da1-108">Os aplicativos podem usar os vários métodos de coleção de dispositivos para acessar objetos de dispositivo individuais.</span><span class="sxs-lookup"><span data-stu-id="f8da1-108">Applications can use the various Devices collection methods to access individual Device objects.</span></span>

<span data-ttu-id="f8da1-109">Os objetos de dispositivo sempre contêm uma coleção de serviços que contém um ou mais objetos de serviço.</span><span class="sxs-lookup"><span data-stu-id="f8da1-109">Device objects always contain a Services collection that contains one or more Service objects.</span></span> <span data-ttu-id="f8da1-110">Esses objetos de serviço são usados por aplicativos para se comunicar e controlar dispositivos.</span><span class="sxs-lookup"><span data-stu-id="f8da1-110">These service objects are used by applications to communicate with and control devices.</span></span>

 

 




