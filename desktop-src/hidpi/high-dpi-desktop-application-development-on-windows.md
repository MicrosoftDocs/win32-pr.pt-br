---
title: Desenvolvimento de aplicativos de área de trabalho de DPI alto Windows
description: Esse conteúdo é destinado a desenvolvedores que estão procurando atualizar aplicativos da área de trabalho para lidar com o fator de escala de exibição dinâmico (também conhecido como
ms.assetid: 6C419EEF-D898-4B50-8D16-E65A594487AA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 01958791dccd7c836babedbe726233797eddb646
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471322"
---
# <a name="high-dpi-desktop-application-development-on-windows"></a>Desenvolvimento de aplicativos de área de trabalho de DPI alto Windows

Esse conteúdo é destinado a desenvolvedores que estão procurando atualizar aplicativos da área de trabalho para lidar com alterações de fator de escala de exibição (pontos por polegada ou DPI) dinamicamente, permitindo que seus aplicativos sejam nítidos em qualquer exibição em que eles são renderizados.

Para começar, se você estiver criando um novo aplicativo Windows do zero, é altamente recomendável criar um aplicativo [UWP (Plataforma universal](/windows/uwp/get-started/whats-a-uwp) Windows). Os aplicativos UWP são &mdash; dimensionados automaticamente e dinamicamente &mdash; para cada exibição em que estão sendo executados.

Aplicativos de área de trabalho que usam tecnologias de programação Windows mais antigas (programação win32 bruta, formulários Windows, WPF (estrutura de apresentação do Windows), etc.) não podem lidar automaticamente com o dimensionamento de DPI sem trabalho adicional do desenvolvedor. Sem esse trabalho, os aplicativos aparecerão desfocados ou dimensionado incorretamente em muitos cenários de uso comuns. Este documento fornece contexto e informações sobre o que está envolvido na atualização de um aplicativo da área de trabalho para renderizar corretamente.

## <a name="display-scale-factor--dpi"></a>Exibir DPI do fator de & escala

À medida que a tecnologia de exibição avança, os fabricantes de painéis de exibição empacotam um número cada vez maior de pixels em cada unidade de espaço físico em seus painéis. Isso resultou na DPI (pontos por polegada) dos painéis de exibição modernos sendo muito maiores do que eram historicamente. No passado, a maioria das exibições tinha 96 pixels por polegada linear de espaço físico (96 DPI); em 2017, as exibições com quase 300 DPI ou superior estão prontamente disponíveis.

A maioria das estruturas de interface do usuário da área de trabalho herdam suposições de que o DPI de exibição não mudará durante o tempo de vida do processo.  Essa suposição não se mantém mais verdadeira, com DPIs de exibição que normalmente mudam várias vezes ao longo do tempo de vida de um processo de aplicativo. Alguns cenários comuns em que as alterações de DPI/fator de escala de exibição são:

-   Configurações de vários monitores em que cada exibição tem um fator de escala diferente e o aplicativo é movido de uma exibição para outra (como uma exibição de 4K e 1080p)
-   Encaixe e desencaixamento de um laptop DPI alto com uma exibição externa de DPI baixa (ou vice-versa)
-   Conectar-se Área de Trabalho Remota de um laptop/tablet DPI alto para um dispositivo de DPI baixo (ou vice-versa)
-   Fazer uma alteração nas configurações de fator de escala de exibição enquanto os aplicativos estão em execução

Nesses cenários, os aplicativos UWP redesenham-se automaticamente para o novo DPI. Por padrão, e sem trabalho adicional do desenvolvedor, os aplicativos da área de trabalho não. Os aplicativos da área de trabalho que não fazem esse trabalho extra para responder às alterações de DPI podem parecer desfocados ou dimensionado incorretamente para o usuário.

## <a name="dpi-awareness-mode"></a>Modo de reconhecimento de DPI

Os aplicativos da área de trabalho Windows se eles são suportados com o dimensionamento de DPI. Por padrão, o sistema considera que o DPI de aplicativos da área de trabalho não reconhece e o bitmap alonga suas janelas. Ao definir um dos seguintes modos de reconhecimento de DPI disponíveis, os aplicativos podem Windows como desejam lidar com o dimensionamento de DPI:

### <a name="dpi-unaware"></a>DPI sem conhecimento

Os aplicativos sem conhecimento de DPI são renderizar com um valor de DPI fixo de 96 (100%). Sempre que esses aplicativos são executados em uma tela com uma escala de exibição maior que 96 DPI, Windows ampliará o bitmap do aplicativo para o tamanho físico esperado. Isso resulta em o aplicativo parecer desfocado.

### <a name="system-dpi-awareness"></a>Reconhecimento de DPI do sistema

Os aplicativos da área de trabalho com conhecimento de DPI do sistema normalmente recebem o DPI do monitor conectado primário a partir do momento da conexão do usuário. Durante a inicialização, eles estabelecem a interface do usuário adequadamente (controles de tamanho, escolha de tamanhos de fonte, carregamento de ativos etc.) usando esse valor de DPI do sistema. Dessa forma, os aplicativos com base em DPI do sistema não são dimensionados por DPI (bitmap estendido) por Windows em exibe a renderização nesse único DPI. Quando o aplicativo for movido para uma exibição com um fator de escala diferente ou se o fator de escala de exibição mudar, Windows bitmap dimensionará as janelas do aplicativo, fazendo com que elas pareçam desfocados. Efetivamente, os aplicativos de área de trabalho com suporte a DPI do sistema renderizarão apenas de maneira nítido em um único fator de escala de exibição, tornando-se desfocado sempre que o DPI for mudar.

### <a name="per-monitor-and-per-monitor-v2-dpi-awareness"></a>Per-Monitor e Per-Monitor (V2) Reconhecimento de DPI

É recomendável que os aplicativos da área de trabalho sejam atualizados para usar o modo de reconhecimento de DPI por monitor, permitindo que eles sejam renderizar imediatamente corretamente sempre que o DPI mudar. Quando um aplicativo informa Windows que deseja executar nesse modo, o Windows não ampliará o bitmap do aplicativo quando o DPI mudar, enviando [WM \_ DPICHANGED](wm-dpichanged.md) para a janela do aplicativo. Em seguida, é responsabilidade total do aplicativo lidar com o reizing a si mesmo para o novo DPI. A maioria das estruturas de interface do usuário usadas por aplicativos da área de trabalho (Windows controles comuns (comctl32), Windows Forms, Windows Presentation Framework etc.) não suportam o dimensionamento automático de DPI, exigindo que os desenvolvedores reescalem e reposicionarem o conteúdo das próprias janelas.

Há duas versões do Per-Monitor que um aplicativo pode se registrar como: versão 1 e versão 2 (PMv2). Registrar um processo como em execução no modo de reconhecimento PMv2 resulta em:

1.  O aplicativo que está sendo notificado quando o DPI muda (os HWNDs de nível superior e filho)
2.  O aplicativo vendo os pixels brutos de cada exibição
3.  O aplicativo nunca está sendo dimensionado por bitmap Windows
4.  Área não cliente automática (legenda da janela, barras de rolagem etc.) Dimensionamento de DPI por Windows
5.  Caixas de diálogo Win32 (de [CreateDialog](/windows/desktop/api/winuser/nf-winuser-createdialogw)) automaticamente dimensionadas por Windows
6.  Ativos de bitmap desenhados por tema em controles comuns (caixas de seleção, planos de fundo de botão etc.) sendo renderizados automaticamente no fator de escala de DPI apropriado

Ao executar no modo Per-Monitor reconhecimento v2, os aplicativos são notificados quando seu DPI foi alterado. Se um aplicativo não se reorganizar para o novo DPI, a interface do usuário do aplicativo será muito pequena ou muito grande (dependendo da diferença nos valores de DPI anteriores e novos).

> [!Note]  
> Per-Monitor reconhecimento V1 (PMv1) é muito limitado. É recomendável que os aplicativos usem PMv2.

A tabela a seguir mostra como os aplicativos serão renderados em diferentes cenários:


| Modo de reconhecimento de DPI | Windows Versão introduzida | Exibição do DPI do aplicativo | Comportamento na alteração de DPI | 
|--------------------|----------------------------|---------------------------|------------------------|
| Inconscientes | N/D | Todas as exibições são de 96 DPI | Alongamento de bitmap (desfocado) | 
| Sistema | Vista | Todas as exibições têm o mesmo DPI (o DPI da exibição primária no momento em que a sessão de usuário atual foi iniciada) | Alongamento de bitmap (desfocado) | 
| Per-Monitor | 8.1 | O DPI da exibição em que a janela do aplicativo está localizada principalmente | <ul><li>O HWND de nível superior é notificado sobre a alteração de DPI</li><li>Nenhum dimensionamento de DPI de nenhum elemento de interface do usuário.</li></ul><br /> | 
| Per-Monitor V2 | Atualização do Windows 10 para Criadores (1703) | O DPI da exibição em que a janela do aplicativo está localizada principalmente | <ul><li>HWNDs de nível <span class="underline">superior</span> e filho são notificados sobre a alteração de DPI</li></ul><br /><span class="underline">Dimensionamento automático de DPI de:</span><ul><li>Área não cliente</li><li>Bitmaps desenhados por tema em controles comuns (comctl32 V6)</li><li>Caixas de diálogo (<a href="/windows/desktop/api/winuser/nf-winuser-createdialogw">CreateDialog</a>)</li></ul><br /> | 


### <a name="per-monitor-v1-dpi-awareness"></a>Reconhecimento de DPI por monitor (V1)

Per-Monitor modo de reconhecimento de DPI V1 (PMv1) foi introduzido com Windows 8.1. Esse modo de reconhecimento de DPI é muito limitado e oferece apenas a funcionalidade listada abaixo. É recomendável que os aplicativos da área de trabalho Per-Monitor modo de reconhecimento v2, com suporte Windows 10 1703 ou superior.

O suporte inicial para reconhecimento por monitor só oferece aplicativos do seguinte:

1.  HWNDs de nível superior são notificados sobre uma alteração de DPI e fornecidos um novo tamanho sugerido
2.  Windows bitmap ampliará a interface do usuário do aplicativo
3.  O aplicativo vê todas as exibições em pixels físicos (consulte virtualização)

No Windows 10 1607 ou superior, os aplicativos PMv1 também podem chamar [EnableNonClientDpiScaling](/windows/desktop/api/winuser/nf-winuser-enablenonclientdpiscaling) durante o WM NCCREATE para solicitar que Windows dimensione corretamente a área não cliente da \_ janela.

## <a name="per-monitor-dpi-scaling-support-by-ui-framework--technology"></a>Suporte para dimensionamento de DPI por monitor por estrutura/tecnologia da interface do usuário

A tabela a seguir mostra o nível de suporte de reconhecimento de DPI por monitor oferecido por várias estruturas Windows interface do usuário do Windows 10 1703:


| Estrutura/tecnologia | Suporte | Versão do SO | Dimensionamento de DPI manipulado por | Leitura Adicional | 
|------------------------|---------|------------|------------------------|-----------------|
| Plataforma Universal do Windows (UWP) | Completo | 1607 | Estrutura da interface do usuário | <a href="/windows/uwp/get-started/whats-a-uwp">UWP (Plataforma Universal do Windows)</a> | 
| Controles Win32/comuns V6 brutos (comctl32.dll) | <ul><li>Mensagens de notificação de alteração de DPI enviadas a todos os HWNDs</li><li>Os ativos de tema desenhado são renderizados corretamente em controles comuns</li><li>Dimensionamento automático de DPI para caixas de diálogo</li></ul> | 1703 | Aplicativo | <a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow">GitHub Nova</a> | 
| Windows Forms | Dimensionamento automático limitado por monitor de DPI para alguns controles | 1703 | Estrutura de interface do usuário | <a href="/dotnet/framework/winforms/high-dpi-support-in-windows-forms">suporte a alto DPI no Windows Forms</a> | 
| Windows Estrutura de apresentação (WPF) | Os aplicativos nativos do WPF terão a escala de DPI do WPF hospedado em outras estruturas e outras estruturas hospedadas no WPF não são dimensionadas automaticamente | 1607 | Estrutura de interface do usuário | <a href="https://github.com/Microsoft/WPF-Samples/tree/master/PerMonitorDPI">GitHub Nova</a> | 
| GDI | Nenhum | N/D | Aplicativo | Consulte <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">dimensionamento de dpi alta do GDI</a> | 
| GDI+ | Nenhum | N/D | Aplicativo | Consulte <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">dimensionamento de dpi alta do GDI</a> | 
| MFC | Nenhum | N/D | Aplicativo | N/D | 




 

## <a name="updating-existing-applications"></a>Atualizando aplicativos existentes

Para atualizar um aplicativo de área de trabalho existente para manipular o dimensionamento de DPI corretamente, ele precisa ser atualizado de modo que, no mínimo, as partes importantes de sua interface do usuário sejam atualizadas para responder a alterações de DPI.

A maioria dos aplicativos de desktop é executada no modo de reconhecimento de DPI do sistema. aplicativos com reconhecimento de dpi de sistema normalmente são dimensionados para o DPI da exibição primária (a exibição na qual a bandeja do sistema estava localizada no momento em que a sessão de Windows foi iniciada). quando o DPI for alterado, Windows bitmap ampliará a interface do usuário desses aplicativos, o que geralmente resulta na desfoque. Ao atualizar um aplicativo com reconhecimento de DPI do sistema para se tornar ciente por monitor-DPI, o código que manipula o layout da interface do usuário precisa ser atualizado, de modo que ele seja executado não apenas durante a inicialização do aplicativo, mas também sempre que uma notificação de alteração de DPI ([WM \_ DPICHANGED](wm-dpichanged.md) no caso do Win32) for recebida. Isso geralmente envolve a revisita de qualquer suposição no código que a interface do usuário só precisa ser dimensionada uma vez.

Além disso, no caso da programação Win32, muitas APIs do Win32 não têm nenhum contexto de vídeo ou DPI para que eles retornem apenas valores relativos ao DPI do sistema. Pode ser útil fazer o grep por meio de seu código para procurar algumas dessas APIs e substituí-las por variantes com reconhecimento de DPI. Algumas das APIs comuns que têm variantes com reconhecimento de DPI são:



| Versão de DPI única   | Versão do Per-Monitor        |
|----------------------|----------------------------|
| GetSystemMetrics     | GetSystemMetricsForDpi     |
| AdjustWindowRectEx   | AdjustWindowRectExForDpi   |
| SystemParametersInfo | SystemParametersInfoForDpi |
| GetDpiForMonitor     | GetDpiForWindow            |



 

Também é uma boa ideia Pesquisar os tamanhos embutidos em código na sua codebase que assumem um DPI constante, substituindo-os pelo código que conta corretamente no dimensionamento de DPI. Veja abaixo um exemplo que incorpora todas essas sugestões:

### <a name="example"></a>Exemplo:

O exemplo a seguir mostra um caso do Win32 simplificado de criar um HWND filho. A chamada para CreateWindow pressupõe que o aplicativo está sendo executado às 96 DPI, e nem o tamanho do botão nem a posição estarão corretos em DPIs maiores:


```
case WM_CREATE: 
{ 
    // Add a button 
    HWND hWndChild = CreateWindow(L"BUTTON", L"Click Me",  
        WS_CHILD|WS_VISIBLE|BS_PUSHBUTTON,  
        50,  
        50,  
        100,  
        50,  
        hWnd, (HMENU)NULL, NULL, NULL); 
} 
```



O código atualizado abaixo mostra:

1.  O DPI de código de criação de janela dimensionando a posição e o tamanho do HWND filho para o DPI de sua janela pai
2.  Respondendo à alteração de DPI reposicionando e redimensionando o HWND filho
3.  Tamanhos embutidos em código removidos e substituídos por código que responde a alterações de DPI


```
#define INITIALX_96DPI 50 
#define INITIALY_96DPI 50 
#define INITIALWIDTH_96DPI 100 
#define INITIALHEIGHT_96DPI 50 
 
 
// DPI scale the position and size of the button control 
void UpdateButtonLayoutForDpi(HWND hWnd) 
{ 
    int iDpi = GetDpiForWindow(hWnd); 
    int dpiScaledX = MulDiv(INITIALX_96DPI, iDpi, 96); 
    int dpiScaledY = MulDiv(INITIALY_96DPI, iDpi, 96); 
    int dpiScaledWidth = MulDiv(INITIALWIDTH_96DPI, iDpi, 96); 
    int dpiScaledHeight = MulDiv(INITIALHEIGHT_96DPI, iDpi, 96); 
    SetWindowPos(hWnd, hWnd, dpiScaledX, dpiScaledY, dpiScaledWidth, dpiScaledHeight, SWP_NOZORDER | SWP_NOACTIVATE); 
} 
 
... 
 
case WM_CREATE: 
{ 
    // Add a button 
    HWND hWndChild = CreateWindow(L"BUTTON", L"Click Me",  
        WS_CHILD|WS_VISIBLE|BS_PUSHBUTTON, 
        0, 
        0, 
        0, 
        0, 
        hWnd, (HMENU)NULL, NULL, NULL); 
    if (hWndChild != NULL) 
    { 
        UpdateButtonLayoutForDpi(hWndChild); 
    } 
} 
break; 
 
case WM_DPICHANGED: 
{ 
    // Find the button and resize it 
    HWND hWndButton = FindWindowEx(hWnd, NULL, NULL, NULL); 
    if (hWndButton != NULL) 
    { 
        UpdateButtonLayoutForDpi(hWndButton); 
    } 
} 
break; 
```



Ao atualizar um aplicativo com reconhecimento de DPI do sistema, algumas etapas comuns a serem seguidas são:

1.  Marque o processo como reconhecimento de DPI por monitor (v2) usando um manifesto de aplicativo (ou outro método, dependendo das estruturas de interface do usuário usadas).
2.  tornar a lógica de layout da interface do usuário reutilizável e movê-la do código de inicialização do aplicativo de modo que ela possa ser reutilizada quando ocorrer uma alteração de DPI (WM \_ DPICHANGED no caso de programação Windows (Win32)).
3.  Invalidar qualquer código que assuma que os dados sensíveis a DPI (DPI/fontes/tamanhos/etc.) nunca precisem ser atualizados. É uma prática muito comum armazenar em cache os tamanhos de fonte e valores de DPI na inicialização do processo. Ao atualizar um aplicativo para se tornar um reconhecimento de DPI por monitor, os dados sensíveis a DPI devem ser reavaliados sempre que um novo DPI for encontrado.
4.  Quando ocorre uma alteração de DPI, recarregar (ou rerasterizar) todos os ativos de bitmap para o novo DPI ou, opcionalmente, ampliar os ativos carregados no momento para o tamanho correto.
5.  Grep para APIs que não são Per-Monitor DPI reconhecem e as substituem por Per-Monitor APIs com reconhecimento de DPI (quando aplicável). Exemplo: substitua GetSystemMetrics por GetSystemMetricsForDpi.
6.  Teste seu aplicativo em um sistema de várias exibições/vários DPI.
7.  Para qualquer janela de nível superior em seu aplicativo que você não pode atualizar para a escala de DPI correta, use o dimensionamento de DPI de modo misto (descrito abaixo) para permitir o alargamento de bitmap dessas janelas de nível superior pelo sistema.

## <a name="mixed-mode-dpi-scaling-sub-process-dpi-scaling"></a>Escala de DPI de Mixed-Mode (escala de PPP de subprocesso)

Ao atualizar um aplicativo para dar suporte ao reconhecimento de DPI por monitor, às vezes pode se tornar impraticável ou impossível atualizar cada janela no aplicativo em um só lugar. Isso pode ser simplesmente devido ao tempo e esforço necessários para atualizar e testar toda a interface do usuário, ou porque você não possui todo o código da interface do usuário que precisa ser executado (se seu aplicativo talvez carregue a interface do usuário de terceiros). nessas situações, a Windows oferece uma maneira de facilitar o mundo da conscientização por monitor, permitindo que você execute algumas janelas de aplicativo (somente de nível superior) em seu modo original de reconhecimento de DPI enquanto você se concentra no seu tempo e na atualização de energia das partes mais importantes da sua interface do usuário.

Veja abaixo uma ilustração de como isso poderia ser: você atualiza a interface do usuário do aplicativo principal ("janela principal" na ilustração) para executar com reconhecimento de DPI por monitor enquanto executa outras janelas em seu modo existente ("janela secundária").

![diferenças no dimensionamento de DPI entre modos de reconhecimento](images/hub-page-illustrations.png)

antes da atualização de aniversário de Windows 10 (1607), o modo de reconhecimento de DPI de um processo era uma propriedade de todo o processo. a partir do Windows 10 atualização de aniversário, essa propriedade agora pode ser definida por janela **de nível superior** . (O Windows **filho** deve continuar a corresponder ao tamanho de dimensionamento de seu pai.) Uma janela de nível superior é definida como uma janela sem nenhum pai. Normalmente, essa é uma janela "regular" com os botões minimizar, maximizar e fechar. o cenário para o qual o reconhecimento de DPI de subprocesso é destinado é ter a interface do usuário secundária dimensionada por Windows (bitmap ampliado) enquanto você concentra seu tempo e recursos na atualização da interface do usuário principal.

Para habilitar o reconhecimento de DPI de subprocesso, chame [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) antes e depois de qualquer chamada de criação de janela. A janela criada será associada ao reconhecimento de DPI definido por meio de SetThreadDpiAwarenessContext. Use a segunda chamada para restaurar o reconhecimento de DPI do thread s atual.

embora o uso do dimensionamento de dpi de subprocesso permita que você confie no Windows fazer parte do dimensionamento de dpi para seu aplicativo, ele pode aumentar a complexidade do seu aplicativo. É importante entender as desvantagens dessa abordagem e da natureza das complexidades que ela apresenta. Para obter mais informações sobre o reconhecimento de DPI de subprocesso, consulte [dimensionamento de dpi de modo misto e APIs com reconhecimento de DPI.](high-dpi-improvements-for-desktop-applications.md)

## <a name="testing-your-changes"></a>Testando suas alterações

Depois de atualizar seu aplicativo para se tornar um reconhecimento de DPI por monitor, é importante validar seu aplicativo corretamente responde às alterações de DPI em um ambiente de DPI misto. Algumas especificidades para teste incluem:

1.  Mover janelas de aplicativos para frente e para trás entre telas de valores de DPI diferentes
2.  Iniciando seu aplicativo em exibições de valores de DPI diferentes
3.  Alterando o fator de escala para o monitor enquanto o aplicativo está em execução
4.  alterar a exibição que você usa como a exibição primária, sair _de Windows_ e, em seguida, testar novamente seu aplicativo após entrar novamente. Isso é particularmente útil na localização de código que usa dimensões/tamanhos embutidos em código.

## <a name="common-pitfalls-win32"></a>Armadilhas comuns (Win32)

**Não está usando o retângulo sugerido que é fornecido no WM \_ DPICHANGED**

Quando Windows a janela do aplicativo uma mensagem [**WM \_ DPICHANGED,**](wm-dpichanged.md) essa mensagem inclui um retângulo sugerido que você deve usar para reessular a janela. É essencial que seu aplicativo use esse retângulo para reessular a si mesmo, pois isso vai:

1.  Certifique-se de que o cursor do mouse permaneça na mesma posição relativa na Janela ao arrastar entre as exibições
2.  Impedir que a janela do aplicativo entre em um ciclo recursivo dpi-change em que uma alteração de DPI dispara uma alteração de DPI subsequente, o que dispara outra alteração de DPI.

Se você tiver requisitos específicos do aplicativo que o impeçam de usar o retângulo sugerido que Windows fornece na mensagem WM \_ DPICHANGED, consulte [**WM \_ GETDPISCALEDSIZE**](wm-getdpiscaledsize.md). Essa mensagem pode ser usada para Windows um tamanho desejado que você gostaria de usar depois que a alteração de DPI tiver ocorrido, evitando ainda os problemas descritos acima.

**Falta de documentação sobre virtualização**

Quando um HWND ou um processo é executado como DPI sem conhecimento ou com conhecimento de DPI do sistema, ele pode ser estendido por bitmap por Windows. Quando isso acontece, Windows dimensiona e converte informações confidenciais de DPI de algumas APIs para o espaço de coordenadas do thread de chamada. Por exemplo, se um thread sem conhecimento de DPI consultar o tamanho da tela durante a execução em uma exibição de DPI alto, o Windows virtualizará a resposta dada ao aplicativo como se a tela estivesse em 96 unidades de DPI. Como alternativa, quando um thread com conhecimento de DPI do sistema estiver interagindo com uma exibição em um DPI diferente do que estava em uso quando a sessão do usuário atual foi iniciada, o Windows dimensionará algumas chamadas à API para o espaço de coordenadas que o HWND usaria se estivesse em execução em seu fator de escala de DPI original.

Quando você atualiza seu aplicativo da área de trabalho para dimensionamento de DPI corretamente, pode ser difícil saber quais chamadas à API podem retornar valores virtualizados com base no contexto do thread; Atualmente, essas informações não estão documentadas o suficiente pela Microsoft. Esteja ciente de que, se você chamar qualquer API do sistema de um contexto de thread com conhecimento de DPI ou com conhecimento de DPI do sistema, o valor de retorno poderá ser virtualizado. Dessa forma, certifique-se de que o thread está em execução no contexto de DPI esperado ao interagir com a tela ou janelas individuais. Ao alterar temporariamente o contexto de DPI de um thread usando [SetThreadDpiAwarenessContext](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext), restaure o contexto antigo quando terminar para evitar causar comportamento incorreto em outro lugar no aplicativo.

**Muitas Windows APIs não têm um contexto de DPI**

Muitas APIs Windows herdados não incluem um contexto de DPI ou HWND como parte de sua interface. Como resultado, os desenvolvedores geralmente têm que fazer trabalho adicional para lidar com o dimensionamento de qualquer informação sensível ao DPI, como tamanhos, pontos ou ícones. Por exemplo, os desenvolvedores que usam [LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadiconw) devem usar ícones carregados de stretch bitmap ou usar APIs alternativas para carregar ícones de tamanho correto para o DPI apropriado, como [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagew).

**Redefinição forçada do reconhecimento de DPI em todo o processo**

Em geral, o modo de reconhecimento de DPI do processo não pode ser alterado após a inicialização do processo. Windows pode, no entanto, alterar à força o modo de reconhecimento de DPI do seu processo se você tentar quebrar o requisito de que todos os HWNDs em uma árvore de janelas tenham o mesmo modo de reconhecimento de DPI. Em todas as versões do Windows, a partir do Windows 10 1703, não é possível ter HWNDs diferentes em uma árvore HWND em diferentes modos de reconhecimento de DPI. Se você tentar criar uma relação pai-filho que interrompe essa regra, o reconhecimento de DPI de todo o processo poderá ser redefinido. Isso pode ser disparado por:

1.  Uma chamada CreateWindow em que a janela pai passada é de um modo de reconhecimento de DPI diferente do thread de chamada.
2.  Uma chamada SetParent em que as duas janelas estão associadas a diferentes modos de reconhecimento de DPI.

A tabela a seguir mostra o que acontece se você tentar violar essa regra:



| Operação                 | Windows 8.1                                  | Windows 10 (1607 e versões anteriores)                | Windows 10 (1703 e posterior)                  |
|---------------------------|----------------------------------------------|----------------------------------------------|----------------------------------------------|
| CreateWindow (In-Proc)    | N/D                                          | **Heranças filho** (modo misto)              | **Heranças filho** (modo misto)              |
| CreateWindow (Cross-Proc) | **Redefinição** forçada (do processo do chamador)       | **Heranças filho** (modo misto)              | **Redefinição** forçada (do processo do chamador)       |
| SetParent (In-Proc)       | N/D                                          | **Redefinição forçada** (do processo atual)        | **Falha** (ERRO \_ ESTADO \_ INVÁLIDO)             |
| SetParent (Cross-Proc)    | **Redefinição forçada** (do processo da janela filho) | **Redefinição forçada** (do processo da janela filho) | **Redefinição forçada** (do processo da janela filho) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de API de DPI alta](high-dpi-reference.md)
</dt> <dt>

[Dimensionamento de DPI de modo misto e APIs com conhecimento de DPI.](high-dpi-improvements-for-desktop-applications.md)
</dt> </dl>

