---
title: Mensagens de erro (noções básicas de design)
description: Uma mensagem de erro alerta os usuários sobre um problema que já ocorreu.
ms.assetid: b02110e9-985d-4448-9c95-eb958b0059b1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 50e9d945baf736329d38334a94ede6158621167c
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984099"
---
# <a name="error-messages-design-basics"></a>Mensagens de erro (noções básicas de design)

> [!NOTE]
> este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Uma mensagem de erro alerta os usuários sobre um problema que já ocorreu. Por outro lado, uma mensagem de aviso alerta os usuários de uma condição que pode causar um problema no futuro. As mensagens de erro podem ser apresentadas usando caixas de diálogo modais, mensagens in-loco, notificações ou balões.

![captura de tela da mensagem de erro: não é possível renomear](images/mess-error-image1.png)

Uma mensagem de erro modal típica.

As mensagens de erro efetivas informam aos usuários que ocorreu um problema, explicam por que ele aconteceu e fornecem uma solução para que os usuários possam corrigir o problema. Os usuários devem executar uma ação ou alterar seu comportamento como resultado de uma mensagem de erro.

As mensagens de erro úteis e bem escritas são cruciais para uma experiência de usuário de qualidade. Mensagens de erro mal gravadas resultam em baixa satisfação do produto e são uma das principais causas dos custos de suporte técnico do podem ser evitados. As mensagens de erro desnecessárias interrompem o fluxo dos usuários.

**Observação:** As diretrizes relacionadas a [caixas de diálogo](win-dialog-box.md), mensagens de [aviso](mess-warn.md), [confirmações](mess-confirm.md), [ícones padrão](vis-std-icons.md), [notificações](mess-notif.md)e [layout](vis-layout.md) são apresentadas em artigos separados.

## <a name="is-this-the-right-user-interface"></a>Esta é a interface do usuário correta?

Para decidir, considere estas perguntas:

- **A interface do usuário está apresentando um problema que já ocorreu?** Caso contrário, a mensagem não é um erro. Se o usuário estiver alertando sobre uma condição que pode causar um problema no futuro, use uma mensagem de aviso.
- **O problema pode ser impedido sem causar confusão?** Nesse caso, evite o problema. Por exemplo, use controles que são restritos a valores válidos em vez de usar controles irrestrito que podem exigir mensagens de erro. Além disso, desabilitar controles ao clicar resultaria em erro, contanto que seja óbvio por que o controle está desabilitado.
- **O problema pode ser corrigido automaticamente?** Nesse caso, manipule o problema e omita a mensagem de erro.
- **Os usuários provavelmente executarão uma ação ou alterarão seu comportamento como resultado da mensagem?** Caso contrário, a condição não justifica a interrupção do usuário para que seja melhor suprimir o erro.
- **O problema é relevante quando os usuários estão usando ativamente outros programas?** Nesse caso, considere mostrar o problema usando um [ícone da área de notificação](winenv-notification.md).
- **O problema não está relacionado à atividade do usuário atual, não requer ação imediata do usuário e pode ignorá-lo livremente?** Em caso afirmativo, use uma [notificação de falha de ação](mess-notif.md) .
- **O problema está relacionado ao status de uma tarefa em segundo plano dentro de uma janela principal?** Nesse caso, considere mostrar o problema usando [barras de status](ctrl-status-bars.md).
- **Os principais usuários de destino são profissionais de ti?** Nesse caso, considere o uso de um mecanismo de comentários alternativo, como entradas de [arquivo de log](glossary.md) ou alertas de email. Os profissionais de ti preferem fortemente os arquivos de log para informações não críticas.

## <a name="design-concepts"></a>Conceitos de design

**As características de mensagens de erro deficientes**

Não deve ser surpresa que haja muitas mensagens de erro irritantes, inconvenientes e mal escritas. E como as mensagens de erro geralmente são apresentadas usando caixas de diálogo modais, elas interrompem a atividade atual do usuário e a demanda para serem confirmadas antes de permitir que o usuário continue.

Parte do problema é que há muitas maneiras de fazer isso de errado. Considere estes exemplos da sala de mensagens de erro do pena:

**Mensagens de erro desnecessárias**

**Incorreto:**

![captura de tela de mensagem de erro: falha no aplicativo ](images/mess-error-image2.png)

este exemplo do Windows XP pode ser a pior mensagem de erro nunca. ele indica que um programa não pôde ser iniciado porque Windows em si está no processo de desligamento. não há nada que o usuário possa fazer sobre isso ou até mesmo deseja fazer isso (o usuário optou por desligar Windows, depois de tudo). e exibindo essa mensagem de erro, Windows impede que ela seja desligada!

**O problema:** A própria mensagem de erro é o problema. Além de ignorar a mensagem de erro, não há nada para que os usuários façam.

**Causa principal:** Relatar todos os casos de erro, independentemente dos objetivos dos usuários ou do ponto de vista.

**Alternativa recomendada:** Não Relate erros que os usuários não se preocupam.

**Mensagens de erro "êxito"**

**Incorreto:**

![captura de tela de mensagem de erro: falha na remoção ](images/mess-error-image3.png)

essa mensagem de erro resultou do usuário optando por não reiniciar Windows imediatamente após a remoção do programa. A remoção do programa foi bem-sucedida do ponto de vista do usuário.

**O problema:** Não há nenhum erro do ponto de vista do usuário. Além de ignorar a mensagem de erro, não há nada para que os usuários façam.

**Causa principal:** A tarefa foi concluída com êxito do ponto de vista do usuário, mas falhou no ponto de vista do programa de desinstalação.

**Alternativa recomendada:** Não Relate erros para condições que os usuários consideram aceitáveis.

**Mensagens de erro completamente inútil**

**Incorreto:**

![captura de tela de mensagem de erro: erro desconhecido ](images/mess-error-image4.png)

Os usuários aprendem que houve um erro, mas não têm idéia do que o erro foi ou o que fazer a respeito. E não, não está OK!

**O problema:** A mensagem de erro não dá um problema específico e não há nada que os usuários possam fazer a respeito.

**Causa principal:** Provavelmente, o programa tem tratamento de erro ruim.

**Alternativa recomendada:** Projete um bom tratamento de erros no programa.

**Mensagens de erro do incompreensível**

**Incorreto:**

![captura de tela de mensagem de erro: backup não concluído ](images/mess-error-image5.png)

Neste exemplo, a declaração do problema está clara, mas a explicação suplementar é totalmente desafiadora.

**O problema:** A declaração ou a solução do problema é incompreensível.

**Causa principal:** Explicando o problema do ponto de vista do código em vez do do usuário.

**Alternativa recomendada:** Grave o texto da mensagem de erro que os usuários de destino podem entender facilmente. Forneça soluções que os usuários podem realmente executar. Criar a experiência de mensagem de erro do seu programa não tem os programadores comporem mensagens de erro no local.

**Mensagens de erro que se comunicam**

**Incorreto:**

![captura de tela de mensagem extremamente detalhada ](images/mess-error-image6.png)

Neste exemplo, a mensagem de erro, aparentemente, tenta explicar cada etapa de solução de problemas.

**O problema:** Excesso de informações.

**Causa principal:** Fornecendo muitos detalhes ou tentando explicar um processo complicado de solução de problemas em uma mensagem de erro.

**Alternativa recomendada:** Evite detalhes desnecessários. Além disso, evite solucionadores de problemas. Se uma solução de problemas for necessária, concentre-se nas soluções mais prováveis e explique o restante vinculando-se ao tópico apropriado na ajuda.

**Mensagens de erro desnecessariamente esdurantes**

**Incorreto:**

![captura de tela da mensagem: não é possível localizar o objeto ](images/mess-error-image7.png)

A incapacidade do programa de encontrar um objeto dificilmente parece catastrófica. E supondo que seja catastrófico, por que a resposta é OK?

**O problema:** O tom do programa é desnecessariamente surpreendente ou drástico.

**Causa principal:** O problema ocorre devido a um bug que aparece catastrófico no ponto de vista do programa.

**Alternativa recomendada:** Escolha o idioma cuidadosamente com base no ponto de vista do usuário.

**Mensagens de erro que os usuários culpam**

**Incorreto:**

![captura de tela da mensagem: caractere ilegal ](images/mess-error-image8.png)

Por que fazer com que os usuários se sintam como um criminal?

**O problema:** A mensagem de erro é formulada de uma maneira que desmente o usuário de fazer um erro.

**Causa principal:** Frases insensíveis que se concentram no comportamento do usuário em vez do problema.

**Alternativa recomendada:** Concentre-se no problema, não na ação do usuário que levou ao problema, usando a voz passiva conforme necessário.

**Mensagens de erro falsas**

**Incorreto:**

![captura de tela da mensagem: erro no relatório de erros ](images/mess-error-image9.png)

Neste exemplo, a instrução do problema é bastante problemática e nenhuma solução é fornecida.

**O problema:** Instruções de mensagem de erro que são falsas ou não são sepresentes.

**Causa principal:** Criar mensagens de erro sem prestar atenção ao contexto.

**Alternativa recomendada:** Fazer com que suas mensagens de erro tenham sido feitas e revisadas por um autor. Considere o contexto e o estado de mente do usuário ao revisar os erros.

**Mensagens de erro do programador**

**Incorreto:**

![captura de tela da mensagem: endereço de violação de acesso ](images/mess-error-image10.png)

Neste exemplo, a mensagem de erro indica que há um bug no programa. Essa mensagem de erro tem significado apenas para o programador.

**O problema:** As mensagens destinadas a ajudar os desenvolvedores do programa a encontrar bugs são deixadas na versão de lançamento do programa. Essas mensagens de erro não têm nenhum significado ou valor para os usuários.

**Causa principal:** Programadores que usam a interface do usuário normal para fazer mensagens para si mesmos.

**Alternativa recomendada:** Os desenvolvedores devem compilar condicionalmente todas essas mensagens para que elas sejam removidas automaticamente da versão de lançamento de um produto. Não perca tempo tentando fazer erros como esse para os usuários porque seu único público-alvo são os programadores.

**Mensagens de erro mal apresentadas**

**Incorreto:**

![captura de tela da mensagem: falha inesperada ](images/mess-error-image11.png)

Este exemplo tem muitos erros comuns de apresentação.

**O problema:** Recebendo todos os detalhes errados na apresentação da mensagem de erro.

**Causa principal:** Não saber e aplicar as diretrizes de mensagem de erro. Não usar editores e autores para criar e revisar as mensagens de erro.

A natureza do tratamento de erros é tal que muitos desses erros são muito fáceis de fazer. É estranho perceber que a maioria das mensagens de erro pode ser falsa para o Hall of The Hall of The.

**As características de boas mensagens de erro**

Ao contrário dos exemplos ruins anteriores, boas mensagens de erro têm:

- **Um problema.** Declara que ocorreu um problema.
- **Uma causa.** Explica por que o problema ocorreu.
- **Uma solução.** Fornece uma solução para que os usuários possam corrigir o problema.

Além disso, boas mensagens de erro são apresentadas de uma maneira que é:

- **Relevantes.** A mensagem apresenta um problema que os usuários se importam.
- **Acionáveis.** Os usuários devem executar uma ação ou alterar seu comportamento como resultado da mensagem.
- **Centralizado pelo usuário.** A mensagem descreve o problema em termos de metas ou ações do usuário de destino, não em termos de com o que o código está triste.
- **Breve.** A mensagem é o mais curta possível, mas não é mais curta.
- **Claro.** A mensagem usa linguagem sem-texto para que os usuários de destino possam entender facilmente o problema e a solução.
- **Específico.** A mensagem descreve o problema usando um idioma específico, dando nomes, locais e valores específicos dos objetos envolvidos.
- **Cortês.** Os usuários não devem ser responsabilizados nem deixar de se sentir mal.
- **Raro.** Exibido raramente. Mensagens de erro exibidas com frequência são um sinal de design ruim.

Ao projetar sua experiência de tratamento de erros para ter essas características, você pode manter as mensagens de erro do programa fora do Hall de Mensagens de Erro da Cidade.

**Evitando mensagens de erro desnecessárias**

Geralmente, a melhor mensagem de erro não é nenhuma mensagem de erro. Muitos erros podem ser evitados por meio de um melhor design e geralmente há alternativas melhores para mensagens de erro. Normalmente, é melhor evitar um erro do que relatar um.

As mensagens de erro mais óbvias a evitar são aquelas que não são ativas. Se os usuários provavelmente descartarem a mensagem sem fazer ou alterar nada, omita a mensagem de erro.

Algumas mensagens de erro podem ser eliminadas porque não são problemas do ponto de vista do usuário. Por exemplo, suponha que o usuário tentou excluir um arquivo que já está no processo de exclusão. Embora esse possa ser um caso inesperado do ponto de vista do código, os usuários não consideram isso um erro porque o resultado desejado é obtido.

**Incorreto:**

![captura de tela da mensagem: não é possível excluir o arquivo ](images/mess-error-image12.png)

Essa mensagem de erro deve ser eliminada porque a ação foi bem-sucedida do ponto de vista do usuário.

Para outro exemplo, suponha que o usuário cancele explicitamente uma tarefa. Para o ponto de vista do usuário, a condição a seguir não é um erro.

**Incorreto:**

![captura de tela da mensagem: não é possível concluir o backup ](images/mess-error-image13.png)

Essa mensagem de erro também deve ser eliminada porque a ação foi bem-sucedida do ponto de vista do usuário.

Às vezes, as mensagens de erro podem ser eliminadas concentrando-se nas metas dos usuários em vez da tecnologia. Ao fazer isso, repensa o que um erro realmente é. O problema é com as metas do usuário ou com a capacidade do programa de satisfazê-las? Se a ação do usuário fizer sentido no mundo real, ela também deverá fazer sentido no software.

Por exemplo, suponha que em um programa de comércio eletrônico um usuário tente encontrar um produto usando a pesquisa, mas a consulta de pesquisa literal não tem nenhuma corresponde e o produto desejado está sem estoque. Tecnicamente, esse é um erro, mas em vez de dar uma mensagem de erro, o programa poderia:

- Continue a pesquisar produtos que mais se aproximam da consulta.
- Se a pesquisa tiver erros óbvios, recomende automaticamente uma consulta corrigida.
- Lida automaticamente com problemas comuns, como erros ortográficos, ortografias alternativas e casos verbais e pluralização incompatibilidades.
- Indique quando o produto estará em estoque.

Desde que a solicitação do usuário seja razoável, um programa de comércio eletrônico bem projetado deve retornar resultados razoáveis, não erros.

Outra ótima maneira de evitar mensagens de erro é impedindo problemas em primeiro lugar. Você pode evitar erros:

- **Usando controles restritos.** Use controles restritos a valores válidos. Controles como listas, controles deslizantes, caixas de seleção, botões de opção e seladores de data e hora são restritos a valores válidos, enquanto caixas de texto geralmente não são e podem exigir mensagens de erro. No entanto, você pode restringir caixas de texto para aceitar apenas determinados caracteres e aceitar um número máximo de caracteres.
- **Usando interações restritas.** Para operações de arrastar, permita que os usuários soltem somente em destinos válidos.
- **Usando controles desabilitados e itens de menu.** Desabilite controles e itens de menu quando os usuários puderem deduzir facilmente por que o item de controle ou de menu está desabilitado.
- **Fornecendo bons valores padrão.** Os usuários têm menor probabilidade de fazer erros de entrada se puderem aceitar os valores padrão. Mesmo se os usuários decidirem alterar o valor, o valor padrão permitirá que os usuários saibam o formato de entrada esperado.
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


| Rótulo | Valor |
|--------|-------|
| <strong>Problemas do sistema</strong><br /> O sistema operacional, o dispositivo de hardware, a rede ou o programa falhou ou não está no estado necessário para executar uma tarefa. <br /> | Muitos problemas do sistema podem ser resolvidos pelo usuário: <br /><ul><li>Os problemas do dispositivo podem ser resolvidos ao ligar o dispositivo, reconectar o dispositivo e inserir a mídia.</li><li>Os problemas de rede podem ser resolvidos verificando a conexão de rede física e <strong>executando o diagnóstico e o reparo de rede.</strong></li><li>Os problemas do programa podem ser resolvidos alterando as opções do programa ou reiniciando o programa.</li></ul><img src="images/mess-error-image25.png" alt="Screen shot of message: Can't find a camera " /><br /> Neste exemplo, o programa não pode encontrar uma câmera para executar uma tarefa de usuário.<br /><img src="images/mess-error-image26.png" alt="Screen shot of message Network discovery off " /><br /> Neste exemplo, um recurso necessário para executar uma tarefa precisa ser ligado.<br /> | 
| <strong>Problemas de arquivo</strong><br /> Um arquivo ou pasta necessário para uma tarefa iniciada pelo usuário não foi encontrado, já está em uso ou não tem o formato esperado. <br /> | <img src="images/mess-error-image27.png" alt="Screen shot of message: Can't delete file " /><br /> Neste exemplo, o arquivo ou a pasta não pode ser excluído porque não foi encontrado.<br /><img src="images/mess-error-image28.png" alt="Screen shot of message: Can't play this file " /><br /> Neste exemplo, o programa não dá suporte ao formato de arquivo determinado.<br /> | 
| <strong>Problemas de segurança</strong><br /> O usuário não tem permissão para acessar um recurso ou privilégio suficiente para executar uma tarefa iniciada pelo usuário. <br /> | <img src="images/mess-error-image29.png" alt="Screen shot of message: You don't have permission " /><br /> Neste exemplo, o usuário não tem permissão para acessar um recurso.<br /><img src="images/mess-error-image30.png" alt="Screen shot of message: You don't have privilege " /><br /> Neste exemplo, o usuário não tem o privilégio de executar uma tarefa.<br /> | 
| <strong>Problemas de tarefa</strong><br /> Há um problema específico ao executar uma tarefa iniciada pelo usuário (que não seja um sistema, arquivo não encontrado, formato de arquivo ou problema de segurança). <br /> | <img src="images/mess-error-image31.png" alt="Screen shot of message: Data can't be pasted " /><br /> Neste exemplo, os dados da Área de Transferência não podem ser Paint.<br /><img src="images/mess-error-image32.png" alt="Screen shot of message: Upgrade can't be installed " /><br /> Neste exemplo, o usuário não pode instalar uma atualização de software.<br /> | 
| <strong>Problemas de entrada do usuário</strong><br /> O usuário entrou em um valor incorreto ou inconsistente com outra entrada do usuário. <br /> | <img src="images/mess-error-image33.png" alt="Screen shot of message: Incorrect time value " /><br /> Neste exemplo, o usuário entrou em um valor de hora incorreto.<br /><img src="images/mess-error-image34.png" alt="Screen shot of message: Incorrect input format " /><br /> Neste exemplo, a entrada do usuário não está no formato correto.<br /> | 


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
  - Se o erro for um problema de entrada do usuário exibido usando uma caixa de diálogo modal ou um balão, não use um ícone. Fazer isso é um contador para o Tom incentivado de Windows. No entanto, as mensagens de erro in-loco devem usar um pequeno ícone de erro (16x16 pixels) para identificá-las claramente como mensagens de erro.

     ![captura de tela de formato postal incorreto da mensagem](images/mess-error-image38.png)

     ![captura de tela do nome do computador da mensagem muito longa](images/mess-error-image39.png)

     Nesses exemplos, os problemas de entrada do usuário não precisam de ícones de erro.

     ![captura de tela do formato incorreto do número de telefone da mensagem](images/mess-error-image40.png)

     Neste exemplo, uma mensagem de erro in-loco precisa de um pequeno ícone de erro para identificá-la claramente como uma mensagem de erro.

- Se o problema for para um recurso que tem um ícone (e não um problema de entrada do usuário), você poderá usar o ícone de recurso com uma sobreposição de erro. Se você fizer isso, use também o nome do recurso como o assunto do erro.

    ![o player de mídia de mensagem de captura de tela não pode reproduzir o arquivo ](images/mess-error-image41.png)

    Neste exemplo, o ícone de recurso tem uma sobreposição de erro e o recurso é o assunto do erro.

- **Não use ícones de aviso para erros.** Isso geralmente é feito para fazer com que a apresentação fique menos grave. Erros não são avisos.

    **Incorreto:**

    ![captura de tela de alternância rápida de mensagem não habilitada ](images/mess-error-image42.png)

    Neste exemplo, um ícone de aviso é usado incorretamente para fazer com que o erro fique menos grave.

Para obter mais diretrizes e exemplos, consulte [ícones padrão](vis-std-icons.md).

### <a name="progressive-disclosure"></a>Divulgação progressiva

- **Use um botão Mostrar/ocultar detalhes de divulgação progressiva para ocultar informações avançadas ou detalhadas em uma mensagem de erro.** Isso simplifica a mensagem de erro para uso típico. Não oculte as informações necessárias, pois os usuários talvez não as encontrem.

![captura de tela da mensagem: o ActiveSync não pode fazer logon ](images/mess-error-image43.png)

Neste exemplo, o botão de divulgação progressiva ajuda os usuários a fazer uma busca detalhada em mais detalhes se desejarem ou simplificar a interface do usuário, se não estiverem.

- **Não use mostrar/ocultar detalhes, a menos que realmente haja mais detalhes.** Não apenas redeclare as informações existentes em um formato mais detalhado.
- **Não use mostrar/ocultar detalhes para mostrar informações de ajuda.** Em vez disso, use os links da ajuda.

Para obter diretrizes de rotulamento, consulte [controles de divulgação progressiva](ctrl-progressive-disclosure-controls.md).

**Não mostrar esta mensagem novamente**

- **Se uma mensagem de erro precisar dessa opção, reconsidere o erro e sua frequência.** Se ele tiver todas as características de um erro bom (relevante, acionável e não frequente), não deverá fazer sentido para os usuários suprimirem.

Para obter mais diretrizes, consulte [caixas de diálogo](win-dialog-box.md).

### <a name="default-values"></a>Valores padrão

- **Selecione a resposta mais segura, menos destrutiva ou mais segura para ser o padrão.** Se a segurança não for um fator, selecione o comando mais provável ou conveniente.

### <a name="help"></a>Ajuda

- **Crie mensagens de erro para evitar a necessidade de ajuda.** Normalmente, os usuários não precisam ler o texto externo para entender e resolver o problema, a menos que a solução exija várias etapas.
- **Verifique se o conteúdo da ajuda é relevante e útil.** Ele não deve ser uma reversão detalhada da mensagem de erro em vez disso, deve conter informações úteis que estão além do escopo da mensagem de erro, como maneiras de evitar o problema no futuro. Não forneça um link de ajuda apenas porque você pode.
- **Use links de ajuda específicos, concisos e relevantes para acessar o conteúdo da ajuda.** Não use botões de comando ou divulgação progressiva para essa finalidade.
- **Para mensagens de erro que você não pode tornar específicas e acionáveis, considere fornecer links para o conteúdo da ajuda online.** Ao fazer isso, você pode fornecer aos usuários informações adicionais que podem ser atualizadas depois que o programa é liberado.

Para obter mais diretrizes, consulte [a ajuda](winenv-help.md).

### <a name="error-codes"></a>Códigos do Erro

- **Para mensagens de erro que você não pode tornar específicas e acionáveis ou que se beneficiam da ajuda, considere também fornecer códigos de erro.** Os usuários geralmente usam esses códigos de erro para pesquisar informações adicionais na Internet.
- **Sempre forneça uma descrição de texto do problema e da solução.** Não depende apenas do código de erro para essa finalidade.

**Incorreto:**

![captura de tela da mensagem: não é possível abrir o arquivo ](images/mess-error-image44.png)

Neste exemplo, um código de erro é usado como um substituto para um texto de solução.

- **Atribua um código de erro exclusivo para cada causa diferente.** Isso evita a solução de problemas.
- **Escolha os códigos de erro que podem ser pesquisados facilmente na Internet.** Se você usar códigos de 32 bits, use uma representação hexadecimal com um "0x" à esquerda e caracteres maiúsculos.

**Correto:**

1234

0xC0001234

**Incorreto:**

-1

-67113524

- **Use mostrar/ocultar detalhes para exibir códigos de erro.** Frase como código de erro: <error code> .

![captura de tela da mensagem: o programa não foi inicializado ](images/mess-error-image45.png)

Neste exemplo, um código de erro é usado para complementar uma mensagem de erro que pode se beneficiar de mais informações.

### <a name="sound"></a>Som

- **Não acompanha mensagens de erro com um efeito sonoro ou um aviso sonoro.** Fazer isso é dissonante e desnecessário.
  - **Exceção:** Reproduza o efeito crítico de parada de som se o problema for crítico para a operação do computador, e o usuário deve tomar uma ação imediata para evitar sérias conseqüências.

## <a name="text"></a>Texto

**Geral**

- **Remova o texto redundante.** Procure por ele em títulos, instruções principais, instruções complementares, links de comando e botões de confirmação. Em geral, deixe texto completo em instruções e controles interativos e remova qualquer redundância dos outros locais.
- **Use explicações centralizadas pelo usuário.** Descreva o problema em termos de ações ou metas do usuário, não em termos de como o software é insatisfeito. Use o idioma que os usuários de destino entendem e usam. Evite um jargão técnico.

**Incorreto:**

![captura de tela da mensagem: entrada-chamada síncrona ](images/mess-error-image46.png)

**Correto:**

![captura de tela da mensagem: ocupado recebendo uma chamada ](images/mess-error-image47.png)

Nesses exemplos, a versão correta fala sobre o idioma do usuário, enquanto a versão incorreta é muito técnica.

- **Não use as seguintes palavras:**
  - Erro, falha (em vez disso, use o problema)
  - Falha ao (em vez disso, use não é possível)
  - Inválido, inválido, incorreto (use em vez disso)
  - Abort, Kill e Terminate (use parar em vez disso)
  - Catastrófico, fatal (em vez disso, use grave)

Esses termos são desnecessários e ao contrário do Tom incentivado de Windows. Quando [usado corretamente](vis-std-icons.md), o ícone de erro comunica suficientemente que há um problema.

**Incorreto:**

![captura de tela da mensagem: falha catastrófica! ](images/mess-error-image48.png)

**Correto:**

![captura de tela da mensagem: o backup deve ser fechado ao mesmo tempo ](images/mess-error-image49.png)

No exemplo incorreto, os termos "catastrófico" e "falha" são desnecessários.

- Não use frases que responsabilizam o usuário ou implicam em erro do usuário. Evite usar você e seu na frase. Embora a voz ativa seja geralmente preferencial, use a voz passiva quando o usuário for o assunto e poderá se sentir responsável pelo erro se a voz ativa tiver sido usada.

**Incorreto:**

![captura de tela da mensagem que você entrou no logon incorreto ](images/mess-error-image50.png)

**Correto:**

![captura de tela da mensagem: senha incorreta ](images/mess-error-image51.png)

O exemplo incorreto responsabiliza o usuário usando a voz ativa.

- **Seja específico.** Evite palavras vaga, como erro de sintaxe e operação ilegal. Forneça nomes, locais e valores específicos dos objetos envolvidos.

**Incorreto:**

Arquivo não localizado.

O disco está cheio.

Valor fora do intervalo.

O caractere é inválido.

Dispositivo não disponível.

Esses problemas seriam muito mais fáceis de resolver com nomes, locais e valores específicos.

- **Não dê problemas, causas ou soluções possivelmente improváveis em uma tentativa de ser específica.** Não forneça um problema, uma causa ou uma solução, a menos que seja provável que ela esteja correta. Por exemplo, é melhor dizer que ocorreu um erro desconhecido do que algo que provavelmente será impreciso.
- **Evite a palavra "por favor",** exceto em situações em que o usuário é solicitado a fazer algo inconveniente (como aguardar) ou o software é o responsável pela situação.

**Correto:**

Aguarde enquanto Windows copia os arquivos para o computador.

- **Use a palavra "sorry" somente** em mensagens de erro que resultem em problemas sérios para o usuário (por exemplo, perda de dados ou incapacidade de usar o computador). Não peça desculpas se o problema ocorreu durante o funcionamento normal do programa (por exemplo, se o usuário precisar aguardar uma conexão de rede ser encontrada).

**Correto:**

O Backup da Fabrikam detectou um problema irrecuperável e foi desligado para proteger arquivos no computador.

- **Consulte produtos usando seus nomes curtos.** Não use nomes completos de produtos ou símbolos de marca. Não inclua o nome da empresa, a menos que os usuários associem o nome da empresa ao produto. Não inclua números de versão do programa.

**Incorreto:**

![Captura de tela que mostra Microsoft Office Outlook mensagem "Não é possível abrir este item". ](images/mess-error-image52.png)

**Correto:**

![captura de tela da mensagem: não é possível abrir este item ](images/mess-error-image53.png)

No exemplo incorreto, são usados nomes completos de produtos e símbolos de marca.

- **Use aspas duplas em torno de nomes de objeto.** Isso facilita a análise do texto e evita instruções potencialmente embaraçosas.
  - **Exceção:** Caminhos de arquivo totalmente qualificados, URLs e nomes de domínio não precisam estar entre aspas duplas.

**Correto:**

![captura de tela da mensagem: "minha casa" não está disponível ](images/mess-error-image54.png)

Neste exemplo, a mensagem de erro seria confusa se o nome do objeto não estivesse entre aspas.

- **Evite iniciar frases com nomes de objeto.** Fazer isso geralmente é difícil de analisar.
- **Não use pontos de exclamação ou palavras com todas as letras maiúsculas.** As marcas de exclamação e as letras maiúsculas fazem parecer que você está olhando para o usuário.

Para obter mais diretrizes e exemplos, consulte [Estilo e tom.](text-style-tone.md)

**Títulos**

- **Use o título para identificar o comando ou recurso do qual o erro foi originado.** Exceções:
  - Se um erro for exibido por muitos comandos diferentes, considere usar o nome do programa.
  - Se esse título for redundante ou confuso com a instrução principal, use o nome do programa.
- **Não use o título para explicar ou resumir o problema** que é a finalidade da instrução principal.

**Incorreto:**

![Captura de tela que mostra uma mensagem "Não é possível renomear a nova pasta". ](images/mess-error-image55.png)

Neste exemplo, o título está sendo usado incorretamente para explicar o problema.

- Use a capitalização de estilo de título, sem terminar a pontuação.

**Instruções principais**

- **Use a instrução principal para descrever o problema em linguagem clara, simples e específica.**
- **Seja conciso, use apenas uma única frase completa.** Pare a instrução principal até as informações essenciais. Você pode deixar o assunto implícito se ele for seu programa ou o usuário. Inclua o motivo do problema se você puder fazer isso de forma concisa. Se você precisa explicar mais alguma coisa, use uma instrução complementar.

**Incorreto:**

![captura de tela da mensagem: a atualização não pode ser instalada ](images/mess-error-image56.png)

Neste exemplo, toda a mensagem de erro é colocada na instrução principal, dificultando a leitura.

- **Seja específico se houver objetos envolvidos, dê seus nomes.**
- **Evite colocar caminhos de arquivo completos e URLs na instrução principal.** Em vez disso, use um nome curto (como o nome do arquivo) e coloque o nome completo (como o caminho do arquivo) na instrução complementar. No entanto, você pode colocar um único caminho de arquivo completo ou URL na instrução principal se a mensagem de erro não precisar de uma instrução complementar.

![captura de tela da mensagem: não é possível excluir o arquivo fabrikam ](images/mess-error-image57.png)

Neste exemplo, somente o nome do arquivo está na instrução principal. O caminho completo está na instrução complementar.

- **Não dê o caminho e a URL completos do arquivo se for óbvio no contexto.**

![captura de tela da mensagem: não é possível renomear a nova pasta ](images/mess-error-image58.png)

Neste exemplo, o usuário está renomeando um arquivo do Windows Explorer. Nesse caso, o caminho completo do arquivo não é necessário porque é óbvio no contexto.

- Use o tempo presente sempre que possível.
- Use a capitalização com estilo de frase.
- Não inclua períodos finais se a instrução for uma instrução. Se a instrução for uma pergunta, inclua um ponto de interrogação final.

**Modelos de instrução principais**

Embora não haja regras estritas para frase, tente usar os seguintes modelos de instrução principais sempre que possível:

- [nome da assunto opcional] não pode [executar ação]
- [nome da assunto opcional] não pode [executar ação] porque [motivo]
- [nome da assunto opcional] não pode [executar ação] para "[nome do objeto]"
- [nome da assunto opcional] não pode [executar ação] para "[nome do objeto]" porque [motivo]
- Não há [recurso] suficiente para [executar a ação]
- [Nome da assunto] não tem um [nome do objeto] necessário para [finalidade]
- [Dispositivo ou configuração] está desligado para que [resultados indesejáveis]
- [Dispositivo ou configuração] não está [disponível \| encontrado \| \| ativado]
- "[nome do objeto]" não está disponível no momento
- O nome de usuário ou a senha está incorreto
- Você não tem permissão para acessar "[nome do objeto]"
- Você não tem privilégio para [executar a ação]
- [nome do programa] teve um problema sério e deve ser fechado imediatamente

É claro que faça alterações conforme necessário para que a instrução principal seja gramaticalmente correta e cumpra as diretrizes de instrução principais.

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
