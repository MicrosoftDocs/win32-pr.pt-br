---
description: Aborda a nova funcionalidade da barra de tarefas, incluindo a consolidação de inicialização e alternância, recursos aprimorados de botões da barra de tarefas, como acesso de clique único a documentos e tarefas específicas do aplicativo, controles de transporte e notificações de status, representações de miniaturas e destinos de comutador com base em guias individuais em um aplicativo com guias e a capacidade de reordenar botões da barra de tarefas
ms.assetid: cbf2b07d-d67c-4755-888c-d40692d13cae
title: Extensões da barra de tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4df308d8045301b98937eb03af595d2e800921b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829701"
---
# <a name="taskbar-extensions"></a>Extensões da barra de tarefas

A partir do Windows 7, a barra de tarefas foi ampliada significativamente sob o princípio de orientação para obter os usuários onde eles estão indo de forma rápida e eficiente quanto possível. Para esse fim, as janelas de aplicativo, os arquivos e os comandos que o usuário precisa realizar que agora são centralizados em um único botão da barra de tarefas que consolida fontes de informações e controles anteriormente dispersos. Agora, um usuário pode encontrar tarefas comuns, arquivos recentes e frequentes, alertas, notificações de progresso e miniaturas para documentos ou guias individuais em um único lugar.

-   [Ativação e troca unificadas](#unified-launching-and-switching)
-   [Listas de atalhos](#jump-lists)
-   [Destinos](#destinations)
-   [Tarefas](#tasks)
-   [Personalizando listas de atalhos](#customizing-jump-lists)
-   [Barras de ferramentas de miniatura](#thumbnail-toolbars)
-   [Sobreposições de ícone](#icon-overlays)
-   [Barras de progresso](#progress-bars)
-   [Deskbands](#deskbands)
-   [Área de notificação](#notification-area)
-   [Miniaturas](#thumbnails)
-   [Tópicos relacionados](#related-topics)

## <a name="unified-launching-and-switching"></a>Ativação e troca unificadas

Na barra de tarefas do Windows 7, o início rápido não é mais uma barra de ferramentas separada. Os atalhos do iniciador que normalmente são incluídos agora estão fixados na própria barra de tarefas, misturados com botões para aplicativos em execução no momento. Quando um usuário inicia um aplicativo a partir de um atalho de iniciador fixado, o ícone é transformado no botão da barra de tarefas do aplicativo enquanto o aplicativo está em execução. Quando o usuário fecha o aplicativo, o botão reverte para o ícone. No entanto, o atalho do iniciador e o botão para o aplicativo em execução são apenas formas diferentes do botão da barra de tarefas do Windows 7.

![barra de tarefas do Windows 7](images/taskbar/taskbar.png)

Um pequeno conjunto de aplicativos é fixado por padrão para novas instalações. Além desses, somente o usuário pode fixar outros aplicativos; a fixação programática por um aplicativo não é permitida.

O recurso Mostrar área de trabalho do início rápido agora está localizado na barra de tarefas da extrema direita. Passar o mouse sobre essa área faz com que todas as janelas ativas se tornem transparentes, mostrando a área de trabalho. Clicar na área executa a ação familiar de minimizar todas as janelas e alternar para a área de trabalho.

Enquanto o aplicativo está em execução, seu botão da barra de tarefas se torna o único local para acessar todos os recursos a seguir, cada um discutido em detalhes abaixo.

-   [Tarefas](#tasks): comandos de aplicativo comuns, presentes mesmo quando o aplicativo não está em execução.
-   [Destinos](#destinations): arquivos recentemente e acessados com frequência específicos ao aplicativo.
-   [Miniaturas](#thumbnails): comutação de janela, incluindo destinos de switch para guias e documentos individuais.
-   [Barras de ferramentas de miniatura](#thumbnail-toolbars): controle de aplicativo básico da própria miniatura.
-   [Barras de progresso](#progress-bars) e [sobreposições de ícone](#icon-overlays): notificações de status.

O botão da barra de tarefas pode representar um iniciador, uma única janela de aplicativo ou um grupo. Um identificador conhecido como ID do modelo de usuário (AppUserModelID) do aplicativo é atribuído a cada grupo. Um AppUserModelID pode ser especificado para substituir o agrupamento da barra de tarefas padrão, o que permite que o Windows se torne membros do mesmo grupo quando eles podem não ser vistos de outra forma. Cada membro de um grupo recebe uma visualização separada no submenu de miniaturas que é mostrada quando o mouse passa sobre o botão da barra de tarefas do grupo. Observe que o agrupamento em si permanece opcional.

A partir do Windows 7, os botões da barra de tarefas agora podem ser reorganizados pelo usuário por meio de operações de arrastar e soltar.

> [!Note]  
> A pasta inicialização rápida ([* * * * FolderId \_ ](knownfolderid.md)início rápido * * * *) ainda está disponível para compatibilidade com versões anteriores, embora não haja mais uma interface do usuário de início rápido. No entanto, novos aplicativos não devem pedir para adicionar um ícone ao início rápido durante a instalação.

 

Para obter mais informações, consulte [IDs de modelo de usuário de aplicativo (AppUserModelIDs)](appids.md).

## <a name="jump-lists"></a>Listas de atalhos

Normalmente, um usuário inicia um programa com a intenção de acessar um documento ou executar tarefas dentro do programa. O usuário de um programa de jogo pode querer chegar a um jogo salvo ou ser iniciado como um caractere específico em vez de reiniciar um jogo desde o início. Para obter os usuários com mais eficiência para sua meta final, uma lista de [destinos](#destinations) e [tarefas](#tasks) comuns associadas a um aplicativo é anexada ao botão da barra de tarefas desse aplicativo (bem como à entrada equivalente do menu **Iniciar** ). Esta é a lista de atalhos do aplicativo. A lista de atalhos está disponível se o botão da barra de tarefas está em um estado iniciador (o aplicativo não está em execução) ou se representa uma ou mais janelas. Clicar com o botão direito do mouse no botão da barra de tarefas mostra a lista de atalhos do aplicativo, conforme mostrado na ilustração a seguir.

![lista de atalhos com categorias fixas, frequentes e tarefas](images/taskbar/jumplist.png)

Por padrão, uma lista de atalhos padrão contém duas categorias: itens recentes e itens fixados, embora porque apenas categorias com conteúdo são mostradas na interface do usuário, nenhuma dessas categorias é mostrada na primeira inicialização. Sempre presente é um ícone de inicialização de aplicativo (para iniciar mais instâncias do aplicativo), uma opção para fixar ou desafixar o aplicativo da barra de tarefas e um comando **fechar** para qualquer janela aberta.

## <a name="destinations"></a>Destinos

As categorias **recentes** e **frequentes** são consideradas para conter destinos. Um destino, geralmente um arquivo, um documento ou uma URL, é algo que pode ser editado, navegado, exibido e assim por diante. Imagine um destino como algo em vez de uma ação. Normalmente, um destino é um item no namespace do Shell, representado por um [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) ou [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka). Essas partes da lista de destino são análogas à lista de documentos usados recentemente do menu **Iniciar** (não são mais mostrados por padrão) e à lista de aplicativos usados com frequência, mas são específicas a um aplicativo e, portanto, mais precisas e úteis para o usuário. Os resultados usados na lista de destino são calculados por meio de chamadas para [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs). Observe que quando o usuário abre um arquivo do Windows Explorer ou usa a caixa de diálogo arquivo comum para abrir, salvar ou criar um arquivo, o **SHAddToRecentDocs** é chamado para você automaticamente, o que resulta em muitos aplicativos que obtêm seus itens recentes mostrados na lista de destino sem nenhuma ação de sua parte.

Iniciar um destino é muito semelhante a iniciar um item usando o comando **abrir com** . O aplicativo é iniciado com esse destino carregado e pronto para uso. Os itens na lista de destino também podem ser arrastados da lista para um destino de soltar, como uma mensagem de email. Ao fazer com que esses itens sejam centralizados em uma lista de destino, ele obtém os usuários onde desejam fazer isso muito mais rápido, que é o objetivo.

À medida que os itens aparecem na categoria **recente** de uma lista de destino (ou na categoria **frequente** ou em uma [categoria personalizada](#customizing-jump-lists) , conforme discutido em uma seção posterior), um usuário pode querer garantir que o item esteja sempre na lista para acesso rápido. Para fazer isso, ele pode fixar o item na lista, o que adiciona o item à categoria **fixada** . Quando um usuário está trabalhando ativamente com um destino, ele deseja facilmente em mãos e, portanto, o fixaria na lista de destino do aplicativo. Após a conclusão do trabalho do usuário, ele simplesmente desafixa o item. Esse controle de usuário mantém a lista organizada e relevante.

Uma lista de destino pode ser considerada como uma versão específica do aplicativo do menu **Iniciar** . Uma lista de destino não é um menu de atalho. Cada item em uma lista de destino pode ser clicado com o botão direito do mouse para seu próprio menu de atalho.

### <a name="apis"></a>APIs

-   [**IApplicationDestinations::RemoveDestination**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-removedestination)
-   [**IApplicationDestinations::RemoveAllDestinations**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-removealldestinations)
-   [**IApplicationDocumentLists:: GetList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist)
-   [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)

## <a name="tasks"></a>Tarefas

Outra parte interna de uma lista de atalhos é a categoria de **tarefas** . Embora um destino seja algo, uma tarefa é uma ação e, nesse caso, é uma ação específica do aplicativo. Em outras palavras, um destino é um substantivo e uma tarefa é um verbo. Normalmente, as tarefas são itens [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) com argumentos de linha de comando que indicam funcionalidades específicas que podem ser disparadas por um aplicativo. Mais uma vez, a ideia é centralizar a quantidade de informações relacionadas a um aplicativo, como é prático.

Os aplicativos definem tarefas com base nos recursos do programa e as principais coisas que um usuário deve fazer com eles. As tarefas devem ser livres de contexto, pois o aplicativo não precisa estar em execução para que elas funcionem. Elas também devem ser as ações mais comuns estatisticamente que um usuário normal executaria em um aplicativo, como compor uma mensagem de email ou abrir o calendário em um programa de email, criar um novo documento em um processador de texto, iniciar um aplicativo em um determinado modo ou iniciar um de seus subcomandos. Um aplicativo não deve obstruir o menu com recursos avançados que os usuários padrão não precisarão ou ações de uso único, como registro. Não use tarefas para itens promocionais, como atualizações ou ofertas especiais.

É altamente recomendável que a lista de tarefas seja estática. Ele deve permanecer o mesmo, independentemente do Estado ou do status do aplicativo. Embora seja possível variar a lista dinamicamente, você deve considerar que isso pode confundir o usuário que não espera que parte da lista de destino seja alterada.

### <a name="apis"></a>APIs

-   [**ICustomDestinationList::AddUserTasks**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-addusertasks)

## <a name="customizing-jump-lists"></a>Personalizando listas de atalhos

Um aplicativo pode definir suas próprias categorias e adicioná-las, além de ou no lugar das categorias padrão **recentes** e **frequentes** em uma lista de atalhos. O aplicativo pode controlar seus próprios destinos nessas categorias personalizadas com base na arquitetura do aplicativo e no uso pretendido. A captura de tela a seguir mostra uma lista de atalhos personalizada com uma categoria de histórico.

![lista de atalhos personalizada](images/taskbar/customjumplist.png)

Se um aplicativo decidir fornecer uma categoria personalizada, esse aplicativo assumirá a responsabilidade de preenchê-la. O conteúdo da categoria ainda deve ser específico do usuário e com base no histórico do usuário, em ações ou em ambos, mas por meio de uma categoria personalizada, um aplicativo pode determinar o que ele deseja controlar e o que ele deseja ignorar, talvez com base em uma opção de aplicativo. Por exemplo, um programa de áudio pode optar por incluir apenas álbuns reproduzidos recentemente e ignorar faixas individuais reproduzidas recentemente.

Se um usuário tiver removido um item da lista, que é sempre uma opção de usuário, o aplicativo deverá honrar isso. O aplicativo também deve garantir que os itens na lista sejam válidos ou que falhem normalmente se tiverem sido excluídos. Itens individuais ou todo o conteúdo da lista pode ser removido de forma programática.

O número máximo de itens em uma lista de destino é determinado pelo sistema com base em vários fatores, como resolução de exibição e tamanho da fonte. Se não houver espaço suficiente para todos os itens em todas as categorias, eles serão truncados de baixo para cima.

### <a name="apis"></a>APIs

-   [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)
-   [**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations)
-   [**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)

## <a name="thumbnail-toolbars"></a>Barras de ferramentas de miniatura

Para fornecer acesso a comandos de chave de uma janela específica sem fazer com que o usuário restaure ou ative a janela do aplicativo, um controle da barra de ferramentas ativa pode ser inserido na visualização em miniatura da janela. Por exemplo, o Windows Media Player pode oferecer controles de transporte de mídia padrão, como reproduzir, pausar, ativar mudo e parar. A interface do usuário exibe essa barra de ferramentas diretamente abaixo da miniatura, conforme mostrado na ilustração a seguir, que não cobre nenhuma parte dela.

![barra de tarefas de miniatura do Windows Media Player, com três botões: voltar, reproduzir e avançar](images/taskbar/thumbbar.png)

Essa barra de ferramentas é simplesmente o conhecido controle comum da barra de ferramentas padrão. Ele tem um máximo de sete botões. A ID, a imagem, a dica de ferramenta e o estado de cada botão são definidos em uma estrutura, que é passada para a barra de tarefas. O aplicativo pode mostrar, habilitar, desabilitar ou ocultar botões da barra de ferramentas de miniatura conforme exigido pelo seu estado atual.

Como há espaço limitado para exibir miniaturas e um número variável de miniaturas a serem exibidas, os aplicativos não têm garantia de um tamanho de barra de ferramentas específico. Se o espaço for restrito, os botões na barra de ferramentas serão truncados da direita para a esquerda. Portanto, ao projetar sua barra de ferramentas, você deve priorizar os comandos associados aos seus botões e garantir que o mais importante venha primeiro e que seja menos provável de ser descartado devido a problemas de espaço.

> [!Note]  
> Quando um aplicativo exibe uma janela, seu botão da barra de tarefas é criado pelo sistema. Quando o botão estiver em vigor, a barra de tarefas enviará uma mensagem **TaskbarButtonCreated** para a janela. Seu valor é calculado chamando [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)(L ("TaskbarButtonCreated")). Essa mensagem deve ser recebida pelo seu aplicativo antes de chamar qualquer método [**ITaskbarList3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3) .

 

### <a name="api"></a>API

-   [**ITaskbarList3::ThumbBarAddButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons)
-   [**ITaskbarList3::ThumbBarSetImageList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist)
-   [**ITaskbarList3::ThumbBarUpdateButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarupdatebuttons)
-   [**THUMBBUTTON**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton)

## <a name="icon-overlays"></a>Sobreposições de ícone

Um aplicativo pode comunicar determinadas notificações e status ao usuário por meio de seu botão da barra de tarefas pela exibição de sobreposições pequenas no botão. Essas sobreposições são semelhantes ao tipo de sobreposição existente usado para atalhos ou notificações de segurança, exibidos no canto inferior direito do botão. Para exibir um ícone de sobreposição, a barra de tarefas deve estar no modo de ícone grande padrão, conforme mostrado na captura de tela a seguir.

![botão da barra de tarefas do Windows Messenger com uma sobreposição para indicar um status disponível](images/taskbar/taskbaroverlay.png)

As sobreposições de ícone servem como uma notificação contextual de status e destinam-se a negar a necessidade de um ícone de status de área de notificação separado para comunicar essas informações ao usuário. Por exemplo, o novo status de email no Microsoft Outlook, atualmente mostrado na área de notificação, agora pode ser indicado por meio de uma sobreposição no botão da barra de tarefas. Novamente, você deve decidir durante o ciclo de desenvolvimento qual método é melhor para seu aplicativo. Os ícones de sobreposição destinam-se a fornecer status ou notificações importantes, duradouras, como status da rede, status do Messenger ou novo email. O usuário não deve ser apresentado com sobreposições ou animações em constante alteração.

Como uma única sobreposição é sobreposta no botão da barra de tarefas e não nas miniaturas de janela individuais, esse é um recurso por grupo, em vez de por janela. As solicitações de ícones de sobreposição podem ser recebidas de janelas individuais em um grupo da barra de tarefas, mas não são enfileiradas. A última sobreposição recebida é a sobreposição mostrada.

### <a name="apis"></a>APIs

-   [**ITaskbarList3::SetOverlayIcon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon)

## <a name="progress-bars"></a>Barras de progresso

Um botão da barra de tarefas pode ser usado para exibir uma barra de progresso. Isso permite que uma janela forneça informações de progresso ao usuário sem que o usuário precise alternar para a própria janela. O usuário pode permanecer produtivo em outro aplicativo, observando rapidamente o progresso de uma ou mais operações que ocorrem em outras janelas. O objetivo é que uma barra de progresso em um botão da barra de tarefas reflita um indicador de progresso mais detalhado na própria janela. Esse recurso pode ser usado para rastrear cópias de arquivos, downloads, instalações, gravação de mídia ou qualquer operação que vai levar um período de tempo. Esse recurso não se destina ao uso com ações de periféricos normalmente, como o carregamento de uma página da Web ou a impressão de um documento. Esse tipo de progresso deve continuar a ser mostrado na barra de status da janela.

A barra de progresso do botão da barra de tarefas é uma experiência semelhante ao controle de barra de progresso familiar. Ele pode exibir o progresso de destérmino com base em um percentual concluído da operação ou em um progresso de estilo de letreiro indeterminado para indicar que a operação está em andamento sem qualquer previsão do tempo restante. Ele também pode mostrar que a operação está em pausa ou encontrou um erro e requer a intervenção do usuário.

### <a name="apis"></a>APIs

-   [**ITaskbarList3:: SetProgressState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate)
-   [**ITaskbarList3:: setprogridevalue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue)

## <a name="deskbands"></a>Deskbands

Em versões do Windows anteriores ao Windows 7, algo semelhante à funcionalidade da barra de ferramentas de miniatura poderia ser obtido por meio de um Deskband — uma barra de ferramentas hospedada na barra de tarefas. Por exemplo, o Windows Media Player pode minimizar para a barra de tarefas como um conjunto de controles de transporte em vez de um botão padrão. No Windows 7, a deskbands ainda pode ser implementada e as barras de ferramentas de miniatura não se destinam a substituir todas elas. Nem todos os aplicativos se prestarão a uma barra de ferramentas de miniatura, e outra solução como uma Deskband ou uma tarefa em uma lista de destino pode ser a resposta certa para seu aplicativo; Você deve decidir qual solução funciona melhor para seu aplicativo como parte do seu ciclo de desenvolvimento. No entanto, lembre-se de que o deskbands deve dar suporte ao Windows Aero com Translucency ("vidro") habilitado e a interface [**IDeskBand2**](/windows/desktop/api/Shobjidl/nn-shobjidl-ideskband2) .

### <a name="apis"></a>APIs

-   [**IDeskBand2**](/windows/desktop/api/Shobjidl/nn-shobjidl-ideskband2)

## <a name="notification-area"></a>Área de notificação

Houve alterações na área de notificação que dão ao usuário muito mais controle sobre quais ícones aparecem na barra de tarefas. Todos os ícones de notificação agora ficam ocultos por padrão e essa visibilidade não pode ser controlada de forma programática. Somente o usuário tem permissão para escolher quais ícones de notificação aparecem na barra de tarefas. Quando um balão de notificação é exibido, o ícone torna-se temporariamente visível, mas, mesmo depois, um usuário pode optar por silenciar. Uma sobreposição de ícone em um botão da barra de tarefas, portanto, se torna uma opção atraente quando você deseja que seu aplicativo comunique essas informações para os usuários.

## <a name="thumbnails"></a>Miniaturas

No Windows Vista, passar o mouse sobre o botão da barra de tarefas de um aplicativo exibe uma miniatura que representa a janela em execução. Se a barra de tarefas tiver recolhido as janelas do aplicativo, a miniatura representará isso aparecendo como uma pilha, mas apenas a janela ativa será mostrada na própria miniatura.

No Windows 7, cada membro de um grupo é mostrado como uma miniatura separada e agora é também um destino de switch. Um aplicativo pode definir seus filhos (como janelas filho verdadeiras, documentos individuais ou guias) e fornecer miniaturas correspondentes para cada uma dessas janelas, mesmo quando elas normalmente não aparecem na barra de tarefas. Isso permite que os usuários alternem diretamente para a exibição do aplicativo desejado em vez de alternar para o aplicativo e, em seguida, alternar para o destino. Por exemplo, aplicativos de interface de/tabbed-Document (MDI) (interface de vários documentos) podem ter cada documento ou guia exibidos como uma miniatura separada e um destino de comutador quando o mouse passa sobre o botão da barra de tarefas de um grupo.

![três miniaturas da barra de tarefas que representam guias individuais no Windows Internet Explorer](images/taskbar/taskbarthumbnails.png)

> [!Note]  
> Como no Windows Vista, o Aero deve estar ativo para exibir miniaturas.

 

### <a name="api"></a>API

-   [**ITaskbarList3::RegisterTab**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-registertab)
-   [**ITaskbarList3::SetTabActive**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settabactive)
-   [**ITaskbarList3::SetTabOrder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settaborder)
-   [**ITaskbarList3::UnregisterTab**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-unregistertab)
-   [**ITaskbarList4::SetTabProperties**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist4-settabproperties)

As representações em miniatura do Windows são normalmente automáticas, mas nos casos em que o resultado não é ideal, a miniatura pode ser especificada explicitamente. Por padrão, somente as janelas de nível superior têm uma miniatura gerada automaticamente para elas e as miniaturas das janelas filhas aparecem como uma representação genérica. Isso pode resultar em uma experiência menor do que o ideal (e até mesmo confusa) para o usuário final. Uma miniatura de destino de comutador específica para cada janela filho, por exemplo, fornece uma experiência de usuário muito melhor.

### <a name="api"></a>API

-   [**DwmSetWindowAttribute**](/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)
-   [**DwmSetIconicThumbnail**](/windows/win32/api/dwmapi/nf-dwmapi-dwmseticonicthumbnail)
-   [**DwmSetIconicLivePreviewBitmap**](/windows/win32/api/dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap)
-   [**DwmInvalidateIconicBitmaps**](/windows/win32/api/dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
-   [**DWMSENDICONICTHUMBNAIL do WM \_**](../dwm/wm-dwmsendiconicthumbnail.md)
-   [**DWMSENDICONICLIVEPREVIEWBITMAP do WM \_**](../dwm/wm-dwmsendiconiclivepreviewbitmap.md)

Você pode selecionar uma área específica da janela para usar como miniatura. Isso pode ser útil quando um aplicativo sabe que seus documentos ou guias serão semelhantes quando forem exibidos em tamanho de miniatura. O aplicativo pode optar por mostrar apenas a parte de sua área de cliente que o usuário pode usar para distinguir entre miniaturas. No entanto, passar o mouse sobre qualquer miniatura exibe uma exibição da janela completa por trás dela para que o usuário possa rapidamente resumir as mesmas.

Se houver mais miniaturas que podem ser exibidas, a visualização será revertida para a miniatura herdada ou para um ícone padrão.

### <a name="api"></a>API

-   [**ITaskbarList3::SetThumbnailClip**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setthumbnailclip)

Para adicionar **PIN à barra de tarefas** ao menu de atalho de um item, que normalmente é necessário apenas para tipos de arquivo que incluem a entrada [IsShortcut](./links.md) , é feito registrando o manipulador de menu de contexto apropriado. Isso também se aplica ao **menu iniciar no pino**. Consulte [Registrando manipuladores de extensão de shell](reg-shell-exts.md) para obter mais informações.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[A barra de tarefas](taskbar.md)
</dt> <dt>

[IDs de modelo de usuário de aplicativo (AppUserModelIDs)](appids.md)
</dt> <dt>

[Notificações e a área de notificação](notification-area.md)
</dt> </dl>

 

 
