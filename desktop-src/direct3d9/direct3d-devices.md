---
description: Um dispositivo Direct3D é o componente de renderização do Direct3D. Ele encapsula e armazena o estado de renderização. Além disso, um dispositivo Direct3D executa transformações e operações de iluminação e rasteriza uma imagem para uma superfície.
ms.assetid: b592edb8-351a-4a82-9ff7-8a69d82723bc
title: Dispositivos Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c07726069b952ba99d608e5f36df8e1fb7745cd7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163772"
---
# <a name="direct3d-devices-direct3d-9"></a>Dispositivos Direct3D (Direct3D 9)

Um dispositivo Direct3D é o componente de renderização do Direct3D. Ele encapsula e armazena o estado de renderização. Além disso, um dispositivo Direct3D executa transformações e operações de iluminação e rasteriza uma imagem para uma superfície.

-   [XPDM vs. WDDM](xpdm-vs-wddm.md)
-   [Tipos de dispositivo (Direct3D 9)](device-types.md)
-   [Criando um dispositivo (Direct3D 9)](creating-a-device.md)
-   [Modo Window vs Full-Screen (Direct3D 9)](windowed-vs-full-screen-mode.md)
-   [Selecionando um dispositivo (Direct3D 9)](selecting-a-device.md)
-   [Dispositivos perdidos (Direct3D 9)](lost-devices.md)
-   [Determinando o suporte de hardware (Direct3D 9)](determining-hardware-support.md)
-   [Processando dados de vértice (Direct3D 9)](processing-vertex-data.md)
-   [Primitivos](primitives.md)

Arquitetonicamente, os dispositivos Direct3D contêm um módulo de transformação, um módulo de iluminação e um módulo de rasterização, como mostra o diagrama a seguir.

![diagrama da arquitetura do dispositivo direct3d](images/d3ddev.png)

Atualmente, o Direct3D dá suporte a dois tipos principais de dispositivos Direct3D:

-   Um dispositivo hal com rasterização e sombreamento acelerados por hardware com processamento de vértice de hardware e software
-   Um dispositivo de referência

Você pode considerar esses dispositivos como dois drivers separados. Os dispositivos de referência e software são representados por drivers de software, e o dispositivo hal é representado por um driver de hardware. A maneira mais comum de tirar proveito desses dispositivos é usar o dispositivo hal para envio de aplicativos e o dispositivo de referência para o teste de recurso. Eles são fornecidos por terceiros para emular dispositivos específicos - por exemplo, um hardware de desenvolvimento que ainda não foi liberado.

O dispositivo Direct3D que cria um aplicativo deve corresponder aos recursos do hardware no qual o aplicativo é executado. O Direct3D fornece recursos de renderização, acessando o hardware 3D que está instalado no computador ou emulando as capacidades de hardware 3D no software. Portanto, o Direct3D fornece dispositivos para o acesso de hardware e a emulação de software.

Os dispositivos com aceleração de hardware oferecem desempenho muito melhor que dispositivos de software. O tipo de dispositivo hal está disponível em todos os adaptadores gráficos do Direct3D compatíveis. Na maioria dos casos, os aplicativos têm como foco computadores que têm aceleração de hardware e dependem de emulação de software para acomodar computadores inferiores.

Com exceção do dispositivo de referência, os dispositivos de software não dão suporte sempre aos mesmos recursos que um dispositivo de hardware. Os aplicativos sempre devem consultar recursos de dispositivo para determinar quais recursos têm suporte.

Como o comportamento dos dispositivos de referência e software fornecidos com o Direct3D 9 é idêntico ao do dispositivo hal, o código de aplicativo criado para funcionar com o dispositivo hal funcionará com os dispositivos de software ou referência sem modificações. Observe que, embora o comportamento do dispositivo de referência ou software fornecido seja idêntico ao do dispositivo Hal, os recursos do dispositivo variam, e um determinado dispositivo de software pode implementar um conjunto muito menor de recursos.

## <a name="behaviors"></a>Comportamentos

O Direct3D permite que você especifique o comportamento de um dispositivo, bem como o tipo do dispositivo. O método [**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) permite uma combinação de um ou mais sinalizadores de comportamento para controlar os comportamentos globais do dispositivo Direct3D. Esses comportamentos especificam o que é e não é mantido na parte de tempo de execução do Direct3D e os tipos de dispositivo especificam qual driver usar. Embora algumas combinações de comportamentos de dispositivo não sejam válidas, é possível usar todos os comportamentos de dispositivo com todos os tipos de dispositivo. Por exemplo, é válido especificar D3DDEVTYPE \_ SW em um dispositivo criado com D3DCREATE \_ PUREDEVICE.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução](getting-started.md)
</dt> </dl>

 

 
