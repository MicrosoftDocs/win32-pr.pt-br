---
title: Mensagens de erro (noções básicas de design)
description: Uma mensagem de erro alerta os usuários sobre um problema que já ocorreu.
ms.assetid: b02110e9-985d-4448-9c95-eb958b0059b1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 0a8ee17093618dc8a192cfad8ce962f7ed04fc76
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104553602"
---
# <a name="error-messages-design-basics"></a>Mensagens de erro (noções básicas de design)

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

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

Este exemplo do Windows XP pode ser a pior mensagem de erro nunca. Ele indica que um programa não pôde ser iniciado porque o próprio Windows está no processo de desligamento. Não há nada que o usuário possa fazer sobre isso ou até mesmo deseja fazer isso (o usuário optou por desligar o Windows, afinal). E exibindo essa mensagem de erro, o Windows impede que ele seja desligado!

**O problema:** A própria mensagem de erro é o problema. Além de ignorar a mensagem de erro, não há nada para que os usuários façam.

**Causa principal:** Relatar todos os casos de erro, independentemente dos objetivos dos usuários ou do ponto de vista.

**Alternativa recomendada:** Não Relate erros que os usuários não se preocupam.

**Mensagens de erro "êxito"**

**Incorreto:**

![captura de tela de mensagem de erro: falha na remoção ](images/mess-error-image3.png)

Essa mensagem de erro resultou do usuário optando por não reiniciar o Windows imediatamente após a remoção do programa. A remoção do programa foi bem-sucedida do ponto de vista do usuário.

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

![Captura de tela que mostra uma mensagem ' servidor indisponível ' do Office Communicator. ](images/mess-error-image21.png)

Essa mensagem de erro é adequada para um erro desconhecido se a conectividade de rede costuma ser o problema.

**Determinar o tipo de mensagem apropriado**

Alguns problemas podem ser apresentados como erro, aviso ou informações, dependendo da ênfase e da formulação. Por exemplo, suponha que uma página da Web não possa carregar um controle ActiveX não assinado com base na configuração atual do Windows Internet Explorer:

- **Ao.** "Esta página não pode carregar um controle ActiveX não assinado". (Fraseada como um problema existente.)
- **Alerta.** "Esta página pode não se comportar conforme o esperado porque o Windows Internet Explorer não está configurado para carregar controles ActiveX não assinados." ou "permitir que esta página instale um controle ActiveX não assinado? Fazer isso de fontes não confiáveis pode prejudicar seu computador. " (Fraseada como condições que podem causar problemas futuros.)
- **Divulgação.** "Você configurou o Windows Internet Explorer para bloquear controles ActiveX não assinados". (Fraseada como uma declaração de fato).

**Para determinar o tipo de mensagem apropriado, concentre-se no aspecto mais importante do problema que os usuários precisam conhecer ou agir.** Normalmente, se um problema impedir que o usuário Continue, você deverá apresentá-lo como um erro; Se o usuário puder continuar, apresente-o como um aviso. Crie a [instrução principal](text-ui.md) ou outro texto correspondente com base nesse foco e, em seguida, escolha um ícone ([padrão](vis-std-icons.md) ou de outra forma) que corresponda ao texto. O texto da instrução principal e os ícones sempre devem corresponder.

**Apresentação da mensagem de erro**

A maioria das mensagens de erro em programas do Windows é apresentada usando caixas de diálogo modais (como mostra a maioria dos exemplos neste artigo), mas há outras opções:

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

**Evitar sobrecomunicação**

Em geral, [os usuários não lêem, digitalizam](vis-layout.md). Quanto mais texto houver, mais difícil será a verificação do texto e os usuários mais prováveis não lerá o texto. Como resultado, é importante reduzir o texto para seu Essentials e usar a divulgação progressiva e os links de ajuda quando necessário para fornecer informações adicionais.

Há muitos exemplos extremos, mas vamos examinar mais um típico. O exemplo a seguir tem a maioria dos atributos de uma boa mensagem de erro, mas seu texto não é conciso e requer que a motivação seja lida.

**Incorreto:**

![captura de tela da mensagem detalhada ](images/mess-error-image23.png)

Este exemplo é uma boa mensagem de erro, mas se comunica.

O que tudo esse texto realmente diz? Algo assim:

**Correto:**

![captura de tela da mensagem: gravador de CD não detectado ](images/mess-error-image24.png)

Essa mensagem de erro tem basicamente as mesmas informações, mas é muito mais concisa.

Usando a ajuda para fornecer os detalhes, essa mensagem de erro tem um [estilo de pirâmide invertido](text-ui.md) de apresentação.

Para obter mais diretrizes e exemplos sobre a sobrecomunicação, consulte [texto da interface do usuário](text-ui.md).

**Se você fizer apenas oito coisas**

1. Crie seu programa para tratamento de erros.
2. Não forneça mensagens de erro desnecessárias.
3. Evite confusão do usuário, fornecendo as mensagens de erro necessárias.
4. Verifique se a mensagem de erro fornece um problema, uma causa e uma solução.
5. Verifique se a mensagem de erro é relevante, acionável, breve, claro, específico, educado e raro.
6. Criar mensagens de erro do ponto de vista do usuário, não do ponto de vista do programa.
7. Evite envolver o usuário na solução de problemas Use uma mensagem de erro diferente para cada causa detectável.
8. Use o método de apresentação de peso mais leve que faz o trabalho bem.

**Padrões de uso**

As mensagens de erro têm vários padrões de uso:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Problemas do sistema</strong><br/> O sistema operacional, o dispositivo de hardware, a rede ou o programa falhou ou não está no estado necessário para executar uma tarefa. <br/></td>
<td>Muitos problemas do sistema podem ser resolvidos pelo usuário: <br/>
<ul>
<li>Problemas de dispositivo podem ser resolvidos ligando o dispositivo, reconectando o dispositivo e inserindo mídia.</li>
<li>Problemas de rede podem ser resolvidos verificando a conexão de rede física e executando o <strong>diagnóstico e o reparo da rede</strong>.</li>
<li>Problemas de programa podem ser resolvidos alterando-se as opções do programa ou reiniciando o programa.</li>
</ul>
<img src="images/mess-error-image25.png" alt="Screen shot of message: Can&#39;t find a camera " /><br/> Neste exemplo, o programa não pode localizar uma câmera para executar uma tarefa de usuário.<br/> <img src="images/mess-error-image26.png" alt="Screen shot of message Network discovery off " /><br/> Neste exemplo, um recurso necessário para executar uma tarefa precisa ser ativado.<br/></td>
</tr>
<tr class="even">
<td><strong>Problemas de arquivo</strong><br/> Um arquivo ou pasta necessário para uma tarefa iniciada pelo usuário não foi encontrado, já está em uso ou não tem o formato esperado. <br/></td>
<td><img src="images/mess-error-image27.png" alt="Screen shot of message: Can&#39;t delete file " /><br/> Neste exemplo, o arquivo ou a pasta não pode ser excluída porque não foi encontrada.<br/> <img src="images/mess-error-image28.png" alt="Screen shot of message: Can&#39;t play this file " /><br/> Neste exemplo, o programa não dá suporte ao formato de arquivo fornecido.<br/></td>
</tr>
<tr class="odd">
<td><strong>Problemas de segurança</strong><br/> O usuário não tem permissão para acessar um recurso ou privilégio suficiente para executar uma tarefa iniciada pelo usuário. <br/></td>
<td><img src="images/mess-error-image29.png" alt="Screen shot of message: You don&#39;t have permission " /><br/> Neste exemplo, o usuário não tem permissão para acessar um recurso.<br/> <img src="images/mess-error-image30.png" alt="Screen shot of message: You don&#39;t have privilege " /><br/> Neste exemplo, o usuário não tem o privilégio para executar uma tarefa.<br/></td>
</tr>
<tr class="even">
<td><strong>Problemas de tarefas</strong><br/> Há um problema específico ao executar uma tarefa iniciada pelo usuário (diferente de um sistema, arquivo não encontrado, formato de arquivo ou problema de segurança). <br/></td>
<td><img src="images/mess-error-image31.png" alt="Screen shot of message: Data can&#39;t be pasted " /><br/> Neste exemplo, os dados da área de transferência não podem ser colados no Paint.<br/> <img src="images/mess-error-image32.png" alt="Screen shot of message: Upgrade can&#39;t be installed " /><br/> Neste exemplo, o usuário não pode instalar uma atualização de software.<br/></td>
</tr>
<tr class="odd">
<td><strong>Problemas de entrada do usuário</strong><br/> O usuário inseriu um valor incorreto ou inconsistente com outra entrada do usuário. <br/></td>
<td><img src="images/mess-error-image33.png" alt="Screen shot of message: Incorrect time value " /><br/> Neste exemplo, o usuário inseriu um valor de hora incorreto.<br/> <img src="images/mess-error-image34.png" alt="Screen shot of message: Incorrect input format " /><br/> Neste exemplo, a entrada do usuário não está no formato correto.<br/></td>
</tr>
</tbody>
</table>

## <a name="guidelines"></a>Diretrizes

### <a name="presentation"></a>Apresentação

- **Use caixas de diálogo de tarefas sempre que apropriado** para obter uma aparência e um layout consistentes. As caixas de diálogo de tarefas exigem o Windows Vista ou posterior, portanto, elas não são adequadas para versões anteriores do Windows. Se você precisar usar uma caixa de mensagem, separe a instrução principal da instrução complementar com duas quebras de linha.

### <a name="user-input-errors"></a>Erros de entrada do usuário

- **Sempre que possível, evite ou reduza os erros de entrada do usuário:**
  - Usando controles que são restritos a valores válidos.
  - A desabilitação de controles e itens de menu ao clicar resultaria em erro, desde que seja óbvio por que o item de controle ou de menu está desabilitado.
  - Fornecendo bons valores padrão.

**Incorreto:**

![captura de tela de caixa de texto com rótulo de volume do orador ](images/mess-error-image35.png)

Neste exemplo, uma caixa de texto irrestrita é usada para entrada restrita. Em vez disso, use um controle deslizante.

- **Use o tratamento de erros sem janela restrita (erros in-loco ou balões) para problemas de entrada de usuário contextual.**
- **Use balões para problemas de entrada do usuário de ponto único não crítico detectados em uma caixa de texto ou imediatamente depois que uma caixa de texto perde o foco.** Os [balões](https://msdn.microsoft.com/library/windows/desktop/aa511451.aspx) não exigem o espaço de tela disponível ou o layout dinâmico necessário para exibir mensagens in-loco. Exibir apenas um único balão de cada vez. Como o problema não é crítico, nenhum ícone de erro é necessário. Os balões desaparecem quando clicados, quando o problema é resolvido ou após um tempo limite.

![captura de tela da mensagem: caractere incorreto ](images/mess-error-image36.png)

Neste exemplo, um balão indica um problema de entrada enquanto ainda está no controle.

- **Use erros in-loco para detecção de erro atrasada,** geralmente erros encontrados ao clicar em um botão de confirmação. (Não use [erros](glossary.md) in-loco para as configurações que são confirmadas imediatamente.) Pode haver vários erros in-loco por vez. Use um texto normal e um ícone de erro de 16x16 pixels, colocando-os diretamente ao lado do problema sempre que possível. Os erros in-loco não desaparecem a menos que o usuário confirme e nenhum outro erro seja encontrado.

![captura de tela de mensagem: endereço de email incorreto ](images/mess-error-image37.png)

Neste exemplo, um erro in-loco é usado para um erro encontrado clicando no botão confirmar.

- **Use o tratamento de erro modal (caixas de diálogo de tarefas ou de mensagens) para todos os outros problemas,** incluindo erros que envolvem vários controles ou que são erros não-contextuais ou não de entrada encontrados ao clicar em um botão de confirmação.
- **Quando um problema de entrada do usuário é relatado, defina o foco de entrada para o primeiro controle com os dados incorretos.** Role o controle para a exibição, se necessário. Se o controle for uma caixa de texto, selecione todo o conteúdo. Deve ser sempre óbvio para que a mensagem de erro se refere.
- **Não limpe a entrada incorreta.** Em vez disso, deixe-o para que o usuário possa ver e corrigir o problema sem começar de novo.
  - **Exceção:** Apague as caixas de texto senha incorreta e PIN porque os usuários não podem corrigir a entrada mascarada com eficiência.

### <a name="troubleshooting"></a>Solução de problemas

- **Evite a criação de problemas de solução.** Não confie em uma única mensagem de erro para relatar um problema com várias causas detectáveis diferentes.
- **Use uma mensagem de erro diferente (normalmente uma instrução complementar diferente) para cada causa detectável.** Por exemplo, se um arquivo não puder ser aberto por vários motivos, forneça uma instrução complementar separada para cada motivo.
- **Use uma mensagem com várias causas somente quando a causa específica não puder ser determinada.** Nesse caso, apresente as soluções em ordem de probabilidade de corrigir o problema. Isso ajuda os usuários a resolver o problema com mais eficiência.

### <a name="icons"></a>Ícones

- **As caixas de diálogo de mensagem de erro modal não têm ícones de barra de título.** Os ícones da barra de título são usados como uma distinção visual entre janelas primárias e secundárias.
- **Use um ícone de erro.** Exceções:
  - Se o erro for um problema de entrada do usuário exibido usando uma caixa de diálogo modal ou um balão, não use um ícone. Fazer isso é um contador para o Tom incentivado do Windows. No entanto, as mensagens de erro in-loco devem usar um pequeno ícone de erro (16x16 pixels) para identificá-las claramente como mensagens de erro.

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

Esses termos são desnecessários e ao contrário do Tom incentivado do Windows. Quando [usado corretamente](vis-std-icons.md), o ícone de erro comunica suficientemente que há um problema.

**Incorreto:**

![captura de tela da mensagem: falha catastrófica! ](images/mess-error-image48.png)

**Correto:**

![captura de tela da mensagem: o backup deve fechar ao mesmo tempo ](images/mess-error-image49.png)

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

Aguarde enquanto o Windows copia os arquivos para o computador.

- **Use a palavra "Desculpa" somente em mensagens de erro que resultam em sérios problemas para o usuário** (por exemplo, perda de dados ou incapacidade de usar o computador). Não se esqueça de que o problema ocorreu durante o funcionamento normal do programa (por exemplo, se o usuário precisar aguardar uma conexão de rede ser encontrada).

**Correto:**

Infelizmente, o backup da Fabrikam detectou um problema irrecuperável e foi desligado para proteger os arquivos no computador.

- **Consulte os produtos usando seus nomes curtos.** Não use nomes completos de produtos ou símbolos de marcas. Não inclua o nome da empresa, a menos que os usuários associem o nome da empresa ao produto. Não inclua números de versão do programa.

**Incorreto:**

![Captura de tela que mostra uma mensagem Microsoft Office o Outlook "não é possível abrir este item". ](images/mess-error-image52.png)

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

Neste exemplo, o usuário está renomeando um arquivo do Windows Explorer. Nesse caso, o caminho completo do arquivo não é necessário porque é óbvio do contexto.

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
  - Forneça detalhes adicionais sobre o problema.
  - Explique a causa do problema.
  - Listar as etapas que o usuário pode executar para corrigir o problema.
  - Forneça medidas para evitar que o problema ocorra novamente.
- **Sempre que possível, proponha uma solução prática e útil para que os usuários possam corrigir o problema.** No entanto, certifique-se de que a solução proposta provavelmente resolverá o problema. Não gaste o tempo dos usuários sugerindo soluções possíveis, mas que podem ser investigadas.

**Incorreto:**

![captura de tela da mensagem: memória insuficiente ](images/mess-error-image59.png)

Neste exemplo, embora o problema e sua solução recomendada sejam possíveis, eles são muito improvável.

- **Se o problema for um valor incorreto que o usuário inseriu, use a instrução complementar para explicar os valores corretos.** Os usuários não devem ter que determinar essas informações de outra fonte.
- **Não forneça uma solução se ela puder ser deduzida trivialmente da declaração do problema.**

![captura de tela de mensagem: valor de tempo incorreto ](images/mess-error-image33.png)

Neste exemplo, nenhuma instrução suplementar é necessária; a solução pode ser deduzida trivialmente da declaração do problema.

- **Se a solução tiver várias etapas, apresente as etapas na ordem em que elas devem ser concluídas.** No entanto, evite soluções de várias etapas porque os usuários têm dificuldade em lembrar mais de duas ou três etapas simples. Se mais etapas forem necessárias, consulte o tópico da ajuda apropriado.
- **Mantenha as instruções suplementares concisas.** Forneça apenas o que os usuários precisam saber. Omita os detalhes desnecessários. Objetivo de um máximo de três frases de comprimento moderado.
- **Para evitar erros enquanto os usuários executam instruções, coloque os resultados antes da ação.**

**Correto:**

Para reiniciar o Windows, clique em OK.

**Incorreto:**

Clique em OK para reiniciar o Windows.

No exemplo incorreto, é mais provável que os usuários cliquem em OK por acidente.

- **Não recomende entrar em contato com um administrador, a menos que isso esteja entre as soluções mais prováveis para o problema.** Reserve essas soluções para problemas que realmente só podem ser resolvidos por um administrador.

**Incorreto:**

![captura de tela da mensagem: servidor não disponível ](images/mess-error-image60.png)

Neste exemplo, provavelmente o problema é com a conexão de rede do usuário, portanto, não vale a pena entrar em contato com um administrador.

- **Não recomende entrar em contato com o suporte técnico.** A opção de contatar o suporte técnico para resolver um problema está sempre disponível e não precisa ser promovida por meio de mensagens de erro. Em vez disso, concentre-se em escrever mensagens de erro úteis para que os usuários possam resolver problemas sem entrar em contato com o suporte técnico.

**Incorreto:**

![Captura de tela que mostra uma mensagem ' não é possível abrir este item '. ](images/mess-error-image61.png)

Neste exemplo, a mensagem de erro recomenda incorretamente entrar em contato com o suporte técnico.

- Use frases completas, maiúsculas e minúsculas no estilo da frase e pontuação final.

**Botões de confirmação**

- Se a mensagem de erro fornecer botões de comando ou links de comando que resolvem o problema, siga suas respectivas diretrizes nas [caixas de diálogo](win-dialog-box.md).
- Se o programa precisar ser encerrado como resultado do erro, forneça um botão de programa de saída. Para evitar confusão, não use fechar para essa finalidade.
- Caso contrário, forneça um botão fechar. Não use OK para mensagens de erro, pois essa palavra implica que problemas estão OK.
  - **Exceção:** Use OK se o mecanismo de relatório de erros tiver corrigido os rótulos (assim como ocorre com a API MessageBox).

## <a name="documentation"></a>Documentação

Ao fazer referência a erros:

- Consulte os erros por sua instrução principal. Se a instrução principal for longa ou detalhada, resuma-a.
- Se necessário, você pode consultar uma caixa de diálogo de mensagem de erro como uma mensagem. Consulte como uma mensagem de erro somente em programação e outras documentações técnicas.
- Quando possível, formate o texto usando negrito. Caso contrário, coloque o texto entre aspas somente se necessário para evitar confusão.

**Exemplo:** Se você receber um **disco de CD na mensagem da unidade** , insira um novo CD na unidade e tente novamente.