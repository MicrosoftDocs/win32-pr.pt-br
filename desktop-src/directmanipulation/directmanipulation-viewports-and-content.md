---
description: A Manipulação Direta usa viewports, conteúdo e contatos para descrever os elementos interativos da interface do usuário.
ms.assetid: 1564F6F2-844F-4392-9EB5-AA46059D514C
title: Viewports e conteúdo
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: a103df916e5880380064250d05806169ff4187e6a8be0b22d2dd72d92343f38f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118787031"
---
# <a name="viewports-and-content"></a>Viewports e conteúdo

[A Manipulação](direct-manipulation-portal.md) Direta *usa viewports,* *conteúdo* e contatos para descrever os elementos *interativos* da interface do usuário.

- [Configurando um viewport](#configuring-a-viewport)
- [Pontos de snap e limites](#snap-points-and-boundaries)
- [Cenários de deslocamento de ponto de snap e RTL](#snap-point-offset-and-rtl-scenarios)
- [Comportamentos](#behaviors)
- [Sistema de coordenadas](#coordinate-system)
- [Transformações](#transforms)
- [Estado do viewport](#viewport-state)
- [Tópicos relacionados](#related-topics)

Um *viewport* é uma região dentro de uma janela que pode receber e processar a entrada de interações do usuário. O viewport representa a região do conteúdo que pode ser vista pelo usuário final em um determinado momento (também chamado de clipe de conteúdo). O viewport tem várias funções:

- Ele gerencia o estado de interação (por exemplo, quando o conteúdo está pronto para ser manipulado, quando o conteúdo está passando por manipulação, quando o conteúdo está em animação de inércia) e mapeia a entrada para as transformaçãos de saída.
- Ele contém conteúdo que se move em resposta à interação do usuário. Isso pode ser um elemento div HTML (rolagem), uma lista de painéis (o Windows 8 tela inicial) ou o menu pop-up para um controle de seleção.

Um viewport é criado chamando [**CreateViewport.**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-createviewport) Vários viewports podem ser criados em uma única janela para produzir uma experiência de interface do usuário rica.

*O* conteúdo representa o elemento que é transformado em resposta a uma interação. Em outras palavras, o conteúdo é o que se move ou dimensiona à medida que o usuário faz movimento panorêneo ou pinça. Há dois tipos de conteúdo:

- *O conteúdo primário* é o único elemento intrínseco dentro de um viewport que responde a manipulações de entrada e inércia. O conteúdo primário é criado ao mesmo tempo que o viewport e não pode ser adicionado ou removido de um viewport. Você pode personalizar o comportamento do conteúdo primário usando pontos de snap (discutidos posteriormente).
- *O conteúdo secundário* se move em relação ao movimento do conteúdo primário. O conteúdo secundário é criado separadamente do viewport e pode ser adicionado ou removido de um viewport. Todas as transformação de conteúdo secundário são calculadas com base na transformação do conteúdo primário. Regras específicas podem ser aplicadas para alterar como a transformação é calculada com base na finalidade pretendida do elemento, identificada por seu CLSID durante a criação.

Neste diagrama mostrando antes e depois de uma panor abaixo, um único contato foi usado para panorcar o conteúdo primário. Embora o usuário não interaja diretamente com o indicador de panorâmico (conteúdo secundário), o conteúdo secundário se move conforme o conteúdo primário é panorâmico. Isso fornece responsabilidades visuais para a distância em que o usuário foi panorramado.

![diagrama mostrando antes/depois de uma panor](images/dm-art-2.png)

## <a name="configuring-a-viewport"></a>Configurando um viewport

Depois de criar o viewport. configure seu comportamento usando uma *configuração de interação*. A configuração de interação especifica quais manipulações, como o panorâmico, têm suporte.

*O panorâmico* altera a posição do conteúdo ao longo do eixo horizontal ou vertical ou ambos como painéis de usuário. Quando você configura a tradução em ambos os eixos, o conteúdo se move livremente em qualquer direção.

Para restringir o movimento do conteúdo, configure *os trilhos*, normalmente no eixo horizontal e vertical. Se a interação de um usuário estiver principalmente ao longo de um único eixo  (representado pelas regiões azuis no diagrama seguinte), a panorrama ficará sobrecarada e o conteúdo só se move ao longo do eixo trilho. Se o usuário tiver panorramado e estiver atualmente em um trilho e executar uma segunda panorpe enquanto o conteúdo estiver em inércia, a nova panorpe continuará sendo ressulada.

![diagrama mostrando o conteúdo dentro de um viewport em uma panorramada](images/dm-art-3.png)

Exemplo: um viewport é configurado para o panorâmico horizontal e vertical. No primeiro quadro, o contato é baixado. No segundo, uma panorpe vertical é iniciada e o contato é bloqueado para o trilho vertical. Por fim, uma vez que a panorrama está sobrecarrada, somente o componente vertical de uma panorpe diagonal é usado para mover o conteúdo.

Se o usuário faz a panorramenta diagonalmente de uma forma que não  está nas regiões de detecção de trilhos (as regiões brancas), a panorpe fica descarada e o conteúdo se move livremente em ambos os eixos.

![diagrama mostrando o conteúdo se movendo em uma panorramada](images/dm-art-4.png)

*O zoom* altera o fator de escala do conteúdo à medida que um usuário pinça ou alonga. O ponto em torno do qual o conteúdo é dimensionado (chamado de centro de zoom) está no centro dos contatos. Se você definiu o alinhamento horizontal ou vertical, o centro de zoom muda para preservar o alinhamento.

![diagrama mostrando o zoom do conteúdo com um alinhamento especificado](images/dm-art-5.png)

Você pode substituir esse comportamento especificando o centro de desbloqueio, que define o centro de zoom no centro dos contatos.

![diagrama mostrando o zoom do conteúdo com o centro de zoom desbloqueado](images/dm-art-6.png)

*A inércia* é a desaceleração gradual de uma manipulação, tanto o panorâmico quanto o zoom, depois que todos os contatos foram retirados (no caso de toque) ou após a entrada do teclado/mouse (como clicar em uma barra de rolagem ou pressionar as teclas de seta). Quando um usuário manipula o conteúdo, a manipulação não para imediatamente depois que o contato é retirado. Em vez disso, o conteúdo continua na direção e na velocidade atuais, diminuindo gradualmente para uma parada.

## <a name="snap-points-and-boundaries"></a>Pontos de snap e limites

Uma animação de inércia ocorre depois que a manipulação termina como resultado de um dedo sendo retirado da tela (no caso de toque) ou como resultado de uma ação do teclado/mouse (como teclas de direção, página para cima/para baixo, rolagem da roda do mouse etc.).

Há duas informações que definem a animação de inércia:

- O ponto restante da animação – a posição final final do componente de transformação específico.
- A duração da animação, a curva e a velocidade – elas são determinadas pelo tipo do ponto de repouso.

A animação de inércia é afetada por pontos de snap e limites. Os limites especificam os pontos de repouso máximo e mínimo para o conteúdo. Se o conteúdo atingir um limite durante a inércia, uma animação de limite será aplicada. Os pontos de snap são definidos no conteúdo primário para modificar o ponto de repouso e modificar a própria curva de animação de inércia.

Você define pontos de snap com [**SetSnapInterval**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapinterval) quando o conteúdo é espamado regularmente ou com [**SetSnapPoints**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnappoints) quando o conteúdo é espaiso desigual. Aqui está um exemplo de pontos de snap:

![diagrama mostrando como os pontos de snap definidos no conteúdo afetam o panorâmico](images/dm-snappoint-states-3.png)

No diagrama, há uma parte do conteúdo com uma série de blocos de subconjunto – itens de notícias em um aplicativo de tipo leitor de notícias ou itens em uma Exibição de Grade. A intenção é ajustar a borda esquerda de um item à borda esquerda do viewport após o fim da inércia.

Há dois grupos de tipos de ponto de snap:

- *Opcional vs. Obrigatório: um* ponto de snap opcional ajustará a animação de inércia somente se o ponto de rest de inércia estiver próximo ao ponto de snap. Um ponto de snap obrigatório sempre encaixa a animação de inércia para um ponto de snap especificado.
- *Único vs. Múltiplo:* um tipo de ponto de snap múltiplo permite que o conteúdo passe por muitos pontos de snap antes de chegar a um ponto de snap próximo de seu ponto de repouso natural. Um único tipo de ponto de snap escolhe o próximo ponto de snap mais próximo como o ponto de repouso para a animação de inércia.

O diagrama a seguir demonstra como os tipos de ponto de snap modificam a posição rest da animação de inércia.

![diagrama mostrando como a inércia e os pontos de snap interagem](images/dm-snappoint-states-1.png)

Neste diagrama, o ponto de partida de inércia é rotulado como 'Start' e a posição final de inércia natural na ausência de pontos de snap como 'End'. As linhas verticais marcam os vários pontos de alinhamento. Esta tabela descreve como cada tipo de ponto de snap afetará a posição final da animação.

| Tipo de ponto         | Descrição                                                                                |
|--------------------|--------------------------------------------------------------------------------------------|
| Obrigatório único   | O ponto de snap P1 é escolhido porque é o primeiro ponto de snap na direção da inércia     |
| Múltiplo obrigatório | O ponto de snap P2 é escolhido porque está mais próximo do ponto de extremidade na direção da inércia |
| Opcional único    | O ponto de snap P1 é escolhido porque é o primeiro ponto de snap encontrado durante a inércia      |
| Múltiplo opcional  | O ponto de snap P2 é escolhido porque está próximo ao ponto de extremidade natural                           |

## <a name="snap-point-offset-and-rtl-scenarios"></a>Cenários de deslocamento de ponto de snap e RTL

![diagrama mostrando o uso de ponto de snap rtl](images/dm-snappoint-states-2.png)

Você aplica o deslocamento do ponto de snap e o sistema de coordenadas usando a API [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) – que desloca todos os pontos de snap ou intervalos de snap usando o sistema de deslocamento/coordenadas especificado.

O sistema de coordenadas é muito útil em cenários de RTL, em que você deseja descrever pontos de snap da borda esquerda do conteúdo na direção inversa. No diagrama anterior, [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) é usado com o sinalizador **DIRECTMANIPULATION \_ MOTION \_ TRANSLATEX** e **DIRECTMANIPULATION \_ COORDINATE \_ MIRRORED,** que desloca automaticamente os pontos de snap da borda esquerda do conteúdo e os fornece na ordem da direita para a esquerda: S1 está em 0px, S2 está em 50px (e assim por diante). Qualquer conjunto de **deslocamentos usando SetSnapCoordinate** será mais deslocada dessa borda esquerda do conteúdo automaticamente, incluindo o fator de escala correto.

Você quase sempre usará [**SetSnapCoordinate com**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) o parâmetro de origem definido para evitar definir pontos de ajuste fora da área de conteúdo. 

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
