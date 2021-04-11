---
title: Primeira experiência
description: Na primeira experiência ideal, os usuários instalam seu programa e o utilizam de forma produtiva, sem responder a várias perguntas ou aprender uma série de coisas.
ms.assetid: d925f71c-fc5a-4ff2-8f5d-9434c162b4b4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c965ae77507b0041d17cabb34c4f53dc8216c134
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104172436"
---
# <a name="first-experience"></a>Primeira experiência

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Na primeira experiência ideal, os usuários instalam seu programa e o utilizam de forma produtiva, sem responder a várias perguntas ou aprender uma série de coisas.

Uma interface do usuário de primeira experiência ajuda os usuários a fazer a transição de sua primeira exposição para um novo programa ou recurso para o uso diário.

Para programas do Windows, a primeira experiência inicial ocorre quando os usuários executam o programa de instalação. Programas de instalação normalmente:

-   Exigir que o usuário aceite um contrato de licença de usuário final (EULA).
-   Solicitar uma chave do produto (Product Key).
-   Apresente as opções relacionadas à configuração necessárias, incluindo a instalação de software opcional.
-   Copie o software para o disco rígido do usuário.
-   Apresente as opções do programa que se aplicam a todos os usuários.

![captura de tela da caixa de diálogo ' digitar sua chave do produto ' ](images/exper-first-exper-image1.png)

Parte de uma experiência típica de instalação do Windows.

A primeira experiência continua na primeira utilização do programa ou recurso. Essa experiência de uso inicial pode:

-   Apresente as opções do programa que se aplicam somente ao usuário atual.
-   Ofereça tutoriais sobre produtos ou recursos.

![captura de tela da caixa de diálogo ' centro de boas-vindas ' ](images/exper-first-exper-image2.png)

A primeira experiência de uso.

**Observação:** As diretrizes relacionadas às [Opções de programa](win-property-win.md) são apresentadas em um artigo separado.

## <a name="is-this-the-right-user-interface"></a>Esta é a interface do usuário correta?

Para decidir, considere as perguntas a seguir.

### <a name="setup-experience"></a>Experiência de instalação

As seguintes condições se aplicam?

-   As configurações corretas são necessárias para usar o programa e se aplicam a todos os usuários.
-   As configurações personalizam uma experiência principal, ou uma que é crucial para a identificação pessoal do usuário com o programa.
-   Não há nenhum padrão seguro, o usuário provavelmente escolherá configurações que não são o padrão ou as configurações padrão exigem consentimento do usuário.
-   É improvável que o usuário altere as configurações após a instalação.
-   A alteração das configurações requer elevação.

Nesse caso, considere apresentar as configurações durante a experiência de instalação.

### <a name="first-use-experience"></a>Primeira experiência de uso

As seguintes condições se aplicam?

-   As configurações ou tarefas corretas são necessárias para usar o programa ou recurso e elas se aplicam a usuários individuais.
-   As configurações personalizam uma experiência principal, ou uma que é crucial para a identificação pessoal do usuário com o programa.
-   Não há nenhum padrão seguro, o usuário provavelmente escolherá configurações que não são o padrão ou as configurações padrão exigem consentimento do usuário.
-   É provável que os usuários façam escolhas melhores no contexto do programa do que na instalação.
-   É improvável que o usuário altere as configurações usando as opções.

Nesse caso, considere apresentar as tarefas e configurações durante a primeira experiência de uso do programa ou recurso.

## <a name="design-concepts"></a>Conceitos de design

Na primeira experiência ideal, os usuários instalam seu programa (ou até mesmo apenas o iniciam se não exigir instalação) e o usam de forma produtiva imediatamente sem responder a várias perguntas ou aprender uma série de coisas.

Isso é ideal para a maioria dos programas, portanto, você deve buscar essa experiência ideal sempre que puder. No entanto, essa meta geralmente não é possível para programas que exigem integração significativa do sistema, têm muitos recursos opcionais ou têm implicações de privacidade. Por exemplo, se o seu programa tiver recursos que possam revelar informações pessoais para partes não confiáveis, as filosofias da [computação confiável](https://www.microsoft.com/mscorp/twc/default.mspx) exigirão que você obtenha o consentimento do usuário antes de habilitar esses recursos.

### <a name="questions-arent-choices"></a>As perguntas não são opções

As perguntas exigem respostas que devem ser respondidas antes que os usuários possam continuar. As perguntas durante a primeira experiência são as barreiras que os usuários devem passar antes de poderem usar seu programa de forma produtiva. Por outro lado, as opções são opcionais. Os usuários não precisam responder a eles ou podem optar por vê-los somente quando desejarem.

Portanto, as configurações apresentadas no fluxo principal de um assistente de instalação são perguntas, enquanto as configurações fora do fluxo de instalação principal ou em uma caixa de diálogo opções de programa são opções. As perguntas desnecessárias tornam a primeira experiência do seu programa complicada e longa, eliminando efetivamente a previsão positiva e a empolgação dos usuários sobre a introdução ao seu programa.

### <a name="use-the-first-experience-when-you-must"></a>Use a primeira experiência quando precisar

Apresente as configurações e as tarefas para os usuários durante as primeiras experiências quando precisar, mas geralmente há alternativas melhores:



|                                             |                                                                                                                                                    |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| **Primeira experiência**<br/>             | **Alternativas**<br/>                                                                                                                        |
| Perguntas de instalação<br/>                  | Selecione os padrões apropriados.<br/> Permitir que os usuários alterem as opções do programa.<br/> Forneça caminhos de instalação típicos e personalizados. <br/> |
| Perguntas do primeiro uso<br/>              | Selecione os padrões apropriados e permita que os usuários alterem as opções do programa.<br/>                                                            |
| Primeiras tarefas de uso<br/>                  | Presente contextualmente.<br/>                                                                                                           |
| Primeiro usar anúncios de recursos<br/> | Tornar as tarefas mais comuns e importantes detectáveis e contextuais.<br/>                                                                   |
| Primeiros tutoriais de uso<br/>              | Torne os recursos autoexplicativos do programa.<br/>                                                                                                 |
| Registro do produto<br/>             | Forneça o comando no menu ajuda e na caixa sobre.<br/>                                                                                             |



 

**Se você fizer apenas uma coisa...**

Mantenha sua primeira experiência o mais simples possível. Faça seu programa funcionar imediatamente. Escolha padrões seguros, seguros e convenientes e faça perguntas durante a instalação e primeiro use somente quando precisar.

Você tem apenas uma chance de fazer uma boa primeira impressão e essa primeira impressão é duradoura.

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Limite as primeiras experiências às tarefas e configurações necessárias para usar um programa ou recurso e inclua-as somente quando não houver nenhuma alternativa melhor.** Consulte a tabela anterior para obter alternativas.
    -   **Exceção:** Adicione configurações personalizadas ou de personalização do programa à primeira experiência se sua personalização fizer parte da experiência principal ou crucial para a identificação pessoal do usuário com o programa.

![captura de tela da caixa de diálogo ' digitar um nome do computador ' ](images/exper-first-exper-image3.png)

O Windows solicita aos usuários o nome do computador e a escolha do plano de fundo durante a instalação, pois essas configurações ajudam a formar uma conexão emocional com o produto.

-   **Use a experiência de instalação** para tarefas e configurações se elas se aplicarem a todos os usuários ou se as configurações de alteração exigirem elevação.
-   **Use a primeira experiência de uso** para tarefas e configurações se elas se aplicarem a usuários individuais.

### <a name="presentation"></a>Apresentação

-   **Prefira tarefas e configurações opcionais às tarefas e configurações necessárias.** Evite forçar os usuários a configurar seu programa.

    ![captura de tela da caixa de diálogo "novo hardware encontrado" ](images/exper-first-exper-image4.png)

    A caixa de diálogo novo hardware encontrado torna opcional a instalação do software de driver em vez de torná-lo uma tarefa necessária.

-   **Faça tarefas e configurações opcionais fora do fluxo de tarefas principal sempre que for prático.** Por exemplo, muitos programas de instalação fornecem um caminho de instalação personalizado para remover configurações raramente alteradas do fluxo de tarefas principal.

    ![captura de tela de botões de opção completo e personalizado ](images/exper-first-exper-image5.png)

    Uma experiência de instalação que facilita o fluxo de tarefas principal se o usuário não pretende personalizar a instalação.

-   **Não sobrecarregar usuários com tarefas e configurações:**
    -   **Comece com algo simples.** Comece com configurações simples e de personalização e o progresso em relação a configurações e tarefas técnicas mais complexas. Por exemplo, a instalação do Windows começa com informações pessoais e termina com a configuração de rede.
    -   **Use uma experiência contextual primeiro** para tarefas e configurações se elas se aplicarem somente a recursos que não são fundamentais para o programa principal.

        ![captura de tela da caixa de diálogo ' configuração de áudio e vídeo ' ](images/exper-first-exper-image6.png)

        O Windows Live Messenger tem uma configuração contextual para áudio e vídeo, pois eles são usados por recursos secundários.

-   **Não apresente tudo de uma só vez.** Consolide para usar uma única interface do usuário em vez de várias superfícies de interface do usuário ou exibir tarefas em momentos diferentes, em vez de todas de uma só vez.

    **Incorreto:**

    ![captura de tela de cinco caixas de diálogo sobrepostas ](images/exper-first-exper-image7.png)

    Neste exemplo, a primeira experiência de uso é impressionante.

-   **Expresse perguntas e opções em termos de metas e tarefas dos usuários, não em termos de tecnologia.** Forneça as opções que os usuários entendem e diferenciam claramente. Certifique-se de fornecer informações suficientes para que os usuários tomem decisões informadas.
-   **Se a necessidade de informações pessoais não for óbvia, explique por que o programa precisa das informações e como ela será usada.**

    ![captura de tela de texto que informa o uso do endereço de email ](images/exper-first-exper-image8.png)

    Neste exemplo, um aplicativo de comércio eletrônico explica como as informações pessoais serão usadas.

-   **Apresente a primeira experiência em tela inteira somente se os usuários não puderem executar outras tarefas de forma produtiva.** Por exemplo, a instalação do Windows é apresentada em tela inteira para desencorajar os usuários de executar outras tarefas enquanto o Windows está sendo instalado. A maioria das primeiras experiências não deve ser de tela inteira.

### <a name="settings"></a>Configurações

-   **Para todas as configurações, selecione a mais segura (para evitar a perda de dados ou acesso ao sistema), o valor mais seguro e privado por padrão.** Se não houver fatores de segurança e segurança, selecione o valor mais provável ou conveniente. Escolher bons padrões é uma maneira eficaz de simplificar a primeira experiência.
-   **Exigir que os usuários aceitem:**

    -   Configurações com implicações legais, como contratos de licenciamento de usuário final (EULAs). Essas configurações não podem ter seleções padrão.
    -   Recursos que executam alterações automáticas de configuração do sistema, como atualizações automáticas do Windows.
    -   Recursos que revelam informações de identificação pessoal (PII) ou informações do sistema.
    -   Alterações na área de trabalho do usuário além de adicionar entradas ao menu Iniciar, como adicionar ícones à área de trabalho ou à barra de início rápido.
    -   Software opcional, como aprimoramentos de produtos, assinaturas e produtos de terceiros.

    ![captura de tela da caixa de diálogo escolher recursos desejados ](images/exper-first-exper-image9.png)

    Neste exemplo, os usuários optam por aprimoramentos de produtos, assinaturas e produtos de terceiros.

-   **Se uma configuração for altamente recomendável, adicione "(recomendado)" ao rótulo.** Para botões de opção e caixas de seleção, certifique-se de adicionar ao rótulo de controle, não às anotações complementares.
-   **Se uma configuração for destinada somente a usuários avançados, adicione "(avançado)" ao rótulo.** Para botões de opção e caixas de seleção, certifique-se de adicionar ao rótulo de controle, não às anotações complementares.

### <a name="tasks"></a>Tarefas

-   **Ajude os usuários a passar o tempo de espera de forma produtiva.**
    -   Se o tempo de espera for normalmente entre um e dois minutos, considere fornecer informações úteis enquanto os usuários estão aguardando, como uma apresentação do que há de novo durante a instalação.
    -   Se o tempo de espera for normalmente maior que dois minutos, facilite para os usuários executarem outras tarefas. Exiba o tempo de espera estimado, recomende que os usuários façam alguma outra coisa enquanto isso e tornem a conclusão da tarefa óbvia alterando a tela significativamente.
-   **Reconsidere a apresentação de tutoriais durante a primeira experiência.** Os usuários provavelmente desejam usar seu programa imediatamente e estão interessados em tutoriais em um ponto posterior.
-   **Não use notificações de anúncio de recursos na primeira experiência.** Em vez de usar uma [notificação de anúncio de recursos](mess-notif.md), crie o recurso para ser mais fácil de descobrir em contextos onde for necessário ou não faça nada especial e permita que os usuários descubram o recurso por conta própria.
-   **Não use nenhuma notificação durante a experiência inicial do Windows.** Para melhorar sua primeira experiência, o Windows 7 suprime todas as notificações exibidas durante as primeiras horas de uso. Projete seu programa supondo que os usuários não vejam essas notificações.

 

