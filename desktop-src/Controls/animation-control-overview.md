---
title: Sobre os controles de animação
description: Um controle de animação é uma janela que exibe um clipe AVI (intercalado Audio-Video). Um clipe AVI é uma série de quadros de bitmap como um filme. Os controles de animação só podem exibir clipes AVI que não contenham áudio.
ms.assetid: 6be69d1a-5b2c-41d5-b6d7-e86ddac2cb0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1625828e5f4febce7314da365c9db93ce3a07136
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105769036"
---
# <a name="about-animation-controls"></a>Sobre os controles de animação

Um *controle de animação* é uma janela que exibe um clipe AVI (intercalado Audio-Video). Um clipe AVI é uma série de quadros de bitmap como um filme. Os controles de animação só podem exibir clipes AVI que não contenham áudio.

Um uso comum para um controle de animação é indicar a atividade do sistema durante uma operação demorada. Isso é possível porque o thread de operação continua em execução enquanto o clipe AVI é exibido. Por exemplo, a caixa de diálogo Localizar do Windows Explorer exibe uma lupa de movimentação à medida que o sistema procura um arquivo.

> [!Note]  
> Se você estiver usando ComCtl32.dll versão 6, o thread não terá suporte; Verifique se o aplicativo não bloqueia a interface do usuário ou se a animação não ocorrerá.

 

Um controle de animação pode exibir um clipe AVI originado de um arquivo AVI descompactado ou de um arquivo AVI que foi compactado usando a codificação de tamanho de execução (BI \_ RLE8). Você pode adicionar o clipe AVI ao seu aplicativo como um recurso AVI ou o clipe pode acompanhar seu aplicativo como um arquivo AVI separado.

> [!Note]  
> O arquivo AVI ou recurso não deve ter um canal de som. Os recursos do controle de animação são muito limitados e estão sujeitos a alterações. Se você precisar de um controle para fornecer recursos de reprodução e gravação de multimídia para seu aplicativo, poderá usar o controle MCIWnd. Para obter mais informações, consulte [classe de janela MCIWnd](/windows/desktop/Multimedia/mciwnd-window-class).

 

Esta seção aborda os tópicos a seguir.

-   [Criação de controle de animação](#animation-control-creation)
-   [Sobre as mensagens de controle de animação](#about-animation-control-messages)
-   [Processamento de mensagens padrão](#default-message-processing)

## <a name="animation-control-creation"></a>Criação de controle de animação

Um controle de animação pertence à classe de janela de [**\_ classe Animate**](common-control-window-classes.md) . Você cria um controle de animação usando a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou a macro [**anima \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) . A macro posiciona o controle de animação no canto superior esquerdo da janela pai e, se o estilo do [**\_ centro do ACS**](animation-control-styles.md) não for especificado, define a largura e a altura do controle com base nas dimensões de um quadro no clipe AVI. Se o **ACS \_ Center** for especificado, a **\_ criação de animação** definirá a largura e a altura do controle como zero. Você pode usar a função [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para definir a posição e o tamanho do controle.

Se você criar um controle de animação dentro de uma caixa de diálogo ou de um recurso da caixa de diálogo, o controle será destruído automaticamente quando o usuário fechar a caixa de diálogo. Se você criar um controle de animação dentro de uma janela, deverá destruir explicitamente o controle.

## <a name="about-animation-control-messages"></a>Sobre as mensagens de controle de animação

Um aplicativo envia mensagens a um controle de animação para abrir, reproduzir, parar e fechar o clipe AVI correspondente. Cada mensagem tem uma ou mais macros que você pode usar em vez de enviar a mensagem explicitamente.

Depois de criar um controle de animação, um aplicativo envia a mensagem [**\_ aberta do ACM**](acm-open.md) para abrir um clipe AVI e carregá-lo na memória. A mensagem Especifica o caminho de um arquivo AVI ou o nome de um recurso AVI. O sistema carrega o recurso AVI do módulo que criou o controle de animação.

Se o controle de animação tiver o estilo de [**\_ reprodução automática do ACS**](animation-control-styles.md) , o controle começará a tocar o clipe AVI imediatamente depois que o arquivo AVI ou o recurso AVI for aberto. Caso contrário, um aplicativo poderá usar a mensagem de [**\_ reprodução do ACM**](acm-play.md) para iniciar o clipe AVI. Um aplicativo pode parar o clipe a qualquer momento enviando a mensagem [**de \_ parada do ACM**](acm-stop.md) . O último quadro reproduzido permanece exibido quando o controle termina de reproduzir o clipe AVI ou quando a **\_ parada do ACM** é enviada.

Um controle de animação pode enviar dois códigos de notificação para sua janela pai: [ACN \_ Start](acn-start.md) e [ACN \_ Stop](acn-stop.md). A maioria dos aplicativos não lidam com nenhuma notificação.

Para fechar o arquivo AVI ou o recurso AVI e removê-lo da memória, um aplicativo pode usar a macro [**animar \_ fechar**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) , que envia o [**ACM \_ Open**](acm-open.md) com o nome do arquivo ou o nome do recurso definido como **NULL**.

## <a name="default-message-processing"></a>Processamento de mensagens padrão

Esta seção descreve as mensagens de janela tratadas pelo procedimento de janela para a classe de janela [**animar \_ classe**](common-control-window-classes.md) .



| Mensagem                                    | Processamento realizado                                                                                                                                                                                                                                                                        |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**fechar o WM \_**](/windows/desktop/winmsg/wm-close)           | Libera o arquivo AVI ou o recurso AVI associado ao controle de animação.                                                                                                                                                                                                                   |
| [**destruição do WM \_**](/windows/desktop/winmsg/wm-destroy)       | Libera o arquivo AVI ou o recurso AVI, libera uma estrutura de dados interna e, em seguida, chama a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .                                                                                                                                                |
| [**ERASEBKGND do WM \_**](/windows/desktop/winmsg/wm-erasebkgnd) | Apaga o plano de fundo da janela usando a cor de plano de fundo atual para controles estáticos.                                                                                                                                                                                                        |
| [**NCCREATE do WM \_**](/windows/desktop/winmsg/wm-nccreate)     | Aloca e Inicializa uma estrutura de dados interna e, em seguida, chama [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).                                                                                                                                                                              |
| [**NCHITTEST do WM \_**](/windows/desktop/inputdev/wm-nchittest) | Retorna o valor do teste de clique HTTRANSPARENT.                                                                                                                                                                                                                                                   |
| [**pintura do WM \_**](/windows/desktop/gdi/wm-paint)              | Desenha um quadro AVI no controle de animação.                                                                                                                                                                                                                                                |
| [**tamanho do WM \_**](/windows/desktop/winmsg/wm-size)             | Verifica se o controle tem o estilo do [**\_ Centro ACS**](animation-control-styles.md) . Se o controle não tiver, ele chamará [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). Caso contrário, ele centraliza a animação no controle, invalida o controle e, em seguida, chama **DefWindowProc**. |



 

 

 