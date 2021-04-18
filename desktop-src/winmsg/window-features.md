---
description: Esta visão geral discute os recursos do Windows, como tipos de janela, Estados, tamanho e posição.
ms.assetid: 8318c22f-85a2-490e-8233-ee1e234890d9
title: Recursos de janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 228c6b4ab59102cae38a248935fbbad32198f2e0
ms.sourcegitcommit: 8755905962e156f29203705d09d6df8b7d0e2fca
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/25/2021
ms.locfileid: "105755871"
---
# <a name="window-features"></a>Recursos de janela

Esta visão geral discute os recursos do Windows, como tipos de janela, Estados, tamanho e posição.

-   [Tipos de janela](#window-types)
    -   [Janelas sobrepostas](#overlapped-windows)
    -   [Janelas pop-up](#pop-up-windows)
    -   [Janelas filhas](#child-windows)
        -   [Posicionamento](#positioning)
        -   [Recorte](#clipping)
        -   [Relação com a janela pai](#relationship-to-parent-window)
        -   [Mensagens](#size-and-position-messages)
    -   [Janelas em camadas](#layered-windows)
    -   [Janelas somente de mensagens](#message-only-windows)
-   [Relacionamentos de janela](#window-relationships)
    -   [Janelas de primeiro e segundo plano](#foreground-and-background-windows)
    -   [Janelas de propriedade](#owned-windows)
    -   [Ordem Z](#z-order)
-   [Estado de exibição da janela](#window-show-state)
    -   [Janela ativa](#active-window)
    -   [Janelas desabilitadas](#disabled-windows)
    -   [Visibilidade da janela](#window-visibility)
    -   [Janelas minimizadas, maximizadas e restauradas](#minimized-maximized-and-restored-windows)
-   [Tamanho e posição da janela](#window-size-and-position)
    -   [Tamanho e posição padrão](#default-size-and-position)
    -   [Tamanho do rastreamento](#tracking-size)
    -   [Comandos do sistema](#system-commands)
    -   [Funções de tamanho e posição](#size-and-position-functions)
    -   [Mensagens de tamanho e posição](#size-and-position-messages)
-   [Animação de janela](#window-animation)
-   [Layout e espelhamento de janela](#window-layout-and-mirroring)
    -   [Caixas de diálogo e caixas de mensagem de espelhamento](#mirroring-dialog-boxes-and-message-boxes)
    -   [Contextos de dispositivo de espelhamento não associados a uma janela](#mirroring-device-contexts-not-associated-with-a-window)
-   [Destruição de janelas](#window-destruction)

## <a name="window-types"></a>Tipos de janela

Esta seção contém os tópicos a seguir que descrevem os tipos de janela.

-   [Janelas sobrepostas](#overlapped-windows)
-   [Janelas pop-up](#pop-up-windows)
-   [Janelas filhas](#child-windows)
-   [Janelas em camadas](#layered-windows)
-   [Janelas somente de mensagens](#message-only-windows)

### <a name="overlapped-windows"></a>Janelas sobrepostas

Uma *janela sobreposta* é uma janela de nível superior (janela não-filho) que tem uma barra de título, borda e área de cliente; Ele serve para servir como uma janela principal do aplicativo. Ele também pode ter um menu de janela, minimizar e maximizar botões e barras de rolagem. Uma janela sobreposta usada como uma janela principal normalmente inclui todos esses componentes.

Ao especificar o estilo [**WS \_ Overlapped**](window-styles.md) ou **WS \_ OVERLAPPEDWINDOW** na função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , um aplicativo cria uma janela sobreposta. Se você usar o estilo **WS \_ Overlapped** , a janela terá uma barra de título e uma borda. Se você usar o estilo **WS \_ OVERLAPPEDWINDOW** , a janela terá uma barra de título, uma borda de dimensionamento, um menu de janela e os botões minimizar e maximizar.

### <a name="pop-up-windows"></a>Janelas pop-up

Uma *janela pop-up* é um tipo especial de janela sobreposta usada para caixas de diálogo, caixas de mensagem e outras janelas temporárias que aparecem fora da janela principal de um aplicativo. As barras de título são opcionais para janelas pop-up; caso contrário, as janelas pop-up são as mesmas que as janelas sobrepostas do estilo [**WS \_ Overlapped**](window-styles.md) .

Você cria uma janela pop-up especificando o estilo [**WS- \_ Popup**](window-styles.md) em [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa). Para incluir uma barra de título, especifique o estilo de **\_ legenda WS** . Use o estilo **WS \_ POPUPWINDOW** para criar uma janela pop-up que tenha uma borda e um menu de janela. O estilo de **\_ legenda WS** deve ser combinado com o estilo **WS \_ POPUPWINDOW** para tornar o menu janela visível.

### <a name="child-windows"></a>Janelas filhas

Uma *janela filho* tem o [**estilo \_ filho WS**](window-styles.md) e é confinada na área do cliente de sua janela pai. Um aplicativo geralmente usa janelas filhas para dividir a área do cliente de uma janela pai em áreas funcionais. Você cria uma janela filho especificando o estilo **\_ filho WS** na função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .

Uma janela filho deve ter uma janela pai. A janela pai pode ser uma janela sobreposta, uma janela pop-up ou até mesmo outra janela filho. Você especifica a janela pai ao chamar [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa). Se você especificar o [**estilo \_ filho WS**](window-styles.md) em **CreateWindowEx** , mas não especificar uma janela pai, o sistema não criará a janela.

Uma janela filho tem uma área de cliente, mas nenhum outro recurso, a menos que elas sejam explicitamente solicitadas. Um aplicativo pode solicitar uma barra de título, um menu de janela, minimizar e maximizar botões, uma borda e barras de rolagem para uma janela filho, mas uma janela filho não pode ter um menu. Se o aplicativo especificar um identificador de menu, seja ao registrar a classe de janela do filho ou criar a janela filho, o identificador de menu será ignorado. Se nenhum estilo de borda for especificado, o sistema criará uma janela sem borda. Um aplicativo pode usar janelas filho sem borda para dividir a área do cliente de uma janela pai e, ao mesmo tempo, manter as divisões invisíveis para o usuário.

Esta seção aborda os seguintes aspectos das janelas filhas:

-   [Posicionamento](#positioning)
-   [Recorte](#clipping)
-   [Relação com a janela pai](#relationship-to-parent-window)
-   [Mensagens](#size-and-position-messages)

#### <a name="positioning"></a>Posicionamento

O sistema sempre posiciona uma janela filho em relação ao canto superior esquerdo da área cliente da janela pai. Nenhuma parte de uma janela filho aparece fora das bordas de sua janela pai. Se um aplicativo criar uma janela filho maior do que a janela pai ou posicionar uma janela filho para que algumas ou todas as janelas filho ultrapassem as bordas do pai, o sistema cortará a janela filho; ou seja, a parte fora da área do cliente da janela pai não é exibida. As ações que afetam a janela pai também podem afetar a janela filho, como a seguir.



| Janela pai | Janela filho                                                                                                             |
|---------------|--------------------------------------------------------------------------------------------------------------------------|
| Destruído     | Destruído antes que a janela pai seja destruída.                                                                         |
| Hidden        | Oculto antes da janela pai ser oculta. Uma janela filho é visível somente quando a janela pai está visível.             |
| Sido         | Movido com a área do cliente da janela pai. A janela filho é responsável por pintar sua área de cliente após a movimentação. |
| Hubs         | Mostrado depois que a janela pai é mostrada.                                                                                  |



 

#### <a name="clipping"></a>Recortando

O sistema não corta automaticamente uma janela filho da área do cliente da janela pai. Isso significa que a janela pai se desenha na janela filho se ela executar qualquer desenho no mesmo local que a janela filho. No entanto, o sistema corta a janela filho da área do cliente da janela pai se a janela pai tem o estilo [**WS \_ CLIPCHILDREN**](window-styles.md) . Se a janela filho for recortada, a janela pai não poderá desenhá-la.

Uma janela filho pode sobrepor outras janelas filhas na mesma área do cliente. Uma janela filho que compartilha a mesma janela pai como uma ou mais janelas filhas é chamada de *janela irmã*. As janelas irmãs podem ser desenhadas na área do cliente, a menos que uma das janelas filhas tenha o estilo [**WS \_ CLIPSIBLINGS**](window-styles.md) . Se uma janela filho tiver esse estilo, qualquer parte da janela irmã que está dentro da janela filho será recortada.

Se uma janela tiver o estilo [**WS \_ CLIPCHILDREN**](window-styles.md) ou **WS \_ CLIPSIBLINGS** , ocorrerá uma pequena perda de desempenho. Cada janela usa recursos do sistema, de modo que um aplicativo não deve usar o Windows filho indiscriminative. Para obter um melhor desempenho, um aplicativo que precisa dividir logicamente sua janela principal deve fazer isso no procedimento de janela da janela principal, em vez de usar janelas filhas.

#### <a name="relationship-to-parent-window"></a>Relação com a janela pai

Um aplicativo pode alterar a janela pai de uma janela filho existente chamando a função [**setpai**](/windows/win32/api/winuser/nf-winuser-setparent) . Nesse caso, o sistema remove a janela filho da área do cliente da antiga janela pai e a move para a área do cliente da nova janela pai. Se **SetParent** especificar um identificador **nulo** , a janela da área de trabalho se tornará a nova janela pai. Nesse caso, a janela filho é desenhada na área de trabalho, fora das bordas de qualquer outra janela. A função [**GetParent**](/windows/win32/api/winuser/nf-winuser-getparent) recupera um identificador para a janela pai de uma janela filho.

A janela pai abandona uma parte de sua área de cliente para uma janela filho, e a janela filho recebe todas as entradas dessa área. A classe Window não precisa ser a mesma para cada uma das janelas filhas da janela pai. Isso significa que um aplicativo pode preencher uma janela pai com janelas filhas que parecem diferentes e executam tarefas diferentes. Por exemplo, uma caixa de diálogo pode conter muitos tipos de controles, cada um com uma janela filho que aceita diferentes tipos de dados do usuário.

Uma janela filho tem apenas uma janela pai, mas um pai pode ter qualquer número de janelas filhas. Cada janela filho, por sua vez, pode ter janelas filhas. Nessa cadeia de janelas, cada janela filho é chamada de janela descendente da janela pai original. Um aplicativo usa a função [**IsChild**](/windows/win32/api/winuser/nf-winuser-ischild) para descobrir se uma determinada janela é uma janela filho ou uma janela descendente de uma determinada janela pai.

A função [**EnumChildWindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) enumera as janelas filhas de uma janela pai. Em seguida, **EnumChildWindows** passa o identificador para cada janela filho para uma função de retorno de chamada definida pelo aplicativo. Janelas descendentes da janela pai fornecida também são enumeradas.

#### <a name="messages"></a>Mensagens

O sistema passa as mensagens de entrada de uma janela filho diretamente para a janela filho; as mensagens não são passadas pela janela pai. A única exceção é se a janela filho tiver sido desabilitada pela função [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) . Nesse caso, o sistema passa todas as mensagens de entrada que teriam sido feitas na janela filho para a janela pai. Isso permite que a janela pai examine as mensagens de entrada e habilite a janela filho, se necessário.

Uma janela filho pode ter um identificador inteiro exclusivo. Identificadores de janela filho são importantes ao trabalhar com janelas de controle. Um aplicativo direciona a atividade de um controle enviando mensagens de ti. O aplicativo usa o identificador de janela filho do controle para direcionar as mensagens para o controle. Além disso, um controle envia mensagens de notificação para sua janela pai. Uma mensagem de notificação inclui o identificador de janela filho do controle, que o pai usa para identificar qual controle enviou a mensagem. Um aplicativo especifica o identificador da janela filho para outros tipos de janelas filho, definindo o parâmetro *HMENU* da função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) como um valor em vez de um identificador de menu.

### <a name="layered-windows"></a>Janelas em camadas

Usar uma janela em camadas pode melhorar significativamente o desempenho e os efeitos visuais de uma janela que tem uma forma complexa, anima sua forma ou deseja usar efeitos de mistura alfa. O sistema automaticamente compõe e redesenha janelas em camadas e as janelas de aplicativos subjacentes. Como resultado, as janelas em camadas são processadas suavemente, sem a cintilação típica de regiões de janela complexas. Além disso, as janelas em camadas podem ser parcialmente translúcidas, ou seja, de combinação alfa.

Para criar uma janela em camadas, especifique o estilo de janela estendida em **\_ \_ camadas do WS ex** ao chamar a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) ou chame a função [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) para definir o **WS \_ ex \_ Layer** , depois que a janela tiver sido criada. Após a chamada **CreateWindowEx** , a janela em camadas não ficará visível até que a função [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) ou [**UpdateLayeredWindow**](/windows/win32/api/winuser/nf-winuser-updatelayeredwindow) tenha sido chamada para essa janela.

> [!Note]  
> A partir do Windows 8, o **WS \_ ex \_ Layer** pode ser usado com janelas filhas e janelas de nível superior. Versões anteriores do Windows oferecem suporte ao **WS \_ ex em \_ camadas** apenas para janelas de nível superior.

 

Para definir o nível de opacidade ou a chave de cor de transparência para uma determinada janela em camadas, chame [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes). Após a chamada, o sistema ainda pode solicitar que a janela seja pintada quando a janela for mostrada ou redimensionada. No entanto, como o sistema armazena a imagem de uma janela em camadas, o sistema não solicitará que a janela seja pintada se partes dela forem reveladas como resultado de movimentações de janela relativas na área de trabalho. Os aplicativos herdados não precisam reestruturar o código de pintura se desejarem adicionar efeitos de Translucency ou transparência para uma janela, pois o sistema redireciona a pintura do Windows que chamou **SetLayeredWindowAttributes** na memória fora da tela e a recompõe para obter o efeito desejado.

Para uma animação mais rápida e eficiente ou se alfa por pixel for necessário, chame [**UpdateLayeredWindow**](/windows/win32/api/winuser/nf-winuser-updatelayeredwindow). **UpdateLayeredWindow** deve ser usado principalmente quando o aplicativo deve fornecer diretamente a forma e o conteúdo de uma janela em camadas, sem usar o mecanismo de redirecionamento que o sistema fornece por meio do [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes). Além disso, usar o **UpdateLayeredWindow** diretamente usa a memória com mais eficiência, porque o sistema não precisa da memória adicional necessária para armazenar a imagem da janela redirecionada. Para obter a eficiência máxima nas janelas de animação, chame **UpdateLayeredWindow** para alterar a posição e o tamanho de uma janela em camadas. Observe que, após **SetLayeredWindowAttributes** ter sido chamado, as chamadas de **UpdateLayeredWindow** subsequentes falharão até que o bit do estilo de camadas seja limpo e definido novamente.

O teste de clique de uma janela em camadas é baseado na forma e na transparência da janela. Isso significa que as áreas da janela que são codificadas por cor ou cujo valor alfa é zero permitirão que as mensagens do mouse sejam transformadas. No entanto, se a janela em camadas tiver o estilo de janela estendida do **WS \_ ex \_ Transparent** , a forma da janela em camadas será ignorada e os eventos do mouse serão passados para outras janelas abaixo da janela em camadas.

### <a name="message-only-windows"></a>Message-Only Windows

Uma *janela somente mensagem* permite que você envie e receba mensagens. Não é visível, não tem nenhuma ordem z, não pode ser enumerada e não recebe mensagens de difusão. A janela simplesmente despacha mensagens.

Para criar uma janela somente mensagem, especifique a constante [de \_ mensagem HWND](#message-only-windows) ou um identificador para uma janela somente de mensagem existente no parâmetro *hwndParent* da função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Você também pode alterar uma janela existente para uma janela somente mensagem especificando a mensagem HWND \_ no parâmetro *hWndNewParent* da função [**setpai**](/windows/win32/api/winuser/nf-winuser-setparent) .

Para localizar o Windows somente mensagens, especifique [a \_ mensagem HWND](#message-only-windows) no parâmetro *hwndParent* da função [**FindWindowEx**](/windows/win32/api/winuser/nf-winuser-findwindowexa) . Além disso, **FindWindowEx** pesquisa janelas somente mensagens, bem como janelas de nível superior, se os parâmetros *hwndParent* e *hwndChildAfter* forem **nulos**.

## <a name="window-relationships"></a>Relacionamentos de janela

Há muitas maneiras pelas quais uma janela pode se relacionar ao usuário ou a outra janela. Uma janela pode ser uma janela de propriedade, uma janela em primeiro plano ou uma janela de plano de fundo. Uma janela também tem uma ordem z relativa a outras janelas. Para mais informações, consulte os seguintes tópicos:

-   [Janelas de primeiro e segundo plano](#foreground-and-background-windows)
-   [Janelas de propriedade](#owned-windows)
-   [Ordem Z](#z-order)

### <a name="foreground-and-background-windows"></a>Janelas de primeiro e segundo plano

Cada processo pode ter vários threads de execução, e cada thread pode criar o Windows. O thread que criou a janela com a qual o usuário está trabalhando no momento é chamado de thread em primeiro plano e a janela é chamada de *janela em primeiro plano*. Todos os outros threads são threads em segundo plano, e as janelas criadas por threads em segundo plano são chamadas de *janelas em segundo plano*.

Cada thread tem um nível de prioridade que determina a quantidade de tempo de CPU que o thread recebe. Embora um aplicativo possa definir o nível de prioridade de seus threads, normalmente o thread em primeiro plano tem um nível de prioridade um pouco maior do que os threads em segundo plano. Como tem uma prioridade mais alta, o thread em primeiro plano recebe mais tempo de CPU do que os threads em segundo plano. O thread em primeiro plano tem uma prioridade de base normal de 9; um thread em segundo plano tem uma prioridade de base normal de 7.

O usuário define a janela em primeiro plano clicando em uma janela ou usando a combinação de teclas ALT + TAB ou ALT + ESC. Para recuperar um identificador para a janela em primeiro plano, use a função [**GetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-getforegroundwindow) . Para verificar se a janela do aplicativo é a janela em primeiro plano, compare o identificador retornado por **GetForegroundWindow** com o da janela do aplicativo.

Um aplicativo define a janela em primeiro plano usando a função [**SetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-setforegroundwindow) .

O sistema restringe quais processos podem definir a janela em primeiro plano. Um processo pode definir a janela de primeiro plano somente se:

- Todas as condições a seguir são verdadeiras:
  - O processo que chama **SetForegroundWindow** pertence a um aplicativo de área de trabalho, não a um aplicativo UWP ou a um aplicativo da Windows Store projetado para o Windows 8 ou 8,1.
  - O processo em primeiro plano não desabilitou chamadas para **SetForegroundWindow** por uma chamada anterior à função [**LockSetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-locksetforegroundwindow) .
  - O tempo limite de bloqueio em primeiro plano expirou (consulte [ **SPI_GETFOREGROUNDLOCKTIMEOUT** em **SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa#SPI_GETFOREGROUNDLOCKTIMEOUT)).
  - Nenhum menu está ativo.
- Além disso, pelo menos uma das seguintes condições é verdadeira:
  - O processo de chamada é o processo em primeiro plano.
  - O processo de chamada foi iniciado pelo processo em primeiro plano.
  - No momento, não há janela em primeiro plano e, portanto, nenhum processo em primeiro plano.
  - O processo de chamada recebeu o último evento de entrada.
  - O processo em primeiro plano ou o processo de chamada está sendo depurado.

É possível que um processo seja negado ao direito de definir a janela em primeiro plano mesmo que atenda a essas condições.

Um processo que pode definir a janela em primeiro plano pode habilitar outro processo para definir a janela em primeiro plano chamando a função [**AllowSetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-allowsetforegroundwindow) ou chamando a função [**BroadcastSystemMessage**](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessage) com o sinalizador **BSF \_ ALLOWSFW** . O processo em primeiro plano pode desabilitar chamadas para [**SetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-setforegroundwindow) chamando a função [**LockSetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-locksetforegroundwindow) .

### <a name="owned-windows"></a>Janelas de propriedade

Uma janela sobreposta ou pop-up pode ser de propriedade de outra janela sobreposta ou pop-up. Ter sido um lugar com várias restrições em uma janela.

-   Uma janela de propriedade está sempre acima do seu proprietário na ordem z.
-   O sistema destrói automaticamente uma janela de propriedade quando seu proprietário é destruído.
-   Uma janela de propriedade é ocultada quando seu proprietário é minimizado.

Somente uma janela sobreposta ou pop-up pode ser uma janela do proprietário; uma janela filho não pode ser uma janela de proprietário. Um aplicativo cria uma janela de propriedade especificando o identificador de janela do proprietário como o parâmetro *hwndParent* de [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) quando ele cria uma janela com o estilo **\_ pop-up** [**WS \_ Overlapped**](window-styles.md) ou WS. O parâmetro *hwndParent* deve identificar uma janela sobreposta ou pop-up. Se *hwndParent* identificar uma janela filho, o sistema atribuirá Propriedade à janela pai de nível superior da janela filho. Depois de criar uma janela de propriedade, um aplicativo não pode transferir a propriedade da janela para outra janela.

As caixas de diálogo e caixas de mensagem são janelas de propriedade, por padrão. Um aplicativo especifica a janela do proprietário ao chamar uma função que cria uma caixa de diálogo ou caixa de mensagem.

Um aplicativo pode usar a função [**GetWindow**](/windows/win32/api/winuser/nf-winuser-getwindow) com o sinalizador de **\_ proprietário GW** para recuperar um identificador para o proprietário de uma janela.

### <a name="z-order"></a>Ordem Z

A *ordem z* de uma janela indica a posição da janela em uma pilha de janelas sobrepostas. Essa pilha de janela é orientada ao longo de um eixo imaginário, o eixo z, que se estende para fora da tela. A janela na parte superior da ordem z se sobrepõe a todas as outras janelas. A janela na parte inferior da ordem z é sobreposta por todas as outras janelas.

O sistema mantém a ordem z em uma única lista. Ele adiciona o Windows à ordem z com base em se eles são janelas superiores, janelas de nível superior ou janelas filhas. Uma *janela mais elevada* sobrepõe todas as outras janelas que não são mais altas, independentemente de ser a janela ativa ou de primeiro plano. Uma janela superior tem o estilo **WS \_ ex mais \_ alto** . Todas as janelas de nível superior aparecem na ordem z antes de qualquer janela que não seja superior. Uma janela filho é agrupada com seu pai na ordem z.

Quando um aplicativo cria uma janela, o sistema a coloca na parte superior da ordem z para janelas do mesmo tipo. Você pode usar a função [**BringWindowToTop**](/windows/win32/api/winuser/nf-winuser-bringwindowtotop) para trazer uma janela para a parte superior da ordem z para janelas do mesmo tipo. Você pode reorganizar a ordem z usando as funções [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) e [**DeferWindowPos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos) .

O usuário altera a ordem z ativando uma janela diferente. O sistema posiciona a janela ativa na parte superior da ordem z para janelas do mesmo tipo. Quando uma janela chega à parte superior da ordem z, então suas janelas filhas. Você pode usar a função [**GetTopWindow**](/windows/win32/api/winuser/nf-winuser-gettopwindow) para pesquisar todas as janelas filhas de uma janela pai e retornar um identificador para a janela filho que é mais alta em ordem z. A função [**GetNextWindow**](/windows/win32/api/winuser/nf-winuser-getnextwindow) recupera um identificador para a janela seguinte ou anterior na ordem z.

## <a name="window-show-state"></a>Estado de exibição da janela

Em um determinado momento, uma janela pode estar ativa ou inativa; oculto ou visível; e minimizado, maximizado ou restaurado. Essas qualidades são referidas coletivamente como o *estado de exibição da janela*. Os tópicos a seguir discutem o estado da janela mostrar:

-   [Janela ativa](#active-window)
-   [Janelas desabilitadas](#disabled-windows)
-   [Visibilidade da janela](#window-visibility)
-   [Janelas minimizadas, maximizadas e restauradas](#minimized-maximized-and-restored-windows)

### <a name="active-window"></a>Janela ativa

Uma *janela ativa* é a janela de nível superior do aplicativo com a qual o usuário está trabalhando no momento. Para permitir que o usuário identifique facilmente a janela ativa, o sistema a coloca na parte superior da ordem z e altera a cor de sua barra de título e borda para as cores de janela ativa definidas pelo sistema. Somente uma janela de nível superior pode ser uma janela ativa. Quando o usuário está trabalhando com uma janela filho, o sistema ativa a janela pai de nível superior associada à janela filho.

Apenas uma janela de nível superior no sistema está ativa por vez. O usuário ativa uma janela de nível superior clicando nela (ou em uma de suas janelas filhas) ou usando a combinação de teclas ALT + ESC ou ALT + TAB. Um aplicativo ativa uma janela de nível superior chamando a função [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) . Outras funções podem fazer com que o sistema Ative uma janela de nível superior diferente, incluindo [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos), [**DeferWindowPos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos), [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement)e [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow). Embora um aplicativo possa ativar uma janela de nível superior diferente a qualquer momento, para evitar a confusão do usuário, ele deve fazer isso somente em resposta a uma ação do usuário. Um aplicativo usa a função [**GetActiveWindow**](/windows/win32/api/winuser/nf-winuser-getactivewindow) para recuperar um identificador para a janela ativa.

Quando a ativação muda de uma janela de nível superior de um aplicativo para a janela de nível superior de outra, o sistema envia uma mensagem do [**WM \_ ACTIVATEAPP**](wm-activateapp.md) para ambos os aplicativos, notificando-os sobre a alteração. Quando a ativação é alterada para uma janela de nível superior diferente no mesmo aplicativo, o sistema envia uma mensagem de [**\_ ativação**](../inputdev/wm-activate.md) do Windows a WM.

### <a name="disabled-windows"></a>Janelas desabilitadas

Uma janela pode ser desabilitada. Uma *janela desabilitada* não recebe nenhuma entrada de teclado ou mouse do usuário, mas pode receber mensagens de outras janelas, de outros aplicativos e do sistema. Um aplicativo normalmente desabilita uma janela para impedir que o usuário use a janela. Por exemplo, um aplicativo pode desabilitar um botão de ação em uma caixa de diálogo para impedir que o usuário o escolha. Um aplicativo pode habilitar uma janela desabilitada a qualquer momento; a habilitação de uma janela restaura a entrada normal.

Por padrão, uma janela é habilitada quando criada. No entanto, um aplicativo pode especificar o estilo [**WS \_ Disabled**](window-styles.md) para desabilitar uma nova janela. Um aplicativo habilita ou desabilita uma janela existente usando a função [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) . O sistema envia uma mensagem de [**\_ habilitação do WM**](wm-enable.md) para uma janela quando seu estado habilitado está prestes a ser alterado. Um aplicativo pode determinar se uma janela está habilitada usando a função [**IsWindowEnabled**](/windows/win32/api/winuser/nf-winuser-iswindowenabled) .

Quando uma janela filho é desabilitada, o sistema passa as mensagens de entrada do mouse do filho para a janela pai. O pai usa as mensagens para determinar se a janela filho deve ser habilitada. Para obter mais informações, consulte [entrada do mouse](../inputdev/mouse-input.md).

Somente uma janela por vez pode receber entrada de teclado; essa janela é indicada para o foco do teclado. Se um aplicativo usar a função [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) para desabilitar uma janela de foco do teclado, a janela perderá o foco do teclado, além de ser desabilitada. Em seguida, **EnableWindow** define o foco do teclado como **NULL**, o que significa que nenhuma janela tem o foco. Se uma janela filho, ou outra janela descendente, tiver o foco do teclado, a janela descendente perderá o foco quando a janela pai estiver desabilitada. Para obter mais informações, consulte [entrada do teclado](../inputdev/keyboard-input.md).

### <a name="window-visibility"></a>Visibilidade da janela

Uma janela pode ser visível ou oculta. O sistema exibe uma *janela visível* na tela. Ele oculta uma *janela oculta* sem desenhá-la. Se uma janela estiver visível, o usuário poderá fornecer entradas a ela e exibir suas saídas. Se uma janela for oculta, ele estará efetivamente desabilitada. Uma janela oculta pode processar mensagens do sistema ou de outras janelas, mas não pode processar a entrada do usuário ou exibir a saída. Um aplicativo define o estado de visibilidade da janela ao criar a janela. Posteriormente, o aplicativo pode alterar o estado de visibilidade.

Uma janela fica visível quando o [**estilo \_ visível do WS**](window-styles.md) é definido para a janela. Por padrão, a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) cria uma janela oculta, a menos que o aplicativo especifique o estilo do **WS \_ Visible** . Normalmente, um aplicativo define o estilo do **WS \_ Visible** depois de ter criado uma janela para manter os detalhes do processo de criação oculto do usuário. Por exemplo, um aplicativo pode manter uma nova janela oculta enquanto personaliza a aparência da janela. Se o estilo do **WS \_ Visible** for especificado em **CreateWindowEx**, o sistema enviará a mensagem do WM para a janela depois de criar a janela, mas antes de exibi-la. [**\_**](wm-showwindow.md)

Um aplicativo pode determinar se uma janela está visível usando a função [**IsWindowVisible**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) . Um aplicativo pode mostrar (tornar visível) ou ocultar uma janela [**usando a função**](/windows/win32/api/winuser/nf-winuser-showwindow) [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos), [**DeferWindowPos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos)ou [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) ou [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) . Essas funções mostram ou ocultam uma janela Configurando ou removendo o estilo [**\_ visível WS**](window-styles.md) para a janela. Eles também enviam a mensagem de [**\_ janela do WM**](wm-showwindow.md) para a janela antes de mostrá-la ou ocultá-la.

Quando uma janela do proprietário é minimizada, o sistema oculta automaticamente as janelas de propriedade associadas. Da mesma forma, quando uma janela do proprietário é restaurada, o sistema mostra automaticamente as janelas de propriedade associadas. Em ambos os casos, o sistema envia a mensagem do [**WM show \_ Window**](wm-showwindow.md) para as janelas de propriedade antes de ocultá-las ou mostrá-las. Ocasionalmente, um aplicativo pode precisar ocultar as janelas de propriedade sem precisar minimizar ou ocultar o proprietário. Nesse caso, o aplicativo usa a função [**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups) . Essa função define ou remove o [**estilo \_ visível WS**](window-styles.md) para todas as janelas de propriedade e envia a mensagem do **WM show \_ Window** para as janelas de propriedade antes de ocultá-las ou mostrá-las. Ocultar uma janela do proprietário não tem nenhum efeito sobre o estado de visibilidade das janelas de propriedade.

Quando uma janela pai é visível, suas janelas filhas associadas também são visíveis. Da mesma forma, quando a janela pai está oculta, suas janelas filhas também são ocultas. Minimizar a janela pai não tem nenhum efeito sobre o estado de visibilidade das janelas filhas; ou seja, as janelas filhas são minimizadas junto com o pai, mas o estilo do [**WS \_ Visible**](window-styles.md) não é alterado.

Mesmo que uma janela tenha o estilo de [**WS \_ visível**](window-styles.md) , talvez o usuário não consiga ver a janela na tela; outras janelas podem sobrepostá-la completamente ou pode ter sido movida além da borda da tela. Além disso, uma janela filho visível está sujeita às regras de recorte estabelecidas por sua relação pai-filho. Se a janela pai da janela não estiver visível, ela também não estará visível. Se a janela pai se mover além da borda da tela, a janela filho também será movida porque uma janela filho é desenhada em relação ao canto superior esquerdo do pai. Por exemplo, um usuário pode mover a janela pai que contém a janela filho muito longe da borda da tela que o usuário pode não conseguir ver a janela filho, mesmo que a janela filho e sua janela pai tenham o estilo de **WS \_ Visible** .

### <a name="minimized-maximized-and-restored-windows"></a>Janelas minimizadas, maximizadas e restauradas

Uma *janela maximizada* é uma janela que tem o estilo [**WS \_ Maxim**](window-styles.md) . Por padrão, o sistema aumenta uma janela maximizada para que ela ocupe a tela ou, no caso de uma janela filho, a área de cliente da janela pai. Embora o tamanho de uma janela possa ser definido com o mesmo tamanho de uma janela maximizada, uma janela maximizada é ligeiramente diferente. O sistema move automaticamente a barra de título da janela para a parte superior da tela ou para a parte superior da área do cliente da janela pai. Além disso, o sistema desabilita a borda de dimensionamento da janela e o recurso de posicionamento da janela da barra de título (para que o usuário não possa mover a janela arrastando a barra de título).

Uma *janela minimizada* é uma janela com o estilo [**WS \_ minimize**](window-styles.md) . Por padrão, o sistema reduz uma janela minimizada ao tamanho do seu botão da barra de tarefas e a move para a barra de tarefas. Uma *janela restaurada* é uma janela que foi retornada ao tamanho e posição anteriores, ou seja, o tamanho antes de ser minimizado ou maximizado.

Se um aplicativo especificar o estilo [**WS \_ Maxim**](window-styles.md) ou **WS \_ minimize** na função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , a janela será inicialmente maximizada ou minimizada. Depois de criar uma janela, um aplicativo pode usar a função [**CloseWindow**](/windows/win32/api/winuser/nf-winuser-closewindow) para minimizar a janela. A função [**ArrangeIconicWindows**](/windows/win32/api/winuser/nf-winuser-arrangeiconicwindows) organiza os ícones na área de trabalho ou organiza as janelas filho minimizadas de uma janela pai na janela pai. A função [**OpenIcon**](/windows/win32/api/winuser/nf-winuser-openicon) restaura uma janela minimizada para seu tamanho e posição anteriores.

A função de [**janela**](/windows/win32/api/winuser/nf-winuser-showwindow) pode minimizar, maximizar ou restaurar uma janela. Ele também pode definir a visibilidade e os Estados de ativação da janela. A função [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) inclui a mesma funcionalidade que o de **janela**, mas pode substituir as posições padrão minimizadas, maximizadas e restauradas da janela.

As funções [**Isapliqued**](/windows/win32/api/winuser/nf-winuser-iszoomed) e [**isicony**](/windows/win32/api/winuser/nf-winuser-isiconic) determinam se uma determinada janela é maximizada ou minimizada, respectivamente. A função [**GetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-getwindowplacement) recupera as posições minimizadas, maximizadas e restauradas para a janela e também determina o estado de exibição da janela.

Quando o sistema recebe um comando para maximizar ou restaurar uma janela minimizada, ele envia a janela uma mensagem do [**WM \_ QUERYOPEN**](wm-queryopen.md) . Se o procedimento de janela retornar **false**, o sistema ignorará o comando maximizar ou restaurar.

O sistema define automaticamente o tamanho e a posição de uma janela maximizada para os padrões definidos pelo sistema para uma janela maximizada. Para substituir esses padrões, um aplicativo pode chamar a função [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) ou processar a mensagem do [**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) que é recebida por uma janela quando o sistema está prestes a maximizar a janela. **WM \_ GETMINMAXINFO** inclui um ponteiro para uma estrutura [**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) que contém valores que o sistema usa para definir o tamanho e a posição maximizados. Substituir esses valores substitui os padrões.

## <a name="window-size-and-position"></a>Tamanho e posição da janela

O tamanho e a posição de uma janela são expressos como um retângulo delimitador, fornecidos em coordenadas relativas à tela ou à janela pai. As coordenadas de uma janela de nível superior são relativas ao canto superior esquerdo da tela; as coordenadas de uma janela filho são relativas ao canto superior esquerdo da janela pai. Um aplicativo especifica o tamanho inicial e a posição de uma janela quando ele cria a janela, mas pode alterar o tamanho e a posição da janela a qualquer momento. Para obter mais informações, consulte [preenchimento de formas](../gdi/filled-shapes.md).

Esta seção contém os seguintes tópicos:

-   [Tamanho e posição padrão](#default-size-and-position)
-   [Tamanho do rastreamento](#tracking-size)
-   [Comandos do sistema](#system-commands)
-   [Funções de tamanho e posição](#size-and-position-functions)
-   [Mensagens de tamanho e posição](#size-and-position-messages)

### <a name="default-size-and-position"></a>Tamanho e posição padrão

Um aplicativo pode permitir que o sistema calcule o tamanho inicial ou a posição de uma janela de nível superior especificando o peso \_ USEDEFAULT em [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa). Se o aplicativo definir as coordenadas da janela para USEDEFAULT de peso variável \_ e não tiver criado nenhuma outra janela de nível superior, o sistema definirá a posição da nova e em relação ao canto superior esquerdo da tela; caso contrário, ele definirá a posição em relação à posição da janela de nível superior que o aplicativo criou mais recentemente. Se os parâmetros Width e Height forem definidos como \_ USEDEFAULT CW, o sistema calculará o tamanho da nova janela. Se o aplicativo tiver criado outras janelas de nível superior, o sistema baseará o tamanho da nova janela no tamanho da janela de nível superior criada mais recentemente do aplicativo. Especificar \_ USEDEFAULT de PV ao criar uma janela filho ou pop-up faz com que o sistema defina o tamanho da janela para o tamanho mínimo padrão da janela.

### <a name="tracking-size"></a>Tamanho do rastreamento

O sistema mantém um tamanho de rastreamento mínimo e máximo para uma janela do estilo [**WS \_ THICKFRAME**](window-styles.md) ; uma janela com esse estilo tem uma borda de dimensionamento. O *tamanho mínimo de rastreamento* é o menor tamanho de janela que você pode produzir arrastando a borda de dimensionamento da janela. Da mesma forma, o *tamanho máximo de rastreamento* é o maior tamanho de janela que você pode produzir arrastando a borda de dimensionamento.

Os tamanhos de rastreamento mínimo e máximo de uma janela são definidos como valores padrão definidos pelo sistema quando o sistema cria a janela. Um aplicativo pode descobrir os padrões e substituí-los processando a mensagem do [**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) . Para obter mais informações, consulte [as mensagens de tamanho e posição](#size-and-position-messages).

### <a name="system-commands"></a>Comandos do sistema

Um aplicativo que tem um menu de janela pode alterar o tamanho e a posição dessa janela enviando comandos do sistema. Comandos do sistema são gerados quando o usuário escolhe comandos no menu janela. Um aplicativo pode emular a ação do usuário enviando uma mensagem do [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md) para a janela. Os comandos do sistema a seguir afetam o tamanho e a posição de uma janela.



| Comando      | Descrição                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SC \_ Close    | Fecha a janela. Esse comando envia uma mensagem de [**\_ fechamento do WM**](wm-close.md) para a janela. A janela executa todas as etapas necessárias para limpar e destruir a si mesma. |
| \_maximize SC | Maximiza a janela.                                                                                                                                                |
| \_minimizar SC | Minimiza a janela.                                                                                                                                                |
| \_mover SC     | Move a janela.                                                                                                                                                    |
| restauração do SC \_  | Restaura uma janela minimizada ou maximizada para seu tamanho e posição anteriores.                                                                                          |
| tamanho de SC \_     | Inicia um comando de tamanho. Para alterar o tamanho da janela, use o mouse ou o teclado.                                                                                  |



 

### <a name="size-and-position-functions"></a>Funções de tamanho e posição

Depois de criar uma janela, um aplicativo pode definir o tamanho ou a posição da janela chamando uma das várias funções diferentes, incluindo [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement), [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow), [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)e [**DeferWindowPos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos). **SetWindowPlacement** define a posição minimizada de uma janela, a posição maximizada, o tamanho e a posição restaurados e o estado de exibição. As funções **MoveWindow** e **SetWindowPos** são semelhantes; ambos definem o tamanho ou a posição de uma janela de aplicativo único. A função **SetWindowPos** inclui um conjunto de sinalizadores que afetam o estado de exibição da janela; **MoveWindow** não inclui esses sinalizadores. Use as funções [**BeginDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-begindeferwindowpos), **DeferWindowPos** e [**EndDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos) para definir simultaneamente a posição de um número de janelas, incluindo o tamanho, a posição, a posição na ordem z e o estado de exibição.

Um aplicativo pode recuperar as coordenadas do retângulo delimitador de uma janela usando a função [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) . **GetWindowRect** preenche uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) com as coordenadas dos cantos superior esquerdo da janela e inferior direito. As coordenadas são relativas ao canto superior esquerdo da tela, mesmo para uma janela filho. A função [**ScreenToClient**](/windows/win32/api/winuser/nf-winuser-screentoclient) ou [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) mapeia as coordenadas de tela do retângulo delimitador de uma janela filho para coordenar em relação à área do cliente da janela pai.

A função [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) recupera as coordenadas de uma área do cliente da janela. **GetClientRect** preenche uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) com as coordenadas dos cantos superior esquerdo e inferior direito da área do cliente, mas as coordenadas são relativas à própria área do cliente. Isso significa que as coordenadas do canto superior esquerdo da área do cliente são sempre (0, 0) e as coordenadas do canto inferior direito são a largura e a altura da área do cliente.

A função [**CascadeWindows**](/windows/win32/api/winuser/nf-winuser-cascadewindows) em cascata as janelas na área de trabalho ou em cascata as janelas filhas da janela pai especificada. A função [**TileWindows**](/windows/win32/api/winuser/nf-winuser-tilewindows) organiza as janelas na área de trabalho ou organiza as janelas filhas da janela pai especificada.

### <a name="size-and-position-messages"></a>Mensagens de tamanho e posição

O sistema envia a mensagem do [**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) para uma janela cujo tamanho ou posição está prestes a ser alterado. Por exemplo, a mensagem é enviada quando o usuário clica em **mover** ou **dimensionar** no menu janela ou clica na borda de dimensionamento ou na barra de título; a mensagem também é enviada quando um aplicativo chama [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) para mover ou dimensionar a janela. **WM \_ GETMINMAXINFO** inclui um ponteiro para uma estrutura [**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) que contém o tamanho e a posição maximizados padrão para a janela, bem como os tamanhos de rastreamento mínimo e máximo padrão. Um aplicativo pode substituir os padrões processando o **WM \_ GETMINMAXINFO** e definindo os membros apropriados de **MINMAXINFO**. Uma janela deve ter o estilo de **\_ legenda** [**WS \_ THICKFRAME**](window-styles.md) ou WS para receber o **WM \_ GETMINMAXINFO**. Uma janela com o estilo **WS \_ THICKFRAME** recebe essa mensagem durante o processo de criação de janela, bem como quando ela está sendo movida ou dimensionada.

O sistema envia a mensagem do [**WM \_ WINDOWPOSCHANGING**](wm-windowposchanging.md) para uma janela cujo tamanho, posição, posição na ordem z ou mostrar estado está prestes a ser alterado. Essa mensagem inclui um ponteiro para uma estrutura [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) que especifica o novo tamanho, a posição, a posição da janela na ordem z e o estado de exibição. Ao definir os membros de **WINDOWPOS**, um aplicativo pode afetar o novo tamanho, a posição e a aparência da janela.

Depois de alterar o tamanho, a posição, a posição da janela na ordem z ou mostrar o estado, o sistema envia a mensagem [**\_ WINDOWPOSCHANGED do WM**](wm-windowposchanged.md) para a janela. Essa mensagem inclui um ponteiro para [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) que informa a janela de seu novo tamanho, posição, posição na ordem z e o estado de exibição. Definir os membros da estrutura **WINDOWPOS** que é passada com o **WM \_ WINDOWPOSCHANGED** não tem nenhum efeito na janela. Uma janela que deve processar [**o \_ tamanho do WM**](wm-size.md) e mensagens de [**\_ movimentação do WM**](wm-move.md) deve passar o **WM \_ WINDOWPOSCHANGED** para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ; caso contrário, o sistema não enviará o **\_ tamanho do WM** e o **WM \_ moverá** as mensagens para a janela.

O sistema envia a mensagem do [**WM \_ NCCALCSIZE**](wm-nccalcsize.md) para uma janela quando a janela é criada ou dimensionada. O sistema usa a mensagem para calcular o tamanho da área do cliente da janela e a posição da área do cliente em relação ao canto superior esquerdo da janela. Uma janela normalmente passa essa mensagem para o procedimento de janela padrão; no entanto, essa mensagem pode ser útil em aplicativos que personalizam a área não cliente de uma janela ou preservam partes da área do cliente quando a janela é dimensionada. Para obter mais informações, consulte [pintando e desenhando](../gdi/painting-and-drawing.md).

## <a name="window-animation"></a>Animação de janela

Você pode produzir efeitos especiais ao mostrar ou ocultar o Windows usando a função [**AnimateWindow**](/windows/win32/api/winuser/nf-winuser-animatewindow) . Quando a janela é animada dessa maneira, o sistema vai lançar, deslizar ou esmaecer a janela, dependendo dos sinalizadores que você especificar em uma chamada para **AnimateWindow**.

Por padrão, o sistema usa o *rolo de animação*. Com esse efeito, a janela parece ser revertida aberta (mostrando a janela) ou um rolo fechado (ocultando a janela). Você pode usar o parâmetro *dwFlags* para especificar se a janela é revertida horizontalmente, verticalmente ou diagonalmente.

Quando você especifica o sinalizador de **\_ Slide aw** , o sistema usa a *animação de slide*. Com esse efeito, a janela é exibida para deslizar para a exibição (mostrando a janela) ou deslizar para fora da exibição (ocultando a janela). Você pode usar o parâmetro *dwFlags* para especificar se a janela deslizará horizontalmente, verticalmente ou diagonalmente.

Quando você especifica o sinalizador de **\_ mistura de aw** , o sistema usa um *esmaecimento de mistura alfabética*.

Você também pode usar o sinalizador **aw \_ Center** para fazer uma janela aparecer para ser recolhida ou expandida para fora.

## <a name="window-layout-and-mirroring"></a>Layout e espelhamento de janela

O layout da janela define como os objetos Text e Windows Graphics Device Interface (GDI) são dispostos em uma janela ou em um contexto de dispositivo (DC). Algumas linguagens, como Inglês, francês e alemão, exigem um layout da esquerda para a direita (LTR). Outras linguagens, como árabe e Hebraico, exigem layout da direita para a esquerda (RTL). O layout da janela aplica-se ao texto, mas também afeta os outros elementos GDI da janela, incluindo bitmaps, ícones, o local da origem, os botões, os controles de árvore em cascata e se a coordenada horizontal aumenta à medida que você passa para a esquerda ou para a direita. Por exemplo, depois que um aplicativo tiver definido o layout RTL, a origem será posicionada na borda direita da janela ou do dispositivo, e o número que representa a coordenada horizontal aumentará à medida que você mover para a esquerda. No entanto, nem todos os objetos são afetados pelo layout de uma janela. Por exemplo, o layout de caixas de diálogo, caixas de mensagem e contextos de dispositivo que não estão associados a uma janela, como controladores de metarquivo e de impressora, devem ser tratados separadamente. As especificações para elas são mencionadas posteriormente neste tópico.

As funções de janela permitem que você especifique ou altere o layout da janela nas versões árabe e Hebraico do Windows. Observe que não há suporte para a alteração para um layout RTL (também conhecido como espelhamento) para Windows que têm o estilo [cs \_ OWNDC](about-window-classes.md) ou para um DC com o \_ modo gráfico do GM Advanced.

Por padrão, o layout da janela é da esquerda para a direita (EPD). Para definir o layout da janela RTL, chame [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) com o estilo **WS \_ ex \_ LAYOUTRTL**. Também por padrão, uma janela filho (ou seja, uma criada com o [**estilo \_ filho WS**](window-styles.md) e com um parâmetro pai *HWND* válido na chamada para [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou **CreateWindowEx**) tem o mesmo layout que seu pai. Para desabilitar a herança de espelhamento para todas as janelas filhas, especifique **WS \_ ex \_ NOINHERITLAYOUT** na chamada para **CreateWindowEx**. Observe que o espelhamento não é herdado por janelas de propriedade (aquelas criadas sem o estilo de **WS \_ filho** ) ou aqueles criados com o parâmetro pai *HWND* em **CreateWindowEx** definido como **NULL**. Para desabilitar a herança de espelhamento para uma janela individual, processe a mensagem do [**WM \_ NCCREATE**](wm-nccreate.md) com [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) e [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) para desativar o sinalizador **WS \_ ex \_ LAYOUTRTL** . Esse processamento é além de qualquer outro processamento necessário. O fragmento de código a seguir mostra como isso é feito.


```
SetWindowLong (hWnd, 
               GWL_EXSTYLE, 
               GetWindowLong(hWnd,GWL_EXSTYLE) & ~WS_EX_LAYOUTRTL))
```



Você pode definir o layout padrão como RTL chamando [**SetProcessDefaultLayout**](/windows/win32/api/winuser/nf-winuser-setprocessdefaultlayout)(layout \_ DPE). Todas as janelas criadas após a chamada serão espelhadas, mas as janelas existentes não serão afetadas. Para desativar o espelhamento padrão, chame **SetProcessDefaultLayout**(0).

Observe que o [**SetProcessDefaultLayout**](/windows/win32/api/winuser/nf-winuser-setprocessdefaultlayout) espelha os DCS somente de janelas espelhadas. Para espelhar qualquer DC, chame [**SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout)(hDC, layout \_ DPE). Para obter mais informações, consulte a discussão sobre contextos de dispositivo de espelhamento não associados ao Windows, que vem mais adiante neste tópico.

Bitmaps e ícones em uma janela espelhada também são espelhados por padrão. No entanto, nem todos eles devem ser espelhados. Por exemplo, aqueles com texto, um logotipo de negócios ou um relógio analógico não devem ser espelhados. Para desabilitar o espelhamento de bitmaps, chame [**SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout) com o \_ conjunto de bits BITMAPORIENTATIONPRESERVED de layout em *dwLayout*. Para desabilitar o espelhamento em um DC, chame **SetLayout**(hDC, 0).

Para consultar o layout padrão atual, chame [**GetProcessDefaultLayout**](/windows/win32/api/winuser/nf-winuser-getprocessdefaultlayout). Após um retorno bem-sucedido, *pdwDefaultLayout* contém layout \_ DPE ou 0. Para consultar as configurações de layout do contexto do dispositivo, chame [**GetLayout**](/windows/win32/api/wingdi/nf-wingdi-getlayout). Após um retorno bem-sucedido, **GetLayout** retorna um **DWORD** que indica as configurações de LAYOUT pelas configurações do LAYOUT \_ DPE e o layout \_ BITMAPORIENTATIONPRESERVED bits.

Após a criação de uma janela, você altera o layout usando a função [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) . Por exemplo, isso é necessário quando o usuário altera o idioma da interface do usuário de uma janela existente de árabe ou hebraico para alemão. No entanto, ao alterar o layout de uma janela existente, você deve invalidar e atualizar a janela para garantir que o conteúdo da janela seja todos desenhados no mesmo layout. O exemplo de código a seguir é de código de exemplo que altera o layout da janela conforme necessário:


```
// Using ANSI versions of GetWindowLong and SetWindowLong because Unicode
// is not needed for these calls

lExStyles = GetWindowLongA(hWnd, GWL_EXSTYLE);

// Check whether new layout is opposite the current layout
if (!!(pLState -> IsRTLLayout) != !!(lExStyles & WS_EX_LAYOUTRTL))
{
    // the following lines will update the window layout

    lExStyles ^= WS_EX_LAYOUTRTL;        // toggle layout
    SetWindowLongA(hWnd, GWL_EXSTYLE, lExStyles);
    InvalidateRect(hWnd, NULL, TRUE);    // to update layout in the client area
}
```



No espelhamento, você deve imaginar em termos de "Near" e "Far" em vez de "Left" e "Right". A falha em fazer isso pode causar problemas. Uma prática de codificação comum que causa problemas em uma janela espelhada ocorre ao mapear entre coordenadas de tela e coordenadas de cliente. Por exemplo, os aplicativos geralmente usam código semelhante ao seguinte para posicionar um controle em uma janela:


```
// DO NOT USE THIS IF APPLICATION MIRRORS THE WINDOW

// get coordinates of the window in screen coordinates
GetWindowRect(hControl, (LPRECT) &rControlRect);  

// map screen coordinates to client coordinates in dialog
ScreenToClient(hDialog, (LPPOINT) &rControlRect.left); 
ScreenToClient(hDialog, (LPPOINT) &rControlRect.right);
```



Isso causa problemas no espelhamento porque a borda esquerda do retângulo se torna a borda direita em uma janela espelhada e vice-versa. Para evitar esse problema, substitua as chamadas [**ScreenToClient**](/windows/win32/api/winuser/nf-winuser-screentoclient) por uma chamada para [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) da seguinte maneira:


```
// USE THIS FOR MIRRORING

GetWindowRect(hControl, (LPRECT) &rControlRect);
MapWindowPoints(NULL, hDialog, (LPPOINT) &rControlRect, 2)
```



Esse código funciona porque, em plataformas que dão suporte a espelhamento, [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) é modificado para alternar as coordenadas de ponto esquerdo e direito quando a janela do cliente é espelhada. Para obter mais informações, consulte a seção comentários de **MapWindowPoints**.

Outra prática comum que pode causar problemas em janelas espelhadas é posicionar objetos em uma janela do cliente usando deslocamentos em coordenadas da tela em vez de coordenadas do cliente. Por exemplo, o código a seguir usa a diferença em coordenadas de tela como a posição x nas coordenadas do cliente para posicionar um controle em uma caixa de diálogo.


```
// OK if LTR layout and mapping mode of client is MM_TEXT,
// but WRONG for a mirrored dialog 

RECT rdDialog;
RECT rcControl;

HWND hControl = GetDlgItem(hDlg, IDD_CONTROL);
GetWindowRect(hDlg, &rcDialog);             // gets rect in screen coordinates
GetWindowRect(hControl, &rcControl);
MoveWindow(hControl,
           rcControl.left - rcDialog.left,  // uses x position in client coords
           rcControl.top - rcDialog.top,
           nWidth,
           nHeight,
           FALSE);
```



Esse código é bom quando a janela da caixa de diálogo tem layout da esquerda para a direita (LTR) e o modo de mapeamento do cliente é o \_ texto mm, pois a nova posição x nas coordenadas do cliente corresponde à diferença nas bordas esquerda do controle e na caixa de diálogo em coordenadas da tela. No entanto, em uma caixa de diálogo espelhada, esquerda e direita são revertidas, portanto, você deve usar [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) da seguinte maneira:


```
RECT rcDialog;
RECT rcControl;

HWND hControl - GetDlgItem(hDlg, IDD_CONTROL);
GetWindowRect(hControl, &rcControl);

// MapWindowPoints works correctly in both mirrored and non-mirrored windows.
MapWindowPoints(NULL, hDlg, (LPPOINT) &rcControl, 2);

// Now rcControl is in client coordinates.
MoveWindow(hControl, rcControl.left, rcControl.top, nWidth, nHeight, FALSE)
```



### <a name="mirroring-dialog-boxes-and-message-boxes"></a>Caixas de diálogo e caixas de mensagem de espelhamento

Caixas de diálogo e caixas de mensagem não herdam layout, portanto, você deve definir o layout explicitamente. Para espelhar uma caixa de mensagem, chame [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) ou [**MessageBoxEx**](/windows/win32/api/winuser/nf-winuser-messageboxexa) com a opção **MB \_ RTLREADING** . Para fazer o layout de uma caixa de diálogo da direita para a esquerda, use o estilo estendido WS \_ ex \_ LAYOUTRTL na estrutura do modelo de caixa de diálogo [**DLGTEMPLATEEX**](../dlgbox/dlgtemplateex.md). As folhas de propriedades são um caso especial de caixas de diálogo. Cada guia é tratada como uma caixa de diálogo separada, portanto, você precisa incluir o \_ estilo WS ex \_ LAYOUTRTL em cada guia que desejar espelhado.

### <a name="mirroring-device-contexts-not-associated-with-a-window"></a>Contextos de dispositivo de espelhamento não associados a uma janela

Os DCs que não estão associados a uma janela, como o metarquivo ou os DCs da impressora, não herdam o layout, portanto, você deve definir o layout explicitamente. Para alterar o layout do contexto do dispositivo, use a função [**SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout) .

A função [**SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout) é raramente usada com o Windows. Normalmente, o Windows recebe um controlador de domínio associado somente no processamento de uma mensagem de [**\_ pintura do WM**](../gdi/wm-paint.md) . Ocasionalmente, um programa cria um controlador de domínio para uma janela chamando [**GetDC**](/windows/win32/api/winuser/nf-winuser-getdc). De qualquer forma, o layout inicial para o DC é definido por [**BeginPaint**](/windows/win32/api/winuser/nf-winuser-beginpaint) ou **GetDC** de acordo com o \_ sinalizador WS ex LAYOUTRTL da janela \_ .

Os valores retornados por [**GetWindowOrgEx**](/windows/win32/api/wingdi/nf-wingdi-getwindoworgex), [**GetWindowExtEx**](/windows/win32/api/wingdi/nf-wingdi-getwindowextex), [**GetViewportOrgEx**](/windows/win32/api/wingdi/nf-wingdi-getviewportorgex) e [**GetViewportExtEx**](/windows/win32/api/wingdi/nf-wingdi-getviewportextex) não são afetados pela chamada de [**SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout).

Quando o layout é RTL, [**GetMapMode**](/windows/win32/api/wingdi/nf-wingdi-getmapmode) retornará mm \_ ANISOTROPIC em vez de \_ texto mm. Chamar [**SetMapMode**](/windows/win32/api/wingdi/nf-wingdi-setmapmode) com \_ texto mm funcionará corretamente; somente o valor de retorno de **GetMapMode** é afetado. Da mesma forma, chamar [**SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout)(hDC, layout \_ DPE) quando o modo de mapeamento é \_ texto mm faz com que o modo de mapeamento relatado mude para mm \_ ANISOTROPIC.

## <a name="window-destruction"></a>Destruição de janelas

Em geral, um aplicativo deve destruir todas as janelas que ele cria. Ele faz isso usando a função [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) . Quando uma janela for destruída, o sistema ocultará a janela, se ela estiver visível, e removerá todos os dados internos associados à janela. Isso invalida o identificador de janela, que não pode mais ser usado pelo aplicativo.

Um aplicativo destrói muitas das janelas que ele cria em breve depois de criá-las. Por exemplo, um aplicativo geralmente destrói uma janela da caixa de diálogo assim que o aplicativo tem uma entrada suficiente do usuário para continuar sua tarefa. Um aplicativo eventualmente destrói a janela principal do aplicativo (antes de encerrar).

Antes de destruir uma janela, um aplicativo deve salvar ou remover todos os dados associados à janela e deve liberar todos os recursos do sistema alocados para a janela. Se o aplicativo não liberar os recursos, o sistema liberará todos os recursos não liberados pelo aplicativo.

Destruir uma janela não afeta a classe de janela da qual a janela é criada. Novas janelas ainda podem ser criadas usando essa classe, e todas as janelas existentes dessa classe continuam a operar. Destruir uma janela também destrói as janelas descendentes da janela. A função [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) envia uma mensagem do [**WM \_ Destroy**](wm-destroy.md) primeiro para a janela e, em seguida, para suas janelas filhas e janelas descendentes. Dessa forma, todas as janelas descendentes da janela que está sendo destruída também são destruídas.

Uma janela com um menu janela recebe uma mensagem de [**\_ fechamento do WM**](wm-close.md) quando o usuário clica em **Fechar**. Ao processar essa mensagem, um aplicativo pode solicitar a confirmação do usuário antes de destruir a janela. Se o usuário confirmar que a janela deve ser destruída, o aplicativo poderá chamar a função [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) para destruir a janela.

Se a janela que está sendo destruída for a janela ativa, os Estados ativo e de foco serão transferidos para outra janela. A janela que se torna a janela ativa é a próxima janela, conforme determinado pela combinação de teclas ALT + ESC. A nova janela ativa determina qual janela recebe o foco do teclado.

 

 
