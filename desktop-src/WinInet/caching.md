---
title: Caching (Internet do Windows)
description: As funções do WinINet têm suporte de cache interno simples, mas flexível.
ms.assetid: 44c268c9-a745-432a-8540-60d7e7d2cb2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e753d826ec3abe580b94158296562208dcbed44
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085063"
---
# <a name="caching-windows-internet"></a>Caching (Internet do Windows)

As funções do WinINet têm suporte de cache interno simples, mas flexível. Todos os dados recuperados da rede são armazenados em cache no disco rígido e recuperados para solicitações subsequentes. O aplicativo pode controlar o cache em cada solicitação. Para solicitações HTTP do servidor, a maioria dos cabeçalhos recebidos também é armazenada em cache. Quando uma solicitação HTTP é satisfeita no cache, os cabeçalhos armazenados em cache também são retornados ao chamador. Isso torna o download de dados contínuo, se os dados são provenientes do cache ou da rede.

Os aplicativos devem alocar corretamente um buffer para obter os resultados desejados ao usar as funções de cache de URL persistentes. Para obter mais informações, consulte [usando buffers](appendix-b-using-buffers.md).

## <a name="cache-behavior-during-response-processing"></a>Comportamento de cache durante o processamento de resposta

O cache do WinINet é compatível com as diretivas HTTP Cache-Control descritas na RFC 2616. As diretivas de controle de cache e os sinalizadores de conjunto de aplicativos determinam o que pode ser armazenado em cache; no entanto, o WinINet determina o que realmente é armazenado em cache com base no seguinte critério:

-   O WinINet apenas armazena em cache as respostas HTTP e FTP.
-   Somente as respostas bem compostas podem ser armazenadas por um cache e usadas em uma resposta a uma solicitação subsequente. As respostas bem compostas são definidas como respostas que retornam com êxito.
-   Por padrão, o WinINet armazenará em cache as respostas bem-sucedidas, a menos que uma diretiva de controle de cache do servidor ou um sinalizador definido pelo aplicativo denotasse especificamente que a resposta não pode ser armazenada em cache.
-   Em geral, as respostas para o verbo GET serão armazenadas em cache se os requisitos listados acima forem atendidos. As respostas aos verbos PUT e POST não são armazenadas em cache em nenhuma circunstância.
-   Os itens serão armazenados em cache mesmo quando o cache estiver cheio. Se um item adicionado for colocar o cache sobre o limite de tamanho, a recuperação de cache será agendada. Por padrão, não há garantia de que os itens permaneçam mais de 10 minutos no cache. Para obter mais informações, consulte a seção [recuperação de cache](#cache-scavenger) abaixo.
-   O HTTPS é armazenado em cache por padrão. Isso é gerenciado por uma configuração global que não pode ser substituída por diretivas de cache definidas pelo aplicativo. Para substituir a configuração global, selecione o miniaplicativo opções da Internet no painel de controle e vá para a guia Avançado. Marque a caixa "não salvar páginas criptografadas no disco" na seção "segurança".

## <a name="cache-scavenger"></a>Recuperação de cache

A recuperação de cache limpa periodicamente os itens do cache. Se um item for adicionado ao cache e o cache estiver cheio, o item será adicionado ao cache e a recuperação de cache será agendada. Se a recuperação do cache concluir uma rodada de eliminação e o cache não tiver atingido o limite de cache, a recuperação será agendada para outra rodada quando outro item for adicionado ao cache. Em geral, a recuperação é agendada quando um item adicionado coloca o cache sobre seu limite de tamanho. Por padrão, o tempo de vida mínimo no cache é definido como 10 minutos, a menos que especificado de outra forma em uma diretiva de controle de cache. Quando o cache de recuperação é iniciado, não há nenhuma garantia de que os itens mais antigos sejam os primeiros a serem excluídos do cache.

O cache é compartilhado entre todos os aplicativos WinINet no computador para o mesmo usuário. A partir do Windows Vista e do Windows Server 2008, o tamanho do cache é definido como 1/32 º do tamanho do disco, com um tamanho mínimo de 8MB e um tamanho máximo de 50 MB.

## <a name="using-flags-to-control-caching"></a>Usando sinalizadores para controlar o cache

Os sinalizadores de cache permitem que um aplicativo controle quando e como ele usa o cache. Esses sinalizadores podem ser usados sozinhos ou em combinação com o parâmetro *dwFlags* em funções que acessam informações ou recursos na Internet. Por padrão, as funções armazenam todos os dados baixados da Internet.

Os sinalizadores a seguir podem ser usados para controlar o cache.



| Valor                                                                                                                                                  | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CACHE de sinalizador da INTERNET \_ \_ \_ assíncrono**](api-flags.md)                                                                            | Este sinalizador não tem efeito.                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**CACHE de sinalizador da INTERNET \_ \_ \_ se \_ net \_ falhar**](api-flags.md)                                                              | Retorna o recurso do cache se a solicitação de rede para o recurso falhar devido a um [erro \_ de \_ \_ redefinição de conexão com a Internet](wininet-errors.md) ou [erro a \_ Internet \_ não pode \_ se conectar](wininet-errors.md) . Esse sinalizador é usado pelo [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).                                                                                                              |
| [**sinalizador da INTERNET não \_ \_ \_ cache**](api-flags.md)                                                                              | Não armazena em cache os dados, seja localmente ou em qualquer gateway. Idêntico ao valor preferencial, o [**sinalizador da Internet \_ \_ não \_ \_ grava cache**](api-flags.md).                                                                                                                                                                                                                                                                                 |
|                                                                                                                                                        | Indica que se trata de um envio de formulários.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**Internet \_ sinalizador \_ de \_ envio de formulários de sinalizador da Internet do cache**](api-flags.md)[**\_ \_ \_**](api-flags.md) | Não faz solicitações de rede. Todas as entidades são retornadas do cache. Se o item solicitado não estiver no cache, um erro adequado, como o arquivo de \_ erro \_ não \_ encontrado, será retornado. Somente a função [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa esse sinalizador.                                                                                                                                                                                                       |
| [**sinalizador de INTERNET do \_ \_ FWD \_ back**](api-flags.md)                                                                                  | Indica que a função deve usar a cópia do recurso que está atualmente no cache da Internet. A data de validade e outras informações sobre o recurso não são verificadas. Se o item solicitado não for encontrado no cache da Internet, o sistema tentará localizar o recurso na rede. Esse valor foi introduzido no Microsoft Internet Explorer 5 e está associado às operações de botão **Avançar** e **voltar** do Internet Explorer. |
| [**\_hiperlink de sinalizador da Internet \_**](api-flags.md)                                                                                 | Força o aplicativo a recarregar um recurso se nenhum tempo de expiração e nenhuma hora da última modificação foi retornada quando o recurso foi armazenado no cache.                                                                                                                                                                                                                                                                                                                  |
| [**sinalizador da INTERNET \_ \_ tornar \_ persistente**](api-flags.md)                                                                    | Não tem mais suporte.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**o \_ sinalizador da Internet \_ deve \_ armazenar a solicitação em cache \_**](api-flags.md)                                                             | Faz com que um arquivo temporário seja criado se o arquivo não puder ser armazenado em cache. Isso é idêntico ao valor preferencial, o [**sinalizador de Internet \_ \_ precisa de \_ arquivo**](api-flags.md).                                                                                                                                                                                                                                                                            |
| [**sinalizador de INTERNET- \_ \_ \_ arquivo necessário**](api-flags.md)                                                                                | Faz com que um arquivo temporário seja criado se o arquivo não puder ser armazenado em cache.                                                                                                                                                                                                                                                                                                                                                                                               |
| [**sinalizador da INTERNET \_ \_ sem \_ gravação de cache \_**](api-flags.md)                                                                     | Rejeita qualquer tentativa da função para armazenar dados baixados da Internet no cache. Esse sinalizador será necessário se o aplicativo não quiser que os recursos baixados sejam armazenados localmente.                                                                                                                                                                                                                                                               |
| [**\_sinalizador \_ da Internet sem \_ interface do usuário**](api-flags.md)                                                                                        | Desabilita a caixa de diálogo cookie. Esse sinalizador pode ser usado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (somente solicitações HTTP).                                                                                                                                                                                                                                                                                          |
| [**sinalizador de INTERNET \_ \_ offline**](api-flags.md)                                                                                     | Impede que o aplicativo envie solicitações para a rede. Todas as solicitações são resolvidas usando os recursos armazenados no cache. Se o recurso não estiver no cache, um erro adequado, como o arquivo de \_ erro \_ não \_ encontrado, será retornado.                                                                                                                                                                                                                            |
| [**PRAGMA do sinalizador de INTERNET \_ \_ \_ NoCache**](api-flags.md)                                                                      | Força a solicitação a ser resolvida pelo servidor de origem, mesmo que exista uma cópia armazenada em cache no proxy. A função [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (somente em solicitações HTTP e HTTPS) e a função [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usam esse sinalizador.                                                                                                                                                                                               |
| [**recarregamento de sinalizador da INTERNET \_ \_**](api-flags.md)                                                                                       | Força a função a recuperar o recurso solicitado diretamente da Internet. As informações baixadas são armazenadas no cache.                                                                                                                                                                                                                                                                                                                     |
| [**sinalizador de INTERNET \_ \_ ressincronizar**](api-flags.md)                                                                         | Faz com que um aplicativo execute um download condicional do recurso da Internet. Se a versão armazenada no cache estiver atualizada, as informações serão baixadas do cache. Caso contrário, as informações serão recarregadas do servidor.                                                                                                                                                                                                                   |



 

## <a name="persistent-caching-functions"></a>Funções de cache persistentes

Os clientes que precisam de serviços de cache persistentes usam as funções de cache persistentes para permitir que seus aplicativos salvem dados no sistema de arquivos local para uso posterior, como em situações em que um link de baixa largura de banda limita o acesso aos dados ou o acesso não está disponível.

As funções de cache fornecem cache persistente e navegação offline. A menos que o [**sinalizador da Internet sem sinalizador de \_ \_ \_ \_ gravação de cache não**](api-flags.md) especifique explicitamente nenhum cache, as funções armazenam em cache todos os dados baixados da rede. As respostas para postar dados não são armazenadas em cache.

## <a name="using-the-persistent-url-cache-functions"></a>Usando as funções de cache de URL persistentes

As seguintes funções de cache de URL persistentes permitem que um aplicativo acesse e manipule informações armazenadas no cache.



| Função                                                           | Descrição                                                                                                                                                   |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitUrlCacheEntryA**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)               | Armazena em cache os dados no arquivo especificado no armazenamento de cache e associa-os à URL fornecida.                                                                  |
| [**CommitUrlCacheEntryW**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentryw)               | Armazena em cache os dados no arquivo especificado no armazenamento de cache e associa-os à URL fornecida.                                                                  |
| [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya)                 | Aloca o armazenamento de cache solicitado e cria um nome de arquivo local para salvar a entrada de cache que corresponde ao nome de origem.                           |
| [**CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup)                 | Gera uma identificação de grupo de cache.                                                                                                                       |
| [**DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry)                 | Remove o arquivo associado ao nome de origem do cache, se o arquivo existir.                                                                          |
| [**DeleteUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcachegroup)                 | Libera um **GroupId** e qualquer estado associado no arquivo de índice de cache.                                                                                      |
| [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache)                     | Fecha o identificador de enumeração especificado.                                                                                                                      |
| [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)           | Inicia a enumeração do cache.                                                                                                                          |
| [**FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa)       | Inicia uma enumeração filtrada do cache.                                                                                                                   |
| [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya)             | Recupera a próxima entrada no cache.                                                                                                                        |
| [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa)         | Recupera a próxima entrada em uma enumeração de cache filtrada.                                                                                                     |
| [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa)               | Recupera informações sobre uma entrada de cache.                                                                                                                    |
| [**GetUrlCacheEntryInfoEx**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoexa)           | Pesquisa a URL após a tradução de qualquer redirecionamento em cache que seria aplicado no modo offline por [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).           |
| [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)         | Lê os dados armazenados em cache de um fluxo que foi aberto usando [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).                            |
| [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea)     | Recupera uma entrada de cache do cache na forma de um arquivo.                                                                                                 |
| [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) | Fornece a maneira mais eficiente e independente de implementação de acessar os dados de cache.                                                                   |
| [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup)             | Adiciona ou remove entradas de um grupo de cache.                                                                                                                   |
| [**SetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentryinfoa)               | Define os membros especificados da estrutura [**de \_ \_ \_ informações de entrada de cache da Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) .                                                |
| [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile)         | Desbloqueia a entrada de cache que foi bloqueada quando o arquivo foi recuperado para uso do cache por [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea). |
| [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream)     | Fecha o fluxo que foi recuperado usando [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).                                           |



 

### <a name="enumerating-the-cache"></a>Enumerando o cache

As funções [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) e [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) enumeram as informações armazenadas no cache. [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) inicia a enumeração por meio de um padrão de pesquisa, um buffer e um tamanho de buffer para criar um identificador e retornar a primeira entrada de cache. [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) usa o identificador criado por [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya), um buffer e um tamanho de buffer para retornar a próxima entrada de cache.

Ambas as funções armazenam uma estrutura de informações de entrada de cache da Internet no buffer. [**\_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) O tamanho dessa estrutura varia para cada entrada. Se o tamanho do buffer passado para uma das funções for insuficiente, a função falhará e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará um erro de \_ buffer insuficiente \_ . A variável de tamanho do buffer contém o tamanho do buffer necessário para recuperar essa entrada de cache. Um buffer do tamanho indicado pela variável de tamanho do buffer deve ser alocado e a função deve ser chamada novamente com o novo buffer.

A estrutura de informações de entrada de cache da Internet contém o tamanho da estrutura, a URL das informações armazenadas em cache, o nome do arquivo local, o tipo de entrada de cache, a contagem de uso, a taxa de acesso, a hora da última modificação, a expiração, o último acesso, a hora da última sincronização, as informações do cabeçalho e a extensão do nome do arquivo [**\_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa)

A função [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) usa um padrão de pesquisa, um buffer que armazena a estrutura de informações de entrada de cache da [**Internet \_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) e o tamanho do buffer. Atualmente, apenas o padrão de pesquisa padrão, que retorna todas as entradas de cache, é implementado.

Depois que o cache é enumerado, o aplicativo deve chamar [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache) para fechar o identificador de enumeração de cache.

O exemplo a seguir exibe a URL de cada entrada de cache em uma caixa de listagem, **IDC \_ cachelist**. Ele usa \_ \_ \_ o tamanho máximo das informações de entrada de cache \_ para alocar inicialmente um buffer, já que as versões anteriores da API do Wininet não enumeram o cache corretamente de outra forma. As versões posteriores enumeram o cache corretamente e não há nenhum limite de tamanho de cache. Todos os aplicativos executados em computadores com a versão da API do WinINet do Internet Explorer 4,0 devem alocar um buffer do tamanho necessário. Para obter mais informações, consulte [usando buffers](appendix-b-using-buffers.md).


```C++
int WINAPI EnumerateCacheOld(HWND hX)
{
    DWORD dwEntrySize;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;
    DWORD MAX_CACHE_ENTRY_INFO_SIZE = 4096;
    HANDLE hCacheDir;
    int nCount=0;

    SendDlgItemMessage(hX,IDC_CacheList,LB_RESETCONTENT,0,0);
    
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
    lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
    lpCacheEntry->dwStructSize = dwEntrySize;

again:

    hCacheDir = FindFirstUrlCacheEntry(NULL,
                                       lpCacheEntry,
                                       &dwEntrySize);
    if (!hCacheDir)                                             
    {
        delete[]lpCacheEntry;
        switch(GetLastError())
        {
            case ERROR_NO_MORE_ITEMS: 
                TCHAR tempout[80];
                _stprintf_s(tempout, 
                            80,   
                            TEXT("The number of cache entries = %d \n"),
                            nCount);
                MessageBox(hX,tempout,TEXT("Cache Enumeration"),MB_OK);
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return TRUE;
                break;
            case ERROR_INSUFFICIENT_BUFFER:
                lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                                new char[dwEntrySize];
                lpCacheEntry->dwStructSize = dwEntrySize;
                goto again;
                break;
            default:
                ErrorOut( hX,GetLastError(),
                          TEXT("FindNextUrlCacheEntry Init"));
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return FALSE;
        }
    }

    SendDlgItemMessage(hX,IDC_CacheList,LB_ADDSTRING,
                       0,(LPARAM)(lpCacheEntry->lpszSourceUrlName));
    nCount++;
    delete (lpCacheEntry);

    do 
    {
        dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
        lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
        lpCacheEntry->dwStructSize = dwEntrySize;

retry:
        if (!FindNextUrlCacheEntry(hCacheDir,
                                   lpCacheEntry, 
                                   &dwEntrySize))
        {
            delete[]lpCacheEntry;
            switch(GetLastError())
            {
                case ERROR_NO_MORE_ITEMS: 
                    TCHAR tempout[80];
                    _stprintf_s(tempout,
                                80,
                                TEXT("The number of cache entries = %d \n"),nCount);
                    MessageBox(hX,
                               tempout,
                               TEXT("Cache Enumeration"),MB_OK);
                    FindCloseUrlCache(hCacheDir);
                    return TRUE;
                    break;
                case ERROR_INSUFFICIENT_BUFFER:
                    lpCacheEntry = 
                             (LPINTERNET_CACHE_ENTRY_INFO) 
                              new char[dwEntrySize];
                    lpCacheEntry->dwStructSize = dwEntrySize;
                    goto retry;
                    break;
                default:
                    ErrorOut(hX,
                             GetLastError(),
                             TEXT("FindNextUrlCacheEntry Init"));
                    FindCloseUrlCache(hCacheDir);
                    return FALSE;
            }
        }

        SendDlgItemMessage(hX,
                           IDC_CacheList,LB_ADDSTRING,
                           0,
                          (LPARAM)(lpCacheEntry->lpszSourceUrlName));
        nCount++;
        delete[] lpCacheEntry;        
    }  while (TRUE);

    SetCursor(LoadCursor(NULL,IDC_ARROW));
    return TRUE;        
}
```



### <a name="retrieving-cache-entry-information"></a>Recuperando informações de entrada de cache

A função [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) permite recuperar a estrutura [**de \_ \_ \_ informações de entrada de cache da Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) para a URL especificada. Essa estrutura contém o tamanho da estrutura, a URL das informações armazenadas em cache, o nome do arquivo local, o tipo de entrada do cache, a contagem de uso, a taxa de acesso, a hora da última modificação, a expiração, o último acesso, a hora da última sincronização, as informações do cabeçalho, o tamanho das informações do cabeçalho e a extensão do nome

O [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) aceita uma URL, um buffer para uma estrutura de informações de entrada de cache da [**Internet \_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) e o tamanho do buffer. Se a URL for encontrada, as informações serão copiadas no buffer. Caso contrário, a função falhará e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o arquivo de erro \_ \_ não \_ encontrado. Se o tamanho do buffer for insuficiente para armazenar as informações de entrada de cache, a função falhará e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará um erro de \_ buffer insuficiente \_ . O tamanho necessário para recuperar as informações é armazenado na variável de tamanho do buffer.

O [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) não faz nenhuma análise de URL, portanto, uma URL que contém uma âncora ( \# ) não será encontrada no cache, mesmo que o recurso seja armazenado em cache. Por exemplo, se a URL " https://example.com/example.htm\#sample " for passada, a função retornará o \_ arquivo de erro \_ não \_ encontrado mesmo se " https://example.com/example.htm " estiver no cache.

O exemplo a seguir recupera as informações de entrada de cache para a URL especificada. Em seguida, a função exibe as informações de cabeçalho na caixa de edição **IDC \_ CacheDump** .


```C++
int WINAPI GetCacheEntryInfo(HWND hX,LPTSTR lpszUrl)
{
    DWORD dwEntrySize=0;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;

    SetCursor(LoadCursor(NULL,IDC_WAIT));
    if (!GetUrlCacheEntryInfo(lpszUrl,NULL,&dwEntrySize))
    {
        if (GetLastError()!=ERROR_INSUFFICIENT_BUFFER)
        {
            ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
            lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                            new char[dwEntrySize];
    }
    else
        return FALSE; // should not be successful w/ NULL buffer
                      // and 0 size

    if (!GetUrlCacheEntryInfo(lpszUrl,lpCacheEntry,&dwEntrySize))
    {
        ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return FALSE;
    }
    else
    {
        if ((lpCacheEntry->dwHeaderInfoSize)!=0)
        {
            LPSTR(lpCacheEntry->lpHeaderInfo)
                                [lpCacheEntry->dwHeaderInfoSize]=TEXT('\0');
            SetDlgItemText(hX,IDC_Headers,
                           lpCacheEntry->lpHeaderInfo);
        }
        else
        {
            SetDlgItemText(hX,IDC_Headers,TEXT("None"));
        }

        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return TRUE;
    }
        
}
```



### <a name="creating-a-cache-entry"></a>Criando uma entrada de cache

Um aplicativo usa as funções [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) e [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) para criar uma entrada de cache.

[**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) aceita a URL, o tamanho de arquivo esperado e a extensão de nome de arquivo. Em seguida, a função cria um nome de arquivo local para salvar a entrada de cache que corresponde à URL e à extensão de nome de arquivo.

Usando o nome do arquivo local, grave os dados no arquivo local. Depois que os dados tiverem sido gravados no arquivo local, o aplicativo deverá chamar [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).

[**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) aceita a URL, o nome do arquivo local, a expiração, a hora da última modificação, o tipo de entrada do cache, as informações do cabeçalho, o tamanho das informações do cabeçalho e a extensão do nome do arquivo Em seguida, a função armazena em cache os dados no arquivo especificado no armazenamento de cache e o associa à URL fornecida.

O exemplo a seguir usa o nome do arquivo local, criado por uma chamada anterior para [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya), armazenado na caixa de texto, **IDC \_ LocalFile**, para armazenar o texto da caixa de texto, **IDC \_ CacheDump**, na entrada de cache. Depois que os dados tiverem sido gravados no arquivo usando **fopen**, **fprintf** e **fclose**, a entrada será confirmada usando [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).


```C++
int WINAPI CommitEntry(HWND hX)
{
    LPTSTR lpszUrl, lpszExt, lpszFileName;
    LPTSTR lpszData,lpszSize;
    DWORD dwSize;
    DWORD dwEntryType=0;
    FILE *lpfCacheEntry;
    LPFILETIME lpdtmExpire, lpdtmLastModified;
    LPSYSTEMTIME lpdtmSysTime;
    errno_t err;

    if( SendDlgItemMessage(hX,IDC_RBNormal,BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + NORMAL_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBSticky, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + STICKY_CACHE_ENTRY;
    }
    else if(SendDlgItemMessage( hX,IDC_RBSparse, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + SPARSE_CACHE_ENTRY;
    }
 

    if( SendDlgItemMessage(hX,IDC_RBCookie, BM_GETCHECK,0,0))
    {
            dwEntryType = dwEntryType + COOKIE_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBUrl, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + URLHISTORY_CACHE_ENTRY;
    }


    if( SendDlgItemMessage(hX,IDC_RBNone, BM_GETCHECK,0,0) )
    {
        dwEntryType=0;
    }
        
    lpdtmSysTime = new SYSTEMTIME;
    lpdtmExpire = new FILETIME;
    lpdtmLastModified = new FILETIME;

    GetLocalTime(lpdtmSysTime);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmExpire);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmLastModified);
    delete(lpdtmSysTime);

    lpszUrl = new TCHAR[MAX_PATH];
    lpszFileName = new TCHAR[MAX_PATH];
    lpszExt = new TCHAR[5];
    lpszSize = new TCHAR[10];

    GetDlgItemText(hX,IDC_SourceURL,lpszUrl,MAX_PATH);
    GetDlgItemText(hX,IDC_LocalFile,lpszFileName,MAX_PATH);
    GetDlgItemText(hX,IDC_FileExt,lpszExt,5);

    GetDlgItemText(hX,IDC_SizeLow,lpszSize,10);
    dwSize = (DWORD)_ttol(lpszSize);
    delete(lpszSize);

    if (dwSize==0)
    {
        if((MessageBox(hX,
                       TEXT("Incorrect File Size.\nUsing 8000 characters, Okay?\n"),
                       TEXT("Commit Entry"),MB_YESNO))
                        ==IDYES)
        {
            dwSize = 8000;
        }
        else
        {
            return FALSE;
        }
    }

    lpszData = new TCHAR[dwSize];
    GetDlgItemText(hX,IDC_CacheDump,lpszData,dwSize);
        
     err = _tfopen_s(&lpfCacheEntry,lpszFileName,_T("w"));
     if (err)
        return FALSE;
    fprintf(lpfCacheEntry,"%s",lpszData);
    fclose(lpfCacheEntry);
    delete(lpszData);

    if ( !CommitUrlCacheEntry( lpszUrl, 
                               lpszFileName, 
                               *lpdtmExpire,
                               *lpdtmLastModified, 
                               dwEntryType,
                               NULL,
                               0,
                               lpszExt,
                               0) )
    {
        ErrorOut(hX,GetLastError(),TEXT("Commit Cache Entry"));
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return FALSE;
    }
    else
    {
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return TRUE;
    }
}
```



### <a name="deleting-a-cache-entry"></a>Excluindo uma entrada de cache

A função [**DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry) usa uma URL e remove o arquivo de cache associado a ela. Se o arquivo de cache não existir, a função falhará e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o arquivo de erro \_ \_ não \_ encontrado. Se o arquivo de cache estiver bloqueado ou em uso no momento, a função falhará e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o acesso ao erro \_ \_ negado. O arquivo é excluído quando desbloqueado.

### <a name="retrieving-cache-entry-files"></a>Recuperando arquivos de entrada de cache

Para aplicativos que exigem o nome de arquivo de um recurso, use as funções [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) e [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) . Os aplicativos que não exigem o nome do arquivo devem usar as funções [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama), [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)e [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream) para recuperar as informações no cache.

O [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) não faz nenhuma análise de URL, portanto, uma URL que contém uma âncora ( \# ) não será encontrada no cache, mesmo que o recurso seja armazenado em cache. Por exemplo, se a URL " https://example.com/example.htm\#sample " for passada, a função retornará o \_ arquivo de erro \_ não \_ encontrado mesmo se " https://example.com/example.htm " estiver no cache.

O [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) aceita uma URL, um buffer que armazena a estrutura de informações de entrada de cache da [**Internet \_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) e o tamanho do buffer. A função é recuperada e bloqueada para o chamador.

Depois que as informações no arquivo forem usadas, o aplicativo deverá chamar [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) para desbloquear o arquivo.

### <a name="cache-groups"></a>Grupos de cache

Para criar um grupo de cache, a função [**CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup) deve ser chamada para gerar um **GroupId** para o grupo de cache. As entradas podem ser adicionadas ao grupo de cache, fornecendo a URL da entrada de cache e o \_ sinalizador adicionar do grupo de cache da Internet \_ \_ à função [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup) . Para remover uma entrada de cache de um grupo, passe a URL da entrada de cache e o \_ sinalizador de remoção do grupo de caches da Internet \_ \_ para [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup).

As funções [**FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa) e [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa) podem ser usadas para enumerar as entradas em um grupo de cache especificado. Depois que a enumeração for concluída, a função deverá chamar [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache).

## <a name="handling-structures-with-variable-size-information"></a>Manipulando estruturas com informações de tamanho variável

O cache pode conter informações de tamanho variável para cada URL armazenada. Isso se reflete na estrutura [**de \_ \_ \_ informações da entrada de cache da Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) . Quando as funções de cache retornam essa estrutura, elas criam um buffer que sempre é o tamanho das informações de entrada de cache da Internet, além de qualquer informação de tamanho variável. [**\_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) Se um membro de ponteiro não for **nulo**, ele apontará para a área de memória imediatamente após a estrutura. Ao copiar o buffer retornado por uma função em outro buffer, os membros do ponteiro devem ser corrigidos para apontar para o local apropriado no novo buffer, como mostra o exemplo a seguir.

``` syntax
lpDstCEInfo->lpszSourceUrlName = 
    (LPINTERNET_CACHE_ENTRY_INFO) ((LPBYTE) lpSrcCEInfo + 
       ((DWORD)(lpOldCEInfo->lpszSourceUrlName) - (DWORD)lpOldCEInfo));
```

Algumas funções de cache falharão com a \_ mensagem de erro de buffer insuficiente \_ se você especificar um buffer que é muito pequeno para conter as informações de entrada de cache recuperadas pela função. Nesse caso, a função também retorna o tamanho necessário do buffer. Em seguida, você pode alocar um buffer do tamanho apropriado e chamar a função novamente.

> [!Note]  
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 
