---
title: Jogos com Least-Privileged contas de usuário
description: este artigo descreve como os desenvolvedores de jogos podem criar jogos do Microsoft Windows que funcionam bem com contas de usuário com privilégios mínimos (também conhecidos como contas de usuário limitado).
ms.assetid: 1b7cc3c9-b180-14b1-53c8-57f9e545d009
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 939d22b1d8bf381e98c5b6a7222be29b565c3d9e1f0758788aff94b0915b1807
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119340736"
---
# <a name="gaming-with-least-privileged-user-accounts"></a>Jogos com Least-Privileged contas de usuário

este artigo descreve como os desenvolvedores de jogos podem criar jogos do Microsoft Windows que funcionam bem com contas de usuário com privilégios mínimos (também conhecidos como contas de usuário limitado).

-   [Introdução](#introduction)
-   [Acesso a arquivos para contas de usuário Least-Privileged](#file-access-for-least-privileged-user-accounts)
    -   [Cenário 1: arquivos que não precisam ser exibidos ou alterados por usuários](#scenario-1-files-that-do-not-need-to-be-viewed-or-altered-by-users)
    -   [Cenário 2: arquivos que precisam ser exibidos ou alterados por usuários](#scenario-2-files-that-need-to-be-viewed-or-altered-by-users)
-   [Acesso ao registro para contas de usuário Least-Privileged](#registry-access-for-least-privileged-user-accounts)
-   [Aplicação de patch com contas de usuário Least-Privileged](#patching-with-least-privileged-user-accounts)

## <a name="introduction"></a>Introdução

Windows gerencia seus usuários com contas. Hoje, mais de 80% dos usuários de computador em casa compartilham seus computadores com outros membros da família. quando vários usuários compartilham um computador Windows, várias contas de usuário são criadas e cada usuário faz logon com uma conta individual para acessar o computador. Com o aumento da conscientização da segurança, mais pessoas operam seus computadores com contas de usuário com privilégios mínimos, também conhecidas como contas de usuário limitado, que não têm controle total sobre o sistema. As contas de administrador normalmente têm acesso irrestrito a todas as partes do computador. isso pode afetar o funcionamento dos jogos baseados em Windows.

Há benefícios adicionais para os desenvolvedores de jogos que escrevem seus jogos para trabalhar com contas de usuário com privilégios mínimos. no Windows Vista e versões posteriores, as contas de usuário com privilégios mínimos são impostas, o que significa que cada conta no sistema, com exceção do administrador local, é uma conta de usuário com privilégios mínimos. isso afetará a forma como os jogos que não seguem a diretriz (aplicativos herdados) são executados no Windows Vista e versões posteriores. Por exemplo, quando um aplicativo tenta gravar em uma pasta ou um valor de registro ao qual ele não tem permissão, a gravação de arquivo é redirecionada para um repositório de arquivos virtual para o usuário. Esse repositório de arquivos virtual residirá em uma pasta para a qual o usuário tem acesso de gravação. Esse comportamento pode não parecer tão catastrófico quanto a falha na tentativa de gravação; no entanto, os aplicativos que criam arquivos virtualizados podem confundir os usuários porque os arquivos não serão gravados no local esperado pelos usuários. Por exemplo, os jogos que gravam arquivos de pontuação alta na mesma pasta que a pasta executável gravarão esses arquivos em uma pasta virtualizada em vez disso. Consequentemente, um usuário não pode ver a pontuação alta obtida por outro usuário porque cada usuário tem um repositório de arquivos virtualizado separado.

os jogos que seguem as diretrizes neste artigo serão executados com contas de usuário com privilégios mínimos e, consequentemente, manterão a compatibilidade com o Windows Vista e posterior.

## <a name="file-access-for-least-privileged-user-accounts"></a>Acesso a arquivos para contas de usuário Least-Privileged

o Windows dá suporte a dois sistemas de arquivos: FAT32 e NTFS. O FAT32 é um sistema de arquivos herdado com suporte apenas para compatibilidade com versões anteriores; O NTFS dá suporte a permissões de arquivo mais poderosas e robustas. o uso do NTFS está se expandindo à medida que os varejistas estão enviando novos computadores com Windows pré-instalado em um disco rígido com partição NTFS. em um sistema Windows XP baseado em NTFS, os usuários com contas de usuário com privilégios mínimos têm acesso limitado a várias pastas. no entanto, eles teriam acesso completo em um sistema Windows XP baseado em FAT32.

A tabela a seguir lista o local padrão dessas pastas e suas permissões.



| Caminho                                               | Conteúdo da pasta              | Ler | Gravar | Criar, excluir |
|----------------------------------------------------|------------------------------|------|-------|---------------|
| <Drive>: \\ Windows                            | o sistema operacional Windows | X    |       |               |
| <Drive>: \\ Arquivos de programas                      | Arquivos de aplicativo executáveis | X    |       |               |
| <Drive>: \\ documentos e Configurações \\ nome de usuário\* | Arquivos de cada usuário            | X    | X     | X             |
| <Drive>: \\ documentos e Configurações \\ todos os usuários  | Todos os arquivos de usuário               | X    | X     | X             |



 

\* Username é o nome de logon do usuário.

em uma conta de usuário com privilégios mínimos, você pode ler, gravar, criar e excluir arquivos em qualquer pasta: documentos e Configurações \\ nome de usuário ou documentos e Configurações \\ todos os usuários.

Isso significa que você não deve fazer o salvamento de jogos em \\ arquivos de programas, em vez disso, eles devem entrar em uma subpasta em \\ meus documentos. Além disso, você não deve colocar dados de aplicativos temporários em \\ arquivos de programas ou em \\ meus documentos, em vez disso, eles devem ser colocados na pasta de dados de aplicativos (CSIDL \_ local de \_ AppData).

Mais especificamente, há dois cenários que cada jogo deve tratar:

### <a name="scenario-1-files-that-do-not-need-to-be-viewed-or-altered-by-users"></a>Cenário 1: arquivos que não precisam ser exibidos ou alterados por usuários

Um exemplo típico seria o arquivo de configuração do jogo, arquivos temporários e arquivos de cache de jogos. Esses arquivos normalmente são mantidos na pasta dados do aplicativo. Para obter esse caminho de pasta, chame a função [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) com CSIDL \_ AppData ou CSIDL \_ local \_ AppData, conforme mostrado no exemplo de código a seguir.

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

a diferença entre as pastas de dados de aplicativos locais e móveis é que, no Windows 2000 e no Windows XP, o conteúdo de roaming é copiado para e do servidor durante o processo de logon/logoff, enquanto o conteúdo local não é. Para a maioria dos jogos, os dados do aplicativo local são suficientes.

### <a name="scenario-2-files-that-need-to-be-viewed-or-altered-by-users"></a>Cenário 2: arquivos que precisam ser exibidos ou alterados por usuários

Um exemplo típico seria os arquivos de jogos salvos de um usuário. Armazene os arquivos na pasta de documentos do usuário para que eles sejam facilmente visíveis ao usuário. Um aplicativo obtém o caminho da pasta de documento do usuário chamando [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) com CSIDL \_ pessoal, como mostra o exemplo de código a seguir:

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

Às vezes, um jogo pode precisar armazenar arquivos que todos os usuários devem ver e usar. Um exemplo é o recorde de pontuação, onde todos os usuários gravam no mesmo arquivo de registro para que as pontuações altas sejam mantidas em todo o sistema, em vez de uma pontuação alta separada para cada usuário. Outros exemplos são mapas, missões e modificações de jogos baixados. Se eles forem compartilhados, somente um usuário precisará baixá-los em vez de todos os usuários. Nesse cenário, use a pasta de documentos na pasta de perfil compartilhado, conforme demonstrado no código a seguir.

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

## <a name="registry-access-for-least-privileged-user-accounts"></a>Acesso ao registro para contas de usuário Least-Privileged

é comum que os aplicativos usem o registro de Windows para armazenar informações. Semelhante ao acesso a arquivos, o administrador e as contas de usuário com privilégios mínimos não têm a mesma permissão para o registro. Para contas de usuário com privilégios mínimos, o \_ nó de máquina local hKey inteiro \_ é somente leitura. Por exemplo, um jogo pode ler as informações de configuração padrão, mas não pode gravar nenhuma nova informação nesse nó. Consequentemente, os jogos em execução no modo de usuário com privilégios mínimos que precisam gravar no registro precisarão usar \_ o \_ nó HKEY Current User para armazenar informações por usuário, conforme ilustrado no código a seguir.

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

Vale a pena observar que durante a instalação, as informações do registro devem ser gravadas em HKEY \_ \_ computador local, não como hKey \_ Current \_ User. Isso ocorre porque a pessoa que está executando a instalação normalmente é um administrador e pode não ser a única pessoa a usar o programa. Nessa situação, gravar em HKEY \_ Current \_ User torna as informações indisponíveis para outros usuários. Isso geralmente não é um problema porque as informações gravadas no registro durante a instalação são as configurações padrão e de configuração que se aplicam a todos os usuários do programa.

Ao desinstalar o jogo, é necessário um esforço extra para remover cada valor que o jogo gravou no registro. Como o desinstalador é executado por uma pessoa, geralmente o administrador, simplesmente excluindo as informações relevantes em HKEY \_ local \_ Machine e hKey \_ Current \_ User não removerá valores para outros usuários. Uma maneira de remover as informações por usuário no registro é enumerar a \_ raiz do hive do registro de usuários HKEY. Cada subchave em \_ usuários de hKey corresponde ao \_ hive do usuário atual do hKey \_ para um usuário específico no sistema. Ao enumerar \_ os usuários de hKey e remover as informações específicas do jogo em cada subchave, o desinstalador pode garantir que nenhuma informação seja deixada para trás.

## <a name="patching-with-least-privileged-user-accounts"></a>Aplicação de patch com contas de usuário Least-Privileged

A aplicação de patches em um jogo envolve a atualização dos arquivos do jogo. Portanto, ele geralmente requer acesso de gravação à pasta do programa do jogo. Aplicar patches em um jogo é um processo simples quando é feito por um administrador, pois eles têm acesso irrestrito à pasta do programa do jogo. Por outro lado, tradicionalmente era difícil, se não impossível, para que um usuário com privilégios mínimos corrija os jogos devido à restrição de acesso. agora, a [Windows Installer](/windows/desktop/Msi/windows-installer-portal) foi aprimorada para tornar possível a aplicação de patch de conta de usuário com privilégios mínimos. para aproveitar esse recurso, os jogos são incentivados a utilizar Windows Installer para instalação e aplicação de patches.

a partir do Windows Installer 3,0, os patches de aplicativos podem ser aplicados por usuários menos privilegiados quando determinadas condições são atendidas. Essas condições são:

-   o aplicativo foi instalado usando Windows Installer 3,0.
-   O aplicativo foi originalmente instalado por computador.
-   O aplicativo é instalado por meio de mídia removível, como um CD-ROM ou DVD (disco de vídeo digital).
-   Os patches são assinados digitalmente por um certificado identificado pelo pacote do instalador original (.msi arquivo).
-   Os patches podem ser validados em relação à assinatura digital.
-   O pacote do instalador original não desabilitou a adoção de patch de conta de usuário com privilégios mínimos.
-   O administrador do sistema não desabilitou a adoção de patch de conta de usuário com privilégios mínimos por meio da política do sistema.

Normalmente, um usuário menos privilegiado não pode modificar os arquivos de programa de um jogo. No entanto, quando as condições acima são atendidas e a adoção de patch LUA está habilitada, Windows Instalador pode atualizar os arquivos do jogo para que o usuário obtém a versão mais recente.

> [!Note]  
> As informações contidas neste artigo estão relacionadas ao produto de software de pré-lançamento, que pode ser substancialmente modificado antes de sua primeira versão comercial. Da mesma forma, as informações podem não descrever ou refletir com precisão o produto de software quando lançados comercialmente pela primeira vez. Este artigo é fornecido apenas para fins informacionais e a Microsoft não faz nenhuma garantia, expressa ou implícita, em relação a este artigo ou às informações contidas nele.

 

 

 