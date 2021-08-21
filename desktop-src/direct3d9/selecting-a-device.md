---
description: Os aplicativos podem consultar hardware para detectar os tipos de dispositivo Direct3D com suporte. Esta seção contém informações sobre as principais tarefas envolvidas na enumeração de adaptadores de exibição e na seleção de dispositivos Direct3D.
ms.assetid: d140b90c-3a20-49f4-883b-662b6c05dcea
title: Selecionando um dispositivo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63428e15948e15790364f310d55989a9bbc7339846f7db5d301e316bee4d872
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044244"
---
# <a name="selecting-a-device-direct3d-9"></a>Selecionando um dispositivo (Direct3D 9)

Os aplicativos podem consultar hardware para detectar os tipos de dispositivo Direct3D com suporte. Esta seção contém informações sobre as principais tarefas envolvidas na enumeração de adaptadores de exibição e na seleção de dispositivos Direct3D.

Um aplicativo deve executar uma série de tarefas para selecionar um dispositivo Direct3D apropriado. Observe que as etapas a seguir destinam-se a um aplicativo de tela inteira e que, na maioria dos casos, um aplicativo em janelas pode ignorar a maioria dessas etapas.

1.  Inicialmente, o aplicativo deve enumerar os adaptadores de exibição no sistema. Um adaptador é uma parte física do hardware. Observe que a placa gráfica pode conter mais de um único adaptador, como é o caso com uma exibição de duas cabeça. Aplicativos que não estão preocupados com o suporte a vários monitores podem desconsiderar essa etapa e passar D3DADAPTER DEFAULT para o método \_ [**IDirect3D9::EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) na etapa 2.
2.  Para cada adaptador, o aplicativo enumera os modos de exibição com suporte chamando [**IDirect3D9::EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).
3.  Se necessário, o aplicativo verifica a presença de aceleração de hardware em cada modo de exibição enumerado chamando [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype), conforme mostrado no exemplo de código a seguir. Observe que esse é apenas um dos usos possíveis para **IDirect3D9::CheckDeviceType**; Para obter detalhes, consulte [Determinando o suporte a hardware (Direct3D 9)](determining-hardware-support.md).
    ```
    D3DPRESENT_PARAMETERS Params;
    // Initialize values for D3DPRESENT_PARAMETERS members. 

    Params.BackBufferFormat = D3DFMT_X1R5G5B5; 

    if(FAILED(m_pD3D->CheckDeviceType(Device.m_uAdapter, 
                      Device.m_DevType, 
                      Params.BackBufferFormat, Params.BackBufferFormat, 
                      FALSE))) 
        return E_FAIL;
    ```

    

4.  O aplicativo verifica o nível desejado de funcionalidade para o dispositivo nesse adaptador chamando o [**método IDirect3D9::GetDeviceCaps.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) A funcionalidade retornada por esse método tem a garantia de ser constante para um dispositivo em todos os modos de exibição, verificada por [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype).
5.  Os dispositivos sempre podem renderizar para superfícies do formato de um modo de exibição enumerado com suporte pelo dispositivo. Se o aplicativo for necessário para renderizar em uma superfície de um formato diferente, ele poderá chamar [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat). Se o dispositivo puder renderizar para o formato, será garantido que todos os recursos retornados por [**IDirect3D9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) sejam aplicáveis.
6.  Por fim, o aplicativo pode determinar se técnicas de multisampling, como a antialiação de cena completa, têm suporte para um formato de renderização usando o método [**IDirect3D9::CheckDeviceMultiSampleType.**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)

Depois de concluir as etapas anteriores, o aplicativo deve ter uma lista de modos de exibição nos quais ele pode operar. A etapa final é verificar se há memória acessível pelo dispositivo suficiente disponível para acomodar o número necessário de buffers e a antialização. Esse teste é necessário porque o consumo de memória para a combinação de modo e multisample é impossível de prever sem confirmá-lo. Além disso, algumas arquiteturas de adaptador de exibição podem não ter uma quantidade constante de memória acessível pelo dispositivo. Isso significa que um aplicativo deve ser capaz de relatar falhas de memória fora do vídeo ao entrar no modo de tela inteira. Normalmente, um aplicativo deve remover o modo de tela inteira da lista de modos que ele oferece a um usuário ou deve tentar consumir menos memória reduzindo o número de buffers de fundo ou usando uma técnica de multisampling menos complexa.

Um aplicativo em janelas executa um conjunto semelhante de tarefas.

1.  Ele determina o retângulo da área de trabalho coberto pela área de cliente da janela.
2.  Ele enumera adaptadores, procurando o adaptador cujo monitor abrange a área do cliente. Se a área de cliente pertence a mais de um adaptador, o aplicativo pode optar por conduzir cada adaptador de forma independente ou para conduzir um único adaptador e fazer com que o Direct3D transfira pixels de um dispositivo para outro na apresentação. O aplicativo também pode desconsiderar duas etapas anteriores e usar o adaptador DEFAULT D3DADAPTER. \_ Observe que isso pode resultar em uma operação mais lenta quando a janela é colocada em um monitor secundário.
3.  O aplicativo deve chamar [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype) para determinar se o dispositivo pode dar suporte à renderização em um buffer de fundo do formato especificado no modo de área de trabalho. [**IDirect3D9::GetAdapterDisplayMode**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode) pode ser usado para determinar o formato de exibição da área de trabalho, conforme mostrado no exemplo de código a seguir.
    ```
    D3DPRESENT_PARAMETERS Params;
    // Initialize values for D3DPRESENT_PARAMETERS members. 

    // Use the current display mode.
    D3DDISPLAYMODE mode;

    if(FAILED(m_pD3D->GetAdapterDisplayMode(Device.m_uAdapter , &mode)))
        return E_FAIL;

    Params.BackBufferFormat = mode.Format;

    if(FAILED(m_pD3D->CheckDeviceType(Device.m_uAdapter, Device.m_DevType, 
    Params.BackBufferFormat, Params.BackBufferFormat, FALSE)))
        return E_FAIL;
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
