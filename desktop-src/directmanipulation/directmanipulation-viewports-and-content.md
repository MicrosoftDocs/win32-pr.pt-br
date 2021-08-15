---
description: A manipulação direta usa visores, conteúdo e contatos para descrever os elementos interativos da interface do usuário.
ms.assetid: 1564F6F2-844F-4392-9EB5-AA46059D514C
title: Visores e conteúdo
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: a103df916e5880380064250d05806169ff4187e6a8be0b22d2dd72d92343f38f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118787031"
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
- Ele contém o conteúdo que se move em resposta à interação do usuário. isso pode ser um elemento HTML div (rolagem), uma lista de panorâmica (a Windows 8 tela inicial) ou o menu pop-up para um controle select.

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

Por exemplo, se o viewport for 200x200 e o conteúdo for 1000x200 e a interface for RTL, o viewport terá sua borda esquerda em x=800 quando o viewport for apresentado pela primeira vez. Chame [**SetSnapCoordinate com**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) para especificar que os pontos de snap devem ser calculados da ordem da direita para a esquerda, começando na `SetSnapCoordinate(DIRECTMANIPULATION_MOTION_TRANSLATEX, DIRECTMANIPULATION_COORDINATE_MIRRORED, 1000.0)` borda DIREITA do conteúdo.

## <a name="behaviors"></a>Comportamentos

Um *comportamento* é um objeto que pode ser anexado [](direct-manipulation-portal.md) a um viewport para modificar como a Manipulação Direta manipula a transformação de saída do conteúdo primário ou secundário de um viewport. Um objeto de comportamento pode afetar um ou mais aspectos de uma manipulação, como como a entrada é processada ou como a animação de inércia é aplicada. Por exemplo, um comportamento de autoscroll afeta a animação de inércia executando uma animação de rolagem para uma extremidade do conteúdo primário. Um comportamento de configuração entre slides afeta o processamento de entrada de Manipulação Direta, que detecta quando uma ação entre slides está sendo executada.

Um objeto de comportamento é criado chamando [**CreateBehavior**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager2-createbehavior), adicionado a um viewport e, em seguida, seu comportamento é configurado de forma assíncrona. Remover o comportamento do viewport remove seus efeitos.

## <a name="coordinate-system"></a>Sistema de coordenadas

Há três sistemas de coordenadas principais empregados pela [Manipulação Direta:](direct-manipulation-portal.md)

- Sistema de coordenadas do cliente – descreve o retângulo da janela do cliente. As unidades estão em pixels.
- Sistema de coordenadas do viewport – descreve o retângulo de uma região dentro do cliente que pode processar a entrada. As unidades são definidas pelo aplicativo (usando [**SetViewportRect**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setviewportrect)).
- Sistema de coordenadas de conteúdo – descreve o retângulo ou o tamanho do conteúdo primário. As unidades são definidas pelo aplicativo (usando [**SetContentRect**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-setcontentrect)).

Para todos os três sistemas, as coordenadas são definidas em relação à respectiva origem superior esquerda e são positivas aumentando para a direita e para baixo. Esses sistemas de coordenadas são ilustrados no próximo diagrama. Somente a seção do conteúdo dentro do retângulo do viewport pode ser vista ou manipulada pelo usuário final.

![diagrama mostrando como as coordenadas de conteúdo, cliente e viewport interagem](images/dm-art-7.png)

## <a name="transforms"></a>Transformações

[A Manipulação](direct-manipulation-portal.md) Direta mantém várias transformação diferentes que contribuem para a saída geral exibida.

- *Transformação de* conteúdo – a transformação inicial computada pela [Manipulação Direta](direct-manipulation-portal.md) com base em uma manipulação ou inércia. Ele captura os efeitos das animações snap points, railing, overpan (manipulação), overbounce padrão (inércia) e ZoomToRect.
- *Transformação de saída* – o visual final ou a transformação de saída. É a combinação do conteúdo, bem como das transformaçãos de sincronização.
- *Transformação de* sincronização – calculada quando você chama [**SyncContentTransform.**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-synccontenttransform) Ele ajuda [a Manipulação Direta](direct-manipulation-portal.md) a aplicar uma nova transformação de conteúdo fornecida pelo aplicativo, mantendo também a transformação de saída existente.
- *Transformação de* exibição – aplicada pelo aplicativo como parte do pós-processamento. Consulte [**SyncDisplayTransform para**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-syncdisplaytransform) obter mais detalhes.

Como a transformação de saída destina-se a deslocar uma superfície visualmente na [tela,](direct-manipulation-portal.md) a Manipulação Direta executa o arredondamento necessário nos componentes de transformação de saída para que o texto e outros conteúdos sejam sempre renderizados/compostos em um limite de pixel integral. O mecanismo de arredondamento depende de vários fatores, incluindo a velocidade do movimento e a presença de Área de Trabalho Remota. O mecanismo de arredondamento para conteúdo secundário corresponde ao conteúdo primário, levando em conta a diferença no movimento entre os dois. Os clientes [**de GetOutputTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) não devem depender do mecanismo de arredondamento exato da transformação de saída, pois vários fatores a afetam.

> [!Note]
>
> Isso significa que os componentes de uma transformação de conteúdo podem não ser integrais e podem conter deslocamentos de sub pixel. Os clientes [que usam a](direct-manipulation-portal.md) Manipulação Direta são incentivados a usar o [**GetOutputTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) para calcular a transformação visual correta a ser aplicada ao conteúdo ao usar o modo de atualização manual. Ao usar o modo de atualização automática usando o compositor integrado, a Manipulação Direta aplica automaticamente essa transformação em nome do cliente. Essa transformação é gerada pela Manipulação Direta para garantir resultados visualmente desagradados ao compor a saída visual.

## <a name="viewport-state"></a>Estado do viewport

Conforme a entrada é processada, o viewport gerencia o estado de interação e o mapeamento da entrada para as transformação de saída. Verifique o estado de interação do viewport chamando [**GetStatus**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-getstatus).

![diagrama mostrando os estados de interação de directmanipulation](images/dm-states-diagram.png)

- Criação – o viewport está sendo criado e ainda não é capaz de processar a entrada. Para processar a entrada, chame [**IDirectManipulationViewport::Enable**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-enable). Se **Habilitar** não for chamado, o viewport irá para o estado Desabilitado.

    > [!Note]  
    > Esse é o estado inicial da interação.

- Habilitado – o viewport está pronto para processar a entrada. Quando um contato é baixado [**(SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) é chamado) e uma manipulação é detectada, o viewport faz a transição para Em execução.

- Em execução – atualmente, o viewport está izando a entrada e atualizando o conteúdo. Quando o contato é retirado, o viewport faz a transição para Inércia, se configurado.

- Inércia – o conteúdo está se movendo em uma animação de inércia. Depois que a inércia for concluída, o viewport fará a transição para Pronto. Se a desabilitação automática tiver sido definida no viewport, ela fará a transição de Inércia para Pronto e, em seguida, para Desabilitado.

- Pronto – o viewport está pronto para processar a entrada. Quando um contato é baixado [**(SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) é chamado) e uma manipulação é detectada, o viewport faz a transição para Em execução.

- Suspenso – o viewport pode se tornar Suspenso quando sua entrada foi promovida a um pai na [**cadeia SetContact.**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) Isso é discutido em mais detalhes em Vários [viewports: teste de impacto e hierarquia do viewport](directmanipulation-multiple-vieports.md).

- Desabilitado – o viewport não processará a entrada nem fará retornos de chamada. Um viewport pode ser desabilitado de vários estados chamando [**IDirectManipulationViewport::D isable.**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-disable) Se a desabilitação automática tiver sido definida no viewport, ela fará a transição automaticamente para Desabilitada depois que uma manipulação for processada. Para habilitar um viewport desabilitado, chame [**IDirectManipulationViewport::Enable**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-enable).

## <a name="related-topics"></a>Tópicos relacionados

[Vários viewports: teste de acerto](directmanipulation-multiple-vieports.md)e hierarquia do viewport, [**ActivateConfiguration,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration) [**GetOutputTransform,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) [**SyncDisplayTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-syncdisplaytransform)
