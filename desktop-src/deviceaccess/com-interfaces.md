---
title: Interfaces COM – Acesso ao Dispositivo
description: Component Object Model interfaces (COM) no API de Acesso a Dispositivo.
ms.assetid: 96F532B7-5CF9-4341-932B-7F8BEDA9551F
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 22447151b944a2ac5515222eebd528fed11e2479d8a8c4db59e2da46dd07a130
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793368"
---
# <a name="com-interfaces---device-access"></a>Interfaces COM – Acesso ao Dispositivo

Component Object Model interfaces (COM) no API de Acesso a Dispositivo.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|---|---|
| [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync)<br/> | A interface [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) é retornada de uma chamada para CreateDeviceAccessInstance. Ele permite que o chamador controle a operação de associação a uma instância de um dispositivo para recuperar outra interface que pode ser usada para interagir com esse dispositivo.<br/> |
| [**IDeviceIoControl**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol)<br/> | Envia um código de controle para um driver de dispositivo. Essa ação faz com que o dispositivo execute a operação correspondente. <br/> |
| [**IDeviceRequestCompletionCallback**](/windows/win32/api/Deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback)<br/> | Fornece um método para lidar com a conclusão de chamadas para o [**método DeviceIoControlAsync.**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync)<br/> |

## <a name="related-topics"></a>Tópicos relacionados

[Exemplo de acesso de driver personalizado,](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample)aplicativos de dispositivo [UWP para dispositivos internos,](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) [Centro de Desenvolvimento de Hardware](/windows-hardware/drivers/)
