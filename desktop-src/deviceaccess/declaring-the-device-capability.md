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
# <a name="declaring-the-device-capability"></a>Declarando a capacidade do dispositivo

Este tópico explica como declarar o GUID de capacidade do dispositivo. Todos os aplicativos que se destinam a drivers personalizados devem declarar esse recurso.

No manifesto do aplicativo, você precisará adicionar uma funcionalidade de dispositivo, da seguinte maneira:

Este é um exemplo de uma declaração de funcionalidade para um dispositivo personalizado. O GUID é o GUID da classe de interface do dispositivo.

```XML
<DeviceCapability Name="0B1F1048-B64B-FC9A-CED7-7E4FED3A0DEB" />
```

## <a name="related-topics"></a>Tópicos relacionados

[Exemplo de acesso de driver personalizado](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [aplicativos de dispositivo UWP para dispositivos internos](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [centro de desenvolvimento de hardware](/windows-hardware/drivers/)
