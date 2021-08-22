---
title: Operações de área de transferência
description: Uma janela deve usar a área de transferência ao cortar, copiar ou colar dados. Uma janela coloca dados na área de transferência para operações de recortar e copiar e recupera dados da área de transferência para operações de colar.
ms.assetid: 27f9142c-3154-4de5-aea6-3c53f7e940ec
keywords:
- Windows Interface do Usuário, área de transferência
- área de transferência, janelas
- área de transferência, reduzindo dados
- área de transferência, copiando dados
- área de transferência, colar dados
- área de transferência, janela proprietário
- área de transferência, renderização atrasada
- área de transferência, memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a0dfe82f6130f0435521ac4e17cf8e8b7162115074f7b3ff716187730f8bb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118545430"
---
# <a name="clipboard-operations"></a>Operações de área de transferência

Uma janela deve usar a área de transferência ao cortar, copiar ou colar dados. Uma janela coloca dados na área de transferência para operações de recortar e copiar e recupera dados da área de transferência para operações de colar. As seções a seguir descrevem essas operações e problemas relacionados.

Para colocar dados ou recuperar dados da área de transferência, uma janela deve primeiro abrir a área de transferência usando a [**função OpenClipboard.**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) Somente uma janela pode ter a área de transferência aberta por vez. Para descobrir qual janela tem a área de transferência aberta, chame a [**função GetOpenClipboardWindow.**](/windows/desktop/api/Winuser/nf-winuser-getopenclipboardwindow) Quando terminar, a janela deverá fechar a área de transferência chamando a [**função CloseClipboard.**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard)

Os tópicos a seguir são discutidos nesta seção.

-   [Operações de recortar e copiar](#cut-and-copy-operations)
-   [Operações de colar](#paste-operations)
-   [Propriedade da área de transferência](#clipboard-ownership)
-   [Renderização atrasada](#delayed-rendering)
-   [Memória e Área de Transferência](#memory-and-the-clipboard)

## <a name="cut-and-copy-operations"></a>Operações de recortar e copiar

Para colocar informações na área de transferência, uma janela primeiro limpa qualquer conteúdo da área de transferência anterior usando a [**função EmptyClipboard.**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) Essa função envia a mensagem [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) para o proprietário da área de transferência anterior, libera os recursos associados aos dados na área de transferência e atribui a propriedade da área de transferência à janela que tem a área de transferência aberta. Para descobrir qual janela possui a área de transferência, chame a [**função GetClipboardOwner.**](/windows/win32/api/winuser/nf-winuser-getclipboardowner)

Depois de esvaziar a área de transferência, a janela coloca os dados na área de transferência no máximo de formatos de área de transferência possível, ordenado do formato mais descritivo da área de transferência para o menos descritivo. Para cada formato, a janela chama a [**função SetClipboardData,**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) especificando o identificador de formato e um identificador de memória global. O alça de memória pode ser NULL, indicando que a janela renderiza os dados na solicitação. Para obter mais informações, consulte [Renderização atrasada.](#delayed-rendering)

## <a name="paste-operations"></a>Operações de colar

Para recuperar informações de colar da área de transferência, uma janela primeiro determina o formato da área de transferência a ser recuperado. Normalmente, uma janela enumera os formatos de área de transferência disponíveis usando a função [**EnumClipboardFormats**](/windows/desktop/api/Winuser/nf-winuser-enumclipboardformats) e usa o primeiro formato que reconhece. Esse método seleciona o melhor formato disponível de acordo com o conjunto de prioridade quando os dados foram colocados na área de transferência.

Como alternativa, uma janela pode usar a [**função GetPriorityClipboardFormat.**](/windows/desktop/api/Winuser/nf-winuser-getpriorityclipboardformat) Essa função identifica o melhor formato de área de transferência disponível de acordo com uma prioridade especificada. Uma janela que reconhece apenas um formato de área de transferência pode simplesmente determinar se esse formato está disponível usando a [**função IsClipboardFormatAvailable.**](/windows/desktop/api/Winuser/nf-winuser-isclipboardformatavailable)

Depois de determinar o formato da área de transferência a ser usado, uma janela chama a [**função GetClipboardData.**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) Essa função retorna o identificador para um objeto de memória global que contém dados no formato especificado. Uma janela pode bloquear brevemente o objeto de memória para examinar ou copiar os dados. No entanto, uma janela não deve liberar o objeto ou deixá-lo bloqueado por um longo período de tempo.

## <a name="clipboard-ownership"></a>Propriedade da área de transferência

O *proprietário da área de* transferência é a janela associada às informações na área de transferência. Uma janela se torna o proprietário da área de transferência quando ela coloca dados na área de transferência, especificamente, quando chama a [**função EmptyClipboard.**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) A janela permanece o proprietário da área de transferência até ser fechada ou outra janela esvazia a área de transferência.

Quando a área de transferência é esvaziada, o proprietário da área de transferência recebe uma [**mensagem WM \_ DESTROYCLIPBOARD.**](wm-destroyclipboard.md) A seguir estão alguns motivos pelos quais uma janela pode processar essa mensagem:

-   A renderização atrasada da janela de um ou mais formatos de área de transferência. Em resposta à mensagem [**WM \_ DESTROYCLIPBOARD,**](wm-destroyclipboard.md) a janela pode liberar recursos alocados para renderizar dados na solicitação. Para obter mais informações sobre a renderização de dados, consulte [Renderização atrasada.](#delayed-rendering)
-   A janela colocou dados na área de transferência em um formato de área de transferência privada. Os dados para formatos de área de transferência privada não são liberados pelo sistema quando a área de transferência é esvaziada. Portanto, o proprietário da área de transferência deve liberar os dados ao receber a [**mensagem WM \_ DESTROYCLIPBOARD.**](wm-destroyclipboard.md) Para obter mais informações sobre formatos de área de transferência privada, consulte [Formatos da área de transferência.](clipboard-formats.md)
-   A janela colocou dados na área de transferência usando o formato da área de transferência **\_ CF OWNERDISPLAY.** Em resposta à mensagem [**WM \_ DESTROYCLIPBOARD,**](wm-destroyclipboard.md) a janela pode liberar recursos usados para exibir informações na janela do visualizador da área de transferência. Para obter mais informações sobre esse formato alternativo, consulte [Formato de exibição do proprietário.](about-the-clipboard.md)

## <a name="delayed-rendering"></a>Renderização atrasada

Ao colocar um formato de área de transferência na área de transferência, uma janela pode atrasar a renderização dos dados nesse formato até que os dados são necessários. Para fazer isso, um aplicativo pode especificar **NULL** para o *parâmetro hData* da [**função SetClipboardData.**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) Isso é útil se o aplicativo dá suporte a vários formatos de área de transferência, alguns ou todos os quais são demorados para renderizar. Ao passar um **alça NULL,** uma janela renderiza formatos de área de transferência complexos somente quando e se eles são necessários.

Se uma janela atrasar a renderização de um formato de área de transferência, ela deverá estar preparada para renderizar o formato mediante solicitação, desde que seja o proprietário da área de transferência. O sistema envia ao proprietário da área de transferência uma mensagem [**WM \_ RENDERFORMAT**](wm-renderformat.md) quando uma solicitação é recebida para um formato específico que não foi renderizado. Ao receber essa mensagem, a janela deve chamar a função [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) para colocar um alça de memória global na área de transferência no formato solicitado.

Um aplicativo não deve abrir a área de transferência antes de chamar [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) em resposta à mensagem [**WM \_ RENDERFORMAT.**](wm-renderformat.md) Abrir a área de transferência não é necessário e qualquer tentativa de fazer isso falhará porque a área de transferência está sendo mantida aberta no momento pelo aplicativo que solicitou que o formato fosse renderizado.

Se o proprietário da área de transferência estiver prestes a ser destruído e tiver atrasado a renderização de alguns ou todos os formatos de área de transferência, ele receberá a mensagem [**WM \_ RENDERALLFORMATS.**](wm-renderallformats.md) Ao receber essa mensagem, a janela deve abrir a área de transferência, verificar se ela ainda é o proprietário da área de transferência com a [**função GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) e colocar os alças de memória válidos na área de transferência para todos os formatos de área de transferência que ela fornece. Isso garante que esses formatos permaneçam disponíveis depois que o proprietário da área de transferência for destruído.

Ao contrário [**do WM \_ RENDERFORMAT**](wm-renderformat.md), um aplicativo que responde ao [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) deve abrir a área de transferência antes de chamar [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) para colocar quaisquer alças de memória globais na área de transferência.

Todos os formatos de área de transferência que não são renderizados em resposta à mensagem [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) deixam de estar disponíveis para outros aplicativos e não são mais enumerados pelas funções da área de transferência.

## <a name="memory-and-the-clipboard"></a>Memória e Área de Transferência

Um objeto de memória que deve ser colocado na área de transferência deve ser alocado usando a função [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) com o **sinalizador GMEM \_ MOVEABLE.**

Depois que um objeto de memória é colocado na área de transferência, a propriedade desse identificador de memória é transferida para o sistema. Quando a área de transferência é esvaziada e o objeto de memória tem um dos seguintes formatos de área de transferência, o sistema libera o objeto de memória chamando a função especificada:



| Função para liberar o objeto                             | Formato da área de transferência                                                                                                                                               |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Deletemetafile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile)<br/> | **CF \_ DSPEN LTDAFILE**<br/> **CF \_ DSPMETAFILEPICT**<br/> **CF \_ EN LTDAFILE**<br/> **CF \_ METAFILEPICT**<br/>                            |
| [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)<br/>     | **BITMAP do CF \_**<br/> **CF \_ DSPBITMAP**<br/> **PALETA \_ DE CF**<br/>                                                                              |
| [**Globalfree**](/windows/desktop/api/winbase/nf-winbase-globalfree)<br/>        | **CF \_ DIB**<br/> **CF \_ DIBV5**<br/> **CF \_ DSPTEXT**<br/> **CF \_ OEMTEXT**<br/> **CF \_ TEXT**<br/> **CF \_ UNICODETEXT**<br/>   |
| nenhum<br/>                                     | **CF \_ OWNERDISPLAY**<br/> Quando a área de transferência é esvaziada de um **objeto \_ CF OWNERDISPLAY,** o próprio aplicativo deve liberar o objeto de memória.<br/> |



 

 

