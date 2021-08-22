---
title: Como projetar o UX para aplicativos da área de trabalho
description: Um ótimo aplicativo de área de trabalho é poderoso e, ao mesmo tempo, simples. Por meio da seleção e apresentação de recursos cuidadosamente equilibradas, você pode obter potência e simplicidade.
ms.assetid: 0039a3ee-95bc-457f-a1a8-6a036ce22fd2
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a9c191a92ccf6147d37deca191a861220c4a925035bf39c92e7e7d062fa14184
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119221718"
---
# <a name="how-to-design-a-great-user-experience-for-desktop-applications"></a>Como criar uma ótima experiência do usuário para aplicativos da área de trabalho

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Um ótimo aplicativo de área de trabalho é poderoso e, ao mesmo tempo, simples. Por meio da seleção e apresentação de recursos cuidadosamente equilibradas, você pode obter potência e simplicidade.

**Poderoso:**

![captura de tela da caixa de diálogo ortografia e gramática ](images/powerful-simple-image1.png)

**Poderoso e simples:**

![captura de tela da lista de possíveis revisões ortográficas ](images/powerful-simple-image2.png)

O aplicativo Windows baseado em dados ideal é poderoso e simples. É claro que você deseja que seu aplicativo seja poderoso e, é claro, você deseja que ele seja simples, mas você pode obter ambos? Há uma tensão natural entre essas metas, mas essa tensão está longe de ser irreconcilável. Você pode obter potência e simplicidade por meio da seleção e apresentação de recursos cuidadosamente equilibradas.

## <a name="what-makes-an-application-powerful"></a>O que torna um aplicativo poderoso?

O que "energia" realmente significa em termos de software? Um aplicativo pode ser considerado poderoso se estiver cheio de recursos, tendo uma enorme amplitude de funcionalidade em uma tentativa de ser tudo para todos os usuários. Esse design provavelmente não será bem-sucedido porque é improvável que um conjunto de recursos sem-alvo atenda às necessidades de qualquer pessoa. Esse não é o tipo de energia que estamos atrás.

Um aplicativo é poderoso quando tem a combinação certa dessas características:

-   **Permitindo.** O aplicativo atende às necessidades de seus usuários de destino, permitindo que eles executem tarefas que, de outra forma, não poderiam fazer e atingir suas metas com eficiência.
-   **Eficiente.** O aplicativo permite que os usuários executem tarefas com um nível de produtividade e escala que não era possível antes.
-   **Versátil.** O aplicativo permite que os usuários executem uma ampla variedade de tarefas efetivamente em uma variedade de circunstâncias.
-   **Direto.** O aplicativo parece estar ajudando diretamente os usuários a atingir suas metas, em vez de ficar no caminho ou exigir etapas desnecessárias. Recursos como atalhos, acesso ao teclado e macros melhoram a noção de direcionamento.
-   **Flexível.** O aplicativo permite que os usuários concluam um controle fino sobre seu trabalho.
-   **Integrado.** O aplicativo é bem integrado ao Microsoft Windows, permitindo que ele compartilhe dados com outros aplicativos.
-   **Avançado.** O aplicativo tem recursos inovadores, inovadores e de última geração que não são encontrados em soluções concorrentes.

Algumas dessas características dependem da percepção do usuário e são relativas aos recursos atuais dos usuários. O que é considerado poderoso pode mudar ao longo do tempo, portanto, o recurso de pesquisa avançada de hoje pode ser comum amanhã.

Todas essas características podem ser combinadas em nossa definição de poder:

**Um aplicativo é poderoso quando permite que seus usuários de destino realizem todo o potencial com eficiência.**

Portanto, a medida final de poder é a produtividade, não o número de recursos.

Usuários diferentes precisam de ajuda para alcançar todo o potencial de maneiras diferentes. O que está habilitando para alguns usuários pode prejudicar a versatilidade, a direcionamento e o controle para outros. O software bem projetado deve equilibrar essas características adequadamente. Por exemplo, um sistema de publicação de área de trabalho projetado para não profissionales pode usar assistentes para ajudar os usuários a realizar tarefas complexas. Esses assistentes permitem que os usuários de destino executem tarefas que, de outra forma, não seriam capazes de executar. Por outro lado, um sistema de publicação de área de trabalho para profissionais pode se concentrar na direcionamento, na eficiência e no controle completo. Para usuários desse aplicativo, os assistentes podem ser limitados e frustrantes.

**Se você fizer apenas uma coisa...**

Entenda as metas dos usuários de destino e crie um conjunto de recursos que permite que eles alcancem essas metas de maneira produtiva.

## <a name="what-makes-a-user-experience-simple"></a>O que torna a experiência do usuário simples?

Definimos a simplicidade da seguinte forma:

**Simplicidade é a redução ou eliminação de um atributo de um design que os usuários de destino estão cientes e consideram unessential.**

Na prática, a simplicidade é alcançada selecionando o conjunto de recursos correto e apresentando os recursos da maneira correta. Isso reduz o unessential, real e percebido.

A simplicidade depende da percepção dos usuários. Considere como o efeito de uma transmissão automática depende da perspectiva de um usuário:

-   Para o driver típico (o usuário de destino), uma transmissão automática elimina a necessidade de uma mudança de engrenagem manual e de um motor, facilitando muito a direção de um carro. Um deslocamento de engrenagem manual e uma engrenagem não são essenciais para a tarefa de condução, portanto, eles são removidos para obter simplicidade.
-   Para um piloto de carro de corrida profissional, ter controle direto sobre a transmissão é essencial para ser competitivo. Uma transmissão automática afeta negativamente o desempenho do carro, portanto, ela não é considerada como resultado de simplicidade.
-   Para um aprendiz, uma transmissão automática é um mecanismo mais complexo e, portanto, não é mais fácil de reparar ou manter do que uma transmissão manual. Ao contrário do público-alvo, o usuário de destino não está ciente dessa complexidade interna.

Embora usuários diferentes consideram a transmissão automática de forma diferente, ela é bem-sucedida porque elimina a necessidade de conhecimento, habilidade e esforço unessential de seus usuários de destino. Para o driver típico, a transmissão automática é um ótimo recurso porque funciona.

### <a name="simplicity-vs-ease-of-use"></a>Simplicidade versus facilidade de uso

A simplicidade, quando aplicada corretamente, resulta em facilidade de uso. Mas a simplicidade e a facilidade de uso não são os mesmos conceitos. A facilidade de uso é alcançada quando os usuários podem executar uma tarefa com êxito por conta própria sem dificuldade ou confusão em um período de tempo adequado. Há muitas maneiras de obter facilidade de uso e a simplicidade, a redução do unessential, é apenas uma delas.

Todos os usuários, independentemente de quão sofisticados, querem fazer seu trabalho com uma quantidade mínima de esforço desnecessário. Todos os usuários, até mesmo usuários avançados, são principalmente incentivados a fazer seu trabalho, não para saber mais sobre computadores ou seu aplicativo.

A simplicidade é a maneira mais eficaz de obter facilidade de uso e a facilidade de uso é igual ao uso. Recursos complexos e difíceis de usar não são usados. Por outro lado, designs simples e elegantes que executam bem sua função são uma moda a ser usada. Eles invocam uma resposta positiva e emocional.

Por exemplo, considere o suporte à rede sem fio no Microsoft Windows XP. A Microsoft poderia ter adicionado um assistente para passar os usuários pelo processo de configuração. Essa abordagem teria resultado na facilidade de uso, mas não na simplicidade, porque um recurso unessential (o assistente) teria sido adicionado. Em vez disso, a Microsoft criou uma rede sem fio para se configurar automaticamente. Os usuários, em última análise, não se importam com os detalhes de configuração, desde que "funcionem apenas" de forma confiável e segura. Essa combinação de poder e simplicidade na tecnologia de rede sem fio levou à sua popularidade e à rápida adoção.

**Se você fizer apenas uma coisa...**

Inicie seu processo de design com os designs mais simples que fazem o trabalho bem.

Se você não estiver satisfeito com seu design atual, comece retirando todos os elementos unessential. Você encontrará que o que permanece geralmente é muito bom.

## <a name="obtaining-simplicity-while-maintaining-power"></a>Obtendo simplicidade ao manter a potência

### <a name="design-principles"></a>Princípios de design

Para obter simplicidade, sempre projete para o provável, não o possível.

O possível

Decisões de design baseadas no que é possível levam a interfaces de usuário complexas, como o Editor do Registro, em que o design pressuém que todas as ações são igualmente possíveis e, como resultado, exigem esforço igual. Como tudo é possível, as metas do usuário não são consideradas em decisões de design.

O provável

Decisões de design baseadas no potencial potencial para soluções simplificadas, baseadas em meta e tarefa, em que os cenários prováveis recebem foco e exigem esforço mínimo para executar.

O princípio de design de simplicidade

**Para obter simplicidade, concentre-se no que é provável; reduzir, ocultar ou remover o que é improvável; e eliminam o que é impossível.**

O que os usuários fazerão é muito mais relevante para o design do que o que eles podem fazer.

### <a name="design-techniques"></a>Técnicas de design

Para obter simplicidade enquanto mantém o poder, escolha o conjunto certo de **recursos,** localize os recursos nos locais certos e reduza o esforço **para** usá-los. Esta seção fornece algumas técnicas comuns para atingir essas metas.

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
-   **Selecione os controles certos.** Os elementos de design são incorporados pelos controles que você usa para representá-los, portanto, selecionar o controle certo é crucial para uma apresentação eficiente. por exemplo, a caixa de seleção de fonte usada pelo Microsoft Word mostra uma visualização da fonte, bem como as fontes usadas mais recentemente. Da mesma forma, a maneira como o Word mostra possíveis erros de ortografia e gramática é muito mais simples do que a alternativa da caixa de diálogo, conforme mostrado no início deste artigo.

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

O poder é para habilitar seus usuários e torná-los produtivos. A simplicidade é a remoção dos recursos não essenciais e de apresentação da maneira correta. ao compreender os usuários de destino e obter o equilíbrio certo dos recursos e da apresentação, você pode projetar aplicativos baseados em Windows que fazem ambos.

 

 