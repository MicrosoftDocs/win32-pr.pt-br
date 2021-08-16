---
description: Requisitos gerais para o desenvolvimento de aplicativos
ms.assetid: 8ac88d6f-fc4b-4253-932d-aaa3c801b18f
title: Requisitos gerais para o desenvolvimento de aplicativos (API WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ad1ed207774494102f673bd7fb4f92acbdcb4629542d238613637d9509336c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430875"
---
# <a name="general-requirements-for-application-development-wpd-api"></a>Requisitos gerais para o desenvolvimento de aplicativos (API WPD)

para criar um aplicativo de dispositivos portáteis Windows, você deve ter o [Software Development Kit (SDK) do Windows](https://developer.microsoft.com/windows/downloads) instalado em seu computador. Os cabeçalhos e as bibliotecas necessárias aparecem na lista a seguir.

-   PortableDeviceGuids. lib
-   PortableDevice. h
-   PortableDeviceTypes. h
-   PortableDeviceApi. h
-   Quaisquer outras bibliotecas necessárias e cabeçalhos exigidos pelo seu aplicativo para consumir ou processar arquivos de mídia.

Se seu aplicativo der suporte às novas interfaces de serviços de dispositivo, ele também incluirá um ou mais dos seguintes arquivos de cabeçalho.

-   AnchorSyncDeviceService. h
-   BridgeDeviceService. h
-   CalendarDeviceService. h
-   ContactDeviceService. h
-   Dispositivoservices. h
-   FullEnumSyncDeviceService. h
-   HintsDeviceService. h
-   MessageDeviceService. h
-   MetadataDeviceService. h
-   NotesDeviceService. h
-   RingtoneDeviceService. h
-   StatusDeviceService. h
-   SyncDeviceService. h
-   TaskDeviceService. h

Dos arquivos na lista anterior, BridgeDeviceService. h e DeviceService. h são necessários para quase todos os aplicativos que dão suporte aos serviços de dispositivo; os outros arquivos definem tipos diferentes de serviços de dispositivo e seriam incluídos conforme apropriado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Windows Dispositivos portáteis**](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
