---
title: Controle de conta de usuário para desenvolvedores de jogos
description: Este artigo descreve as diretrizes e as práticas recomendadas para que os desenvolvedores de jogos trabalhem com eficiência com o recurso de segurança UAC (controle de conta de usuário) introduzido no Windows Vista.
ms.assetid: dbac1c07-73dd-f2bc-3c5c-d6160368a88f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57d5533a3fbdd349cc25dfde501a234bbd7b05b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366322"
---
# <a name="user-account-control-for-game-developers"></a>Controle de conta de usuário para desenvolvedores de jogos

Este artigo descreve as diretrizes e as práticas recomendadas para que os desenvolvedores de jogos trabalhem com eficiência com o recurso de segurança UAC (controle de conta de usuário) introduzido no Windows Vista.

-   [Visão geral do controle de conta de usuário](#overview-of-user-account-control)
-   [Contas de usuário no Windows Vista](#user-accounts-in-windows-vista)
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

O UAC (controle de conta de usuário), introduzido no Windows Vista, é um recurso de segurança criado para ajudar a impedir que invasores mal-intencionados usem pontos fracos ou bugs encontrados em aplicativos amplamente usados para alterar o sistema operacional ou outros programas instalados. Isso é feito pela execução da grande maioria dos programas e processos como usuário padrão (também conhecido como usuário limitado, usuário restrito ou Least-Privileged usuário), mesmo que a conta do usuário atual tenha credenciais administrativas. Um processo com privilégios de usuário padrão tem muitas restrições inerentes que o impedem de fazer alterações em todo o sistema.

O UAC também é responsável pela elevação de privilégios de um processo pelo uso de um esquema de autenticação baseado em caixa de diálogo, iniciado na execução de determinados processos designados como exigindo privilégios administrativos. A elevação de privilégio permite que os administradores executem a maioria de seus aplicativos em um nível de privilégio seguro (o mesmo que qualquer outro usuário padrão), mas também permite processos e operações que exigem privilégios administrativos. O UAC dá suporte à autenticação no ressalto para que um administrador possa conceder privilégios elevados a um programa enquanto um usuário padrão estiver conectado ao sistema no momento.

O recurso UAC é habilitado por padrão. Embora seja possível que um administrador desabilite todo o sistema do UAC, isso tem várias ramificações negativas. Primeiro, isso enfraquece a segurança de todas as contas administrativas, pois todos os processos seriam executados com credenciais administrativas, mesmo quando a maioria dos aplicativos não os exige realmente. Com o UAC desabilitado, um aplicativo de usuário padrão que expõe uma vulnerabilidade explorável na segurança pode potencialmente ser usado para roubar informações particulares, instalar rootkits ou spyware, destruir a integridade do sistema ou hospedar ataques zumbis em outros sistemas. Enquanto com o UAC habilitado, a execução da maioria do software como usuário padrão limita bastante o dano potencial desse bug. Em segundo lugar, desativar o UAC desabilita muitas das soluções alternativas para a compatibilidade de aplicativos que permitem que os usuários padrão verdadeiros executem com êxito uma ampla gama de aplicativos. Desabilitar o UAC nunca deve ser recomendado como solução alternativa de compatibilidade.

É importante observar que os aplicativos devem se esforçar para usar somente direitos de usuário padrão, se possível. Embora os administradores possam facilmente elevar os privilégios de um processo, a elevação ainda exige a interação do usuário e a confirmação sempre que um aplicativo é executado, o que exige credenciais administrativas. Essa elevação também deve ser feita no momento em que o programa é iniciado, portanto, exigir credenciais administrativas mesmo para uma única operação requer a exposição do sistema a um risco maior para todo o tempo de execução do aplicativo. Os usuários padrão sem qualquer capacidade de elevar seus privilégios também são comuns em configurações de negócios e de família. "Executar como administrador" não é uma boa solução alternativa para a compatibilidade, expõe o usuário e o sistema a um risco maior de segurança e cria frustração para os usuários em muitas situações.

> [!Note]  
> O recurso de controle de conta de usuário introduzido no Windows Vista também está presente no Windows 7. Embora a experiência do usuário que trabalha com os vários recursos do sistema tenha sido aprimorada em relação ao controle de conta de usuário, o impacto nos aplicativos é basicamente o mesmo. Todas as recomendações do Windows Vista neste artigo também se aplicam ao Windows 7. Para obter detalhes sobre as alterações da interface do usuário do UAC para o Windows 7, consulte [User interface-caixa de diálogo controle de conta de usuário](../win7appqual/user-interface---user-account-control-dialog-updates.md).

 

## <a name="user-accounts-in-windows-vista"></a>Contas de usuário no Windows Vista

O Windows Vista categoriza cada usuário em dois tipos de conta de usuário: administradores e usuários padrão.

Uma conta de usuário padrão é semelhante a uma conta de usuário limitado no Windows XP. Assim como no Windows XP, um usuário padrão não pode gravar na pasta arquivos de programas, não pode gravar \_ na \_ parte do computador local hKey do registro e não pode executar tarefas que alteram o sistema, como a instalação de um driver no modo kernel ou o acesso a espaços de processo no nível do sistema.

A conta de administrador mudou significativamente desde que o Windows XP foi lançado. Anteriormente, todos os processos iniciados por um membro do grupo Administradores receberam privilégios administrativos. Com o UAC habilitado, todos os processos são executados com privilégios de usuário padrão, a menos que seja especificamente elevado por um administrador. Essa diferença torna as contas no grupo Administradores mais seguras, reduzindo o risco de segurança apresentado por possíveis bugs na maioria dos programas.

É importante que todos os aplicativos, especialmente jogos, operem com eficiência e responsabilidade quando executados como um processo de usuário padrão. Todas as operações que exigem privilégios administrativos devem ser feitas no momento da instalação ou por programas auxiliares que solicitam credenciais administrativas explicitamente. Embora a elevação de privilégios seja bastante trivial para um membro do grupo Administradores, os usuários padrão devem adiar para alguém com credenciais administrativas para inserir fisicamente sua senha para elevar privilégios. Como as contas protegidas pelos controles dos pais devem ser usuários padrão, essa será uma situação muito comum para os jogadores que estão usando o Windows Vista.

Se o seu jogo já estiver trabalhando no Windows XP com contas de usuário limitado, a mudança para o controle de conta de usuário no Windows Vista deve ser muito fácil. A maioria desses aplicativos funcionará no estado em que se encontra, embora a adição de um manifesto de aplicativo seja altamente recomendada. (Os manifestos são descritos posteriormente neste tópico em [definindo o nível de execução no manifesto do aplicativo](#setting-the-execution-level-in-the-application-manifest).)

## <a name="file-access-as-a-standard-user"></a>Acesso a arquivos como usuário padrão

O aspecto do seu jogo mais afetado pelas restrições de usuário padrão é a organização do sistema de arquivos e a acessibilidade. Você nunca deve assumir que o jogo pode gravar arquivos na pasta onde o jogo está instalado. No Windows Vista, por exemplo, os privilégios de um usuário devem ser elevados pelo sistema operacional antes que um aplicativo possa gravar na pasta arquivos de programas. Para evitar isso, você deve categorizar os arquivos de dados do jogo por escopo e acessibilidade e usar a função [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) , juntamente com as constantes de CSIDL fornecidas pelo shell do Windows, para gerar os caminhos de arquivo apropriados. As constantes de CSIDl correspondem a pastas conhecidas no sistema de arquivos que o sistema operacional usa e promove para particionar arquivos globais e específicos do usuário.

A tentativa de criar ou gravar um arquivo ou diretório em uma pasta que não conceda permissão de gravação ao processo falhará no Windows Vista se o aplicativo não tiver privilégios administrativos. Se o seu executável de jogo de 32 bits estiver em execução no modo herdado, porque ele não declarou um nível de execução solicitado, suas operações de gravação terão sucesso, mas estarão sujeitas à virtualização, conforme descrito na seção "compatibilidade do UAC com jogos mais antigos", posteriormente neste artigo.

**Tabela 1. Pastas conhecidas**



| Nome CSIDl             | Caminho típico (Windows Vista)                                                   | Direitos de usuário padrão | Direitos de administrador | Escopo de acesso | Descrição                                                                                                                      | Exemplos                                                          |
|------------------------|--------------------------------------------------------------------------------|----------------------|----------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| pessoa CSIDl \_ pessoal        | C: \\ usuários \\ nome de usuário \\ documentos                                                | Leitura/Gravação           | Leitura/Gravação           | Per-User     | Arquivos de jogos específicos do usuário que são lidos e modificados e podem ser manipulados fora do contexto do jogo.                          | Capturas de tela. Arquivos de jogos salvos com uma associação de extensão de arquivo. |
| \_AppData local CSIDL \_  | C: \\ Users \\ User name \\ AppData \\ local                                           | Leitura/Gravação           | Leitura/Gravação           | Per-User     | Arquivos de jogos específicos do usuário que são lidos e modificados e são usados somente dentro do contexto do jogo.                                 | Arquivos de cache do jogo. Configurações do Player.                          |
| AppData comuns de CSIDl \_ \_ | C: \\ ProgramData                                                                | Ler/gravar se proprietário  | Leitura/Gravação           | Todos os Usuários    | Arquivos de jogos que podem ser criados por um usuário e lidos por todos os usuários. O acesso de gravação é concedido somente ao criador do arquivo (proprietário). | Perfis de Usuário                                                     |
| arquivos de \_ programa CSIDL \_  | C: \\ arquivos de programas<br/> ou<br/> C: \\ arquivos de programas (x86) <br/> | Somente leitura            | Leitura/Gravação           | Todos os Usuários    | Arquivos de jogos estáticos gravados pelo instalador do jogo s que são lidos por todos os usuários.                                                    | Ativos de jogos, como materiais e malhas.                        |



 

Seu jogo normalmente será instalado em uma pasta sob a pasta representada pela \_ constante arquivos de programas CSIDL \_ . No entanto, esse nem sempre é o caso. Em vez disso, você deve usar um caminho relativo do seu arquivo executável ao gerar cadeias de caracteres de caminho para arquivos ou diretórios localizados em sua pasta de instalação.

Você também deve evitar suposições embutidas em código sobre os caminhos de pasta conhecidos. Por exemplo, no Windows XP Professional 64-bit Edition e no Windows Vista x64, o caminho dos arquivos de programas é C: \\ Program Files (x86) for 32-bit Programs e C: \\ Program Files for 64-bit Programs. Esses caminhos conhecidos são alterados do Windows XP, e os usuários podem reconfigurar o local de muitas dessas pastas e até mesmo localizá-las em unidades diferentes. Portanto, sempre use as constantes de CSIDl para evitar confusão e problemas potenciais. Instalação do Windows compreende esses locais de pastas conhecidos e moverá os dados ao atualizar o sistema operacional do Windows XP; por outro lado, o uso de locais não padrão ou caminhos embutidos em código pode falhar bem após uma atualização do sistema operacional.

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

No Windows Vista, qualquer aplicativo que exija privilégios administrativos deve declarar uma solicitação de um nível de execução administrativo em seu manifesto (descrito na próxima seção, [definindo o nível de execução no manifesto do aplicativo](#setting-the-execution-level-in-the-application-manifest)).

A elevação, como é conhecida, é o procedimento controlado pelo UAC para promover um processo a um processo administrativo. Os privilégios de um processo só podem ser elevados no momento da criação. Depois de criado, um processo nunca será promovido a um nível de privilégio mais alto. Por esse motivo. as operações que exigem credenciais administrativas devem ser isoladas para instaladores separados e outros programas auxiliares.

Após a execução de um programa, o UAC inspeciona o nível de execução solicitado no manifesto e, se forem necessários privilégios elevados, solicitará ao usuário atual uma das duas caixas de diálogo padrão: uma para um usuário padrão e outra para um administrador.

Se o usuário atual for um usuário padrão, o UAC solicitará ao usuário as credenciais de um administrador antes de permitir que o programa seja executado.

**Figura 1. Solicitar que um usuário padrão insira credenciais para uma conta administrativa**

![solicitar que um usuário padrão insira credenciais para uma conta administrativa](images/uac-prompt-elevation.jpg)

Se o usuário atual for um administrador, o UAC solicitará permissão ao usuário antes de permitir que o programa seja executado.

**Figura 2. Solicitar que um administrador autorize alterações no computador**

![solicitar que um administrador autorize alterações no computador](images/uac-prompt-authorization.jpg)

O aplicativo só receberá privilégios administrativos se um usuário padrão fornecer as credenciais administrativas apropriadas ou um usuário administrativo fornecer a confirmação; qualquer outra coisa fará com que o aplicativo seja encerrado.

É importante observar que um processo com privilégios elevados é executado como o usuário administrativo que inseriu as credenciais no prompt do UAC, e não como o usuário padrão que está conectado no momento. Isso é semelhante ao **runas** no Windows XP o processo elevado Obtém a pasta do administrador e as chaves do registro ao acessar dados por usuário, e todos os programas que o processo elevado inicia também herdam os locais de conta de usuário e direitos administrativos. Para os administradores que são solicitados a confirmar (**continuar** ou **Cancelar**), esses locais corresponderão aos locais do usuário no momento. Em geral, no entanto, processos que exigem elevação não devem operar em dados por usuário. Observe que isso pode afetar substancialmente como o instalador deve funcionar! Se o instalador, em execução como administrador, gravar em HKCU ou em um perfil de usuário, talvez esteja muito bem gravando no local errado. Considere a criação desses valores por usuário na primeira execução do jogo.

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

Ao definir explicitamente requestedExecutionLevel como "asInvoker", este exemplo declara que o sistema operacional se comportará corretamente sem privilégios administrativos. Como resultado, o UAC desabilita a virtualização e executa o jogo com os mesmos privilégios que o chamador, que normalmente é de privilégios de usuário padrão, uma vez que o Windows Explorer é executado como usuário padrão.

O sistema operacional pode ser informado de que um jogo requer elevação para privilégios administrativos, substituindo "asInvoker" por "requireAdministrator", para criar a seguinte marca:

``` syntax
<ms_asmv2:requestedExecutionLevel level="requireAdministrator" uiAccess="false" />
```

Com essa configuração, o sistema operacional solicita ao usuário atual uma das caixas de diálogo de elevação padrão do UAC toda vez que o jogo é executado. É altamente recomendável que nenhum jogo exija privilégios de administrador para ser executado, pois não apenas essa caixa de diálogo se tornará apenas irritante, mas também fará com que o jogo seja incompatível com controles dos pais. Pense muito cuidadosamente antes de adicionar esse requisito a qualquer executável.

Um equívoco comum é que a adição de um manifesto que define requestedExecutionLevel como "requireAdministrator" ignora a necessidade de um prompt de elevação. Isso não é verdade. Ele simplesmente impede que o sistema operacional Adivinhe se seu aplicativo de instalação ou atualização precisa de privilégios administrativos. O usuário ainda será solicitado a autorizar a elevação.

O Windows verifica a assinatura de qualquer aplicativo marcado para elevação antes de exibir o prompt do UAC. Um executável grande que é marcado para elevação leva mais tempo para ser verificado do que um pequeno executável e mais longo do que um executável marcado como "asInvoker". Os executáveis de instalação que são de extração automática devem, portanto, ser marcados como "asInvoker" e qualquer parte que precise ser marcada como "requireAdministrator" deve ser colocada em um executável auxiliar separado.

O atributo uiAccess, mostrado nos exemplos anteriores, deve ser sempre FALSE para jogos. Esse atributo especifica se os clientes de automação da interface do usuário têm acesso à interface do usuário do sistema protegido e têm implicações de segurança especiais se estiverem definidos como TRUE.

## <a name="embedding-a-manifest-in-visual-studio"></a>Inserindo um manifesto no Visual Studio

O suporte ao manifesto foi adicionado primeiro ao Visual Studio a partir do VS2005. Por padrão, um executável criado no Visual Studio 2005 (ou mais recente) terá um manifesto gerado automaticamente inserido como parte do processo de compilação. O conteúdo do manifesto gerado automaticamente depende de determinadas configurações de projeto que você especifica na caixa de diálogo Propriedades do projeto.

O manifesto gerado automaticamente pelo Visual Studio 2005 não conterá um <trustInfo> bloco, pois não há como configurar o nível de execução do UAC nas propriedades do projeto. A maneira preferida de adicionar essas informações é permitir que o VS2005 Mescle um manifesto definido pelo usuário que contenha o <trustInfo> bloco com o manifesto gerado automaticamente. Isso é tão simples quanto adicionar um \* arquivo. manifest à sua solução que contém o XML listado na seção anterior. Quando o Visual Studio encontra um arquivo. manifest em sua solução, ele invocará automaticamente a ferramenta de manifesto (mt.exe) para mesclar os arquivos. manifest com o gerado automaticamente.

> [!Note]  
> Há um bug na ferramenta de manifesto (mt.exe) fornecido pelo Visual Studio 2005 que resulta em um manifesto mesclado e incorporado que pode causar problemas quando o executável é executado no Windows XP antes do SP3. O bug é um resultado de como a ferramenta redefine o namespace padrão na declaração do <trustInfo> bloco. Felizmente, é fácil ignorar o problema inteiramente declarando explicitamente um namespace diferente no <trustInfo> bloco e escopondo os nós filho para o novo namespace. O XML fornecido na seção anterior demonstra essa correção.

 

Uma limitação no uso da ferramenta de mt.exe incluída no Visual Studio 2005 é que ela gerará um aviso ao processar o <trustInfo> bloco, pois a ferramenta não contém um esquema atualizado para validar o XML. Para corrigir esse aviso, é recomendável substituir todos os arquivos de mt.exe no diretório de instalação do Visual Studio 2005 (há várias instâncias) com os mt.exe fornecidos na SDK do Windows mais recente.

A partir do Visual Studio 2008, agora você pode especificar um nível de execução do aplicativo de dentro da caixa de diálogo de propriedades do projeto (Figura 3) ou usando o sinalizador do vinculador/MANIFESTUAC. Definir essas opções fará com que o Visual Studio 2008 gere automaticamente e insira um manifesto com o <trustInfo> bloco apropriado no executável.

**Figura 3. Definindo o nível de execução no Visual Studio 2008**

![definindo o nível de execução no Visual Studio 2008](images/setting-execution-level-in-vs2008.jpg)

A inserção de um manifesto em versões mais antigas do Visual Studio sem suporte a manifesto ainda é possível, mas requer mais trabalho do desenvolvedor. Para obter um exemplo de como fazer isso, examine o projeto do Visual Studio 2003 incluído em qualquer amostra no SDK do DirectX antes da versão de 2008 de março.

## <a name="uac-compatibility-with-older-games"></a>Compatibilidade com o UAC com jogos mais antigos

Se seu jogo parece estar salvando e carregando um arquivo com êxito no diretório arquivos de programas, mas sem evidências do arquivo de íon do Windows Vista, qualquer aplicativo de 32 bits que não contenha um nível de execução solicitado em seu manifesto é considerado um aplicativo herdado. Antes do Windows Vista, a maioria dos aplicativos eram normalmente executados por usuários com privilégios administrativos. Como resultado, esses aplicativos podiam ler e gravar livremente arquivos do sistema e chaves do registro, e muitos desenvolvedores não fizeram as alterações necessárias para funcionar corretamente em contas de usuário limitadas no Windows XP. No entanto, no Windows Vista, esses mesmos aplicativos falhariam devido a privilégios de acesso insuficientes no novo modelo de segurança, o que impõe a execução de usuário padrão para aplicativos herdados. Para reduzir o impacto disso, a virtualização também foi adicionada ao Windows Vista. A virtualização impedirá que milhares de aplicativos herdados funcionem bem no Windows Vista sem exigir que esses aplicativos tenham privilégios elevados o tempo todo apenas para serem bem-sucedidos em algumas operações secundárias. s encontrados, é provável que seu jogo esteja sendo executado no modo herdado e esteja sujeito à virtualização.

A virtualização afeta o sistema de arquivos e o registro redirecionando gravações sensíveis ao sistema (e operações de registro ou arquivo subsequentes) para um local por usuário dentro do perfil do usuário atual. Por exemplo, se um aplicativo tentar gravar no seguinte arquivo:

<dl> C: \\ arquivos de programas \\ nome da empresa \\ título \\config.ini  
</dl>

a gravação é redirecionada automaticamente para:

<dl> C: \\ Users \\ User name \\ AppData \\ local \\ VirtualStore \\ Program files \\ nome da empresa \\ title \\config.ini  
</dl>

Da mesma forma, se um aplicativo tentar gravar um valor de registro como o seguinte:

<dl> HKEY \_ local \_ Machine \\ software \\ empresa nome \\ título  
</dl>

Ele será redirecionado em vez de:

<dl> HKEY \_ Current \_ user \\ software \\ classes \\ VirtualStore \\ Machine \\ software \\ empresa name \\ title  
</dl>

Arquivos e chaves do registro afetados pela virtualização só são acessados por operações de arquivo e registro de aplicativos virtualizados que estão sendo executados como o usuário atual.

No entanto, há muitas restrições à virtualização. Um é que os aplicativos de 64 bits nunca são executados no modo herdado para operações de compatibilidade sujeitas à virtualização em aplicativos de 32 bits falharão no 64 bit. Além disso, se um aplicativo herdado executado como um usuário padrão tentar gravar qualquer tipo de arquivo executável em um local que exija credenciais administrativas, a virtualização não ocorrerá e ocorrerá uma falha na gravação.

**Figura 4. Processo de virtualização**

![processo de virtualização](images/uac-virtualization-process.jpg)

Quando um aplicativo herdado tenta uma operação de leitura em locais sensíveis ao sistema no sistema de arquivos ou no registro, os locais virtuais são pesquisados primeiro. Se o arquivo ou a chave do registro não for encontrado, o sistema operacional acessará os locais do sistema padrão.

A virtualização será removida das versões subsequentes do Windows para que seja importante não confiar nesse recurso. Em vez disso, você deve configurar explicitamente o manifesto do aplicativo para privilégios administrativos ou de usuário padrão, pois isso desabilitará a virtualização. A virtualização também não é óbvia para os usuários finais, portanto, embora a virtualização possa permitir que seu aplicativo seja executado, ele pode gerar chamadas de suporte e dificultar o problema com esses clientes.

Observe que, se o UAC estiver desabilitado, a virtualização também será desabilitada. Se a virtualização estiver desabilitada, as contas de usuário padrão se comportarão exatamente como contas de usuário limitadas no Windows XP e os aplicativos herdados poderão não funcionar corretamente para usuários padrão que, de outra forma, teriam êxito devido à virtualização.

## <a name="legacy-scenarios-and-manifests"></a>Cenários herdados e manifestos

Para a maioria dos cenários de uso, basta marcar o. exe com os elementos de manifesto do UAC corretos e garantir que o aplicativo funcione corretamente, pois um usuário padrão é suficiente para uma excelente compatibilidade com o UAC. A maioria dos jogos estão executando o Windows Vista ou o Windows 7 com o controle de conta de usuário habilitado. Para o Windows XP e os usuários no Windows Vista ou no Windows7 com o recurso de controle de conta de usuário desabilitado, eles normalmente são executados usando contas de administrador. Embora esse seja um modo de operação menos seguro, geralmente não haverá nenhum problema de compatibilidade adicional, embora indicado acima, desabilitar o UAC desabilita a virtualização também.

Há um caso especial que vale a pena observar quando o programa é marcado como "requireAdministrator" no manifesto do UAC. No Windows XP e no Windows Vista ou no Windows 7 com o controle de conta de usuário desabilitado, os elementos do manifesto do UAC são ignorados pelo sistema. Nessa situação, os usuários com contas de administrador sempre executarão todos os programas com direitos totais de administrador e, portanto, esses programas funcionarão conforme o esperado. Os usuários restritos do Windows XP e os usuários padrão em execução no Windows Vista ou no Windows 7, no entanto, sempre executarão esses programas com direitos restritos e todas as operações de nível de administrador falharão. Portanto, é recomendável que os programas marcados como "requiretAdministrator" Chamem [**IsUserAnAdmin**](/windows/win32/api/shlobj_core/nf-shlobj_core-isuseranadmin) na inicialização e exibam uma mensagem de erro fatal se ele retornar false. Para o cenário principal acima, isso sempre terá sucesso, mas fornece uma experiência de usuário melhor e uma mensagem de erro clara para essa situação rara.

## <a name="conclusion"></a>Conclusão

Como um desenvolvedor de jogos destinado ao ambiente de vários usuários do Windows, é imperativo que você projete seu jogo para operar com eficiência e responsabilidade. O arquivo executável principal do seu jogo não deve depender de privilégios administrativos. Isso não apenas impede a aparência de prompts para elevação sempre que o jogo é executado, o que pode afetar negativamente a experiência geral do usuário, mas também permite que seu jogo Aproveite outros recursos que exigem execução com privilégios de usuário padrão, como controles dos pais.

Os aplicativos projetados corretamente para operar como com as credenciais de um usuário padrão (ou usuário limitado) em versões anteriores do Windows não serão afetados pelo UAC que serão executados sem elevação. No entanto, eles devem incluir um manifesto com o nível de execução solicitado definido como "asInvoker" para estar em conformidade com os padrões de aplicativo para o vista.

## <a name="further-reading"></a>Leitura Adicional

Para obter ajuda com a criação de aplicativos para o Windows Vista que são compatíveis com o controle de conta de usuário, baixe os seguintes white paper: [requisitos de desenvolvimento de aplicativos do Windows Vista para compatibilidade de controle de conta de usuário](/previous-versions/dotnet/articles/bb530410(v=msdn.10)).

Este white paper fornece etapas detalhadas sobre o processo de design, juntamente com exemplos de código, requisitos e práticas recomendadas. Este documento também detalha as atualizações técnicas e as alterações na experiência do usuário no Windows Vista.

Para obter mais informações sobre o controle de conta de usuário, visite [Windows Vista: controle de conta de usuário](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) no [Microsoft TechNet](https://www.microsoft.com/technet/).

Outro recurso útil é o artigo [ensinar seus aplicativos a brincar perfeitamente com o controle de conta de usuário do Windows Vista](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control), da [msdn Magazine](/archive/msdn-magazine/msdn-magazine-issues), de janeiro de 2007. Este artigo aborda problemas gerais de compatibilidade de aplicativos, bem como as vantagens e problemas de usar pacotes de Windows Installer no Windows Vista.

Para obter mais informações sobre o bug e a correção para mt.exe, a ferramenta usada pelo Visual Studio 2005 para mesclar e inserir automaticamente um manifesto em um executável, consulte [explorando manifestos parte 2: namespaces padrão e manifestos do UAC no Windows Vista](https://techcommunity.microsoft.com/t5/Windows-Blog-Archive/bg-p/Windows-Blog-Archive/2006/09/08/exploring-manifests-part-2-default-namespaces-and-uac-manifests-in-windows-vista/) no blog de Chris Jackson no [msdn](/archive/blogs/).

 

