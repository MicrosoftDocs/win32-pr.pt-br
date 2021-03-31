---
title: Compartilhamento de superfície entre as APIs de gráficos do Windows
description: Este tópico fornece uma visão geral técnica da interoperabilidade usando o compartilhamento de superfície entre as APIs de gráficos do Windows, incluindo Direct3D 11, Direct2D, DirectWrite, Direct3D 10 e Direct3D 9Ex.
ms.assetid: 65abf33e-3d15-42ff-99bd-674f24da773e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d889797902c964e603adefc51b25039afca7d46
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "103641965"
---
# <a name="surface-sharing-between-windows-graphics-apis"></a>Compartilhamento de superfície entre as APIs de gráficos do Windows

Este tópico fornece uma visão geral técnica da interoperabilidade usando o compartilhamento de superfície entre as APIs de gráficos do Windows, incluindo Direct3D 11, Direct2D, DirectWrite, Direct3D 10 e Direct3D 9Ex. Se você já tiver um conhecimento prático dessas APIs, este documento poderá ajudá-lo a usar várias APIs para renderizar a mesma superfície em um aplicativo projetado para os sistemas operacionais Windows 7 ou Windows Vista. Este tópico também fornece diretrizes de práticas recomendadas e ponteiros para recursos adicionais.

> [!Note]  
> Para a interoperabilidade Direct2D e DirectWrite no tempo de execução do DirectX 11,1, você pode usar [dispositivos Direct2D e contextos de dispositivo](/windows/desktop/Direct2D/devices-and-device-contexts) para renderizar diretamente em dispositivos Direct3D 11.

 

Este tópico inclui as seções a seguir.

-   [Introdução](#introduction)
-   [Visão geral da interoperabilidade de API](#api-interoperability-overview)
-   [Cenários de interoperabilidade](#interoperability-scenarios)
    -   [Compartilhamento de dispositivo Direct3D 10,1 com Direct2D](#direct3d-101-device-sharing-with-direct2d)
    -   [Superfícies compartilhadas sincronizadas do DXGI 1,1](#dxgi-11-synchronized-shared-surfaces)
    -   [Interoperabilidade entre as APIs baseadas em Direct3D 9Ex e DXGI](#interoperability-between-direct3d-9ex-and-dxgi-based-apis)
-   [Conclusão](#conclusion)

## <a name="introduction"></a>Introdução

Neste documento, a interoperabilidade da API gráfica do Windows refere-se ao compartilhamento da mesma superfície de renderização por APIs diferentes. Esse tipo de interoperabilidade permite que os aplicativos criem exibições atraentes aproveitando várias APIs de gráficos do Windows e facilitam a migração para novas tecnologias, mantendo a compatibilidade com as APIs existentes.

No Windows 7 (e no Windows Vista SP2 com o Windows 7 Interop Pack, vista 7IP), as APIs de renderização de gráficos são Direct3D 11, Direct2D, Direct3D 10,1, Direct3D 10,0, Direct3D 9Ex, Direct3D 9c e anteriores do Direct3D APIs, bem como GDI e GDI+. O Windows Imaging Component (WIC) e o DirectWrite são tecnologias relacionadas para processamento de imagens e o Direct2D executa a renderização de texto. A API de aceleração de vídeo do DirectX (DXVA), baseada no Direct3D 9c e no Direct3D 9Ex, é usada para processamento de vídeo.

À medida que as APIs de gráficos do Windows evoluem para serem baseadas em Direct3D, a Microsoft está investindo mais esforço na garantia de interoperabilidade entre as APIs. APIs do Direct3D e APIs de nível mais alto desenvolvidas com base em APIs do Direct3D também fornecem suporte quando necessário para a compatibilidade de ponte com APIs mais antigas. Para ilustrar, os aplicativos Direct2D podem usar o Direct3D 10,1 compartilhando um dispositivo Direct3D 10,1. Além disso, as APIs do Direct3D 11, Direct2D e Direct3D 10,1 podem aproveitar a (infraestrutura de gráficos do DirectX) 1,1, que permite superfícies compartilhadas sincronizadas que dão suporte total à interoperabilidade entre essas APIs. As APIs baseadas em DXGI 1,1 interoperam com GDI e com GDI+ por associação, obtendo o contexto do dispositivo GDI de uma superfície do DXGI 1,1. Para obter mais informações, consulte a documentação de interoperabilidade de DXGI e GDI disponível no MSDN.

O compartilhamento de superfície não sincronizado tem suporte do tempo de execução do Direct3D 9Ex. Os aplicativos de vídeo baseados em DXVA podem usar o auxiliar de interoperabilidade do Direct3D 9Ex e DXGI para a interoperabilidade de DXVA baseada em Direct3D 9Ex com o Direct3D 11 para o sombreador de computação ou podem interoperar com Direct2D para controles 2D ou renderização de texto. O WIC e o DirectWrite também interoperam com GDI, Direct2D e por associação, outras APIs do Direct3D.

O Direct3D 10,0, o Direct3D 9c e os tempos de execução do Direct3D mais antigos não oferecem suporte a superfícies compartilhadas. As cópias de memória do sistema continuarão sendo usadas para interoperabilidade com APIs baseadas em GDI ou DXGI.

Observe que os cenários de interoperabilidade neste documento referem-se a várias APIs de gráficos Renderizando em uma superfície de renderização compartilhada, em vez de na mesma janela do aplicativo. A sincronização de APIs separadas que visam superfícies diferentes que são compostas na mesma janela está fora do escopo deste documento.

## <a name="api-interoperability-overview"></a>Visão geral da interoperabilidade de API

A interoperabilidade do compartilhamento de superfície de APIs de gráficos do Windows pode ser descrita em termos de cenários de API para API e a funcionalidade de interoperabilidade correspondente. A partir do Windows 7 e a partir do Windows Vista SP2 com 7IP, novas APIs e tempos de execução associados incluem Direct2D e tecnologias relacionadas: Direct3D 11 e DXGI 1,1. O desempenho do GDI também foi aprimorado no Windows 7. O Direct3D 10,1 foi introduzido no Windows Vista SP1. O diagrama a seguir mostra o suporte de interoperabilidade entre APIs.

![diagrama de suporte de interoperabilidade entre APIs de gráficos do Windows](images/surface-sharing-interoperability.png)

Neste diagrama, as setas mostram cenários de interoperabilidade nos quais a mesma superfície pode ser acessível pelas APIs conectadas. As setas azuis indicam mecanismos de interoperabilidade introduzidos no Windows Vista. As setas verdes indicam o suporte de interoperabilidade para novas APIs ou aprimoramentos que ajudam as APIs mais antigas a interoperar com as APIs mais recentes. Por exemplo, as setas verdes representam o compartilhamento de dispositivos, o suporte à superfície compartilhada sincronizada, o auxiliar de sincronização do Direct3D 9Ex/DXGI e a obtenção de um contexto de dispositivo GDI de uma superfície compatível.

## <a name="interoperability-scenarios"></a>Cenários de interoperabilidade

A partir do Windows 7 e do Windows Vista 7IP, as ofertas principais das APIs de gráficos do Windows dão suporte à renderização de várias APIs na mesma superfície de DXGI 1,1.

**Direct3D 11, Direct3D 10,1, Direct2D – interoperabilidade entre si**

As APIs do Direct3D 11, Direct3D 10,1 e Direct2D (e suas APIs relacionadas, como DirectWrite e WIC) podem interoperar entre si usando o compartilhamento de dispositivo Direct3D 10,1 ou superfícies compartilhadas sincronizadas.

### <a name="direct3d-101-device-sharing-with-direct2d"></a>Compartilhamento de dispositivo Direct3D 10,1 com Direct2D

O compartilhamento de dispositivos entre o Direct2D e o Direct3D 10,1 permite que um aplicativo use ambas as APIs para renderizar de forma direta e eficiente na mesma superfície do DXGI 1,1, usando o mesmo objeto de dispositivo Direct3D subjacente. O Direct2D fornece a capacidade de chamar APIs Direct2D usando um dispositivo Direct3D 10,1 existente, aproveitando o fato de que o Direct2D é criado sobre os tempos de execução do Direct3D 10,1 e DXGI 1,1. Os trechos de código a seguir ilustram como o Direct2D Obtém o destino de renderização de dispositivo Direct3D 10,1 de uma superfície DXGI 1,1 associada ao dispositivo. O destino de renderização do dispositivo Direct3D 10,1 pode executar chamadas de desenho Direct2D entre as APIs BeginDraw e EndDraw.


```C++
// Direct3D 10.1 Device and Swapchain creation
HRESULT hr = D3D10CreateDeviceandSwapChain1(
                pAdapter,
                DriverType,
                Software,
                D3D10_CREATE_DEVICE_BGRA_SUPPORT,
                featureLevel,
                D3D10_1_SDK_VERSION,
                pSwapChainDesc,
                &pSwapChain,
                &pDevice
                );

hr = pSwapChain->GetBuffer(
        0,
        __uuidof(IDXGISurface),
        (void **)&pDXGIBackBuffer
        ));

// Direct3D 10.1 API rendering calls
...

hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &m_spD2DFactory
        ));

pD2DFactory->CreateDxgiSurfaceRenderTarget(
        pDXGIBackBuffer,
        &renderTargetProperties,
        &pD2DBackBufferRenderTarget
        ));
...

pD2DBackBufferRenderTarget->BeginDraw();
//Direct2D API rendering calls
...

pD2DBackBufferRenderTarget->EndDraw();

pSwapChain->Present(0, 0);
```



**Comentários**

-   O dispositivo Direct3D 10,1 associado deve dar suporte ao formato BGRA. Esse dispositivo foi criado chamando D3D10CreateDevice1 com o parâmetro D3D10 \_ criar \_ dispositivo \_ BGRA \_ suporte. O formato BGRA tem suporte a partir do nível de recurso 9,1 do Direct3D 10.
-   O aplicativo não deve criar várias ID2D1RenderTargets associando ao mesmo dispositivo Direct3D 10.1.
-   Para obter um desempenho ideal, mantenha pelo menos um recurso em todos os momentos, como texturas ou superfícies associadas ao dispositivo.

O compartilhamento de dispositivo é adequado para uso em processo e de thread único de um dispositivo de renderização compartilhado por APIs de renderização Direct3D 10,1 e Direct2D. As superfícies de compartilhamento sincronizadas permitem o uso de vários threads, em processo e fora do processo de vários dispositivos de renderização usados pelas APIs do Direct3D 10,1, Direct2D e Direct3D 11.

Outro método de interoperabilidade entre Direct3D 10,1 e Direct2D é usando ID3D1RenderTarget:: CreateSharedBitmap, que cria um objeto ID2D1Bitmap de IDXGISurface. Você pode escrever uma cena do Direct3D 10.1 no bitmap e renderizá-la com Direct2D. Para obter mais informações, consulte [método ID2D1RenderTarget:: CreateSharedBitmap](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap).

### <a name="direct2d-software-rasterization"></a>Rasterização de software Direct2D

Não há suporte para o compartilhamento de dispositivos com o Direct3D 10,1 ao usar o processador de software Direct2D, por exemplo, especificando D2D1 \_ \_ renderização de destino \_ \_ forçada de \_ \_ processamento de software em d2d1 \_ renderizar \_ o uso de destino \_ ao criar um destino de renderização Direct2D.

O Direct2D pode usar o rasterizador de software WARP10 para compartilhar o dispositivo com o Direct3D 10 ou o Direct3D 11, mas o desempenho diminui significativamente.

### <a name="dxgi-11-synchronized-shared-surfaces"></a>Superfícies compartilhadas sincronizadas do DXGI 1,1

As APIs do Direct3D 11, Direct3D 10,1 e Direct2D usam DXGI 1,1, que fornece a funcionalidade para sincronizar a leitura e gravação na mesma superfície de memória de vídeo (DXGISurface1) por dois ou mais dispositivos Direct3D. Os dispositivos de renderização que usam superfícies compartilhadas sincronizadas podem ser dispositivos Direct3D 10,1 ou Direct3D 11, cada um executando no mesmo processo ou processos cruzados.

Os aplicativos podem usar superfícies compartilhadas sincronizadas para interoperar entre qualquer dispositivo baseado em DXGI 1,1, como o Direct3D 11 e o Direct3D 10,1, ou entre o Direct3D 11 e o Direct2D, obtendo o dispositivo Direct3D 10,1 do objeto de destino Direct2D render.

No Direct3D 10,1 e nas APIs posteriores, para usar DXGI 1,1, verifique se o dispositivo Direct3D foi criado usando um objeto de adaptador de 1,1 DXGI, que é enumerado a partir do objeto de fábrica do DXGI 1,1. Chame CreateDXGIFactory1 para criar o objeto IDXGIFactory1 e EnumAdapters1 para enumerar o objeto IDXGIAdapter1. O objeto IDXGIAdapter1 precisa ser passado como parte da chamada D3D10CreateDevice ou D3D10CreateDeviceAndSwapChain. Para obter mais informações sobre APIs de DXGI 1,1, consulte o [Guia de programação para dxgi](https://msdn.microsoft.com/library/ee418147(VS.85).aspx).

### <a name="apis"></a>APIs

**D3D10 \_ \_ \_ dishared \_ KEYEDMUTEX de recursos**  
Ao criar o recurso compartilhado sincronizado, defina \_ d3d10 \_ do recurso variado \_ \_ KEYEDMUTEX no \_ sinalizador de recurso variado do d3d10 \_ \_ .  


```C++
typedef enum D3D10_RESOURCE_MISC_FLAG {
    D3D10_RESOURCE_MISC_GENERATE_MIPS      = 0x1L,
    D3D10_RESOURCE_MISC_SHARED             = 0x2L,
    D3D10_RESOURCE_MISC_TEXTURECUBE        = 0x4L,
    D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX  = 0x10L,
    D3D10_RESOURCE_MISC_GDI_COMPATIBLE     = 0x20L,
}   D3D10_RESOURCE_MISC_FLAG;
```



**D3D10 \_ \_ \_ dishared \_ KEYEDMUTEX de recursos**  
Habilita o recurso criado para ser sincronizado usando as APIs IDXGIKeyedMutex:: AcquireSync e ReleaseSync. As seguintes APIs do Direct3D 10,1 de criação de recursos que usam um \_ parâmetro de sinalizador variado de recurso d3d10 foram \_ \_ estendidas para dar suporte ao novo sinalizador.  

-   ID3D10Device1::CreateTexture1D
-   ID3D10Device1::CreateTexture2D
-   ID3D10Device1::CreateTexture3D
-   ID3D10Device1:: CreateBuffer

  
Se qualquer uma das funções listadas for chamada com o \_ \_ sinalizador de \_ KEYEDMUTEX d3d10 dishared do recurso \_ , a interface retornada poderá ser consultada para uma interface IDXGIKeyedMutex, que implementa APIs AcquireSync e ReleaseSync para sincronizar o acesso à superfície. O dispositivo que cria a superfície e qualquer outro dispositivo que abra a superfície (usando OpenSharedResource) é necessário para chamar IDXGIKeyedMutex:: AcquireSync antes de qualquer comando de renderização na superfície e IDXGIKeyedMutex:: ReleaseSync quando a renderização é concluída.  
Os dispositivos WARP e REF não dão suporte a recursos compartilhados. A tentativa de criar um recurso com esse sinalizador em um dispositivo WARP ou REF fará com que o método Create retorne um \_ código de erro E OUTOFMEMORY.  
**INTERFACE IDXGIKEYEDMUTEX**  
Uma nova interface no DXGI 1,1, IDXGIKeyedMutex, representa um mutex com chave, que permite o acesso exclusivo a um recurso compartilhado que é usado por vários dispositivos. Para obter a documentação de referência sobre essa interface e seus dois métodos, AcquireSync e ReleaseSync, consulte [IDXGIKeyedMutex](https://msdn.microsoft.com/library/ee421920(VS.85).aspx).  
</dl>

### <a name="sample-synchronized-surface-sharing-between-two-direct3d-101-devices"></a>Exemplo: compartilhamento de superfície sincronizado entre dois dispositivos Direct3D 10,1

O exemplo a seguir ilustra o compartilhamento de uma superfície entre dois dispositivos Direct3D 10,1. A superfície compartilhada sincronizada é criada por um dispositivo Direct3D 10.1.


```C++
// Create Sync Shared Surface using Direct3D10.1 Device 1.
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = width;
desc.Height = height;
desc.MipLevels = 1;
desc.ArraySize = 1;
// must match swapchain format in order to CopySubresourceRegion.
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
// creates 2D texture as a Synchronized Shared Surface.
desc.MiscFlags = D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;
ID3D10Texture2D* g_pShared = NULL;
g_pd3dDevice1->CreateTexture2D( &desc, NULL, &g_pShared );

// QI IDXGIResource interface to synchronized shared surface.
IDXGIResource* pDXGIResource = NULL;
g_pShared->QueryInterface(__uuidof(IDXGIResource), (LPVOID*) &pDXGIResource);

// obtain handle to IDXGIResource object.
pDXGIResource->GetSharedHandle(&g_hsharedHandle);
pDXGIResource->Release();
if ( !g_hsharedHandle )
    return E_FAIL;

// QI IDXGIKeyedMutex interface of synchronized shared surface's resource handle.
hr = g_pShared->QueryInterface( __uuidof(IDXGIKeyedMutex),
    (LPVOID*)&g_pDXGIKeyedMutex_dev1 );
If ( FAILED( hr ) || ( g_pDXGIKeyedMutex_dev1 == NULL ) )
    return E_FAIL;
```



O mesmo dispositivo Direct3D 10.1 pode obter a superfície compartilhada sincronizada para renderização chamando AcquireSync e, em seguida, liberando a superfície para a renderização do outro dispositivo chamando ReleaseSync. Quando não estiver compartilhando a superfície compartilhada sincronizada com qualquer outro dispositivo Direct3D, o criador poderá obter e liberar a superfície compartilhada sincronizada (para iniciar e encerrar a renderização) adquirindo e liberando usando o mesmo valor de chave.


```C++
// Obtain handle to Sync Shared Surface created by Direct3D10.1 Device 1.
hr = g_pd3dDevice2->OpenSharedResource( g_hsharedHandle,__uuidof(ID3D10Texture2D),
                                        (LPVOID*) &g_pdev2Shared);
if (FAILED (hr))
    return hr;
hr = g_pdev2Shared->QueryInterface( __uuidof(IDXGIKeyedMutex),
                                    (LPVOID*) &g_pDXGIKeyedMutex_dev2);
if( FAILED( hr ) || ( g_pDXGIKeyedMutex_dev2 == NULL ) )
    return E_FAIL;

// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 2.
UINT acqKey = 1;
UINT relKey = 0;
DWORD timeOut = 5;
DWORD result = g_pDXGIKeyedMutex_dev2->AcquireSync(acqKey, timeOut);
if ( result == WAIT_OBJECT_0 )
    // Rendering calls using Device 2.
else
    // Handle unable to acquire shared surface error.
result = g_pDXGIKeyedMutex_dev2->ReleaseSync(relKey));
if (result == WAIT_OBJECT_0)
    return S_OK;
```



O segundo dispositivo Direct3D 10.1 pode obter a superfície compartilhada sincronizada para renderização chamando AcquireSync e, em seguida, liberando a superfície para a renderização do primeiro dispositivo chamando ReleaseSync. Observe que o dispositivo 2 é capaz de adquirir a superfície compartilhada sincronizada usando o mesmo valor de chave que aquela especificada na chamada ReleaseSync pelo dispositivo 1.


```C++
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 1.
UINT acqKey = 0;
UINT relKey = 1;
DWORD timeOut = 5;
DWORD result = g_pDXGIKeyedMutex_dev1->AcquireSync(acqKey, timeOut);
if (result == WAIT_OBJECT_0)
    // Rendering calls using Device 1.
else
    // Handle unable to acquire shared surface error.
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(relKey));
if ( result == WAIT_OBJECT_0 )
    return S_OK;
```



Dispositivos adicionais que compartilham a mesma superfície podem assumir a compra e a liberação da superfície usando chaves adicionais, conforme mostrado nas chamadas a seguir.


```C++
// Within Device 1's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 1
result = g_pDXGIKeyedMutex_dev1->AcquireSync(0, timeOut);
// Rendering calls using Device 1
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(1);
...
////////////////////////////////////////////////////////////////////////////
// Within Device 2's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 2
result = g_pDXGIKeyedMutex_dev2->AcquireSync(1, timeOut);
// Rendering calls using Device 2
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(2);

////////////////////////////////////////////////////////////////////////////
// Within Device 3's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 3
result = g_pDXGIKeyedMutex_dev1->AcquireSync(2, timeOut);
// Rendering calls using Device 3
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(0);
...
```



Observe que um aplicativo do mundo real sempre pode ser renderizado para uma superfície intermediária que é então copiada na superfície compartilhada para evitar que um dispositivo espere em outro dispositivo que compartilhe a superfície.

### <a name="using-synchronized-shared-surfaces-with-direct2d-and-direct3d-11"></a>Usando superfícies compartilhadas sincronizadas com Direct2D e Direct3D 11

Da mesma forma, para o compartilhamento entre as APIs do Direct3D 11 e do Direct3D 10,1, uma superfície compartilhada sincronizada pode ser criada a partir de um dispositivo de API e compartilhada com os outros dispositivos de API, dentro ou fora do processo.

Os aplicativos que usam o Direct2D podem compartilhar um dispositivo Direct3D 10,1 e usar uma superfície compartilhada sincronizada para interoperar com o Direct3D 11 ou outros dispositivos do Direct3D 10,1, independentemente de eles pertencerem ao mesmo processo ou a processos diferentes. No entanto, para aplicativos de processo único, de thread único, o compartilhamento de dispositivo é o método mais alto de desempenho e eficiente de interoperabilidade entre o Direct2D e o Direct3D 10 ou o Direct3D 11.

### <a name="software-rasterizer"></a>Rasterizador de software

As superfícies compartilhadas não têm suporte quando os aplicativos usam os rasterizadores de software Direct3D ou Direct2D, incluindo o rasterizador de referência e a detorção, em vez de usar a aceleração de hardware de gráficos.

### <a name="interoperability-between-direct3d-9ex-and-dxgi-based-apis"></a>Interoperabilidade entre as APIs baseadas em Direct3D 9Ex e DXGI

As APIs do Direct3D 9Ex incluíam a noção de compartilhamento de superfície para permitir que outras APIs leiam da superfície compartilhada. Para compartilhar a leitura e a gravação em uma superfície compartilhada do Direct3D 9Ex, você deve adicionar a sincronização manual ao próprio aplicativo.

### <a name="direct3d-9ex-shared-surfaces-plus-manual-synchronization-helper"></a>Superfícies compartilhadas do Direct3D 9Ex, além do auxiliar de sincronização manual

A tarefa mais fundamental no Direct3D 9Ex e no Direct3D 10 ou 11 interoperabilidade é passar uma única superfície do primeiro dispositivo (dispositivo A) para o segundo (dispositivo B), de modo que quando o dispositivo B adquire um identificador na superfície, a renderização do dispositivo A é garantida para ser concluída. Portanto, o dispositivo B pode usar essa superfície sem se preocupar. Isso é muito semelhante ao problema clássico de produtor-consumidor e essa discussão modela o problema dessa maneira. O primeiro dispositivo que usa a superfície e, em seguida, o abandona é o produtor (dispositivo A) e o dispositivo que está aguardando inicialmente é o consumidor (dispositivo B). Qualquer aplicativo do mundo real é mais sofisticado do que isso e encadeará vários blocos de construção de produtor-consumidor para criar a funcionalidade desejada.

Os blocos de construção produtor-consumidor são implementados no auxiliar usando uma fila de superfícies. As superfícies são enfileiradas pelo produtor e removidas da fila pelo consumidor. O auxiliar apresenta três interfaces COM: ISurfaceQueue, ISurfaceProducer e ISurfaceConsumer.

### <a name="high-level-overview-of-helper"></a>High-Level visão geral do auxiliar

O objeto ISurfaceQueue é o bloco de construção para usar as superfícies compartilhadas. Ele é criado com um dispositivo Direct3D inicializado e uma descrição para criar um número fixo de superfícies compartilhadas. O objeto de fila gerencia a criação de recursos e a abertura de código. O número e o tipo de superfícies são fixos; Depois que as superfícies são criadas, o aplicativo não pode adicioná-las ou removê-las.

Cada instância do objeto ISurfaceQueue fornece um tipo de rua unidirecional que pode ser usada para enviar superfícies do dispositivo de produção para o dispositivo consumidor. Várias ruas unidirecionais podem ser usadas para habilitar cenários de compartilhamento de superfície entre dispositivos de aplicativos específicos.

**Tempo de vida de criação/objeto**  
Há duas maneiras de criar o objeto de fila: por meio de CreateSurfaceQueue, ou por meio do método clone de ISurfaceQueue. Como as interfaces são objetos COM, o gerenciamento de tempo de vida padrão COM é aplicável.  
**Modelo de produtor/consumidor**  
Enqueue (): o produtor chama essa função para indicar que ela é feita com a superfície, que agora pode ser disponibilizada para outro dispositivo. Ao retornar dessa função, o dispositivo produtor não tem mais direitos à superfície e não é seguro continuar a usá-lo.  
Remover da fila (): o dispositivo consumidor chama essa função para obter uma superfície compartilhada. A API garante que todas as superfícies removidas da fila estejam prontas para serem usadas.  
**Metadados**  
A API dá suporte à associação de metadados com as superfícies compartilhadas.  
Enqueue () tem a opção de especificar metadados adicionais que serão passados para o dispositivo de consumo. Os metadados devem ser menos do que um máximo conhecido no momento da criação.  
A remoção da fila () pode, opcionalmente, passar um buffer e um ponteiro para o tamanho do buffer. A fila preenche o buffer com os metadados da chamada de enfileiramento correspondente.  
**Clonar**  
Cada objeto ISurfaceQueue resolve uma sincronização unidirecional. Supomos que a grande maioria dos aplicativos que usam essa API usará um sistema fechado. O sistema fechado mais simples com dois dispositivos que enviam superfícies de volta e para trás requer duas filas. O objeto ISurfaceQueue tem um método clone () para possibilitar a criação de várias filas que fazem parte do mesmo pipeline maior.  
Clone cria um novo objeto ISurfaceQueue de um existente e compartilha todos os recursos abertos entre eles. O objeto resultante tem exatamente as mesmas superfícies que a fila de origem. As filas clonadas podem ter diferentes tamanhos de metadados uns dos outros.  
**Surfaces**  
O ISurfaceQueue assume a responsabilidade pela criação e gerenciamento de suas superfícies. Não é válido enfileirar superfícies arbitrárias. Além disso, uma superfície deve ter apenas um "proprietário" ativo. Ele deve estar em uma fila específica ou ser usado por um dispositivo específico. Não é válido tê-lo em várias filas ou para que os dispositivos continuem usando a superfície depois que ele é enfileirado.  
</dl>

### <a name="api-details"></a>Detalhes da API

### <a name="isurfacequeue"></a>IsurfaceQueue

A fila é responsável por criar e manter os recursos compartilhados. Ele também fornece a funcionalidade para encadear várias filas usando clone. A fila tem métodos que abrem o dispositivo de produção e um dispositivo de consumo. Somente um de cada pode ser aberto a qualquer momento.

A fila expõe as seguintes APIs:



|                             |                                                                                  |
|-----------------------------|----------------------------------------------------------------------------------|
| CreateSurfaceQueue          | Cria um objeto ISurfaceQueue (a fila "raiz").                              |
| ISurfaceQueue::OpenConsumer | Retorna uma interface para o dispositivo consumidor a ser removido da fila.                        |
| ISurfaceQueue::OpenProducer | Retorna uma interface para o dispositivo de produção a ser enfileirado.                        |
| ISurfaceQueue:: clone        | Cria um objeto ISurfaceQueue que compartilha superfícies com o objeto de fila raiz. |



 

**CreateSurfaceQueue**  


```C++
typedef struct SURFACE_QUEUE_DESC {
  UINT            Width;
  UINT            Height;
  DXGI_FORMAT     Format;
  UINT            NumSurfaces;
  UINT            MetaDataSize;
  DWORD           Flags;
} SURFACE_QUEUE_DESC;
```



**Membros**  

**Largura**, **altura**  das dimensões das superfícies compartilhadas. Todas as superfícies compartilhadas devem ter as mesmas dimensões.  
**Formato** O formato das superfícies compartilhadas. Todas as superfícies compartilhadas devem ter o mesmo formato. Os formatos válidos dependem dos dispositivos que serão usados, pois diferentes pares de dispositivos podem compartilhar tipos de formato diferentes.  
**NumSurfaces**  O número de superfícies que fazem parte da fila. Este é um número fixo.  
 **MetaDataSize**  O tamanho máximo do buffer de metadados.  
**Sinalizadores**  de  Sinalizadores para controlar o comportamento da fila. Consulte Observações.  



```C++
HRESULT CreateSurfaceQueue(
  [in]   SURFACE_QUEUE_DESC *pDesc,
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



**Parâmetros**

 *pDesc* \[ na \]  Descrição da fila de superfície compartilhada a ser criada.  

 *pDevice* \[ no \]  dispositivo que deve ser usado para criar as superfícies compartilhadas. Esse é um parâmetro explícito devido a um recurso do Windows Vista. Para superfícies compartilhadas entre o Direct3D 9 e o Direct3D 10, as superfícies devem ser criadas com o Direct3D 9.  

 *ppQueue* \[ out \]  no retorno, contém um ponteiro para o objeto ISurfaceQueue.  


**Valores de retorno**

Se *pDevice* não for capaz de compartilhar recursos, essa função retornará uma \_ chamada de erro dxgi \_ inválida \_ . Essa função cria os recursos. Se falhar, ele retornará um erro. Se for bem sucedido, retornará S \_ OK.

**Comentários**

Criar o objeto de fila também cria todas as superfícies. Todas as superfícies são consideradas como destinos de renderização em 2D e serão criadas com os sinalizadores de D3D10 de \_ destino de processamento de ligação \_ \_ e d3d10 \_ BIND \_ Shader \_ (ou os sinalizadores equivalentes para diferentes tempos de execução).

O desenvolvedor pode especificar um sinalizador que indica se a fila será acessada por vários threads. Se nenhum sinalizador for definido (**flags** = = 0), a fila será usada por vários threads. O desenvolvedor pode especificar o acesso de thread único, que desativa o código de sincronização e fornece uma melhoria de desempenho para esses casos. Cada fila clonada tem seu próprio sinalizador, portanto, é possível que filas diferentes no sistema tenham controles de sincronização diferentes.

 **Abrir um produtor**  


```C++
HRESULT OpenProducer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceProducer **ppProducer
);
```



**Parâmetros**  

*pDevice* \[ no\]  

O dispositivo produtor que enfileira as superfícies na fila de superfície. 

*ppProducer* \[ out \] retorna um objeto para a interface do produtor.  


**Valores de retorno**

Se o dispositivo não for capaz de compartilhar superfícies, retorna a \_ chamada de erro dxgi \_ inválido \_ .

**Abrir um consumidor**  


```C++
HRESULT OpenConsumer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceConsumer **ppConsumer
);
```



**Parâmetros**  
 *pDevice* \[ no\]  
 O dispositivo de consumidor que recoloca as superfícies da fila de superfície. 
 *ppConsumer* \[ out \]  retorna um objeto para a interface do consumidor.  


**Valores de retorno**

Se o dispositivo não for capaz de compartilhar superfícies, retorna a \_ chamada de erro dxgi \_ inválido \_ .

**Comentários**

Essa função abre todas as superfícies na fila para o dispositivo de entrada e as armazena em cache. As chamadas subsequentes para remover a fila simplesmente vão para o cache e não precisam reabrir as superfícies a cada vez.



### <a name="cloning-an-idxgixsurfacequeue"></a>Clonando um IDXGIXSurfaceQueue




```C++
typedef struct SHARED_SURFACE_QUEUE_CLONE_DESC {
  UINT         MetaDataSize;
  DWORD        Flags;
} SHARED_SURFACE_QUEUE_CLONE_DESC;
```



**Os membros** **MetaDataSize** e **flags** têm o mesmo comportamento que eles fazem para o CreateSurfaceQueue.  



```C++
HRESULT Clone(
  [in]   SHARED_SURFACE_QUEUE_CLONE_DESC *pDesc,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



**Parâmetros**

*pDesc* \[ em \] uma struct que fornece uma descrição do objeto de clonagem a ser criado. Esse parâmetro deve ser inicializado.  
*ppQueue* \[ out \] retorna o objeto Initialized.  
</dl>

**Comentários**

Você pode clonar de qualquer objeto de fila existente, mesmo que não seja a raiz.  
</dl>

### <a name="idxgixsurfaceconsumer"></a>IDXGIXSurfaceConsumer

<dl>


```C++
HRESULT Dequeue(
  [in]      REFIID    id,
  [out]     void      **ppSurface,
  [in,out]  void      *pBuffer,
  [in,out]  UINT      *pBufferSize,
  [in]      DWORD     dwTimeout
);
```



**Parâmetros**  
*ID* \[ em\]  
O REFIID de uma superfície 2D do dispositivo de consumo.  

-   Para um IDirect3DDevice9, o REFIID deve ser \_ \_ uuidof (IDirect3DTexture9).
-   Para um ID3D10Device, o REFIID deve ser \_ \_ uuidof (ID3D10Texture2D).
-   Para um ID3D11Device, o REFIID deve ser \_ \_ uuidof (ID3D11Texture2D).

*ppSurface* \[ out \] retorna um ponteiro para a superfície.  
*pBuffer* \[ no, \] um parâmetro opcional e, se não for **nulo**, no retorno, contém os metadados que foram passados na chamada de enfileiramento correspondente.  
*pBufferSize* \[ in, out \] o tamanho de *pBuffer*, em bytes. Retorna o número de bytes retornados em *pBuffer*. Se a chamada de enfileiramento não fornecer metadados, *pBuffer* será definido como 0.  
*dwTimeout* \[ em \] especifica um valor de tempo limite. Consulte os comentários para obter mais detalhes.  
</dl>

**Valores de retorno**

Essa função pode retornar \_ o tempo limite de espera se um valor de tempo limite for especificado e a função não retornar antes do valor de tempo limite. Consulte Observações. Se nenhuma superfície estiver disponível, a função retornará com *ppSurface* definido como **NULL**, *pBufferSize* definido como 0 e o valor de retorno será 0x80070120 (Win32 \_ para \_ HRESULT ( \_ tempo limite de espera)).  
</dl>

**Comentários**

Essa API pode bloquear se a fila estiver vazia. O parâmetro *dwTimeout* funciona de forma idêntica às APIs de sincronização do Windows, como WaitForSingleObject. Para o comportamento de não bloqueio, use um tempo limite de 0.  
</dl>

### <a name="isurfaceproducer"></a>ISurfaceProducer

Essa interface fornece dois métodos que permitem ao aplicativo enfileirar superfícies. Depois que uma superfície é enfileirada, o ponteiro de superfície não é mais válido e não é seguro de usar. A única ação que o aplicativo deve executar com o ponteiro é liberá-lo.



|                           |                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ISurfaceProducer:: enqueue | Enfileira uma superfície ao objeto de fila. Após a conclusão dessa chamada, o produtor é feito com a superfície e a superfície está pronta para outro dispositivo. |
| ISurfaceProducer:: flush   | Usado se os aplicativos tiverem um comportamento não bloqueado. Consulte Comentários para obter detalhes.                                                                  |



 

**Enfileirar**  


```C++
HRESULT Enqueue(
  [in]  IUnknown *pSurface,
  [in]  void *pBuffer,
  [in]  UINT BufferSize,
  [in]  DWORD Flags
);
```



**Parâmetros**  
*pSurface* \[ no\]  
A superfície do dispositivo de produção que precisa ser enfileirado. Essa superfície deve ser uma superfície removida da fila da mesma rede de fila. *pBuffer* \[ em \] um parâmetro opcional, que é usado para transmitir metadados. Ele deve apontar para os dados que serão passados para a chamada de remoção da fila.  
*BufferSize* \[ no \] tamanho de *pBuffer*, em bytes.  
*Sinalizadores* \[ de em \] um parâmetro opcional que controla o comportamento dessa função. O único sinalizador é o \_ sinalizador da fila de superfície \_ \_ \_ não \_ aguardar. Consulte os comentários para liberação. Se nenhum sinalizador for passado (*flags* = = 0), o comportamento de bloqueio padrão será usado.  
</dl>

**Valores de retorno**

Essa função pode retornar \_ um erro \_ dxgi \_ ainda \_ está desenhando se um sinalizador de fila de superfície \_ \_ \_ \_ não \_ aguardar é usado.  
</dl>

**Comentários**

-   Essa função coloca a superfície na fila. Se o aplicativo não especificar o sinalizador de fila de superfície não \_ \_ \_ \_ \_ esperar, essa função está bloqueando e fará uma sincronização de GPU-CPU para garantir que toda a renderização na superfície enfileirada seja concluída. Se essa função for realizada com sucesso, uma superfície estará disponível para remoção da fila. Se você quiser um comportamento sem bloqueio, use o \_ sinalizador não \_ aguardar. Consulte flush () para obter detalhes.
-   De acordo COM as regras de contagem de referência COM, a superfície retornada pela remoção será AddRef () para que o aplicativo não precise fazer isso. Depois de chamar enqueue, o aplicativo deve liberar a superfície porque não está mais usando-a.

**Liberar**  


```C++
HRESULT Flush(
  [in]  DWORD Flags,
  [out] UINT *nSurfaces
);
```



**Parâmetros**  
*Flags* \[in\]  
O único sinalizador é o \_ sinalizador da fila de superfície \_ \_ \_ não \_ aguardar. Consulte Observações. *nSurfaces* \[ out \] retorna o número de superfícies que ainda estão pendentes e não são liberadas.  
</dl>

**Valores de retorno**

Essa função pode retornar \_ um erro \_ dxgi \_ ainda \_ está desenhando se o sinalizador da fila de superfície não \_ \_ \_ \_ \_ aguardar é usado. Essa função retornará S \_ OK se alguma superfície tiver sido liberada com êxito. Essa função retornará \_ um erro \_ dxgi \_ ainda estará \_ desenhando somente se nenhuma superfície fosse liberada. Juntos, o valor de retorno e *nSurfaces* indicam ao aplicativo qual trabalho foi feito e se algum trabalho é deixado para fazer.  
</dl>

**Comentários**

A liberação só será significativa se a chamada anterior para enfileirar usou o \_ \_ sinalizador não aguardar; caso contrário, será uma operação não operacional. Se a chamada para enqueue usou o \_ \_ sinalizador não aguardar, o enqueue retornará imediatamente e a sincronização de GPU-CPU não será garantida. A superfície ainda é considerada enfileirada, o dispositivo de produção não pode continuar a usá-la, mas não está disponível para remoção da fila. Para tentar confirmar a superfície da remoção da fila, a liberação deve ser chamada. Tentativas de liberação para confirmar todas as superfícies que estão enfileiradas no momento. Se nenhum sinalizador for passado para flush, ele bloqueará e limpará toda a fila, preparando todas as superfícies para remoção da fila. Se o \_ sinalizador não \_ aguardar for usado, a fila verificará as superfícies para ver se alguma delas está pronta; esta etapa é sem bloqueio. As superfícies que concluíram a sincronização de GPU-CPU estarão prontas para o dispositivo do consumidor. As superfícies que ainda estiverem pendentes não serão afetadas. A função retorna o número de superfícies que ainda precisam ser liberadas.

> [!Note]  
> A liberação não interromperá a semântica da fila. A API garante que as superfícies enfileiradas primeiro serão confirmadas antes das superfícies enfileiradas posteriormente, independentemente de quando ocorrer a sincronização de GPU-CPU.

 

  
</dl>

### <a name="direct3d-9ex-and-dxgi-interop-helper-how-to-use"></a>Auxiliar de interoperabilidade do Direct3D 9Ex e DXGI: como usar

Esperamos que a maioria dos casos de uso envolva dois dispositivos compartilhando várias superfícies. Como esse também é o cenário mais simples, este documento detalha como usar as APIs para atingir essa meta, discute uma variação sem bloqueio e termina com uma breve seção sobre a inicialização de três dispositivos.

### <a name="two-devices"></a>Dois dispositivos

O aplicativo de exemplo que usa esse auxiliar pode usar o Direct3D 9Ex e o Direct3D 11 juntos. O aplicativo pode processar o conteúdo com ambos os dispositivos e apresentar o conteúdo usando o Direct3D 9. O processamento pode significar a renderização de conteúdo, a decodificação de vídeo, a execução de sombreadores de computação e assim por diante. Para cada quadro, o aplicativo será processado primeiro com o Direct3D 11, depois o processo com o Direct3D 9 e, finalmente, presente com o Direct3D 9. Além disso, o processamento com o Direct3D 11 produzirá alguns metadados que o Direct3D 9 presente precisará consumir. Esta seção aborda o uso do auxiliar em três partes que correspondem a esta sequência: inicialização, loop principal e limpeza.

**Initialization**  
A inicialização envolve as seguintes etapas:  

1.  Inicialize ambos os dispositivos.
2.  Crie a fila raiz: m \_ 11to9Queue.
3.  Clone da fila raiz: m \_ 9to11Queue.
4.  Chame OpenProducer/OpenConsumer em ambas as filas.

Os nomes de fila usam os números 9 e 11 para indicar qual API é o produtor e qual é a fila consumidor: **m do \_ ***produtor*** para o ***consumidor*****. Da mesma forma, m \_ 11to9Queue indica uma fila para a qual o dispositivo Direct3D 11 produz superfícies que o dispositivo Direct3D 9 consome. Da mesma forma, m \_ 9to11Queue indica uma fila para a qual o Direct3D 9 produz superfícies que o Direct3D 11 consome.  
A fila raiz está inicialmente cheia e todas as filas clonadas estão vazias inicialmente. Isso não deve ser um problema para o aplicativo, exceto para o primeiro ciclo de enfileiramentos e remoção de filas e a disponibilidade dos metadados. Se uma remoção da fila solicitar metadados, mas nenhum tiver sido definido (porque nada está lá inicialmente ou o enfileiramento não definiu nada), a remoção da fila verá que nenhum metadado foi recebido.  

1.  **Inicialize ambos os dispositivos.**  
    ```C++
    m_pD3D9Device = InitializeD3D9ExDevice();
    m_pD3D11Device = InitializeD3D11Device();
    ```

    

2.  **Crie a fila raiz.**  
    Essa etapa também cria as superfícies. As restrições de tamanho e formato são idênticas à criação de qualquer recurso compartilhado. O tamanho do buffer de metadados é fixo no momento da criação e, nesse caso, vamos apenas passar um UINT.  
    A fila deve ser criada com um número fixo de superfícies. O desempenho irá variar dependendo do cenário. Ter várias superfícies aumenta as chances de os dispositivos serem ocupados. Por exemplo, se houver apenas uma superfície, não haverá nenhuma paralelização entre os dois dispositivos. Por outro lado, aumentar o número de superfícies aumenta o volume de memória, o que pode prejudicar o desempenho. Este exemplo usa duas superfícies.  
    ```C++
    SURFACE_QUEUE_DESC Desc;
    Desc.Width        = 640;
    Desc.Height       = 480;
    Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
    Desc.NumSurfaces  = 2;
    Desc.MetaDataSize = sizeof(UINT);
    Desc.Flags        = 0;

    CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
    ```

    

3.  **Clone a fila raiz.**  
    Cada fila clonada deve usar as mesmas superfícies, mas pode ter diferentes tamanhos de buffer de metadados e diferentes sinalizadores. Nesse caso, não há metadados do Direct3D 9 para o Direct3D 11.  
    ```C++
    SURFACE_QUEUE_CLONE_DESC Desc;
    Desc.MetaDataSize = 0;
    Desc.Flags        = 0;

    m_11to9Queue->Clone(&Desc, &m_9to11Queue);
    ```

    

4.  **Abra os dispositivos produtor e consumidor.**  
    O aplicativo deve executar essa etapa antes de chamar Enqueue e remover a fila. Abrir um produtor e consumidor retorna interfaces que contêm as APIs de enfileiramento/remoção da fila.  
    ```C++
    // Open for m_p9to11Queue.
    m_p9to11Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
    m_p9to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

    // Open for m_p11to9Queue.
    m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
    m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
    ```

    

**Loop principal**  
O uso da fila é modelado após o problema de produtor/consumidor clássico. Considere isso a partir de uma perspectiva por dispositivo. Cada dispositivo deve executar estas etapas: remover da fila para obter uma superfície de sua fila de consumo, processar na superfície e enfileirar em sua fila de produção. Para o dispositivo Direct3D 11, o uso do Direct3D 9 é quase idêntico.  


```C++
// Direct3D 9 Device.
IDirect3DTexture9* pTexture9 = NULL;
REFIID             surfaceID9 = _uuidof(IDirect3DTexture9);
UINT               metaData;
UINT               metaDataSize;
while (!done)
{
    // Dequeue surface.
    m_pD3D9Consumer->Dequeue(surfaceID9, (void**)&pSurface9,
                             &metaData, &metaDataSize, INFINITE);

    // Process the surface.
    ProcessD3D9(pSurface9);

    // Present the surface using the meta data.
    PresentD3D9(pSurface9, metaData, metaDataSize);

    // Enqueue surface.
    m_pD3D9Producer->Enqueue(pSurface9, NULL, 0, 0);
}
```



**Limpando**  
Esta etapa é muito simples. Além das etapas normais para limpar as APIs do Direct3D, o aplicativo deve liberar as interfaces COM de retorno.  


```C++
m_pD3D9Producer->Release();
m_pD3D9Consumer->Release();
m_pD3D11Producer->Release();
m_pD3D11Consumer->Release();
m_p9to11Queue->Release();
m_p11to9Queue->Release();
```



</dl>

### <a name="non-blocking-use"></a>Uso sem bloqueio

O exemplo anterior faz sentido para um caso de uso multithread, no qual cada dispositivo tem seu próprio thread. O exemplo usa as versões de bloqueio das APIs: infinito para tempo limite e nenhum sinalizador para enfileirar. Se você quiser usar o auxiliar em uma forma sem bloqueio, precisará fazer apenas algumas alterações. Esta seção mostra o uso sem bloqueio com ambos os dispositivos em um thread.

**Initialization**  
A inicialização é idêntica, exceto pelos sinalizadores. Como o aplicativo é de thread único, use esse sinalizador para a criação. Isso desativa um pouco do código de sincronização, o que potencialmente melhora o desempenho.  


```C++
SURFACE_QUEUE_DESC Desc;
Desc.Width        = 640;
Desc.Height       = 480;
Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
Desc.NumSurfaces  = 2;
Desc.MetaDataSize = sizeof(UINT);
Desc.Flags        = SURFACE_QUEUE_FLAG_SINGLE_THREADED;

CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
```




```C++
SURFACE_QUEUE_CLONE_DESC Desc;
Desc.MetaDataSize = 0;
Desc.Flags        = SURFACE_QUEUE_FLAG_SINGLE_THREADED;

m_11to9Queue->Clone(&Desc, &m_9to11Queue);
```



Abrir os dispositivos produtor e consumidor é o mesmo que no exemplo de bloqueio.  
**Usando a fila**  
Há várias maneiras de usar a fila em um modo sem bloqueio com várias características de desempenho. O exemplo a seguir é simples, mas tem baixo desempenho devido à rotação e sondagem excessivas. Apesar desses problemas, o exemplo mostra como usar o auxiliar. A abordagem é constantemente se sentar em um loop e remover da fila, processar, enfileirar e liberar. Se qualquer uma das etapas falhar porque o recurso não está disponível, o aplicativo simplesmente tentará novamente o loop seguinte.  


```C++
// Direct3D 11 Device.
ID3D11Texture2D* pSurface11 = NULL;
REFIID           surfaceID11 = __uuidof(ID3D11Texture2D);
UINT             metaData;
while (!done)
{
    //
    // D3D11 Portion.
    //

    // Dequeue surface.
    hr = m_pD3D11Consumer->Dequeue(surfaceID11,
                                   (void**)&pSurface11,
                                   NULL, 0, 0);
    // Only continue if we got a surface.
    if (SUCCEEDED(hr))
    {
        // Process the surface and return some meta data.
        ProcessD3D11(pSurface11, &metaData);

        // Enqueue surface.
        m_pD3D11Producer->Enqueue(pSurface11, &metaData,
                                  sizeof(UINT),
                                  SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
    }
    // Flush the queue to check if any surfaces completed.
    m_pD3D11Producer->Flush(NULL,SURFACE_QUEUE_FLAG_DO_NOT_WAIT);

    //
    // Do the same with the Direct3D 9 Device.
    //

    // Dequeue surface.
    hr = m_pD3D9Consumer->Dequeue(surfaceID9,
                                  (void**)&pSurface9,
                                  &metaData,
                                  &metaDataSize, 0);
    // Only continue if we got a surface.
    if (SUCCEEDED(hr)))
    {
        // Process the surface.
        ProcessD3D9(pSurface9);

        // Present the surface using the meta data.
        PresentD3D9(pSurface9, metaData, metaDataSize);

        // Enqueue surface.
        m_pD3D9Producer->Enqueue(pSurface9, NULL, 0,
                                 SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
    }
    // Flush the queue to check if any surfaces completed.
    m_pD3D9Producer->Flush(NULL,SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
}
```



Uma solução mais complexa poderia verificar o valor de retorno de enfileirar e liberar para determinar se a liberação é necessária.  
</dl>

### <a name="three-devices"></a>Três dispositivos

A extensão dos exemplos anteriores para abranger vários dispositivos é simples. O código a seguir executa a inicialização. Depois que os objetos produtor/consumidor tiverem sido criados, o código para usá-los será o mesmo. Este exemplo tem três dispositivos e, portanto, três filas. As superfícies fluem do Direct3D 9 para o Direct3D 10 para o Direct3D 11.


```C++
SURFACE_QUEUE_DESC Desc;
Desc.Width        = 640;
Desc.Height       = 480;
Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
Desc.NumSurfaces  = 2;
Desc.MetaDataSize = sizeof(UINT);
Desc.Flags        = 0;

SURFACE_QUEUE_CLONE_DESC Desc;
Desc.MetaDataSize = 0;
Desc.Flags        = 0;

CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
m_11to9Queue->Clone(&Desc, &m_9to10Queue);
m_11to9Queue->Clone(&Desc, &m_10to11Queue);
```



Como mencionado anteriormente, a clonagem funciona da mesma forma, não importa qual fila é clonada. Por exemplo, a segunda chamada de clonagem poderia ter sido desativada do \_ objeto m 9to10Queue.


```C++
// Open for m_p9to10Queue.
m_p9to10Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
m_p9to10Queue->OpenConsumer(m_pD3D10Device, &m_pD3D10Consumer);

// Open for m_p10to11Queue.
m_p10to11Queue->OpenProducer(m_pD3D10Device, &m_pD3D10Producer);
m_p10to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

// Open for m_p11to9Queue.
m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
```



## <a name="conclusion"></a>Conclusão

Você pode criar soluções que usam a interoperabilidade para empregar o poder de várias APIs do DirectX. A interoperabilidade da API de gráficos do Windows agora oferece um DXGI 1,1 de tempo de execução de gerenciamento de superfície comum Esse tempo de execução habilita o suporte a compartilhamento de superfície sincronizado em APIs recentemente desenvolvidas, como Direct3D 11, Direct3D 10,1 e Direct2D. As melhorias de interoperabilidade entre novas APIs e APIs existentes auxiliam na migração de aplicativos e na compatibilidade com versões anteriores. As APIs de consumidor do Direct3D 9Ex e DXGI 1,1 podem interoperar, conforme mostrado com o mecanismo de sincronização fornecido por meio do código auxiliar de exemplo na Galeria de códigos do MSDN.

 

 