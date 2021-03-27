---
description: Quando o Shell detecta a inserção de uma nova mídia ou o anexo de um dispositivo de hot-plug, o conteúdo do dispositivo ou da mídia é determinado. A reprodução automática, dependendo de suas configurações atuais, realiza uma das ações a seguir.
title: Usando e configurando a reprodução automática
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 096c7042-8cf0-4e4f-934f-274564218f4c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 04a4f6dd09e03f26b13649e860beb7f2621ce952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646850"
---
# <a name="using-and-configuring-autoplay"></a>Usando e configurando a reprodução automática

Quando o Shell detecta a inserção de uma nova mídia ou o anexo de um dispositivo de hot-plug, o conteúdo do dispositivo ou da mídia é determinado. A reprodução automática, dependendo de suas configurações atuais, realiza uma das ações a seguir.

-   Reproduz o conteúdo automaticamente.
-   Exibe uma caixa de diálogo solicitando que o usuário escolha um manipulador padrão para um único tipo de conteúdo.
-   Apresenta, no caso de conteúdo misto, uma lista de aplicativos de manipuladores disponíveis a serem iniciados. O manipulador escolhido, em seguida, executa automaticamente seu tipo de conteúdo associado.
-   Exibe uma exibição de pasta padrão dos arquivos.
-   Não faz nada se, anteriormente, o usuário tivesse escolhido não **executar nenhuma ação** para esse tipo de conteúdo, bem como o especificado **sempre faz a ação selecionada**.

Se o conteúdo não atender aos critérios de reprodução automática, o evento será passado para a WIA (aquisição de imagem do Windows).

Os tópicos a seguir abordam a configuração e o uso da reprodução automática.

-   [Preparando o hardware e o software para uso com a reprodução automática](#preparing-hardware-and-software-for-use-with-autoplay)
-   [Como a reprodução automática pesquisa mídia](#how-autoplay-searches-media)
-   [Definindo tipos de conteúdo únicos e mistos](#defining-single-and-mixed-content-types)
-   [Cenários de exemplo](#sample-scenarios)
    -   [Reprodução automática para dispositivos de armazenamento com mídia de imagem](#autoplay-for-storage-devices-with-picture-media)
    -   [Reprodução automática de dispositivos de música e dispositivos de armazenamento com mídia de música](#autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media)
    -   [Reprodução automática para reprodução de vídeo na primeira apresentação](#autoplay-for-video-playback-on-first-presentation)
-   [Atribuindo aplicativos de manipulador padrão](#assigning-default-handler-applications)
-   [Manipulando mídia que contém tipos de conteúdo mistos](#handling-media-containing-mixed-content-types)
-   [Interfaces do usuário de reprodução automática](#autoplay-user-interfaces)
    -   [Caixa de diálogo tipo de conteúdo único](#single-content-type-dialog-box)
    -   [Caixa de diálogo mídia mista](#mixed-media-dialog-box)
    -   [Página de Propriedades](#property-page)

## <a name="preparing-hardware-and-software-for-use-with-autoplay"></a>Preparando o hardware e o software para uso com a reprodução automática

Várias informações precisam aparecer no registro para que a reprodução automática funcione. Essas informações interagem e fazem referência umas às outras para formar o ambiente completo de reprodução automática. Este documento apresenta a configuração de cada uma dessas informações como um procedimento autônomo individual.

Consulte os tópicos a seguir para obter instruções adicionais.

-   [Como atribuir um manipulador de dispositivo a um dispositivo](how-to-assign-a-device-handler-to-a-device.md)
-   [Como especificar um ícone, rótulo ou manipulador de dispositivo para um dispositivo usando um grupo de dispositivos](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md)
-   [Como especificar um ícone, rótulo ou manipulador de dispositivo para um dispositivo usando uma classe de dispositivo](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md)
-   [Como evitar a reprodução automática para um componente](how-to-prevent-autoplay-for-a-component.md)
-   [Como registrar um manipulador para um evento de dispositivo](how-to-register-a-handler-for-a-device-event.md)
-   [Como usar eventos de reprodução automática em aplicativos em execução](how-to-use-autoplay-events-in-running-applications.md)
-   [Como registrar um manipulador de eventos](how-to-register-an-event-handler.md)

## <a name="how-autoplay-searches-media"></a>Como a reprodução automática pesquisa mídia

A reprodução automática pesquisa quatro níveis de diretório de mídia abaixo do diretório raiz para encontrar tipos de arquivos conhecidos. Ele usa o valor percebido associado a uma extensão de nome de arquivo no registro para determinar a categoria do arquivo, seja uma imagem, um arquivo de áudio ou um arquivo de vídeo. Com essas informações, a reprodução automática inicia o manipulador apropriado para esse dispositivo e tipo de arquivo. Para obter mais informações, consulte [tipos observados e registro de aplicativo](fa-perceivedtypes.md).

## <a name="defining-single-and-mixed-content-types"></a>Definindo tipos de conteúdo únicos e mistos

A reprodução automática define três categorias de conteúdo principal.

-   Imagens
-   Música
-   Vídeo

Uma mídia é considerada para conter um único tipo de conteúdo se todos os arquivos na mídia se enquadram em apenas uma dessas três categorias. Observe que isso não significa que os arquivos devem ser do mesmo tipo de *arquivo* ;. jpg,. gif e. bmp são tipos de arquivo diferentes, mas um tipo de conteúdo (imagens).

Se os tipos de conteúdo com suporte estiverem presentes na mídia, mas nenhum tipo de conteúdo único puder considerar 100 por cento do total, a mídia será considerada para conter o tipo de conteúdo misto e será manipulada de acordo. Para obter mais informações, consulte [manipulando mídia que contém tipos de conteúdo mistos](#handling-media-containing-mixed-content-types).

## <a name="sample-scenarios"></a>Cenários de Exemplo

Os cenários a seguir fornecem uma compreensão básica do que esperar da reprodução automática.

### <a name="autoplay-for-storage-devices-with-picture-media"></a>Reprodução automática para dispositivos de armazenamento com mídia de imagem

1.  O usuário anexa um dispositivo de leitor USB SanDisk CompactFlash que já tem mídia inserida contendo o tipo de conteúdo de imagem de 100% na forma de arquivos. jpg.
2.  As exibições **de notificação encontraram novo hardware – SanDisk ImageMate**.
3.  A reprodução automática inicia o aplicativo de imagem apropriado.

Da mesma forma, quando o usuário insere essa mesma mídia do CompactFlash no leitor quando o leitor já está anexado ao sistema, o evento de inserção de mídia também faz com que a reprodução automática inicie o aplicativo de apresentação de slides de imagem. O usuário tem a opção de ir para a página de propriedades do dispositivo de mídia SanDisk para alterar o padrão para outro aplicativo de reprodução automática registrado, como o assistente de scanner e câmera ou o Picture It!.

### <a name="autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media"></a>Reprodução automática de dispositivos de música e dispositivos de armazenamento com mídia de música

1.  O usuário anexa um player de MP3 USB Diamond Rio.
2.  As telas de notificação **encontraram um novo hardware-Diamond Rio MP3 Player**.
3.  A reprodução automática reproduz os arquivos usando seu manipulador padrão registrado — por exemplo, o Windows Media Player.

Da mesma forma, se o usuário insere qualquer mídia contendo arquivos. mp3 (por exemplo, CompactFlash, SmartMedia, Memory Stick ou CD-ROM) que conta com 100% do conteúdo total com suporte em um dispositivo de armazenamento, o evento de inserção de mídia também faria com que a reprodução automática reproduza os arquivos usando o Windows Media Player. O usuário pode acessar a folha de propriedades do dispositivo de armazenamento e alterar a ação padrão para outro aplicativo de reprodução automática registrado, como WinAmp ou real player.

### <a name="autoplay-for-video-playback-on-first-presentation"></a>Reprodução automática para reprodução de vídeo na primeira apresentação

1.  O usuário conecta uma câmera de vídeo digital 1394 pela primeira vez.
2.  O usuário recebe uma caixa de diálogo simples que pergunta qual aplicativo deve ser executado. As opções são executar um dos aplicativos de reprodução automática registrados ou abrir uma pasta para exibir arquivos. O usuário pode definir o comportamento selecionado para ser salvo como a ação padrão para eventos de hot-plug da câmera de vídeo digital posterior.

## <a name="assigning-default-handler-applications"></a>Atribuindo aplicativos de manipulador padrão

Uma nova instalação do Windows localiza a reprodução automática com um conjunto de aplicativos de manipulador registrados. Os aplicativos registrados por padrão durante uma instalação do Windows são os seguintes.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de Mídia</th>
<th>Aplicativos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Imagens</td>
<td><ul>
<li>Apresentação de slides (padrão)</li>
<li>Assistente de câmera e scanner</li>
<li>Assistente de impressão</li>
<li>Abrir pasta</li>
</ul></td>
</tr>
<tr class="even">
<td>Música</td>
<td><ul>
<li>Windows Media Player (padrão)</li>
<li>Abrir pasta</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vídeo</td>
<td><ul>
<li>Windows Media Player (padrão)</li>
<li>Abrir pasta</li>
</ul></td>
</tr>
</tbody>
</table>



 

No caso de tipos sem suporte, os usuários são solicitados a atribuir a configuração padrão para a ação de reprodução automática associada a cada dispositivo de armazenamento na primeira introdução ao sistema. Nesse momento, o usuário será solicitado a escolher uma ação em uma lista fornecida de aplicativos registrados ou exibir uma exibição de pasta listando o conteúdo da mídia. O usuário também tem a opção de escolher ser solicitada cada vez que o tipo de mídia for detectado, em vez de salvar qualquer aplicativo específico como padrão.

> [!Note]  
> Os fabricantes de dispositivos têm a opção de registrar e atribuir aplicativos padrão a serem usados com seus produtos específicos. Nesses casos, a caixa de diálogo que oferece uma opção para o usuário não é exibida.

 

Para ser oferecido como uma opção de manipulador por reprodução automática, os aplicativos recém-instalados devem se registrar no registro. Para obter detalhes, consulte [preparando o hardware e o software para uso com a reprodução automática](#preparing-hardware-and-software-for-use-with-autoplay).

Os usuários sempre podem alterar o manipulador de reprodução automática padrão para qualquer dispositivo de armazenamento ou tipo de conteúdo. A página de propriedades de reprodução automática pode ser acessada para alteração na folha de propriedades do dispositivo de armazenamento no **meu computador**.

Para obter exemplos de prompts do usuário e páginas de propriedades, consulte [interfaces do usuário de reprodução automática](#autoplay-user-interfaces).

## <a name="handling-media-containing-mixed-content-types"></a>Manipulando mídia que contém tipos de conteúdo mistos

Quando a reprodução automática é apresentada com um meio de conteúdo misto, ela requer entrada do usuário para que possa tomar medidas. Nesse caso, o usuário recebe uma caixa de diálogo contendo uma lista filtrada de todos os aplicativos registrados apropriados disponíveis para os tipos de conteúdo presentes na mídia. O usuário pode escolher um desses aplicativos para executar uma reprodução automática desse tipo de conteúdo específico, enquanto o restante permanece inalterado. Como a composição de mídia de conteúdo misto varia de acordo com cada disco individual, não há nenhuma opção para salvar essa opção como padrão.

Para obter exemplos de prompts do usuário, consulte [interfaces do usuário de reprodução automática](#autoplay-user-interfaces).

## <a name="autoplay-user-interfaces"></a>Interfaces do usuário de reprodução automática

Há três interfaces de usuário possíveis.

-   Uma caixa de diálogo que solicita que o usuário insira uma ação para um único tipo de conteúdo
-   Uma caixa de diálogo que solicita que o usuário insira uma ação para tipos de conteúdo misto
-   Uma página de propriedades

### <a name="single-content-type-dialog-box"></a>Caixa de diálogo tipo de conteúdo único

Uma caixa de diálogo semelhante à seguinte é exibida quando qualquer mídia com suporte ainda não atribuída a uma ação de reprodução automática é apresentada ao sistema.

![captura de tela da caixa de diálogo tipo de conteúdo único](images/pix.png)

Os usuários podem executar uma das ações a seguir.

-   Escolha uma ação na lista de aplicativos registrados.
-   Liste os arquivos na mídia em um modo de exibição de pasta normal.
-   Não executar nenhuma ação.

Um usuário também pode salvar uma opção como a ação padrão para essa mídia clicando na caixa de **ação sempre fazer a seleção** . Depois que essa opção for feita, a caixa de diálogo não será mostrada novamente. No entanto, no Windows XP Service Pack 1 (SP1), se um novo aplicativo que pode manipular um determinado tipo de mídia for adicionado ao computador, a caixa de diálogo será novamente apresentada ao usuário, dando a oportunidade de selecionar o novo aplicativo como a ação de reprodução automática padrão. Os aplicativos também podem ser definidos como a seleção padrão quando são instalados.

O Windows XP SP1 também adiciona um recurso que retém a opção de ação de reprodução automática do usuário se eles não clicarem na caixa de **ação sempre fazer a seleção** . Se um usuário escolher uma ação de reprodução automática para uma única instância, na próxima vez que essa caixa de diálogo for apresentada para esse tipo de mídia, a mesma ação será a seleção padrão.

Para que um aplicativo seja incluído na lista de ações possíveis, ele deve ser registrado com a reprodução automática. Para obter mais informações, consulte [preparando o hardware e o software para uso com a reprodução automática](#preparing-hardware-and-software-for-use-with-autoplay).

### <a name="mixed-media-dialog-box"></a>Caixa de diálogo mídia mista

A caixa de diálogo a seguir é exibida quando qualquer meio contendo uma combinação de tipos de arquivo com suporte é apresentada ao sistema. Isso é essencialmente o mesmo que a caixa de diálogo meio de conteúdo único, mas com duas diferenças significativas. Primeiro, as opções de ação disponíveis consistem em uma lista filtrada de aplicativos relevantes para todos os tipos de conteúdo presentes na mídia. Em segundo lugar, não há nenhuma opção para escolher uma ação padrão permanente, pois os tipos de conteúdo e as porcentagens de mídia de conteúdo mista são muito imprevisíveis.

![captura de tela da caixa de diálogo mídia mista](images/mix.png)

Para que um aplicativo seja incluído na lista de ações possíveis, ele deve ser registrado com a reprodução automática. Para obter mais informações, consulte [preparando o hardware e o software para uso com a reprodução automática](#preparing-hardware-and-software-for-use-with-autoplay).

### <a name="property-page"></a>Página de Propriedades

Veja a seguir uma página de propriedades de reprodução automática de exemplo para um dispositivo de DVD/CD-ROM.

![captura de tela da página de propriedades](images/apdlg.png)

Cada tipo de dispositivo oferece um subconjunto apropriado de tipos de conteúdo para configuração de reprodução automática. Por sua vez, cada tipo de conteúdo, quando selecionado, oferece uma lista apropriada de opções de ação na caixa de listagem. Uma ação diferente pode ser escolhida para cada tipo de conteúdo.

 

 



