---
title: Controle de conta de usuário para desenvolvedores de jogos
description: este artigo descreve as diretrizes e as práticas recomendadas para que os desenvolvedores de jogos trabalhem com eficiência com o recurso de segurança UAC (controle de conta de usuário) introduzido no Windows Vista.
ms.assetid: dbac1c07-73dd-f2bc-3c5c-d6160368a88f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14013a99926301d93a9b7b710af30f33f85b4fa1a48a60a6979c8a6868474e09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118396512"
---
# <a name="user-account-control-for-game-developers"></a>Controle de conta de usuário para desenvolvedores de jogos

este artigo descreve as diretrizes e as práticas recomendadas para que os desenvolvedores de jogos trabalhem com eficiência com o recurso de segurança UAC (controle de conta de usuário) introduzido no Windows Vista.

-   [Visão geral do controle de conta de usuário](#overview-of-user-account-control)
-   [contas de usuário no Windows Vista](#user-accounts-in-windows-vista)
-   [Acesso a arquivos como usuário padrão](#file-access-as-a-standard-user)
-   [Acesso de registro como usuário padrão](#registry-access-as-a-standard-user)
-   [Elevação de privilégio](#privilege-elevation)
-   [Implicações do UAC com CreateProcess ()](#uac-implications-with-createprocess)
-   [Definindo o nível de execução no manifesto do aplicativo](#setting-the-execution-level-in-the-application-manifest)
-   [Inserindo um manifesto no Visual Studio](#embedding-a-manifest-in-visual-studio)
-   [Compatibilidade com o UAC com jogos mais antigos](#uac-compatibility-with-older-games)
-   [Cenários herdados e manifestos](#legacy-scenarios-and-manifests)
-   [Conclusão](#conclusion)
-   [Leitura adicional](#further-reading)

## <a name="overview-of-user-account-control"></a>Visão geral do controle de conta de usuário

o UAC (controle de conta de usuário), introduzido no Windows Vista, é um recurso de segurança criado para ajudar a impedir que invasores mal-intencionados usem pontos fracos ou bugs encontrados em aplicativos amplamente usados para alterar o sistema operacional ou outros programas instalados. Isso é feito pela execução da grande maioria dos programas e processos como usuário padrão (também conhecido como usuário limitado, usuário restrito ou Least-Privileged usuário), mesmo que a conta do usuário atual tenha credenciais administrativas. Um processo com privilégios de usuário padrão tem muitas restrições inerentes que o impedem de fazer alterações em todo o sistema.

O UAC também é responsável pela elevação de privilégios de um processo pelo uso de um esquema de autenticação baseado em caixa de diálogo, iniciado na execução de determinados processos designados como exigindo privilégios administrativos. A elevação de privilégio permite que os administradores executem a maioria de seus aplicativos em um nível de privilégio seguro (o mesmo que qualquer outro usuário padrão), mas também permite processos e operações que exigem privilégios administrativos. O UAC dá suporte à autenticação no ressalto para que um administrador possa conceder privilégios elevados a um programa enquanto um usuário padrão estiver conectado ao sistema no momento.

O recurso UAC é habilitado por padrão. Embora seja possível que um administrador desabilite todo o sistema do UAC, isso tem várias ramificações negativas. Primeiro, isso enfraquece a segurança de todas as contas administrativas, pois todos os processos seriam executados com credenciais administrativas, mesmo quando a maioria dos aplicativos não os exige realmente. Com o UAC desabilitado, um aplicativo de usuário padrão que expõe uma vulnerabilidade explorável na segurança pode potencialmente ser usado para roubar informações particulares, instalar rootkits ou spyware, destruir a integridade do sistema ou hospedar ataques zumbis em outros sistemas. Enquanto com o UAC habilitado, a execução da maioria do software como usuário padrão limita bastante o dano potencial desse bug. Em segundo lugar, desativar o UAC desabilita muitas das soluções alternativas para a compatibilidade de aplicativos que permitem que os usuários padrão verdadeiros executem com êxito uma ampla gama de aplicativos. Desabilitar o UAC nunca deve ser recomendado como solução alternativa de compatibilidade.

É importante observar que os aplicativos devem se esforçar para usar somente direitos de usuário padrão, se possível. Embora os administradores possam facilmente elevar os privilégios de um processo, a elevação ainda exige a interação do usuário e a confirmação sempre que um aplicativo é executado, o que exige credenciais administrativas. Essa elevação também deve ser feita no momento em que o programa é iniciado, portanto, exigir credenciais administrativas mesmo para uma única operação requer a exposição do sistema a um risco maior para todo o tempo de execução do aplicativo. Os usuários padrão sem qualquer capacidade de elevar seus privilégios também são comuns em configurações de negócios e de família. "Executar como administrador" não é uma boa solução alternativa para a compatibilidade, expõe o usuário e o sistema a um risco maior de segurança e cria frustração para os usuários em muitas situações.

> [!Note]  
> o recurso de controle de conta de usuário introduzido no Windows Vista também está presente no Windows 7. Embora a experiência do usuário que trabalha com os vários recursos do sistema tenha sido aprimorada em relação ao controle de conta de usuário, o impacto nos aplicativos é basicamente o mesmo. todas as recomendações do Windows Vista neste artigo também se aplicam ao Windows 7. para obter detalhes sobre as alterações da interface do usuário do UAC para o Windows 7, consulte [user Interface-caixa de diálogo controle de conta de usuário](../win7appqual/user-interface---user-account-control-dialog-updates.md).

 

## <a name="user-accounts-in-windows-vista"></a>contas de usuário no Windows Vista

Windows O vista categoriza cada usuário em dois tipos de conta de usuário: administradores e usuários padrão.

uma conta de usuário padrão é semelhante a uma conta de usuário limitado no Windows XP. como no Windows XP, um usuário padrão não pode gravar na pasta arquivos de programas, não pode gravar na \_ parte do computador LOCAL HKEY \_ do registro e não pode executar tarefas que alteram o sistema, como a instalação de um driver de modo kernel ou o acesso a espaços de processo no nível do sistema.

a conta de administrador mudou significativamente desde que o Windows XP foi lançado. Anteriormente, todos os processos iniciados por um membro do grupo Administradores receberam privilégios administrativos. Com o UAC habilitado, todos os processos são executados com privilégios de usuário padrão, a menos que seja especificamente elevado por um administrador. Essa diferença torna as contas no grupo Administradores mais seguras, reduzindo o risco de segurança apresentado por possíveis bugs na maioria dos programas.

É importante que todos os aplicativos, especialmente jogos, operem com eficiência e responsabilidade quando executados como um processo de usuário padrão. Todas as operações que exigem privilégios administrativos devem ser feitas no momento da instalação ou por programas auxiliares que solicitam credenciais administrativas explicitamente. Embora a elevação de privilégios seja bastante trivial para um membro do grupo Administradores, os usuários padrão devem adiar para alguém com credenciais administrativas para inserir fisicamente sua senha para elevar privilégios. como as contas protegidas pelos controles dos pais devem ser usuários padrão, essa será uma situação muito comum para os jogadores que estão usando o Windows Vista.

se o seu jogo já estiver trabalhando no Windows XP com contas de usuário limitado, a mudança para o controle de conta de usuário no Windows Vista deve ser muito fácil. A maioria desses aplicativos funcionará no estado em que se encontra, embora a adição de um manifesto de aplicativo seja altamente recomendada. (Os manifestos são descritos posteriormente neste tópico em [definindo o nível de execução no manifesto do aplicativo](#setting-the-execution-level-in-the-application-manifest).)

## <a name="file-access-as-a-standard-user"></a>Acesso a arquivos como usuário padrão

O aspecto do seu jogo mais afetado pelas restrições de usuário padrão é a organização do sistema de arquivos e a acessibilidade. Você nunca deve assumir que o jogo pode gravar arquivos na pasta onde o jogo está instalado. no Windows Vista por exemplo, os privilégios de s do usuário devem ser elevados pelo sistema operacional antes que um aplicativo possa gravar na pasta arquivos de programas. para evitar isso, você deve categorizar os arquivos de dados do jogo por escopo e acessibilidade e usar a função [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) , juntamente com as constantes de csidl fornecidas pelo Windows shell, para gerar os caminhos de arquivo apropriados. As constantes de CSIDl correspondem a pastas conhecidas no sistema de arquivos que o sistema operacional usa e promove para particionar arquivos globais e específicos do usuário.

a tentativa de criar ou gravar um arquivo ou diretório em uma pasta que não conceda permissão de gravação ao processo falhará em Windows Vista se o aplicativo não tiver privilégios administrativos. Se o seu executável de jogo de 32 bits estiver em execução no modo herdado, porque ele não declarou um nível de execução solicitado, suas operações de gravação terão sucesso, mas estarão sujeitas à virtualização, conforme descrito na seção "compatibilidade do UAC com jogos mais antigos", posteriormente neste artigo.

**Tabela 1. Pastas conhecidas**



| Nome CSIDl             | caminho típico (Windows Vista)                                                   | Direitos de usuário padrão | Direitos de administrador | Escopo de acesso | Descrição                                                                                                                      | Exemplos                                                          |
|------------------------|--------------------------------------------------------------------------------|----------------------|----------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| pessoa CSIDl \_ pessoal        | C: \\ usuários \\ nome de usuário \\ documentos                                                | Leitura/Gravação           | Leitura/Gravação           | Per-User     | Arquivos de jogos específicos do usuário que são lidos e modificados e podem ser manipulados fora do contexto do jogo.                          | Capturas de tela. Arquivos de jogos salvos com uma associação de extensão de arquivo. |
| \_AppData local CSIDL \_  | C: \\ Users \\ User name \\ AppData \\ local                                           | Leitura/Gravação           | Leitura/Gravação           | Per-User     | Arquivos de jogos específicos do usuário que são lidos e modificados e são usados somente dentro do contexto do jogo.                                 | Arquivos de cache do jogo. Configurações do Player.                          |
| AppData comuns de CSIDl \_ \_ | C: \\ ProgramData                                                                | Ler/gravar se proprietário  | Leitura/Gravação           | Todos os Usuários    | Arquivos de jogos que podem ser criados por um usuário e lidos por todos os usuários. O acesso de gravação é concedido somente ao criador do arquivo (proprietário). | Perfis de Usuário                                                     |
| arquivos de \_ programa CSIDL \_  | C: \\ arquivos de programas<br/> ou<br/> C: \\ arquivos de programas (x86) <br/> | Somente leitura            | Leitura/Gravação           | Todos os Usuários    | Arquivos de jogo estáticos gravados pelo instalador do jogo que são lidos por todos os usuários.                                                    | Ativos de jogo, como materiais e malhas.                        |



 

Seu jogo normalmente será instalado em uma pasta na pasta representada pela constante CSIDL \_ PROGRAM \_ FILES. No entanto, esse nem sempre é o caso. Em vez disso, você deve usar um caminho relativo do arquivo executável ao gerar cadeias de caracteres de caminho para arquivos ou diretórios localizados na pasta de instalação.

Você também deve evitar suposições em código sobre os caminhos de pasta conhecidos. Por exemplo, no Windows XP Professional 64 bits Edition e no Windows Vista x64, o caminho dos arquivos de programa é C: Arquivos de Programas (x86) para programas de 32 bits e C: Arquivos de Programas para programas \\ \\ de 64 bits. Esses caminhos conhecidos são alterados do Windows XP e os usuários podem reconfigurar o local de muitas dessas pastas e até mesmo localizá-los em unidades diferentes. Portanto, sempre use as constantes CSIDL para evitar confusão e possíveis problemas. Windows A instalação compreende esses locais de pasta conhecidos e move os dados ao atualizar o sistema operacional do Windows XP; Por outro lado, o uso de locais não padrão ou caminhos em código pode falhar após uma atualização do sistema operacional.

A atenção deve ser dada às diferenças sutis de usabilidade entre as pastas específicas do usuário especificadas por CSIDL PERSONAL e \_ CSIDL \_ LOCAL \_ APPDATA. A prática recomendada para selecionar a constante CSIDL a ser usada para escrever um arquivo é usar CSIDL PERSONAL se o usuário deve interagir com o arquivo, como clicar duas vezes nele para abri-lo em uma ferramenta ou aplicativo e usar \_ CSIDL LOCAL APPDATA para \_ outros \_ arquivos. Ambas as pastas podem ser aproveitadas pelo seu aplicativo para armazenar e organizar arquivos de dados específicos do usuário, pois não há nenhuma diferença em seu escopo de acesso ou nível de privilégio. É preciso ter cuidado para criar nomes de caminho exclusivos o suficiente para não colidir com outros aplicativos, mas curto o suficiente para manter o número de caracteres no caminho completo menor que o valor de MAX \_ PATH, 260.

O código a seguir fornece um exemplo de como gravar um arquivo em uma pasta conhecida:

``` syntax
#include <windows.h>
#include <shlobj.h>
#include <shlwapi.h>
        ...
        ...
        ...
        TCHAR strPath[MAX_PATH];
        if( SUCCEEDED(
        SHGetFolderPath( NULL, CSIDL_PERSONAL, NULL, SHGFP_TYPE_CURRENT, strPath ) ) )
        {
        PathAppend( strPath, TEXT( "Company Name\\Title" ) );

        if( !PathFileExists( strPath ) )
        {
        if( ERROR_SUCCESS != SHCreateDirectoryEx( NULL, strPath, NULL ) )
        return E_FAIL;
        }

        PathAppend( strPath, TEXT( "gamefile.txt" ) );

        // strPath is now something like:
        // C:\Users\<current user>\Documents\Company Name\Title\gamefile.txt
        // Open the file for writing
        HANDLE hFile = CreateFile(strPath, GENERIC_WRITE, NULL, NULL, CREATE_ALWAYS, FILE_ATTRIBUTE_NORMAL, NULL);

        if( INVALID_HANDLE_VALUE != hFile )
        {
        // TODO: Write to file
        CloseHandle(hFile);
        }
        }
```

## <a name="registry-access-as-a-standard-user"></a>Acesso ao Registro como um usuário padrão

O acesso ao Registro por um usuário padrão é restrito de maneira semelhante ao sistema de arquivos. Um usuário padrão tem permissão para acesso de leitura a todas as chaves no Registro; No entanto, o acesso de gravação só é concedido à subárvore \_ \_ HKEY HKCU (USUÁRIO ATUAL), que é mapeada internamente para a SID \_ (ID de Segurança dos Usuários) da sub-chave específica do usuário do \\ usuário atual. Um aplicativo que precisa gravar em qualquer local do Registro diferente de HKEY \_ CURRENT USER requer privilégios \_ administrativos.

Se o aplicativo de 32 bits não contém um nível de execução solicitado em seu manifesto, todas as gravações no HKEY LOCAL MACHINE Software serão virtualizadas, enquanto as gravações em outros locais fora do \_ \_ \\ HKEY \_ CURRENT USER \_ falharão.

O armazenamento de dados persistentes no Registro, como a configuração de um usuário, não é recomendado. O método preferencial de armazenar dados persistentes do seu jogo é gravar os dados no sistema de arquivos chamando [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) e obter o valor de uma constante CSIDL, descrito na seção anterior.

## <a name="privilege-elevation"></a>Elevação de privilégio

No Windows Vista, qualquer aplicativo que exija privilégios administrativos deve declarar uma solicitação para um nível de execução administrativa em seu manifesto (descrito na próxima seção, Definindo o nível de execução no manifesto do [aplicativo).](#setting-the-execution-level-in-the-application-manifest)

Elevação, como é conhecido, é o procedimento orientado pela UAC para promover um processo para um processo administrativo. Os privilégios de um processo só podem ser elevados no momento da criação. Depois de criado, um processo nunca será promovido para um nível de privilégio mais alto. Por esse motivo. operações que exigem credenciais administrativas devem ser isoladas para instaladores separados e outros programas auxiliares.

Após a execução de um programa, o UAC inspeciona o nível de execução solicitado no manifesto e, se privilégios elevados são necessários, solicita ao usuário atual uma das duas caixas de diálogo padrão: uma para um usuário padrão e outra para um administrador.

Se o usuário atual for um usuário padrão, o UAC solicitará ao usuário as credenciais de um administrador antes de permitir que o programa seja executado.

**Figura 1. Solicitar que um usuário padrão insira credenciais para uma conta administrativa**

![solicitar que um usuário padrão insira credenciais para uma conta administrativa](images/uac-prompt-elevation.jpg)

Se o usuário atual for um administrador, o UAC solicitará permissão ao usuário antes de permitir que o programa seja executado.

**Figura 2. Solicitar que um administrador autorize as alterações no computador**

![solicitar que um administrador autorize as alterações no computador](images/uac-prompt-authorization.jpg)

O aplicativo só receberá privilégios administrativos se um usuário padrão fornece as credenciais administrativas apropriadas ou um usuário administrativo fornece confirmação; qualquer outra coisa fará com que o aplicativo seja encerrado.

É importante observar que um processo com privilégios elevados é executado como o usuário administrativo que entrou em credenciais no prompt do UAC em vez de como o usuário padrão que está conectado no momento. Isso é semelhante a **RunAs** no Windows XP, o processo elevado obtém a pasta e as chaves do Registro do administrador ao acessar dados por usuário, e todos os programas que o processo elevado inicia também herdam os direitos administrativos e os locais de conta de usuário. Para administradores que são solicitados a confirmar (**Continuar** ou Cancelar **),** esses locais corresponderão aos locais do usuário no momento. Em geral, no entanto, os processos que exigem elevação não devem operar em dados por usuário. Observe que isso pode afetar substancialmente como o instalador deve operar! Se o instalador, em execução como administrador, grava no HKCU ou no perfil de um usuário, ele pode muito bem estar gravando no local errado. Considere criar esses valores por usuário na primeira corrida do jogo.

## <a name="uac-implications-with-createprocess"></a>Implicações do UAC com CreateProcess()

O mecanismo de elevação do UAC não será invocado de uma chamada para a função Win32 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)() para iniciar um executável configurado para exigir um nível de execução mais alto do que o processo atual. Como resultado, a chamada para **CreateProcess**() falhará com [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)() retornando ERROR \_ ELEVATION \_ REQUIRED. **CreateProcess**() só terá êxito quando o nível de execução do chamador for igual ou menor que o do chamador. Um processo não elevado que deve gerar processos elevados deve fazer isso usando a função [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)(), que fará com que o mecanismo de elevação do UAC seja disparado por meio do shell.

## <a name="setting-the-execution-level-in-the-application-manifest"></a>Definindo o nível de execução no manifesto do aplicativo

Declare o nível de execução solicitado do jogo adicionando uma extensão ao manifesto do aplicativo. O código XML a seguir mostra a configuração mínima necessária para definir o nível de execução de um aplicativo:

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <ms_asmv2:trustInfo xmlns:ms_asmv2="urn:schemas-microsoft-com:asm.v2">
        <ms_asmv2:security>
            <ms_asmv2:requestedPrivileges>
                <ms_asmv2:requestedExecutionLevel level="asInvoker" uiAccess="false" />
            </ms_asmv2:requestedPrivileges>
        </ms_asmv2:security>
    </ms_asmv2:trustInfo>
</assembly>
```

No código anterior, o sistema operacional é informado de que o jogo requer apenas privilégios de usuário padrão pela seguinte marca:

``` syntax
<ms_asmv2:requestedExecutionLevel level="asInvoker" uiAccess="false" />
```

Ao definir explicitamente requestedExecutionLevel como "asInvoker", este exemplo declara ao sistema operacional que o jogo se comportará corretamente sem privilégios administrativos. Como resultado, o UAC desabilita a virtualização e executa o jogo com os mesmos privilégios do invocador, que normalmente são privilégios de usuário padrão, pois o Windows Explorer é executado como usuário padrão.

O sistema operacional pode ser informado de que um jogo requer elevação para privilégios administrativos substituindo "asInvoker" por "requireAdministrator", para criar a seguinte marca:

``` syntax
<ms_asmv2:requestedExecutionLevel level="requireAdministrator" uiAccess="false" />
```

Com essa configuração, o sistema operacional solicita ao usuário atual uma das caixas de diálogo de elevação de UAC padrão sempre que o jogo é executado. É altamente recomendável que nenhum jogo exige privilégios de administrador para ser executado, pois essa caixa de diálogo não só se tornará entediante rapidamente, mas também tornará o jogo incompatível com os controles dos pais. Pense com muito cuidado antes de adicionar esse requisito a qualquer executável.

Um erro comum é que adicionar um manifesto que define requestedExecutionLevel como "requireAdministrator" ignora a necessidade de um prompt de elevação. Isso não é verdade. Ele simplesmente impede que o sistema operacional adivinha se o aplicativo de instalação ou atualização precisa de privilégios administrativos. O usuário ainda será solicitado a autorizar a elevação.

Windows verifica a assinatura de qualquer aplicativo marcado para elevação antes de exibir o prompt do UAC. Um executável grande marcado para elevação leva mais tempo para ser marcado do que um executável pequeno e maior que um executável marcado como "asInvoker". Os executáveis de instalação que são autoextraíveis devem, portanto, ser marcados como "asInvoker", e qualquer parte que precise ser marcada como "requireAdministrator" deve ser colocada em um executável auxiliar separado.

O atributo uiAccess, mostrado nos exemplos anteriores, sempre deve ser FALSE para jogos. Esse atributo especifica se os clientes de automação da interface do usuário têm acesso à interface do usuário do sistema protegida e tem implicações especiais de segurança se definidas como TRUE.

## <a name="embedding-a-manifest-in-visual-studio"></a>Incorporação de um manifesto no Visual Studio

O suporte ao manifesto foi adicionado pela primeira vez Visual Studio a partir do VS2005. Por padrão, um executável criado no Visual Studio 2005 (ou mais novo) terá um manifesto gerado automaticamente inserido nele como parte do processo de build. O conteúdo do manifesto gerado automaticamente depende de determinadas configurações de projeto especificadas na caixa de diálogo de propriedades do projeto.

O manifesto gerado automaticamente pelo Visual Studio 2005 não conterá um bloco, pois não há como configurar o nível de execução do UAC nas propriedades <trustInfo> do projeto. A maneira preferencial de adicionar essas informações é permitir que o VS2005 mescale um manifesto definido pelo usuário que contém o bloco com o <trustInfo> manifesto gerado automaticamente. Isso é tão simples quanto adicionar um arquivo .manifest à sua solução que contém o \* XML listado na seção anterior. Quando Visual Studio encontrar um arquivo .manifest em sua solução, ele invocará automaticamente a Ferramenta de Manifesto (mt.exe) para mesclar os arquivos .manifest com o gerado automaticamente.

> [!Note]  
> Há um bug na Ferramenta de Manifesto (mt.exe) fornecida pelo Visual Studio 2005 que resulta em um manifesto mesclado e inserido que pode causar problemas quando o executável é executado no Windows XP antes do SP3. O bug é resultado de como a ferramenta redefine o namespace padrão após a declaração do <trustInfo> bloco. Felizmente, é fácil ignorar o problema inteiramente declarando explicitamente um namespace diferente no bloco e definindo o scoping dos nós filho para o <trustInfo> novo namespace. O XML fornecido na seção anterior demonstra essa correção.

 

Uma advertência no uso da ferramenta mt.exe incluída no Visual Studio 2005 é que ela gerará um aviso ao processar o bloco, pois a ferramenta não contém um esquema atualizado para validar o <trustInfo> XML. Para corrigir esse aviso, é recomendável substituir todos os arquivos mt.exe no diretório de instalação do Visual Studio 2005 (há várias instâncias) pelo mt.exe fornecido no SDK do Windows mais recente.

A partir do Visual Studio 2008, agora você pode especificar o nível de execução de um aplicativo de dentro da caixa de diálogo de propriedades do projeto (Figura 3) ou usando o sinalizador de vinculador /MANIFESTUAC. Definir essas opções fará Visual Studio 2008 gerar automaticamente e inserir um manifesto com o bloco apropriado <trustInfo> no executável.

**Figura 3. Definindo o nível de execução Visual Studio 2008**

![definindo o nível de execução no Visual Studio 2008](images/setting-execution-level-in-vs2008.jpg)

A incorporação de um manifesto em versões mais antigas do Visual Studio sem suporte de manifesto ainda é possível, mas exige mais trabalho do desenvolvedor. Para ver um exemplo de como fazer isso, examine o projeto Visual Studio 2003 incluído em qualquer exemplo no SDK do DirectX antes da versão de março de 2008.

## <a name="uac-compatibility-with-older-games"></a>Compatibilidade do UAC com jogos mais antigos

Se o jogo parece estar salvando e carregando um arquivo com êxito no diretório Arquivos de Programas, mas nenhuma evidência do arquivo iOn Windows Vista, qualquer aplicativo de 32 bits que não contenha um nível de execução solicitado em seu manifesto será considerado um aplicativo herdado. Antes do Windows Vista, a maioria dos aplicativos normalmente era executado por usuários com privilégios administrativos. Como resultado, esses aplicativos podem ler e gravar gratuitamente arquivos do sistema e chaves do Registro, e muitos desenvolvedores não fizeram as alterações necessárias para funcionar corretamente em Contas de Usuário Limitadas no Windows XP. No entanto, Windows Vista, esses mesmos aplicativos agora falhariam devido a privilégios de acesso insuficientes no novo modelo de segurança, que impõe a execução do usuário padrão para aplicativos herdáveis. Para atenuar o impacto disso, a virtualização também foi adicionada ao Windows Vista. A virtualização manterá milhares de aplicativos herdados funcionando bem no Windows Vista sem exigir que esses aplicativos tenham privilégios elevados em todos os momentos simplesmente para ter êxito em algumas operações secundárias. s encontrados, as chances são que seu jogo está em execução no modo herdado e foi sujeito à virtualização.

A virtualização afeta o sistema de arquivos e o Registro redirecionando gravações confidenciais do sistema (e operações subsequentes de arquivo ou registro) para um local por usuário dentro do perfil do usuário atual. Por exemplo, se um aplicativo tentar gravar no seguinte arquivo:

<dl> C: Título do nome da empresa de arquivos \\ \\ de \\ \\config.ini  
</dl>

a gravação é redirecionada automaticamente para:

<dl> C: Nome \\ de usuário dos usuários \\ \\ AppData Local \\ \\ VirtualStore Program Files Nome da \\ \\ \\ empresaconfig.ini \\  
</dl>

Da mesma forma, se um aplicativo tentar gravar um valor de Registro como o seguinte:

<dl> HKEY \_ LOCAL \_ MACHINE \\ Software \\ Company Name \\ Title  
</dl>

em vez disso, ele será redirecionado para:

<dl> HKEY \_ CURRENT \_ USER \\ Software \\ Classes \\ VirtualStore \\ MACHINE \\ Software \\ Company Name \\ Title  
</dl>

Arquivos e chaves do Registro afetados pela virtualização só são acessados por operações de arquivo e registro de aplicativos virtualizados que estão sendo executados como o usuário atual.

No entanto, há muitas restrições à virtualização. Uma delas é que os aplicativos de 64 bits nunca são executados no modo herdado para operações de compatibilidade sujeitas à virtualização em aplicativos de 32 bits falharão apenas em 64 bits. Além disso, se um aplicativo herdado em execução como um usuário padrão tentar gravar qualquer tipo de arquivo executável em um local que exija credenciais administrativas, a virtualização não ocorrerá e a gravação falhará.

**Figura 4. Processo de virtualização**

![processo de virtualização](images/uac-virtualization-process.jpg)

Quando um aplicativo herdado tenta uma operação de leitura em locais confidenciais do sistema no sistema de arquivos ou no Registro, os locais virtuais são pesquisados primeiro. Se o arquivo ou a chave do Registro não for encontrado, o sistema operacional acessará os locais padrão do sistema.

A virtualização será removida das versões subsequentes Windows, portanto, é importante não depender desse recurso. Em vez disso, você deve configurar explicitamente o manifesto do aplicativo para privilégios de usuário padrão ou administrativos, pois isso desabilitará a virtualização. A virtualização também não é óbvia para os usuários finais, portanto, embora a virtualização possa permitir que seu aplicativo seja executado, ela pode gerar chamadas de suporte e dificultar a busca de problemas para esses clientes.

Observe que, se o UAC estiver desabilitado, a virtualização também será desabilitada. Se a virtualização estiver desabilitada, as contas de usuário padrão se comportarão exatamente como contas de usuário limitadas no Windows XP e os aplicativos herdados poderão não funcionar corretamente para usuários padrão que de outra forma teriam êxito devido à virtualização.

## <a name="legacy-scenarios-and-manifests"></a>Cenários e manifestos herddos

Para a maioria dos cenários de uso, basta marcar o .exe com os elementos de manifesto UAC corretos e garantir que o aplicativo funcione corretamente, pois um Usuário Padrão é suficiente para excelente compatibilidade de UAC. A maioria dos jogadores está executando Windows Vista ou Windows 7 com o Controle de Conta de Usuário habilitado. Para Windows XP e usuários no Windows Vista ou Windows7 com o recurso controle de conta de usuário desabilitado, eles normalmente são executados usando contas de administrador. Embora esse seja um modo de operação menos seguro, ele geralmente não terá problemas de compatibilidade adicionais, embora, conforme mencionado acima, desabilitar o UAC desabilite a virtualização também.

Há um caso especial que vale a pena notar quando o programa é marcado como "requireAdministrator" no manifesto UAC. No Windows XP e no Windows Vista ou Windows 7 com o Controle de Conta de Usuário desabilitado, os elementos de manifesto UAC são ignorados pelo sistema. Nessa situação, os usuários com contas de administrador sempre executarão todos os programas com direitos de administrador completos e, portanto, esses programas funcionarão conforme o esperado. Windows Os Usuários Restritos do XP e os Usuários Padrão em execução no Windows Vista ou Windows 7, no entanto, sempre executarão esses programas com direitos restritos e todas as operações de nível de administrador falharão. Portanto, é recomendável que programas marcados como "requiretAdministrator" chamem [**IsUserAnAdmin**](/windows/win32/api/shlobj_core/nf-shlobj_core-isuseranadmin) na inicialização e exibem uma mensagem de erro fatal se ela retornar FALSE. Para o cenário de maioria acima, isso sempre terá êxito, mas fornece uma melhor experiência do usuário e uma mensagem de erro clara para essa situação rara.

## <a name="conclusion"></a>Conclusão

Como desenvolvedor de jogos destinado ao Windows de vários usuários, é fundamental que você projete seu jogo para operar de maneira eficaz e responsável. O arquivo executável principal do jogo não deve depender de privilégios administrativos. Isso não apenas impede a aparência de prompts de elevação sempre que seu jogo é executado, o que pode afetar negativamente a experiência geral do usuário, mas também permite que seu jogo aproveite outros recursos que exigem execução com privilégios de usuário padrão, como controles dos pais.

Os aplicativos projetados corretamente para operar como com as credenciais de um usuário padrão (ou usuário limitado) nas versões anteriores do Windows não serão afetados pelo UAC, eles serão executados sem elevação. No entanto, eles devem incluir um manifesto com seu nível de execução solicitado definido como "asInvoker" para estar em conformidade com os padrões de aplicativo para Vista.

## <a name="further-reading"></a>Leitura Adicional

Para assistência com a criação de aplicativos para Windows Vista compatíveis com o Controle de Conta de Usuário, baixe o seguinte white paper: Requisitos de desenvolvimento de aplicativos do Windows Vista para compatibilidade de controle de conta de [usuário.](/previous-versions/dotnet/articles/bb530410(v=msdn.10))

Este white paper fornece etapas detalhadas sobre o processo de design, juntamente com exemplos de código, requisitos e melhores práticas. Este documento também detalha as atualizações técnicas e as alterações na experiência do usuário no Windows Vista.

Para obter mais informações sobre o Controle de Conta de Usuário, [visite Windows Vista: Controle de Conta de Usuário](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) no Microsoft [TechNet](https://www.microsoft.com/technet/).

Outro recurso útil é o artigo Ensinar seus aplicativos a reproduzir com o controle de conta de usuário do [Windows Vista,](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control)da [MSDN Magazine,](/archive/msdn-magazine/msdn-magazine-issues)de janeiro de 2007. Este artigo aborda problemas gerais de compatibilidade do aplicativo, bem como as vantagens e problemas de uso de pacotes do Windows Installer no Windows Vista.

Para obter mais informações sobre o bug e a correção do mt.exe, a ferramenta usada pelo Visual Studio 2005 para mesclar e inserir automaticamente um manifesto em um executável, consulte [Explorando manifestos parte 2: namespaces](https://techcommunity.microsoft.com/t5/Windows-Blog-Archive/bg-p/Windows-Blog-Archive/2006/09/08/exploring-manifests-part-2-default-namespaces-and-uac-manifests-in-windows-vista/) padrão e manifestos UAC no Windows Vista no blog de Chris Jackson no [MSDN](/archive/blogs/).

 

