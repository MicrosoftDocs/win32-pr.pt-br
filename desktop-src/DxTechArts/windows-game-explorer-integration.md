---
title: Windows Explorador de jogos para desenvolvedores de jogos
description: este artigo descreve o processo de registro de um jogo com o explorador de jogos e controles dos pais em Windows Vista e Windows 7 usando o novo esquema GDF.
ms.assetid: 628f14bf-2714-0d68-8267-4f7f48c2774a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6420b4783cfad7afd82483d45448ccb219342b4a7b88aa54e36c2de15ca0f778
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070416"
---
# <a name="windows-games-explorer-for-game-developers"></a>Windows Explorador de jogos para desenvolvedores de jogos

Windows o Vista melhora a experiência do usuário em jogos em Windows, incluindo o explorador de jogos. o explorador de jogos é exposto no Menu iniciar do Windows Vista como a pasta jogos e fornece um local central para acessar jogos.

a partir da versão de março de 2009 do SDK do DirectX, um novo esquema de GDF (arquivo de definição de jogo) é usado para dar suporte a recursos no Windows 7, provedor de jogos e RSS feed e IGameExplorer2. o IGameExplorer2 é uma nova interface no Windows 7 que simplifica o processo de integração de um jogo com o explorador de jogos.

este artigo descreve o processo de registro de um jogo com o explorador de jogos e controles dos pais em Windows Vista e Windows 7 usando o novo esquema GDF.

Conteúdo:

-   [Pré-requisitos](#prerequisites)
-   [Integração com um instalador](#integrating-with-an-installer)
-   [Processo de integração](#integration-process)
-   [Tarefas do explorador de jogos](#games-explorer-tasks)
-   [Integrando no InstallScript](#integrating-into-installscript)
-   [Integrando-se a um pacote MSI](#integrating-into-an-msi-package)
-   [Dicas de depuração](#debugging-tips)
    -   [Teste com código de exemplo](#test-with-sample-code)
    -   [Certifique-se de que seu jogo foi removido corretamente](#make-sure-that-your-game-was-removed-properly)
    -   [Não se esqueça de assinar usando Authenticode](#be-sure-to-sign-using-authenticode)
    -   [Verifique se os controles dos pais estão disponíveis](#be-sure-that-parental-controls-are-available)
    -   [Verificar se as tarefas são do tipo correto](#verify-that-tasks-are-of-the-correct-type)
    -   [Verificar os dados no binário GDF](#verify-the-data-in-gdf-binary)
-   [Resumo](#summary)

## <a name="prerequisites"></a>Pré-requisitos

Para poder integrar um jogo no explorador de jogos, você deve criar um arquivo de definição de jogo (GDF). Um GDF é um arquivo XML que contém metadados que descrevem o jogo. Na versão de março de 2009 do SDK do DirectX, uma seção para o provedor de jogos, o RSS feed e a tarefa de jogo foram adicionados ao esquema GDF. Para usar as instruções neste artigo, você deve usar esse novo formato GDF para criar o arquivo GDF.

A Microsoft fornece uma ferramenta para a criação de GDFs no SDK do DirectX, editor de arquivos de definição de jogos, para facilitar esse processo de criação. Essa ferramenta também ajuda a criar versões localizadas de um GDF.

Depois que um GDF tiver sido criado e localizado, ele deverá ser encapsulado dentro de uma seção de recurso de um arquivo binário (executável ou DLL), junto com a miniatura e o ícone do jogo. O GDF contém todos os metadados associados ao jogo, incluindo a classificação do jogo. Windows Os controles dos pais usam a classificação do jogo para permitir que os pais controlem o acesso ao jogo. O arquivo binário que contém o GDF deve ser assinado digitalmente com um certificado Authenticode válido; caso contrário, o explorador de jogos e o sistema de controle de pais ignoram a classificação do jogo, pois as informações de classificação não podem ser confiáveis sem certificação. Para obter mais detalhes sobre o código de assinatura com Authenticode, consulte [assinatura Authenticode para desenvolvedores de jogos](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).

## <a name="integrating-with-an-installer"></a>Integração com um instalador

para simplificar a integração do explorador de jogos, o exemplo GameUXInstallHelper fornece uma API comum que pode ser chamada em Windows XP, Windows Vista e Windows 7. Ele foi projetado para trabalhar com scripts para o sistema de instalação do InstallShield e Wise, bem como ações personalizadas do MSI e ferramentas de instalação personalizadas. a detecção do sistema operacional é tratada dentro dessa DLL de exemplo, portanto, o chamador não precisa se preocupar se o cliente está executando o Windows XP, Windows Vista ou Windows 7.

As funções exportadas por essa DLL são as seguintes:

<dl> <dt>

<span id="GameExplorerInstallW"></span><span id="gameexplorerinstallw"></span><span id="GAMEEXPLORERINSTALLW"></span>**GameExplorerInstallW**
</dt> <dd>

Registra um jogo com o explorador de jogos, dado um caminho para o binário GDF, um caminho completo para a pasta em que o jogo está instalado e o escopo da instalação.

</dd> <dt>

<span id="GameExplorerInstallA"></span><span id="gameexplorerinstalla"></span><span id="GAMEEXPLORERINSTALLA"></span>**GameExplorerInstallA**
</dt> <dd>

Registra um jogo com o explorador de jogos; Versão ANSI do **GameExplorerInstallW**.

</dd> <dt>

<span id="GameExplorerUninstallW"></span><span id="gameexploreruninstallw"></span><span id="GAMEEXPLORERUNINSTALLW"></span>**GameExplorerUninstallW**
</dt> <dd>

Remove um jogo do registro com o explorador de jogos, dado um caminho para o binário GDF.

</dd> <dt>

<span id="GameExplorerUninstallA"></span><span id="gameexploreruninstalla"></span><span id="GAMEEXPLORERUNINSTALLA"></span>**GameExplorerUninstallA**
</dt> <dd>

Remove um jogo do registro com o explorador de jogos; Versão ANSI do **GameExplorerUninstallW**.

</dd> <dt>

<span id="GameExplorerSetMSIProperties"></span><span id="gameexplorersetmsiproperties"></span><span id="GAMEEXPLORERSETMSIPROPERTIES"></span>**GameExplorerSetMSIProperties**
</dt> <dd>

Configura as propriedades CustomActionData para as ações de uma instalação personalizada adiada do MSI. O uso dessa função é descrito em detalhes posteriormente neste artigo.

</dd> <dt>

<span id="GameExplorerInstallUsingMSI"></span><span id="gameexplorerinstallusingmsi"></span><span id="GAMEEXPLORERINSTALLUSINGMSI"></span>**GameExplorerInstallUsingMSI**
</dt> <dd>

Adiciona um jogo ao explorador de jogos; para uso durante uma instalação de ação personalizada do MSI.

</dd> <dt>

<span id="GameExplorerUninstallUsingMSI"></span><span id="gameexploreruninstallusingmsi"></span><span id="GAMEEXPLORERUNINSTALLUSINGMSI"></span>**GameExplorerUninstallUsingMSI**
</dt> <dd>

Remover um jogo do explorador de jogos; para uso durante uma instalação de ação personalizada do MSI.

</dd> </dl>

Essas funções são explicadas ainda mais no cabeçalho GameUXInstallHelper. h.

## <a name="integration-process"></a>Processo de integração

Depois que o GDF e os arquivos relacionados tiverem sido adicionados a um recurso binário, será possível integrar o jogo ao explorador de jogos. O uso do **GameUXInstallHelper** simplificará o processo de integração. Para registrar o jogo no explorador de jogos, chame o **GameExplorerInstall** com um caminho para o binário GDF, um caminho completo para a pasta em que o jogo está instalado e o escopo de instalação. Para remover o registro do jogo, chame **GameExplorerUninstall** com um caminho para o binário GDF.

Observe que o processo de remoção remove apenas uma instalação exclusiva. Se um jogo tiver sido instalado várias vezes, esse processo deverá ser repetido para cada instalação exclusiva.

## <a name="games-explorer-tasks"></a>Tarefas do explorador de jogos

As tarefas do explorador de jogos serão exibidas no menu de contexto de um item no explorador de jogos. As tarefas são divididas em tarefas de reprodução e tarefas de suporte. As tarefas de reprodução iniciam um jogo em um modo específico, enquanto as tarefas de suporte atendem a qualquer outra finalidade, incluindo a vinculação a sites da Web.

no Windows Vista, as tarefas são simplesmente atalhos que estão localizados em pastas específicas. Tarefas de reprodução e tarefas de suporte são armazenadas em pastas com os nomes correspondentes PlayTasks e SupportTasks. GameUXInstallHelper pode ler as informações sobre a tarefa do jogo do arquivo binário GDF e criar todos os atalhos automaticamente.

no Windows 7, os atalhos para as tarefas não são necessários, pois o explorador de jogos obtém todas as informações da tarefa diretamente do arquivo binário GDF.

## <a name="integrating-into-installscript"></a>Integrando no InstallScript

Chamar APIs do explorador de jogos do InstallScript do InstallShield é facilitado usando o exemplo GameUXInstallHelper. As etapas necessárias para a integração com o InstallShield são as seguintes:

1.  Abra um projeto do InstallScript no editor do InstallShield.
2.  Adicione GameUXInstallHelper.dll ao projeto a ser instalado no diretório de destino.

    **Para adicionar GameUXInstallHelper.dll a um projeto de InstallScript:**

    1.  Na guia **Designer de instalação** , clique em **dados do aplicativo** no painel de navegação à esquerda.
    2.  Clique em **arquivos e pastas** e procure nas **pastas do computador de origem** para localizar GameUXInstallerHelper.dll nos **arquivos do computador de origem**.

        O local padrão para GameUXInstallerHelper.dll é o DirectX SDK root \\ Samples \\ C++ \\ misc \\ bin \\ x86.

    3.  Em **pastas do computador de destino**, clique em **pasta de destino do aplicativo**.
    4.  Arraste GameUXInstallerHelper.dll dos **arquivos do computador de origem** para **os arquivos do computador de destino**.

3.  No Gerenciador de InstallScript, clique no arquivo InstallScript (geralmente setup. RUL) que chama a função DLL.
4.  Cole o seguinte InstallScript no arquivo:

    ``` syntax
    typedef GUID
    begin
    LONG  Data1;
    SHORT Data2;
    SHORT Data3;
    CHAR  Data4(8);
    end;

    prototype LONG GameUXInstallHelper.GameExplorerInstallW(WSTRING, WSTRING, NUMBER);
    prototype LONG GameUXInstallHelper.GameExplorerUninstallW(WSTRING);

    function OnMoved()

    WSTRING gdfbin[256];
    WSTRING path[256];
    NUMBER scope;

    begin

    if !MAINTENANCE then

    UseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UseDLL( WINSYSDIR ^ "OLE32.dll" );

    path = TARGETDIR;
    gdfbin = TARGETDIR ^ "bin\\ExampleGame.exe";  // TODO: Change this to point to binary containing the GDF

    if ALLUSERS == 1 then
    scope = 3;
    else
    scope = 2;
    endif;

    GameUXInstallHelper.GameExplorerInstallW( gdfbin, path, scope);

    UnUseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UnUseDLL( WINSYSDIR ^ "OLE32.dll" );

    endif;

    end;

    function OnMoving()

    WSTRING gdfbin[256];

    begin

    if MAINTENANCE && UNINST != "" then

    UseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UseDLL( WINSYSDIR ^ "OLE32.dll" );

    gdfbin = path ^ "bin\\ExampleGame.exe";  // TODO: Change this to point to binary containing the GDF

    GameUXInstallHelper.GameExplorerUninstallW(gdfbin);
    UnUseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UnUseDLL( WINSYSDIR ^ "OLE32.dll" );

    endif;

    end;
    ```

## <a name="integrating-into-an-msi-package"></a>Integrando-se a um pacote MSI

Veja a seguir uma descrição de alto nível das etapas necessárias para chamar as APIs do explorador de jogos usando as ações personalizadas do MSI:

1.  Adicione uma propriedade à tabela de propriedades do MSI chamada "RelativePathToGDF" contendo o caminho relativo para o binário GDF.
2.  Após a ação CostFinalize, chame a função GameUXInstallHelper DLL **SetMSIGameExplorerProperties** em uma ação personalizada imediata para definir as propriedades apropriadas do MSI para as outras ações personalizadas.
3.  Após a instalação, dispare uma ação personalizada adiada após a ação InstallFiles que chama a função GameUXInstallHelper DLL **AddToGameExplorerUsingMSI**. Se a instalação for para todos os usuários, a ação personalizada deverá definir o sinalizador msidbCustomActionTypeNoImpersonate; caso contrário, ele não deve definir esse sinalizador. Portanto, duas ações personalizadas quase idênticas são definidas: GameUXAddAsAdmin e GameUXAddAsCurUser.
4.  Após a remoção da instalação, dispare uma ação personalizada adiada antes da ação removida que chama a função GameUXInstallHelper DLL **RemoveFromGameExplorerUsingMSI**. Se a instalação for para todos os usuários, a ação personalizada deverá definir o sinalizador msidbCustomActionTypeNoImpersonate; caso contrário, ele não deve definir esse sinalizador. Portanto, duas ações personalizadas quase idênticas são definidas: GameUXRemoveAsAdmin e GameUXRemoveAsCurUser.
5.  Defina reversão de ações personalizadas para lidar com o caso em que o usuário cancelar a instalação ou remoção depois que uma das ações personalizadas já tiver acontecido. Isso resulta em quatro ações personalizadas adicionais: GameUXRollBackAddAsAdmin, GameUXRollBackAddAsCurUser, GameUXRollBackRemoveAsAdmin e GameUXRollBackRemoveAsCurUser.

Esse procedimento é descrito em detalhes nas instruções a seguir, que descrevem um processo que pode ser feito usando um editor de MSI, como o editor Orca encontrado no SDK da plataforma. Alguns editores MSI têm assistentes que simplificam algumas dessas etapas de configuração.

**Para configurar um pacote MSI para integração com o explorador de jogos**

1.  Abra o pacote MSI em orca.
2.  Adicione a linha mostrada na tabela a seguir à tabela **binária** no pacote MSI. 

    | Nome   | Dados                                          |
    |--------|-----------------------------------------------|
    | GAMEUX | caminho do arquivo para a DLL \\GameUXInstallHelper.dll |

    

     

    > [!Note]  
    > Esse arquivo será inserido no pacote MSI, portanto, você deve fazer essa etapa sempre que recompilar GameUXInstallHelper.dll.

     

3.  Adicione as linhas mostradas na tabela a seguir à tabela **CustomAction** no pacote MSI.

    | Ação                        | Tipo                                                                                                                                                                                                   | Fonte | Destino                         |
    |-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------|--------------------------------|
    | GameUXSetMSIProperties        | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65                                                                                                        | GAMEUX | SetMSIGameExplorerProperties   |
    | GameUXAddAsAdmin              | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | GAMEUX | AddToGameExplorerUsingMSI      |
    | GameUXAddAsCurUser            | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript = 1089                                                                      | GAMEUX | AddToGameExplorerUsingMSI      |
    | GameUXRollBackAddAsAdmin      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | GAMEUX | RemoveFromGameExplorerUsingMSI |
    | GameUXRollBackAddAsCurUser    | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript = 1345                                      | GAMEUX | RemoveFromGameExplorerUsingMSI |
    | GameUXRemoveAsAdmin           | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137                                 | GAMEUX | RemoveFromGameExplorerUsingMSI |
    | GameUXRemoveAsCurUser         | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript = 1089                                                                      | GAMEUX | RemoveFromGameExplorerUsingMSI |
    | GameUXRollBackRemoveAsAdmin   | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393 | GAMEUX | AddToGameExplorerUsingMSI      |
    | GameUXRollBackRemoveAsCurUser | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript = 1345                                      | GAMEUX | AddToGameExplorerUsingMSI      |

    

     

4.  Adicione os valores mostrados para ação, condição e sequência na tabela a seguir à tabela **InstallExecuteSequence** no pacote MSI.

    | Ação                        | Condição                      | Sequência | Observações                                                                                                                                                                                            |
    |-------------------------------|--------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | GameUXSetMSIProperties        |                                | 1015     | O número de sequência coloca a ação logo após CostFinalize.                                                                                                                                   |
    | GameUXAddAsAdmin              | NÃO instalado e ALLUSERS     | 4003     | Essa ação personalizada só ocorrerá durante uma nova instalação para todos os usuários. O número de sequência coloca a ação após InstallFiles e após as reversões.                                 |
    | GameUXAddAsCurUser            | NÃO instalado e não é ALLUSERS | 4004     | Essa ação personalizada só ocorrerá durante uma nova instalação para o usuário atual. O número de sequência coloca a ação após InstallFiles e após as reversões.                     |
    | GameUXRollBackAddAsAdmin      | NÃO instalado e ALLUSERS     | 4001     | Essa ação personalizada ocorrerá somente quando uma instalação nova para todos os usuários for cancelada. O número de sequência coloca a ação após InstallFiles e antes da ação de adicionar Personalizada.             |
    | GameUXRollBackAddAsCurUser    | NÃO instalado e não é ALLUSERS | 4002     | Essa ação personalizada só acontecerá quando uma nova instalação do usuário atual for cancelada. O número de sequência coloca a ação após InstallFiles e antes da ação de adicionar Personalizada. |
    | GameUXRemoveAsAdmin           | REMOVER ~ = "TODOS" E ALLUSERS     | 3452     | Essa ação personalizada só ocorrerá durante a remoção para todos os usuários. O número de sequência coloca a ação diretamente antes de removes e após as reversões.                                     |
    | GameUXRemoveAsCurUser         | REMOVER ~ = "ALL" E NÃO ALLUSERS | 3453     | Esta ação personalizada só ocorrerá durante a remoção do usuário atual. O número de sequência coloca a ação diretamente antes de removes e após as reversões.                              |
    | GameUXRollBackRemoveAsAdmin   | REMOVER ~ = "TODOS" E ALLUSERS     | 3450     | Esta ação personalizada ocorrerá somente quando a remoção de todos os usuários for cancelada. O número de sequência coloca a ação diretamente antes de removidas e antes da ação personalizada de remoção.              |
    | GameUXRollBackRemoveAsCurUser | REMOVER ~ = "ALL" E NÃO ALLUSERS | 3451     | Esta ação personalizada ocorrerá somente quando a remoção do usuário atual for cancelada. O número de sequência coloca a ação diretamente antes de removidas e antes da ação personalizada de remoção.       |

    

     

5.  Adicione a linha mostrada na tabela a seguir à tabela de propriedades no pacote MSI.

    | Propriedade          | Valor                                                         |
    |-------------------|---------------------------------------------------------------|
    | RelativePathToGDF | \\nome do caminho de arquivo relativo do arquivo binário que contém o GDF |

    

     

    > [!Note]  
    > O local especificado pelo caminho é relativo ao local especificado pelo caminho de instalação. Por exemplo, bin \\GDF.dll.

     

6.  Salve o pacote MSI.

para obter informações mais detalhadas sobre pacotes e Windows Installer do MSI, consulte [Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="debugging-tips"></a>Dicas de depuração

Veja a seguir algumas dicas para ajudar a depurar problemas ao chamar APIs do explorador de jogos:

### <a name="test-with-sample-code"></a>Teste com código de exemplo

A criação da solução de exemplo GameUXInstallHelper criará uma GameUXInstallHelper.dll e uma GDFInstall.exe. O GDFInstall.exe é um aplicativo de exemplo que usa GameUXInstallHelper.dll. A execução de GDFInstall.exe será solicitada se você quiser instalar ou remover um binário GDF do explorador de jogos. Você pode testar o arquivo binário GDF passando-o como o primeiro ARG de linha de comando para GDFInstall.exe.

Se você não tiver um binário GDF ou o seu não for instalado, tente usar o GDF de exemplo no SDK do DirectX. O exemplo de GDFExampleBinary é encontrado no SDK do DirectX e é apenas uma DLL que contém apenas um arquivo GDF. Também estão incluídos na fonte seu projeto GDFMaker. Você pode compilá-lo e testá-lo usando GDFInstall.exe. Você também pode comparar o XML com o seu para identificar exatamente onde está o problema.

### <a name="make-sure-that-your-game-was-removed-properly"></a>Certifique-se de que seu jogo foi removido corretamente

Se o jogo já estiver instalado no explorador de jogos, as chamadas subsequentes para **IGameExplorer:: addgame** retornarão E \_ falharão. portanto, verifique se o jogo não está instalado antes do teste. Isso também se aplicará se você instalar o GDF somente para o usuário atual e, em seguida, tentar instalar o GDF para todos os usuários. Primeiro, você deve remover o jogo dos usuários atuais antes de **IGameExplorer:: addgame** terá sucesso.

Se você executar **GDFInstall.exe Enumeração**, o aplicativo de exemplo entrará em um modo diferente que enumerará todos os jogos do explorador de jogos instalados e solicitará que você os remova. você também pode procurar e pesquisar o registro em HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ GameUX para ter certeza de que seu jogo não está instalado para outro usuário no sistema. No entanto, não altere essas configurações de registro para nenhuma outra finalidade, pois não há garantia de que elas permaneçam compatíveis em versões futuras do sistema operacional.

### <a name="be-sure-to-sign-using-authenticode"></a>Não se esqueça de assinar usando Authenticode

Se você forneceu uma classificação, mas não a está vendo no explorador de jogos, certifique-se de que usou o Authenticode para assinar o arquivo executável ou DLL que contém a classificação. O explorador de jogos ignora as informações de classificações em arquivos não assinados. Para obter mais informações sobre Authenticode, consulte [assinatura Authenticode para desenvolvedores de jogos](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).

### <a name="be-sure-that-parental-controls-are-available"></a>Verifique se os controles dos pais estão disponíveis

verifique se você está testando controles dos pais em uma edição do Windows Vista que fornece controles dos pais: home Basic, home Premium ou Ultimate. Windows o vista Business e Windows vista Enterprise não fornecem controles dos pais no entanto, se você estiver testando no Windows Vista Ultimate e o computador de teste estiver ingressado em um domínio, será necessário alterar uma configuração de diretiva de grupo para tornar os controles dos pais visíveis. Para fazer isso, consulte [introdução com o explorador de jogos](/previous-versions/windows/desktop/legacy/ee417682(v=vs.85)).

### <a name="verify-that-tasks-are-of-the-correct-type"></a>Verificar se as tarefas são do tipo correto

Se você tiver especificado tarefas de suporte que não aparecem no explorador de jogos, verifique se elas são todos os links da Web. Qualquer outra tarefa de atalho deve ser criada como tarefas de reprodução. As tarefas são abordadas anteriormente neste artigo em [tarefas do explorador de jogos](#games-explorer-tasks).

### <a name="verify-the-data-in-gdf-binary"></a>Verificar os dados no binário GDF

GDFTrace.exe é uma ferramenta encontrada no SDK do DirectX. Você pode executar GDFTrace.exe em seu binário GDF e produzirá todos os metadados GDF contidos no binário para cada idioma com suporte para validação rápida. Ele também exibe quaisquer avisos sobre informações ausentes ou desatualizadas.

## <a name="summary"></a>Resumo

o explorador de jogos no Windows Vista fornece uma maneira fácil e personalizável de apresentar os usuários do Windows vista, mas também exige que você registre o jogo com o sistema durante o processo de instalação. O exemplo GameUXInstallHelper simplifica muito esse processo para os desenvolvedores.

 

 