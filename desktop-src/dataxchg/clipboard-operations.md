---
title: Operações da área de transferência
description: Uma janela deve usar a área de transferência ao recortar, copiar ou colar dados. Uma janela coloca dados na área de transferência para operações de recortar e copiar e recupera dados da área de transferência para operações de colagem.
ms.assetid: 27f9142c-3154-4de5-aea6-3c53f7e940ec
keywords:
- Interface do usuário do Windows, área de transferência
- área de transferência, Windows
- área de transferência, recortando dados
- área de transferência, copiando dados
- área de transferência, colando dados
- área de transferência, janela do proprietário
- área de transferência, renderização atrasada
- área de transferência, memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cb2c3451cf562b35b976e137a974e19892acbb3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294419"
---
# <a name="clipboard-operations"></a>Operações da área de transferência

Uma janela deve usar a área de transferência ao recortar, copiar ou colar dados. Uma janela coloca dados na área de transferência para operações de recortar e copiar e recupera dados da área de transferência para operações de colagem. As seções a seguir descrevem essas operações e problemas relacionados.

Para inserir dados ou recuperar dados da área de transferência, uma janela deve primeiro abrir a área de transferência usando a função [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) . Somente uma janela pode ter a área de transferência aberta por vez. Para descobrir qual janela tem a área de transferência aberta, chame a função [**GetOpenClipboardWindow**](/windows/desktop/api/Winuser/nf-winuser-getopenclipboardwindow) . Quando tiver terminado, a janela deverá fechar a área de transferência chamando a função [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) .

Os tópicos a seguir são discutidos nesta seção.

-   [Operações de recortar e copiar](#cut-and-copy-operations)
-   [Operações de colagem](#paste-operations)
-   [Propriedade da área de transferência](#clipboard-ownership)
-   [Renderização atrasada](#delayed-rendering)
-   [Memória e área de transferência](#memory-and-the-clipboard)

## <a name="cut-and-copy-operations"></a>Operações de recortar e copiar

Para inserir informações na área de transferência, uma janela primeiro limpa qualquer conteúdo da área de transferência anterior usando a função [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) . Essa função envia a mensagem do [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) para o proprietário anterior da área de transferência, libera recursos associados aos dados na área de transferência e atribui a propriedade da área de transferência à janela que tem a área de transferência aberta. Para descobrir qual janela é proprietária da área de transferência, chame a função [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) .

Depois de esvaziar a área de transferência, a janela coloca os dados na área de transferência em quantos formatos de área de transferência forem possíveis, ordenados do formato de área de transferência mais descritivo para o menos descritivo. Para cada formato, a janela chama a função [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) , especificando o identificador de formato e um identificador de memória global. O identificador de memória pode ser nulo, indicando que a janela renderiza os dados na solicitação. Para obter mais informações, consulte [processamento atrasado](#delayed-rendering).

## <a name="paste-operations"></a>Operações de colagem

Para recuperar informações de colagem da área de transferência, uma janela determina primeiro o formato da área de transferência a ser recuperada. Normalmente, uma janela enumera os formatos de área de transferência disponíveis usando a função [**EnumClipboardFormats**](/windows/desktop/api/Winuser/nf-winuser-enumclipboardformats) e usa o primeiro formato que ele reconhece. Esse método seleciona o melhor formato disponível de acordo com o conjunto de prioridade quando os dados foram colocados na área de transferência.

Como alternativa, uma janela pode usar a função [**GetPriorityClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-getpriorityclipboardformat) . Essa função identifica o melhor formato de área de transferência disponível de acordo com uma prioridade especificada. Uma janela que reconhece apenas um formato de área de transferência pode simplesmente determinar se esse formato está disponível usando a função [**IsClipboardFormatAvailable**](/windows/desktop/api/Winuser/nf-winuser-isclipboardformatavailable) .

Depois de determinar o formato da área de transferência a ser usado, uma janela chama a função [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) . Essa função retorna o identificador para um objeto de memória global que contém dados no formato especificado. Uma janela pode bloquear brevemente o objeto de memória para examinar ou copiar os dados. No entanto, uma janela não deve liberar o objeto ou deixá-lo bloqueado por um longo período de tempo.

## <a name="clipboard-ownership"></a>Propriedade da área de transferência

O *proprietário da área de transferência* é a janela associada às informações na área de transferência. Uma janela torna-se o proprietário da área de transferência quando coloca dados na área de transferência, especificamente, quando chama a função [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) . A janela permanece o proprietário da área de transferência até que seja fechada ou outra janela esvazia a área de transferência.

Quando a área de transferência é esvaziada, o proprietário da área de transferência recebe uma mensagem do [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) . A seguir estão alguns motivos pelos quais uma janela pode processar esta mensagem:

-   A janela de renderização atrasada de um ou mais formatos de área de transferência. Em resposta à mensagem do [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) , a janela pode liberar recursos alocados para processar dados na solicitação. Para obter mais informações sobre a renderização de dados, consulte [processamento atrasado](#delayed-rendering).
-   A janela colocou dados na área de transferência em um formato de área de transferência particular. Os dados para formatos de área de transferência privada não são liberados pelo sistema quando a área de transferência é esvaziada. Portanto, o proprietário da área de transferência deve liberar os dados após receber a mensagem [**\_ DESTROYCLIPBOARD do WM**](wm-destroyclipboard.md) . Para obter mais informações sobre formatos de área de transferência privada, consulte [formatos de área de transferência](clipboard-formats.md).
-   A janela colocou dados na área de transferência usando o formato de área de transferência do **CF \_ OWNERDISPLAY** . Em resposta à mensagem do [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) , a janela pode liberar recursos que usavam para exibir informações na janela do Visualizador da área de transferência. Para obter mais informações sobre esse formato alternativo, consulte o [formato de exibição do proprietário](about-the-clipboard.md).

## <a name="delayed-rendering"></a>Renderização atrasada

Ao colocar um formato de área de transferência na área de transferência, uma janela pode atrasar o processamento dos dados nesse formato até que os dados sejam necessários. Para fazer isso, um aplicativo pode especificar **NULL** para o parâmetro *HData* da função [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) . Isso é útil se o aplicativo dá suporte a vários formatos de área de transferência, alguns ou todos os que estão demorando para renderizar. Ao passar um identificador **nulo** , uma janela renderiza formatos de área de transferência complexos somente quando e se forem necessários.

Se uma janela atrasar o processamento de um formato de área de transferência, ela deverá estar preparada para renderizar o formato mediante solicitação, desde que seja o proprietário da área de transferência. O sistema envia ao proprietário da área de transferência uma mensagem do [**WM \_ RENDERFORMAT**](wm-renderformat.md) quando uma solicitação é recebida para um formato específico que não foi renderizado. Após receber essa mensagem, a janela deve chamar a função [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) para posicionar um identificador de memória global na área de transferência no formato solicitado.

Um aplicativo não deve abrir a área de transferência antes de chamar [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) em resposta à mensagem do [**WM \_ RENDERFORMAT**](wm-renderformat.md) . A abertura da área de transferência não é necessária e qualquer tentativa de fazer isso falhará porque a área de transferência está sendo mantida aberta pelo aplicativo que solicitou o formato a ser renderizado.

Se o proprietário da área de transferência estiver prestes a ser destruído e tiver atrasado processamento de alguns ou de todos os formatos da área de transferência, ele receberá a mensagem [**\_ RENDERALLFORMATS do WM**](wm-renderallformats.md) . Ao receber essa mensagem, a janela deve abrir a área de transferência, verifique se ela ainda é o proprietário da área de transferência com a função [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) e coloque identificadores de memória válidos na área de transferência para todos os formatos de área de transferência que ele fornece. Isso garante que esses formatos permaneçam disponíveis depois que o proprietário da área de transferência for destruído.

Ao contrário do [**WM \_ RENDERFORMAT**](wm-renderformat.md), um aplicativo respondendo ao [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) deve abrir a área de transferência antes de chamar [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) para inserir qualquer identificador de memória global na área de transferência.

Todos os formatos da área de transferência que não são renderizados em resposta à mensagem do [**WM \_ RENDERALLFORMATS**](wm-renderallformats.md) deixam de estar disponíveis para outros aplicativos e não são mais enumerados pelas funções da área de transferência.

## <a name="memory-and-the-clipboard"></a>Memória e área de transferência

Um objeto de memória a ser colocado na área de transferência deve ser alocado usando a função [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) com o sinalizador **GMEMable \_** .

Depois que um objeto de memória é colocado na área de transferência, a propriedade desse identificador de memória é transferida para o sistema. Quando a área de transferência é esvaziada e o objeto de memória tem um dos seguintes formatos de área de transferência, o sistema libera o objeto de memória chamando a função especificada:



| Função para objeto livre                             | Formato da área de transferência                                                                                                                                               |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile)<br/> | **\_DSPENHMETAFILE CF**<br/> **\_DSPMETAFILEPICT CF**<br/> **\_ENHMETAFILE CF**<br/> **\_METAFILEPICT CF**<br/>                            |
| [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)<br/>     | **BITMAP do CF \_**<br/> **\_DSPBITMAP CF**<br/> **paleta do CF \_**<br/>                                                                              |
| [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree)<br/>        | **DIB do CF \_**<br/> **\_DIBV5 CF**<br/> **\_DSPTEXT CF**<br/> **\_OEMTEXT CF**<br/> **texto do CF \_**<br/> **\_UNICODETEXT CF**<br/>   |
| none<br/>                                     | **\_OWNERDISPLAY CF**<br/> Quando a área de transferência é esvaziada de um objeto **CF \_ OWNERDISPLAY** , o próprio aplicativo deve liberar o objeto de memória.<br/> |



 

 

