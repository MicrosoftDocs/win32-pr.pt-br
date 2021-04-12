---
title: Instalação e manutenção de jogos
description: Este artigo descreve um conjunto de práticas recomendadas que podem ajudar a reduzir a frustração do usuário sobre o tempo necessário para instalar um jogo, evitar chamadas de suporte desnecessárias e permitir que os usuários comecem a jogar o jogo de forma mais rápida e fácil possível.
ms.assetid: c953165d-2318-ca06-a895-abedcbcb594c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de171fd76654eb3b6edb8818ec073c4ef5ba8ca4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294473"
---
# <a name="installation-and-maintenance-of-games"></a>Instalação e manutenção de jogos

Este artigo descreve um conjunto de práticas recomendadas que podem ajudar a reduzir a frustração do usuário sobre o tempo necessário para instalar um jogo, evitar chamadas de suporte desnecessárias e permitir que os usuários comecem a jogar o jogo de forma mais rápida e fácil possível.

-   [Instalação inicial](#initial-installation)
    -   [Simplificando a interface do usuário de instalação](#streamlining-the-installation-ui)
    -   [Reduzindo o tempo necessário para a instalação](#reducing-the-time-required-for-installation)
    -   [Instalação mínima](#minimal-installation)
    -   [Instalar sob demanda](#install-on-demand)
-   [Jogo de pós-instalação](#post-installation-game-play)
    -   [Execução](#autorun)
    -   [Convertendo uma instalação instalada sob demanda em uma instalação completa](#converting-an-install-on-demand-installation-to-a-full-installation)
    -   [Manutenção de software e conteúdo de jogos](#maintenance-of-game-software-and-content)
    -   [Verificando se há atualizações automaticamente](#checking-for-updates-automatically)
    -   [Baixando patches automaticamente](#downloading-patches-automatically)
-   [Outros recursos](#other-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="initial-installation"></a>Instalação inicial

Os usuários compram jogos porque gostam de reproduzi-los, não porque eles gostam de instalá-los. A instalação de um jogo deve ser rápida, simples e tão simples quanto possível para o usuário final. Idealmente, os usuários finais não devem até ver uma interface do usuário de instalação; Eles devem ser capazes de simplesmente soltar o disco do jogo na bandeja e começar a jogar.

### <a name="streamlining-the-installation-ui"></a>Simplificando a interface do usuário de instalação

Os aspectos comuns das UIs de instalação de jogos existentes interferem na experiência do usuário final desejada:

-   Solicitando perguntas desnecessárias ao usuário.

    Por exemplo, muitos jogos perguntam se o usuário deseja instalar o DirectX. Se o jogo exigir que o Microsoft DirectX seja executado e a versão correta do DirectX ainda não estiver instalada, o jogo deverá simplesmente instalar o DirectX.

-   Perguntar ao usuário as perguntas que uma grande maioria dos usuários responderá da mesma maneira.

    Para usuários típicos, as configurações padrão para o caminho de instalação, o local do menu iniciar e assim por diante estão tudo bem. Ofereça opções avançadas para os usuários que desejam alterar essas configurações.

A interface do usuário de instalação deve ser projetada para permitir que o usuário típico comece a jogar o jogo o mais rápido possível. Se a execução automática estiver habilitada no computador do usuário, que é o padrão, o programa de instalação deverá assumir que o usuário deseja jogar o jogo assim que possível, ignorando as perguntas desnecessárias. A instalação progra[instalar sob demanda](#install-on-demand)m deve começar a instalar o jogo no caminho de instalação padrão, preferencialmente usando uma configuração como a descrita em. É apropriado conceder aos usuários a oportunidade de alterar as configurações de instalação antes de iniciar a instalação automaticamente. No entanto, isso deve ser feito solicitando que o usuário pressione uma tecla para as opções de configuração avançadas e continue automaticamente com as opções padrão se o usuário não atingir essa chave em cinco a dez segundos.

Se a execução automática não estiver habilitada no computador do usuário, o programa de instalação deverá assumir que o usuário não deseja que o programa de instalação comece a instalar o jogo automaticamente. Se o programa de instalação for iniciado por alguns meios diferentes de AutoRun, ele deverá iniciar a interface do usuário de instalação avançada.

### <a name="reducing-the-time-required-for-installation"></a>Reduzindo o tempo necessário para a instalação

A maioria dos jogos do Microsoft Windows hoje levará de cinco minutos a meia hora para concluir o processo de instalação. Por outro lado, a maioria dos jogos de console não leva mais de trinta segundos a partir do momento em que o usuário insere o CD do jogo até o momento em que o usuário pode jogar o jogo. Essa diferença se deve ao fato de que a maioria dos jogos do Windows foi projetada para executar a maioria, se não todo, de seu conteúdo a partir do disco rígido do computador; os consoles do, que não têm um local para armazenar permanentemente grandes quantidades de conteúdo, exigem que o conteúdo seja executado da mídia de origem. Embora o carregamento de conteúdo do disco rígido local faça tempos de carregamento mais rápidos no jogo, a desvantagem é que todo esse conteúdo precisa ser copiado da mídia de origem para o disco rígido em algum momento. A maioria dos jogos do Windows escolhe copiar todo o conteúdo no disco rígido de uma só vez, como parte de um processo de instalação. Isso se reduz da experiência inicial do usuário com o jogo fazendo com que o usuário Assista a uma barra de progresso por vários minutos antes de poder jogar o jogo.

Há duas abordagens que podem ser usadas para minimizar o tempo gasto inicialmente na instalação do jogo: [instalação mínima](#minimal-installation) e [instalação sob demanda](#install-on-demand).

### <a name="minimal-installation"></a>Instalação mínima

Em um cenário de instalação mínima, o jogo instala apenas um conjunto mínimo de conteúdo no disco rígido. Normalmente, isso consiste apenas no executável do jogo e DLLs. O restante do conteúdo é acessado diretamente da mídia de origem. Isso reduz drasticamente o tempo necessário para a instalação, pois o executável de um jogo raramente é maior do que 10-20 MB. A desvantagem é que o jogo leva mais tempo para carregar o conteúdo durante o jogo, já que ele deve carregá-lo a partir da mídia de origem mais lenta.

Para criar uma configuração de instalação mínima em uma instalação baseada em Windows Installer:

-   Agrupe todos os componentes a serem instalados no disco rígido em um recurso marcado para instalação local.

    Esse recurso será chamado de recurso de "inicialização".

-   Agrupe todos os componentes que devem ser executados da mídia de origem em um recurso que está marcado como "executar da origem".
-   Ao abrir um arquivo que pode estar na mídia de origem, use a função [**MsiGetComponentPath**](/windows/desktop/api/msi/nf-msi-msigetcomponentpatha) para determinar o caminho para o arquivo, em vez de embutir em código o caminho.

    Isso garante que o arquivo pode ser encontrado mesmo se a letra da unidade da unidade de CD/DVD do usuário for alterada.

-   Compacte o conteúdo que permanece no CD/DVD.

    A quantidade de tempo de CPU gasto com a descompactação do conteúdo normalmente será ocultada pela taxa de transferência lenta de dados da unidade de CD/DVD.

-   Agrupe o conteúdo em arquivos grandes e contíguos e acesse-os em ordem sequencial.

    Os tempos de busca das unidades de CD/DVD são ABYSMAL em comparação com aquelas de discos rígidos, e a maioria das unidades de CD/DVD não atinge as taxas de pico de transferência, a menos que estejam lendo um arquivo grande e contíguo.

-   Deite o conteúdo no CD/DVD na ordem em que é provável que ele seja acessado.

    Os tempos de busca são significativamente reduzidos quando os arquivos são acessados na mesma ordem que o layout em disco.

### <a name="install-on-demand"></a>Instalar sob demanda

Em um cenário de instalação sob demanda, como para a instalação mínima, o jogo inicialmente instala no disco rígido apenas os arquivos necessários para iniciar o jogo. No entanto, em vez de acessar o conteúdo restante da mídia de origem toda vez que for necessário, o jogo realmente instala cada parte do conteúdo no disco rígido conforme necessário pela primeira vez e, em seguida, acessa-o a partir do disco rígido local em cada uso subsequente. O tempo necessário para a instalação inicial é tão pequeno quanto no para uma instalação mínima, mas após a primeira vez que cada parte do conteúdo é acessado, os tempos de carregamento melhoram.

Para criar uma configuração de instalação sob demanda em uma instalação baseada em Windows Installer:

-   Agrupe todos os componentes a serem instalados inicialmente no disco rígido em um recurso que está marcado para ser instalado localmente.

    Observe que isso é idêntico ao recurso de inicialização para uma instalação mínima.

-   Agrupe o conteúdo restante em vários recursos com base nos componentes que provavelmente serão usados juntos.

    Por exemplo, em um jogo baseado em nível, agrupe todo o conteúdo usado em um determinado nível em um único recurso. Observe que Windows Installer permite que um componente seja compartilhado por vários recursos, portanto, se você tiver conteúdo usado em vários níveis, poderá adicionar esse conteúdo aos recursos de todos os níveis necessários sem replicar o conteúdo. Todos esses recursos devem ser marcados como "anunciados", o que significa que eles não serão instalados inicialmente, mas poderão ser instalados posteriormente, conforme necessário.

-   Quando um arquivo for necessário, verifique primeiro se o arquivo já está instalado usando a função [**MsiQueryFeatureState**](/windows/desktop/api/msi/nf-msi-msiqueryfeaturestatea).

    Se ainda não estiver instalado (ou seja, seu estado é INSTALLstate \_ anunciado), chame a função [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) para instalar o recurso localmente. Ao abrir o arquivo depois que ele for instalado, chame [**MsiGetComponentPath**](/windows/desktop/api/msi/nf-msi-msigetcomponentpatha) para determinar o caminho para o arquivo. Embora não seja estritamente necessário para esse cenário (como o conteúdo sempre será instalado no disco rígido antes de ser usado), isso torna mais fácil oferecer suporte à instalação mínima, além da instalação sob demanda.

-   Se possível, antecipar qual conteúdo provavelmente será necessário em breve e instalá-lo em segundo plano durante o tempo ocioso.

    A instalação em segundo plano é mais apropriada quando o jogo está em um ponto que não precisa de todas as últimas onças de desempenho do computador; por exemplo, ao exibir um filme de introdução, recortar cena, menu e assim por diante.

-   Crie uma opção no menu de opções do jogo para forçar a instalação de todo o conteúdo restante.

    Para implementar isso, crie um recurso que seja pai de todos os recursos de instalação sob demanda e, em seguida, chame [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) para instalar esse recurso mestre localmente. Isso fará com que os sub-recursos sejam instalados localmente também.

-   O layout do conteúdo deve ser semelhante ao de uma instalação mínima, exceto que o conteúdo deve ser clusterizado apenas com outro conteúdo que provavelmente será necessário ao mesmo tempo (por exemplo, todo o conteúdo de um nível deve estar em conjunto).

## <a name="post-installation-game-play"></a>Game-Play pós-instalação

### <a name="autorun"></a>Execução

Para participar de um jogo que já está instalado, o usuário só precisa descartar o disco de instalação na bandeja da unidade. A primeira coisa que o executável de AutoRun no disco deve fazer é verificar se o jogo já foi instalado e, nesse caso, iniciar o jogo. Supondo que o jogo foi instalado usando uma instalação baseada em Windows Installer, a verificação para determinar se o jogo está instalado pode ser realizada com uma única chamada para a função [**MsiQueryProductState**](/windows/desktop/api/msi/nf-msi-msiqueryproductstatea).

### <a name="converting-an-install-on-demand-installation-to-a-full-installation"></a>Convertendo uma instalação instalada sob demanda em uma instalação completa

Embora uma instalação de instalação sob demanda permita que o usuário comece a jogar o jogo muito antes de uma instalação completa, um usuário pode querer instalar explicitamente o restante do conteúdo do jogo no disco rígido local. O usuário pode querer ser capaz de jogar o jogo sem exigir a mídia de origem, ou talvez simplesmente queira evitar os tempos de carregamento mais longos no jogo que resultam da instalação do conteúdo sob demanda. Se a configuração do jogo usar Windows Installer, o jogo poderá fornecer uma opção na interface do usuário opções no jogo para concluir a instalação do conteúdo restante. Quando o usuário seleciona essa opção, o jogo pode chamar [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) para forçar a instalação local dos recursos restantes; Não é necessário gerar um aplicativo de instalação separado para fazer isso.

### <a name="maintenance-of-game-software-and-content"></a>Manutenção de software e conteúdo de jogos

Uma das vantagens que os jogos do Windows têm sobre jogos de console é a facilidade relativa com a qual o Publicador pode lançar atualizações para o jogo após sua versão inicial. Quer essas atualizações introduzam novo conteúdo ou apenas corrijam bugs, é importante tornar o processo de atualização o mais fácil possível para o usuário final. O processo de atualização é ainda mais importante para jogos online, o que normalmente requer que todos os usuários estejam executando a versão mais recente do jogo para se conectar.

### <a name="checking-for-updates-automatically"></a>Verificando se há atualizações automaticamente

Os usuários não devem se lembrar de buscar patches. Se houver uma atualização disponível para o jogo, o usuário deverá, pelo menos, ser notificado e, idealmente, o patch já deverá ser baixado.

Uma maneira simples de um jogo verificar se há atualizações é conectar-se a um servidor Web hospedado pelo Publicador usando uma URL específica e baixar um arquivo de texto que especifique o número da versão mais recente disponível do jogo, juntamente com uma URL da qual baixar um pacote que atualizará o jogo para a versão mais recente.

A verificação de atualizações sempre que o usuário desempenha o jogo é adequada para garantir que o usuário esteja executando a versão mais recente. No entanto, se a existência de uma nova atualização for descoberta imediatamente antes que o usuário tente jogar o jogo, o usuário poderá ser forçado a atrasar a reprodução do jogo até que o download da atualização seja concluído. Para atualizações grandes ou conexões lentas, esse atraso pode estar na ordem de horas. Para evitar forçar o usuário a aguardar antes de jogar o jogo, o jogo pode usar Agendador de Tarefas para agendar verificações periódicas em busca de novas atualizações. Se uma atualização for detectada, o jogo poderá começar a baixar a atualização imediatamente, para que seja provável que seja completamente baixado e pronto para ser instalado pela próxima vez que o usuário jogar o jogo.

### <a name="downloading-patches-automatically"></a>Baixando patches automaticamente

Depois que o jogo detectar que uma nova atualização está disponível, ele deverá começar imediatamente a baixar a atualização. Como a tarefa que verifica se há atualizações normalmente está sendo executada silenciosamente em segundo plano, o download precisa ser o mais discreto possível. O Serviço de Transferência Inteligente em Segundo Plano (BITS) é um recurso do sistema operacional que permite que os aplicativos baixem arquivos da Internet mesmo que o próprio aplicativo não esteja em execução. Os trabalhos de download do BITS são executados somente quando o usuário está conectado e somente quando o computador já está conectado à rede. O BITS não tentará forçar o computador a se conectar à rede por conta própria. Se o usuário se desconectar da rede ou fizer logoff, o trabalho do BITS será pausado e continuará o download na próxima vez que o usuário fizer logon e se conectar à rede. O aplicativo pode configurar seus trabalhos BITS para usar apenas a largura de banda de rede que, de outra forma, permaneceria não utilizada, para impedir que o trabalho afete o desempenho de quaisquer outros aplicativos que possam estar usando a rede (por exemplo, um jogo online). O BITS está disponível no Windows XP e no Windows 2000 Service Pack 3.

## <a name="other-resources"></a>Outros recursos

Para obter mais informações sobre as tecnologias mencionadas neste artigo, consulte as seções relevantes da biblioteca MSDN:

-   [Windows Installer](/windows/desktop/Msi/windows-installer-portal)
-   [Agendador de Tarefas](/windows/desktop/TaskSchd/task-scheduler-start-page)
-   [Serviço de transferência inteligente em segundo plano](/windows/desktop/Bits/background-intelligent-transfer-service-portal) (bits)

Para obter mais informações sobre como usar Windows Installer para jogos, ajuste para a coluna do DirectX de condução do próximo mês, "introdução ao Windows Installer para desenvolvedores de jogos".

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea)
</dt> <dt>

[**MsiQueryProductState**](/windows/desktop/api/msi/nf-msi-msiqueryproductstatea)
</dt> <dt>

[**MsiQueryFeatureState**](/windows/desktop/api/msi/nf-msi-msiqueryfeaturestatea)
</dt> <dt>

[**MsiGetComponentPath**](/windows/desktop/api/msi/nf-msi-msigetcomponentpatha)
</dt> </dl>

 

 