---
title: Desenvolvimento de aplicativos de desktop de alto DPI no Windows
description: Esse conteúdo é destinado a desenvolvedores que procuram atualizar aplicativos de área de trabalho para lidar com o fator de escala de exibição dinâmica (também conhecido como
ms.assetid: 6C419EEF-D898-4B50-8D16-E65A594487AA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7af4a7a1d65077838dfa65f7cf89dee475a0b4dc
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104084966"
---
# <a name="high-dpi-desktop-application-development-on-windows"></a>Desenvolvimento de aplicativos de desktop de alto DPI no Windows

Esse conteúdo é destinado a desenvolvedores que procuram atualizar aplicativos de área de trabalho para lidar dinamicamente com as alterações de fator de escala de exibição (pontos por polegada ou DPI), permitindo que seus aplicativos sejam nítidos em qualquer exibição na qual são renderizados.

Para começar, se você estiver criando um novo aplicativo do Windows do zero, é altamente recomendável que você crie um aplicativo [plataforma universal do Windows (UWP)](/windows/uwp/get-started/whats-a-uwp) . Os aplicativos UWP &mdash; &mdash; são dimensionados de forma automática e dinâmica para cada exibição em que estão sendo executados.

Os aplicativos de desktop que usam tecnologias mais antigas de programação do Windows (programação pura do Win32, Windows Forms, Windows Presentation Framework (WPF) etc.) não conseguem lidar automaticamente com o dimensionamento de DPI sem o trabalho adicional do desenvolvedor. Sem tal trabalho, os aplicativos aparecerão borrados ou incorretamente dimensionados em muitos cenários de uso comuns. Este documento fornece contexto e informações sobre o que está envolvido na atualização de um aplicativo de área de trabalho para renderização correta.

## <a name="display-scale-factor--dpi"></a>Exibir fator de escala & DPI

À medida que a tecnologia de vídeo progrediu, os fabricantes de painel de exibição lançaram um número cada vez maior de pixels em cada unidade de espaço físico em seus painéis. Isso resultou em pontos por polegada (DPI) dos painéis de exibição modernos sendo muito maiores do que historicamente. No passado, a maioria dos monitores tinha 96 pixels por polegada linear de espaço físico (96 DPI); no 2017, os monitores com quase 300 DPI ou mais estão prontamente disponíveis.

A maioria das estruturas de interface do usuário da área de trabalho herdada tem suposições internas de que o DPI de vídeo não será alterado durante o tempo de vida do processo.  Essa suposição não é mais verdadeira, com o DPIs de exibição geralmente mudando várias vezes durante o tempo de vida de um processo do aplicativo. Alguns cenários comuns em que as alterações de fator de escala de exibição/DPI são:

-   Configurações de monitores múltiplos em que cada exibição tem um fator de escala diferente e o aplicativo é movido de uma exibição para outra (como uma exibição de 4K e 1080p)
-   Encaixe e desencaixe de um laptop de DPI alto com uma exibição externa de DPI baixo (ou vice-versa)
-   Conectar-se via Área de Trabalho Remota de um laptop/Tablet de DPI alto a um dispositivo de baixo DPI (ou vice-versa)
-   Alterando as configurações do fator de escala de exibição enquanto os aplicativos estão em execução

Nesses cenários, os aplicativos UWP redesenham-se para o novo DPI automaticamente. Por padrão, e sem trabalho adicional para desenvolvedores, os aplicativos de área de trabalho não. Os aplicativos de área de trabalho que não fazem esse trabalho extra para responder às alterações de DPI podem aparecer borrados ou ter um tamanho incorreto para o usuário.

## <a name="dpi-awareness-mode"></a>Modo de reconhecimento de DPI

Os aplicativos da área de trabalho devem informar ao Windows se eles dão suporte ao dimensionamento de DPI Por padrão, o sistema considera o DPI dos aplicativos de desktop sem reconhecimento e bitmap – amplia suas janelas. Ao definir um dos seguintes modos de reconhecimento de DPI disponíveis, os aplicativos podem dizer explicitamente ao Windows como eles desejam lidar com o dimensionamento de DPI:

### <a name="dpi-unaware"></a>Sem reconhecimento de DPI

Aplicativos sem reconhecimento de DPI renderizam em um valor de DPI fixo de 96 (100%). Sempre que esses aplicativos são executados em uma tela com uma escala de exibição maior que 96 DPI, o Windows vai alongar o bitmap do aplicativo para o tamanho físico esperado. Isso resulta na exibição desfoque do aplicativo.

### <a name="system-dpi-awareness"></a>Reconhecimento de DPI do sistema

Os aplicativos de desktop com reconhecimento de DPI do sistema normalmente recebem o DPI do monitor conectado primário a partir do momento da entrada do usuário. Durante a inicialização, eles formam sua interface do usuário adequadamente (controles de dimensionamento, escolhendo tamanhos de fonte, carregando ativos, etc.) usando esse valor de DPI do sistema. Assim, os aplicativos com reconhecimento de DPI do sistema não são escalares de DPI (bitmap ampliado) pelo Windows no exibe a renderização naquele único DPI. Quando o aplicativo é movido para uma exibição com um fator de escala diferente, ou se o fator de escala de exibição for alterado, o Windows fará o bitmap dimensionar as janelas do aplicativo, tornando-as aparentemente borradas. Efetivamente, os aplicativos de área de trabalho com reconhecimento de DPI do sistema são processados de forma nítida em um único fator de escala de exibição, ficando desfocado sempre que o DPI é alterado.

### <a name="per-monitor-and-per-monitor-v2-dpi-awareness"></a>Reconhecimento de DPI de Per-Monitor e Per-Monitor (v2)

É recomendável que os aplicativos da área de trabalho sejam atualizados para usar o modo de reconhecimento de DPI por monitor, permitindo que eles sejam renderizados imediatamente sempre que o DPI for alterado. Quando um aplicativo se reporta ao Windows que deseja executar nesse modo, o Windows não bitmap amplia o aplicativo quando o DPI muda, em vez disso, envia o [WM \_ DPICHANGED](wm-dpichanged.md) para a janela do aplicativo. Em seguida, é responsabilidade total do aplicativo lidar com o redimensionamento para o novo DPI. A maioria das estruturas de interface do usuário usadas por aplicativos de desktop (comctl32), Windows Forms, Windows Presentation Framework, etc.) não dão suporte ao dimensionamento automático de DPI, exigindo que os desenvolvedores redimensionem e reposicionem o conteúdo de suas próprias janelas.

Há duas versões do Per-Monitor reconhecimento de que um aplicativo pode se registrar como: versão 1 e versão 2 (PMv2). O registro de um processo como executado no modo de reconhecimento de PMv2 resulta em:

1.  O aplicativo que está sendo notificado quando o DPI é alterado (ambos os HWNDs de nível superior e filho)
2.  O aplicativo que vê os pixels brutos de cada exibição
3.  O aplicativo nunca é um bitmap dimensionado pelo Windows
4.  Área não cliente automática (legenda da janela, barras de rolagem, etc.) Escala de DPI pelo Windows
5.  Caixas de diálogo do Win32 (de [CreateDialog](/windows/desktop/api/winuser/nf-winuser-createdialogw)) automaticamente dpi dimensionada pelo Windows
6.  Os ativos de bitmap desenhado por tema em controles comuns (caixas de seleção, planos de fundo de botão, etc.) são automaticamente renderizados no fator de escala de DPI apropriado

Ao executar no modo de reconhecimento de Per-Monitor v2, os aplicativos são notificados quando seu DPI é alterado. Se um aplicativo não se redimensionar para o novo DPI, a interface do usuário do aplicativo aparecerá muito pequena ou muito grande (dependendo da diferença nos valores de DPI anterior e novo).

> [!Note]  
> A conscientização do Per-Monitor V1 (PMv1) é muito limitada. É recomendável que os aplicativos usem o PMv2.

A tabela a seguir mostra como os aplicativos serão renderizados em diferentes cenários:

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Modo de reconhecimento de DPI</th>
<th>Versão do Windows introduzida</th>
<th>Modo de exibição do aplicativo de DPI</th>
<th>Comportamento na alteração de DPI</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Conhecida</td>
<td>N/D</td>
<td>Todas as telas são 96 DPI</td>
<td>Alongamento de bitmap (borrado)</td>
</tr>
<tr class="even">
<td>Sistema</td>
<td>Vista</td>
<td>Todos os monitores têm o mesmo DPI (o DPI da exibição primária no momento em que a sessão do usuário atual foi iniciada)</td>
<td>Alongamento de bitmap (borrado)</td>
</tr>
<tr class="odd">
<td>Per-Monitor</td>
<td>8.1</td>
<td>O DPI da exibição na qual a janela do aplicativo está localizada principalmente</td>
<td><ul>
<li>O HWND de nível superior é notificado de alteração de DPI</li>
<li>Sem ajuste de DPI de nenhum elemento de interface do usuário.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Per-Monitor V2</td>
<td>Atualização do Windows 10 para criadores (1703)</td>
<td>O DPI da exibição na qual a janela do aplicativo está localizada principalmente</td>
<td><ul>
<li>Os HWNDs de nível superior <span class="underline">e</span> filho são notificados da alteração de DPI</li>
</ul>
<br/> <span class="underline">Ajuste automático de DPI de:</span>
<ul>
<li>Área não cliente</li>
<li>Bitmaps desenhados por tema em controles comuns (comctl32 V6)</li>
<li>Caixas de diálogo (<a href="/windows/desktop/api/winuser/nf-winuser-createdialogw">CreateDialog</a>)</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>

### <a name="per-monitor-v1-dpi-awareness"></a>Reconhecimento de DPI por monitor (v1)

O modo de reconhecimento de Per-Monitor v1 DPI (PMv1) foi introduzido com Windows 8.1. Esse modo de reconhecimento de DPI é muito limitado e oferece apenas a funcionalidade listada abaixo. É recomendável que os aplicativos de desktop usem o modo de reconhecimento v2 Per-Monitor, com suporte no Windows 10 1703 ou superior.

O suporte inicial para reconhecimento por monitor oferecia apenas os aplicativos a seguir:

1.  Os HWNDs de nível superior são notificados de uma alteração de DPI e fornecem um novo tamanho sugerido
2.  O Windows não ampliará o bitmap da interface do usuário do aplicativo
3.  O aplicativo vê todas as telas em pixels físicos (consulte virtualização)

No Windows 10 1607 ou superior, os aplicativos PMv1 também podem chamar [EnableNonClientDpiScaling](/windows/desktop/api/winuser/nf-winuser-enablenonclientdpiscaling) durante \_ o WM NCCREATE para solicitar que o Windows dimensione corretamente a área não cliente da janela.

## <a name="per-monitor-dpi-scaling-support-by-ui-framework--technology"></a>Suporte ao dimensionamento de DPI por monitor pela estrutura/tecnologia da interface do usuário

A tabela a seguir mostra o nível de suporte de reconhecimento de DPI por monitor oferecido por várias estruturas da interface do usuário do Windows a partir do Windows 10 1703:

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th>Estrutura/tecnologia</th>
<th>Suporte</th>
<th>Versão do SO</th>
<th>Escala de DPI manipulada por</th>
<th>Leitura Adicional</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Plataforma Universal do Windows (UWP)</td>
<td>Completo</td>
<td>1607</td>
<td>Estrutura de interface do usuário</td>
<td><a href="/windows/uwp/get-started/whats-a-uwp">UWP (Plataforma Universal do Windows)</a></td>
</tr>
<tr class="even">
<td>Controles Win32/comuns V6 brutos (comctl32.dll)</td>
<td><ul>
<li>Mensagens de notificação de alteração de DPI enviadas a todos os HWNDs</li>
<li>Os ativos de tema desenhado são renderizados corretamente em controles comuns</li>
<li>Dimensionamento automático de DPI para caixas de diálogo</li>
</ul></td>
<td>1703</td>
<td>Aplicativo</td>
<td><a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow">Exemplo do GitHub</a></td>
</tr>
<tr class="odd">
<td>Windows Forms</td>
<td>Dimensionamento automático limitado por monitor de DPI para alguns controles</td>
<td>1703</td>
<td>Estrutura de interface do usuário</td>
<td><a href="/dotnet/framework/winforms/high-dpi-support-in-windows-forms">Suporte a alto DPI no Windows Forms</a></td>
</tr>
<tr class="even">
<td>Windows Presentation Framework (WPF)</td>
<td>Os aplicativos nativos do WPF terão a escala de DPI do WPF hospedado em outras estruturas e outras estruturas hospedadas no WPF não são dimensionadas automaticamente</td>
<td>1607</td>
<td>Estrutura de interface do usuário</td>
<td><a href="https://github.com/Microsoft/WPF-Samples/tree/master/PerMonitorDPI">Exemplo do GitHub</a></td>
</tr>
<tr class="odd">
<td>GDI</td>
<td>Nenhum</td>
<td>N/D</td>
<td>Aplicativo</td>
<td>Consulte <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">dimensionamento de dpi alta do GDI</a></td>
</tr>
<tr class="even">
<td>GDI+</td>
<td>Nenhum</td>
<td>N/D</td>
<td>Aplicativo</td>
<td>Consulte <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">dimensionamento de dpi alta do GDI</a></td>
</tr>
<tr class="odd">
<td>MFC</td>
<td>Nenhum</td>
<td>N/D</td>
<td>Aplicativo</td>
<td>N/D</td>
</tr>
</tbody>
</table>



 

## <a name="updating-existing-applications"></a>Atualizando aplicativos existentes

Para atualizar um aplicativo de área de trabalho existente para manipular o dimensionamento de DPI corretamente, ele precisa ser atualizado de modo que, no mínimo, as partes importantes de sua interface do usuário sejam atualizadas para responder a alterações de DPI.

A maioria dos aplicativos de desktop é executada no modo de reconhecimento de DPI do sistema. Aplicativos com reconhecimento de DPI de sistema normalmente são dimensionados para o DPI da exibição primária (a exibição na qual a bandeja do sistema estava localizada no momento em que a sessão do Windows foi iniciada). Quando o DPI é alterado, o Windows bitmap amplia a interface do usuário desses aplicativos, o que geralmente resulta na desfoque. Ao atualizar um aplicativo com reconhecimento de DPI do sistema para se tornar ciente por monitor-DPI, o código que manipula o layout da interface do usuário precisa ser atualizado, de modo que ele seja executado não apenas durante a inicialização do aplicativo, mas também sempre que uma notificação de alteração de DPI ([WM \_ DPICHANGED](wm-dpichanged.md) no caso do Win32) for recebida. Isso geralmente envolve a revisita de qualquer suposição no código que a interface do usuário só precisa ser dimensionada uma vez.

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
2.  Torne a lógica de layout da interface do usuário reutilizável e mova-a para fora do código de inicialização do aplicativo, de modo que ela possa ser reutilizada quando ocorrer uma alteração de DPI (WM \_ DPICHANGED no caso da programação do Windows (Win32)).
3.  Invalidar qualquer código que assuma que os dados sensíveis a DPI (DPI/fontes/tamanhos/etc.) nunca precisem ser atualizados. É uma prática muito comum armazenar em cache os tamanhos de fonte e valores de DPI na inicialização do processo. Ao atualizar um aplicativo para se tornar um reconhecimento de DPI por monitor, os dados sensíveis a DPI devem ser reavaliados sempre que um novo DPI for encontrado.
4.  Quando ocorre uma alteração de DPI, recarregar (ou rerasterizar) todos os ativos de bitmap para o novo DPI ou, opcionalmente, ampliar os ativos carregados no momento para o tamanho correto.
5.  Grep para APIs que não são Per-Monitor DPI reconhecem e as substituem por Per-Monitor APIs com reconhecimento de DPI (quando aplicável). Exemplo: substitua GetSystemMetrics por GetSystemMetricsForDpi.
6.  Teste seu aplicativo em um sistema de várias exibições/vários DPI.
7.  Para qualquer janela de nível superior em seu aplicativo que você não pode atualizar para a escala de DPI correta, use o dimensionamento de DPI de modo misto (descrito abaixo) para permitir o alargamento de bitmap dessas janelas de nível superior pelo sistema.

## <a name="mixed-mode-dpi-scaling-sub-process-dpi-scaling"></a>Escala de DPI de Mixed-Mode (escala de PPP de subprocesso)

Ao atualizar um aplicativo para dar suporte ao reconhecimento de DPI por monitor, às vezes pode se tornar impraticável ou impossível atualizar cada janela no aplicativo em um só lugar. Isso pode ser simplesmente devido ao tempo e esforço necessários para atualizar e testar toda a interface do usuário, ou porque você não possui todo o código da interface do usuário que precisa ser executado (se seu aplicativo talvez carregue a interface do usuário de terceiros). Nessas situações, o Windows oferece uma maneira de facilitar o mundo da conscientização por monitor, permitindo que você execute algumas janelas de aplicativo (somente de nível superior) em seu modo original de reconhecimento de DPI enquanto você se concentra no seu tempo e na atualização de energia das partes mais importantes da sua interface do usuário.

Veja abaixo uma ilustração de como isso poderia ser: você atualiza a interface do usuário do aplicativo principal ("janela principal" na ilustração) para executar com reconhecimento de DPI por monitor enquanto executa outras janelas em seu modo existente ("janela secundária").

![diferenças no dimensionamento de DPI entre modos de reconhecimento](images/hub-page-illustrations.png)

Antes da atualização de aniversário do Windows 10 (1607), o modo de reconhecimento de DPI de um processo era uma propriedade de todo o processo. A partir da atualização de aniversário do Windows 10, essa propriedade agora pode ser definida por janela **de nível superior** . (O Windows **filho** deve continuar a corresponder ao tamanho de dimensionamento de seu pai.) Uma janela de nível superior é definida como uma janela sem nenhum pai. Normalmente, essa é uma janela "regular" com os botões minimizar, maximizar e fechar. O cenário para o qual o reconhecimento de DPI de subprocesso é destinado é ter a interface do usuário secundária dimensionada pelo Windows (bitmap ampliado) enquanto você concentra seu tempo e recursos na atualização da interface do usuário principal.

Para habilitar o reconhecimento de DPI de subprocesso, chame [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) antes e depois de qualquer chamada de criação de janela. A janela criada será associada ao reconhecimento de DPI definido por meio de SetThreadDpiAwarenessContext. Use a segunda chamada para restaurar o reconhecimento de DPI do thread s atual.

Embora o uso do dimensionamento de DPI de subprocesso permita que você confie no Windows para fazer parte do ajuste de DPI para seu aplicativo, ele pode aumentar a complexidade do seu aplicativo. É importante entender as desvantagens dessa abordagem e da natureza das complexidades que ela apresenta. Para obter mais informações sobre o reconhecimento de DPI de subprocesso, consulte [dimensionamento de dpi de modo misto e APIs com reconhecimento de DPI.](high-dpi-improvements-for-desktop-applications.md)

## <a name="testing-your-changes"></a>Testando suas alterações

Depois de atualizar seu aplicativo para se tornar um reconhecimento de DPI por monitor, é importante validar seu aplicativo corretamente responde às alterações de DPI em um ambiente de DPI misto. Algumas especificidades para teste incluem:

1.  Mover janelas de aplicativos para frente e para trás entre telas de valores de DPI diferentes
2.  Iniciando seu aplicativo em exibições de valores de DPI diferentes
3.  Alterando o fator de escala para o monitor enquanto o aplicativo está em execução
4.  Alterar a exibição que você usa como a exibição primária, _sair do Windows_ e, em seguida, testar novamente seu aplicativo depois de entrar novamente. Isso é particularmente útil na localização de código que usa dimensões/tamanhos embutidos em código.

## <a name="common-pitfalls-win32"></a>Armadilhas comuns (Win32)

**Não está usando o retângulo sugerido que é fornecido no WM \_ DPICHANGED**

Quando o Windows envia a janela do aplicativo a uma mensagem do [**WM \_ DPICHANGED**](wm-dpichanged.md) , essa mensagem inclui um retângulo sugerido que você deve usar para redimensionar a janela. É fundamental que seu aplicativo use esse retângulo para se redimensionar, como isso irá:

1.  Verifique se o cursor do mouse permanecerá na mesma posição relativa na janela ao arrastar entre exibições
2.  Impedir que a janela do aplicativo entre em um ciclo de alteração de DPI recursivo em que uma alteração de DPI disparará uma alteração de DPI subsequente, que disparará ainda outra alteração de DPI.

Se você tiver requisitos específicos do aplicativo que impedem o uso do retângulo sugerido que o Windows fornece na \_ mensagem do WM DPICHANGED, consulte [**WM \_ GETDPISCALEDSIZE**](wm-getdpiscaledsize.md). Essa mensagem pode ser usada para dar ao Windows um tamanho desejado que você gostaria de usar depois que a alteração de DPI ocorreu, enquanto ainda evitava os problemas descritos acima.

**Falta de documentação sobre virtualização**

Quando um HWND ou processo está sendo executado como um DPI ou reconhecimento de DPI do sistema, ele pode ser bitmap ampliado pelo Windows. Quando isso acontece, o Windows dimensiona e converte informações sensíveis a DPI de algumas APIs para o espaço de coordenadas do thread de chamada. Por exemplo, se um thread sem reconhecimento de DPI consultar o tamanho da tela durante a execução em uma exibição de alto DPI, o Windows virtualizará a resposta fornecida para o aplicativo como se a tela estivesse em unidades de 96 DPI. Como alternativa, quando um thread com reconhecimento de DPI do sistema está interagindo com uma exibição em um DPI diferente do que estava em uso quando a sessão do usuário atual foi iniciada, o Windows irá dimensionar em DPI algumas chamadas à API para o espaço de coordenadas que o HWND usaria se estivesse em execução em seu fator de escala de DPI original.

Quando você atualiza seu aplicativo de desktop para a escala de DPI corretamente, pode ser difícil saber quais chamadas de API podem retornar valores virtualizados com base no contexto do thread; Atualmente, essas informações não estão suficientemente documentadas pela Microsoft. Lembre-se de que se você chamar qualquer API do sistema de um contexto de thread com reconhecimento de DPI ou sistema, o valor de retorno poderá ser virtualizado. Dessa forma, verifique se o thread está em execução no contexto de DPI que você espera ao interagir com a tela ou com janelas individuais. Ao alterar temporariamente o contexto de DPI de um thread usando [SetThreadDpiAwarenessContext](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext), certifique-se de restaurar o contexto antigo quando terminar de evitar causar um comportamento incorreto em outro lugar em seu aplicativo.

**Muitas APIs do Windows não têm um contexto de DPI**

Muitas APIs herdadas do Windows não incluem um contexto de DPI ou HWND como parte de sua interface. Como resultado, os desenvolvedores geralmente precisam realizar trabalho adicional para lidar com o dimensionamento de qualquer informação sensível a DPI, como tamanhos, pontos ou ícones. Por exemplo, os desenvolvedores que usam [LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadiconw) devem bitmaps de Stretch ou usar APIs alternativas para carregar ícones de tamanho correto para o DPI apropriado, como [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagew).

**Redefinição forçada do reconhecimento de DPI em todo o processo**

Em geral, o modo de reconhecimento de DPI do seu processo não pode ser alterado após a inicialização do processo. No entanto, o Windows pode alterar forçosamente o modo de reconhecimento de DPI do seu processo se você tentar interromper o requisito de que todos os HWNDs em uma árvore de janela tenham o mesmo modo de reconhecimento de DPI. Em todas as versões do Windows, a partir do Windows 10 1703, não é possível ter diferentes HWNDs em uma árvore HWND executada em modos de reconhecimento de DPI diferentes. Se você tentar criar uma relação filho-pai que interrompa essa regra, o reconhecimento de DPI do processo inteiro poderá ser redefinido. Isso pode ser disparado por:

1.  Uma chamada CreateWindow em que a janela pai passada é de um modo de reconhecimento de DPI diferente do thread de chamada.
2.  Uma chamada setpai em que as duas janelas estão associadas a modos de reconhecimento de DPI diferentes.

A tabela a seguir mostra o que acontece se você tentar violar esta regra:



| Operação                 | Windows 8.1                                  | Windows 10 (1607 e anterior)                | Windows 10 (1703 e posterior)                  |
|---------------------------|----------------------------------------------|----------------------------------------------|----------------------------------------------|
| CreateWindow (em processo)    | N/D                                          | **Heranças filho** (modo misto)              | **Heranças filho** (modo misto)              |
| CreateWindow (proc cruzado) | **Redefinição forçada** (do processo do chamador)       | **Heranças filho** (modo misto)              | **Redefinição forçada** (do processo do chamador)       |
| Setpai (no processo)       | N/D                                          | **Redefinição forçada** (do processo atual)        | **Falha** ( \_ estado inválido do erro \_ )             |
| Setpai (proc cruzado)    | **Redefinição forçada** (do processo da janela filho) | **Redefinição forçada** (do processo da janela filho) | **Redefinição forçada** (do processo da janela filho) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de API de DPI alta](high-dpi-reference.md)
</dt> <dt>

[Dimensionamento de DPI de modo misto e APIs com reconhecimento de DPI.](high-dpi-improvements-for-desktop-applications.md)
</dt> </dl>

