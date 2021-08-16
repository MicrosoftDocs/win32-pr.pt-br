---
title: Aplicativo de ponto de controle de usuário genérico
description: O aplicativo UCP (ponto de controle de usuário genérico) permite que você descubra dispositivos, controle esses dispositivos descobertos e veja as informações de eventos relacionadas, tudo isso usando uma interface gráfica.
ms.assetid: 18ac23df-9d69-4a28-91e5-991eb4f3e6ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0bbf454da2bf36becb3c8b0aff2babc87925df7ac658fc9dc7963ba9182fad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655726"
---
# <a name="generic-user-control-point-application"></a>Aplicativo de ponto de controle de usuário genérico

O aplicativo UCP (ponto de controle de usuário genérico) permite que você descubra dispositivos, controle esses dispositivos descobertos e veja as informações de eventos relacionadas, tudo isso usando uma interface gráfica.

**Para iniciar o aplicativo UCP genérico**

1.  Crie e configure os exemplos \\ netds \\ upnp \\ GenericUCP CPPdevtype.txt arquivo (ou o arquivo \\devtype.txt \\ \\ VisualBasic) \\ com informações do dispositivo. Esse arquivo permite configurar o UCP genérico para as pesquisas "encontrar por tipo" e "encontrar assíncrono". Cada linha do arquivo deve conter um tipo de dispositivo e a descrição relacionada. Por exemplo:

    ``` syntax
    upnp:rootdevice All Root Devices
    urn:schemas-upnp-org:device:mediaplayer:1    Media Player
    ```

    Este exemplo é para um dispositivo de player de mídia fictício. O "Media Player" no final da segunda linha não faz parte do tipo de dispositivo, é para fins informacionais no aplicativo UCP genérico. O mesmo se aplica a "Todos os Dispositivos Raiz" na primeira linha.

    Adicione uma linha que contém o tipo de dispositivo e a descrição específicos para cada dispositivo.

2.  Crie e configure os exemplos do arquivo deudn.txt \\ \\ netds upnp GenericUCP (ou o arquivo \\udn.txt \\ \\ VisualBasic) com informações \\ \\ de UDN para seus dispositivos. Esse arquivo permite que você configure o UCP genérico para a pesquisa "encontrar por UDN". Cada linha usa o seguinte formulário:

    ``` syntax
    uuid:{7d50b574-4213-4b88-84d9-e5c9241fcb3a}
    ```

    Adicione uma linha que contém seu UDN específico para cada dispositivo.

3.  Execute GenericUCP.exe. A **janela UCP** genérico é exibida.

    ![janela UCP genérica](images/generic-ucp.png)

> [!Note]  
> A **Desc Exibir Apresentação** e Exibir **Serviço.** A funcionalidade não é implementada no código de exemplo do C++.

 

 

 




