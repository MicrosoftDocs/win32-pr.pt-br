---
title: Mensagens de erro (noções básicas de design)
description: Uma mensagem de erro alerta os usuários de um problema que já ocorreu.
ms.assetid: b02110e9-985d-4448-9c95-eb958b0059b1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 0ceffd3d1fecccd8342cb1e634735653bdba9722
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469013"
---
# <a name="error-messages-design-basics"></a>Mensagens de erro (noções básicas de design)

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Uma mensagem de erro alerta os usuários de um problema que já ocorreu. Por outro lado, uma mensagem de aviso alerta os usuários de uma condição que pode causar um problema no futuro. As mensagens de erro podem ser apresentadas usando caixas de diálogo modais, mensagens in-locar, notificações ou balão.

![captura de tela da mensagem de erro: não é possível renomear](images/mess-error-image1.png)

Uma mensagem de erro modal típica.

Mensagens de erro efetivas informam aos usuários que ocorreu um problema, explicam por que ele aconteceu e fornecem uma solução para que os usuários possam corrigir o problema. Os usuários devem executar uma ação ou alterar seu comportamento como resultado de uma mensagem de erro.

Mensagens de erro úteis e bem escritas são cruciais para uma experiência de usuário de qualidade. Mensagens de erro mal escritas resultam em baixa satisfação do produto e são uma causa principal de custos de suporte técnico que podem ser evitados. Mensagens de erro desnecessárias quebram o fluxo dos usuários.

**Observação:** Diretrizes relacionadas a [caixas de](win-dialog-box.md)diálogo [,](mess-warn.md)mensagens de aviso [,](mess-confirm.md)confirmações , [ícones](vis-std-icons.md)padrão, notificações e [layout](vis-layout.md) são [apresentadas](mess-notif.md)em artigos separados.

## <a name="is-this-the-right-user-interface"></a>Essa é a interface do usuário certa?

Para decidir, considere estas perguntas:

- **A interface do usuário está apresentando um problema que já ocorreu?** Caso não seja, a mensagem não será um erro. Se o usuário que está sendo alertado de uma condição que pode causar um problema no futuro, use uma mensagem de aviso.
- **O problema pode ser evitado sem causar confusão?** Em caso afirmado, evite o problema. Por exemplo, use controles restritos a valores válidos em vez de usar controles irr pouco restritos que podem exigir mensagens de erro. Além disso, desabilitar controles ao clicar resultaria em erro, desde que seja óbvio por que o controle está desabilitado.
- **O problema pode ser corrigido automaticamente?** Se sim, tratar o problema e suprimir a mensagem de erro.
- **É provável que os usuários executem uma ação ou alterem seu comportamento como resultado da mensagem?** Caso não seja, a condição não justifica a interrupção do usuário, portanto, é melhor suprimir o erro.
- **O problema é relevante quando os usuários estão usando ativamente outros programas?** Se sim, considere mostrar o problema usando um ícone de área [de notificação](winenv-notification.md).
- **O problema não está relacionado à atividade do usuário atual, não requer ação imediata do usuário e os usuários podem ignorá-lo livremente?** Em caso afirmativa, use uma [notificação de falha de ação.](mess-notif.md)
- **O problema está relacionado ao status de uma tarefa em segundo plano dentro de uma janela primária?** Em caso afirmado, considere mostrar o problema usando barras [de status](ctrl-status-bars.md).
- **Os principais usuários de TI são profissionais de TI?** Nesse caso, considere usar um mecanismo de comentários alternativo, como entradas de arquivo de [log](glossary.md) ou alertas de email. Os profissionais de TI preferem fortemente arquivos de log para informações não críticas.

## <a name="design-concepts"></a>Conceitos de design

**As características de mensagens de erro ruim**

Não deve ser surpresa que haja muitas mensagens de erro entediantes, insacitivas e mal escritas. E como as mensagens de erro geralmente são apresentadas usando diálogos modais, elas interrompem a atividade e a demanda atuais do usuário a serem confirmadas antes de permitir que o usuário continue.

Parte do problema é que há muitas maneiras de fazer isso errado. Considere estes exemplos do Hall de Mensagens de Erro de São Paulo:

**Mensagens de erro desnecessárias**

**Incorreto:**

![captura de tela da mensagem de erro: falha no aplicativo ](images/mess-error-image2.png)

Este exemplo de Windows XP pode ser a pior mensagem de erro de sempre. Indica que um programa não pôde ser lançado porque Windows em si está em processo de desligamento. Não há nada que o usuário possa fazer sobre isso ou até mesmo deseja fazer isso (o usuário optou por desligar Windows, depois de tudo). E ao exibir essa mensagem de erro, Windows se impede de desligar!

**O problema:** A mensagem de erro em si é o problema. Além de descartar a mensagem de erro, não há nada para os usuários fazer.

**Causa principal:** Relatar todos os casos de erro, independentemente das metas ou do ponto de vista dos usuários.

**Alternativa recomendada:** Não reporte erros que os usuários não se importam.

**Mensagens de erro "Êxito"**

**Incorreto:**

![captura de tela da mensagem de erro: falha na remoção ](images/mess-error-image3.png)

Essa mensagem de erro resultou da escolha do usuário de não reiniciar Windows imediatamente após a remoção do programa. A remoção do programa foi bem-sucedida do ponto de vista do usuário.

**O problema:** Não há nenhum erro do ponto de vista do usuário. Além de descartar a mensagem de erro, não há nada para os usuários fazer.

**Causa principal:** A tarefa foi concluída com êxito do ponto de vista do usuário, mas falhou do ponto de vista do programa de desinstalação.

**Alternativa recomendada:** Não reporte erros para condições que os usuários consideram aceitáveis.

**Mensagens de erro completamente inúteis**

**Incorreto:**

![captura de tela da mensagem de erro: erro desconhecido ](images/mess-error-image4.png)

Os usuários aprendem que houve um erro, mas não têm ideia do que foi o erro ou o que fazer sobre ele. E não, não está ok!

**O problema:** A mensagem de erro não dá um problema específico e não há nada que os usuários possam fazer sobre isso.

**Causa principal:** Provavelmente, o programa tem um tratamento de erro ruim.

**Alternativa recomendada:** Projete um bom tratamento de erro no programa.

**Mensagens de erro incomputíveis**

**Incorreto:**

![captura de tela da mensagem de erro: backup não concluído ](images/mess-error-image5.png)

Neste exemplo, a instrução do problema é clara, mas a explicação suplementar é uma grande surpresa.

**O problema:** A instrução ou solução do problema é incomphensível.

**Causa principal:** Explicando o problema do ponto de vista do código em vez do do usuário.

**Alternativa recomendada:** Escreva um texto de mensagem de erro que os usuários de destino possam entender facilmente. Forneça soluções que os usuários podem realmente executar. Projetar a experiência de mensagem de erro do programa não faz com que os programadores componham mensagens de erro no local.

**Mensagens de erro que se comunicam em excesso**

**Incorreto:**

![captura de tela de mensagem extremamente detalhada ](images/mess-error-image6.png)

Neste exemplo, a mensagem de erro aparentemente tenta explicar cada etapa de solução de problemas.

**O problema:** Muitas informações.

**Causa principal:** Dando muitos detalhes ou tentando explicar um processo de solução de problemas complicado dentro de uma mensagem de erro.

**Alternativa recomendada:** Evite detalhes desnecessários. Além disso, evite solucionar problemas. Se uma solução de problemas for necessária, concentre-se nas soluções mais prováveis e explique o restante vinculando-se ao tópico apropriado na Ajuda.

**Mensagens de erro desnecessariamente desnecessariamente des**

**Incorreto:**

![captura de tela da mensagem: não é possível encontrar o objeto ](images/mess-error-image7.png)

A incapacidade do programa de encontrar um objeto parece catastrófica. E supondo que seja catastrófico, por que a resposta está ok?

**O problema:** O tom do programa é desnecessariamente agressivo ou crítico.

**Causa principal:** O problema ocorre devido a um bug que parece catastrófico do ponto de vista do programa.

**Alternativa recomendada:** Escolha o idioma cuidadosamente com base no ponto de vista do usuário.

**Mensagens de erro que responsabilizam os usuários**

**Incorreto:**

![captura de tela de mensagem: caractere inválido ](images/mess-error-image8.png)

Por que os usuários se sentem como um criminoso?

**O problema:** A mensagem de erro é desenhada de forma que accuses o usuário de fazer um erro.

**Causa principal:** Frases insensíveis que se concentram no comportamento do usuário em vez do problema.

**Alternativa recomendada:** Concentre-se no problema, não na ação do usuário que levou ao problema, usando a voz passiva, conforme necessário.

**Mensagens de erro repróprias**

**Incorreto:**

![captura de tela da mensagem: erro no relatório de erros ](images/mess-error-image9.png)

Neste exemplo, a declaração do problema é muito ferro e nenhuma solução é fornecida.

**O problema:** Instruções de mensagem de erro que são repróprias ou não sequitors.

**Causa principal:** Criar mensagens de erro sem prestar atenção ao seu contexto.

**Alternativa recomendada:** Suas mensagens de erro foram criadas e revisadas por um gravador. Considere o contexto e o estado de preocupação do usuário ao revisar os erros.

**Mensagens de erro do programador**

**Incorreto:**

![captura de tela da mensagem: endereço de violação de acesso ](images/mess-error-image10.png)

Neste exemplo, a mensagem de erro indica que há um bug no programa. Essa mensagem de erro tem significado apenas para o programador.

**O problema:** As mensagens destinadas a ajudar os desenvolvedores do programa a encontrar bugs são deixadas na versão de lançamento do programa. Essas mensagens de erro não têm significado ou valor para os usuários.

**Causa principal:** Programadores usando a interface do usuário normal para fazer mensagens.

**Alternativa recomendada:** Os desenvolvedores devem compilar condicionalmente todas essas mensagens para que elas sejam automaticamente removidas da versão de lançamento de um produto. Não gaste tempo tentando fazer erros como esse abrangente para os usuários porque seu único público-alvo são os programadores.

**Mensagens de erro inadequadamente apresentadas**

**Incorreto:**

![captura de tela da mensagem: falha inesperada ](images/mess-error-image11.png)

Este exemplo tem muitos erros de apresentação comuns.

**O problema:** Obtendo todos os detalhes incorretos na apresentação da mensagem de erro.

**Causa principal:** Não conhece e aplicando as diretrizes de mensagem de erro. Não usar gravadores e editores para criar e revisar as mensagens de erro.

A natureza da manipulação de erros é que muitos desses erros são muito fáceis de fazer. É perturbador perceber que a maioria das mensagens de erro pode ser nominal para o Hall da pena.

**As características de boas mensagens de erro**

Em contraste com os exemplos incorretos anteriores, boas mensagens de erro têm:

- **Um problema.** Declara que ocorreu um problema.
- **Uma causa.** Explica por que o problema ocorreu.
- **Uma solução.** Fornece uma solução para que os usuários possam corrigir o problema.

Além disso, boas mensagens de erro são apresentadas de uma maneira que:

- **Relativas.** A mensagem apresenta um problema com o qual os usuários se preocupam.
- **Acionáveis.** Os usuários devem executar uma ação ou alterar seu comportamento como resultado da mensagem.
- **Centralizado pelo usuário.** A mensagem descreve o problema em termos de ações ou metas do usuário de destino, não em termos de como o código é insatisfeito.
- **Visão.** A mensagem é tão curta quanto possível, mas não é mais curta.
- **Formatação.** A mensagem usa linguagem simples para que os usuários de destino possam entender facilmente o problema e a solução.
- **Determinados.** A mensagem descreve o problema usando um idioma específico, fornecendo nomes, locais e valores específicos dos objetos envolvidos.
- **Educado.** Os usuários não devem ser culpados nem se sentir estúpidos.
- **Encontrar.** Exibido com pouca frequência. Mensagens de erro exibidas com frequência são um sinal de design inadequado.

Ao projetar sua experiência de tratamento de erros para ter essas características, você pode manter as mensagens de erro do programa fora da sala de mensagens de erro do pena.

**Evitando mensagens de erro desnecessárias**

Geralmente, a melhor mensagem de erro não é uma mensagem de erro. Muitos erros podem ser evitados por meio de um design melhor, e geralmente há alternativas melhores para mensagens de erro. Geralmente é melhor evitar um erro do que relatar um.

As mensagens de erro mais óbvias a serem evitadas são aquelas que não são acionáveis. Se for provável que os usuários ignorem a mensagem sem fazer ou alterar nada, omita a mensagem de erro.

Algumas mensagens de erro podem ser eliminadas porque não são problemas do ponto de vista do usuário. Por exemplo, suponha que o usuário tentou excluir um arquivo que já está no processo de ser excluído. Embora isso possa ser um caso inesperado do ponto de vista do código, os usuários não consideram esse erro porque o resultado desejado é atingido.

**Incorreto:**

![captura de tela da mensagem: não é possível excluir o arquivo ](images/mess-error-image12.png)

Esta mensagem de erro deve ser eliminada porque a ação foi bem-sucedida do ponto de vista do usuário.

Para outro exemplo, suponha que o usuário cancele explicitamente uma tarefa. Para o ponto de vista do usuário, a condição a seguir não é um erro.

**Incorreto:**

![captura de tela da mensagem: não é possível concluir o backup ](images/mess-error-image13.png)

Essa mensagem de erro também deve ser eliminada porque a ação foi bem-sucedida do ponto de vista do usuário.

Às vezes, as mensagens de erro podem ser eliminadas concentrando-se nas metas dos usuários em vez da tecnologia. Ao fazer isso, reconsidere o que é um erro realmente. O problema é com as metas do usuário ou com a capacidade do seu programa de atender a elas? Se a ação do usuário fizer sentido no mundo real, ela também deverá fazer sentido em software.

Por exemplo, suponha que em um programa de comércio eletrônico um usuário tenta localizar um produto usando a pesquisa, mas a consulta de pesquisa literal não tem correspondência e o produto desejado está fora de estoque. Tecnicamente, esse é um erro, mas em vez de fornecer uma mensagem de erro, o programa poderia:

- Continue a procurar produtos que mais se correspondam à consulta.
- Se a pesquisa tiver erros óbvios, recomende automaticamente uma consulta corrigida.
- Trate automaticamente problemas comuns, como grafias incorretas, grafias alternativas e casos de pluralização e verbos incompatíveis.
- Indique quando o produto estará em estoque.

Desde que a solicitação do usuário seja razoável, um programa de comércio eletrônico bem projetado deve retornar resultados razoáveis, não erros.

Outra excelente maneira de evitar mensagens de erro é evitar problemas em primeiro lugar. Você pode evitar erros de:

- **Usando controles restritos.** Use controles que são restritos a valores válidos. Controles como listas, controles deslizantes, caixas de seleção, botões de opção e seletores de data e hora são restritos a valores válidos, enquanto as caixas de texto geralmente não são e podem exigir mensagens de erro. No entanto, você pode restringir as caixas de texto para aceitar apenas determinados caracteres e aceitar um número máximo de caracteres.
- **Usando interações restritas.** Para operações de arrastar, permita que os usuários sejam descartados somente em destinos válidos.
- **Usando controles desabilitados e itens de menu.** Desabilite controles e itens de menu quando os usuários puderem deduzir facilmente por que o item de controle ou de menu está desabilitado.
- **Fornecendo bons valores padrão.** Os usuários têm menos probabilidade de fazer erros de entrada se puderem aceitar os valores padrão. Mesmo que os usuários decidam alterar o valor, o valor padrão permite que os usuários saibam o formato de entrada esperado.
- **Fazer as coisas simplesmente funcionam.** Os usuários têm menos probabilidade de cometer erros se as tarefas forem desnecessárias ou executadas automaticamente para eles. Ou se os usuários fizerem pequenos erros, mas sua intenção for clara, o problema será corrigido automaticamente. Por exemplo, você pode corrigir automaticamente os problemas de formatação secundária.

**Fornecendo mensagens de erro necessárias**

Às vezes, você realmente precisa fornecer uma mensagem de erro. Os usuários cometem erros, redes e dispositivos param de funcionar, os objetos não podem ser localizados ou modificados, as tarefas não podem ser concluídas e os programas têm bugs. O ideal é que esses problemas ocorram com menos frequência, por exemplo, podemos projetar nosso software para evitar muitos tipos de erros do usuário, mas não é realista evitar todos esses problemas. E quando um desses problemas ocorre, uma mensagem de erro útil leva os usuários de volta aos seus pés rapidamente.

Uma crença comum é que as mensagens de erro são a pior experiência do usuário e devem ser evitadas a todos os custos, mas é mais preciso dizer que a confusão do usuário é a pior experiência e deve ser evitada a todos os custos. Às vezes, esse custo é uma mensagem de erro útil.

Considere os controles desabilitados. Na maioria das vezes, é óbvio por que um controle está desabilitado, portanto, desabilitar o controle é uma ótima maneira de evitar uma mensagem de erro. No entanto, e se o motivo pelo qual um controle está desabilitado não for óbvio? O usuário não pode continuar e não há nenhum comentário para determinar o problema. Agora o usuário está preso e precisa deduzir o problema ou obter suporte técnico. Nesses casos, é muito melhor deixar o controle habilitado e fornecer uma mensagem de erro útil em vez disso.

**Incorreto:**

![captura de tela da mensagem: onde salvar backup? ](images/mess-error-image14.png)

Por que o botão Avançar está desabilitado aqui? É melhor deixá-lo habilitado e evitar confusão do usuário, fornecendo uma mensagem de erro útil.

Se você não tiver certeza se deve dar uma mensagem de erro, comece compondo a mensagem de erro que você pode dar. Se for provável que os usuários executem uma ação ou alterem seu comportamento como resultado, forneça a mensagem de erro. Por outro lado, se for provável que os usuários ignorem a mensagem sem fazer ou alterar nada, omita a mensagem de erro.

**Criando um bom tratamento de erros**

Embora criar um bom texto de mensagem de erro possa ser desafiador, às vezes é impossível sem um bom suporte ao tratamento de erros do programa. Considere esta mensagem de erro:

**Incorreto:**

![captura de tela da mensagem: erro desconhecido ](images/mess-error-image15.png)

É provável que o problema seja desconhecido porque o suporte ao tratamento de erros do programa está faltando.

Embora seja possível que essa seja uma mensagem de erro muito mal escrita, é mais provável que ela reflita a falta de um bom tratamento de erro pelo código subjacente não há informações específicas conhecidas sobre o problema.

Para criar mensagens de erro específicas, acionáveis e centralizadas pelo usuário, o código de tratamento de erros do seu programa deve fornecer informações de erro específicas de alto nível:

- Cada problema deve ter um código de erro exclusivo atribuído.
- Se um problema tiver várias causas, o programa deverá determinar a causa específica sempre que possível.
- Se o problema tiver parâmetros, os parâmetros deverão ser mantidos.
- Problemas de nível baixo devem ser tratados em um nível suficientemente alto para que a mensagem de erro possa ser apresentada do ponto de vista do usuário.

Boas mensagens de erro não são apenas um problema de interface do usuário, são um problema de design de software. Uma boa experiência de mensagem de erro não é algo que possa ser retratado posteriormente.

**Solução de problemas (e como evitá-lo)**

Solução de problemas de resultados quando um problema com várias causas diferentes é relatado com uma única mensagem de erro.

**Incorreto:**

![diagrama de uma mensagem declarando três causas ](images/mess-error-image16.png)

**Correto:**

![diagrama de três mensagens indicando uma causa](images/mess-error-image17.png)

Solução de problemas de resultados quando vários problemas são relatados com uma única mensagem de erro.

No exemplo a seguir, não foi possível mover um item porque ele já foi movido ou excluído ou o acesso foi negado. Se o programa puder determinar facilmente a causa, por que a carga do usuário deve determinar a causa específica?

**Incorreto:**

![captura de tela da mensagem declarando duas causas ](images/mess-error-image18.png)

Bem, o que é? Agora o usuário precisa solucionar problemas.

O programa pode determinar se o acesso foi negado, portanto, esse problema deve ser relatado com uma mensagem de erro específica.

**Correto:**

![captura de tela de mensagem dizendo uma causa ](images/mess-error-image19.png)

Com uma causa específica, nenhuma solução de problemas é necessária.

Use mensagens com várias causas somente quando a causa específica não puder ser determinada. Neste exemplo, seria difícil para o programa determinar se o item foi movido ou excluído, portanto, uma única mensagem de erro com várias causas pode ser usada aqui. No entanto, é improvável que os usuários irão se preocupar se, por exemplo, não podiam mover um arquivo excluído. Para essas causas, a mensagem de erro não é nem necessária.

**Manipulando erros desconhecidos**

Em alguns casos, você não saberá, de forma genuína, o problema, a causa ou a solução. Se não for recomendável suprimir o erro, é melhor ter a falta de informações do que apresentar problemas, causas ou soluções que podem não estar corretas.

Por exemplo, se o programa tiver uma exceção sem tratamento, a seguinte mensagem de erro será adequada:

![captura de tela da mensagem: ocorreu um erro desconhecido ](images/mess-error-image20.png)

Se não for possível suprimir um erro desconhecido, é melhor estar na frente da falta de informações.

Por outro lado, forneça informações específicas e acionáveis se for provável que seja útil na maioria das vezes.

![captura de tela que mostra um Office mensagem de Communicator ' servidor indisponível '. ](images/mess-error-image21.png)

Essa mensagem de erro é adequada para um erro desconhecido se a conectividade de rede costuma ser o problema.

**Determinar o tipo de mensagem apropriado**

Alguns problemas podem ser apresentados como erro, aviso ou informações, dependendo da ênfase e da formulação. por exemplo, suponha que uma página da Web não possa carregar um controle de ActiveX não assinado com base na configuração atual do Windows Internet Explorer:

- **Ao.** "esta página não pode carregar um controle de ActiveX não assinado". (Fraseada como um problema existente.)
- **Alerta.** "esta página pode não se comportar conforme o esperado porque Windows o Internet Explorer não está configurado para carregar controles de ActiveX não assinados". ou "permitir que esta página instale um controle de ActiveX não assinado? Fazer isso de fontes não confiáveis pode prejudicar seu computador. " (Fraseada como condições que podem causar problemas futuros.)
- **Divulgação.** "você configurou o Windows Internet Explorer para bloquear controles de ActiveX não assinados". (Fraseada como uma declaração de fato).

**Para determinar o tipo de mensagem apropriado, concentre-se no aspecto mais importante do problema que os usuários precisam conhecer ou agir.** Normalmente, se um problema impedir que o usuário Continue, você deverá apresentá-lo como um erro; Se o usuário puder continuar, apresente-o como um aviso. Crie a [instrução principal](text-ui.md) ou outro texto correspondente com base nesse foco e, em seguida, escolha um ícone ([padrão](vis-std-icons.md) ou de outra forma) que corresponda ao texto. O texto da instrução principal e os ícones sempre devem corresponder.

**Apresentação da mensagem de erro**

a maioria das mensagens de erro em Windows programas é apresentada usando caixas de diálogo modais (como mostra a maioria dos exemplos neste artigo), mas há outras opções:

- No local
- Balões
- Notificações
- Ícones da área de notificação
- Barras de status
- Arquivos de log (para erros direcionados a profissionais de ti)

A colocação de mensagens de erro em caixas de diálogo modais tem o benefício de exigir a atenção e a confirmação imediatas do usuário. No entanto, essa também é sua desvantagem principal se essa atenção não for necessária.

![captura de tela da mensagem: Pare o que você está fazendo ](images/mess-error-image22.png)

Você realmente precisa interromper os usuários para que eles possam clicar no botão fechar? Caso contrário, considere alternativas ao uso de uma caixa de diálogo modal.

Caixas de diálogo modais são uma ótima opção quando o usuário deve confirmar o problema imediatamente antes de continuar, mas geralmente uma escolha ruim de outra forma. Em geral, você deve preferir usar a apresentação de peso mais leve que faz o trabalho bem.

**Evitar o excesso de comentários**

Em geral, [os usuários não leem, eles digitalizarão](vis-layout.md). Quanto mais texto houver, mais difícil será a verificação do texto e mais provavelmente os usuários não lerão o texto. Como resultado, é importante reduzir o texto até seus fundamentos e usar a divulgação progressiva e os links de Ajuda quando necessário para fornecer informações adicionais.

Há muitos exemplos extremos, mas vamos ver mais um típico. O exemplo a seguir tem a maioria dos atributos de uma boa mensagem de erro, mas seu texto não é conciso e requer motivação para ler.

**Incorreto:**

![captura de tela da mensagem detalhada ](images/mess-error-image23.png)

Este exemplo é uma boa mensagem de erro, mas sobrecomunidades.

O que todo esse texto está realmente dizendo? Algo assim:

**Correto:**

![captura de tela da mensagem: cd recorder não detectado ](images/mess-error-image24.png)

Essa mensagem de erro tem essencialmente as mesmas informações, mas é muito mais concisa.

Usando a Ajuda para fornecer os detalhes, essa mensagem de erro tem [um estilo invertido de pirâmide](text-ui.md) de apresentação.

Para obter mais diretrizes e exemplos sobre a supercomunidade, consulte [Interface do Usuário Texto.](text-ui.md)

**Se você fizer apenas oito coisas**

1. Projete seu programa para tratamento de erros.
2. Não dê mensagens de erro desnecessárias.
3. Evite confusão do usuário, dando as mensagens de erro necessárias.
4. Certifique-se de que a mensagem de erro dê um problema, uma causa e uma solução.
5. Certifique-se de que a mensagem de erro seja relevante, a ação, breve, clara, específica, cortejosa e rara.
6. Criar mensagens de erro do ponto de vista do usuário, não do ponto de vista do programa.
7. Evite envolver o usuário na solução de problemas, use uma mensagem de erro diferente para cada causa detectável.
8. Use o método de apresentação de peso mais leve que faz o trabalho bem.

**Padrões de uso**

As mensagens de erro têm vários padrões de uso:


| | | <strong>Problemas do sistema</strong><br /> O sistema operacional, o dispositivo de hardware, a rede ou o programa falhou ou não está no estado necessário para executar uma tarefa. <br /> | Muitos problemas do sistema podem ser resolvidos pelo usuário: <br /><ul><li>Os problemas do dispositivo podem ser resolvidos ao ligar o dispositivo, reconectar o dispositivo e inserir a mídia.</li><li>Os problemas de rede podem ser resolvidos verificando a conexão de rede física e <strong>executando o diagnóstico e o reparo de rede.</strong></li><li>Os problemas do programa podem ser resolvidos alterando as opções do programa ou reiniciando o programa.</li></ul><img src="images/mess-error-image25.png" alt="Screen shot of message: Can't find a camera " /><br /> Neste exemplo, o programa não pode encontrar uma câmera para executar uma tarefa de usuário.<br /><img src="images/mess-error-image26.png" alt="Screen shot of message Network discovery off " /><br /> Neste exemplo, um recurso necessário para executar uma tarefa precisa ser ligado.<br /> | | <strong>Problemas de arquivo</strong><br /> Um arquivo ou pasta necessário para uma tarefa iniciada pelo usuário não foi encontrado, já está em uso ou não tem o formato esperado. <br /> | <img src="images/mess-error-image27.png" alt="Screen shot of message: Can't delete file " /><br /> Neste exemplo, o arquivo ou a pasta não pode ser excluído porque não foi encontrado.<br /><img src="images/mess-error-image28.png" alt="Screen shot of message: Can't play this file " /><br /> Neste exemplo, o programa não dá suporte ao formato de arquivo determinado.<br /> | | <strong>Problemas de segurança</strong><br /> O usuário não tem permissão para acessar um recurso ou privilégio suficiente para executar uma tarefa iniciada pelo usuário. <br /> | <img src="images/mess-error-image29.png" alt="Screen shot of message: You don't have permission " /><br /> Neste exemplo, o usuário não tem permissão para acessar um recurso.<br /><img src="images/mess-error-image30.png" alt="Screen shot of message: You don't have privilege " /><br /> Neste exemplo, o usuário não tem o privilégio de executar uma tarefa.<br /> | | <strong>Problemas de tarefa</strong><br /> Há um problema específico ao executar uma tarefa iniciada pelo usuário (que não seja um sistema, arquivo não encontrado, formato de arquivo ou problema de segurança). <br /> | <img src="images/mess-error-image31.png" alt="Screen shot of message: Data can't be pasted " /><br /> Neste exemplo, os dados da Área de Transferência não podem ser Paint.<br /><img src="images/mess-error-image32.png" alt="Screen shot of message: Upgrade can't be installed " /><br /> Neste exemplo, o usuário não pode instalar uma atualização de software.<br /> | | <strong>Problemas de entrada do usuário</strong><br /> O usuário entrou em um valor incorreto ou inconsistente com outra entrada do usuário. <br /> | <img src="images/mess-error-image33.png" alt="Screen shot of message: Incorrect time value " /><br /> Neste exemplo, o usuário entrou em um valor de hora incorreto.<br /><img src="images/mess-error-image34.png" alt="Screen shot of message: Incorrect input format " /><br /> Neste exemplo, a entrada do usuário não está no formato correto.<br /> | 


## <a name="guidelines"></a>Diretrizes

### <a name="presentation"></a>Apresentação

- **Use caixas de diálogo de tarefa sempre que apropriado** para obter uma aparência e layout consistentes. As caixas de diálogo de Windows o Vista ou posterior, portanto, não são adequadas para versões anteriores do Windows. Se você precisa usar uma caixa de mensagem, separe a instrução principal da instrução complementar com duas quebras de linha.

### <a name="user-input-errors"></a>Erros de entrada do usuário

- **Sempre que possível, evite ou reduza erros de entrada do usuário:**
  - Usando controles restritos a valores válidos.
  - Desabilitar controles e itens de menu ao clicar resultaria em erro, desde que seja óbvio por que o controle ou item de menu está desabilitado.
  - Fornecendo bons valores padrão.

**Incorreto:**

![captura de tela da caixa de texto com o rótulo do volume do locutor ](images/mess-error-image35.png)

Neste exemplo, uma caixa de texto não restrita é usada para entrada restrita. Em vez disso, use um controle deslizante.

- **Use o tratamento de erro sem modo (erros ou balão in-locar) para problemas de entrada do usuário contextual.**
- **Use balão para problemas de** entrada de usuário de ponto único não crítico detectados em uma caixa de texto ou imediatamente após uma caixa de texto perder o foco. [Os balão](https://msdn.microsoft.com/library/windows/desktop/aa511451.aspx) não exigem espaço na tela disponível ou o layout dinâmico necessário para exibir mensagens in-locar. Exibir apenas um balão por vez. Como o problema não é crítico, nenhum ícone de erro é necessário. Os balão vão embora quando clicados, quando o problema é resolvido ou após um tempo-final.

![captura de tela da mensagem: caractere incorreto ](images/mess-error-image36.png)

Neste exemplo, um balão indica um problema de entrada enquanto ainda está no controle .

- **Use erros in-locar para detecção de erros atrasadas, geralmente** erros encontrados clicando em um botão de confirmação. (Não use erros [in-locar](glossary.md) para configurações que são imediatamente confirmados.) Pode haver vários erros in-in-place por vez. Use texto normal e um ícone de erro de 16 x 16 pixels, colocando-os diretamente ao lado do problema sempre que possível. Os erros in-locar não desaparecerão, a menos que o usuário faça commits e nenhum outro erro seja encontrado.

![captura de tela da mensagem: endereço de email incorreto ](images/mess-error-image37.png)

Neste exemplo, um erro in-place é usado para um erro encontrado clicando no botão de confirmação.

- Use o tratamento de erro **modal (caixas** de diálogo de tarefa ou de mensagem) para todos os outros problemas, incluindo erros que envolvem vários controles ou são erros não contextuais ou não de entrada encontrados clicando em um botão de confirmação.
- **Quando um problema de entrada do usuário é relatado, de definir o foco de entrada para o primeiro controle com os dados incorretos.** Role o controle para a exibição, se necessário. Se o controle for uma caixa de texto, selecione todo o conteúdo. Sempre deve ser óbvio ao que a mensagem de erro está se referindo.
- **Não limpe a entrada incorreta.** Em vez disso, deixe-o para que o usuário possa ver e corrigir o problema sem começar de novo.
  - **Exceção:** Limpe a senha incorreta e as caixas de texto PIN porque os usuários não podem corrigir a entrada mascarada com eficiência.

### <a name="troubleshooting"></a>Solução de problemas

- **Evite criar problemas de solução de problemas.** Não confie em uma única mensagem de erro para relatar um problema com várias causas detectáveis diferentes.
- **Use uma mensagem de erro diferente (normalmente uma instrução complementar diferente) para cada causa detectável.** Por exemplo, se um arquivo não puder ser aberto por vários motivos, forneça uma instrução complementar separada para cada motivo.
- **Use uma mensagem com várias causas somente quando a causa específica não puder ser determinada.** Nesse caso, apresente as soluções em ordem de probabilidade de corrigir o problema. Isso ajuda os usuários a resolver o problema com mais eficiência.

### <a name="icons"></a>Ícones

- **As caixas de diálogo de mensagem de erro modal não têm ícones de barra de título.** Os ícones da barra de título são usados como uma distinção visual entre janelas primárias e secundárias.
- **Use um ícone de erro.** Exceções:
  - Se o erro for um problema de entrada do usuário exibido usando uma caixa de diálogo modal ou balão, não use um ícone. Isso é um contador para o tom incentivador de Windows. No entanto, as mensagens de erro in-locar devem usar um pequeno ícone de erro (16 x 16 pixels) para identificá-las claramente como mensagens de erro.

     ![captura de tela do formato postal incorreto da mensagem](images/mess-error-image38.png)

     ![captura de tela do nome do computador de mensagem muito longo](images/mess-error-image39.png)

     Nesses exemplos, os problemas de entrada do usuário não precisam de ícones de erro.

     ![captura de tela do formato errado do número de telefone da mensagem](images/mess-error-image40.png)

     Neste exemplo, uma mensagem de erro in-loque precisa de um pequeno ícone de erro para identificá-la claramente como uma mensagem de erro.

- Se o problema for para um recurso que tenha um ícone (e não um problema de entrada do usuário), você poderá usar o ícone de recurso com uma sobreposição de erro. Se você fizer isso, use também o nome do recurso como assunto do erro.

    ![o player de mídia de mensagem de captura de tela não pode reproduzir o arquivo ](images/mess-error-image41.png)

    Neste exemplo, o ícone de recurso tem uma sobreposição de erro e o recurso é o assunto do erro.

- **Não use ícones de aviso para erros.** Isso geralmente é feito para fazer com que a apresentação se sinta menos grave. Erros não são avisos.

    **Incorreto:**

    ![captura de tela da troca rápida de mensagens não habilitada ](images/mess-error-image42.png)

    Neste exemplo, um ícone de aviso é usado incorretamente para fazer com que o erro se sinta menos grave.

Para obter mais diretrizes e exemplos, consulte [Ícones Padrão.](vis-std-icons.md)

### <a name="progressive-disclosure"></a>Divulgação progressiva

- **Use um botão Mostrar/Ocultar detalhes de divulgação progressiva para ocultar informações avançadas ou detalhadas em uma mensagem de erro.** Isso simplifica a mensagem de erro para uso típico. Não o oculta as informações necessárias, pois os usuários podem não encontrá-los.

![captura de tela da mensagem: o activesync não pode fazer logon ](images/mess-error-image43.png)

Neste exemplo, o botão de divulgação progressiva ajuda os usuários a fazer drill down para obter mais detalhes se quiserem ou simplificar a interface do usuário, caso não o queira.

- **Não use Mostrar/Ocultar detalhes, a menos que realmente haja mais detalhes.** Não apenas restate as informações existentes em um formato mais detalhado.
- **Não use Mostrar/Ocultar detalhes para mostrar informações da Ajuda.** Em vez disso, use links de Ajuda.

Para diretrizes de rotulagem, consulte [Controles de divulgação progressiva.](ctrl-progressive-disclosure-controls.md)

**Não mostre essa mensagem novamente**

- **Se uma mensagem de erro precisar dessa opção, refrescar o erro e sua frequência.** Se ele tiver todas as características de um bom erro (relevante, a ação e pouco frequente), não deverá fazer sentido para os usuários suprimi-lo.

Para obter mais diretrizes, consulte Caixas [de diálogo](win-dialog-box.md).

### <a name="default-values"></a>Valores padrão

- **Selecione a resposta mais segura, menos destrutiva ou mais segura para ser o padrão.** Se a segurança não for um fator, selecione o comando mais provável ou conveniente.

### <a name="help"></a>Ajuda

- **Criar mensagens de erro para evitar a necessidade de Ajuda.** Normalmente, os usuários não devem ter que ler texto externo para entender e resolver o problema, a menos que a solução exija várias etapas.
- **Certifique-se de que o conteúdo da Ajuda seja relevante e útil.** Ele não deve ser uma reformulação detalhada da mensagem de erro, deve conter informações úteis que estão além do escopo da mensagem de erro, como maneiras de evitar o problema no futuro. Não forneça um link de Ajuda apenas porque você pode.
- **Use links de Ajuda específicos, concisos e relevantes para acessar o conteúdo da Ajuda.** Não use botões de comando ou divulgação progressiva para essa finalidade.
- **Para mensagens de erro que você não pode tornar específicas e ativas, considere fornecer links para o conteúdo da Ajuda online.** Ao fazer isso, você pode fornecer aos usuários informações adicionais que podem ser atualizadas após o lançamento do programa.

Para obter mais diretrizes, consulte [Ajuda](winenv-help.md).

### <a name="error-codes"></a>Códigos do Erro

- **Para mensagens de erro que você não pode tornar específicas e ativas ou elas se beneficiam da Ajuda, considere também fornecer códigos de erro.** Os usuários geralmente usam esses códigos de erro para pesquisar informações adicionais na Internet.
- **Sempre forneça uma descrição de texto do problema e da solução.** Não dependa apenas do código de erro para essa finalidade.

**Incorreto:**

![captura de tela da mensagem: não é possível abrir o arquivo ](images/mess-error-image44.png)

Neste exemplo, um código de erro é usado como um substituto para um texto de solução.

- **Atribua um código de erro exclusivo para cada causa diferente.** Isso evita a solução de problemas.
- **Escolha códigos de erro que podem ser pesquisados facilmente na Internet.** Se você usar códigos de 32 bits, use uma representação hexadecimal com caracteres "0x" e maiúsculas à frente.

**Correto:**

1234

0xC0001234

**Incorreto:**

-1

-67113524

- **Use Mostrar/Ocultar detalhes para exibir códigos de erro.** Frase como Código de erro: <error code> .

![captura de tela da mensagem: o programa não foi inicializado ](images/mess-error-image45.png)

Neste exemplo, um código de erro é usado para complementar uma mensagem de erro que pode se beneficiar de mais informações.

### <a name="sound"></a>Som

- **Não acompanhe mensagens de erro com um efeito de som ou um aviso.** Fazer isso é jarring e desnecessário.
  - **Exceção:** Reproduza o efeito de som De parada crítica se o problema for crítico para a operação do computador e o usuário deve tomar medidas imediatas para evitar consequências graves.

## <a name="text"></a>Texto

**Geral**

- **Remova texto redundante.** Procure-o em títulos, instruções principais, instruções complementares, links de comando e botões de commit. Em geral, deixe texto completo em instruções e controles interativos e remova qualquer redundância de outros locais.
- **Use explicações centralizadas pelo usuário.** Descreva o problema em termos de ações ou metas do usuário, não em termos de com o que o software está insatisfeito. Use o idioma que os usuários de destino entendem e usam. Evite jargões técnicos.

**Incorreto:**

![captura de tela da mensagem: chamada síncrona de entrada ](images/mess-error-image46.png)

**Correto:**

![captura de tela da mensagem: ocupado recebendo uma chamada ](images/mess-error-image47.png)

Nesses exemplos, a versão correta fala o idioma do usuário, enquanto a versão incorreta é muito técnica.

- **Não use as seguintes palavras:**
  - Erro, falha (use o problema em vez disso)
  - Falha ao (não é possível usar em vez disso)
  - Ilegal, inválido, inválido (use incorreto em vez disso)
  - Anular, encerrar, encerrar (usar parar em vez disso)
  - Catastrófico, fatal (use sério em vez disso)

Esses termos são desnecessários e contrários ao tom incentivador de Windows. Quando [usado corretamente,](vis-std-icons.md)o ícone de erro comunica suficientemente que há um problema.

**Incorreto:**

![captura de tela da mensagem: falha catastrófica! ](images/mess-error-image48.png)

**Correto:**

![captura de tela da mensagem: o backup deve ser fechado ao mesmo tempo ](images/mess-error-image49.png)

No exemplo incorreto, os termos "catastrófico" e "falha" são desnecessários.

- Não use frases que culpam o usuário ou implicam erro do usuário. Evite usar você e seu na formulação. Embora a voz ativa seja geralmente preferida, use a voz passiva quando o usuário for o assunto e poderá sentir a culpa do erro se a voz ativa fosse usada.

**Incorreto:**

![captura de tela da mensagem que você inseriu logon incorreto ](images/mess-error-image50.png)

**Correto:**

![captura de tela da mensagem: senha incorreta ](images/mess-error-image51.png)

O exemplo incorreto culpa o usuário usando a voz ativa.

- **Seja específico.** Evite palavras vagas, como erro de sintaxe e operação ilegal. Forneça nomes, locais e valores específicos dos objetos envolvidos.

**Incorreto:**

Arquivo não localizado.

O disco está cheio.

Valor fora do intervalo.

O caractere é inválido.

Dispositivo não disponível.

Esses problemas seriam muito mais fáceis de resolver com nomes, locais e valores específicos.

- **Não dê problemas possivelmente improvável, causas ou soluções em uma tentativa de ser específica.** Não forneça um problema, causa ou solução, a menos que seja provável que esteja certo. Por exemplo, é melhor dizer que ocorreu um erro desconhecido do que algo que provavelmente não é preciso.
- **Evite a palavra "por favor",** exceto nas situações em que o usuário é solicitado a fazer algo inconveniente (como aguardar) ou o software é culpado pela situação.

**Correto:**

aguarde enquanto Windows copia os arquivos para o computador.

- **Use a palavra "Desculpa" somente em mensagens de erro que resultam em sérios problemas para o usuário** (por exemplo, perda de dados ou incapacidade de usar o computador). Não se esqueça de que o problema ocorreu durante o funcionamento normal do programa (por exemplo, se o usuário precisar aguardar uma conexão de rede ser encontrada).

**Correto:**

Infelizmente, o backup da Fabrikam detectou um problema irrecuperável e foi desligado para proteger os arquivos no computador.

- **Consulte os produtos usando seus nomes curtos.** Não use nomes completos de produtos ou símbolos de marcas. Não inclua o nome da empresa, a menos que os usuários associem o nome da empresa ao produto. Não inclua números de versão do programa.

**Incorreto:**

![captura de tela que mostra uma mensagem Microsoft Office Outlook ' não é possível abrir este item '. ](images/mess-error-image52.png)

**Correto:**

![captura de tela da mensagem: não é possível abrir este item ](images/mess-error-image53.png)

No exemplo incorreto, são usados nomes completos de produtos e símbolos de marcas comerciais.

- **Use aspas duplas ao contrário dos nomes de objetos.** Isso torna o texto mais fácil de analisar e evita instruções potencialmente constrangedorass.
  - **Exceção:** Caminhos de arquivo totalmente qualificados, URLs e nomes de domínio não precisam estar entre aspas duplas.

**Correto:**

![captura de tela da mensagem: ' minha casa ' está indisponível ](images/mess-error-image54.png)

Neste exemplo, a mensagem de erro seria confusa se o nome do objeto não estivesse entre aspas.

- **Evite iniciar frases com nomes de objeto.** Fazer isso geralmente é difícil de analisar.
- **Não use pontos de exclamação ou palavras com todas as letras maiúsculas.** Os pontos de exclamação e as letras maiúsculas fazem parecer que você está gritar ao usuário.

Para obter mais diretrizes e exemplos, consulte [estilo e Tom](text-style-tone.md).

**Títulos**

- **Use o título para identificar o comando ou recurso do qual o erro foi originado.** Exceções:
  - Se um erro for exibido por vários comandos diferentes, considere usar o nome do programa em vez disso.
  - Se esse título fosse redundante ou confuso com a instrução principal, use o nome do programa em vez disso.
- **Não use o título para explicar ou resumir o problema** que é a finalidade da instrução principal.

**Incorreto:**

![Captura de tela que mostra uma mensagem ' não é possível renomear nova pasta '. ](images/mess-error-image55.png)

Neste exemplo, o título está sendo usado incorretamente para explicar o problema.

- Use maiúsculas e minúsculas no estilo de título, sem pontuação final.

**Instruções principais**

- **Use a instrução principal para descrever o problema em linguagem clara, simples e específica.**
- **Seja conciso Use apenas uma única frase completa.** Parênteses da instrução principal até as informações essenciais. Você pode deixar o assunto implícito se for seu programa ou usuário. Inclua o motivo do problema se você puder fazer isso de forma concisa. Se você precisar explicar algo mais, use uma instrução complementar.

**Incorreto:**

![captura de tela da mensagem: não é possível instalar a atualização ](images/mess-error-image56.png)

Neste exemplo, a mensagem de erro inteira é colocada na instrução principal, tornando-a difícil de ler.

- **Seja específico se houver objetos envolvidos, forneça seus nomes.**
- **Evite colocar caminhos de arquivo completos e URLs na instrução principal.** Em vez disso, use um nome curto (como o nome do arquivo) e coloque o nome completo (como o caminho do arquivo) na instrução complementar. No entanto, você pode colocar um único caminho de arquivo completo ou uma URL na instrução principal, caso a mensagem de erro não precise de uma instrução complementar.

![captura de tela da mensagem: não é possível excluir o arquivo fabrikam ](images/mess-error-image57.png)

Neste exemplo, somente o nome do arquivo está na instrução principal. O caminho completo está na instrução complementar.

- **Não forneça o caminho completo do arquivo e a URL se isso for óbvio no contexto.**

![captura de tela da mensagem: não é possível renomear a nova pasta ](images/mess-error-image58.png)

neste exemplo, o usuário está renomeando um arquivo do Windows Explorer. Nesse caso, o caminho completo do arquivo não é necessário porque é óbvio do contexto.

- Use conjugação presente sempre que possível.
- Use a capitalização com estilo de frase.
- Não inclua os períodos finais se a instrução for uma instrução. Se a instrução for uma pergunta, inclua um ponto de interrogação final.

**Modelos de instrução principal**

Embora não haja regras estritas para frases, tente usar os seguintes modelos de instrução principal sempre que possível:

- [nome de entidade opcional] não pode [executar ação]
- [nome de entidade opcional] não é possível [executar ação] porque [motivo]
- [nome de entidade opcional] não é possível [executar ação] para "[nome do objeto]"
- [nome de entidade opcional] não é possível [executar ação] para "[nome do objeto]" porque [motivo]
- Não há [recurso] suficiente para [executar ação]
- [Nome da entidade] não tem um [nome do objeto] necessário para [finalidade]
- [O dispositivo ou a configuração] está desativado para que [resultados indesejados]
- [Dispositivo ou configuração] não está [disponível \| foi encontrado \| habilitado ativado \| ]
- "[nome do objeto]" não está disponível no momento
- O nome de usuário ou a senha está incorreta
- Você não tem permissão para acessar "[nome do objeto]"
- Você não tem privilégios para [executar ação]
- [nome do programa] ocorreu um problema sério e deve ser fechado imediatamente

É claro que faça alterações conforme necessário para que a instrução principal seja gramaticamente correta e esteja em conformidade com as principais diretrizes de instrução.

**Instruções complementares**

- Use a instrução complementar para:
  - Dê detalhes adicionais sobre o problema.
  - Explicar a causa do problema.
  - Liste as etapas que o usuário pode seguir para corrigir o problema.
  - Forneça medidas para evitar que o problema se repita.
- **Sempre que possível, proponha uma solução prática e útil para que os usuários possam corrigir o problema.** No entanto, certifique-se de que a solução proposta provavelmente resolva o problema. Não perca tempo dos usuários sugerindo soluções possíveis, mas improváveis.

**Incorreto:**

![captura de tela da mensagem: sem memória ](images/mess-error-image59.png)

Neste exemplo, embora o problema e sua solução recomendada sejam possíveis, eles são muito improváveis.

- **Se o problema for um valor incorreto inserido pelo usuário, use a instrução complementar para explicar os valores corretos.** Os usuários não devem ter que determinar essas informações de outra fonte.
- **Não forneça uma solução se ela puder ser deduzida trivialmente da instrução do problema.**

![captura de tela da mensagem: valor de hora incorreto ](images/mess-error-image33.png)

Neste exemplo, nenhuma instrução complementar é necessária; a solução pode ser deduzida trivialmente da instrução do problema.

- **Se a solução tiver várias etapas, apresente as etapas na ordem em que elas devem ser concluídas.** No entanto, evite soluções de várias etapas porque os usuários têm dificuldade para se lembrar de mais de duas ou três etapas simples. Se mais etapas são necessárias, consulte o tópico de Ajuda apropriado.
- **Mantenha as instruções complementares concisas.** Forneça apenas o que os usuários precisam saber. Omita detalhes desnecessários. Visa um máximo de três frases de comprimento moderado.
- **Para evitar erros enquanto os usuários executam instruções, coloque os resultados antes da ação.**

**Correto:**

Para reiniciar Windows, clique em OK.

**Incorreto:**

Clique em OK para reiniciar Windows.

No exemplo incorreto, os usuários têm maior probabilidade de clicar em OK por acidente.

- **Não é recomendável entrar em contato com um administrador, a menos que isso esteja entre as soluções mais prováveis para o problema.** Reserve essas soluções para problemas que realmente só podem ser resolvidos por um administrador.

**Incorreto:**

![captura de tela da mensagem: servidor indisponível ](images/mess-error-image60.png)

Neste exemplo, provavelmente o problema é com a conexão de rede do usuário, portanto, não vale a pena entrar em contato com um administrador.

- **Não recomenda entrar em contato com o suporte técnico.** A opção de entrar em contato com o suporte técnico para resolver um problema está sempre disponível e não precisa ser promovida por meio de mensagens de erro. Em vez disso, concentre-se em escrever mensagens de erro úteis para que os usuários possam resolver problemas sem entrar em contato com o suporte técnico.

**Incorreto:**

![Captura de tela que mostra uma mensagem "Não é possível abrir este item". ](images/mess-error-image61.png)

Neste exemplo, a mensagem de erro recomenda incorretamente entrar em contato com o suporte técnico.

- Use frases completas, capitalização de estilo de frase e pontuação final.

**Botões de commit**

- Se a mensagem de erro fornece botões de comando ou links de comando que resolvem o problema, siga suas respectivas diretrizes nas [Caixas de Diálogo](win-dialog-box.md).
- Se o programa deve terminar como resultado do erro, forneça um botão Sair do programa. Para evitar confusão, não use Fechar para essa finalidade.
- Caso contrário, forneça um botão Fechar. Não use OK para mensagens de erro, pois essa palavra implica que os problemas estão ok.
  - **Exceção:** Use OK se o mecanismo de relatório de erros tiver rótulos fixos (como com a API MessageBox.)

## <a name="documentation"></a>Documentação

Ao se referir a erros:

- Consulte erros por sua instrução principal. Se a instrução principal for longa ou detalhada, resumi-a.
- Se necessário, você pode consultar uma caixa de diálogo de mensagem de erro como uma mensagem. Veja como uma mensagem de erro somente na programação e em outras documentações técnicas.
- Quando possível, forja o texto usando negrito. Caso contrário, coloque o texto entre aspas somente se necessário para evitar confusão.

**Exemplo:** Se você receber um **Não há nenhum disco CD** na mensagem da unidade, insira um novo disco cd na unidade e tente novamente.
