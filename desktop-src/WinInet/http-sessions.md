---
title: Sessões HTTP
description: Os recursos na WWW são acessados usando http.
ms.assetid: 0f307e28-9c38-41e7-9795-7eef08e99a3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b0b4d30bc86c588495a55ed4867a4084c43a09
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084656"
---
# <a name="http-sessions"></a>Sessões HTTP

O WinINet permite que você acesse recursos no World Wide Web (WWW). Esses recursos podem ser acessados diretamente usando [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para obter mais informações, consulte [acessando URLs diretamente](handling-uniform-resource-locators.md)).

Os recursos na WWW são acessados usando http. As funções HTTP lidam com os protocolos subjacentes, permitindo que seu aplicativo acesse as informações na WWW. À medida que o protocolo HTTP evolui, os protocolos subjacentes são atualizados para manter o comportamento da função.

O diagrama a seguir mostra as relações das funções que são usadas com o protocolo HTTP. As caixas sombreadas representam funções que retornam identificadores [**HINTERNET**](appendix-a-hinternet-handles.md) , enquanto as caixas simples representam funções que usam o identificador **HINTERNET** criado pela função na qual dependem.

![funções do Wininet usadas para http](images/ax-wnt05.png)

Para obter mais informações, consulte [HINTERNET Handles](appendix-a-hinternet-handles.md).

## <a name="using-the-wininet-functions-to-access-the-www"></a>Usando as funções WinINet para acessar a WWW

-   [Iniciando uma conexão com a WWW](#initiating-a-connection-to-the-www)
-   [Abrindo uma solicitação](#opening-a-request)
-   [Adicionando cabeçalhos de solicitação](#adding-request-headers)
-   [Enviando uma solicitação](#sending-a-request)
-   [Postando dados no servidor](#posting-data-to-the-server)
-   [Obtendo informações sobre uma solicitação](#getting-information-about-a-request)
-   [Baixando recursos da WWW](#downloading-resources-from-the-www)

As funções a seguir são usadas durante sessões HTTP para acessar a WWW.



| Função                                               | Descrição                                                                                                                                                                                  |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) | Adiciona cabeçalhos de solicitação HTTP ao identificador de solicitação HTTP. Essa função requer um identificador criado pelo [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).                                                 |
| [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)             | Abre um identificador de solicitação HTTP. Essa função requer um identificador criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                                                                         |
| [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)                 | Consulta informações sobre uma solicitação HTTP. Essa função requer um identificador criado pela função [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) ou [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) . |
| [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)             | Envia a solicitação HTTP especificada para o servidor HTTP. Essa função requer um identificador criado pelo [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).                                                  |
| [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)           | Exibe caixas de diálogo predefinidas para condições comuns de erro da Internet. Essa função requer o identificador usado na chamada para [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).                     |



 

### <a name="initiating-a-connection-to-the-www"></a>Iniciando uma conexão com a WWW

Para iniciar uma conexão com a WWW, o aplicativo deve chamar a função [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) no [**HINTERNET**](appendix-a-hinternet-handles.md) raiz retornado por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) deve estabelecer uma sessão http declarando o \_ tipo de serviço http do serviço de Internet \_ . Para obter mais informações sobre como usar o [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), consulte [usando o InternetConnect](enabling-internet-functionality.md).

### <a name="opening-a-request"></a>Abrindo uma solicitação

A função [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) abre uma solicitação HTTP e retorna um identificador [**HINTERNET**](appendix-a-hinternet-handles.md) que pode ser usado pelas outras funções http. Ao contrário das outras funções abertas (como [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)), o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) não envia a solicitação para a Internet quando chamada. A função [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) envia a solicitação e estabelece uma conexão pela rede.

O [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usa um identificador de sessão http criado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) e um verbo http, nome do objeto, Cadeia de caracteres de versão, referenciador, tipos de aceitação, sinalizadores e valor de contexto.

O verbo HTTP é uma cadeia de caracteres a ser usada na solicitação. Os verbos HTTP comuns usados em solicitações incluem GET, PUT e POST. Se esse valor for definido como **NULL**, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usará o valor padrão Get.

O nome do objeto é uma cadeia de caracteres que contém o nome do objeto de destino do verbo HTTP especificado. Geralmente, esse é um nome de arquivo, um módulo executável ou um especificador de pesquisa. Se o nome do objeto fornecido for uma cadeia de caracteres vazia, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) procurará a página padrão.

A cadeia de caracteres da versão deve conter a versão HTTP. Se esse parâmetro for **nulo**, a função usará "" http/1.1 "".

O referenciador especifica o endereço do documento do qual o nome do objeto foi obtido. Se esse parâmetro for **NULL**, nenhum referenciador será especificado.

A cadeia de caracteres terminada em **nulo** que contém os tipos de aceitação indica os tipos de conteúdo aceitos pelo aplicativo. Definir esse parâmetro como **NULL** indica que nenhum tipo de conteúdo é aceito pelo aplicativo. Se uma cadeia de caracteres vazia for fornecida, o aplicativo indicará que aceita somente documentos do tipo "" Text/ \* "". O valor "" Text/ \* "" indica documentos somente texto — não imagens ou outros arquivos binários.

Os valores do sinalizador controlam o cache, os cookies e os problemas de segurança. Para o Microsoft Network (MSN), o NTLM e outros tipos de autenticação, defina o sinalizador [Internet \_ Flag \_ manter \_ conexão](api-flags.md) .

Se o [sinalizador \_ \_ assíncrono de sinalizador da Internet](api-flags.md) tiver sido definido na chamada para [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), um valor de contexto diferente de zero deverá ser definido para a operação assíncrona adequada.

O exemplo a seguir é uma chamada de exemplo para [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).

`hHttpRequest = HttpOpenRequest( hHttpSession, "GET", "", NULL, "", NULL, 0, 0);`

### <a name="adding-request-headers"></a>Adicionando cabeçalhos de solicitação

A função [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) permite que os aplicativos adicionem um ou mais cabeçalhos de solicitação à solicitação inicial. Essa função permite que um aplicativo acrescente cabeçalhos de formato livre adicionais ao identificador de solicitação HTTP; Ele é destinado ao uso por aplicativos sofisticados que exigem controle preciso sobre a solicitação enviada ao servidor HTTP.

[**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) precisa de um identificador de solicitação HTTP criado pelo [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), uma cadeia de caracteres que contém os cabeçalhos, o comprimento dos cabeçalhos e os modificadores.

### <a name="sending-a-request"></a>Enviando uma solicitação

[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) estabelece uma conexão com a Internet e envia a solicitação para o site especificado. Essa função requer um identificador [**HINTERNET**](appendix-a-hinternet-handles.md) criado pelo [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta). O [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) também pode enviar cabeçalhos adicionais ou informações opcionais. As informações opcionais geralmente são usadas para operações que gravam informações no servidor, como PUT e POST.

Depois que o [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) envia a solicitação, o aplicativo pode usar as funções [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)e [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) no identificador [**HINTERNET**](appendix-a-hinternet-handles.md) criado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) para baixar os recursos do servidor.

### <a name="posting-data-to-the-server"></a>Postando dados no servidor

Para postar dados em um servidor, o verbo HTTP na chamada para [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) deve ser post ou PUT. O endereço do buffer que contém os dados de POSTAgem deve ser passado para o parâmetro *lpOptional* em [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). O parâmetro *dwOptionalLength* deve ser definido como o tamanho dos dados.

Você também pode usar a função [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) para postar dados em um identificador [**HINTERNET**](appendix-a-hinternet-handles.md) enviado usando o [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa).

### <a name="getting-information-about-a-request"></a>Obtendo informações sobre uma solicitação

O [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) permite que um aplicativo recupere informações sobre uma solicitação HTTP. A função requer um identificador [**HINTERNET**](appendix-a-hinternet-handles.md) criado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) ou [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), um valor de nível de informação e um comprimento de buffer. O [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) também aceita um buffer que armazena as informações e um índice de cabeçalho baseado em zero que enumera vários cabeçalhos com o mesmo nome.

### <a name="downloading-resources-from-the-www"></a>Baixando recursos da WWW

Depois de abrir uma solicitação com [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e enviá-la ao servidor [**com HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta), o aplicativo poderá usar as funções [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)e [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) para baixar o recurso do servidor http.

O exemplo a seguir baixa um recurso. A função aceita o identificador para a janela atual, o número de identificação de uma caixa de edição e um identificador [**HINTERNET**](appendix-a-hinternet-handles.md) criado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e enviado por [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). Ele usa [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) para determinar o tamanho do recurso e, em seguida, baixa-o usando [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile). O conteúdo é exibido na caixa de edição.


```C++
int WINAPI Dumper(HWND hX, int intCtrlID, HINTERNET hResource)
{
    LPTSTR lpszData;    // buffer for the data
    DWORD  dwSize;       // size of the data available
    DWORD  dwDownloaded; // size of the downloaded data
    DWORD  dwSizeSum=0;  // size of the data in the textbox
    LPTSTR lpszHolding;  // buffer to merge the textbox data and buffer

    // Set the cursor to an hourglass.
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    // This loop handles reading the data.
    do
    {
        // The call to InternetQueryDataAvailable determines the
        // amount of data available to download.
        if (!InternetQueryDataAvailable(hResource,&dwSize,0,0))
        {
            printf("InternetQueryDataAvailable failed (%d)\n", GetLastError());
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
        {
            // Allocate a buffer of the size returned by
            // InternetQueryDataAvailable.
            lpszData = new TCHAR[dwSize+1];

            // Read the data from the HINTERNET handle.
            if(!InternetReadFile(hResource,
                                 (LPVOID)lpszData,
                                 dwSize,
                                 &dwDownloaded))
            {
                printf("InternetReadFile failed (%d)\n", GetLastError());
                delete[] lpszData;
                break;
            }
            else
            {
                // Add a null terminator to the end of the data buffer
                lpszData[dwDownloaded]='\0';

                // Allocate the holding buffer.
                lpszHolding = new TCHAR[dwSizeSum + dwDownloaded + 1];

                // Check if there has been any data written
                // to the textbox.
                if (dwSizeSum != 0)
                {
                    // Retrieve the data stored in the textbox if any
                    GetDlgItemText(hX,intCtrlID,
                                   (LPTSTR)lpszHolding,
                                   dwSizeSum);

                    // Add a null terminator at the end of the
                    // textbox data.
                    lpszHolding[dwSizeSum]='\0';
                }
                else
                {
                    // Make the holding buffer an empty string.
                    lpszHolding[0]='\0';
                }

                size_t cchDest = dwSizeSum + dwDownloaded + dwDownloaded + 1;
                LPTSTR* ppszDestEnd = 0;
                size_t* pcchRemaining = 0;

                // Add the new data to the holding buffer
                HRESULT hr = StringCchCatEx(lpszHolding,
                                            cchDest,
                                            lpszData,
                                            ppszDestEnd,
                                            pcchRemaining,
                                            STRSAFE_NO_TRUNCATION);

                if(SUCCEEDED(hr))
                {
                    // Write the holding buffer to the textbox.
                    SetDlgItemText(hX,intCtrlID,(LPTSTR)lpszHolding);

                    // Delete the two buffers.
                    delete[] lpszHolding;
                    delete[] lpszData;

                    // Add the size of the downloaded data to the
                    // textbox data size.
                    dwSizeSum = dwSizeSum + dwDownloaded + 1;

                    // Check the size of the remaining data.
                    // If it is zero, break.
                    if (dwDownloaded == 0)
                        break;
                    else
                    {
                    //  TODO: Insert error handling code here.
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

    return TRUE;
}
```



> [!Note]  
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 