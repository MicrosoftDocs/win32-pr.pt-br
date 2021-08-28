---
title: Introdução a um dispositivo no Direct3D 11
description: O modelo de objeto do Direct3D 11 separa a funcionalidade de criação e renderização de recursos em um dispositivo e em um ou mais contextos; Essa separação foi projetada para facilitar o multithreading.
ms.assetid: b9b45d18-f7b7-40f9-ae4e-576ca7a6eba7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9459574ad7d8732714ac54519294ae232e4d8d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475702"
---
# <a name="introduction-to-a-device-in-direct3d-11"></a>Introdução a um dispositivo no Direct3D 11

O modelo de objeto do Direct3D 11 separa a funcionalidade de criação e renderização de recursos em um dispositivo e em um ou mais contextos; Essa separação foi projetada para facilitar o multithreading.

-   [Dispositivo](#introduction-to-a-device-in-direct3d-11)
-   [Contexto do dispositivo](#device-context)
    -   [Contexto imediato](#immediate-context)
    -   [Contexto adiado](#deferred-context)
-   [Considerações de thread](#threading-considerations)
-   [Tópicos relacionados](#related-topics)

## <a name="device"></a>Dispositivo

Um dispositivo é usado para criar recursos e para enumerar os recursos de um adaptador de vídeo. No Direct3D 11, um dispositivo é representado por uma interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) .

Cada aplicativo deve ter pelo menos um dispositivo; a maioria dos aplicativos só cria um dispositivo. Crie um dispositivo para um dos drivers de hardware instalados em seu computador chamando [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) ou [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) e especifique o tipo de driver com o sinalizador de [**\_ \_ tipo de driver do D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) . Cada dispositivo pode usar um ou mais contextos de dispositivo, dependendo da funcionalidade desejada.

## <a name="device-context"></a>Contexto do dispositivo

Um contexto de dispositivo contém a circunstância ou a configuração em que um dispositivo é usado. Mais especificamente, um contexto de dispositivo é usado para definir o estado do pipeline e gerar comandos de renderização usando os recursos de propriedade de um dispositivo. O Direct3D 11 implementa dois tipos de contextos de dispositivo, um para renderização imediata e outro para renderização adiada; ambos os contextos são representados com uma interface [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

### <a name="immediate-context"></a>Contexto imediato

Um contexto imediato é renderizado diretamente para o driver. Cada dispositivo tem um e apenas um contexto imediato que pode recuperar dados da GPU. Um contexto imediato pode ser usado para renderizar imediatamente (ou reproduzir) uma [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md).

Há duas maneiras de obter um contexto imediato:

-   Chamando [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) ou [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).
-   Chamando [**ID3D11Device:: GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).

### <a name="deferred-context"></a>Contexto adiado

Um contexto adiado registra comandos de GPU em uma [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md). Um contexto adiado é usado principalmente para multithreading e não é necessário para um aplicativo de thread único. Um contexto adiado geralmente é usado por um thread de trabalho em vez do thread de renderização principal. Quando você cria um contexto adiado, ele não herda nenhum estado do contexto imediato.

Para obter um contexto adiado, chame [**ID3D11Device:: CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).

Qualquer contexto--immediate ou adiado--pode ser usado em qualquer thread, desde que o contexto seja usado apenas em um thread por vez.

## <a name="threading-considerations"></a>Considerações de thread

Esta tabela destaca as diferenças no modelo de threading no Direct3D 11 de versões anteriores do Direct3D.




| | | Diferenças entre o Direct3D 11 e versões anteriores do Direct3D:<br /> Todos os métodos de interface <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> são de thread livre, o que significa que é seguro ter vários threads chamando as funções ao mesmo tempo.<br /><ul><li>Todas as interfaces derivadas de <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>(<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer"><strong>ID3D11Buffer</strong></a>, <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a>, etc.) são de thread livre.</li><li>O Direct3D 11 divide a criação e a renderização de recursos em duas interfaces. MAP, remapear, Begin, end e GetData são implementados em <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> porque <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> define fortemente a ordem das operações. As interfaces <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11resource"><strong>ID3D11Resource</strong></a> e <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a> também implementam métodos para operações de thread livre.</li><li>Os métodos <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> (exceto aqueles que existem em <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>) não são de thread livre, ou seja, eles exigem um único Threading. Somente um thread pode chamar com segurança qualquer um de seus métodos (Draw, copiar, mapear, etc.) de cada vez.</li><li>Em geral, o Threading livre minimiza o número de primitivos de sincronização usados, bem como sua duração. No entanto, um aplicativo que usa a sincronização mantida por um longo tempo pode impactar diretamente a quantidade de simultaneidade que um aplicativo pode esperar alcançar.</li></ul>Os métodos de interface ID3D10Device não são projetados para serem de thread livre. ID3D10Device implementa toda a funcionalidade de criação e renderização (como o ID3D9Device no Direct3D 9). Mapear e desmapear são implementados em interfaces derivadas de ID3D10Resource, Begin, end e GetData são implementados em interfaces derivadas de ID3D10Asynchronous.<br /> | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





