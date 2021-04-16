---
title: Instalação
description: Os usuários não gostam de instalar o software, portanto, as experiências de instalação modernas precisam ser simples, eficientes e sem problemas.
ms.assetid: ed0265a6-4c39-4a1f-9493-e316a6519df7
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 4e5de6f15dd797dd1d1362d1b515122b78c770f4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104563390"
---
# <a name="setup"></a>Instalação

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Os usuários não gostam de instalar o software, portanto, as experiências de instalação modernas precisam ser simples, eficientes e sem problemas.

A instalação geralmente se refere à experiência de instalação e configuração inicial de um programa. No entanto, a instalação também pode se referir a todo o ciclo de vida da instalação, incluindo a instalação inicial, atualizações incrementais do programa (como atualizações de versão ou Service Packs), reparo e desinstalação.

A maioria dos usuários considera a instalação como um mal necessário, a ser executada o mais rápido possível. O ponto de instalação do programa é usá-lo, sem tomar decisões incontávels sobre configuração e uso, ou, pior ainda, gastar muito tempo respondendo perguntas pessoais usadas para fins de inscrição ou marketing.

![Captura de tela que mostra uma caixa de diálogo de instalação com quatro opções.](images/exper-setup-image1.png)

Uma experiência de configuração simplificada.

A experiência de instalação combinada com o primeiro uso do programa é conhecida como a primeira experiência. Seu programa deve fornecer uma primeira experiência simplificada para os usuários. Cada pergunta ou etapa que não é necessária ou pode ser adiada atrasa a utilização do seu programa. Programas de instalação excessivamente complexos são relíquias de uma idade diferente.

**Observação:** As diretrizes relacionadas à [primeira experiência](exper-first-exper.md) usando um programa e [assistentes](win-wizards.md) são apresentadas em artigos separados.

## <a name="is-this-the-right-user-interface"></a>Esta é a interface do usuário correta?

Embora todos os programas do Microsoft Windows precisem de algum tipo de programa de instalação, você tem a opção de onde colocar as configurações do programa:

-   Instalação
-   Primeiro uso do programa
-   Opções de programa centralizado
-   No contexto do uso do recurso

**Instalação**

Apresente as configurações na instalação se:

-   As configurações corretas são necessárias para usar o programa e se aplicam a todos os usuários.
-   O uso de configurações padrão não é aceitável, porque não há nenhum padrão seguro, os usuários provavelmente escolhem configurações que não são o padrão ou as configurações padrão exigem o consentimento do usuário.
-   Os usuários devem, mas não provavelmente, alterar configurações importantes após a instalação.

**Primeiro uso do programa**

Apresente as configurações no primeiro uso do programa se:

-   As configurações corretas são necessárias para usar o programa e se aplicam a usuários individuais.
-   O uso de configurações padrão não é aceitável, porque não há nenhum padrão seguro, os usuários provavelmente escolhem configurações que não são o padrão ou as configurações padrão exigem o consentimento do usuário.
-   Os usuários devem, mas não provavelmente, alterar configurações importantes usando as opções do programa.
-   As configurações personalizam uma experiência básica ou uma que é crucial para a identificação pessoal de um usuário com o programa.

Para essas configurações, é provável que os usuários façam escolhas melhores no contexto do programa do que na instalação.

**Opções de programa centralizado**

Apresente as configurações na caixa de [diálogo opções](win-property-win.md) do programa se todas as condições a seguir se aplicarem:

-   Há configurações padrão que funcionam bem para a maioria dos usuários.
-   Há muitas configurações e elas se aplicam entre recursos e tarefas.
-   É mais provável que os usuários pretendam encontrar as configurações em um local centralizado.

**No contexto do uso do recurso**

Apresente as configurações no contexto relevante se todas as condições a seguir se aplicarem:

-   Há configurações padrão que funcionam bem para a maioria dos usuários.
-   Há um pequeno número de configurações independentes para um recurso específico.
-   É mais provável que os usuários pretendam encontrar as configurações com o recurso associado do que um local centralizado.
-   Há um lugar óbvio na interface do usuário para acessar as configurações.

Com atenção cuidadosa ao posicionamento das definições de configuração, você pode reduzir a carga dos usuários durante sua primeira experiência com seu programa.

## <a name="design-concepts"></a>Conceitos de design

### <a name="design-a-lightweight-setup"></a>Criar uma configuração leve

Bem-vindo, avançar, avançar, avançar, avançar, avançar, instalar, concluir, parabéns! Essa experiência de configuração parece familiar? Historicamente, os programas de instalação adotaram esse tipo de design ineficiente: uma longa sequência de telas, convidando os usuários em uma sequência automatizará de cliques apenas para obtê-lo.

Se os usuários descreverem a configuração do seu programa com palavras como rápida e simples, certamente praising a experiência. Eles funcionariam muito bem usando o programa do que configurá-lo.

**Revise seu design de instalação para perguntas, opções, páginas e caminhos não essenciais e seja Ruthless sobre como eliminar esses problemas.** Execute a pesquisa de usuário para descobrir quais opções os usuários realmente precisam e certifique-se de que elas não estão mindlessly clicando no botão Avançar em todas as páginas. Adie quaisquer opções ou perguntas mais bem abordadas no contexto do programa em execução.

Muitos programas de instalação oferecem páginas padrão, não porque são necessárias ou úteis, mas porque são padrão. Por exemplo, páginas de boas-vindas, páginas de resumo e páginas de parabéns, muitas vezes, simplesmente adicionam cliques. Em vez disso, o programa de instalação deve adicionar páginas somente se for necessário concluir a tarefa de instalação. Para obter diretrizes sobre os tipos de páginas de instalação e como avaliá-las, consulte [tipos de página](#page-types) mais adiante neste artigo.

![captura de tela da primeira página de configuração do ProClarity ](images/exper-setup-image2.png)

Neste exemplo, o programa de instalação elimina a página de boas-vindas tradicional e fica direto para os negócios.

Embora possa ser necessário oferecer diferentes ramificações de instalação (uma experiência mais rápida, típica e uma experiência mais controlável e personalizada), verifique se você tem opções personalizadas suficientes para garantir a complexidade extra. Não adicione ramificações, a menos que seja necessário. Algumas opções inimportantes em uma ramificação personalizada sugerem a necessidade de reorganizar o design da instalação.

Outro motivo para simplificar a configuração é que os usuários inexperientes às vezes sobreanalisam opções, temendo que uma escolha errada poderia ser irreversível ou destrutiva. Forçar os usuários a tomar decisões sobre coisas que eles não entendem ou se preocupam pode fazer com que eles se sintam ansiosos, incompetentes e até mesmo frustrados. Não é uma boa primeira impressão. É melhor fazê-lo rapidamente, se sentir confortável e confiante ao explorar os recursos em seu programa e tomar decisões melhores sobre as opções de recursos nesse momento. Para obter mais diretrizes, consulte [simplificando a configuração](#streamlining-setup) mais adiante neste artigo.

Busque para tornar sua experiência de instalação o mais [simples possível, mas não mais simples](/previous-versions//dn742474(v=vs.85)). Programas destinados a usuários altamente técnicos podem precisar de uma configuração complexa. Por exemplo, a equipe de Microsoft SQL Server descobriu que os administradores de banco de dados preferem manter o controle sobre muitas opções de configuração, como locais de arquivos. Além disso, o SQL Server é um aplicativo de negócios grande, com vários componentes que diferem amplamente em finalidade e funcionalidade. Portanto, embora queiramos manter as coisas simples, a instalação precisa refletir a complexidade do produto e as expectativas e necessidades de seus usuários.

Ainda assim, esses programas complexos de instalação devem ser a exceção, não a regra. A maioria dos programas do Windows deve se esforçar para iniciar o processo de instalação com uma única etapa simples.

### <a name="setup-phases"></a>Fases da instalação

Os programas de instalação bem projetados permitem que os usuários executem outras atividades durante a tarefa demorada de baixar e copiar arquivos. Para executar o autônomo, os programas de instalação são projetados para ter quatro fases separadas:

-   **A fase de decisão.** Os usuários indicam como querem que o programa seja instalado e configurado.
-   **A fase de download.** Para programas baixados da Internet. Se o programa tiver vários aplicativos ou versões, os usuários indicam o que baixar durante a fase de decisão.
-   **A fase de instalação.** O programa de instalação copia os arquivos e faz as alterações de configuração apropriadas.
-   **A fase de conclusão.** Todos os detalhes, etapas ou problemas restantes são resolvidos.

Como a fase de instalação pode levar muito tempo, essa fase deve ser projetada para ser executada até a conclusão sem qualquer envolvimento do usuário. Isso significa que todas as perguntas devem ser feitas durante a fase de decisão, e os problemas que surgirem devem ser enfileirados e tratados com a fase de conclusão. **Se a fase de instalação levar mais de um minuto para ser concluída, presuma que os usuários estarão fazendo algo mais durante as fases de download e instalação.**

**Incorreto:**

![captura de tela de € instalar o relatório automático? diálogo ](images/exper-setup-image3.png)

Neste exemplo, o programa de instalação interrompe o progresso para fazer uma pergunta que deveria ter sido solicitada durante a fase de decisão.

### <a name="present-helpful-progress"></a>Apresente o progresso útil

Se os usuários aguardarem pacientemente pela fase de instalação da experiência de instalação, talvez observando uma barra de progresso até sua conclusão aparente, apenas para testemunhar a redefinição da barra de progresso e recomeçar, há uma noção real de bebandeja. O progresso relatado foi enganoso e, por fim, não tem significado.

Uma variação nesse cenário problemático é a instalação "brinksmanship": os usuários veem o alcance do progresso, digamos, 99 por cento concluído, mas são forçados a aguardar uma quantidade de tempo desproporcional antes de finalmente chegar a 100% concluído. Portanto, em termos do que é mais importante para o usuário, uma promessa implícita sobre a quantidade de tempo de espera, a reivindicação de 99% concluída é enganosa.

Durante as fases de download e instalação, os usuários normalmente têm duas coisas que desejam saber: se eles esperam ou fazem alguma outra coisa, e a configuração será feita em breve. Embora haja variáveis suficientes no processo de instalação para impedir que você forneça informações de progresso perfeitamente precisas, os comentários sobre o progresso precisam ser precisos o suficiente para responder a essas duas perguntas e definir as expectativas apropriadas. Além de uma barra de progresso, você pode incluir uma breve instrução sobre o tempo geral esperado para o processo.

![captura de tela da caixa de diálogo mostrando o progresso da instalação ](images/exper-setup-image4.png)

Neste exemplo, a página de progresso inclui uma breve declaração geral sobre quanto tempo a instalação pode levar.

Bons programas de instalação usam barras de progresso com eficiência para fornecer aos usuários informações úteis sobre o progresso do programa de instalação. Para obter mais diretrizes, consulte [barras de progresso](progress-bars.md).

### <a name="design-for-all-setup-scenarios"></a>Design de todos os cenários de instalação

Os programas de instalação modernos devem ser projetados para lidar com uma variedade de cenários de instalação:

-   O usuário do programa está instalando-o de um disco ou compartilhamento de arquivos de rede.
-   O usuário do programa está baixando-o da Web.
-   Um OEM (fabricante original do equipamento) está incluindo o programa no computador na fábrica.
-   Um profissional de ti está instalando o programa em vários computadores em uma organização.
-   Alguém que não seja o usuário está instalando o programa (por exemplo, um pai em nome de um filho ou um colega de trabalho que está usando o mesmo computador que outro colega de trabalho).

Considerando esses cenários, você não deve presumir que os usuários estejam sempre instalando o programa para si mesmos (fazendo opções de preferências pessoais inadequadas), indo monitorar o processo de maneira minuciosa (fazendo a configuração autônoma importante) ou até mesmo querer uma interface gráfica do usuário para a tarefa.

### <a name="dont-forget-the-uninstall-experience"></a>Não se esqueça da experiência de desinstalação

Para concluir o ciclo de vida da instalação do software, os usuários precisam ser capazes de remover o software que eles não querem ou não precisam mais. Isso é especialmente importante se eles não instalaram o próprio programa (por exemplo, se ele chegou previamente no computador).

### <a name="handle-technical-support-strategically"></a>Manipule o suporte técnico estrategicamente

Instalar o programa é a única tarefa que todos os usuários devem concluir com êxito. Se os usuários não conseguirem instalar seu programa, você precisará fornecê-los com suporte técnico dispendioso ou que não sejam mais seus usuários.

Crie seu programa de instalação para fornecer à equipe de suporte técnico os recursos e as informações de que eles precisam para ajudar os usuários a instalar com êxito. Esses detalhes normalmente não devem ser expostos aos usuários, mas eles devem estar prontamente acessíveis quando necessário.

**Incorreto:**

![captura de tela do rótulo que mostra o nome do servidor com ](images/exper-setup-image5.png)

Neste exemplo, a barra de progresso mostra detalhes significativos apenas para o suporte técnico.

Mantenha a experiência do usuário normal simples — não se preocupe com informações com valor apenas para o suporte técnico. Em vez disso, registre as informações de suporte em um arquivo de log de instalação. E o mais importante é ajudar os usuários a evitar a necessidade de suporte técnico com mensagens de erro irncisas e claras que explicam problemas bem e fornecem soluções práticas. Forneça links para artigos de ajuda quando necessário. Considere fornecer uma opção de reparo para o programa de instalação para reparar arquivos ou configurações ausentes ou corrompidos.

**Se você fizer apenas três coisas...**

1.  1. Torne a instalação o mais simples e leve possível. Lembre-se de que os usuários não aproveitam a instalação, eles o sutratam. Examine atentamente cada pergunta, opção, página e caminho e corte tudo o que não é essencial para concluir a instalação.
2.  2. Projete para todos os cenários de configuração, incluindo instalações autônomas, instalações com script e desinstalação. Para instalações autônomas eficientes, verifique se há uma separação limpa entre as fases de configuração.
3.  3. Crie seu programa de instalação para que os usuários possam resolver problemas de instalação por conta própria, mas também Registre as informações necessárias para o suporte técnico no caso. Tenha em mente que a instalação é a única tarefa que todos os usuários devem concluir com êxito.

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Aplique as diretrizes padrão do assistente para programas de instalação baseados em assistente.** Use estas diretrizes para determinar um bom design de página, navegação eficaz, bons rótulos de controle, uso de instruções principais e uso de ajuda.
-   **Permitir que os usuários reiniciem o programa de instalação onde eles saíram, caso precise de muita entrada do usuário ou demore muito para serem concluídos.** Se os usuários reiniciarem o programa depois de fechá-lo antes da conclusão, restaure a entrada do usuário anterior e reinicie o local em que a instalação foi interrompida.
-   **Não exibir janelas de instalação maximizadas.** A exibição de uma janela de instalação maximizada pressupõe que os usuários darão à instalação sua atenção não dividida, o que é improvável. Em vez disso, escolha um tamanho que seja apropriado para que o conteúdo mantenha uma aparência simples.

### <a name="windows-integration"></a>Integração do Windows

-   **Nomeie o arquivo de instalação "Setup.exe".** "Install.exe" é uma alternativa aceitável. Isso permite que o Windows (e os usuários) reconheça o arquivo como um programa de instalação.
    -   **Exceção:** Para programas baixados da Internet, ajude os usuários a gerenciar e organizar sua pasta downloads, incluindo o nome do programa no nome do arquivo de instalação. Por exemplo, SetupVisualStudioExpress2008.exe.
-   **Copie os arquivos de programa para os locais do sistema de arquivos apropriados.** Isso permite que os usuários e o Windows encontrem e organizem melhor os arquivos. Para obter mais informações, consulte as [diretrizes de uso do namespace do sistema de arquivos do Windows](../fileio/naming-a-file.md#namespaces).

### <a name="user-account-control"></a>Controle de Conta de Usuário

-   **Assine digitalmente o arquivo executável da instalação.** Os executáveis assinados têm muitas vantagens, incluindo o uso de uma interface do usuário mais específica de elevação do controle de contas de usuários. Para obter informações sobre como assinar arquivos, consulte [introdução à assinatura de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).
-   **Se uma instalação puder exigir elevação, eleve o mais tarde possível.** Exiba a interface do usuário de elevação somente depois que o usuário tiver confirmado uma opção que requer elevação. Normalmente, a interface do usuário de elevação aparece durante a fase de instalação, não a fase de decisão. No entanto, se uma configuração sempre exigir elevação, eleve-a em seu ponto de entrada.
-   **Sempre exigir elevação para desinstalação.** Isso evita que malwares desinstalem software crítico sem que os usuários saibam disso.
-   **Uma vez com privilégios elevados, mantenha-se elevado até que privilégios elevados não sejam mais necessários.** Os usuários não devem ter que elevar várias vezes para executar uma instalação completa do programa.
-   **Se forem necessários privilégios especiais para a instalação, verifique as credenciais do usuário e relate quaisquer problemas na primeira ou na segunda página.** Não permita que os usuários executem muito trabalho apenas para descobrir que eles não têm as credenciais corretas para concluir a instalação.
-   **Exija os privilégios mínimos possíveis.** Por exemplo, os administradores são relutantes para instalar o software que exige credenciais de administrador de domínio.

Para obter mais diretrizes, consulte [controle de conta de usuário](winenv-uac.md).

### <a name="restarting-windows"></a>Reiniciando o Windows

-   **Evite reiniciar o Windows.** A maioria dos programas deve ser instalada sem reiniciar o Windows. O principal motivo pelo qual instalações ou atualizações do programa exigem uma reinicialização do sistema é que alguns dos arquivos envolvidos estão sendo usados atualmente por um programa em execução. Nesse caso, uma alternativa melhor é fazer com que os usuários reconheçam a situação, permitir que os usuários fechem esses programas e repita a ação. Para obter mais informações sobre como evitar reinicializações, consulte [Restart Manager](../rstmgr/restart-manager-portal.md).
-   **Se a sua instalação deve reiniciar o Windows:**
    -   **Use uma única reinicialização.** Atrase a reinicialização exigida por quaisquer pré-requisitos até que o programa e suas atualizações sejam completamente instalados.
    -   **Permitir que os usuários determinem quando isso acontece.** Não reinicie o Windows automaticamente, pois os usuários podem perder o trabalho. Certifique-se de que está claro para os usuários que eles têm uma opção.

        **Incorreto:**

        ![captura de tela da caixa de diálogo com reinicialização e cancelamento ](images/exper-setup-image6.png)

        Neste exemplo, os usuários não parecem ter a opção de quando reiniciar o Windows.

    -   **Se o usuário optar por não reiniciar o Windows imediatamente, apresente os comentários finais como sucesso, não uma falha.** Embora tecnicamente a instalação não seja concluída até a reinicialização, ela foi bem-sucedida do ponto de vista do usuário.

### <a name="streamlining-setup"></a>Simplificando a instalação

-   **Sempre que for prático, inicie o processo de instalação com uma única etapa.** Por exemplo, em vez de adicionar uma página separada na instalação dos termos de licença, você pode fornecer um link para eles em vez disso. Se você vincular aos termos:
    -   Frase o botão de confirmação como "concordar e instalar" para exigir consentimento explícito para aceitar os termos de licença.
    -   Verifique se o link do contrato de licença não pode ser quebrado vinculando-se a um arquivo local para a instalação em vez de uma página da Web.
    -   Forneça a capacidade de imprimir o contrato de licença de sua janela de exibição.
-   **Elimine as opções e as perguntas desnecessárias.**
    -   Adie as opções mais apropriadas para o primeiro uso do programa ou recurso.

        ![captura de tela da caixa de diálogo com a opção de configurações personalizadas ](images/exper-setup-image7.png)

        Neste exemplo, o Windows Media Player apresenta opções de privacidade por usuário na primeira utilização do programa.

    -   Não faça perguntas aos usuários sobre o estado do sistema. Em vez disso, detecte essas informações automaticamente e peça que os usuários verifiquem apenas se há um motivo para alterar.
    -   Não faça perguntas sobre detalhes não importantes. Por exemplo, para programas típicos do Windows, é seguro pressupor que você deve copiar os arquivos de programa para a pasta arquivos de programas.

        **Incorreto:**

        ![captura de tela da caixa de diálogo com local de instalação ](images/exper-setup-image8.png)

        Neste exemplo, a instalação deve ser simplificada ao eliminar a solicitação de entrada de local de arquivo. Dado o tamanho do programa, a maioria dos usuários não se preocupa e simplesmente clique em Avançar.

    -   Não peça permissão para fazer o que você não deve fazer mesmo assim. Por exemplo, a maioria dos programas não deve incluir uma opção para colocar o ícone do programa na área de trabalho.
    -   Não confirme o cancelamento da instalação. Se os usuários clicarem em cancelar durante a instalação, suponha que o cancelamento era intencional e feche o programa sem confirmação. Se você estiver fazendo com que os riscos percam tempo ou esforço significativo, permita que os usuários reiniciem o programa de instalação e escolham onde eles saíram.

-   **Otimizar para instalação autônoma.**
    -   Apresente todas as opções e perguntas durante a fase de decisão.
    -   Para as fases de download e instalação, adie a necessidade de entrada do usuário para quaisquer problemas encontrados até o fim da fase. Ao fazer isso, os usuários podem deixar a instalação autônoma até que elas retornem à sua conveniência.
-   **Elimine páginas desnecessárias.** Se a maioria dos usuários sempre clicar em avançar em uma página, considere a possibilidade de se livrar da página. Para obter diretrizes sobre como eliminar determinados tipos de páginas, consulte [tipos de página](#page-types).
-   **Elimine o texto desnecessário.**
    -   Remova o texto redundante de instruções e rótulos.
    -   Não explique os conceitos básicos de uso do Windows, como:
        -   Como interagir com controles (exemplos: para começar, clique em avançar; Para obter mais opções, clique em opções; Para obter mais informações, clique em ajuda).
        -   Como funcionam os assistentes (exemplo: se desejar revisar ou alterar as configurações, clique em voltar).
        -   Como funciona a instalação (exemplo: este programa copiará os arquivos de programa para o disco rígido...).
-   **Elimine o esforço desnecessário.**
    -   Forneça bons valores padrão:
        -   Em geral, selecione a resposta mais segura e privada como o padrão.
        -   Se a segurança e a privacidade não forem fatores, selecione a resposta mais provável ou conveniente.

            ![captura de tela de caixa de diálogo com nome e empresa mostrados ](images/exper-setup-image9.png)

            Neste exemplo, o nome de usuário e a organização fornecidos por padrão são obtidos do registro.

        -   Se uma opção for altamente recomendável, considere selecioná-la por padrão ou adicionar "(recomendado)" a seu rótulo.

    -   Avançar automaticamente as páginas quando uma página não tiver nenhuma entrada e a tarefa for realizada com êxito, como nas páginas Download, instalação, progresso e atualizações. Quando a etapa for concluída, permaneça nessas páginas apenas para mostrar problemas.
    -   Quando for prático, inicie o programa automaticamente quando a instalação for concluída, em vez de mostrar uma página de parabéns ou de conclusão. Quando a instalação é executada interativamente, suponha que o usuário esteja instalando seu programa para executá-lo imediatamente, portanto, executar o programa é o melhor comentário para mostrar que a instalação foi concluída. A execução automática do programa não é prática quando a instalação instala mais de um programa (por exemplo, um conjunto que consiste em muitos programas), quando a instalação não é executada interativamente ou quando o processo de instalação não é concluído após a instalação.

### <a name="page-types"></a>Tipos de página

**Páginas de boas-vindas e Introdução**

-   **Elimine as páginas de boas-vindas.** Embora seja ótimo se sentir bem-vindo, normalmente os usuários simplesmente clicam em avançar sem ler. E como os usuários normalmente ignoram essas páginas sem leitura, o texto faz pouco mais do que declarar o óbvio, por design.

    **Incorreto:**

    ![captura de tela da tela de boas-vindas com avançar e cancelar ](images/exper-setup-image10.png)

    Neste exemplo, não há nada para o usuário fazer, mas clique em Avançar.

-   **Use uma página Introdução somente se você precisar informar os usuários sobre os pré-requisitos para a instalação do.** Esses pré-requisitos incluem a instalação de software ou hardware necessário, a execução de atualizações e alterações de configuração do sistema necessárias, a execução de um backup do sistema para proteger contra a perda de dados ou a obtenção de informações necessárias que o usuário provavelmente já não tenha.
-   **Sempre que for prático, forneça a capacidade de executar os pré-requisitos diretamente do programa de instalação.** Os usuários devem ter que executar as etapas manualmente somente se não houver uma alternativa.
-   Se uma página de boas-vindas ou Introdução página não for usada, **inclua o nome e a descrição do programa em qualquer que seja a primeira página do programa de instalação.** Você pode usar a linguagem de boas-vindas como texto introdutório, desde que a finalidade da página esteja clara.

**Páginas de termos de licença**

-   **Escreva os termos de licença usando texto claro e conciso.** Use linguagem simples. Evite "legalese".
-   **Apresente o uso de um formato fácil de ler e verificar.** Não use passagens longas de texto em maiúsculas.

    **Incorreto:**

    ![captura de tela de termos de licença em letras maiúsculas ](images/exper-setup-image11.png)

    Neste exemplo, o texto em maiúsculas e o tamanho de fonte grande tornam os termos difíceis de serem lidos, forçando os usuários a rolar mais do que o necessário.

-   **Exigir consentimento explícito para aceitar os termos de licença.** A aceitação da licença nunca deve ser selecionada por padrão. Se botões de opção forem usados para indicar a aceitação, deixe as opções desmarcadas por padrão e exija que os usuários aceitem os termos antes de habilitar o botão Avançar.

    ![captura de tela da caixa de diálogo com o botão Avançar esmaecido ](images/exper-setup-image12.png)

    Neste exemplo, o botão Avançar é desabilitado até que os usuários aceitem explicitamente os termos de licença.

-   **Não exija que os usuários rolem para a parte inferior do texto dos termos de licença antes de o botão Avançar ser habilitado.** Isso impõe uma sobrecarga desnecessária nos usuários para entender por que o botão Avançar está desabilitado.
-   **Forneça um comando de impressão,** seja com um botão de comando ou um menu de contexto. Apresente os termos em um formato otimizado para impressão.

**Páginas de registro do produto**

-   **Exigir que os usuários se registrem somente se precisarem para usar o programa.** Explique claramente por que os usuários devem se registrar.
-   **Forneça registro opcional somente se houver um benefício de usuário claro,** por exemplo, para notificar os usuários sobre atualizações de produtos. Deixe essa opção desmarcada por padrão.
-   **Permitir que os usuários se registrem mais tarde.** Forneça um máximo de três lembretes e permita que os usuários ignorem os lembretes com um único clique.

**Páginas de escopo (típica, personalizada ou mínima)**

-   **Prefira eliminar esta página.** Suponha que a maioria dos usuários desejam a experiência de configuração típica (e projetem essa experiência para que funcione bem para a maioria dos usuários).
-   Se você precisar incluir uma página de escopo:
    -   **Explique as diferenças entre as opções em termos de funcionalidade e espaço em disco.** Os usuários dependem da clareza de informações na página escopo para garantir que eles façam a escolha certa.
    -   **Certifique-se de que as opções personalizadas são necessárias apenas para uma pequena porcentagem de usuários, enquanto a maioria dos usuários pode ignorá-las com segurança.** Caso contrário, as opções devem estar no caminho de instalação típico.
    -   **Se os usuários escolherem opções personalizadas, terá as opções de instalação típicas selecionadas por padrão.** Os usuários consideram a instalação típica como a linha de base e desejam personalizar adicionando ou removendo opções dessa linha de base.
-   Se você precisar usar uma opção de instalação personalizada, **considere usar o dimensionamento e o posicionamento do botão relativo para orientar a maioria dos usuários na instalação típica.**

    ![captura de tela da caixa de diálogo com o botão de instalação grande ](images/exper-setup-image13.png)

    Neste exemplo, o design da página reforça visualmente o fato de que a maioria dos usuários deve optar pela instalação típica.

**Páginas de entrada**

-   **Reduza o número de opções de instalação fazendo a coisa certa por padrão.** Para obter maneiras de eliminar opções, consulte [simplificando a instalação](#streamlining-setup).
-   **Forneça valores padrão aceitáveis sempre que possível.** Escolha os padrões que são seguros e privados e são aceitáveis para a maioria dos usuários sem alterações.
-   **A menos que seu programa tenha requisitos incomuns, busque ter uma única página de perguntas e opções.** Mas se o seu programa exigir várias páginas de perguntas e opções, exiba-as no fluxo de página principal do assistente. Não tente reduzir o número de páginas tecnicamente, colocando opções em caixas de diálogo ou usando guias.
-   ![captura de tela da caixa de diálogo de instalação com quatro opções ](images/exper-setup-image14.png)
-   Neste exemplo, as opções são limitadas a uma única página.
-   **Valide a entrada assim que possível:**
    -   Proibir caracteres inválidos na entrada.
    -   Use [balões](ctrl-balloons.md) para relatar problemas com caixas de texto inválidas.
    -   Validar os campos relacionados em uma página quando os usuários clicarem em Avançar.
    -   Valide os campos relacionados nas páginas de entrada assim que os problemas puderem ser detectados.
-   **Dê a todos os caminhos de arquivo editado um botão procurar.** Permitir que os usuários especifiquem os caminhos de rede.
-   **Para a página de entrada final, Rotule o botão confirmar instalar e não avançar.** Os usuários não devem se surpreender quando a instalação é iniciada. Antes do ponto de confirmação, verifique se os usuários podem alterar facilmente as configurações.

**Iniciar páginas de instalação**

-   **Elimine esta página se ela não tiver nenhuma finalidade diferente de resumir as opções anteriores e iniciar a instalação.** Se as páginas de entrada estiverem claras e poucas em número, não será necessário resumirá-las. Em vez disso, a página de entrada final deve ter o botão instalar, levando diretamente à página progresso.
-   **Para instalações complexas direcionadas a profissionais de ti, forneça uma página de instalação com uma lista abrangente das alterações que o programa de instalação executará.** Muitos profissionais de ti têm controle estrito de gerenciamento de alterações, portanto, eles precisam saber o efeito que a instalação do programa terá em detalhes.

**Páginas de progresso**

-   **Sempre forneça uma página de progresso,** mesmo que o programa seja instalado rapidamente. Forneça uma página de progresso separada para [a fase de download](#setup-phases) se houver uma. Desabilite os botões voltar (ou anterior) e avançar enquanto a instalação estiver em andamento, mas deixe o botão Cancelar habilitado e respondendo.

    ![captura de tela da caixa de diálogo com barra de progresso ](images/exper-setup-image15.png)

    Uma página de progresso típica.

-   **Use uma barra de progresso única e desterminada.** Siga as [diretrizes da barra de progresso de destérmino](progress-bars.md), incluindo:
    -   Indicar claramente a conclusão. Não deixe que uma barra de progresso vá para 100 por cento, a menos que a operação tenha sido concluída.
    -   Não reinicie o progresso. Uma barra de progresso perderá seu valor se ela for reiniciada (talvez porque uma etapa na operação seja concluída) porque os usuários não têm como saber quando a operação será concluída. Em vez disso, todas as etapas na operação compartilham uma parte do progresso e a barra de progresso passa para a conclusão uma vez.
-   **Forneça uma descrição concisa da etapa atual acima da barra de progresso.** Para instalações rápidas, tal texto é desnecessário; a barra de progresso sozinha é suficiente. Para instalações que exigem um minuto ou mais, o texto pode ser útil para os usuários que participarem da instalação.
    -   **Use fragmentos de sentença, normalmente começando com um verbo e terminando com uma elipse.** Exemplos: copiando arquivos..., instalando os componentes necessários....
    -   **Coloque o texto acima da barra, não abaixo.**

        **Incorreto:**

        ![captura de tela de texto exibido na barra de progresso ](images/exper-setup-image16.png)

        Neste exemplo, o texto explicativo deve aparecer acima da barra de progresso.

    -   **Evite desobstruir a página de progresso com detalhes desnecessários.** Esta página não é para [suporte técnico](#handle-technical-support-strategically), portanto, não é necessário exibir GUIDs de registro ou arquivos específicos copiados.

        **Incorreto:**

        ![captura de tela de GUID exibida acima da barra de progresso ](images/exper-setup-image17.png)

        Neste exemplo, os detalhes técnicos, como GUIDs, não têm significado para os usuários.

**Páginas de erro**

-   **Se a instalação falhar com um problema significativo, exiba uma página de erro que explique os problemas junto com as etapas práticas para resolvê-los.** Exiba a página com um ícone de erro. Não use uma caixa de diálogo para essa finalidade.

    ![captura de tela da página de erro e ícone ](images/exper-setup-image18.png)

    Neste exemplo, a falha de instalação é explicada em uma página de erro, juntamente com algumas etapas para resolver o problema.

-   **Se a instalação for concluída com um problema secundário recuperável, apresente o problema como uma tarefa adicional em vez de um erro.** Use um idioma positivo, orientado a sucesso e incentivado, e não termos como erro, falha ou problema. Não use um ícone de erro.

**Páginas de parabéns/conclusão**

-   **Ao instalar um único programa interativamente, inicie o programa (e feche o assistente de instalação) para indicar a configuração bem-sucedida, em vez de exibir uma página de conclusão. Exceção**
    -   As configurações que são executadas a partir da linha de comando não devem iniciar os programas.
    -   As atualizações automáticas (por exemplo, Windows Update) não devem iniciar os programas.
    -   A instalação da diretiva de grupo não deve iniciar programas.
    -   Qualquer cenário de configuração profissional de ti (porque eles não estão sendo instalados para seu próprio uso).
-   **Se a instalação tiver etapas de acompanhamento após a instalação, liste-as em uma página de conclusão.** Mas para justificar uma página de conclusão, certifique-se de que os usuários provavelmente executarão as etapas e que as etapas originais precisam ser declaradas (ou seja, elas não são óbvias).

    **Incorreto:**

    ![a captura de tela da página mostrando a configuração foi concluída ](images/exper-setup-image19.png)

    Neste exemplo, uma página de conclusão desnecessária declara o óbvio. Windows Update é executado automaticamente, portanto, não há motivo para os usuários executá-lo manualmente.

-   **Ao instalar um pacote de programas, exiba uma página de conclusão para indicar êxito e quaisquer etapas de acompanhamento que possam ser necessárias.**

    ![captura de tela da página final de instalação do pacote do Office ](images/exper-setup-image20.png)

    Neste exemplo, a instalação instalou vários programas, portanto, não faz sentido iniciar um programa específico automaticamente. Uma página de conclusão é mais apropriada.

### <a name="leaving-users-in-control"></a>Deixando os usuários no controle

-   **Não colete informações pessoais, como as usadas para fins de marketing.** A instalação não é uma oportunidade de enviar sua própria agenda, vender várias ofertas de programa ou realizar pesquisas de mercado; Você pode danificar a relação de confiança com os usuários dessa maneira.
-   **Não force os usuários a recusarem a instalação de recursos opcionais.** Permita que eles [aceitem em](glossary.md) vez disso. Por exemplo, os usuários devem optar explicitamente por instalar um gadget de área de trabalho do Windows.
-   **Permitir que os usuários adicionem ou removam recursos opcionais usando o programa de instalação após a configuração inicial.** Os usuários podem executar essa tarefa usando o item **desinstalar ou alterar um painel de** controle do programa.
-   **Para iniciativas de aperfeiçoamento da experiência do usuário, explique quais dados são transmitidos, como eles são usados e por quanto tempo ele é mantido.** Use um link para um tópico da ajuda da política de privacidade para essa finalidade.
-   **Evite usar som,** pois muitos cenários de instalação são autônomos, e como o som pode ser desnecessariamente confuso mesmo durante instalações assistidas.

### <a name="security"></a>Segurança

-   **Para a instalação baseada na Internet, forneça todas as atualizações de segurança automaticamente durante a instalação inicial.** Os usuários não devem ser atualizados como uma etapa separada.
-   **Evite recomendar que os usuários Desativem os firewalls como um pré-requisito para instalar seu programa.**
-   Se um firewall precisar ser desativado, faça o seguinte:
    -   **Limite a duração dessa condição a um tempo menor possível.**
    -   **Enfatize explicitamente quando os usuários puderem ligar o firewall novamente.**

### <a name="uninstall"></a>Desinstalar

-   **A desinstalação deve remover todos os rastreamentos de um programa, incluindo o seguinte:**
    -   Arquivos de programas, incluindo o programa de instalação.
    -   Entradas do menu iniciar.
    -   Ícones da área de trabalho e ícones de início rápido (se houver).
    -   Configurações do registro.
    -   Associações de arquivos.
-   **A desinstalação deve deixar por trás do seguinte:**
    -   Arquivos criados pelo usuário, como arquivos de documentos.
    -   Bibliotecas de vínculo dinâmico compartilhado armazenadas na pasta do sistema.

### <a name="help-and-support"></a>Ajuda e suporte

-   **Projete seu programa de instalação para não precisar de ajuda fazendo perguntas claras e autoexplicativas.** Reserve ajuda para perguntas avançadas que realmente se beneficiam de mais explicações.
-   **Não use arquivos Leiame.** Esses arquivos agora são obsoletos e os usuários não os lêem de qualquer maneira. Em vez disso, forneça conteúdo online, se necessário.
-   **Link para tópicos de ajuda apropriados ou para solução de problemas de conteúdo de mensagens de erro de instalação.** Verifique se o conteúdo da ajuda fornece um caminho claro para resolver o problema. Para obter mais informações, consulte [mensagens de erro](mess-error.md).
-   **Crie arquivos de log para capturar informações úteis para o suporte técnico.** Não conorganize a interface do usuário da instalação com detalhes relacionados ao suporte técnico que não têm significado para a maioria dos usuários. Em vez disso, use arquivos de log para essa finalidade.

### <a name="text"></a>Texto

-   **Seja conciso.** Os assistentes de instalação geralmente explicam os recursos e as opções, usando blocos de texto difíceis de serem verificados rapidamente. **Exceção**
    -   Soletrar todos os acrônimos. A instalação é frequentemente a primeira experiência dos usuários com seu programa, portanto, não presuma que eles compreendam um jargão como acrônimos.
    -   Explique conceitos e terminologia desconhecidos, preferencialmente em vigor, mas usando tópicos de ajuda, se necessário.
-   **Prefira um tom amigável e profissional; Evite um tom muito técnico.**

**Incorreto:**

Restringir a instalação por usuário.

**Correto:**

Instale somente para mim.

-   Não use agora nos rótulos do botão de comando porque o imediata do comando pode ser obtido para concedido.
    -   **Exceção:** Quando necessário, use agora para diferenciar comandos que iniciam uma tarefa a partir de comandos que executam uma tarefa imediatamente.

![captura de tela do botão baixar ](images/exper-setup-image21.png)

Neste exemplo, clicar no botão de comando vai para uma janela ou página que permite que os usuários façam o download.

![captura de tela do botão baixar agora ](images/exper-setup-image22.png)

Neste exemplo, clicar no botão de comando executa o download imediatamente.

Somente um comando em um fluxo de tarefas deve ser rotulado com Now. Portanto, por exemplo, um comando **baixar agora** nunca deve ser seguido por outro comando **baixar agora** .

-   Use termos de licença, não contrato de licença, contrato de licenciamento, contrato de licença de usuário final ou EULA.

Para obter mais diretrizes, consulte [estilo e Tom](text-style-tone.md).

## <a name="documentation"></a>Documentação

-   Como um verbo, a configuração é de duas palavras; como um adjetivo ou substantivo, a instalação é uma palavra.
-   O programa de instalação está em letras maiúsculas e não está hifenizado.
-   Use instalar para se referir a adicionar hardware ou software a um sistema de computador.
-   Não use instalar como um substantivo. Em vez disso, use a instalação.
-   Use reiniciar, não reinicializar. Indique que é o computador, não um programa, que está sendo reiniciado.

 

 