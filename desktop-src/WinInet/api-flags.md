---
title: Sinalizadores de API (Wininet. h)
description: Muitas das funções do WinINet aceitam uma matriz de sinalizadores como um parâmetro. Veja a seguir uma breve descrição dos sinalizadores definidos.
ms.assetid: 63027a3b-dc59-41c4-a22a-5d6e841159aa
topic_type:
- apiref
api_name:
- INTERNET_COOKIE_EVALUATE_P3P
- INTERNET_COOKIE_THIRD_PARTY
- INTERNET_FLAG_ASYNC
- INTERNET_FLAG_CACHE_ASYNC
- INTERNET_FLAG_CACHE_IF_NET_FAIL
- INTERNET_FLAG_DONT_CACHE
- INTERNET_FLAG_EXISTING_CONNECT
- INTERNET_FLAG_FORMS_SUBMIT
- INTERNET_FLAG_FROM_CACHE
- INTERNET_FLAG_FWD_BACK
- INTERNET_FLAG_HYPERLINK
- INTERNET_FLAG_IGNORE_CERT_CN_INVALID
- INTERNET_FLAG_IGNORE_CERT_DATE_INVALID
- INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP
- INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS
- INTERNET_FLAG_KEEP_CONNECTION
- INTERNET_FLAG_MAKE_PERSISTENT
- INTERNET_FLAG_MUST_CACHE_REQUEST
- INTERNET_FLAG_NEED_FILE
- INTERNET_FLAG_NO_AUTH
- INTERNET_FLAG_NO_AUTO_REDIRECT
- INTERNET_FLAG_NO_CACHE_WRITE
- INTERNET_FLAG_NO_COOKIES
- INTERNET_FLAG_NO_UI
- INTERNET_FLAG_OFFLINE
- INTERNET_FLAG_PASSIVE
- INTERNET_FLAG_PRAGMA_NOCACHE
- INTERNET_FLAG_RAW_DATA
- INTERNET_FLAG_READ_PREFETCH
- INTERNET_FLAG_RELOAD
- INTERNET_FLAG_RESTRICTED_ZONE
- INTERNET_FLAG_RESYNCHRONIZE
- INTERNET_FLAG_SECURE
- INTERNET_FLAG_TRANSFER_ASCII
- INTERNET_FLAG_TRANSFER_BINARY
- INTERNET_NO_CALLBACK
- INTERNET_OPTION_SUPPRESS_SERVER_AUTH
- WININET_API_FLAG_ASYNC
- WININET_API_FLAG_SYNC
- WININET_API_FLAG_USE_CONTEXT
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a111bf418e6cf599f99c9dfa34ca0f5025a1d779
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105798240"
---
# <a name="api-flags"></a>Sinalizadores de API

Muitas das funções do WinINet aceitam uma matriz de sinalizadores como um parâmetro. Veja a seguir uma breve descrição dos sinalizadores definidos.

<dl> <dt>

<span id="INTERNET_COOKIE_EVALUATE_P3P"></span><span id="internet_cookie_evaluate_p3p"></span>**O \_ Cookie da Internet \_ avaliar \_ P3P**
</dt> <dd> <dl> <dt>

0x80
</dt> <dt>



Indica que uma plataforma para o cabeçalho da proteção de privacidade (P3P) deve ser associada a um cookie.


</dt> </dl> </dd> <dt>

<span id="INTERNET_COOKIE_THIRD_PARTY"></span><span id="internet_cookie_third_party"></span>**COOKIE de INTERNET \_ \_ terceirizado \_**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>



Indica que um cookie de terceiros está sendo definido ou recuperado.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_ASYNC"></span><span id="internet_flag_async"></span>**sinalizador de INTERNET \_ \_ assíncrono**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



Faz com que somente solicitações assíncronas em identificadores sejam decrescentes do identificador retornado por essa função. Somente a função [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa esse sinalizador.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_CACHE_ASYNC"></span><span id="internet_flag_cache_async"></span>**CACHE de sinalizador da INTERNET \_ \_ \_ assíncrono**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Permite uma gravação de cache lenta.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_CACHE_IF_NET_FAIL"></span><span id="internet_flag_cache_if_net_fail"></span>**CACHE de sinalizador da INTERNET \_ \_ \_ se \_ net \_ falhar**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Retorna o recurso do cache se a solicitação de rede para o recurso falhar devido a um [erro \_ de \_ \_ redefinição de conexão com a Internet](wininet-errors.md) ou [erro a \_ Internet \_ não pode \_ se conectar](wininet-errors.md) . Esse sinalizador é usado pelo [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_DONT_CACHE"></span><span id="internet_flag_dont_cache"></span>**sinalizador da INTERNET não \_ \_ \_ cache**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



Não adiciona a entidade retornada ao cache. Isso é idêntico ao valor preferencial, [Internet \_ Flag \_ sem \_ \_ gravação de cache](/windows).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_EXISTING_CONNECT"></span><span id="internet_flag_existing_connect"></span>**conexão do sinalizador de INTERNET \_ \_ existente \_**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Tenta usar um objeto [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) existente se existir um com os mesmos atributos necessários para fazer a solicitação. Isso é útil apenas com as operações de FTP, pois o FTP é o único protocolo que normalmente executa várias operações durante a mesma sessão. O WinINet armazena em cache um único identificador de conexão para cada identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) gerado pelo [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). As funções [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) e **InternetConnect** usam esse sinalizador para conexões http e FTP.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FORMS_SUBMIT"></span><span id="internet_flag_forms_submit"></span>**\_envio de \_ formulários de sinalizador da Internet \_**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Indica que se trata de um envio de formulários.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FROM_CACHE"></span><span id="internet_flag_from_cache"></span>**\_sinalizador \_ da Internet do \_ cache**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



Não faz solicitações de rede. Todas as entidades são retornadas do cache. Se o item solicitado não estiver no cache, um erro adequado, como o arquivo de \_ erro \_ não \_ encontrado, será retornado. Somente a função [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa esse sinalizador.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FWD_BACK"></span><span id="internet_flag_fwd_back"></span>**sinalizador de INTERNET do \_ \_ FWD \_ back**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Indica que a função deve usar a cópia do recurso que está atualmente no cache da Internet. A data de validade e outras informações sobre o recurso não são verificadas. Se o item solicitado não for encontrado no cache da Internet, o sistema tentará localizar o recurso na rede. Esse valor foi introduzido no Microsoft Internet Explorer 5 e está associado às operações de botão **Avançar** e **voltar** do Internet Explorer.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_HYPERLINK"></span><span id="internet_flag_hyperlink"></span>**\_hiperlink de sinalizador da Internet \_**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



Força uma recarga se não houver tempo de expiração e nenhum horário de LastModified retornado do servidor ao determinar se deseja recarregar o item da rede. Esse sinalizador pode ser usado por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

**Windows XP e Windows Server 2003 R2 e anteriores:** Também usado por [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) e [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="internet_flag_ignore_cert_cn_invalid"></span>**sinalizador da INTERNET \_ \_ ignorar \_ CN do certificado \_ \_ inválido**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Desabilita a verificação de certificados baseados em SSL/PCT que são retornados do servidor em relação ao nome de host fornecido na solicitação. O WinINet usa uma verificação simples em relação a certificados por meio da comparação de nomes de host correspondentes e regras de curinga simples. Esse sinalizador pode ser usado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para solicitações HTTP).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="internet_flag_ignore_cert_date_invalid"></span>**sinalizador de INTERNET \_ \_ ignorar \_ data de certificado \_ \_ inválida**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Desabilita a verificação de certificados baseados em SSL/PCT para datas de validade adequadas. Esse sinalizador pode ser usado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para solicitações HTTP).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="internet_flag_ignore_redirect_to_http"></span>**sinalizador da INTERNET \_ \_ ignorar \_ redirecionamento \_ para \_ http**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



Desabilita a detecção desse tipo especial de redirecionamento. Quando esse sinalizador é usado, o WinINet permite de forma transparente redirecionamentos de HTTPS para URLs HTTP. Esse sinalizador pode ser usado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para solicitações HTTP).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="internet_flag_ignore_redirect_to_https"></span>**sinalizador da INTERNET \_ \_ ignorar \_ redirecionamento \_ para \_ https**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Desabilita a detecção desse tipo especial de redirecionamento. Quando esse sinalizador é usado, o WinINet permite redirecionar de forma transparente as URLs de HTTP para HTTPS. Esse sinalizador pode ser usado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para solicitações HTTP).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_KEEP_CONNECTION"></span><span id="internet_flag_keep_connection"></span>**sinalizador de INTERNET \_ \_ manter \_ conexão**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



Usa semântica Keep-Alive, se disponível, para a conexão. Esse sinalizador é usado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para solicitações HTTP). Esse sinalizador é necessário para o Microsoft Network (MSN), o NTLM e outros tipos de autenticação.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_MAKE_PERSISTENT"></span><span id="internet_flag_make_persistent"></span>**sinalizador da INTERNET \_ \_ tornar \_ persistente**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



Não tem mais suporte.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_MUST_CACHE_REQUEST"></span><span id="internet_flag_must_cache_request"></span>**o \_ sinalizador da Internet \_ deve \_ armazenar a solicitação em cache \_**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Idêntico ao valor preferencial, o **sinalizador de Internet \_ \_ precisa de \_ arquivo**. Faz com que um arquivo temporário seja criado se o arquivo não puder ser armazenado em cache. Esse sinalizador pode ser usado por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

**Windows XP e Windows Server 2003 R2 e anteriores:** Também usado por [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) e [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NEED_FILE"></span><span id="internet_flag_need_file"></span>**sinalizador de INTERNET- \_ \_ \_ arquivo necessário**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Faz com que um arquivo temporário seja criado se o arquivo não puder ser armazenado em cache. Esse sinalizador pode ser usado por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

**Windows XP e Windows Server 2003 R2 e anteriores:** Também usado por [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) e [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_AUTH"></span><span id="internet_flag_no_auth"></span>**sinalizador da INTERNET \_ \_ sem \_ autenticação**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



O não tenta a autenticação automaticamente. Esse sinalizador pode ser usado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para solicitações HTTP).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_AUTO_REDIRECT"></span><span id="internet_flag_no_auto_redirect"></span>**sinalizador da INTERNET \_ \_ sem \_ \_ redirecionamento automático**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



O não manipula automaticamente o redirecionamento no [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). Esse sinalizador também pode ser usado pelo [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) para solicitações HTTP.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_CACHE_WRITE"></span><span id="internet_flag_no_cache_write"></span>**sinalizador da INTERNET \_ \_ sem \_ gravação de cache \_**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



Não adiciona a entidade retornada ao cache. Esse sinalizador é usado por, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

**Windows XP e Windows Server 2003 R2 e anteriores:** Também usado por [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) e [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_COOKIES"></span><span id="internet_flag_no_cookies"></span>**sinalizador da INTERNET \_ \_ sem \_ cookies**
</dt> <dd> <dl> <dt>

0x00080000
</dt> <dt>



Não adiciona automaticamente cabeçalhos de cookie a solicitações e não adiciona automaticamente cookies retornados ao banco de dados de cookie. Esse sinalizador pode ser usado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para solicitações HTTP).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_UI"></span><span id="internet_flag_no_ui"></span>**\_sinalizador \_ da Internet sem \_ interface do usuário**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Desabilita a caixa de diálogo cookie. Esse sinalizador pode ser usado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (somente solicitações HTTP).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_OFFLINE"></span><span id="internet_flag_offline"></span>**sinalizador de INTERNET \_ \_ offline**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



Idêntico ao **\_ sinalizador \_ da Internet do \_ cache**. Não faz solicitações de rede. Todas as entidades são retornadas do cache. Se o item solicitado não estiver no cache, um erro adequado, como o arquivo de \_ erro \_ não \_ encontrado, será retornado. Somente a função [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa esse sinalizador.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_PASSIVE"></span><span id="internet_flag_passive"></span>**sinalizador de INTERNET \_ \_ passivo**
</dt> <dd> <dl> <dt>

0x08000000
</dt> <dt>



Usa a semântica de FTP passiva. Somente [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usam esse sinalizador. O [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usa esse sinalizador para solicitações de FTP e o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usa esse sinalizador para arquivos e diretórios FTP.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_PRAGMA_NOCACHE"></span><span id="internet_flag_pragma_nocache"></span>**PRAGMA do sinalizador de INTERNET \_ \_ \_ NoCache**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Força a solicitação a ser resolvida pelo servidor de origem, mesmo que exista uma cópia armazenada em cache no proxy. A função [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (somente em solicitações HTTP e HTTPS) e a função [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usam esse sinalizador.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RAW_DATA"></span><span id="internet_flag_raw_data"></span>**sinalizador de INTERNET \_ \_ dados brutos \_**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Retorna os dados como uma estrutura de [**\_ \_ dados de localização do Win32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) ao recuperar informações do diretório FTP. Se esse sinalizador não for especificado ou se a chamada for feita por meio de um proxy CERN, [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) retornará a versão HTML do diretório. Somente a função [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usa esse sinalizador.

**Windows XP e Windows Server 2003 R2 e anteriores:** Também retorna uma estrutura de [**\_ \_ dados de localização do Gopher**](/windows/desktop/api/Wininet/ns-wininet-gopher_find_dataa) ao recuperar informações de diretório do Gopher.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_READ_PREFETCH"></span><span id="internet_flag_read_prefetch"></span>**\_pré-busca de \_ leitura do sinalizador da Internet \_**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



Este sinalizador está desabilitado no momento.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RELOAD"></span><span id="internet_flag_reload"></span>**recarregamento de sinalizador da INTERNET \_ \_**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



Força um download da listagem de arquivo, objeto ou diretório solicitada do servidor de origem, não do cache. As funções [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usam esse sinalizador.

**Windows XP e Windows Server 2003 R2 e anteriores:** Também usado por [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) e [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RESTRICTED_ZONE"></span><span id="internet_flag_restricted_zone"></span>**\_ \_ zona restrita de sinalizador da Internet \_**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Indica que o cookie que está sendo definido está associado a um site não confiável.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RESYNCHRONIZE"></span><span id="internet_flag_resynchronize"></span>**sinalizador de INTERNET \_ \_ ressincronizar**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Recarregará recursos HTTP se o recurso tiver sido modificado desde a última vez que foi baixado. Todos os recursos de FTP são recarregados. Esse sinalizador pode ser usado por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

**Windows XP e Windows Server 2003 R2 e anteriores:** Também usado por [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) e [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), e os recursos de Gopher são recarregados.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_SECURE"></span><span id="internet_flag_secure"></span>**sinalizador de INTERNET \_ \_ seguro**
</dt> <dd> <dl> <dt>

0x00800000
</dt> <dt>



Usa semântica de transação segura. Isso se traduz em usar a tecnologia de comunicação protocolo SSL/privada (SSL/PCT) e só é significativo em solicitações HTTP. Esse sinalizador é usado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), mas isso será redundante se https://aparecer na URL. A função [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usa esse sinalizador para conexões http; todos os identificadores de solicitação criados nessa conexão herdarão esse sinalizador.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_TRANSFER_ASCII"></span><span id="internet_flag_transfer_ascii"></span>**\_ASCII de \_ transferência de sinalizador da Internet \_**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Transfere o arquivo como ASCII (somente FTP). Esse sinalizador pode ser usado por [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)e [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_TRANSFER_BINARY"></span><span id="internet_flag_transfer_binary"></span>**\_binário de \_ transferência de sinalizador da Internet \_**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Transfere o arquivo como binário (somente FTP). Esse sinalizador pode ser usado por [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)e [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_NO_CALLBACK"></span><span id="internet_no_callback"></span>**INTERNET \_ sem \_ retorno de chamada**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Indica que nenhum retorno de chamada deve ser feito para essa API. Isso é usado para o parâmetro *dxContext* das funções que permitem operações assíncronas.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**opção de INTERNET \_ \_ suprimir \_ autenticação de servidor \_**
</dt> <dd> <dl> <dt>

104
</dt> <dt>



Define um objeto de solicitação HTTP de modo que ele não fará logon nos servidores de origem, mas executará o logon automático em servidores proxy HTTP. Essa opção é diferente do sinalizador de solicitação da \_ Internet \_ sem \_ autenticação, o que impede a autenticação tanto nos servidores proxy quanto nos servidores de origem. Definir esse modo irá suprimir o uso de qualquer material de credencial (anteriormente fornecido nome de usuário/senha ou certificado SSL de cliente) ao se comunicar com um servidor de origem. No entanto, se a solicitação precisar transitar por meio de um proxy de autenticação, o WinINet ainda executará a autenticação automática para o proxy HTTP de acordo com as configurações de zona da intranet do usuário. A configuração de zona da intranet padrão é permitir o logon automático usando as credenciais padrão do usuário. Para garantir a supressão de todas as informações de identificação, o chamador deve combinar a opção da INTERNET \_ \_ suprimir a \_ autenticação do servidor \_ com o sinalizador Internet sem sinalizador de \_ solicitação de \_ \_ cookies. Essa opção só pode ser definida em objetos de solicitação antes de serem enviadas. As tentativas de definir essa opção após a solicitação ter sido enviada retornarão \_ um \_ estado de identificador incorreto da Internet \_ \_ . Nenhum buffer é necessário para essa opção. Isso é usado por InternetSetOption em identificadores retornados apenas por HttpOpenRequest. Versão: requer o Internet Explorer 8,0 ou posterior.


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_ASYNC"></span><span id="wininet_api_flag_async"></span>**sinalizador de API do WININET \_ \_ \_ assíncrono**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Força operações assíncronas.


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_SYNC"></span><span id="wininet_api_flag_sync"></span>**\_sincronização de \_ sinalizador de API do Wininet \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Força operações síncronas.


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_USE_CONTEXT"></span><span id="wininet_api_flag_use_context"></span>**\_contexto de \_ uso de sinalizador de API do Wininet \_ \_**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Força a API a usar o valor de contexto, mesmo se ele estiver definido como zero.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

> [!Note]  
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>WinInet. h</dt> </dl> |



 

