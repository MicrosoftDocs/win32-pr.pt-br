---
description: Os aplicativos podem consultar o hardware para detectar os tipos de dispositivo Direct3D com suporte. Esta seção contém informações sobre as principais tarefas envolvidas na enumeração de adaptadores de vídeo e seleção de dispositivos Direct3D.
ms.assetid: d140b90c-3a20-49f4-883b-662b6c05dcea
title: Selecionando um dispositivo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdfa1faf38007f00959ac7263b4538954044688
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500728"
---
# <a name="selecting-a-device-direct3d-9"></a><span data-ttu-id="40eae-104">Selecionando um dispositivo (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="40eae-104">Selecting a Device (Direct3D 9)</span></span>

<span data-ttu-id="40eae-105">Os aplicativos podem consultar o hardware para detectar os tipos de dispositivo Direct3D com suporte.</span><span class="sxs-lookup"><span data-stu-id="40eae-105">Applications can query hardware to detect the supported Direct3D device types.</span></span> <span data-ttu-id="40eae-106">Esta seção contém informações sobre as principais tarefas envolvidas na enumeração de adaptadores de vídeo e seleção de dispositivos Direct3D.</span><span class="sxs-lookup"><span data-stu-id="40eae-106">This section contains information about the primary tasks involved in enumerating display adapters and selecting Direct3D devices.</span></span>

<span data-ttu-id="40eae-107">Um aplicativo deve executar uma série de tarefas para selecionar um dispositivo Direct3D apropriado.</span><span class="sxs-lookup"><span data-stu-id="40eae-107">An application must perform a series of tasks to select an appropriate Direct3D device.</span></span> <span data-ttu-id="40eae-108">Observe que as etapas a seguir destinam-se a um aplicativo de tela inteira e que, na maioria dos casos, um aplicativo em janela pode ignorar a maioria dessas etapas.</span><span class="sxs-lookup"><span data-stu-id="40eae-108">Note that the following steps are intended for a full-screen application and that, in most cases, a windowed application can skip most of these steps.</span></span>

1.  <span data-ttu-id="40eae-109">Inicialmente, o aplicativo deve enumerar os adaptadores de vídeo no sistema.</span><span class="sxs-lookup"><span data-stu-id="40eae-109">Initially, the application must enumerate the display adapters on the system.</span></span> <span data-ttu-id="40eae-110">Um adaptador é uma parte física do hardware.</span><span class="sxs-lookup"><span data-stu-id="40eae-110">An adapter is a physical piece of hardware.</span></span> <span data-ttu-id="40eae-111">Observe que a placa gráfica pode conter mais de um único adaptador, como é o caso com uma exibição de duas pontas.</span><span class="sxs-lookup"><span data-stu-id="40eae-111">Note that the graphics card might contain more than a single adapter, as is the case with a dual-headed display.</span></span> <span data-ttu-id="40eae-112">Os aplicativos que não se preocupam com o suporte a vários monitores podem ignorar essa etapa e passar D3DADAPTER \_ por padrão para o método [**IDirect3D9:: EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="40eae-112">Applications that are not concerned with multi-monitor support can disregard this step, and pass D3DADAPTER\_DEFAULT to the [**IDirect3D9::EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) method in step 2.</span></span>
2.  <span data-ttu-id="40eae-113">Para cada adaptador, o aplicativo enumera os modos de exibição com suporte chamando [**IDirect3D9:: EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span><span class="sxs-lookup"><span data-stu-id="40eae-113">For each adapter, the application enumerates the supported display modes by calling [**IDirect3D9::EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span>
3.  <span data-ttu-id="40eae-114">Se necessário, o aplicativo verifica a presença de aceleração de hardware em cada modo de exibição enumerado chamando [**IDirect3D9:: CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype), conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="40eae-114">If required, the application checks for the presence of hardware acceleration in each enumerated display mode by calling [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype), as shown in the following code example.</span></span> <span data-ttu-id="40eae-115">Observe que esse é apenas um dos usos possíveis para **IDirect3D9:: CheckDeviceType**; para obter detalhes, consulte [determinando o suporte de hardware (Direct3D 9)](determining-hardware-support.md).</span><span class="sxs-lookup"><span data-stu-id="40eae-115">Note that this is only one of the possible uses for **IDirect3D9::CheckDeviceType**; for details, see [Determining Hardware Support (Direct3D 9)](determining-hardware-support.md).</span></span>
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

    

4.  <span data-ttu-id="40eae-116">O aplicativo verifica o nível de funcionalidade desejado para o dispositivo nesse adaptador chamando o método [**IDirect3D9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) .</span><span class="sxs-lookup"><span data-stu-id="40eae-116">The application checks for the desired level of functionality for the device on this adapter by calling the [**IDirect3D9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) method.</span></span> <span data-ttu-id="40eae-117">A capacidade retornada por esse método é garantida como constante para um dispositivo em todos os modos de exibição, verificada por [**IDirect3D9:: CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype).</span><span class="sxs-lookup"><span data-stu-id="40eae-117">The capability returned by this method is guaranteed to be constant for a device across all display modes, verified by [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype).</span></span>
5.  <span data-ttu-id="40eae-118">Os dispositivos sempre podem ser renderizados em superfícies do formato de um modo de exibição enumerado que é suportado pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40eae-118">Devices can always render to surfaces of the format of an enumerated display mode that is supported by the device.</span></span> <span data-ttu-id="40eae-119">Se o aplicativo precisar ser processado para uma superfície de um formato diferente, ele poderá chamar [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span><span class="sxs-lookup"><span data-stu-id="40eae-119">If the application is required to render to a surface of a different format, it can call [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span></span> <span data-ttu-id="40eae-120">Se o dispositivo puder renderizar para o formato, será garantido que todos os recursos retornados por [**IDirect3D9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) sejam aplicáveis.</span><span class="sxs-lookup"><span data-stu-id="40eae-120">If the device can render to the format, then it is guaranteed that all capabilities returned by [**IDirect3D9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) are applicable.</span></span>
6.  <span data-ttu-id="40eae-121">Por fim, o aplicativo pode determinar se as técnicas de multiamostragem, como anti-aliasing em cena completa, têm suporte para um formato de renderização usando o método [**IDirect3D9:: CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) .</span><span class="sxs-lookup"><span data-stu-id="40eae-121">Lastly, the application can determine if multisampling techniques, such as full-scene antialiasing, are supported for a render format by using the [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) method.</span></span>

<span data-ttu-id="40eae-122">Depois de concluir as etapas anteriores, o aplicativo deve ter uma lista de modos de exibição nos quais ele pode operar.</span><span class="sxs-lookup"><span data-stu-id="40eae-122">After completing the preceding steps, the application should have a list of display modes in which it can operate.</span></span> <span data-ttu-id="40eae-123">A etapa final é verificar se há memória suficiente acessível ao dispositivo disponível para acomodar o número necessário de buffers e de anti-aliasing.</span><span class="sxs-lookup"><span data-stu-id="40eae-123">The final step is to verify that enough device-accessible memory is available to accommodate the required number of buffers and antialiasing.</span></span> <span data-ttu-id="40eae-124">Esse teste é necessário porque o consumo de memória para a combinação de modo e de multiamostrabilidade é impossível de prever sem verificá-lo.</span><span class="sxs-lookup"><span data-stu-id="40eae-124">This test is necessary because the memory consumption for the mode and multisample combination is impossible to predict without verifying it.</span></span> <span data-ttu-id="40eae-125">Além disso, algumas arquiteturas de adaptadores de vídeo podem não ter uma quantidade constante de memória acessível ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40eae-125">Moreover, some display adapter architectures might not have a constant amount of device-accessible memory.</span></span> <span data-ttu-id="40eae-126">Isso significa que um aplicativo deve ser capaz de relatar falhas de memória fora do vídeo ao entrar no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="40eae-126">This means that an application should be able to report out-of-video-memory failures when going into full-screen mode.</span></span> <span data-ttu-id="40eae-127">Normalmente, um aplicativo deve remover o modo de tela inteira da lista de modos que ele oferece a um usuário, ou deve tentar consumir menos memória reduzindo o número de buffers de fundo ou usando uma técnica de várias amostras menos complexa.</span><span class="sxs-lookup"><span data-stu-id="40eae-127">Typically, an application should remove full-screen mode from the list of modes that it offers to a user, or it should attempt to consume less memory by reducing the number of back buffers or by using a less complex multisampling technique.</span></span>

<span data-ttu-id="40eae-128">Um aplicativo em janela executa um conjunto de tarefas semelhantes.</span><span class="sxs-lookup"><span data-stu-id="40eae-128">A windowed application performs a similar set of tasks.</span></span>

1.  <span data-ttu-id="40eae-129">Ele determina o retângulo da área de trabalho coberto pela área do cliente da janela.</span><span class="sxs-lookup"><span data-stu-id="40eae-129">It determines the desktop rectangle covered by the client area of the window.</span></span>
2.  <span data-ttu-id="40eae-130">Ele enumera adaptadores, procurando o adaptador cujo monitor cobre a área do cliente.</span><span class="sxs-lookup"><span data-stu-id="40eae-130">It enumerates adapters, looking for the adapter whose monitor covers the client area.</span></span> <span data-ttu-id="40eae-131">Se a área do cliente pertencer a mais de um adaptador, o aplicativo poderá optar por direcionar cada adaptador independentemente ou para orientar um único adaptador e ter pixels de transferência de Direct3D de um dispositivo para outro na apresentação.</span><span class="sxs-lookup"><span data-stu-id="40eae-131">If the client area is owned by more than one adapter, then the application can choose to drive each adapter independently, or to drive a single adapter and have Direct3D transfer pixels from one device to another at presentation.</span></span> <span data-ttu-id="40eae-132">O aplicativo também pode ignorar duas etapas anteriores e usar o \_ adaptador padrão D3DADAPTER.</span><span class="sxs-lookup"><span data-stu-id="40eae-132">The application can also disregard two preceding steps and use the D3DADAPTER\_DEFAULT adapter.</span></span> <span data-ttu-id="40eae-133">Observe que isso pode resultar em uma operação mais lenta quando a janela é colocada em um monitor secundário.</span><span class="sxs-lookup"><span data-stu-id="40eae-133">Note that this might result in slower operation when the window is placed on a secondary monitor.</span></span>
3.  <span data-ttu-id="40eae-134">O aplicativo deve chamar [**IDirect3D9:: CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype) para determinar se o dispositivo pode dar suporte à renderização em um buffer de fundo do formato especificado no modo de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="40eae-134">The application should call [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype) to determine if the device can support rendering to a back buffer of the specified format while in desktop mode.</span></span> <span data-ttu-id="40eae-135">[**IDirect3D9:: GetAdapterDisplayMode**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode) pode ser usado para determinar o formato de exibição da área de trabalho, conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="40eae-135">[**IDirect3D9::GetAdapterDisplayMode**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode) can be used to determine the desktop display format, as shown in the following code example.</span></span>
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

    

## <a name="related-topics"></a><span data-ttu-id="40eae-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="40eae-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40eae-137">Dispositivos Direct3D</span><span class="sxs-lookup"><span data-stu-id="40eae-137">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
