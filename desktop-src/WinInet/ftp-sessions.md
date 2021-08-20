---
title: Sessões FTP
description: O WinINet permite que os aplicativos naveguem e manipulem diretórios e arquivos em um servidor ftp. Como os proxies CERN não são suportados por FTP, os aplicativos que usam um proxy CERN exclusivamente devem usar a função InternetOpenUrl.
ms.assetid: 23763672-765f-4bbc-95c9-c28775e91f3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70942fea5865fa96c9ee81ab996238e3f382471a701ac44969d1ff8797c8780d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113961"
---
# <a name="ftp-sessions"></a>Sessões FTP

O WinINet permite que os aplicativos naveguem e manipulem diretórios e arquivos em um servidor ftp. Como os proxies CERN não são suportados por FTP, os aplicativos que usam um proxy CERN exclusivamente devem usar a [**função InternetOpenUrl.**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) Para obter mais informações sobre como usar [**InternetOpenUrl,**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)consulte [Acessando URLs diretamente.](handling-uniform-resource-locators.md)

Para iniciar uma sessão FTP, use [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) para criar o alça de sessão.

O WinINet permite que você execute as seguintes ações em um servidor FTP:

-   Navegue entre diretórios.
-   Enumerar, criar, remover e renomear diretórios.
-   Renomeie, carregue, baixe e exclua arquivos.

A navegação é fornecida pelas [**funções FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) [**e FtpSetCurrentDirectory.**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) Essas funções utilizam o alça de sessão criado por uma chamada anterior para [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) para determinar em qual diretório o aplicativo está atualmente ou para alterar para um subdiretório diferente.

A enumeração de diretório é executada usando as [**funções FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) [**e InternetFindNextFile.**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) usa o alça de sessão criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) para encontrar o primeiro arquivo que corresponde aos critérios de pesquisa determinados e retorna um handle para continuar a enumeração de diretório. [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) usa o handle retornado por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) para retornar o próximo arquivo que corresponde aos critérios de pesquisa originais. O aplicativo deve continuar a chamar [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) até que não haja mais arquivos no diretório.

Use a [**função FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) para criar novos diretórios. Essa função usa o alça de sessão criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) e cria o diretório especificado pela cadeia de caracteres passada para a função. A cadeia de caracteres pode conter um nome de diretório relativo ao diretório atual ou um caminho de diretório totalmente qualificado.

Para renomear arquivos ou diretórios, o aplicativo pode chamar [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea). Essa função substitui o nome original pelo novo nome passado para a função. O nome do arquivo ou diretório pode ser relativo ao diretório atual ou a um nome totalmente qualificado.

Para carregar ou colocar arquivos em um servidor FTP, o aplicativo pode usar [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) ou [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (juntamente com [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)). [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) poderá ser usado se o arquivo já existir localmente, enquanto [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) e [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) poderão ser usados se os dados precisarem ser gravados em um arquivo no servidor FTP.

Para baixar ou obter arquivos, o aplicativo pode usar [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) ou [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (com [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)). [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) é usado para recuperar um arquivo de um servidor FTP e armazená-lo localmente, enquanto [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) e [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) podem ser usados para controlar para onde as informações baixadas estão indo (por exemplo, o aplicativo pode exibir as informações em uma caixa de edição).

Exclua arquivos em um servidor FTP usando a [**função FtpDeleteFile.**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) Essa função remove um nome de arquivo relativo ao diretório atual ou a um nome de arquivo totalmente qualificado do servidor FTP. [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) requer um handle de sessão retornado por [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)

## <a name="ftp-function-handles"></a>Alças de função FTP

Para funcionar corretamente, as funções FTP exigem determinados tipos de [**alças HINTERNET.**](appendix-a-hinternet-handles.md) Esses alças devem ser criados em uma ordem específica, começando com o alça raiz criado por [**InternetA abrir**](/windows/desktop/api/Wininet/nf-wininet-internetopena). [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) pode criar um alça de sessão FTP.

O diagrama a seguir mostra as funções que dependem do handle de sessão FTP retornado por [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) As caixas sombreadas representam funções que retornam alças [**HINTERNET,**](appendix-a-hinternet-handles.md) enquanto as caixas simples representam funções que usam o alça HINTERNET criado pela função da qual dependem.

![funções ftp dependentes do handle de sessão ftp retornado por internetconnect](images/ax-wnt06.png)

O diagrama a seguir mostra as duas funções que retornam as alças [HINTERNET](appendix-a-hinternet-handles.md) e as funções que dependem delas. As caixas sombreadas representam funções que retornam alças **HINTERNET,** enquanto as caixas simples representam funções que usam o alça **HINTERNET** criado pela função da qual dependem.

![funções ftp que retornam alças hinternet](images/ax-wnt03.png)

Para obter mais informações, consulte [HintERNET Handles](appendix-a-hinternet-handles.md).

## <a name="using-the-wininet-functions-for-ftp-sessions"></a>Usando as funções WinINet para sessões de FTP

As funções a seguir são usadas durante sessões FTP. Essas funções não são reconhecidas por proxies CERN. Os aplicativos que devem funcionar por meio de proxies CERN devem usar [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) e acessar os recursos diretamente. Para obter mais informações sobre o acesso direto a recursos, consulte [Acessando URLs diretamente.](handling-uniform-resource-locators.md)



| Função                                                 | Descrição                                                                                                                                                    |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)         | Cria um novo diretório no servidor. Essa função requer um alça criado pelo [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                                  |
| [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)                   | Exclui um arquivo do servidor. Essa função requer um alça criado pelo [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                                         |
| [**Ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)             | Inicia a enumeração de arquivo ou a pesquisa de arquivos no diretório atual. Essa função requer um alça criado pelo [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)        |
| [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) | Retorna o diretório atual do cliente no servidor. Essa função requer um alça criado pelo [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                   |
| [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)                         | Recupera um arquivo do servidor. Essa função requer um alça criado pelo [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                                       |
| [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)                       | Inicia o acesso a um arquivo no servidor para leitura ou escrita. Essa função requer um alça criado pelo [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) |
| [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)                         | Grava um arquivo no servidor. Essa função requer um alça criado pelo [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                                            |
| [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)         | Exclui um diretório no servidor. Essa função requer um alça criado pelo [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                                      |
| [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)                   | Renomeia um arquivo no servidor. Essa função requer um alça criado pelo [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                                           |
| [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) | Altera o diretório atual do cliente no servidor. Essa função requer um alça criado pelo [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                   |
| [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)           | Grava dados em um arquivo aberto no servidor. Essa função requer um handle criado por [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea).                                      |



 

### <a name="starting-an-ftp-session"></a>Iniciando uma sessão FTP

O aplicativo estabelece uma sessão FTP chamando [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) em um handle criado por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). [**O InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) precisa do nome do servidor, do número da porta, do nome de usuário, da senha e do tipo de serviço (que deve ser definido como \_ FTP do SERVIÇO \_ INTERNET). Para semântica FTP passiva, o aplicativo também deve definir o sinalizador [PASSIVO DO SINALIZADOR \_ DA \_ INTERNET.](api-flags.md)

Os valores \_ INTERNET DEFAULT \_ FTP PORT e INTERNET \_ INVALID PORT NUMBER podem ser usados para o número da \_ \_ \_ porta. INTERNET \_ DEFAULT \_ FTP PORT usa a porta \_ FTP padrão, mas o tipo de serviço ainda deve ser definido. INTERNET \_ INVALID PORT NUMBER usa o valor padrão para o tipo de serviço \_ \_ indicado.

Os valores para o nome de usuário e a senha podem ser definidos como **NULL.** Se ambos os valores são definidos como **NULL,** [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usa "anônimo" para o nome de usuário e o endereço de email do usuário para a senha. Se apenas a senha for definida como **NULL,** o nome de usuário passado para [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) será usado para o nome de usuário e uma cadeia de caracteres vazia será usada para a senha. Se nenhum valor for **NULL,** o nome de usuário e a senha fornecidos para [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) serão usados.

### <a name="enumerating-directories"></a>Enumerando diretórios

A enumeração de um diretório em um servidor FTP requer a criação de um handle por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea). Esse é um branch do alça de sessão criado pelo [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) localiza o primeiro arquivo ou diretório no servidor e o retorna em uma estrutura [**WIN32 \_ FIND \_ DATA.**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) Use [**InternetFindNextFile até**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) retornar [**ERROR NO MORE \_ \_ \_ FILES**](wininet-errors.md). Esse método localiza todos os arquivos e diretórios subsequentes no servidor. Para obter mais informações [**sobre InternetFindNextFile,**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)consulte [Encontrando o próximo arquivo](common-functions.md).

Para determinar se o arquivo recuperado por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) ou [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) é um diretório, verifique o membro **dwFileAttributes** da estrutura [**de \_ \_ dados de localização do Win32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) para ver se ele é igual ao diretório de atributo de arquivo \_ \_ .

Se o aplicativo fizer alterações no servidor FTP ou se o servidor FTP for alterado com frequência, [o \_ sinalizador \_ Internet \_ sem \_ gravação do cache](api-flags.md) e sinalizadores de [ \_ \_ recarga da Internet](api-flags.md) deverão ser definidos em [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea). Esses sinalizadores garantem que as informações de diretório que estão sendo recuperadas do servidor FTP sejam atuais.

Depois que o aplicativo concluir a enumeração do diretório, o aplicativo deverá fazer uma chamada para [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) no identificador criado pelo [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea). Até que o identificador seja fechado, o aplicativo não poderá chamar [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) novamente no identificador de sessão criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). Se uma chamada para [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) for feita no mesmo identificador de sessão antes de a chamada anterior para a mesma função ser fechada, a função falhará, retornando a [ \_ \_ transferência \_ de FTP de erro em \_ andamento](wininet-errors.md).

O exemplo a seguir enumera o conteúdo de um diretório de FTP em um controle de caixa de listagem. O parâmetro *hConnection* é um identificador retornado pela função [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) depois que ele estabelece uma sessão de FTP. O código-fonte de exemplo para a função InternetErrorOut referenciada neste exemplo pode ser encontrado no tópico [Manipulando erros](appendix-c-handling-errors.md).


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



### <a name="navigating-directories"></a>Navegando em diretórios

As funções [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) e [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) lidam com a navegação de diretório.

[**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) retorna o diretório atual do aplicativo no servidor FTP. O caminho do diretório do diretório raiz no servidor FTP está incluído.

[**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) altera o diretório de trabalho no servidor. As informações de diretório passadas para [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) podem ser um nome de caminho parcialmente ou totalmente qualificado relativo ao diretório atual. Por exemplo, se o aplicativo estiver atualmente no diretório "Public/info" e o caminho for "FTP/example", [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) alterará o diretório atual para "Public/info/FTP/example".

O exemplo a seguir usa o identificador de sessão de FTP hConnection, que é retornado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). O novo nome de diretório é obtido da caixa de edição do diálogo pai cuja IDC é passada no parâmetro *nDirNameId* . Antes que a alteração de diretório seja feita, a função recupera o diretório atual e o armazena na mesma caixa de edição. O código do recurso para a função DisplayFtpDir chamada no final é listado acima.


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



### <a name="manipulating-directories-on-an-ftp-server"></a>Manipulando diretórios em um servidor FTP

O WinINet fornece a capacidade de criar e remover diretórios em um servidor FTP para o qual o aplicativo tem os privilégios necessários. Se o aplicativo precisar fazer logon em um servidor com um nome de usuário e senha específicos, os valores poderão ser usados em [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) ao criar o identificador de sessão de FTP.

A função [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) usa um identificador de sessão de ftp válido e uma cadeia de caracteres terminada em **nulo** que contém um caminho totalmente qualificado ou um nome relativo ao diretório atual e cria um diretório no servidor FTP.

O exemplo a seguir mostra duas chamadas separadas para [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya). Em ambos os exemplos, hFtpSession é o identificador de sessão criado pela função [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) , e o diretório raiz é o diretório atual.

``` syntax
/* Creates the directory "test" in the current (root) directory. */
FtpCreateDirectory( hFtpSession, "test" );

/* Creates the directory "example" in the test directory. */
FtpCreateDirectory( hFtpSession, "\\test\\example" );
```

A função [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) usa um identificador de sessão e uma cadeia de caracteres terminada em **nulo** que contém um caminho totalmente qualificado ou um nome relativo ao diretório atual e remove esse diretório do servidor FTP.

O exemplo a seguir mostra duas chamadas de exemplo para [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya). Em ambas as chamadas, hFtpSession é o identificador de sessão criado pela função [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) , e o diretório raiz é o diretório atual. Há um diretório chamado "Test" no diretório raiz e um diretório chamado "example" no diretório "Test".

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



O exemplo a seguir cria um novo diretório no servidor FTP. O novo nome de diretório é obtido da caixa de edição do diálogo pai cuja IDC é passada no parâmetro *nDirNameId* . O identificador *hConnection* foi criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) depois de estabelecer uma sessão FTP. O código-fonte da função DisplayFtpDir chamada no final está listado acima.


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



O exemplo a seguir exclui um diretório do servidor FTP. O nome do diretório a ser excluído é obtido da caixa de edição no diálogo pai cuja IDC é passada para o parâmetro *nDirNameId* . O identificador *hConnection* foi criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) depois de estabelecer uma sessão FTP. O código-fonte da função DisplayFtpDir chamada no final está listado acima.


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



### <a name="getting-files-on-an-ftp-server"></a>Obtendo arquivos em um servidor FTP

Há três métodos para recuperar arquivos de um servidor FTP:

-   Use [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) e [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).
-   Use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) e [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).
-   Use [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea).

Para obter mais informações sobre como usar a função [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) , consulte [lendo arquivos](common-functions.md).

Se a URL do arquivo estiver disponível, o aplicativo poderá chamar [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) para se conectar a essa URL e, em seguida, usar [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) para controlar o download do arquivo. Isso permite o controle mais rígido do aplicativo sobre o download e é ideal para situações em que nenhuma outra operação precisa ser feita no servidor FTP. Para obter mais informações sobre como acessar recursos diretamente, consulte [acessando URLs diretamente](handling-uniform-resource-locators.md).

Se o aplicativo tiver estabelecido um identificador de sessão de FTP para o servidor com [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), o aplicativo poderá chamar [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) com o nome de arquivo existente e com um novo nome para o arquivo armazenado localmente. Em seguida, o aplicativo pode usar [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) para baixar o arquivo. Isso permite o controle mais rígido do aplicativo sobre o download e mantém a conexão com o servidor FTP, para que mais comandos possam ser executados.

Se o aplicativo não precisar de controle rígido sobre o download, o aplicativo poderá usar o [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) com o identificador de sessão de FTP, o nome do arquivo remoto e o nome do arquivo local para recuperar o arquivo. O [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) executa toda a escrituração e a contabilização associada à leitura de um arquivo de um servidor FTP e ao armazená-lo localmente.

O exemplo a seguir recupera um arquivo de um servidor FTP e o salva localmente. O nome do arquivo no servidor de FTP é obtido da caixa de edição no diálogo pai cuja IDC é passada no parâmetro *nFtpFileNameId* e o nome local no qual o arquivo é salvo é obtido da caixa de edição cuja IDC é passada no parâmetro *nLocalFileNameId* . O identificador *hConnection* foi criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) depois de estabelecer uma sessão FTP.


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



### <a name="placing-files-on-an-ftp-server"></a>Colocando arquivos em um servidor FTP

Há dois métodos para colocar um arquivo em um servidor FTP:

-   Use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) com [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile).
-   Use [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).

Um aplicativo que deve enviar dados para um servidor FTP, mas que não tem um arquivo local que contém todos os dados, deve usar [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) para criar e abrir um arquivo no servidor FTP. Em seguida, o aplicativo pode usar [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) para carregar as informações no arquivo.

Se o arquivo já existir localmente, o aplicativo poderá usar [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) para carregar o arquivo no servidor FTP. O [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) executa toda a sobrecarga que acompanha o carregamento de um arquivo local para um servidor FTP remoto.

O exemplo a seguir copia um arquivo local no servidor FTP. O nome local do arquivo é obtido da caixa de edição no diálogo pai cuja IDC é passada no parâmetro *nLocalFileNameId* e o nome no qual o arquivo é salvo no servidor FTP é obtido da caixa de edição cuja IDC é passada no parâmetro *nFtpFileNameId* . O identificador *hConnection* foi criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) depois de estabelecer uma sessão FTP.


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



### <a name="deleting-files-from-an-ftp-server"></a>Excluindo arquivos de um servidor FTP

Para excluir um arquivo de um servidor FTP, use a função [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) . O aplicativo de chamada deve ter os privilégios necessários para excluir um arquivo do servidor FTP.

O exemplo a seguir exclui um arquivo do servidor FTP. O nome do arquivo a ser excluído é obtido da caixa de edição no diálogo pai cuja IDC é passada para o parâmetro *nFtpFileNameId* . O identificador *hConnection* foi criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) depois de estabelecer uma sessão FTP. Como essa função não atualiza listagens de arquivos ou exibição de diretório, o processo de chamada deve fazer isso após a exclusão bem-sucedida.


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



### <a name="renaming-files-and-directories-on-an-ftp-server"></a>Renomeando arquivos e diretórios em um servidor FTP

Os arquivos e diretórios em um servidor FTP podem ser renomeados usando a função [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) . [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) aceita duas cadeias de caracteres terminadas em **nulo** que contêm nomes parcialmente ou totalmente qualificados relativos ao diretório atual. A função altera o nome do arquivo designado pela primeira cadeia de caracteres para o nome designado pela segunda cadeia de caracteres.

O exemplo a seguir renomeia um arquivo ou diretório no servidor FTP. O nome atual do arquivo ou diretório é obtido da caixa de edição no diálogo pai cuja IDC é passada no parâmetro *nOldFileNameId* e o novo nome é obtido da caixa de edição cuja IDC é passada no parâmetro *nNewFileNameId* . O identificador *hConnection* foi criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) depois de estabelecer uma sessão FTP. Como essa função não atualiza listagens de arquivos ou exibição de diretório, o processo de chamada deve fazer isso após a renomeação bem-sucedida.


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
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. para implementações de servidor ou serviços, use [o Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 