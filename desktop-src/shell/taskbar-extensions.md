---
description: Discute a nova funcionalidade da barra de tarefas, incluindo a consolidação de iniciar e alternar, recursos aprimorados de botões da barra de tarefas, como acesso a documentos e tarefas específicas do aplicativo, controles de transporte e notificações de status, representações em miniatura e destinos de comutadores com base em guias individuais em um aplicativo com guias e a capacidade de reordenar botões da barra de tarefas por meio de uma operação do tipo "arrastar e soltar".
ms.assetid: cbf2b07d-d67c-4755-888c-d40692d13cae
title: Extensões da barra de tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92cb8f100da2c7b5173319c25369a0ada7284b2ff5f4adbfe9b519c0ee96485
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773746"
---
# <a name="taskbar-extensions"></a>Extensões da barra de tarefas

A partir Windows 7, a barra de tarefas foi estendida significativamente sob o princípio orientador de levar os usuários para onde eles estão indo o mais rápido e eficiente possível. Para isso, as janelas, arquivos e comandos do aplicativo que o usuário precisa realizar agora estão centralizados em um único botão de barra de tarefas que consolida fontes de informações e controles dispersos anteriormente. Agora, um usuário pode encontrar tarefas comuns, arquivos recentes e frequentes, alertas, notificações de progresso e miniaturas para documentos ou guias individuais em um único lugar.

-   [Iniciando e alternando unificados](#unified-launching-and-switching)
-   [Listas de saltos](#jump-lists)
-   [Destinos](#destinations)
-   [Tarefas](#tasks)
-   [Personalização de listas de saltos](#customizing-jump-lists)
-   [Barras de ferramentas em miniatura](#thumbnail-toolbars)
-   [Sobreposições de ícone](#icon-overlays)
-   [Barras de progresso](#progress-bars)
-   [Faixas de mesa](#deskbands)
-   [Área de notificação](#notification-area)
-   [Miniaturas](#thumbnails)
-   [Tópicos relacionados](#related-topics)

## <a name="unified-launching-and-switching"></a>Iniciando e alternando unificados

A partir da barra Windows 7, o Início Rápido não é mais uma barra de ferramentas separada. Os atalhos do launcher que Início Rápido normalmente contidos agora são fixados na própria barra de tarefas, mesclados com botões para aplicativos em execução no momento. Quando um usuário inicia um aplicativo de um atalho fixado do iniciador, o ícone se transforma no botão da barra de tarefas do aplicativo enquanto o aplicativo estiver em execução. Quando o usuário fecha o aplicativo, o botão volta para o ícone. No entanto, o atalho do launcher e o botão para o aplicativo em execução são apenas formas diferentes do botão da barra de tarefas Windows 7.

![barra de tarefas do Windows 7](images/taskbar/taskbar.png)

Um pequeno conjunto de aplicativos é fixado por padrão para novas instalações. Além desses, somente o usuário pode fixar outros aplicativos; A fixar programática por um aplicativo não é permitida.

O recurso Mostrar Área de Trabalho Início Rápido agora está localizado na extrema direita da barra de tarefas. Passar o mouse sobre essa área faz com que todas as janelas ativas se tornem transparentes, mostrando a área de trabalho. Clicar na área executa a ação familiar de minimizar todas as janelas e alternar para a área de trabalho.

Enquanto o aplicativo está em execução, seu botão de barra de tarefas se torna o único lugar para acessar todos os recursos a seguir, cada um discutido em detalhes abaixo.

-   [Tarefas](#tasks): comandos de aplicativo comuns, presentes mesmo quando o aplicativo não está em execução.
-   [Destinos:](#destinations)arquivos acessados recentemente e com frequência específicos para o aplicativo.
-   [Miniaturas: alternação](#thumbnails)de janela, incluindo destinos de comutadores para guias e documentos individuais.
-   [Barras de ferramentas em miniatura:](#thumbnail-toolbars)controle de aplicativo básico da própria miniatura.
-   [Barras de progresso](#progress-bars) [e sobreposições de ícone:](#icon-overlays)notificações de status.

O botão da barra de tarefas pode representar um launcher, uma única janela do aplicativo ou um grupo. Um identificador conhecido como AppUserModelID (ID do Modelo de Usuário do Aplicativo) é atribuído a cada grupo. Um AppUserModelID pode ser especificado para substituir o grupo de barras de tarefas padrão, que permite que as janelas se tornem membros do mesmo grupo quando podem não ser vistas como tal de outra forma. Cada membro de um grupo recebe uma visualização separada no flyout da miniatura que é mostrada quando o mouse passar o mouse sobre o botão da barra de tarefas do grupo. Observe que o próprio grupo permanece opcional.

A partir Windows 7, os botões da barra de tarefas agora podem ser reorganizedos pelo usuário por meio de operações do tipo "arrastar e soltar".

> [!Note]  
> A pasta Início Rápido ([***FOLDERID \_ QuickLaunch***](knownfolderid.md)) ainda está disponível para compatibilidade com backward, embora não haja mais uma Início Rápido interface do usuário. No entanto, novos aplicativos não devem pedir para adicionar um ícone para Início Rápido durante a instalação.

 

Para obter mais informações, consulte IDs de modelo de usuário [do aplicativo (AppUserModelIDs)](appids.md).

## <a name="jump-lists"></a>Listas de saltos

Um usuário normalmente inicia um programa com a intenção de acessar um documento ou executar tarefas dentro do programa. O usuário de um programa de jogos pode querer chegar a um jogo salvo ou iniciar como um caractere específico, em vez de reiniciar um jogo desde o início. Para obter aos usuários uma meta final mais eficiente, uma lista de destinos e tarefas comuns [associadas](#destinations) a um aplicativo é anexada ao botão da barra de tarefas do aplicativo (bem como à entrada de **menu** Iniciar equivalente). [](#tasks) Este é o recurso do Lista de Atalhos. O Lista de Atalhos está disponível se o botão da barra de tarefas está em um estado inicial (o aplicativo não está em execução) ou se ele representa uma ou mais janelas. Clicar com o botão direito do mouse no botão da barra de tarefas mostra a Lista de Atalhos do aplicativo, conforme mostrado na ilustração a seguir.

![lista de saltos com categorias fixadas, frequentes e de tarefas](images/taskbar/jumplist.png)

Por padrão, um Lista de Atalhos padrão contém duas categorias: itens recentes e itens fixados, embora, como apenas categorias com conteúdo sejam mostradas na interface do usuário, nenhuma dessas categorias é mostrada no primeiro lançamento. Sempre presente estão um ícone de lançamento do aplicativo (para iniciar mais instâncias do aplicativo),  uma opção para fixar ou desempinar o aplicativo na barra de tarefas e um comando Fechar para qualquer janela aberta.

## <a name="destinations"></a>Destinos

As **categorias** **Recentes e** Frequentes são consideradas para conter destinos. Um destino, geralmente um arquivo, documento ou URL, é algo que pode ser editado, navegado, exibido e assim por diante. Pense em um destino como uma coisa em vez de uma ação. Normalmente, um destino é um item no namespace do Shell, representado por [**um IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) ou [**IShellLink.**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) Essas partes da lista de destino são análogas à lista de documentos usados recentemente do **menu** Iniciar (não mais mostrada por padrão) e à lista de aplicativos usados com frequência, mas são específicas de um aplicativo e, portanto, mais precisas e úteis para o usuário. Os resultados usados na lista de destino são calculados por meio de chamadas para [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs). Observe que quando o usuário abre um arquivo do Windows Explorer ou usa a caixa de diálogo de arquivo comum para abrir, salvar ou criar um arquivo, **SHAddToRecentDocs** é chamado para você automaticamente, o que resulta em muitos aplicativos que têm seus itens recentes mostrados na lista de destino sem nenhuma ação de sua parte.

Iniciar um destino é muito parecido com iniciar um item usando **o comando Abrir com.** O aplicativo é lançado com esse destino carregado e pronto para uso. Os itens na lista de destino também podem ser arrastados da lista para um destino de soltar, como uma mensagem de email. Ao ter esses itens centralizados em uma lista de destino, ele obtém os usuários para onde eles querem ir muito mais rapidamente, que é a meta.

Conforme os itens aparecem na categoria Recente  de uma [](#customizing-jump-lists) lista de destino (ou categoria Frequente ou uma categoria personalizada, conforme discutido em uma seção posterior), um usuário pode querer garantir que o item sempre está na lista para acesso rápido.  Para fazer isso, ele pode fixar esse item na lista, o que adiciona o item à **categoria Fixado.** Quando um usuário estiver trabalhando ativamente com um destino, ele o deseja facilmente em mãos e, portanto, o fixaria na lista de destino do aplicativo. Depois que o trabalho do usuário é feito, ele simplesmente desempina o item. Esse controle de usuário mantém a lista não emclusa e relevante.

Uma lista de destino pode ser considerada uma versão específica do aplicativo **do** menu Iniciar. Uma lista de destino não é um menu de atalho. Cada item em uma lista de destino pode ser clicado com o botão direito do mouse em seu próprio menu de atalho.

### <a name="apis"></a>APIs

-   [**IApplicationDestinations::RemoveDestination**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-removedestination)
-   [**IApplicationDestinations::RemoveAllDestinations**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-removealldestinations)
-   [**IApplicationDocumentLists::GetList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist)
-   [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)

## <a name="tasks"></a>Tarefas

Outra parte de um Lista de Atalhos é a **categoria** Tarefas. Embora um destino seja uma coisa, uma tarefa é uma ação e, nesse caso, é uma ação específica do aplicativo. Em outras condições, um destino é um substantivo e uma tarefa é um verbo. Normalmente, as tarefas são [**itens IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) com argumentos de linha de comando que indicam uma funcionalidade específica que pode ser disparada por um aplicativo. Novamente, a ideia é centralizar o máximo de informações relacionadas a um aplicativo quanto é prático.

Os aplicativos definem tarefas com base nos recursos do programa e nas principais coisas que um usuário deve fazer com eles. As tarefas devem ser sem contexto, pois o aplicativo não precisa estar em execução para que elas funcionem. Elas também devem ser as ações estatisticamente mais comuns que um usuário normal executaria em um aplicativo, como compor uma mensagem de email ou abrir o calendário em um programa de email, criar um novo documento em um processador de palavras, iniciar um aplicativo em um determinado modo ou iniciar um de seus subcomutadores. Um aplicativo não deve desorganização do menu com recursos avançados que os usuários padrão não precisarão ou ações únicas, como registro. Não use tarefas para itens promocionais, como atualizações ou ofertas especiais.

É altamente recomendável que a lista de tarefas seja estática. Ele deve permanecer o mesmo, independentemente do estado ou status do aplicativo. Embora seja possível variar a lista dinamicamente, você deve considerar que isso pode confundir o usuário que não espera que essa parte da lista de destino mude.

### <a name="apis"></a>APIs

-   [**ICustomDestinationList::AddUserTasks**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-addusertasks)

## <a name="customizing-jump-lists"></a>Personalização de listas de saltos

Um aplicativo pode definir suas próprias categorias e adicioná-las além ou no lugar das categorias padrão **Recentes** e **Frequentes** em um Lista de Atalhos. O aplicativo pode controlar seus próprios destinos nessas categorias personalizadas com base na arquitetura do aplicativo e no uso pretendido. A captura de tela a seguir mostra um Lista de Atalhos personalizado com uma categoria Histórico.

![lista de saltos personalizada](images/taskbar/customjumplist.png)

Se um aplicativo decidir fornecer uma categoria personalizada, esse aplicativo assumirá a responsabilidade de populá-la. O conteúdo da categoria ainda deve ser específico do usuário e com base no histórico do usuário, ações ou ambos, mas por meio de uma categoria personalizada, um aplicativo pode determinar o que deseja acompanhar e o que deseja ignorar, talvez com base em uma opção de aplicativo. Por exemplo, um programa de áudio pode optar por incluir apenas os discos tocadas recentemente e ignorar faixas individuais tocadas recentemente.

Se um usuário tiver removido um item da lista, que é sempre uma opção de usuário, o aplicativo deverá fazer isso. O aplicativo também deve garantir que os itens na lista sejam válidos ou que eles falhem normalmente se foram excluídos. Itens individuais ou todo o conteúdo da lista podem ser removidos programaticamente.

O número máximo de itens em uma lista de destino é determinado pelo sistema com base em vários fatores, como resolução de exibição e tamanho da fonte. Se não houver espaço suficiente para todos os itens em todas as categorias, eles serão truncados de baixo para cima.

### <a name="apis"></a>APIs

-   [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)
-   [**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations)
-   [**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)

## <a name="thumbnail-toolbars"></a>Barras de ferramentas em miniatura

Para fornecer acesso aos comandos de chave de uma janela específica sem fazer com que o usuário restaure ou ative a janela do aplicativo, um controle de barra de ferramentas ativo pode ser inserido na visualização em miniatura dessa janela. Por exemplo, Windows Media Player pode oferecer controles de transporte de mídia padrão, como reproduzir, pausar, mudo e parar. A interface do usuário exibe essa barra de ferramentas diretamente abaixo da miniatura, conforme mostrado na ilustração a seguir– ela não abrange nenhuma parte dela.

![barra de tarefas em miniatura para o player de mídia do Windows, com três botões: voltar, reproduzir e avançar](images/taskbar/thumbbar.png)

Essa barra de ferramentas é simplesmente o controle comum da barra de ferramentas padrão familiar. Ele tem um máximo de sete botões. A ID, a imagem, a dica de ferramenta e o estado de cada botão são definidos em uma estrutura, que é passada para a barra de tarefas. O aplicativo pode mostrar, habilitar, desabilitar ou ocultar botões da barra de ferramentas em miniatura, conforme exigido pelo estado atual.

Como há espaço limitado para exibir miniaturas e um número variável de miniaturas a exibir, os aplicativos não têm garantia de um determinado tamanho de barra de ferramentas. Se o espaço for restrito, os botões na barra de ferramentas serão truncados da direita para a esquerda. Portanto, ao projetar sua barra de ferramentas, você deve priorizar os comandos associados aos seus botões e garantir que os mais importantes sejam os primeiros e com menos probabilidade de serem descartados devido a problemas de espaço.

> [!Note]  
> Quando um aplicativo exibe uma janela, seu botão de barra de tarefas é criado pelo sistema. Quando o botão estiver em ação, a barra de tarefas enviará uma **mensagem TaskbarButtonCreated** para a janela. Seu valor é calculado chamando [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)(L("TaskbarButtonCreated")). Essa mensagem deve ser recebida pelo seu aplicativo antes de chamar qualquer [**método ITaskbarList3.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3)

 

### <a name="api"></a>API

-   [**ITaskbarList3::ThumbBarAddButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons)
-   [**ITaskbarList3::ThumbBarSetImageList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist)
-   [**ITaskbarList3::ThumbBarUpdateButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarupdatebuttons)
-   [**THUMBBUTTON**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton)

## <a name="icon-overlays"></a>Sobreposições de ícone

Um aplicativo pode comunicar determinadas notificações e status ao usuário por meio de seu botão de barra de tarefas pela exibição de pequenas sobreposições no botão. Essas sobreposições são semelhantes ao tipo de sobreposição existente usado para atalhos ou notificações de segurança, exibidos no canto inferior direito do botão. Para exibir um ícone de sobreposição, a barra de tarefas deve estar no modo de ícone grande padrão, conforme mostrado na captura de tela a seguir.

![botão da barra de tarefas do Windows Messenger com uma sobreposição para indicar um status disponível](images/taskbar/taskbaroverlay.png)

As sobreposições de ícone servem como uma notificação contextual de status e destinam-se a negar a necessidade de um ícone de status de área de notificação separado para comunicar essas informações ao usuário. Por exemplo, o novo status de email no Microsoft Outlook, atualmente mostrado na área de notificação, agora pode ser indicado por meio de uma sobreposição no botão da barra de tarefas. Novamente, você deve decidir durante o ciclo de desenvolvimento qual método é melhor para seu aplicativo. Os ícones de sobreposição destinam-se a fornecer status ou notificações importantes e de longa duração, como status de rede, status do messenger ou novo email. O usuário não deve ser apresentado com sobreposições ou animações em constante alteração.

Como uma única sobreposição é sobreposição no botão da barra de tarefas e não nas miniaturas de janela individuais, esse é um recurso por grupo em vez de por janela. As solicitações de ícones de sobreposição podem ser recebidas de janelas individuais em um grupo de barras de tarefas, mas não são enfileirodas. A última sobreposição recebida é a sobreposição mostrada.

### <a name="apis"></a>APIs

-   [**ITaskbarList3::SetOverlayIcon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon)

## <a name="progress-bars"></a>Barras de progresso

Um botão da barra de tarefas pode ser usado para exibir uma barra de progresso. Isso permite que uma janela forneça informações de progresso para o usuário sem que o usuário tenha que alternar para a própria janela. O usuário pode permanecer produtivo em outro aplicativo enquanto vê rapidamente o progresso de uma ou mais operações que ocorrem em outras janelas. Destina-se a que uma barra de progresso em um botão de barra de tarefas reflita um indicador de progresso mais detalhado na própria janela. Esse recurso pode ser usado para acompanhar cópias de arquivo, downloads, instalações, gravação de mídia ou qualquer operação que levará um período de tempo. Esse recurso não se destina ao uso com ações normalmente periféricos, como o carregamento de uma página da Web ou a impressão de um documento. Esse tipo de progresso deve continuar a ser mostrado na barra de status de uma janela.

A barra de progresso do botão da barra de tarefas é uma experiência semelhante ao controle familiar da Barra de Progresso. Ele pode exibir o progresso determinado com base em um percentual concluído da operação ou um progresso de estilo de marquete indeterminado para indicar que a operação está em andamento sem nenhuma previsão de tempo restante. Ele também pode mostrar que a operação está em pausa ou encontrou um erro e requer intervenção do usuário.

### <a name="apis"></a>APIs

-   [**ITaskbarList3::SetProgressState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate)
-   [**ITaskbarList3::SetProgressValue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue)

## <a name="deskbands"></a>Faixas de mesa

Em versões do Windows anteriores ao Windows 7, algo semelhante à funcionalidade da barra de ferramentas em miniatura poderia ser obtido por meio de uma faixa de ferramentas — uma barra de ferramentas hospedada na barra de tarefas. Por exemplo, Windows Media Player pode minimizar para a barra de tarefas como um conjunto de controles de transporte em vez de um botão padrão. No Windows 7, as faixas de mesa ainda podem ser implementadas e as barras de ferramentas em miniatura não se destinam a substituí-las. Nem todos os aplicativos se prestam a uma barra de ferramentas em miniatura, e outra solução, como uma faixa de mesa ou uma tarefa em uma lista de destino, pode ser a resposta certa para seu aplicativo; você deve decidir qual solução funciona melhor para seu aplicativo como parte do ciclo de desenvolvimento. No entanto, esteja ciente de que as bandas de suporte devem dar suporte Windows Aero com translúência ("glass") habilitada e a interface [**IDeskBand2.**](/windows/desktop/api/Shobjidl/nn-shobjidl-ideskband2)

### <a name="apis"></a>APIs

-   [**IDeskBand2**](/windows/desktop/api/Shobjidl/nn-shobjidl-ideskband2)

## <a name="notification-area"></a>Área de notificação

Houve alterações na área de notificação que dão ao usuário muito mais controle sobre quais ícones aparecem na barra de tarefas. Todos os ícones de notificação agora estão ocultos por padrão e essa visibilidade não pode ser controlada programaticamente. Somente o usuário tem permissão para escolher quais ícones de notificação aparecem na barra de tarefas. Quando um balão de notificação é exibido, o ícone fica temporariamente visível, mas mesmo assim um usuário pode optar por calá-lo. Portanto, uma sobreposição de ícone em um botão de barra de tarefas se torna uma opção atraente quando você deseja que seu aplicativo comunique essas informações aos usuários.

## <a name="thumbnails"></a>Miniaturas

No Windows Vista, passar o mouse sobre o botão da barra de tarefas de um aplicativo exibe uma miniatura que representa a janela em execução. Se a barra de tarefas tiver recolhido as janelas do aplicativo, a miniatura representará isso aparecendo como uma pilha, mas somente a janela ativa será mostrada na própria miniatura.

No Windows 7, cada membro de um grupo é mostrado como uma miniatura separada e agora também é um destino de comutador. Um aplicativo pode definir seus filhos (como janelas filho verdadeiras, documentos individuais ou guias) e fornecer miniaturas correspondentes para cada uma dessas janelas, mesmo quando normalmente não apareceriam na barra de tarefas. Isso permite que os usuários alternem diretamente para a exibição do aplicativo que eles querem em vez de alternar para o aplicativo e, em seguida, alternar para seu destino. Por exemplo, aplicativos MDI (interface de vários documentos)/TDI (tabbed-document interface) podem ter cada documento ou guia exibido como uma miniatura separada e alternar o destino quando o mouse passar o mouse sobre o botão da barra de tarefas de um grupo.

![três miniaturas da barra de tarefas que representam guias individuais no Windows Internet Explorer](images/taskbar/taskbarthumbnails.png)

> [!Note]  
> Como no Windows Vista, o Aero deve estar ativo para exibir miniaturas.

 

### <a name="api"></a>API

-   [**ITaskbarList3::RegisterTab**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-registertab)
-   [**ITaskbarList3::SetTabActive**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settabactive)
-   [**ITaskbarList3::SetTabOrder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settaborder)
-   [**ITaskbarList3::UnregisterTab**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-unregistertab)
-   [**ITaskbarList4::SetTabProperties**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist4-settabproperties)

As representações em miniatura para janelas normalmente são automáticas, mas nos casos em que o resultado não é ideal, a miniatura pode ser especificada explicitamente. Por padrão, somente as janelas de nível superior têm uma miniatura gerada automaticamente para elas, e as miniaturas para janelas filho aparecem como uma representação genérica. Isso pode resultar em uma experiência menor do que a ideal (e até mesmo confusa) para o usuário final. Uma miniatura de destino de comutador específica para cada janela filho, por exemplo, fornece uma experiência de usuário muito melhor.

### <a name="api"></a>API

-   [**DwmSetWindowAttribute**](/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)
-   [**DwmSetIconicThumbnail**](/windows/win32/api/dwmapi/nf-dwmapi-dwmseticonicthumbnail)
-   [**DwmSetIconicLivePreviewBitmap**](/windows/win32/api/dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap)
-   [**DwmInvalidateIconicBitmaps**](/windows/win32/api/dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
-   [**WM \_ DWMSENDICONICTHUMBNAIL**](../dwm/wm-dwmsendiconicthumbnail.md)
-   [**WM \_ DWMSENDICONICLIVEPREVIEWBITMAP**](../dwm/wm-dwmsendiconiclivepreviewbitmap.md)

Você pode selecionar uma área específica da janela a ser usada como a miniatura. Isso pode ser útil quando um aplicativo sabe que seus documentos ou guias serão semelhantes quando exibidos em tamanho de miniatura. Em seguida, o aplicativo pode optar por mostrar apenas a parte de sua área de cliente que o usuário pode usar para distinguir entre miniaturas. No entanto, passar o mouse sobre qualquer miniatura abrirá uma exibição da janela inteira por trás dela para que o usuário possa dar uma olhada rapidamente neles também.

Se houver mais miniaturas do que podem ser exibidas, a visualização será reverteda para a miniatura herdada ou um ícone padrão.

### <a name="api"></a>API

-   [**ITaskbarList3::SetThumbnailClip**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setthumbnailclip)

Para adicionar **Fixar** à Barra de Tarefas ao menu de atalho de um item, que normalmente é necessário apenas para tipos de arquivo que incluem a entrada [IsShortCut,](./links.md) é feito registrando o manipulador de menu de contexto apropriado. Isso também se aplica ao **Menu Fixar ao Iniciar**. Consulte [Registrando manipuladores de extensão do Shell](reg-shell-exts.md) para obter mais informações.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[A barra de tarefas](taskbar.md)
</dt> <dt>

[IDs de modelo de usuário do aplicativo (AppUserModelIDs)](appids.md)
</dt> <dt>

[Notificações e a área de notificação](notification-area.md)
</dt> </dl>

 

 
