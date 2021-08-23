---
title: Mixed-Mode dimensionamento de DPI e APIs com conhecimento de DPI
description: Mixed-Mode dimensionamento de DPI e APIs com conhecimento de DPI
ms.assetid: 44AC0B29-3283-4801-90F5-3E78CCD87B9F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb32de01390f2794b5714bdca5465a5997121c270ded9c170e0b0171fd972542
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036214"
---
# <a name="mixed-mode-dpi-scaling-and-dpi-aware-apis"></a>Mixed-Mode dimensionamento de DPI e APIs com conhecimento de DPI

## <a name="sub-process-dpi-awareness-support"></a>Sub-Process reconhecimento de DPI

[**SetThreadDpiAwarenessContext permite**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) o uso de diferentes modos de dimensionamento de DPI em um único processo. Antes da Atualização de Aniversário do Windows 10, o reconhecimento de DPI de uma janela era vinculado ao modo de reconhecimento de DPI em todo o processo (sem reconhecimento de DPI, com reconhecimento de DPI do sistema ou com reconhecimento de DPI Per-Monitor). Mas agora, com **SetThreadDpiAwarenessContext,** as janelas de nível superior podem ter um modo de reconhecimento de DPI diferente do modo de reconhecimento de DPI em todo o processo. Isso também afeta as janelas filho, pois elas sempre terão o mesmo modo de reconhecimento de DPI que a janela pai.

O uso de **SetThreadDpiAwarenessContext** permite que os desenvolvedores decidam onde eles querem concentrar seus esforços de desenvolvimento ao definir o comportamento específico do DPI para aplicativos da área de trabalho. Por exemplo, a janela de nível superior principal de um aplicativo pode ser dimensionada por monitor, enquanto as janelas secundárias de nível superior podem ser dimensionadas por meio do dimensionamento de bitmap pelo sistema operacional.

## <a name="the-dpi-awareness-context"></a>O contexto de reconhecimento de DPI

Antes da disponibilidade de **SetThreadDpiAwarenessContext,** o reconhecimento de DPI de um processo era definido no manifesto do binário do aplicativo ou por meio de uma chamada para [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) durante a inicialização do processo. Com **SetThreadDpiAwarenessContext**, cada thread pode ter um contexto de reconhecimento de DPI individual que pode ser diferente do modo de reconhecimento de DPI em todo o processo. O contexto de reconhecimento de DPI de um thread é representado com o tipo ***CONTEXTO DE RECONHECIMENTO [de \_ DPI*** \_ ](dpi-awareness-context.md) e se comporta das seguintes maneiras:

-   Um thread pode ter seu contexto de reconhecimento de DPI alterado a qualquer momento.
-   Todas as chamadas à API que são feitas depois que o contexto é alterado serão executados no contexto de DPI correspondente (e podem ser virtualizados).
-   Quando uma janela é criada, seu reconhecimento de DPI é definido como o reconhecimento de DPI do thread de chamada no momento.
-   Quando o procedimento de janela para uma janela é chamado, o thread é alternado automaticamente para o contexto de reconhecimento de DPI que estava em uso quando a janela foi criada.

Um cenário comum para o uso de **SetThreadDpiAwarenessContext** é o seguinte: Comece com um thread em execução com um contexto (como CONTEXTO DE RECONHECIMENTO **de DPI \_ POR MONITOR \_ \_ \_ \_ AWARE**) alternar temporariamente para um contexto diferente ( CONTEXTO DE RECONHECIMENTO de DPI SEM RECONHECIMENTO), criar uma janela e, em seguida, alternar imediatamente o contexto de thread de volta para seu estado anterior.**\_ \_ \_** A janela criada terá um contexto DPI de CONTEXTO DE RECONHECIMENTO de **DPI \_ \_ \_ SEM** RECONHECIMENTO, enquanto o contexto do thread de chamada será restaurado para CONTEXTO DE RECONHECIMENTO **de DPI \_ POR MONITOR \_ \_ \_ \_ AWARE** com uma chamada subsequente para **SetThreadDpiAwarenessContext**. Nesse cenário, a janela associada ao thread de chamada seria executado com um contexto por monitor (e, portanto, não seria ampliada pelo bitmap pelo sistema operacional), enquanto a janela recém-criada não estaria ciente de DPI (e, portanto, seria automaticamente ampliada em um bitmap estendido em um conjunto de exibição para >100% de dimensionamento).

A Figura 1 ilustra como o thread de processo principal é executado com o CONTEXTO DE RECONHECIMENTO **de DPI \_ POR \_ \_ \_ MONITOR,** alterna seu contexto para CONTEXTO DE RECONHECIMENTO **de DPI SEM \_ \_ \_ RECONHECIMENTO** e cria uma nova janela. Em seguida, a janela recém-criada é executada com um contexto de reconhecimento de DPI de CONTEXTO DE RECONHECIMENTO **de DPI \_ SEM RECONHECIMENTO \_ \_ SEMPRE** que uma mensagem é enviada a ela ou chamadas à API são feitas dela. Imediatamente após a criação da nova janela, o thread principal é restaurado para seu contexto anterior de **CONTEXTO DE RECONHECIMENTO de DPI POR \_ \_ \_ \_ MONITOR.**

![diagrama mostrando o reconhecimento de dpi por monitor em ação](images/dpi-awareness-context.png)

## <a name="new-dpi-related-apis"></a>Novas APIs relacionadas ao DPI

Além do suporte para diferentes modos de reconhecimento de DPI em um único processo que **SetThreadDpiAwarenessContext** oferece, a seguinte funcionalidade específica de DPI foi adicionada para aplicativos da área de trabalho:<dl> <dd>[EnableNonClientDpiScaling****](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling)<dl> <dt>



> [!Note]  
> O modo de reconhecimento de DPI por monitor **V2** habilita automaticamente essa funcionalidade e chamar **EnableNonClientDpiScaling** é, portanto, desnecessário em aplicativos que a usam.

 

Chamar **EnableNonClientDpiScaling** de dentro do manipulador **WM \_ NCCREATE** de uma janela resultará na área não cliente de uma janela de nível superior dimensionando automaticamente para DPI. Se a janela de nível superior for com suporte a DPI por monitor (seja porque o processo em si é com suporte a DPI por monitor ou porque a janela foi criada em um thread com suporte para DPI por monitor), a barra de legendas, as barras de rolagem, os menus e as barras de menu dessas janelas serão dimensionados em DPI sempre que o DPI da janela mudar.
</dt> <dt>

Observe que áreas não cliente de uma janela filho, como barras de rolagem não cliente de um controle de edição filho, não serão dimensionadas automaticamente quando essa API for usada.
</dt> <dt>

> [!Note]  
> **EnableNonClientDpiScaling** deve ser chamado do manipulador **WM \_ NCCREATE.**

</dt> </dl> </dd> <dd> <b> As APIs *ForDpi </b>

-   Várias APIs usadas com frequência, como [**GetSystemMetrics,**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) não têm nenhum contexto de um HWND e, portanto, não têm nenhuma maneira de induzir o reconhecimento de DPI adequado para seus valores de retorno. Chamar essas APIs de um thread que está em execução em um modo ou contexto de reconhecimento de DPI diferente pode retornar valores que não são dimensionados para o contexto do thread de chamada. [****GetSystemMetricForDpi****](/windows/desktop/api/Winuser/nf-winuser-getsystemmetricsfordpi), [***SystemParametersInfoForDpi***](/windows/desktop/api/Winuser/nf-winuser-systemparametersinfofordpi)e [***AdjustWindowRectExForDpi***](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi) executarão a mesma funcionalidade que seus equivalentes sem reconhecimento de DPI, mas pegarão um DPI como um argumento e inferirão o reconhecimento de dpi do contexto atual do thread.
-   **GetSystemMetricForDpi** e **SystemParametersInfoForDpi** retornarão valores de métrica do sistema dimensionados por DPI e valores de parâmetro do sistema de acordo com esta equação:

    
    GetSystemMetrics(...) @ dpi == GetSystemMetricsForDpi(..., dpi)

    

     

    Portanto, chamar **GetSystemMetrics** (ou **SystemParametersInfoForDpi**), durante a execução em um dispositivo com um determinado valor de DPI do sistema retornará o mesmo valor que suas variantes com conhecimento de DPI **(GetSystemMetricsForDpi** e **SystemParametersInfoForDpi**), considerando o mesmo valor de DPI que a entrada.

-   [**AdjustWindowRectExForDpi**](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi) recebe um HWND e calculará o tamanho necessário de um retângulo de janela de maneira sensível a DPI.

</dd> <dd>

</dd> <dd><b><a href="/windows/desktop/api/Winuser/nf-winuser-getdpiforwindow">GetDpiForWindow</a></b><dl> <dt><b>GetDpiForWindow</b> retornará o DPI associado ao HWND fornecido. A resposta dependerá do modo de reconhecimento de DPI do HWND:

| Modo de Reconhecimento de DPI do HWND | Valor retornado                                                                                                                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inconscientes                    | 96                                                                                                                                                                                                            |
| Sistema                     | O DPI do sistema                                                                                                                                                                                                |
| Per-Monitor                | O DPI de exibição em que a janela de nível superior associada está localizada principalmente <br/> (Se uma janela filho for fornecida, o DPI da janela pai de nível superior correspondente será retornado)<br/> |

</dt> </dl> </dd> <dd><b><a href="/windows/desktop/api/Winuser/nf-winuser-getdpiforsystem">GetDpiForSystem</a></b><dl> <dt>

Chamar **GetDpiForSystem é** mais eficiente do que chamar [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc) e [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) para obter o DPI do sistema.
</dt> <dt>

Qualquer componente que possa estar em execução em um aplicativo que usa reconhecimento de DPI de sub process não deve assumir que o DPI do sistema é estático durante o ciclo de vida do processo. Por exemplo, se um thread que está em execução no contexto de reconhecimento SEM RECONHECIMENTO de DPI consultar o DPI do sistema, a resposta será 96. **\_ \_ \_** No entanto, se esse mesmo thread alternado para o contexto de reconhecimento do SISTEMA de CONTEXTO DE RECONHECIMENTO de DPI e consultado o DPI do sistema novamente, a resposta poderá ser diferente. **\_ \_ \_** Para evitar o uso de um valor DPI de sistema armazenado em cache (e possivelmente desleixado), use **GetDpiForSystem** para recuperar o DPI do sistema em relação ao modo de reconhecimento de DPI do thread de chamada. 
</dt> </dl> </dd> </dl>
