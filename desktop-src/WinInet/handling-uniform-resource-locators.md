---
title: Manipulando localizadores de recursos uniformes
description: Um URL (Uniform Resource Locator) é uma representação compacta do local e do método de acesso para um recurso localizado na Internet.
ms.assetid: bb59ada6-f49f-412c-a32c-4fb9495b1222
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 419433c8a06b6243bf048896664a67da31a3c58d1d79eb6fea65f9fc99dbe63a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121866"
---
# <a name="handling-uniform-resource-locators"></a>Manipulando localizadores de recursos uniformes

Um URL (Uniform Resource Locator) é uma representação compacta do local e do método de acesso para um recurso localizado na Internet. Cada URL consiste em um esquema (HTTP, HTTPS ou FTP) e uma cadeia de caracteres específica do esquema. Essa cadeia de caracteres também pode incluir uma combinação de um caminho de diretório, cadeia de caracteres de pesquisa ou nome do recurso. As funções WinINet fornecem a capacidade de criar, combinar, quebrar e canonizar URLs. Para obter mais informações sobre URLs, [consulte RFC-1738](https://www.ietf.org/rfc/rfc1738.txt) em URL (Uniform Resource Locators).

As funções de URL operam de maneira orientada a tarefas. O conteúdo e o formato da URL que é dado à função não são verificados. O aplicativo de chamada deve acompanhar o uso dessas funções para garantir que os dados estão no formato pretendido. Por exemplo, a [**função InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) converteria o caractere "%" na sequência de escape "%25" ao usar nenhum sinalizador. Se [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) for usado na URL canonizada, a sequência de escape "%25" será convertida na sequência de escape "%2525", que não funcionaria corretamente.

-   [O que é uma URL canonizada?](#what-is-a-canonicalized-url)
-   [Usando as funções do WinINet para lidar com URLs](#using-the-wininet-functions-to-handle-urls)
-   [Canonizar URLs](#what-is-a-canonicalized-url)
-   [Combinando URLs base e relativas](#combining-base-and-relative-urls)
-   [Como quebrar URLs](#cracking-urls)
-   [Criando URLs](#creating-urls)
-   [Acessando URLs diretamente](#accessing-urls-directly)

## <a name="what-is-a-canonicalized-url"></a>O que é uma URL canonizada?

O formato de todas as URLs deve seguir a sintaxe e a semântica aceitas para acessar recursos por meio da Internet. Canonicalização é o processo de formatação de uma URL para seguir essa sintaxe e semântica aceitas.

Os caracteres que devem ser codificados incluem caracteres que não têm caracteres gráficos correspondentes no conjunto de caracteres codificados US-ASCII (80-FF hexadecimal, que não são usados no conjunto de caracteres codificados us-ASCII e hexadecimais 00-1F e 7F, que são caracteres de controle), espaços em branco, "%" (que é usado para codificar outros caracteres) e caracteres não seguros (<, >, ", \# {, }, \| , , \\ ^, ~, \[ , e \] ').

## <a name="using-the-wininet-functions-to-handle-urls"></a>Usando as funções do WinINet para lidar com URLs

A tabela a seguir resume as funções de URL.



| Função                                                   | Descrição                                        |
|------------------------------------------------------------|----------------------------------------------------|
| [**Internetcanonicalizeurl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) | Canoniza a URL.                             |
| [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla)           | Combina URLs base e relativas.                   |
| [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla)               | Analisar uma cadeia de caracteres de URL em componentes.               |
| [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla)             | Cria uma cadeia de caracteres de URL de componentes.              |
| [**Internetopenurl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)                 | Começa a recuperar um recurso FTP, HTTP ou HTTPS. |



 

## <a name="canonicalizing-urls"></a>Canonizar URLs

A canonização de uma URL é o processo que converte uma URL, que pode conter caracteres não seguros, como espaços em branco, caracteres reservados e assim por diante, em um formato aceito.

A [**função InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) pode ser usada para canonizar URLs. Essa função é muito orientada a tarefas, portanto, o aplicativo deve acompanhar seu uso com cuidado. [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) não verifica se a URL passada para ela já está canonizada e se a URL retornada é válida.

Os cinco sinalizadores a seguir controlam como [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) lida com uma URL específica. Os sinalizadores podem ser usados em combinação. Se nenhum sinalizador for usado, a função codifica a URL por padrão.



| Valor                     | Significado                                                                                                                                                                                                 |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MODO DE NAVEGADOR \_ DA \_ UTI        | Não codificar ou decodificar caracteres depois de " " ou "?" e não remova o \# espaço em branco à seguir após "?". Se esse valor não for especificado, a URL inteira será codificada e o espaço em branco à parte final será removido. |
| DECODIFICAR \_ A ICU               | Converta todas as sequências %XX em caracteres, incluindo sequências de escape, antes que a URL seja analisado.                                                                                                          |
| SOMENTE ESPAÇOS DE \_ \_ CODIFICAÇÃO DE \_ UTI | Codificar somente espaços.                                                                                                                                                                                     |
| ICU \_ SEM \_ CODIFICAÇÃO           | Não converta caracteres não seguros em sequências de escape.                                                                                                                                                   |
| ICU \_ NO \_ META             | Não remova as metadadas (como "." e "..") da URL.                                                                                                                                       |



 

O sinalizador DECODE de ICU deve ser usado somente em URLs canonizadas, pois pressu que todas as sequências %XX são códigos de escape e converte-as nos \_ caracteres indicados pelo código. Se a URL tiver um símbolo "%" que não faz parte de um código de escape, o DECODE da ICU ainda o \_ tratará como um. Essa característica pode fazer [**com que InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) crie uma URL inválida.

Para usar [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) para retornar uma URL completamente decodificada, os sinalizadores ICU DECODE e ICU NO ENCODE devem \_ ser \_ \_ especificados. Essa configuração pressu que a URL que está sendo passada [**para InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) foi canonizada anteriormente.

## <a name="combining-base-and-relative-urls"></a>Combinando URLs base e relativas

Uma URL relativa é uma representação compacta do local de um recurso em relação a uma URL base absoluta. A URL base deve ser conhecida pelo analisador e geralmente inclui o esquema, o local da rede e as partes do caminho da URL. Um aplicativo pode chamar [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) para combinar a URL relativa com sua URL base. [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) também canoniza a URL resultante.

## <a name="cracking-urls"></a>Como quebrar URLs

A [**função InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) separa uma URL em suas partes de componente e retorna os componentes indicados pela estrutura [**\_ COMPONENTEs da URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) que é passada para a função.

Os componentes que comem a estrutura [**COMPONENTEs \_**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) da URL são o número do esquema, o nome do host, o número da porta, o nome de usuário, a senha, o caminho da URL e as informações adicionais (como parâmetros de pesquisa). Cada componente, exceto os números de esquema e porta, tem um membro de cadeia de caracteres que contém as informações e um membro que contém o comprimento do membro da cadeia de caracteres. Os números de esquema e porta têm apenas um membro que armazena o valor correspondente; ambos são retornados em todas as chamadas bem-sucedidas para [**InternetCrackUrl.**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla)

Para obter o valor de um componente específico na estrutura COMPONENTEs da [**URL, \_**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) o membro que armazena o comprimento da cadeia de caracteres desse componente deve ser definido como um valor diferente de zero. O membro da cadeia de caracteres pode ser o endereço de um buffer ou **NULL.**

Se o membro do ponteiro contiver o endereço de um buffer, o membro de comprimento da cadeia de caracteres deverá conter o tamanho desse buffer. [**InternetCrackUrl retorna**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) as informações do componente como uma cadeia de caracteres no buffer e armazena o comprimento da cadeia de caracteres no membro de comprimento da cadeia de caracteres.

Se o membro do ponteiro for **NULL,** o membro de comprimento da cadeia de caracteres poderá ser definido como qualquer valor que não seja zero. [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) armazena o endereço do primeiro caractere da cadeia de caracteres de URL que contém as informações do componente e define o comprimento da cadeia de caracteres para o número de caracteres na parte restante da cadeia de caracteres de URL que pertence ao componente.

Todos os membros de ponteiro definidos como **NULL** com um ponto de membro de comprimento diferente de zero para o ponto de partida apropriado na cadeia de caracteres de URL. O comprimento armazenado no membro de comprimento deve ser usado para determinar o final das informações do componente individual.

Para concluir a inicialização correta da estrutura [**\_ COMPONENTES**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) da URL, o membro **dwStructSize** deve ser definido como o tamanho da estrutura [**\_ COMPONENTEs da URL,**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) em bytes.

O exemplo a seguir retorna os componentes da URL na caixa de edição, IDC PreOpen1, e retorna os componentes para a caixa de \_ listagem, \_ PreOpenList do IDC. Para exibir apenas as informações de um componente individual, essa função copia o caractere imediatamente após as informações do componente na cadeia de caracteres e o substitui temporariamente por **um NULL.**


```C++
#include <windows.h>
#include <tchar.h>
#include <strsafe.h>
#include <wininet.h>
#include <stdlib.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  CRACKER_BUFFER_SIZE           MAX_PATH

// For sample source code implementing the InternetErrorOut( ) 
// function referenced below, see the "Handling Errors" topic  
// under "Using WinInet"
extern BOOL WINAPI InternetErrorOut( HWND hWnd, DWORD dwError,
                                     LPCTSTR szFailingFunctionName );

// Forward declaration of listUrlPart helper functions:
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength );
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, int partValue );

// Static list describing the URL Scheme types 
// enumerated in INTERNET_SCHEME:
TCHAR* schemeType[] =
{
  TEXT( "[Partial URL]" ),                //  0
  TEXT( "[Unknown scheme]" ),             //  1
  TEXT( "[Default scheme]" ),             //  2
  TEXT( "FTP" ),                          //  3
  TEXT( "Gopher" ),                       //  4
  TEXT( "HTTP" ),                         //  5
  TEXT( "HTTPS" ),                        //  6
  TEXT( "File" ),                         //  7
  TEXT( "News" ),                         //  8
  TEXT( "MailTo" ),                       //  9
  TEXT( "Socks" ),                        // 10
  TEXT( "JavaScript" ),                   // 11
  TEXT( "VBScript" )                      // 12
};
#define  CRACKER_SCHEME_TYPE_ARRAY_SIZE      13

BOOL WINAPI Cracker( HWND hDlg, int nURLtextBoxId, int nListBoxId )
{
   int i, j;
   TCHAR* failedFunctionName;
   TCHAR URL_buffer[CRACKER_BUFFER_SIZE];

   URL_COMPONENTS URLparts;

   URLparts.dwStructSize = sizeof( URLparts );

   // The following elements determine which components are displayed
   URLparts.dwSchemeLength    = 1;
   URLparts.dwHostNameLength  = 1;
   URLparts.dwUserNameLength  = 1;
   URLparts.dwPasswordLength  = 1;
   URLparts.dwUrlPathLength   = 1;
   URLparts.dwExtraInfoLength = 1;

   URLparts.lpszScheme     = NULL;
   URLparts.lpszHostName   = NULL;
   URLparts.lpszUserName   = NULL;
   URLparts.lpszPassword   = NULL;
   URLparts.lpszUrlPath    = NULL;
   URLparts.lpszExtraInfo  = NULL;

   SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
   if( !GetDlgItemText( hDlg, nURLtextBoxId, 
                        URL_buffer, CRACKER_BUFFER_SIZE ) )
   {
       failedFunctionName = TEXT( "GetDlgItemText" );
       goto CrackerError_01;
   }

   if( FAILED( StringCchLength( URL_buffer, CRACKER_BUFFER_SIZE, 
                                (size_t*) &i ) ) )
   {
       failedFunctionName = TEXT( "StringCchLength" );
       goto CrackerError_01;
   }

   if( !InternetCrackUrl( URL_buffer, (DWORD)_tcslen( URL_buffer ), 0, 
                          &URLparts ) )
   {
       failedFunctionName = TEXT( "InternetCrackUrl" );
       goto CrackerError_01;
   }

   failedFunctionName = TEXT( "listURLpart" );

   i = URLparts.nScheme + 2;
   if( ( i >= 0 ) && ( i < CRACKER_SCHEME_TYPE_ARRAY_SIZE ) )
   {
       StringCchLength( schemeType[i], 
                        CRACKER_BUFFER_SIZE, 
                        (size_t*) &j );
       if( !listURLpart( hDlg, nListBoxId, 
                         TEXT("Scheme type"), 
                         schemeType[i], j ))
           goto CrackerError_01;
   }

   if( !listURLpart( hDlg, nListBoxId, TEXT( "Scheme text" ), 
                     URLparts.lpszScheme, 
                     URLparts.dwSchemeLength ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Host name" ), 
                     URLparts.lpszHostName, 
                     URLparts.dwHostNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Port number" ), 
                     (int) URLparts.nPort ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "User name" ), 
                     URLparts.lpszUserName, 
                     URLparts.dwUserNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Password" ), 
                     URLparts.lpszPassword, 
                     URLparts.dwPasswordLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Path" ), 
                     URLparts.lpszUrlPath, 
                     URLparts.dwUrlPathLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Extra information"), 
                     URLparts.lpszExtraInfo, 
                     URLparts.dwExtraInfoLength))
           goto CrackerError_01;

   return( TRUE );

CrackerError_01:
// For sample source code of the InternetErrorOut( ) function 
// referenced below, see the "Handling Errors" 
// topic under "Using WinInet"
   InternetErrorOut( hDlg, GetLastError( ), failedFunctionName );
   return FALSE;
}

// listURLpart( ) helper function for string parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];
  LPTSTR nextStart;
  size_t nextSize;

  if( partLength == 0 )  // Just skip empty ones
    return( TRUE );

  if( FAILED( StringCchCopyEx( outputBuffer, 
                              (size_t) CRACKER_BUFFER_SIZE,
                               szPartName, &nextStart, 
                               &nextSize, 0 ) ) ||
      FAILED( StringCchCopyEx( nextStart, nextSize, TEXT( ": " ), 
                               &nextStart, &nextSize, 0 ) ) ||
      FAILED( StringCchCopyNEx( nextStart, nextSize, part, 
                                (size_t) partLength,
                                &nextStart, &nextSize, 0 ) ) )
    return( FALSE );

  *nextStart = 0;
  if( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                          (LPARAM)outputBuffer ) < 0 )
    return( FALSE );
  return( TRUE );
}

// listURLpart( ) helper function for numeric parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, int partValue )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];

  if( FAILED( StringCchPrintf( outputBuffer, 
                               (size_t) CRACKER_BUFFER_SIZE,
                               TEXT( "%s: %d" ), szPartName, 
                               partValue ) ) ||
      ( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                            (LPARAM)outputBuffer ) < 0 ) )
    return( FALSE );
  return( TRUE );
}
```



## <a name="creating-urls"></a>Criando URLs

A [**função InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) usa as informações na estrutura [**COMPONENTES \_ de URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) para criar um Uniform Resource Locator.

Os componentes que comem a estrutura [**COMPONENTEs \_**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) da URL são o esquema, o nome do host, o número da porta, o nome de usuário, a senha, o caminho da URL e as informações adicionais (como parâmetros de pesquisa). Cada componente, exceto o número da porta, tem um membro de cadeia de caracteres que contém as informações e um membro que contém o comprimento do membro da cadeia de caracteres.

Para cada componente necessário, o membro do ponteiro deve conter o endereço do buffer que contém as informações. O membro de comprimento deverá ser definido como zero se o membro do ponteiro contiver o endereço de uma cadeia de caracteres terminada em zero; o membro de comprimento deverá ser definido como o comprimento da cadeia de caracteres se o membro do ponteiro contiver o endereço de uma cadeia de caracteres que não é terminada em zero. O membro do ponteiro de todos os componentes que não são necessários deve ser **NULL.**

## <a name="accessing-urls-directly"></a>Acessando URLs diretamente

Os recursos FTP e HTTP na Internet podem ser acessados diretamente usando as funções [**InternetOpenUrl,**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)e [**InternetFindNextFile.**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) abre uma conexão com o recurso na URL passada para a função. Quando essa conexão é feita, há duas etapas possíveis. Primeiro, se o recurso for um arquivo, [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) poderá baixá-lo; em segundo lugar, se o recurso for um diretório, [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) poderá enumerar os arquivos dentro do diretório (exceto ao usar proxies CERN). Para obter mais informações sobre [**InternetReadFile,**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)consulte [Lendo arquivos](common-functions.md). Para obter mais informações [**sobre InternetFindNextFile,**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)consulte [Encontrando o próximo arquivo](common-functions.md).

Para aplicativos que precisam operar por meio de um proxy CERN, [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) pode ser usado para acessar diretórios e arquivos FTP. As solicitações FTP são empacotados para aparecerem como uma solicitação HTTP, que o proxy CERN aceitaria.

[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usa o [**handle HINTERNET**](appendix-a-hinternet-handles.md) criado pela [**função InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) e a URL do recurso. A URL deve incluir o esquema (http:, ftp:, arquivo: para um arquivo local ou https: para protocolo de hipertexto seguro ) e local \[ \] de rede \[ \] (como `www.microsoft.com` ). A URL também pode incluir um caminho (por exemplo, /isapi/gomscom.asp? TARGET=/windows/feature/) e nome do recurso (por exemplo, default.htm). Para solicitações HTTP ou HTTPS, cabeçalhos adicionais podem ser incluídos.

[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetFindNextFile,**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)e [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (somente URLs HTTP ou HTTPS) podem usar o handle criado por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) para baixar o recurso.

O diagrama a seguir ilustra quais alças usar com cada função.

![alças a usar com funções](images/ax-wnt02.png)

O handle [**HINTERNET raiz**](appendix-a-hinternet-handles.md) criado por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) é usado por [**InternetOpenUrl.**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) O handle **HINTERNET** criado por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) pode ser usado por [**InternetQueryDataAvailable,**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) [**InternetReadFile,**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) (não mostrado aqui) e [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (somente URLs HTTP ou HTTPS).

Para obter mais informações, consulte [**HintERNET Handles**](appendix-a-hinternet-handles.md).

> [!Note]  
> O WinINet não dá suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o WinHTTP (Microsoft Windows HTTP Services).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 