---
title: DPI_AWARENESS_CONTEXT de DPI_AWARENESS_CONTEXT (windef.h)
description: Identifica o contexto de reconhecimento de uma janela.
ms.assetid: BFD54A9F-642B-4A3A-BBB9-F3A80779251D
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 25e270f59af32b33fdb5ad3f511b693b3eebad71407d48b80a72aff5996edf14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727176"
---
# <a name="dpi_awareness_context-handle"></a>Alça de \_ CONTEXTO DE RECONHECIMENTO DE DPI \_

Identifica o contexto de reconhecimento de uma janela.

## <a name="syntax"></a>Syntax

``` syntax
#define DPI_AWARENESS_CONTEXT_UNAWARE              ((DPI_AWARENESS_CONTEXT)-1)
#define DPI_AWARENESS_CONTEXT_SYSTEM_AWARE         ((DPI_AWARENESS_CONTEXT)-2)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE    ((DPI_AWARENESS_CONTEXT)-3)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2 ((DPI_AWARENESS_CONTEXT)-4)
#define DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED    ((DPI_AWARENESS_CONTEXT)-5)
```

## <a name="constants"></a>Constantes

**CONTEXTO DE RECONHECIMENTO DE DPI \_ \_ SEM \_ RECONHECIMENTO**<dl> DPI sem conhecimento. Essa janela não é dimensionado para alterações de DPI e sempre é presumida como ter um fator de escala de 100% (96 DPI). Ele será dimensionado automaticamente pelo sistema em qualquer outra configuração de DPI.  
</dl>

**RECONHECIMENTO DO SISTEMA \_ DE CONTEXTO DE RECONHECIMENTO \_ \_ DE \_ DPI**<dl> Ciente de DPI do sistema. Essa janela não é dimensiona para alterações de DPI. Ele consultará o DPI uma vez e usará esse valor durante o tempo de vida do processo. Se o DPI mudar, o processo não será ajustado para o novo valor de DPI. Ele será automaticamente escalado ou rebaixado pelo sistema quando o DPI mudar do valor do sistema.  
</dl>

**CONTEXTO DE RECONHECIMENTO DE DPI \_ \_ POR MONITOR \_ \_ \_ CIENTE**<dl> Por monitor com conhecimento de DPI. Essa janela verifica o DPI quando ele é criado e ajusta o fator de escala sempre que o DPI muda. Esses processos não são dimensionados automaticamente pelo sistema.  
</dl>

**CONTEXTO DE RECONHECIMENTO DE DPI \_ POR MONITOR COM RECONHECIMENTO \_ \_ \_ \_ \_ V2**<dl> Também conhecido como **Por Monitor v2**. Um avanço sobre o modo de reconhecimento de DPI original por monitor, que permite que os aplicativos acessem novos comportamentos de dimensionamento relacionados ao DPI por janela de nível superior.  
Por Monitor v2 foi disponibilizado na Atualização para Criadores do Windows 10 e não está disponível em versões anteriores do sistema operacional.  
Os comportamentos adicionais introduzidos são os seguinte:

-   **Notificações de alteração de DPI** da janela filho – em contextos por monitor v2, toda a árvore de janelas é notificada sobre as alterações de DPI que ocorrem.
-   **Dimensionamento de área não cliente** – todas as janelas terão automaticamente sua área não cliente desenhada de maneira sensível ao DPI. Chamadas para [**EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling) são desnecessárias.
-   **Dimensionamento de menus Win32** – Todos os menus NTUSER criados em Contextos por Monitor v2 serão dimensionados de forma por monitor.
-   **Dimensionamento de caixa de** diálogo – Caixas de diálogo Win32 criadas em contextos por Monitor v2 responderão automaticamente às alterações de DPI.
-   **Dimensionamento aprimorado** de controles comctl32 – vários controles comctl32 melhoraram o comportamento de dimensionamento de DPI em contextos por monitor v2.
-   **Comportamento de temas** aprimorado – os handles de UxTheme abertos no contexto de uma janela Por Monitor v2 operarão em termos do DPI associado a essa janela.

  
</dl>

**DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED**

DPI sem conhecimento da qualidade aprimorada do conteúdo baseado em GDI. Esse modo se comporta de modo semelhante ao DPI_AWARENESS_CONTEXT_UNAWARE, mas também permite que o sistema melhore automaticamente a qualidade de renderização de texto e outros primitivos baseados em GDI quando a janela é exibida em um monitor de alto DPI.

Para obter mais detalhes, consulte [Melhorando a experiência de alto DPI em aplicativos](https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/#Uwv9gY1SvpbgQ4dK.97)da Área de Trabalho baseados em GDI.

DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED foi introduzido na atualização de outubro de 2018 do Windows 10 (também conhecida como versão 1809).


## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|----|-----------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1607 somente \[ aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível <br/>  |
| Cabeçalho<br/>                   | <dl> <dt>windef.h</dt> </dl> |

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
