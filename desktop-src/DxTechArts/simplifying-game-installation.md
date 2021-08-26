---
title: Simplificando a instalação do jogo
description: este artigo descreve alguns conceitos que os desenvolvedores de jogos para Windows podem e devem implementar para melhorar a experiência geral.
ms.assetid: 356780b7-801d-c6dd-a266-6272bcb8bd36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53062b9905e59435f1b9175eb95832294d93e51193003622d3bcc6dd16ee07df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042456"
---
# <a name="simplifying-game-installation"></a>Simplificando a instalação do jogo

uma grande vantagem dos jogos que são executados em um console em vez de em Windows é o processo de instalação — ou a falta deles. Quando um jogo é executado pela primeira vez em um console, o jogador faz algumas opções ou confirmações e é capaz de começar a jogar quase imediatamente. a instalação de um jogo em Windows é mais complicada, por comparação, por sua necessidade de entrada substancial do usuário e seu processo de instalação potencialmente longo. no entanto, esse processo de instalação pode ser melhorado para fornecer uma melhor experiência para os jogadores de jogos baseados em Windows. este artigo descreve alguns conceitos que os desenvolvedores de jogos para Windows podem e devem implementar para melhorar a experiência geral.

-   [Instalação típica do jogo](#typical-game-installation)
-   [Instalação simplificada de jogos](#simplified-game-installation)
    -   [Faça todas as perguntas com antecedência](#ask-all-questions-up-front)
    -   [Fornecer modos de instalação especiais](#provide-special-installation-modes)
    -   [Minimizar a quantidade de perguntas de instalação](#minimize-the-quantity-of-installation-questions)
    -   [Alterar componentes opcionais em componentes necessários](#change-optional-components-into-required-components)
    -   [Sempre instalar o DirectX e fazer isso silenciosamente](#always-install-directx-and-do-so-silently)
    -   [Pense em seu EULA](#think-about-your-eula)
    -   [Iniciar automaticamente após a instalação](#automatically-launch-after-installation)
    -   [Otimizar o desempenho da instalação](#optimize-your-installation-performance)
    -   [registrar-se no Firewall do Windows durante a instalação](#register-with-windows-firewall-during-installation)
    -   [Instalar para todos os usuários, não apenas o usuário atual](#install-for-all-users-not-just-the-current-user)
-   [Exemplo de instalação simplificada](#example-of-simplified-installation)
-   [Resumo](#summary)

## <a name="typical-game-installation"></a>Instalação típica do jogo

Ao comparar a facilidade de instalação e a quantidade de tempo necessária para começar a jogar um jogo, a experiência típica do Xbox é muito melhor do que a Windows. o fluxograma na figura 1 mostra os processos de instalação típicos no Xbox e no Windows, para comparação.

**Figura 1. Processo de instalação típico, Xbox versus Windows**

![Xbox \- vs \- PC](images/pcvsconsoleinstall.png)

## <a name="simplified-game-installation"></a>Instalação simplificada de jogos

no entanto, os requisitos maiores colocados no usuário para instalar um jogo em Windows não precisam ser. Ao implementar os conceitos a seguir, você diminuirá o número de etapas que um usuário deve concluir, o que pode reduzir a quantidade de tempo necessária para a instalação.

### <a name="ask-all-questions-up-front"></a>Faça todas as perguntas com antecedência

Todas as opções que o jogador seleciona durante a instalação que podem causar a anulação da instalação devem ser oferecidas antes daquelas que não interrompem a instalação; o pior cenário é que o jogador receberá uma opção que pode fazer com que a instalação seja anulada depois que o jogo for completamente copiado da mídia de instalação. Isso pode ser especialmente frustrante se a instalação exigir que a troca de vários discos seja concluída. Você deve projetar seu instalador para fazer todas as perguntas importantes (como a aceitação do EULA) no início do processo, para que a instalação não precise ser revertida em ou perto de sua conclusão.

Você também pode solicitar que o usuário aceite o EULA e insira a chave do produto (Product Key) quando o jogo iniciar pela primeira vez, em vez de pedir isso como parte da instalação. Nesse cenário, a recusa de aceitar o EULA ou cancelamento durante a entrada da chave do produto não reverterá a instalação, pois essas solicitações fazem parte do próprio jogo. Isso pode ser útil se você tiver cenários pré-instalados ou OEM. No entanto, tome cuidado para não solicitar que o usuário faça escolhas durante a inicialização inicial que exija credenciais administrativas.

### <a name="provide-special-installation-modes"></a>Fornecer modos de instalação especiais

o ideal é que Windows instaladores de jogos só ofereçam modos de instalação totalmente automáticos e personalizados e nada entre eles.

O modo automático não deve fazer mais perguntas do que absolutamente necessário para criar uma instalação em funcionamento e simplesmente usar as configurações padrão sem solicitar outras opções. Muitos jogos não se preocupam com o local do jogo no disco rígido ou com as configurações iniciais do jogo – eles apenas querem jogar o jogo assim que possível.

O modo personalizado deve ser apenas para usuários avançados que precisam ou querem alterar o caminho de instalação ou outras opções de instalação, e ele não deve ser o modo padrão.

O modo personalizado pode oferecer a opção de uma instalação completa ou de uma instalação mínima que instala apenas os arquivos necessários para jogar o jogo. Se o jogador escolher a instalação mínima, o jogo poderá usar as técnicas de instalação sob demanda ou de streaming para ler os dados de instalação restantes, o que permite que o jogador comece a jogar rapidamente o jogo sem precisar aguardar a conclusão da instalação completa. No entanto, a instalação de dados dessa maneira tem um impacto no design do mecanismo de jogo. Para obter mais informações sobre como instalar o conteúdo sob demanda, consulte [instalar sob demanda para jogos](/windows/desktop/DxTechArts/install-on-demand-for-games).

### <a name="minimize-the-quantity-of-installation-questions"></a>Minimizar a quantidade de perguntas de instalação

Nos dois modos de instalação, você deve tentar limitar o número de vezes que você solicita o jogador durante a instalação. Isso reduzirá a quantidade de leitura necessária para que o jogo seja instalado e em execução. Se necessário, deve haver apenas um prompt de acompanhamento após a conclusão da instalação. Como você pode ver, o exemplo mostrado na Figura 1 tem muitos prompts pós-instalação.

### <a name="change-optional-components-into-required-components"></a>Alterar componentes opcionais em componentes necessários

Faça a instalação de todos os componentes necessários em vez de torná-los opcionais, a menos que haja um bom motivo para fazer o contrário. A simples instalação de todos os componentes fará com que o jogo seja iniciado sem atraso e confusão.

### <a name="always-install-directx-and-do-so-silently"></a>Sempre instalar o DirectX e fazer isso silenciosamente

É altamente recomendável que o jogo instale silenciosamente o DirectX redistribuível no qual o jogo foi criado. O processo de instalação do DirectX foi projetado de forma que ele verifique se algo precisa ser atualizado e retorna rapidamente se não estiver. Portanto, não é necessário perguntar aos usuários se eles querem que o DirectX esteja instalado. Uma instalação silenciosa do DirectX pode ser feita executando este comando do seu pacote de instalação: **dxsetup.exe/Silent**

Perguntar a um usuário se ele deseja instalar o DirectX pode causar muitos problemas. Por exemplo, se o usuário supor que ele tem os pacotes redistribuíveis mais recentes instalados e optar por ignorar a instalação do DirectX; a instalação do jogo pode continuar com êxito mesmo assim. No entanto, se o jogo exigir uma versão específica do D3DX ou outra funcionalidade atualizada que foi ignorada, o jogo não funcionará e o usuário ficará muito frustrado.

Se, por alguma razão, você precisar perguntar ao usuário se deseja instalar o DirectX, o instalador deverá, pelo menos, anular e reverter todo o processo de instalação se o usuário optar por não instalar o DirectX. Reverter a instalação evitará erros causados pelo sistema não ter a versão mais recente do DirectX instalada quando o jogo for iniciado.

Observe que é importante enviar o redistribuível para o qual seu jogo foi criado em vez de simplesmente enviar o redistribuível do SDK do DirectX mais recente. Os redistribuíveis mais recentes podem não conter todos os componentes encontrados em uma versão anterior.

Também é importante fazer com que o instalador Verifique o que já está instalado e determine se a reinicialização do sistema é necessária. Se o DirectX for atualizado, a cópia de uma DLL não deverá exigir a reinicialização.

### <a name="think-about-your-eula"></a>Pense em seu EULA

O EULA do DirectX pode e deve ser anexado ao EULA do desenvolvedor do jogo. Não há nenhum ponto em permitir que o usuário concorde com o EULA do desenvolvedor e não com o EULA do DirectX. Ou o usuário deve concordar com ambos os EULAs ou não instalar o jogo. Se um desenvolvedor sentir que ela deve oferecer ao usuário a opção, toda a instalação deverá falhar se o usuário optar por não concordar com o EULA do DirectX.

Se possível, consulte seu departamento jurídico para ver se você pode evitar completamente os EULAs e usar um EULA comprimido, como o uso de jogos de console. Isso evitará a necessidade de perguntar aos usuários se eles desejam aceitar o EULA. O EULA do DirectX precisa ser anexado ao EULA com encolhimento reduzido; caso contrário, o EULA do DirectX deve ser exibido e aceito, o que anula a finalidade de usar um EULA comprimido.

Uma exceção a um EULA com encolhimento reduzido é para um editor de conteúdo. Qualquer editor precisa exibir um EULA durante a instalação do editor ou quando o editor é iniciado pela primeira vez. Muitos jogadores estão interessados apenas em reproduzir e não fazer conteúdo, portanto, a instalação de um editor deve ser um processo separado.

### <a name="automatically-launch-after-installation"></a>Iniciar automaticamente após a instalação

Quase todos os jogadores querem jogar um jogo assim que receberem. Por padrão, o instalador deve iniciar o jogo após concluir a instalação, embora seja uma prática recomendada, em uma instalação personalizada, para especificar isso em uma caixa de seleção que o usuário pode substituir.

### <a name="optimize-your-installation-performance"></a>Otimizar o desempenho da instalação

Os desenvolvedores devem testar suas instalações para determinar a quantidade de tempo necessária para a instalação. Os desenvolvedores podem reduzir o tempo de instalação usando a versão mais recente de suas ferramentas de instalação e otimizando o layout de dados na mídia de instalação. A maioria das ferramentas de criação de DVD tem opções de otimização de layout que podem melhorar os tempos de instalação sem aumentar a carga de trabalho de desenvolvimento.

### <a name="register-with-windows-firewall-during-installation"></a>registrar-se no Firewall do Windows durante a instalação

se o seu jogo puder ser executado como um servidor ou se o modelo de rede de jogos for ponto a ponto, registre seu jogo com Windows firewall no momento da instalação. Isso impedirá que a caixa de diálogo do firewall apareça no meio do jogo quando o usuário tentar acessar a rede. Se o jogo for um cliente puro, o instalador não deverá adicionar o jogo à lista de exceções do firewall.

para obter mais informações, consulte Windows Firewall para desenvolvedores de jogos.

### <a name="install-for-all-users-not-just-the-current-user"></a>Instalar para todos os usuários, não apenas o usuário atual

Basta, por padrão, instalar o jogo para todos os usuários. Isso permitirá que qualquer usuário novo no sistema reproduza o jogo sem precisar instalá-lo para eles. Se a instalação de todos os usuários for tentada em uma conta de usuário Least-Privileged, o instalador irá falhar ou solicitar ao usuário uma senha de administrador. Portanto, tente detectar se a conta tem privilégios adequados antes de oferecer a opção de instalar para todos os usuários. Se o usuário optar por instalar o jogo somente para o usuário atual, certifique-se de alterar o caminho de instalação para um local dentro do perfil do usuário. Idealmente, altere o caminho para algum lugar em dados de aplicativo não móveis (por exemplo, um subdiretório de \_ AppData local CSIDL \_ ).

## <a name="example-of-simplified-installation"></a>Exemplo de instalação simplificada

A seguir, a Figura 2 é um exemplo de um processo aprimorado para instalar um jogo no Windows, com diálogos de instalação simplificados.

**Figura 2. Processo de instalação simplificado**

![instalar](images/simplifiedgameinstall.png)

Veja a seguir pontos importantes de observação:

-   O instalador é automaticamente lançado após a inserção do disco de instalação (executar automaticamente).
-   A tela inicial , com opções para instalar, remover, exibir o site ou sair, não será mostrada se o jogo ainda não estiver instalado no computador.
-   A **caixa de** diálogo Instalação é a primeira caixa de diálogo mostrada pelo instalador.
-   O **botão** Instalar é a implementação do modo de instalação automática.
-   O **botão** Opções é a implementação do modo de instalação personalizado.
-   O **botão** Cancelar sairá imediatamente do instalador. Como iniciar o instalador é uma ação trivial para o usuário, não solicitar confirmação.
-   Depois que o usuário aceitar o EULA e inserir uma chave do produto (Product Key) válida, a instalação será iniciada.
-   Quando o processo de instalação for concluído, o jogo será lançado automaticamente ou exibirá uma caixa  de diálogo que alerta o usuário de que a instalação foi concluída e oferecerá opções adicionais, com base em se Executar jogo após a instalação foi selecionado.
-   A **caixa de seleção** Executar jogo oferece outra chance de iniciar o jogo, para sua conveniência. Essa opção sempre é deseleitada por padrão,  pois a caixa de diálogo Instalação Concluída só poderá ser mostrada se Executar jogo após a instalação ter sido deseleitada na caixa de diálogo **Opções de** Instalação. 
-   O **botão OK** descarta a caixa de  diálogo, opcionalmente, em ação nas caixas de seleção Executar e Exibir o **Leiame.**

## <a name="summary"></a>Resumo

Os jogadores querem jogar um jogo assim que possível. A última coisa que um jogador deseja fazer é passar pelas caixas de diálogo e fazer escolhas que sejam as mesmas para todos os outros jogos que ele instalou. Implementar essas ideias pode reduzir a quantidade de tempo que um jogador gasta instalando um jogo no Windows e ajudar a melhorar a qualidade geral da experiência de Windows jogos.

 

 