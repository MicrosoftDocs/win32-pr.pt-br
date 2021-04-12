---
title: Jogos com Least-Privileged contas de usuário
description: Este artigo descreve como os desenvolvedores de jogos podem criar jogos do Microsoft Windows que funcionam bem com contas de usuário com privilégios mínimos (também conhecidos como contas de usuário limitado).
ms.assetid: 1b7cc3c9-b180-14b1-53c8-57f9e545d009
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4c44d94345462fc02ec649c5674ed88c38c12ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454203"
---
# <a name="gaming-with-least-privileged-user-accounts"></a><span data-ttu-id="86dc2-103">Jogos com Least-Privileged contas de usuário</span><span class="sxs-lookup"><span data-stu-id="86dc2-103">Gaming with Least-Privileged User Accounts</span></span>

<span data-ttu-id="86dc2-104">Este artigo descreve como os desenvolvedores de jogos podem criar jogos do Microsoft Windows que funcionam bem com contas de usuário com privilégios mínimos (também conhecidos como contas de usuário limitado).</span><span class="sxs-lookup"><span data-stu-id="86dc2-104">This article describes how games developers can author Microsoft Windows games that work well with least-privileged user accounts (also known as limited-user accounts).</span></span>

-   [<span data-ttu-id="86dc2-105">Introdução</span><span class="sxs-lookup"><span data-stu-id="86dc2-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="86dc2-106">Acesso a arquivos para contas de usuário Least-Privileged</span><span class="sxs-lookup"><span data-stu-id="86dc2-106">File Access for Least-Privileged User Accounts</span></span>](#file-access-for-least-privileged-user-accounts)
    -   [<span data-ttu-id="86dc2-107">Cenário 1: arquivos que não precisam ser exibidos ou alterados por usuários</span><span class="sxs-lookup"><span data-stu-id="86dc2-107">Scenario 1: Files that do not need to be viewed or altered by users</span></span>](#scenario-1-files-that-do-not-need-to-be-viewed-or-altered-by-users)
    -   [<span data-ttu-id="86dc2-108">Cenário 2: arquivos que precisam ser exibidos ou alterados por usuários</span><span class="sxs-lookup"><span data-stu-id="86dc2-108">Scenario 2: Files that need to be viewed or altered by users</span></span>](#scenario-2-files-that-need-to-be-viewed-or-altered-by-users)
-   [<span data-ttu-id="86dc2-109">Acesso ao registro para contas de usuário Least-Privileged</span><span class="sxs-lookup"><span data-stu-id="86dc2-109">Registry Access for Least-Privileged User Accounts</span></span>](#registry-access-for-least-privileged-user-accounts)
-   [<span data-ttu-id="86dc2-110">Aplicação de patch com contas de usuário Least-Privileged</span><span class="sxs-lookup"><span data-stu-id="86dc2-110">Patching with Least-Privileged User Accounts</span></span>](#patching-with-least-privileged-user-accounts)

## <a name="introduction"></a><span data-ttu-id="86dc2-111">Introdução</span><span class="sxs-lookup"><span data-stu-id="86dc2-111">Introduction</span></span>

<span data-ttu-id="86dc2-112">O Windows gerencia seus usuários com contas.</span><span class="sxs-lookup"><span data-stu-id="86dc2-112">Windows manages its users with accounts.</span></span> <span data-ttu-id="86dc2-113">Hoje, mais de 80% dos usuários de computador em casa compartilham seus computadores com outros membros da família.</span><span class="sxs-lookup"><span data-stu-id="86dc2-113">Today, more than eighty percent of computer users at home share their computer with other family members.</span></span> <span data-ttu-id="86dc2-114">Quando vários usuários compartilham um computador Windows, várias contas de usuário são criadas e cada usuário faz logon com uma conta individual para acessar o computador.</span><span class="sxs-lookup"><span data-stu-id="86dc2-114">When multiple users share a Windows computer, multiple user accounts are created, and each user logs in with an individual account to access the computer.</span></span> <span data-ttu-id="86dc2-115">Com o aumento da conscientização da segurança, mais pessoas operam seus computadores com contas de usuário com privilégios mínimos, também conhecidas como contas de usuário limitado, que não têm controle total sobre o sistema.</span><span class="sxs-lookup"><span data-stu-id="86dc2-115">With the increasing awareness for security, more people operate their computers with least-privileged user accounts, also known as limited-user accounts, which do not have complete control over the system.</span></span> <span data-ttu-id="86dc2-116">As contas de administrador normalmente têm acesso irrestrito a todas as partes do computador.</span><span class="sxs-lookup"><span data-stu-id="86dc2-116">Administrator accounts typically have unrestricted access to every part of the computer.</span></span> <span data-ttu-id="86dc2-117">Isso pode afetar a forma como os jogos baseados em Windows funcionam.</span><span class="sxs-lookup"><span data-stu-id="86dc2-117">This can affect how Windows-based games work.</span></span>

<span data-ttu-id="86dc2-118">Há benefícios adicionais para os desenvolvedores de jogos que escrevem seus jogos para trabalhar com contas de usuário com privilégios mínimos.</span><span class="sxs-lookup"><span data-stu-id="86dc2-118">There are additional benefits for games developers who write their games to work with least-privileged user accounts.</span></span> <span data-ttu-id="86dc2-119">No Windows Vista e versões posteriores, as contas de usuário com privilégios mínimos são impostas, o que significa que cada conta no sistema, com exceção do administrador local, é uma conta de usuário com privilégios mínimos.</span><span class="sxs-lookup"><span data-stu-id="86dc2-119">In Windows Vista and later, least-privileged user accounts are enforced, which means that every account on the system, with the exception of the local administrator, is a least-privileged user account.</span></span> <span data-ttu-id="86dc2-120">Isso afetará a forma como os jogos que não seguem a diretriz (aplicativos herdados) são executados no Windows Vista e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="86dc2-120">This will affect how games that do not follow the guideline (legacy applications) run on Windows Vista and later.</span></span> <span data-ttu-id="86dc2-121">Por exemplo, quando um aplicativo tenta gravar em uma pasta ou um valor de registro ao qual ele não tem permissão, a gravação de arquivo é redirecionada para um repositório de arquivos virtual para o usuário.</span><span class="sxs-lookup"><span data-stu-id="86dc2-121">For instance, when an application attempts to write to a folder or a registry value to which it does not have permission, the file write is redirected to a virtual file store for the user.</span></span> <span data-ttu-id="86dc2-122">Esse repositório de arquivos virtual residirá em uma pasta para a qual o usuário tem acesso de gravação.</span><span class="sxs-lookup"><span data-stu-id="86dc2-122">This virtual file store will reside in a folder to which the user has write access.</span></span> <span data-ttu-id="86dc2-123">Esse comportamento pode não parecer tão catastrófico quanto a falha na tentativa de gravação; no entanto, os aplicativos que criam arquivos virtualizados podem confundir os usuários porque os arquivos não serão gravados no local esperado pelos usuários.</span><span class="sxs-lookup"><span data-stu-id="86dc2-123">This behavior may not seem as catastrophic as outright failing the write attempt; however, applications that create virtualized files may confuse users because files will not be written to the location users expect.</span></span> <span data-ttu-id="86dc2-124">Por exemplo, os jogos que gravam arquivos de pontuação alta na mesma pasta que a pasta executável gravarão esses arquivos em uma pasta virtualizada em vez disso.</span><span class="sxs-lookup"><span data-stu-id="86dc2-124">For instance, games that write high score files to the same folder as the executable folder will write these files to a virtualized folder instead.</span></span> <span data-ttu-id="86dc2-125">Consequentemente, um usuário não pode ver a pontuação alta obtida por outro usuário porque cada usuário tem um repositório de arquivos virtualizado separado.</span><span class="sxs-lookup"><span data-stu-id="86dc2-125">Consequently, one user cannot see the high score achieved by another user because every user has a separate virtualized file store.</span></span>

<span data-ttu-id="86dc2-126">Os jogos que seguem as diretrizes neste artigo serão executados com contas de usuário com privilégios mínimos e, consequentemente, manterão a compatibilidade com o Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="86dc2-126">Games that follow the guidelines in this article will run with least-privileged user accounts, and consequently will maintain compatibility with Windows Vista and later.</span></span>

## <a name="file-access-for-least-privileged-user-accounts"></a><span data-ttu-id="86dc2-127">Acesso a arquivos para contas de usuário Least-Privileged</span><span class="sxs-lookup"><span data-stu-id="86dc2-127">File Access for Least-Privileged User Accounts</span></span>

<span data-ttu-id="86dc2-128">O Windows dá suporte a dois sistemas de arquivos: FAT32 e NTFS.</span><span class="sxs-lookup"><span data-stu-id="86dc2-128">Windows supports two file systems: FAT32 and NTFS.</span></span> <span data-ttu-id="86dc2-129">O FAT32 é um sistema de arquivos herdado com suporte apenas para compatibilidade com versões anteriores; O NTFS dá suporte a permissões de arquivo mais poderosas e robustas.</span><span class="sxs-lookup"><span data-stu-id="86dc2-129">FAT32 is a legacy file system supported only for backward compatibility; NTFS supports more powerful and robust file permissions.</span></span> <span data-ttu-id="86dc2-130">O uso do NTFS está se expandindo à medida que os varejistas estão enviando novos computadores com o Windows pré-instalado em um disco rígido com particionamento NTFS.</span><span class="sxs-lookup"><span data-stu-id="86dc2-130">The use of NTFS is expanding as retailers are shipping new computers with Windows pre-installed on a NTFS-partitioned hard drive.</span></span> <span data-ttu-id="86dc2-131">Em um sistema Windows XP baseado em NTFS, os usuários com contas de usuário com privilégios mínimos têm acesso limitado a várias pastas.</span><span class="sxs-lookup"><span data-stu-id="86dc2-131">On an NTFS-based Windows XP system, users with least-privileged user accounts have only limited access to several folders.</span></span> <span data-ttu-id="86dc2-132">No entanto, eles teriam acesso completo em um sistema Windows XP baseado em FAT32.</span><span class="sxs-lookup"><span data-stu-id="86dc2-132">However, they would have complete access on a FAT32-based Windows XP system.</span></span>

<span data-ttu-id="86dc2-133">A tabela a seguir lista o local padrão dessas pastas e suas permissões.</span><span class="sxs-lookup"><span data-stu-id="86dc2-133">The following table lists the default location of these folders and their permissions.</span></span>



| <span data-ttu-id="86dc2-134">Caminho</span><span class="sxs-lookup"><span data-stu-id="86dc2-134">Path</span></span>                                               | <span data-ttu-id="86dc2-135">Conteúdo da pasta</span><span class="sxs-lookup"><span data-stu-id="86dc2-135">Folder Contents</span></span>              | <span data-ttu-id="86dc2-136">Ler</span><span class="sxs-lookup"><span data-stu-id="86dc2-136">Read</span></span> | <span data-ttu-id="86dc2-137">Gravar</span><span class="sxs-lookup"><span data-stu-id="86dc2-137">Write</span></span> | <span data-ttu-id="86dc2-138">Criar, excluir</span><span class="sxs-lookup"><span data-stu-id="86dc2-138">Create/Delete</span></span> |
|----------------------------------------------------|------------------------------|------|-------|---------------|
| <span data-ttu-id="86dc2-139"><Drive>: \\ Windows</span><span class="sxs-lookup"><span data-stu-id="86dc2-139"><Drive>:\\Windows</span></span>                            | <span data-ttu-id="86dc2-140">O sistema operacional Windows</span><span class="sxs-lookup"><span data-stu-id="86dc2-140">The Windows operating system</span></span> | <span data-ttu-id="86dc2-141">X</span><span class="sxs-lookup"><span data-stu-id="86dc2-141">X</span></span>    |       |               |
| <span data-ttu-id="86dc2-142"><Drive>: \\ Arquivos de programas</span><span class="sxs-lookup"><span data-stu-id="86dc2-142"><Drive>:\\Program Files</span></span>                      | <span data-ttu-id="86dc2-143">Arquivos de aplicativo executáveis</span><span class="sxs-lookup"><span data-stu-id="86dc2-143">Executable application files</span></span> | <span data-ttu-id="86dc2-144">X</span><span class="sxs-lookup"><span data-stu-id="86dc2-144">X</span></span>    |       |               |
| <span data-ttu-id="86dc2-145"><Drive>: \\ Nome de usuário de documentos e configurações \\\*</span><span class="sxs-lookup"><span data-stu-id="86dc2-145"><Drive>:\\Documents and Settings\\Username\*</span></span> | <span data-ttu-id="86dc2-146">Arquivos de cada usuário</span><span class="sxs-lookup"><span data-stu-id="86dc2-146">Each user's files</span></span>            | <span data-ttu-id="86dc2-147">X</span><span class="sxs-lookup"><span data-stu-id="86dc2-147">X</span></span>    | <span data-ttu-id="86dc2-148">X</span><span class="sxs-lookup"><span data-stu-id="86dc2-148">X</span></span>     | <span data-ttu-id="86dc2-149">X</span><span class="sxs-lookup"><span data-stu-id="86dc2-149">X</span></span>             |
| <span data-ttu-id="86dc2-150"><Drive>: \\ Documenta e configurações \\ todos os usuários</span><span class="sxs-lookup"><span data-stu-id="86dc2-150"><Drive>:\\Documents and Settings\\All Users</span></span>  | <span data-ttu-id="86dc2-151">Todos os arquivos de usuário</span><span class="sxs-lookup"><span data-stu-id="86dc2-151">All user files</span></span>               | <span data-ttu-id="86dc2-152">X</span><span class="sxs-lookup"><span data-stu-id="86dc2-152">X</span></span>    | <span data-ttu-id="86dc2-153">X</span><span class="sxs-lookup"><span data-stu-id="86dc2-153">X</span></span>     | <span data-ttu-id="86dc2-154">X</span><span class="sxs-lookup"><span data-stu-id="86dc2-154">X</span></span>             |



 

<span data-ttu-id="86dc2-155">\* Username é o nome de logon do usuário.</span><span class="sxs-lookup"><span data-stu-id="86dc2-155">\* Username is the user's login name.</span></span>

<span data-ttu-id="86dc2-156">Em uma conta de usuário com privilégios mínimos, você pode ler, gravar, criar e excluir arquivos em qualquer pasta: Documents and Settings \\ nome de usuário ou documentos e configurações \\ todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="86dc2-156">In a least-privileged user account, you may read, write, create and delete files in either folder: Documents and Settings\\Username or Documents and Settings\\All Users.</span></span>

<span data-ttu-id="86dc2-157">Isso significa que você não deve fazer o salvamento de jogos em \\ arquivos de programas, em vez disso, eles devem entrar em uma subpasta em \\ meus documentos.</span><span class="sxs-lookup"><span data-stu-id="86dc2-157">What this means is that you should not place save games in \\Program Files, instead they should go in a sub-folder in \\My Documents.</span></span> <span data-ttu-id="86dc2-158">Além disso, você não deve colocar dados de aplicativos temporários em \\ arquivos de programas ou em \\ meus documentos, em vez disso, eles devem ser colocados na pasta de dados de aplicativos (CSIDL \_ local de \_ AppData).</span><span class="sxs-lookup"><span data-stu-id="86dc2-158">Also you should not place temporary application data in \\Program Files or \\My Documents, instead it should be placed in Application Data folder (CSIDL\_LOCAL\_APPDATA).</span></span>

<span data-ttu-id="86dc2-159">Mais especificamente, há dois cenários que cada jogo deve tratar:</span><span class="sxs-lookup"><span data-stu-id="86dc2-159">More specifically, there are two scenarios that each game should handle:</span></span>

### <a name="scenario-1-files-that-do-not-need-to-be-viewed-or-altered-by-users"></a><span data-ttu-id="86dc2-160">Cenário 1: arquivos que não precisam ser exibidos ou alterados por usuários</span><span class="sxs-lookup"><span data-stu-id="86dc2-160">Scenario 1: Files that do not need to be viewed or altered by users</span></span>

<span data-ttu-id="86dc2-161">Um exemplo típico seria o arquivo de configuração do jogo, arquivos temporários e arquivos de cache de jogos.</span><span class="sxs-lookup"><span data-stu-id="86dc2-161">A typical example would be the game's configuration file, temporary files, and game cache files.</span></span> <span data-ttu-id="86dc2-162">Esses arquivos normalmente são mantidos na pasta dados do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="86dc2-162">These files are typically kept in the Application Data folder.</span></span> <span data-ttu-id="86dc2-163">Para obter esse caminho de pasta, chame a função [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) com CSIDL \_ AppData ou CSIDL \_ local \_ AppData, conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="86dc2-163">To obtain this folder path, call the [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) function with CSIDL\_APPDATA or CSIDL\_LOCAL\_APPDATA as shown in the following code example.</span></span>

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

<span data-ttu-id="86dc2-164">A diferença entre as pastas de dados de aplicativos locais e móveis é que, no Windows 2000 e no Windows XP, o conteúdo de roaming é copiado de e para o servidor durante o processo de logon/logoff, enquanto o conteúdo local não é.</span><span class="sxs-lookup"><span data-stu-id="86dc2-164">The difference between local and roaming Application Data folders is that on Windows 2000 and Windows XP, roaming content is copied to and from the server during the logon/logoff process, while local content is not.</span></span> <span data-ttu-id="86dc2-165">Para a maioria dos jogos, os dados do aplicativo local são suficientes.</span><span class="sxs-lookup"><span data-stu-id="86dc2-165">For most games, local Application Data is sufficient.</span></span>

### <a name="scenario-2-files-that-need-to-be-viewed-or-altered-by-users"></a><span data-ttu-id="86dc2-166">Cenário 2: arquivos que precisam ser exibidos ou alterados por usuários</span><span class="sxs-lookup"><span data-stu-id="86dc2-166">Scenario 2: Files that need to be viewed or altered by users</span></span>

<span data-ttu-id="86dc2-167">Um exemplo típico seria os arquivos de jogos salvos de um usuário.</span><span class="sxs-lookup"><span data-stu-id="86dc2-167">A typical example would be a user's saved game files.</span></span> <span data-ttu-id="86dc2-168">Armazene os arquivos na pasta de documentos do usuário para que eles sejam facilmente visíveis ao usuário.</span><span class="sxs-lookup"><span data-stu-id="86dc2-168">Store the files in the user's document folder so that they are easily visible to the user.</span></span> <span data-ttu-id="86dc2-169">Um aplicativo obtém o caminho da pasta de documento do usuário chamando [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) com CSIDL \_ pessoal, como mostra o exemplo de código a seguir:</span><span class="sxs-lookup"><span data-stu-id="86dc2-169">An application gets the user's document folder path by calling [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) with CSIDL\_PERSONAL, as the following code example shows:</span></span>

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

<span data-ttu-id="86dc2-170">Às vezes, um jogo pode precisar armazenar arquivos que todos os usuários devem ver e usar.</span><span class="sxs-lookup"><span data-stu-id="86dc2-170">At times, a game may need to store files that all users are meant to see and use.</span></span> <span data-ttu-id="86dc2-171">Um exemplo é o recorde de pontuação, onde todos os usuários gravam no mesmo arquivo de registro para que as pontuações altas sejam mantidas em todo o sistema, em vez de uma pontuação alta separada para cada usuário.</span><span class="sxs-lookup"><span data-stu-id="86dc2-171">One example is the high score record, where all users write to the same record file so that high scores are maintained system-wide instead of a separate high score for each user.</span></span> <span data-ttu-id="86dc2-172">Outros exemplos são mapas, missões e modificações de jogos baixados.</span><span class="sxs-lookup"><span data-stu-id="86dc2-172">Other examples are downloaded maps, missions, and game modifications.</span></span> <span data-ttu-id="86dc2-173">Se eles forem compartilhados, somente um usuário precisará baixá-los em vez de todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="86dc2-173">If these are shared, then only one user has to download them instead of every user.</span></span> <span data-ttu-id="86dc2-174">Nesse cenário, use a pasta de documentos na pasta de perfil compartilhado, conforme demonstrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="86dc2-174">In this scenario, use the document folder under the shared profile folder, as demonstrated in the following code.</span></span>

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

## <a name="registry-access-for-least-privileged-user-accounts"></a><span data-ttu-id="86dc2-175">Acesso ao registro para contas de usuário Least-Privileged</span><span class="sxs-lookup"><span data-stu-id="86dc2-175">Registry Access for Least-Privileged User Accounts</span></span>

<span data-ttu-id="86dc2-176">É comum que os aplicativos usem o registro do Windows para armazenar informações.</span><span class="sxs-lookup"><span data-stu-id="86dc2-176">It is common for applications to use the Windows registry to store information.</span></span> <span data-ttu-id="86dc2-177">Semelhante ao acesso a arquivos, o administrador e as contas de usuário com privilégios mínimos não têm a mesma permissão para o registro.</span><span class="sxs-lookup"><span data-stu-id="86dc2-177">Similar to file access, administrator and least-privileged user accounts do not have the same permission to the registry.</span></span> <span data-ttu-id="86dc2-178">Para contas de usuário com privilégios mínimos, o \_ nó de máquina local hKey inteiro \_ é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="86dc2-178">For least-privileged user accounts, the entire HKEY\_LOCAL\_MACHINE node is read-only.</span></span> <span data-ttu-id="86dc2-179">Por exemplo, um jogo pode ler as informações de configuração padrão, mas não pode gravar nenhuma nova informação nesse nó.</span><span class="sxs-lookup"><span data-stu-id="86dc2-179">For instance, a game can read the default configuration information, but may not write any new information to this node.</span></span> <span data-ttu-id="86dc2-180">Consequentemente, os jogos em execução no modo de usuário com privilégios mínimos que precisam gravar no registro precisarão usar \_ o \_ nó HKEY Current User para armazenar informações por usuário, conforme ilustrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="86dc2-180">Consequently, games running in least-privileged user mode that need to write to the registry will need to use the HKEY\_CURRENT\_USER node to store per-user information, as illustrated in the following code.</span></span>

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

<span data-ttu-id="86dc2-181">Vale a pena observar que durante a instalação, as informações do registro devem ser gravadas em HKEY \_ \_ computador local, não como hKey \_ Current \_ User.</span><span class="sxs-lookup"><span data-stu-id="86dc2-181">It is worth noting that during installation, registry information should be written to HKEY\_LOCAL\_MACHINE, not HKEY\_CURRENT\_USER.</span></span> <span data-ttu-id="86dc2-182">Isso ocorre porque a pessoa que está executando a instalação normalmente é um administrador e pode não ser a única pessoa a usar o programa.</span><span class="sxs-lookup"><span data-stu-id="86dc2-182">This is because the person running the installation is usually an administrator, and may not be the only person to use the program.</span></span> <span data-ttu-id="86dc2-183">Nessa situação, gravar em HKEY \_ Current \_ User torna as informações indisponíveis para outros usuários.</span><span class="sxs-lookup"><span data-stu-id="86dc2-183">In this situation, writing to HKEY\_CURRENT\_USER makes the information unavailable to other users.</span></span> <span data-ttu-id="86dc2-184">Isso geralmente não é um problema porque as informações gravadas no registro durante a instalação são as configurações padrão e de configuração que se aplicam a todos os usuários do programa.</span><span class="sxs-lookup"><span data-stu-id="86dc2-184">This is not usually an issue because the information written to the registry during installation is the configuration and default settings that apply to every user of the program.</span></span>

<span data-ttu-id="86dc2-185">Ao desinstalar o jogo, é necessário um esforço extra para remover cada valor que o jogo gravou no registro.</span><span class="sxs-lookup"><span data-stu-id="86dc2-185">When uninstalling the game, extra effort is necessary to remove every value that the game has written to the registry.</span></span> <span data-ttu-id="86dc2-186">Como o desinstalador é executado por uma pessoa, geralmente o administrador, simplesmente excluindo as informações relevantes em HKEY \_ local \_ Machine e hKey \_ Current \_ User não removerá valores para outros usuários.</span><span class="sxs-lookup"><span data-stu-id="86dc2-186">Because the uninstaller is run by one person, usually the administrator, simply deleting the relevant information in HKEY\_LOCAL\_MACHINE and HKEY\_CURRENT\_USER will not remove values for other users.</span></span> <span data-ttu-id="86dc2-187">Uma maneira de remover as informações por usuário no registro é enumerar a \_ raiz do hive do registro de usuários HKEY.</span><span class="sxs-lookup"><span data-stu-id="86dc2-187">One way to remove the per-user information in the registry is to enumerate the HKEY\_USERS registry hive root.</span></span> <span data-ttu-id="86dc2-188">Cada subchave em \_ usuários de hKey corresponde ao \_ hive do usuário atual do hKey \_ para um usuário específico no sistema.</span><span class="sxs-lookup"><span data-stu-id="86dc2-188">Each subkey under HKEY\_USERS corresponds to the HKEY\_CURRENT\_USER hive for a particular user on the system.</span></span> <span data-ttu-id="86dc2-189">Ao enumerar \_ os usuários de hKey e remover as informações específicas do jogo em cada subchave, o desinstalador pode garantir que nenhuma informação seja deixada para trás.</span><span class="sxs-lookup"><span data-stu-id="86dc2-189">By enumerating HKEY\_USERS and removing the game-specific information under each subkey, the uninstaller can ensure that no information is left behind.</span></span>

## <a name="patching-with-least-privileged-user-accounts"></a><span data-ttu-id="86dc2-190">Aplicação de patch com contas de usuário Least-Privileged</span><span class="sxs-lookup"><span data-stu-id="86dc2-190">Patching with Least-Privileged User Accounts</span></span>

<span data-ttu-id="86dc2-191">A aplicação de patches em um jogo envolve a atualização dos arquivos do jogo.</span><span class="sxs-lookup"><span data-stu-id="86dc2-191">Patching a game involves updating the game's files.</span></span> <span data-ttu-id="86dc2-192">Portanto, ele geralmente requer acesso de gravação à pasta do programa do jogo.</span><span class="sxs-lookup"><span data-stu-id="86dc2-192">Therefore, it usually requires write access to the game's program folder.</span></span> <span data-ttu-id="86dc2-193">Aplicar patches em um jogo é um processo simples quando é feito por um administrador, pois eles têm acesso irrestrito à pasta do programa do jogo.</span><span class="sxs-lookup"><span data-stu-id="86dc2-193">Patching a game is a straightforward process when it is done by an administrator because they have unrestricted access to the game's program folder.</span></span> <span data-ttu-id="86dc2-194">Por outro lado, tradicionalmente era difícil, se não impossível, para que um usuário com privilégios mínimos corrija os jogos devido à restrição de acesso.</span><span class="sxs-lookup"><span data-stu-id="86dc2-194">Conversely, it has traditionally been difficult, if not impossible, for a least privileged user to patch games because of the access restriction.</span></span> <span data-ttu-id="86dc2-195">Agora, a [Windows Installer](/windows/desktop/Msi/windows-installer-portal) foi aprimorada para tornar possível a aplicação de patch de conta de usuário com privilégios mínimos.</span><span class="sxs-lookup"><span data-stu-id="86dc2-195">Now, [Windows Installer](/windows/desktop/Msi/windows-installer-portal) has been enhanced to make least-privileged user account patching possible.</span></span> <span data-ttu-id="86dc2-196">Para aproveitar esse recurso, os jogos são incentivados a utilizar Windows Installer para instalação e aplicação de patches.</span><span class="sxs-lookup"><span data-stu-id="86dc2-196">To take advantage of this feature, games are encouraged to utilize Windows Installer for installation and patching.</span></span>

<span data-ttu-id="86dc2-197">A partir do Windows Installer 3,0, os patches de aplicativos podem ser aplicados por usuários menos privilegiados quando determinadas condições são atendidas.</span><span class="sxs-lookup"><span data-stu-id="86dc2-197">Starting with Windows Installer 3.0, application patches can be applied by least privileged users when certain conditions are met.</span></span> <span data-ttu-id="86dc2-198">Essas condições são:</span><span class="sxs-lookup"><span data-stu-id="86dc2-198">These conditions are:</span></span>

-   <span data-ttu-id="86dc2-199">O aplicativo foi instalado usando Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="86dc2-199">The application was installed using Windows Installer 3.0.</span></span>
-   <span data-ttu-id="86dc2-200">O aplicativo foi originalmente instalado por computador.</span><span class="sxs-lookup"><span data-stu-id="86dc2-200">The application was originally installed per-machine.</span></span>
-   <span data-ttu-id="86dc2-201">O aplicativo é instalado a partir de mídia removível, como um CD-ROM ou DVD (disco de vídeo digital).</span><span class="sxs-lookup"><span data-stu-id="86dc2-201">The application is installed from removable media, such a CD-ROM or digital video disc (DVD).</span></span>
-   <span data-ttu-id="86dc2-202">Os patches são assinados digitalmente por um certificado que é identificado pelo pacote do instalador original (arquivo. msi).</span><span class="sxs-lookup"><span data-stu-id="86dc2-202">The patches are digitally signed by a certificate that is identified by the original installer package (.msi file).</span></span>
-   <span data-ttu-id="86dc2-203">Os patches podem ser validados em relação à assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="86dc2-203">The patches can be validated against the digital signature.</span></span>
-   <span data-ttu-id="86dc2-204">O pacote do instalador original não desabilitou a aplicação de patch de conta de usuário com privilégios mínimos.</span><span class="sxs-lookup"><span data-stu-id="86dc2-204">The original installer package has not disabled least-privileged user account patching.</span></span>
-   <span data-ttu-id="86dc2-205">O administrador do sistema não desabilitou a aplicação de patch de conta de usuário com privilégios mínimos por meio da política do sistema.</span><span class="sxs-lookup"><span data-stu-id="86dc2-205">The system administrator has not disabled least-privileged user account patching via system policy.</span></span>

<span data-ttu-id="86dc2-206">Normalmente, um usuário com privilégios mínimos não pode modificar os arquivos de programa de um jogo.</span><span class="sxs-lookup"><span data-stu-id="86dc2-206">Normally, a least privileged user cannot modify a game's program files.</span></span> <span data-ttu-id="86dc2-207">No entanto, quando as condições acima são atendidas e a aplicação de patches de LUA está habilitada, Windows Installer pode atualizar os arquivos do jogo para que o usuário obtenha a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="86dc2-207">However, when the above conditions are met and LUA patching is enabled, Windows Installer can update the game's files so that the user gets the latest version.</span></span>

> [!Note]  
> <span data-ttu-id="86dc2-208">As informações contidas neste artigo estão relacionadas ao produto de pré-lançamento software, que pode ser substancialmente modificado antes de sua primeira versão comercial.</span><span class="sxs-lookup"><span data-stu-id="86dc2-208">The information contained in this article relates to pre-release software product, which may be substantially modified before its first commercial release.</span></span> <span data-ttu-id="86dc2-209">De acordo, as informações podem não descrever ou refletir com precisão o produto de software quando o primeiro é lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="86dc2-209">Accordingly, the information may not accurately describe or reflect the software product when first commercially released.</span></span> <span data-ttu-id="86dc2-210">Este artigo é fornecido apenas para fins informativos e a Microsoft não oferece nenhuma garantia, expressa ou implícita, em relação a este artigo ou às informações contidas nele.</span><span class="sxs-lookup"><span data-stu-id="86dc2-210">This article is provided for informational purposes only, and Microsoft makes no warranties, express or implied, with respect to this article or the information contained in it.</span></span>

 

 

 