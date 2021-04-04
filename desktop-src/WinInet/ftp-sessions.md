---
title: Sessões de FTP
description: O WinINet permite que os aplicativos naveguem e manipulem diretórios e arquivos em um servidor FTP. Como os proxies de CERN não oferecem suporte a FTP, os aplicativos que usam um proxy CERN exclusivamente devem usar a função InternetOpenUrl.
ms.assetid: 23763672-765f-4bbc-95c9-c28775e91f3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8310c2b83b81fc18b84d39153ed3dc7afda0df5a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007843"
---
# <a name="ftp-sessions"></a><span data-ttu-id="0df5e-104">Sessões de FTP</span><span class="sxs-lookup"><span data-stu-id="0df5e-104">FTP Sessions</span></span>

<span data-ttu-id="0df5e-105">O WinINet permite que os aplicativos naveguem e manipulem diretórios e arquivos em um servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="0df5e-105">WinINet enables applications to navigate and manipulate directories and files on an ftp server.</span></span> <span data-ttu-id="0df5e-106">Como os proxies de CERN não oferecem suporte a FTP, os aplicativos que usam um proxy CERN exclusivamente devem usar a função [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="0df5e-106">Because CERN proxies do not support FTP, applications that use a CERN proxy exclusively must use the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span> <span data-ttu-id="0df5e-107">Para obter mais informações sobre como usar o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), consulte [acessando URLs diretamente](handling-uniform-resource-locators.md).</span><span class="sxs-lookup"><span data-stu-id="0df5e-107">For more information about how to use [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), see [Accessing URLs Directly](handling-uniform-resource-locators.md).</span></span>

<span data-ttu-id="0df5e-108">Para iniciar uma sessão de FTP, use [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) para criar o identificador de sessão.</span><span class="sxs-lookup"><span data-stu-id="0df5e-108">To begin an FTP session, use [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) to create the session handle.</span></span>

<span data-ttu-id="0df5e-109">O WinINet permite que você execute as seguintes ações em um servidor FTP:</span><span class="sxs-lookup"><span data-stu-id="0df5e-109">WinINet enables you to perform the following actions on an FTP server:</span></span>

-   <span data-ttu-id="0df5e-110">Navegar entre diretórios.</span><span class="sxs-lookup"><span data-stu-id="0df5e-110">Navigate between directories.</span></span>
-   <span data-ttu-id="0df5e-111">Enumerar, criar, remover e renomear diretórios.</span><span class="sxs-lookup"><span data-stu-id="0df5e-111">Enumerate, create, remove, and rename directories.</span></span>
-   <span data-ttu-id="0df5e-112">Renomear, carregar, baixar e excluir arquivos.</span><span class="sxs-lookup"><span data-stu-id="0df5e-112">Rename, upload, download, and delete files.</span></span>

<span data-ttu-id="0df5e-113">A navegação é fornecida pelas funções [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) e [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) .</span><span class="sxs-lookup"><span data-stu-id="0df5e-113">Navigation is provided by the [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) and [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) functions.</span></span> <span data-ttu-id="0df5e-114">Essas funções utilizam o identificador de sessão criado por uma chamada anterior para [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) para determinar em qual diretório o aplicativo está no momento ou para alterar para um subdiretório diferente.</span><span class="sxs-lookup"><span data-stu-id="0df5e-114">These functions utilize the session handle created by a previous call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) to determine which directory the application is currently in, or to change to a different subdirectory.</span></span>

<span data-ttu-id="0df5e-115">A enumeração de diretório é executada usando as funções [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) e [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) .</span><span class="sxs-lookup"><span data-stu-id="0df5e-115">Directory enumeration is performed by using the [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) and [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) functions.</span></span> <span data-ttu-id="0df5e-116">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) usa o identificador de sessão criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) para localizar o primeiro arquivo que corresponde aos critérios de pesquisa fornecidos e retorna um identificador para continuar a enumeração do diretório.</span><span class="sxs-lookup"><span data-stu-id="0df5e-116">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) uses the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) to find the first file that matches the given search criteria and returns a handle to continue the directory enumeration.</span></span> <span data-ttu-id="0df5e-117">[**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) usa o identificador retornado pelo [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) para retornar o próximo arquivo que corresponde aos critérios de pesquisa originais.</span><span class="sxs-lookup"><span data-stu-id="0df5e-117">[**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) uses the handle returned by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) to return the next file that matches the original search criteria.</span></span> <span data-ttu-id="0df5e-118">O aplicativo deve continuar a chamar [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) até que não haja mais arquivos restantes no diretório.</span><span class="sxs-lookup"><span data-stu-id="0df5e-118">The application should continue to call [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) until there are no more files left in the directory.</span></span>

<span data-ttu-id="0df5e-119">Use a função [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) para criar novos diretórios.</span><span class="sxs-lookup"><span data-stu-id="0df5e-119">Use the [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) function to create new directories.</span></span> <span data-ttu-id="0df5e-120">Essa função usa o identificador de sessão criado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) e cria o diretório especificado pela cadeia de caracteres passada para a função.</span><span class="sxs-lookup"><span data-stu-id="0df5e-120">This function uses the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) and creates the directory specified by the string passed to the function.</span></span> <span data-ttu-id="0df5e-121">A cadeia de caracteres pode conter um nome de diretório relativo ao diretório atual ou um caminho de diretório totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="0df5e-121">The string can contain a directory name relative to the current directory, or a fully qualified directory path.</span></span>

<span data-ttu-id="0df5e-122">Para renomear arquivos ou diretórios, o aplicativo pode chamar [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea).</span><span class="sxs-lookup"><span data-stu-id="0df5e-122">To rename either files or directories, the application can call [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea).</span></span> <span data-ttu-id="0df5e-123">Essa função substitui o nome original pelo novo nome passado para a função.</span><span class="sxs-lookup"><span data-stu-id="0df5e-123">This function replaces the original name with the new name passed to the function.</span></span> <span data-ttu-id="0df5e-124">O nome do arquivo ou diretório pode ser relativo ao diretório atual ou um nome totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="0df5e-124">The name of the file or directory can be relative to the current directory, or a fully qualified name.</span></span>

<span data-ttu-id="0df5e-125">Para carregar ou inserir arquivos em um servidor FTP, o aplicativo pode usar [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) ou [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (juntamente com [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)).</span><span class="sxs-lookup"><span data-stu-id="0df5e-125">To upload or place files on an FTP server, the application can use either [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) or [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (along with [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)).</span></span> <span data-ttu-id="0df5e-126">[**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) pode ser usado se o arquivo já existir localmente, enquanto [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) e [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) podem ser usados se os dados precisarem ser gravados em um arquivo no servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="0df5e-126">[**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) can be used if the file already exists locally, while [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) can be used if data needs to be written to a file on the FTP server.</span></span>

<span data-ttu-id="0df5e-127">Para baixar ou obter arquivos, o aplicativo pode usar [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) ou [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (com [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)).</span><span class="sxs-lookup"><span data-stu-id="0df5e-127">To download or get files, the application can use either [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) or [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (with [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)).</span></span> <span data-ttu-id="0df5e-128">[**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) é usado para recuperar um arquivo de um servidor FTP e armazená-lo localmente, enquanto [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) e [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) podem ser usados para controlar onde as informações baixadas estão indo (por exemplo, o aplicativo pode exibir as informações em uma caixa de edição).</span><span class="sxs-lookup"><span data-stu-id="0df5e-128">[**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) is used to retrieve a file from an FTP server and store it locally, while [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) can be used to control where the downloaded information is going (for example, the application could display the information in an edit box).</span></span>

<span data-ttu-id="0df5e-129">Exclua arquivos em um servidor FTP usando a função [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) .</span><span class="sxs-lookup"><span data-stu-id="0df5e-129">Delete files on an FTP server by using the [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) function.</span></span> <span data-ttu-id="0df5e-130">Essa função remove um nome de arquivo relativo ao diretório atual ou a um nome de arquivo totalmente qualificado do servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="0df5e-130">This function removes a file name that is relative either to the current directory or to a fully qualified file name from the FTP server.</span></span> <span data-ttu-id="0df5e-131">[**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) requer um identificador de sessão retornado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="0df5e-131">[**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) requires a session handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>

## <a name="ftp-function-handles"></a><span data-ttu-id="0df5e-132">Identificadores de função FTP</span><span class="sxs-lookup"><span data-stu-id="0df5e-132">FTP Function Handles</span></span>

<span data-ttu-id="0df5e-133">Para funcionar corretamente, as funções de FTP exigem determinados tipos de identificadores [**HINTERNET**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="0df5e-133">To work properly, the FTP functions require certain types of [**HINTERNET**](appendix-a-hinternet-handles.md) handles.</span></span> <span data-ttu-id="0df5e-134">Esses identificadores devem ser criados em uma ordem específica, começando com o identificador raiz criado pelo [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="0df5e-134">These handles must be created in a specific order, starting with the root handle created by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="0df5e-135">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) pode criar um identificador de sessão de FTP.</span><span class="sxs-lookup"><span data-stu-id="0df5e-135">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) can then create an FTP session handle.</span></span>

<span data-ttu-id="0df5e-136">O diagrama a seguir mostra as funções que dependem do identificador de sessão de FTP retornado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="0df5e-136">The following diagram shows the functions that are dependent on the FTP session handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="0df5e-137">As caixas sombreadas representam funções que retornam identificadores [**HINTERNET**](appendix-a-hinternet-handles.md) , enquanto as caixas simples representam funções que usam o identificador HINTERNET criado pela função na qual dependem.</span><span class="sxs-lookup"><span data-stu-id="0df5e-137">The shaded boxes represent functions that return [**HINTERNET**](appendix-a-hinternet-handles.md) handles, while the plain boxes represent functions that use the HINTERNET handle created by the function on which they depend.</span></span>

![funções de FTP dependentes do identificador de sessão de FTP retornado por InternetConnect](images/ax-wnt06.png)

<span data-ttu-id="0df5e-139">O diagrama a seguir mostra as duas funções que retornam identificadores [HINTERNET](appendix-a-hinternet-handles.md) e as funções que dependem deles.</span><span class="sxs-lookup"><span data-stu-id="0df5e-139">The following diagram shows the two functions that return [HINTERNET](appendix-a-hinternet-handles.md) handles and the functions that are dependent on them.</span></span> <span data-ttu-id="0df5e-140">As caixas sombreadas representam funções que retornam identificadores **HINTERNET** , enquanto as caixas simples representam funções que usam o identificador **HINTERNET** criado pela função na qual dependem.</span><span class="sxs-lookup"><span data-stu-id="0df5e-140">The shaded boxes represent functions that return **HINTERNET** handles, while the plain boxes represent functions that use the **HINTERNET** handle created by the function on which they depend.</span></span>

![funções de FTP que retornam identificadores de HINTERNET](images/ax-wnt03.png)

<span data-ttu-id="0df5e-142">Para obter mais informações, consulte [HINTERNET Handles](appendix-a-hinternet-handles.md).</span><span class="sxs-lookup"><span data-stu-id="0df5e-142">For more information, see [HINTERNET Handles](appendix-a-hinternet-handles.md).</span></span>

## <a name="using-the-wininet-functions-for-ftp-sessions"></a><span data-ttu-id="0df5e-143">Usando as funções do WinINet para sessões de FTP</span><span class="sxs-lookup"><span data-stu-id="0df5e-143">Using the WinINet Functions for FTP Sessions</span></span>

<span data-ttu-id="0df5e-144">As funções a seguir são usadas durante as sessões de FTP.</span><span class="sxs-lookup"><span data-stu-id="0df5e-144">The following functions are used during FTP sessions.</span></span> <span data-ttu-id="0df5e-145">Essas funções não são reconhecidas por proxies de CERN.</span><span class="sxs-lookup"><span data-stu-id="0df5e-145">These functions are not recognized by CERN proxies.</span></span> <span data-ttu-id="0df5e-146">Os aplicativos que devem funcionar por meio de proxies de CERN devem usar [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) e acessar os recursos diretamente.</span><span class="sxs-lookup"><span data-stu-id="0df5e-146">Applications that must function through CERN proxies should use [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and access the resources directly.</span></span> <span data-ttu-id="0df5e-147">Para obter mais informações sobre o acesso direto a recursos, consulte [acessando URLs diretamente](handling-uniform-resource-locators.md).</span><span class="sxs-lookup"><span data-stu-id="0df5e-147">For more information on direct resource access, see [Accessing URLs Directly](handling-uniform-resource-locators.md).</span></span>



| <span data-ttu-id="0df5e-148">Função</span><span class="sxs-lookup"><span data-stu-id="0df5e-148">Function</span></span>                                                 | <span data-ttu-id="0df5e-149">Descrição</span><span class="sxs-lookup"><span data-stu-id="0df5e-149">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0df5e-150">**FtpCreateDirectory**</span><span class="sxs-lookup"><span data-stu-id="0df5e-150">**FtpCreateDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)         | <span data-ttu-id="0df5e-151">Cria um novo diretório no servidor.</span><span class="sxs-lookup"><span data-stu-id="0df5e-151">Creates a new directory on the server.</span></span> <span data-ttu-id="0df5e-152">Essa função requer um identificador criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="0df5e-152">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                  |
| [<span data-ttu-id="0df5e-153">**FtpDeleteFile**</span><span class="sxs-lookup"><span data-stu-id="0df5e-153">**FtpDeleteFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)                   | <span data-ttu-id="0df5e-154">Exclui um arquivo do servidor.</span><span class="sxs-lookup"><span data-stu-id="0df5e-154">Deletes a file from the server.</span></span> <span data-ttu-id="0df5e-155">Essa função requer um identificador criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="0df5e-155">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                         |
| [<span data-ttu-id="0df5e-156">**FtpFindFirstFile**</span><span class="sxs-lookup"><span data-stu-id="0df5e-156">**FtpFindFirstFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)             | <span data-ttu-id="0df5e-157">Inicia a enumeração de arquivos ou a pesquisa de arquivos no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="0df5e-157">Starts file enumeration or file search in the current directory.</span></span> <span data-ttu-id="0df5e-158">Essa função requer um identificador criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="0df5e-158">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>        |
| [<span data-ttu-id="0df5e-159">**FtpGetCurrentDirectory**</span><span class="sxs-lookup"><span data-stu-id="0df5e-159">**FtpGetCurrentDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) | <span data-ttu-id="0df5e-160">Retorna o diretório atual do cliente no servidor.</span><span class="sxs-lookup"><span data-stu-id="0df5e-160">Returns the client's current directory on the server.</span></span> <span data-ttu-id="0df5e-161">Essa função requer um identificador criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="0df5e-161">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                   |
| [<span data-ttu-id="0df5e-162">**FtpGetFile**</span><span class="sxs-lookup"><span data-stu-id="0df5e-162">**FtpGetFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)                         | <span data-ttu-id="0df5e-163">Recupera um arquivo do servidor.</span><span class="sxs-lookup"><span data-stu-id="0df5e-163">Retrieves a file from the server.</span></span> <span data-ttu-id="0df5e-164">Essa função requer um identificador criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="0df5e-164">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                       |
| [<span data-ttu-id="0df5e-165">**FtpOpenFile**</span><span class="sxs-lookup"><span data-stu-id="0df5e-165">**FtpOpenFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)                       | <span data-ttu-id="0df5e-166">Inicia o acesso a um arquivo no servidor para leitura ou gravação.</span><span class="sxs-lookup"><span data-stu-id="0df5e-166">Initiates access to a file on the server for either reading or writing.</span></span> <span data-ttu-id="0df5e-167">Essa função requer um identificador criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="0df5e-167">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> |
| [<span data-ttu-id="0df5e-168">**FtpPutFile**</span><span class="sxs-lookup"><span data-stu-id="0df5e-168">**FtpPutFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)                         | <span data-ttu-id="0df5e-169">Grava um arquivo no servidor.</span><span class="sxs-lookup"><span data-stu-id="0df5e-169">Writes a file to the server.</span></span> <span data-ttu-id="0df5e-170">Essa função requer um identificador criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="0df5e-170">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                            |
| [<span data-ttu-id="0df5e-171">**FtpRemoveDirectory**</span><span class="sxs-lookup"><span data-stu-id="0df5e-171">**FtpRemoveDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)         | <span data-ttu-id="0df5e-172">Exclui um diretório no servidor.</span><span class="sxs-lookup"><span data-stu-id="0df5e-172">Deletes a directory on the server.</span></span> <span data-ttu-id="0df5e-173">Essa função requer um identificador criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="0df5e-173">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                      |
| [<span data-ttu-id="0df5e-174">**FtpRenameFile**</span><span class="sxs-lookup"><span data-stu-id="0df5e-174">**FtpRenameFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)                   | <span data-ttu-id="0df5e-175">Renomeia um arquivo no servidor.</span><span class="sxs-lookup"><span data-stu-id="0df5e-175">Renames a file on the server.</span></span> <span data-ttu-id="0df5e-176">Essa função requer um identificador criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="0df5e-176">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                           |
| [<span data-ttu-id="0df5e-177">**FtpSetCurrentDirectory**</span><span class="sxs-lookup"><span data-stu-id="0df5e-177">**FtpSetCurrentDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) | <span data-ttu-id="0df5e-178">Altera o diretório atual do cliente no servidor.</span><span class="sxs-lookup"><span data-stu-id="0df5e-178">Changes the client's current directory on the server.</span></span> <span data-ttu-id="0df5e-179">Essa função requer um identificador criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="0df5e-179">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                   |
| [<span data-ttu-id="0df5e-180">**InternetWriteFile**</span><span class="sxs-lookup"><span data-stu-id="0df5e-180">**InternetWriteFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)           | <span data-ttu-id="0df5e-181">Grava dados em um arquivo aberto no servidor.</span><span class="sxs-lookup"><span data-stu-id="0df5e-181">Writes data to an open file on the server.</span></span> <span data-ttu-id="0df5e-182">Essa função requer um identificador criado pelo [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea).</span><span class="sxs-lookup"><span data-stu-id="0df5e-182">This function requires a handle created by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea).</span></span>                                      |



 

### <a name="starting-an-ftp-session"></a><span data-ttu-id="0df5e-183">Iniciando uma sessão de FTP</span><span class="sxs-lookup"><span data-stu-id="0df5e-183">Starting an FTP Session</span></span>

<span data-ttu-id="0df5e-184">O aplicativo estabelece uma sessão de FTP chamando [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) em um identificador criado por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="0df5e-184">The application establishes an FTP session by calling [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) on a handle created by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="0df5e-185">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) precisa do nome do servidor, número da porta, nome de usuário, senha e tipo de serviço (que deve ser definido como FTP do serviço de Internet \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="0df5e-185">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) needs the server name, port number, user name, password, and service type (which must be set to INTERNET\_SERVICE\_FTP).</span></span> <span data-ttu-id="0df5e-186">Para a semântica de FTP passivo, o aplicativo também deve definir o sinalizador [ \_ \_ passivo de sinalizador da Internet](api-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="0df5e-186">For passive FTP semantics, the application must also set the [INTERNET\_FLAG\_PASSIVE](api-flags.md) flag.</span></span>

<span data-ttu-id="0df5e-187">Os valores da porta \_ FTP padrão da Internet \_ e do número de \_ \_ \_ porta inválido da Internet \_ podem ser usados para o número da porta.</span><span class="sxs-lookup"><span data-stu-id="0df5e-187">The INTERNET\_DEFAULT\_FTP\_PORT and INTERNET\_INVALID\_PORT\_NUMBER values can be used for the port number.</span></span> <span data-ttu-id="0df5e-188">A \_ \_ porta FTP padrão \_ da Internet usa a porta FTP padrão, mas o tipo de serviço ainda deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="0df5e-188">INTERNET\_DEFAULT\_FTP\_PORT uses the default FTP port, but the service type still must be set.</span></span> <span data-ttu-id="0df5e-189">\_O número de porta inválido da Internet \_ \_ usa o valor padrão para o tipo de serviço indicado.</span><span class="sxs-lookup"><span data-stu-id="0df5e-189">INTERNET\_INVALID\_PORT\_NUMBER uses the default value for the indicated service type.</span></span>

<span data-ttu-id="0df5e-190">Os valores para o nome de usuário e a senha podem ser definidos como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0df5e-190">The values for the user name and password can be set to **NULL**.</span></span> <span data-ttu-id="0df5e-191">Se ambos os valores forem definidos como **NULL**, [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usará "Anonymous" para o nome de usuário e o endereço de email do usuário para a senha.</span><span class="sxs-lookup"><span data-stu-id="0df5e-191">If both values are set to **NULL**, [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) uses "anonymous" for the user name, and the user's email address for the password.</span></span> <span data-ttu-id="0df5e-192">Se apenas a senha for definida como **NULL**, o nome de usuário passado para [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) será usado para o nome de usuário e uma cadeia de caracteres vazia será usada para a senha.</span><span class="sxs-lookup"><span data-stu-id="0df5e-192">If only the password is set to **NULL**, the user name passed to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) is used for the user name, and an empty string is used for the password.</span></span> <span data-ttu-id="0df5e-193">Se nenhum valor for **nulo**, o nome de usuário e a senha fornecidos para [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) serão usados.</span><span class="sxs-lookup"><span data-stu-id="0df5e-193">If neither value is **NULL**, the user name and password given to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) are used.</span></span>

### <a name="enumerating-directories"></a><span data-ttu-id="0df5e-194">Enumerando diretórios</span><span class="sxs-lookup"><span data-stu-id="0df5e-194">Enumerating Directories</span></span>

<span data-ttu-id="0df5e-195">A enumeração de um diretório em um servidor FTP requer a criação de um identificador por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span><span class="sxs-lookup"><span data-stu-id="0df5e-195">Enumeration of a directory on an FTP server requires the creation of a handle by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span></span> <span data-ttu-id="0df5e-196">Esse identificador é uma ramificação do identificador de sessão criado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="0df5e-196">This handle is a branch of the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="0df5e-197">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) localiza o primeiro arquivo ou diretório no servidor e o retorna em uma estrutura de [**\_ \_ dados de localização do Win32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) .</span><span class="sxs-lookup"><span data-stu-id="0df5e-197">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) locates the first file or directory on the server and returns it in a [**WIN32\_FIND\_DATA**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) structure.</span></span> <span data-ttu-id="0df5e-198">Use [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) até que ele retorne [**um erro de \_ \_ mais \_ arquivos**](wininet-errors.md).</span><span class="sxs-lookup"><span data-stu-id="0df5e-198">Use [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) until it returns [**ERROR\_NO\_MORE\_FILES**](wininet-errors.md).</span></span> <span data-ttu-id="0df5e-199">Esse método localiza todos os arquivos e diretórios subsequentes no servidor.</span><span class="sxs-lookup"><span data-stu-id="0df5e-199">This method finds all subsequent files and directories on the server.</span></span> <span data-ttu-id="0df5e-200">Para obter mais informações sobre o [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), consulte [localizando o próximo arquivo](common-functions.md).</span><span class="sxs-lookup"><span data-stu-id="0df5e-200">For more information on [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), see [Finding the Next File](common-functions.md).</span></span>

<span data-ttu-id="0df5e-201">Para determinar se o arquivo recuperado por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) ou [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) é um diretório, verifique o membro **dwFileAttributes** da estrutura [**de \_ \_ dados de localização do Win32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) para ver se ele é igual ao diretório de atributo de arquivo \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0df5e-201">To determine if the file retrieved by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) or [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) is a directory, check the **dwFileAttributes** member of the [**WIN32\_FIND\_DATA**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) structure to see if it is equal to FILE\_ATTRIBUTE\_DIRECTORY.</span></span>

<span data-ttu-id="0df5e-202">Se o aplicativo fizer alterações no servidor FTP ou se o servidor FTP for alterado com frequência, [o \_ sinalizador \_ Internet \_ sem \_ gravação do cache](api-flags.md) e sinalizadores de [ \_ \_ recarga da Internet](api-flags.md) deverão ser definidos em [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span><span class="sxs-lookup"><span data-stu-id="0df5e-202">If the application makes changes on the FTP server or if the FTP server changes frequently, the [INTERNET\_FLAG\_NO\_CACHE\_WRITE](api-flags.md) and [INTERNET\_FLAG\_RELOAD](api-flags.md) flags should be set in [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span></span> <span data-ttu-id="0df5e-203">Esses sinalizadores garantem que as informações de diretório que estão sendo recuperadas do servidor FTP sejam atuais.</span><span class="sxs-lookup"><span data-stu-id="0df5e-203">These flags ensure that the directory information being retrieved from the FTP server is current.</span></span>

<span data-ttu-id="0df5e-204">Depois que o aplicativo concluir a enumeração do diretório, o aplicativo deverá fazer uma chamada para [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) no identificador criado pelo [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span><span class="sxs-lookup"><span data-stu-id="0df5e-204">After the application completes the directory enumeration, the application must make a call to [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) on the handle created by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span></span> <span data-ttu-id="0df5e-205">Até que o identificador seja fechado, o aplicativo não poderá chamar [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) novamente no identificador de sessão criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="0df5e-205">Until that handle is closed, the application cannot call [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) again on the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="0df5e-206">Se uma chamada para [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) for feita no mesmo identificador de sessão antes de a chamada anterior para a mesma função ser fechada, a função falhará, retornando a [ \_ \_ transferência \_ de FTP de erro em \_ andamento](wininet-errors.md).</span><span class="sxs-lookup"><span data-stu-id="0df5e-206">If a call to [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) is made on the same session handle before the previous call to the same function is closed, the function fails, returning [ERROR\_FTP\_TRANSFER\_IN\_PROGRESS](wininet-errors.md).</span></span>

<span data-ttu-id="0df5e-207">O exemplo a seguir enumera o conteúdo de um diretório de FTP em um controle de caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="0df5e-207">The following example enumerates the contents of an FTP directory into a list box control.</span></span> <span data-ttu-id="0df5e-208">O parâmetro *hConnection* é um identificador retornado pela função [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) depois que ele estabelece uma sessão de FTP.</span><span class="sxs-lookup"><span data-stu-id="0df5e-208">The *hConnection* parameter is a handle returned by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function after it establishes an FTP session.</span></span> <span data-ttu-id="0df5e-209">O código-fonte de exemplo para a função InternetErrorOut referenciada neste exemplo pode ser encontrado no tópico [Manipulando erros](appendix-c-handling-errors.md).</span><span class="sxs-lookup"><span data-stu-id="0df5e-209">Sample source code for the InternetErrorOut function referenced in this example can be found in the [Handling Errors](appendix-c-handling-errors.md)topic.</span></span>


```C++
#include <windows.h>
#include <strsafe.h>
#include <wininet.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  FTP_FUNCTIONS_BUFFER_SIZE          MAX_PATH+8

BOOL WINAPI DisplayFtpDir(
                           HWND hDlg,
                           HINTERNET hConnection,
                           DWORD dwFindFlags,
                           int nListBoxId )
{
  WIN32_FIND_DATA dirInfo;
  HINTERNET       hFind;
  DWORD           dwError;
  BOOL            retVal = FALSE;
  TCHAR           szMsgBuffer[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR           szFName[FTP_FUNCTIONS_BUFFER_SIZE];
  
  SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
  hFind = FtpFindFirstFile( hConnection, TEXT( "*.*" ), 
                            &dirInfo, dwFindFlags, 0 );
  if ( hFind == NULL )
  {
    dwError = GetLastError( );
    if( dwError == ERROR_NO_MORE_FILES )
    {
      StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
        TEXT( "No files found at FTP location specified." ) );
      retVal = TRUE;
      goto DisplayDirError_1;
    }
    StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
      TEXT( "FtpFindFirstFile failed." ) );
    goto DisplayDirError_1;
  }

  do
  {
    if( FAILED( StringCchCopy( szFName, FTP_FUNCTIONS_BUFFER_SIZE,
                  dirInfo.cFileName ) ) ||
        ( ( dirInfo.dwFileAttributes & FILE_ATTRIBUTE_DIRECTORY ) &&
        ( FAILED( StringCchCat( szFName, FTP_FUNCTIONS_BUFFER_SIZE,
         TEXT( " <DIR> " ) ) ) ) ) )
    {
      StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
        TEXT( "Failed to copy a file or directory name." ) );
      retVal = FALSE;
      goto DisplayDirError_2;
    }
    SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 
                        0, (LPARAM) szFName );
  } while( InternetFindNextFile( hFind, (LPVOID) &dirInfo ) );

  if( ( dwError = GetLastError( ) ) == ERROR_NO_MORE_FILES )
  {
    InternetCloseHandle(hFind);
    return( TRUE );
  }
  StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
    TEXT( "FtpFindNextFile failed." ) );

DisplayDirError_2:
  InternetCloseHandle( hFind );
DisplayDirError_1:
  MessageBox( hDlg,
    (LPCTSTR) szMsgBuffer,
    TEXT( "DisplayFtpDir( ) Problem" ),
    MB_OK | MB_ICONERROR );
  return( retVal );
}
```



### <a name="navigating-directories"></a><span data-ttu-id="0df5e-210">Navegando em diretórios</span><span class="sxs-lookup"><span data-stu-id="0df5e-210">Navigating Directories</span></span>

<span data-ttu-id="0df5e-211">As funções [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) e [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) lidam com a navegação de diretório.</span><span class="sxs-lookup"><span data-stu-id="0df5e-211">The [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) and [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) functions handle directory navigation.</span></span>

<span data-ttu-id="0df5e-212">[**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) retorna o diretório atual do aplicativo no servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="0df5e-212">[**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) returns the application's current directory on the FTP server.</span></span> <span data-ttu-id="0df5e-213">O caminho do diretório do diretório raiz no servidor FTP está incluído.</span><span class="sxs-lookup"><span data-stu-id="0df5e-213">The directory path from the root directory on the FTP server is included.</span></span>

<span data-ttu-id="0df5e-214">[**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) altera o diretório de trabalho no servidor.</span><span class="sxs-lookup"><span data-stu-id="0df5e-214">[**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) changes the working directory on the server.</span></span> <span data-ttu-id="0df5e-215">As informações de diretório passadas para [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) podem ser um nome de caminho parcialmente ou totalmente qualificado relativo ao diretório atual.</span><span class="sxs-lookup"><span data-stu-id="0df5e-215">The directory information passed to [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) can be either a partially or fully qualified path name relative to the current directory.</span></span> <span data-ttu-id="0df5e-216">Por exemplo, se o aplicativo estiver atualmente no diretório "Public/info" e o caminho for "FTP/example", [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) alterará o diretório atual para "Public/info/FTP/example".</span><span class="sxs-lookup"><span data-stu-id="0df5e-216">For example, if the application is currently in the directory "public/info" and the path is "ftp/example", [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) changes the current directory to "public/info/ftp/example".</span></span>

<span data-ttu-id="0df5e-217">O exemplo a seguir usa o identificador de sessão de FTP hConnection, que é retornado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="0df5e-217">The following example uses the FTP session handle hConnection, which is returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="0df5e-218">O novo nome de diretório é obtido da caixa de edição do diálogo pai cuja IDC é passada no parâmetro *nDirNameId* .</span><span class="sxs-lookup"><span data-stu-id="0df5e-218">The new directory name is taken from the edit box of the parent dialog whose IDC is passed in the *nDirNameId* parameter.</span></span> <span data-ttu-id="0df5e-219">Antes que a alteração de diretório seja feita, a função recupera o diretório atual e o armazena na mesma caixa de edição.</span><span class="sxs-lookup"><span data-stu-id="0df5e-219">Before the directory change is made, the function retrieves the current directory and stores it in the same edit box.</span></span> <span data-ttu-id="0df5e-220">O código do recurso para a função DisplayFtpDir chamada no final é listado acima.</span><span class="sxs-lookup"><span data-stu-id="0df5e-220">The souce code for the DisplayFtpDir function called at the end is listed above.</span></span>


```C++
BOOL WINAPI ChangeFtpDir( HWND hDlg, 
                          HINTERNET hConnection,
                          int nDirNameId, 
                          int nListBoxId )
{
  DWORD dwSize;
  TCHAR szNewDirName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szOldDirName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR* szFailedFunctionName;

  dwSize = FTP_FUNCTIONS_BUFFER_SIZE;

  if( !GetDlgItemText( hDlg, nDirNameId, szNewDirName, dwSize ) )
  {
    szFailedFunctionName = TEXT( "GetDlgItemText" );
    goto ChangeFtpDirError;
  }

  if ( !FtpGetCurrentDirectory( hConnection, szOldDirName, &dwSize ))
  {
    szFailedFunctionName = TEXT( "FtpGetCurrentDirectory" );
    goto ChangeFtpDirError;
  }

  if( !SetDlgItemText( hDlg, nDirNameId, szOldDirName ) )
  {
    szFailedFunctionName = TEXT( "SetDlgItemText" );
    goto ChangeFtpDirError;
  }

  if( !FtpSetCurrentDirectory( hConnection, szNewDirName ) )
  {
    szFailedFunctionName = TEXT( "FtpSetCurrentDirectory" );
    goto ChangeFtpDirError;
  }
  return( DisplayFtpDir( hDlg, hConnection, 0, nListBoxId ) );

ChangeFtpDirError:
  InternetErrorOut( hDlg, GetLastError( ), szFailedFunctionName );
  DisplayFtpDir( hDlg, hConnection, INTERNET_FLAG_RELOAD, nListBoxId);
  return( FALSE );
}
```



### <a name="manipulating-directories-on-an-ftp-server"></a><span data-ttu-id="0df5e-221">Manipulando diretórios em um servidor FTP</span><span class="sxs-lookup"><span data-stu-id="0df5e-221">Manipulating Directories on an FTP Server</span></span>

<span data-ttu-id="0df5e-222">O WinINet fornece a capacidade de criar e remover diretórios em um servidor FTP para o qual o aplicativo tem os privilégios necessários.</span><span class="sxs-lookup"><span data-stu-id="0df5e-222">WinINet provides the capability to create and remove directories on an FTP server to which the application has the necessary privileges.</span></span> <span data-ttu-id="0df5e-223">Se o aplicativo precisar fazer logon em um servidor com um nome de usuário e senha específicos, os valores poderão ser usados em [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) ao criar o identificador de sessão de FTP.</span><span class="sxs-lookup"><span data-stu-id="0df5e-223">If the application must log on to a server with a specific user name and password, the values can be used in [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) when creating the FTP session handle.</span></span>

<span data-ttu-id="0df5e-224">A função [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) usa um identificador de sessão de ftp válido e uma cadeia de caracteres terminada em **nulo** que contém um caminho totalmente qualificado ou um nome relativo ao diretório atual e cria um diretório no servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="0df5e-224">The [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) function takes a valid FTP session handle and a **null**-terminated string that contains either a fully qualified path or a name relative to the current directory and creates a directory on the FTP server.</span></span>

<span data-ttu-id="0df5e-225">O exemplo a seguir mostra duas chamadas separadas para [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya).</span><span class="sxs-lookup"><span data-stu-id="0df5e-225">The following example shows two separate calls to [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya).</span></span> <span data-ttu-id="0df5e-226">Em ambos os exemplos, hFtpSession é o identificador de sessão criado pela função [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) , e o diretório raiz é o diretório atual.</span><span class="sxs-lookup"><span data-stu-id="0df5e-226">In both examples, hFtpSession is the session handle created by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function, and the root directory is the current directory.</span></span>

``` syntax
/* Creates the directory "test" in the current (root) directory. */
FtpCreateDirectory( hFtpSession, "test" );

/* Creates the directory "example" in the test directory. */
FtpCreateDirectory( hFtpSession, "\\test\\example" );
```

<span data-ttu-id="0df5e-227">A função [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) usa um identificador de sessão e uma cadeia de caracteres terminada em **nulo** que contém um caminho totalmente qualificado ou um nome relativo ao diretório atual e remove esse diretório do servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="0df5e-227">The [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) function takes a session handle and a **null**-terminated string that contains either a fully qualified path or a name relative to the current directory and removes that directory from the FTP server.</span></span>

<span data-ttu-id="0df5e-228">O exemplo a seguir mostra duas chamadas de exemplo para [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya).</span><span class="sxs-lookup"><span data-stu-id="0df5e-228">The following example shows two sample calls to [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya).</span></span> <span data-ttu-id="0df5e-229">Em ambas as chamadas, hFtpSession é o identificador de sessão criado pela função [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) , e o diretório raiz é o diretório atual.</span><span class="sxs-lookup"><span data-stu-id="0df5e-229">In both calls, hFtpSession is the session handle created by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function, and the root directory is the current directory.</span></span> <span data-ttu-id="0df5e-230">Há um diretório chamado "Test" no diretório raiz e um diretório chamado "example" no diretório "Test".</span><span class="sxs-lookup"><span data-stu-id="0df5e-230">There is a directory called "test" in the root directory and a directory called "example" in the "test" directory.</span></span>

``` syntax
/* Removes the "example" directory (plus any files/directories it contains) from the "test" directory. */
FtpRemoveDirectory(hFtpSession,"\\test\\example");

/* Removes the "test" directory (plus any files/directories it contains) from the root directory. */
FtpRemoveDirectory(hFtpSession, "test");
```


```C++
FtpRemoveDirectory(hFtpSession,TEXT("\\test\\example"));
/* Removes the "example" directory and any files or 
directories contained in it from the "test" directory. */

FtpRemoveDirectory(hFtpSession, TEXT("test"));
/* Removes the "test" directory and any files or 
directories contained in it from the root directory. */
```



<span data-ttu-id="0df5e-231">O exemplo a seguir cria um novo diretório no servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="0df5e-231">The following example creates a new directory on the FTP server.</span></span> <span data-ttu-id="0df5e-232">O novo nome de diretório é obtido da caixa de edição do diálogo pai cuja IDC é passada no parâmetro *nDirNameId* .</span><span class="sxs-lookup"><span data-stu-id="0df5e-232">The new directory name is taken from the edit box of the parent dialog whose IDC is passed in the *nDirNameId* parameter.</span></span> <span data-ttu-id="0df5e-233">O identificador *hConnection* foi criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) depois de estabelecer uma sessão FTP.</span><span class="sxs-lookup"><span data-stu-id="0df5e-233">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="0df5e-234">O código-fonte da função DisplayFtpDir chamada no final está listado acima.</span><span class="sxs-lookup"><span data-stu-id="0df5e-234">The source code for the DisplayFtpDir function called at the end is listed above.</span></span>


```C++
BOOL WINAPI CreateFtpDir( HWND hDlg, HINTERNET hConnection,
                          int nDirNameId, int nListBoxId )
{
  TCHAR szNewDirName[FTP_FUNCTIONS_BUFFER_SIZE];

  if( !GetDlgItemText( hDlg, nDirNameId, 
                       szNewDirName, 
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Error: Directory Name Must Be Specified" ),
                TEXT( "Create FTP Directory" ), 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpCreateDirectory( hConnection, szNewDirName ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), 
                      TEXT( "FtpCreateDirectory" ) );
    return( FALSE );
  }

  return( DisplayFtpDir( hDlg, hConnection, 
                         INTERNET_FLAG_RELOAD, 
                         nListBoxId ) );
}
```



<span data-ttu-id="0df5e-235">O exemplo a seguir exclui um diretório do servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="0df5e-235">The following example deletes a directory from the FTP server.</span></span> <span data-ttu-id="0df5e-236">O nome do diretório a ser excluído é obtido da caixa de edição no diálogo pai cuja IDC é passada para o parâmetro *nDirNameId* .</span><span class="sxs-lookup"><span data-stu-id="0df5e-236">The name of the directory to be deleted is taken from the edit box in the parent dialog whose IDC is passed into the *nDirNameId* parameter.</span></span> <span data-ttu-id="0df5e-237">O identificador *hConnection* foi criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) depois de estabelecer uma sessão FTP.</span><span class="sxs-lookup"><span data-stu-id="0df5e-237">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="0df5e-238">O código-fonte da função DisplayFtpDir chamada no final está listado acima.</span><span class="sxs-lookup"><span data-stu-id="0df5e-238">The source code for the DisplayFtpDir function called at the end is listed above.</span></span>


```C++
BOOL WINAPI RemoveFtpDir( HWND hDlg, HINTERNET hConnection,
                          int nDirNameId, int nListBoxId )
{
  TCHAR szDelDirName[FTP_FUNCTIONS_BUFFER_SIZE];

  if( !GetDlgItemText( hDlg, nDirNameId, szDelDirName, 
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Error: Directory Name Must Be Specified" ),
                TEXT( "Remove FTP Directory" ), 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpRemoveDirectory( hConnection, szDelDirName ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), 
                      TEXT( "FtpRemoveDirectory" ) );
    return( FALSE );
  }

  return( DisplayFtpDir( hDlg, hConnection, 
                         INTERNET_FLAG_RELOAD, nListBoxId ) );
}
```



### <a name="getting-files-on-an-ftp-server"></a><span data-ttu-id="0df5e-239">Obtendo arquivos em um servidor FTP</span><span class="sxs-lookup"><span data-stu-id="0df5e-239">Getting Files on an FTP Server</span></span>

<span data-ttu-id="0df5e-240">Há três métodos para recuperar arquivos de um servidor FTP:</span><span class="sxs-lookup"><span data-stu-id="0df5e-240">There are three methods for retrieving files from an FTP server:</span></span>

-   <span data-ttu-id="0df5e-241">Use [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) e [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span><span class="sxs-lookup"><span data-stu-id="0df5e-241">Use [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span>
-   <span data-ttu-id="0df5e-242">Use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) e [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span><span class="sxs-lookup"><span data-stu-id="0df5e-242">Use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span>
-   <span data-ttu-id="0df5e-243">Use [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea).</span><span class="sxs-lookup"><span data-stu-id="0df5e-243">Use [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea).</span></span>

<span data-ttu-id="0df5e-244">Para obter mais informações sobre como usar a função [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) , consulte [lendo arquivos](common-functions.md).</span><span class="sxs-lookup"><span data-stu-id="0df5e-244">For more information about using the [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) function, see [Reading Files](common-functions.md).</span></span>

<span data-ttu-id="0df5e-245">Se a URL do arquivo estiver disponível, o aplicativo poderá chamar [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) para se conectar a essa URL e, em seguida, usar [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) para controlar o download do arquivo.</span><span class="sxs-lookup"><span data-stu-id="0df5e-245">If the URL of the file is available, the application can call [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) to connect to that URL, then use [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) to control the download of the file.</span></span> <span data-ttu-id="0df5e-246">Isso permite o controle mais rígido do aplicativo sobre o download e é ideal para situações em que nenhuma outra operação precisa ser feita no servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="0df5e-246">This allows the application tighter control over the download and is ideal for situations where no other operations need to be made on the FTP server.</span></span> <span data-ttu-id="0df5e-247">Para obter mais informações sobre como acessar recursos diretamente, consulte [acessando URLs diretamente](handling-uniform-resource-locators.md).</span><span class="sxs-lookup"><span data-stu-id="0df5e-247">For more information about how to directly access resources, see [Accessing URLs Directly](handling-uniform-resource-locators.md).</span></span>

<span data-ttu-id="0df5e-248">Se o aplicativo tiver estabelecido um identificador de sessão de FTP para o servidor com [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), o aplicativo poderá chamar [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) com o nome de arquivo existente e com um novo nome para o arquivo armazenado localmente.</span><span class="sxs-lookup"><span data-stu-id="0df5e-248">If the application has established an FTP session handle to the server with [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), the application can call [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) with the existing file name and with a new name for the locally stored file.</span></span> <span data-ttu-id="0df5e-249">Em seguida, o aplicativo pode usar [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) para baixar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="0df5e-249">The application can then use [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) to download the file.</span></span> <span data-ttu-id="0df5e-250">Isso permite o controle mais rígido do aplicativo sobre o download e mantém a conexão com o servidor FTP, para que mais comandos possam ser executados.</span><span class="sxs-lookup"><span data-stu-id="0df5e-250">This allows the application tighter control over the download and keeps the connection to the FTP server, so more commands can be executed.</span></span>

<span data-ttu-id="0df5e-251">Se o aplicativo não precisar de controle rígido sobre o download, o aplicativo poderá usar o [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) com o identificador de sessão de FTP, o nome do arquivo remoto e o nome do arquivo local para recuperar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="0df5e-251">If the application does not need tight control over the download, the application can use [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) with the FTP session handle, remote file name, and local file name to retrieve the file.</span></span> <span data-ttu-id="0df5e-252">O [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) executa toda a escrituração e a contabilização associada à leitura de um arquivo de um servidor FTP e ao armazená-lo localmente.</span><span class="sxs-lookup"><span data-stu-id="0df5e-252">[**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) performs all the bookkeeping and overhead associated with reading a file from an FTP server and storing it locally.</span></span>

<span data-ttu-id="0df5e-253">O exemplo a seguir recupera um arquivo de um servidor FTP e o salva localmente.</span><span class="sxs-lookup"><span data-stu-id="0df5e-253">The following example retrieves a file from an FTP server and saves it locally.</span></span> <span data-ttu-id="0df5e-254">O nome do arquivo no servidor de FTP é obtido da caixa de edição no diálogo pai cuja IDC é passada no parâmetro *nFtpFileNameId* e o nome local no qual o arquivo é salvo é obtido da caixa de edição cuja IDC é passada no parâmetro *nLocalFileNameId* .</span><span class="sxs-lookup"><span data-stu-id="0df5e-254">The name of the file on the FTP server is taken from the edit box in the parent dialog whose IDC is passed in the *nFtpFileNameId* parameter, and the local name under which the file is saved is taken from the edit box whose IDC is passed in the *nLocalFileNameId* parameter.</span></span> <span data-ttu-id="0df5e-255">O identificador *hConnection* foi criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) depois de estabelecer uma sessão FTP.</span><span class="sxs-lookup"><span data-stu-id="0df5e-255">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span>


```C++
BOOL WINAPI GetFtpFile( HWND hDlg, HINTERNET hConnection,
                        int nFtpFileNameId, int nLocalFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szLocalFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  DWORD dwTransferType;
  TCHAR szBoxTitle[] = TEXT( "Download FTP File" );
  TCHAR szAsciiQuery[] =
    TEXT("Do you want to download as ASCII text?(Default is binary)");
  TCHAR szAsciiDone[] = 
    TEXT( "ASCII Transfer completed successfully..." );
  TCHAR szBinaryDone[] = 
    TEXT( "Binary Transfer completed successfully..." );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nLocalFileNameId, szLocalFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Target File or Destination File Missing" ),
                szBoxTitle, 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  dwTransferType = ( MessageBox( hDlg, 
                                 szAsciiQuery, 
                                 szBoxTitle, 
                                 MB_YESNO ) == IDYES ) ?
                   FTP_TRANSFER_TYPE_ASCII : FTP_TRANSFER_TYPE_BINARY;
  dwTransferType |= INTERNET_FLAG_RELOAD;

  if( !FtpGetFile( hConnection, szFtpFileName, szLocalFileName, FALSE,
                   FILE_ATTRIBUTE_NORMAL, dwTransferType, 0 ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), TEXT( "FtpGetFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg,( dwTransferType == 
                      (FTP_TRANSFER_TYPE_ASCII | INTERNET_FLAG_RELOAD)) ?
                      szAsciiDone : szBinaryDone, szBoxTitle, MB_OK );
  return( TRUE );
}
```



### <a name="placing-files-on-an-ftp-server"></a><span data-ttu-id="0df5e-256">Colocando arquivos em um servidor FTP</span><span class="sxs-lookup"><span data-stu-id="0df5e-256">Placing Files on an FTP Server</span></span>

<span data-ttu-id="0df5e-257">Há dois métodos para colocar um arquivo em um servidor FTP:</span><span class="sxs-lookup"><span data-stu-id="0df5e-257">There are two methods for placing a file on an FTP server:</span></span>

-   <span data-ttu-id="0df5e-258">Use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) com [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile).</span><span class="sxs-lookup"><span data-stu-id="0df5e-258">Use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) with [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile).</span></span>
-   <span data-ttu-id="0df5e-259">Use [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span><span class="sxs-lookup"><span data-stu-id="0df5e-259">Use [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span></span>

<span data-ttu-id="0df5e-260">Um aplicativo que deve enviar dados para um servidor FTP, mas que não tem um arquivo local que contém todos os dados, deve usar [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) para criar e abrir um arquivo no servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="0df5e-260">An application that must send data to an FTP server, but does not have a local file that contains all the data, should use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) to create and open a file on the ftp server.</span></span> <span data-ttu-id="0df5e-261">Em seguida, o aplicativo pode usar [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) para carregar as informações no arquivo.</span><span class="sxs-lookup"><span data-stu-id="0df5e-261">The application then can use [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) to upload the information to the file.</span></span>

<span data-ttu-id="0df5e-262">Se o arquivo já existir localmente, o aplicativo poderá usar [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) para carregar o arquivo no servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="0df5e-262">If the file already exists locally, the application can use [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) to upload the file to the FTP server.</span></span> <span data-ttu-id="0df5e-263">O [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) executa toda a sobrecarga que acompanha o carregamento de um arquivo local para um servidor FTP remoto.</span><span class="sxs-lookup"><span data-stu-id="0df5e-263">[**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) performs all the overhead that goes with uploading a local file to a remote FTP server.</span></span>

<span data-ttu-id="0df5e-264">O exemplo a seguir copia um arquivo local no servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="0df5e-264">The following example copies a local file onto the FTP server.</span></span> <span data-ttu-id="0df5e-265">O nome local do arquivo é obtido da caixa de edição no diálogo pai cuja IDC é passada no parâmetro *nLocalFileNameId* e o nome no qual o arquivo é salvo no servidor FTP é obtido da caixa de edição cuja IDC é passada no parâmetro *nFtpFileNameId* .</span><span class="sxs-lookup"><span data-stu-id="0df5e-265">The local name of the file is taken from the edit box in the parent dialog whose IDC is passed in the *nLocalFileNameId* parameter, and the name under which the file is saved on the FTP server is taken from the edit box whose IDC is passed in the *nFtpFileNameId* parameter.</span></span> <span data-ttu-id="0df5e-266">O identificador *hConnection* foi criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) depois de estabelecer uma sessão FTP.</span><span class="sxs-lookup"><span data-stu-id="0df5e-266">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span>


```C++
BOOL WINAPI PutFtpFile( HWND hDlg, HINTERNET hConnection,
                        int nFtpFileNameId, int nLocalFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szLocalFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  DWORD dwTransferType;
  TCHAR szBoxTitle[] = TEXT( "Upload FTP File" );
  TCHAR szASCIIQuery[] =
    TEXT("Do you want to upload as ASCII text? (Default is binary)");
  TCHAR szAsciiDone[] = 
    TEXT( "ASCII Transfer completed successfully..." );
  TCHAR szBinaryDone[] = 
    TEXT( "Binary Transfer completed successfully..." );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nLocalFileNameId, szLocalFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT("Target File or Destination File Missing"),
                szBoxTitle, 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  dwTransferType =
    ( MessageBox( hDlg, 
                  szASCIIQuery, 
                  szBoxTitle, 
                  MB_YESNO ) == IDYES ) ?
    FTP_TRANSFER_TYPE_ASCII : FTP_TRANSFER_TYPE_BINARY;

  if( !FtpPutFile( hConnection, 
                   szLocalFileName, 
                   szFtpFileName, 
                   dwTransferType, 
                   0 ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), TEXT( "FtpGetFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg,
              ( dwTransferType == FTP_TRANSFER_TYPE_ASCII ) ?
                szAsciiDone : szBinaryDone, szBoxTitle, MB_OK );
  return( TRUE );  // Remember to refresh directory listing
}
```



### <a name="deleting-files-from-an-ftp-server"></a><span data-ttu-id="0df5e-267">Excluindo arquivos de um servidor FTP</span><span class="sxs-lookup"><span data-stu-id="0df5e-267">Deleting Files from an FTP Server</span></span>

<span data-ttu-id="0df5e-268">Para excluir um arquivo de um servidor FTP, use a função [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) .</span><span class="sxs-lookup"><span data-stu-id="0df5e-268">To delete a file from an FTP server, use the [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) function.</span></span> <span data-ttu-id="0df5e-269">O aplicativo de chamada deve ter os privilégios necessários para excluir um arquivo do servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="0df5e-269">The calling application must have the necessary privileges to delete a file from the FTP server.</span></span>

<span data-ttu-id="0df5e-270">O exemplo a seguir exclui um arquivo do servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="0df5e-270">The following example deletes a file from the FTP server.</span></span> <span data-ttu-id="0df5e-271">O nome do arquivo a ser excluído é obtido da caixa de edição no diálogo pai cuja IDC é passada para o parâmetro *nFtpFileNameId* .</span><span class="sxs-lookup"><span data-stu-id="0df5e-271">The name of the file to be deleted is taken from the edit box in the parent dialog whose IDC is passed int the *nFtpFileNameId* parameter.</span></span> <span data-ttu-id="0df5e-272">O identificador *hConnection* foi criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) depois de estabelecer uma sessão FTP.</span><span class="sxs-lookup"><span data-stu-id="0df5e-272">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="0df5e-273">Como essa função não atualiza listagens de arquivos ou exibição de diretório, o processo de chamada deve fazer isso após a exclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0df5e-273">Since this function does not refresh file listings or directory display, the calling process should do so upon successful deletion.</span></span>


```C++
BOOL WINAPI DeleteFtpFile( HWND hDlg, HINTERNET hConnection,
                           int nFtpFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szBoxTitle[] = TEXT( "Delete FTP File" );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, TEXT( "File Name Must Be Specified!" ),
                szBoxTitle, MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpDeleteFile( hConnection, szFtpFileName ) )
  {
    InternetErrorOut( hDlg, 
                      GetLastError( ), 
                      TEXT( "FtpDeleteFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg, 
              TEXT( "File has been deleted" ), 
              szBoxTitle, 
              MB_OK );
  return( TRUE );  // Remember to refresh directory listing
}
```



### <a name="renaming-files-and-directories-on-an-ftp-server"></a><span data-ttu-id="0df5e-274">Renomeando arquivos e diretórios em um servidor FTP</span><span class="sxs-lookup"><span data-stu-id="0df5e-274">Renaming Files and Directories on an FTP Server</span></span>

<span data-ttu-id="0df5e-275">Os arquivos e diretórios em um servidor FTP podem ser renomeados usando a função [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) .</span><span class="sxs-lookup"><span data-stu-id="0df5e-275">Files and directories on an FTP server can be renamed using the [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) function.</span></span> <span data-ttu-id="0df5e-276">[**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) aceita duas cadeias de caracteres terminadas em **nulo** que contêm nomes parcialmente ou totalmente qualificados relativos ao diretório atual.</span><span class="sxs-lookup"><span data-stu-id="0df5e-276">[**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) accepts two **null**-terminated strings that contain either partially or fully qualified names relative to the current directory.</span></span> <span data-ttu-id="0df5e-277">A função altera o nome do arquivo designado pela primeira cadeia de caracteres para o nome designado pela segunda cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0df5e-277">The function changes the name of the file designated by the first string to the name designated by the second string.</span></span>

<span data-ttu-id="0df5e-278">O exemplo a seguir renomeia um arquivo ou diretório no servidor FTP.</span><span class="sxs-lookup"><span data-stu-id="0df5e-278">The following example renames a file or directory on the FTP server.</span></span> <span data-ttu-id="0df5e-279">O nome atual do arquivo ou diretório é obtido da caixa de edição no diálogo pai cuja IDC é passada no parâmetro *nOldFileNameId* e o novo nome é obtido da caixa de edição cuja IDC é passada no parâmetro *nNewFileNameId* .</span><span class="sxs-lookup"><span data-stu-id="0df5e-279">The current name of the file or directory is taken from the edit box in the parent dialog whose IDC is passed in the *nOldFileNameId* parameter, and the new name is taken from the edit box whose IDC is passed in the *nNewFileNameId* parameter.</span></span> <span data-ttu-id="0df5e-280">O identificador *hConnection* foi criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) depois de estabelecer uma sessão FTP.</span><span class="sxs-lookup"><span data-stu-id="0df5e-280">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="0df5e-281">Como essa função não atualiza listagens de arquivos ou exibição de diretório, o processo de chamada deve fazer isso após a renomeação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0df5e-281">Since this function does not refresh file listings or directory display, the calling process should do so upon successful renaming.</span></span>


```C++
BOOL WINAPI RenameFtpFile( HWND hDlg, HINTERNET hConnection,
                           int nOldFileNameId, int nNewFileNameId )
{
  TCHAR szOldFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szNewFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szBoxTitle[] = TEXT( "Rename FTP File" );

  if( !GetDlgItemText( hDlg, nOldFileNameId, szOldFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nNewFileNameId, szNewFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg,
        TEXT( "Both the current and new file names must be supplied" ),
        szBoxTitle, 
        MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpRenameFile( hConnection, szOldFileName, szNewFileName ) )
  {
    MessageBox( hDlg,
        TEXT( "FtpRenameFile failed" ),
        szBoxTitle, 
        MB_OK | MB_ICONERROR );
    return( FALSE );
  }
  return( TRUE );  // Remember to refresh directory listing
}
```



> [!Note]  
> <span data-ttu-id="0df5e-282">O WinINet não oferece suporte a implementações de servidor.</span><span class="sxs-lookup"><span data-stu-id="0df5e-282">WinINet does not support server implementations.</span></span> <span data-ttu-id="0df5e-283">Além disso, ele não deve ser usado de um serviço.</span><span class="sxs-lookup"><span data-stu-id="0df5e-283">In addition, it should not be used from a service.</span></span> <span data-ttu-id="0df5e-284">Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="0df5e-284">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 