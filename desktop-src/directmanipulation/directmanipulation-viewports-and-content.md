---
description: A manipulação direta usa visores, conteúdo e contatos para descrever os elementos interativos da interface do usuário.
ms.assetid: 1564F6F2-844F-4392-9EB5-AA46059D514C
title: Visores e conteúdo
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 9cda367067ea860ce6a42a16e81d38393937276a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104551726"
---
# <a name="viewports-and-content"></a>Visores e conteúdo

A [manipulação direta](direct-manipulation-portal.md) usa *visores*, *conteúdo* e *contatos* para descrever os elementos interativos da interface do usuário.

- [Configurando um visor](#configuring-a-viewport)
- [Ajustar pontos e limites](#snap-points-and-boundaries)
- [Cenários de deslocamento e DPE do ponto de ajuste](#snap-point-offset-and-rtl-scenarios)
- [Comportamentos](#behaviors)
- [Sistema de coordenadas](#coordinate-system)
- [Transformações](#transforms)
- [Estado do visor](#viewport-state)
- [Tópicos relacionados](#related-topics)

Um *visor* é uma região dentro de uma janela que pode receber e processar a entrada de interações do usuário. O visor representa a região do conteúdo que pode ser vista pelo usuário final em um determinado momento (também chamado de clipe de conteúdo). O visor tem várias funções:

- Ele gerencia o estado de interação (por exemplo, quando o conteúdo está pronto para ser manipulado, quando o conteúdo está passando por manipulação, quando o conteúdo está na animação inércia) e mapeia a entrada para transformações de saída.
- Ele contém o conteúdo que se move em resposta à interação do usuário. Isso pode ser um elemento HTML div (rolagem), uma lista de panorâmica (a tela inicial do Windows 8) ou o menu pop-up para um controle SELECT.

Um visor é criado chamando [**createviewport**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-createviewport). Várias visores podem ser criadas em uma única janela para produzir uma experiência de interface do usuário rica.

*Conteúdo* representa o elemento que é transformado em resposta a uma interação. Em outras palavras, o conteúdo é movido ou dimensionado conforme o usuário se desloca ou pinça. Há dois tipos de conteúdo:

- O *conteúdo primário* é o único elemento intrínseco dentro de um visor que responde a manipulações de entrada e inércia. O conteúdo primário é criado ao mesmo tempo que o visor e não pode ser adicionado ou removido de um visor. Você pode personalizar o comportamento do conteúdo primário usando pontos de ajuste (discutidos posteriormente).
- O *conteúdo secundário* se move em relação ao movimento do conteúdo primário. O conteúdo secundário é criado separadamente do visor e pode ser adicionado ou removido de um visor. Todas as transformações de conteúdo secundário são calculadas com base na transformação do conteúdo primário. Regras específicas podem ser aplicadas para alterar como a transformação é calculada com base na finalidade pretendida do elemento, identificada por seu CLSID durante a criação.

Neste diagrama mostrando antes e depois de uma panorâmica, um único contato foi usado para deslocar o conteúdo principal. Embora o usuário não esteja interagindo diretamente com o indicador de panorâmica (conteúdo secundário), o conteúdo secundário é movido à medida que o conteúdo primário é panorâmico. Isso fornece indicações visuais sobre até que distância o usuário tem movimento panorâmico.

![diagrama mostrando antes/depois de uma panorâmica](images/dm-art-2.png)

## <a name="configuring-a-viewport"></a>Configurando um visor

Depois de criar o visor. configure seu comportamento usando uma *configuração de interação*. A configuração de interação especifica quais manipulações, como movimento panorâmico, têm suporte.

O *movimento panorâmico* altera a posição do conteúdo ao longo do eixo horizontal ou vertical ou tanto como um usuário. Quando você configura a tradução em ambos os eixos, o conteúdo se move livremente em qualquer direção.

Para restringir o movimento do conteúdo, configure *Rails*, normalmente no eixo horizontal e vertical. Se a interação de um usuário for basicamente ao longo de um único eixo (representado pelas regiões azuis no próximo diagrama), a Pan *se* tornará enquadrada e o conteúdo se moverá apenas ao longo do eixo Rails. Se o usuário tiver movimento panorâmico e estiver atualmente enquadrado e executar uma segunda Pan enquanto o conteúdo estiver em inércia, o novo Pan continuará a ser enquadrado.

![diagrama mostrando o conteúdo dentro de um visor em uma Pan em trilho](images/dm-art-3.png)

Exemplo: um visor é configurado para panorâmica horizontal e vertical. No primeiro quadro, o contato é desativado. No segundo, uma Pan vertical é iniciada e o contato é bloqueado para o trilho vertical. Por fim, quando a Pan é Rails, somente o componente vertical de uma panorâmica diagonal é usado para mover o conteúdo.

Se o usuário se deslocar diagonalmente de forma que *não esteja nas* regiões de detecção de trilhos (as regiões brancas), a Pan será destinada e o conteúdo será movido livremente em ambos os eixos.

![diagrama mostrando a movimentação de conteúdo em uma Pan não enquadrada](images/dm-art-4.png)

O *zoom* altera o fator de escala do conteúdo à medida que um usuário é pinçado ou ampliado. O ponto em volta do qual o conteúdo é dimensionado (chamado de centro de zoom) está no centro dos contatos. Se você tiver definido o alinhamento horizontal ou vertical, o centro de zoom mudará para preservar o alinhamento.

![diagrama mostrando o zoom do conteúdo com um alinhamento especificado](images/dm-art-5.png)

Você pode substituir esse comportamento especificando o centro de bloqueio, que define o centro de zoom no centro dos contatos.

![diagrama mostrando o zoom do conteúdo com o centro de zoom desbloqueado](images/dm-art-6.png)

*Inércia* é a desaceleração gradual de uma manipulação, o movimento panorâmico e o zoom, depois que todos os contatos tiverem sido levantados (no caso de toque) ou após a entrada do teclado/mouse (como clicar em uma barra de rolagem ou pressionar as teclas de direção). Quando um usuário manipula o conteúdo, a manipulação não é interrompida imediatamente depois que o contato é levantado. Em vez disso, o conteúdo continua na direção e velocidade atuais, diminuindo gradualmente para uma parada.

## <a name="snap-points-and-boundaries"></a>Ajustar pontos e limites

Uma animação inércia ocorre depois que a manipulação termina como resultado de um dedo ser levantado da tela (no caso de toque) ou como resultado de uma ação de teclado/mouse (como teclas de seta, página para cima/para baixo, rolagem de roda do mouse, etc).

Há duas informações que definem a animação inércia:

- O ponto de REST da animação – a posição final do componente de transformação específico.
- A duração da animação, a curva e a velocidade – elas são determinadas pelo tipo do ponto de REST.

A animação inércia é afetada por pontos de alinhamento e limites. Os limites especificam o máximo e o mínimo de pontos REST para o conteúdo. Se o conteúdo atingir um limite durante o inércia, uma animação de limite será aplicada. Os pontos de ajuste são definidos no conteúdo primário para modificar o ponto de REST e modificar a própria curva de animação inércia.

Você define pontos de ajuste com [**SetSnapInterval**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapinterval) quando o conteúdo tem um espaçamento regular ou com [**SetSnapPoints**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnappoints) quando o conteúdo tem espaçamento inigualmente. Aqui está um exemplo de pontos de ajuste:

![diagrama mostrando como os pontos de ajuste definidos no conteúdo afetam o movimento panorâmico](images/dm-snappoint-states-3.png)

No diagrama, há um pedaço de conteúdo com uma série de blocos de subconteúdo – itens de notícias em um aplicativo de tipo de leitor de notícias ou itens em uma exibição de grade. A intenção é ajustar a borda esquerda de um item na borda esquerda do visor após a finalização do inércia.

Há dois grupos de tipos de ponto de ajuste:

- *Opcional versus obrigatório*: um ponto de ajuste opcional ajustará a animação inércia somente se o ponto de REST inércia estiver próximo do ponto de ajuste. Um ponto de ajuste obrigatório sempre ajusta a animação inércia a um ponto de ajuste especificado.
- *Único vs. múltiplo*: um tipo de vários pontos de ajuste permite que o conteúdo seja movido para o final de muitos ponto de ajuste antes de chegar a um restante em um ponto de ajuste próximo ao seu ponto de REST natural. Um único tipo de ponto de ajuste escolhe o próximo ponto de ajuste mais próximo que o ponto de REST para a animação inércia.

O próximo diagrama demonstra como os tipos de ponto de ajuste modificam a posição REST da animação inércia.

![diagrama mostrando como os pontos de inércia e de encaixe interagem](images/dm-snappoint-states-1.png)

Neste diagrama, o ponto de partida inércia é rotulado como ' Start ' e a posição de extremidade de inércia natural na ausência de pontos de ajuste como ' End '. As linhas verticais marcam os vários pontos de ajuste. Esta tabela descreve como cada tipo de ponto de ajuste afetará a posição final da animação.

| Tipo de ponto         | Descrição                                                                                |
|--------------------|--------------------------------------------------------------------------------------------|
| Único obrigatório   | O ponto de ajuste P1 é escolhido porque é o primeiro ponto de ajuste na direção de inércia     |
| Múltiplo obrigatório | O ponto de ajuste P2 é escolhido porque está mais próximo do ponto de extremidade na direção do inércia |
| Opcional único    | O ponto de ajuste P1 é escolhido porque é o primeiro ponto de ajuste encontrado durante inércia      |
| Múltiplo opcional  | O ponto de ajuste P2 é escolhido porque está próximo ao ponto de extremidade natural                           |

## <a name="snap-point-offset-and-rtl-scenarios"></a>Cenários de deslocamento e DPE do ponto de ajuste

![diagrama mostrando o uso do ponto de encaixe DPE](images/dm-snappoint-states-2.png)

Aplique o deslocamento do ponto de ajuste e o sistema de coordenadas usando a API [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) – que desloca todos os pontos de ajuste ou snap-intervalos usando o sistema de deslocamento/coordenado especificado.

O sistema de coordenadas é muito útil em cenários RTL, onde você deseja descrever os pontos de ajuste da borda esquerda do conteúdo na direção inversa. No diagrama anterior, [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) é usado com o sinalizador **\_ \_ espelhado** **DIRECTMANIPULATION \_ Motion \_ TRANSLATEX** e DIRECTMANIPULATION Coordinate, que desloca automaticamente os pontos de ajuste da borda esquerda do conteúdo e os fornece na ordem da direita para a esquerda: S1 está em 0px, S2 está em 50px (e assim por diante). Qualquer conjunto de deslocamento usando **SetSnapCoordinate** será mais deslocado dessa borda esquerda do conteúdo automaticamente, incluindo o fator de escala correto.

Você quase sempre usará [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) com o parâmetro *Origin* definido para evitar a configuração de pontos de ajuste fora da área de conteúdo.

Por exemplo, se o visor for 200 x 200 e o conteúdo for 1000x200 e a interface for RTL, o visor terá sua borda esquerda em x = 800 quando o visor for apresentado pela primeira vez. Chame [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) com `SetSnapCoordinate(DIRECTMANIPULATION_MOTION_TRANSLATEX, DIRECTMANIPULATION_COORDINATE_MIRRORED, 1000.0)` para especificar que os pontos de ajuste devem ser calculados da ordem direita para a esquerda, começando da borda direita do conteúdo.

## <a name="behaviors"></a>Comportamentos

Um *comportamento* é um objeto que pode ser anexado a um visor para modificar como a [manipulação direta](direct-manipulation-portal.md) manipula a transformação de saída do conteúdo primário ou secundário de um visor. Um objeto de comportamento pode afetar um ou mais aspectos de uma manipulação, como a forma como a entrada é processada ou como a animação inércia é aplicada. Por exemplo, um comportamento de rolagem afeta a animação inércia executando uma animação de rolagem em direção a uma extremidade do conteúdo primário. Um comportamento de configuração de slide cruzado afeta o processamento de entrada de manipulação direta que detecta quando uma ação de slide cruzado está sendo executada.

Um objeto de comportamento é criado chamando [**CreateBehavior**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager2-createbehavior), adicionado a um visor e, em seguida, seu comportamento é configurado de forma assíncrona. A remoção do comportamento do visor remove seus efeitos.

## <a name="coordinate-system"></a>Sistema de coordenadas

Há três sistemas principais de coordenadas empregados pela [manipulação direta](direct-manipulation-portal.md):

- Sistema de coordenadas do cliente – descreve o retângulo da janela do cliente. As unidades estão em pixels.
- Sistema de coordenadas do visor – descreve o retângulo de uma região dentro do cliente que pode processar a entrada. As unidades são definidas pelo aplicativo (usando [**SetViewportRect**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setviewportrect)).
- Sistema de coordenadas de conteúdo-descreve o retângulo ou o tamanho do conteúdo primário. As unidades são definidas pelo aplicativo (usando [**SetContentRect**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-setcontentrect)).

Para todos os três sistemas, as coordenadas são definidas em relação à respectiva origem de cima para a esquerda e são positivas crescentes à direita e abaixo. Esses sistemas de coordenadas são ilustrados no próximo diagrama. Somente a seção do conteúdo dentro do retângulo do visor pode ser vista ou manipulada pelo usuário final.

![diagrama mostrando como as coordenadas de conteúdo, cliente e visor interagem](images/dm-art-7.png)

## <a name="transforms"></a>Transformações

A [manipulação direta](direct-manipulation-portal.md) mantém várias transformações diferentes que contribuem para a saída geral exibida.

- *Transformação de conteúdo* – a transformação inicial calculada pela [manipulação direta](direct-manipulation-portal.md) com base em uma manipulação ou inércia. Ele captura os efeitos de pontos de encaixe, trilhos, overpan padrão (manipulação), inércia (prebounce padrão) e animações de ZoomToRect.
- *Transformação de saída* -a transformação Visual final ou saída. É a combinação do conteúdo, bem como as transformações de sincronização.
- *Sincronizar transformação* – calculada quando você chama [**SyncContentTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-synccontenttransform). Ele ajuda a [manipulação direta](direct-manipulation-portal.md) a aplicar uma nova transformação de conteúdo fornecida pelo aplicativo, mantendo também a transformação saída existente.
- *Exibir transformação* – aplicada pelo aplicativo como parte do pós-processamento. Consulte [**SyncDisplayTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-syncdisplaytransform) para obter mais detalhes.

Como a transformação de saída tem como objetivo deslocar uma superfície visualmente na tela, a [manipulação direta](direct-manipulation-portal.md) executa o arredondamento necessário nos componentes de transformação de saída para que o texto e outros conteúdos sempre sejam renderizados/compostos em um limite de pixels integral. O mecanismo de arredondamento depende de vários fatores, incluindo a velocidade do movimento e a presença de Área de Trabalho Remota. O mecanismo de arredondamento para conteúdo secundário corresponde ao conteúdo principal, ao mesmo tempo em que leva em conta a diferença no movimento entre os dois. Os clientes de [**GetOutputTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) não devem depender do mecanismo de arredondamento exato da transformação de saída, pois vários fatores afetam isso.

> [!Note]
>
> Isso significa que os componentes de uma transformação de conteúdo podem não ser integrantes e podem conter deslocamentos de sub-pixel. Os clientes que usam a [manipulação direta](direct-manipulation-portal.md) são incentivados a usar o [**GetOutputTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) para calcular a transformação visual correta a ser aplicada ao conteúdo ao usar o modo de atualização manual. Ao usar o modo de atualização automática usando o compositor interno, a manipulação direta aplica automaticamente essa transformação em nome do cliente. Essa transformação é gerada pela manipulação direta para garantir resultados visualmente agradáveis ao compor a saída Visual.

## <a name="viewport-state"></a>Estado do visor

À medida que a entrada é processada, o visor gerencia o estado de interação e o mapeamento de entrada para transformações de saída. Verifique o estado de interação do visor chamando [**GetStatus**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-getstatus).

![diagrama mostrando os Estados de interação do directmanipulation](images/dm-states-diagram.png)

- Compilando – o visor está sendo criado e ainda não é capaz de processar a entrada. Para processar a entrada, chame [**IDirectManipulationViewport:: Enable**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-enable). Se **Enable** não for chamado, o visor vai para o estado Disabled.

    > [!Note]  
    > Esse é o estado inicial da interação.

- Habilitado – o visor está pronto para processar a entrada. Quando um contato é inativo (o [**setcontact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) é chamado) e uma manipulação é detectada, o visor faz a transição para em execução.

- Em execução – o visor está processando a entrada e atualizando o conteúdo no momento. Quando o contato é levantado, o visor faz a transição para inércia, se configurado.

- Inércia – o conteúdo está sendo movido em uma animação inércia. Quando o inércia for concluído, o visor passará para pronto. Se a desabilitação automática tiver sido definida no visor, ela fará a transição de inércia para pronto e, em seguida, para desabilitada.

- Pronto – o visor está pronto para processar a entrada. Quando um contato é inativo (o [**setcontact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) é chamado) e uma manipulação é detectada, o visor faz a transição para em execução.

- Suspenso – o visor pode se tornar suspenso quando sua entrada for promovida para um pai na cadeia [**setcontact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) . Isso é discutido com mais detalhes em [vários visores: teste de clique e hierarquia do visor](directmanipulation-multiple-vieports.md).

- Desabilitado – o visor não processará a entrada nem fará retornos de chamada. Um visor pode ser desabilitado de vários Estados chamando [**IDirectManipulationViewport::D isaptod**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-disable). Se a desabilitação automática tiver sido definida no visor, ela passará automaticamente para desabilitada depois que uma manipulação for processada. Para reabilitar um visor desabilitado, chame [**IDirectManipulationViewport:: Enable**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-enable).

## <a name="related-topics"></a>Tópicos relacionados

[Vários visores: teste de clique e hierarquia de visor](directmanipulation-multiple-vieports.md), [**ActivateConfiguration**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration), [**GetOutputTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform), [**SyncDisplayTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-syncdisplaytransform)
