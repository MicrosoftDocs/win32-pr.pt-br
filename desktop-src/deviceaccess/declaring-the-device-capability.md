---
title: Declarando a capacidade do dispositivo
description: Este tópico explica como declarar o GUID de capacidade do dispositivo.
ms.assetid: C663F8D2-2CB6-4C3C-A1EB-A3D93AA71FC8
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 0b1f98717c7e9487874aa71691beefbac635660a
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "103917765"
---
# <a name="declaring-the-device-capability"></a><span data-ttu-id="46ca5-103">Declarando a capacidade do dispositivo</span><span class="sxs-lookup"><span data-stu-id="46ca5-103">Declaring the Device Capability</span></span>

<span data-ttu-id="46ca5-104">Este tópico explica como declarar o GUID de capacidade do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="46ca5-104">This topic explains how to declare the device capability GUID.</span></span> <span data-ttu-id="46ca5-105">Todos os aplicativos que se destinam a drivers personalizados devem declarar esse recurso.</span><span class="sxs-lookup"><span data-stu-id="46ca5-105">All applications that target custom drivers must declare this capability.</span></span>

<span data-ttu-id="46ca5-106">No manifesto do aplicativo, você precisará adicionar uma funcionalidade de dispositivo, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="46ca5-106">In your application manifest, you'll need to add a device capability, as follows:</span></span>

<span data-ttu-id="46ca5-107">Este é um exemplo de uma declaração de funcionalidade para um dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="46ca5-107">This is an example of a capability declaration for a custom device.</span></span> <span data-ttu-id="46ca5-108">O GUID é o GUID da classe de interface do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="46ca5-108">The GUID is the GUID of the device interface class.</span></span>

```XML
<DeviceCapability Name="0B1F1048-B64B-FC9A-CED7-7E4FED3A0DEB" />
```

## <a name="related-topics"></a><span data-ttu-id="46ca5-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="46ca5-109">Related topics</span></span>

<span data-ttu-id="46ca5-110">[Exemplo de acesso de driver personalizado](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [aplicativos de dispositivo UWP para dispositivos internos](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [centro de desenvolvimento de hardware](/windows-hardware/drivers/)</span><span class="sxs-lookup"><span data-stu-id="46ca5-110">[Custom Driver Access Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware Dev Center](/windows-hardware/drivers/)</span></span>
