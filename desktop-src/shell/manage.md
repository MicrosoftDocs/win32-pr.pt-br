---
description: O Shell fornece várias maneiras de gerenciar sistemas de arquivos.
ms.assetid: d9ffda6f-adc0-44a3-b410-e23bf5f4f165
title: Gerenciando o sistema de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0f3b47e17e691c540a9775f3b8588b311b9878
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581614"
---
# <a name="managing-the-file-system"></a><span data-ttu-id="77cd1-103">Gerenciando o sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="77cd1-103">Managing the File System</span></span>

<span data-ttu-id="77cd1-104">O Shell fornece várias maneiras de gerenciar sistemas de arquivos.</span><span class="sxs-lookup"><span data-stu-id="77cd1-104">The Shell provides a number of ways to manage file systems.</span></span> <span data-ttu-id="77cd1-105">O Shell fornece uma função, [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa), que permite que um aplicativo mova, copie, renomeie e exclua programaticamente arquivos.</span><span class="sxs-lookup"><span data-stu-id="77cd1-105">The Shell provides a function, [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa), that allows an application to programmatically move, copy, rename, and delete files.</span></span> <span data-ttu-id="77cd1-106">O Shell também dá suporte a alguns recursos adicionais de gerenciamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="77cd1-106">The Shell also supports some additional file management capabilities.</span></span>

-   <span data-ttu-id="77cd1-107">Documentos HTML podem ser *conectados* a arquivos relacionados, como arquivos gráficos ou folhas de estilo.</span><span class="sxs-lookup"><span data-stu-id="77cd1-107">HTML documents can be *connected* to related files, such as graphics files or style sheets.</span></span> <span data-ttu-id="77cd1-108">Quando o documento é movido ou copiado, os arquivos conectados também são movidos automaticamente ou copiados.</span><span class="sxs-lookup"><span data-stu-id="77cd1-108">When the document is moved or copied, the connected files are automatically moved or copied as well.</span></span>
-   <span data-ttu-id="77cd1-109">Para sistemas que estão disponíveis para mais de um usuário, os arquivos podem ser gerenciados por usuário.</span><span class="sxs-lookup"><span data-stu-id="77cd1-109">For systems that are available to more than one user, files can be managed on a per-user basis.</span></span> <span data-ttu-id="77cd1-110">Os usuários têm acesso fácil aos seus arquivos de dados, mas não aos arquivos que pertencem a outros usuários.</span><span class="sxs-lookup"><span data-stu-id="77cd1-110">Users have easy access to their data files, but not to files belonging to other users.</span></span>
-   <span data-ttu-id="77cd1-111">Se os arquivos de documento forem adicionados ou modificados, eles poderão ser adicionados à lista de documentos recentes do Shell.</span><span class="sxs-lookup"><span data-stu-id="77cd1-111">If document files are added or modified, they can be added to the Shell's list of recent documents.</span></span> <span data-ttu-id="77cd1-112">quando o usuário clica no comando **documentos** na menu Iniciar, uma lista de links para os documentos é exibida.</span><span class="sxs-lookup"><span data-stu-id="77cd1-112">When the user clicks the **Documents** command on the Start menu, a list of links to the documents appears.</span></span>

<span data-ttu-id="77cd1-113">Este documento discute como essas tecnologias de gerenciamento de arquivos funcionam.</span><span class="sxs-lookup"><span data-stu-id="77cd1-113">This document discusses how these file management technologies work.</span></span> <span data-ttu-id="77cd1-114">Em seguida, descreve como usar o Shell para mover, copiar, renomear e excluir arquivos e como gerenciar objetos na lixeira.</span><span class="sxs-lookup"><span data-stu-id="77cd1-114">It then outlines how to use the Shell to move, copy, rename, and delete files, and how to manage objects in the Recycle Bin.</span></span>

-   [<span data-ttu-id="77cd1-115">Gerenciamento de arquivos por usuário</span><span class="sxs-lookup"><span data-stu-id="77cd1-115">Per-User File Management</span></span>](#per-user-file-management)
-   [<span data-ttu-id="77cd1-116">Pastas meus documentos e minhas imagens</span><span class="sxs-lookup"><span data-stu-id="77cd1-116">My Documents and My Pictures Folders</span></span>](#my-documents-and-my-pictures-folders)
-   [<span data-ttu-id="77cd1-117">Arquivos conectados</span><span class="sxs-lookup"><span data-stu-id="77cd1-117">Connected Files</span></span>](#connected-files)
-   [<span data-ttu-id="77cd1-118">Movendo, copiando, renomeando e excluindo arquivos</span><span class="sxs-lookup"><span data-stu-id="77cd1-118">Moving, Copying, Renaming, and Deleting Files</span></span>](#moving-copying-renaming-and-deleting-files)
    -   [<span data-ttu-id="77cd1-119">Notificando o Shell</span><span class="sxs-lookup"><span data-stu-id="77cd1-119">Notifying the Shell</span></span>](#notifying-the-shell)
-   [<span data-ttu-id="77cd1-120">Exemplo simples de gerenciamento de arquivos com o SHFileOperation</span><span class="sxs-lookup"><span data-stu-id="77cd1-120">Simple Example of Managing Files with SHFileOperation</span></span>](#simple-example-of-managing-files-with-shfileoperation)
-   [<span data-ttu-id="77cd1-121">Adicionando arquivos à lista de documentos recentes do Shell</span><span class="sxs-lookup"><span data-stu-id="77cd1-121">Adding Files to the Shell's List of Recent Documents</span></span>](#adding-files-to-the-shells-list-of-recent-documents)

## <a name="per-user-file-management"></a><span data-ttu-id="77cd1-122">Gerenciamento de arquivos Per-User</span><span class="sxs-lookup"><span data-stu-id="77cd1-122">Per-User File Management</span></span>

<span data-ttu-id="77cd1-123">o Windows Shell 2000 permite que os arquivos sejam associados a um usuário específico para que os arquivos permaneçam ocultos de outros usuários.</span><span class="sxs-lookup"><span data-stu-id="77cd1-123">The Windows 2000 Shell allows files to be associated with a particular user so the files remain hidden from other users.</span></span> <span data-ttu-id="77cd1-124">em termos do sistema de arquivos, os arquivos são armazenados na pasta de perfil do usuário, normalmente C: \\ documents e Configurações \\ *nome de usuário* \\ em sistemas Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="77cd1-124">In terms of the file system, the files are stored under the user's profile folder, typically C:\\Documents and Settings\\*Username*\\ on Windows 2000 systems.</span></span> <span data-ttu-id="77cd1-125">Esse recurso permite que muitos indivíduos usem o mesmo computador, mantendo a privacidade de seus arquivos de outros usuários.</span><span class="sxs-lookup"><span data-stu-id="77cd1-125">This feature allows many individuals to use the same computer, while maintaining the privacy of their files from other users.</span></span> <span data-ttu-id="77cd1-126">Diferentes usuários podem ter programas diferentes disponíveis.</span><span class="sxs-lookup"><span data-stu-id="77cd1-126">Different users can have different programs available.</span></span> <span data-ttu-id="77cd1-127">Ele também fornece uma maneira simples para os administradores e aplicativos armazenarem coisas como arquivos de inicialização (.ini) ou link (. lnk).</span><span class="sxs-lookup"><span data-stu-id="77cd1-127">It also provides a straightforward way for administrators and applications to store such things as initialization (.ini) or link (.lnk) files.</span></span> <span data-ttu-id="77cd1-128">Assim, os aplicativos podem preservar um estado diferente para cada usuário e recuperar facilmente esse estado em particular quando necessário.</span><span class="sxs-lookup"><span data-stu-id="77cd1-128">Applications can thus preserve a different state for each user and easily recover that particular state when needed.</span></span> <span data-ttu-id="77cd1-129">Também há uma pasta de perfil para armazenar informações comuns a todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="77cd1-129">There is also a profile folder for storing information that is common to all users.</span></span>

<span data-ttu-id="77cd1-130">Como é inconveniente determinar qual usuário está conectado e onde seus arquivos estão localizados, as pastas padrão por usuário são pastas especiais e são identificadas por uma [**CSIDL**](csidl.md).</span><span class="sxs-lookup"><span data-stu-id="77cd1-130">Because it is inconvenient to determine which user is logged in and where their files are located, the standard per-user folders are special folders and are identified by a [**CSIDL**](csidl.md).</span></span> <span data-ttu-id="77cd1-131">Por exemplo, a CSIDl para a pasta arquivos de programas por usuário são os programas CSIDl \_ .</span><span class="sxs-lookup"><span data-stu-id="77cd1-131">For instance, the CSIDL for the per-user Program Files folder is CSIDL\_PROGRAMS.</span></span> <span data-ttu-id="77cd1-132">Se seu aplicativo chamar [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) ou [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) com um dos CSIDLs por usuário, a função retornará o ponteiro para uma PIDL (lista de identificadores de item) ou caminho apropriado para o usuário conectado no momento.</span><span class="sxs-lookup"><span data-stu-id="77cd1-132">If your application calls [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) or [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) with one of the per-user CSIDLs, the function returns the pointer to an item identifier list (PIDL) or path appropriate to the currently logged-in user.</span></span> <span data-ttu-id="77cd1-133">Se seu aplicativo precisar recuperar o caminho ou PIDL da pasta de perfil, seu CSIDl será o **\_ perfil CSIDL**.</span><span class="sxs-lookup"><span data-stu-id="77cd1-133">If your application needs to retrieve the path or PIDL of the profile folder, its CSIDL is **CSIDL\_PROFILE**.</span></span>

## <a name="my-documents-and-my-pictures-folders"></a><span data-ttu-id="77cd1-134">Pastas meus documentos e minhas imagens</span><span class="sxs-lookup"><span data-stu-id="77cd1-134">My Documents and My Pictures Folders</span></span>

<span data-ttu-id="77cd1-135">Um dos ícones padrão encontrados na área de trabalho é **meus documentos**.</span><span class="sxs-lookup"><span data-stu-id="77cd1-135">One of the standard icons found on the desktop is **My Documents**.</span></span> <span data-ttu-id="77cd1-136">Quando você abre essa pasta, ela contém os arquivos de documento atuais do usuário.</span><span class="sxs-lookup"><span data-stu-id="77cd1-136">When you open this folder, it contains the current user's document files.</span></span> <span data-ttu-id="77cd1-137">A instância de área de trabalho de meus documentos é uma pasta virtual — um alias para o local do sistema de arquivos usado para armazenar fisicamente os documentos do usuário — localizado imediatamente abaixo da área de trabalho na hierarquia de namespace.</span><span class="sxs-lookup"><span data-stu-id="77cd1-137">The desktop instance of My Documents is a virtual folder—an alias to the file system location used to physically store the user's documents—located immediately below the desktop in the namespace hierarchy.</span></span>

<span data-ttu-id="77cd1-138">A finalidade das pastas meus documentos e minhas imagens é fornecer uma maneira direta e segura para que os usuários acessem seus arquivos de documento e imagem em um sistema que possa ter vários usuários.</span><span class="sxs-lookup"><span data-stu-id="77cd1-138">The purpose of the My Documents and My Pictures folders is to provide a straightforward and secure way for users to access their document and picture files on a system that might have multiple users.</span></span> <span data-ttu-id="77cd1-139">Cada usuário recebe pastas separadas do sistema de arquivos para seus arquivos.</span><span class="sxs-lookup"><span data-stu-id="77cd1-139">Each user is assigned separate file system folders for his or her files.</span></span> <span data-ttu-id="77cd1-140">por exemplo, o local da pasta documentos de um usuário no sistema de arquivos normalmente é algo como C: \\ documents e Configurações \\ *nome de usuário* \\ My documents.</span><span class="sxs-lookup"><span data-stu-id="77cd1-140">For example, the location of a user's documents folder in the file system is typically something like C:\\Documents and Settings\\*username*\\My Documents.</span></span> <span data-ttu-id="77cd1-141">Não há necessidade de que os usuários saibam nada sobre o local físico de suas pastas do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="77cd1-141">There is no need for users to know anything about the physical location of their file system folders.</span></span> <span data-ttu-id="77cd1-142">Eles simplesmente acessam seus arquivos por meio do ícone meus documentos.</span><span class="sxs-lookup"><span data-stu-id="77cd1-142">They simply access their files through the My Documents icon.</span></span>

> [!Note]  
> <span data-ttu-id="77cd1-143">Meus documentos permite que um usuário acesse seus próprios arquivos, mas não aqueles de qualquer outro usuário.</span><span class="sxs-lookup"><span data-stu-id="77cd1-143">My Documents allows a user to access his or her own files but not those of any other user.</span></span> <span data-ttu-id="77cd1-144">Se vários indivíduos usarem o mesmo computador, um administrador poderá bloquear os usuários fora da parte do sistema de arquivos onde os arquivos reais estão armazenados.</span><span class="sxs-lookup"><span data-stu-id="77cd1-144">If multiple individuals use the same computer, an administrator can lock users out of the part of the file system where the actual files are stored.</span></span> <span data-ttu-id="77cd1-145">Portanto, os usuários poderão trabalhar em seus próprios documentos por meio da pasta meus documentos, mas não em documentos que pertençam a outros usuários.</span><span class="sxs-lookup"><span data-stu-id="77cd1-145">Users will thus be able to work on their own documents through the My Documents folder but not on documents that belong to any other users.</span></span>

 

<span data-ttu-id="77cd1-146">Normalmente, não há necessidade de que um aplicativo saiba qual usuário está conectado ou no sistema de arquivos em que a pasta meus documentos do usuário está localizada.</span><span class="sxs-lookup"><span data-stu-id="77cd1-146">There is usually no need for an application to know which user is logged in or where in the file system that user's My Documents folder is located.</span></span> <span data-ttu-id="77cd1-147">Em vez disso, seu aplicativo pode recuperar o PIDL do ícone meus documentos na área de trabalho chamando o método IShellFolder da área de trabalho [**::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) .</span><span class="sxs-lookup"><span data-stu-id="77cd1-147">Instead, your application can retrieve the PIDL of the My Documents desktop icon by calling the desktop's [**IShellFolder::ParseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) method.</span></span> <span data-ttu-id="77cd1-148">O nome de análise usado para identificar a pasta meus documentos não é um caminho de arquivo, mas sim: {450d8fba-ad25-11D0-98a8-0800361b1103}.</span><span class="sxs-lookup"><span data-stu-id="77cd1-148">The parsing name used to identify the My Documents folder is not a file path but rather ::{450d8fba-ad25-11d0-98a8-0800361b1103}.</span></span> <span data-ttu-id="77cd1-149">A expressão entre colchetes é a forma de texto do GUID meus documentos.</span><span class="sxs-lookup"><span data-stu-id="77cd1-149">The bracketed expression is the text form of the My Documents GUID.</span></span> <span data-ttu-id="77cd1-150">Por exemplo, para recuperar o PIDL de meus documentos, seu aplicativo deve usar essa chamada para **IShellFolder::P arsedisplayname**.</span><span class="sxs-lookup"><span data-stu-id="77cd1-150">For example, to retrieve the PIDL of My Documents, your application should use this call to **IShellFolder::ParseDisplayName**.</span></span>


```C++
hr = psfDeskTop->ParseDisplayName(NULL, 
                                  NULL, 
                                  L"::{450d8fba-ad25-11d0-98a8-0800361b1103}", 
                                  &chEaten, 
                                  &pidlDocFiles, 
                                  NULL);
```



<span data-ttu-id="77cd1-151">Depois que o aplicativo tiver os meus documentos PIDL, ele poderá manipular a pasta da mesma forma que faria com uma pasta normal do sistema de arquivos, enumerando itens, analisando, vinculando e executando qualquer outra operação de pasta válida.</span><span class="sxs-lookup"><span data-stu-id="77cd1-151">Once your application has the My Documents PIDL, it can handle the folder just as it would a normal file system folder—enumerating items, parsing, binding, and performing any other valid folder operations.</span></span> <span data-ttu-id="77cd1-152">O Shell mapeia automaticamente as alterações em meus documentos ou em suas subpastas nas pastas apropriadas do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="77cd1-152">The Shell automatically maps changes in My Documents or its subfolders to the appropriate file system folders.</span></span>

<span data-ttu-id="77cd1-153">Se seu aplicativo precisar de acesso à pasta do sistema de arquivos real que contém os documentos do usuário atual, passe CSIDl \_ pessoal para [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation).</span><span class="sxs-lookup"><span data-stu-id="77cd1-153">If your application needs access to the actual file system folder that contains the current user's documents, pass CSIDL\_PERSONAL to [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation).</span></span> <span data-ttu-id="77cd1-154">A função retorna o PIDL da pasta do sistema de arquivos que é exibida na pasta meus documentos do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="77cd1-154">The function returns the PIDL of the file system folder that is displayed in the current user's My Documents folder.</span></span>

## <a name="connected-files"></a><span data-ttu-id="77cd1-155">Arquivos conectados</span><span class="sxs-lookup"><span data-stu-id="77cd1-155">Connected Files</span></span>

<span data-ttu-id="77cd1-156">documentos HTML geralmente têm um número de arquivos gráficos associados, um arquivo de folha de estilos, vários arquivos do Microsoft JScript (compatíveis com a especificação de linguagem ECMA 262) e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="77cd1-156">HTML documents often have a number of associated graphics files, a style sheet file, several Microsoft JScript (compatible with ECMA 262 language specification ) files, and so on.</span></span> <span data-ttu-id="77cd1-157">Ao mover ou copiar o documento HTML primário, normalmente, você também deseja mover ou copiar seus arquivos associados para evitar a interrupção dos links.</span><span class="sxs-lookup"><span data-stu-id="77cd1-157">When you move or copy the primary HTML document, you also usually want to move or copy its associated files to avoid breaking links.</span></span> <span data-ttu-id="77cd1-158">Infelizmente, não houve uma maneira fácil até agora determinar quais arquivos estão relacionados a qualquer documento HTML específico, a não ser pela análise de seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="77cd1-158">Unfortunately, there has been no easy way until now to determine which files are related to any given HTML document other than by analyzing their contents.</span></span> <span data-ttu-id="77cd1-159">para aliviar esse problema, Windows 2000 fornece uma maneira simples de *conectar* um documento HTML primário ao seu grupo de arquivos associados.</span><span class="sxs-lookup"><span data-stu-id="77cd1-159">To alleviate this problem, Windows 2000 provides a simple way to *connect* a primary HTML document to its group of associated files.</span></span> <span data-ttu-id="77cd1-160">Se a conexão de arquivo estiver habilitada, quando o documento for movido ou copiado, todos os seus arquivos conectados irão para ele.</span><span class="sxs-lookup"><span data-stu-id="77cd1-160">If file connection is enabled, when the document is moved or copied all its connected files go with it.</span></span>

<span data-ttu-id="77cd1-161">Para criar um grupo de arquivos conectados, o documento primário deve ter uma extensão de nome de arquivo .htm ou .html.</span><span class="sxs-lookup"><span data-stu-id="77cd1-161">To create a group of connected files, the primary document must have an .htm or .html file name extension.</span></span> <span data-ttu-id="77cd1-162">Crie uma subpasta da pasta pai do documento primário.</span><span class="sxs-lookup"><span data-stu-id="77cd1-162">Create a subfolder of the primary document's parent folder.</span></span> <span data-ttu-id="77cd1-163">O nome da subpasta deve ser o nome do documento primário, menos a .htm ou .html extensão, seguido de uma das extensões listadas abaixo.</span><span class="sxs-lookup"><span data-stu-id="77cd1-163">The subfolder's name must be the name of the primary document, minus the .htm or .html extension, followed by one of the extensions listed below.</span></span> <span data-ttu-id="77cd1-164">As extensões usadas com mais frequência são ". Files" ou " \_ Files".</span><span class="sxs-lookup"><span data-stu-id="77cd1-164">The most commonly used extensions are ".files" or "\_files".</span></span> <span data-ttu-id="77cd1-165">Por exemplo, se o documento primário for denominado MyDoc.htm, nomear a subpasta " \_ arquivos MyDoc" definirá a subpasta como o contêiner para os arquivos conectados do documento.</span><span class="sxs-lookup"><span data-stu-id="77cd1-165">For instance, if the primary document is named MyDoc.htm, naming the subfolder "MyDoc\_files" defines the subfolder as the container for the document's connected files.</span></span> <span data-ttu-id="77cd1-166">Se o documento primário for movido ou copiado, a subpasta e seus arquivos também serão movidos ou copiados.</span><span class="sxs-lookup"><span data-stu-id="77cd1-166">If the primary document is moved or copied, the subfolder and its files are moved or copied as well.</span></span>

<span data-ttu-id="77cd1-167">Para alguns idiomas, é possível usar um equivalente localizado de " \_ arquivos" para criar uma subpasta para arquivos conectados.</span><span class="sxs-lookup"><span data-stu-id="77cd1-167">For some languages, it is possible to use a localized equivalent of "\_files" to create a subfolder for connected files.</span></span> <span data-ttu-id="77cd1-168">A tabela a seguir lista as cadeias de caracteres válidas que podem ser acrescentadas a um nome de documento para criar uma subpasta arquivos conectados.</span><span class="sxs-lookup"><span data-stu-id="77cd1-168">The following table lists the valid strings that can be appended to a document name to create a connected files subfolder.</span></span> <span data-ttu-id="77cd1-169">Observe que algumas dessas cadeias de caracteres têm '-' como seu primeiro caractere em vez de ' \_ ' ou '. '.</span><span class="sxs-lookup"><span data-stu-id="77cd1-169">Note that some of these strings have '-' as their first character rather than '\_' or '.'.</span></span>



:::row:::
   :::column span="":::
      <span data-ttu-id="77cd1-170">" \_ archivos"</span><span class="sxs-lookup"><span data-stu-id="77cd1-170">"\_archivos"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="77cd1-171">" \_ arquivos"</span><span class="sxs-lookup"><span data-stu-id="77cd1-171">"\_arquivos"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="77cd1-172">" \_ befique"</span><span class="sxs-lookup"><span data-stu-id="77cd1-172">"\_bestanden"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="77cd1-173">" \_ bylos"</span><span class="sxs-lookup"><span data-stu-id="77cd1-173">"\_bylos"</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="77cd1-174">"-Dateien"</span><span class="sxs-lookup"><span data-stu-id="77cd1-174">"-Dateien"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="77cd1-175">" \_ datoteke"</span><span class="sxs-lookup"><span data-stu-id="77cd1-175">"\_datoteke"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="77cd1-176">" \_ dosyalar"</span><span class="sxs-lookup"><span data-stu-id="77cd1-176">"\_dosyalar"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="77cd1-177">" \_ elemei"</span><span class="sxs-lookup"><span data-stu-id="77cd1-177">"\_elemei"</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="77cd1-178">" \_ failid"</span><span class="sxs-lookup"><span data-stu-id="77cd1-178">"\_failid"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="77cd1-179">" \_ falha"</span><span class="sxs-lookup"><span data-stu-id="77cd1-179">"\_fails"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="77cd1-180">" \_ fajlovi"</span><span class="sxs-lookup"><span data-stu-id="77cd1-180">"\_fajlovi"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="77cd1-181">" \_ ficheiros"</span><span class="sxs-lookup"><span data-stu-id="77cd1-181">"\_ficheiros"</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="77cd1-182">" \_ fichiers"</span><span class="sxs-lookup"><span data-stu-id="77cd1-182">"\_fichiers"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="77cd1-183">"-Filer"</span><span class="sxs-lookup"><span data-stu-id="77cd1-183">"-filer"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="77cd1-184">". Files"</span><span class="sxs-lookup"><span data-stu-id="77cd1-184">".files"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="77cd1-185">" \_ arquivos"</span><span class="sxs-lookup"><span data-stu-id="77cd1-185">"\_files"</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="77cd1-186">" \_ arquivo"</span><span class="sxs-lookup"><span data-stu-id="77cd1-186">"\_file"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="77cd1-187">" \_ fitxers"</span><span class="sxs-lookup"><span data-stu-id="77cd1-187">"\_fitxers"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="77cd1-188">" \_ fitxategiak"</span><span class="sxs-lookup"><span data-stu-id="77cd1-188">"\_fitxategiak"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="77cd1-189">" \_ pliki"</span><span class="sxs-lookup"><span data-stu-id="77cd1-189">"\_pliki"</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="77cd1-190">" \_ soubory"</span><span class="sxs-lookup"><span data-stu-id="77cd1-190">"\_soubory"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="77cd1-191">" \_ tiedostot"</span><span class="sxs-lookup"><span data-stu-id="77cd1-191">"\_tiedostot"</span></span>
   :::column-end:::
   :::column span="":::
   :::column-end:::
   :::column span="":::
   :::column-end:::
:::row-end:::



 

> [!Note]  
> <span data-ttu-id="77cd1-192">Esse recurso é sensível ao caso da extensão.</span><span class="sxs-lookup"><span data-stu-id="77cd1-192">This feature is sensitive to the case of the extension.</span></span> <span data-ttu-id="77cd1-193">Por exemplo, para os exemplos fornecidos acima, uma subpasta denominada " \_ arquivos MyDoc" não será conectada a MyDoc.htm.</span><span class="sxs-lookup"><span data-stu-id="77cd1-193">For instance, for the example given above, a subfolder named "MyDoc\_Files" will not be connected to MyDoc.htm.</span></span>

 

<span data-ttu-id="77cd1-194">Se a conexão de arquivo está habilitada ou desabilitada é controlada por um valor **reg \_ DWORD** , NoFileFolderConnection, da seguinte chave do registro.</span><span class="sxs-lookup"><span data-stu-id="77cd1-194">Whether file connection is enabled or disabled is controlled by a **REG\_DWORD** value, NoFileFolderConnection, of the following registry key.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
```

<span data-ttu-id="77cd1-195">Esse valor normalmente não está definido e a conexão do arquivo está habilitada.</span><span class="sxs-lookup"><span data-stu-id="77cd1-195">This value normally is not defined, and file connection is enabled.</span></span> <span data-ttu-id="77cd1-196">Se necessário, você pode desabilitar a conexão de arquivo adicionando esse valor à chave e definindo-o como 1.</span><span class="sxs-lookup"><span data-stu-id="77cd1-196">If necessary, you can disable file connection by adding this value to the key and setting it to 1.</span></span> <span data-ttu-id="77cd1-197">Para habilitar a conexão de arquivo novamente, defina NoFileFolderConnection como zero.</span><span class="sxs-lookup"><span data-stu-id="77cd1-197">To enable file connection again, set NoFileFolderConnection to zero.</span></span>

> [!Note]  
> <span data-ttu-id="77cd1-198">A conexão de arquivo normalmente deve ser habilitada porque outros aplicativos podem depender dela.</span><span class="sxs-lookup"><span data-stu-id="77cd1-198">File connection should normally be enabled because other applications might depend on it.</span></span> <span data-ttu-id="77cd1-199">Desabilite a conexão de arquivos somente se for absolutamente necessário.</span><span class="sxs-lookup"><span data-stu-id="77cd1-199">Disable file connection only if absolutely necessary.</span></span>

 

## <a name="moving-copying-renaming-and-deleting-files"></a><span data-ttu-id="77cd1-200">Movendo, copiando, renomeando e excluindo arquivos</span><span class="sxs-lookup"><span data-stu-id="77cd1-200">Moving, Copying, Renaming, and Deleting Files</span></span>

<span data-ttu-id="77cd1-201">O namespace não é estático e normalmente os aplicativos precisam gerenciar o sistema de arquivos executando uma das seguintes operações.</span><span class="sxs-lookup"><span data-stu-id="77cd1-201">The namespace is not static, and applications commonly need to manage the file system by performing one of the following operations.</span></span>

-   <span data-ttu-id="77cd1-202">Copiando um objeto para outra pasta.</span><span class="sxs-lookup"><span data-stu-id="77cd1-202">Copying an object to another folder.</span></span>
-   <span data-ttu-id="77cd1-203">Movendo um objeto para outra pasta.</span><span class="sxs-lookup"><span data-stu-id="77cd1-203">Moving an object to another folder.</span></span>
-   <span data-ttu-id="77cd1-204">Excluindo um objeto.</span><span class="sxs-lookup"><span data-stu-id="77cd1-204">Deleting an object.</span></span>
-   <span data-ttu-id="77cd1-205">Renomeando um objeto.</span><span class="sxs-lookup"><span data-stu-id="77cd1-205">Renaming an object.</span></span>

<span data-ttu-id="77cd1-206">Todas essas operações são executadas com [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa).</span><span class="sxs-lookup"><span data-stu-id="77cd1-206">These operations are all performed with [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa).</span></span> <span data-ttu-id="77cd1-207">Essa função usa um ou mais arquivos de origem e produz arquivos de destino correspondentes.</span><span class="sxs-lookup"><span data-stu-id="77cd1-207">This function takes one or more source files and produces corresponding destination files.</span></span> <span data-ttu-id="77cd1-208">No caso da operação de exclusão, o sistema tenta colocar os arquivos excluídos na lixeira.</span><span class="sxs-lookup"><span data-stu-id="77cd1-208">In the case of the delete operation, the system attempts to put the deleted files into the Recycle Bin.</span></span>

<span data-ttu-id="77cd1-209">Também é possível mover arquivos usando a funcionalidade de [arrastar e soltar](dragdrop.md) .</span><span class="sxs-lookup"><span data-stu-id="77cd1-209">It is also possible to move files using the [drag-and-drop](dragdrop.md) functionality.</span></span>

<span data-ttu-id="77cd1-210">Para usar a função, você deve preencher os membros de uma estrutura [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) e passá-la para [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa).</span><span class="sxs-lookup"><span data-stu-id="77cd1-210">To use the function, you must fill in the members of an [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) structure and pass it to [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa).</span></span> <span data-ttu-id="77cd1-211">Os principais membros da estrutura são **pFrom** e **PTO**.</span><span class="sxs-lookup"><span data-stu-id="77cd1-211">The key members of the structure are **pFrom** and **pTo**.</span></span>

<span data-ttu-id="77cd1-212">O membro **pFrom** é uma cadeia de caracteres dupla terminada com **nulo** que contém um ou mais nomes de arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="77cd1-212">The **pFrom** member is a double **null**-terminated string that contains one or more source file names.</span></span> <span data-ttu-id="77cd1-213">Esses nomes podem ser caminhos totalmente qualificados ou curingas de DOS padrão, como \* . \* .</span><span class="sxs-lookup"><span data-stu-id="77cd1-213">These names can be either fully qualified paths or standard DOS wildcards such as \*.\*.</span></span> <span data-ttu-id="77cd1-214">Embora esse membro seja declarado como uma cadeia de caracteres terminada em **nulo**, ele é usado como um buffer para manter vários nomes de arquivo.</span><span class="sxs-lookup"><span data-stu-id="77cd1-214">Although this member is declared as a **null**-terminated string, it is used as a buffer to hold multiple file names.</span></span> <span data-ttu-id="77cd1-215">Cada nome de arquivo deve ser terminado pelo caractere **nulo** único usual.</span><span class="sxs-lookup"><span data-stu-id="77cd1-215">Each file name must be terminated by the usual single **NULL** character.</span></span> <span data-ttu-id="77cd1-216">Um caractere **nulo** adicional deve ser acrescentado ao final do nome final para indicar o fim de **pFrom**.</span><span class="sxs-lookup"><span data-stu-id="77cd1-216">An additional **NULL** character must be appended to the end of the final name to indicate the end of **pFrom**.</span></span>

<span data-ttu-id="77cd1-217">O membro **PTO** é uma cadeia de caracteres dupla terminada com **nulo**, muito parecida com **pFrom**.</span><span class="sxs-lookup"><span data-stu-id="77cd1-217">The **pTo** member is a double **null**-terminated string, much like **pFrom**.</span></span> <span data-ttu-id="77cd1-218">O membro **PTO** contém os nomes de um ou mais nomes de destino totalmente qualificados.</span><span class="sxs-lookup"><span data-stu-id="77cd1-218">The **pTo** member contains the names of one or more fully qualified destination names.</span></span> <span data-ttu-id="77cd1-219">Eles são incluídos em **PTO** da mesma forma que são para o **pFrom**.</span><span class="sxs-lookup"><span data-stu-id="77cd1-219">They are packed into **pTo** in the same way as they are for **pFrom**.</span></span> <span data-ttu-id="77cd1-220">Se **PTO** contiver vários nomes, você também deverá definir o sinalizador **fof \_ MULTIDESTFILES** no membro **fFlags** .</span><span class="sxs-lookup"><span data-stu-id="77cd1-220">If **pTo** contains multiple names, you must also set the **FOF\_MULTIDESTFILES** flag in the **fFlags** member.</span></span> <span data-ttu-id="77cd1-221">O uso de **PTO** depende da operação, conforme descrito aqui.</span><span class="sxs-lookup"><span data-stu-id="77cd1-221">The usage of **pTo** depends on the operation as described here.</span></span>

-   <span data-ttu-id="77cd1-222">Para operações de cópia e movimentação, se todos os arquivos estiverem indo para um único diretório, **PTO** conterá o nome do diretório totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="77cd1-222">For copy and move operations, if all the files are going to a single directory, **pTo** contains the fully qualified directory name.</span></span> <span data-ttu-id="77cd1-223">Se os arquivos estiverem em destinos diferentes, **PTO** também poderá conter um diretório totalmente qualificado ou nome de arquivo para cada arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="77cd1-223">If the files are going to different destinations, **pTo** can also contain one fully qualified directory or file name for each source file.</span></span> <span data-ttu-id="77cd1-224">Se um diretório não existir, o sistema o criará.</span><span class="sxs-lookup"><span data-stu-id="77cd1-224">If a directory does not exist, the system creates it.</span></span>
-   <span data-ttu-id="77cd1-225">Para operações de renomeação, **PTO** contém um caminho totalmente qualificado para cada arquivo de origem em **pFrom**.</span><span class="sxs-lookup"><span data-stu-id="77cd1-225">For rename operations, **pTo** contains one fully qualified path for each source file in **pFrom**.</span></span>
-   <span data-ttu-id="77cd1-226">Para operações de exclusão, **PTO** não é usado.</span><span class="sxs-lookup"><span data-stu-id="77cd1-226">For delete operations, **pTo** is not used.</span></span>

### <a name="notifying-the-shell"></a><span data-ttu-id="77cd1-227">Notificando o Shell</span><span class="sxs-lookup"><span data-stu-id="77cd1-227">Notifying the Shell</span></span>

<span data-ttu-id="77cd1-228">Notifique o Shell da alteração depois de usar o [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) para mover, copiar, renomear ou excluir arquivos, ou depois de realizar qualquer outra ação que afete o namespace.</span><span class="sxs-lookup"><span data-stu-id="77cd1-228">Notify the Shell of the change after using [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) to move, copy, rename, or delete files, or after taking any other action that affects the namespace.</span></span> <span data-ttu-id="77cd1-229">As ações que devem ser acompanhadas por notificação incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="77cd1-229">Actions that should be accompanied by notification include the following:</span></span>

-   <span data-ttu-id="77cd1-230">Adicionando ou excluindo arquivos ou pastas.</span><span class="sxs-lookup"><span data-stu-id="77cd1-230">Adding or deleting files or folders.</span></span>
-   <span data-ttu-id="77cd1-231">Mover, copiar ou renomear arquivos ou pastas.</span><span class="sxs-lookup"><span data-stu-id="77cd1-231">Moving, copying, or renaming files or folders.</span></span>
-   <span data-ttu-id="77cd1-232">Alteração de uma associação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="77cd1-232">Changing a file association.</span></span>
-   <span data-ttu-id="77cd1-233">Alterando atributos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="77cd1-233">Changing file attributes.</span></span>
-   <span data-ttu-id="77cd1-234">Adicionar ou remover unidades ou mídia de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="77cd1-234">Adding or removing drives or storage media.</span></span>
-   <span data-ttu-id="77cd1-235">Criando ou desabilitando uma pasta compartilhada.</span><span class="sxs-lookup"><span data-stu-id="77cd1-235">Creating or disabling a shared folder.</span></span>
-   <span data-ttu-id="77cd1-236">Alterando a lista de imagens do sistema.</span><span class="sxs-lookup"><span data-stu-id="77cd1-236">Changing the system image list.</span></span>

<span data-ttu-id="77cd1-237">Um aplicativo notifica o Shell chamando [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) com os detalhes do que mudou.</span><span class="sxs-lookup"><span data-stu-id="77cd1-237">An application notifies the Shell by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) with the details of what has changed.</span></span> <span data-ttu-id="77cd1-238">O Shell pode então atualizar sua imagem do namespace para refletir com precisão seu novo estado.</span><span class="sxs-lookup"><span data-stu-id="77cd1-238">The Shell can then update its image of the namespace to accurately reflect its new state.</span></span>

## <a name="simple-example-of-managing-files-with-shfileoperation"></a><span data-ttu-id="77cd1-239">Exemplo simples de gerenciamento de arquivos com o SHFileOperation</span><span class="sxs-lookup"><span data-stu-id="77cd1-239">Simple Example of Managing Files with SHFileOperation</span></span>

<span data-ttu-id="77cd1-240">O exemplo de aplicativo de console a seguir ilustra o uso de [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) para copiar arquivos de um diretório para outro.</span><span class="sxs-lookup"><span data-stu-id="77cd1-240">The following sample console application illustrates the use of [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) to copy files from one directory to another.</span></span> <span data-ttu-id="77cd1-241">Os diretórios de origem e de destino, C: \\ My \_ docs e C: \\ My \_ Docs2, são embutidos em código no aplicativo para simplificar a simplicidade.</span><span class="sxs-lookup"><span data-stu-id="77cd1-241">The source and destination directories, C:\\My\_Docs and C:\\My\_Docs2, are hard-coded into the application for simplicity.</span></span>


```C++
#include <shlobj.h>
#include <shlwapi.h>
#include <strsafe.h>

int main(void)
{
    IShellFolder *psfDeskTop = NULL;
    IShellFolder *psfDocFiles = NULL;
    LPITEMIDLIST pidlDocFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IEnumIDList *ppenum = NULL;
    SHFILEOPSTRUCT sfo;
    STRRET strDispName;
    TCHAR szParseName[MAX_PATH];
    TCHAR szSourceFiles[256];
    int i;
    int iBufPos = 0;
    ULONG chEaten;
    ULONG celtFetched;
    size_t ParseNameSize = 0;
    HRESULT hr;
    

    szSourceFiles[0] = '\0';
    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->ParseDisplayName(NULL, NULL, L"c:\\My_Docs", 
         &chEaten, &pidlDocFiles, NULL);
    hr = psfDeskTop->BindToObject(pidlDocFiles, NULL, IID_IShellFolder, 
         (LPVOID *) &psfDocFiles);
    hr = psfDeskTop->Release();

    hr = psfDocFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, 
         &ppenum);

    while( (hr = ppenum->Next(1,&pidlItems, &celtFetched)) == S_OK 
       && (celtFetched) == 1)
    {
        psfDocFiles->GetDisplayNameOf(pidlItems, SHGDN_FORPARSING, 
            &strDispName);
        StrRetToBuf(&strDispName, pidlItems, szParseName, MAX_PATH);
        
        hr = StringCchLength(szParseName, MAX_PATH, &ParseNameSize);
        
        if (SUCCEEDED(hr))
        {
            for(i=0; i<=ParseNameSize; i++)
            {
                szSourceFiles[iBufPos++] = szParseName[i];
            }
            CoTaskMemFree(pidlItems);
        }
    }
    ppenum->Release();
    
    szSourceFiles[iBufPos] = '\0';

    sfo.hwnd = NULL;
    sfo.wFunc = FO_COPY;
    sfo.pFrom = szSourceFiles;
    sfo.pTo = "c:\\My_Docs2\0";
    sfo.fFlags = FOF_SILENT | FOF_NOCONFIRMATION | FOF_NOCONFIRMMKDIR;

    hr = SHFileOperation(&sfo);
    
    SHChangeNotify(SHCNE_UPDATEDIR, SHCNF_PATH, (LPCVOID) "c:\\My_Docs2", 0);

    CoTaskMemFree(pidlDocFiles);
    psfDocFiles->Release();

    return 0;
}
```



<span data-ttu-id="77cd1-242">O aplicativo primeiro recupera um ponteiro para a interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="77cd1-242">The application first retrieves a pointer to the desktop's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span> <span data-ttu-id="77cd1-243">Em seguida, ele recupera o PIDL do diretório de origem passando seu caminho totalmente qualificado para [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname).</span><span class="sxs-lookup"><span data-stu-id="77cd1-243">It then retrieves the source directory's PIDL by passing its fully qualified path to [**IShellFolder::ParseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname).</span></span> <span data-ttu-id="77cd1-244">Observe que **IShellFolder::P arsedisplayname** requer que o caminho do diretório seja uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="77cd1-244">Note that **IShellFolder::ParseDisplayName** requires the directory's path to be a Unicode string.</span></span> <span data-ttu-id="77cd1-245">Em seguida, o aplicativo é associado ao diretório de origem e usa sua interface **IShellFolder** para recuperar a interface [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) de um objeto enumerador.</span><span class="sxs-lookup"><span data-stu-id="77cd1-245">The application then binds to the source directory and uses its **IShellFolder** interface to retrieve an enumerator object's [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) interface.</span></span>

<span data-ttu-id="77cd1-246">Como cada arquivo no diretório de origem é enumerado, [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) é usado para recuperar seu nome.</span><span class="sxs-lookup"><span data-stu-id="77cd1-246">As each file in the source directory is enumerated, [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) is used to retrieve its name.</span></span> <span data-ttu-id="77cd1-247">O \_ sinalizador SHGDN FORPARSING está definido, o que faz com que **IShellFolder:: GetDisplayNameOf** retorne o caminho totalmente qualificado do arquivo.</span><span class="sxs-lookup"><span data-stu-id="77cd1-247">The SHGDN\_FORPARSING flag is set, which causes **IShellFolder::GetDisplayNameOf** to return the file's fully qualified path.</span></span> <span data-ttu-id="77cd1-248">Os caminhos de arquivo, incluindo os caracteres **nulos** de terminação, são concatenados em uma única matriz, *szSourceFiles*.</span><span class="sxs-lookup"><span data-stu-id="77cd1-248">The file paths, including the terminating **NULL** characters, are concatenated into a single array, *szSourceFiles*.</span></span> <span data-ttu-id="77cd1-249">Um segundo caractere **nulo** é acrescentado ao caminho final para encerrar a matriz corretamente.</span><span class="sxs-lookup"><span data-stu-id="77cd1-249">A second **NULL** character is appended to the final path to terminate the array properly.</span></span>

<span data-ttu-id="77cd1-250">Depois que a enumeração for concluída, o aplicativo atribuirá valores a uma estrutura [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) .</span><span class="sxs-lookup"><span data-stu-id="77cd1-250">Once the enumeration is complete, the application assigns values to an [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) structure.</span></span> <span data-ttu-id="77cd1-251">Observe que a matriz atribuída a **PTO** para especificar o destino também deve ser terminada por um **nulo** duplo.</span><span class="sxs-lookup"><span data-stu-id="77cd1-251">Note that the array assigned to **pTo** to specify the destination must also be terminated by a double **NULL**.</span></span> <span data-ttu-id="77cd1-252">Nesse caso, ele é simplesmente incluído na cadeia de caracteres que é atribuída a **PTO**.</span><span class="sxs-lookup"><span data-stu-id="77cd1-252">In this case, it is simply included in the string that is assigned to **pTo**.</span></span> <span data-ttu-id="77cd1-253">Como esse é um aplicativo de console, os \_ sinalizadores fof silencioso, FOF \_ confirmion e fof \_ NOCONFIRMMKDIR são definidos para suprimir as caixas de diálogo que podem aparecer.</span><span class="sxs-lookup"><span data-stu-id="77cd1-253">Because this is a console application, the FOF\_SILENT, FOF\_NOCONFIRMATION, and FOF\_NOCONFIRMMKDIR flags are set to suppress any dialog boxes that might appear.</span></span> <span data-ttu-id="77cd1-254">Depois que [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) retorna, [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) é chamado para notificar o Shell da alteração.</span><span class="sxs-lookup"><span data-stu-id="77cd1-254">After [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) returns, [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) is called to notify the Shell of the change.</span></span> <span data-ttu-id="77cd1-255">Em seguida, o aplicativo executa a limpeza e o retornos usuais.</span><span class="sxs-lookup"><span data-stu-id="77cd1-255">Then the application performs the usual cleanup and returns.</span></span>

## <a name="adding-files-to-the-shells-list-of-recent-documents"></a><span data-ttu-id="77cd1-256">Adicionando arquivos à lista de documentos recentes do Shell</span><span class="sxs-lookup"><span data-stu-id="77cd1-256">Adding Files to the Shell's List of Recent Documents</span></span>

<span data-ttu-id="77cd1-257">O Shell mantém uma lista de documentos recentemente adicionados ou modificados para cada usuário.</span><span class="sxs-lookup"><span data-stu-id="77cd1-257">The Shell maintains a list of recently added or modified documents for each user.</span></span> <span data-ttu-id="77cd1-258">o usuário pode exibir uma lista de links para esses arquivos clicando em documentos na menu Iniciar.</span><span class="sxs-lookup"><span data-stu-id="77cd1-258">The user can display a list of links to these files by clicking Documents on the Start menu.</span></span> <span data-ttu-id="77cd1-259">Assim como acontece com meus documentos, cada usuário tem um diretório do sistema de arquivos para manter os links reais.</span><span class="sxs-lookup"><span data-stu-id="77cd1-259">As with My Documents, each user has a file system directory to hold the actual links.</span></span> <span data-ttu-id="77cd1-260">Para recuperar o PIDL do diretório recente do usuário atual, seu aplicativo pode chamar [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) com CSIDL \_ recente ou chamar [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) para recuperar seu caminho.</span><span class="sxs-lookup"><span data-stu-id="77cd1-260">To retrieve the PIDL of the current user's Recent directory, your application can call [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) with CSIDL\_RECENT, or call [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) to retrieve its path.</span></span>

<span data-ttu-id="77cd1-261">Seu aplicativo pode enumerar o conteúdo da pasta recente usando as técnicas discutidas anteriormente neste documento.</span><span class="sxs-lookup"><span data-stu-id="77cd1-261">Your application can enumerate the contents of the Recent folder using the techniques discussed earlier in this document.</span></span> <span data-ttu-id="77cd1-262">No entanto, um aplicativo não deve modificar o conteúdo da pasta como se fosse uma pasta normal do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="77cd1-262">However, an application should not modify the contents of the folder as if it were a normal file system folder.</span></span> <span data-ttu-id="77cd1-263">se isso ocorrer, a lista de documentos recentes do Shell não será atualizada corretamente e as alterações não serão refletidas na menu Iniciar.</span><span class="sxs-lookup"><span data-stu-id="77cd1-263">If it does so, the Shell's list of recent documents will not be updated properly, and the changes will not be reflected in the Start menu.</span></span> <span data-ttu-id="77cd1-264">Em vez disso, para adicionar um link de documento à pasta recente de um usuário, seu aplicativo pode chamar [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs).</span><span class="sxs-lookup"><span data-stu-id="77cd1-264">Instead, to add a document link to a user's Recent folder, your application can call [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs).</span></span> <span data-ttu-id="77cd1-265">o Shell adicionará um link à pasta do sistema de arquivos apropriada, bem como atualizando sua lista de documentos recentes e o menu Iniciar.</span><span class="sxs-lookup"><span data-stu-id="77cd1-265">The Shell will add a link to the appropriate file system folder, as well as updating its list of recent documents and the Start menu.</span></span> <span data-ttu-id="77cd1-266">Você também pode usar essa função para limpar a pasta.</span><span class="sxs-lookup"><span data-stu-id="77cd1-266">You can also use this function to clear the folder.</span></span>

 

 
