---
title: Sobre os controles de barra de progresso
description: Uma barra de progresso é uma janela que um aplicativo pode usar para indicar o progresso de uma operação demorada. Ele consiste em um retângulo que é animado conforme uma operação progride.
ms.assetid: 1db7a5c9-71cd-4ebc-86b8-8159f30348fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f00c80b1f9e97cec1657fe979a19437f607251b8
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641887"
---
# <a name="about-progress-bar-controls"></a>Sobre os controles de barra de progresso

Uma barra de progresso é uma janela que um aplicativo pode usar para indicar o progresso de uma operação demorada.

Ele consiste em um retângulo que é animado conforme uma operação progride.

A ilustração a seguir mostra uma barra de progresso que não usa estilos visuais.

![captura de tela de uma barra de progresso que adiciona retângulos em uma linha para indicar o progresso](images/pb-oldstyle.png)

A ilustração a seguir mostra uma barra de progresso usando estilos visuais. A aparência do controle irá variar dependendo do sistema operacional e do tema selecionado. Para obter mais informações, consulte [Visual Styles](themes-overview.md).

![captura de tela de uma barra de progresso que aumenta um retângulo verde animado para indicar o progresso](images/pb-newstyle.png)

Mais informações estão contidas nos seguintes cabeçalhos.

-   [Usando barras de progresso](#using-progress-bars)
    -   [Intervalo e posição atual](#range-and-current-position)
    -   [Processamento de mensagens da barra de progresso padrão](#default-progress-bar-message-processing)
    -   [Estilo do letreiro](#marquee-style)

## <a name="using-progress-bars"></a>Usando barras de progresso

Você pode criar uma barra de progresso usando a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando a classe de janela de [**\_ classe Progress**](common-control-window-classes.md) . Essa classe de janela é registrada quando a DLL de controles comuns é carregada. Para obter mais informações, consulte [sobre controles comuns](common-controls-intro.md).

O controle também está disponível na caixa de ferramentas Microsoft Visual Studio, onde é chamado de controle de progresso.

### <a name="range-and-current-position"></a>Intervalo e posição atual

O *intervalo* de uma barra de progresso representa a duração total da operação e a *posição atual* representa o progresso que o aplicativo fez para concluir a operação. O procedimento de janela usa o intervalo e a posição atual para determinar a porcentagem da barra de progresso a ser preenchida com a cor de realce.

Se você não definir os valores de intervalo, o sistema definirá o valor mínimo como 0 e o valor máximo como 100. Você pode ajustar o intervalo para inteiros convenientes usando a mensagem [**\_ SETRANGE do PBM**](pbm-setrange.md) .

Uma barra de progresso fornece várias mensagens que você pode usar para definir a posição atual. A [**mensagem \_ SETPOS do PBM**](pbm-setpos.md) define a posição para um determinado valor. A [**mensagem \_ DELTAPOS do PBM**](pbm-deltapos.md) avança a posição adicionando um valor especificado à posição atual.

A mensagem do [**PBM \_ SetStep**](pbm-setstep.md) permite especificar um incremento de etapa para uma barra de progresso. Subsequentemente, sempre que você enviar a mensagem [**\_ STEPIT do PBM**](pbm-stepit.md) para a barra de progresso, a posição atual avança pelo incremento especificado. Por padrão, o incremento Step é definido como 10.

### <a name="default-progress-bar-message-processing"></a>Processamento de mensagens da barra de progresso padrão

Esta seção descreve as mensagens tratadas pelo procedimento de janela para a classe de [**\_ classe Progress**](common-control-window-classes.md) .



| Mensagem            | Processamento realizado                                                                                                                                                               |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **criação do WM \_**     | Aloca e Inicializa uma estrutura inicial.                                                                                                                                    |
| **destruição do WM \_**    | Libera todos os recursos associados à barra de progresso.                                                                                                                              |
| **ERASEBKGND do WM \_** | Desenha o plano de fundo e as bordas da barra de progresso.                                                                                                                              |
| **WM \_ GETfont**    | Retorna o identificador para a fonte atual. No momento, a barra de progresso não Desenha texto, portanto, o envio desta mensagem não tem nenhum efeito sobre o controle.                                       |
| **pintura do WM \_**      | Desenha a barra de progresso. Se o parâmetro *wParam* for não **nulo**, o controle assumirá que o valor é um hDC e pinta usando esse contexto de dispositivo.                              |
| **WM \_ SETfont**    | Salva o identificador para a nova fonte e retorna o identificador para a fonte anterior. No momento, a barra de progresso não Desenha texto, portanto, o envio desta mensagem não tem nenhum efeito sobre o controle. |



 

### <a name="marquee-style"></a>Estilo do letreiro

Ao criar o controle de barra de progresso com o estilo de [**\_ letreiro do PBS**](progress-bar-control-styles.md) , você pode animá-lo de uma maneira que mostra a atividade, mas não indica a proporção da tarefa concluída. A parte realçada da barra de progresso é movida repetidamente ao longo do comprimento da barra. Você pode iniciar e parar a animação e controlar sua velocidade, enviando a mensagem [**\_ setmarquee do PBM**](pbm-setmarquee.md) . As barras de progresso do letreiro não têm um intervalo ou posição.

A ilustração a seguir mostra uma barra de progresso no modo de letreiro. A parte realçada se move pela barra.

![captura de tela de uma barra de progresso que move um realce verde em um retângulo cinza para indicar o progresso](images/pb-marquee.png)

 

 