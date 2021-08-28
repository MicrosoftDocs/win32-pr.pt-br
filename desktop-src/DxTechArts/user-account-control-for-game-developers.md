---
title: Controle de conta de usuário para desenvolvedores de jogos
description: Este artigo descreve as diretrizes e as práticas recomendadas para os desenvolvedores de jogos trabalharem com eficiência com o recurso de segurança UAC (Controle de Conta de Usuário) introduzido no Windows Vista.
ms.assetid: dbac1c07-73dd-f2bc-3c5c-d6160368a88f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cb8b6ac31ef13e3ace4d439c82f4708673aeffb
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886062"
---
# <a name="user-account-control-for-game-developers"></a>Controle de conta de usuário para desenvolvedores de jogos

Este artigo descreve as diretrizes e as práticas recomendadas para os desenvolvedores de jogos trabalharem com eficiência com o recurso de segurança UAC (Controle de Conta de Usuário) introduzido no Windows Vista.

-   [Visão geral do controle de conta de usuário](#overview-of-user-account-control)
-   [Contas de usuário no Windows Vista](#user-accounts-in-windows-vista)
-   [Acesso a arquivos como um usuário padrão](#file-access-as-a-standard-user)
-   [Acesso ao Registro como um usuário padrão](#registry-access-as-a-standard-user)
-   [Elevação de privilégio](#privilege-elevation)
-   [Implicações do UAC com CreateProcess()](#uac-implications-with-createprocess)
-   [Definindo o nível de execução no manifesto do aplicativo](#setting-the-execution-level-in-the-application-manifest)
-   [Incorporação de um manifesto no Visual Studio](#embedding-a-manifest-in-visual-studio)
-   [Compatibilidade do UAC com jogos mais antigos](#uac-compatibility-with-older-games)
-   [Cenários e manifestos herddos](#legacy-scenarios-and-manifests)
-   [Conclusão](#conclusion)
-   [Leitura Adicional](#further-reading)

## <a name="overview-of-user-account-control"></a>Visão geral do controle de conta de usuário

O UAC (Controle de Conta de Usuário), introduzido no Windows Vista, é um recurso de segurança projetado para ajudar a impedir que invasores mal-intencionados usem pontos fracos ou bugs encontrados em aplicativos amplamente usados para alterar o sistema operacional ou outros programas instalados. Isso é feito executando a grande maioria dos programas e processos como um Usuário Padrão (também conhecido como Usuário Limitado, Usuário Restrito ou Usuário Least-Privileged) mesmo que a conta do usuário atual tenha credenciais administrativas. Um processo com privilégios de usuário padrão tem muitas restrições inerentes que o impedem de fazer alterações em todo o sistema.

O UAC também é responsável pela elevação de privilégio de um processo por meio de um esquema de autenticação baseado em diálogo iniciado após a execução de determinados processos designados como exigindo privilégios administrativos. A elevação de privilégio permite que os administradores executem a maioria de seus aplicativos em um nível de privilégio seguro (o mesmo que qualquer outro usuário padrão), mas também permitem processos e operações que exigem privilégios administrativos. O UAC dá suporte à autenticação over-the-shoulder para que um administrador possa conceder privilégios elevados a um programa enquanto um usuário padrão está conectado ao sistema no momento.

O recurso UAC está habilitado por padrão. Embora seja possível que um administrador desabilite o UAC em todo o sistema, isso tem várias ramificações negativas. Primeiro, isso diminui a segurança de todas as contas administrativas, pois todos os processos seriam executados com credenciais administrativas, mesmo quando a maioria dos aplicativos realmente não as exige. Com o UAC desabilitado, um aplicativo de usuário padrão que expõe uma vulnerabilidade explorável na segurança pode potencialmente ser usado para roubar informações privadas, instalar rootkits ou spyware, destruir a integridade do sistema ou hospedar ataques de vírus em outros sistemas. Enquanto com o UAC habilitado, a execução da maioria dos softwares como um usuário padrão limita muito os possíveis danos desse bug. Em segundo lugar, desativar o UAC desabilita muitas das soluções alternativas para compatibilidade de aplicativos que permitem que os usuários padrão verdadeiros executem com êxito uma ampla variedade de aplicativos. A desabilitação do UAC nunca deve ser recomendada como uma solução alternativa de compatibilidade.

É importante observar que os aplicativos devem se esforçar para usar apenas os direitos de usuário padrão, se possível. Embora os administradores possam elevar facilmente os privilégios de um processo, a elevação ainda requer interação e confirmação do usuário sempre que um aplicativo é executado que requer credenciais administrativas. Essa elevação também deve ser feita no momento em que o programa é iniciado, portanto, exigir credenciais administrativas mesmo para uma única operação requer expor o sistema a um risco maior para todo o tempo de execução do aplicativo. Usuários padrão sem capacidade de elevar seus privilégios também são comuns em configurações de família e negócios. "Executar como Administrador" não é uma boa solução alternativa para compatibilidade, expõe o usuário e o sistema a um risco de segurança maior e cria frustração para os usuários em muitas situações.

> [!Note]  
> O recurso controle de conta de usuário introduzido no Windows Vista também está presente no Windows 7. Embora a experiência do usuário trabalhando com os vários recursos do sistema tenha sido aprimorada em relação ao Controle de Conta de Usuário, o impacto nos aplicativos é basicamente o mesmo. Todas as recomendações Windows Vista neste artigo se aplicam Windows 7 também. Para obter detalhes sobre as alterações de interface do usuário do UAC para Windows 7, consulte [Interface do Usuário – Atualizações](../win7appqual/user-interface---user-account-control-dialog-updates.md)da caixa de diálogo Controle de Conta de Usuário .

 

## <a name="user-accounts-in-windows-vista"></a>Contas de usuário no Windows Vista

Windows O Vista categoriza cada usuário em dois tipos de conta de usuário: administradores e usuários padrão.

Uma conta de usuário padrão é semelhante a uma conta de usuário limitado no Windows XP. Assim como no Windows XP, um usuário padrão não pode gravar na pasta Arquivos de Programas, não pode gravar na parte HKEY LOCAL MACHINE do Registro e não pode executar tarefas que alteram o sistema, como instalar um driver de modo kernel ou acessar espaços de processo no nível do \_ \_ sistema.

A conta de Administrador foi alterada significativamente desde Windows XP foi lançado. Anteriormente, todos os processos lançados por um membro do grupo Administradores tinham privilégios administrativos. Com o UAC habilitado, todos os processos são executados com privilégios de usuário padrão, a menos que especificamente elevados por um administrador. Essa diferença torna as contas no grupo Administradores mais seguras, reduzindo o risco de segurança causado por possíveis bugs na maioria dos programas.

É importante que todos os aplicativos, especialmente os jogos, operem com eficiência e responsabilidade quando executados como um processo de usuário padrão. Todas as operações que exigem privilégios administrativos devem ser feitas no momento da instalação ou por programas auxiliares que solicitam explicitamente credenciais administrativas. Embora a elevação de privilégio seja bastante trivial para um membro do grupo Administradores, os usuários padrão devem adiar alguém com credenciais administrativas para inserir fisicamente sua senha para elevar privilégios. Como as contas protegidas por controles dos pais devem ser usuários padrão, essa será uma situação muito comum para jogadores que estão usando o Windows Vista.

Se seu jogo já estiver funcionando no Windows XP com contas de usuário limitadas, a mudança para o Controle de Conta de Usuário no Windows Vista deverá ser muito fácil. A maioria desses aplicativos funcionará no estado em que se está, embora a adição de um manifesto do aplicativo seja altamente recomendável. (Os manifestos são descritos posteriormente neste tópico em [Definindo o nível de execução no manifesto do aplicativo](#setting-the-execution-level-in-the-application-manifest).)

## <a name="file-access-as-a-standard-user"></a>Acesso a arquivos como um usuário padrão

O aspecto do jogo mais afetado pelas restrições de usuário padrão é a organização e a acessibilidade do sistema de arquivos. Você nunca deve presumir que seu jogo pode gravar arquivos na pasta em que o jogo está instalado. No Windows Vista, por exemplo, os privilégios de um usuário devem ser elevados pelo sistema operacional antes que um aplicativo possa gravar na pasta Arquivos de Programas. Para evitar isso, você deve categorizar os arquivos de dados do jogo por escopo e acessibilidade e usar a função [**SHGetFolderPath,**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) juntamente com as constantes CSIDL fornecidas pelo shell Windows, para gerar os caminhos de arquivo apropriados. As constantes CSIDL correspondem a pastas conhecidas no sistema de arquivos que o sistema operacional usa e promove para particionar arquivos globais e específicos do usuário.

A tentativa de criar ou gravar um arquivo ou diretório em uma pasta que não concede permissão de gravação ao processo falhará no Windows Vista se o aplicativo não tiver privilégios administrativos. Se o executável do jogo de 32 bits estiver em execução no modo herdado, porque ele não declarou um nível de execução solicitado, suas operações de gravação serão bem-sucedidas, mas serão sujeitas à virtualização, conforme descrito na seção "Compatibilidade do UAC com jogos mais antigos" mais adiante neste artigo.

**Tabela 1. Pastas conhecidas**



| Nome CSIDL             | Caminho típico (Windows Vista)                                                   | Direitos de Usuário Padrão | Direitos de administrador | Escopo de acesso | Descrição                                                                                                                      | Exemplos                                                          |
|------------------------|--------------------------------------------------------------------------------|----------------------|----------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| CSIDL \_ PERSONAL        | C: \\ Documentos de nome de usuário dos \\ \\ usuários                                                | Leitura/Gravação           | Leitura/Gravação           | Per-User     | Arquivos de jogo específicos do usuário que são lidos e modificados e podem ser manipulados fora do contexto do jogo.                          | Capturas de tela. Arquivos de jogo salvos com uma associação de extensão de arquivo. |
| CSIDL \_ LOCAL \_ APPDATA  | C: \\ Nome de usuário dos usuários \\ \\ AppData \\ Local                                           | Leitura/Gravação           | Leitura/Gravação           | Per-User     | Arquivos de jogo específicos do usuário que são lidos e modificados e são de uso somente dentro do contexto do jogo.                                 | Arquivos de cache de jogos. Configurações do player.                          |
| CSIDL \_ COMMON \_ APPDATA | C: \\ ProgramData                                                                | Ler/gravar se o proprietário  | Leitura/Gravação           | Todos os Usuários    | Arquivos de jogo que podem ser criados por um usuário e lidos por todos os usuários. O acesso de gravação é concedido somente ao criador do arquivo (proprietário). | Perfis de Usuário                                                     |
| ARQUIVOS DO PROGRAMA \_ \_ CSIDL  | C: \\ Arquivos de Programas<br/> ou<br/> C: \\ Arquivos de Programas (x86) <br/> | Somente leitura            | Leitura/Gravação           | Todos os Usuários    | Arquivos de jogos estáticos gravados pelo instalador do jogo s que são lidos por todos os usuários.                                                    | Ativos de jogos, como materiais e malhas.                        |



 

Seu jogo normalmente será instalado em uma pasta sob a pasta representada pela \_ constante arquivos de programas CSIDL \_ . No entanto, esse nem sempre é o caso. Em vez disso, você deve usar um caminho relativo do seu arquivo executável ao gerar cadeias de caracteres de caminho para arquivos ou diretórios localizados em sua pasta de instalação.

Você também deve evitar suposições embutidas em código sobre os caminhos de pasta conhecidos. por exemplo, no Windows XP Professional edição de 64 bits e Windows Vista x64, o caminho dos arquivos de programas é C: \\ arquivos de programas (x86) para programas de 32 bits e C: \\ arquivos de programas para programas de 64 bits. esses caminhos conhecidos são alterados do Windows XP, e os usuários podem reconfigurar o local de muitas dessas pastas e até mesmo localizá-las em unidades diferentes. Portanto, sempre use as constantes de CSIDl para evitar confusão e problemas potenciais. Windows a instalação compreende esses locais de pastas conhecidos e moverá os dados ao atualizar o sistema operacional do Windows XP; por outro lado, o uso de locais não padrão ou caminhos embutidos em código pode falhar bem após uma atualização do sistema operacional.

A atenção deve ser dada às diferenças sutis de usabilidade entre as pastas específicas do usuário especificadas por CSIDl \_ pessoal e CSIDL \_ local \_ AppData. A prática recomendada para selecionar a constante de CSIDl a ser usada para gravar um arquivo é usar a CSIDl \_ pessoal se o usuário for pretendo interagir com o arquivo, como clicar duas vezes nele para abri-lo em uma ferramenta ou aplicativo e usar \_ AppData local CSid \_ para outros arquivos. Ambas as pastas podem ser aproveitadas pelo seu aplicativo para armazenar e organizar arquivos de dados específicos do usuário, pois não há nenhuma diferença no seu escopo de acesso ou nível de privilégio. Deve-se ter cuidado para criar nomes de caminho que sejam exclusivos o suficiente para não colidir com outros aplicativos, mas curto o suficiente para manter o número de caracteres no caminho completo menor que o valor de \_ caminho máximo, 260.

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

## <a name="registry-access-as-a-standard-user"></a>Acesso de registro como usuário padrão

O acesso ao registro por um usuário padrão é restrito de maneira semelhante ao sistema de arquivos. Um usuário padrão tem permissão de acesso de leitura para todas as chaves no registro; no entanto, o acesso de gravação só é concedido à \_ subárvore de HKEY Current \_ User (HKCU), que é mapeada internamente para a subchave específica do usuário hKey \_ Users \\ ID de segurança (SID) do usuário atual. Um aplicativo que precisa gravar em qualquer local do registro diferente de HKEY \_ Current \_ User requer privilégios administrativos.

Se o aplicativo de 32 bits não contiver um nível de execução solicitado em seu manifesto, todas as gravações em HKEY \_ local \_ Machine \\ software serão virtualizadas, enquanto as gravações em outros locais fora do hKey \_ Current \_ User falharão.

O armazenamento de dados persistentes no registro, como a configuração de um usuário, não é recomendado. O método preferencial para armazenar dados persistentes do jogo é gravar os dados no sistema de arquivos chamando [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) e obter o valor de uma constante CSIDL, descrita na seção anterior.

## <a name="privilege-elevation"></a>Elevação de privilégio

no Windows Vista, qualquer aplicativo que exija privilégios administrativos deve declarar uma solicitação de um nível de execução administrativo em seu manifesto (descrito na próxima seção, [definindo o nível de execução no manifesto do aplicativo](#setting-the-execution-level-in-the-application-manifest)).

A elevação, como é conhecida, é o procedimento controlado pelo UAC para promover um processo a um processo administrativo. Os privilégios de um processo só podem ser elevados no momento da criação. Depois de criado, um processo nunca será promovido a um nível de privilégio mais alto. Por esse motivo. as operações que exigem credenciais administrativas devem ser isoladas para instaladores separados e outros programas auxiliares.

Após a execução de um programa, o UAC inspeciona o nível de execução solicitado no manifesto e, se forem necessários privilégios elevados, solicitará ao usuário atual uma das duas caixas de diálogo padrão: uma para um usuário padrão e outra para um administrador.

Se o usuário atual for um usuário padrão, o UAC solicitará ao usuário as credenciais de um administrador antes de permitir que o programa seja executado.

**Figura 1. Solicitar que um usuário padrão insira credenciais para uma conta administrativa**

![solicitar que um usuário padrão insira credenciais para uma conta administrativa](images/uac-prompt-elevation.jpg)

Se o usuário atual for um administrador, o UAC solicitará permissão ao usuário antes de permitir que o programa seja executado.

**Figura 2. Solicitar que um administrador autorize alterações no computador**

![solicitar que um administrador autorize alterações no computador](images/uac-prompt-authorization.jpg)

O aplicativo só receberá privilégios administrativos se um usuário padrão fornecer as credenciais administrativas apropriadas ou um usuário administrativo fornecer a confirmação; qualquer outra coisa fará com que o aplicativo seja encerrado.

É importante observar que um processo com privilégios elevados é executado como o usuário administrativo que inseriu as credenciais no prompt do UAC, e não como o usuário padrão que está conectado no momento. isso é semelhante ao **RunAs** no Windows XP o processo elevado obtém a pasta do administrador e as chaves do registro ao acessar dados por usuário, e todos os programas que o processo elevado inicia também herdam os locais de conta de usuário e direitos administrativos. Para os administradores que são solicitados a confirmar (**continuar** ou **Cancelar**), esses locais corresponderão aos locais do usuário no momento. Em geral, no entanto, processos que exigem elevação não devem operar em dados por usuário. Observe que isso pode afetar substancialmente como o instalador deve funcionar! Se o instalador, em execução como administrador, gravar em HKCU ou em um perfil de usuário, talvez esteja muito bem gravando no local errado. Considere a criação desses valores por usuário na primeira execução do jogo.

## <a name="uac-implications-with-createprocess"></a>Implicações do UAC com CreateProcess ()

O mecanismo de elevação do UAC não será invocado de uma chamada para a função do Win32 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)() para iniciar um executável que é configurado para exigir um nível de execução mais alto do que o processo atual. Como resultado, a chamada para **CreateProcess**() falhará com [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)() retornando elevação de erro \_ \_ necessária. **CreateProcess**() só terá sucesso quando o nível de execução do receptor for igual ou menor que o do chamador. Um processo não elevado que deve gerar processos elevados deve fazer isso usando a função [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)(), que fará com que o mecanismo de elevação do UAC seja disparado por meio do Shell.

## <a name="setting-the-execution-level-in-the-application-manifest"></a>Definindo o nível de execução no manifesto do aplicativo

Você declara o nível de execução solicitado de seu jogo adicionando uma extensão ao manifesto do aplicativo. O código XML a seguir mostra a configuração mínima necessária para definir o nível de execução para um aplicativo:

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

Ao definir explicitamente requestedExecutionLevel como "asInvoker", este exemplo declara que o sistema operacional se comportará corretamente sem privilégios administrativos. como resultado, o UAC desabilita a virtualização e executa o jogo com os mesmos privilégios que o chamador, que normalmente é privilégios de usuário padrão, pois o Windows Explorer é executado como usuário padrão.

O sistema operacional pode ser informado de que um jogo requer elevação para privilégios administrativos, substituindo "asInvoker" por "requireAdministrator", para criar a seguinte marca:

``` syntax
<ms_asmv2:requestedExecutionLevel level="requireAdministrator" uiAccess="false" />
```

Com essa configuração, o sistema operacional solicita ao usuário atual uma das caixas de diálogo de elevação padrão do UAC toda vez que o jogo é executado. É altamente recomendável que nenhum jogo exija privilégios de administrador para ser executado, pois não apenas essa caixa de diálogo se tornará apenas irritante, mas também fará com que o jogo seja incompatível com controles dos pais. Pense muito cuidadosamente antes de adicionar esse requisito a qualquer executável.

Um equívoco comum é que a adição de um manifesto que define requestedExecutionLevel como "requireAdministrator" ignora a necessidade de um prompt de elevação. Isso não é verdade. Ele simplesmente impede que o sistema operacional Adivinhe se seu aplicativo de instalação ou atualização precisa de privilégios administrativos. O usuário ainda será solicitado a autorizar a elevação.

Windows verifica a assinatura de qualquer aplicativo marcado para elevação antes de exibir o prompt do UAC. Um executável grande que é marcado para elevação leva mais tempo para ser verificado do que um pequeno executável e mais longo do que um executável marcado como "asInvoker". Os executáveis de instalação que são de extração automática devem, portanto, ser marcados como "asInvoker" e qualquer parte que precise ser marcada como "requireAdministrator" deve ser colocada em um executável auxiliar separado.

O atributo uiAccess, mostrado nos exemplos anteriores, deve ser sempre FALSE para jogos. Esse atributo especifica se os clientes de automação da interface do usuário têm acesso à interface do usuário do sistema protegido e têm implicações de segurança especiais se estiverem definidos como TRUE.

## <a name="embedding-a-manifest-in-visual-studio"></a>Inserindo um manifesto no Visual Studio

o suporte ao manifesto foi adicionado primeiro a Visual Studio a partir de VS2005. por padrão, um executável interno Visual Studio 2005 (ou mais recente) terá um manifesto gerado automaticamente inserido como parte do processo de compilação. O conteúdo do manifesto gerado automaticamente depende de determinadas configurações de projeto que você especifica na caixa de diálogo Propriedades do projeto.

o manifesto gerado automaticamente pelo Visual Studio 2005 não conterá um &lt; &gt; bloco trustInfo, pois não há nenhuma maneira de configurar o nível de execução do UAC nas propriedades do projeto. A maneira preferida de adicionar essas informações é permitir que o VS2005 Mescle um manifesto definido pelo usuário que contenha o &lt; &gt; bloco TrustInfo com o manifesto gerado automaticamente. Isso é tão simples quanto adicionar um \* arquivo. manifest à sua solução que contém o XML listado na seção anterior. quando Visual Studio encontrar um arquivo. manifest em sua solução, ele invocará automaticamente a ferramenta de manifesto (mt.exe) para mesclar os arquivos. manifest com o gerado automaticamente.

> [!Note]  
> há um bug na ferramenta de manifesto (mt.exe) fornecido pelo Visual Studio 2005 que resulta em um manifesto mesclado e inserido que pode causar problemas quando o executável é executado no Windows XP antes do SP3. O bug é um resultado de como a ferramenta redefine o namespace padrão na declaração do &lt; &gt; bloco TrustInfo. Felizmente, é fácil ignorar o problema inteiramente declarando explicitamente um namespace diferente no &lt; &gt; bloco TrustInfo e escopondo os nós filho para o novo namespace. O XML fornecido na seção anterior demonstra essa correção.

 

uma limitação no uso da ferramenta de mt.exe incluída no Visual Studio 2005 é que ela gerará um aviso ao processar &lt; o &gt; bloco trustInfo, pois a ferramenta não contém um esquema atualizado para validar o XML. para corrigir esse aviso, é recomendável substituir todos os arquivos de mt.exe no diretório de instalação do Visual Studio 2005 (há várias instâncias) com o mt.exe fornecido na SDK do Windows mais recente.

a partir do Visual Studio 2008, agora você pode especificar o nível de execução do aplicativo de dentro da caixa de diálogo de propriedades do projeto (figura 3) ou usando o sinalizador do vinculador/MANIFESTUAC. definir essas opções fará com que Visual Studio 2008 gere automaticamente e insira um manifesto com o &lt; bloco trustInfo apropriado &gt; no executável.

**Figura 3. definindo o nível de execução no Visual Studio 2008**

![definindo o nível de execução no Visual Studio 2008](images/setting-execution-level-in-vs2008.jpg)

a inserção de um manifesto em versões mais antigas do Visual Studio sem o suporte a manifesto ainda é possível, mas requer mais trabalho do desenvolvedor. para obter um exemplo de como fazer isso, examine o projeto Visual Studio 2003 incluído em qualquer amostra no SDK do DirectX antes da versão de 2008 de março.

## <a name="uac-compatibility-with-older-games"></a>Compatibilidade com o UAC com jogos mais antigos

se seu jogo parece estar salvando e carregando um arquivo com êxito no diretório arquivos de programas, mas nenhuma evidência do arquivo de íon Windows Vista, qualquer aplicativo de 32 bits que não contenha um nível de execução solicitado em seu manifesto é considerado um aplicativo herdado. antes do Windows Vista, a maioria dos aplicativos eram normalmente executados por usuários com privilégios administrativos. como resultado, esses aplicativos podiam ler e gravar livremente arquivos do sistema e chaves do registro, e muitos desenvolvedores não fizeram as alterações necessárias para funcionar corretamente em contas de usuário limitadas no Windows XP. no entanto, no Windows Vista, esses mesmos aplicativos falharão devido a privilégios de acesso insuficientes no novo modelo de segurança, o que impõe a execução de usuário padrão para aplicativos herdados. para reduzir o impacto disso, a virtualização também foi adicionada ao Windows Vista. a virtualização manterá milhares de aplicativos herdados funcionando bem no Windows Vista, sem exigir que esses aplicativos tenham privilégios elevados em todos os momentos simplesmente para serem bem-sucedidos em algumas operações secundárias. s encontrados, é provável que seu jogo esteja sendo executado no modo herdado e esteja sujeito à virtualização.

A virtualização afeta o sistema de arquivos e o registro redirecionando gravações sensíveis ao sistema (e operações de registro ou arquivo subsequentes) para um local por usuário dentro do perfil do usuário atual. Por exemplo, se um aplicativo tentar gravar no seguinte arquivo:

<dl> C: \\ arquivos de programas \\ nome da empresa \\ título \\config.ini  
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

Os aplicativos projetados corretamente para operar como com as credenciais de um usuário padrão (ou usuário limitado) em versões anteriores do Windows não serão afetados pelo UAC, eles serão executados sem elevação. No entanto, eles devem incluir um manifesto com seu nível de execução solicitado definido como "asInvoker" para estar em conformidade com os padrões de aplicativo para Vista.

## <a name="further-reading"></a>Leitura Adicional

Para assistência com a criação de aplicativos para Windows Vista compatíveis com o Controle de Conta de Usuário, baixe o seguinte white paper: requisitos de desenvolvimento de aplicativos [do Windows Vista](/previous-versions/dotnet/articles/bb530410(v=msdn.10))para compatibilidade de controle de conta de usuário.

Este white paper fornece etapas detalhadas sobre o processo de design, juntamente com exemplos de código, requisitos e práticas recomendadas. Este documento também detalha as atualizações técnicas e as alterações na experiência do usuário no Windows Vista.

Para obter mais informações sobre o Controle de Conta de Usuário, [visite Windows Vista: Controle de Conta de Usuário](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) no Microsoft [TechNet](https://www.microsoft.com/technet/).

Outro recurso útil é o artigo Ensinar seus aplicativos a reproduzir com o controle de conta de usuário do [Windows Vista,](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control)da [MSDN Magazine,](/archive/msdn-magazine/msdn-magazine-issues)de janeiro de 2007. Este artigo aborda problemas gerais de compatibilidade de aplicativos, bem como as vantagens e problemas de uso de pacotes do Windows Installer no Windows Vista.

Para obter mais informações sobre o bug e a correção do mt.exe, a ferramenta usada pelo Visual Studio 2005 para mesclar e inserir automaticamente um manifesto em um executável, consulte [Explorando manifestos parte 2: namespaces](https://techcommunity.microsoft.com/t5/Windows-Blog-Archive/bg-p/Windows-Blog-Archive/2006/09/08/exploring-manifests-part-2-default-namespaces-and-uac-manifests-in-windows-vista/) padrão e manifestos UAC no Windows Vista no blog de Chris Jackson no [MSDN](/archive/blogs/).

 

