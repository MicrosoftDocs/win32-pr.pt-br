---
title: Balões
description: Um balão é uma pequena janela pop-up que informa os usuários sobre um problema não crítico ou uma condição especial em um controle.
ms.assetid: 67092831-e573-4ad6-b1fc-baa1836031cb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 792974ebaaa946a3e1a4f05d52c8fd9ac32fc87a
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524550"
---
# <a name="balloons"></a>Balões

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Um balão é uma pequena janela pop-up que informa os usuários sobre um problema não crítico ou uma condição especial em um controle.

![Captura de tela que mostra um balão indicando que Caps Lock está.](images/ctrl-balloons-image1.png)

Um balão típico.

Os balão têm um ícone, um título e um texto do corpo, que são opcionais. Ao contrário de dicas de ferramenta e infotips, os balão também têm uma cauda que identifica sua origem. Normalmente, a origem é um controle, se for o caso, ele é chamado de controle [de proprietário](glossary.md).

Embora os balão informem os usuários sobre problemas não críticos, eles não impedem problemas, embora o controle de proprietário possa. Todos os problemas sem manipulação devem ser tratados pela interface do usuário do proprietário quando os usuários tentam se comprometer com a ação.

Os balão geralmente são usados com caixas de texto ou controles que usam caixas de texto para alterar valores, como caixas de combinação, exibições de lista e exibições de árvore. Outros tipos de controles são suficientemente restritos e não precisam dos balão de comentários adicionais. Além disso, se houver um problema com outros tipos de controles, isso geralmente envolverá inconsistência entre vários controles, uma situação para a qual os balão não são adequados. Somente controles de entrada de texto não são restritos e uma fonte comum de [erros de ponto único.](glossary.md)

Uma notificação é um tipo específico de balão exibido por um ícone de área [de](winenv-notification.md) notificação.

**Observação:** Diretrizes [relacionadas a notificações,](mess-notif.md)dicas de ferramenta e [infotips](ctrl-tooltips-and-infotips.md)e mensagens [de](mess-error.md) erro são apresentadas em artigos separados.

**Esse é o controle correto?**

Para decidir, considere estas perguntas:

-   **As informações descrevem um problema ou condição especial?** Se não, use outro controle. Não use balão para exibir informações complementares para um controle; considere usar [texto estático,](glossary.md)[infotips,](glossary.md) [divulgação progressiva](glossary.md)ou prompts.
-   **O problema ou condição especial pode ser detectado imediatamente** na entrada ou quando o controle de proprietário perde o foco de entrada? Caso não, use uma mensagem de erro exibida em uma caixa [de diálogo de tarefa](glossary.md) ou caixa de [mensagem](glossary.md).
-   **Para problemas, o problema é crítico?** Nesse caso, use uma mensagem de erro exibida em uma caixa de diálogo de tarefa ou caixa de mensagem. Essas mensagens de erro exigem interação (que é adequada para erros críticos), enquanto os balão não.
-   **Para condições especiais, a condição ainda é válida e provavelmente não é intencional?** Em caso afirmaível, os balão são apropriados. Para condições não válidas, é melhor impedi-las em primeiro lugar. Para condições prováveis pretendido, não há necessidade de fazer nada.
-   **O problema ou a condição especial pode ser expresso de forma concisa?** Se não, use outro controle. Os balão não podem ter explicações detalhadas nem fornecer informações complementares.
-   **As informações descrevem o controle que está sendo passar o mouse no momento?** Em caso afirmativos, use uma dica, a menos que os usuários precisem interagir com a mensagem.
-   **As informações estão relacionadas à atividade atual do usuário?** Caso contrário, considere usar uma [notificação ou](mess-notif.md) [caixa de diálogo.](win-dialog-box.md) Os usuários provavelmente ignorarão os balão fora da atividade atual e, por padrão, os balão passarão do tempo após 10 segundos.
-   **As informações vêm de uma única origem específica?** Se um problema ou condição tiver várias fontes ou nenhuma fonte específica, use uma [mensagem in-locar](glossary.md) ou uma caixa de diálogo.

**Incorreto:** ![ captura de tela de um balão: logon malsucedido](images/ctrl-balloons-image2.png)

Neste exemplo, o problema pode ser com o nome de usuário ou a senha, mas relatar o problema com um balão sugere visualmente que apenas a senha é o problema. Consequentemente, os comentários de inserir um nome de usuário incorreto são enganoso.

Os balão são uma alternativa a infotips, caixas de diálogo e mensagens in-locar. Em contraste com dicas de ferramenta e infotips:

-   Os balão podem ser exibidos independentemente do local do ponteiro atual, portanto, eles têm uma cauda que indica sua origem.
-   Os balão têm um título, texto do corpo e um ícone.
-   Os balão podem ser interativos, enquanto é impossível clicar em uma gorjeta.

Ao contrário das caixas de diálogo modais:

-   Os balão não roubarão o foco de entrada nem exigirão interação.
-   Os balão identificam uma única origem específica. Os diálogos modais podem ter várias fontes ou nenhuma fonte específica.

Ao contrário das mensagens in-locar:

-   Os balão são mais perceptíveis.
-   Os balão não exigem espaço na tela disponível ou o layout dinâmico necessário para exibir mensagens in-locar.
-   Os balão são removidos automaticamente após um tempo-fim.

**Padrões de uso**

Os balão têm estes padrões de uso:



|   Uso                                                                                                                                                            |    Exemplo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Problema de entrada** Um problema de entrada de usuário não crítico proveniente de um único controle de proprietário, geralmente uma caixa de texto. <br/>                                               | O uso de balão para mensagens de erro não roubará o foco de entrada, mas ainda será muito perceptível se o controle de proprietário tiver o foco de entrada. para corrigir o problema, o usuário pode ter que alterar ou inserir novamente a entrada; mas se o controle de proprietário ignorar a entrada incorreta, o usuário poderá não ter que fazer nenhuma alteração. como o problema não é crítico, nenhum [ícone de erro](vis-std-icons.md) é necessário. <br/> ![Captura de tela que mostra um balão indicando um caractere incorreto.](images/ctrl-balloons-image3.png)<br/> Um balão usado para relatar um problema de entrada do usuário não crítico.<br/>                                                                                                  |
| **Condição especial** O controle de proprietário está em um estado que afeta a entrada. Esse estado provavelmente não é intencional e o usuário pode não perceber que a entrada é afetada. <br/> | use os balão para evitar frustração alertando os usuários de condições especiais assim que elas ocorrerem (por exemplo, excedendo o tamanho máximo de entrada ou definindo o bloqueio de limites por engano). É importante dar esses comentários sem roubar o foco de entrada ou forçar a interação porque essas condições podem ser intencionais. esses balão são especialmente importantes para caixas de senha e pino, em que os usuários estão trabalhando com comentários mínimos. esses balão têm um ícone [de aviso](vis-std-icons.md). <br/> ![Captura de tela que mostra os balão indicando que Caps Lock está em e um caractere incorreto é inserido.](images/ctrl-balloons-image4.png)<br/> Um balão usado para relatar uma condição especial.<br/> |



 

**Diretrizes**

**Quando exibir**

-   **Exibir o balão assim que o problema ou condição especial for detectado, mesmo que repetidamente, sem nenhum atraso perceptível.**
    -   Para problemas envolvendo caracteres individuais ou o tamanho máximo de entrada, exinte o balão imediatamente na entrada.
    -   Para problemas que envolvem o valor de entrada (incluindo a necessidade de um valor não em branco), exibe o balão quando o controle de proprietário perde o foco de entrada. Caso contrário, exibir os balão enquanto os usuários estão inserindo uma entrada potencialmente válida pode ser uma distração e uma chatice.
-   **Exibe apenas um balão por vez.** Exibir vários balão pode ser difícil. Se um único evento resulta em vários problemas, apresente todos os problemas de uma vez ou reporte apenas o problema mais importante.

**Incorreto:** ![ captura de tela de dois balão apontando para uma caixa](images/ctrl-balloons-image5.png)

Neste exemplo, dois problemas são apresentados incorretamente ao mesmo tempo.

**Por quanto tempo exibir**

-   **Remova um balão quando:**
    -   O problema é resolvido ou a condição especial é removida.
    -   O usuário ins insira dados válidos (para problemas de entrada).
    -   O balão tem tempo de vida. Por padrão, os balão se removem após 10 segundos, embora os usuários possam alterar isso modificando o parâmetro do sistema SPI \_ MESSAGEDURATION.
-   **Remova o tempo de vida se os usuários não puderem continuar até que o problema seja resolvido. Desenvolvedores:** no Win32, você pode definir a hora de exibição com a mensagem \_ TTM SETDELAYTIME.

**Como exibir**

-   **Exibir balão abaixo de seu controle de proprietário.** Isso permite que os usuários vejam o contexto, incluindo o controle de proprietário e seu rótulo. O Microsoft Windows ajusta automaticamente as posições de balão para que elas sejam completamente na tela. O comportamento padrão é exibir um balão acima de seu controle de proprietário, conforme feito com notificações.

**Correto:** ![ captura de tela de um balão exibido abaixo de seu controle](images/ctrl-balloons-image6.png)

**Incorreto:** ![ captura de tela de um balão exibido acima de seu controle](images/ctrl-balloons-image7.png)

No exemplo incorreto, o balão é exibido inadequadamente acima de seu controle de proprietário.

**Caixas de texto de senha e PIN**

-   **Use um balão para indicar que Caps Lock está ativado**, usando o texto no exemplo a seguir:

![captura de tela de um balão que indica que Caps Lock está ativado](images/ctrl-balloons-image8.png)

Neste exemplo, um balão indica que Caps Lock está ativado em uma caixa de texto de PIN.

-   **Use um balão para indicar quando os usuários tentam exceder o tamanho máximo de entrada.** Atingir o tamanho máximo de entrada é muito menos óbvio em caixas de texto de senha e PIN do que as caixas de texto comuns.

![captura de tela de um balão que indica limites de código PIN](images/ctrl-balloons-image9.png)

Neste exemplo, um balão indica que o usuário está tentando exceder o tamanho máximo de entrada.

-   **Use um balão para indicar quando os usuários inserim caracteres incorretos.** No entanto, é melhor não ter essas restrições porque reduzem a segurança da senha ou do PIN. Para evitar a divulgação de informações, o balão deve mencionar apenas os fatos documentados sobre senhas ou PINs válidos.

![captura de tela de um balão que indica entrada incorreta](images/ctrl-balloons-image10.png)

Neste exemplo, um balão indica que o PIN requer números.

**Outras caixas de texto**

-   **Considere usar um balão para indicar quando os usuários tentam exceder o tamanho máximo de entrada para caixas de texto curtas e críticas direcionadas a usuários iniciantes.** Os exemplos incluem nomes de usuário e nomes de conta. As caixas de texto são emitidas quando os usuários tentam exceder a entrada máxima, mas os usuários iniciantes podem não entender o significado do aviso sonoro.

![captura de tela de um balão que indica limites de caracteres](images/ctrl-balloons-image11.png)

Neste exemplo, um balão indica que o usuário tentou exceder o tamanho máximo de entrada.

**Interação**

-   **Quando os usuários clicam em um balão, apenas descartam o balão sem exibir nenhuma outra interface do usuário ou ter qualquer outro efeito colateral.** Ao contrário das notificações, os balões não devem ter botões de fechamento.

**Ícones**

-   Escolha o ícone com base no padrão de uso:



    |  Padrão |  ícone                                                                                                                                                       |
    ------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Problema de entrada | Nenhum ícone. Não usar um [ícone de erro](vis-std-icons.md) aqui é consistente com as diretrizes de [Tom do Windows](text-style-tone.md) . |
    | Condição especial | O [ícone de aviso](vis-std-icons.md)de 16x16 pixel padrão.                                                                                  |

**Acessibilidade**

Quando usado corretamente, os balões aprimoram a acessibilidade. Para que os balões sejam acessíveis:

-   Exiba somente os balões relacionados à atividade atual do usuário.
-   Mantenha o texto de balão conciso. Isso torna o texto do balão mais fácil de ler para os usuários com pouca visão e minimiza a interrupção quando lida por leitores de tela.
-   Exibir novamente o balão sempre que o problema ou condição ocorrer.

**Text**

**Texto do título**

-   **Use o texto do título que resume brevemente o problema de entrada ou a condição especial em linguagem clara, simples, concisa e específica.** Os usuários devem ser capazes de entender a finalidade do balão rapidamente e com um mínimo de esforço.
-   **Use fragmentos de texto ou frases completas sem pontuação final.**
-   **Use a capitalização com estilo de frase.** Para obter mais informações, consulte o [Glossário](./glossary.md).
-   **Use no máximo 48 caracteres (em inglês) para acomodar a localização.** O título tem um comprimento máximo de 63 caracteres e deve ser capaz de expandir por pelo menos 30 por cento para acomodar a localização.

**Texto do corpo**

-   **Use a primeira frase do texto do corpo para declarar o problema ou a condição de uma maneira que seja claramente relevante para o usuário.** Não repita as informações no título. Omita isso se não houver nada mais a ser adicionado.
-   **Use a segunda frase para declarar o que o usuário pode fazer para resolver o problema ou reverter o estado.** De acordo com as diretrizes de [estilo e Tom](./text-style-tone.md) , não há necessidade de usar a palavra nesta declaração. Coloque duas quebras de linha entre a primeira e a segunda sentenças.

![captura de tela de um balão com título e corpo de texto](images/ctrl-balloons-image12.png)

Este exemplo mostra o layout de texto de balão padrão.

-   **Explique como resolver o problema ou reverter o estado mesmo que essa explicação seja óbvia,** mas omita a redundância entre a declaração do problema e sua resolução. **Exceções:**
    -   Omita a resolução se ela não puder ser expressa de forma concisa ou sem redundância significativa.
    -   Omita a resolução se não houver nada para o usuário fazer, como quando caracteres incorretos são ignorados.
-   **Use frases completas com pontuação final.**
-   **Use a capitalização com estilo de frase.**
-   **Use no máximo 200 caracteres (em inglês) para acomodar a localização.** O texto do corpo tem um comprimento máximo de 255 caracteres e deve ser capaz de expandir por pelo menos 30 por cento para acomodar a localização.

**Documentação**

Ao fazer referência a balões:

-   Use o texto do título exato, incluindo sua capitalização.
-   Consulte o componente como um balão, não como uma notificação ou um alerta.
-   Quando possível, formate o texto do título usando texto em negrito. Caso contrário, coloque o título entre aspas somente se necessário para evitar confusão.

