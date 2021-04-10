---
description: Requisitos gerais para o desenvolvimento de aplicativos
ms.assetid: 8ac88d6f-fc4b-4253-932d-aaa3c801b18f
title: Requisitos gerais para o desenvolvimento de aplicativos (API WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16be9656f72324b8f3687bca72146320561b0d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170292"
---
# <a name="general-requirements-for-application-development-wpd-api"></a>Requisitos gerais para o desenvolvimento de aplicativos (API WPD)

Para criar um aplicativo de dispositivos portáteis do Windows, você deve ter o [SDK (Software Development Kit) do Windows](https://developer.microsoft.com/windows/downloads) instalado no computador. Os cabeçalhos e as bibliotecas necessárias aparecem na lista a seguir.

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

[**Dispositivos portáteis do Windows**](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
