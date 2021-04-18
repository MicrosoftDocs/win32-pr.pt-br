---
title: Firewall do Windows para Desenvolvedores de Jogos
description: Este artigo descreve o Firewall do Windows – por que ele existe, o que é realizado e como ele faz isso. O mais importante é que ele descreve como configurar seu jogo para funcionar bem com o firewall.
ms.assetid: 2ee9f769-03dc-3661-5d5b-6a4ecd151fd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88656fb3f622a847c15544646c333b807f3a0fb2
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104506365"
---
# <a name="windows-firewall-for-game-developers"></a>Firewall do Windows para Desenvolvedores de Jogos

Este artigo descreve o Firewall do Windows – por que ele existe, o que é realizado e como ele faz isso. O mais importante é que ele descreve como configurar seu jogo para funcionar bem com o firewall.

Conteúdo:

-   [O que é um firewall?](#what-is-a-firewall)
-   [Como saber se meu jogo foi afetado?](#how-can-i-tell-if-my-game-is-affected)
-   [O firewall antes do Windows XP SP2](#the-firewall-before-windows-xp-sp2)
-   [O Firewall do Windows XP SP2 é melhor](#windows-xp-sp2-firewall-is-better)
-   [Trabalhando com o Firewall do Windows](#working-with-the-windows-firewall)
-   [Integração usando o InstallShield InstallScript](#integrating-using-installshield-installscript)
-   [Integrando-se ao Wise para Windows Installer](#integrating-into-wise-for-windows-installer)
-   [Integrando-se ao Windows Installer](#integrating-into-windows-installer)
-   [Recomendações](#recommendations)

## <a name="what-is-a-firewall"></a>O que é um firewall?

O firewall fornece uma barreira contra invasões baseadas em rede. Ele bloqueia o tráfego de entrada não solicitado e torna o sistema praticamente invisível na Internet, rejeitando as solicitações do protocolo ICMP. Isso significa que ping e tracert não funcionarão. O firewall também procura e rejeita pacotes inválidos.

Essa barreira impede ataques oportunistas. Os ataques se disseminam encontrando vários sistemas com a mesma vulnerabilidade. O firewall pode impedir muitos ataques, colocando um sinal de "não incomodar" para esses recursos que não estão em uso no momento; o ataque é ignorado e não está em casa. O benefício essencial do firewall do Windows é que os recursos e aplicativos que não estão em uso não podem ser caminhos para ataques.

O usuário configura o sistema para identificar quais aplicativos e recursos são necessários e devem ser abertos na rede. Isso ocorre quando um aplicativo é instalado ou quando tenta se abrir para a rede.

## <a name="how-can-i-tell-if-my-game-is-affected"></a>Como saber se meu jogo foi afetado?

Com a chegada do Windows XP SP2, o Firewall do Windows foi amplamente implantado. Todos os jogos do Windows com vários participantes são afetados em certo grau. Embora os clientes geralmente estejam em boa forma, os servidores, os hosts e os pares em ponto a ponto precisam do firewall configurado para continuar trabalhando. Especificamente, o tráfego de entrada não solicitado é Descartado. O firewall intercepta pacotes de filtro de tráfego de rede com base no conteúdo do pacote e na atividade de rede recente. O firewall usa o conteúdo e a atividade para decidir encaminhar ou descartar um pacote. Depois que o firewall estiver configurado corretamente, um jogo poderá aceitar o tráfego de entrada não solicitado como antes.

Quem tem tráfego de entrada não solicitado?

-   Cliente/servidor: todos os participantes se conectam a um servidor central. O servidor central é aquele com tráfego de entrada não solicitado. Os clientes que se conectam ao servidor estão solicitando o tráfego de retorno, que é esperado e têm permissão para passar pelo firewall se as regras para os clientes forem seguidas. O servidor central deve ser configurado para aceitar o tráfego não solicitado para permitir que o tráfego do cliente passe pelo firewall.
-   Vários multiplayer (MMP): todos os participantes estão conectados a um data center. Isso resulta em uma relação complexa de cliente/servidor, pois o data center tem o tráfego de entrada não solicitado. Os participantes são clientes e, em geral, não precisam aceitar tráfego não solicitado.
-   Ponto a ponto, em que todos os participantes estão conectados entre si diretamente: todos os participantes devem estar prontos para aceitar o tráfego não solicitado de qualquer novo jogador ingressando no grupo. De certa forma, cada um dos participantes deve funcionar como um host, portanto, eles devem ser configurados como se fossem hosts.

Os clientes geralmente estão em bom formato. Suas conexões TCP/IP (protocolo de controle de transmissão) de saída funcionarão bem, assim como mensagens de UDP (protocolo de datagrama do usuário) de saída junto com respostas oportunas para essas mensagens – o firewall mantém a porta aberta por 90 segundos após cada mensagem de saída na previsão de uma resposta.

## <a name="the-firewall-before-windows-xp-sp2"></a>O firewall antes do Windows XP SP2

O firewall de conexão com a Internet (ICF) no Windows XP e no Windows Server 2003 é um filtro de pacote com estado e lida com protocolo IP, versão 4 (IPv4) e protocolo IP, versão 6 (IPv6). No entanto, ela não é ativada por padrão e não oferece suporte a pilhas de rede de terceiros, das quais há um número significativo no mundo, como grandes provedores de Internet, incluindo empresas telefônicas nacionais.

Para aqueles que não estão no Windows XP SP2, é altamente recomendável ativar o ICF. Consulte as instruções "usar um firewall de Internet" em https://www.microsoft.com/security/protect como a primeira etapa para proteger seu PC. O firewall de conexão com a Internet (ICF) fornece o mapeamento de porta para substituir o filtro de pacote. Essencialmente, você especifica a porta a ser aberta e permanece aberta até que você a feche. Se o usuário for reinicializado antes de ser fechado, ele permanecerá aberto até ser fechado especificamente. O controle do firewall e o gerenciamento dos mapeamentos de porta são feitos via [**INetSharingManager**](/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingmanager) (IPv4) e [**INetFwV6Mgr**](/previous-versions/windows/desktop/ics/inetfwv6mgr) (IPv6).

O Firewall do Windows para Windows XP SP2 é uma solução mais abrangente que oferece suporte a pilhas de rede de terceiros e trata as portas de forma mais inteligente: as portas são mantidas abertas somente contanto que o aplicativo que precisa delas ainda esteja ativo.

## <a name="windows-xp-sp2-firewall-is-better"></a>O Firewall do Windows XP SP2 é melhor

O Windows XP SP2 coloca as opções de segurança e as configurações na frente. O objetivo é proteger por padrão e permitir que o usuário faça escolhas informadas sobre quais aplicativos podem ser executados em seu computador.

O novo Firewall do Windows está disponível no Windows XP SP2 e no Windows Server 2003 Service Pack 1 (SP1). Como o ICF, trata-se de um firewall de software que dá suporte a IPv4 e IPv6, mas, ao contrário do ICF, o Firewall do Windows:

-   Tem proteção de tempo de inicialização do sistema, eliminando uma pequena janela de vulnerabilidade durante a inicialização.
-   Dá suporte a pilhas de rede de terceiros.
-   Tem um modo "on sem exceções" que bloqueia todos os pacotes de entrada não solicitados. Isso é ótimo quando você está usando uma rede pública, como em um aeroporto ou cafeteria.

No modo "on sem exceções", todos os buracos estáticos são fechados. As chamadas à API para abrir uma brecha estática são permitidas, mas adiadas; ou seja, eles não são aplicados até que o firewall volte para a operação normal. Todas as solicitações de escuta por aplicativos também serão ignoradas. As conexões de saída ainda terão sucesso.

Para novos aplicativos, adicione seu aplicativo à "lista de exceções" durante a instalação. Você pode adicionar o aplicativo usando a interface [**INetFwAuthorizedApplications**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications) , fornecendo o caminho completo. Abordaremos os detalhes no exemplo.

Como uma observação adicional, você deve estar se perguntando se é um risco de segurança que os aplicativos podem adicionar e remover aplicativos da lista de exceções, qualquer intervenção do usuário, ou talvez você ache que o maior risco é que os aplicativos possam desabilitar completamente o firewall. Para executar essas realizações, o aplicativo deve ter privilégios de administrador. Se você tiver um código mal-intencionado em execução no modo de administrador em seu sistema, o jogo já estará acima e o hacker já ganhou. A capacidade do hacker de desabilitar o firewall seria um pouco mais do que uma nota de rodapé.

Aplicativos herdados, incluindo aplicativos instalados antes da atualização do usuário para o Windows XP SP2, são tratados com o pop-up lista de exceções (consulte a Figura 1). Essa caixa de diálogo mostra quando um aplicativo tenta abrir uma porta para o tráfego de entrada-seja ao chamar Bind () com uma porta diferente de zero para UDP ou Accept () para o protocolo TCP/IP. Você deve estar executando como administrador para aplicativos "desbloquear", enquanto "perguntar mais tarde" não permite esse tempo, mas pergunta novamente na próxima vez.

Esta é uma caixa de diálogo modal do sistema que não é de bloqueio. Ao executar um aplicativo Microsoft Direct3D em tela inteira, a caixa de diálogo entra em baixo; e o usuário pode tratá-lo quando o aplicativo sai do modo de tela inteira ou das guias Alt-back para a área de trabalho. No entanto, nem sempre é óbvio para o usuário que essa caixa de diálogo apareceu quando um jogo está executando a tela inteira, portanto, é importante evitar fazer com que essa caixa de diálogo apareça usando a interface [**INetFwAuthorizedApplications**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications) , conforme discutido abaixo.

**Figura 1. Caixa de diálogo pop-up lista de exceções**

![caixa de diálogo pop-up lista de exceções](images/firewalls1.jpg)

Você observará que o Popup sabe o nome e o editor do aplicativo. Não há mágica aqui-ela foi extraída das informações de versão do executável. Essas informações são uma ferramenta de administração de sistema importante; Ele é até mesmo usado para o trabalho de compatibilidade de aplicativos em andamento. Alguns aplicativos desaparecem para manter essas informações de versão atualizadas.

Os usuários também podem adicionar seus aplicativos por meio da interface do usuário (veja a Figura 2)

**Figura 2. Configurando o firewall**

![Configurando o firewall](images/firewalls2.jpg)

**Figura 3. Adicionando um programa à lista de exceções de firewall**

![adicionando um programa à lista de exceções de firewall](images/firewalls3.jpg)

O melhor cenário é fazer adições e remoções da lista de exceções automatizadas. O melhor momento para executar essas adições e remoções é durante o processo de instalação e desinstalação. Adicionar ou remover da lista de exceções de firewall requer privilégios de administrador, portanto, lembre-se de levar isso em conta.

## <a name="working-with-the-windows-firewall"></a>Trabalhando com o Firewall do Windows

Novamente, a maioria dos jogos só precisará ser adicionada à lista de exceções do firewall se ele puder funcionar como um servidor ou se implementar um protocolo de comunicação ponto a ponto. O FirewallInstallHelper.dll é um exemplo de DLL que pode ser chamado a partir de um instalador. A origem será fornecida se você quiser integrar a fonte diretamente em seu próprio aplicativo. O exemplo pode ser encontrado aqui:



|             |                                                                              |
|-------------|------------------------------------------------------------------------------|
| Origem:     | (Raiz do SDK) \\ Exemplos de \\ FirewallInstallHelper de C++ \\ misc \\                        |
| Executável: | (Raiz do SDK) \\ Amostras \\ de \\ \\ \\ <arch> \\FirewallInstallHelper.dll misc bin do C++ |



 

As funções exportadas por essa DLL são as seguintes:

<dl> <dt>

<span id="AddApplicationToExceptionListW"></span><span id="addapplicationtoexceptionlistw"></span><span id="ADDAPPLICATIONTOEXCEPTIONLISTW"></span>**AddApplicationToExceptionListW**
</dt> <dd>

Essa função adiciona um aplicativo à lista de exceções. Ele usa um caminho completo para o executável e um nome amigável que será exibido na lista de exceção do firewall. Essa função requer privilégios de administrador.

</dd> <dt>

<span id="AddApplicationToExceptionListA"></span><span id="addapplicationtoexceptionlista"></span><span id="ADDAPPLICATIONTOEXCEPTIONLISTA"></span>**AddApplicationToExceptionListA**
</dt> <dd>

Versão ANSI do **AddApplicationToExceptionListW**

</dd> <dt>

<span id="RemoveApplicationFromExceptionListW"></span><span id="removeapplicationfromexceptionlistw"></span><span id="REMOVEAPPLICATIONFROMEXCEPTIONLISTW"></span>**RemoveApplicationFromExceptionListW**
</dt> <dd>

Essa função remove o aplicativo da lista de exceções. Ele usa um caminho completo para o executável. Esta função requer privilégios de administrador

</dd> <dt>

<span id="RemoveApplicationFromExceptionListA"></span><span id="removeapplicationfromexceptionlista"></span><span id="REMOVEAPPLICATIONFROMEXCEPTIONLISTA"></span>**RemoveApplicationFromExceptionListA**
</dt> <dd>

Versão ANSI do **RemoveApplicationFromExceptionListW**

</dd> <dt>

<span id="CanLaunchMultiplayerGameW"></span><span id="canlaunchmultiplayergamew"></span><span id="CANLAUNCHMULTIPLAYERGAMEW"></span>**CanLaunchMultiplayerGameW**
</dt> <dd>

Essa função relata se o aplicativo foi desabilitado ou removido da lista de exceções. Ele deve ser chamado toda vez que o jogo for executado. A função usa um caminho completo para o executável. Essa função não requer privilégios de administrador.

</dd> <dt>

<span id="CanLaunchMultiplayerGameA"></span><span id="canlaunchmultiplayergamea"></span><span id="CANLAUNCHMULTIPLAYERGAMEA"></span>**CanLaunchMultiplayerGameA**
</dt> <dd>

Versão ANSI do **CanLaunchMultiplayerGameW**

</dd> <dt>

<span id="SetMSIFirewallProperties"></span><span id="setmsifirewallproperties"></span><span id="SETMSIFIREWALLPROPERTIES"></span>**SetMSIFirewallProperties**
</dt> <dd>

Chame isso somente se você estiver usando ações personalizadas no Windows Installer. Consulte abaixo para obter mais detalhes.

</dd> <dt>

<span id="AddToExceptionListUsingMSI"></span><span id="addtoexceptionlistusingmsi"></span><span id="ADDTOEXCEPTIONLISTUSINGMSI"></span>**AddToExceptionListUsingMSI**
</dt> <dd>

Chame isso somente se você estiver usando ações personalizadas no Windows Installer. Consulte abaixo para obter mais detalhes.

</dd> <dt>

<span id="RemoveFromExceptionListUsingMSI"></span><span id="removefromexceptionlistusingmsi"></span><span id="REMOVEFROMEXCEPTIONLISTUSINGMSI"></span>**RemoveFromExceptionListUsingMSI**
</dt> <dd>

Chame isso somente se você estiver usando ações personalizadas no Windows Installer. Consulte abaixo para obter mais detalhes.

</dd> </dl>

As seções a seguir descrevem métodos específicos de chamar as funções de DLL exportadas desse FirewallInstallHelper de dentro de um pacote InstallShield, Wise ou Windows Installer. Todos os métodos renderizam os mesmos resultados e cabe ao desenvolvedor determinar qual método implementar.

## <a name="integrating-using-installshield-installscript"></a>Integração usando o InstallShield InstallScript

Um método alternativo de usar as APIs de firewall é adicionar as chamadas de função a um InstallScript do InstallShield. As etapas necessárias para integrar são bem simples:

1.  Abra um projeto do InstallScript no editor do InstallShield.
2.  Adicione o FirewallInstallHelper.dll ao projeto como um arquivo de suporte.

    1.  Na guia Assistente de projeto, abra a guia arquivos de aplicativo.
    2.  Clique no botão Adicionar arquivos para adicionar arquivos à pasta de destino do aplicativo.
    3.  Navegue até o FirewallInstallHelper.dll que você criou ou usou aquele fornecido no SDK do DirectX e adicione-o ao projeto.

3.  Adicione o InstallScript ao projeto.

    1.  Abra a exibição do designer de instalação e clique no comportamento e na lógica do \| InstallScript
    2.  Clique no arquivo InstallScript (geralmente setup. RUL) para abri-lo no editor
    3.  Cole o seguinte código no arquivo InstallScript:

    ``` syntax
    #include "ifx.h"

    prototype BOOL FirewallInstallHelper.AddApplicationToExceptionListW( WSTRING, WSTRING );
    prototype BOOL FirewallInstallHelper.RemoveApplicationFromExceptionListW( WSTRING );

    function OnMoved()
        WSTRING path[256];
    begin
        // The DLL has been installed into the TARGETDIR
        if !MAINTENANCE then // TRUE when installing
            UseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
            path = TARGETDIR ^ "TODO: change to relative path to executable from install directory";
            FirewallInstallHelper.AddApplicationToExceptionListW( path, "TODO: change to friendly app name" );
            UnUseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
        endif;
    end;
          

    function OnMoving()
        WSTRING path[256];
    begin
        // The DLL is about to be removed from TARGETDIR
        if MAINTENANCE && UNINST != "" then // TRUE when uninstalling
            UseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
            path = TARGETDIR ^ "TODO: change to relative path to executable from install directory";
            FirewallInstallHelper.RemoveApplicationFromExceptionListW( path );
            UnUseDLL( TARGETDIR ^ "FirewallInstallHelper.dll" );
        endif;
    end;
    ```

    4.  Altere os comentários de tarefas pendentes com o nome do aplicativo que será mostrado na lista de exceção do firewall e o caminho para o executável do jogo em relação ao diretório de instalação.

## <a name="integrating-into-wise-for-windows-installer"></a>Integrando-se ao Wise para Windows Installer

Para integrar com o Wise for Windows Installer, estas etapas devem ser feitas:

1.  Abra seu Wise para Windows Installer projeto.
2.  Selecione a guia "especialista em instalação" na parte inferior.
3.  Clique em arquivos e adicione o FirewallInstallHelper.dll do DXSDK ao diretório de instalação do jogo.
4.  Selecione a guia "script MSI" na parte inferior.
5.  Selecione a guia "executar imediatamente" perto da parte inferior.
6.  Após CostFinalize, adicione uma ação "definir propriedade" que define o FULLPATH como \[ " \] caminho relativo de installdir para executável do diretório de instalação". Por exemplo, " \[ INSTALLDIR \]game.exe" sem as aspas
7.  Selecione a guia "executar adiada" perto da parte inferior.
8.  Após PublishProduct, adicione uma "instrução If" com a condição "não instalado" (diferencia maiúsculas de minúsculas).
9.  No bloco If, adicione uma ação "chamar DLL personalizada do destino".

    1.  Defina o campo de arquivo DLL como " \[ INSTALLDIR \]FirewallInstallHelper.dll".
    2.  Defina o campo nome da função como "AddApplicationToExceptionListA".
    3.  Adicione um parâmetro com o tipo "ponteiro de cadeia de caracteres", fonte de valor "Propriedade" e nome da propriedade "FULLPATH".
    4.  Adicione um segundo parâmetro com o tipo "ponteiro de cadeia de caracteres", fonte de valor "constante" e defina o valor constante como o nome de aplicativo amigável que você deseja exibir na lista de exceção do firewall.
    5.  Feche o bloco If adicionando uma "instrução End".

10. Logo acima da ação removidas próxima à parte superior, adicione outro bloco If, com a condição para ser "REMOVE ~ =" ALL "" (diferencia maiúsculas de minúsculas e sem as aspas externas).
11. No segundo bloco If, adicione uma ação "chamar DLL personalizada do destino".

    1.  Defina o campo de arquivo DLL como " \[ INSTALLDIR \]FirewallInstallHelper.dll".
    2.  Defina o campo nome da função como "RemoveApplicationFromExceptionListA".
    3.  Adicione um parâmetro com o tipo "ponteiro de cadeia de caracteres", fonte de valor "Propriedade" e nome da propriedade "FULLPATH".
    4.  Feche o segundo bloco If adicionando uma "instrução End".

## <a name="integrating-into-windows-installer"></a>Integrando-se ao Windows Installer

Para integrar com Windows Installer no alto nível, essas etapas devem ser feitas. Eles serão explicados em detalhes abaixo:

-   Adicione 2 Propriedades "FriendlyNameForFirewall" e "RelativePathToExeForFirewall" conforme descrito abaixo.
-   Após a ação CostFinalize, chame "SetMSIFirewallProperties" em uma ação personalizada imediata para definir as propriedades apropriadas do MSI para as outras ações personalizadas.
-   Durante a instalação após a ação InstallFiles, chame uma ação personalizada adiada que usa a função "AddToExceptionListUsingMSI" do FirewallInstallHelper.
-   Durante a desinstalação após a ação InstallFiles, chame uma ação personalizada adiada que usa a função "RemoveFromExceptionListUsingMSI" do FirewallInstallHelper.
-   Durante a reversão, chame uma ação personalizada adiada que também chama a função "RemoveFromExceptionListUsingMSI" do FirewallInstallHelper.

Veja a seguir as etapas necessárias para fazer isso usando um editor MSI, como o orca, encontrado no SDK da plataforma. Observe que alguns editores têm assistentes que simplificam algumas dessas etapas:

1.  Abra o pacote MSI em orca.
2.  Adicione o seguinte à tabela binária:

    

    | Nome     | Dados                                                                                                                                                                          |
    |----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | FIREWALL | Aponte para a FirewallInstallHelper.dll. Esse arquivo será inserido no pacote MSI, de modo que você terá que fazer essa etapa sempre que recompilar FirewallInstallHelper.dll. |

    

     

3.  Adicione o seguinte à tabela CustomAction:

    

    | Ação                   | Tipo                                                                                                                                                                                                   | Fonte   | Destino                          |
    |--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|---------------------------------|
    | FirewallSetMSIProperties | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65                                                                                                        | FIREWALL | SetMSIFirewallProperties        |
    | FirewallAdd              | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | FIREWALL | AddToExceptionListUsingMSI      |
    | FirewallRemove           | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | FIREWALL | RemoveFromExceptionListUsingMSI |
    | FirewallRollBackAdd      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | FIREWALL | RemoveFromExceptionListUsingMSI |
    | FirewallRollBackRemove   | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | FIREWALL | AddToExceptionListUsingMSI      |

    

     

4.  Adicione o seguinte à tabela InstallExecuteSequence:

    

    | Ação                   | Condição     | Sequência | Observações                                                                                                                                                                      |
    |--------------------------|---------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | FirewallSetMSIProperties |               | 1010     | Isso é colocado logo após CostFinalize.                                                                                                                                       |
    | FirewallAdd              | NÃO instalado | 4021     | Essa ação personalizada só ocorrerá durante uma instalação nova. O número de sequência coloca a ação após InstallFiles e após as reversões.                              |
    | FirewallRollBackAdd      | NÃO instalado | 4020     | Essa ação personalizada ocorrerá somente quando uma instalação nova for cancelada. O número de sequência coloca a ação após InstallFiles e antes da ação de adicionar Personalizada.          |
    | FirewallRemove           | Instalado     | 3461     | Esta ação personalizada só ocorrerá durante a desinstalação. O número de sequência coloca a ação diretamente antes de removes e após as reversões.                           |
    | FirewallRollBackRemove   | NÃO instalado | 3460     | Essa ação personalizada ocorrerá somente quando uma desinstalação for cancelada. O número de sequência coloca a ação diretamente antes de removidas e antes da ação personalizada de remoção. |

    

     

5.  Adicione o seguinte à tabela de propriedades:

    

    | Propriedade                     | Valor                                                                             |
    |------------------------------|-----------------------------------------------------------------------------------|
    | FriendlyNameForFirewall      | Precisa ser o nome que a lista de exceções exibirá. Por exemplo, "jogo de exemplo" |
    | RelativePathToExeForFirewall | Precisa ser o executável do jogo instalado. Por exemplo, "ExampleGame.exe"  |

    

     

Para obter mais informações sobre Windows Installer, consulte [Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="recommendations"></a>Recomendações

O firewall está aqui para permanecer. Essas recomendações darão aos seus clientes uma boa experiência de firewall com seu jogo do Windows:

-   Não diga aos usuários para desabilitar o firewall para reproduzir o jogo. Isso torna todo o computador vulnerável mesmo quando eles não estão jogando no jogo.
-   Tornar a configuração do firewall direta para seus usuários. Adicione seu aplicativo à lista de exceções durante a instalação e remova seu aplicativo da lista de exceções durante a instalação.
-   Forneça comentários para o usuário se os vários jogadores estiverem bloqueados pelo estado do firewall. Por exemplo, desabilite os recursos de rede se eles não funcionarem porque o aplicativo não é permitido ou porque o sistema está no modo "sem exceções".

 

 