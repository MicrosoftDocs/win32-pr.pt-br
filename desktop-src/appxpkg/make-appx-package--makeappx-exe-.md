---
title: Empacotador de aplicativo (MakeAppx.exe)
description: O app Packager (MakeAppx.exe) cria um pacote de aplicativo de arquivos em disco ou extrai os arquivos de um pacote de aplicativo para o disco.
ms.assetid: 9B7BF420-8E19-4BFD-B378-D09E61F68A39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41595550f3bee7b1149959886ed649e9212224b2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104084457"
---
# <a name="app-packager-makeappxexe"></a><span data-ttu-id="1aa98-103">Empacotador de aplicativo (MakeAppx.exe)</span><span class="sxs-lookup"><span data-stu-id="1aa98-103">App packager (MakeAppx.exe)</span></span>

> [!Note]  
> <span data-ttu-id="1aa98-104">Para obter diretrizes de UWP sobre como usar essa ferramenta, consulte [criar um pacote de aplicativo com a ferramenta de MakeAppx.exe](/windows/msix/package/create-app-package-with-makeappx-tool).</span><span class="sxs-lookup"><span data-stu-id="1aa98-104">For UWP guidance on using this tool, see [Create an app package with the MakeAppx.exe tool](/windows/msix/package/create-app-package-with-makeappx-tool).</span></span>

 

<span data-ttu-id="1aa98-105">O app Packager (MakeAppx.exe) cria um pacote de aplicativo de arquivos em disco ou extrai os arquivos de um pacote de aplicativo para o disco.</span><span class="sxs-lookup"><span data-stu-id="1aa98-105">App packager (MakeAppx.exe) creates an app package from files on disk or extracts the files from an app package to disk.</span></span> <span data-ttu-id="1aa98-106">A partir do Windows 8.1, o app Packager também cria um pacote de aplicativos de pacotes de aplicativos no disco ou extrai os pacotes de aplicativos de um pacote de pacotes de aplicativos para o disco.</span><span class="sxs-lookup"><span data-stu-id="1aa98-106">Starting with Windows 8.1, App packager also creates an app package bundle from app packages on disk or extracts the app packages from an app package bundle to disk.</span></span> <span data-ttu-id="1aa98-107">Ele está incluído no Microsoft Visual Studio e no SDK (Software Development Kit) do Windows para Windows 8 ou Windows Software Development Kit (SDK) para Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="1aa98-107">It is included in Microsoft Visual Studio and the Windows Software Development Kit (SDK) for Windows 8 or Windows Software Development Kit (SDK) for Windows 8.1.</span></span> <span data-ttu-id="1aa98-108">Visite [downloads para que os desenvolvedores os]( https://msdn.microsoft.com/windows/apps/br229516.aspx) obtenham.</span><span class="sxs-lookup"><span data-stu-id="1aa98-108">Visit [Downloads for developers]( https://msdn.microsoft.com/windows/apps/br229516.aspx) to get them.</span></span>

<span data-ttu-id="1aa98-109">A ferramenta de MakeAppx.exe normalmente é encontrada nestes locais:</span><span class="sxs-lookup"><span data-stu-id="1aa98-109">The MakeAppx.exe tool is typically found at these locations:</span></span>

-   <span data-ttu-id="1aa98-110">Em x86: C: \\ Program Files (x86) \\ windows kits \\ 8,0 \\ bin \\ x86 \\makeappx.exe ou C: \\ Program files (x86) \\ Windows kits \\ 8,1 \\ bin \\ x86 \\makeappx.exe</span><span class="sxs-lookup"><span data-stu-id="1aa98-110">On x86: C:\\Program Files (x86)\\Windows Kits\\8.0\\bin\\x86\\makeappx.exe or C:\\Program Files (x86)\\Windows Kits\\8.1\\bin\\x86\\makeappx.exe</span></span>
-   <span data-ttu-id="1aa98-111">Em x64 em dois locais:</span><span class="sxs-lookup"><span data-stu-id="1aa98-111">On x64 in two locations:</span></span>
    -   <span data-ttu-id="1aa98-112">C: \\ arquivos de programas (x86) \\ kits do Windows \\ 8,0 \\ bin \\ x86 \\makeappx.exe ou C: \\ arquivos de programas (x86) \\ kits do Windows \\ 8,1 \\ compartimento \\ x86 \\makeappx.exe</span><span class="sxs-lookup"><span data-stu-id="1aa98-112">C:\\Program Files (x86)\\Windows Kits\\8.0\\bin\\x86\\makeappx.exe or C:\\Program Files (x86)\\Windows Kits\\8.1\\bin\\x86\\makeappx.exe</span></span>
    -   <span data-ttu-id="1aa98-113">C: \\ arquivos de programas (x86) \\ windows kits \\ 8,0 \\ bin \\ x64 \\makeappx.exe ou C: \\ arquivos de programas (x86) kits do \\ Windows \\ 8,1 \\ bin \\ x64 \\makeappx.exe</span><span class="sxs-lookup"><span data-stu-id="1aa98-113">C:\\Program Files (x86)\\Windows Kits\\8.0\\bin\\x64\\makeappx.exe or C:\\Program Files (x86)\\Windows Kits\\8.1\\bin\\x64\\makeappx.exe</span></span>

<span data-ttu-id="1aa98-114">Não há nenhuma versão ARM da ferramenta.</span><span class="sxs-lookup"><span data-stu-id="1aa98-114">There is no ARM version of the tool.</span></span>

-   [<span data-ttu-id="1aa98-115">Para criar um pacote usando uma estrutura de diretório</span><span class="sxs-lookup"><span data-stu-id="1aa98-115">To create a package using a directory structure</span></span>](#to-create-a-package-using-a-directory-structure)
-   [<span data-ttu-id="1aa98-116">Para criar um pacote usando um arquivo de mapeamento</span><span class="sxs-lookup"><span data-stu-id="1aa98-116">To create a package using a mapping file</span></span>](#to-create-a-package-using-a-mapping-file)
-   [<span data-ttu-id="1aa98-117">Para assinar o pacote usando SignTool</span><span class="sxs-lookup"><span data-stu-id="1aa98-117">To sign the package using SignTool</span></span>](#to-sign-the-package-using-signtool)
-   [<span data-ttu-id="1aa98-118">Para extrair arquivos de um pacote</span><span class="sxs-lookup"><span data-stu-id="1aa98-118">To extract files from a package</span></span>](#to-extract-files-from-a-package)
-   [<span data-ttu-id="1aa98-119">Para criar um pacote de pacotes usando uma estrutura de diretório</span><span class="sxs-lookup"><span data-stu-id="1aa98-119">To create a package bundle using a directory structure</span></span>](#to-create-a-package-bundle-using-a-directory-structure)
-   [<span data-ttu-id="1aa98-120">Para criar um pacote de pacotes usando um arquivo de mapeamento</span><span class="sxs-lookup"><span data-stu-id="1aa98-120">To create a package bundle using a mapping file</span></span>](#to-create-a-package-bundle-using-a-mapping-file)
-   [<span data-ttu-id="1aa98-121">Para extrair pacotes de um pacote</span><span class="sxs-lookup"><span data-stu-id="1aa98-121">To extract packages from a bundle</span></span>](#to-extract-packages-from-a-bundle)
-   [<span data-ttu-id="1aa98-122">Para criptografar um pacote com um arquivo de chave</span><span class="sxs-lookup"><span data-stu-id="1aa98-122">To encrypt a package with a key file</span></span>](#to-encrypt-a-package-with-a-key-file)
-   [<span data-ttu-id="1aa98-123">Para criptografar um pacote com uma chave de teste global</span><span class="sxs-lookup"><span data-stu-id="1aa98-123">To encrypt a package with a global test key</span></span>](#to-encrypt-a-package-with-a-global-test-key)
-   [<span data-ttu-id="1aa98-124">Para descriptografar um pacote com um arquivo de chave</span><span class="sxs-lookup"><span data-stu-id="1aa98-124">To decrypt a package with a key file</span></span>](#to-decrypt-a-package-with-a-key-file)
-   [<span data-ttu-id="1aa98-125">Para descriptografar um pacote com uma chave de teste global</span><span class="sxs-lookup"><span data-stu-id="1aa98-125">To decrypt a package with a global test key</span></span>](#to-decrypt-a-package-with-a-global-test-key)
-   [<span data-ttu-id="1aa98-126">Usage</span><span class="sxs-lookup"><span data-stu-id="1aa98-126">Usage</span></span>](#usage)

## <a name="using-app-packager"></a><span data-ttu-id="1aa98-127">Usando o app Packager</span><span class="sxs-lookup"><span data-stu-id="1aa98-127">Using App packager</span></span>

> [!Note]  
> <span data-ttu-id="1aa98-128">Caminhos relativos têm suporte em toda a ferramenta.</span><span class="sxs-lookup"><span data-stu-id="1aa98-128">Relative paths are supported throughout the tool.</span></span>

 

### <a name="to-create-a-package-using-a-directory-structure"></a><span data-ttu-id="1aa98-129">Para criar um pacote usando uma estrutura de diretório</span><span class="sxs-lookup"><span data-stu-id="1aa98-129">To create a package using a directory structure</span></span>

<span data-ttu-id="1aa98-130">Coloque o AppxManifest.xml na raiz de um diretório que contém todos os arquivos de carga para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1aa98-130">Place the AppxManifest.xml in the root of a directory containing all of the payload files for your app.</span></span> <span data-ttu-id="1aa98-131">Uma estrutura de diretório idêntica é criada para o pacote do aplicativo e estará disponível quando o pacote for extraído no momento da implantação.</span><span class="sxs-lookup"><span data-stu-id="1aa98-131">An identical directory structure is created for the app package, and will be available when the package is extracted at deployment time.</span></span>

1.  <span data-ttu-id="1aa98-132">Coloque todos os arquivos em uma única estrutura de diretório, criando subdiretórios conforme desejado.</span><span class="sxs-lookup"><span data-stu-id="1aa98-132">Place all files in a single directory structure, creating subdirectories as desired.</span></span>

2.  <span data-ttu-id="1aa98-133">Crie um manifesto de pacote válido, AppxManifest.xml e coloque-o no diretório raiz.</span><span class="sxs-lookup"><span data-stu-id="1aa98-133">Create a valid package manifest, AppxManifest.xml, and place it in the root directory.</span></span>

3.  <span data-ttu-id="1aa98-134">Execute este comando:</span><span class="sxs-lookup"><span data-stu-id="1aa98-134">Run this command:</span></span>

    <span data-ttu-id="1aa98-135">**MakeAppx Pack/d** *entrada \_ DirectoryPath* **/p** _FilePath_**. Appx**</span><span class="sxs-lookup"><span data-stu-id="1aa98-135">**MakeAppx pack /d** *input\_directorypath* **/p** _filepath_**.appx**</span></span>

### <a name="to-create-a-package-using-a-mapping-file"></a><span data-ttu-id="1aa98-136">Para criar um pacote usando um arquivo de mapeamento</span><span class="sxs-lookup"><span data-stu-id="1aa98-136">To create a package using a mapping file</span></span>

1.  <span data-ttu-id="1aa98-137">Crie um manifesto de pacote válido, AppxManifest.xml.</span><span class="sxs-lookup"><span data-stu-id="1aa98-137">Create a valid package manifest, AppxManifest.xml.</span></span>

2.  <span data-ttu-id="1aa98-138">Crie um arquivo de mapeamento.</span><span class="sxs-lookup"><span data-stu-id="1aa98-138">Create a mapping file.</span></span> <span data-ttu-id="1aa98-139">A primeira linha contém os **\[ arquivos \]** de cadeia de caracteres e as linhas a seguir especificam os caminhos de origem (disco) e destino (pacote) em cadeias de caracteres entre aspas.</span><span class="sxs-lookup"><span data-stu-id="1aa98-139">The first line contains the string **\[Files\]**, and the lines that follow specify the source (disk) and destination (package) paths in quoted strings.</span></span>

    ``` syntax
    [Files]
    "C:\MyApp\StartPage.htm"     "default.html"
    "C:\MyApp\readme.txt"        "doc\readme.txt"
    "\\MyServer\path\icon.png"   "icon.png"
    "MyCustomManifest.xml"       "AppxManifest.xml"
    ```

3.  <span data-ttu-id="1aa98-140">Execute este comando:</span><span class="sxs-lookup"><span data-stu-id="1aa98-140">Run this command:</span></span>

    <span data-ttu-id="1aa98-141">**MakeAppx Pack/f** *mapeando \_ FilePath* **/p** _FilePath_**. Appx**</span><span class="sxs-lookup"><span data-stu-id="1aa98-141">**MakeAppx pack /f** *mapping\_filepath* **/p** _filepath_**.appx**</span></span>

### <a name="to-sign-the-package-using-signtool"></a><span data-ttu-id="1aa98-142">Para assinar o pacote usando SignTool</span><span class="sxs-lookup"><span data-stu-id="1aa98-142">To sign the package using SignTool</span></span>

1.  <span data-ttu-id="1aa98-143">Crie o certificado.</span><span class="sxs-lookup"><span data-stu-id="1aa98-143">Create the certificate.</span></span> <span data-ttu-id="1aa98-144">O Publicador listado no manifesto deve corresponder às informações do assunto do Publicador do certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="1aa98-144">The publisher listed in the manifest must match the publisher subject information of the signing certificate.</span></span> <span data-ttu-id="1aa98-145">Para obter mais informações sobre como criar um certificado de autenticação, consulte [como criar um certificado de assinatura de pacote de aplicativo](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="1aa98-145">For more info about creating a signing certificate, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>

2.  <span data-ttu-id="1aa98-146">Execute SignTool.exe para assinar o pacote:</span><span class="sxs-lookup"><span data-stu-id="1aa98-146">Run SignTool.exe to sign the package:</span></span>

    <span data-ttu-id="1aa98-147">**Signtool sinal/a/v/FD** *hashAlgorithm* **/f** *certFileName* _FilePath_**. Appx**</span><span class="sxs-lookup"><span data-stu-id="1aa98-147">**SignTool sign /a /v /fd** *hashAlgorithm* **/f** *certFileName* _filepath_**.appx**</span></span>

    <span data-ttu-id="1aa98-148">O *hashAlgorithm* deve corresponder ao algoritmo de hash usado para criar o blockmap quando o aplicativo foi empacotado.</span><span class="sxs-lookup"><span data-stu-id="1aa98-148">The *hashAlgorithm* must match the hash algorithm used to create the blockmap when the app was packaged.</span></span> <span data-ttu-id="1aa98-149">Com o utilitário de empacotamento MakeAppx, o algoritmo de hash Appx blockmap padrão é **SHA256**.</span><span class="sxs-lookup"><span data-stu-id="1aa98-149">With the MakeAppx packaging utility, the default Appx blockmap hash algorithm is **SHA256**.</span></span> <span data-ttu-id="1aa98-150">Execute SignTool.exe especificando **SHA256** como o algoritmo de síntese de arquivo (/FD):</span><span class="sxs-lookup"><span data-stu-id="1aa98-150">Run SignTool.exe specifying **SHA256** as the file digest (/fd) algorithm:</span></span>

    <span data-ttu-id="1aa98-151">**Signtool sinal/a/v/FD SHA256/F** *certFileName* _FilePath_**. Appx**</span><span class="sxs-lookup"><span data-stu-id="1aa98-151">**SignTool sign /a /v /fd SHA256 /f** *certFileName* _filepath_**.appx**</span></span>

    <span data-ttu-id="1aa98-152">Para obter mais informações sobre como assinar pacotes, consulte [como assinar um pacote de aplicativo usando Signtool](how-to-sign-a-package-using-signtool.md).</span><span class="sxs-lookup"><span data-stu-id="1aa98-152">For more info about how to sign packages, see [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md).</span></span>

### <a name="to-extract-files-from-a-package"></a><span data-ttu-id="1aa98-153">Para extrair arquivos de um pacote</span><span class="sxs-lookup"><span data-stu-id="1aa98-153">To extract files from a package</span></span>

1.  <span data-ttu-id="1aa98-154">Execute este comando:</span><span class="sxs-lookup"><span data-stu-id="1aa98-154">Run this command:</span></span>

    <span data-ttu-id="1aa98-155">**MakeAppx Unpack/p** _File_**. Appx/d** *\_ diretório de saída*</span><span class="sxs-lookup"><span data-stu-id="1aa98-155">**MakeAppx unpack /p** _file_**.appx /d** *output\_directory*</span></span>

2.  <span data-ttu-id="1aa98-156">O pacote desempacotado tem a mesma estrutura que o pacote instalado.</span><span class="sxs-lookup"><span data-stu-id="1aa98-156">The unpacked package has the same structure as the installed package.</span></span>

### <a name="to-create-a-package-bundle-using-a-directory-structure"></a><span data-ttu-id="1aa98-157">Para criar um pacote de pacotes usando uma estrutura de diretório</span><span class="sxs-lookup"><span data-stu-id="1aa98-157">To create a package bundle using a directory structure</span></span>

<span data-ttu-id="1aa98-158">Usamos o comando **Bundle** para criar um pacote de aplicativo em</span><span class="sxs-lookup"><span data-stu-id="1aa98-158">We use the **bundle** command to create an app bundle at</span></span> <output bundle name> <span data-ttu-id="1aa98-159">Adicionando todos os pacotes de <content directory> (incluindo subpastas).</span><span class="sxs-lookup"><span data-stu-id="1aa98-159">by adding all packages from <content directory> (including subfolders).</span></span> <span data-ttu-id="1aa98-160">Se <content directory> contiver um manifesto de pacote, AppxBundleManifest.xml, ele será ignorado.</span><span class="sxs-lookup"><span data-stu-id="1aa98-160">If <content directory> contains a bundle manifest, AppxBundleManifest.xml, it is ignored.</span></span>

1.  <span data-ttu-id="1aa98-161">Coloque todos os pacotes em uma única estrutura de diretório, criando subdiretórios conforme desejado.</span><span class="sxs-lookup"><span data-stu-id="1aa98-161">Place all packages in a single directory structure, creating subdirectories as desired.</span></span>

2.  <span data-ttu-id="1aa98-162">Execute este comando:</span><span class="sxs-lookup"><span data-stu-id="1aa98-162">Run this command:</span></span>

    <span data-ttu-id="1aa98-163">**MakeAppx Bundle/d** *entrada \_ DirectoryPath* **/p** _FilePath_**. appxbundle**</span><span class="sxs-lookup"><span data-stu-id="1aa98-163">**MakeAppx bundle /d** *input\_directorypath* **/p** _filepath_**.appxbundle**</span></span>

### <a name="to-create-a-package-bundle-using-a-mapping-file"></a><span data-ttu-id="1aa98-164">Para criar um pacote de pacotes usando um arquivo de mapeamento</span><span class="sxs-lookup"><span data-stu-id="1aa98-164">To create a package bundle using a mapping file</span></span>

<span data-ttu-id="1aa98-165">Usamos o comando **Bundle** para criar um pacote de aplicativo em</span><span class="sxs-lookup"><span data-stu-id="1aa98-165">We use the **bundle** command to create an app bundle at</span></span> <output bundle name> <span data-ttu-id="1aa98-166">Adicionando todos os pacotes de uma lista de pacotes no <mapping file> .</span><span class="sxs-lookup"><span data-stu-id="1aa98-166">by adding all packages from a list of packages within <mapping file>.</span></span> <span data-ttu-id="1aa98-167">Se <mapping file> contiver um manifesto de pacote, AppxBundleManifest.xml, ele será ignorado.</span><span class="sxs-lookup"><span data-stu-id="1aa98-167">If <mapping file> contains a bundle manifest, AppxBundleManifest.xml, it is ignored.</span></span>

1.  <span data-ttu-id="1aa98-168">Criará um <mapping file>.</span><span class="sxs-lookup"><span data-stu-id="1aa98-168">Create a <mapping file>.</span></span> <span data-ttu-id="1aa98-169">A primeira linha contém os **\[ arquivos \]** de cadeia de caracteres e as linhas a seguir especificam os pacotes a serem adicionados ao pacote.</span><span class="sxs-lookup"><span data-stu-id="1aa98-169">The first line contains the string **\[Files\]**, and the lines that follow specify the packages to add to the bundle.</span></span> <span data-ttu-id="1aa98-170">Cada pacote é descrito por um par de caminhos entre aspas, separados por espaços ou tabulações.</span><span class="sxs-lookup"><span data-stu-id="1aa98-170">Each package is described by a pair of paths in quotation marks, separated by spaces or tabs.</span></span> <span data-ttu-id="1aa98-171">O par de caminhos representa a origem do pacote (no disco) e o destino (em grupo).</span><span class="sxs-lookup"><span data-stu-id="1aa98-171">The pair of paths represents the package's source (on disk) and destination (in bundle).</span></span> <span data-ttu-id="1aa98-172">Todos os nomes de pacote de destino devem ter a extensão. Appx.</span><span class="sxs-lookup"><span data-stu-id="1aa98-172">All destination package names must have the .appx extension.</span></span>

    ``` syntax
        [Files]
        "C:\MyApp\MyApp_x86.appx"                 "MyApp_x86.appx"
        "C:\Program Files (x86)\ResPack.appx"    "resources\resPack.appx"
        "\\MyServer\path\ResPack.appx"           "Respack.appx"
        "my app files\respack.appx"              "my app files\respack.appx"
    ```

2.  <span data-ttu-id="1aa98-173">Execute este comando:</span><span class="sxs-lookup"><span data-stu-id="1aa98-173">Run this command:</span></span>

    <span data-ttu-id="1aa98-174">**Pacote MakeAppx/f** *mapeando \_ FilePath* **/p** _FilePath_**. appxbundle**</span><span class="sxs-lookup"><span data-stu-id="1aa98-174">**MakeAppx bundle /f** *mapping\_filepath* **/p** _filepath_**.appxbundle**</span></span>

### <a name="to-extract-packages-from-a-bundle"></a><span data-ttu-id="1aa98-175">Para extrair pacotes de um pacote</span><span class="sxs-lookup"><span data-stu-id="1aa98-175">To extract packages from a bundle</span></span>

1.  <span data-ttu-id="1aa98-176">Execute este comando:</span><span class="sxs-lookup"><span data-stu-id="1aa98-176">Run this command:</span></span>

    <span data-ttu-id="1aa98-177">**MakeAppx desagrupar/p** _\_ nome do pacote_**. appxbundle/d** *\_ diretório de saída*</span><span class="sxs-lookup"><span data-stu-id="1aa98-177">**MakeAppx unbundle /p** _bundle\_name_**.appxbundle /d** *output\_directory*</span></span>

2.  <span data-ttu-id="1aa98-178">O pacote desempacotado tem a mesma estrutura que o pacote de pacotes instalado.</span><span class="sxs-lookup"><span data-stu-id="1aa98-178">The unpacked bundle has the same structure as the installed package bundle.</span></span>

### <a name="to-encrypt-a-package-with-a-key-file"></a><span data-ttu-id="1aa98-179">Para criptografar um pacote com um arquivo de chave</span><span class="sxs-lookup"><span data-stu-id="1aa98-179">To encrypt a package with a key file</span></span>

1.  <span data-ttu-id="1aa98-180">Crie um arquivo de chave.</span><span class="sxs-lookup"><span data-stu-id="1aa98-180">Create a key file.</span></span> <span data-ttu-id="1aa98-181">Os arquivos de chave devem começar com uma linha que contém a cadeia de caracteres " \[ Keys \] " seguida por linhas que descrevem as chaves com as quais criptografar o pacote.</span><span class="sxs-lookup"><span data-stu-id="1aa98-181">Key files must begin with a line containing the string "\[Keys\]" followed by lines describing the keys to encrypt the package with.</span></span> <span data-ttu-id="1aa98-182">Cada chave é descrita por um par de cadeias de caracteres entre aspas, separadas por espaços ou tabulações.</span><span class="sxs-lookup"><span data-stu-id="1aa98-182">Each key is described by a pair of strings in quotation marks, separated by spaces or tabs.</span></span> <span data-ttu-id="1aa98-183">A primeira cadeia de caracteres representa a ID da chave e a segunda cadeia de caracteres representa a chave de criptografia em formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="1aa98-183">The first string represents the key ID and the second string represents the encryption key in hexadecimal form.</span></span>

    ``` syntax
        [Keys]
        "0"                 "1AC4CDCFF1924D2885A0607269787BA6BF09B7FFEBF74ED4B9D86E423CF9186B"
    ```

2.  <span data-ttu-id="1aa98-184">Execute este comando:</span><span class="sxs-lookup"><span data-stu-id="1aa98-184">Run this command:</span></span>

    <span data-ttu-id="1aa98-185">**MakeAppx.exe criptografar/p** _\_ nome do pacote_**. Appx/EP** _Encrypted \_ Package \_ Name_**. eappx/KF** _keyfile \_ Name_**. txt**</span><span class="sxs-lookup"><span data-stu-id="1aa98-185">**MakeAppx.exe encrypt /p** _package\_name_**.appx /ep** _encrypted\_package\_name_**.eappx /kf** _keyfile\_name_**.txt**</span></span>

3.  <span data-ttu-id="1aa98-186">O pacote de entrada será criptografado no pacote criptografado especificado usando o arquivo de chave fornecido.</span><span class="sxs-lookup"><span data-stu-id="1aa98-186">The input package will be encrypted into the specified encrypted package using the provided key file.</span></span>

### <a name="to-encrypt-a-package-with-a-global-test-key"></a><span data-ttu-id="1aa98-187">Para criptografar um pacote com uma chave de teste global</span><span class="sxs-lookup"><span data-stu-id="1aa98-187">To encrypt a package with a global test key</span></span>

1.  <span data-ttu-id="1aa98-188">Execute este comando:</span><span class="sxs-lookup"><span data-stu-id="1aa98-188">Run this command:</span></span>

    <span data-ttu-id="1aa98-189">**MakeAppx.exe criptografar/p** _\_ nome do pacote_**. Appx/EP** _\_ \_ nome do pacote criptografado_**. eappx/KT**</span><span class="sxs-lookup"><span data-stu-id="1aa98-189">**MakeAppx.exe encrypt /p** _package\_name_**.appx /ep** _encrypted\_package\_name_**.eappx /kt**</span></span>

2.  <span data-ttu-id="1aa98-190">O pacote de entrada será criptografado no pacote criptografado especificado usando a chave de teste global.</span><span class="sxs-lookup"><span data-stu-id="1aa98-190">The input package will be encrypted into the specified encrypted package using the global test key.</span></span>

### <a name="to-decrypt-a-package-with-a-key-file"></a><span data-ttu-id="1aa98-191">Para descriptografar um pacote com um arquivo de chave</span><span class="sxs-lookup"><span data-stu-id="1aa98-191">To decrypt a package with a key file</span></span>

1.  <span data-ttu-id="1aa98-192">Crie um arquivo de chave.</span><span class="sxs-lookup"><span data-stu-id="1aa98-192">Create a key file.</span></span> <span data-ttu-id="1aa98-193">Os arquivos de chave devem começar com uma linha que contém a cadeia de caracteres " \[ Keys \] " seguida por linhas que descrevem as chaves com as quais criptografar o pacote.</span><span class="sxs-lookup"><span data-stu-id="1aa98-193">Key files must begin with a line containing the string "\[Keys\]" followed by lines describing the keys to encrypt the package with.</span></span> <span data-ttu-id="1aa98-194">Cada chave é descrita por um par de cadeias de caracteres entre aspas, separadas por espaços ou tabulações.</span><span class="sxs-lookup"><span data-stu-id="1aa98-194">Each key is described by a pair of strings in quotation marks, separated by spaces or tabs.</span></span> <span data-ttu-id="1aa98-195">A primeira cadeia de caracteres representa a ID de chave de 32 bytes codificada em Base64 e a segunda cadeia de caracteres representa a chave de criptografia de 32 bytes codificada em base64.</span><span class="sxs-lookup"><span data-stu-id="1aa98-195">The first string represents the base64 encoded 32-byte key ID and the second string represents the base64 encoded 32-byte encryption key.</span></span>

    ``` syntax
        [Keys]
        "OWVwSzliRGY1VWt1ODk4N1Q4R2Vqc04zMzIzNnlUREU="                 "MjNFTlFhZGRGZEY2YnVxMTBocjd6THdOdk9pZkpvelc="
    ```

2.  <span data-ttu-id="1aa98-196">Execute este comando:</span><span class="sxs-lookup"><span data-stu-id="1aa98-196">Run this command:</span></span>

    <span data-ttu-id="1aa98-197">**MakeAppx.exe descriptografar/p** _\_ nome do pacote_**. Appx/EP** _\_ \_ nome do pacote não criptografado_**. eappx/KF** _\_ nome do keyfile_**. txt**</span><span class="sxs-lookup"><span data-stu-id="1aa98-197">**MakeAppx.exe decrypt /p** _package\_name_**.appx /ep** _unencrypted\_package\_name_**.eappx /kf** _keyfile\_name_**.txt**</span></span>

3.  <span data-ttu-id="1aa98-198">O pacote de entrada será descriptografado no pacote não criptografado especificado usando o arquivo de chave fornecido.</span><span class="sxs-lookup"><span data-stu-id="1aa98-198">The input package will be decrypted into the specified unencrypted package using the provided key file.</span></span>

### <a name="to-decrypt-a-package-with-a-global-test-key"></a><span data-ttu-id="1aa98-199">Para descriptografar um pacote com uma chave de teste global</span><span class="sxs-lookup"><span data-stu-id="1aa98-199">To decrypt a package with a global test key</span></span>

1.  <span data-ttu-id="1aa98-200">Execute este comando:</span><span class="sxs-lookup"><span data-stu-id="1aa98-200">Run this command:</span></span>

    <span data-ttu-id="1aa98-201">**MakeAppx.exe descriptografar/p** _\_ nome do pacote_**. Appx/EP** _\_ \_ nome do pacote não criptografado_**. eappx/KT**</span><span class="sxs-lookup"><span data-stu-id="1aa98-201">**MakeAppx.exe decrypt /p** _package\_name_**.appx /ep** _unencrypted\_package\_name_**.eappx /kt**</span></span>

2.  <span data-ttu-id="1aa98-202">O pacote de entrada será descriptografado no pacote não criptografado especificado usando a chave de teste global.</span><span class="sxs-lookup"><span data-stu-id="1aa98-202">The input package will be decrypted into the specified unencrypted package using the global test key.</span></span>

## <a name="usage"></a><span data-ttu-id="1aa98-203">Uso</span><span class="sxs-lookup"><span data-stu-id="1aa98-203">Usage</span></span>

<span data-ttu-id="1aa98-204">O argumento de linha de comando **/p** é sempre necessário, com **/d**, **/f** ou **/EP**.</span><span class="sxs-lookup"><span data-stu-id="1aa98-204">The command line argument **/p** is always required, with either **/d**, **/f**, or **/ep**.</span></span> <span data-ttu-id="1aa98-205">Observe que **/d**, **/f** e **/EP** são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="1aa98-205">Note that **/d**, **/f**, and **/ep** are mutually exclusive.</span></span>

<span data-ttu-id="1aa98-206">**\[ Opções \] do MakeAppx Pack** **/p** *\<output package name\>* \**/d\*\*\*\<content directory\>*</span><span class="sxs-lookup"><span data-stu-id="1aa98-206">**MakeAppx pack \[options\]** **/p** *\<output package name\>* **/d** *\<content directory\>*</span></span>

<span data-ttu-id="1aa98-207">**\[ Opções \] do MakeAppx Pack** **/p** *\<output package name\>* \**/f\*\*\*\<mapping file\>*</span><span class="sxs-lookup"><span data-stu-id="1aa98-207">**MakeAppx pack \[options\]** **/p** *\<output package name\>* **/f** *\<mapping file\>*</span></span>

<span data-ttu-id="1aa98-208">**MakeAppx \[ opções \] de desempacotamento** **/p** *\<input package name\>* \**/d\*\*\*\<output directory\>*</span><span class="sxs-lookup"><span data-stu-id="1aa98-208">**MakeAppx unpack \[options\]** **/p** *\<input package name\>* **/d** *\<output directory\>*</span></span>

<span data-ttu-id="1aa98-209">**\[ Opções \] de pacote MakeAppx** **/p** *\<output bundle name\>* \**/d\*\*\*\<content directory\>*</span><span class="sxs-lookup"><span data-stu-id="1aa98-209">**MakeAppx bundle \[options\]** **/p** *\<output bundle name\>* **/d** *\<content directory\>*</span></span>

<span data-ttu-id="1aa98-210">**\[ Opções \] de pacote MakeAppx** **/p** *\<output bundle name\>* \**/f\*\*\*\<mapping file\>*</span><span class="sxs-lookup"><span data-stu-id="1aa98-210">**MakeAppx bundle \[options\]** **/p** *\<output bundle name\>* **/f** *\<mapping file\>*</span></span>

<span data-ttu-id="1aa98-211">**MakeAppx \[ opções \] de desempacotamento** **/p** *\<input bundle name\>* \**/d\*\*\*\<output directory\>*</span><span class="sxs-lookup"><span data-stu-id="1aa98-211">**MakeAppx unbundle \[options\]** **/p** *\<input bundle name\>* **/d** *\<output directory\>*</span></span>

<span data-ttu-id="1aa98-212">**MakeAppx \[ opções \] de criptografia** **/p** *\<input package name\>* \**/EP\*\*\*\<output package name\>*</span><span class="sxs-lookup"><span data-stu-id="1aa98-212">**MakeAppx encrypt \[options\]** **/p** *\<input package name\>* **/ep** *\<output package name\>*</span></span>

<span data-ttu-id="1aa98-213">**MakeAppx descriptografar \[ opções \]** **/p** *\<input package name\>* \**/EP\*\*\*\<output package name\>*</span><span class="sxs-lookup"><span data-stu-id="1aa98-213">**MakeAppx decrypt \[options\]** **/p** *\<input package name\>* **/ep** *\<output package name\>*</span></span>

## <a name="command-line-syntax"></a><span data-ttu-id="1aa98-214">Sintaxe da linha de comando</span><span class="sxs-lookup"><span data-stu-id="1aa98-214">Command-line Syntax</span></span>

<span data-ttu-id="1aa98-215">Aqui está a sintaxe de uso comum de linha de comando para MakeAppx.</span><span class="sxs-lookup"><span data-stu-id="1aa98-215">Here is the command-line common usage syntax for MakeAppx.</span></span>

<span data-ttu-id="1aa98-216">Pacote Unpack MakeAppx Pack do pacote desempacotar **\[ \| \| \| \| criptografar/ \| descriptografar \]** \[ **/h** **/KF** **/KT** **/l** **/o**  / **/NV** **/v** **/PFN** **/?**\]</span><span class="sxs-lookup"><span data-stu-id="1aa98-216">**MakeAppx \[pack\|unpack\|bundle\|unbundle\|encrypt\|decrypt\]** \[**/h** **/kf** **/kt** **/l** **/o** **/no** **/nv** **/v** **/pfn** **/?**\]</span></span>

<span data-ttu-id="1aa98-217">**MakeAppx** packs ou descompactam os arquivos em um pacote, agrupa ou desagrupa os pacotes em um pacote, ou criptografa ou descriptografa o pacote do aplicativo ou o grupo no diretório de entrada ou no arquivo de mapeamento especificado.</span><span class="sxs-lookup"><span data-stu-id="1aa98-217">**MakeAppx** packs or unpacks the files in a package, bundles or unbundles the packages in a bundle, or encrypts or decrypts the app package or bundle in the specified input directory or mapping file.</span></span> <span data-ttu-id="1aa98-218">Aqui está a lista de parâmetros que se aplicam ao **MakeAppx Pack**, **MakeAppx Unpack**, **MakeAppx Bundle**, **MakeAppx desagrupar**, **MakeAppx Encrypt** ou **MakeAppx Decrypt**.</span><span class="sxs-lookup"><span data-stu-id="1aa98-218">Here is the list of parameters that apply to **MakeAppx pack**, **MakeAppx unpack**, **MakeAppx bundle**, **MakeAppx unbundle**, **MakeAppx encrypt**, or **MakeAppx decrypt**.</span></span>

<dl> <dt>

<span data-ttu-id="1aa98-219"><span id="_l"></span><span id="_L"></span>**/l**</span><span class="sxs-lookup"><span data-stu-id="1aa98-219"><span id="_l"></span><span id="_L"></span>**/l**</span></span>
</dt> <dd>

<span data-ttu-id="1aa98-220">Essa opção é usada para pacotes localizados.</span><span class="sxs-lookup"><span data-stu-id="1aa98-220">This option is used for localized packages.</span></span> <span data-ttu-id="1aa98-221">A validação padrão é bloqueada em pacotes localizados.</span><span class="sxs-lookup"><span data-stu-id="1aa98-221">The default validation trips on localized packages.</span></span> <span data-ttu-id="1aa98-222">Essa opção desabilita apenas essa validação específica, sem a necessidade de que todas as validações sejam desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="1aa98-222">This option disables only that specific validation, without requiring that all validation be disabled.</span></span>

</dd> <dt>

<span data-ttu-id="1aa98-223"><span id="_o"></span><span id="_O"></span>**/o**</span><span class="sxs-lookup"><span data-stu-id="1aa98-223"><span id="_o"></span><span id="_O"></span>**/o**</span></span>
</dt> <dd>

<span data-ttu-id="1aa98-224">Substituir o arquivo de saída se ele existir.</span><span class="sxs-lookup"><span data-stu-id="1aa98-224">Overwrite the output file if it exists.</span></span> <span data-ttu-id="1aa98-225">Se você não especificar essa opção ou a opção **/** não, o usuário será perguntado se deseja substituir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="1aa98-225">If you don't specify this option or the **/no** option, the user is asked whether they want to overwrite the file.</span></span>

<span data-ttu-id="1aa98-226">Você não pode usar essa opção com **/**.</span><span class="sxs-lookup"><span data-stu-id="1aa98-226">You can't use this option with **/no**.</span></span>

</dd> <dt>

<span data-ttu-id="1aa98-227"><span id="_no"></span><span id="_NO"></span>**/**</span><span class="sxs-lookup"><span data-stu-id="1aa98-227"><span id="_no"></span><span id="_NO"></span>**/no**</span></span>
</dt> <dd>

<span data-ttu-id="1aa98-228">Impede uma substituição do arquivo de saída, se houver.</span><span class="sxs-lookup"><span data-stu-id="1aa98-228">Prevents an overwrite of the output file if it exists.</span></span> <span data-ttu-id="1aa98-229">Se você não especificar essa opção ou a opção **/o** , o usuário será perguntado se deseja substituir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="1aa98-229">If you don't specify this option or the **/o** option, the user is asked whether they want to overwrite the file.</span></span>

<span data-ttu-id="1aa98-230">Você não pode usar essa opção com **/o**.</span><span class="sxs-lookup"><span data-stu-id="1aa98-230">You can't use this option with **/o**.</span></span>

</dd> <dt>

<span data-ttu-id="1aa98-231"><span id="_nv"></span><span id="_NV"></span>**/nv**</span><span class="sxs-lookup"><span data-stu-id="1aa98-231"><span id="_nv"></span><span id="_NV"></span>**/nv**</span></span>
</dt> <dd>

<span data-ttu-id="1aa98-232">Ignore a validação semântica.</span><span class="sxs-lookup"><span data-stu-id="1aa98-232">Skip semantic validation.</span></span> <span data-ttu-id="1aa98-233">Se você não especificar essa opção, a ferramenta executará uma validação completa do pacote.</span><span class="sxs-lookup"><span data-stu-id="1aa98-233">If you don't specify this option, the tool performs a full validation of the package.</span></span>

</dd> <dt>

<span data-ttu-id="1aa98-234"><span id="_v"></span><span id="_V"></span>**/v**</span><span class="sxs-lookup"><span data-stu-id="1aa98-234"><span id="_v"></span><span id="_V"></span>**/v**</span></span>
</dt> <dd>

<span data-ttu-id="1aa98-235">Habilite a saída de log detalhado para o console.</span><span class="sxs-lookup"><span data-stu-id="1aa98-235">Enable verbose logging output to the console.</span></span>

</dd> <dt>

<span data-ttu-id="1aa98-236"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="1aa98-236"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="1aa98-237">Exibir texto de ajuda.</span><span class="sxs-lookup"><span data-stu-id="1aa98-237">Display help text.</span></span>

</dd> </dl>

<span data-ttu-id="1aa98-238">**MakeAppx Pack** , **MakeAppx Unpack** , **pacote de MakeAppx**, **MakeAppx desagrupar**, **MakeAppx Encrypt** e **MakeAppx Decrypt** são comandos mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="1aa98-238">**MakeAppx pack** , **MakeAppx unpack** , **MakeAppx bundle**, **MakeAppx unbundle**, **MakeAppx encrypt**, and **MakeAppx decrypt** are mutually exclusive commands.</span></span> <span data-ttu-id="1aa98-239">Estes são os parâmetros de linha de comando que se aplicam especificamente a cada comando:</span><span class="sxs-lookup"><span data-stu-id="1aa98-239">Here are the command-line parameters that apply specifically to each command:</span></span>

<span data-ttu-id="1aa98-240">**Pacote MakeAppx** \[ **h**\]</span><span class="sxs-lookup"><span data-stu-id="1aa98-240">**MakeAppx pack** \[**h**\]</span></span>

<span data-ttu-id="1aa98-241">Cria um pacote.</span><span class="sxs-lookup"><span data-stu-id="1aa98-241">Creates a package.</span></span>

<dl> <dt>

<span data-ttu-id="1aa98-242"><span id="_h_algorithm"></span><span id="_H_ALGORITHM"></span> *algoritmo* /h</span><span class="sxs-lookup"><span data-stu-id="1aa98-242"><span id="_h_algorithm"></span><span id="_H_ALGORITHM"></span>**/h** *algorithm*</span></span>
</dt> <dd>

<span data-ttu-id="1aa98-243">Especifica o algoritmo de hash a ser usado ao criar o mapa de blocos.</span><span class="sxs-lookup"><span data-stu-id="1aa98-243">Specifies the hash algorithm to use when creating the block map.</span></span> <span data-ttu-id="1aa98-244">Aqui estão os valores válidos para o *algoritmo*:</span><span class="sxs-lookup"><span data-stu-id="1aa98-244">Here are valid values for *algorithm*:</span></span>

<dl> <dd><span data-ttu-id="1aa98-245">SHA256 (padrão)</span><span class="sxs-lookup"><span data-stu-id="1aa98-245">SHA256 (default)</span></span></dd> <dd><span data-ttu-id="1aa98-246">SHA384</span><span class="sxs-lookup"><span data-stu-id="1aa98-246">SHA384</span></span></dd> <dd><span data-ttu-id="1aa98-247">SHA512</span><span class="sxs-lookup"><span data-stu-id="1aa98-247">SHA512</span></span></dd> </dl>

<span data-ttu-id="1aa98-248">Você não pode usar essa opção com o comando **Unpack** .</span><span class="sxs-lookup"><span data-stu-id="1aa98-248">You can't use this option with the **unpack** command.</span></span>

</dd> </dl>

<span data-ttu-id="1aa98-249">**Descompactar MakeAppx** \[ **PFN**\]</span><span class="sxs-lookup"><span data-stu-id="1aa98-249">**MakeAppx unpack** \[**pfn**\]</span></span>

<span data-ttu-id="1aa98-250">Extrai todos os arquivos do pacote especificado para o diretório de saída especificado.</span><span class="sxs-lookup"><span data-stu-id="1aa98-250">Extracts all files in the specified package to the specified output directory.</span></span> <span data-ttu-id="1aa98-251">A saída tem a mesma estrutura de diretório que o pacote.</span><span class="sxs-lookup"><span data-stu-id="1aa98-251">The output has the same directory structure as the package.</span></span>

<dl> <dt>

<span data-ttu-id="1aa98-252"><span id="_pfn"></span><span id="_PFN"></span>**/pfn**</span><span class="sxs-lookup"><span data-stu-id="1aa98-252"><span id="_pfn"></span><span id="_PFN"></span>**/pfn**</span></span>
</dt> <dd>

<span data-ttu-id="1aa98-253">Especifica um diretório chamado com o nome completo do pacote.</span><span class="sxs-lookup"><span data-stu-id="1aa98-253">Specifies a directory named with the package full name.</span></span> <span data-ttu-id="1aa98-254">Esse diretório é criado no local de saída fornecido.</span><span class="sxs-lookup"><span data-stu-id="1aa98-254">This directory is created under the provided output location.</span></span> <span data-ttu-id="1aa98-255">Você não pode usar essa opção com o comando **Pack** .</span><span class="sxs-lookup"><span data-stu-id="1aa98-255">You can't use this option with the **pack** command.</span></span>

</dd> </dl>

<span data-ttu-id="1aa98-256">**Desagrupar MakeAppx** \[ **PFN**\]</span><span class="sxs-lookup"><span data-stu-id="1aa98-256">**MakeAppx unbundle** \[**pfn**\]</span></span>

<span data-ttu-id="1aa98-257">Desempacota todos os pacotes em um subdiretório no caminho de saída especificado, nomeados após o nome completo do pacote.</span><span class="sxs-lookup"><span data-stu-id="1aa98-257">Unpacks all packages to a subdirectory under the specified output path, named after the bundle full name.</span></span> <span data-ttu-id="1aa98-258">A saída tem a mesma estrutura de diretório que o pacote de pacotes instalado.</span><span class="sxs-lookup"><span data-stu-id="1aa98-258">The output has the same directory structure as the installed package bundle.</span></span>

<dl> <dt>

<span data-ttu-id="1aa98-259"><span id="_pfn"></span><span id="_PFN"></span>**/pfn**</span><span class="sxs-lookup"><span data-stu-id="1aa98-259"><span id="_pfn"></span><span id="_PFN"></span>**/pfn**</span></span>
</dt> <dd>

<span data-ttu-id="1aa98-260">Especifica um diretório chamado com o nome completo do pacote de pacotes.</span><span class="sxs-lookup"><span data-stu-id="1aa98-260">Specifies a directory named with the package bundle full name.</span></span> <span data-ttu-id="1aa98-261">Esse diretório é criado no local de saída fornecido.</span><span class="sxs-lookup"><span data-stu-id="1aa98-261">This directory is created under the provided output location.</span></span> <span data-ttu-id="1aa98-262">Você não pode usar essa opção com o comando **Bundle** .</span><span class="sxs-lookup"><span data-stu-id="1aa98-262">You can't use this option with the **bundle** command.</span></span>

</dd> </dl>

<span data-ttu-id="1aa98-263">**MakeAppx criptografar** \[ **KF**, **KT**\]</span><span class="sxs-lookup"><span data-stu-id="1aa98-263">**MakeAppx encrypt** \[**kf**, **kt**\]</span></span>

<span data-ttu-id="1aa98-264">Cria um pacote de aplicativo criptografado do pacote do aplicativo de entrada especificado no pacote de saída especificado.</span><span class="sxs-lookup"><span data-stu-id="1aa98-264">Creates an encrypted app package from the specified input app package at the specified output package.</span></span>

<dl> <dt>

<span data-ttu-id="1aa98-265"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>\**/KF\*\*\*<key file>*</span><span class="sxs-lookup"><span data-stu-id="1aa98-265"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>**/kf** *<key file>*</span></span>
</dt> <dd>

<span data-ttu-id="1aa98-266">Criptografa o pacote ou grupo usando a chave do arquivo de chave especificado.</span><span class="sxs-lookup"><span data-stu-id="1aa98-266">Encrypts the package or bundle using the key from the specified key file.</span></span> <span data-ttu-id="1aa98-267">Você não pode usar essa opção com **KT**.</span><span class="sxs-lookup"><span data-stu-id="1aa98-267">You can't use this option with **kt**.</span></span>

</dd> <dt>

<span data-ttu-id="1aa98-268"><span id="_kt"></span><span id="_KT"></span>**/kt**</span><span class="sxs-lookup"><span data-stu-id="1aa98-268"><span id="_kt"></span><span id="_KT"></span>**/kt**</span></span>
</dt> <dd>

<span data-ttu-id="1aa98-269">Criptografa o pacote ou grupo usando a chave de teste global.</span><span class="sxs-lookup"><span data-stu-id="1aa98-269">Encrypts the package or bundle using the global test key.</span></span> <span data-ttu-id="1aa98-270">Você não pode usar essa opção com **KF**.</span><span class="sxs-lookup"><span data-stu-id="1aa98-270">You can't use this option with **kf**.</span></span>

</dd> </dl>

<span data-ttu-id="1aa98-271">**Descriptografar MakeAppx** \[ **KF**, **KT**\]</span><span class="sxs-lookup"><span data-stu-id="1aa98-271">**MakeAppx decrypt** \[**kf**, **kt**\]</span></span>

<span data-ttu-id="1aa98-272">Cria um pacote de aplicativo não criptografado do pacote do aplicativo de entrada especificado no pacote de saída especificado.</span><span class="sxs-lookup"><span data-stu-id="1aa98-272">Creates an unencrypted app package from the specified input app package at the specified output package.</span></span>

<dl> <dt>

<span data-ttu-id="1aa98-273"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>\**/KF\*\*\*<key file>*</span><span class="sxs-lookup"><span data-stu-id="1aa98-273"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>**/kf** *<key file>*</span></span>
</dt> <dd>

<span data-ttu-id="1aa98-274">Descriptografa o pacote ou grupo usando a chave do arquivo de chave especificado.</span><span class="sxs-lookup"><span data-stu-id="1aa98-274">Decrypts the package or bundle using the key from the specified key file.</span></span> <span data-ttu-id="1aa98-275">Você não pode usar essa opção com **KT**.</span><span class="sxs-lookup"><span data-stu-id="1aa98-275">You can't use this option with **kt**.</span></span>

</dd> <dt>

<span data-ttu-id="1aa98-276"><span id="_kt"></span><span id="_KT"></span>**/kt**</span><span class="sxs-lookup"><span data-stu-id="1aa98-276"><span id="_kt"></span><span id="_KT"></span>**/kt**</span></span>
</dt> <dd>

<span data-ttu-id="1aa98-277">Descriptografa o pacote ou grupo usando a chave de teste global.</span><span class="sxs-lookup"><span data-stu-id="1aa98-277">Decrypts the package or bundle using the global test key.</span></span> <span data-ttu-id="1aa98-278">Você não pode usar essa opção com **KF**.</span><span class="sxs-lookup"><span data-stu-id="1aa98-278">You can't use this option with **kf**.</span></span>

</dd> </dl>

## <a name="semantic-validation-performed-by-makeappx"></a><span data-ttu-id="1aa98-279">Validação semântica executada pelo MakeAppx</span><span class="sxs-lookup"><span data-stu-id="1aa98-279">Semantic validation performed by MakeAppx</span></span>

<span data-ttu-id="1aa98-280">O MakeAppx executa uma validação semântica limitada que é projetada para detectar os erros de implantação mais comuns e ajudar a garantir que o pacote do aplicativo seja válido.</span><span class="sxs-lookup"><span data-stu-id="1aa98-280">MakeAppx performs limited semantic validation that is designed to catch the most common deployment errors and help ensure that the app package is valid.</span></span>

<span data-ttu-id="1aa98-281">Essa validação garante que:</span><span class="sxs-lookup"><span data-stu-id="1aa98-281">This validation ensures that:</span></span>

-   <span data-ttu-id="1aa98-282">Todos os arquivos referenciados no manifesto do pacote sejam incluídos no pacote de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1aa98-282">All files referenced in the package manifest are included in the app package.</span></span>
-   <span data-ttu-id="1aa98-283">Um app não tenha duas chaves idênticas.</span><span class="sxs-lookup"><span data-stu-id="1aa98-283">An application does not have two identical keys.</span></span>
-   <span data-ttu-id="1aa98-284">Um aplicativo não se registra para um protocolo proibido desta lista: SMB, arquivo, MS-WWA-WEB, MS-WWA.</span><span class="sxs-lookup"><span data-stu-id="1aa98-284">An application does not register for a forbidden protocol from this list: SMB , FILE, MS-WWA-WEB, MS-WWA.</span></span>

<span data-ttu-id="1aa98-285">Essa validação semântica não está completa e não há garantia de que os pacotes criados pelo MakeAppx sejam instaláveis.</span><span class="sxs-lookup"><span data-stu-id="1aa98-285">This semantic validation is not complete, and packages built by MakeAppx are not guaranteed to be installable.</span></span>

 

 