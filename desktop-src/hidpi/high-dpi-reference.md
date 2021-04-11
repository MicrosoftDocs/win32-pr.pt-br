---
title: Referência de DPI alto
description: .
ms.assetid: 07A2D45E-721C-4DA8-82A5-38B2FB94BC6D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ec59f34aa5ed036d7f4376cb3d170b5d7849f4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365861"
---
# <a name="high-dpi-reference"></a>Referência de DPI alto

## <a name="functions"></a>Funções



|                                                                                          |                                                                                                                                                                   |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tópico**                                                                                | **Descrição**                                                                                                                                                   |
| [**AdjustWindowRectExForDpi**](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi)                             | Uma variante de [AdjustWindowRectEx](/windows/desktop/api/winuser/nf-winuser-adjustwindowrectex) que retorna valores dimensionados para um dpi específico.       |
| [**AreDpiAwarenessContextsEqual**](/windows/desktop/api/Winuser/nf-winuser-aredpiawarenesscontextsequal)                     | Determina se dois valores de [**\_ \_ contexto de reconhecimento de DPI**](dpi-awareness-context.md) são equivalentes.                                                            |
| [**EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling)                           | Habilita o dimensionamento automático da área não cliente da janela de nível superior especificada.                                                                               |
| [**GetAwarenessFromDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-getawarenessfromdpiawarenesscontext)       | Recupera o valor de [**\_ reconhecimento de DPI**](/windows/desktop/api/windef/ne-windef-dpi_awareness) de um [**contexto de \_ reconhecimento \_ de DPI**](dpi-awareness-context.md)                                       |
| [**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor)                                             | Consulta as informações de DPI associadas a um monitor.                                                                                                            |
| [**GetDpiForSystem**](/windows/desktop/api/Winuser/nf-winuser-getdpiforsystem)                                               | Retorna o DPI do sistema.                                                                                                                                           |
| [**GetDpiForWindow**](/windows/desktop/api/Winuser/nf-winuser-getdpiforwindow)                                               | Retorna o DPI atual para a janela especificada.                                                                                                                 |
| [**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness)                                 | Recupera o modo de virtualização de DPI do processo especificado.                                                                                                   |
| [**GetSystemMetricsForDpi**](/windows/desktop/api/Winuser/nf-winuser-getsystemmetricsfordpi)                                 | Uma variante de [GetSystemMetrics](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) que retorna valores dimensionados para um dpi específico.         |
| [**GetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-getthreaddpiawarenesscontext)                     | Recupera o contexto de reconhecimento de DPI ativo para o thread atual.                                                                                                |
| [**GetWindowDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-getwindowdpiawarenesscontext)                     | Recupera o contexto de reconhecimento de DPI para uma janela.                                                                                                                 |
| [**IsValidDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-isvaliddpiawarenesscontext)                         | Determina se um [**\_ \_ contexto de reconhecimento de DPI**](dpi-awareness-context.md) é válido e tem suporte do sistema atual.                                            |
| [**LogicalToPhysicalPointForPerMonitorDPI**](/windows/desktop/api/winuser/nf-winuser-logicaltophysicalpointforpermonitordpi) | Converte um ponto em uma janela de coordenadas lógicas em coordenadas físicas, independentemente do reconhecimento de DPI do chamador.                                   |
| [**PhysicalToLogicalPointForPerMonitorDPI**](/windows/desktop/api/winuser/nf-winuser-physicaltologicalpointforpermonitordpi) | Converte um ponto em uma janela de coordenadas físicas em coordenadas lógicas, independentemente do reconhecimento de DPI do chamador.                                   |
| [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness)                                 | Define o modo de virtualização de DPI para o processo atual.                                                                                                         |
| [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext)                     | Altera o contexto de reconhecimento de DPI ativo para o thread atual.                                                                                                  |
| [**SystemParametersInfoForDpi**](/windows/desktop/api/Winuser/nf-winuser-systemparametersinfofordpi)                         | Uma variante de [SystemParametersInfo](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) que retorna valores dimensionados para um dpi específico.     |
| [**SetProcessDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext)                   | Define o contexto de reconhecimento de DPI para o processo atual.                                                                                                           |
| [**SetDialogDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-setdialogdpichangebehavior)                         | Substitui o comportamento padrão de dimensionamento de DPI por monitor de uma caixa de diálogo.                                                                                               |
| [**GetDialogDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-getdialogdpichangebehavior)                         | Recupera o comportamento de dimensionamento de DPI por monitor de uma caixa de diálogo.                                                                                                       |
| [**SetDialogControlDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-setdialogcontroldpichangebehavior)                     | Substitui o comportamento padrão de dimensionamento de DPI por monitor de uma janela filho em uma caixa de diálogo.                                                                             |
| [**GetDialogControlDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-getdialogcontroldpichangebehavior)                     | Recupera qualquer substituição de comportamento de dimensionamento de DPI por monitor de uma janela filho em uma caixa de diálogo.                                                                           |
| [**OpenThemeDataForDpi**](/windows/desktop/api/uxtheme/nf-uxtheme-openthemedatafordpi)                                       | Uma variante de [OpenThemeData](/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata) que abre identificadores de tema associados a um dpi específico. |
| [**GetSystemDpiForProcess**](/windows/desktop/api/winuser/nf-winuser-getsystemdpiforprocess)                                 | Recupera o sistema de DPI associado a um determinado processo.                                                                                                         |
| [**GetDpiFromDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getdpifromdpiawarenesscontext)                   | Recupera o DPI de um determinado identificador de [ \_ \_ contexto de reconhecimento de DPI](dpi-awareness-context.md) .                                                                       |
| [**SetThreadDpiHostingBehavior**](/windows/desktop/api/winuser/nf-winuser-setthreaddpihostingbehavior)                       | Substitui o comportamento de Hospedagem de DPI padrão do thread atual.                                                                                                 |
| [**GetThreadDpiHostingBehavior**](/windows/desktop/api/winuser/nf-winuser-getthreaddpihostingbehavior)                       | Recupera o comportamento de Hospedagem de DPI do thread atual.                                                                                                         |
| [**GetWindowDpiHostingBehavior**](/windows/desktop/api/winuser/nf-winuser-getwindowdpihostingbehavior)                       | Recupera o comportamento de Hospedagem de DPI da janela especificada.                                                                                                       |



 

## <a name="types"></a>Tipos



|                                                                            |                                                                                        |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| **Tópico**                                                                  | **Descrição**                                                                        |
| [**reconhecimento de DPI \_**](/windows/desktop/api/windef/ne-windef-dpi_awareness)                                    | Representa os modos de virtualização de coordenadas de DPI.                                        |
| [**\_contexto de reconhecimento de DPI \_**](dpi-awareness-context.md)                   | Um token que representa um modo de virtualização de DPI e comportamentos associados.           |
| [**\_comportamentos de \_ alteração de dpi de controle de diálogo \_ \_**](/windows/desktop/api/winuser/ne-winuser-dialog_control_dpi_change_behaviors) | Descreve as substituições de comportamento de dimensionamento de DPI por monitor para janelas filhas em caixas de diálogo. |
| [**\_comportamentos de \_ alteração de dpi de diálogo \_**](/windows/desktop/api/winuser/ne-winuser-dialog_dpi_change_behaviors)      | Descreve as substituições de comportamento de dimensionamento de DPI por monitor para caixas de diálogo.                      |
| [**\_tipo de DPI do monitor \_**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-monitor_dpi_type)                 | Representa o tipo de DPI associado a um monitor.                                  |
| [**\_reconhecimento de dpi de processo \_**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness)                   | Representa o modo de virtualização de coordenadas de DPI de um processo.                        |
| [**\_comportamento de Hospedagem de DPI \_**](/windows/win32/api/windef/ne-windef-dpi_hosting_behavior)                    | Representa o comportamento de Hospedagem de DPI para uma janela.                                      |



 

## <a name="messages"></a>Mensagens



|                                                                    |                                                                                                                                         |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **Tópico**                                                          | **Descrição**                                                                                                                         |
| [**DPICHANGED do WM \_**](wm-dpichanged.md)                            | Notifica uma janela de nível superior que seu DPI mudou.                                                                                   |
| [**BEFOREPARENT do WM \_ DPICHANGED \_**](wm-dpichanged-beforeparent.md) | Notifica uma janela filho que a DPI associada à sua janela recipiente foi alterada. Entregue antes que a janela pai seja notificada. |
| [**AFTERPARENT do WM \_ DPICHANGED \_**](wm-dpichanged-afterparent.md)   | Notifica uma janela filho que a DPI associada à sua janela recipiente foi alterada. Entregue depois que a janela pai é notificada.  |
| [**GETDPISCALEDSIZE do WM \_**](wm-getdpiscaledsize.md)                | Permite que janelas de nível superior redimensionem *não linearmente* em resposta a alterações de DPI.                                                           |



 

 

 