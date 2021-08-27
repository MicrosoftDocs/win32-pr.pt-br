---
title: Mouse e ponteiros
description: O mouse é o dispositivo de entrada primário usado para interagir com objetos no Windows.
ms.assetid: 4d99287d-e908-4c8b-b4f6-6e8c91c6c93e
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: e973ad46ec864c20ad7eef5708388f86e8489909df1fdae609106d1ca65d4614
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119030175"
---
# <a name="mouse-and-pointers"></a>Mouse e ponteiros

> [!NOTE]
> este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

O mouse é o dispositivo de entrada primário usado para interagir com objetos no Windows. a funcionalidade do Mouse também pode abranger outros dispositivos apontadores, como trackball, touchpads e pontos de apontador criados em computadores notebook, canetas usadas com Tecnologia Windows Tablet and Touch e, em computadores com telas de toque, até mesmo o dedo de um usuário.

> [!NOTE]
> As diretrizes relacionadas à [acessibilidade](inter-accessibility.md), à [caneta](inter-pen.md)e ao [toque](inter-touch.md) são apresentadas em artigos separados.

Mover fisicamente o mouse move o ponteiro gráfico (também chamado de cursor) na tela. O ponteiro tem uma variedade de formas para indicar seu comportamento atual.

![captura de tela de cinco ponteiros de mouse típicos ](images/inter-mouse-image1.png)

*Ponteiros de mouse típicos*

Os dispositivos com o mouse geralmente têm um botão principal (geralmente o botão esquerdo), um botão secundário (geralmente o direito) e uma roda do mouse entre os dois. Ao posicionar o ponteiro e clicar nos botões primário e secundário do mouse, os usuários podem selecionar objetos e executar ações neles. Para a maioria das interações, pressionar um botão do mouse enquanto o cursor está sobre um destino indica o destino selecionado e soltar o botão executa qualquer ação associada ao destino.

Todos os ponteiros, exceto o ponteiro ocupado, têm um ponto de acesso de pixel único que define o local exato da tela do mouse. O ponto de acesso determina qual objeto é afetado pelas ações do mouse. Os objetos definem uma zona de acesso, que é a área em que o ponto de acesso é considerado sobre o objeto. Normalmente, a zona quente coincide com as bordas de um objeto, mas pode ser maior para facilitar a execução do usuário.

O cursor é a barra vertical piscando que é exibida quando o usuário está digitando em uma caixa de texto ou em outro editor de texto. o cursor é independente do ponteiro (por padrão, Windows oculta o ponteiro enquanto o usuário está digitando).

![captura de tela da caixa de texto com cursor ](images/inter-mouse-image2.png)

*O cursor*

## <a name="design-concepts"></a>Conceitos de design

### <a name="the-mouse-is-intuitive"></a>O mouse é intuitivo

O mouse tem sido um dispositivo de entrada com êxito porque é fácil de usar para a mão humana típica. A interação baseada em ponteiros foi bem-sucedida porque é intuitiva e permite uma ampla variedade de experiências.

**Os objetos da interface do usuário (IU) bem projetados devem ter preços acessíveis, que são visual e propriedades comportamentais de um objeto que sugere como ele é usado.** O ponteiro atua como um proxy para a mão, permitindo que os usuários interajam com objetos de tela da mesma forma que fariam com objetos físicos. Nós humanos temos uma compreensão inato de como a mão humana funciona, portanto, se algo parecer que ele pode ser enviado por push, tentaremos enviá-lo; se parecer que ele pode ser capturado, tentamos obter. Consequentemente, os usuários podem descobrir como usar objetos com uma forte unificação apenas examinando-os e experimentando-os.

![captura de tela de um botão e controle deslizante](images/inter-mouse-image3.png)

*Os botões e os controles deslizantes têm um preço forte*

Por outro lado, os objetos com baixo custo são difíceis de descobrir. Esses objetos geralmente exigem um rótulo ou instrução para explica-los.

![captura de tela de texto do link e ícone do Internet Earth](images/inter-mouse-image4.png)

*o texto do link e os ícones têm baixo custo*

### <a name="some-aspects-of-mouse-use-are-not-intuitive"></a>Alguns aspectos do uso do mouse não são intuitivos

**Clicar com o botão direito do mouse, clicar duas vezes e clicar com os modificadores de tecla Shift ou CTRL são três interações com o mouse que não são intuitivas**, pois não têm contrapartes do mundo real. Ao contrário dos atalhos de teclado e das chaves de acesso, essas interações com o mouse geralmente não estão documentadas em nenhum lugar da interface Isso sugere que clique com o botão direito do mouse, clique duas vezes e os modificadores de teclado não devem ser necessários para executar tarefas básicas, especialmente por usuários iniciantes. Ele também sugere que essas interações avançadas devem ter um comportamento consistente e previsível para ser usado com eficiência.

### <a name="single-click-or-double-click"></a>Clicar uma vez ou clicar duas vezes?

o clique duplo é usado tão extensivamente na área de trabalho Windows que talvez não pareça uma interação avançada. por exemplo, abrir pastas, programas ou documentos no painel arquivo do Windows Explorer é executado clicando duas vezes em. abrir um atalho na área de trabalho do Windows também usa um clique duplo. por outro lado, a abertura de pastas ou programas na menu Iniciar requer um único clique.

Os objetos selecionáveis usam um clique único para executar a seleção, para que eles precisem de um clique duplo para abrir, enquanto objetos não selecionáveis exigem apenas um único clique para abrir. Essa distinção não é compreendida por muitos usuários (clicar em um ícone de programa está clicando em um ícone de programa, certo?) e, como resultado, alguns usuários simplesmente continuam clicando nos ícones até obter o que desejam.

### <a name="direct-manipulation"></a>Manipulação direta

Interagir com objetos diretamente é conhecido como manipulação direta. Apontando, clicando, selecionando, movendo, redimensionando, dividindo, rolando, panorâmica e aplicando zoom são manipulações diretas comuns. Por outro lado, a interação com um objeto por meio de sua janela Propriedades ou outra caixa de diálogo pode ser descrita como manipulação indireta.

**No entanto, onde há uma manipulação direta, pode haver uma manipulação acidental e, portanto, a necessidade de Forgiveness.** O Forgiveness é a capacidade de reverter ou corrigir uma ação indesejada facilmente. Você faz manipulações diretas tolerante fornecendo desfazer, fornecendo bons comentários visuais e permitindo que os usuários corrijam os erros facilmente. Associado a Forgiveness está impedindo que ações indesejadas ocorram em primeiro lugar, o que pode ser feito usando controles restritos e confirmações para ações arriscadas ou comandos que têm consequências indesejadas.

### <a name="standard-mouse-button-interactions"></a>Interações com o botão do mouse padrão

As interações de mouse padrão dependem de uma variedade de fatores, incluindo a tecla do mouse clicada, o número de vezes em que ele é clicado, sua posição durante os cliques e se algum modificador de teclado foi pressionado. Aqui está um resumo de como esses fatores geralmente afetam a interação:

- Para a maioria dos objetos, clicar duas vezes com o botão esquerdo do mouse executa um único clique com o botão esquerdo e executa o comando padrão. O comando padrão é identificado no menu de contexto.
- Para alguns tipos de objetos selecionáveis, cada clique expande o efeito do clique. Por exemplo, clicar uma vez em uma caixa de texto define o local de entrada, clicar duas vezes seleciona uma palavra e um clique triplo seleciona uma frase ou parágrafo.
- Clicar com o botão direito do mouse exibe o menu de contexto de um objeto.
- Manter o mouse continua enquanto aponta os resultados no cursor.
- Manter o mouse ainda enquanto pressiona os botões do mouse indica um clique e uma seleção de objeto único. Mover o mouse indica Movimentação, redimensionamento, divisão, arrastar e várias seleções de objetos.
- A tecla Shift estende a seleção de forma contígua.
- A tecla CTRL estende a seleção alternando o estado de seleção do item clicado sem afetar a seleção de outros objetos.

### <a name="simple-mouse-interactions"></a>Interações simples com o mouse

A tabela a seguir descreve as interações e efeitos comuns do mouse.

| Ação simples | Interação | Efeito típico |
|:---|:---|:---|
| Apontá<br/>          | Posicione o ponteiro para um objeto específico sem clicar em nenhum botão do mouse.<br/>                                                                                                                                                                                                                                      | Destino exibe seu estado de foco e qualquer capacidades dinâmico.<br/>                                                                                                                                                                                                                                                                                                                                                         |
| Passar<br/>          | Posicione o ponteiro para um objeto específico sem clicar em nenhum botão do mouse e sem mover pelo menos um segundo.<br/>                                                                                                                                                                                             | Target exibe sua dica de ferramenta, InfoTip ou equivalente.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| Depois<br/>          | Posicione o ponteiro para um objeto específico, não selecionável, e pressione e solte um botão do mouse sem mover. Clicar Entrará em vigor na versão do botão do mouse para permitir aos usuários a oportunidade de cancelar o clique movendo o mouse para fora do destino. Portanto, pressionar o botão do mouse indica apenas o destino selecionado.<br/> | Para cliques únicos com o botão primário, ative o objeto. Para cliques duplos com o botão primário, ative o objeto e execute o comando padrão. Para o botão secundário, exiba o menu de contexto do objeto.<br/>                                                                                                                                                                                         |
| Seleção<br/>         | Posicione o ponteiro para um objeto específico e selecionável e pressione e solte um botão do mouse.<br/>                                                                                                                                                                                                                        | Para cliques únicos com o botão primário, selecione o objeto. Se os usuários arrastarem o mouse, selecione um intervalo contíguo de objetos. Para cliques duplos com o botão primário, selecione o objeto e execute o comando padrão.<br/> Para texto, o botão primário direito clica em define o ponto de inserção, o segundo seleciona o Word no ponto de inserção e o terceiro clique seleciona a frase ou o parágrafo.<br/> |
| Pressionando<br/>          | Posicione o ponteiro para um objeto específico e pressione um botão do mouse sem soltar.<br/>                                                                                                                                                                                                                              | Para funções de repetição automática (como pressionar uma seta de rolagem para rolagem contínua), ative repetidamente. Caso contrário, indica o início de um movimento, redimensionamento, divisão ou arrastar, a menos que seguido por uma versão sem movimentação.<br/>                                                                                                                                                                                               |
| Rodando<br/>          | Mova a roda do mouse.<br/>                                                                                                                                                                                                                                                                                                  | A janela rola verticalmente na direção da movimentação da roda do mouse.<br/>                                                                                                                                                                                                                                                                                                                                                      |

### <a name="pointer-shapes"></a>Formas de ponteiro

A tabela a seguir descreve formas e usos de ponteiro comuns.

| Forma | Nome | Quando usado |
|:---|:---|:---|
| ![captura de tela do ponteiro com forma de seta ](images/inter-mouse-image5.png)<br/>           | Seleção normal<br/>    | Usado para a maioria dos objetos.<br/>                                             |
| ![captura de tela da mão com o dedo indicador apontando ](images/inter-mouse-image6.png)<br/>    | Seleção de link<br/>      | Usado para links de texto e gráficos devido à sua fraca governança.<br/> |
| ![captura de tela do ponteiro com a forma de i-shape ](images/inter-mouse-image7.png)<br/>          | Seleção de texto<br/>      | Usado para texto para indicar um local entre caracteres.<br/>           |
| ![captura de tela do ponteiro com forma grande de sinal de adoção ](images/inter-mouse-image8.png)<br/> | Seleção de precisão<br/> | Usado para interação gráfica e outra bidimensional.<br/>            |

### <a name="compound-mouse-interactions"></a>Interações compostas do mouse

A tabela a seguir descreve as interações comuns do mouse.

| Ação composta | Interação | Efeito típico | Ponteiros |
|:---|:---|:---|:---|
| Movendo<br/>                | Se mover for um modo (inserido dando um comando), insira o modo , posicione o ponteiro sobre um objeto móvel, pressione o botão e mova o mouse, solte o botão do mouse. nesse caso, o ponteiro altera a forma para indicar o modo.<br/> caso contrário, posicione o ponteiro sobre o grabber de um objeto móvel, pressione o botão e mova o mouse, solte o botão do mouse. nesse caso, o ponteiro não precisa alterar a forma.<br/> | O objeto se move na direção do movimento do ponteiro.<br/>            | move<br/> ![captura de tela do ponteiro com quatro setas ](images/inter-mouse-image9.png)<br/> usado para mover uma janela em qualquer direção.<br/> panorâmico<br/> ![captura de tela do ponteiro com forma de mão ](images/inter-mouse-image10.png)<br/> Usado para mover um objeto dentro de uma janela em qualquer direção.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Redimensionamento<br/>              | Posiciona o ponteiro sobre uma borda resizável ou alça de reeslização, pressione um botão do mouse e mova o mouse e, em seguida, solte o botão do mouse.<br/>                                                                                                                                                                                                                                                                                 | O objeto resize na direção do movimento do ponteiro.<br/>          | resize vertical e horizontal<br/> ![Captura de tela que mostra ponteiros para cima para baixo.](images/inter-mouse-image11.png)![captura de tela de ponteiros para cima para baixo e para a direita ](images/inter-mouse-image12.png)<br/> usado para re dimensionar uma única dimensão.<br/> resize diagonal<br/> ![bb545459.mouse13(en-us,msdn.10).png](images/inter-mouse-image13.png)![captura de tela de ponteiros diagonais com dicas de seta](images/inter-mouse-image14.png)<br/> usado para re dimensionar duas dimensões simultaneamente.<br/> resize de linha e coluna<br/> ![bb545459.mouse15(en-us,msdn.10).png](images/inter-mouse-image15.png)![captura de tela de ponteiros de seta com barra cruzada ](images/inter-mouse-image16.png)<br/> Usado para reorganizar uma linha ou coluna em uma grade.<br/> |
| Divisão<br/>             | Posiciona o ponteiro sobre um divisor, pressione um botão do mouse e mova o mouse e solte o botão do mouse.<br/>                                                                                                                                                                                                                                                                                                          | A borda do painel dividido se move na direção do movimento do ponteiro.<br/> | divisor de janela<br/> ![bb545459.mouse17(en-us,msdn.10).png](images/inter-mouse-image17.png)![captura de tela de ponteiros de seta com barra cruzada dupla ](images/inter-mouse-image18.png)<br/> Usado para reorganizar um painel de divisão vertical ou horizontalmente.<br/> |
| Arrastando e soltando<br/> | Posiciona o ponteiro sobre um objeto válido para arrastar, pressione um botão do mouse e mova o mouse para um destino de soltar e solte o botão do mouse.<br/> | O objeto é movido ou copiado para o destino de soltar.<br/>             | seleção normal<br/> ![captura de tela de foto, ponteiro padrão e infotip ](images/inter-mouse-image19.png)<br/> usado em destinos de arrastar válidos. também pode ter uma infotip para indicar um efeito específico.<br/> indisponível<br/> ![captura de tela do pequeno ícone bloqueado/offline ](images/inter-mouse-image20.png)<br/> Usado para indicar que uma superfície não é um destino de soltar válido.<br/> |

### <a name="activity-indicators"></a>Indicadores de atividade

A tabela a seguir mostra ponteiros que os usuários veem ao executar uma ação que leva mais de alguns segundos para ser concluída.

| Forma | Nome | Quando usado |
|:---|:---|:---|
| ![Captura de tela que mostra um ponteiro "ocupado" em forma de rosca.](images/inter-mouse-image21.png)<br/>          | Ponteiro ocupado<br/>                  | Usado para aguardar uma janela se tornar responsiva.<br/>                                  |
| ![captura de tela do ponteiro e da seta em forma de rosca](images/inter-mouse-image22.png)<br/> | Trabalhando no ponteiro em segundo plano<br/> | Usado para apontar, clicar, pressionar ou selecionar enquanto uma tarefa é concluída em segundo plano.<br/> |

### <a name="hand-pointers"></a>Ponteiros de mão

Links de texto e elementos gráficos usam um ponteiro de mão ou "seleção de link" (uma mão com o dedo indicador apontando ![captura de tela da mão com o dedo indicador apontando ](images/inter-mouse-image6.png)) devido à sua fraca governança. Embora os links possam ter outras pistas visuais para indicar que são links (como sublinhados e posicionamento especial), exibir o ponteiro de mão ao passar o mouse é a indicação definitiva de um link.

**Para evitar confusão, é imperativo não usar o ponteiro de mão para outras finalidades.** Por exemplo, os botões de comando já têm uma forte governança, portanto, eles não precisam de um ponteiro de mão. O ponteiro de mão deve significar "este destino é um link" e nada mais.

### <a name="custom-pointers"></a>Ponteiros personalizados

Windows dá suporte à criação de ponteiros personalizados. Para obter mais detalhes, consulte [Configurando a imagem do cursor e](../learnwin32/setting-the-cursor-image.md) a [entrada do usuário: Exemplo estendido.](../learnwin32/user-input--extended-example.md)

Muitos aplicativos fornecem uma paleta de controles com ponteiros personalizados para dar suporte à funcionalidade do aplicativo.

![captura de tela da paleta com ponteiro de spray-can ](images/inter-mouse-image23.png)

*Microsoft Paint inclui uma paleta de funções diferentes, cada uma com um ponteiro exclusivo*

### <a name="fitts-law"></a>Lei do Fitts

A Lei do Fitts é um princípio conhecido em design de interface gráfica do usuário que basicamente declara:

- Quanto mais distante for um destino, mais tempo demorará para adquira-lo com o mouse.
- Quanto menor for o destino, mais tempo demorará para adquira-lo com o mouse.

Portanto, destinos grandes são bons. Certifique-se de tornar toda a área de destino clicável.

| Incorreto | Correto (o destino inteiro pode ser clicado) |
|:---|:---|
| ![captura de tela do ícone com apenas rótulo clicável ](images/inter-mouse-image24.png) | ![captura de tela do ícone clicável e do rótulo clicável ](images/inter-mouse-image25.png) |

Você pode alterar dinamicamente o tamanho de um destino ao apontar para facilitar a aquisição.

![captura de tela do mapa de caracteres com número ampliado ](images/inter-mouse-image26.png)

*Um destino se torna maior quando o usuário está apontando para facilitar a aquisição*

E os destinos de fechamento também são bons. Localize itens clicáveis perto de onde eles provavelmente serão usados. Na imagem a seguir, a paleta de cores está muito longe do seletor de ferramentas.

![captura de tela da paleta de cores separada das ferramentas ](images/inter-mouse-image27.png)

*A paleta de cores está muito longe de onde é provável que ela seja usada*

Considere o fato de que o local atual do ponteiro do usuário é o mais próximo possível de um destino, tornando trivial a aquisição. Assim, os menus de contexto aproveitam ao máximo a lei do Fitts, assim como as minibaras de ferramentas usadas pelo Microsoft Office.

![captura de tela de ponteiros próximo à lista de listas listadas ](images/inter-mouse-image28.png)

*O local do ponteiro atual é sempre o mais fácil de adquirir*

Além disso, considere dispositivos de entrada alternativos ao determinar tamanhos de objetos. Por exemplo, o tamanho mínimo de destino recomendado para toque é de 23x23 pixels (13x13 DLUs).

### <a name="environments-without-a-mouse"></a>Ambientes sem um mouse

Nem todos Windows ambientes têm um mouse. Por exemplo, os quiosques raramente têm um mouse e geralmente têm uma tela sensível ao toque. Isso significa que os usuários podem executar interações simples, como clicar com o botão esquerdo e, talvez, arrastar e soltar. No entanto, eles não podem passar o mouse, clicar com o botão direito do mouse ou clicar duas vezes. Essa situação é fácil de projetar porque essas limitações geralmente são conhecidas com antecedência.

Usar um mouse requer habilidades motoras finas e, como resultado, nem todos os usuários podem usar um mouse. Para tornar seu software acessível ao público mais amplo, certifique-se de que todas as interações para as quais as habilidades motoras finas não são essenciais podem ser executadas usando o teclado.

Para obter mais informações e diretrizes, consulte [Acessibilidade.](inter-accessibility.md)

**Se você fizer apenas quatro coisas...**

1.  Dê comportamentos de interações do mouse consistentes com seus efeitos padrão, usando os ponteiros padrão sempre que apropriado.
2.  Limite interações avançadas do mouse (aquelas que exigem cliques com o botão direito do mouse, vários cliques ou teclas modificadora) a tarefas avançadas direcionadas a usuários avançados.
3.  Atribua comportamentos consistentes e previsíveis às interações avançadas do mouse para que elas possam ser usadas com eficiência.
4.  Certifique-se de que seu programa fornece a capacidade de reverter ou corrigir quaisquer ações indesejáveis, especialmente para comandos destrutivas. Ações acidentais são mais prováveis ao usar a manipulação direta.

## <a name="guidelines"></a>Diretrizes

### <a name="click-affordance"></a>Clique em recursos

- **Nunca exigir que os usuários cliquem em um objeto para determinar se ele é clicável.** Os usuários devem ser capazes de determinar a capacidade de clique somente pela inspeção visual.
  - A interface do usuário primária (como botões de commit) deve ter uma capacidade de clique estático. Os usuários não devem ter que passar o mouse para descobrir a interface do usuário primária.
  - A interface do usuário secundária (como comandos secundários ou controles de divulgação progressiva) pode exibir sua responsabilidade de clique ao passar o mouse.
  - [Os links de](ctrl-links.md) texto devem sugerir estaticamente o texto do link e exibir a capacidade de clique (sublinhado ou outra alteração de apresentação, com ponteiro [de](#hand-pointers)mão ) ao passar o mouse.
  - [Os links gráficos](ctrl-links.md) exibem apenas um ponteiro de mão ao passar o mouse.
- **Use o ponteiro de mão (ou "seleção de link") somente para links de texto e gráficos.** Caso contrário, os usuários teriam que clicar em objetos para determinar se são links.

### <a name="standard-mouse-button-interactions"></a>Interações padrão do botão do mouse

A tabela a seguir resume as interações de botão do mouse que se aplicam na maioria dos casos:



| Interação                                    | Efeito                                                                                                                                                                                                                                                          |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Passar o mouse<br/>                    | O destino exibe sua dica de ferramenta, infotip ou equivalente.<br/>                                                                                                                                                                                           |
| Clique com o botão esquerdo único<br/>        | Ativa ou seleciona o objeto . Para texto, define o ponto de inserção.<br/>                                                                                                                                                                           |
| Clique com o botão direito do mouse<br/>       | Seleciona o objeto e exibe seu menu de contexto.<br/>                                                                                                                                                                                              |
| Clique duas vezes com o botão esquerdo do mouse<br/>        | Ativa ou seleciona o objeto e executa o comando padrão. Para texto, seleciona a palavra no ponto de inserção (um terceiro clique seleciona a frase ou parágrafo).<br/>                                                                            |
| Clique duas vezes com o botão direito do mouse<br/>       | O mesmo que clicar com o botão direito do mouse.<br/>                                                                                                                                                                                                                    |
| Shift único clique à esquerda<br/>  | Para objetos selecionáveis, estende contíguamente a seleção. Caso contrário, o mesmo que um único clique esquerdo com possíveis modificações. Por exemplo, no Paint, desenhar uma oval com o modificador de tecla Shift resulta no desenho de um círculo.<br/>                  |
| Shift único clique com o botão direito do mouse<br/> | O mesmo que Shift com um único clique esquerdo.<br/>                                                                                                                                                                                                               |
| Shift double left-click<br/>  | O mesmo que Shift clica com o botão esquerdo único e executa o comando padrão em toda a seleção.<br/>                                                                                                                                                     |
| Shift duplo clique com o botão direito do mouse<br/> | O mesmo que Shift com um único clique esquerdo.<br/>                                                                                                                                                                                                               |
| Ctrl com um único clique esquerdo<br/>   | Para objetos selecionáveis, estende a seleção, acionando o estado de seleção do item clicado sem afetar a seleção de outros objetos (permitindo, portanto, a seleção que não é contígua). Caso contrário, o mesmo que um único clique à esquerda.<br/> |
| Clique com o botão direito do mouse único em Ctrl<br/>  | O mesmo que Ctrl com um único clique esquerdo.<br/>                                                                                                                                                                                                                |
| Clique duas vezes com o botão esquerdo do mouse em Ctrl<br/>   | O mesmo que Ctrl com um único clique esquerdo e executa o comando padrão em toda a seleção.<br/>                                                                                                                                                      |
| Clique duas vezes com o botão direito do mouse em Ctrl<br/>  | O mesmo que Ctrl com um único clique esquerdo.<br/>                                                                                                                                                                                                                |



 

### <a name="mouse-interaction"></a>Interação do mouse

- **Faça com que os destinos de clique sejam pelo menos 16 x 16 pixels para que eles possam ser facilmente clicados por qualquer dispositivo de entrada.** Para [toque,](inter-touch.md)o tamanho mínimo recomendado do controle é de 23x23 pixels (DLUs de 13x13). Considere alterar dinamicamente o tamanho de destinos pequenos quando o usuário estiver apontando para torná-los mais fáceis de adquirir.

    Neste exemplo, os botões de controle de rotação são muito pequenos para serem usados efetivamente com toque ou uma caneta.

    ![captura de tela do controle de rotação com setas pequenas ](images/inter-mouse-image29.png) 

- **Tornar divisores com pelo menos cinco pixels de largura para que eles possam ser facilmente clicados por qualquer dispositivo de entrada.** Considere alterar dinamicamente o tamanho de destinos pequenos quando o usuário estiver apontando para torná-los mais fáceis de adquirir.

    Neste exemplo, o divisor no painel de navegação Windows Explorer é muito estreito para ser usado efetivamente com um mouse ou caneta.

    ![captura de tela de divisor estreito quase invisível ](images/inter-mouse-image30.png)

- **Forneça aos usuários uma margem de erro espacialmente.** Permita algum movimento do mouse (por exemplo, três pixels) quando os usuários liberarem um botão do mouse. Às vezes, os usuários movem o mouse ligeiramente à medida que liberam o botão do mouse, portanto, a posição do mouse logo antes da liberação do botão reflete melhor a intenção do usuário do que a posição logo após.
- **Forneça aos usuários uma margem de erro temporalmente.** Use a velocidade de clique duplo do sistema para distinguir entre cliques simples e duplos.
- **Fazer com que os cliques tenham efeito no botão do mouse para cima.** Permita que os usuários abandonem ações do mouse removendo o mouse de destinos válidos antes de liberar o botão do mouse. Para a maioria das interações do mouse, pressionar um botão do mouse indica apenas o destino selecionado e liberar o botão ativa a ação. As funções de repetição automática (como pressionar uma seta de rolagem para rolar continuamente) são uma exceção.
- [Capture o mouse](/windows/win32/api/winuser/nf-winuser-setcapture) para selecionar, mover, reizing, dividir e arrastar.
- Use a chave Esc para permitir que os usuários abandonem interações compostas do mouse, como mover, reizing, dividir e arrastar.
- **Se um objeto não dá suporte a cliques duplos, mas os usuários provavelmente supõem que sim, interprete um "clique duplo" como um único clique.** Suponha que o usuário pretenda uma única ação em vez de duas.

    Como os usuários provavelmente supõem que os botões da barra de tarefas suportam cliques duplos, um "clique duplo" deve ser tratado como um único clique.

    ![captura de tela do botão de barra de tarefas e do ponteiro padrão ](images/inter-mouse-image31.png)

- **Ignore os cliques redundantes do mouse enquanto o programa está inativo.** Por exemplo, se o usuário clicar em um botão 10 vezes enquanto um programa estiver inativo, interprete-o como um único clique.
- **Não use arrastar duplos ou instrumentos.** Um arrastar duplo é uma ação de arrastar iniciada com um clique duplo e é quando vários botões do mouse são pressionados simultaneamente. Essas interações não são padrão, não são descobriveis, são difíceis de executar e provavelmente são executadas acidentalmente.
- **Não use Alt como um modificador para interações do mouse.** A tecla Alt é reservada para chaves de acesso e acesso da barra de ferramentas.
- **Não use Shift+Ctrl como um modificador para interações do mouse.** Fazer isso seria muito difícil de usar.
- **Tornar o foco redundante.** Para tornar seu programa sensível ao toque, aproveite ao máximo o foco, mas apenas de maneiras que não são necessárias para executar uma ação. Isso geralmente significa que uma ação também pode ser executada clicando, mas não necessariamente da mesma maneira. O foco não é suportado pela maioria das tecnologias de toque, portanto, os usuários com essas telas touch não podem executar tarefas que exigem passar o mouse.

### <a name="mouse-wheel"></a>Botão de rolagem do mouse

- **Faça com que a roda do mouse afete o controle, o painel ou a janela em que o ponteiro está atualmente.** Isso evita resultados não intencionais.
- **Faça com que a roda do mouse entre em vigor sem clicar ou ter o foco de entrada.** Passar o mouse é suficiente.
- **Faça com que a roda do mouse afete o objeto com o escopo mais específico.** Por exemplo, se o ponteiro estiver sobre um controle de caixa de listagem rolável em um painel rolável dentro de uma janela rolável, a roda do mouse afetará o controle da caixa de listagem.
- **Não altere o foco de entrada ao usar a roda do mouse.**
- Dê à roda do mouse os seguintes efeitos:
  - Para janelas roláveis, painéis e controles:
    - **Girar a roda do mouse rola o objeto verticalmente, em que a rotação para cima rola para cima.** Para que a roda tenha mapeamento natural, girar a roda do mouse nunca deve rolar horizontalmente porque isso é confuso e inesperado.
      - **Se a tecla Ctrl** for pressionada, girar a roda do mouse ampliará o objeto, em que girar para cima ampliará e reduzirá o zoom.
      - **Inclinar a roda do mouse rola o objeto horizontalmente.**
  - Para janelas e painéis com zoom (sem barras de rolagem):
    - **Girar a roda do mouse amplia o objeto,** em que a rotação para cima amplia e a rotação para baixo é ampliada.
    - Inclinar a roda do mouse não tem nenhum efeito.
  - Para guias:
    - **Girar a roda do mouse pode alterar a guia atual,** independentemente da orientação das guias.
    - Inclinar a roda do mouse não tem nenhum efeito.
  - Se as teclas Shift e Alt estão desaixadas, a roda do mouse não tem nenhum efeito.
- **Use as Windows do sistema para o tamanho vertical da rolagem (para girar) e o tamanho da rolagem horizontal (para inclinação).** Essas configurações são configuráveis por meio do item do painel de controle do mouse.
- **Fazer girar a roda do mouse mais rapidamente resulta na rolagem mais rapidamente.** Isso permite que os usuários rolem documentos grandes com mais eficiência.
- **Para janelas roláveis, considere clicar no botão de roda do mouse para colocar a janela no "modo de leitor".** O modo leitor planta um ícone de origem de rolagem especial e rola a janela em uma direção e velocidade em relação à origem da rolagem.

![captura de tela da página com o ícone de origem de rolagem ](images/inter-mouse-image32.png)

*Internet Explorer dá suporte ao modo de leitor, que apresenta o ícone de origem de rolagem*

### <a name="hiding-the-pointer"></a>Ocultando o ponteiro

- **Não o oculta.** Exceções:
  - Aplicativos de apresentação em execução no modo de apresentação de tela inteira podem ocultar o ponteiro. No entanto, o ponteiro deve ser restaurado imediatamente quando os usuários movem o mouse e podem ser rehidden após dois segundos de inatividade.
  - Ambientes sem um mouse (como quiosques) podem ocultar permanentemente o ponteiro.
- Por padrão, Windows oculta o ponteiro enquanto o usuário está digitando em uma caixa de texto. Essa Windows do sistema é configurável por meio do item do painel de controle do mouse.

### <a name="activity-pointers"></a>Ponteiros de atividade

Os ponteiros de atividade Windows são o ponteiro ocupado (![captura de tela do ponteiro em forma de rosca ](images/inter-mouse-image33.png)) e o trabalho no ponteiro em segundo plano (![captura de tela do ponteiro e da seta em forma de rosca ](images/inter-mouse-image34.png)).

- Exibe o ponteiro ocupado quando os usuários têm que aguardar mais de um segundo para que uma ação seja concluída. Observe que o ponteiro ocupado não tem nenhum ponto de calor, portanto, os usuários não podem clicar em nada enquanto ele é exibido.
- Exibe o ponteiro de trabalho em segundo plano quando os usuários têm que aguardar mais de um segundo para que uma ação seja concluída, mas o programa está respondendo e não há outros comentários visuais de que a ação não foi concluída.
- Não combine ponteiros de atividade com barras de progresso ou animações de progresso.

### <a name="caret"></a>Cursor

- **Não exibir o achamado até que a janela de entrada de texto ou o controle tenha o foco de entrada.** O sinal de adoção sugere o foco de entrada para os usuários, mas uma janela ou controle pode exibir o a careta sem o foco de entrada. É claro que não roubar o foco de entrada para que uma caixa de diálogo fora do contexto possa exibir o cursor.

    O Windows Gerenciador de Credenciais é exibido fora do contexto com o a caret, mas sem o foco de entrada. Como resultado, os usuários terminam digitando sua senha em locais inesperados.

    ![captura de tela do gerenciador de credenciais sem foco ](images/inter-mouse-image35.png)

- **Coloque o a careta em que os usuários têm maior probabilidade de digitar primeiro.** Geralmente, esse é o último lugar em que o usuário estava digitando ou no final do texto.

### <a name="accessibility"></a>Acessibilidade

- Para usuários que não podem usar o mouse, faça com que o mouse seja redundante com o teclado.
  - Os usuários devem ser capazes de fazer tudo com o teclado que puderem com o mouse, exceto ações para as quais habilidades motoras finas são essenciais, como desenho e jogo.
  - Os usuários devem ser capazes de fazer tudo com o mouse que puderem com o teclado, exceto a entrada de texto eficiente.
- Para usuários com capacidade limitada de usar o mouse:
  - Não faça clique duas vezes e arraste a única maneira de executar uma ação.

Para obter mais informações e diretrizes, consulte [Acessibilidade.](inter-accessibility.md)

## <a name="documentation"></a>Documentação

Ao fazer referência ao mouse:

- Evite usar os mouses plurais; se você precisar se referir a mais de um mouse, use dispositivos do mouse.
- Use o botão do mouse para indicar o botão esquerdo do mouse. Não use o botão principal do mouse. Da mesma forma, use o botão direito do mouse em vez do botão secundário do mouse. Independentemente da precisão, os usuários entendem esses termos e os usuários que têm seus botões fazem a mudança mental.
- Use a roda para a parte giratória da roda do mouse e o botão de roda para se referir à parte clicável.
- Use verbos como clique, aponte e arraste para se referir a ações do mouse. Os usuários giram a roda verticalmente, inclinam-na horizontalmente e clicam no botão de roda.
- Use arrastar, não arrastar e soltar para a ação de mover um documento ou pasta. É aceitável usar o tipo "arrastar e soltar" como um adjetivo, como em "mover a pasta é uma operação do tipo "arrastar e soltar".
- Sempre hifenizar clique duas vezes e clique com o botão direito do mouse como verbos.
- Use clique, não clique em. Clique em (como em "clique na janela") é aceitável.

Ao fazer referência a ponteiros do mouse:

- Consulte o ponteiro do mouse como o ponteiro. Use o cursor somente na documentação técnica.
- Para ponteiros com indicadores de atividade, use o ponteiro ocupado para o ponteiro que consiste em apenas um indicador de atividade e trabalhando em ponteiro de segundo plano para o ponteiro de combinação e o indicador de atividade.
- Para os outros tipos de ponteiros, não use rótulos descritivos para se referir ao ponteiro. Se necessário, use um gráfico para descrever como o ponteiro do mouse pode aparecer na tela.

**Exemplos:**

- Aponte para a borda da janela.
- Usando o mouse, clique no botão **minimizar** .
- Mantenha pressionada a tecla Shift e clique com o botão direito do mouse.
- Quando o ponteiro se tornar um ![captura de tela de seta com dois Crossbars](images/inter-mouse-image18.png), arraste o ponteiro para mover a linha de divisão.

## <a name="see-also"></a>Confira também

- [Diretrizes de interação de acessibilidade](inter-accessibility.md)
- [Diretrizes de interação por toque](inter-touch.md)
- [Diretrizes de interação da caneta](inter-pen.md)
- [Links de texto](ctrl-links.md)
- [Links gráficos](ctrl-links.md)
- [Capturar o mouse](/windows/win32/api/winuser/nf-winuser-setcapture)
- [Definindo a imagem do cursor](../learnwin32/setting-the-cursor-image.md)
- [Entrada do usuário: exemplo estendido](../learnwin32/user-input--extended-example.md)