---
description: Este tópico fornece ISVs (fornecedores independentes de software) com um guia rápido para as etapas necessárias para registrar e gerenciar padrões de aplicativo no Windows Vista e posterior. Links são fornecidos para artigos mais aprofundados sobre o tópico de cada seção.
ms.assetid: 649eb20d-07d3-4209-abff-45fc50f05631
title: Gerenciando aplicativos padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc146858d197b96229edda49ac2e7249db51bf4c
ms.sourcegitcommit: 4d639170c06864e47ef66b2cfe6ca3d07cce0b02
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109812821"
---
# <a name="managing-default-applications"></a>Gerenciando aplicativos padrão

O **recurso Definir Acesso ao** Programa e Padrões do Computador (SPAD) foi adicionado ao Windows XP e versões posteriores do Windows para gerenciar padrões por computador. Além do SPAD, o Windows Vista introduziu o conceito de aplicativos padrão por usuário e o **item** Programas Padrão no Painel de Controle.

> [!IMPORTANT]
> Este tópico não se aplica a Windows 10. A maneira como as associações de arquivos padrão funcionam mudou Windows 10. Para obter mais informações, consulte a seção sobre **Alterações em como Windows 10 lida com aplicativos padrão** nesta [postagem.](https://blogs.windows.com/windows-insider/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/)

 

As configurações padrão por usuário são específicas para uma conta de usuário individual no sistema. Se as configurações padrão por usuário estão presentes, elas têm precedência sobre os padrões por computador correspondentes para essa conta. A partir Windows 8, o sistema de extensibilidade para o tipo de arquivo e os padrões de protocolo são estritamente por usuário e os padrões por computador são ignorados. O SPAD também foi alterado Windows 8 para definir padrões por usuário.

-   Em sistemas que executam versões do Windows anteriores ao Windows 8, uma conta de usuário recém-criada recebe padrões por computador até que os padrões por usuário sejam estabelecidos. No Windows Vista e posterior, os usuários podem usar o **item** Programas Padrão no Painel de Controle para definir ou alterar seus padrões por usuário. Além disso, quando um aplicativo é executado pela primeira vez, os padrões por usuário podem ser definidos usando as diretrizes a seguir na seção Application [First Run and Defaults](#application-first-run-and-defaults) .
-   Em sistemas que executam o Windows 8, uma conta de usuário recém-criada depende dos padrões por usuário desde o início e não há mais suporte para a configuração desses padrões na primeira execução, conforme explicado na seção Application [First Run and Defaults.](#application-first-run-and-defaults)

Um aplicativo deve ser registrado com o SPAD e o recurso de programas padrão para ser oferecido como o programa padrão no Windows Vista e posterior.

Este tópico fornece ISVs (fornecedores de software independentes) com um guia rápido para as etapas necessárias para registrar e gerenciar os padrões de aplicativo no Windows Vista e versões posteriores. São fornecidos links para artigos mais detalhados sobre o tópico de cada seção.

-   [Item programas padrão no painel de controle](#default-programs-item-in-control-panel)
-   [Definir o acesso do programa e padrões do computador](#set-program-access-and-computer-defaults)
    -   [Definindo padrões em SPAD](#setting-defaults-in-spad)
    -   [Ocultar o acesso no SPAD](#hide-access-in-spad)
-   [Registrando para pontos de entrada de aplicativo](#registering-for-application-entry-points)
    -   [Abrir com](#open-with)
    -   [Menu iniciar e barra de início rápido](#start-menu-and-quick-launch-bar)
-   [Instalação e padrões do aplicativo](#application-installation-and-defaults)
-   [Atualizações e padrões de aplicativos](#application-upgrades-and-defaults)
-   [Execução e padrões da primeira aplicação](#application-first-run-and-defaults)
-   [Verificando padrões e solicitando o consentimento do usuário](#verifying-defaults-and-asking-for-user-consent)
-   [Dicas de compatibilidade de aplicativos](#application-compatibility-tips)
    -   [Evite disparar Per-User virtualização](#avoid-triggering-per-user-virtualization)
    -   [Evitar avisos ou blocos de AppCompat do assistente de compatibilidade de programa](#avoid-appcompat-warnings-or-blocks-from-the-program-compatibility-assistant)
    -   [Suporte para versões anteriores do sistema operacional Windows](#support-for-previous-windows-operating-system-versions)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="default-programs-item-in-control-panel"></a>Item programas padrão no painel de controle

O **programas padrão** é um recurso introduzido no Windows Vista, acessível diretamente do menu **Iniciar** , bem como do painel de controle. Ele fornece uma nova infraestrutura que funciona com privilégio de usuário padrão (não elevado) e foi projetada para permitir que usuários e aplicativos gerenciem padrões por usuário. Para usuários, os Programas Padrão fornece uma maneira unificada e facilmente acessível de gerenciar padrões, associações de arquivos e configurações de reprodução automática em todos os aplicativos no sistema. Para aplicativos, o uso do escopo por usuário fornecido pelas APIs de Programas Padrão oferece as seguintes vantagens:

-   **Nenhuma elevação**

    Um aplicativo não precisa elevar seus privilégios para reivindicar padrões.

-   **Boa Cidadãos**

    Em um computador com vários usuários, cada usuário pode selecionar diferentes aplicativos padrão.

-   **Gerenciamento Padrão**

    As APIs de Programas Padrão oferecem um mecanismo confiável e consistente para verificar o status padrão e recuperar as configurações perdidas sem recorrer à escrita diretamente no Registro. No entanto, desde Windows 8, não recomendamos que os aplicativos consultem o status padrão porque um aplicativo não pode mais alterar as configurações padrão– essas alterações podem ser feitas somente pelo usuário.

Para permitir que seu aplicativo gerencie padrões com eficiência, você deve registrar seu aplicativo como um programa padrão potencial. Para obter detalhes sobre como registrar e usar as APIs de Programas Padrão, consulte [Programas Padrão](default-programs.md).

Os Programas Padrão também fornece estes dois recursos:

-   **Interface do usuário de padrões reutilizáveis**

    A interface do usuário dos padrões do programa **(** Definir seus programas padrão ) e associações de arquivo ( Associar um tipo de arquivo ou protocolo **a um** programa ) pode ser reutilizada e chamada de dentro de um aplicativo. Isso permite que os aplicativos forneçam uma experiência de usuário padrão para gerenciar padrões e salva isVs de ter que desenvolver uma interface do usuário personalizada ou equivalente.

-   **Inclusão de URL e informações de marketing**

    Como parte da página Definir **seus** programas padrão do **item** Programas Padrão no Painel de Controle, um aplicativo pode fornecer informações de marketing e um link para o site do fornecedor. Essa URL é derivada do certificado Authenticode com o qual o aplicativo foi assinado. Isso impede o uso indevido e a substituição não autorizada desse link. Se um aplicativo tiver um certificado Authenticode que inclui uma URL inserida, a interface do usuário do Windows exibirá essa URL inserida. Os ISVs devem aproveitar esse recurso para direcionar os usuários ao site para atualizações e outros downloads.

## <a name="set-program-access-and-computer-defaults"></a>Definir o acesso do programa e padrões do computador

**Definir acesso do programa e padrões do computador** (SPAD) permite que os administradores gerenciem padrões de todo o computador que são herdados por todos os novos usuários desse computador. Antes do Windows 8, o SPAD também permitia que os administradores reparasse as associações de arquivos se fossem desfeitos quando os programas foram removidos do sistema. No entanto, a partir do Windows 8, SPAD afeta apenas os padrões específicos do usuário.

Para obter mais informações sobre como registrar um aplicativo em SPAD, consulte [trabalhando com definir acesso do programa e padrões do computador (SPAD)](cpl-setprogramaccess.md) e [registrar programas com tipos de cliente](reg-middleware-apps.md). As alterações específicas e as novas recomendações são discutidas nas seções a seguir.

### <a name="setting-defaults-in-spad"></a>Definindo padrões em SPAD

Padrões por usuário substituem padrões por computador.

-   **Antes do Windows 8**: os padrões definidos em SPAD (que são por computador) não serão vistos pelos usuários se os padrões correspondentes por usuário estiverem definidos. Se um usuário não tiver definido um padrão por usuário, o sistema usará o padrão do computador correspondente. As novas contas de usuário em um computador inicialmente herdam os padrões do computador. Na primeira vez que um usuário executa um aplicativo, o aplicativo deve solicitar que o usuário atribua seus padrões por usuário. Consulte [execução e padrões da primeira aplicação](#application-first-run-and-defaults).
-   **A partir do Windows 8**: todos os padrões são por usuário e qualquer configuração padrão por computador é ignorada. Os aplicativos não podem mais definir opções padrão, para que não possam orientar o usuário por meio de sua atribuição desses padrões.

Quando um aplicativo anterior ao Windows 8 implementa **definido como padrão** no SPAD, essas diretrizes devem ser seguidas:

-   Os aplicativos devem reivindicar apenas padrões de nível de computador por meio do SPAD.
-   Os *aplicativos não devem* reivindicar padrões por usuário por SPAD.

Quando um Windows 8 implementa  Definir como Padrão no SPAD, ele deve registrar seus tipos de arquivo e protocolos em Programas Padrão [,](default-programs.md)usando o mesmo nome de aplicativo usado no SPAD. Isso permite que uma alteração no SPAD reflita como uma alteração na entrada Programas Padrão correspondente para o usuário atual.

### <a name="hide-access-in-spad"></a>Ocultar o acesso no SPAD

A opção ocultar acesso para cada padrão possível no SPAD é acessada de uma das duas maneiras:

-   Escolha a **categoria não Microsoft** de padrões, que remove o acesso a todos os padrões da Microsoft.
-   Escolha a **categoria Personalizado** e des marque a caixa de **seleção Habilitar acesso a este** programa.

Anteriormente, a tomada de qualquer uma dessas ações removeu todos os pontos de entrada para os aplicativos apropriados no sistema. Diretrizes específicas para essa situação dizem para remover atalhos e ícones dos seguintes locais:

-   Desktop
-   Menu Iniciar
-   Início Rápido barra (somente Windows Vista e anteriores)
-   Área de notificação
-   Menus de atalho
-   Faixa de tarefas de pasta

Os fornecedores são incentivados a implementar essas diretrizes na função de retorno de chamada Ocultar Acesso do aplicativo.

### <a name="alternate-hide-access-method-in-spad"></a>Método alternativo ocultar acesso no SPAD

Para alguns aplicativos herdado, uma implementação completa de Ocultar Acesso pode não ser prática. Um método alternativo que atinge o mesmo efeito, mas não é facilmente reversível pelo usuário, é desinstalar o aplicativo. O exemplo a seguir mostra o comportamento de exemplo e o código de exemplo para implementar isso.

A experiência do usuário recomendada para essa alternativa é a seguinte:

-   Quando o usuário limpa a caixa **Habilitar acesso** a esse programa no SPAD, a interface do usuário a seguir é apresentada.

    ![caixa de diálogo vista sobre como ocultar o acesso ao programa](images/hideaccessvista.png)

-   Quando o usuário clica em **OK**, o item **programas e recursos** no painel de controle é exibido para que o usuário possa desinstalar o aplicativo.
-   Os usuários do Windows XP devem ser apresentados com a caixa de diálogo a seguir.

    ![caixa de diálogo do Windows XP sobre como ocultar o acesso ao programa](images/hideaccessxp.png)

-   Quando o usuário do Windows XP clica em **OK**, o item **Adicionar ou remover programas** no painel de controle é exibido para que o usuário possa desinstalar o aplicativo.

O código a seguir fornece uma implementação reutilizável para o recurso ocultar acesso conforme descrito anteriormente. Ele pode ser usado no Windows XP, no Windows Vista e no Windows 7.


```
#include <windows.h>
#include <shlwapi.h>
#include <strsafe.h>

PCWSTR c_pszMessage1 = L"To hide access to this program, you need to uninstall it by ";
PCWSTR c_pszMessage2 = L"using\n%s in Control Panel.\n\nWould you like to start %s?";
PCWSTR c_pszApplicationName  = L"Sample App";

int _tmain(int argc, WCHAR* argv[])
{
    OSVERSIONINFO version;
    version.dwOSVersionInfoSize = sizeof(version);

    if (GetVersionEx(&version))
    {
        PCWSTR pszCPLName = NULL;

        if (version.dwMajorVersion >= 6)
        {
            // Windows Vista and later
            pszCPLName = L"Programs and Features";
        }
        else if (version.dwMajorVersion == 5 &&
                 version.dwMinorVersion == 1)
        {
            // XP
            pszCPLName = L"Add/Remove Programs";
        }

        if (pszCPLName != NULL)
        {
            WCHAR szMessage[256], szScratch[256];
            if (SUCCEEDED(StringCchPrintf(szScratch, 
                                          ARRAYSIZE(szScratch), 
                                          c_pszMessage2, 
                                          pszCPLName, 
                                          pszCPLName)))
            {
                if (SUCCEEDED(StringCchCopy(szMessage, 
                                            ARRAYSIZE(szMessage), 
                                            c_pszMessage1)))
                {
                    if (SUCCEEDED(StringCchCat(szMessage, 
                                               ARRAYSIZE(szMessage), 
                                               szScratch)))
                    {
                        if (IDOK == MessageBox(NULL, 
                                               szMessage, 
                                               c_pszApplicationName, 
                                               MB_OKCANCEL))
                        {
                            ShellExecute(NULL, 
                                         NULL, 
                                         L"appwiz.cpl", 
                                         NULL, 
                                         NULL, 
                                         SW_SHOWNORMAL);
                        }
                    }
                }
            }
        }
    }
    return 0;
}
```



## <a name="registering-for-application-entry-points"></a>Registrando para pontos de entrada de aplicativo

Um aplicativo pode ter muitos pontos de entrada no sistema operacional. Estes são os locais recomendados para pontos de entrada:

-   Desktop
-   Menu Iniciar
-   Barra de início rápido (somente Windows Vista e anterior)
-   Área de notificação
-   Menus de atalho
-   Faixa de tarefas da pasta

Esta seção enfoca estas áreas específicas:

-   [Abrir com](#open-with)
-   [Menu iniciar e barra de início rápido](#start-menu-and-quick-launch-bar)

### <a name="open-with"></a>Abrir com

O menu de atalho **abrir com** permite que o usuário selecione um aplicativo que possa manipular um tipo de arquivo específico. Embora **Open with** possa ser usado para abrir um arquivo com um aplicativo uma vez, ele também pode ser usado para definir o padrão para essa extensão de nome de arquivo. Portanto, um aplicativo sempre deve se registrar para **abrir com** para que os usuários sejam apresentados com esse aplicativo como uma opção. Os aplicativos podem registrar tipos de arquivo e protocolos **para Abrir com**. Aplicativos que registram protocolos na estrutura Programas Padrão são adicionados automaticamente às **opções Abrir com** para protocolos.

Para obter informações sobre como **registrar-se no Open With**, consulte [Introdução às associações de arquivos](fa-intro.md).

### <a name="start-menu-and-quick-launch-bar"></a>Menu Iniciar e Início Rápido Barra

Para se tornar mais descobrivel para o usuário, os aplicativos podem adicionar atalhos a vários locais no Windows. O local mais comum para adicionar um atalho é **o** menu Iniciar. No Windows Vista e posterior, um aplicativo cria um atalho na pasta oculta %ProgramData% Programas de Menu Iniciar do Microsoft Windows para aparecer na lista de programas do menu Iniciar para todos \\ \\ os \\ \\ usuários.  Normalmente, um aplicativo adiciona uma subpasta que contém o atalho.

Para programas de navegador e email, o **menu** Iniciar do Windows Vista também apresenta dois links dedicados fora da lista de programas, intitulados canonicamente **internet** **e email**. Depois que um aplicativo se registra nessas categorias, a estrutura Programas Padrão pode gerenciar o que é lançado por meio desses links.

> [!Note]  
> Os links **do** **menu** **Iniciar** dedicado de Internet e email não estão mais presentes no Windows 7.

 

Para aumentar ainda mais a capacidade de descoberta, os aplicativos também podem adicionar atalhos à área de trabalho e à Início Rápido barra. Os aplicativos devem solicitar permissão ao usuário (geralmente durante a instalação ou na primeira vez) antes de adicionar um ícone ao **menu** Iniciar, área de trabalho ou Início Rápido barra.

> [!Note]  
> A Início Rápido de dados não está mais disponível a partir do Windows 7. A alternativa do Windows 7 é ter o aplicativo fixado na barra de tarefas, mas a fixar não pode ser feita programaticamente, pois é estritamente uma escolha do usuário.

 

Para saber mais, consulte esses tópicos:

-   [Como registrar um navegador da Internet ou um cliente de email com o menu Iniciar do Windows](start-menu-reg.md)
-   [Registrando programas com tipos de cliente](reg-middleware-apps.md)

## <a name="application-installation-and-defaults"></a>Instalação e padrões do aplicativo

Os procedimentos de instalação do aplicativo não foram alterados fundamentalmente desde o Windows XP, com exceção de uma nova diretriz para sistemas que executam versões do Windows anteriores ao Windows 8: assumem padrões por computador no momento da instalação, mas não definem padrões por usuário até que o usuário execute o aplicativo pela primeira vez. (Consulte [execução e padrões do aplicativo pela primeira vez](#application-first-run-and-defaults).) Os aplicativos não devem definir padrões por usuário durante a instalação porque há situações em que a pessoa que está instalando o aplicativo não é o usuário pretendido. A partir do Windows 8, não há suporte para padrões por computador e os aplicativos não podem alterar as configurações padrão por usuário.

Durante a instalação, um aplicativo deve copiar seus binários para o disco rígido e gravar seus ProgIDs no registro. O aplicativo também deve se registrar para programas padrão e **abrir com** no momento para cada associação de arquivo que for um candidato a ser manipulado. O aplicativo pode usar a subchave **OpenWithProgIDs** para se registrar com **Open with**.

Para saber mais, consulte esses tópicos:

-   [Programas padrão](default-programs.md)
-   [Introdução às associações de arquivo](fa-intro.md)

## <a name="application-upgrades-and-defaults"></a>Atualizações e padrões de aplicativos

Muitos aplicativos têm a capacidade de atualizar a si mesmos ao longo do tempo. Esse procedimento de atualização não deve alterar o estado de padrões por usuário, pois essa alteração seria inesperada para o usuário. No entanto, é aceitável que um aplicativo Verifique as associações de arquivo no nível do computador e repare-as se elas estiverem corrompidas.

## <a name="application-first-run-and-defaults"></a>Execução e padrões da primeira aplicação

> [!Note]  
> A partir do Windows 8, o sistema lida com esse procedimento em nome de todos os aplicativos. Os próprios aplicativos não podem mais consultar e alterar os padrões. Somente o usuário pode fazer isso. Portanto, os aplicativos não devem tentar consultar o padrão atual ou alterar o padrão por meio de qualquer mecanismo. No entanto, os aplicativos podem fornecer um ponto de entrada para programas padrão no painel de controle chamando o método [**LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) da interface [**IApplicationAssociationRegistrationUI**](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui) .

 

Com a introdução de padrões por usuário no Windows Vista, é importante que os aplicativos que disputam extensões de nome de arquivo populares forneçam uma experiência de usuário comum para reivindicar essas extensões. Como esses padrões agora estão definidos no contexto do usuário, eles devem se apresentar como uma possibilidade padrão somente quando o usuário executa o programa após a instalação.

A diretriz para estabelecer padrões por usuário é esta: quando um aplicativo é executado pela primeira vez para um usuário específico, esse aplicativo deve solicitar preferências do usuário para padrões e associações de arquivo para si mesmo.

A interface do usuário recomendada deve fornecer duas opções claras para o usuário:

1.  Aceite todos os padrões que o aplicativo gostaria de reivindicar. Essa opção também pode definir outras propriedades padrão do aplicativo, como privacidade ou configurações de atualização automática. Essa opção permite que o aplicativo reclame todos os seus padrões registrados.
2.  Personalize aceitando ou não seleções padrão e configurações de programa individualmente. Essa opção apresenta mais interface do usuário que permite que o usuário faça escolhas granulares para suas opções padrão.

Para obter mais informações, consulte [Programas padrão](default-programs.md).

## <a name="verifying-defaults-and-asking-for-user-consent"></a>Verificando padrões e solicitando consentimento do usuário

> [!Note]  
> Não há suporte para isso desde Windows 8.

 

Depois que um aplicativo é registrado com Programas Padrão no Windows Vista e posterior, determinadas APIs ficam disponíveis para o aplicativo. Por exemplo, um aplicativo pode precisar verificar se ele é o programa padrão. A interface [**IApplicationAssociationRegistration**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) fornece métodos para fazer isso.

Qualquer aplicativo que deseja reivindicar padrões deve primeiro perguntar ao usuário e nunca reivindicar padrões sem permissão. O usuário deve ser perguntado se deseja tornar o aplicativo o padrão ou deixar o padrão atual em prática. Também deve haver uma opção para não fazer essa pergunta novamente depois que o usuário tiver feito sua escolha.

Para obter mais informações, consulte [Programas padrão](default-programs.md).

## <a name="application-compatibility-tips"></a>Dicas de compatibilidade do aplicativo

Esta seção fornece algumas dicas de compatibilidade de aplicativos relacionadas à experiência de programas padrão no Windows.

### <a name="avoid-triggering-per-user-virtualization"></a>Evite disparar Per-User virtualização

Com o ambiente de controle de conta de usuário (UAC), os aplicativos sempre devem ser executados com direitos de usuário padrão para a melhor experiência do cliente. Por motivos de segurança, os aplicativos com um nível de privilégio de usuário padrão são impedidos de gravar em determinadas partes do registro e em determinados arquivos do sistema. O Windows Vista e versões posteriores do Windows fornecem uma camada de compatibilidade de aplicativos temporária (AppCompat) para ajudar os aplicativos a fazer a transição. As tentativas bloqueadas de gravar no registro ou em arquivos do sistema são "virtualizadas" para que o aplicativo continue a ser executado, mas as áreas confidenciais do sistema não são alteradas. No entanto, os aplicativos não devem contar com a tecnologia AppCompat como uma solução de longo prazo. Em vez disso, os aplicativos devem usar as várias ferramentas disponíveis para verificar se podem ser executados com êxito em direitos de usuário padrão. Uma reprogramação do aplicativo pode ser necessária para fazer isso, mas deve ser feita no interesse da compatibilidade de longo prazo.

### <a name="avoid-appcompat-warnings-or-blocks-from-the-program-compatibility-assistant"></a>Evitar avisos ou blocos de AppCompat do assistente de compatibilidade de programa

O PCA (Assistente de compatibilidade de programa) é fornecido no Windows Vista e posterior. Seu objetivo é fornecer um método automatizado para que os programas mais antigos com problemas de compatibilidade funcionem melhor. O PCA monitora os programas em busca de problemas conhecidos. Se um problema for detectado, ele notificará o usuário sobre o problema e oferecerá a aplicação de soluções efetivas antes que o usuário execute o programa novamente. Para evitar a exibição desses avisos ou blocos, os ISVs devem usar as várias ferramentas disponíveis para garantir que seus aplicativos sejam compatíveis com o Windows Vista, o Windows 7 e versões posteriores.

### <a name="support-for-previous-windows-operating-system-versions"></a>Suporte para versões anteriores do sistema operacional Windows

A infraestrutura de programas padrão não está disponível em nenhum sistema operacional Windows antes do Windows Vista. Portanto, quando os aplicativos se movem para a nova infraestrutura de Programas Padrão, eles devem manter seu código padrão de aplicativo mais antigo para manter a compatibilidade com versões mais antigas do Windows. Um aplicativo deve executar uma verificação de versão do sistema operacional como parte de sua instalação para determinar qual código padrão do aplicativo deve ser executado.

Para dar suporte a uma atualização do Windows XP para o Windows Vista ou posterior, os aplicativos devem adicionar todas as entradas do Registro necessárias para Programas Padrão, mesmo quando eles estão sendo instalados em um computador que executa o Windows XP. O registro não terá efeito em um computador que executa o Windows XP, mas se o computador for atualizado posteriormente, o aplicativo já estará registrado e poderá aproveitar a estrutura.

Para obter mais informações, consulte [**OSVERSIONINFO**](/windows/win32/api/winnt/ns-winnt-osversioninfoa).

## <a name="additional-resources"></a>Recursos adicionais

-   [Introdução às associações de arquivos](fa-intro.md)
-   [Como registrar um navegador da Internet ou um cliente de email com o menu Iniciar do Windows](start-menu-reg.md)
-   [Registrando um aplicativo em um esquema de URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Práticas recomendadas para associações de arquivos](fa-best-practices.md)
</dt> <dt>

[Cenário de exemplo de associação de arquivo](fa-sample-scenarios.md)
</dt> <dt>

[Programas padrão](default-programs.md)
</dt> <dt>

[Trabalhando com definir o acesso ao programa e padrões de computador (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 
