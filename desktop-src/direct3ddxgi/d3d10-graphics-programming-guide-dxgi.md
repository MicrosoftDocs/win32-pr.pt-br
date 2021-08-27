---
description: Este tópico inclui as seções a seguir.
ms.assetid: 0522ccbf-e754-470a-8199-004fcbaa927d
title: Visão geral do DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 604787a1b3f747b9d33cc04e249128aede7b7a3e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626132"
---
# <a name="dxgi-overview"></a>Visão geral do DXGI

A Microsoft DirectX Graphics Infrastructure (DXGI) reconhece que algumas partes de gráficos evoluem mais lentamente do que outras. O principal objetivo do DXGI é gerenciar tarefas de nível baixo que podem ser independentes do tempo de execução de gráficos do DirectX. DXGI fornece uma estrutura comum para futuros componentes de gráficos; o primeiro componente que aproveita o DXGI é o Microsoft Direct3D 10.

Nas versões anteriores do Direct3D, tarefas de nível baixo, como a enumeração de dispositivos de hardware, a apresentação de quadros renderizados a uma saída, o controle de gama e o gerenciamento de uma transição de tela inteira foram incluídas no tempo de execução do Direct3D. Essas tarefas agora são implementadas em DXGI.

A finalidade de DXGI é comunicar-se com o driver de modo kernel e o hardware do sistema, conforme mostrado no diagrama a seguir.

![diagrama da comunicação entre aplicativos, DXGI e drivers e hardware](images/dxgi-dll.png)

Um aplicativo pode acessar o DXGI diretamente ou chamar as APIs do Direct3D em D3D11 \_ 1. h, D3D11. h, d3d10 \_ 1. h ou d3d10. h, que manipula as comunicações com dxgi para você. Talvez você queira trabalhar com DXGI diretamente se seu aplicativo precisar enumerar dispositivos ou controlar como os dados são apresentados a uma saída.

Este tópico inclui as seções a seguir.

-   [Enumerando adaptadores](#enumerating-adapters)
    -   [Novas informações sobre como enumerar adaptadores para Windows 8](#new-info-about-enumerating-adapters-for-windows-8)
-   [Apresentação](#presentation)
    -   [Criar uma cadeia de permuta](#create-a-swap-chain)
    -   [Cuidado e alimentação da cadeia de permuta](#care-and-feeding-of-the-swap-chain)
    -   [Manipulando o redimensionamento da janela](#handling-window-resizing)
    -   [Escolhendo a saída e o tamanho de DXGI](#choosing-the-dxgi-output-and-size)
    -   [Depuração no modo de Full-Screen](#debugging-in-full-screen-mode)
    -   [Destruindo uma cadeia de permuta](#destroying-a-swap-chain)
    -   [Usando um monitor girado](#using-a-rotated-monitor)
    -   [Alternando modos](#switching-modes)
    -   [Dica de desempenho de tela inteira](#full-screen-performance-tip)
    -   [Considerações sobre o multithread](#multithread-considerations)
-   [Respostas de DXGI do DLLMain](#dxgi-responses-from-dllmain)
-   [Alterações de DXGI 1,1](#dxgi-11-changes)
-   [Alterações de DXGI 1,2](#dxgi-12-changes)
-   [Tópicos relacionados](#related-topics)

Para ver quais formatos têm suporte do hardware do Direct3D 11:

-   [Suporte ao formato DXGI para hardware 12,1 de nível de recurso Direct3D](hardware-support-for-direct3d-12-1-formats.md)
-   [Suporte ao formato DXGI para hardware 12,0 de nível de recurso Direct3D](hardware-support-for-direct3d-12-0-formats.md)
-   [Suporte ao formato DXGI para hardware 11,1 de nível de recurso Direct3D](format-support-for-direct3d-11-1-feature-level-hardware.md)
-   [Suporte ao formato DXGI para hardware 11,0 de nível de recurso Direct3D](format-support-for-direct3d-11-0-feature-level-hardware.md)
-   [Suporte de hardware para formatos Direct3D 10Level9](/previous-versions//ff471324(v=vs.85))
-   [Suporte de hardware para formatos Direct3D 10,1](/previous-versions//cc627091(v=vs.85))
-   [Suporte de hardware para formatos Direct3D 10](/previous-versions//cc627090(v=vs.85))

## <a name="enumerating-adapters"></a>Enumerando adaptadores

Um adaptador é uma abstração do hardware e do recurso de software do seu computador. Geralmente, há muitos adaptadores em seu computador. Alguns dispositivos são implementados no hardware (como sua placa de vídeo) e alguns são implementados no software (como o rasterizador de referência do Direct3D). Os adaptadores implementam a funcionalidade usada por um aplicativo gráfico. O diagrama a seguir mostra um sistema com um único computador, dois adaptadores (placas de vídeo) e três monitores de saída.

![diagrama de um computador com duas placas de vídeo e três monitores](images/dxgi-terms.png)

Ao enumerar essas partes de hardware, DXGI cria uma interface [**IDXGIOutput1**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutput1) para cada saída (ou monitor) e uma interface [**IDXGIAdapter2**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgiadapter2) para cada placa de vídeo (mesmo que seja uma placa de vídeo incorporada a uma placa-mãe). A enumeração é feita usando uma chamada de interface [**IDXGIFactory**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) , [**IDXGIFactory:: EnumAdapters**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-enumadapters), para retornar um conjunto de interfaces [**IDXGIAdapter**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter) que representam o hardware de vídeo.

DXGI 1,1 adicionou a interface [**IDXGIFactory1**](/windows/win32/api/DXGI/nn-dxgi-idxgifactory1) . [**IDXGIFactory1:: EnumAdapters1**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) retorna um conjunto de interfaces [**IDXGIAdapter1**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter1) que representa o hardware de vídeo.

Se você quiser selecionar recursos específicos de hardware de vídeo ao usar APIs do Direct3D, recomendamos que você chame iterativamente a função [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice) ou [**D3D11CreateDeviceAndSwapChain**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain) com cada identificador de adaptador e um [nível de recurso](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md)de hardware possível. Essa função terá sucesso se o nível de recurso tiver suporte do adaptador especificado.

### <a name="new-info-about-enumerating-adapters-for-windows-8"></a>Novas informações sobre como enumerar adaptadores para Windows 8

a partir do Windows 8, um adaptador chamado "Driver de renderização básico da Microsoft" está sempre presente. Esse adaptador tem um VendorID de **0x1414** e um DeviceID de **0x8c**. Esse adaptador também tem o valor de [**\_ \_ \_ software Flag do adaptador dxgi**](/windows/win32/api/dxgi/ne-dxgi-dxgi_adapter_flag) definido no membro **flags** de sua estrutura [**\_ \_ DESC2 do adaptador dxgi**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_adapter_desc2) . Esse adaptador é um dispositivo somente de renderização que não tem saídas de exibição. DXGI nunca retorna [**o \_ dispositivo de erro dxgi \_ \_ removido**](dxgi-error.md) para esse adaptador.

Se o driver de vídeo de um computador não estiver funcionando ou estiver desabilitado, o adaptador primário (**nulo**) do computador também poderá ser chamado de "driver de renderização básico da Microsoft". Mas esse adaptador tem saídas e não tem o valor de [**\_ software do \_ sinalizador \_ do adaptador dxgi**](/windows/win32/api/dxgi/ne-dxgi-dxgi_adapter_flag) definido. O sistema operacional e os aplicativos usam esse adaptador por padrão. Se um driver de vídeo estiver instalado ou habilitado, os aplicativos poderão receber o [**\_ dispositivo de erro dxgi \_ \_ removido**](dxgi-error.md) desse adaptador e deverão enumerar novamente os adaptadores novamente.

Quando o adaptador de vídeo primário de um computador é o "adaptador de vídeo básico da Microsoft" (adaptador de[detorção](../direct3d11/overviews-direct3d-11-devices-create-warp.md) ), esse computador também tem um segundo adaptador. Esse segundo adaptador é o dispositivo somente de processamento que não tem saídas de exibição e para os quais DXGI nunca retorna o [**\_ dispositivo de erro dxgi \_ \_ removido**](dxgi-error.md).

Se você quiser usar WARP para renderização, computação ou outras tarefas de execução longa, recomendamos o uso do dispositivo somente de renderização. Você pode obter um ponteiro para o dispositivo somente de renderização chamando o método [**IDXGIFactory1:: EnumAdapters1**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) . Você também cria o dispositivo somente de renderização ao especificar o [**\_ tipo de driver D3D \_ \_ Warp**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_driver_type) no parâmetro *driverType* de [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice) porque o dispositivo Warp também usa o adaptador de detorção somente de renderização.

## <a name="presentation"></a>Apresentação

O trabalho do seu aplicativo é renderizar os quadros e pedir DXGI para apresentar esses quadros à saída. Se o aplicativo tiver dois buffers disponíveis, ele poderá renderizar um buffer durante a apresentação de outro. O aplicativo pode exigir mais de dois buffers dependendo do tempo necessário para renderizar um quadro ou a taxa de quadros desejada para apresentação. O conjunto de buffers criado é chamado de uma cadeia de permuta, como mostrado aqui.

![ilustração de uma cadeia de permuta](images/dxgi-swap-chain.png)

-   [Criar uma cadeia de permuta](#create-a-swap-chain)
-   [Cuidado e alimentação da cadeia de permuta](#care-and-feeding-of-the-swap-chain)
-   [Manipulando o redimensionamento da janela](#handling-window-resizing)
-   [Escolhendo a saída e o tamanho de DXGI](#choosing-the-dxgi-output-and-size)
-   [Depuração no modo de Full-Screen](#debugging-in-full-screen-mode)
-   [Destruindo uma cadeia de permuta](#destroying-a-swap-chain)
-   [Usando um monitor girado](#using-a-rotated-monitor)
-   [Alternando modos](#switching-modes)
-   [Dica de desempenho de tela inteira](#full-screen-performance-tip)
-   [Considerações sobre o multithread](#multithread-considerations)

Uma cadeia de permuta tem um buffer frontal e um ou mais buffers de fundo. Cada aplicativo cria sua própria cadeia de permuta. Para maximizar a velocidade da apresentação dos dados a uma saída, uma cadeia de permuta quase sempre é criada na memória de um subsistema de exibição, que é mostrada na ilustração a seguir.

![ilustração de um subsistema de exibição](images/dxgi-adapter.png)

O subsistema de vídeo (que geralmente é uma placa de vídeo, mas pode ser implementado em uma placa-mãe) contém uma GPU, um conversor digital para analógico (DAC) e memória. A cadeia de permuta é alocada nessa memória para tornar a apresentação muito rápida. O subsistema de exibição apresenta os dados no buffer frontal para a saída.

Uma cadeia de permuta é configurada para desenhar no modo de tela inteira ou janelada, isso elimina a necessidade de saber se uma saída é exibida em janela ou em tela inteira. Uma cadeia de troca de modo de tela inteira pode otimizar o desempenho alternando a resolução de vídeo.

### <a name="create-a-swap-chain"></a>Criar uma cadeia de troca

<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Diferenças entre o Direct3D 9 e o Direct3D 10: o Direct3D 10 é o primeiro componente gráfico a usar DXGI. DXGI tem alguns comportamentos de cadeia de troca diferentes.<br/>
<ul>
<li>Em DXGI, uma cadeia de permuta é vinculada a uma janela quando a cadeia de permuta é criada. Essa alteração melhora o desempenho e economiza memória. As versões anteriores do Direct3D permitiam que a cadeia de permuta alterasse a janela à qual a cadeia de permuta está vinculada.</li>
<li>Em DXGI, uma cadeia de permuta está vinculada a um dispositivo de renderização na criação. O objeto de dispositivo que as funções de dispositivo de criação de Direct3D retornam implementa a interface <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> . Você pode chamar <a href="/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> para consultar a interface <a href="/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgidevice2"><strong>IDXGIDevice2</strong></a> correspondente do dispositivo. Uma alteração no dispositivo de renderização requer que a cadeia de permuta seja recriada.</li>
<li><p>No DXGI, os efeitos de permuta disponíveis são DXGI_SWAP_EFFECT_DISCARD e DXGI_SWAP_EFFECT_SEQUENTIAL. Começando com Windows 8 o DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL de troca de dados também está disponível. A tabela a seguir mostra um mapeamento do efeito de troca direct3D 9 para DXGI definido. </p>
<table>
<thead>
<tr class="header">
<th>Efeito de troca D3D9</th>
<th>Efeito de troca DXGI</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3DSWAPEFFECT_DISCARD</td>
<td>DXGI_SWAP_EFFECT_DISCARD</td>
</tr>
<tr class="even">
<td>D3DSWAPEFFECT_COPY</td>
<td>DXGI_SWAP_EFFECT_SEQUENTIAL com 1 buffer</td>
</tr>
<tr class="odd">
<td>D3DSWAPEFFECT_FLIP</td>
<td>DXGI_SWAP_EFFECT_SEQUENTIAL com 2 ou mais buffers</td>
</tr>
<tr class="even">
<td>D3DSWAPEFFECT_FLIPEX</td>
<td>DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL com 2 ou mais buffers</td>
</tr>
</tbody>
</table>
<p></p>
<p> </p></li>
</ul></td>
</tr>
</tbody>
</table>



 

Os buffers de uma cadeia de permuta são criados em um tamanho específico e em um formato específico. O aplicativo especifica esses valores (ou você pode herdar o tamanho da janela de destino) na inicialização e, opcionalmente, pode modificá-los à medida que o tamanho da janela muda em resposta à entrada do usuário ou eventos do programa.

Depois de criar a cadeia de permuta, normalmente você deseja renderizar imagens nele. Aqui está um fragmento de código que configura um contexto direct3D para renderizar em uma cadeia de permuta. Esse código extrai um buffer da cadeia de permuta, cria uma exibição de destino de renderização desse buffer e, em seguida, define-o no dispositivo:


```
ID3D11Resource * pBB;
ThrowFailure( pSwapChain->GetBuffer(0, __uuidof(pBB),    
  reinterpret_cast<void**>(&pBB)), "Couldn't get back buffer");
ID3D11RenderTargetView * pView;
ThrowFailure( pD3D11Device->CreateRenderTargetView(pBB, NULL, &pView), 
  "Couldn't create view" );
pD3D11DeviceContext->OMSetRenderTargets(1, &pView, 0);
        
```



Depois que o aplicativo renderizar um quadro em um buffer de cadeia de permuta, chame [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). Em seguida, o aplicativo pode renderizar a próxima imagem.

### <a name="care-and-feeding-of-the-swap-chain"></a>Cuidado e alimentação da cadeia de permuta

Depois de renderizar sua imagem, chame [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) e vá renderizar a próxima imagem. Essa é a extensão de sua responsabilidade.

Se você tiver chamado [**IDXGIFactory::MakeWindowAssociation**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-makewindowassociation)anteriormente, o usuário poderá pressionar a combinação de teclas Alt-Enter e o DXGI fará a transição do aplicativo entre o modo de janela e de tela inteira. **É recomendável IDXGIFactory::MakeWindowAssociation,** pois um mecanismo de controle padrão para o usuário é altamente desejado.

Embora você não tenha que escrever mais código do que foi descrito, algumas etapas simples podem tornar seu aplicativo mais responsivo. A consideração mais importante é o re tamanho dos buffers da cadeia de permuta em resposta ao re tamanho da janela de saída. Naturalmente, a melhor rota do aplicativo é responder ao WM SIZE e chamar \_ [**IDXGISwapChain::ResizeBuffers,**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers)passando o tamanho contido nos parâmetros da mensagem. Obviamente, esse comportamento faz com que seu aplicativo responda bem ao usuário quando ele arrasta as bordas da janela, mas também é exatamente o que permite uma transição suave de tela inteira. Sua janela receberá uma mensagem WM SIZE sempre que essa transição ocorrer e chamar \_ **IDXGISwapChain::ResizeBuffers** é a chance da cadeia de permuta de alocar o armazenamento dos buffers para uma apresentação ideal. É por isso que o aplicativo é necessário para liberar quaisquer referências que ele tenha nos buffers existentes antes de chamar **IDXGISwapChain::ResizeBuffers**.

A falha ao chamar [**IDXGISwapChain::ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) em resposta à alternação para o modo de tela inteira (mais naturalmente, em resposta ao WM SIZE), pode impedir a otimização de invertida, em que o DXGI pode simplesmente trocar qual buffer está sendo exibido, em vez de copiar o valor de dados de uma tela \_ inteira.

[**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) informará se a janela de saída está totalmente oclusa por meio de **STATUS DO DXGI \_ \_ OCCLUDED**. Quando isso ocorre, recomendamos que seu aplicativo entre no modo de espera (chamando **IDXGISwapChain1::P resent1** com **DXGI \_ PRESENT \_ TEST**), pois os recursos usados para renderizar o quadro são perdidos. Usar **DXGI \_ PRESENT \_ TEST** impedirá que qualquer dado seja apresentado enquanto ainda executa a verificação de oclusão. Depois **que IDXGISwapChain1::P resent1** retornar S OK, você deverá sair do modo de espera; não use o código de retorno para alternar para o modo de espera, pois isso pode deixar a cadeia de permuta não conseguir abrir mão do modo de tela \_ inteira.

O runtime do Direct3D 11.1, que está disponível a partir do Windows 8, fornece uma cadeia de permuta de inverter modelo (ou seja, uma cadeia de permuta que tem o valor [**\_ \_ \_ \_ SEQUENTIAL FLIP DE EFEITO SWAP DXGI**](/windows/win32/api/DXGI/ne-dxgi-dxgi_swap_effect) definido no membro **SwapEffect** da [**\_ DXGI SWAP CHAIN \_ \_ DESC**](/windows/win32/api/DXGI/ns-dxgi-dxgi_swap_chain_desc) ou [**DXGI \_ SWAP CHAIN \_ \_ DESC1**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)). Quando você apresenta quadros a uma saída com uma cadeia de permuta de modelo in flip, o DXGI desvincula o buffer de fundo de todos os locais de estado do pipeline, como um destino de renderização de fusão de saída, que gravará no buffer de fundo 0. Portanto, recomendamos que você chame [**ID3D11DeviceContext::OMSetRenderTargets**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-omsetrendertargets) imediatamente antes de renderizar para o buffer de fundo. Por exemplo, não chame **OMSetRenderTargets** e execute o trabalho de sombreador de computação que não termine de renderizar para o recurso. Para obter mais informações sobre cadeias de permuta de flip-model e seus benefícios, consulte Modelo de in flip [do DXGI.](dxgi-flip-model.md)

> [!NOTE]  
> No Direct3D 10 e direct3D 11, você não precisa chamar [**IDXGISwapChain::GetBuffer**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-getbuffer) para recuperar o buffer 0 depois de chamar [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) porque, para sua conveniência, as identidades dos buffers de fundo mudam. Isso não acontece no Direct3D 12 e seu aplicativo deve controlar manualmente os índices de buffer.

### <a name="handling-window-resizing"></a>Tratando o resizing da janela

Você pode usar o [**método IDXGISwapChain::ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) para lidar com o reizing de janela. Antes de chamar **ResizeBuffers**, você deve liberar todas as referências pendentes para os buffers da cadeia de permuta. O objeto que normalmente contém uma referência ao buffer de uma cadeia de permuta é uma exibição de destino de renderização.

O código de exemplo a seguir mostra como chamar [**ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) de dentro do manipulador WindowProc para mensagens WM \_ SIZE:


```
    case WM_SIZE:
        if (g_pSwapChain)
        {
            g_pd3dDeviceContext->OMSetRenderTargets(0, 0, 0);

            // Release all outstanding references to the swap chain's buffers.
            g_pRenderTargetView->Release();

            HRESULT hr;
            // Preserve the existing buffer count and format.
            // Automatically choose the width and height to match the client rect for HWNDs.
            hr = g_pSwapChain->ResizeBuffers(0, 0, 0, DXGI_FORMAT_UNKNOWN, 0);
                                            
            // Perform error handling here!

            // Get buffer and create a render-target-view.
            ID3D11Texture2D* pBuffer;
            hr = g_pSwapChain->GetBuffer(0, __uuidof( ID3D11Texture2D),
                                         (void**) &pBuffer );
            // Perform error handling here!

            hr = g_pd3dDevice->CreateRenderTargetView(pBuffer, NULL,
                                                     &g_pRenderTargetView);
            // Perform error handling here!
            pBuffer->Release();

            g_pd3dDeviceContext->OMSetRenderTargets(1, &g_pRenderTargetView, NULL );

            // Set up the viewport.
            D3D11_VIEWPORT vp;
            vp.Width = width;
            vp.Height = height;
            vp.MinDepth = 0.0f;
            vp.MaxDepth = 1.0f;
            vp.TopLeftX = 0;
            vp.TopLeftY = 0;
            g_pd3dDeviceContext->RSSetViewports( 1, &vp );
        }
        return 1;
```



### <a name="choosing-the-dxgi-output-and-size"></a>Escolhendo a saída e o tamanho do DXGI

Por padrão, o DXGI escolhe a saída que contém a maior parte da área do cliente da janela. Essa é a única opção disponível para o DXGI quando ele entra em tela inteira em resposta a alt-enter. Se o aplicativo optar por ir para o modo de tela inteira sozinho, ele poderá chamar [**IDXGISwapChain::SetFullscreenState**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) e passar um [**IDXGIOutput1**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutput1) explícito (ou **NULL,** se o aplicativo estiver satisfeito em permitir que o DXGI decida).

Para reorganizar a saída durante a tela inteira ou em janelas, é recomendável chamar [**IDXGISwapChain::ResizeTarget,**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget)pois esse método também resize a janela de destino. Como a janela de destino é ressalvada, o sistema operacional envia **WM \_ SIZE** e seu código naturalmente chamará [**IDXGISwapChain::ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) em resposta. Portanto, é um desperdício de esforço ressarcimento dos buffers e, em seguida, reorganizar o destino posteriormente.

### <a name="debugging-in-full-screen-mode"></a>Depuração no modo de tela inteira

Uma cadeia de permuta DXGI relincha o modo de tela inteira somente quando absolutamente necessário. Isso significa que você pode depurar um aplicativo de tela inteira usando vários monitores, desde que a janela de depuração não se sobreponha à janela de destino da cadeia de permuta. Como alternativa, você pode impedir completamente a alternação de modo não definindo o sinalizador SWITCH DO MODO DE OPÇÃO DE MODO DE TROCA **DXGI \_ \_ \_ \_ \_ \_** SWAP.

Se a alternação de modo for permitida, uma cadeia de permuta abrirá mão do modo de tela inteira sempre que sua janela de saída for oclusiva por outra janela. A verificação de oclusão é executada durante [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)ou por um thread separado cuja finalidade é observar para ver se o aplicativo ficou sem resposta (e não chama mais **IDXGISwapChain1::P resent1**). Para desabilitar a capacidade do thread separado de causar uma opção, de definir a seguinte chave do Registro como qualquer valor que não seja zero.

**HKCU \\ Software \\ Microsoft \\ DXGI \\ DisableFullscreenWatchdog**

### <a name="destroying-a-swap-chain"></a>Destruir uma cadeia de permuta

Você não pode liberar uma cadeia de permuta no modo de tela inteira porque isso pode criar contenção de thread (o que fará com que o DXGI aloque uma exceção não continuavel). Antes de liberar uma cadeia de permuta, primeiro mude para o modo em janela (usando [**IDXGISwapChain::SetFullscreenState**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate)( **FALSE**, **NULL** )) e, em seguida, chame [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

### <a name="using-a-rotated-monitor"></a>Usando um monitor girado

Um aplicativo não precisa se preocupar com a orientação do monitor, o DXGI girará um buffer de cadeia de permuta durante a apresentação, se necessário. É claro que essa rotação adicional pode afetar o desempenho. Para melhor desempenho, tome conta da rotação em seu aplicativo fazendo o seguinte:

-   Use o SINALIZADOR DE CADEIA DE **\_ \_ PERMUTA \_ DXGI \_ NÃOPREROTADO.** Isso notifica o DXGI de que o aplicativo produzirá uma imagem girada (por exemplo, alterando sua matriz de projeção). Uma coisa a ser anotada é que esse sinalizador só é válido enquanto estiver no modo de tela inteira.
-   Alocar cada buffer de cadeia de permuta em seu tamanho girado. Use [**IDXGIOutput::GetDesc**](/windows/win32/api/DXGI/nf-dxgi-idxgioutput-getdesc) para obter esses valores, se necessário.

Ao executar a rotação em seu aplicativo, o DXGI simplesmente fará uma cópia em vez de uma cópia e uma rotação.

O runtime do Direct3D 11.1, que está disponível a partir do Windows 8, fornece uma cadeia de permuta de flip-model (ou seja, uma cadeia de permuta que tem o valor [**\_ \_ \_ \_ SEQUENTIAL**](/windows/win32/api/DXGI/ne-dxgi-dxgi_swap_effect) FLIP DE EFEITO SWAP DXGI definido no membro **SwapEffect** de [**DXGI \_ SWAP CHAIN \_ \_ DESC1**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)). Para maximizar as otimizações de apresentação disponíveis com uma cadeia de troca de modelo in flip, recomendamos que você faça com que seus aplicativos orientem o conteúdo para corresponder à saída específica na qual o conteúdo reside quando esse conteúdo ocupa totalmente a saída. Para obter mais informações sobre cadeias de permuta de flip-model e seus benefícios, consulte Modelo de in flip [do DXGI.](dxgi-flip-model.md)

### <a name="switching-modes"></a>Alternando modos

A cadeia de permuta DXGI pode alterar o modo de exibição de uma saída ao fazer uma transição de tela inteira. Para habilitar a alteração automática do modo de exibição, você deve especificar **DXGI \_ SWAP CHAIN FLAG ALLOW MODE \_ \_ \_ \_ \_ SWITCH** na descrição da cadeia de permuta. Se o modo de exibição mudar automaticamente, o DXGI escolherá o modo mais silencioso (tamanho e resolução não serão alterados, mas a profundidade da cor poderá). O reizing de buffers de cadeia de permuta não causará uma opção de modo. A cadeia de permuta faz uma promessa implícita de que, se você escolher um buffer de fundo que corresponde exatamente a um modo de exibição com suporte pela saída de destino, ele alternará para esse modo de exibição ao entrar no modo de tela inteira nessa saída. Consequentemente, você escolhe um modo de exibição escolhendo o formato e o tamanho do buffer de fundo.

### <a name="full-screen-performance-tip"></a>Dica de desempenho de tela inteira

Quando você chama [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) em um aplicativo de tela inteira, a cadeia de permuta inverte (em vez de blits) o conteúdo do buffer de fundo para o buffer frontal. Isso requer que a cadeia de permuta foi criada usando um modo de exibição enumerado (especificado em [**DXGI \_ SWAP \_ CHAIN \_ DESC1**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)). Se você não enumerar modos de exibição ou especificar incorretamente o modo de exibição na descrição, a cadeia de permuta poderá executar uma transferência de bloco de bits (bitblt). O bitblt causa uma cópia de alongamento extra, bem como um maior uso de memória de vídeo, e é difícil de detectar. Para evitar esse problema, enumere os modos de exibição e inicialize a descrição da cadeia de permuta corretamente antes de criar a cadeia de permuta. Isso garantirá o desempenho máximo ao inverter no modo de tela inteira e evitar a sobrecarga de memória extra.

### <a name="multithread-considerations"></a>Considerações sobre multithread

Ao usar o DXGI em um aplicativo com vários threads, você precisa ter cuidado para evitar a criação de um deadlock, em que dois threads diferentes estão aguardando a conclusão uns dos outros. Há duas situações em que isso pode ocorrer.

-   O thread de renderização não é o thread de bomba de mensagem.
-   O thread que executa uma API DXGI não é o mesmo thread que criou a janela.

Tenha cuidado para nunca fazer com que o thread de bomba de mensagem aguarde no thread de renderização ao usar cadeias de permuta de tela inteira. Por exemplo, chamar [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) (do thread de renderização) pode fazer com que o thread de renderização Espere no thread de bombeamento de mensagem. Quando ocorrer uma alteração no modo, esse cenário será possível se **Present1** chamar:: SetWindowPos () ou:: setwindowstyle () e qualquer um desses métodos chamar:: SendMessage (). Nesse cenário, se o thread de bombeamento de mensagem tiver uma seção crítica para protegê-lo ou se o thread de renderização estiver bloqueado, os dois threads serão deadlocks.

Para obter mais informações sobre como usar DXGI com vários threads, consulte [multithreading e dxgi](../direct3d11/overviews-direct3d-11-render-multi-thread-intro.md).

## <a name="dxgi-responses-from-dllmain"></a>Respostas de DXGI do DLLMain

Como uma função [**DllMain**](../dlls/dllmain.md) não pode garantir a ordem na qual ela carrega e descarrega DLLs, recomendamos que a função **DllMain** do seu aplicativo não chame funções ou métodos de Direct3D ou dxgi, incluindo funções ou métodos que criam ou liberam objetos. Se a função **DllMain** do seu aplicativo chamar um componente específico, esse componente poderá chamar outra DLL que não está presente no sistema operacional, o que faz com que o sistema operacional falhe. Direct3D e DXGI podem carregar um conjunto de DLLs, normalmente um conjunto de drivers, que difere de computador a computador. Portanto, mesmo que seu aplicativo não falhe em seus computadores de desenvolvimento e teste quando sua função **DllMain** chamar funções ou métodos de Direct3D ou dxgi, ele poderá falhar quando for executado em outro computador.

Para impedir que você crie um aplicativo que pode causar falha no sistema operacional, DXGI fornece as seguintes respostas nas situações especificadas:

-   Se a função [**DllMain**](../dlls/dllmain.md) do seu aplicativo liberar sua última referência a uma fábrica DXGI, DXGI gerará uma exceção.
-   Se a função [**DllMain**](../dlls/dllmain.md) do seu aplicativo criar uma fábrica DXGI, DXGI retornará um código de erro.

## <a name="dxgi-11-changes"></a>Alterações de DXGI 1,1

Adicionamos a funcionalidade a seguir no DXGI 1,1.

-   Suporte a superfícies compartilhada sincronizadas

    As superfícies compartilhadas sincronizadas para o Direct3D 10,1 e o Direct3D 11 permitem o compartilhamento eficiente de superfície de leitura e gravação entre vários dispositivos Direct3D (o compartilhamento entre dispositivos Direct3D 10 e Direct3D 11 é possível). Consulte [**IDXGIKeyedMutex:: AcquireSync**](/windows/win32/api/DXGI/nf-dxgi-idxgikeyedmutex-acquiresync) e [**IDXGIKeyedMutex:: ReleaseSync**](/windows/win32/api/DXGI/nf-dxgi-idxgikeyedmutex-releasesync).

-   Suporte de alta cor

    Dá suporte ao \_ \_ formato dxgi R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM.

-   [**IDXGIDevice1:: SetMaximumFrameLatency**](/windows/win32/api/DXGI/nf-dxgi-idxgidevice1-setmaximumframelatency) e [ **IDXGIDevice1:: GetMaximumFrameLatency**](/windows/win32/api/DXGI/nf-dxgi-idxgidevice1-getmaximumframelatency)
-   [**IDXGIFactory1:: EnumAdapters1**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) enumera adaptadores locais sem monitores ou saídas anexados, bem como adaptadores com saídas anexadas. O primeiro adaptador retornado será o adaptador local no qual a área de trabalho principal é exibida.
-   Suporte ao formato BGRA

    Formato \_ dxgi \_ B8G8R8A8 \_ UNORM e dxgi \_ \_ B8G8R8A8 \_ UNORM \_ sRGB, consulte [**IDXGISurface1:: GetDC**](/windows/win32/api/DXGI/nf-dxgi-idxgisurface1-getdc) e [**IDXGISurface1:: ReleaseDC**](/windows/win32/api/DXGI/nf-dxgi-idxgisurface1-releasedc).

## <a name="dxgi-12-changes"></a>Alterações de DXGI 1,2

Adicionamos a funcionalidade a seguir no DXGI 1,2.

-   Cadeia de permuta estéreo
-   [Cadeia de permuta do flip-Model](dxgi-flip-model.md)
-   Apresentação otimizada (rolagem, retângulos sujos e rotação)
-   Recursos compartilhados e sincronização aprimorados
-   [Duplicação de área de trabalho](desktop-dup-api.md)
-   Uso otimizado da memória de vídeo
-   Suporte para formatos de 16 bits por pixel (BPP) ( \_ formato dxgi \_ B5G6R5 \_ UNORM, \_ formato dxgi \_ B5G5R5A1 \_ UNORM, \_ formato dxgi \_ B4G4R4A4 \_ UNORM)
-   APIs de depuração

Para obter mais informações sobre DXGI 1,2, consulte [melhorias do dxgi 1,2](dxgi-1-2-improvements.md).

## <a name="related-topics"></a>Tópicos relacionados

[Guia de programação para DXGI](dx-graphics-dxgi-overviews.md)
