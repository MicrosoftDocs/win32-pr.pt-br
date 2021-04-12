---
title: Como projetar UX para aplicativos de área de trabalho
description: Um ótimo aplicativo de área de trabalho é poderoso e, ao mesmo tempo, simples. Por meio da seleção e apresentação de recursos cuidadosamente balanceadas, você pode alcançar tanto a potência quanto a simplicidade.
ms.assetid: 0039a3ee-95bc-457f-a1a8-6a036ce22fd2
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 74433514f61b37ba1c9941c8134767be5458ebc8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104297862"
---
# <a name="how-to-design-a-great-user-experience-for-desktop-applications"></a>Como criar uma excelente experiência de usuário para aplicativos de área de trabalho

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Um ótimo aplicativo de área de trabalho é poderoso e, ao mesmo tempo, simples. Por meio da seleção e apresentação de recursos cuidadosamente balanceadas, você pode alcançar tanto a potência quanto a simplicidade.

**Dota**

![captura de tela da caixa de diálogo ortografia e gramática ](images/powerful-simple-image1.png)

**Potente e simples:**

![captura de tela da lista de possíveis revisões de ortografia ](images/powerful-simple-image2.png)

O aplicativo ideal baseado no Windows é poderoso e simples. É claro que você deseja que seu aplicativo seja poderoso e é claro que você deseja que ele seja simples, mas pode conseguir ambos? Há uma tensão natural entre essas metas, mas essa tensão está longe de Irreconcilable. Você pode atingir a potência e a simplicidade por meio da seleção e apresentação de recursos cuidadosamente equilibrados.

## <a name="what-makes-an-application-powerful"></a>O que torna um aplicativo poderoso?

O que significa "potência" realmente em termos de software? Um aplicativo pode ser considerado poderoso se estiver repleto de recursos, tendo uma grande variedade de funcionalidades em uma tentativa de ser tudo para todos os usuários. Esse design não é provavelmente bem-sucedido, pois um conjunto de recursos não-direcionados é improvável de atender às necessidades de qualquer pessoa. Esse não é o tipo de potência que estamos depois.

Um aplicativo é poderoso quando tem a combinação certa dessas características:

-   **Habilita.** O aplicativo atende às necessidades de seus usuários de destino, permitindo que eles executem tarefas que não podiam fazer de outra forma e atinjam suas metas com eficiência.
-   **Eficiente.** O aplicativo permite que os usuários executem tarefas com um nível de produtividade e escala que não era possível antes.
-   **Versátil.** O aplicativo permite que os usuários executem uma ampla gama de tarefas com eficiência em várias circunstâncias.
-   **Encaminhe.** O aplicativo parece que ele está ajudando diretamente os usuários a atingir suas metas, em vez de entrar no caminho ou exigir etapas desnecessárias. Recursos como atalhos, acesso ao teclado e macros melhoram a sensação de direção.
-   **Flexível.** O aplicativo permite que os usuários concluam o controle refinado sobre seu trabalho.
-   **Totalmente.** O aplicativo é bem integrado ao Microsoft Windows, permitindo que ele compartilhe dados com outros aplicativos.
-   **Avançado.** O aplicativo tem recursos extraordinários, inovadores e de ponta que não são encontrados nas soluções concorrentes.

Algumas dessas características dependem da percepção do usuário e são relativas aos recursos atuais dos usuários. O que é considerado poderoso pode mudar ao longo do tempo, portanto, o recurso de pesquisa avançada de hoje pode ser comum amanhã.

Todas essas características podem ser combinadas em nossa definição de energia:

**Um aplicativo é poderoso quando permite que os usuários de destino percebam todo o potencial com eficiência.**

Assim, a medida final do poder é a produtividade, não o número de recursos.

Usuários diferentes precisam de ajuda para atingir seu potencial completo de maneiras diferentes. O que está sendo habilitado para alguns usuários pode prejudicar a versatilidade, a direção e o controle para outras pessoas. O software bem projetado deve balancear essas características adequadamente. Por exemplo, um sistema de publicação de área de trabalho projetado para não profissionais pode usar assistentes para orientar os usuários por meio de tarefas complexas. Esses assistentes permitem que os usuários de destino executem tarefas que, de outra forma, não poderiam executar. Por outro lado, um sistema de publicação de área de trabalho para profissionais pode se concentrar na direção, na eficiência e no controle total. Para usuários desse aplicativo, os assistentes podem estar limitando e frustrantes.

**Se você fizer apenas uma coisa...**

Entenda os objetivos dos usuários de destino e crie um conjunto de recursos que permita atingir essas metas de forma produtiva.

## <a name="what-makes-a-user-experience-simple"></a>O que torna uma experiência do usuário simples?

Definimos a simplicidade da seguinte maneira:

**Simplicidade é a redução ou a eliminação de um atributo de um design para o qual os usuários de destino estão cientes e consideram indispensável.**

Na prática, a simplicidade é obtida selecionando-se o conjunto de recursos correto e apresentando os recursos da maneira correta. Isso reduz os não essenciais, tanto reais quanto percebidos.

A simplicidade depende da percepção dos usuários. Considere como o efeito de uma transmissão automática depende da perspectiva de um usuário:

-   Para o driver típico (o usuário de destino), uma transmissão automática elimina a necessidade de um turno de engrenagem manual e uma embreagem, tornando um carro muito mais fácil de impulsionar. Uma mudança e uma embreagem manual de engrenagem não são essenciais para a tarefa de condução, portanto, elas são removidas para obter simplicidade.
-   Para um driver de carro de corrida profissional, ter controle direto sobre a transmissão é essencial para ser competitivo. Uma transmissão automática afeta negativamente o desempenho do carro e, portanto, não é considerada como resultado em simplicidade.
-   Para um mecânico, uma transmissão automática é um mecanismo mais complexo e, portanto, não é mais fácil de reparar ou manter do que uma transmissão manual. Diferentemente do mecânico, o usuário de destino está tranqüilamente ciente dessa complexidade interna.

Embora diferentes usuários considerem a transmissão automática de forma diferente, ele é bem-sucedido porque elimina a necessidade de conhecimento, habilidades e esforço indispensável dos usuários de destino. Para o driver típico, a transmissão automática é um ótimo recurso porque simplesmente funciona.

### <a name="simplicity-vs-ease-of-use"></a>Simplicidade versus facilidade de uso

A simplicidade, quando aplicada corretamente, resulta em facilidade de uso. Mas a simplicidade e a facilidade de uso não são os mesmos conceitos. A facilidade de uso é obtida quando os usuários podem executar uma tarefa com êxito por conta própria sem dificuldade ou confusão dentro de um período adequado. Há várias maneiras de obter facilidade de uso e simplicidade — a redução do indispensável — é apenas uma delas.

Todos os usuários, não importa a sofisticação, desejam realizar seu trabalho com uma quantidade mínima de esforço desnecessário. Todos os usuários, até mesmo usuários avançados, são motivados principalmente para realizar seu trabalho, não para aprender sobre computadores ou seu aplicativo.

A simplicidade é a maneira mais eficaz de se obter facilidade de uso e a facilidade de uso é igual ao uso. Os recursos complexos e difíceis de usar simplesmente não são usados. Por outro lado, designs simples e elegantes que executam sua função bem são uma alegria de usar. Elas chamam uma resposta positiva e emocional.

Por exemplo, considere o suporte de rede sem fio no Microsoft Windows XP. A Microsoft pode ter adicionado um assistente para orientar os usuários pelo processo de configuração. Essa abordagem teria resultado na facilidade de uso, mas não na simplicidade, porque um recurso indispensável (o assistente) teria sido adicionado. Em vez disso, a Microsoft projetou a rede sem fio para se configurar automaticamente. Por fim, os usuários não se preocupam com os detalhes da configuração, desde que "simplesmente funcione" de forma confiável e segura. Essa combinação de potência e simplicidade em tecnologia de rede sem fio levou à sua popularidade e adoção rápida.

**Se você fizer apenas uma coisa...**

Inicie seu processo de design com os designs mais simples que fazem o trabalho bem.

Se você não estiver satisfeito com o design atual, comece removendo todos os elementos indispensávels. Você verá que o que resta é geralmente muito bom.

## <a name="obtaining-simplicity-while-maintaining-power"></a>Obtendo simplicidade ao manter o poder

### <a name="design-principles"></a>Princípios de design

Para obter simplicidade, sempre projete para o provável, não o possível.

O possível

Decisões de design com base no que é possível para interfaces de usuário complexas como o editor do registro, em que o design pressupõe que todas as ações são igualmente possíveis e, como resultado, exigem um esforço igual. Como tudo é possível, as metas de usuário não são consideradas em decisões de design.

O provável

Decisões de design com base na provável liderança em soluções simplificadas, de metas e baseadas em tarefas, nas quais os cenários prováveis recebem foco e exigem um mínimo de esforço para serem executados.

O princípio de design de simplicidade

**Para obter simplicidade, concentre-se no que é provável; reduzir, ocultar ou remover o que é improvável; e elimine o que é impossível.**

O que os usuários farão é muito mais relevante para o design do que eles podem fazer.

### <a name="design-techniques"></a>Técnicas de design

Para obter simplicidade enquanto mantém a energia, escolha o **conjunto certo de recursos**, localize os recursos **nos locais certos** e **reduza o esforço** para usá-los. Esta seção fornece algumas técnicas comuns para atingir essas metas.

Escolhendo o conjunto de recursos correto

"A perfeição é alcançada, não quando não há nada mais a ser adicionado,

Mas quando não há nada a ser retirado. " — Antoine de Saint-Exupery

As técnicas de design a seguir fornecem aos seus usuários os recursos de que eles precisam ao alcançar a simplicidade por meio da redução ou da remoção real:

-   **Determine os recursos de que seus usuários precisam.** Entenda as necessidades dos usuários por meio da meta, do cenário e da análise de tarefas. Determine um conjunto de recursos que realiza esses objetivos.
-   **Remova elementos desnecessários.** Remova os elementos que provavelmente não serão usados ou que tenham alternativas preferíveis.
-   **Remova a redundância desnecessária.** Pode haver várias maneiras efetivas de executar uma tarefa. Para obter simplicidade, tome a decisão e escolha a melhor para os usuários de destino, em vez de fornecer todos eles e escolher uma opção.
-   **Faça com que "simplesmente funcione" automaticamente.** O elemento é necessário, mas qualquer interação do usuário para fazê-lo funcionar não é porque há um comportamento ou configuração padrão aceitável. Para obter simplicidade, faça com que ele funcione automaticamente e o oculte do usuário completamente ou reduza sua exposição significativamente.

Simplificando a apresentação

"A capacidade de simplificar significa eliminar o

para que seja necessário falar. " — Hans Hofmann

Use as seguintes técnicas de design para preservar a energia, oferecendo, ao mesmo tempo, a simplicidade por meio da percepção da redução ou remoção:

-   **Combine o que deve ser combinado.** Coloque os recursos essenciais que dão suporte a uma tarefa em conjunto para que uma tarefa possa ser executada em um único lugar. As etapas da tarefa devem ter um fluxo unificado e simplificado. Divida tarefas complexas em um conjunto de etapas fáceis e claras, para que "um" local possa consistir em várias superfícies de interface do usuário, como um assistente.
-   **Separe o que deve ser separado.** Nem tudo pode ser apresentado em um único lugar, portanto, sempre tenha limites claros e bem escolhidos. Torne os recursos que dão suporte a cenários principais centrais e óbvios e oculte a funcionalidade opcional ou torne o periférico. Separe as tarefas individuais e forneça links para tarefas relacionadas. Por exemplo, as tarefas relacionadas à manipulação de fotos devem ser claramente separadas das tarefas relacionadas ao gerenciamento de coleções de fotos, mas elas devem estar prontamente acessíveis entre si.
-   **Elimine o que pode ser eliminado.** Faça uma cópia impressa do design e realce os elementos usados para executar as tarefas mais importantes. Até mesmo realce as palavras individuais no texto da interface do usuário que comunicam informações úteis. Agora, examine o que não está realçado e considere removê-lo do design. Se você remover o item, ocorreria algo errado? Caso contrário, remova-o!
-   A consistência, a capacidade de configurabilidade e a generalização são geralmente qualidades desejáveis, mas podem levar à complexidade desnecessária. Examine o design de esforços com orientação inadequada em consistência (como com texto redundante), generalização (como ter qualquer número de fusos horários quando dois é suficiente) e a capacidade de configurabilidade (como opções que os usuários não têm probabilidade de alterar) e elimine o que pode ser eliminado.
-   **Coloque os elementos no lugar certo.** Dentro de uma janela, o local de um elemento deve seguir seu utilitário. Os controles, as instruções e as explicações essenciais devem estar no contexto em ordem lógica. Se mais opções forem necessárias, expor-as no contexto clicando em uma divisa ou mecanismo semelhante; se mais informações forem necessárias, exiba uma InfoTip ao focalizar o mouse. Coloque tarefas, opções e informações de ajuda menos importantes fora do fluxo principal em uma janela ou página separada. A técnica de exibir detalhes adicionais conforme necessário é chamada de divulgação progressiva.
-   **Use combinações significativas de alto nível.** Geralmente, é mais simples e mais escalonável selecionar e manipular grupos de elementos relacionados do que elementos individuais. Exemplos de combinações de alto nível incluem pastas, temas, estilos e grupos de usuários. Essas combinações geralmente são mapeadas para uma meta ou intenção de usuário que não é aparente dos elementos individuais. Por exemplo, a intenção por trás do Alto Contraste esquema de cor preta é muito mais aparente do que a de um plano de fundo de janela preta.
-   **Selecione os controles certos.** Os elementos de design são incorporados pelos controles que você usa para representá-los, portanto, selecionar o controle certo é crucial para uma apresentação eficiente. Por exemplo, a caixa de seleção de fontes usada pelo Microsoft Word mostra uma visualização da fonte, bem como as fontes usadas mais recentemente. Da mesma forma, a maneira como o Word mostra possíveis erros de ortografia e gramática é muito mais simples do que a alternativa da caixa de diálogo, conforme mostrado no início deste artigo.

Reduzindo o esforço

"Coisas simples devem ser simples.

Coisas complexas devem ser possíveis. " – Alan Kay

As seguintes técnicas de design resultam em um esforço reduzido para os usuários:

-   **Tornar as tarefas detectáveis e visíveis.** Todas as tarefas, mas especialmente tarefas frequentes, devem ser prontamente detectáveis na interface do usuário. As etapas necessárias para executar tarefas devem estar visíveis e não devem depender da memorização.
-   **Apresente as tarefas no domínio do usuário.** O software complexo exige que os usuários mapeiem seus problemas para a tecnologia. O software simples faz esse mapeamento para eles apresentando o que é natural. Por exemplo, um recurso de redução de olhos vermelhos mapeia diretamente para o espaço problemático e não exige que os usuários considerem em termos de detalhes como matizes e gradientes.
-   **Coloque o conhecimento do domínio no programa.** Os usuários não devem ser solicitados a acessar informações externas para usar o aplicativo com êxito. O conhecimento do domínio pode variar de dados complexos e algoritmos para simplesmente torná-lo claro que tipo de entrada é válido.
-   **Use o texto que os usuários entendem.** O texto bem criado é crucial para a comunicação eficaz com os usuários. Use conceitos e termos familiares aos seus usuários. Explique totalmente o que está sendo solicitado em linguagem sem formatação para que os usuários possam tomar decisões inteligentes e informadas.
-   **Use padrões seguros, seguros e prováveis.** Se uma configuração tiver um valor que se aplica à maioria dos usuários na maioria das circunstâncias, e essa configuração for segura e segura, use-a como o valor padrão. Fazer com que os usuários especifiquem valores somente quando necessário.
-   **Restrições de uso.** Se houver muitas maneiras de executar uma tarefa, mas apenas algumas estiverem corretas, restrinja a tarefa às maneiras corretas. Os usuários não devem ter permissão para fazer erros prontamente preventivos.

### <a name="simplicity-does-not-mean-simplistic"></a>A simplicidade não significa simplista

"Tudo o que deve ser feito o mais simples possível,

Mas não é mais simples ". — Albert Einstein

Acreditamos que a simplicidade é crucial para uma experiência de usuário eficaz e desejável — mas sempre é possível fazer um bom ponto muito distante. A essência da simplicidade é a redução ou a eliminação da indispensável. A remoção da Essential só produz um design ruim. Se a "simplificação" resultar em usuários que se tornaram frustrados, confusos, não confiáveis ou não conseguirem concluir as tarefas com êxito, você removerá muito.

### <a name="simplicity-does-mean-more-effort-for-you"></a>A simplicidade significa mais esforço para você

"Só fiz essa letra por mais tempo porque tenho

Não é o momento de torná-lo mais curto. " — Blaise Pascal

A obtenção de simplicidade enquanto preserva a energia geralmente exige uma complexidade interna significativa. Geralmente, é mais fácil criar um software que exponha toda a tecnologia que está contratando do que criar um que o oculte — o último requer uma compreensão excelente dos seus usuários de destino e suas metas. A remoção de um recurso requer disciplina, como a decisão de adicionar esse recurso interessante que realmente não é prático. A simplicidade exige a criação de opções de design rígido em vez de tornar tudo configurável. O software complexo geralmente resulta de um equívoco sobre os usuários: que eles são recursos não utilizados ou recursos muito complexos que não podem entender.

## <a name="powerful-and-simple"></a>Potente e simples

O poder é para habilitar seus usuários e torná-los produtivos. A simplicidade é a remoção dos recursos não essenciais e de apresentação da maneira correta. Ao compreender os usuários de destino e obter o equilíbrio certo dos recursos e da apresentação, você pode criar aplicativos baseados no Windows que fazem ambos.

 

 