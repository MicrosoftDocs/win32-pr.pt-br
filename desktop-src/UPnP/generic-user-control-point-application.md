---
title: Aplicativo de ponto de controle de usuário genérico
description: O aplicativo genérico do UCP (ponto de controle do usuário) permite que você descubra dispositivos, controle esses dispositivos descobertos e exiba as informações de eventos relacionadas, tudo usando uma interface gráfica.
ms.assetid: 18ac23df-9d69-4a28-91e5-991eb4f3e6ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee56710cc1fafcc8551b34cb53df531f1f8cb601
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104552395"
---
# <a name="generic-user-control-point-application"></a>Aplicativo de ponto de controle de usuário genérico

O aplicativo genérico do UCP (ponto de controle do usuário) permite que você descubra dispositivos, controle esses dispositivos descobertos e exiba as informações de eventos relacionadas, tudo usando uma interface gráfica.

**Para iniciar o aplicativo UCP genérico**

1.  Crie e configure o arquivo de exemplos \\ netds \\ upnp \\ GenericUCP \\ \\devtype.txt cpp (ou \\ o \\ arquivo VisualBasicdevtype.txt) com as informações do dispositivo. Esse arquivo permite que você configure o UCP genérico para as pesquisas "localizar por tipo" e "localização assíncrona". Cada linha do arquivo deve conter um tipo de dispositivo e a Descrição relacionada. Por exemplo:

    ``` syntax
    upnp:rootdevice All Root Devices
    urn:schemas-upnp-org:device:mediaplayer:1    Media Player
    ```

    Este exemplo é para um dispositivo de player de mídia fictício. O "Player de mídia" no final da segunda linha não faz parte do tipo de dispositivo, é para fins informativos no aplicativo UCP genérico. O mesmo se aplica a "todos os dispositivos raiz" na primeira linha.

    Adicione uma linha que contenha o tipo de dispositivo e a descrição específicos para cada dispositivo.

2.  Crie e configure o \\ arquivo netds \\ UPnP \\ GenericUCP \\ cpp \\udn.txt (ou o \\ arquivo VISUALBASIC \\udn.txt) com informações de UDN para seus dispositivos. Esse arquivo permite que você configure o UCP genérico para a pesquisa "localizar por UDN". Cada linha usa a seguinte forma:

    ``` syntax
    uuid:{7d50b574-4213-4b88-84d9-e5c9241fcb3a}
    ```

    Adicione uma linha que contém seu UDN específico para cada dispositivo.

3.  Execute GenericUCP.exe. A janela **UCP genérica** é exibida.

    ![janela UCP genérica](images/generic-ucp.png)

> [!Note]  
> A funcionalidade **Exibir apresentação** e **Exibir serviço desc.** não está implementada no código de exemplo C++.

 

 

 




