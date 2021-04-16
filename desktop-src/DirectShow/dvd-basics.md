---
description: Noções básicas de DVD
ms.assetid: 08357ff5-4606-4bfc-8dd6-907aca4b5f07
title: Noções básicas de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d0b2af8bc16fa0890c0103a063e750364cece0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105758474"
---
# <a name="dvd-basics"></a>Noções básicas de DVD

Os recursos que tornam o DVD atraente para os consumidores – ramificação direta, várias linguagens, controle de pais, suporte a karaokê e vários ângulos — também tornam o trabalho do desenvolvedor um pouco mais complexo. Um DVD Player não deve reproduzir fluxos de áudio, vídeo e subimagem, mas também deve manter o controle das opções de navegação que o disco está permitindo no momento e lidar corretamente com muitos tipos de comandos de usuário. O navegador de DVD protege você de grande parte dessa complexidade, permitindo que você crie um aplicativo de DVD totalmente funcional. Você não precisa se referir à especificação de DVD para usar a API do navegador de DVD com eficiência, mas precisa conhecer os conceitos básicos de navegação do DVD.

**Dados de controle de navegação**

Os dados de áudio e vídeo em um disco DVD-Video são intercalados em intervalos regulares com vários tipos de dados de controle de navegação. Esses dados podem ser uma instrução que diz ao jogador para fazer algo, por exemplo, mover para algum lugar específico no disco, ou pode ser um marcador somente informativo que informa ao Player, por exemplo, que o conteúdo a seguir tem um nível de gerenciamento pai mais alto do que o conteúdo anterior ou que a operação de ignorar capítulo está desabilitada. O Player transmite essas informações para um aplicativo, e é responsabilidade do aplicativo agir sobre ela. Esses marcadores de navegação fazem parte do que dá ao DVD seu nível mais alto de interatividade do usuário em comparação com CDs de vídeo. Um aplicativo de DVD-Player deve manipular eventos originados com o disco, bem como eventos originados com o usuário.

**Dados de áudio, vídeo e subimagem**

Um disco DVD-Video contém três tipos principais de fluxos: vídeo, áudio e subimagem.

-   O fluxo de vídeo pode conter até nove "ângulos", que podem ser considerados como subfluxos. Os autores de DVD podem incluir vários ângulos sempre que desejarem oferecer ao visualizador uma opção de ângulos de câmera do qual exibir a mesma cena. Apenas um ângulo pode estar ativo por vez. O fluxo de vídeo também contém a linha 21 de dados de legenda oculta, se existir algum.
-   Pode haver até oito fluxos de áudio separados, ou faixas, fornecendo até oito trilhas sonoras multicanal e permitindo que discos de karaokê de DVD façam uso de áudio multicanal.
-   Um DVD pode conter até 32 fluxos de *subimagem* . Eles consistem em bitmaps de 16 cores compactados com um canal alfa, que são sobrepostos sobre o vídeo. Normalmente, os fluxos de subimagem contêm legendas e botões de menu, embora também possam conter outros elementos gráficos. Um fluxo de subimagem pode ter um idioma especificado. Alguns conteúdos de subimagem são sempre mostrados e um conteúdo de subimagem é mostrado apenas se o usuário habilitá-lo.

Observe que as legendas em um fluxo de subimagem não são as mesmas que as legendas ocultas de linha-21. As legendas codificadas, que se destinam a visualizadores com deficiência auditiva, são inseridas no sinal de vídeo. Eles consistem inteiramente em cadeias de caracteres. As legendas de subimagem, por outro lado, são bitmaps gráficos. Em um dispositivo de consumidor, as legendas ocultas são exibidas pelo conjunto de televisão, enquanto o fluxo de subimagem é renderizado pelo DVD Player. Um DVD pode conter ambos os tipos de legenda.

**Títulos e capítulos**

O conteúdo de vídeo em um DVD é dividido em *títulos* e *menus*. Os títulos são divididos em unidades que a especificação de DVD chama *de partes de títulos* (PTTS). Com mais frequência, eles são chamados de *cenas* ou *capítulos*. (A documentação do DirectShow usa o termo capítulo.) O Visualizador pode navegar para títulos ou capítulos específicos em títulos.

O autor de um DVD decide como dividir o conteúdo em títulos e capítulos. Quando um DVD contém um filme de tamanho de recurso, o filme inteiro geralmente é colocado em um título, dividido em capítulos para os bastidores individuais. Recursos adicionais no DVD, como trailers ou cenas excluídos, são colocados em títulos separados. No entanto, essas divisões são arbitrárias e muitos DVDs são organizados de forma diferente.

Pode haver até 99 títulos em um disco e os autores de disco podem dividir o título em até 999 capítulos lógicos. Na maioria dos filmes de recursos em DVD, o conteúdo do filme é formatado como uma série de capítulos que automaticamente executam um após o outro. Nesses discos, o marcador de fim do capítulo contém uma instrução de ramificação que informa ao Player para continuar jogando o próximo capítulo na sequência. Esses títulos são chamados de *títulos de PGC sequenciais*. (PGC significa a cadeia de programas, outro nome para um grupo de capítulos que pertencem a juntos. Este termo não é usado na documentação do navegador de DVD.) Em discos com outros tipos de conteúdo, como discos do karaokê, um marcador de fim do capítulo pode instruir o jogador a mostrar um menu ou pode simplesmente instruir o jogador a parar.

Os desenvolvedores de aplicativos de DVD usam números de título e capítulo para saltar para pontos específicos em um disco. Para obter acesso mais preciso, um número de título e um código de tempo podem ser usados. Os códigos de tempo só podem ser usados com um título de PGC sequencial, já que outros tipos não contêm mapas de código de tempo.

**Menus**

A especificação de DVD define seis tipos de menu:

-   **Título.** O menu título é o primeiro menu a ser exibido. Normalmente, ele tem botões para selecionar títulos. O menu título também é chamado de *menu Gerenciador de vídeo*. Há apenas um menu de título em um DVD.
-   **Básica.** Um menu raiz é o menu de nível superior de um título. Cada título pode ter um menu raiz. Os quatro menus a seguir são submenus do menu raiz. Um menu raiz também é chamado de *menu de conjunto de título de vídeo*. O menu raiz normalmente tem botões que navegam para qualquer um dos títulos no conjunto de títulos. Além disso, ele pode ter submenus que permitem ao usuário escolher opções para o fluxo de áudio, o ângulo da câmera, o fluxo de subimagem ou o capítulo. No entanto, esses submenus não são usados na maioria dos DVDs.
-   **Subimagem.** O menu subimagem seleciona o fluxo de subimagem.
-   **Sonoro.** O menu áudio seleciona o fluxo de áudio. Normalmente, esse menu permite que o visualizador selecione uma faixa de idioma.
-   **Firmeza.** O menu de ângulo seleciona o ângulo da câmera.
-   **6.** O menu capítulo, também chamado de menu PTT, seleciona capítulos dentro de um título.

A maioria dos menus tem botões, que podem ser *selecionados* e *ativados*. A seleção de um botão altera a aparência do botão. Ativar um botão dispara um comando de DVD, como mostrar outro menu ou iniciar a reprodução.

**Níveis de gerenciamento de pais**

Todo ou parte de um disco de DVD pode ser codificado com um PML (nível de gerenciamento de pais) numerado de um a oito. Oito é o nível mais restritivo (somente para adultos) e um é o menos restritivo (todas as idades). A ideia é impedir que os filhos assistam a conteúdo adulto sem o consentimento dos pais, enquanto permite aos adultos assistir a conteúdo seguro para o filho. No Estados Unidos e no Canadá, os níveis são mapeados para o sistema de classificação do MPAA (G, PG, PG-13, NC-17), mas esse não é o caso em outros países ou regiões.

Como os capítulos podem existir logicamente dentro de um bloco pai, pode haver duas versões do mesmo capítulo em um título, cada uma atribuída a um PML diferente e em um bloco de pais diferente. Por exemplo, um filho que faz logon e reproduz o disco veria uma versão do capítulo 3, e um adulto que faz logon veria uma versão diferente, supondo que o aplicativo dá suporte a PMLs.

Um título ou capítulo também pode conter PMLs temporários, cujo conteúdo é classificado como maior do que o PML do título ou do capítulo como um todo. Isso significa que um título pode ter mais de um nível de pai. Os PMLs temporários geralmente são criados como blocos de ângulo, de forma que uma cena em um filme possa ter duas versões, uma classificada para espectadores mais jovens e outra para adultos.

É responsabilidade do aplicativo de Player impor os níveis de pais.

**Domínios**

O termo *domínio* refere-se ao estado interno de um DVD Player; Não é algo criado no disco. Os domínios são importantes porque alguns comandos de DVD são válidos apenas em determinados domínios. O DirectShow fornece uma maneira de consultar o domínio atual e ser notificado quando o domínio for alterado. Os seguintes domínios são definidos:

-   **Primeira reprodução.** Nesse domínio, o DVD Player acabou de começar a reproduzir o DVD. Depois de entrar no primeiro domínio de reprodução, o player alterna para outro domínio — um domínio de menu ou o domínio de título, dependendo do disco.
-   **Menu Gerenciador de vídeo.** O player está mostrando o menu Gerenciador de vídeos, também chamado de menu de título.
-   **Menu VTS.** O player está mostrando um menu associado a um conjunto de título de vídeo, o menu raiz ou um submenu (áudio, subimagem, ângulo ou capítulo).
-   **Título.** O player está reproduzindo vídeo em um título.
-   **Deixar.** O Player não está exibindo nada. (Estritamente falando, a especificação de DVD não chama esse estado de um domínio, mas pode ser tratada como uma.)

O domínio pode ser considerado como uma variável de estado que um DVD Player monitora, a fim de controlar o tipo de conteúdo que o player está lendo atualmente do disco. os players de DVD usam domínios para evitar a emissão de comandos sem sentido na unidade de DVD.

**Controles de operação do usuário**

Os UOPs (controles de operação do usuário) são marcadores em um disco que os autores de DVD podem inserir em qualquer lugar para restringir as opções de navegação do usuário. A maioria dos discos segue as restrições de UOP padrão. Por exemplo, a maioria dos discos não permite que o visualizador avance rapidamente ou mostre um menu enquanto estiver no primeiro domínio de reprodução. Em princípio, cada disco pode inserir qualquer comando UOP em qualquer ponto no disco, mesmo que o comando seja válido no domínio atual. Por exemplo, um disco pode ser criado para não permitir o encaminhamento rápido em um determinado título ou para impedir que um menu específico seja mostrado depois que o usuário inserir o domínio do título. O navegador de DVD está em conformidade com todos esses comandos do disco e não permitirá que um aplicativo substitua os controles UOP do disco.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 



