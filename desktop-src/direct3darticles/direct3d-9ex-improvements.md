---
title: Aprimoramentos do Direct3D 9Ex
description: este tópico descreve o suporte adicionado do Windows 7 para o modo invertido presente e suas estatísticas atuais associadas no Direct3D 9ex e Gerenciador de Janelas da Área de Trabalho.
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

este tópico descreve o suporte adicionado do Windows 7 para o modo invertido presente e suas estatísticas atuais associadas no Direct3D 9ex e Gerenciador de Janelas da Área de Trabalho. Os aplicativos de destino incluem aplicativos de apresentação baseados em taxas de vídeo ou quadros. Os aplicativos que usam o modo de flip do Direct3D 9Ex presente reduzem a carga de recursos do sistema quando o DWM está habilitado. As melhorias de estatísticas atuais associadas ao modo Inverter apresentam a habilitação dos aplicativos do Direct3D 9Ex para controlar melhor a taxa de apresentação, fornecendo comentários em tempo real e mecanismos de correção. São incluídas explicações e ponteiros detalhados para recursos de exemplo.

Este tópico inclui as seções a seguir.

-   [o que melhorou sobre o Direct3D 9ex para Windows 7](#whats-improved-about-direct3d-9ex-for-windows-7)
-   [Apresentação do modo de flip do Direct3D 9EX](#direct3d-9ex-flip-mode-presentation)
-   [Modelo de programação e APIs](#programming-model-and-apis)
    -   [Como optar pelo modelo de inversão do Direct3D 9Ex](#how-to-opt-into-the-direct3d-9ex-flip-model)
    -   [Diretrizes de design para aplicativos de modelo do Direct3D 9Ex flip](#design-guidelines-for-direct3d-9ex-flip-model-applications)
    -   [Sincronização de quadros de aplicativos de modelo do Direct3D 9Ex flip](#frame-synchronization-of-direct3d-9ex-flip-model-applications)
    -   [Sincronização de quadros para aplicativos em janelas quando o DWM está desativado](#frame-synchronization-for-windowed-applications-when-dwm-is-off)
-   [Passo a passo de um modelo do Direct3D 9Ex flip e apresentar estatísticas de exemplo](#walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample)
    -   [resumo de Recomendações de programação para sincronização de quadros](#summary-of-programming-recommendations-for-frame-synchronization)
-   [Conclusão sobre os aprimoramentos do Direct3D 9Ex](#conclusion-about-direct3d-9ex-improvements)
-   [Plano de ação](#call-to-action)
-   [Tópicos relacionados](#related-topics)

## <a name="whats-improved-about-direct3d-9ex-for-windows-7"></a>o que melhorou sobre o Direct3D 9ex para Windows 7

a apresentação do modo inverter do direct3d 9ex é um modo aprimorado de apresentar imagens no Direct3D 9ex, que efetivamente transfere imagens renderizadas para Windows 7 Gerenciador de Janelas da Área de Trabalho (DWM) para composição. a partir do Windows Vista, o DWM compõe toda a área de trabalho. Quando o DWM está habilitado, os aplicativos de modo em janela apresentam seu conteúdo na área de trabalho usando um método chamado modo blt presente para DWM (ou modelo BLT). Com o modelo BLT, o DWM mantém uma cópia da superfície do Direct3D 9Ex renderizada para composição de área de trabalho. Quando o aplicativo é atualizado, o novo conteúdo é copiado para a superfície do DWM por meio de um blt. Para aplicativos que contêm conteúdo de Direct3D e GDI, os dados GDI também são copiados na superfície do DWM.

disponível no Windows 7, o modo Flip presente para o DWM (ou o Flip Model) é um novo método de apresentação que essencialmente habilita a passagem de identificadores de superfícies de aplicativos entre aplicativos de modo em janelas e DWM. Além de salvar recursos, o flip Model dá suporte a estatísticas de apresentação avançadas.

As estatísticas atuais são informações de tempo de quadro que os aplicativos podem usar para sincronizar fluxos de áudio e vídeo e recuperar-se de falhas de reprodução de vídeo. As informações de tempo de quadro em estatísticas atuais permitem que os aplicativos ajustem a taxa de apresentação de seus quadros de vídeo para uma apresentação mais suave. no Windows Vista, em que o DWM mantém uma cópia correspondente da superfície do quadro para composição de área de trabalho, os aplicativos podem usar as estatísticas atuais fornecidas pelo DWM. esse método de obtenção de estatísticas presentes ainda estará disponível no Windows 7 para aplicativos existentes.

no Windows 7, os aplicativos baseados no Direct3D 9ex que adotam o Flip Model devem usar APIs D3D9Ex para obter estatísticas atuais. Quando o DWM está habilitado, o modo em janela e o modo exclusivo de tela inteira aplicativos do Direct3D 9Ex podem esperar as mesmas informações de estatísticas presentes ao usar o flip Model. As estatísticas do Direct3D 9Ex flip Model presente permitem que os aplicativos consultem as estatísticas atuais em tempo real, em vez de após o quadro ter sido mostrado na tela; as mesmas informações de estatísticas presentes estão disponíveis para aplicativos habilitados para o modo de Flip-Model de janela como aplicativos de tela inteira; um sinalizador adicionado nas APIs D3D9Ex permite que os aplicativos de modelo de inversão descartem com eficiência quadros atrasados no momento da apresentação.

o modelo de Flip do Direct3D 9ex deve ser usado por novos aplicativos de apresentação baseados em taxa de vídeo ou de quadros direcionados Windows 7. Devido à sincronização entre o DWM e o tempo de execução do Direct3D 9Ex, os aplicativos que usam o modelo de flip devem especificar entre 2 e 4 buffers de reversão para garantir uma apresentação suave. Esses aplicativos que usam informações de estatísticas atuais se beneficiarão do uso dos aprimoramentos de estatísticas presentes do flip Model habilitado.

## <a name="direct3d-9ex-flip-mode-presentation"></a>Apresentação do modo de flip do Direct3D 9EX

As melhorias de desempenho do modo de inversão do Direct3D 9Ex presentes são significativas no sistema quando o DWM está ativado e quando o aplicativo está no modo de janela, em vez de em modo de tela inteira. A tabela e a ilustração a seguir mostram uma comparação simplificada de usos de largura de banda de memória e leituras do sistema e gravações de aplicativos em janelas que escolhem o modelo de flip versus o modelo de BLT de uso padrão.



| Modo blt presente para DWM                                                                                                 | Modo flip D3D9Ex presente para DWM                                             |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| 1. o aplicativo atualiza seu quadro (gravação)<br/>                                                                 | 1. o aplicativo atualiza seu quadro (gravação)<br/>                     |
| 2. o tempo de execução do Direct3D copia o conteúdo da superfície para uma superfície de redirecionamento do DWM (leitura, gravação)<br/>                       | 2. o tempo de execução do Direct3D passa a superfície do aplicativo para o DWM<br/>        |
| 3. após a cópia da superfície compartilhada ser concluída, o DWM renderiza a superfície do aplicativo na tela (leitura, gravação)<br/> | 3. o DWM renderiza a superfície do aplicativo na tela (leitura, gravação)<br/> |



 

![ilustração de uma comparação do modelo BLT e do flip Model](images/blt-flip-mode-present.png)

O modo Inverter apresenta redução do uso de memória do sistema, reduzindo o número de leituras e gravações pelo tempo de execução do Direct3D para a composição de quadro em janela pelo DWM. Isso reduz o consumo de energia do sistema e o uso geral da memória.

Os aplicativos podem tirar proveito do modo Inverter do Direct3D 9Ex presente nas melhorias de estatísticas quando o DWM está ativado, independentemente de o aplicativo estar no modo de janela ou em modo de tela inteira.

## <a name="programming-model-and-apis"></a>Modelo de programação e APIs

nova taxa de vídeo ou quadro-os aplicativos medir que usam as APIs do Direct3D 9ex no Windows 7 podem aproveitar a memória e a economia de energia e a apresentação aprimorada oferecida pelo modo Flip presente ao ser executado no Windows 7. (ao executar em versões anteriores do Windows, o tempo de execução do Direct3D usa como padrão o aplicativo para o modo Blt presente.)

O modo Inverter significa que o aplicativo pode aproveitar os comentários de estatísticas e os mecanismos de correção presentes em tempo real quando o DWM está ativado. No entanto, os aplicativos que usam o modo flip presente devem estar cientes das limitações quando usam a renderização simultânea da API GDI.

Você pode modificar os aplicativos existentes para aproveitar o modo invertido presente, com os mesmos benefícios e limitações que os aplicativos desenvolvidos recentemente.

### <a name="how-to-opt-into-the-direct3d-9ex-flip-model"></a>Como optar pelo modelo de inversão do Direct3D 9Ex

os aplicativos do Direct3D 9ex direcionados Windows 7 podem optar pelo Flip Model criando a cadeia de permuta com o valor de enumeração [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) . Para aceitar o modelo de inversão, os aplicativos especificam a estrutura de [**\_ parâmetros D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) e passam um ponteiro para essa estrutura quando chamam a API [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) . esta seção descreve como os aplicativos direcionados Windows 7 usam **IDirect3D9Ex:: CreateDeviceEx** para aceitar o modelo de inversão. Para obter mais informações sobre a API **IDirect3D9Ex:: CreateDeviceEx** , consulte **IDirect3D9Ex:: CreateDeviceEx no MSDN**.

Para sua conveniência, a sintaxe [**dos \_ parâmetros D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) e [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) é repetida aqui.

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

ao modificar aplicativos do Direct3D 9ex para Windows 7 para optar pelo Flip Model, você deve considerar os seguintes itens sobre os membros especificados dos [**\_ parâmetros D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters):

<dl> <dt>

**BackBufferCount**
</dt> <dd>

(somente Windows 7)

Quando **SwapEffect** é definido como o novo \_ tipo de efeito de cadeia de permuta D3DSWAPEFFECT FLIPEX, a contagem de buffers de fundo deve ser igual ou maior que 2, para evitar uma penalidade de desempenho de aplicativo como resultado da espera do buffer presente anterior a ser liberado pelo DWM.

Quando o aplicativo também usa as estatísticas atuais associadas ao D3DSWAPEFFECT \_ FLIPEX, recomendamos que você defina a contagem de buffers de fundo como de 2 a 4.

usar D3DSWAPEFFECT \_ FLIPEX no Windows Vista ou versões anteriores do sistema operacional retornará falha de [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).

</dd> <dt>

**SwapEffect**
</dt> <dd>

(somente Windows 7)

O novo \_ tipo de efeito de cadeia de permuta D3DSWAPEFFECT FLIPEX designa quando um aplicativo está adotando o modo invertido presente no DWM. Ele permite que o aplicativo tenha uso mais eficiente de memória e energia, além de permitir que o aplicativo aproveite as estatísticas de tela inteira em modo de janela. O comportamento do aplicativo de tela inteira não é afetado. Se a janela estiver definida como **true** e **SwapEffect** estiver definida como D3DSWAPEFFECT \_ FLIPEX, o tempo de execução criará um buffer de fundo extra e girará qualquer identificador que pertença ao buffer que se torna o buffer frontal no momento da apresentação.

</dd> <dt>

**Sinalizadores**
</dt> <dd>

(somente Windows 7)

O sinalizador de [ \_ \_ BackBuffer D3DPRESENTFLAG bloqueáveis](/windows/desktop/direct3d9/d3dpresentflag) não pode ser definido se **SwapEffect** está definido como o novo tipo de efeito de cadeia de permuta [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) .

</dd> </dl>

### <a name="design-guidelines-for-direct3d-9ex-flip-model-applications"></a>Diretrizes de design para aplicativos de modelo do Direct3D 9Ex flip

Use as diretrizes nas seções a seguir para projetar seus aplicativos de modelo do Direct3D 9Ex flip.

### <a name="use-flip-mode-present-in-a-separate-hwnd-from-blt-mode-present"></a>Usar o modo flip presente em um HWND separado do modo blt presente

Os aplicativos devem usar o modo de flip do Direct3D 9Ex presente em um HWND que não é também direcionado por outras APIs, incluindo o modo blt presente Direct3D 9Ex, outras versões do Direct3D ou GDI. O modo invertido presente pode ser usado para apresentar janelas filhas; ou seja, os aplicativos podem usar o flip Model quando não são misturados com o modelo BLT no mesmo HWND, conforme mostrado nas ilustrações a seguir.

![ilustração da janela pai do Direct3D e uma janela filho GDI, cada uma com seu próprio HWND](images/parent-d3d.png)

![ilustração da janela pai do GDI e uma janela filho do Direct3D, cada uma com seu próprio HWND](images/parent-gdi.png)

Como o modelo BLT mantém uma cópia adicional da superfície, o GDI e outros conteúdos do Direct3D podem ser adicionados ao mesmo HWND por meio de atualizações por etapas do Direct3D e GDI. Usando o modelo inverter, somente o conteúdo do Direct3D 9Ex nas cadeias de permuta do [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) que são transmitidas para o DWM será visível. Todas as outras atualizações de conteúdo do modelo BLT Direct3D ou GDI serão ignoradas, conforme mostrado nas ilustrações a seguir.

![ilustração de texto GDI que pode não ser exibido se o modelo de flip for usado e o conteúdo do Direct3D e GDI estiverem no mesmo HWND](images/d3d-gdi-same-hwnd.png)

![ilustração do conteúdo de Direct3D e GDI no qual o DWM está habilitado e o aplicativo está no modo de janela](images/d3d-gdinotext-same-hwnd.png)

Portanto, o modelo de inversão deve ser habilitado para superfícies de buffers de cadeia de permuta em que o modelo do Direct3D 9Ex flip sozinho é renderizado para o HWND inteiro.

### <a name="do-not-use-flip-model-with-gdis-scrollwindow-or-scrollwindowex"></a>Não use o modelo de flip com ScrollWindow ou ScrollWindowEx da GDI

Alguns aplicativos do Direct3D 9Ex usam as funções ScrollWindow ou ScrollWindowEx da GDI para atualizar o conteúdo da janela quando um evento Scroll do usuário é disparado. ScrollWindow e ScrollWindowEx executam BLTS do conteúdo da janela na tela, uma vez que uma janela é rolada. Essas funções também exigem atualizações de modelo BLT para conteúdo GDI e Direct3D 9Ex. Os aplicativos que usam qualquer função não exibirão, necessariamente, a rolagem do conteúdo da janela visível na tela quando o aplicativo estiver no modo de janela e o DWM estiver habilitado. Recomendamos que você não use as APIs ScrollWindow e ScrollWindowEx da GDI em seus aplicativos e, em vez disso, redesenhe seu conteúdo na tela em resposta à rolagem.

### <a name="use-one-d3dswapeffect_flipex-swap-chain-per-hwnd"></a>Usar uma \_ cadeia de permuta D3DSWAPEFFECT FLIPEX por HWND

Os aplicativos que usam o modelo de flip não devem usar várias cadeias de permuta de modelo invertidas direcionando o mesmo HWND.

### <a name="frame-synchronization-of-direct3d-9ex-flip-model-applications"></a>Sincronização de quadros de aplicativos de modelo do Direct3D 9Ex flip

As estatísticas atuais são informações de temporização de quadro que os aplicativos de mídia usam para sincronizar fluxos de áudio e vídeo e recuperar-se de problemas de reprodução de vídeo. Para habilitar a disponibilidade de estatísticas atuais, o aplicativo Direct3D 9Ex deve garantir que o parâmetro *BehaviorFlags* que o aplicativo passa para [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) contém o sinalizador de comportamento do dispositivo [D3DCREATE \_ habilitar \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate).

Para sua conveniência, a sintaxe de [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) é repetida aqui.

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

O modelo de flip do Direct3D 9Ex adiciona o sinalizador de apresentação do [D3DPRESENT \_ FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent) que impõe o comportamento da apresentação [ \_ \_ imediata do intervalo de D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) . O aplicativo Direct3D 9Ex especifica esses sinalizadores de apresentação no parâmetro *dwFlags* que o aplicativo passa para [**IDirect3DDevice9Ex::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex), conforme mostrado aqui.

``` syntax
HRESULT PresentEx(
  CONST RECT *pSourceRect,
  CONST RECT *pDestRect,
  HWND hDestWindowOverride,
  CONST RGNDATA *pDirtyRegion,
  DWORD dwFlags
);
```

ao modificar seu aplicativo Direct3D 9ex para o Windows 7, você deve considerar as seguintes informações sobre os sinalizadores de apresentação [D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) especificados:

<dl> <dt>

[D3DPRESENT \_ DONOTFLIP](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

Esse sinalizador está disponível somente no modo de tela inteira ou

(somente Windows 7)

Quando o aplicativo define o membro **SwapEffect** dos [**\_ parâmetros D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) para [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) em uma chamada para [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).

</dd> <dt>

[D3DPRESENT \_ FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

(somente Windows 7)

Esse sinalizador só poderá ser especificado se o aplicativo definir o membro **SwapEffect** dos [**\_ parâmetros D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) para [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) em uma chamada para [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex). O aplicativo pode usar esse sinalizador para atualizar imediatamente uma superfície com vários quadros posteriormente na fila do DWM presente, essencialmente ignorando os quadros intermediários.

Os aplicativos com janela habilitada para FlipEx podem usar esse sinalizador para atualizar imediatamente uma superfície com um quadro posterior na fila do DWM presente, ignorando os quadros intermediários. Isso é especialmente útil para aplicativos de mídia que desejam descartar os quadros que foram detectados como atrasados e apresentar quadros subsequentes no momento da composição. [**IDirect3DDevice9Ex::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) retornará um erro de parâmetro inválido se esse sinalizador estiver incorretamente especificado.

</dd> </dl>

Para obter informações de estatísticas presentes, o aplicativo obtém a estrutura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) chamando a API [**IDirect3DSwapChain9Ex:: GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) .

A estrutura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) contém estatísticas sobre [**IDirect3DDevice9Ex::P chamadas resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) . O dispositivo deve ser criado usando uma chamada [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) com o sinalizador [D3DCREATE \_ Enable \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) . Caso contrário, os dados retornados por [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) são indefinidos. Uma cadeia de permuta do Direct3D 9Ex habilitada para o flip-Model fornece informações de estatísticas presentes nos modos de tela inteira e em janelas.

Para cadeias de permuta do Direct3D 9Ex habilitadas para modelos BLT no modo de janela, todos os valores de estrutura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) serão zerados.

Para as estatísticas presentes do FlipEx, [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) retorna D3DERR \_ \_ as estatísticas presentes \_ nas seguintes situações:

-   Primeira chamada para [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) , que indica o início de uma sequência
-   Transição do DWM de ativado para desativado
-   Alteração de modo: qualquer modo de janela para ou de tela inteira ou tela inteira para transições de tela inteira

Para sua conveniência, a sintaxe de [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) é repetida aqui.

``` syntax
HRESULT GetPresentStatistics(
  D3DPRESENTSTATS * pPresentationStatistics
);
```

O método [**IDirect3DSwapChain9Ex:: GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) retorna o último PresentCount, ou seja, a ID atual da última chamada presente com êxito que foi feita por um dispositivo de vídeo associado à cadeia de permuta. Essa ID atual é o valor do membro **PresentCount** da estrutura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) . Para cadeias de permuta do Direct3D 9Ex habilitadas para modelos BLT, enquanto estiver no modo de janela, todos os valores de estrutura **D3DPRESENTSTATS** serão zerados.

Para sua conveniência, a sintaxe de [**IDirect3DSwapChain9Ex:: GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) é repetida aqui.

``` syntax
HRESULT GetLastPresentCount(
  UINT * pLastPresentCount
);
```

ao modificar seu aplicativo Direct3D 9ex para o Windows 7, você deve considerar as seguintes informações sobre a estrutura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) :

-   O valor de PresentCount que o [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) retorna não é atualizado quando uma chamada [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) com D3DPRESENT \_ DONOTWAIT especificado no parâmetro *dwFlags* retorna uma falha.
-   Quando [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) é chamado com D3DPRESENT \_ DONOTFLIP, uma chamada [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) é executada com sucesso, mas não retorna uma estrutura de [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) atualizada quando o aplicativo está no modo de janela.
-   **PresentRefreshCount** versus **SyncRefreshCount** em [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats):
    -   **PresentRefreshCount** é igual a **SyncRefreshCount** quando o aplicativo apresenta em cada vsync.
    -   **SyncRefreshCount** é obtido no intervalo de vsync quando o presente foi enviado, **SyncQPCTime** é aproximadamente o tempo associado ao intervalo de vsync.

``` syntax
typedef struct _D3DPRESENTSTATS {
    UINT PresentCount;
    UINT PresentRefreshCount;
    UINT SyncRefreshCount;
    LARGE_INTEGER SyncQPCTime;
    LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```

### <a name="frame-synchronization-for-windowed-applications-when-dwm-is-off"></a>Sincronização de quadros para aplicativos em janelas quando o DWM está desativado

Quando o DWM está desativado, os aplicativos em janelas são exibidos diretamente na tela do monitor sem passar por uma cadeia invertida. no Windows Vista, não há suporte para obter informações de estatísticas de quadro para aplicativos em janelas quando o DWM está desativado. para manter uma API em que os aplicativos não precisam ser compatíveis com o dwm, Windows 7 retornará informações de estatísticas de quadro para aplicativos em janelas quando o DWM estiver desativado. As estatísticas de quadro retornadas quando o DWM está desativado são apenas estimativas.

## <a name="walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample"></a>Walk-Through de um modelo do Direct3D 9Ex flip e apresentar estatísticas de exemplo

**Para aceitar o exemplo de apresentação do FlipEx para Direct3D 9Ex**

1.  verifique se o aplicativo de exemplo está em execução na versão do sistema operacional Windows 7 ou posterior.
2.  Defina o membro **SwapEffect** dos [**\_ parâmetros D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) como [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) em uma chamada para [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).


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



**Para também optar por FlipEx estatísticas presentes associadas para o exemplo do Direct3D 9Ex**

-   Defina [D3DCREATE \_ Enable \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) no parâmetro *BehaviorFlags* de [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).


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

1.  Enfileirar chamadas presentes: a contagem de BackBuffer recomendada é de 2 a 4.
2.  O exemplo do Direct3D 9Ex adiciona um BackBuffer implícito, o comprimento real da fila atual é a contagem de backbuffers + 1.
3.  Criar uma estrutura de fila presente auxiliar para armazenar todas as PresentCount (ID presente) do presente com êxito e associado, calculado/esperado PresentRefreshCount.
4.  Para detectar a ocorrência de falha:

    -   Chame [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)).
    -   Obtenha a ID atual (PresentCount) e a contagem de vsync em que o quadro é mostrado (PresentRefreshCount) do quadro cujas estatísticas atuais são obtidas.
    -   Recupere o PresentRefreshCount esperado (TargetRefresh no código de exemplo) associado à ID atual.
    -   Se o PresentRefreshCount real for posterior ao esperado, ocorrerá uma falha.

5.  Para se recuperar do problema:

    -   Calcule quantos quadros ignorar (a variável g \_ iImmediates no código de exemplo).
    -   Apresente os quadros ignorados com o intervalo D3DPRESENT \_ FORCEIMMEDIATE.

**Considerações sobre detecção e recuperação de problemas**

1.  A recuperação de problemas leva N ( \_ iQueueDelay variável no código de exemplo) número de chamadas presentes em que N (g \_ iQueueDelay) é igual a g \_ iImmediates mais o comprimento da fila atual, ou seja:

    -   Ignorando quadros com o intervalo atual D3DPRESENT \_ FORCEIMMEDIATE, além de
    -   Presentes na fila que precisam ser processados

2.  Defina um limite para o comprimento da falha ( \_ limite de recuperação \_ de falha em exemplo). Se o aplicativo de exemplo não puder se recuperar de uma falha que seja muito longa (ou seja, 1 segundo ou 60 vsyncs no monitor de 60 Hz), pule a animação intermitente e redefina a fila do auxiliar atual.


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

-   A ilustração a seguir mostra um aplicativo com a contagem de backbuffers de 4. O comprimento real da fila atual é, portanto, 5.

    ![ilustração de um applicas de quadros renderizados e da fila presente](images/sample-scenario.png)

    O quadro A é direcionado para entrar na tela na contagem de intervalos de sincronização de 1, mas foi detectado que foi mostrado na contagem de intervalos de sincronização de 4. Portanto, ocorreu um problema. Três quadros subsequentes são apresentados com o intervalo de D3DPRESENT \_ \_ FORCEIMMEDIATE. A falha deve levar um total de 8 chamadas presentes antes de ser recuperada-o próximo quadro será mostrado de acordo com sua contagem de intervalos de sincronização de destino.

### <a name="summary-of-programming-recommendations-for-frame-synchronization"></a>resumo de Recomendações de programação para sincronização de quadros

-   Crie uma lista de backup de todas as IDs de LastPresentCount (obtidas via [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)) e a PresentRefreshCount estimada associada de todos os presentes enviados.
    > [!Note]  
    > Quando o aplicativo chama [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) com D3DPRESENT \_ DONOTFLIP, a chamada [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) é realizada com sucesso, mas não retorna uma estrutura de [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) atualizada quando o aplicativo está no modo de janela.

     

-   Chame [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) para obter o PresentRefreshCount real associado a cada ID presente de quadros mostrados, para garantir que o aplicativo manipule as Devoluções de falha da chamada.
-   Se o PresentRefreshCount real for posterior ao PresentRefreshCount estimado, um problema será detectado. Compensar enviando quadros de retardo "presentes com D3DPRESENT \_ FORCEIMMEDIATE.
-   Quando um quadro é apresentado tardiamente na fila atual, todos os quadros em fila subsequentes serão apresentados em atraso. D3DPRESENT \_ FORCEIMMEDIATE corrigirá apenas o próximo quadro a ser apresentado após todos os quadros em fila. Portanto, a contagem de fila atual ou de BackBuffer não deve ser muito longa. portanto, há menos falhas de quadro para acompanhar. A contagem de BackBuffer ideal é de 2 a 4.
-   Se o PresentRefreshCount estimado for posterior ao PresentRefreshCount real, a limitação do DWM poderá ter ocorrido. As seguintes soluções são possíveis:

    -   reduzindo o tamanho da fila atual
    -   reduzir os requisitos de memória da GPU com outros meios além de reduzir o tamanho da fila atual (ou seja, diminuir a qualidade, remover efeitos e assim por diante)
    -   especificando [**DwmEnableMMCSS**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenablemmcss) para evitar a limitação do DWM em geral

-   Verifique a funcionalidade de exibição do aplicativo e o desempenho de estatísticas do quadro nos seguintes cenários:

    -   com o DWM ligado e desligado
    -   modo de tela inteira e modos de janela
    -   hardware de funcionalidade inferior

-   Quando os aplicativos não podem se recuperar de grandes números de quadros com falha com D3DPRESENT \_ FORCEIMMEDIATE presente, eles podem potencialmente executar as seguintes operações:

    -   Reduza o uso de CPU e GPU ao renderizar com menos carga de trabalho.
    -   no caso de decodificação de vídeo, decodificação mais rápido reduzindo a qualidade e, portanto, o uso de CPU e GPU.

## <a name="conclusion-about-direct3d-9ex-improvements"></a>Conclusão sobre os aprimoramentos do Direct3D 9Ex

no Windows 7, os aplicativos que exibem a taxa de quadros de vídeo ou medidor durante a apresentação podem optar pelo Flip Model. Os aprimoramentos de estatísticas atuais que estão associados ao flip Model Direct3D 9Ex podem beneficiar os aplicativos que sincronizam a apresentação por taxa de quadros, com comentários em tempo real para detecção e recuperação de problemas. Os desenvolvedores que adotam o modelo do Direct3D 9Ex flip devem ter como destino um HWND separado do conteúdo do GDI e da sincronização de taxa de quadros em conta. Consulte os detalhes neste tópico e a documentação do MSDN. Para obter mais documentação, consulte [DirectX Developer Center no MSDN](/previous-versions/windows/apps/hh452744(v=win.10)).

## <a name="call-to-action"></a>Plano de ação

incentivamos você a usar o modelo de inversão do Direct3D 9ex e suas estatísticas atuais no Windows 7 ao criar aplicativos que tentam sincronizar a taxa de quadros de apresentação ou se recuperar de falhas de exibição.

## <a name="related-topics"></a>Tópicos relacionados

[Central de desenvolvedores do DirectX no MSDN](/previous-versions/windows/apps/hh452744(v=win.10))
</dt> </dl>