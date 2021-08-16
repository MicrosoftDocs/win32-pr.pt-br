---
title: Aprimoramentos do Direct3D 9Ex
description: Este tópico descreve Windows suporte adicionado da Windows 7 para o Modo de In flip presente e suas estatísticas presentes associadas no Direct3D 9Ex e Gerenciador de Janelas da Área de Trabalho.
ms.assetid: cb92a162-57eb-4aee-af7a-c8ece37075a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3221b805f07408b27e19a00a42ca0c4733ea725bd32a51b5b3e340b48d2070f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118796961"
---
# <a name="direct3d-9ex-improvements"></a>Aprimoramentos do Direct3D 9Ex

Este tópico descreve Windows suporte adicionado da Windows 7 para o Modo de In flip presente e suas estatísticas presentes associadas no Direct3D 9Ex e Gerenciador de Janelas da Área de Trabalho. Os aplicativos de destino incluem aplicativos de apresentação baseados em taxa de quadros ou vídeo. Os aplicativos que usam o Modo de Indução Direct3D 9Ex Presente reduzem a carga de recursos do sistema quando a DWM está habilitada. Os aprimoramentos de estatísticas presentes associados ao Modo de In flip present permitem que os aplicativos Direct3D 9Ex controlem melhor a taxa de apresentação fornecendo comentários em tempo real e mecanismos de correção. Explicações detalhadas e ponteiros para recursos de exemplo são incluídos.

Este tópico inclui as seções a seguir.

-   [O que foi aprimorado sobre o Direct3D 9Ex para Windows 7](#whats-improved-about-direct3d-9ex-for-windows-7)
-   [Apresentação do modo de in flip do Direct3D 9EX](#direct3d-9ex-flip-mode-presentation)
-   [Modelo de programação e APIs](#programming-model-and-apis)
    -   [Como optar pelo modelo de in flip do Direct3D 9Ex](#how-to-opt-into-the-direct3d-9ex-flip-model)
    -   [Diretrizes de design para aplicativos de modelo flip do Direct3D 9Ex](#design-guidelines-for-direct3d-9ex-flip-model-applications)
    -   [Sincronização de quadros de aplicativos de modelo de in flip do Direct3D 9Ex](#frame-synchronization-of-direct3d-9ex-flip-model-applications)
    -   [Sincronização de quadros para aplicativos em janelas quando a DWM está desligada](#frame-synchronization-for-windowed-applications-when-dwm-is-off)
-   [Passo a passo de um modelo de in flip do Direct3D 9Ex e exemplo de estatísticas de apresentação](#walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample)
    -   [Resumo da programação Recomendações para sincronização de quadros](#summary-of-programming-recommendations-for-frame-synchronization)
-   [Conclusão sobre aprimoramentos do Direct3D 9Ex](#conclusion-about-direct3d-9ex-improvements)
-   [Chamar para ação](#call-to-action)
-   [Tópicos relacionados](#related-topics)

## <a name="whats-improved-about-direct3d-9ex-for-windows-7"></a>O que foi aprimorado sobre o Direct3D 9Ex para Windows 7

A apresentação do Modo de In flip do Direct3D 9Ex é um modo aprimorado de apresentação de imagens no Direct3D 9Ex que entrega com eficiência as imagens renderizadas para Windows 7 Gerenciador de Janelas da Área de Trabalho (DWM) para composição. A partir Windows Vista, a DWM compõe toda a Área de Trabalho. Quando a DWM está habilitada, os aplicativos de modo em janela apresentam seu conteúdo na Área de Trabalho usando um método chamado Modo Blt Presente para DWM (ou Modelo Blt). Com o modelo Blt, a DWM mantém uma cópia da superfície renderizada do Direct3D 9Ex para composição desktop. Quando o aplicativo é atualizado, o novo conteúdo é copiado para a superfície DWM por meio de um blt. Para aplicativos que contêm conteúdo do Direct3D e GDI, os dados GDI também são copiados para a superfície DWM.

Disponível no Windows 7, o Modo de Invasão Presente para DWM (ou Modelo de Invasão) é um novo método de apresentação que, essencialmente, permite passar alças de superfícies de aplicativo entre aplicativos de modo de janela e DWM. Além de salvar recursos, o Flip Model dá suporte a estatísticas atuais aprimoradas.

As estatísticas presentes são informações de tempo de quadros que os aplicativos podem usar para sincronizar fluxos de áudio e vídeo e recuperar-se de falhas de reprodução de vídeo. As informações de tempo de quadros nas estatísticas atuais permitem que os aplicativos ajustem a taxa de apresentação de seus quadros de vídeo para uma apresentação mais suave. No Windows Vista, em que a DWM mantém uma cópia correspondente da superfície de quadro para composição da área de trabalho, os aplicativos podem usar estatísticas atuais fornecidas pela DWM. Esse método de obtenção de estatísticas atuais ainda estará disponível no Windows 7 para aplicativos existentes.

No Windows 7, os aplicativos baseados no Direct3D 9Ex que adotam o Flip Model devem usar APIs D3D9Ex para obter estatísticas presentes. Quando a DWM está habilitada, o modo em janelas e o modo exclusivo de tela inteira Os aplicativos Direct3D 9Ex podem esperar as mesmas informações de estatísticas presentes ao usar o Modelo de In flip. As estatísticas atuais do Modelo de In flip do Direct3D 9Ex permitem que os aplicativos consultem estatísticas presentes em tempo real, em vez de depois que o quadro é mostrado na tela; as mesmas informações de estatísticas atuais estão disponíveis para aplicativos habilitados para modo Flip-Model janela como aplicativos de tela inteira; um sinalizador adicionado nas APIs D3D9Ex permite que aplicativos Flip Model descartem efetivamente quadros tardias no momento da apresentação.

O Modelo de In flip do Direct3D 9Ex deve ser usado por novos aplicativos de apresentação baseados em taxa de quadros ou vídeo destinados Windows 7. Devido à sincronização entre o DWM e o runtime do Direct3D 9Ex, os aplicativos que usam Flip Model devem especificar entre 2 e 4 backbuffers para garantir uma apresentação suave. Os aplicativos que usam as informações de estatísticas presentes se beneficiarão do uso de Flip Model habilitado para aprimoramentos de estatísticas.

## <a name="direct3d-9ex-flip-mode-presentation"></a>Apresentação do modo de in flip do Direct3D 9EX

As melhorias de desempenho do Modo de Indução Direct3D 9Ex Presentes são significativas no sistema quando a DWM está em e quando o aplicativo está no modo de janela, em vez de no modo exclusivo de tela inteira. A tabela e a ilustração a seguir mostram uma comparação simplificada de usos de largura de banda de memória e leituras do sistema e gravações de aplicativos em janela que escolhem Inverter Modelo versus o modelo BLT de uso padrão.



| Modo Blt presente no DWM                                                                                                 | Modo de in flip D3D9Ex presente ao DWM                                             |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| 1. O aplicativo atualiza seu quadro (Gravação)<br/>                                                                 | 1. O aplicativo atualiza seu quadro (Gravação)<br/>                     |
| 2. O runtime do Direct3D copia o conteúdo da superfície para uma superfície de redirecionamento DWM (Leitura, Gravação)<br/>                       | 2. O runtime do Direct3D passa a superfície do aplicativo para o DWM<br/>        |
| 3. Depois que a cópia de superfície compartilhada for concluída, a DWM renderizará a superfície do aplicativo na tela (Leitura, Gravação)<br/> | 3. O DWM renderiza a superfície do aplicativo na tela (Leitura, Gravação)<br/> |



 

![ilustração de uma comparação do modelo blt e do modelo de invasão](images/blt-flip-mode-present.png)

O Modo de Inatividade Presente reduz o uso de memória do sistema reduzindo o número de leituras e gravações pelo runtime do Direct3D para a composição de quadro em janela pela DWM. Isso reduz o consumo de energia do sistema e o uso geral de memória.

Os aplicativos podem aproveitar o Modo de Invasão direct3D 9Ex apresentam aprimoramentos de estatísticas quando o DWM está em, independentemente de o aplicativo estar no modo de janela ou no modo exclusivo de tela inteira.

## <a name="programming-model-and-apis"></a>Modelo de programação e APIs

Novos aplicativos de mesagem de taxa de quadros ou vídeo que usam APIs direct3D 9Ex no Windows 7 podem aproveitar a economia de memória e energia e a apresentação aprimorada oferecida pelo Modo de Indução Presente durante a execução no Windows 7. (Ao executar em versões Windows anteriores, o runtime do Direct3D assume o aplicativo como Modo Blt Presente.)

O Modo de Invasão Presente implica que o aplicativo pode aproveitar os comentários e mecanismos de correção de estatísticas presentes em tempo real quando o DWM está. No entanto, os aplicativos que usam o Modo de In flip Present devem estar cientes das limitações ao usarem a renderização simultânea da API GDI.

Você pode modificar aplicativos existentes para aproveitar o Modo de In flip presente, com os mesmos benefícios e advertências que os aplicativos recém-desenvolvidos.

### <a name="how-to-opt-into-the-direct3d-9ex-flip-model"></a>Como optar pelo modelo de in flip do Direct3D 9Ex

Os aplicativos Direct3D 9Ex destinados ao Windows 7 podem optar pelo Modelo de Invasão criando a cadeia de permuta com o valor de enumeração [**\_ FLIPEX D3DSWAPEFFECT.**](/windows/desktop/direct3d9/d3dswapeffect) Para optar pelo Modelo de Inatividade, os aplicativos especificam a estrutura [**D3DPRESENT \_ PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) e, em seguida, passam um ponteiro para essa estrutura quando chamam a API [**IDirect3D9Ex::CreateDeviceEx.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) Esta seção descreve como os aplicativos direcionados Windows 7 usam **IDirect3D9Ex::CreateDeviceEx** para optar pelo Modelo de Invigência. Para obter mais informações sobre a API **IDirect3D9Ex::CreateDeviceEx,** consulte **IDirect3D9Ex::CreateDeviceEx no MSDN**.

Para sua conveniência, a sintaxe [**de \_ PARÂMETROS D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) [**e IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) é repetida aqui.

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

``` syntax
typedef struct D3DPRESENT_PARAMETERS {
    UINT BackBufferWidth, BackBufferHeight;
    D3DFORMAT BackBufferFormat;
    UINT BackBufferCount;
    D3DMULTISAMPLE_TYPE MultiSampleType;
    DWORD MultiSampleQuality;
    D3DSWAPEFFECT SwapEffect;
    HWND hDeviceWindow;
    BOOL Windowed;
    BOOL EnableAutoDepthStencil;
    D3DFORMAT AutoDepthStencilFormat;
    DWORD Flags;
    UINT FullScreen_RefreshRateInHz;
    UINT PresentationInterval;
} D3DPRESENT_PARAMETERS, *LPD3DPRESENT_PARAMETERS;
```

Ao modificar aplicativos Direct3D 9Ex para Windows 7 para optar pelo Modelo de Inatividade, considere os seguintes itens sobre os membros especificados de [**\_ PARÂMETROS D3DPRESENT:**](/windows/desktop/direct3d9/d3dpresent-parameters)

<dl> <dt>

**BackBufferCount**
</dt> <dd>

(Windows somente 7)

Quando **SwapEffect** é definido como o novo tipo de efeito de cadeia de permuta D3DSWAPEFFECT FLIPEX, a contagem de buffers de fundo deve ser igual ou maior que 2, para evitar uma penalidade de desempenho do aplicativo como resultado da espera do buffer Atual anterior a ser liberado \_ pelo DWM.

Quando o aplicativo também usa estatísticas presentes associadas a D3DSWAPEFFECT FLIPEX, é recomendável definir a contagem de buffers de fundo como de \_ 2 a 4.

O uso de D3DSWAPEFFECT FLIPEX no Windows Vista ou versões anteriores do sistema operacional retornará uma falha \_ de [**CreateDeviceEx.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)

</dd> <dt>

**Swapeffect**
</dt> <dd>

(Windows somente 7)

O novo tipo de efeito de cadeia de permuta DE FLIPEX D3DSWAPEFFECT designa quando um aplicativo está adotando o Modo de In flip \_ presente na DWM. Ele permite ao aplicativo o uso mais eficiente de memória e energia e também permite que o aplicativo aproveite as estatísticas presentes de tela inteira no modo em janelas. O comportamento do aplicativo de tela inteira não é afetado. Se Windowed for definido como **TRUE** e **SwapEffect** estiver definido como D3DSWAPEFFECT FLIPEX, o runtime criará um buffer de retorno extra e girará qualquer alça que pertence ao buffer que se torna o buffer frontal no momento da \_ apresentação.

</dd> <dt>

**Sinalizadores**
</dt> <dd>

(Windows somente 7)

O [sinalizador D3DPRESENTFLAG \_ LOCKABLE \_ BACKBUFFER](/windows/desktop/direct3d9/d3dpresentflag) não poderá ser definido se **SwapEffect** estiver definido como o novo tipo de efeito de cadeia de permuta [**\_ FLIPEX D3DSWAPEFFECT.**](/windows/desktop/direct3d9/d3dswapeffect)

</dd> </dl>

### <a name="design-guidelines-for-direct3d-9ex-flip-model-applications"></a>Diretrizes de design para aplicativos de modelo flip do Direct3D 9Ex

Use as diretrizes nas seções a seguir para criar seus aplicativos direct3D 9Ex Flip Model.

### <a name="use-flip-mode-present-in-a-separate-hwnd-from-blt-mode-present"></a>Usar o modo de in flip presente em um HWND separado do modo Blt presente

Os aplicativos devem usar o modo de inversões direct3D 9Ex presente em um HWND que também não é direcionado por outras APIs, incluindo o Modo Blt Present Direct3D 9Ex, outras versões do Direct3D ou GDI. O Modo de Inversões Presente pode ser usado para apresentar às janelas filho; Ou seja, os aplicativos podem usar o Flip Model quando ele não é misto com o modelo Blt no mesmo HWND, conforme mostrado nas ilustrações a seguir.

![ilustração da janela pai direct3d e de uma janela filho gdi, cada uma com seu próprio hwnd](images/parent-d3d.png)

![ilustração da janela pai gdi e uma janela filho direct3d, cada uma com seu próprio hwnd](images/parent-gdi.png)

Como o Modelo Blt mantém uma cópia adicional da superfície, o GDI e outros conteúdos do Direct3D podem ser adicionados ao mesmo HWND por meio de atualizações por etapa do Direct3D e da GDI. Usando o Modelo de Invasão, somente o conteúdo direct3D 9Ex nas cadeias de permuta [**\_ FLIPEX D3DSWAPEFFECT**](/windows/desktop/direct3d9/d3dswapeffect) que são passadas para a DWM ficará visível. Todas as outras atualizações de conteúdo do Blt Model Direct3D ou GDI serão ignoradas, conforme mostrado nas ilustrações a seguir.

![ilustração do texto gdi que pode não ser exibido se o modelo de in flip for usado e o conteúdo de direct3d e gdi estiver no mesmo hwnd](images/d3d-gdi-same-hwnd.png)

![ilustração do conteúdo de direct3d e gdi no qual dwm está habilitado e o aplicativo está no modo de janela](images/d3d-gdinotext-same-hwnd.png)

Portanto, o Modelo de Invasão deve ser habilitado para superfícies de buffers de cadeia de permuta em que o Modelo de In flip do Direct3D 9Ex renderiza apenas para todo o HWND.

### <a name="do-not-use-flip-model-with-gdis-scrollwindow-or-scrollwindowex"></a>Não usar o modelo de indução com ScrollWindow ou ScrollWindowEx da GDI

Alguns aplicativos Direct3D 9Ex usam as funções ScrollWindow ou ScrollWindowEx da GDI para atualizar o conteúdo da janela quando um evento de rolagem do usuário é disparado. ScrollWindow e ScrollWindowEx executam blts de conteúdo da janela na tela à medida que uma janela é rolada. Essas funções também exigem atualizações de modelo BLT para conteúdo GDI e Direct3D 9Ex. Os aplicativos que usam uma das funções não exibirão necessariamente o conteúdo visível da janela rolando na tela quando o aplicativo estiver no modo de janela e a DWM estiver habilitada. Recomendamos que você não use as APIs ScrollWindow e ScrollWindowEx da GDI em seus aplicativos e, em vez disso, redesenhar o conteúdo na tela em resposta à rolagem.

### <a name="use-one-d3dswapeffect_flipex-swap-chain-per-hwnd"></a>Usar uma cadeia de permuta FLIPEX D3DSWAPEFFECT \_ por HWND

Os aplicativos que usam o Modelo de Invasão não devem usar várias cadeias de permuta do Modelo de Invasão visando o mesmo HWND.

### <a name="frame-synchronization-of-direct3d-9ex-flip-model-applications"></a>Sincronização de quadros de aplicativos de modelo de in flip do Direct3D 9Ex

As estatísticas presentes são informações de tempo de quadros que os aplicativos de mídia usam para sincronizar fluxos de áudio e vídeo e recuperar-se de falhas de reprodução de vídeo. Para habilitar a disponibilidade de estatísticas atual, o aplicativo Direct3D 9Ex deve garantir que o parâmetro *BehaviorFlags* que o aplicativo passa para [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) contém o sinalizador de comportamento do dispositivo [D3DCREATE \_ ENABLE \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate).

Para sua conveniência, a sintaxe [**de IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) é repetida aqui.

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

O Modelo de In flip do Direct3D 9Ex adiciona o sinalizador de apresentação [D3DPRESENT \_ FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent) que impõe o comportamento do sinalizador de apresentação [D3DPRESENT \_ INTERVAL \_ IMMEDIATE.](/windows/desktop/direct3d9/d3dpresent) O aplicativo Direct3D 9Ex especifica esses sinalizadores de apresentação no parâmetro *dwFlags* que o aplicativo passa para [**IDirect3DDevice9Ex::P resentEx,**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex)conforme mostrado aqui.

``` syntax
HRESULT PresentEx(
  CONST RECT *pSourceRect,
  CONST RECT *pDestRect,
  HWND hDestWindowOverride,
  CONST RGNDATA *pDirtyRegion,
  DWORD dwFlags
);
```

Ao modificar seu aplicativo Direct3D 9Ex para Windows 7, você deve considerar as seguintes informações sobre os sinalizadores de apresentação [D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) especificados:

<dl> <dt>

[D3DPRESENT \_ FEZTFLIP](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

Esse sinalizador está disponível apenas no modo de tela inteira ou

(Windows somente 7)

quando o aplicativo define o membro **SwapEffect** [**de D3DPRESENT \_ PARAMETERS como D3DSWAPEFFECT**](/windows/desktop/direct3d9/d3dpresent-parameters) [**\_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) em uma chamada para [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).

</dd> <dt>

[D3DPRESENT \_ FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

(Windows somente 7)

Esse sinalizador só poderá ser especificado se o aplicativo define o membro **SwapEffect** de [**D3DPRESENT \_ PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) como [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) em uma chamada para [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex). O aplicativo pode usar esse sinalizador para atualizar imediatamente uma superfície com vários quadros posteriormente na fila DWM Present, basicamente ignorando quadros intermediários.

Aplicativos habilitados para FlipEx em janelas podem usar esse sinalizador para atualizar imediatamente uma superfície com um quadro que está posteriormente na fila DWM Present, ignorando quadros intermediários. Isso é especialmente útil para aplicativos de mídia que querem descartar quadros detectados com atraso e apresentar quadros subsequentes no momento da composição. [**IDirect3DDevice9Ex::P resentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) retornará um erro de parâmetro inválido se esse sinalizador for especificado incorretamente.

</dd> </dl>

Para obter informações de estatísticas presentes, o aplicativo obtém a estrutura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) chamando a API [**IDirect3DSwapChain9Ex::GetPresentStatistics.**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85))

A [**estrutura D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) contém estatísticas sobre chamadas [**IDirect3DDevice9Ex::P resentEx.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) O dispositivo deve ser criado usando uma [**chamada IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) com o sinalizador [D3DCREATE \_ ENABLE \_ PRESENTSTATS.](/windows/desktop/direct3d9/d3dcreate) Caso contrário, os dados [**retornados por GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) serão indefinido. Uma cadeia de permuta direct3D 9Ex habilitada para flip-model fornece informações de estatísticas presentes nos modos de tela inteira e janela.

Para cadeias de permuta direct3D 9Ex habilitadas para Blt-Model no modo de janela, todos os valores de estrutura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) serão zeros.

Para as estatísticas presentes do [**FlipEx, GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) retorna D3DERR \_ PRESENT \_ STATISTICS \_ DISJOINT nas seguintes situações:

-   Primeira chamada para [**GetPresentStatistics,**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) que indica o início de uma sequência
-   Transição de DWM de para desligado
-   Alteração de modo: o modo em janelas para ou de tela inteira ou tela inteira para transições de tela inteira

Para sua conveniência, a sintaxe [**de GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) é repetida aqui.

``` syntax
HRESULT GetPresentStatistics(
  D3DPRESENTSTATS * pPresentationStatistics
);
```

O método [**IDirect3DSwapChain9Ex::GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) retorna a última PresentCount, ou seja, a ID Atual da última chamada Present bem-sucedida feita por um dispositivo de exibição associado à cadeia de permuta. Essa ID Atual é o valor do **membro PresentCount** da [**estrutura D3DPRESENTSTATS.**](/windows/desktop/direct3d9/d3dpresentstats) Para cadeias de permuta direct3D 9Ex habilitadas para Blt-Model, enquanto estiver no modo de janela, todos os valores de estrutura **D3DPRESENTSTATS** serão zeros.

Para sua conveniência, a sintaxe [**de IDirect3DSwapChain9Ex::GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) é repetida aqui.

``` syntax
HRESULT GetLastPresentCount(
  UINT * pLastPresentCount
);
```

Ao modificar seu aplicativo Direct3D 9Ex para Windows 7, considere as seguintes informações sobre a estrutura [**D3DPRESENTSTATS:**](/windows/desktop/direct3d9/d3dpresentstats)

-   O valor PresentCount que [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) retorna não é atualizado quando uma chamada [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) com D3DPRESENT DONOTWAIT especificada no parâmetro \_ *dwFlags* retorna falha.
-   Quando [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) é chamado com D3DPRESENT SEMPRETFLIP, uma chamada GetPresentStatistics é bem-sucedida, mas não retorna uma estrutura \_ [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) atualizada quando o aplicativo está no modo de janela. [](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85))
-   **PresentRefreshCount** versus **SyncRefreshCount** em [**D3DPRESENTSTATS:**](/windows/desktop/direct3d9/d3dpresentstats)
    -   **PresentRefreshCount é** igual a **SyncRefreshCount** quando o aplicativo é presente em cada vsync.
    -   **SyncRefreshCount** é obtido no intervalo vsync quando o presente foi enviado, **SyncQPCTime** é aproximadamente o tempo associado ao intervalo vsync.

``` syntax
typedef struct _D3DPRESENTSTATS {
    UINT PresentCount;
    UINT PresentRefreshCount;
    UINT SyncRefreshCount;
    LARGE_INTEGER SyncQPCTime;
    LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```

### <a name="frame-synchronization-for-windowed-applications-when-dwm-is-off"></a>Sincronização de quadros para aplicativos em janelas quando a DWM está desligada

Quando a DWM está desligada, os aplicativos em janela são exibidos diretamente na tela do monitor sem passar por uma cadeia de invasões. No Windows Vista, não há suporte para obter informações de estatísticas de quadro para aplicativos em janela quando a DWM está desligada. Para manter uma API em que os aplicativos não precisam estar cientes de DWM, Windows 7 retornará informações de estatísticas de quadro para aplicativos em janela quando a DWM estiver desligada. As estatísticas de quadro retornadas quando a DWM está desligada são apenas estimativas.

## <a name="walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample"></a>Walk-Through de um modelo de in flip do Direct3D 9Ex e exemplo de estatísticas de apresentação

**Para optar pela apresentação do FlipEx para o exemplo do Direct3D 9Ex**

1.  Verifique se o aplicativo de exemplo está em execução no Windows 7 ou versão posterior do sistema operacional.
2.  De definir o membro **SwapEffect** [**de D3DPRESENT \_ PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) como [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) em uma chamada para [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).


```C++
    OSVERSIONINFO version;
    ZeroMemory(&version, sizeof(version));
    version.dwOSVersionInfoSize = sizeof(version);
    GetVersionEx(&version);
    
    // Sample would run only on Win7 or higher
    // Flip Model present and its associated present statistics behavior are only available on Windows 7 or higher operating system
    bool bIsWin7 = (version.dwMajorVersion > 6) || 
        ((version.dwMajorVersion == 6) && (version.dwMinorVersion >= 1));

    if (!bIsWin7)
    {
        MessageBox(NULL, L"This sample requires Windows 7 or higher", NULL, MB_OK);
        return 0;
    }
```



**Para também optar pelo exemplo de Estatísticas presentes associadas ao FlipEx para Direct3D 9Ex**

-   Defina [D3DCREATE \_ ENABLE \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) no *parâmetro BehaviorFlags* [**de CreateDeviceEx.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)


```C++
    // Set up the structure used to create the D3DDevice
    D3DPRESENT_PARAMETERS d3dpp;
    ZeroMemory(&d3dpp, sizeof(d3dpp));

    d3dpp.Windowed = TRUE;
    d3dpp.SwapEffect = D3DSWAPEFFECT_FLIPEX;        // Opts into Flip Model present for D3D9Ex swapchain
    d3dpp.BackBufferFormat = D3DFMT_X8R8G8B8;
    d3dpp.BackBufferWidth = 256;                
    d3dpp.BackBufferHeight = 256;
    d3dpp.BackBufferCount = QUEUE_SIZE;
    d3dpp.PresentationInterval = D3DPRESENT_INTERVAL_ONE;

    g_iWidth = d3dpp.BackBufferWidth;
    g_iHeight = d3dpp.BackBufferHeight;

    // Create the D3DDevice with present statistics enabled - set D3DCREATE_ENABLE_PRESENTSTATS for behaviorFlags parameter
    if(FAILED(g_pD3D->CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                      D3DCREATE_HARDWARE_VERTEXPROCESSING | D3DCREATE_ENABLE_PRESENTSTATS,
                                      &d3dpp, NULL, &g_pd3dDevice)))
    {
        return E_FAIL;
    }
```



**Para evitar, detectar e recuperar-se de falhas**

1.  Fila Chamadas presentes: a contagem de backbuffer recomendada é de 2 a 4.
2.  O exemplo do Direct3D 9Ex adiciona um backbuffer implícito, o tamanho real da fila atual é a contagem de backbuffer + 1.
3.  Criar estrutura de filas de presentes auxiliares para armazenar todas as IDs Presentes (Present ID) enviadas com êxito (PresentCount) e PresentRefreshCount associada, calculada/esperada.
4.  Para detectar a ocorrência de falha:

    -   Chame [**GetPresentStatistics.**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85))
    -   Obtenha a ID Atual (PresentCount) e a contagem vsync em que o quadro é mostrado (PresentRefreshCount) do quadro cujas estatísticas atuais são obtidas.
    -   Recupere o PresentRefreshCount esperado (TargetRefresh no código de exemplo) associado à ID Atual.
    -   Se PresentRefreshCount real for posterior ao esperado, ocorrerá uma falha.

5.  Para se recuperar de uma falha:

    -   Calcule quantos quadros ignorar (g \_ iImmediates variable no código de exemplo).
    -   Apresente os quadros ignorados com o intervalo D3DPRESENT \_ FORCEIMMEDIATE.

**Considerações sobre detecção e recuperação de falhas**

1.  A recuperação de falhas leva N (g variável iQueueDelay no código de exemplo) número de chamadas presentes em que \_ N (g \_ iQueueDelay) é igual a g iImmediates mais o comprimento da fila \_ Present, ou seja:

    -   Ignorar quadros com o intervalo presente D3DPRESENT \_ FORCEIMMEDIATE, mais
    -   Apresenta na Fila que precisam ser processados

2.  Definir um limite para o comprimento da falha (LIMITE DE RECUPERAÇÃO DE FALHA \_ \_ no exemplo). Se o aplicativo de exemplo não puder se recuperar de uma falha muito longa (ou seja, 1 segundo ou 60 vsyncs no monitor de 60Hz), pule sobre a animação intermitente e redefinir a fila auxiliar Presente.


```C++
VOID Render()
{
    g_pd3dDevice->Clear(0, NULL, D3DCLEAR_TARGET, D3DCOLOR_XRGB(0, 0, 0), 1.0f, 0);

    g_pd3dDevice->BeginScene();

    // Compute new animation parameters for time and frame based animations

    // Time-based is a difference between base and current SyncRefreshCount
    g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
    // Frame-based is incrementing frame value
    g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;

    RenderBlurredMesh(TRUE);    // Time-based
    RenderBlurredMesh(FALSE);   // Frame-based

    g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;

    DrawText();

    g_pd3dDevice->EndScene();

    // Performs glitch recovery if glitch was detected
    if (g_bGlitchRecovery && (g_iImmediates > 0))
    {
        // If we have present immediates queued as a result of glitch detected, issue forceimmediate Presents for glitch recovery 
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE);
        g_iImmediates--;
        g_iShowingGlitchRecovery = MESSAGE_SHOW;
    }
    // Otherwise, Present normally
    else
    {
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, 0);
    }

    // Add to helper Present queue: PresentID + expected present refresh count of last submitted Present
    UINT PresentCount;
    g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
    g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);
    
    // QueueDelay specifies # Present calls to be processed before another glitch recovery attempt
    if (g_iQueueDelay > 0)
    {
        g_iQueueDelay--;
    }

    if (g_bGlitchRecovery)
    {
        // Additional DONOTFLIP presents for frame conversions, which basically follows the same logic, but without rendering
        for (DWORD i = 0; i < g_iDoNotFlipNum; i++)
        {
            if (g_TargetRefreshCount != -1)
            {
                g_TargetRefreshCount++;
                g_iFrameNumber++;
                g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
                g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;
                g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;
            }
            
            if (g_iImmediates > 0)
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE | D3DPRESENT_DONOTFLIP);
                g_iImmediates--;
            }
            else
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_DONOTFLIP);
            }
            UINT PresentCount;
            g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
            g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);

            if (g_iQueueDelay > 0)
            {
                g_iQueueDelay--;
            }
        }
    }

    // Check Present Stats info for glitch detection 
    D3DPRESENTSTATS PresentStats;

    // Obtain present statistics information for successfully displayed presents
    HRESULT hr = g_pd3dSwapChain->GetPresentStats(&PresentStats);

    if (SUCCEEDED(hr))
    {
        // Time-based update
        g_LastSyncRefreshCount = PresentStats.SyncRefreshCount;
        if ((g_SyncRefreshCount == -1) && (PresentStats.PresentCount != 0))
        {
            // First time SyncRefreshCount is reported, use it as base
            g_SyncRefreshCount = PresentStats.SyncRefreshCount;
        }

        // Fetch frame from the queue...
        UINT TargetRefresh = g_Queue.DequeueFrame(PresentStats.PresentCount);

        // If PresentStats returned a really old frame that we no longer have in the queue, just don't do any glitch detection
        if (TargetRefresh == FRAME_NOT_FOUND)
            return;

        if (g_TargetRefreshCount == -1)
        {
            // This is first time issued frame is confirmed by present stats, so fill target refresh count for all frames in the queue
            g_TargetRefreshCount = g_Queue.FillRefreshCounts(PresentStats.PresentCount, g_SyncRefreshCount);
        } 
        else
        {
            g_TargetRefreshCount++;
            g_iFrameNumber++;

            // To determine whether we're glitching, see if our estimated refresh count is confirmed
            // if the frame is displayed later than the expected vsync count
            if (TargetRefresh < PresentStats.PresentRefreshCount)
            {
                // then, glitch is detected!

                // If glitch is too big, don't bother recovering from it, just jump animation
                if ((PresentStats.PresentRefreshCount - TargetRefresh) > GLITCH_RECOVERY_LIMIT)
                {
                    g_iStartFrame += PresentStats.SyncRefreshCount - g_SyncRefreshCount;
                    ResetAnimation();
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;    
                } 
                // Otherwise, compute number of immediate presents to recover from it -- if we?re not still trying to recover from another glitch
                else if (g_iQueueDelay == 0)
                {
                      // skip frames to catch up to expected refresh count
                    g_iImmediates = PresentStats.PresentRefreshCount - TargetRefresh;
                    // QueueDelay specifies # Present calls before another glitch recovery 
                    g_iQueueDelay = g_iImmediates + QUEUE_SIZE;
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;
                }
            }
            else
            {
                // No glitch, reset glitch count
                g_iGlitchesInaRow = 0;
            }
        }
    }
    else if (hr == D3DERR_PRESENT_STATISTICS_DISJOINT)
    {
        // D3DERR_PRESENT_STATISTICS_DISJOINT means measurements should be started from the scratch (could be caused by mode change or DWM on/off transition)
        ResetAnimation();
    }

    // If we got too many glitches in a row, reduce framerate conversion factor (that is, render less frames)
    if (g_iGlitchesInaRow == FRAMECONVERSION_GLITCH_LIMIT)
    {
        if (g_iDoNotFlipNum < FRAMECONVERSION_LIMIT)
        {
            g_iDoNotFlipNum++;
        }
        g_iGlitchesInaRow = 0;
        g_iShowingDoNotFlipBump = MESSAGE_SHOW;
    }
}
```



**Cenário de exemplo**

-   A ilustração a seguir mostra um aplicativo com contagem de backbuffer de 4. O tamanho real da fila Atual é, portanto, 5.

    ![ilustração de quadros renderizados de aplicativos e fila presente](images/sample-scenario.png)

    O Quadro A é direcionado para ir para a tela na contagem de intervalos de sincronização de 1, mas foi detectado que ele foi mostrado na contagem de intervalos de sincronização de 4. Portanto, ocorreu uma falha. Os três quadros subsequentes são apresentados com D3DPRESENT \_ INTERVAL \_ FORCEIMMEDIATE. A falha deve levar um total de 8 chamadas presentes antes de ser recuperada – o próximo quadro será mostrado de acordo com sua contagem de intervalos de sincronização de alvo.

### <a name="summary-of-programming-recommendations-for-frame-synchronization"></a>Resumo da programação Recomendações para sincronização de quadros

-   Crie uma lista de backup de todas as IDs de LastPresentCount (obtidas por meio de [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)) e presentRefreshCount estimado associado de todos os Apresenta enviados.
    > [!Note]  
    > Quando o aplicativo chama [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) com D3DPRESENT SEMPRETFLIP, a chamada GetPresentStatistics é bem-sucedida, mas não retorna uma estrutura \_ [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) atualizada quando o aplicativo está no modo de janela. [](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85))

     

-   Chame [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) para obter o PresentRefreshCount real associado a cada ID atual dos quadros mostrados, para garantir que o aplicativo trata os retornos de falha da chamada.
-   Se PresentRefreshCount real for posterior ao estimado PresentRefreshCount, uma falha será detectada. Compensando enviando quadros de atraso presentes com D3DPRESENT \_ FORCEIMMEDIATE.
-   Quando um quadro for apresentado com atraso na fila Presente, todos os quadros na fila subsequentes serão apresentados com atraso. D3DPRESENT FORCEIMMEDIATE corrigirá apenas o próximo quadro a ser apresentado após todos os \_ quadros na fila. Portanto, a contagem de fila ou de backbuffer atual não deve ser muito longa, portanto, há menos falhas de quadro para acompanhar. A contagem ideal de backbuffer é de 2 a 4.
-   Se PresentRefreshCount estimado for posterior ao PresentRefreshCount real, poderá ter ocorrido uma reação de DWM. As seguintes soluções são possíveis:

    -   reduzindo o tamanho da fila atual
    -   reduzindo os requisitos de memória de GPU com qualquer outro meio, além de reduzir o tamanho da Fila Atual (ou seja, diminuir a qualidade, remover efeitos e assim por diante)
    -   especificando [**DwmEnableMMCSS**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenablemmcss) para evitar a throttling de DWM em geral

-   Verifique a funcionalidade de exibição do aplicativo e o desempenho das estatísticas de quadro nos seguintes cenários:

    -   com o DWM on e off
    -   modos exclusivos e em janelas de tela inteira
    -   hardware de capacidade inferior

-   Quando os aplicativos não podem se recuperar de um grande número de quadros com falhas com D3DPRESENT FORCEIMMEDIATE Presente, eles podem executar \_ as seguintes operações:

    -   reduzir o uso de CPU e GPU renderizar com menos carga de trabalho.
    -   no caso de decodificação de vídeo, decodificação mais rápido reduzindo a qualidade e, portanto, o uso de CPU e GPU.

## <a name="conclusion-about-direct3d-9ex-improvements"></a>Conclusão sobre os aprimoramentos do Direct3D 9Ex

no Windows 7, os aplicativos que exibem a taxa de quadros de vídeo ou medidor durante a apresentação podem optar pelo Flip Model. Os aprimoramentos de estatísticas atuais que estão associados ao flip Model Direct3D 9Ex podem beneficiar os aplicativos que sincronizam a apresentação por taxa de quadros, com comentários em tempo real para detecção e recuperação de problemas. Os desenvolvedores que adotam o modelo do Direct3D 9Ex flip devem ter como destino um HWND separado do conteúdo do GDI e da sincronização de taxa de quadros em conta. Consulte os detalhes neste tópico e a documentação do MSDN. Para obter mais documentação, consulte [DirectX Developer Center no MSDN](/previous-versions/windows/apps/hh452744(v=win.10)).

## <a name="call-to-action"></a>Plano de ação

incentivamos você a usar o modelo de inversão do Direct3D 9ex e suas estatísticas atuais no Windows 7 ao criar aplicativos que tentam sincronizar a taxa de quadros de apresentação ou se recuperar de falhas de exibição.

## <a name="related-topics"></a>Tópicos relacionados

[Central de desenvolvedores do DirectX no MSDN](/previous-versions/windows/apps/hh452744(v=win.10))
</dt> </dl>