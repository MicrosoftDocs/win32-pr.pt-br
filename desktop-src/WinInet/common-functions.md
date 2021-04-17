---
title: Funções comuns (Internet do Windows)
description: Os diferentes protocolos de Internet (como FTP e http) usam várias das mesmas funções do WinINet para lidar com informações na Internet.
ms.assetid: c80768cf-c8c0-4bdf-9ea2-f82c92ade05a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1893b085da1b3e77228e4a9abf75acc166d84726
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105762127"
---
# <a name="common-functions-windows-internet"></a><span data-ttu-id="e4c35-103">Funções comuns (Internet do Windows)</span><span class="sxs-lookup"><span data-stu-id="e4c35-103">Common Functions (Windows Internet)</span></span>

<span data-ttu-id="e4c35-104">Os diferentes protocolos de Internet (como FTP e http) usam várias das mesmas funções do WinINet para lidar com informações na Internet.</span><span class="sxs-lookup"><span data-stu-id="e4c35-104">The different Internet protocols (such as ftp and http) use several of the same WinINet functions to handle information on the Internet.</span></span> <span data-ttu-id="e4c35-105">Essas funções comuns manipulam suas tarefas de maneira consistente, independentemente do protocolo específico ao qual estão sendo aplicadas.</span><span class="sxs-lookup"><span data-stu-id="e4c35-105">These common functions handle their tasks in a consistent manner, regardless of the particular protocol to which they are being applied.</span></span> <span data-ttu-id="e4c35-106">Os aplicativos podem usar essas funções para criar funções de uso geral que manipulam tarefas em diferentes protocolos (como leitura de arquivos para FTP e http).</span><span class="sxs-lookup"><span data-stu-id="e4c35-106">Applications can use these functions to create general-purpose functions that handle tasks across the different protocols (such as reading files for ftp and http).</span></span>

<span data-ttu-id="e4c35-107">As funções comuns manipulam as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="e4c35-107">The common functions handle the following tasks:</span></span>

-   <span data-ttu-id="e4c35-108">Baixando recursos da Internet ([**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)e [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)).</span><span class="sxs-lookup"><span data-stu-id="e4c35-108">Downloading resources from the Internet ([**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), and [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)).</span></span>
-   <span data-ttu-id="e4c35-109">Configurando operações assíncronas ([**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)).</span><span class="sxs-lookup"><span data-stu-id="e4c35-109">Setting up asynchronous operations ([**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)).</span></span>
-   <span data-ttu-id="e4c35-110">Exibindo e alterando opções ([**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) e [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)).</span><span class="sxs-lookup"><span data-stu-id="e4c35-110">Viewing and changing options ([**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) and [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)).</span></span>
-   <span data-ttu-id="e4c35-111">Fechando todos os tipos de identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) ([**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle)).</span><span class="sxs-lookup"><span data-stu-id="e4c35-111">Closing all types of [**HINTERNET**](appendix-a-hinternet-handles.md) handles ([**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle)).</span></span>
-   <span data-ttu-id="e4c35-112">Colocando e removendo bloqueios em recursos ([**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) e [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)).</span><span class="sxs-lookup"><span data-stu-id="e4c35-112">Placing and removing locks on resources ([**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) and [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)).</span></span>

## <a name="using-common-functions"></a><span data-ttu-id="e4c35-113">Usando funções comuns</span><span class="sxs-lookup"><span data-stu-id="e4c35-113">Using Common Functions</span></span>

<span data-ttu-id="e4c35-114">A tabela a seguir lista as funções comuns incluídas nas funções do WinINet.</span><span class="sxs-lookup"><span data-stu-id="e4c35-114">The following table lists the common functions included in the WinINet functions.</span></span> <span data-ttu-id="e4c35-115">As funções comuns podem ser usadas em diferentes tipos de identificadores [**HINTERNET**](appendix-a-hinternet-handles.md) ou podem ser usadas durante diferentes tipos de sessões.</span><span class="sxs-lookup"><span data-stu-id="e4c35-115">The common functions can be used on different types of [**HINTERNET**](appendix-a-hinternet-handles.md) handles or can be used during different types of sessions.</span></span>



| <span data-ttu-id="e4c35-116">Função</span><span class="sxs-lookup"><span data-stu-id="e4c35-116">Function</span></span>                                                         | <span data-ttu-id="e4c35-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="e4c35-117">Description</span></span>                                                                                                                                                                                                                                             |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4c35-118">**InternetFindNextFile**</span><span class="sxs-lookup"><span data-stu-id="e4c35-118">**InternetFindNextFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)             | <span data-ttu-id="e4c35-119">Continua a enumeração ou a pesquisa de arquivos.</span><span class="sxs-lookup"><span data-stu-id="e4c35-119">Continues file enumeration or search.</span></span> <span data-ttu-id="e4c35-120">Requer um identificador criado pela função [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)ou [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="e4c35-120">Requires a handle created by the [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span>                                                                            |
| [<span data-ttu-id="e4c35-121">**InternetLockRequestFile**</span><span class="sxs-lookup"><span data-stu-id="e4c35-121">**InternetLockRequestFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile)       | <span data-ttu-id="e4c35-122">Permite que o usuário Coloque um bloqueio no arquivo que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="e4c35-122">Allows the user to place a lock on the file that is being used.</span></span> <span data-ttu-id="e4c35-123">Essa função requer um identificador retornado pela função [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)ou [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="e4c35-123">This function requires a handle returned by the [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span> |
| [<span data-ttu-id="e4c35-124">**InternetQueryDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="e4c35-124">**InternetQueryDataAvailable**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) | <span data-ttu-id="e4c35-125">Recupera a quantidade de dados disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e4c35-125">Retrieves the amount of data available.</span></span> <span data-ttu-id="e4c35-126">Requer um identificador criado pela função [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .</span><span class="sxs-lookup"><span data-stu-id="e4c35-126">Requires a handle created by the [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function.</span></span>                                                                                    |
| [<span data-ttu-id="e4c35-127">**InternetQueryOption**</span><span class="sxs-lookup"><span data-stu-id="e4c35-127">**InternetQueryOption**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)               | <span data-ttu-id="e4c35-128">Recupera a configuração de uma opção da Internet.</span><span class="sxs-lookup"><span data-stu-id="e4c35-128">Retrieves the setting of an Internet option.</span></span>                                                                                                                                                                                                            |
| [<span data-ttu-id="e4c35-129">**InternetReadFile**</span><span class="sxs-lookup"><span data-stu-id="e4c35-129">**InternetReadFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)                     | <span data-ttu-id="e4c35-130">Lê dados de URL.</span><span class="sxs-lookup"><span data-stu-id="e4c35-130">Reads URL data.</span></span> <span data-ttu-id="e4c35-131">Requer um identificador criado pela função [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .</span><span class="sxs-lookup"><span data-stu-id="e4c35-131">Requires a handle created by the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function.</span></span>                                                                |
| [<span data-ttu-id="e4c35-132">**InternetSetFilePointer**</span><span class="sxs-lookup"><span data-stu-id="e4c35-132">**InternetSetFilePointer**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)         | <span data-ttu-id="e4c35-133">Define a posição da próxima leitura em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="e4c35-133">Sets the position for the next read in a file.</span></span> <span data-ttu-id="e4c35-134">Requer um identificador criado por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (somente em uma URL http) ou um identificador criado pelo [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usando o verbo HTTP Get.</span><span class="sxs-lookup"><span data-stu-id="e4c35-134">Requires a handle created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (on an HTTP URL only) or a handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) using the GET HTTP verb.</span></span>                 |
| [<span data-ttu-id="e4c35-135">**InternetSetOption**</span><span class="sxs-lookup"><span data-stu-id="e4c35-135">**InternetSetOption**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)                   | <span data-ttu-id="e4c35-136">Define uma opção da Internet.</span><span class="sxs-lookup"><span data-stu-id="e4c35-136">Sets an Internet option.</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="e4c35-137">**InternetSetStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="e4c35-137">**InternetSetStatusCallback**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)   | <span data-ttu-id="e4c35-138">Define uma função de retorno de chamada que recebe informações de status.</span><span class="sxs-lookup"><span data-stu-id="e4c35-138">Sets a callback function that receives status information.</span></span> <span data-ttu-id="e4c35-139">Atribui uma função de retorno de chamada ao identificador [**HINTERNET**](appendix-a-hinternet-handles.md) designado e a todos os identificadores derivados dele.</span><span class="sxs-lookup"><span data-stu-id="e4c35-139">Assigns a callback function to the designated [**HINTERNET**](appendix-a-hinternet-handles.md) handle and all handles derived from it.</span></span>                                                      |
| [<span data-ttu-id="e4c35-140">**InternetUnlockRequestFile**</span><span class="sxs-lookup"><span data-stu-id="e4c35-140">**InternetUnlockRequestFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)   | <span data-ttu-id="e4c35-141">Desbloqueia um arquivo que foi bloqueado usando a função [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) .</span><span class="sxs-lookup"><span data-stu-id="e4c35-141">Unlocks a file that was locked using the [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) function.</span></span>                                                                                                                                           |



 

<span data-ttu-id="e4c35-142">A leitura de arquivos, a localização do próximo arquivo, a manipulação de opções e a configuração de operações assíncronas são comuns às funções que dão suporte a vários protocolos e tipos de identificadores [**HINTERNET**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="e4c35-142">Reading files, finding the next file, manipulating options, and setting up asynchronous operations are common to the functions that support various protocols and [**HINTERNET**](appendix-a-hinternet-handles.md) handle types.</span></span>

### <a name="reading-files"></a><span data-ttu-id="e4c35-143">Lendo arquivos</span><span class="sxs-lookup"><span data-stu-id="e4c35-143">Reading Files</span></span>

<span data-ttu-id="e4c35-144">A função [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) é usada para baixar recursos de um identificador [**HINTERNET**](appendix-a-hinternet-handles.md) retornado pela função [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .</span><span class="sxs-lookup"><span data-stu-id="e4c35-144">The [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) function is used to download resources from an [**HINTERNET**](appendix-a-hinternet-handles.md) handle returned by the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function.</span></span>

<span data-ttu-id="e4c35-145">[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) aceita uma variável de ponteiro void que contém o endereço de um buffer e um ponteiro para uma variável que contém o comprimento do buffer.</span><span class="sxs-lookup"><span data-stu-id="e4c35-145">[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) accepts a void pointer variable that contains the address of a buffer and a pointer to a variable that contains the length of the buffer.</span></span> <span data-ttu-id="e4c35-146">A função retorna os dados no buffer e a quantidade de dados baixados no buffer.</span><span class="sxs-lookup"><span data-stu-id="e4c35-146">The function returns the data in the buffer and the amount of data downloaded into the buffer.</span></span>

<span data-ttu-id="e4c35-147">As funções do WinINet fornecem duas técnicas para baixar um recurso inteiro:</span><span class="sxs-lookup"><span data-stu-id="e4c35-147">The WinINet functions provide two techniques to download an entire resource:</span></span>

-   <span data-ttu-id="e4c35-148">A função [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) .</span><span class="sxs-lookup"><span data-stu-id="e4c35-148">The [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) function.</span></span>
-   <span data-ttu-id="e4c35-149">Os valores de retorno de [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span><span class="sxs-lookup"><span data-stu-id="e4c35-149">The return values of [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span>

<span data-ttu-id="e4c35-150">[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) usa o identificador [**HINTERNET**](appendix-a-hinternet-handles.md) criado por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (depois que [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) é chamado no identificador) e retorna o número de bytes disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e4c35-150">[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) takes the [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (after [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) has been called on the handle) and returns the number of bytes available.</span></span> <span data-ttu-id="e4c35-151">O aplicativo deve alocar um buffer igual ao número de bytes disponíveis, mais 1 para o caractere **nulo** de terminação e usar esse buffer com [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span><span class="sxs-lookup"><span data-stu-id="e4c35-151">The application should allocate a buffer equal to the number of bytes available, plus 1 for the terminating **null** character, and use that buffer with [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span> <span data-ttu-id="e4c35-152">Esse método nem sempre funciona porque [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) está verificando o tamanho do arquivo listado no cabeçalho e não o arquivo real.</span><span class="sxs-lookup"><span data-stu-id="e4c35-152">This method does not always work because [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) is checking the file size listed in the header and not the actual file.</span></span> <span data-ttu-id="e4c35-153">As informações no arquivo de cabeçalho podem estar desatualizadas ou o arquivo de cabeçalho pode estar ausente, pois ele não é necessário atualmente em todos os padrões.</span><span class="sxs-lookup"><span data-stu-id="e4c35-153">The information in the header file could be outdated, or the header file could be missing, since it is not currently required under all standards.</span></span>

<span data-ttu-id="e4c35-154">O exemplo a seguir lê o conteúdo do recurso acessado pelo identificador hResource e é exibido na caixa de edição indicada por intCtrlID.</span><span class="sxs-lookup"><span data-stu-id="e4c35-154">The following example reads the contents of the resource accessed by the hResource handle and displayed in the edit box indicated by intCtrlID.</span></span>


```C++
int WINAPI Dumper(HWND hX, int intCtrlID, HINTERNET hResource)
{
    LPTSTR    lpszData;           // buffer for the data
    DWORD     dwSize;             // size of the data available
    DWORD     dwDownloaded;       // size of the downloaded data
    DWORD     dwSizeSum=0;        // size of the data in the text box
    LPTSTR    lpszHolding;        // buffer to merge the text box 
                                  // data and buffer

    // Set the cursor to an hourglass.
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    // This loop handles reading the data.  
    do
    {
        // The call to InternetQueryDataAvailable determines the
        // amount of data available to download.
        if (!InternetQueryDataAvailable(hResource,&dwSize,0,0))
        {
            ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
        {    
            // Allocate a buffer of the size returned by
            // InternetQueryDataAvailable.
            lpszData = new TCHAR[dwSize+1];

            // Read the data from the HINTERNET handle.
            if(!InternetReadFile(hResource,(LPVOID)lpszData,
                                 dwSize,&dwDownloaded))
            {
                ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
                delete[] lpszData;
                break;
            }
            else
            {
                // Add a null terminator to the end of the 
                // data buffer.
                lpszData[dwDownloaded]='\0';

                // Allocate the holding buffer.
                lpszHolding = new TCHAR[dwSizeSum + dwDownloaded + 1];
                    
                // Check if there has been any data written to 
                // the text box.
                if (dwSizeSum != 0)
                {
                    // Retrieve the data stored in the text 
                    // box, if any.
                    GetDlgItemText(hX,intCtrlID,
                                   (LPTSTR)lpszHolding, 
                                   dwSizeSum);
                         
                    // Add a null terminator at the end of 
                    // the text box data.
                    lpszHolding[dwSizeSum]='\0';
                }
                else
                {
                    // Make the holding buffer an empty string. 
                    lpszHolding[0]='\0';
                }

                size_t cchDest = dwSizeSum + dwDownloaded + 
                                 dwDownloaded + 1;
                LPTSTR pszDestEnd;
                size_t cchRemaining;

                // Add the new data to the holding buffer.
                HRESULT hr = StringCchCatEx(lpszHolding, cchDest, 
                                            lpszData, &pszDestEnd, 
                                            &cchRemaining, 
                                            STRSAFE_NO_TRUNCATION);
                if(SUCCEEDED(hr))
                {
                    // Write the holding buffer to the text box.
                    SetDlgItemText(hX,intCtrlID,(LPTSTR)lpszHolding);

                    // Delete the two buffers.
                    delete[] lpszHolding;
                    delete[] lpszData;

                    // Add the size of the downloaded data to 
                    // the text box data size.
                    dwSizeSum = dwSizeSum + dwDownloaded + 1;

                    // Check the size of the remaining data.  
                    // If it is zero, break.
                    if (dwDownloaded == 0)
                    {
                        break;
                    }                    
                    else
                    {
                        //  Insert error handling code here.
                    }
                }
            }
        }
    }
    while(TRUE);

    // Close the HINTERNET handle.
    InternetCloseHandle(hResource);

    // Set the cursor back to an arrow.
    SetCursor(LoadCursor(NULL,IDC_ARROW));

    // Return.
    return TRUE;
}
```



<span data-ttu-id="e4c35-155">[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) retorna zero bytes lidos e concluídos com êxito quando todos os dados disponíveis tiverem sido lidos.</span><span class="sxs-lookup"><span data-stu-id="e4c35-155">[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) returns zero bytes read and completes successfully when all available data has been read.</span></span> <span data-ttu-id="e4c35-156">Isso permite que um aplicativo use [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) em um loop para baixar os dados e sair quando retorna zero bytes lidos e concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="e4c35-156">This allows an application to use [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) in a loop to download the data and exit when it returns zero bytes read and completes successfully.</span></span>

<span data-ttu-id="e4c35-157">O exemplo a seguir lê o recurso da Internet e exibe o recurso na caixa de edição indicada por intCtrlID.</span><span class="sxs-lookup"><span data-stu-id="e4c35-157">The following example reads the resource from the Internet and displays the resource in the edit box indicated by intCtrlID.</span></span> <span data-ttu-id="e4c35-158">O identificador [**HINTERNET**](appendix-a-hinternet-handles.md) , HINTERNET, foi retornado por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (depois de ser enviado por [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)).</span><span class="sxs-lookup"><span data-stu-id="e4c35-158">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle, hInternet, was returned by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (after being sent by [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)).</span></span>


```C++
int WINAPI Dump(HWND hX, int intCtrlID, HINTERNET hResource)
{
     DWORD dwSize = 0;
     LPTSTR lpszData;
     LPTSTR lpszOutPut;
     LPTSTR lpszHolding = TEXT("");
     int nCounter = 1;
     int nBufferSize = 0;
     DWORD BigSize = 8000;

     // Set the cursor to an hourglass.
     SetCursor(LoadCursor(NULL,IDC_WAIT));

     // Begin the loop that reads the data.
     do
     {
          // Allocate the buffer.
          lpszData =new TCHAR[BigSize+1];

          // Read the data.
          if(!InternetReadFile(hResource,
                              (LPVOID)lpszData,
                              BigSize,&dwSize))
          {
               ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
               delete []lpszData;
               break;
          }
          else
          {
               // Add a null terminator to the end of the buffer.
               lpszData[dwSize]='\0';

               // Check if all of the data has been read.  This should
               // never get called on the first time through the loop.
               if (dwSize == 0)
               {
                    // Write the final data to the text box.
                    SetDlgItemText(hX,intCtrlID,lpszHolding);

                    // Delete the existing buffers.
                    delete [] lpszData;
                    delete [] lpszHolding;
                    break;
               }

               // Determine the buffer size to hold the new data and
               // the data already written to the text box (if any).
               nBufferSize = (nCounter*BigSize)+1;

               // Increment the number of buffers read.
               nCounter++;               

               // Allocate the output buffer.
               lpszOutPut = new TCHAR[nBufferSize];

               // Make sure the buffer is not the initial buffer.
               if(nBufferSize != int(BigSize+1))
               {
                    // Copy the data in the holding buffer.
                    StringCchCopy(lpszOutPut,nBufferSize,lpszHolding);
                    // Add error handling code here.

                    // Concatenate the new buffer with the 
                    // output buffer.
                    StringCchCat(lpszOutPut, nBufferSize, lpszData);
                    // Add error handling code here.
     
                    // Delete the holding buffer.
                    delete [] lpszHolding;
               }
               else
               {
                    // Copy the data buffer.
                    StringCchCopy(lpszOutPut, nBufferSize, lpszData);
                    // Add error handling code here.
               }

               // Allocate a holding buffer.
               lpszHolding = new TCHAR[nBufferSize]; 

               // Copy the output buffer into the holding buffer.
               memcpy(lpszHolding,lpszOutPut,nBufferSize);

               // Delete the other buffers.
               delete [] lpszData;
               delete [] lpszOutPut;

          }

     }
     while (TRUE);

     // Close the HINTERNET handle.
     InternetCloseHandle(hResource);

     // Set the cursor back to an arrow.
     SetCursor(LoadCursor(NULL,IDC_ARROW));

     // Return.
     return TRUE;
}
```



### <a name="finding-the-next-file"></a><span data-ttu-id="e4c35-159">Localizando o próximo arquivo</span><span class="sxs-lookup"><span data-stu-id="e4c35-159">Finding the Next File</span></span>

<span data-ttu-id="e4c35-160">A função [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) é usada para localizar o próximo arquivo em uma pesquisa de arquivo, usando os parâmetros de pesquisa e o identificador [**HINTERNET**](appendix-a-hinternet-handles.md) de [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)ou [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="e4c35-160">The [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) function is used to find the next file in a file search, using the search parameters and [**HINTERNET**](appendix-a-hinternet-handles.md) handle from [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="e4c35-161">Para concluir uma pesquisa de arquivo, continue a chamar [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) usando o identificador [**HINTERNET**](appendix-a-hinternet-handles.md) retornado por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)ou [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) até que a função falhe com o erro de mensagem de erro estendido [ \_ não \_ mais \_ arquivos](wininet-errors.md).</span><span class="sxs-lookup"><span data-stu-id="e4c35-161">To complete a file search, continue to call [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) using the [**HINTERNET**](appendix-a-hinternet-handles.md) handle returned by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) until the function fails with the extended error message [ERROR\_NO\_MORE\_FILES](wininet-errors.md).</span></span> <span data-ttu-id="e4c35-162">Para obter as informações de erro estendidas, chame a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="e4c35-162">To get the extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="e4c35-163">O exemplo a seguir exibe o conteúdo de um diretório FTP na caixa de listagem indicada por lstDirectory.</span><span class="sxs-lookup"><span data-stu-id="e4c35-163">The following example displays the contents of an FTP directory in the list box indicated by lstDirectory.</span></span> <span data-ttu-id="e4c35-164">O identificador [**HINTERNET**](appendix-a-hinternet-handles.md) , hConnect, é um identificador retornado pela função [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) depois que ele estabelece uma sessão de FTP.</span><span class="sxs-lookup"><span data-stu-id="e4c35-164">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle, hConnect, is a handle returned by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function after it establishes an FTP session.</span></span>


```C++
bool WINAPI DisplayDir( HWND hX, 
                        int lstDirectory, 
                        HINTERNET hConnect, 
                        DWORD dwFlag )
{
     WIN32_FIND_DATA pDirInfo;
     HINTERNET hDir;
     TCHAR DirList[MAX_PATH];

     // Set the cursor to an hourglass.
     SetCursor(LoadCursor(NULL,IDC_WAIT));

     // Reset the list box.
     SendDlgItemMessage(hX, lstDirectory,LB_RESETCONTENT,0,0);

     // Find the first file.
     hDir = FtpFindFirstFile (hConnect, TEXT ("*.*"), 
                              &pDirInfo, dwFlag, 0);
     if (!hDir)                                     
     {
          // Check if the error was because there were no files.
          if (GetLastError()  == ERROR_NO_MORE_FILES) 
          {
               // Alert user.
               MessageBox(hX, TEXT("There are no files here!!!"), 
                          TEXT("Display Dir"), MB_OK);

               // Close the HINTERNET handle.
               InternetCloseHandle(hDir);

               // Set the cursor back to an arrow.
               SetCursor(LoadCursor(NULL,IDC_ARROW));

               // Return.
               return TRUE;
          }
          else 
          {
               // Call error handler.
               ErrorOut (hX, GetLastError (), TEXT("FindFirst error: "));

               // Close the HINTERNET handle.
               InternetCloseHandle(hDir);

               // Set the cursor back to an arrow.
               SetCursor(LoadCursor(NULL,IDC_ARROW));

               // Return.
               return FALSE;
          }
     }
     else
     {
          // Write the file name to a string.
          StringCchPrintf(DirList, MAX_PATH, pDirInfo.cFileName);

          // Check the type of file.
          if (pDirInfo.dwFileAttributes == FILE_ATTRIBUTE_DIRECTORY)
          {
               // Add <DIR> to indicate that this is 
               // a directory to the user.
               StringCchCat(DirList, MAX_PATH, TEXT(" <DIR> "));
               // Add error handling code here.
          }
       
          // Add the file name (or directory) to the list box.
          SendDlgItemMessage(hX, lstDirectory, LB_ADDSTRING,
                             0, (LPARAM)DirList);
     }
     do
     {
          // Find the next file.
          if (!InternetFindNextFile (hDir, &pDirInfo))
          {
               // Check if there are no more files left. 
               if ( GetLastError() == ERROR_NO_MORE_FILES ) 
               {
                    // Close the HINTERNET handle.
                    InternetCloseHandle(hDir);

                    // Set the cursor back to an arrow.
                    SetCursor(LoadCursor(NULL,IDC_ARROW));

                    // Return.
                    return TRUE;
               }
               else
               {   
                    // Handle the error.
                    ErrorOut (hX, GetLastError(), 
                              TEXT("InternetFindNextFile"));

                    // Close the HINTERNET handle.
                    InternetCloseHandle(hDir);

                    // Set the cursor back to an arrow.
                    SetCursor(LoadCursor(NULL,IDC_ARROW));

                    // Return.
                    return FALSE;
               }
           }
           else
           {
               // Write the file name to a string.
               StringCchPrintf(DirList, MAX_PATH, pDirInfo.cFileName);

               // Check the type of file.
               if(pDirInfo.dwFileAttributes==FILE_ATTRIBUTE_DIRECTORY)
               {
                    // Add <DIR> to indicate that this is a 
                    // directory to the user.
                    StringCchCat(DirList, MAX_PATH, TEXT(" <DIR> "));
                    // Add error handling code here.
               }
     
               // Add the file name (or directory) to the list box.
               SendDlgItemMessage(hX, lstDirectory, LB_ADDSTRING,
                                  0, (LPARAM)DirList);
           }
     }
     while ( TRUE);
     
}
```



### <a name="manipulating-options"></a><span data-ttu-id="e4c35-165">Opções de manipulação</span><span class="sxs-lookup"><span data-stu-id="e4c35-165">Manipulating Options</span></span>

<span data-ttu-id="e4c35-166">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) e [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) são usados para manipular as opções de WinInet.</span><span class="sxs-lookup"><span data-stu-id="e4c35-166">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) and [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) are used to manipulate the WinINet options.</span></span>

<span data-ttu-id="e4c35-167">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) aceita uma variável que indica a opção a ser definida, um buffer para manter a configuração de opção e um ponteiro que contém o endereço da variável que contém o comprimento do buffer.</span><span class="sxs-lookup"><span data-stu-id="e4c35-167">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) accepts a variable that indicates the option to set, a buffer to hold the option setting, and a pointer that contains the address of the variable that contains the length of the buffer.</span></span>

<span data-ttu-id="e4c35-168">[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) aceita uma variável que indica a opção de recuperar, um buffer para manter a configuração de opção e um ponteiro que contém o endereço da variável que contém o comprimento do buffer.</span><span class="sxs-lookup"><span data-stu-id="e4c35-168">[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) accepts a variable that indicates the option to retrieve, a buffer to hold the option setting, and a pointer that contains the address of the variable that contains the length of the buffer.</span></span>

### <a name="setting-up-asynchronous-operations"></a><span data-ttu-id="e4c35-169">Configurando operações assíncronas</span><span class="sxs-lookup"><span data-stu-id="e4c35-169">Setting Up Asynchronous Operations</span></span>

<span data-ttu-id="e4c35-170">Por padrão, as funções do WinINet operam de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="e4c35-170">By default, the WinINet functions operate synchronously.</span></span> <span data-ttu-id="e4c35-171">Um aplicativo pode solicitar operação assíncrona definindo o [sinalizador \_ \_ assíncrono de sinalizador da Internet](api-flags.md) na chamada para a função [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) .</span><span class="sxs-lookup"><span data-stu-id="e4c35-171">An application can request asynchronous operation by setting the [INTERNET\_FLAG\_ASYNC](api-flags.md) flag in the call to the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function.</span></span> <span data-ttu-id="e4c35-172">Todas as chamadas futuras feitas em relação a identificadores derivados do identificador retornado de [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) são feitas de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="e4c35-172">All future calls made against handles derived from the handle returned from [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) are made asynchronously.</span></span>

<span data-ttu-id="e4c35-173">A lógica para a operação assíncrona versus síncrona é permitir que um aplicativo de thread único maximize sua utilização da CPU sem precisar aguardar a conclusão da e/s de rede.</span><span class="sxs-lookup"><span data-stu-id="e4c35-173">The rationale for asynchronous versus synchronous operation is to allow a single-threaded application to maximize its utilization of the CPU without having to wait for network I/O to complete.</span></span> <span data-ttu-id="e4c35-174">Portanto, dependendo da solicitação, a operação pode ser concluída de forma síncrona ou assíncrona.</span><span class="sxs-lookup"><span data-stu-id="e4c35-174">Therefore, depending on the request, the operation might complete synchronously or asynchronously.</span></span> <span data-ttu-id="e4c35-175">O aplicativo deve verificar o código de retorno.</span><span class="sxs-lookup"><span data-stu-id="e4c35-175">The application should check the return code.</span></span> <span data-ttu-id="e4c35-176">Se uma função retornar **false** ou **NULL** e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornar uma \_ e/s \_ de erro pendente, a solicitação terá sido feita de forma assíncrona e o aplicativo será chamado de volta com a \_ solicitação de status da Internet \_ \_ concluída quando a função for concluída.</span><span class="sxs-lookup"><span data-stu-id="e4c35-176">If a function returns **FALSE** or **NULL**, and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_IO\_PENDING, the request has been made asynchronously, and the application is called back with INTERNET\_STATUS\_REQUEST\_COMPLETE when the function has completed.</span></span>

<span data-ttu-id="e4c35-177">Para iniciar a operação assíncrona, o aplicativo deve definir o sinalizador [ \_ \_ assíncrono de sinalizador da Internet](api-flags.md) em sua chamada para [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="e4c35-177">To begin asynchronous operation, the application must set the [INTERNET\_FLAG\_ASYNC](api-flags.md) flag in its call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="e4c35-178">O aplicativo deve então registrar uma função de retorno de chamada válida usando [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback).</span><span class="sxs-lookup"><span data-stu-id="e4c35-178">The application must then register a valid callback function, using [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback).</span></span>

<span data-ttu-id="e4c35-179">Depois que uma função de retorno de chamada é registrada para um identificador, todas as operações nesse identificador podem gerar indicações de status, desde que o valor de contexto que foi fornecido quando o identificador foi criado não fosse zero.</span><span class="sxs-lookup"><span data-stu-id="e4c35-179">After a callback function is registered for a handle, all operations on that handle can generate status indications, provided that the context value that was supplied when the handle was created was not zero.</span></span> <span data-ttu-id="e4c35-180">Fornecer um valor de contexto zero força uma operação a ser concluída de forma síncrona, mesmo que o [ \_ sinalizador \_ assíncrono da Internet](api-flags.md) tenha sido especificado em [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="e4c35-180">Providing a zero context value forces an operation to complete synchronously, even though [INTERNET\_FLAG\_ASYNC](api-flags.md) was specified in [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span>

<span data-ttu-id="e4c35-181">As indicações de status fornecem ao aplicativo comentários sobre o progresso de operações de rede, como resolver um nome de host, conectar-se a um servidor e receber dados.</span><span class="sxs-lookup"><span data-stu-id="e4c35-181">Status indications give the application feedback about the progress of network operations, such as resolving a host name, connecting to a server, and receiving data.</span></span> <span data-ttu-id="e4c35-182">Três indicações de status de finalidade especial podem ser feitas para um identificador:</span><span class="sxs-lookup"><span data-stu-id="e4c35-182">Three special-purpose status indications can be made for a handle:</span></span>

-   <span data-ttu-id="e4c35-183">\_ \_ \_ O fechamento do identificador de status da Internet é a última indicação de status feita para um identificador.</span><span class="sxs-lookup"><span data-stu-id="e4c35-183">INTERNET\_STATUS\_HANDLE\_CLOSING is the last status indication that is made for a handle.</span></span>
-   <span data-ttu-id="e4c35-184">\_ \_ \_ O identificador de status da Internet criado indica quando o identificador é criado inicialmente.</span><span class="sxs-lookup"><span data-stu-id="e4c35-184">INTERNET\_STATUS\_HANDLE\_CREATED indicates when the handle is initially created.</span></span>
-   <span data-ttu-id="e4c35-185">\_Solicitação de status da Internet \_ \_ concluída indica que uma operação assíncrona foi concluída.</span><span class="sxs-lookup"><span data-stu-id="e4c35-185">INTERNET\_STATUS\_REQUEST\_COMPLETE indicates an asynchronous operation has completed.</span></span>

<span data-ttu-id="e4c35-186">O aplicativo deve verificar a estrutura de [**\_ \_ resultados assíncronos da Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_async_result) para determinar se a operação foi bem-sucedida ou falhou após receber uma indicação de solicitação de status da Internet \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e4c35-186">The application must check the [**INTERNET\_ASYNC\_RESULT**](/windows/desktop/api/Wininet/ns-wininet-internet_async_result) structure to determine whether the operation succeeded or failed after receiving an INTERNET\_STATUS\_REQUEST\_COMPLETE indication.</span></span>

<span data-ttu-id="e4c35-187">O exemplo a seguir mostra um exemplo de uma função de chamada de retorno e uma chamada para [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) para registrar a função como a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e4c35-187">The following sample shows an example of a callback function and a call to [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) to register the function as the callback function.</span></span>


```C++
void CALLBACK InternetCallback(
    HINTERNET hInternet,
    DWORD_PTR dwcontext,
    DWORD dwInternetStatus,
    LPVOID lpvStatusInformation,
    DWORD dwStatusInformationLength
    )
{
    _tprintf(TEXT("%0xd %0xp %0xd %0xp %0xd\n"),
             hInternet,
             dwcontext,
             dwInternetStatus,
             lpvStatusInformation,
             dwStatusInformationLength);
};

INTERNET_STATUS_CALLBACK dwISC =
    InternetSetStatusCallback(hInternet, InternetCallback); 
```



### <a name="closing-hinternet-handles"></a><span data-ttu-id="e4c35-188">Fechando identificadores de HINTERNET</span><span class="sxs-lookup"><span data-stu-id="e4c35-188">Closing HINTERNET Handles</span></span>

<span data-ttu-id="e4c35-189">Todos os identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) podem ser fechados usando a função [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) .</span><span class="sxs-lookup"><span data-stu-id="e4c35-189">All [**HINTERNET**](appendix-a-hinternet-handles.md) handles can be closed by using the [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) function.</span></span> <span data-ttu-id="e4c35-190">Os aplicativos cliente devem fechar todos os identificadores de **HINTERNET** derivados do identificador **HINTERNET** que estão tentando fechar antes de chamar [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) no identificador.</span><span class="sxs-lookup"><span data-stu-id="e4c35-190">Client applications must close all **HINTERNET** handles derived from the **HINTERNET** handle they are trying to close before calling [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) on the handle.</span></span>

<span data-ttu-id="e4c35-191">O exemplo a seguir ilustra a hierarquia de identificador.</span><span class="sxs-lookup"><span data-stu-id="e4c35-191">The following example illustrates the handle hierarchy.</span></span>


```C++
HINTERNET hRootHandle, hOpenUrlHandle;

hRootHandle = InternetOpen( TEXT("Example"), 
                            INTERNET_OPEN_TYPE_DIRECT, 
                            NULL, 
                            NULL, 0);

hOpenUrlHandle = InternetOpenUrl(hRootHandle, 
    TEXT("https://www.server.com/default.htm"), NULL, 0, 
    INTERNET_FLAG_RAW_DATA,0);

// Close the handle created by InternetOpenUrl so that the
// InternetOpen handle can be closed.
InternetCloseHandle(hOpenUrlHandle); 

// Close the handle created by InternetOpen.
InternetCloseHandle(hRootHandle);
```



### <a name="locking-and-unlocking-resources"></a><span data-ttu-id="e4c35-192">Bloqueando e desbloqueando recursos</span><span class="sxs-lookup"><span data-stu-id="e4c35-192">Locking and Unlocking Resources</span></span>

<span data-ttu-id="e4c35-193">A função [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) permite que um aplicativo Verifique se o recurso em cache associado ao identificador [**HINTERNET**](appendix-a-hinternet-handles.md) passado para ele não desaparece do cache.</span><span class="sxs-lookup"><span data-stu-id="e4c35-193">The [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) function allows an application to ensure that the cached resource associated with the [**HINTERNET**](appendix-a-hinternet-handles.md) handle passed to it does not disappear from the cache.</span></span> <span data-ttu-id="e4c35-194">Se outro download tentar confirmar um recurso que tem a mesma URL que o arquivo bloqueado, o cache evita a remoção do arquivo, fazendo uma exclusão segura.</span><span class="sxs-lookup"><span data-stu-id="e4c35-194">If another download tries to commit a resource that has the same URL as the locked file, the cache avoids removing the file by doing a safe delete.</span></span> <span data-ttu-id="e4c35-195">Depois que o aplicativo chama a função [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile) , o cache recebe permissão para excluir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="e4c35-195">After the application calls the [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile) function, the cache is given permission to delete the file.</span></span>

<span data-ttu-id="e4c35-196">Se o [sinalizador \_ Internet \_ sem \_ \_ gravação do cache](api-flags.md) ou sinalizador de Internet não tiver sido definido, o [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) criará um arquivo temporário com a extensão tmp, a menos que o identificador esteja conectado a um recurso HTTPS. [ \_ \_ \_](api-flags.md)</span><span class="sxs-lookup"><span data-stu-id="e4c35-196">If the [INTERNET\_FLAG\_NO\_CACHE\_WRITE](api-flags.md) or [INTERNET\_FLAG\_DONT\_CACHE](api-flags.md) flag has been set, [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) creates a temporary file with the extension TMP, unless the handle is connected to an https resource.</span></span> <span data-ttu-id="e4c35-197">Se a função acessar um recurso HTTPS e um sinalizador de INTERNET \_ \_ sem \_ \_ gravação de cache (ou o sinalizador de Internet não \_ \_ \_ cache) tiver sido definido, [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) falhará.</span><span class="sxs-lookup"><span data-stu-id="e4c35-197">If the function accesses an https resource and INTERNET\_FLAG\_NO\_CACHE\_WRITE (or INTERNET\_FLAG\_DONT\_CACHE) has been set, [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) fails.</span></span>

> [!Note]  
> <span data-ttu-id="e4c35-198">O WinINet não oferece suporte a implementações de servidor.</span><span class="sxs-lookup"><span data-stu-id="e4c35-198">WinINet does not support server implementations.</span></span> <span data-ttu-id="e4c35-199">Além disso, ele não deve ser usado de um serviço.</span><span class="sxs-lookup"><span data-stu-id="e4c35-199">In addition, it should not be used from a service.</span></span> <span data-ttu-id="e4c35-200">Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="e4c35-200">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 
