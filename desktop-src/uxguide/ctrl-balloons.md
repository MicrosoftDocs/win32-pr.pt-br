---
title: Balões
description: Um balão é uma pequena janela pop-up que informa os usuários de um problema não crítico ou uma condição especial em um controle.
ms.assetid: 67092831-e573-4ad6-b1fc-baa1836031cb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 348167594db2f7895e185d8d7761832ec5c0c1cb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104297861"
---
# <a name="balloons"></a>Balões

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Um balão é uma pequena janela pop-up que informa os usuários de um problema não crítico ou uma condição especial em um controle.

![Captura de tela que mostra um balão indicando que a tecla Caps Lock está ativada.](images/ctrl-balloons-image1.png)

Um balão típico.

Os balões têm um ícone, um título e um texto de corpo, todos opcionais. Ao contrário das dicas de ferramentas e infotips, os balões também têm uma cauda que identifica sua origem. Normalmente, a origem é um controle, se for, é chamada de [controle de proprietário](glossary.md).

Embora os balões informam os usuários sobre problemas não críticos, eles não impedem problemas, embora o controle de proprietário possa. Qualquer problema sem tratamento deve ser tratado pela interface do usuário do proprietário quando os usuários tentam confirmar a ação.

Os balões geralmente são usados com caixas de texto, ou controles que usam caixas de texto para alterar valores, como caixas de combinação, exibições de lista e exibições de árvore. Outros tipos de controles são bastante restritos e não precisam de balões de comentários adicionais. Além disso, se houver um problema com outros tipos de controles, isso geralmente envolve inconsistência entre vários controles uma situação para a qual os balões não são adequados. Somente controles de entrada de texto são irrestrito e uma fonte comum de erros de [ponto único](glossary.md).

Uma notificação é um tipo específico de balão exibido por um ícone da [área de notificação](winenv-notification.md) .

**Observação:** As diretrizes relacionadas a [notificações](mess-notif.md), [dicas de ferramentas e Infotips](ctrl-tooltips-and-infotips.md)e [mensagens de erro](mess-error.md) são apresentadas em artigos separados.

**Esse é o controle correto?**

Para decidir, considere estas perguntas:

-   **As informações descrevem um problema ou uma condição especial?** Se não, use outro controle. Não use balões para exibir informações complementares de um controle; Considere o uso de [texto estático](glossary.md),[Infotips](glossary.md), [divulgação progressiva](glossary.md)ou prompts.
-   **O problema ou a condição especial podem ser detectados imediatamente** na entrada ou quando o controle de proprietário perde o foco de entrada? Caso contrário, use uma mensagem de erro exibida em uma caixa de [diálogo de tarefa](glossary.md) ou de [mensagem](glossary.md).
-   **Para problemas, o problema é crítico?** Nesse caso, use uma mensagem de erro exibida em uma caixa de diálogo de tarefa ou de mensagem. Essas mensagens de erro exigem interação (que é adequada para erros críticos), enquanto os balões não.
-   **Para condições especiais, a condição válida ainda é provavelmente indesejada?** Nesse caso, os balões são apropriados. Para condições não válidas, é melhor impedi-las em primeiro lugar. Para condições pretendidas prováveis, não há necessidade de fazer nada.
-   **O problema ou a condição especial pode ser expressa de forma concisa?** Se não, use outro controle. Os balões não podem ter explicações detalhadas ou fornecer informações complementares.
-   **As informações descrevem o controle que está sendo focalizado no momento?** Nesse caso, use uma dica em vez disso, a menos que os usuários precisem interagir com a mensagem.
-   **As informações estão relacionadas à atividade atual do usuário?** Caso contrário, considere usar uma [notificação](mess-notif.md) ou [caixa de diálogo](win-dialog-box.md) em vez disso. Os usuários provavelmente esquecerão os balões fora da atividade atual e, por padrão, os balões atingirão o tempo limite após 10 segundos.
-   **As informações são provenientes de uma fonte única e específica?** Se um problema ou condição tiver várias fontes ou nenhuma fonte específica, use uma [mensagem](glossary.md) in-loco ou uma caixa de diálogo em vez disso.

**Incorreto:** ![ captura de tela de um balão: logon malsucedido](images/ctrl-balloons-image2.png)

Neste exemplo, o problema pode ser com o nome de usuário ou a senha, mas relatar o problema com um balão sugere visualmente que apenas a senha é o problema. Consequentemente, os comentários de inserir um nome de usuário incorreto é enganoso.

Os balões são uma alternativa para infotips, caixas de diálogo e mensagens in-loco. Em contraste com tooltips e Infotips:

-   Os balões podem ser exibidos independentemente do local do ponteiro atual, portanto, eles têm uma cauda que indica sua origem.
-   Os balões têm um título, corpo de texto e um ícone.
-   Os balões podem ser interativos, enquanto é impossível clicar em uma dica.

Em contraste com as caixas de diálogo modais:

-   Os balões não roubam o foco de entrada nem exigem interação.
-   Os balões identificam uma única fonte específica. Caixas de diálogo modais podem ter várias fontes ou nenhuma fonte específica.

Em contraste com as mensagens in-loco:

-   Os balões são mais perceptíveis.
-   Os balões não exigem o espaço de tela disponível ou o layout dinâmico necessário para exibir mensagens in-loco.
-   Os balões são removidos automaticamente após um tempo limite.

**Padrões de uso**

Os balões têm estes padrões de uso:



|                                                                                                                                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Problema de entrada** Um problema de entrada de usuário não crítico proveniente de um único controle de proprietário, geralmente uma caixa de texto. <br/>                                               | o uso de balões para mensagens de erro não rouba o foco de entrada, mas ainda é muito perceptível se o controle de proprietário tem o foco de entrada. para corrigir o problema, o usuário pode precisar alterar ou reinserir a entrada; Mas se o controle de proprietário ignorar a entrada incorreta, talvez o usuário não precise fazer nenhuma alteração. como o problema não é crítico, nenhum [ícone de erro](vis-std-icons.md) é necessário. <br/> ![Captura de tela que mostra um balão que indica um caractere incorreto.](images/ctrl-balloons-image3.png)<br/> Um balão usado para relatar um problema de entrada não crítico do usuário.<br/>                                                                                                  |
| **Condição especial** O controle de proprietário está em um estado que afeta a entrada. Esse Estado provavelmente não é intencional e o usuário pode não perceber que a entrada é afetada. <br/> | Use balões para evitar frustração alertando os usuários de condições especiais assim que eles ocorrerem (por exemplo, excedendo o tamanho máximo de entrada ou definindo Caps Lock por engano). é importante fornecer esses comentários sem roubar o foco de entrada ou forçar a interação, pois essas condições podem ser intencionais. Esses balões são especialmente importantes para as caixas senha e PIN, em que os usuários estão trabalhando com comentários mínimos. Esses balões têm um [ícone de aviso](vis-std-icons.md). <br/> ![Captura de tela que mostra os balões indicando que Caps Lock está ativado e um caractere incorreto é inserido.](images/ctrl-balloons-image4.png)<br/> Um balão usado para relatar uma condição especial.<br/> |



 

**Diretrizes**

**Quando exibir**

-   **Exiba o balão assim que o problema ou a condição especial for detectada, mesmo se repetidamente, sem nenhum atraso perceptível.**
    -   Para problemas que envolvem caracteres individuais ou o tamanho máximo de entrada, exiba o balão imediatamente na entrada.
    -   Para problemas envolvendo o valor de entrada (incluindo a necessidade de um valor não em branco), exiba o balão quando o controle de proprietário perder o foco de entrada. Caso contrário, exibir balões enquanto os usuários estão inserindo uma entrada potencialmente válida pode ser confuso e irritante.
-   **Exibir apenas um balão de cada vez.** A exibição de vários balões pode ser impressionante. Se um único evento resultar em vários problemas, apresente todos os problemas de uma vez ou relate apenas o problema mais importante.

**Incorreto:** ![ captura de tela de dois balões apontando para uma caixa](images/ctrl-balloons-image5.png)

Neste exemplo, dois problemas são apresentados incorretamente ao mesmo tempo.

**Por quanto tempo exibir**

-   **Remover um balão quando:**
    -   O problema foi resolvido ou a condição especial foi removida.
    -   O usuário insere dados válidos (para problemas de entrada).
    -   O balão atinge o tempo limite. Por padrão, os balões se removem após 10 segundos, embora os usuários possam alterar isso modificando o \_ parâmetro de sistema SPI MESSAGEDURATION.
-   **Remova o tempo limite se os usuários não puderem continuar até que o problema seja resolvido. Desenvolvedores:** no Win32, você pode definir a hora de exibição com a \_ mensagem TTM SetDelayTime.

**Como exibir**

-   **Exibir balões abaixo de seu controle de proprietário.** Isso permite que os usuários exibam o contexto, incluindo o controle de proprietário e seu rótulo. O Microsoft Windows ajusta automaticamente as posições de balão para que elas estejam completamente na tela. O comportamento padrão é exibir um balão acima de seu controle de proprietário, como feito com notificações.

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

-   **Explique como resolver o problema ou reverter o estado mesmo que essa explicação seja óbvia,** mas omita a redundância entre a declaração do problema e sua resolução. **Exceção**
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

