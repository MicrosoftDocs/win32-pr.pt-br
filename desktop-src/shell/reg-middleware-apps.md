---
description: 'este tópico explica como registrar um programa no registro de Windows como um dos seguintes tipos de cliente: navegador, email, reprodução de mídia, mensagens instantâneas ou máquina virtual para Java.'
title: Registrando programas com tipos de cliente
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 33fcb63c-3db2-44df-acfe-8c88e2e634e4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c9c2d9a4589b684580250c487a6f83c3c9e79dbc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470414"
---
# <a name="registering-programs-with-client-types"></a>Registrando programas com tipos de cliente

este tópico explica como registrar um programa no registro de Windows como um dos seguintes tipos de cliente: navegador, email, reprodução de mídia, mensagens instantâneas ou máquina virtual para Java.

> [!Note]  
> Essas informações se aplicam aos seguintes sistemas operacionais:
> 
> -   Windows 2000 Service Pack 3 (SP3)
> -   Windows 2000 Service Pack 4 (SP4)
> -   Windows XP Service Pack 1 (SP1)
> -   Windows XP Service Pack 2 (SP2)
> -   Windows XP Service Pack 3 (SP3)
> -   Windows Server 2003
> -   Windows Vista
> -   Windows Vista Service Pack 1 (SP1)
> -   Windows 8

 

Este tópico inclui as seções a seguir.

-   [Elementos de registro comuns para todos os tipos de cliente](#common-registration-elements-for-all-client-types)
    -   [Selecionando um nome canônico](#selecting-a-canonical-name)
    -   [Registrando o nome de exibição de um programa](#registering-a-programs-display-name)
    -   [Registrando o ícone de um programa](#registering-a-programs-icon)
    -   [Registrando um verbo aberto](#registering-an-open-verb)
    -   [Registrando informações de instalação](#registering-installation-information)
-   [Elementos de registro para tipos de cliente específicos](#registration-elements-for-specific-client-types)
    -   [Registro do menu iniciar](#start-menu-registration)
    -   [Registro de cliente de email](#mail-client-registration)
-   [Concluir os registros de exemplo](#complete-sample-registrations)
    -   [Um navegador de exemplo](#a-sample-browser)
    -   [Um navegador de email de exemplo](#a-sample-mail-browser)
    -   [Um player de mídia de exemplo](#a-sample-media-player)
    -   [Um programa de Instant Messenger de exemplo](#a-sample-instant-messenger-program)
    -   [Uma máquina virtual de exemplo para Java](#a-sample-virtual-machine-for-java)
-   [Tópicos relacionados](#related-topics)

Este tópico estende a documentação existente sobre o registro de um programa como um determinado tipo de cliente. Para obter links para essa documentação, consulte a seção Tópicos relacionados.

## <a name="common-registration-elements-for-all-client-types"></a>Elementos de registro comuns para todos os tipos de cliente

Ao registrar um programa como um tipo de cliente, a maioria das entradas de registro é a mesma, independentemente do tipo de cliente. Algumas entradas do registro, no entanto, são específicas para o tipo de cliente e elas são indicadas na seção [elementos de registro para tipos de cliente específicos](#registration-elements-for-specific-client-types) .

Esta seção aborda os seguintes tópicos:

-   [Selecionando um nome canônico](#selecting-a-canonical-name)
-   [Registrando o nome de exibição de um programa](#registering-a-programs-display-name)
-   [Registrando o ícone de um programa](#registering-a-programs-icon)
-   [Registrando um verbo aberto](#registering-an-open-verb)
-   [Registrando informações de instalação](#registering-installation-information)

> [!Note]  
> Nomes de subchaves fornecidos em itálico ao longo deste tópico são espaços reservados para nomes de subchave definidos pelo usuário ou um conjunto de valores possíveis. Exemplos completos com nomes de exemplo no local são fornecidos na seção de [registros de exemplo completo](#complete-sample-registrations) .

 

Todas as informações de registro de tipo de cliente são armazenadas na seguinte subchave:

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
```

*ClientTypeName* é um dos seguintes nomes de subchave:

-   StartMenuInternet (para navegadores)
-   Email (para email)
-   Mídia (para reprodução de mídia)
-   MENSAGENS instantâneas (para mensagens instantâneas)
-   JavaVM (para máquina virtual para Java)

Ao longo deste tópico, você notará referências a um programa de computador fictício chamado "visão acesa" da Litware Inc., com um arquivo executável chamado Litview.exe. Esse programa hipotético é usado de maneira intercambiável como um Messenger imediato, um navegador ou outro tipo de programa cliente, conforme necessário, para fins ilustrativos.

### <a name="selecting-a-canonical-name"></a>Selecionando um nome canônico

O fornecedor deve escolher um *nome canônico* para o programa. O nome canônico nunca é mostrado ao usuário, portanto, ele não precisa ser localizado. Sua única finalidade é fornecer uma cadeia de caracteres exclusiva que possa ser usada para identificar o programa. Normalmente, é o mesmo que o nome em inglês do programa, mas essa é meramente uma convenção.

Para tipos de cliente diferentes de navegadores, o nome canônico pode ser qualquer cadeia de caracteres. Escolha um nome exclusivo, que provavelmente não será usado por outro fornecedor.

Para clientes de navegador, o nome canônico deve ser o nome — incluindo a extensão — do executável associado; por exemplo, "Litview.exe".

Aqui estão alguns exemplos de nomes canônicos.

-   Iexplore.exe (navegador)
-   Windows Email (email)
-   Windows Media Player (mídia)
-   Windows Messenger (mensagens instantâneas)

Registre o nome canônico criando uma subchave, como mostrado aqui. O nome da subchave é o nome canônico. Todas as informações relacionadas ao registro desse programa existirão nessa subchave.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
```

### <a name="registering-a-programs-display-name"></a>Registrando o nome de exibição de um programa

A próxima etapa no registro é especificar o nome de exibição do programa. Ele é fornecido como um valor sob a chave de nome canônica, como mostrado aqui. Observe novamente que *canônicaname* e *ClientTypeName* não são os nomes reais das chaves, mas somente espaços reservados para os nomes verdadeiros, como a *exibição acesa*.

> [!Note]  
> a partir de Windows 8, o nome usado para se registrar para [definir o acesso do programa e padrões do computador (SPAD)](cpl-setprogramaccess.md) e para [programas padrão](default-programs.md) deve corresponder para que as alterações de SPAD disparem os registros de programas padrão.

 

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               LocalizedString = @FilePath,-StringID
```

O valor de **localizadastring** é uma \_ cadeia de caracteres reg sz e consiste em um sinal "arroba" (@), o caminho completo para um arquivo de .dll ou .exe, uma vírgula, um sinal de subtração e um inteiro decimal. O inteiro decimal é a ID de um recurso de cadeia de caracteres — contida no arquivo de .dll ou .exe — cujo valor deve ser exibido para o usuário como o nome desse cliente. Observe que o caminho do arquivo não requer aspas, mesmo que contenha espaços.

Registrar a cadeia de caracteres do nome de exibição dessa maneira permite que o mesmo registro seja usado para vários idiomas. Cada instalação de idioma fornece um arquivo de recurso diferente com o nome de exibição armazenado na mesma ID de recurso.

O exemplo a seguir mostra o registro de um programa de mensagens instantâneas de exibição iluminada fictícia. Como é um programa de mensagens instantâneas, a subchave *canônicaname* (nesse caso, *exibição iluminada*) é armazenada na subchave **im** .

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

Observe o uso da entrada (padrão) como uma declaração secundária do nome de exibição do cliente. Se a **localizadastring** não estiver presente, o valor (padrão) será usado em seu lugar. Isso funciona com todos os tipos de cliente (navegadores da Internet, navegadores de email, mensageiros instantâneos e players de mídia). Para compatibilidade com versões anteriores com o [layout do registro do cliente do Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85)), os programas de email devem definir o valor (padrão) da subchave *canônicaname* para o nome de exibição do cliente no idioma atualmente instalado.

### <a name="registering-a-programs-icon"></a>Registrando o ícone de um programa

> [!Note]  
> esta seção não se aplica a Windows 2000.

 

por padrão, a seção superior do menu **iniciar** do Windows XP e do Windows Vista contém ícones de **Internet** e **email** . esses ícones não estão presentes no Windows 7 e versões posteriores. Para clientes de navegador e email, quando um programa é atribuído como o padrão para seu tipo de cliente, o ícone registrado desse programa é exibido para essas entradas do menu **Iniciar** .

O registro do ícone de um programa é obrigatório para clientes de navegador e email. o registro de um ícone para a reprodução de mídia, mensagens instantâneas ou máquina virtual para tipos de cliente Java é opcional, e os ícones registrados para esses tipos de cliente não são usados atualmente pelo Windows e não são exibidos na seção superior dos menus **iniciar** do Windows XP ou Windows Vista.

Para registrar um ícone para um programa cliente, adicione uma subchave **DefaultIcon** com um valor padrão, conforme mostrado aqui.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               DefaultIcon
                  (Default) = FilePath,IconIndex
```

O valor de **FilePath** é o caminho completo para o arquivo que contém o ícone. Esse caminho não requer aspas, mesmo que contenha espaços.

O valor de **IconIndex** é interpretado da seguinte maneira:

-   Se **IconIndex** for um número positivo, o número será usado como o índice da matriz *com base em zero* dos ícones armazenados no arquivo. Por exemplo, se **IconIndex** for 1, o segundo ícone será carregado a partir do arquivo.
-   Se **IconIndex** for um número negativo, o valor absoluto de **IconIndex** será usado como o identificador de recurso (em vez do índice) para o ícone. Por exemplo, se **IconIndex** for-3, o ícone cujo identificador de recurso é 3 será carregado a partir do arquivo.

O exemplo a seguir mostra o registro de um navegador de exibição iluminada hipotética. O segundo ícone armazenado no arquivo de Litview.exe é usado como o padrão.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\Litview.exe,1
```

### <a name="registering-an-open-verb"></a>Registrando um verbo aberto

> [!Note]  
> esta seção não se aplica a Windows 2000. A etapa a seguir é necessária apenas para clientes de navegador e de email.

 

Suponha que um usuário tenha selecionado seu programa como a Internet ou o programa de email padrão. esse usuário clica no ícone **Internet** ou **email** no menu **iniciar** do Windows XP ou Windows Vista para abrir o programa. Nesse ponto, a linha de comando registrada conforme mostrado aqui é executada.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               shell
                  open
                     command
                        (Default) = command line
```

A linha de comando deve especificar um caminho absoluto totalmente qualificado para o arquivo, seguido por opções de linha de comando opcionais. Se o tipo de entrada for REG \_ Expand \_ sz, as variáveis de ambiente poderão ser usadas no caminho. Use aspas adequadamente para garantir que os espaços na linha de comando não sejam interpretados erroneamente. A linha de comando deve executar o programa com os padrões apropriados. Os navegadores geralmente assumem como padrão o home page do usuário. Os programas de email geralmente abrem a **caixa de entrada** do usuário.

O exemplo a seguir mostra o registro de um `open` verbo para um navegador de exibição iluminada hipotética. Ele não especifica opções de linha de comando.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\Litview.exe"
```

Observe que, nesse valor, as aspas são colocadas em volta do caminho porque contêm espaços inseridos. Omitir essas aspas pode fazer com que a linha de comando seja interpretada erroneamente.

### <a name="registering-installation-information"></a>Registrando informações de instalação

> [!Note]  
> esta seção não se aplica ao Windows Server 2003.

 

-   [O comando reinstalar](#the-reinstall-command)
-   [O comando Ocultar ícones](#the-hide-icons-command)
-   [O comando mostrar ícones](#the-show-icons-command)
-   [Configuração do programa de grupo](#group-program-configuration)
-   [Exemplo de registro do navegador](#browser-registration-example)

O recurso pelo qual o usuário seleciona programas padrão por máquina é nomeado e acessado conforme mostrado na tabela a seguir. (o Windows Vista introduziu um novo recurso, **definiu os programas padrão**, pelos quais um usuário pode definir padrões por usuário.)




| Sistema operacional | Título | Local de acesso | 
|------------------|-------|-----------------|
| Windows 7 | Definir o acesso do programa e padrões do computador | <ul><li>Opção de <strong>programas padrão</strong> do menu <strong>Iniciar</strong></li><li><strong>Programas padrão</strong> Item do painel de controle</li></ul> | 
| Windows Vista | Definir o acesso do programa e padrões do computador | <ul><li>Opção de <strong>programas padrão</strong> do menu <strong>Iniciar</strong></li><li><strong>Programas padrão</strong> Item do painel de controle</li></ul> | 
| Windows XP SP2 | Definir acesso e padrões do programa | <ul><li>Menu <strong>Iniciar</strong></li><li><strong>Adicionar ou remover programas</strong> Item do painel de controle</li></ul> | 
| Windows XP SP1 | Configurar programas | <ul><li><strong>Adicionar ou remover programas</strong> Item do painel de controle</li></ul> | 




 

para simplificar, este tópico usa o título Windows 7 do recurso. Todas as versões do recurso são conhecidas como SPAD.

> [!Note]  
> se você estiver executando o Windows 2000 ou Windows xp, deverá ter pelo menos Windows 2000 SP3 ou Windows xp SP1 instalado para ver a página **definir acesso e padrões do programa** . no Windows Vista e posterior, o acesso à página **definir padrões de acesso e computador do programa** requer privilégios de administrador. Por esse motivo, os desenvolvedores são incentivados a se registrarem no item definir o painel de controle de [programas padrão](default-programs.md) para que qualquer usuário possa gerenciar os padrões do aplicativo.

 

A árvore de registro a seguir mostra a variedade de informações que devem ser registradas na chave **InstallInfo** do programa para que o programa apareça na página **Definir acesso do programa e padrões do computador** como uma opção para seu tipo de cliente. Cada um desses valores é discutido em detalhes nas seções a seguir.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  HideIconsCommand = command line
                  ReinstallCommand = command line
                  ShowIconsCommand = command line
                  IconsVisible = 1
```

A linha de comando deve especificar um caminho absoluto totalmente qualificado para o arquivo, seguido por opções de linha de comando opcionais. Use aspas adequadamente para garantir que os espaços na linha de comando não sejam interpretados erroneamente.

### <a name="the-reinstall-command"></a>O comando reinstalar

A linha de comando REINSTALL declarada no valor ReinstallCommand é executada quando o usuário usa a página **Definir acesso do programa e padrões do computador** para selecionar seu programa como o padrão para seu tipo de cliente. no Windows Vista e posterior, o acesso a essa página requer um nível de privilégio de administrador. em Windows 8, se você registrou seu aplicativo usando o mesmo nome para **definir o acesso do programa e os padrões do computador** e os **programas padrão**, os padrões especificados em **programas padrão** para esse aplicativo serão aplicados para o usuário atual, bem como a execução do comando reinstalar.

O programa iniciado pela linha de comando de reinstalação deve associar o aplicativo ao conjunto completo de tipos de [arquivo](fa-intro.md) e [protocolo](/previous-versions//aa767743(v=vs.85)) que o aplicativo pode manipular. Todos os aplicativos devem estabelecer a capacidade do manipulador no comando reinstalar. Os aplicativos podem usar o comando reinstalar para registrar o recurso, bem como, opcionalmente, estabelecer o status padrão. Quando um aplicativo opta por implementar o status do manipulador de capacidade e padrão no comando reinstalar, ele também deve restabelecer os links ou atalhos visíveis desejados. Os pontos de entrada visíveis a maioria dos aplicativos escolhem são listados no [comando Ocultar ícones](#the-hide-icons-command).

> [!Note]  
> É altamente recomendável que os aplicativos implementem o recurso de manipulação no comando REINSTALL.

 

Depois que o processo de reinstalação for concluído, o programa iniciado pela linha de comando de reinstalação deverá sair. Ele não deve iniciar o programa correspondente; Ele deve meramente registrar os padrões. Por exemplo, o comando reinstalar de um navegador não deve abrir o home page do usuário.

> [!Note]  
> para clientes de navegador e email no Windows XP e Windows Vista, os aplicativos que optam por estabelecer o recurso de manipulação e o status padrão no comando reinstalar devem se registrar no ícone correspondente na parte superior do menu Iniciar. Consulte o [registro do menu iniciar](#start-menu-registration) para obter informações adicionais.

 

### <a name="the-hide-icons-command"></a>O comando Ocultar ícones

A linha de comando declarada no valor HideIconsCommand é executada quando o usuário limpa a caixa **habilitar acesso a este programa** na página **Definir acesso do programa e padrões do computador** . Essa linha de comando deve ocultar todos os pontos de acesso do programa visíveis na interface do usuário. As diretrizes específicas são remover atalhos e ícones dos seguintes locais:

-   Ícones da área de trabalho
-   links de menu Iniciar, incluindo o grupo de **inicialização**
-   Links da barra de início rápido
-   Área de notificação
-   Menus de atalho
-   Faixa de tarefas da pasta

Essa linha de comando também deve impedir invocações automáticas do programa, como as especificadas na chave do registro de **execução** . Os fornecedores são incentivados a implementar essas diretrizes no retorno de chamada ocultar acesso do aplicativo.

Você não precisa ceder o registro (funcionalidade do aplicativo) dos tipos de arquivo quando os ícones estão ocultos. Você também não precisa ceder o status padrão do aplicativo para tipos de arquivo e protocolo. Isso pode levar a uma experiência de usuário inadequada quando esses tipos são encontrados na interface do usuário.

Depois de ocultar os ícones com êxito, você deve atualizar o valor do registro IconsVisible para 0, conforme mostrado:

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 0
```

A entrada IconsVisible é do tipo **reg \_ DWORD**.

### <a name="an-alternate-hide-icons-method-in-spad"></a>Um método alternativo para ocultar ícones em SPAD

Para alguns aplicativos herdados, uma implementação completa do acesso de ocultar pode não ser prática. Um método alternativo que alcança o mesmo efeito é desinstalar o aplicativo. A seção a seguir mostra o comportamento de exemplo e o código de exemplo para implementar essa alternativa. Em geral, os ISVs (fornecedores independentes de software) devem evitar essa alternativa, pois ela irá:

-   Desinstale completamente o aplicativo do sistema.
-   Remova os padrões selecionados anteriormente.
-   Não deixe a opção de interface do usuário para reinstalar o aplicativo.
-   Tornar o recurso habilitar acesso não mais disponível, pois uma desinstalação remove o aplicativo completamente do SPAD.

A experiência do usuário recomendada é a seguinte:

-   Quando o usuário desmarca a caixa de seleção **habilitar o acesso a este programa** no SPAD, a interface do usuário a seguir é apresentada.

    ![caixa de diálogo sobre como ocultar o acesso ao programa](images/hideaccessvista.png)

-   Quando o usuário seleciona **OK**, o item do painel de controle **programas e recursos** é iniciado para permitir que o usuário desinstale o aplicativo.
-   Windows Os usuários do XP devem ser apresentados com essa caixa de diálogo.

    ![caixa de diálogo equivalente do Windows Xp](images/hideaccessxp.png)

-   Quando o Windows XP seleciona **OK,**  o item Adicionar ou Remover Programas Painel de Controle é lançado para permitir que o usuário desinstale o aplicativo.

O código a seguir fornece uma implementação reutilizável para o recurso Ocultar Acesso, conforme descrito acima. Ele pode ser usado no Windows XP, Windows Vista e Windows 7.


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
            // Windows XP
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



### <a name="the-show-icons-command"></a>O comando Mostrar Ícones

A linha de comando declarada na entrada ShowIconsCommand  é executada quando o usuário verifica a caixa Habilitar acesso a esse programa na página Definir Acesso ao Programa e Padrões **do** Computador. Essa linha de comando pode restaurar os pontos de acesso do programa, incluindo  aqueles no **menu** Iniciar, na área de trabalho  e no grupo Inicialização, bem como invocações automáticas normais, como aquelas especificadas na chave Executar registro. Os pontos de acesso visíveis de interesse para a maioria dos aplicativos estão [listados no Comando Ocultar Ícones](#the-hide-icons-command). O aplicativo não deve alterar os padrões por usuário; que a alteração deve ser feita pelo usuário por meio de **Programas Padrão**.

Depois de mostrar com êxito seus ícones, você deve atualizar o valor do Registro IconsVisible para 1, conforme mostrado:

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 1
```

Observe que, se você tiver usado a entrada HideIconsCommand para solicitar uma desinstalação do aplicativo, a entrada ShowIconsCommand não será usada. Ele deve ser removido do Registro com o restante das informações do aplicativo durante o processo de desinstalação.

### <a name="group-program-configuration"></a>Configuração do Programa de Grupo

> [!Note]  
> Esta seção não se aplica ao Windows 2000.

 

Como parte da preparação do sistema, um OEM pode estabelecer uma configuração que oculta pontos de acesso para o navegador da Microsoft, email, reprodução de mídia, mensagens instantâneas ou máquina virtual para programas cliente Java e especifica seus próprios programas padrão. Os OEMs podem permitir que os usuários redefinam seus computadores a qualquer momento para essa configuração padrão definindo os seguintes valores do Registro.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  OEMShowIcons = 1
                  OEMDefault = 1
```

Se essas chaves estão definidas, os usuários  podem restaurar a configuração do OEM selecionando a opção Fabricante do Computador na página Definir Acesso ao Programa e Padrões **do** Computador. Se essas chaves não estão definidas, a **opção Fabricante** do Computador não é mostrada.

A **entrada OEMShowIcons,** se presente, define o ícone mostrar estado para o cliente especificado que será aplicado se o usuário selecionar **Fabricante do Computador**. Um valor de 1 faz com que ícones sejam mostrados e um valor de 0 faz com que os ícones não sejam mostrados. Se **OEMShowIcons** estiver ausente, **selecionar** Fabricante do Computador não terá nenhum efeito na configuração de exibição de ícone. **OEMShowIcons** é do tipo **REG \_ DWORD.**

A **entrada OEMDefault,** se presente e definida como 1, estabelece a preferência OEM para o cliente padrão do tipo indicado. Somente um cliente de um tipo específico pode ser marcado como o padrão OEM. Se mais do que o registro de um cliente contiver a entrada **OEMDefault,** todos serão ignorados e o cliente atual continuará sendo usado como cliente padrão. Se a **entrada OEMDefault** não estiver presente ou estiver presente e definida como 0, esse cliente específico não será usado como o cliente padrão se o usuário selecionar **Fabricante do Computador**. **OEMDefault é** do tipo **REG \_ DWORD.**

Além da opção de redefinir seus computadores para a configuração padrão estabelecida pelo OEM, os usuários têm três outras opções de configuração:

-   De definir o computador como uma configuração Windows Microsoft. Nesse caso, a página Definir Acesso ao Programa e Padrões do Computador permite o acesso a todos os softwares da Microsoft e não Microsoft no computador registrado nas **categorias** de produto relevantes. Os Windows microsoft são selecionados como a opção padrão para cada categoria.
-   De definir o computador como uma configuração que não seja da Microsoft. Essa configuração oculta os pontos de acesso (como o **menu** Iniciar) para Windows Internet Explorer, Windows Media Player, Windows Messenger e Microsoft Outlook Express. Ele permite o acesso ao software não Microsoft no computador nessas categorias. Além disso, se um programa não Microsoft estiver disponível em uma categoria, ele será definido como o padrão para essa categoria. Se mais de um programa não Microsoft estiver disponível em uma categoria, o usuário será solicitado a escolher qual programa não Microsoft deve ser usado como o padrão.
-   Estabeleça uma configuração personalizada. Os usuários fazem suas próprias seleções para habilenciar ou remover o acesso, combinando programas da Microsoft e que não são da Microsoft conforme a sua escolha. Os usuários estabelecem opções padrão de categoria por categoria.

Os usuários podem alterar qualquer uma dessas opções a qualquer momento.

### <a name="browser-registration-example"></a>Exemplo de registro do navegador

O exemplo a seguir mostra o registro **Completo de InstallInfo** para um navegador de Exibição Lit fictício. Nesse caso, as opções de linha de comando permitem que o arquivo Litview.exe execute as ações necessárias para cada valor.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\Litview.exe" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /showicons
                  IconsVisible = 1
```

Observe que aspas são colocadas em torno dos caminhos porque contêm espaços inseridos.

## <a name="registration-elements-for-specific-client-types"></a>Elementos de registro para tipos de cliente específicos

As informações a seguir também podem ser encontradas nos recursos listados na seção Tópicos Relacionados no final deste tópico.

-   [Iniciar registro de menu](#start-menu-registration)
-   [Registro de cliente de email](#mail-client-registration)

### <a name="start-menu-registration"></a>Iniciar registro de menu

No Windows XP, os aplicativos normalmente registram padrões em um escopo **de computador (HKEY \_ LOCAL \_ MACHINE)** em vez de um usuário (**HKEY CURRENT \_ \_ USER).** Com a introdução do Windows Vista do UAC (Controle de Conta de Usuário), os aplicativos que reivindicam os **slots** de **Internet** e email no **menu** Iniciar devem implementar o comando de reinstalação dentro do contexto de execução correto.

> [!Note]  
> O menu Iniciar **de email foi** removido a partir Windows 7. No entanto, o registro discutido nesta seção ainda deve ser executado porque atribui o cliente MAPI padrão.

 

Um usuário limitado no Windows XP, Windows Vista ou Windows 7 não pode acessar o SPAD. Por esse motivo, os desenvolvedores são incentivados a se registrar no item Definir seus programas **padrão** Painel de Controle para que qualquer usuário possa gerenciar padrões de aplicativo por usuário.

As seleções feitas no SPAD só devem afetar as configurações por computador.

De definir o valor do Registro da seguinte forma.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            (Default) = CanonicalName
```

> [!Note]
> 
> **As informações a seguir se Windows xp somente.**
> 
> Se o registro do padrão no nível do computador em HKEY LOCAL MACHINE conforme mostrado acima for bem-sucedido, o aplicativo deverá excluir o valor atribuído à entrada Padrão na \_ \_ seguinte sub-chave:
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
> ```
> 
> Se o registro do padrão no nível do computador em HKEY LOCAL MACHINE conforme mostrado acima falhar, geralmente porque o usuário não tem permissão de gravação para a \_ sub-chave, o aplicativo deve definir o \_ seguinte valor:
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
>             (Default) = CanonicalName
> ```
> 
> Isso registra o nome canônico somente para o usuário atual, não para todos os usuários.

 

Depois de atualizar as chaves do Registro, o programa deve transmitir a mensagem [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) com **wParam** = 0 e **lParam** apontando para a cadeia de caracteres terminada em nulo "Clientes de Software \\ \\ **ClientTypeName"** para notificar o sistema operacional de que o cliente padrão foi alterado.

### <a name="mail-client-registration"></a>Registro de cliente de email

Para um cliente de email, o programa precisa ter configurações registradas na chave **HKEY \_ CLASSES \_ ROOT** mailto para atender a \\  URLs que usam o `mailto` protocolo. Definir valores e chaves que espelham essas configurações na chave a seguir.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
```

Essa hierarquia do Registro substitui a hierarquia de registro `mailto` existente encontrada em **HKEY CLASSES \_ \_ ROOT** \\ **mailto**. A hierarquia permanece a mesma, somente o local foi alterado. O formato dessa hierarquia está documentado no MSDN em Visão geral e tutoriais do protocolo [assíncrono plug-able.](/previous-versions//aa767913(v=vs.85)) Normalmente, o protocolo é registrado em um programa em vez de um protocolo assíncrono, caso em que a documentação sobre Como registrar um aplicativo em um esquema `mailto` [de URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85)) se aplica.

O exemplo a seguir mostra `mailto` a seção do registro de um manipulador registrado em um `mailto` programa.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = %FilePath%,IconIndex
                     shell
                        open
                           command
                              (Default) = command line
```

O valor do Registro EditFlags está documentado em [Tipos](fa-file-types.md) de Arquivo na seção intitulada "Definindo atributos de tipo de arquivo".

## <a name="complete-sample-registrations"></a>Concluir registros de exemplo

Os exemplos a seguir são fornecidos para mostrar os requisitos de registro completos para os vários tipos de cliente.

-   [Um navegador de exemplo](#a-sample-browser)
-   [Um navegador de email de exemplo](#a-sample-mail-browser)
-   [Um player de mídia de exemplo](#a-sample-media-player)
-   [Um programa de exemplo do Instant Messenger](#a-sample-instant-messenger-program)
-   [Uma máquina virtual de exemplo para Java](#a-sample-virtual-machine-for-java)

### <a name="a-sample-browser"></a>Um navegador de exemplo

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
                  shell
                     open
                        command
                           (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /homepage
```

### <a name="a-sample-mail-browser"></a>Um navegador de email de exemplo

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            Lit View
               (Default) = Lit View
               DLLPath = @C:\Program Files\LItwareInc\LitwareMAPI.dll
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /inbox
               protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
                     shell
                        open
                           command
                              (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /mailto:%1
```

### <a name="a-sample-media-player"></a>Um player de mídia de exemplo

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Media
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-instant-messenger-program"></a>Um programa de exemplo do Instant Messenger

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-virtual-machine-for-java"></a>Uma máquina virtual de exemplo para Java

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         JavaVM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

*As empresas de exemplo, organizações, produtos, nomes de domínio, endereços de email, logotipos, pessoas, locais e eventos descritos aqui são fictícios. Nenhuma associação com nenhuma empresa, organização, produto, nome de domínio, endereço de email, logotipo, pessoa, local ou evento real é pretendida ou deve ser inferida.*

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Programas padrão](default-programs.md)
</dt> <dt>

[Como registrar um navegador da Internet ou um cliente de email com o menu Windows iniciar](start-menu-reg.md)
</dt> <dt>

[Internet Explorer Layout do Registro do Cliente (consulte a seção "Definições de Chave do Registro do Cliente" )](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))
</dt> <dt>

[Tutoriais e visão geral do protocolo plug-able assíncrono](/previous-versions//aa767913(v=vs.85))
</dt> <dt>

[Registrando um aplicativo em um esquema de URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))
</dt> </dl>

 

 
