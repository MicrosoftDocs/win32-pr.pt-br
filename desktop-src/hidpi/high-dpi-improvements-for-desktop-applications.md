---
title: Mixed-Mode o dimensionamento de DPI e APIs com reconhecimento de DPI
description: Mixed-Mode o dimensionamento de DPI e APIs com reconhecimento de DPI
ms.assetid: 44AC0B29-3283-4801-90F5-3E78CCD87B9F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6f5b16e4c438cfe1f0d04e61524899e213b25ea
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119721"
---
# <a name="mixed-mode-dpi-scaling-and-dpi-aware-apis"></a>Mixed-Mode o dimensionamento de DPI e APIs com reconhecimento de DPI

## <a name="sub-process-dpi-awareness-support"></a>Suporte ao reconhecimento de DPI de Sub-Process

O [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) permite o uso de diferentes modos de dimensionamento de DPI em um único processo. Antes da atualização de aniversário do Windows 10, um reconhecimento da janela s DPI era associado ao modo de reconhecimento de DPI de todo o processo (sem reconhecimento de DPI, reconhecimento de DPI de sistema ou reconheceção de Per-Monitor DPI). Mas agora, com o **SetThreadDpiAwarenessContext**, as janelas de nível superior podem ter um modo de reconhecimento de DPI diferente daquele do modo de reconhecimento de dpi de todo o processo. Isso também afeta as janelas filhas, pois elas sempre terão o mesmo modo de reconhecimento de DPI que sua janela pai.

O uso de **SetThreadDpiAwarenessContext** permite que os desenvolvedores decidam onde desejam concentrar seus esforços de desenvolvimento ao definir o comportamento específico de dpi para aplicativos de desktop. Por exemplo, uma janela de nível superior primária de um aplicativo pode ser dimensionada de acordo com o monitor, enquanto janelas de nível superior secundárias podem ser dimensionadas por meio do dimensionamento de bitmap pelo sistema operacional.

## <a name="the-dpi-awareness-context"></a>O contexto de reconhecimento de DPI

Antes da disponibilidade de **SetThreadDpiAwarenessContext** , o reconhecimento de dpi de um processo foi definido no manifesto do binário do aplicativo ou por meio de uma chamada para [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) durante a inicialização do processo. Com o **SetThreadDpiAwarenessContext**, cada thread pode ter um contexto de reconhecimento de DPI individual que pode ser diferente daquele do modo de reconhecimento de dpi de todo o processo. O contexto de reconhecimento de DPI de um thread é representado com o * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *. [ \_ \_ ](dpi-awareness-context.md)

-   Um thread pode ter seu contexto de reconhecimento de DPI alterado a qualquer momento.
-   Todas as chamadas à API feitas após o contexto ser alterada serão executadas no contexto de DPI correspondente (e podem ser virtualizadas).
-   Quando uma janela é criada, seu reconhecimento de DPI é definido como o reconhecimento de DPI do thread de chamada nesse momento.
-   Quando o procedimento de janela para uma janela é chamado, o thread é alternado automaticamente para o contexto de reconhecimento de DPI que estava em uso quando a janela foi criada.

Um cenário comum para o uso de **SetThreadDpiAwarenessContext** é o seguinte: comece com um thread que está sendo executado com um contexto (como o **contexto de reconhecimento de DPI \_ \_ \_ por \_ \_ reconhecimento de monitor**) alterne temporariamente para um contexto diferente (o contexto de reconhecimento de DPI não **\_ \_ \_ reconhece**), crie uma janela e, em seguida, alterne imediatamente o contexto de thread para seu estado anterior. A janela criada terá um contexto de DPI de contexto de **reconhecimento de DPI sem \_ \_ \_ reconhecimento**, enquanto o contexto de thread s de chamada será restaurado para o **contexto de reconhecimento de DPI \_ \_ \_ por \_ Monitor \_ ciente** de uma chamada subsequente para **SetThreadDpiAwarenessContext**. Nesse cenário, a janela associada ao thread de chamada seria executada com um contexto por monitor (e, portanto, não deve ser ampliada por bitmap pelo sistema operacional), enquanto a janela recém-criada não seria um reconhecimento de DPI (e, portanto, seria bitmap automaticamente ampliado em um conjunto de exibição para >100% de dimensionamento).

A Figura 1 ilustra como o thread do processo principal é executado com o **contexto de reconhecimento de DPI \_ \_ \_ por \_ Monitor**, alterna seu contexto para o **contexto de reconhecimento de DPI sem \_ \_ \_ reconhecimento** e cria uma nova janela. Em seguida, a janela recém-criada é executada com um contexto de reconhecimento de DPI de contexto de reconhecimento de DPI, sempre que uma mensagem é expedida para a ti ou chamadas de API são feitas a partir dela. **\_ \_ \_** Imediatamente após a criação da nova janela, o thread principal é restaurado para seu contexto anterior de **contexto de reconhecimento de DPI \_ \_ \_ por \_ Monitor**.

![diagrama mostrando reconhecimento de DPI por monitor em ação](images/dpi-awareness-context.png)

## <a name="new-dpi-related-apis"></a>Novas APIs relacionadas a DPI

Além do suporte para modos de reconhecimento de DPI diferentes em um único processo que o **SetThreadDpiAwarenessContext** oferece, a seguinte funcionalidade específica de DPI foi adicionada para aplicativos de área de trabalho:<dl> <dd>[EnableNonClientDpiScaling****](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling)<dl> <dt>



> [!Note]  
> O modo de reconhecimento de DPI **por monitor v2** habilita automaticamente essa funcionalidade, e chamar **EnableNonClientDpiScaling** é, portanto, desnecessário em aplicativos que o utilizam.

 

Chamar **EnableNonClientDpiScaling** de dentro de um manipulador **de \_ NCCREATE do WM** da janela fará com que a área não cliente de uma janela de nível superior seja automaticamente dimensionada para DPI. Se a janela de nível superior tiver reconhecimento de DPI por monitor (independentemente de o próprio processo ter reconhecimento de DPI por monitor ou porque a janela foi criada dentro de um thread com reconhecimento de DPI por monitor), a barra de legendas, as barras de rolagem, os menus e as barras de menus dessas janelas terão escala de DPI sempre que o DPI de s da janela for alterado.
</dt> <dt>

Observe que as áreas que não são do cliente de uma janela filho, como barras de rolagem de não-cliente de um controle de edição filho, não serão dimensionadas automaticamente quando essa API for usada.
</dt> <dt>

> [!Note]  
> **EnableNonClientDpiScaling** deve ser chamado a partir do manipulador de **\_ NCCREATE do WM** .

</dt> </dl> </dd> <dd> <b> As APIs * ForDpi </b>

-   Várias APIs usadas com frequência, como [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) , não têm nenhum contexto de um HWND e, portanto, não têm como deduzindo o reconhecimento de DPI apropriado para seus valores de retorno. Chamar essas APIs de um thread que está sendo executado em um modo de reconhecimento de DPI ou contexto diferente pode retornar valores que não são dimensionados para o contexto do thread de chamada. * * * * [GetSystemMetricForDpi * *](/windows/desktop/api/Winuser/nf-winuser-getsystemmetricsfordpi)* *, * * * * [SystemParametersInfoForDpi * *](/windows/desktop/api/Winuser/nf-winuser-systemparametersinfofordpi)* *, e * * * * [AdjustWindowRectExForDpi * * * *](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi) executará a mesma funcionalidade que suas contrapartes sem reconhecimento de DPI, mas pegará um dpi como um argumento e inferirá o reconhecimento de DPI do contexto do thread atual.
-   **GetSystemMetricForDpi** e **SystemParametersInfoForDpi** retornarão valores de métrica do sistema com escala de dpi e valores de parâmetro do sistema de acordo com esta equação:

    
    GetSystemMetrics (...) @ dpi = = GetSystemMetricsForDpi (..., DPI)

    

     

    Portanto, chamar **GetSystemMetrics** (ou **SystemParametersInfoForDpi**), enquanto em execução em um dispositivo com um determinado valor de DPI do sistema, retornará o mesmo valor que suas variantes de reconhecimento de DPI (**GetSystemMetricsForDpi** e **SystemParametersInfoForDpi**), considerando o mesmo valor de dpi que a entrada.

-   [**AdjustWindowRectExForDpi**](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi) usa um HWND e calculará o tamanho necessário de um retângulo de janela de forma sensível a dpi.

</dd> <dd>

</dd> <dd><b><a href="/windows/desktop/api/Winuser/nf-winuser-getdpiforwindow">GetDpiForWindow</a></b><dl> <dt><b>GetDpiForWindow</b> retornará o dpi associado ao HWND fornecido. A resposta dependerá do modo de reconhecimento de DPI do HWND:

| Modo de reconhecimento de DPI de HWND | Valor retornado                                                                                                                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Conhecida                    | 96                                                                                                                                                                                                            |
| Sistema                     | O DPI do sistema                                                                                                                                                                                                |
| Per-Monitor                | O DPI de exibição que a janela de nível superior associada está localizada principalmente em <br/> (Se uma janela filho for fornecida, o DPI da janela pai de nível superior correspondente será retornada)<br/> |

</dt> </dl> </dd> <dd><b><a href="/windows/desktop/api/Winuser/nf-winuser-getdpiforsystem">GetDpiForSystem</a></b><dl> <dt>

Chamar **GetDpiForSystem** é mais eficiente do que chamar [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc) e [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) para obter o DPI do sistema.
</dt> <dt>

Qualquer componente que pudesse ser executado em um aplicativo que usa reconhecimento de DPI de subprocesso não deve assumir que o DPI do sistema é estático durante o ciclo de vida do processo. Por exemplo, se um thread que está sendo executado sob o contexto de reconhecimento de DPI não tiver reconhecimento de alerta no DPI do sistema, a resposta será 96. **\_ \_ \_** No entanto, se o mesmo thread tiver mudado para o contexto de reconhecimento do **sistema de contexto de reconhecimento de DPI \_ \_ \_** e consultasse novamente o DPI do sistema, a resposta poderá ser diferente. Para evitar o uso de um valor do sistema-DPI em cache (e possivelmente obsoleto), use **GetDpiForSystem** para recuperar o DPI do sistema em relação ao modo de reconhecimento de DPI do thread de chamada. 
</dt> </dl> </dd> </dl>
