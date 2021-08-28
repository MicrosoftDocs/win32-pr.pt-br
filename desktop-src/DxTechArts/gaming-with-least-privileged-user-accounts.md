---
title: Jogos com contas Least-Privileged usuário
description: Este artigo descreve como os desenvolvedores de jogos podem Windows jogos da Microsoft que funcionam bem com contas de usuário com privilégios mínimos (também conhecidas como contas de usuário limitado).
ms.assetid: 1b7cc3c9-b180-14b1-53c8-57f9e545d009
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db15302eb856aaeb05c68fae4746110dd42cb4a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887389"
---
# <a name="gaming-with-least-privileged-user-accounts"></a>Jogos com contas Least-Privileged usuário

Este artigo descreve como os desenvolvedores de jogos podem Windows jogos da Microsoft que funcionam bem com contas de usuário com privilégios mínimos (também conhecidas como contas de usuário limitado).

-   [Introdução](#introduction)
-   [Acesso a arquivos para Least-Privileged de usuário](#file-access-for-least-privileged-user-accounts)
    -   [Cenário 1: arquivos que não precisam ser exibidos ou alterados pelos usuários](#scenario-1-files-that-do-not-need-to-be-viewed-or-altered-by-users)
    -   [Cenário 2: arquivos que precisam ser exibidos ou alterados pelos usuários](#scenario-2-files-that-need-to-be-viewed-or-altered-by-users)
-   [Acesso ao Registro para Least-Privileged de Usuário](#registry-access-for-least-privileged-user-accounts)
-   [A patch com contas Least-Privileged usuário](#patching-with-least-privileged-user-accounts)

## <a name="introduction"></a>Introdução

Windows gerencia seus usuários com contas. Atualmente, mais do que percentual percentual de usuários de computador em casa compartilham seu computador com outros membros da família. Quando vários usuários compartilham um Windows, várias contas de usuário são criadas e cada usuário faz login com uma conta individual para acessar o computador. Com o aumento do reconhecimento de segurança, mais pessoas operam seus computadores com contas de usuário com privilégios mínimos, também conhecidas como contas de usuário limitadas, que não têm controle total sobre o sistema. As contas de administrador normalmente têm acesso irrestrito a todas as partes do computador. Isso pode afetar como Windows jogos baseados em dados funcionam.

Há benefícios adicionais para desenvolvedores de jogos que escrevem seus jogos para trabalhar com contas de usuário com privilégios mínimos. No Windows Vista e posterior, as contas de usuário com privilégios mínimos são impostas, o que significa que cada conta no sistema, com exceção do administrador local, é uma conta de usuário com privilégios mínimos. Isso afetará como os jogos que não seguem as diretrizes (aplicativos herdáveis) são executados no Windows Vista e posterior. Por exemplo, quando um aplicativo tenta gravar em uma pasta ou um valor do Registro para o qual ele não tem permissão, a gravação de arquivo é redirecionada para um armazenamento de arquivos virtual para o usuário. Esse armazenamento de arquivos virtuais residiria em uma pasta à qual o usuário tem acesso de gravação. Esse comportamento pode não parecer tão catastrófico quanto falhar com a tentativa de gravação; No entanto, os aplicativos que criam arquivos virtualizados podem confundir os usuários porque os arquivos não serão gravados no local esperado pelos usuários. Por exemplo, os jogos que escrevem arquivos de pontuação alta na mesma pasta que a pasta executável gravarão esses arquivos em uma pasta virtualizada. Consequentemente, um usuário não pode ver a pontuação alta alcançada por outro usuário porque cada usuário tem um armazenamento de arquivos virtualizado separado.

Os jogos que seguem as diretrizes neste artigo serão executados com contas de usuário com privilégios mínimos e, consequentemente, manterão a compatibilidade com o Windows Vista e posterior.

## <a name="file-access-for-least-privileged-user-accounts"></a>Acesso a arquivos para Least-Privileged de usuário

Windows dá suporte a dois sistemas de arquivos: FAT32 e NTFS. FAT32 é um sistema de arquivos herdado com suporte apenas para compatibilidade com backward; O NTFS dá suporte a permissões de arquivo mais poderosas e robustas. O uso do NTFS está se expandindo à medida que os varejistas estão enviando novos computadores com Windows pré-instalados em um disco rígido particionado por NTFS. Em um sistema XP baseado em NTF Windows S, os usuários com contas de usuário com privilégios mínimos têm acesso limitado apenas a várias pastas. No entanto, eles teriam acesso completo em um sistema XP baseado em FAT32 Windows XP.

A tabela a seguir lista o local padrão dessas pastas e suas permissões.



| Caminho                                               | Conteúdo da pasta              | Ler | Gravar | Criar, excluir |
|----------------------------------------------------|------------------------------|------|-------|---------------|
| &lt;Unidade &gt; : \\ Windows                            | O Windows operacional | X    |       |               |
| &lt;Unidade &gt; : Arquivos de \\ Programas                      | Arquivos de aplicativo executáveis | X    |       |               |
| &lt;Unidade: &gt; documentos e nome de usuário Configurações \\ \\ usuário\* | Arquivos de cada usuário            | X    | X     | X             |
| &lt;Unidade: &gt; documentos e Configurações todos os \\ \\ usuários  | Todos os arquivos de usuário               | X    | X     | X             |



 

\* Nome de usuário é o nome de logon do usuário.

Em uma conta de usuário com privilégios mínimos, você pode ler, gravar, criar e excluir arquivos em uma das pastas: Documentos e Configurações Nome de usuário ou Documentos e Configurações Todos os \\ \\ Usuários.

Isso significa que você não deve colocar os jogos de salvar em Arquivos de Programas, em vez disso, eles devem entrar em uma \\ sub pasta no \\ Meus Documentos. Além disso, você não deve colocar dados temporários do aplicativo em Arquivos de Programas ou Meus Documentos, em vez disso, eles devem ser colocados na pasta Dados do Aplicativo \\ \\ (CSIDL \_ LOCAL \_ APPDATA).

Mais especificamente, há dois cenários que cada jogo deve lidar:

### <a name="scenario-1-files-that-do-not-need-to-be-viewed-or-altered-by-users"></a>Cenário 1: arquivos que não precisam ser exibidos ou alterados pelos usuários

Um exemplo típico seria o arquivo de configuração do jogo, arquivos temporários e arquivos de cache do jogo. Esses arquivos normalmente são mantidos na pasta Dados do Aplicativo. Para obter esse caminho de pasta, chame a função [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) com CSIDL APPDATA ou \_ CSIDL LOCAL APPDATA, conforme mostrado no \_ exemplo de código a \_ seguir.

``` syntax
#include <shlobj.h>
#include <strsafe.h>

#define APPNAME L"MyApp"

WCHAR wszPath[MAX_PATH];

// Local Application Data
SHGetFolderPath( hWnd, CSIDL_LOCAL_APPDATA, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
// Roaming Application Data
SHGetFolderPath( hWnd, CSIDL_APPDATA, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
```

A diferença entre as pastas locais e roaming de Dados do Aplicativo é que, no Windows 2000 e no Windows XP, o conteúdo em roaming é copiado de e para o servidor durante o processo de logon/logoff, enquanto o conteúdo local não é. Para a maioria dos jogos, os Dados do Aplicativo local são suficientes.

### <a name="scenario-2-files-that-need-to-be-viewed-or-altered-by-users"></a>Cenário 2: arquivos que precisam ser exibidos ou alterados pelos usuários

Um exemplo típico seria os arquivos de jogo salvos de um usuário. Armazene os arquivos na pasta de documentos do usuário para que eles sejam facilmente visíveis para o usuário. Um aplicativo obtém o caminho da pasta de documentos do usuário chamando [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) com CSIDL \_ PERSONAL, como mostra o exemplo de código a seguir:

``` syntax
#include <shlobj.h>
#include <strsafe.h>

#define APPNAME L"MyApp"

WCHAR wszPath[MAX_PATH];

SHGetFolderPath( hWnd, CSIDL_PERSONAL, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
```

Às vezes, um jogo pode precisar armazenar arquivos que todos os usuários devem ver e usar. Um exemplo é o registro de pontuação alta, em que todos os usuários gravam no mesmo arquivo de registro para que as pontuações altas sejam mantidas em todo o sistema, em vez de uma pontuação alta separada para cada usuário. Outros exemplos são mapas, missões e modificações de jogos baixados. Se eles são compartilhados, somente um usuário precisa baixá-los em vez de cada usuário. Nesse cenário, use a pasta do documento na pasta de perfil compartilhado, conforme demonstrado no código a seguir.

``` syntax
#include <shlobj.h>
#include <strsafe.h>

#define APPNAME L"MyApp"

WCHAR wszPath[MAX_PATH];

SHGetFolderPath( hWnd, CSIDL_COMMON_DOCUMENTS, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
```

## <a name="registry-access-for-least-privileged-user-accounts"></a>Acesso ao Registro para Least-Privileged de Usuário

É comum que os aplicativos usem o registro Windows para armazenar informações. Semelhante ao acesso a arquivos, as contas de usuário com privilégios mínimos e administrador não têm a mesma permissão para o Registro. Para contas de usuário com privilégios mínimos, todo o nó HKEY \_ LOCAL MACHINE é somente \_ leitura. Por exemplo, um jogo pode ler as informações de configuração padrão, mas pode não gravar nenhuma nova informação nesse nó. Consequentemente, os jogos em execução no modo de usuário com privilégios mínimos que precisam ser escritos no Registro precisarão usar o nó HKEY CURRENT USER para armazenar informações por usuário, conforme ilustrado no código \_ \_ a seguir.

``` syntax
#define APP_REGISTRY_KEY_PATH L"Software\\MyCompany\\MyApp"

LONG lRetVal;
HKEY hKey;

lRetVal = RegCreateKeyExW( HKEY_CURRENT_USER,
                           APP_REGISTRY_KEY_PATH,
                           0,
                           NULL,
                           REG_OPTION_NON_VOLATILE,
                           KEY_WRITE|KEY_READ,
                           NULL,
                           &hKey,
                           NULL );

if( ERROR_SUCCESS == lRetVal )
{
    // Store information in hKey
}
```

Vale a pena notar que, durante a instalação, as informações do Registro devem ser escritas em HKEY LOCAL MACHINE, não \_ \_ em HKEY CURRENT \_ \_ USER. Isso ocorre porque a pessoa que executa a instalação geralmente é um administrador e pode não ser a única pessoa a usar o programa. Nessa situação, a escrita no USUÁRIO ATUAL do HKEY \_ \_ torna as informações indisponíveis para outros usuários. Isso geralmente não é um problema porque as informações escritas no Registro durante a instalação são as configurações e as configurações padrão que se aplicam a todos os usuários do programa.

Ao desinstalar o jogo, é necessário um esforço extra para remover todos os valores que o jogo escreveu no Registro. Como o desinstalador é executado por uma pessoa, geralmente o administrador, simplesmente excluir as informações relevantes em HKEY LOCAL MACHINE e HKEY CURRENT USER não removerá valores para \_ \_ outros \_ \_ usuários. Uma maneira de remover as informações por usuário no Registro é enumerar a raiz do hive do registro HKEY \_ USERS. Cada sub-chave em USUÁRIOS HKEY \_ corresponde ao hive do USUÁRIO ATUAL do HKEY para um usuário específico no \_ \_ sistema. Ao enumerar USUÁRIOS do HKEY e remover as informações específicas do jogo em cada sub-chave, o desinstalador pode garantir que nenhuma informação \_ seja deixada para trás.

## <a name="patching-with-least-privileged-user-accounts"></a>A patch com contas Least-Privileged usuário

A a patch de um jogo envolve a atualização dos arquivos do jogo. Portanto, geralmente requer acesso de gravação à pasta do programa do jogo. A a patch de um jogo é um processo simples quando é feito por um administrador porque ele tem acesso irrestrito à pasta do programa do jogo. Por outro lado, tradicionalmente tem sido difícil, se não impossível, para um usuário menos privilegiado corrigir jogos devido à restrição de acesso. Agora, [Windows Instalador foi](/windows/desktop/Msi/windows-installer-portal) aprimorado para tornar possível a adoção de patch de conta de usuário com privilégios mínimos. Para aproveitar esse recurso, os jogos são incentivados a utilizar Windows Instalador para instalação e a patch.

A partir do Windows 3.0, os patches de aplicativo podem ser aplicados por usuários com privilégios mínimos quando determinadas condições são atendidas. Essas condições são:

-   O aplicativo foi instalado usando o Windows 3.0.
-   O aplicativo foi originalmente instalado por computador.
-   O aplicativo é instalado a partir de mídia removível, como um CD-ROM ou DVD (disco de vídeo digital).
-   Os patches são assinados digitalmente por um certificado que é identificado pelo pacote do instalador original (arquivo de .msi).
-   Os patches podem ser validados em relação à assinatura digital.
-   O pacote do instalador original não desabilitou a aplicação de patch de conta de usuário com privilégios mínimos.
-   O administrador do sistema não desabilitou a aplicação de patch de conta de usuário com privilégios mínimos por meio da política do sistema.

Normalmente, um usuário com privilégios mínimos não pode modificar os arquivos de programa de um jogo. no entanto, quando as condições acima são atendidas e a aplicação de patches de LUA está habilitada, Windows Installer pode atualizar os arquivos do jogo para que o usuário obtenha a versão mais recente.

> [!Note]  
> As informações contidas neste artigo estão relacionadas ao produto de pré-lançamento software, que pode ser substancialmente modificado antes de sua primeira versão comercial. De acordo, as informações podem não descrever ou refletir com precisão o produto de software quando o primeiro é lançado comercialmente. Este artigo é fornecido apenas para fins informativos e a Microsoft não oferece nenhuma garantia, expressa ou implícita, em relação a este artigo ou às informações contidas nele.

 

 

 
