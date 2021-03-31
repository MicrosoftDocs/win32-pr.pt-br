---
description: O objeto Gerenciador de sensor fornece acesso aos sensores que estão disponíveis para seu uso.
ms.assetid: dd39d533-9983-41b4-a9a3-d94dcadebaac
title: O objeto Gerenciador de sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 715448a62c058c5e6825368003939e5ae2066847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090166"
---
# <a name="the-sensor-manager-object"></a><span data-ttu-id="d330b-103">O objeto Gerenciador de sensor</span><span class="sxs-lookup"><span data-stu-id="d330b-103">The Sensor Manager Object</span></span>

<span data-ttu-id="d330b-104">O objeto Gerenciador de sensor fornece acesso aos sensores que estão disponíveis para seu uso.</span><span class="sxs-lookup"><span data-stu-id="d330b-104">The sensor manager object provides access to the sensors that are available for your use.</span></span>

<span data-ttu-id="d330b-105">Para usar a API do sensor, você deve primeiro chamar o método COM **CoCreateInstance** para criar uma instância do objeto do sensor Manager e recuperar um ponteiro para sua interface, chamada [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager).</span><span class="sxs-lookup"><span data-stu-id="d330b-105">To use the Sensor API, you must first call the COM **CoCreateInstance** method to create an instance of the sensor manager object and retrieve a pointer to its interface, named [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager).</span></span> <span data-ttu-id="d330b-106">O Gerenciador de sensor mantém a lista de sensores disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d330b-106">The sensor manager maintains the list of available sensors.</span></span> <span data-ttu-id="d330b-107">Você pode usar **ISensorManager** para chamar métodos que recuperam grupos de sensores por categoria ou por tipo, ou você pode chamar um método para recuperar um sensor específico usando sua ID exclusiva.</span><span class="sxs-lookup"><span data-stu-id="d330b-107">You can use **ISensorManager** to call methods that retrieve groups of sensors by category or by type, or you can call a method to retrieve a particular sensor by using its unique ID.</span></span> <span data-ttu-id="d330b-108">O Gerenciador de sensor também permite que você se registre para receber um evento que notifica quando um novo sensor está conectado à plataforma.</span><span class="sxs-lookup"><span data-stu-id="d330b-108">The sensor manager also enables you to register to receive an event that notifies you when a new sensor has been connected to the platform.</span></span>

<span data-ttu-id="d330b-109">Às vezes, o Gerenciador de sensor fornece um ponteiro para um sensor, mas o usuário não habilitou o sensor.</span><span class="sxs-lookup"><span data-stu-id="d330b-109">Sometimes, the sensor manager provides a pointer to a sensor, but the user has not enabled the sensor.</span></span> <span data-ttu-id="d330b-110">Por exemplo, geralmente é possível recuperar valores para propriedades de sensor não particulares, como o fabricante ou modelo do sensor, antes que o usuário habilite o sensor.</span><span class="sxs-lookup"><span data-stu-id="d330b-110">For example, you can often retrieve values for non-private sensor properties, such as the sensor manufacturer or model, before the user enables the sensor.</span></span> <span data-ttu-id="d330b-111">Essas informações podem ajudá-lo a decidir se deseja solicitar ao usuário a permissão para usar o sensor.</span><span class="sxs-lookup"><span data-stu-id="d330b-111">This information can help you to decide whether to ask the user for permission to use the sensor.</span></span> <span data-ttu-id="d330b-112">Você pode chamar [**ISensorManager:: RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) para solicitar que o usuário habilite um sensor específico ou uma coleção de sensores.</span><span class="sxs-lookup"><span data-stu-id="d330b-112">You can call [**ISensorManager::RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) to prompt the user to enable a particular sensor or collection of sensors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d330b-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d330b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d330b-114">Gerenciando permissões de usuário</span><span class="sxs-lookup"><span data-stu-id="d330b-114">Managing User Permissions</span></span>](managing-user-permissions.md)
</dt> <dt>

[<span data-ttu-id="d330b-115">Solicitando permissões de usuário</span><span class="sxs-lookup"><span data-stu-id="d330b-115">Requesting User Permissions</span></span>](requesting-user-permissions.md)
</dt> </dl>

 

 
