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
# <a name="common-functions-windows-internet"></a>Funções comuns (Internet do Windows)

Os diferentes protocolos de Internet (como FTP e http) usam várias das mesmas funções do WinINet para lidar com informações na Internet. Essas funções comuns manipulam suas tarefas de maneira consistente, independentemente do protocolo específico ao qual estão sendo aplicadas. Os aplicativos podem usar essas funções para criar funções de uso geral que manipulam tarefas em diferentes protocolos (como leitura de arquivos para FTP e http).

As funções comuns manipulam as seguintes tarefas:

-   Baixando recursos da Internet ([**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)e [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)).
-   Configurando operações assíncronas ([**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)).
-   Exibindo e alterando opções ([**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) e [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)).
-   Fechando todos os tipos de identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) ([**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle)).
-   Colocando e removendo bloqueios em recursos ([**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) e [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)).

## <a name="using-common-functions"></a>Usando funções comuns

A tabela a seguir lista as funções comuns incluídas nas funções do WinINet. As funções comuns podem ser usadas em diferentes tipos de identificadores [**HINTERNET**](appendix-a-hinternet-handles.md) ou podem ser usadas durante diferentes tipos de sessões.



| Função                                                         | Descrição                                                                                                                                                                                                                                             |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)             | Continua a enumeração ou a pesquisa de arquivos. Requer um identificador criado pela função [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)ou [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .                                                                            |
| [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile)       | Permite que o usuário Coloque um bloqueio no arquivo que está sendo usado. Essa função requer um identificador retornado pela função [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)ou [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) . |
| [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) | Recupera a quantidade de dados disponíveis. Requer um identificador criado pela função [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .                                                                                    |
| [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)               | Recupera a configuração de uma opção da Internet.                                                                                                                                                                                                            |
| [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)                     | Lê dados de URL. Requer um identificador criado pela função [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .                                                                |
| [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)         | Define a posição da próxima leitura em um arquivo. Requer um identificador criado por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (somente em uma URL http) ou um identificador criado pelo [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usando o verbo HTTP Get.                 |
| [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)                   | Define uma opção da Internet.                                                                                                                                                                                                                                |
| [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)   | Define uma função de retorno de chamada que recebe informações de status. Atribui uma função de retorno de chamada ao identificador [**HINTERNET**](appendix-a-hinternet-handles.md) designado e a todos os identificadores derivados dele.                                                      |
| [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)   | Desbloqueia um arquivo que foi bloqueado usando a função [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) .                                                                                                                                           |



 

A leitura de arquivos, a localização do próximo arquivo, a manipulação de opções e a configuração de operações assíncronas são comuns às funções que dão suporte a vários protocolos e tipos de identificadores [**HINTERNET**](appendix-a-hinternet-handles.md) .

### <a name="reading-files"></a>Lendo arquivos

A função [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) é usada para baixar recursos de um identificador [**HINTERNET**](appendix-a-hinternet-handles.md) retornado pela função [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .

[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) aceita uma variável de ponteiro void que contém o endereço de um buffer e um ponteiro para uma variável que contém o comprimento do buffer. A função retorna os dados no buffer e a quantidade de dados baixados no buffer.

As funções do WinINet fornecem duas técnicas para baixar um recurso inteiro:

-   A função [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) .
-   Os valores de retorno de [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).

[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) usa o identificador [**HINTERNET**](appendix-a-hinternet-handles.md) criado por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (depois que [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) é chamado no identificador) e retorna o número de bytes disponíveis. O aplicativo deve alocar um buffer igual ao número de bytes disponíveis, mais 1 para o caractere **nulo** de terminação e usar esse buffer com [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile). Esse método nem sempre funciona porque [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) está verificando o tamanho do arquivo listado no cabeçalho e não o arquivo real. As informações no arquivo de cabeçalho podem estar desatualizadas ou o arquivo de cabeçalho pode estar ausente, pois ele não é necessário atualmente em todos os padrões.

O exemplo a seguir lê o conteúdo do recurso acessado pelo identificador hResource e é exibido na caixa de edição indicada por intCtrlID.


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



[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) retorna zero bytes lidos e concluídos com êxito quando todos os dados disponíveis tiverem sido lidos. Isso permite que um aplicativo use [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) em um loop para baixar os dados e sair quando retorna zero bytes lidos e concluído com êxito.

O exemplo a seguir lê o recurso da Internet e exibe o recurso na caixa de edição indicada por intCtrlID. O identificador [**HINTERNET**](appendix-a-hinternet-handles.md) , HINTERNET, foi retornado por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (depois de ser enviado por [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)).


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



### <a name="finding-the-next-file"></a>Localizando o próximo arquivo

A função [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) é usada para localizar o próximo arquivo em uma pesquisa de arquivo, usando os parâmetros de pesquisa e o identificador [**HINTERNET**](appendix-a-hinternet-handles.md) de [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)ou [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

Para concluir uma pesquisa de arquivo, continue a chamar [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) usando o identificador [**HINTERNET**](appendix-a-hinternet-handles.md) retornado por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)ou [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) até que a função falhe com o erro de mensagem de erro estendido [ \_ não \_ mais \_ arquivos](wininet-errors.md). Para obter as informações de erro estendidas, chame a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

O exemplo a seguir exibe o conteúdo de um diretório FTP na caixa de listagem indicada por lstDirectory. O identificador [**HINTERNET**](appendix-a-hinternet-handles.md) , hConnect, é um identificador retornado pela função [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) depois que ele estabelece uma sessão de FTP.


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



### <a name="manipulating-options"></a>Opções de manipulação

[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) e [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) são usados para manipular as opções de WinInet.

[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) aceita uma variável que indica a opção a ser definida, um buffer para manter a configuração de opção e um ponteiro que contém o endereço da variável que contém o comprimento do buffer.

[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) aceita uma variável que indica a opção de recuperar, um buffer para manter a configuração de opção e um ponteiro que contém o endereço da variável que contém o comprimento do buffer.

### <a name="setting-up-asynchronous-operations"></a>Configurando operações assíncronas

Por padrão, as funções do WinINet operam de forma síncrona. Um aplicativo pode solicitar operação assíncrona definindo o [sinalizador \_ \_ assíncrono de sinalizador da Internet](api-flags.md) na chamada para a função [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) . Todas as chamadas futuras feitas em relação a identificadores derivados do identificador retornado de [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) são feitas de forma assíncrona.

A lógica para a operação assíncrona versus síncrona é permitir que um aplicativo de thread único maximize sua utilização da CPU sem precisar aguardar a conclusão da e/s de rede. Portanto, dependendo da solicitação, a operação pode ser concluída de forma síncrona ou assíncrona. O aplicativo deve verificar o código de retorno. Se uma função retornar **false** ou **NULL** e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornar uma \_ e/s \_ de erro pendente, a solicitação terá sido feita de forma assíncrona e o aplicativo será chamado de volta com a \_ solicitação de status da Internet \_ \_ concluída quando a função for concluída.

Para iniciar a operação assíncrona, o aplicativo deve definir o sinalizador [ \_ \_ assíncrono de sinalizador da Internet](api-flags.md) em sua chamada para [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). O aplicativo deve então registrar uma função de retorno de chamada válida usando [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback).

Depois que uma função de retorno de chamada é registrada para um identificador, todas as operações nesse identificador podem gerar indicações de status, desde que o valor de contexto que foi fornecido quando o identificador foi criado não fosse zero. Fornecer um valor de contexto zero força uma operação a ser concluída de forma síncrona, mesmo que o [ \_ sinalizador \_ assíncrono da Internet](api-flags.md) tenha sido especificado em [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).

As indicações de status fornecem ao aplicativo comentários sobre o progresso de operações de rede, como resolver um nome de host, conectar-se a um servidor e receber dados. Três indicações de status de finalidade especial podem ser feitas para um identificador:

-   \_ \_ \_ O fechamento do identificador de status da Internet é a última indicação de status feita para um identificador.
-   \_ \_ \_ O identificador de status da Internet criado indica quando o identificador é criado inicialmente.
-   \_Solicitação de status da Internet \_ \_ concluída indica que uma operação assíncrona foi concluída.

O aplicativo deve verificar a estrutura de [**\_ \_ resultados assíncronos da Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_async_result) para determinar se a operação foi bem-sucedida ou falhou após receber uma indicação de solicitação de status da Internet \_ \_ \_ .

O exemplo a seguir mostra um exemplo de uma função de chamada de retorno e uma chamada para [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) para registrar a função como a função de retorno de chamada.


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



### <a name="closing-hinternet-handles"></a>Fechando identificadores de HINTERNET

Todos os identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) podem ser fechados usando a função [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) . Os aplicativos cliente devem fechar todos os identificadores de **HINTERNET** derivados do identificador **HINTERNET** que estão tentando fechar antes de chamar [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) no identificador.

O exemplo a seguir ilustra a hierarquia de identificador.


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



### <a name="locking-and-unlocking-resources"></a>Bloqueando e desbloqueando recursos

A função [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) permite que um aplicativo Verifique se o recurso em cache associado ao identificador [**HINTERNET**](appendix-a-hinternet-handles.md) passado para ele não desaparece do cache. Se outro download tentar confirmar um recurso que tem a mesma URL que o arquivo bloqueado, o cache evita a remoção do arquivo, fazendo uma exclusão segura. Depois que o aplicativo chama a função [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile) , o cache recebe permissão para excluir o arquivo.

Se o [sinalizador \_ Internet \_ sem \_ \_ gravação do cache](api-flags.md) ou sinalizador de Internet não tiver sido definido, o [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) criará um arquivo temporário com a extensão tmp, a menos que o identificador esteja conectado a um recurso HTTPS. [ \_ \_ \_](api-flags.md) Se a função acessar um recurso HTTPS e um sinalizador de INTERNET \_ \_ sem \_ \_ gravação de cache (ou o sinalizador de Internet não \_ \_ \_ cache) tiver sido definido, [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) falhará.

> [!Note]  
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 
