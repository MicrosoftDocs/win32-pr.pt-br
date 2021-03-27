---
description: Este tópico discute como os aplicativos podem expor informações sobre eles próprios necessários para habilitar determinados cenários.
ms.assetid: F88AA3E6-6F7B-442d-935A-7D2CB4958E6B
title: registro de Aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 857e96893d2fe717f1a4939d06c77af043ead318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920758"
---
# <a name="application-registration"></a><span data-ttu-id="541c9-103">registro de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="541c9-103">Application Registration</span></span>

<span data-ttu-id="541c9-104">Este tópico discute como os aplicativos podem expor informações sobre eles próprios necessários para habilitar determinados cenários.</span><span class="sxs-lookup"><span data-stu-id="541c9-104">This topic discusses how applications can expose information about themselves necessary to enable certain scenarios.</span></span> <span data-ttu-id="541c9-105">Isso inclui as informações necessárias para localizar o aplicativo, os verbos aos quais o aplicativo dá suporte e os tipos de arquivos que um aplicativo pode manipular.</span><span class="sxs-lookup"><span data-stu-id="541c9-105">This includes information needed to locate the application, the verbs that the application supports and the types of files that an application can handle.</span></span>

<span data-ttu-id="541c9-106">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="541c9-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="541c9-107">Encontrando um executável de aplicativo</span><span class="sxs-lookup"><span data-stu-id="541c9-107">Finding an Application Executable</span></span>](#finding-an-application-executable)
-   [<span data-ttu-id="541c9-108">Registrando aplicativos</span><span class="sxs-lookup"><span data-stu-id="541c9-108">Registering Applications</span></span>](#registering-applications)
    -   [<span data-ttu-id="541c9-109">Usando a subchave de caminhos do aplicativo</span><span class="sxs-lookup"><span data-stu-id="541c9-109">Using the App Paths Subkey</span></span>](#using-the-app-paths-subkey)
    -   [<span data-ttu-id="541c9-110">Usando a subchave Applications</span><span class="sxs-lookup"><span data-stu-id="541c9-110">Using the Applications Subkey</span></span>](#using-the-applications-subkey)
-   [<span data-ttu-id="541c9-111">Registrando verbos e outras informações de associação de arquivo</span><span class="sxs-lookup"><span data-stu-id="541c9-111">Registering Verbs and Other File Association Information</span></span>](#registering-verbs-and-other-file-association-information)
-   [<span data-ttu-id="541c9-112">Registrando um tipo percebido</span><span class="sxs-lookup"><span data-stu-id="541c9-112">Registering a Perceived Type</span></span>](#registering-a-perceived-type)
-   [<span data-ttu-id="541c9-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="541c9-113">Related topics</span></span>](#related-topics)

> [!Note]  
> <span data-ttu-id="541c9-114">Os aplicativos também podem ser registrados nos aplicativos definir o acesso do programa e padrões do computador (SPAD) e definir os programas padrão (SYDP) do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="541c9-114">Applications can also be registered in the Set Program Access and Computer Defaults (SPAD) and Set Your Default Programs (SYDP) control panel applications.</span></span> <span data-ttu-id="541c9-115">Para obter informações sobre o registro de aplicativo SPAD e SYDP, consulte [diretrizes para associações de arquivo e programas padrão](appguide-fa-defpro.md)e [definir o acesso do programa e padrões do computador (SPAD)](cpl-setprogramaccess.md).</span><span class="sxs-lookup"><span data-stu-id="541c9-115">For information about SPAD and SYDP application registration, see [Guidelines for File Associations and Default Programs](appguide-fa-defpro.md), and [Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md).</span></span>

 

## <a name="finding-an-application-executable"></a><span data-ttu-id="541c9-116">Encontrando um executável de aplicativo</span><span class="sxs-lookup"><span data-stu-id="541c9-116">Finding an Application Executable</span></span>

<span data-ttu-id="541c9-117">Quando a função [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) é chamada com o nome de um arquivo executável em seu parâmetro *lpFile* , há vários locais em que a função procura o arquivo.</span><span class="sxs-lookup"><span data-stu-id="541c9-117">When the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) function is called with the name of an executable file in its *lpFile* parameter, there are several places where the function looks for the file.</span></span> <span data-ttu-id="541c9-118">É recomendável registrar seu aplicativo na subchave do registro de **caminhos do aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="541c9-118">We recommend registering your application in the **App Paths** registry subkey.</span></span> <span data-ttu-id="541c9-119">Isso evita a necessidade de aplicativos para modificar a variável de ambiente do caminho do sistema.</span><span class="sxs-lookup"><span data-stu-id="541c9-119">Doing so avoids the need for applications to modify the system PATH environment variable.</span></span>

<span data-ttu-id="541c9-120">O arquivo é procurado nos seguintes locais:</span><span class="sxs-lookup"><span data-stu-id="541c9-120">The file is sought in the following locations:</span></span>

-   <span data-ttu-id="541c9-121">O diretório de trabalho atual.</span><span class="sxs-lookup"><span data-stu-id="541c9-121">The current working directory.</span></span>
-   <span data-ttu-id="541c9-122">Somente o diretório do **Windows** (nenhum subdiretório é pesquisado).</span><span class="sxs-lookup"><span data-stu-id="541c9-122">The **Windows** directory only (no subdirectories are searched).</span></span>
-   <span data-ttu-id="541c9-123">O diretório **Windows \\ System32** .</span><span class="sxs-lookup"><span data-stu-id="541c9-123">The **Windows\\System32** directory.</span></span>
-   <span data-ttu-id="541c9-124">Diretórios listados na variável de ambiente PATH.</span><span class="sxs-lookup"><span data-stu-id="541c9-124">Directories listed in the PATH environment variable.</span></span>
-   <span data-ttu-id="541c9-125">Recomendado: **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **app Paths**</span><span class="sxs-lookup"><span data-stu-id="541c9-125">Recommended: **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**App Paths**</span></span>

## <a name="registering-applications"></a><span data-ttu-id="541c9-126">Registrando aplicativos</span><span class="sxs-lookup"><span data-stu-id="541c9-126">Registering Applications</span></span>

<span data-ttu-id="541c9-127">As subchaves de registro de **aplicativos** e **caminhos de aplicativo** são usadas para registrar e controlar o comportamento do sistema em nome dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="541c9-127">Both the **App Paths** and **Applications** registry subkeys are used to register and control the behavior of the system on behalf of applications.</span></span> <span data-ttu-id="541c9-128">A subchave de **caminhos do aplicativo** é o local preferencial.</span><span class="sxs-lookup"><span data-stu-id="541c9-128">The **App Paths** subkey is the preferred location.</span></span>

### <a name="using-the-app-paths-subkey"></a><span data-ttu-id="541c9-129">Usando a subchave de caminhos do aplicativo</span><span class="sxs-lookup"><span data-stu-id="541c9-129">Using the App Paths Subkey</span></span>

<span data-ttu-id="541c9-130">No Windows 7 e posterior, é altamente recomendável que você instale aplicativos por usuário, em vez de por computador.</span><span class="sxs-lookup"><span data-stu-id="541c9-130">In Windows 7 and later, we strongly recommend you install applications per user rather than per machine.</span></span> <span data-ttu-id="541c9-131">Um aplicativo que é instalado para por usuário pode ser registrado em **HKEY \_ Current \_ User** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **app Paths**.</span><span class="sxs-lookup"><span data-stu-id="541c9-131">An application that is installed for per user can be registered under **HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**App Paths**.</span></span> <span data-ttu-id="541c9-132">Um aplicativo que é instalado para todos os usuários do computador pode ser registrado em **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **app Paths**.</span><span class="sxs-lookup"><span data-stu-id="541c9-132">An application that is installed for all users of the computer can be registered under **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**App Paths**.</span></span>

<span data-ttu-id="541c9-133">As entradas encontradas em **caminhos de aplicativo** são usadas principalmente para as seguintes finalidades:</span><span class="sxs-lookup"><span data-stu-id="541c9-133">The entries found under **App Paths** are used primarily for the following purposes:</span></span>

-   <span data-ttu-id="541c9-134">Para mapear o nome do arquivo executável de um aplicativo para o caminho totalmente qualificado desse arquivo.</span><span class="sxs-lookup"><span data-stu-id="541c9-134">To map an application's executable file name to that file's fully qualified path.</span></span>
-   <span data-ttu-id="541c9-135">Para obter informações autônomas para a variável de ambiente PATH em uma base por aplicativo, por processo.</span><span class="sxs-lookup"><span data-stu-id="541c9-135">To pre-pend information to the PATH environment variable on a per-application, per-process basis.</span></span>

<span data-ttu-id="541c9-136">Se o nome de uma subchave dos **caminhos do aplicativo** corresponder ao nome do arquivo, o Shell executará duas ações:</span><span class="sxs-lookup"><span data-stu-id="541c9-136">If the name of a subkey of **App Paths** matches the file name, the Shell performs two actions:</span></span>

-   <span data-ttu-id="541c9-137">A entrada (padrão) é usada como o caminho totalmente qualificado do arquivo.</span><span class="sxs-lookup"><span data-stu-id="541c9-137">The (Default) entry is used as the file's fully qualified path.</span></span>
-   <span data-ttu-id="541c9-138">A entrada de caminho para essa subchave é precedente à variável de ambiente PATH do processo.</span><span class="sxs-lookup"><span data-stu-id="541c9-138">The Path entry for that subkey is pre-pended to the PATH environment variable of that process.</span></span> <span data-ttu-id="541c9-139">Se isso não for necessário, o valor do caminho poderá ser omitido.</span><span class="sxs-lookup"><span data-stu-id="541c9-139">If this is not required, the Path value can be omitted.</span></span>

<span data-ttu-id="541c9-140">Os possíveis problemas a serem considerados incluem:</span><span class="sxs-lookup"><span data-stu-id="541c9-140">Potential issues to be aware of include:</span></span>

-   <span data-ttu-id="541c9-141">O Shell limita o comprimento de uma linha de comando para o \_ caminho máximo \* 2 caracteres.</span><span class="sxs-lookup"><span data-stu-id="541c9-141">The Shell limits the length of a command line to MAX\_PATH \* 2 characters.</span></span> <span data-ttu-id="541c9-142">Se houver muitos arquivos listados como entradas de registro ou seus caminhos forem longos, os nomes de arquivo mais tarde na lista poderão ser perdidos à medida que a linha de comando estiver truncada.</span><span class="sxs-lookup"><span data-stu-id="541c9-142">If there are many files listed as registry entries or their paths are long, file names later in the list could be lost as the command line is truncated.</span></span>
-   <span data-ttu-id="541c9-143">Alguns aplicativos não aceitam vários nomes de arquivo em uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="541c9-143">Some applications do not accept multiple file names in a command line.</span></span>
-   <span data-ttu-id="541c9-144">Alguns aplicativos que aceitam vários nomes de arquivo não reconhecem o formato no qual o Shell os fornece.</span><span class="sxs-lookup"><span data-stu-id="541c9-144">Some applications that accept multiple file names do not recognize the format in which the Shell provides them.</span></span> <span data-ttu-id="541c9-145">O Shell fornece a lista de parâmetros como uma cadeia de caracteres entre aspas, mas alguns aplicativos podem exigir cadeias sem aspas.</span><span class="sxs-lookup"><span data-stu-id="541c9-145">The Shell provides the parameter list as a quoted string, but some applications might require strings without quotes.</span></span>
-   <span data-ttu-id="541c9-146">Nem todos os itens que podem ser arrastados fazem parte do sistema de arquivos; por exemplo, impressoras.</span><span class="sxs-lookup"><span data-stu-id="541c9-146">Not all items that can be dragged are part of the file system; for example, printers.</span></span> <span data-ttu-id="541c9-147">Esses itens não têm um caminho Win32 padrão, portanto, não há como fornecer um valor *lpParameters* significativo para [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="541c9-147">These items do not have a standard Win32 path, so there is no way to provide a meaningful *lpParameters* value to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

<span data-ttu-id="541c9-148">O uso da entrada DropTarget evita esses possíveis problemas fornecendo acesso a todos os formatos da área de transferência, incluindo [CFSTR \_ SHELLIDLIST](clipboard.md) (para listas de arquivos longos) e [CFSTR \_ FileContent](clipboard.md) (para objetos que não são do sistema de arquivos).</span><span class="sxs-lookup"><span data-stu-id="541c9-148">Using the DropTarget entry avoids these potential issues by providing access to all of the clipboard formats, including [CFSTR\_SHELLIDLIST](clipboard.md) (for long file lists) and [CFSTR\_FILECONTENTS](clipboard.md) (for non-file-system objects).</span></span>

<span data-ttu-id="541c9-149">**Para registrar e controlar o comportamento de seus aplicativos com a subchave de caminhos do aplicativo**:</span><span class="sxs-lookup"><span data-stu-id="541c9-149">**To register and control the behavior of your applications with the App Paths subkey**:</span></span>

1.  <span data-ttu-id="541c9-150">Adicione uma subchave com o mesmo nome do arquivo executável à subchave de **caminhos do aplicativo** , conforme mostrado na entrada do registro a seguir.</span><span class="sxs-lookup"><span data-stu-id="541c9-150">Add a subkey with the same name as your executable file to the **App Paths** subkey, as shown in the following registry entry.</span></span>

    ```
    HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   App Paths
                      file.exe
                         (Default)
                         DontUseDesktopChangeRouter
                         DropTarget
                         Path
                         UseUrl
    ```

2.  <span data-ttu-id="541c9-151">Consulte a tabela a seguir para obter detalhes das entradas de subchave de **caminhos do aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="541c9-151">See the following table for details of the **App Paths** subkey entries.</span></span> 

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="541c9-152">Entrada de registro</span><span class="sxs-lookup"><span data-stu-id="541c9-152">Registry entry</span></span></th>
    <th><span data-ttu-id="541c9-153">Detalhes</span><span class="sxs-lookup"><span data-stu-id="541c9-153">Details</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="541c9-154">(Padrão)</span><span class="sxs-lookup"><span data-stu-id="541c9-154">(Default)</span></span></td>
    <td><span data-ttu-id="541c9-155">É o caminho totalmente qualificado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="541c9-155">Is the fully qualified path to the application.</span></span> <span data-ttu-id="541c9-156">O nome do aplicativo fornecido na entrada (padrão) pode ser declarado com ou sem sua extensão. exe.</span><span class="sxs-lookup"><span data-stu-id="541c9-156">The application name provided in the (Default) entry can be stated with or without its .exe extension.</span></span> <span data-ttu-id="541c9-157">Se necessário, a função <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> adiciona a extensão ao pesquisar a subchave de <strong>caminhos do aplicativo</strong> .</span><span class="sxs-lookup"><span data-stu-id="541c9-157">If necessary, the <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> function adds the extension when searching <strong>App Paths</strong> subkey.</span></span> <span data-ttu-id="541c9-158">A entrada é do tipo de <strong>REG_SZ</strong> .</span><span class="sxs-lookup"><span data-stu-id="541c9-158">The entry is of the <strong>REG_SZ</strong> type.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="541c9-159">DontUseDesktopChangeRouter</span><span class="sxs-lookup"><span data-stu-id="541c9-159">DontUseDesktopChangeRouter</span></span></td>
    <td><span data-ttu-id="541c9-160">É obrigatório para aplicativos de depurador evitar deadlocks de diálogo de arquivo ao depurar o processo do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="541c9-160">Is mandatory for debugger applications to avoid file dialog deadlocks when debugging the Windows Explorer process.</span></span> <span data-ttu-id="541c9-161">No entanto, definir a entrada DontUseDesktopChangeRouter produz um tratamento ligeiramente menos eficiente das notificações de alteração.</span><span class="sxs-lookup"><span data-stu-id="541c9-161">Setting the DontUseDesktopChangeRouter entry produces a slightly less efficient handling of the change notifications, however.</span></span> <span data-ttu-id="541c9-162">A entrada é do tipo de <strong>REG_DWORD</strong> e o valor é 0x1.</span><span class="sxs-lookup"><span data-stu-id="541c9-162">The entry is of the <strong>REG_DWORD</strong> type and the value is 0x1.</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="541c9-163">DropTarget</span><span class="sxs-lookup"><span data-stu-id="541c9-163">DropTarget</span></span></td>
    <td><span data-ttu-id="541c9-164">É um identificador de classe (CLSID).</span><span class="sxs-lookup"><span data-stu-id="541c9-164">Is a class identifier (CLSID).</span></span> <span data-ttu-id="541c9-165">A entrada DropTarget contém o CLSID de um objeto (geralmente um servidor local em vez de um servidor em processo) que implementa <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="541c9-165">The DropTarget entry contains the CLSID of an object (usually a local server rather than an in-process server) that implements <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a>.</span></span> <span data-ttu-id="541c9-166">Por padrão, quando o destino de soltura é um arquivo executável e nenhum valor de DropTarget é fornecido, o Shell converte a lista de arquivos soltos em um parâmetro de linha de comando e passa-o para <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> por meio de <em>lpParameters</em>.</span><span class="sxs-lookup"><span data-stu-id="541c9-166">By default, when the drop target is an executable file, and no DropTarget value is provided, the Shell converts the list of dropped files into a command-line parameter and passes it to <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> through <em>lpParameters</em>.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="541c9-167">Caminho</span><span class="sxs-lookup"><span data-stu-id="541c9-167">Path</span></span></td>
    <td><span data-ttu-id="541c9-168">Fornece uma cadeia de caracteres (na forma de uma lista de diretórios separados por ponto e vírgula) para acrescentar à variável de ambiente PATH quando um aplicativo é iniciado chamando <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="541c9-168">Supplies a string (in the form of a semicolon-separated list of directories) to append to the PATH environment variable when an application is launched by calling <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>.</span></span> <span data-ttu-id="541c9-169">É o caminho totalmente qualificado para o. exe.</span><span class="sxs-lookup"><span data-stu-id="541c9-169">It is the fully qualified path to the .exe.</span></span> <span data-ttu-id="541c9-170">É de <strong>REG_SZ</strong>.</span><span class="sxs-lookup"><span data-stu-id="541c9-170">It is of <strong>REG_SZ</strong>.</span></span> <span data-ttu-id="541c9-171">No <strong>Windows 7 e posterior</strong>, o tipo pode ser <strong>REG_EXPAND_SZ</strong>e geralmente é <strong>REG_EXPAND_SZ</strong> % ProgramFiles%.</span><span class="sxs-lookup"><span data-stu-id="541c9-171">In <strong>Windows 7 and later</strong>, the type can be <strong>REG_EXPAND_SZ</strong>, and is commonly <strong>REG_EXPAND_SZ</strong> %ProgramFiles%.</span></span>
    <blockquote>
    [!Note]<br />
<span data-ttu-id="541c9-172">Além das entradas (padrão), Path e DropTarget reconhecidas pelo shell, um aplicativo também pode adicionar valores personalizados à subchave de <strong>caminhos do aplicativo</strong> do arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="541c9-172">In addition to the (Default), Path, and DropTarget entries recognized by the Shell, an application can also add custom values to its executable file's <strong>App Paths</strong> subkey.</span></span> <span data-ttu-id="541c9-173">Incentivamos os desenvolvedores de aplicativos a usar a subchave de <strong>caminhos</strong> do aplicativo para fornecer um caminho específico do aplicativo em vez de fazer adições ao caminho do sistema global.</span><span class="sxs-lookup"><span data-stu-id="541c9-173">We encourage application developers to use the <strong>App Paths</strong> subkey to provide an application-specific path instead of making additions to the global system path.</span></span>
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="541c9-174">SupportedProtocols</span><span class="sxs-lookup"><span data-stu-id="541c9-174">SupportedProtocols</span></span></td>
    <td><span data-ttu-id="541c9-175">Cria uma cadeia de caracteres que contém os esquemas de protocolo de URL para uma determinada chave.</span><span class="sxs-lookup"><span data-stu-id="541c9-175">Creates a string that contains the URL protocol schemes for a given key.</span></span> <span data-ttu-id="541c9-176">Isso pode conter vários valores de registro para indicar quais esquemas têm suporte.</span><span class="sxs-lookup"><span data-stu-id="541c9-176">This can contain multiple registry values to indicate which schemes are supported.</span></span> <span data-ttu-id="541c9-177">Essa cadeia de caracteres segue o formato de <strong>scheme1: scheme2</strong>.</span><span class="sxs-lookup"><span data-stu-id="541c9-177">This string follows the format of <strong>scheme1:scheme2</strong>.</span></span> <span data-ttu-id="541c9-178">Se essa lista não estiver vazia, <strong>file:</strong> será adicionado à cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="541c9-178">If this list is not empty, <strong>file:</strong> will be added to the string.</span></span> <span data-ttu-id="541c9-179">Esse protocolo tem suporte implícito quando <em>SupportedProtocols</em> é definido.</span><span class="sxs-lookup"><span data-stu-id="541c9-179">This protocol is implicitly supported when <em>SupportedProtocols</em> is defined.</span></span> <br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="541c9-180">UseUrl</span><span class="sxs-lookup"><span data-stu-id="541c9-180">UseUrl</span></span></td>
    <td><span data-ttu-id="541c9-181">Indica que seu aplicativo pode aceitar uma URL (em vez de um nome de arquivo) na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="541c9-181">Indicates that your application can accept a URL (instead of a file name) on the command line.</span></span> <span data-ttu-id="541c9-182">Os aplicativos que podem abrir documentos diretamente da Internet, como navegadores da Web e media players, devem definir essa entrada.</span><span class="sxs-lookup"><span data-stu-id="541c9-182">Applications that can open documents directly from the internet, like web browsers and media players, should set this entry.</span></span> <br/> <span data-ttu-id="541c9-183">Quando a função <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> inicia um aplicativo e o valor UseUrl = 1 não é definido, <strong>ShellExecuteEx</strong> baixa o documento em um arquivo local e invoca o manipulador na cópia local.</span><span class="sxs-lookup"><span data-stu-id="541c9-183">When the <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> function starts an application and the UseUrl=1 value is not set, <strong>ShellExecuteEx</strong> downloads the document to a local file and invokes the handler on the local copy.</span></span><br/> <span data-ttu-id="541c9-184">Por exemplo, se o aplicativo tiver essa entrada definida e um usuário clicar com o botão direito do mouse em um arquivo armazenado em um servidor Web, o verbo aberto será disponibilizado.</span><span class="sxs-lookup"><span data-stu-id="541c9-184">For example, if the application has this entry set and a user right-clicks on a file stored on a web server, the Open verb will be made available.</span></span> <span data-ttu-id="541c9-185">Caso contrário, o usuário precisará baixar o arquivo e abrir a cópia local.</span><span class="sxs-lookup"><span data-stu-id="541c9-185">If not, the user will have to download the file and open the local copy.</span></span> <br/> <span data-ttu-id="541c9-186">A entrada UseUrl é do tipo <strong>REG_DWORD</strong> e o valor é 0x1.</span><span class="sxs-lookup"><span data-stu-id="541c9-186">The UseUrl entry is of <strong>REG_DWORD</strong> type, and the value is 0x1.</span></span><br/> <span data-ttu-id="541c9-187">No Windows Vista e versões anteriores, essa entrada indicou que a URL deve ser passada para o aplicativo junto com um nome de arquivo local, quando chamado via ShellExecuteEx.</span><span class="sxs-lookup"><span data-stu-id="541c9-187">In Windows Vista and earlier, this entry indicated that the URL should be passed to the application along with a local file name, when called via ShellExecuteEx.</span></span> <span data-ttu-id="541c9-188">No Windows 7, ele indica que o aplicativo pode entender qualquer URL http ou HTTPS que é transmitida a ele, sem precisar fornecer o nome do arquivo de cache também.</span><span class="sxs-lookup"><span data-stu-id="541c9-188">In Windows 7, it indicates that the application can understand any http or https url that is passed to it, without having to supply the cache file name as well.</span></span> <span data-ttu-id="541c9-189">Essa chave do registro está associada à chave <em>SupportedProtocols</em> .</span><span class="sxs-lookup"><span data-stu-id="541c9-189">This registry key is associated with the <em>SupportedProtocols</em> key.</span></span><br/></td>
    </tr>
    </tbody>
    </table>

    

     

### <a name="using-the-applications-subkey"></a><span data-ttu-id="541c9-190">Usando a subchave Applications</span><span class="sxs-lookup"><span data-stu-id="541c9-190">Using the Applications Subkey</span></span>

<span data-ttu-id="541c9-191">Por meio da inclusão de entradas do registro na subchave **HKEY \_ classes \_ raiz** \\ **Applications** \\ *ApplicationName.exe* , os aplicativos podem fornecer as informações específicas do aplicativo mostradas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="541c9-191">Through the inclusion of registry entries under the **HKEY\_CLASSES\_ROOT**\\**Applications**\\*ApplicationName.exe* subkey, applications can provide the application-specific information shown in the following table.</span></span>



| <span data-ttu-id="541c9-192">Entrada de registro</span><span class="sxs-lookup"><span data-stu-id="541c9-192">Registry entry</span></span>                   | <span data-ttu-id="541c9-193">Description</span><span class="sxs-lookup"><span data-stu-id="541c9-193">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="541c9-194">verbo do Shell \\</span><span class="sxs-lookup"><span data-stu-id="541c9-194">shell\\verb</span></span>                      | <span data-ttu-id="541c9-195">Fornece o método verbo para chamar o aplicativo a partir de OpenWith.</span><span class="sxs-lookup"><span data-stu-id="541c9-195">Provides the verb method for calling the application from OpenWith.</span></span> <span data-ttu-id="541c9-196">Sem uma definição de verbo especificada aqui, o sistema pressupõe que o aplicativo dá suporte a [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)e passa o nome do arquivo na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="541c9-196">Without a verb definition specified here, the system assumes that the application supports [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa), and passes the file name on the command line.</span></span> <span data-ttu-id="541c9-197">Essa funcionalidade se aplica a todos os métodos de verbo, incluindo DropTarget, ExecuteCommand e troca dinâmica de dados (DDE).</span><span class="sxs-lookup"><span data-stu-id="541c9-197">This functionality applies to all the verb methods, including DropTarget, ExecuteCommand, and Dynamic Data Exchange (DDE).</span></span>                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="541c9-198">DefaultIcon</span><span class="sxs-lookup"><span data-stu-id="541c9-198">DefaultIcon</span></span>                      | <span data-ttu-id="541c9-199">Permite que um aplicativo forneça um ícone específico para representar o aplicativo em vez do primeiro ícone armazenado no arquivo. exe.</span><span class="sxs-lookup"><span data-stu-id="541c9-199">Enables an application to provide a specific icon to represent the application instead of the first icon stored in the .exe file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="541c9-200">FriendlyAppName</span><span class="sxs-lookup"><span data-stu-id="541c9-200">FriendlyAppName</span></span>                  | <span data-ttu-id="541c9-201">Fornece uma maneira de obter um nome localizável a ser exibido para um aplicativo, em vez de apenas as informações de versão que aparecem, o que pode não ser localizável.</span><span class="sxs-lookup"><span data-stu-id="541c9-201">Provides a way to get a localizable name to display for an application instead of just the version information appearing, which may not be localizable.</span></span> <span data-ttu-id="541c9-202">A consulta de associação [**ASSOCSTR**](/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr) lê esse valor de entrada de registro e volta a usar o nome FileDescription nas informações de versão.</span><span class="sxs-lookup"><span data-stu-id="541c9-202">The association query [**ASSOCSTR**](/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr) reads this registry entry value and falls back to use the FileDescription name in the version information.</span></span> <span data-ttu-id="541c9-203">Se esse nome estiver ausente, a consulta de associação usa como padrão o nome de exibição do arquivo.</span><span class="sxs-lookup"><span data-stu-id="541c9-203">If that name is missing, the association query defaults to the display name of the file.</span></span> <span data-ttu-id="541c9-204">Os aplicativos devem usar **ASSOCSTR \_ FRIENDLYAPPNAME** para recuperar essas informações para obter o comportamento adequado.</span><span class="sxs-lookup"><span data-stu-id="541c9-204">Applications should use **ASSOCSTR\_FRIENDLYAPPNAME** to retrieve this information to obtain the proper behavior.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="541c9-205">SupportedTypes</span><span class="sxs-lookup"><span data-stu-id="541c9-205">SupportedTypes</span></span>                   | <span data-ttu-id="541c9-206">Lista os tipos de arquivos aos quais o aplicativo dá suporte.</span><span class="sxs-lookup"><span data-stu-id="541c9-206">Lists the file types that the application supports.</span></span> <span data-ttu-id="541c9-207">Isso permite que o aplicativo seja listado no menu cascata da caixa de diálogo **abrir com** .</span><span class="sxs-lookup"><span data-stu-id="541c9-207">Doing so enables the application to be listed in the cascade menu of the **Open with** dialog box.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="541c9-208">NoOpenWith</span><span class="sxs-lookup"><span data-stu-id="541c9-208">NoOpenWith</span></span>                       | <span data-ttu-id="541c9-209">Indica que nenhum aplicativo foi especificado para abrir esse tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="541c9-209">Indicates that no application is specified for opening this file type.</span></span> <span data-ttu-id="541c9-210">Lembre-se de que, se uma subchave OpenWithProgIDs tiver sido definida para um aplicativo por tipo de arquivo e a subchave ProgID também não tiver uma entrada NoOpenWith, esse aplicativo será exibido na lista de aplicativos recomendados ou disponíveis, mesmo que tenha especificado a entrada NoOpenWith.</span><span class="sxs-lookup"><span data-stu-id="541c9-210">Be aware that if an OpenWithProgIDs subkey has been set for an application by file type, and the ProgID subkey itself does not also have a NoOpenWith entry, that application will appear in the list of recommended or available applications even if it has specified the NoOpenWith entry.</span></span> <span data-ttu-id="541c9-211">Para obter mais informações, consulte [como incluir um aplicativo na caixa de diálogo abrir com](how-to-include-an-application-on-the-open-with-dialog-box.md) e [como excluir um aplicativo da caixa de diálogo abrir com](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="541c9-211">For more information, see [How to How to Include an Application in the Open With Dialog Box](how-to-include-an-application-on-the-open-with-dialog-box.md) and [How to exclude an Application from the Open with Dialog Box](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md).</span></span><br/> |
| <span data-ttu-id="541c9-212">IsHostApp</span><span class="sxs-lookup"><span data-stu-id="541c9-212">IsHostApp</span></span>                        | <span data-ttu-id="541c9-213">Indica que o processo é um processo de host, como Rundll32.exe ou Dllhost.exe, e não deve ser considerado para fixação do menu **Iniciar** ou inclusão na lista de usados com mais frequência (MFU).</span><span class="sxs-lookup"><span data-stu-id="541c9-213">Indicates that the process is a host process, such as Rundll32.exe or Dllhost.exe, and should not be considered for **Start** menu pinning or inclusion in the Most Frequently Used (MFU) list.</span></span> <span data-ttu-id="541c9-214">Quando iniciado com um atalho que contém uma lista de argumentos não nulos ou um [AppUserModelIDs (IDs de modelo de usuário de aplicativo)](appids.md)explícitas, o processo pode ser fixado (como esse atalho).</span><span class="sxs-lookup"><span data-stu-id="541c9-214">When launched with a shortcut that contains a non-null argument list or an explicit [Application User Model IDs (AppUserModelIDs)](appids.md), the process can be pinned (as that shortcut).</span></span> <span data-ttu-id="541c9-215">Esses atalhos são candidatos para inclusão na lista de MFU.</span><span class="sxs-lookup"><span data-stu-id="541c9-215">Such shortcuts are candidates for inclusion in the MFU list.</span></span>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="541c9-216">NoStartPage</span><span class="sxs-lookup"><span data-stu-id="541c9-216">NoStartPage</span></span>                      | <span data-ttu-id="541c9-217">Indica que o executável do aplicativo e os atalhos devem ser excluídos do menu **Iniciar** e da fixação ou inclusão na lista MFU.</span><span class="sxs-lookup"><span data-stu-id="541c9-217">Indicates that the application executable and shortcuts should be excluded from the **Start** menu and from pinning or inclusion in the MFU list.</span></span> <span data-ttu-id="541c9-218">Essa entrada normalmente é usada para excluir ferramentas, instaladores e desinstaladores do sistema e arquivos Leiame.</span><span class="sxs-lookup"><span data-stu-id="541c9-218">This entry is typically used to exclude system tools, installers and uninstallers, and readme files.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="541c9-219">UseExecutableForTaskbarGroupIcon</span><span class="sxs-lookup"><span data-stu-id="541c9-219">UseExecutableForTaskbarGroupIcon</span></span> | <span data-ttu-id="541c9-220">Faz com que a barra de tarefas use o ícone padrão desse executável se não houver nenhum atalho fixas para esse aplicativo e, em vez do ícone da janela que foi encontrada pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="541c9-220">Causes the taskbar to use the default icon of this executable if there is no pinnable shortcut for this application, and instead of the icon of the window that was first encountered.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="541c9-221">TaskbarGroupIcon</span><span class="sxs-lookup"><span data-stu-id="541c9-221">TaskbarGroupIcon</span></span>                 | <span data-ttu-id="541c9-222">Especifica o ícone usado para substituir o ícone da barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="541c9-222">Specifies the icon used to override the taskbar icon.</span></span> <span data-ttu-id="541c9-223">O ícone de janela normalmente é usado para a barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="541c9-223">The window icon is normally used for the taskbar.</span></span> <span data-ttu-id="541c9-224">Definir a entrada TaskbarGroupIcon faz com que o sistema use o ícone do. exe para o aplicativo em vez disso.</span><span class="sxs-lookup"><span data-stu-id="541c9-224">Setting the TaskbarGroupIcon entry causes the system to use the icon from the .exe for the application instead.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

### <a name="examples"></a><span data-ttu-id="541c9-225">Exemplos</span><span class="sxs-lookup"><span data-stu-id="541c9-225">Examples</span></span>

<span data-ttu-id="541c9-226">Veja a seguir alguns exemplos de registros de aplicativo por meio da subchave **HKEY \_ classes \_ raiz** \\ **Applications** \\ *ApplicationName.exe* .</span><span class="sxs-lookup"><span data-stu-id="541c9-226">Some examples of application registrations through the **HKEY\_CLASSES\_ROOT**\\**Applications**\\*ApplicationName.exe* subkey are as follows.</span></span> <span data-ttu-id="541c9-227">Todos os valores de entrada do registro são do tipo **reg \_ sz** , com a exceção de **DefaultIcon** , que é do tipo **reg \_ Expand \_ sz** .</span><span class="sxs-lookup"><span data-stu-id="541c9-227">All registry entry values are of **REG\_SZ** type, with the exception of **DefaultIcon** which is of **REG\_EXPAND\_SZ** type.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      wordpad.exe
         FriendlyAppName = @%SystemRoot%\System32\shell32.dll,-22069
```

```
HKEY_CLASSES_ROOT
   Applications
      wmplayer.exe
         SupportedTypes
            .3gp2
```

```
HKEY_CLASSES_ROOT
   Applications
      wmplayer.exe
         DefaultIcon
            (Default) = %SystemRoot%\system32\wmploc.dll,-730
```

```
HKEY_CLASSES_ROOT
   Applications
      WScript.exe
         NoOpenWith
```

```
HKEY_CLASSES_ROOT
   Applications
      photoviewer.dll
         shell
            open
               DropTarget
                  Clsid = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
```

```
HKEY_CLASSES_ROOT
   Applications
      mspaint.exe
         SupportedTypes
            .bmp
            .dib
            .rle
            .jpg
            .jpeg
            .jpe
            .jfif
            .gif
            .emf
            .wmf
            .tif
            .tiff
            .png
            .ico
```

## <a name="registering-verbs-and-other-file-association-information"></a><span data-ttu-id="541c9-228">Registrando verbos e outras informações de associação de arquivo</span><span class="sxs-lookup"><span data-stu-id="541c9-228">Registering Verbs and Other File Association Information</span></span>

<span data-ttu-id="541c9-229">As subchaves registradas em **HKEY \_ classes \_ root** \\ **SystemFileAssociations** permitem que o Shell defina o comportamento padrão de atributos para tipos de arquivo e habilite associações de arquivos compartilhados.</span><span class="sxs-lookup"><span data-stu-id="541c9-229">Subkeys registered under **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** enable the Shell to define the default behavior of attributes for file types and enable shared file associations.</span></span> <span data-ttu-id="541c9-230">Quando os usuários alteram o aplicativo padrão para um tipo de arquivo, o ProgID do novo aplicativo padrão tem prioridade no fornecimento de verbos e outras informações de associação.</span><span class="sxs-lookup"><span data-stu-id="541c9-230">When users change the default application for a file type, the ProgID of the new default application has priority in providing verbs and other association information.</span></span> <span data-ttu-id="541c9-231">Essa prioridade se deve ao fato de ser a primeira entrada na matriz de associação.</span><span class="sxs-lookup"><span data-stu-id="541c9-231">This priority is due to it being the first entry in the association array.</span></span> <span data-ttu-id="541c9-232">Se o programa padrão for alterado, as informações no ProgID anterior não estarão mais disponíveis.</span><span class="sxs-lookup"><span data-stu-id="541c9-232">If the default program is changed, the information under the previous ProgID is no longer available.</span></span>

<span data-ttu-id="541c9-233">Para lidar de forma proativa com as consequências de uma alteração nos programas padrão, você pode usar a **\_ \_ raiz das classes hKey** \\ **SystemFileAssociations** para registrar verbos e outras informações de associação.</span><span class="sxs-lookup"><span data-stu-id="541c9-233">To deal proactively with the consequences of a change to default programs, you can use **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** to register verbs and other association information.</span></span> <span data-ttu-id="541c9-234">Devido ao seu local após o ProgID na matriz de associação, esses registros são de prioridade mais baixa.</span><span class="sxs-lookup"><span data-stu-id="541c9-234">Due to their location after the ProgID in the association array, these registrations are lower priority.</span></span> <span data-ttu-id="541c9-235">Esses SystemFileAssociationsregistrations são estáveis mesmo quando os usuários alteram os programas padrão e fornecem um local para registrar os verbos secundários que sempre estarão disponíveis para um determinado tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="541c9-235">These SystemFileAssociationsregistrations are stable even when users change the default programs, and provide a location to register secondary verbs that will always be available for a particular file type.</span></span> <span data-ttu-id="541c9-236">Para obter um exemplo de registro, consulte [registrando um tipo percebido](#registering-a-perceived-type) posteriormente neste tópico.</span><span class="sxs-lookup"><span data-stu-id="541c9-236">For a registry example, see [Registering a Perceived Type](#registering-a-perceived-type) later in this topic.</span></span>

<span data-ttu-id="541c9-237">O exemplo de registro a seguir mostra o que acontece quando o usuário executa o item **programas padrão** no painel de controle para alterar o padrão para arquivos. mp3 para App2ProgID.</span><span class="sxs-lookup"><span data-stu-id="541c9-237">The following registry example shows what happens when the user runs the **Default Programs** item in Control Panel to change the default for .mp3 files to App2ProgID.</span></span> <span data-ttu-id="541c9-238">Depois de alterar o padrão, Verb1 não estará mais disponível e Verb2 se tornará o padrão.</span><span class="sxs-lookup"><span data-stu-id="541c9-238">After changing the default, Verb1 is no longer available, and Verb2 becomes the default.</span></span>

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = App1ProgID
```

```
HKEY_CLASSES_ROOT
   App1ProgID
      shell
         Verb1
```

```
HKEY_CLASSES_ROOT
   App2ProgID
      shell
         Verb2
```

## <a name="registering-a-perceived-type"></a><span data-ttu-id="541c9-239">Registrando um tipo percebido</span><span class="sxs-lookup"><span data-stu-id="541c9-239">Registering a Perceived Type</span></span>

<span data-ttu-id="541c9-240">Os valores do registro para tipos observados são definidos como subchaves da subchave **HKEY \_ classes \_ root** \\ **SystemFileAssociations** do registro.</span><span class="sxs-lookup"><span data-stu-id="541c9-240">Registry values for perceived types are defined as subkeys of the **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** registry subkey.</span></span> <span data-ttu-id="541c9-241">Por exemplo, o **texto** do tipo percebido é registrado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="541c9-241">For example, the perceived type **text** is registered as follows:</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      text
         shell
            edit
               command
                  (Default) = "%SystemRoot%\system32\NOTEPAD.EXE" "%1"
            open
               command
                  (Default) = "%SystemRoot%\system32\NOTEPAD.EXE" "%1"
```

<span data-ttu-id="541c9-242">O tipo percebido de um tipo de arquivo é indicado pela inclusão de um valor percebido na subchave do tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="541c9-242">A file type's perceived type is indicated by including a PerceivedType value in the file type's subkey.</span></span> <span data-ttu-id="541c9-243">O valor percebidotype é definido como o nome do tipo percebido registrado na subchave do registro de **\_ classes \_** \\ **SystemFileAssociations** do hKey, conforme mostrado no exemplo de registro anterior.</span><span class="sxs-lookup"><span data-stu-id="541c9-243">The PerceivedType value is set to the name of the perceived type registered under **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** registry subkey, as shown in the previous registry example.</span></span> <span data-ttu-id="541c9-244">Para declarar arquivos. cpp como sendo do tipo percebido "text", por exemplo, adicione a seguinte entrada de registro:</span><span class="sxs-lookup"><span data-stu-id="541c9-244">To declare .cpp files as being of perceived type "text", for example, add the following registry entry:</span></span>

```
HKEY_CLASSES_ROOT
   .cpp
      PerceivedType = text
```

## <a name="related-topics"></a><span data-ttu-id="541c9-245">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="541c9-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="541c9-246">Tipos de arquivo</span><span class="sxs-lookup"><span data-stu-id="541c9-246">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="541c9-247">Como funcionam as associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="541c9-247">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="541c9-248">Exibição de conteúdo por tipo de arquivo ou tipo</span><span class="sxs-lookup"><span data-stu-id="541c9-248">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="541c9-249">Verificador de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="541c9-249">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="541c9-250">Manipuladores de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="541c9-250">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="541c9-251">Identificadores programáticos</span><span class="sxs-lookup"><span data-stu-id="541c9-251">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="541c9-252">Tipos observados</span><span class="sxs-lookup"><span data-stu-id="541c9-252">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="541c9-253">Matrizes de associação</span><span class="sxs-lookup"><span data-stu-id="541c9-253">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

