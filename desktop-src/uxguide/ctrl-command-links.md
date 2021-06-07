---
title: Links de comando
description: Com links de comando, os usuários selecionam uma única resposta para uma instrução principal e, fazendo isso, vá para a próxima etapa em uma tarefa.
ms.assetid: a77819b1-9a32-4468-94fb-3f73a469fb81
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b579f554d46d48fd7e373d28df516ae1c0baca6a
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524270"
---
# <a name="command-links"></a>Links de comando

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Com links de comando, os usuários selecionam uma única resposta para uma instrução principal e, fazendo isso, vá para a próxima etapa em uma tarefa.

Os links de comando têm uma aparência limpa e leve que permite rótulos descritivos e são exibidos com uma seta padrão ou um ícone personalizado e uma explicação complementar opcional.

![captura de tela de uma caixa de diálogo típica de link de comando ](images/ctrl-command-links-image1.png)

Um conjunto típico de links de comando.

Os links de comando são [semelhantes](ctrl-radio-buttons.md) aos botões de opção, já que eles são usados para selecionar de um conjunto de opções mutuamente exclusivas e relacionadas. Assim como os botões de rádio, os links de comando sempre são apresentados em conjuntos, nunca individualmente. Na aparência, os links de comando têm a aparência leve semelhante aos [links regulares,](ctrl-links.md)sem um quadro ou outra aparência de clique [forte.](glossary.md) Os links de comando também são [semelhantes](ctrl-command-buttons.md)aos botões de comando , pois eles podem ser o "botão de comando" padrão e podem ter uma chave de acesso atribuída. Assim [como os botões de](glossary.md)confirmação , ao clicar, eles fecham a janela (para caixas de diálogo) ou avançam para a próxima página (para fluxos de assistentes e páginas).

> [!Note]  
> Diretrizes relacionadas [a links](ctrl-links.md) [e layout](vis-layout.md) são apresentadas em artigos separados.

 

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

Para decidir, considere estas perguntas:

-   **As opções são respostas à instrução principal e relacionadas à finalidade principal da janela ou da página?** Os usuários devem responder a eles para fazer algo diferente de apenas navegar para uma página diferente? Caso não, use outro controle, como botões de comando ou links. Links de comando não são apropriados para opções secundárias ou opcionais ou navegação pura.

    ![captura de tela de um item do painel de controle de personalização ](images/ctrl-command-links-image2.png)

    Embora o item Painel de Controle personalização pareça estar usando links de comando, as opções são links regulares, pois essa página do [hub](winenv-ctrl-panels.md) é para navegação pura.

-   **O controle é usado para escolher uma resposta de um conjunto de respostas mutuamente exclusivas?** Se não, use outro controle. Para permitir que os usuários escolham comandos individuais, use botões de comando ou links.
-   **Para caixas de diálogo, clicar no controle fecha a janela?** Caso não, use um controle que não exige o fechamento da janela, como botões de rádio, botões de comando ou links.

    **Incorreto:**

    ![captura de tela da caixa de diálogo configurações de firewall com guias ](images/ctrl-command-links-image3.png)

    Links de comando não podem ser usados em janelas de propriedades ou caixas de diálogo com guias porque clicar no controle fecha a janela.

-   **Para assistentes e fluxos de página, o clique avança para a próxima página sem compromisso?** Não use links de comando para fazer commit de uma tarefa; em vez disso, use botões de commit. Como os links de comando se parecem com links e os usuários [](glossary.md) associam links à navegação dentro de um fluxo de página, os links não são apropriados para páginas de commit porque os usuários sempre devem ser capazes de fazer o back-out.
-   **Para assistentes e fluxos de página, outras páginas estão usando links de comando?** Se sim, e todos os outros fatores serem iguais, prefira links de comando para consistência entre páginas.
-   **O número de respostas entre dois e cinco?** Nunca deve haver um único link de comando. Como os links de comando são controles grandes e o espaço de tela usado é proporcional ao número de opções, mantenha o número de respostas para cinco ou menos. Para seis ou mais opções, use botões de opção, links regulares ou uma exibição de lista [de seleção única](ctrl-list-views.md).

    ![captura de tela da caixa de diálogo com a lista de comandos ](images/ctrl-command-links-image4.png)

    Neste exemplo, o recurso Reprodução Automática no Microsoft Windows usa uma exibição de lista.

-   **Uma combinação de botões de opção e um botão de commit seria uma opção melhor?** Os botões de opção são uma opção melhor quando qualquer um dos seguintes é verdadeiro:
    -   **Há uma opção padrão forte que você deseja que a maioria dos usuários selecione.** Os usuários têm menos probabilidade de alterar um botão de opção padrão do que um link de comando padrão, especialmente em um assistente, em que os usuários estão acostumados a clicar em Próximo para aceitar os padrões apropriados. Por outro lado, os links de comando são uma opção melhor se você quiser incentivar os usuários a fazer uma escolha explícita.
    -   **Os usuários precisam interagir com as opções (talvez para ver informações adicionais) antes de tomar uma decisão.** Por exemplo, selecionar um botão de opção pode exibir uma descrição sobre a opção dinamicamente.

        ![captura de tela da caixa de diálogo com botões de rádio ](images/ctrl-command-links-image5.png)

        Neste exemplo, selecionar um botão de opção exibe uma descrição da opção.

    -   **Há opções secundárias ou relacionadas na página.** Os links de comando tendem a dominar a página, tornando mais fácil ignorar todo o resto. Além disso, depois que um link de comando é clicado, é impossível selecionar opções secundárias.

        **Incorreto:**

        ![captura de tela da caixa de diálogo com controles mistos ](images/ctrl-command-links-image6.png)

        Neste exemplo, há duas maneiras diferentes de responder à instrução principal. Um link de comando não foi usado para a primeira resposta porque seria difícil selecionar opções secundárias.

        **Correto:**

        ![captura de tela da caixa de diálogo com os mesmos controles ](images/ctrl-command-links-image7.png)

        Neste exemplo, os botões de opção limpam as respostas, permitindo que os usuários selecionem opções secundárias.

-   **Para caixas de diálogo, um grupo de botões de commit seria uma opção melhor?** Os links de comando funcionam melhor quando as opções exigem respostas mais longas, mais explicativas e explicações complementares, mas um grupo de botões de confirmação é uma opção melhor se houver algumas opções simples.

    **Incorreto:**

    ![captura de tela da caixa de diálogo com salvar e não salvar ](images/ctrl-command-links-image8.png)

    Neste exemplo, o uso de links de comando para comandos simples torna a caixa de diálogo desnecessariamente complicada.

    **Correto:**

    ![Captura de tela que mostra uma caixa de diálogo com os botões de commit "Salvar", "Não salvar" e "Cancelar".](images/ctrl-command-links-image9.png)

    Neste exemplo, o uso de botões de confirmação simples chega ao ponto.

    No entanto, os links de comando autoexplicativos são sempre melhores quando o texto é usado para explicar os botões de commit.

    **Incorreto:**

    ![captura de tela da caixa de diálogo com texto desnecessário ](images/ctrl-command-links-image10.png)

    Neste exemplo, o texto é usado para explicar os botões de confirmação.

    **Correto:**

    ![captura de tela de rótulos que não precisam de mais texto ](images/ctrl-command-links-image11.png)

    Neste exemplo, os links de comando são autoexplicativos.

> [!Note]  
> Os links de comando exigem o Windows Vista ou posterior, portanto, eles não são adequados para versões anteriores do Windows. Você pode usar links regulares como um substituto.

 

![captura de tela de links regulares com ícones e texto ](images/ctrl-command-links-image12.png)

Neste exemplo, links regulares com um ícone e uma explicação complementar são usados como um substituto para links de comando no Windows XP.

## <a name="design-concepts"></a>Conceitos de design

Apenas porque os links de comando permitem que você use rótulos mais descritivos e explicações complementares opcionais não significa que você deve. Considere o seguinte exemplo:

**Incorreto:**

![captura de tela da caixa de diálogo com muito texto ](images/ctrl-command-links-image13.png)

Essa caixa de diálogo está se comunicando muito.

Essa caixa de diálogo faz uma pergunta simples e complica-a desnecessariamente com o texto do link de comando. Os usuários não querem ler todo esse texto para perguntas simples.

Podemos simplificar essa caixa de diálogo aplicando três diretrizes de link de comando:

-   **Não use uma explicação complementar que seja uma restatementação wordy do link de comando.** Use uma explicação complementar somente quando não for possível tornar um link de comando autoexplicativo. Fornecer uma explicação complementar para um link de comando não significa que você precisa forenciá-los para todos os comandos.
-   **Selecione o mais seguro (para evitar a perda de dados ou acesso ao sistema) e a resposta mais segura seja o padrão.** Se segurança e segurança não são fatores, selecione a resposta mais provável ou conveniente.
-   **Forneça um botão Cancelar explícito.** Não use um link de comando para essa finalidade.

Aplicando essas diretrizes, podemos eliminar as explicações complementares desnecessárias, tornar a resposta mais conveniente o padrão e fornecer um botão Cancelar explícito.

**Melhor:**

![captura de tela da caixa de diálogo com comandos e rótulos ](images/ctrl-command-links-image14.png)

Uma versão aprimorada com links de comando mais simples.

Embora seja verdade que essa versão não explique explicitamente que não salvar é contado como uma perda, poucos usuários mudarão sua decisão com base nessas informações, fazendo com que isso seja uma boa desvantagem.

Essa caixa de diálogo poderia se tornar ainda melhor analisando se os links de comando são nem mesmo o controle certo para usar nesse caso. Os botões de confirmação são, na verdade, uma opção melhor, pois as respostas mais explicativas não são necessárias.

**Recomendá**

![captura de tela da caixa de diálogo com botões de confirmação ](images/ctrl-command-links-image15.png)

A versão correta usa botões de confirmação para chegar diretamente ao ponto.

Os links de comando têm muitas vantagens, mas quando usados sem sabedoria, eles levam à comunicação excessiva. Para caixas de diálogo, considere o uso de botões de confirmação primeiro e use links de comando somente se os botões de confirmação não fizerem o trabalho bem.

**Quando usado adequadamente, os links de comando devem simplificar e esclarecer sua interface do usuário.** Se os resultados forem os opostos, volte um pouco, examine as alternativas e concentre-se no que realmente precisa se comunicar.

**Se você fizer apenas uma coisa...** Não use links de comando para comunicação excessiva. Os links de comando devem simplificar e esclarecer a comunicação, não torná-la mais complicada.

## <a name="usage-patterns"></a>Padrões de uso

Os links de comando têm vários padrões de uso:



| Uso                                                                                                                      | Exemplo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Respostas de página** Os links de comando são usados para responder à instrução principal e avançar para a próxima página.    | com esse padrão, os links de comando substituem o botão Avançar, mas ainda há um botão Cancelar.<br/>As respostas de página não implicam em compromisso. como links de comando parecem links e os usuários associam links a navegação em um fluxo de página, os links não são apropriados para páginas de confirmação. os usuários sempre devem ser capazes de fazer backup. <br/> ![Captura de tela que mostra uma caixa de diálogo ' conectar à Internet ' com os links de comando ' sem fio, ' de banda larga (PPPoE) ' e ' dial-up '.](images/ctrl-command-links-image16.png)<br/>Neste exemplo, os links de comando são usados para fornecer respostas descritivas à instrução principal. Embora os botões de opção possam ser usados aqui, os links de comando permitem que os usuários respondam com um único clique.<br/> |
| **Respostas da caixa de diálogo** Os links de comando são usados para responder à instrução principal e fechar a caixa de diálogo.  | com esse padrão, os links de comando substituem os botões de confirmação (como ok), mas ainda há um botão Cancelar.<br/>Ao contrário dos fluxos de página, não há nenhuma maneira de sair de uma resposta baseada na caixa de diálogo quando ela tiver sido feita. Consequentemente, os links de comando da caixa de diálogo implicam em compromisso. <br/> ![captura de tela da caixa de diálogo com links de comando ](images/ctrl-command-links-image17.png)<br/>Neste exemplo, os links de comando são usados para fornecer respostas descritivas à instrução principal. Embora os botões de opção possam ser usados aqui, os links de comando permitem que os usuários escolham com um único clique.<br/>                                                   |
| **Respostas detalhadas** Uma resposta de página ou de caixa de diálogo que inclui informações detalhadas.                          | na ocasião, os usuários podem precisar de informações mais detalhadas para escolher sua resposta. <br/> ![captura de tela da caixa de diálogo e miniaturas do arquivo de cópia ](images/ctrl-command-links-image18.png)<br/> Neste exemplo, os links de comando detalhados são usados para que os usuários possam tomar decisões informadas. As miniaturas e os detalhes do arquivo ajudam os usuários a decidir.<br/>                                                                                                                                                                                                                                                                                                         |



 

## <a name="guidelines"></a>Diretrizes

### <a name="interaction"></a>Interação

-   **Exibir um ponteiro ocupado se o resultado de clicar em um link de comando não for instantâneo.** Sem comentários, os usuários podem assumir que o clique não aconteceu e clicar novamente.

### <a name="presentation"></a>Apresentação

-   **Sempre apresente links de comando em um conjunto de dois ou mais.** Logicamente, não há motivo para fazer uma pergunta que tenha apenas uma resposta.

    **Incorreto:**

    ![captura de tela da caixa de diálogo com um link de comando ](images/ctrl-command-links-image19.png)

    Neste exemplo, a caixa de diálogo parece estar oferecendo o usuário a uma escolha, mas há apenas uma instrução. Em vez disso, deve ser uma caixa de diálogo informativa.

-   **Apresente os links de comando mais comumente usados primeiro.** A ordem resultante deve seguir aproximadamente a probabilidade de uso, mas também ter um fluxo lógico.
    -   **Exceção:** Links de comando que resultam em fazer tudo devem ser colocados primeiro.
-   **Forneça um botão de cancelamento explícito.** Não use um link de comando para essa finalidade. Com muita frequência, os usuários percebem que não querem executar uma tarefa. Usar um link de comando para cancelar exigiria que os usuários leiam todos os links de comandos com cuidado para determinar qual deles significa cancelar. Ter um botão de cancelamento explícito permite que os usuários cancelem uma tarefa com eficiência.

    **Incorreto:**

    ![captura de tela da caixa de diálogo com o link ' não sair ' ](images/ctrl-command-links-image20.png)

    Neste exemplo, o link de comando não sair deve ser um botão Cancelar.

-   **Se fornecer um botão de cancelamento explícito deixar um único link de comando, forneça um link de comando para cancelar e um botão de cancelamento.** Isso torna claro que os usuários têm uma opção. Frase este link de comando em termos de como ele difere da primeira resposta, em vez de apenas "Cancelar" ou de alguma variação.

    ![captura de tela de dois links e um botão de cancelamento ](images/ctrl-command-links-image21.png)

    Neste exemplo, o segundo link de comando indica que o usuário tem uma opção, mas tudo o que ele faz é cancelar. No entanto, ela é fraseada em termos de como ela difere do primeiro link de comando.

-   **Use fechar em vez de cancelar se não for possível retornar o ambiente para seu estado anterior, não deixando nenhum efeito colateral.**
-   **Não exibir links de comando desabilitados.** Se um link de comando não se aplicar ao contexto atual, remova-o em vez disso. Se a remoção de todos os links de comando que não se aplicam sair de um único link de comando, elimine a janela ou a página ou exiba uma [confirmação](mess-confirm.md) se o consentimento explícito do usuário for necessário.

### <a name="icons"></a>Ícones

-   **Todos os links de comando precisam de um ícone.** Os ícones ajudam os usuários a distinguir links de comando de links regulares e texto de interface do usuário.
-   **Use o ícone de seta somente para links de comando.** Os links normais não devem usar o ícone de seta, a menos que estejam sendo usados como substitutos para links de comando no Windows XP.
-   **Use o ícone de blindagem de segurança para indicar que uma resposta requer elevação imediata.** Para obter diretrizes adicionais sobre como usar o ícone de proteção de segurança, consulte o [controle de conta de usuário](winenv-uac.md).
-   **Use ícones personalizados somente se eles ajudarem os usuários a identificar e diferenciar visualmente as opções.** Não use ícones personalizados se eles não forem imediatamente reconhecidos ou significativos.

    **Incorreto:**

    ![captura de tela de dois links de comando com ícones personalizados ](images/ctrl-command-links-image22.png)

    Neste exemplo, os ícones personalizados não são imediatamente reconhecidos.

-   **Para ícones personalizados, use ícones de 16x16 ou 32 pixels.** Use ícones maiores se houver espaço suficiente e eles se beneficiarem visualmente do tamanho maior. Se você precisar de sobreposições de blindagem de segurança, use ícones de 48x48 de 32x32 ou de pixel.

    ![captura de tela de três links de comando com ícones ](images/ctrl-command-links-image23.png)

    Este exemplo usa ícones personalizados de 32 pixels.

    ![captura de tela de dois links de comando com ícones maiores ](images/ctrl-command-links-image24.png)

    Este exemplo usa ícones personalizados de pixel 48x48, com uma sobreposição de proteção de segurança.

-   **Evite misturar ícones personalizados com o ícone de seta padrão em uma janela ou página.** Se você usar um ícone personalizado em uma superfície, tente usar todos os ícones personalizados. No entanto, prefira o ícone de seta padrão sobre ícones personalizados sem sentido.

### <a name="default-values"></a>Valores padrão

-   **Selecione o mais seguro (para evitar a perda de dados ou acesso ao sistema) e a resposta mais segura para o padrão.** Se não houver fatores de segurança e segurança, selecione a resposta mais provável ou conveniente.
-   **Quando for prático, torne a primeira resposta a opção padrão** porque os usuários costumam esperar que, a menos que essa ordem não seja lógica.
-   **Para caixas de diálogo, não faça uma ação destrutiva do link de comando padrão** , a menos que haja uma maneira fácil de desfazer a ação.

## <a name="recommended-sizing-and-spacing"></a>Dimensionamento e espaçamento recomendados

![captura de tela do espaçamento e dimensionamento do link de comando ](images/ctrl-command-links-image25.png)

## <a name="labels"></a>Rótulos

> [!Note]  
> Como links de comando são respostas a uma instrução principal, você deve criar uma [boa instrução Main](text-ui.md) antes de determinar suas respostas.

 

**Rótulos de link de comando**

-   **Escolha um rótulo conciso que se comunique claramente e diferencie o que o link de comando faz.** Ele deve ser auto-explicativo e corresponder à instrução principal. Concentre os rótulos nas diferenças entre as respostas. Os usuários não devem ter que descobrir o que o link de comando realmente significa ou como ele difere de outros links de comando.

    **Incorreto:**

    ![captura de tela de um link de comando redundante ](images/ctrl-command-links-image26.png)

    Neste exemplo, qual é a diferença entre a segunda e a terceira respostas? Não é bom que haja um botão Cancelar?

-   **Rótulos de link de comando de foco em ajudando os usuários a tomar a decisão certa.** Omita os detalhes que não afetam a escolha. Os rótulos não precisam ser uma especificação completa do que acontecerá.
-   **Inicie links de comando com um verbo.** No entanto, não use Click, pois o rótulo deve comunicar o que o link de comando faz, não como ele funciona.
    -   **Exceção:** Se todos os links de comando começarem com o mesmo verbo ou frase, elimine o verbo ou frase redundante.
-   Em geral, **use frases positivas** (fornecendo uma opção para fazer algo). Frases negativas (fornecendo uma escolha para não fazer algo) são aceitáveis se tornam os rótulos mais fáceis de entender.
-   **Use frases paralelas e rótulos de linha única.** Rótulos longos desestimulam a leitura e não devem ser necessários. Além disso, os rótulos de tamanho moderado são mais fáceis de se referir na documentação.
-   **Use a capitalização com estilo de frase.**
-   **Não use pontuação final, a menos que o rótulo seja uma pergunta.**
-   **Atribua uma chave de acesso exclusiva.** Para obter diretrizes, consulte [teclado](inter-keyboard.md).
-   **Não use reticências.** As reticências significam que mais informações podem ser necessárias para executar a ação. Os links de comando usados corretamente não precisam de reticências porque têm um efeito imediato.
-   **Se uma resposta for altamente recomendada, adicione "(recomendado)" ao rótulo.** Certifique-se de adicionar ao rótulo, não à explicação suplementar.
-   **Se uma resposta for destinada apenas a usuários avançados, considere adicionar "(avançado)" ao rótulo.** Certifique-se de adicionar ao rótulo, não à explicação suplementar.

**Dica:** Você pode avaliar os links de comando ao imaginar que um amigo declarou a instrução principal e você respondeu com os links de comando. Se responder com os links de comando não for natural ou estranha, revise os links de comando e, possivelmente, a instrução principal.

**Explicações suplementares**

-   Se um link de comando exigir mais explicações, **forneça uma explicação suplementar**. Explicações suplementares descrevem por que os usuários talvez queiram escolher uma resposta ou o que acontece se uma resposta for escolhida.

    ![captura de tela de texto que descreve os resultados da opção ](images/ctrl-command-links-image27.png)

    Neste exemplo, a explicação suplementar descreve as implicações da opção.

-   **Não use uma explicação suplementar que seja reestado de palavras do link de comando.** Use uma explicação suplementar somente quando não for possível tornar um link de comando auto-explicativo. Fornecer uma explicação suplementar para um link de comando não significa que você precise fornecê-los para todos.
-   **Focalize explicações complementares sobre como ajudar os usuários a tomar a decisão certa.** Omita os detalhes que não afetam a escolha. As explicações suplementares não precisam ser uma especificação completa do que acontecerá.
-   **Use frases paralelas e no máximo três linhas de texto.** Explicações suplementares demoradas desestimulam a leitura e não devem ser necessárias.
-   **Use frases completas e pontuação final.**

**Rótulos do grupo de links de comando**

-   **Não use rótulos de grupo.** As instruções principais atuam como o rótulo de grupo para links de comando.

## <a name="documentation"></a>Documentação

Ao fazer referência a links de comando:

-   Use o texto exato do rótulo, incluindo sua capitalização, mas não inclua o sublinhado da chave de acesso.
-   Se o rótulo incluir um nome de objeto, omita o nome do objeto ou use o texto do espaço reservado.
-   Para descrever a interação do usuário, use clique em.
-   Quando possível, formate o rótulo usando texto em negrito. Caso contrário, coloque o rótulo entre aspas somente se necessário para evitar confusão.

**Exemplos:** Para copiar a imagem, clique em **copiar e substituir**.

Clique em **redefinir o adaptador de rede**. (Para um link de comando rotulado "redefinir o nome do *adaptador* do adaptador de rede".)

 

