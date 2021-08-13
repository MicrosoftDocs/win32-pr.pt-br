---
title: Sobre caixas de diálogo
description: Este tópico discute o uso de caixas de diálogo para criar interfaces de usuário para aplicativos.
ms.assetid: 51960c28-a178-4ad3-b45e-426fec42a945
keywords:
- caixas de diálogo, sobre
- caixas de diálogo, quando usar
- caixas de diálogo modais
- caixas de diálogo sem modo
- caixas de diálogo, modal
- caixas de diálogo, sem janela restrita
- caixas de diálogo, modelos
- caixas de diálogo, janelas de proprietário
- caixas de diálogo, caixas de mensagem
- procedimentos da caixa de diálogo
- caixas de mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7855ba67a04558e0df8ffad0f63d2bd78856f84829bf029fbf811a4b89eb4b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786804"
---
# <a name="about-dialog-boxes"></a>Sobre caixas de diálogo

Há muitas funções, mensagens e controles predefinidos para ajudar a criar e gerenciar caixas de diálogo, facilitando o desenvolvimento da interface do usuário para um aplicativo. Esta visão geral descreve as funções e mensagens da caixa de diálogo e explica como usá-las para criar e usar caixas de diálogo.

Esta visão geral inclui os seguintes tópicos:

-   [Quando usar uma caixa de diálogo](#when-to-use-a-dialog-box)
-   [Janela do proprietário da caixa de diálogo](#dialog-box-owner-window)
-   [Caixas de mensagem](#message-boxes)
-   [Caixas de diálogo modais](#modal-dialog-boxes)
-   [Caixas de diálogo sem janela restrita](#modeless-dialog-boxes)
-   [Modelos de caixa de diálogo](#dialog-box-templates)
    -   [Estilos de modelo de caixa de diálogo](#dialog-box-template-styles)
    -   [Medidas da caixa de diálogo](#dialog-box-measurements)
    -   [Controles da caixa de diálogo](#dialog-box-controls)
    -   [Menu da janela da caixa de diálogo](#dialog-box-window-menu)
    -   [Fontes da caixa de diálogo](#dialog-box-fonts)
    -   [Modelos na memória](#templates-in-memory)

Para obter mais informações sobre as caixas de diálogo comuns, consulte [biblioteca de caixa de diálogo comum](common-dialog-box-library.md).

## <a name="when-to-use-a-dialog-box"></a>Quando usar uma caixa de diálogo

A maioria dos aplicativos usa caixas de diálogo para solicitar informações adicionais para itens de menu que exigem entrada do usuário. Usar uma caixa de diálogo é a única maneira recomendada para um aplicativo recuperar a entrada. Por exemplo, um item de menu **aberto** típico requer o nome de um arquivo a ser aberto e, portanto, um aplicativo deve usar uma caixa de diálogo para solicitar ao usuário o nome. Nesses casos, o aplicativo cria a caixa de diálogo quando o usuário clica no item de menu e destrói a caixa de diálogo imediatamente após o usuário fornecer as informações.

Muitos aplicativos também usam caixas de diálogo para exibir informações ou opções enquanto o usuário trabalha em outra janela. Por exemplo, aplicativos de processamento de texto geralmente usam uma caixa de diálogo com uma opção de pesquisa de textos. Enquanto o aplicativo procura o texto, a caixa de diálogo permanece na tela. O usuário pode retornar à caixa de diálogo e pesquisar a mesma palavra novamente; ou o usuário pode alterar a entrada na caixa de diálogo e procurar uma nova palavra. Os aplicativos que usam caixas de diálogo dessa maneira normalmente criam um quando o usuário clica no item de menu e continua a exibi-lo enquanto o aplicativo é executado ou até que o usuário feche explicitamente a caixa de diálogo.

Para dar suporte às diferentes maneiras como os aplicativos usam caixas de diálogo, há dois tipos de caixa de diálogo: modal e sem janela restrita. Uma *caixa de diálogo modal* exige que o usuário forneça informações ou cancele a caixa de diálogo antes de permitir que o aplicativo continue. Os aplicativos usam caixas de diálogo modais em conjunto com itens de menu que exigem informações adicionais antes que possam continuar. Uma *caixa de diálogo sem janela restrita* permite que o usuário forneça informações e retorne à tarefa anterior sem fechar a caixa de diálogo. As caixas de diálogo modais são mais simples de gerenciar do que as caixas de diálogo sem janela restritas, pois são criadas, executam suas tarefas e são destruídas chamando uma única função.

Para criar uma caixa de diálogo modal ou sem janela restrita, um aplicativo deve fornecer um modelo de caixa de diálogo para descrever o estilo e o conteúdo da caixa de diálogo; o aplicativo também deve fornecer um procedimento de caixa de diálogo para executar tarefas. O *modelo de caixa de diálogo* é uma descrição binária da caixa de diálogo e os controles que ela contém. O desenvolvedor pode criar esse modelo como um recurso a ser carregado do arquivo executável do aplicativo ou criado na memória enquanto o aplicativo é executado. O *procedimento da caixa de diálogo* é uma função de retorno de chamada definida pelo aplicativo que o sistema chama quando tem entrada para a caixa de diálogo ou tarefas para a caixa de diálogo Executar. Embora um procedimento de caixa de diálogo seja semelhante a um procedimento de janela, ele não tem as mesmas responsabilidades.

Um aplicativo normalmente cria uma caixa de diálogo usando a função [**caixa**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) ou [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) . **Caixa** cria uma caixa de diálogo modal; **CreateDialog** cria uma caixa de diálogo sem janela restrita. Essas duas funções carregam um modelo de caixa de diálogo do arquivo executável do aplicativo e criam uma janela pop-up que corresponde às especificações do modelo. Há outras funções que criam uma caixa de diálogo usando modelos na memória; Eles passam informações adicionais para o procedimento da caixa de diálogo, pois a caixa de diálogo é criada.

As caixas de diálogo geralmente pertencem a uma classe de janela predefinida e exclusiva. O sistema usa essa classe de janela e seu procedimento de janela correspondente para caixas de diálogo modais e sem janela restrita. Quando a função é chamada, ela cria a janela da caixa de diálogo, bem como as janelas dos controles na caixa de diálogo e, em seguida, envia as mensagens selecionadas para o procedimento da caixa de diálogo. Enquanto a caixa de diálogo estiver visível, o procedimento de janela predefinido gerenciará todas as mensagens, processando algumas mensagens e passando outras para o procedimento da caixa de diálogo para que o procedimento possa executar tarefas. Os aplicativos não têm acesso direto à classe de janela predefinida ou ao procedimento de janela, mas podem usar o modelo de caixa de diálogo e o procedimento de caixa de diálogo para modificar o estilo e o comportamento de uma caixa de diálogo.

## <a name="dialog-box-owner-window"></a>Janela do proprietário da caixa de diálogo

A maioria das caixas de diálogo tem uma janela do proprietário (ou mais simplesmente, um proprietário). Ao criar a caixa de diálogo, o aplicativo define o proprietário especificando o identificador de janela do proprietário. O sistema usa o proprietário para determinar a posição da caixa de diálogo na ordem Z para que a caixa de diálogo sempre esteja posicionada acima do seu proprietário. Além disso, o sistema pode enviar mensagens para o procedimento de janela do proprietário, notificando-os sobre eventos na caixa de diálogo.

O sistema oculta ou destrói automaticamente a caixa de diálogo sempre que seu proprietário é ocultado ou destruído. Isso significa que o procedimento da caixa de diálogo não requer processamento especial para detectar alterações no estado da janela do proprietário.

Como a caixa de diálogo típica é usada em conjunto com um item de menu, a janela do proprietário geralmente é a janela que contém o menu. Embora seja possível criar uma caixa de diálogo sem proprietário, não é recomendável. Por exemplo, quando uma caixa de diálogo modal não tem proprietário, o sistema não desabilita nenhuma das outras janelas do aplicativo e permite que o usuário continue a realizar o trabalho nas outras janelas, derrotando a finalidade da caixa de diálogo modal.

Quando uma caixa de diálogo sem janela restrita não tem proprietário, o sistema não oculta nem destrói a caixa de diálogo quando outras janelas no aplicativo são ocultas ou destruídas. Embora isso não expire a finalidade da caixa de diálogo sem janela restrita, ele requer que o aplicativo execute o processamento especial para garantir que a caixa de diálogo esteja oculta e destruída em momentos apropriados.

## <a name="message-boxes"></a>Caixas de mensagem

Uma caixa de mensagem é uma caixa de diálogo especial que um aplicativo pode usar para exibir mensagens e solicitar uma entrada simples. Uma caixa de mensagem normalmente contém uma mensagem de texto e um ou mais botões. Um aplicativo cria a caixa de mensagem usando a função [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) ou [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) , especificando o texto e o número e os tipos de botões a serem exibidos. Observe que, no momento, não há nenhuma diferença entre como **MessageBox** e **MessageBoxEx** funcionam.

Embora a caixa de mensagem seja uma caixa de diálogo, o sistema assume o controle total da criação e do gerenciamento da caixa de mensagem. Isso significa que o aplicativo não fornece um procedimento de caixa de diálogo e de caixa de diálogo. O sistema cria seu próprio modelo com base no texto e nos botões especificados para a caixa de mensagem e fornece seu próprio procedimento de caixa de diálogo.

Uma caixa de mensagem é uma caixa de diálogo modal e o sistema a cria usando as mesmas funções internas que o [**caixa**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) usa. Se o aplicativo especificar uma janela de proprietário ao chamar [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) ou [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa), o sistema desabilitará o proprietário. Um aplicativo também pode direcionar o sistema para desabilitar todas as janelas de nível superior que pertencem ao thread atual, especificando o valor de **MB \_ TASKMODAL** ao criar a caixa de diálogo.

O sistema pode enviar mensagens para o proprietário, como o [**WM \_ CancelMode**](/windows/desktop/winmsg/wm-cancelmode) e o [**WM \_ Enable**](/windows/desktop/winmsg/wm-enable), assim como faz ao criar uma caixa de diálogo modal. A janela do proprietário deve executar todas as ações solicitadas por essas mensagens.

## <a name="modal-dialog-boxes"></a>Caixas de diálogo modais

Uma caixa de diálogo modal deve ser uma janela pop-up com um menu janela, uma barra de título e uma borda espessa; ou seja, o modelo de caixa de diálogo deve especificar os estilos **WS \_ -up**, **WS \_ SYSMENU**, **WS \_ Caption** e **DS \_ MODALFRAME** . Embora um aplicativo possa designar o estilo do **WS \_ Visible** , o sistema sempre exibe uma caixa de diálogo modal, independentemente de o modelo da caixa de diálogo especificar o estilo do **WS \_ Visible** . Um aplicativo não deve criar uma caixa de diálogo modal com o estilo **WS \_ filho** . Uma caixa de diálogo modal com esse estilo se desabilita, impedindo que qualquer entrada subsequente atinja o aplicativo.

Um aplicativo cria uma caixa de diálogo modal usando a função [**caixa**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) ou [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) . **Caixa** requer o nome ou o identificador de um recurso que contém um modelo de caixa de diálogo; **DialogBoxIndirect** requer um identificador para um objeto de memória que contém um modelo de caixa de diálogo. As funções [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) e [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama) também criam caixas de diálogo modais; Eles são idênticos às funções mencionadas anteriormente, mas passam um parâmetro especificado para o procedimento da caixa de diálogo quando a caixa de diálogo é criada.

Ao criar a caixa de diálogo modal, o sistema a torna a janela ativa. A caixa de diálogo permanece ativa até que o procedimento da caixa de diálogo chame a função [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) ou o sistema Ative uma janela em outro aplicativo. Nem o usuário nem o aplicativo podem tornar a janela do proprietário ativa até que a caixa de diálogo modal seja destruída.

Quando a janela do proprietário ainda não está desabilitada, o sistema desabilita automaticamente a janela e todas as janelas filhas que pertencem a ela quando ele cria a caixa de diálogo modal. A janela do proprietário permanece desabilitada até que a caixa de diálogo seja destruída. Embora um procedimento de caixa de diálogo possa potencialmente habilitar a janela do proprietário a qualquer momento, a habilitação do proprietário anula a finalidade da caixa de diálogo modal e não é recomendada. Quando o procedimento da caixa de diálogo é destruído, o sistema habilita a janela do proprietário novamente, mas somente se a caixa de diálogo modal fez com que o proprietário fosse desabilitado.

À medida que o sistema cria a caixa de diálogo modal, ele envia a mensagem do [**WM \_ cancelable**](/windows/desktop/winmsg/wm-cancelmode) para a janela (se houver) atualmente capturando a entrada do mouse. Um aplicativo que recebe essa mensagem deve liberar a captura do mouse para que o usuário possa mover o mouse na caixa de diálogo modal. Como o sistema desabilita a janela do proprietário, toda a entrada do mouse será perdida se o proprietário não conseguir liberar o mouse após receber essa mensagem.

Para processar mensagens para a caixa de diálogo modal, o sistema inicia seu próprio loop de mensagem, assumindo o controle temporário da fila de mensagens para todo o aplicativo. Quando o sistema recupera uma mensagem que não é explicitamente para a caixa de diálogo, ele despacha a mensagem para a janela apropriada. Se ele recuperar uma mensagem do [**WM \_ Quit**](/windows/desktop/winmsg/wm-quit) , ele envia a mensagem de volta para a fila de mensagens do aplicativo para que o loop de mensagem principal do aplicativo possa eventualmente recuperar a mensagem.

O sistema envia a mensagem do [**WM \_ ENTERIDLE**](wm-enteridle.md) para a janela do proprietário sempre que a fila de mensagens do aplicativo estiver vazia. O aplicativo pode usar essa mensagem para executar uma tarefa em segundo plano enquanto a caixa de diálogo permanece na tela. Quando um aplicativo usa a mensagem dessa forma, o aplicativo sempre deve produzir controle (por exemplo, usando a função [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) ) para que a caixa de diálogo modal possa receber qualquer entrada do usuário. Para impedir que a caixa de diálogo modal envie as mensagens **\_ ENTERIDLE do WM** , o aplicativo pode especificar o estilo de NOIDLEMSG do DS \_ ao criar a caixa de diálogo.

Um aplicativo destrói uma caixa de diálogo modal usando a função [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) . Na maioria dos casos, o procedimento da caixa de diálogo chama **EndDialog** quando o usuário clica em **fechar** no menu da janela da caixa de diálogo ou clica no botão **OK** ou **Cancelar** na caixa de diálogo. A caixa de diálogo pode retornar um valor por meio da função [**caixa**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) (ou outras funções de criação), especificando um valor ao chamar a função **EndDialog** . O sistema retorna esse valor depois de destruir a caixa de diálogo. A maioria dos aplicativos usa esse valor de retorno para determinar se a caixa de diálogo concluiu sua tarefa com êxito ou foi cancelada pelo usuário. O sistema não retorna o controle da função que cria a caixa de diálogo até que o procedimento da caixa de diálogo tenha chamado a função **EndDialog** .

## <a name="modeless-dialog-boxes"></a>Caixas de diálogo sem janela restrita

Uma caixa de diálogo sem janela restrita deve ser uma janela pop-up com um menu de janela, uma barra de título e uma borda fina; ou seja, o modelo de caixa de diálogo deve especificar os estilos **WS \_ -up**, **WS \_ Caption**, **WS \_ Border** e **WS \_ SYSMENU** . O sistema não exibe automaticamente a caixa de diálogo, a menos que o modelo especifique o estilo de **WS \_ Visible** .

Um aplicativo cria uma caixa de diálogo sem janela restrita usando a função [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) ou [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta) . **CreateDialog** exige o nome ou o identificador de um recurso que contém um modelo de caixa de diálogo; **CreateDialogIndirect** requer um identificador para um objeto de memória que contém um modelo de caixa de diálogo. Duas outras funções, [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama) e [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), também criam caixas de diálogo sem janela restrita; Eles passam um parâmetro especificado para o procedimento da caixa de diálogo quando a caixa de diálogo é criada.

[**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) e outras funções de criação retornam um identificador de janela para a caixa de diálogo. O aplicativo e o procedimento da caixa de diálogo podem usar esse identificador para gerenciar a caixa de diálogo. Por exemplo, se o **WS \_ Visible** não for especificado no modelo da caixa de diálogo, o aplicativo poderá exibir a caixa de diálogo passando o identificador de janela para a função de [**janela**](/windows/desktop/api/winuser/nf-winuser-showwindow) .

Uma caixa de diálogo sem janela restrita não desabilita a janela do proprietário nem envia mensagens a ela. Ao criar a caixa de diálogo, o sistema a torna a janela ativa, mas o usuário ou o aplicativo pode alterar a janela ativa a qualquer momento. Se a caixa de diálogo se tornar inativa, ela permanecerá acima da janela do proprietário na ordem Z, mesmo que a janela do proprietário esteja ativa.

O aplicativo é responsável por recuperar e expedir mensagens de entrada para a caixa de diálogo. A maioria dos aplicativos usa o loop de mensagem principal para isso. Para permitir que o usuário vá para e selecione controles usando o teclado, no entanto, o aplicativo deve chamar a função [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) . Para obter mais informações sobre essa função, consulte [interface de teclado da caixa de diálogo](dlgbox-programming-considerations.md).

Uma caixa de diálogo sem janela restrita não pode retornar um valor para o aplicativo como uma caixa de diálogo modal, mas o procedimento da caixa de diálogo pode enviar informações para a janela do proprietário usando a função [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) .

Um aplicativo deve destruir todas as caixas de diálogo sem janela restrita antes de terminar. Ele pode destruir uma caixa de diálogo sem janela restrita usando a função [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) . Na maioria dos casos, o procedimento da caixa de diálogo chama **DestroyWindow** em resposta à entrada do usuário, como clicar no botão **Cancelar** . Se o usuário nunca fechar a caixa de diálogo dessa forma, o aplicativo deverá chamar **DestroyWindow**.

O [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) invalida o identificador de janela para a caixa de diálogo, portanto, todas as chamadas subsequentes para funções que usam os valores de erro de retorno de identificador. Para evitar erros, o procedimento da caixa de diálogo deve notificar o proprietário de que a caixa de diálogo foi destruída. Muitos aplicativos mantêm uma variável global que contém o identificador para a caixa de diálogo. Quando o procedimento da caixa de diálogo destrói a caixa de diálogo, ele também define a variável global como **NULL**, indicando que a caixa de diálogo não é mais válida.

O procedimento da caixa de diálogo não deve chamar a função [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) para destruir uma caixa de diálogo sem janela restrita.

## <a name="dialog-box-templates"></a>Modelos de caixa de diálogo

Um modelo de caixa de diálogo são dados binários que descrevem a caixa de diálogo, definindo sua altura, largura, estilo e os controles que ele contém. Para criar uma caixa de diálogo, o sistema carrega um modelo de caixa de diálogo dos recursos no arquivo executável do aplicativo ou usa o modelo passado para ele na memória global pelo aplicativo. Em ambos os casos, o aplicativo deve fornecer um modelo ao criar uma caixa de diálogo.

Um desenvolvedor cria recursos de modelo usando um compilador de recurso ou um editor de caixa de diálogo. Um compilador de recurso converte uma descrição de texto em um recurso binário, e um editor de caixa de diálogo salva uma caixa de diálogo construída interativamente como um recurso binário.

> [!Note]  
> Uma explicação de como criar recursos de modelo e adicioná-los ao arquivo executável do aplicativo está além do escopo desta visão geral. Para obter mais informações sobre como criar recursos de modelo e adicioná-los a um arquivo executável, consulte a documentação fornecida com as ferramentas de desenvolvimento de aplicativo.

 

Para criar uma caixa de diálogo sem usar recursos de modelo, você deve criar um modelo na memória e passá-lo para a função [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama) ou [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama) , ou para a macro [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta) ou [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) .

Um modelo de caixa de diálogo na memória consiste em um cabeçalho que descreve a caixa de diálogo, seguida por um ou mais blocos de dados adicionais que descrevem cada um dos controles na caixa de diálogo. O modelo pode usar o formato padrão ou o formato estendido. Em um modelo padrão, o cabeçalho é uma estrutura [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) seguida por matrizes de comprimento variável adicional; e os dados de cada controle consistem em uma estrutura [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) seguida por matrizes de comprimento variável adicional. Em um modelo de caixa de diálogo estendida, o cabeçalho usa o formato [**DLGTEMPLATEEX**](dlgtemplateex.md) e as definições de controle usam o formato [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) .

Você pode criar um modelo de memória alocando um objeto de memória global e preenchendo-o com as definições de controle e cabeçalho padrão ou estendido. Um modelo de memória é idêntico em forma e conteúdo a um recurso de modelo. Muitos aplicativos que usam modelos de memória primeiro usam a função [**LoadResource**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadresource) para carregar um recurso de modelo na memória e, em seguida, modifica o recurso carregado para criar um novo modelo de memória. Para obter mais informações sobre como criar um modelo de caixa de diálogo na memória, consulte [modelos na memória](#templates-in-memory).

As seções a seguir descrevem os estilos, as medidas e outros valores usados em um modelo de caixa de diálogo.

-   [Estilos de modelo de caixa de diálogo](#dialog-box-template-styles)
-   [Medidas da caixa de diálogo](#dialog-box-measurements)
-   [Controles da caixa de diálogo](#dialog-box-controls)
-   [Menu da janela da caixa de diálogo](#dialog-box-window-menu)
-   [Fontes da caixa de diálogo](#dialog-box-fonts)
-   [Modelos na memória](#templates-in-memory)

### <a name="dialog-box-template-styles"></a>Estilos de modelo de caixa de diálogo

Cada modelo de caixa de diálogo especifica uma combinação de valores de estilo que definem a aparência e os recursos da caixa de diálogo. Os valores de estilo podem ser estilos de janela, como **WS \_ Popup** e **WS \_ SYSMENU**, e estilos de caixa de diálogo, como o **DS \_ MODALFRAME**. O número e o tipo de estilos de um modelo dependem do tipo e da finalidade da caixa de diálogo. Para obter uma lista de valores, consulte [**estilos de caixa de diálogo**](dialog-box-styles.md).

O sistema passa todos os estilos de janela especificados no modelo para a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ao criar a caixa de diálogo. O sistema pode passar um ou mais estilos estendidos dependendo dos estilos de caixa de diálogo especificados. Por exemplo, quando o modelo especifica **DS \_ MODALFRAME**, o sistema usa o **WS \_ ex \_ DLGMODALFRAME** ao criar a caixa de diálogo.

A maioria das caixas de diálogo são janelas pop-up que têm um menu janela e uma barra de título. Portanto, o modelo típico especifica os estilos de **\_ legenda** **WS \_ -Popup**, **WS \_ SYSMENU** e WS. O modelo também especifica um estilo de borda: **WS \_ Border** para caixas de diálogo sem janela restrita e **\_ MODALFRAME DS** para caixas de diálogo modais. Um modelo pode especificar um tipo de janela diferente de pop-up (como **WS \_ Overlapped**) se ele criar uma janela personalizada em vez de uma caixa de diálogo.

O sistema sempre exibe uma caixa de diálogo modal, independentemente de o estilo **\_ visível WS** ser especificado. Quando o modelo de uma caixa de diálogo sem janela restrita especifica o estilo do **WS \_ Visible** , o sistema exibe automaticamente a caixa de diálogo quando ela é criada. Caso contrário, o aplicativo é responsável por exibir a caixa de diálogo usando a função de [**janela**](/windows/desktop/api/winuser/nf-winuser-showwindow) .

### <a name="dialog-box-measurements"></a>Medidas da caixa de diálogo

Cada modelo de caixa de diálogo contém medidas que especificam a posição, a largura e a altura da caixa de diálogo e os controles que ela contém. Essas medidas são independentes de dispositivo, portanto, um aplicativo pode usar um único modelo para criar a mesma caixa de diálogo para todos os tipos de dispositivos de vídeo. Isso garante que uma caixa de diálogo terá as mesmas proporções e a mesma aparência em todas as telas, apesar de diferentes resoluções e taxas de proporção entre telas.

As medidas em um modelo de caixa de diálogo são especificadas em unidades de modelo de diálogo. Para converter medidas de unidades de modelo de caixa de diálogo em unidades de tela (pixels), use a função [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) , que leva em conta a fonte usada pela caixa de diálogo e converte corretamente um retângulo de unidades de modelo de caixa de diálogo em pixels. Para caixas de diálogo que usam a fonte do sistema, você pode usar a função [**GetDialogBaseUnits**](/windows/desktop/api/Winuser/nf-winuser-getdialogbaseunits) para executar os cálculos de conversão por conta própria, embora o uso de **MapDialogRect** seja mais simples.

O modelo deve especificar as coordenadas iniciais do canto superior esquerdo da caixa de diálogo. Normalmente, as coordenadas são relativas ao canto superior esquerdo da área do cliente da janela do proprietário. Quando o modelo especifica o \_ estilo DS ABSALIGN ou a caixa de diálogo não tem proprietário, a posição é relativa ao canto superior esquerdo da tela. O sistema define essa posição inicial ao criar a caixa de diálogo, mas permite que um aplicativo ajuste a posição antes de exibir a caixa de diálogo. Por exemplo, um aplicativo pode recuperar as dimensões da janela do proprietário, calcular uma nova posição que centraliza a caixa de diálogo na janela do proprietário e, em seguida, definir a posição usando a função [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) .

O modelo deve especificar uma largura e uma altura da caixa de diálogo que não exceda a largura e a altura da tela e garante que todos os controles estejam dentro da área do cliente da caixa de diálogo. Embora o sistema permita que uma caixa de diálogo seja qualquer tamanho, criar uma que seja muito pequeno ou muito grande pode impedir que o usuário forneça a entrada, derrotando a finalidade da caixa de diálogo. Muitos aplicativos usam mais de uma caixa de diálogo quando há um grande número de controles. Nesses casos, a caixa de diálogo inicial geralmente contém um ou mais botões que o usuário pode escolher para exibir a próxima caixa de diálogo.

### <a name="dialog-box-controls"></a>Controles da caixa de diálogo

O modelo especifica a posição, a largura, a altura, o estilo, o identificador e a classe de janela para cada controle na caixa de diálogo. O sistema cria cada controle passando esses dados para a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) . Os controles são criados na ordem em que são especificados no modelo. O modelo deve especificar o número, o tipo e a ordem de controles apropriados para garantir que o usuário possa inserir a entrada necessária para concluir a tarefa associada à caixa de diálogo.

Para cada controle, o modelo especifica valores de estilo que definem a aparência e a operação do controle. Cada controle é uma janela filho e, portanto, deve ter o **estilo FILHO \_ do WS.** Para garantir que o controle seja visível quando a caixa de diálogo é exibida, cada controle também deve ter o **estilo \_ VISÍVEL do WS.** Outros estilos de janela comumente usados são BORDER do **WS \_** para controles que têm bordas opcionais, **WS \_ DISABLED** para controles que devem ser desabilitados quando a caixa de diálogo é criada inicialmente e **WS \_ TABSTOP** e **WS \_ GROUP** para controles que podem ser acessados usando o teclado. Os **estilos \_ TABSTOP** e WS GROUP do **WS \_** são usados em conjunto com a interface de teclado da caixa de diálogo descrita posteriormente neste tópico.

O modelo também pode especificar estilos de controle específicos para a classe de janela do controle. Por exemplo, um modelo que especifica um controle de botão deve dar um estilo de controle de botão, como **BS \_ PUSHBUTTON** ou **BS \_ CHECKBOX**. O sistema passa os estilos de controle para o procedimento da janela de controle por meio da mensagem [**WM \_ CREATE,**](/windows/desktop/winmsg/wm-create) permitindo que o procedimento adapte a aparência e a operação do controle.

O sistema converte as coordenadas de posição e as medidas de largura e altura de unidades base da caixa de diálogo em pixels, antes de passá-los [**para CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) Quando o sistema cria um controle, ele especifica a caixa de diálogo como a janela pai. Isso significa que o sistema sempre interpreta as coordenadas de posição do controle como coordenadas do cliente, em relação ao canto superior esquerdo da área de cliente da caixa de diálogo.

O modelo especifica a classe de janela para cada controle. Uma caixa de diálogo típica contém controles pertencentes às classes de janela de controle predefinidas, como o botão e editar classes de janela de controle. Nesse caso, o modelo especifica classes de janela fornecendo os valores atom predefinidos correspondentes para as classes. Quando uma caixa de diálogo contém um controle que pertence a uma classe de janela de controle personalizada, o modelo fornece o nome dessa classe de janela registrada ou o valor atom atualmente associado ao nome.

Cada controle em uma caixa de diálogo deve ter um identificador exclusivo para diferenciá-lo de outros controles. Os controles enviam informações para o procedimento da caixa de diálogo por meio de mensagens [**WM \_ COMMAND,**](/windows/desktop/menurc/wm-command) portanto, os identificadores de controle são essenciais para que o procedimento determine qual controle enviou uma mensagem especificada. A única exceção a essa regra são identificadores de controle para controles estáticos. Os controles estáticos não exigem identificadores exclusivos porque não enviam **mensagens WM \_ COMMAND.**

Para permitir que o usuário feche a caixa de diálogo, o modelo deve especificar pelo menos um botão de push e dar a ele o identificador de controle **IDCANCEL.** Para permitir que o usuário escolha entre concluir ou cancelar a tarefa associada à caixa de diálogo, o modelo deve especificar dois botões de push, rotulados **ok** e **Cancelar**, com identificadores de controle **de IDOK** e **IDCANCEL,** respectivamente.

Um modelo também especifica dados opcionais de criação e texto para um controle. O texto normalmente fornece rótulos para controles de botão ou especifica o conteúdo inicial de um controle de texto estático. Os dados de criação são um ou mais bytes de dados que o sistema passa para o procedimento da janela de controle ao criar o controle. Os dados de criação são úteis para controles que exigem mais informações sobre seu conteúdo ou estilo inicial do que o especificado por outros dados. Por exemplo, um aplicativo pode usar dados de criação para definir a configuração inicial e o intervalo para um controle de barra de rolagem.

### <a name="dialog-box-window-menu"></a>Menu da Janela da Caixa de Diálogo

O sistema fornece uma caixa de diálogo a um menu de janela quando o modelo especifica o **estilo \_ SYSMENU do WS.** Para evitar entradas inadequadas, o sistema desabilita automaticamente todos os itens no menu, exceto **Mover** e **Fechar**. O usuário pode clicar em **Mover** para mover a caixa de diálogo. Quando o usuário clica em **Fechar**, o sistema envia uma mensagem [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) para o procedimento da caixa de diálogo com o *parâmetro wParam* definido como **IDCANCEL.** Isso é idêntico à mensagem enviada pelo **botão Cancelar** quando o usuário clica nele. A ação recomendada para essa mensagem é fechar a caixa de diálogo e cancelar a tarefa solicitada.

Embora outros menus nas caixas de diálogo não sejam recomendados, um modelo de caixa de diálogo pode especificar um menu fornecendo o identificador ou o nome de um recurso de menu. Nesse caso, o sistema carrega o recurso e cria o menu para a caixa de diálogo. Os aplicativos normalmente usam identificadores de menu ou nomes em modelos ao usar os modelos para criar janelas personalizadas em vez de caixas de diálogo.

### <a name="dialog-box-fonts"></a>Fontes da caixa de diálogo

O sistema usa a largura média do caractere da fonte da caixa de diálogo para calcular a posição e as dimensões da caixa de diálogo. Por padrão, o sistema desenha todo o texto em uma caixa de diálogo usando a **fonte SYSTEM \_ FONT.**

Para especificar uma fonte para uma caixa de diálogo diferente do padrão, você deve criar a caixa de diálogo usando um modelo de caixa de diálogo. Em um recurso de modelo, use a [instrução FONT](../menurc/font-statement.md). Em um modelo de caixa de diálogo, de definido o estilo **SHELLFONT ou DS \_ DS** **\_ SHELLFONT** e especifique um tamanho de ponto e um nome de face de tipo. Mesmo que um modelo de caixa de diálogo especifique uma fonte dessa maneira, o sistema sempre usa a fonte do sistema para o título da caixa de diálogo e os menus da caixa de diálogo.

Quando a caixa de diálogo tem o estilo **DS \_ SETFONT** ou **DS \_ SHELLFONT,** o sistema envia uma mensagem [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont) para o procedimento da caixa de diálogo e para cada controle conforme ele cria o controle. O procedimento da caixa de diálogo é responsável por salvar o alça de fonte passado com a mensagem **WM \_ SETFONT** e selecionar o alça no contexto do dispositivo de exibição sempre que ele grava texto na janela. Os controles predefinidos fazem isso por padrão.

A fonte do sistema pode variar entre diferentes versões Windows. Para que seu aplicativo use a fonte do sistema, independentemente do sistema em que ele está sendo executado, use **DS \_ SHELLFONT** com a face de tipo MS Shell Dlg e use o Recurso [DIALOGEX](../menurc/dialogex-resource.md) em vez do Recurso [DIALOG.](../menurc/dialog-resource.md) O sistema mapeia essa face de tipo de forma que sua caixa de diálogo usará a fonte Toma. Observe que **o \_ SHELLFONT do DS** não terá nenhum efeito se a face de tipo não for Dlg do Shell do MS.

### <a name="templates-in-memory"></a>Modelos na memória

Um modelo de caixa de diálogo na memória consiste em um header que descreve a caixa de diálogo, seguido por um ou mais blocos de dados adicionais que descrevem cada um dos controles na caixa de diálogo. O modelo pode usar o formato padrão ou o formato estendido. Em um modelo padrão, o header é uma [**estrutura DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) seguida por matrizes de comprimento variável adicionais. Os dados de cada controle consistem em uma [**estrutura DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) seguida por matrizes de comprimento variável adicionais. Em um modelo de caixa de diálogo estendido, o header usa o [**formato DLGTEMPLATEEX**](dlgtemplateex.md) e as definições de controle usam o [**formato DLGITEMTEMPLATEEX.**](dlgitemtemplateex.md)

Para distinguir entre um modelo padrão e um modelo estendido, verifique os primeiros 16 bits de um modelo de caixa de diálogo. Em um modelo estendido, o primeiro **WORD** é 0xFFFF; qualquer outro valor indica um modelo padrão.

Se você criar um modelo de caixa de diálogo na memória, deverá garantir que cada uma das definições de controle [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) ou [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) esteja alinhada em limites **DWORD.** Além disso, todos os dados de criação que seguem uma definição de controle devem ser alinhados em um **limite DWORD.** Todas as outras matrizes de comprimento variável em um modelo de caixa de diálogo devem ser alinhadas nos limites **do WORD.**

### <a name="template-header"></a>Header de modelo

Nos modelos padrão e estendido para caixas de diálogo, o header inclui as seguintes informações gerais:

-   O local e as dimensões da caixa de diálogo
-   Os estilos da janela e da caixa de diálogo para a caixa de diálogo
-   O número de controles na caixa de diálogo. Esse valor determina o número de definições de controle [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) ou [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) no modelo.
-   Um recurso de menu opcional para a caixa de diálogo. O modelo pode indicar que a caixa de diálogo não tem um menu ou pode especificar um valor ordinal ou uma cadeia de caracteres Unicode terminada em nulo que identifica um recurso de menu em um arquivo executável.
-   A classe de janela da caixa de diálogo. Pode ser a classe da caixa de diálogo predefinida ou um valor ordinal ou uma cadeia de caracteres Unicode terminada em nulo que identifica uma classe de janela registrada.
-   Uma cadeia de caracteres Unicode terminada em nulo que especifica o título da janela da caixa de diálogo. Se a cadeia de caracteres estiver vazia, a barra de título da caixa de diálogo será em branco. Se a caixa de diálogo não tiver o estilo **\_ CAPTION do WS,** o sistema define o título para a cadeia de caracteres especificada, mas não o exibe.
-   Se a caixa de diálogo tiver o estilo **DS \_ SETFONT,** o header especificará o tamanho do ponto e o nome da face de tipo da fonte a ser usada para o texto na área do cliente e os controles da caixa de diálogo.

Em um modelo estendido, o [**header DLGTEMPLATEEX**](dlgtemplateex.md) também especifica as seguintes informações adicionais:

-   O identificador de contexto de ajuda da janela da caixa de diálogo quando o sistema envia uma mensagem [**DE \_ AJUDA do WM.**](../shell/wm-help.md)
-   Se a caixa de diálogo tiver o estilo **DS \_ SETFONT** ou **DS \_ SHELLFONT,** o header especificará o peso da fonte e indicará se a fonte é itálico.

### <a name="control-definitions"></a>Definições de controle

Após o header do modelo, há uma ou mais definições de controle que descrevem os controles da caixa de diálogo. Nos modelos padrão e estendido, o header da caixa de diálogo tem um membro que indica o número de definições de controle no modelo. Em um modelo padrão, cada definição de controle consiste em uma [**estrutura DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) seguida por matrizes de comprimento variável adicionais. Em um modelo estendido, as definições de controle usam o [**formato DLGITEMTEMPLATEEX.**](dlgitemtemplateex.md)

Nos modelos padrão e estendido, a definição de controle inclui as seguintes informações:

-   O local e as dimensões do controle.
-   Os estilos de janela e controle para o controle.
-   O identificador de controle.
-   A classe de janela do controle . Pode ser o valor ordinal de uma classe de sistema predefinida ou uma cadeia de caracteres Unicode terminada em nulo que especifica o nome de uma classe de janela registrada.
-   Uma cadeia de caracteres Unicode terminada em nulo que especifica o texto inicial do controle ou um valor ordinal que identifica um recurso, como um ícone, em um arquivo executável.
-   Um bloco opcional de comprimento variável de dados de criação. Quando o sistema cria o controle , ele passa um ponteiro para esses dados no parâmetro *lParam* da mensagem [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create) que ele envia para o controle.

Em um modelo estendido, a definição de controle também especifica um identificador de contexto de ajuda para o controle quando o sistema envia uma mensagem [**DE \_ AJUDA do WM.**](../shell/wm-help.md)

 

 