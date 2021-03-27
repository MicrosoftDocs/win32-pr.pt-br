---
title: Camadas de software
description: O tempo de execução do Direct3D 11 é construído com camadas, começando com a funcionalidade básica no núcleo e criando a funcionalidade opcional e auxiliar de desenvolvedor em camadas externas. Esta seção descreve a funcionalidade de cada camada.
ms.assetid: c545983c-5351-42a9-82e5-deea73aa035f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb05658860e678e8020392cb046a634e3b03c7c2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499050"
---
# <a name="software-layers"></a><span data-ttu-id="cbe16-104">Camadas de software</span><span class="sxs-lookup"><span data-stu-id="cbe16-104">Software Layers</span></span>

<span data-ttu-id="cbe16-105">O tempo de execução do Direct3D 11 é construído com camadas, começando com a funcionalidade básica no núcleo e criando a funcionalidade opcional e auxiliar de desenvolvedor em camadas externas.</span><span class="sxs-lookup"><span data-stu-id="cbe16-105">The Direct3D 11 runtime is constructed with layers, starting with the basic functionality at the core and building optional and developer-assist functionality in outer layers.</span></span> <span data-ttu-id="cbe16-106">Esta seção descreve a funcionalidade de cada camada.</span><span class="sxs-lookup"><span data-stu-id="cbe16-106">This section describes the functionality of each layer.</span></span>

<span data-ttu-id="cbe16-107">Como regra geral, as camadas adicionam funcionalidade, mas não modificam o comportamento existente.</span><span class="sxs-lookup"><span data-stu-id="cbe16-107">As a general rule, layers add functionality, but do not modify existing behavior.</span></span> <span data-ttu-id="cbe16-108">Por exemplo, as funções principais terão os mesmos valores de retorno independentes da camada de depuração que está sendo instanciada, embora a saída de depuração adicional possa ser fornecida se a camada de depuração for instanciada.</span><span class="sxs-lookup"><span data-stu-id="cbe16-108">For example, core functions will have the same return values independent of the debug layer being instantiated, although additional debug output may be provided if the debug layer is instantiated.</span></span>

<span data-ttu-id="cbe16-109">Para criar camadas quando um dispositivo é criado, chame [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) ou [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) e forneça um ou mais valores de [**\_ sinalizador de \_ dispositivo \_ D3D11 criar**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) .</span><span class="sxs-lookup"><span data-stu-id="cbe16-109">To create layers when a device is created, call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) and supply one or more [**D3D11\_CREATE\_DEVICE\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) values.</span></span>

<span data-ttu-id="cbe16-110">O Direct3D 11 fornece as seguintes camadas de tempo de execução:</span><span class="sxs-lookup"><span data-stu-id="cbe16-110">Direct3D 11 provides the following runtime layers:</span></span>

-   [<span data-ttu-id="cbe16-111">Camada principal</span><span class="sxs-lookup"><span data-stu-id="cbe16-111">Core Layer</span></span>](#core-layer)
-   [<span data-ttu-id="cbe16-112">Camada de depuração</span><span class="sxs-lookup"><span data-stu-id="cbe16-112">Debug Layer</span></span>](#debug-layer)
-   [<span data-ttu-id="cbe16-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cbe16-113">Related topics</span></span>](#related-topics)

## <a name="core-layer"></a><span data-ttu-id="cbe16-114">Camada principal</span><span class="sxs-lookup"><span data-stu-id="cbe16-114">Core Layer</span></span>

<span data-ttu-id="cbe16-115">A camada principal existe por padrão; fornecendo um mapeamento muito fino entre a API e o driver de dispositivo, minimizando a sobrecarga para chamadas de alta frequência.</span><span class="sxs-lookup"><span data-stu-id="cbe16-115">The core layer exists by default; providing a very thin mapping between the API and the device driver, minimizing overhead for high-frequency calls.</span></span> <span data-ttu-id="cbe16-116">Como a camada principal é essencial para o desempenho, ela executa apenas a validação crítica.</span><span class="sxs-lookup"><span data-stu-id="cbe16-116">As the core layer is essential for performance, it only performs critical validation.</span></span> <span data-ttu-id="cbe16-117">As camadas restantes são opcionais.</span><span class="sxs-lookup"><span data-stu-id="cbe16-117">The remaining layers are optional.</span></span>

## <a name="debug-layer"></a><span data-ttu-id="cbe16-118">Camada de depuração</span><span class="sxs-lookup"><span data-stu-id="cbe16-118">Debug Layer</span></span>

<span data-ttu-id="cbe16-119">A camada de depuração fornece um parâmetro adicional e validação de consistência (como validação de vínculo de sombreador e vinculação de recursos, validação de consistência de parâmetro e descrições de erro de relatório).</span><span class="sxs-lookup"><span data-stu-id="cbe16-119">The debug layer provides extensive additional parameter and consistency validation (such as validating shader linkage and resource binding, validating parameter consistency, and reporting error descriptions).</span></span>

<span data-ttu-id="cbe16-120">Para criar um dispositivo que dê suporte à camada de depuração, você deve instalar o SDK do DirectX (para obter D3D11SDKLayers.dll) e, em seguida, especificar o sinalizador de **\_ \_ \_ depuração do dispositivo D3D11 Create** ao chamar a função [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) ou a função [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) .</span><span class="sxs-lookup"><span data-stu-id="cbe16-120">To create a device that supports the debug layer, you must install the DirectX SDK (to get D3D11SDKLayers.dll), and then specify the **D3D11\_CREATE\_DEVICE\_DEBUG** flag when calling the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function or the [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) function.</span></span> <span data-ttu-id="cbe16-121">Se você executar o aplicativo com a camada de depuração habilitada, o aplicativo será consideravelmente mais lento.</span><span class="sxs-lookup"><span data-stu-id="cbe16-121">If you run your application with the debug layer enabled, the application will be substantially slower.</span></span> <span data-ttu-id="cbe16-122">Mas, para garantir que seu aplicativo esteja sem erros e avisos antes de enviá-lo, use a camada de depuração.</span><span class="sxs-lookup"><span data-stu-id="cbe16-122">But, to ensure that your application is clean of errors and warnings before you ship it, use the debug layer.</span></span> <span data-ttu-id="cbe16-123">Para obter mais informações, consulte [usando a camada de depuração para depurar aplicativos](using-the-debug-layer-to-test-apps.md).</span><span class="sxs-lookup"><span data-stu-id="cbe16-123">For more info, see [Using the debug layer to debug apps](using-the-debug-layer-to-test-apps.md).</span></span>


> [!Note]  
> <span data-ttu-id="cbe16-124">Para o Windows 7 com a atualização de plataforma para Windows 7 (KB2670838) ou Windows 8. x, para criar um dispositivo que dê suporte à camada de depuração, instale o SDK (Software Development Kit) do Windows para Windows 8. x para obter o D3D11 \_1SDKLayers.dll.</span><span class="sxs-lookup"><span data-stu-id="cbe16-124">For Windows 7 with Platform Update for Windows 7 (KB2670838) or Windows 8.x, to create a device that supports the debug layer, install the Windows Software Development Kit (SDK) for Windows 8.x to get D3D11\_1SDKLayers.dll.</span></span>


> [!Note]  
> <span data-ttu-id="cbe16-125">Para o Windows 10, para criar um dispositivo que dê suporte à camada de depuração, habilite o recurso opcional "ferramentas de gráficos".</span><span class="sxs-lookup"><span data-stu-id="cbe16-125">For Windows 10, to create a device that supports the debug layer, enable the "Graphics Tools" optional feature.</span></span> <span data-ttu-id="cbe16-126">Vá para o painel configurações, em sistema, aplicativos & recursos, gerencie recursos opcionais, adicione um recurso e procure "ferramentas de gráficos".</span><span class="sxs-lookup"><span data-stu-id="cbe16-126">Go to the Settings panel, under System, Apps & features, Manage optional Features, Add a feature, and then look for "Graphics Tools".</span></span>


> [!Note]  
> <span data-ttu-id="cbe16-127">Para obter informações sobre como depurar aplicativos DirectX remotamente, consulte [Depurando aplicativos DirectX remotamente](/windows/desktop/direct3dtools/debugging-directx-apps-remotely).</span><span class="sxs-lookup"><span data-stu-id="cbe16-127">For info about how to debug DirectX apps remotely, see [Debugging DirectX apps remotely](/windows/desktop/direct3dtools/debugging-directx-apps-remotely).</span></span>

 

<span data-ttu-id="cbe16-128">Como alternativa, você pode habilitar/desabilitar o sinalizador de depuração usando o [painel de controle do DirectX](/previous-versions//bb219725(v=vs.85)) incluído como parte do SDK do DirectX.</span><span class="sxs-lookup"><span data-stu-id="cbe16-128">Alternately, you can enable/disable the debug flag using the [DirectX Control Panel](/previous-versions//bb219725(v=vs.85)) included as part of the DirectX SDK.</span></span>

<span data-ttu-id="cbe16-129">Quando a camada de depuração lista vazamentos de memória, ela gera uma lista de ponteiros de interface de objeto junto com seus nomes amigáveis.</span><span class="sxs-lookup"><span data-stu-id="cbe16-129">When the debug layer lists memory leaks, it outputs a list of object interface pointers along with their friendly names.</span></span> <span data-ttu-id="cbe16-130">O nome amigável padrão é " &lt; sem nome &gt; ".</span><span class="sxs-lookup"><span data-stu-id="cbe16-130">The default friendly name is "&lt;unnamed&gt;".</span></span> <span data-ttu-id="cbe16-131">Você pode definir o nome amigável usando o método [**ID3D11DeviceChild:: SetPrivateData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicechild-setprivatedata) e o GUID **WKPDID \_ D3DDebugObjectName** que está em D3Dcommon. h.</span><span class="sxs-lookup"><span data-stu-id="cbe16-131">You can set the friendly name by using the [**ID3D11DeviceChild::SetPrivateData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicechild-setprivatedata) method and the **WKPDID\_D3DDebugObjectName** GUID that is in D3Dcommon.h.</span></span> <span data-ttu-id="cbe16-132">Por exemplo, para nomear pTexture com um nome SDKLayer de mytexture.jpg, use o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="cbe16-132">For example, to name pTexture with a SDKLayer name of mytexture.jpg, use the following code:</span></span>


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



<span data-ttu-id="cbe16-133">Normalmente, você deve compilar essas chamadas fora de sua versão de produção.</span><span class="sxs-lookup"><span data-stu-id="cbe16-133">Typically, you should compile these calls out of your production version.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbe16-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cbe16-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbe16-135">Dispositivos</span><span class="sxs-lookup"><span data-stu-id="cbe16-135">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 