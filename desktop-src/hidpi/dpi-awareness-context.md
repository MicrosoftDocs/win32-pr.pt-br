---
title: Identificador de DPI_AWARENESS_CONTEXT (windef. h)
description: Identifica o contexto de conscientização de uma janela.
ms.assetid: BFD54A9F-642B-4A3A-BBB9-F3A80779251D
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 1663fad828a2fb29aa0d65ef58ae79616f64edcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295798"
---
# <a name="dpi_awareness_context-handle"></a>Identificador de contexto de \_ reconhecimento de DPI \_

Identifica o contexto de conscientização de uma janela.

## <a name="syntax"></a>Syntax

``` syntax
#define DPI_AWARENESS_CONTEXT_UNAWARE              ((DPI_AWARENESS_CONTEXT)-1)
#define DPI_AWARENESS_CONTEXT_SYSTEM_AWARE         ((DPI_AWARENESS_CONTEXT)-2)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE    ((DPI_AWARENESS_CONTEXT)-3)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2 ((DPI_AWARENESS_CONTEXT)-4)
#define DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED    ((DPI_AWARENESS_CONTEXT)-5)
```

## <a name="constants"></a>Constantes

**contexto de reconhecimento de DPI sem \_ \_ \_ reconhecimento**<dl> Sem reconhecimento de DPI. Essa janela não é dimensionada para alterações de DPI e sempre é presumido ter um fator de escala de 100% (96 DPI). Ele será dimensionado automaticamente pelo sistema em qualquer outra configuração de DPI.  
</dl>

**\_reconhecimento do \_ sistema de contexto de reconhecimento de DPI \_ \_**<dl> Reconhecimento de DPI do sistema. Essa janela não é dimensionada para alterações de DPI. Ele consultará o DPI uma vez e usará esse valor durante o tempo de vida do processo. Se o DPI for alterado, o processo não será ajustado para o novo valor de DPI. Ele será dimensionado ou reduzido automaticamente pelo sistema quando o DPI for alterado do valor do sistema.  
</dl>

**contexto de reconhecimento de DPI \_ \_ \_ por \_ reconhecimento de monitor \_**<dl> Reconhecimento de DPI por monitor. Essa janela verifica o DPI quando ele é criado e ajusta o fator de escala sempre que o DPI é alterado. Esses processos não são dimensionados automaticamente pelo sistema.  
</dl>

**Contexto de reconhecimento de DPI \_ \_ \_ por \_ reconhecimento de monitor \_ \_ v2**<dl> Também conhecido como **por monitor v2**. Um avanço sobre o modo de reconhecimento de DPI original por monitor, que permite que os aplicativos acessem novos comportamentos de dimensionamento relacionados a DPI de acordo com cada janela de nível superior.  
Por monitor v2 foi disponibilizado na atualização de criadores do Windows 10 e não está disponível em versões anteriores do sistema operacional.  
Os comportamentos adicionais introduzidos são os seguintes:

-   **Notificações de alteração de dpi de janela filho** – em contextos de monitor v2, toda a árvore de janela é notificada sobre qualquer alteração de dpi que ocorrer.
-   **Dimensionamento de área de não-cliente** – todas as janelas terão automaticamente sua área que não seja de cliente desenhada de maneira sensível a dpi. Chamadas para [**EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling) são desnecessárias.
-   **Dimensionamento de menus do Win32** – todos os menus do Ntuser criados nos contextos de acordo com o monitor v2 serão dimensionados de acordo com o monitor.
-   **Dimensionamento de caixa de diálogo** -caixas de diálogo do Win32 criadas nos contextos de por monitor v2 responderão automaticamente às alterações de DPI.
-   **Dimensionamento aprimorado de controles comctl32** – vários controles comctl32 melhoraram o comportamento de dimensionamento de DPI nos contextos v2 do monitor.
-   **Comportamento aprimorado-os** identificadores de Uxtheme abertos no contexto de uma janela por monitor v2 funcionarão em termos do dpi associado a essa janela.

  
</dl>

**DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED**

DPI sem reconhecimento com qualidade aprimorada de conteúdo baseado em GDI. Esse modo se comporta de forma semelhante à DPI_AWARENESS_CONTEXT_UNAWARE, mas também permite que o sistema aprimore automaticamente a qualidade de renderização do texto e outros primitivos baseados em GDI quando a janela é exibida em um monitor de DPI alto.

Para obter mais detalhes, consulte [aprimorando a experiência de alto DPI em aplicativos de área de trabalho baseados em GDI](https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/#Uwv9gY1SvpbgQ4dK.97).

DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED foi introduzido na atualização de outubro de 2018 do Windows 10 (também conhecido como versão 1809).


## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|----|-----------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1607\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível <br/>  |
| parâmetro<br/>                   | <dl> <dt>windef. h</dt> </dl> |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**AreDpiAwarenessContextsEqual**](/windows/desktop/api/winuser/nf-winuser-aredpiawarenesscontextsequal)
</dt> <dt>

[**GetAwarenessFromDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getawarenessfromdpiawarenesscontext)
</dt> </dl>

[**GetDpiFromDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getdpifromdpiawarenesscontext)
</dt> </dl>

[**GetThreadDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getthreaddpiawarenesscontext)
</dt> </dl>

[**GetWindowDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext)
</dt> </dl>

[**IsValidDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-isvaliddpiawarenesscontext)
</dt> </dl>

[**SetProcessDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext)
</dt> </dl>

[**SetThreadDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext)
