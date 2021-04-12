---
description: Este tópico descreve o que você deve fazer para começar a criar programas que usam a API do sensor.
ms.assetid: a8d3228a-5f8b-4850-9e47-5dfb2335e655
title: Requisitos gerais para o desenvolvimento de aplicativos (API de sensor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ec328f659bb51eddf93cc69beb2fe6236113ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297178"
---
# <a name="general-requirements-for-application-development-sensor-api"></a><span data-ttu-id="848c1-103">Requisitos gerais para o desenvolvimento de aplicativos (API de sensor)</span><span class="sxs-lookup"><span data-stu-id="848c1-103">General Requirements for Application Development (Sensor API)</span></span>

<span data-ttu-id="848c1-104">Este tópico descreve o que você deve fazer para começar a criar programas que usam a API do sensor.</span><span class="sxs-lookup"><span data-stu-id="848c1-104">This topic describes what you must do to start to create programs that use the Sensor API.</span></span>

<span data-ttu-id="848c1-105">Para criar um aplicativo de API de sensor, você deve instalar o Windows 7 e o SDK (Software Development Kit) do Windows 7 em seu computador.</span><span class="sxs-lookup"><span data-stu-id="848c1-105">To create a Sensor API application, you must install Windows 7 and the Windows 7 Software Development Kit (SDK) on your computer.</span></span> <span data-ttu-id="848c1-106">A tabela a seguir descreve os arquivos específicos que serão necessários.</span><span class="sxs-lookup"><span data-stu-id="848c1-106">The following table describes the specific files that you will need.</span></span>



| <span data-ttu-id="848c1-107">Nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="848c1-107">File name</span></span>               | <span data-ttu-id="848c1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="848c1-108">Description</span></span>                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="848c1-109">Sensorsapi. h</span><span class="sxs-lookup"><span data-stu-id="848c1-109">Sensorsapi.h</span></span>            | <span data-ttu-id="848c1-110">O arquivo de cabeçalho principal para a API do sensor.</span><span class="sxs-lookup"><span data-stu-id="848c1-110">The main header file for the Sensor API.</span></span> <span data-ttu-id="848c1-111">Esse arquivo de cabeçalho contém as definições de interface.</span><span class="sxs-lookup"><span data-stu-id="848c1-111">This header file contains the interface definitions.</span></span>               |
| <span data-ttu-id="848c1-112">Sensores. h</span><span class="sxs-lookup"><span data-stu-id="848c1-112">Sensors.h</span></span>               | <span data-ttu-id="848c1-113">O arquivo de cabeçalho que contém definições de constantes definidas pela plataforma.</span><span class="sxs-lookup"><span data-stu-id="848c1-113">The header file that contains definitions of platform-defined constants.</span></span>                                    |
| <span data-ttu-id="848c1-114">Initguid. h</span><span class="sxs-lookup"><span data-stu-id="848c1-114">Initguid.h</span></span>              | <span data-ttu-id="848c1-115">O arquivo de cabeçalho que contém definições para controlar a inicialização do **GUID** .</span><span class="sxs-lookup"><span data-stu-id="848c1-115">The header file that contains definitions for controlling **GUID** initialization.</span></span>                          |
| <span data-ttu-id="848c1-116">FunctionDiscoveryKeys. h</span><span class="sxs-lookup"><span data-stu-id="848c1-116">FunctionDiscoveryKeys.h</span></span> | <span data-ttu-id="848c1-117">O arquivo de cabeçalho que define as chaves de propriedade de ID do dispositivo que são necessárias quando você se conecta a sensores lógicos.</span><span class="sxs-lookup"><span data-stu-id="848c1-117">The header file that defines device ID property keys that are required when you connect to logical sensors.</span></span> |
| <span data-ttu-id="848c1-118">Sensorsapi. lib</span><span class="sxs-lookup"><span data-stu-id="848c1-118">Sensorsapi.lib</span></span>          | <span data-ttu-id="848c1-119">Uma biblioteca estática que contém definições de **GUID** para a API do sensor.</span><span class="sxs-lookup"><span data-stu-id="848c1-119">A static library that contains **GUID** definitions for the Sensor API.</span></span>                                     |
| <span data-ttu-id="848c1-120">PortableDeviceGuids. lib</span><span class="sxs-lookup"><span data-stu-id="848c1-120">PortableDeviceGuids.lib</span></span> | <span data-ttu-id="848c1-121">Uma biblioteca estática que contém definições de **GUID** para objetos de dispositivos portáteis do Windows.</span><span class="sxs-lookup"><span data-stu-id="848c1-121">A static library that contains **GUID** definitions for Windows Portable Devices objects.</span></span>                   |



 

<span data-ttu-id="848c1-122">Seu programa pode exigir arquivos adicionais.</span><span class="sxs-lookup"><span data-stu-id="848c1-122">Your program may require additional files.</span></span>

## <a name="supported-operating-systems"></a><span data-ttu-id="848c1-123">Sistemas operacionais com suporte</span><span class="sxs-lookup"><span data-stu-id="848c1-123">Supported Operating Systems</span></span>

<span data-ttu-id="848c1-124">Os aplicativos de API do sensor serão executados em todas as edições do Windows 7, exceto para o Windows 7 Starter Edition.</span><span class="sxs-lookup"><span data-stu-id="848c1-124">Sensor API applications will run on all editions of Windows 7, except for Windows 7 Starter edition.</span></span>

## <a name="windows-portable-devices-interfaces"></a><span data-ttu-id="848c1-125">Interfaces de dispositivos portáteis do Windows</span><span class="sxs-lookup"><span data-stu-id="848c1-125">Windows Portable Devices Interfaces</span></span>

<span data-ttu-id="848c1-126">A API do sensor usa determinados objetos de dispositivos portáteis do Windows (WPD) para encapsular valores e chaves de propriedade.</span><span class="sxs-lookup"><span data-stu-id="848c1-126">The Sensor API uses certain Windows Portable Devices (WPD) objects to encapsulate property keys and values.</span></span> <span data-ttu-id="848c1-127">A tabela a seguir descreve as interfaces para esses objetos.</span><span class="sxs-lookup"><span data-stu-id="848c1-127">The following table describes the interfaces for these objects.</span></span>



| <span data-ttu-id="848c1-128">Interface</span><span class="sxs-lookup"><span data-stu-id="848c1-128">Interface</span></span>                                                                       | <span data-ttu-id="848c1-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="848c1-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="848c1-130">[IPortableDeviceValues](/previous-versions//ms740012(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="848c1-130">[IPortableDeviceValues](/previous-versions//ms740012(v=vs.85))</span></span>        | <span data-ttu-id="848c1-131">Essa interface fornece uma maneira conveniente de criar um recipiente de propriedades de pares de nome/valor.</span><span class="sxs-lookup"><span data-stu-id="848c1-131">This interface provides a convenient way to create a property bag of name/value pairs.</span></span> <span data-ttu-id="848c1-132">Os nomes são representados por a **PROPERTYKEY** s e os valores são representados por **PROPVARIANT** s.</span><span class="sxs-lookup"><span data-stu-id="848c1-132">Names are represented by **PROPERTYKEY** s and values are represented by **PROPVARIANT** s.</span></span> <br/> <span data-ttu-id="848c1-133">A API usa essa interface para configurar e recuperar valores únicos e conjuntos de valores.</span><span class="sxs-lookup"><span data-stu-id="848c1-133">The API uses this interface for setting and retrieving both single values and sets of values.</span></span> <span data-ttu-id="848c1-134">Essa interface pode ser recuperada de um método ou, se um novo objeto for necessário, chamando **CoCreateInstance** com CLSID \_ PortableDeviceValues.</span><span class="sxs-lookup"><span data-stu-id="848c1-134">This interface can be retrieved from a method or, if a new object is required, by calling **CoCreateInstance** with CLSID\_PortableDeviceValues.</span></span><br/> |
| <span data-ttu-id="848c1-135">[IPortableDeviceKeyCollection](/previous-versions//ms739549(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="848c1-135">[IPortableDeviceKeyCollection](/previous-versions//ms739549(v=vs.85))</span></span> | <span data-ttu-id="848c1-136">Esta interface contém uma coleção de **PROPERTYKEY** s.</span><span class="sxs-lookup"><span data-stu-id="848c1-136">This interface contains a collection of **PROPERTYKEY** s.</span></span> <span data-ttu-id="848c1-137">Essas chaves representam nomes de propriedade que podem ser armazenados por **IPortableDeviceValues**.</span><span class="sxs-lookup"><span data-stu-id="848c1-137">These keys represent property names that can be stored by **IPortableDeviceValues**.</span></span> <span data-ttu-id="848c1-138">A API usa esse objeto de coleção para definir e recuperar os nomes de propriedade única e os conjuntos de nomes de propriedade.</span><span class="sxs-lookup"><span data-stu-id="848c1-138">The API uses this collection object for setting and retrieving both single property names and sets of property names.</span></span><br/> <span data-ttu-id="848c1-139">Essa interface pode ser recuperada de um método ou, se um novo objeto for necessário, chamando **CoCreateInstance** com CLSID \_ PortableDeviceKeyCollection.</span><span class="sxs-lookup"><span data-stu-id="848c1-139">This interface can be retrieved from a method or, if a new object is required, by calling **CoCreateInstance** with CLSID\_PortableDeviceKeyCollection.</span></span> <br/>    |



 

 

