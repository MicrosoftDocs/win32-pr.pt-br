---
title: Criação de animações
description: Criação de animações
ms.assetid: 6d5c3c61-b3f2-4505-aa43-b6d001c444a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16c460908e7c782054a3f62ece87d01e7c9a817
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104550734"
---
# <a name="creating-animations"></a>Criação de animações

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Para começar a criar animações para seu caractere, selecione o ícone **animações** na árvore. Isso exibe a página **Propriedades** com as configurações padrão para todas as animações. Você pode alterar o tamanho do quadro, a duração do quadro padrão e as configurações da paleta de cores na página **Propriedades** .

### <a name="setting-your-characters-frame-size"></a>Definindo o tamanho do quadro do seu caractere

A altura e a largura do quadro de animação devem permanecer constantes durante toda a definição de caractere (ou seja, para todas as animações desse caractere). Embora você possa alterar o tamanho do quadro de sua configuração padrão (128 x 128 pixels), as imagens exibidas no editor serão dimensionadas para caber no tamanho de exibição padrão. Se você alterar a configuração de quadro padrão, poderá exibir o tamanho completo e não dimensionado do quadro escolhendo **Abrir janela do quadro** no menu **Editar** .

### <a name="setting-your-characters-palette"></a>Definindo a paleta do caractere

Por padrão, o editor usa a primeira imagem de bitmap que você carrega para definir a paleta de cores padrão do caractere, as cores que determinam como o caractere é exibido e define a cor na posição da paleta de 11<sup>°</sup> como sua cor de transparência. No entanto, você pode definir a paleta e a transparência explicitamente no grupo de **informações da paleta** . Isso permite que você especifique um arquivo de imagem a ser usado para a paleta. Você pode especificar um dos arquivos de imagem de animação ou qualquer arquivo gráfico. O arquivo de paleta especificado deve ser um arquivo de cores de 8 bits (256). Depois de carregado, use o botão **Alterar configuração** para alterar a cor de transparência.

A paleta de cores do caractere não deve remapear as cores padrão do sistema. O editor irá reservar automaticamente a paleta de cores do sistema ao exibir imagens. Além disso, todas as suas imagens de animação devem usar a mesma paleta de cores e cor de transparência. Isso é muito importante. Se não tiverem, você poderá ver o remapeamento de cores de suas imagens ao carregá-las no editor.

Embora você possa definir a paleta de cores para o caractere, em sistemas Windows em que as propriedades de exibição são definidas como uma paleta de cores de 8 bits (256), a cor do caractere estará sujeita à paleta atual do sistema. Como os aplicativos podem alterar a paleta do sistema, o caractere pode não aparecer com as configurações de cor corretas. Embora não haja nenhuma maneira de evitar isso, você pode diminuir o efeito limitando os números de cores que você usa e definindo a paleta do caractere com base na paleta usada pelo aplicativo que orienta o caractere. Por exemplo, se você estiver desenvolvendo um caractere a ser usado com páginas da Web, convém definir a paleta do caractere usando a paleta de meio-tom do Microsoft Internet Explorer. Você pode capturar a paleta do navegador clicando com o botão direito do mouse em uma imagem em uma página da Web e escolhendo **Salvar imagem como** comando e escolhendo **bitmap** na opção **salvar como tipo** e, em seguida, clicando em **salvar**. Para otimizar os arquivos de imagem de animação para um arquivo de paleta específico, talvez você queira usar um produto como equilíbrio DeBabelizer.

### <a name="creating-a-new-animation"></a>Criando uma nova animação

Depois de determinar as configurações de animação global, você pode começar a criar animações. Para criar uma nova animação, escolha **nova animação** no menu **Editar** ou no botão **nova animação** na barra de ferramentas. Isso adiciona um novo ícone de animação na árvore sob o ícone **animações** e atribui o novo ícone a um nome padrão. Você pode renomear sua animação digitando o campo **nome da animação** . Observe que os nomes de animação dentro de uma definição de caractere devem ser exclusivos. Além disso, evite usar caracteres no nome que não sejam caracteres válidos para nomes de arquivo.

### <a name="adding-frames"></a>Adicionando quadros

Cada animação é composta de quadros. Para criar um novo quadro para sua animação, escolha **novo quadro** no menu **Editar** ou na barra de ferramentas. Isso adiciona um novo ícone de quadro à árvore sob o ícone de animação e exibe três páginas com guias. A página **geral** inclui controles que permitem que você carregue e ajuste uma imagem para seu quadro. Ele também inclui uma área de exibição para a aparência do quadro.

![Captura de tela que mostra o painel de imagem com o nome de arquivo, o caminho e a posição.](images/f2charflame.gif)

Um quadro pode conter uma ou mais imagens. Para definir uma imagem para um quadro, clique no botão **Adicionar arquivo de imagem** logo acima da caixa de listagem **imagens** . A caixa de diálogo **selecionar arquivos de imagem** é exibida, permitindo que você selecione um arquivo de imagem de bitmap.

![Captura de tela que mostra um arquivo de imagem que está sendo selecionado no explorador de arquivos.](images/f3chardialbox.gif)

Selecione o arquivo que você deseja carregar, escolha **abrir** e a imagem aparecerá na exibição do quadro na página **geral** . O editor aceita imagens armazenadas como formato de bitmap de 1 bit (monocromático), de 4 bits ou de 8 bits do Windows ou como formato GIF.

Você pode usar os botões de seta quatro abaixo da imagem na caixa **posição** para ajustar a aparência da imagem dentro do quadro. Se a imagem for maior do que o tamanho do quadro, somente a parte da imagem que aparece dentro do quadro será exibida. Se você aumentar o tamanho do quadro, a imagem poderá ser dimensionada para caber na área de exibição do editor.

Você também pode exibir um quadro escolhendo **Abrir janela do quadro** no menu **Editar** . Isso exibe o quadro atual em uma janela separada sem dimensionar as imagens carregadas no quadro. O tamanho inicial da janela é baseado nas configurações de altura e largura do quadro. Você pode redimensioná-lo como menor, mas não maior. A janela do quadro reflete as alterações feitas usando os controles no editor e também permite que você exiba o quadro enquanto exibe suas outras páginas de propriedades.

![Captura de tela que mostra o painel posição.](images/f4charposctrl.gif)

Você pode compor um quadro de várias imagens. Cada vez que você seleciona o botão **Adicionar imagem** e escolhe outra imagem, a imagem é adicionada à lista e à área de exibição da imagem. Você também pode adicionar várias imagens selecionando mais de um arquivo. Pressione SHIFT ou CTRL enquanto clica na caixa de diálogo **selecionar arquivos de imagem** e, em seguida, escolha **abrir**. Os botões **mover para cima** e **mover para baixo** acima da caixa de listagem **imagens** movem uma imagem selecionada na ordem de exibição (ordem z) para o quadro. Você também pode mover imagens arrastando-as na lista. Selecionar uma imagem na lista e clicar no botão **excluir** remove uma imagem. Para alterar uma imagem que você carregou em outro arquivo de imagem, você pode clicar no nome para editá-lo diretamente ou usar o botão **...** (reticências) para abrir a caixa de diálogo **selecionar arquivos de imagem** e selecionar um arquivo diferente.

![Captura de tela que mostra o botão de reticências.](images/f5charell.gif)

Você pode usar a caixa de texto **duração** para definir a duração do quadro; ou seja, quanto tempo o quadro será exibido. Se um quadro não tiver nenhuma imagem e duração zero, o quadro não será exibido quando a animação for reproduzida.

Você também pode especificar um arquivo de efeito de som a ser tocado quando o quadro for exibido. Se você planeja carregar o caractere de um servidor Web, talvez queira compactar o arquivo de efeito de som para minimizar o tempo de carregamento. Em seguida, você pode especificar o arquivo de som compactado no editor de caracteres do agente. Além disso, evite usar um efeito de som com uma duração maior do que a duração da animação e, especialmente, evitar um efeito de som que faça um loop, porque os serviços de animação do Microsoft Agent não enviam um evento de animação completa até que o som seja concluído. Evite também especificar um efeito de som para qualquer animação que você atribui aos Estados de **escuta** ou **audição** , pois isso interfere na entrada de fala. Por fim, embora você possa incluir mais de um efeito de som em uma animação, evite colocá-los para sobreposição, pois isso pode afetar o tempo da animação. Além disso, tenha em mente que os efeitos sonoros podem ser reproduzidos em taxas diferentes com base no hardware do usuário.

Para adicionar quadros à animação, escolha o comando **novo quadro** novamente e siga o mesmo procedimento. Como opção, você também pode carregar várias imagens e gerar automaticamente novos quadros para elas. Para usar esse recurso, escolha **novos quadros de imagens** no menu **Editar** . Os quadros serão criados em ordem alfabética com base nos nomes de fileimage. Quando terminar de definir todos os quadros para a animação, você poderá escolher novamente o comando **nova animação** para iniciar uma nova animação.

Há outras maneiras de adicionar quadros a animações e mover quadros dentro ou entre animações. Você pode selecionar outro quadro (da mesma ou de outra animação) e escolher **recortar** ou **copiar** e, em seguida, selecionar a animação ou um quadro nessa animação e escolher **colar**. Você também pode arrastar um quadro de uma animação para outra. Se você arrastar dentro de uma animação, a ação moverá o quadro. Se você arrastar para outra animação, ela copiará o quadro. Arrastar para um quadro anterior na mesma animação insere o quadro antes do quadro que você arrasta. Arrastar para um quadro a seguir o coloca após o quadro no qual você arrasta. Se você arrastar um quadro usando o botão direito do mouse, soltar o botão exibirá um menu pop-up com suas opções de transferência.

Você também pode criar uma animação copiando uma animação existente (selecione a animação e escolha **copiar**) e selecionando o ícone de **animações** ou outro ícone de animação e escolhendo **colar**. O editor cria automaticamente um novo nome para a animação, embora você possa alterar o nome.

### <a name="branching"></a>Ramificação

Ao criar um quadro, você também pode definir qual quadro é reproduzido em seguida. Por padrão, o próximo quadro reproduzido na sequência de animação é sempre o próximo quadro na ordem z. No entanto, escolhendo a página **ramificação** , você pode definir a probabilidade para até três outros quadros que o servidor pode reproduzir. Insira o percentual de probabilidade e o número do quadro de destino nos campos apropriados. Você pode especificar a ramificação até mesmo para quadros que não têm imagens e têm sua duração definida como zero. Isso permite que você ramificar sem primeiro exibir uma imagem específica.

![Captura de tela que mostra a página ' ramificação '.](images/f6charbranch.gif)

Você pode usar o recurso de ramificação para criar animações que entrarão em loop indefinidamente. No entanto, observe que quando uma animação de looping é reproduzida, outras animações na fila do caractere não serão reproduzidas até que um evento — como um usuário pressionando a chave Push-to-Talk ou o aplicativo cliente que chama o método [**Stop**](stop-method.md) — pare a animação de loop. Portanto, considere cuidadosamente o contexto no qual a animação será usada antes de criar uma animação de looping.

A página de ramificação também permite que você crie ramificações de saída. Uma ramificação de saída é uma ramificação para um quadro que a animação executará quando a animação for interrompida e antes de a próxima animação ser reproduzida. Definir branches de saída permitirá que você se movimente suavemente durante a transição de uma animação para outra. Sua ramificação de saída não deve criar um loop circular, mas, eventualmente, deve ser capaz de sair para o último quadro da animação.

Você não precisa fornecer uma ramificação de saída para cada quadro, no entanto, se não tiver, a animação seguirá a ramificação normal do quadro. Se o quadro não tiver nenhuma ramificação explícita, a animação será automaticamente ramificada para o quadro que a segue. Por exemplo, se você ramificar do quadro 3 para o quadro 1 e o quadro 1 não tiver nenhuma outra ramificação (ramificação normal ou de saída), o quadro 1 será ramificado para o quadro 2. Se o quadro 2 não tiver nenhuma ramificação, a animação fará o Branch de volta para o quadro 3 e você terá um loop circular. Em vez disso, você poderia ramificar do quadro 3 para o quadro 1 e, em seguida, definir a ramificação de saída do quadro 1 para qualquer quadro após o quadro 3 e normalmente prosseguir para o último quadro da animação.

Às vezes, talvez seja necessário criar um quadro final explícito de uma animação que não seja executada visivelmente, mas que forneça um fim da animação. Por exemplo, você precisa sair da animação, mas sair para o último quadro não seria apropriado. Você pode fazer isso criando um quadro de duração em branco e zero como o último quadro da animação. Isso permite que a animação seja executada normalmente por meio do último quadro da animação e também permite que você forneça um ponto de saída final para sua ramificação de saída.

### <a name="previewing-an-animation"></a>Visualizando uma animação

Você pode visualizar a animação no editor de caracteres do agente escolhendo o comando **Visualizar** no menu **Editar** ou o botão Visualizar na barra de ferramentas. Isso reproduz sua animação, incluindo qualquer ramificação e efeitos sonoros, a partir do quadro selecionado atual. Ele é redefinido para o quadro selecionado atual quando a animação é concluída. Para reproduzir toda a animação, vá para o modo de exibição de árvore, selecione o ícone da animação ou o primeiro quadro da animação e escolha o comando **Visualizar** . O editor anima os quadros na página **geral** . Para interromper a visualização antes de terminar, escolha o comando **parar visualização** . O comando **Preview** muda automaticamente para **parar a visualização** enquanto a visualização é reproduzida.

Você também pode visualizar sua ramificação de saída escolhendo o comando versão **prévia sair da ramificação** no menu **Editar** ou na barra de ferramentas. O permite que você teste como a ramificação de saída será exibida em qualquer quadro específico.

### <a name="assigning-speaking-overlays"></a>Atribuindo sobreposições de fala

Você pode definir um caractere para que ele seja falado durante o último quadro de sua animação. Nesse quadro, escolha a página **sobreposição** . Esta página permite que você carregue e atribua arquivos de imagem de boca às posições de boca padrão com suporte pelo Microsoft Agent. Clique no botão **Adicionar imagem** e selecione a imagem na caixa de diálogo. Você também pode selecionar várias imagens, e o editor será carregado e atribuirá as imagens começando com a posição da boca selecionada. Clique nos botões **mover para cima** e **mover para baixo** ou arraste uma entrada para alterar uma atribuição de imagem na lista. Clique no botão **excluir** para remover uma imagem. Você também pode editar o nome do caminho de um arquivo atribuído clicando em sua entrada na lista e digitando novamente seu filename ou escolhendo o botão de **reticências** para exibir a caixa de diálogo **selecionar arquivos de imagem** .

![Captura de tela que mostra a página ' sobreposições ' com um arquivo selecionado.](images/f7charover.gif)

As sobreposições de boca devem se ajustar no contorno do quadro base sobre o qual serão exibidas. Se não tiverem, eles serão recortados no quadro base.

Se você quiser que o caractere fale com sua boca fora do quadro de base, por exemplo, quando o caractere for para falar lateralmente, primeiro crie o quadro base com a cabeça do caractere (ou a área que será movida conforme o caractere se enquadrar) como sua imagem superior. Em seguida, defina as sobreposições de boca para substituir essa imagem e definir a opção **substituir quadro superior da imagem de base** . Você também pode usar o botão **definir tudo** para definir essa opção para todas as sobreposições de boca no quadro.

### <a name="assigning-a-return-animation"></a>Atribuindo uma animação de retorno

Para criar uma transição suave de uma animação para a seguinte, crie suas sequências de animação para começar e terminar com uma imagem neutra. Para obter mais informações, consulte [**criando caracteres para o Microsoft Agent**](designing-characters-for-microsoft-agent.md). No entanto, isso não significa que todas as animações devem terminar na posição neutra. Você pode animar um caractere por meio de uma sequência de quadros, fazê-lo falar durante o último quadro e criar uma animação complementar separada que retorna o caractere para a posição neutra. Essa animação complementar é chamada de animação de retorno.

Você pode definir uma animação de retorno criando uma animação explícita para essa finalidade. Você também pode criar uma animação de retorno usando a ramificação de saída que você define dentro da animação. Para atribuir uma animação de retorno, selecione a animação na árvore e selecione a animação de retorno criada ou use sair da ramificação na lista suspensa retornar animação na página Propriedades.

Criar e atribuir uma animação de retorno tem um benefício adicional: quando o servidor recebe uma solicitação para reproduzir outra animação, ele tentará reproduzir a animação de retorno para a última animação que foi reproduzida, se uma animação de retorno for atribuída. Isso garante uma transição suave. Se uma animação começar e terminar na posição neutra, você não precisará definir uma animação de retorno. Da mesma forma, se você pretende lidar com transições de uma animação para outra, talvez não seja necessário atribuir uma animação de retorno.

### <a name="assigning-animations-to-states"></a>Atribuindo animações a Estados

Os serviços de animação do Microsoft Agent executam animações automaticamente quando o aplicativo cliente de hospedagem usa determinados métodos. Por exemplo, quando um aplicativo chama os métodos [**MoveTo**](moveto-method.md) e [**GestureAt**](gestureat-method.md) , o servidor determina automaticamente onde o caractere é exibido e desempenha uma animação apropriada. Da mesma forma, o Microsoft Agent reproduz automaticamente animações ociosas quando o usuário não interage com o caractere por vários segundos. Essas condições, quando o servidor reproduz animações automaticamente em nome de um aplicativo, são chamadas de *Estados*. No entanto, para que o servidor saiba qual animação reproduzir, você deve atribuir animações a esses Estados.

Para atribuir uma animação ou animações a um estado, crie a animação apropriada, expanda a entrada Estados no modo de exibição de árvore da janela do editor e selecione o ícone de estado. A lista de animações que você criou aparece em uma caixa de listagem no lado direito da janela. Verifique a animação que você deseja atribuir a esse estado. Observe que você pode atribuir mais de uma animação ao mesmo estado. Isso permite que o servidor selecione aleatoriamente diferentes animações para o estado. A atribuição de uma animação a um estado não impede que uma animação reproduza essa animação diretamente.

Você também pode atribuir uma animação a um estado selecionando a entrada da animação na árvore. A caixa de listagem **atribuir ao estado** na página **Propriedades** lista os Estados. Marque a caixa de seleção do estado ao qual você está atribuindo a animação.

O editor não dá suporte à criação de Estados adicionais porque os Estados se aplicam somente a situações em que o servidor deve reproduzir uma animação automaticamente em nome do aplicativo cliente. Portanto, não há nenhum benefício em definir seu próprio estado. Se necessário, você pode reproduzir qualquer animação explicitamente usando o método [**Play**](play-method.md) .

### <a name="saving-your-character-definition"></a>Salvando sua definição de caractere

Você pode salvar o arquivo de definição do caractere escolhendo o comando **salvar** no menu **arquivo** ou o botão **salvar definição de caracteres** na barra de ferramentas. Se você quiser salvar o arquivo de definição de caractere com um novo nome, escolha o comando **salvar como** no menu **arquivo** . O editor salva a definição editável de um caractere como uma definição de caractere do agente (. AD) arquivo. Você também pode editar esse formato de arquivo de texto de autodocumentação com a maioria dos editores de texto e aplicativos de processamento de textos.

### <a name="printing-your-character-definition"></a>Imprimindo sua definição de caractere

Para imprimir a definição de seu caractere, escolha o comando **Imprimir** no menu **arquivo** ou o botão **Imprimir** na barra de ferramentas. Para definir as propriedades da saída impressa, escolha o comando de **configuração de página** e escolha suas configurações antes de selecionar o comando **Imprimir** .

### <a name="building-a-character"></a>Criando um caractere

Quando você terminar de criar suas animações, o caractere e as imagens devem ser compilados em um formato especial que o Microsoft Agent usa para carregar esses dados. Para criar um caractere, selecione o comando criar caractere no menu **arquivo** ou na barra de ferramentas. Se você tiver edições não salvas no arquivo de definição de caractere, o editor salvará o arquivo de definição antes de exibir a caixa de diálogo **criar caractere** .

![Captura de tela que mostra a janela ' criar caractere ' com um arquivo selecionado.](images/f8charbldg.gif)

O editor de caracteres do agente irá propor automaticamente um nome de arquivo com base em seu nome de arquivo de definição de caractere. A caixa de diálogo Criar caractere também inclui uma lista suspensa para que você possa escolher entre criar o caractere como um único arquivo de armazenamento (. ACS) ou como vários arquivos. Se você escolher o último, o editor criará um. Arquivo ACF que inclui dados do caractere e um. Arquivo ACA para cada animação que você criou. Se você planeja instalar e acessar um caractere armazenado no mesmo computador que o aplicativo cliente, normalmente escolheria o formato de arquivo estruturado único. Esse formato fornece uma instalação fácil e eficiente e o acesso ao caractere. No entanto, se o caractere for acessado de um servidor Web usando o protocolo HTTP, crie seu caractere usando o. Formato de arquivo ACF (individual). Essa última estrutura de arquivo permite que um script de página da Web carregue arquivos de animação individuais, armazenando os dados no cache de arquivos do navegador do usuário. Ele fornece acesso mais eficiente pela Web porque os dados de animação podem ser baixados conforme necessário, em vez de exigir que o usuário aguarde até que o conjunto inteiro de animações seja baixado ao mesmo tempo. Além disso, como os dados do caractere são armazenados no cache do navegador, o espaço de arquivo pode ser recuperado automaticamente.

Embora você também possa baixar dados de caractere (como um único arquivo estruturado ou vários arquivos) de um servidor Web e instalar em outro lugar na máquina de um usuário, esse método requer provisões de segurança para download e instalação. Como resultado, a API do Microsoft Agent não inclui suporte para instalação para download de um caractere, exceto para o cache do navegador. No entanto, você ainda pode dar suporte a esse cenário criando seu próprio controle de instalação e distribuí-lo seguindo as convenções de segurança apropriadas. Para obter mais informações, consulte o kit de desenvolvimento do Microsoft Internet Client Software.

A opção compress permite que você defina se os dados de caracteres são compactados. Normalmente, você desejará definir essa opção para compactar seus dados de caractere, embora a criação de um caractere com os dados compactados demore mais.

Depois de criar um caractere, as compilações subsequentes serão mais rápidas se você criar o caractere para o mesmo local de diretório. O editor de caracteres verifica e copia automaticamente os arquivos que não foram alterados e recompila todos os dados que foram editados.

Se o editor detectar erros no arquivo de caracteres durante a criação do caractere, ele gravará as informações em um arquivo de log e exibirá uma caixa de mensagem. Você pode optar por exibir o arquivo de log ou ignorá-lo e lê-lo mais tarde com um editor de texto. No entanto, observe que o editor substituirá o arquivo de log na próxima vez que você criar um arquivo de caractere.

### <a name="editing-an-existing-character"></a>Editando um caractere existente

Para editar um caractere existente, escolha **abrir** no menu **arquivo** , selecione o arquivo de definição do caractere (. AD) na caixa de diálogo resultante e escolha abrir. O arquivo será carregado no editor. Observe que você não pode carregar arquivos de caracteres compilados (. ACS,. ACF ou. ACA) com o editor.

Porque o arquivo de definição do caractere (. AD) é um arquivo de texto, você também pode editar a definição de um caractere abrindo o arquivo com um editor de texto ou programa de processamento de textos. No entanto, ao concluir as alterações, certifique-se de salvar o arquivo em seu formato original antes de carregá-lo no editor de caracteres para compilação.

 

 




