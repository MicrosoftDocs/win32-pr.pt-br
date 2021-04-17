---
title: Sinalizadores de opção (Wininet. h)
description: Os sinalizadores de opção a seguir são usados com as funções InternetQueryOption e InternetSetOption. Todos os sinalizadores de opção válidos têm um valor maior ou igual à \_ opção Internet First \_ e menor ou igual à \_ última \_ opção Internet.
ms.assetid: 708510b8-468a-4287-849b-cba3d7001ea8
topic_type:
- apiref
api_name:
- INTERNET_OPTION_ALTER_IDENTITY
- INTERNET_OPTION_ASYNC
- INTERNET_OPTION_ASYNC_ID
- INTERNET_OPTION_ASYNC_PRIORITY
- INTERNET_OPTION_BYPASS_EDITED_ENTRY
- INTERNET_OPTION_CACHE_STREAM_HANDLE
- INTERNET_OPTION_CACHE_TIMESTAMPS
- INTERNET_OPTION_CALLBACK
- INTERNET_OPTION_CALLBACK_FILTER
- INTERNET_OPTION_CLIENT_CERT_CONTEXT
- INTERNET_OPTION_CODEPAGE
- INTERNET_OPTION_CODEPAGE_PATH
- INTERNET_OPTION_CODEPAGE_EXTRA
- INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH
- INTERNET_OPTION_CONNECT_BACKOFF
- INTERNET_OPTION_CONNECT_RETRIES
- INTERNET_OPTION_CONNECT_TIME
- INTERNET_OPTION_CONNECT_TIMEOUT
- INTERNET_OPTION_CONNECTED_STATE
- INTERNET_OPTION_CONTEXT_VALUE
- INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT
- INTERNET_OPTION_CONTROL_SEND_TIMEOUT
- INTERNET_OPTION_DATA_RECEIVE_TIMEOUT
- INTERNET_OPTION_DATA_SEND_TIMEOUT
- INTERNET_OPTION_DATAFILE_NAME
- INTERNET_OPTION_DATAFILE_EXT
- INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO
- INTERNET_OPTION_DIGEST_AUTH_UNLOAD
- INTERNET_OPTION_DISABLE_AUTODIAL
- INTERNET_OPTION_DISCONNECTED_TIMEOUT
- INTERNET_OPTION_ENABLE_HTTP_PROTOCOL
- INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ
- INTERNET_OPTION_ENCODE_EXTRA
- INTERNET_OPTION_END_BROWSER_SESSION
- INTERNET_OPTION_ERROR_MASK
- INTERNET_OPTION_ENTERPRISE_CONTEXT
- INTERNET_OPTION_EXTENDED_ERROR
- INTERNET_OPTION_FROM_CACHE_TIMEOUT
- INTERNET_OPTION_HANDLE_TYPE
- INTERNET_OPTION_HSTS
- INTERNET_OPTION_HTTP_DECODING
- INTERNET_OPTION_HTTP_PROTOCOL_USED
- INTERNET_OPTION_HTTP_VERSION
- INTERNET_OPTION_IDENTITY
- INTERNET_OPTION_IDLE_STATE
- INTERNET_OPTION_IDN
- INTERNET_OPTION_IGNORE_OFFLINE
- INTERNET_OPTION_KEEP_CONNECTION
- INTERNET_OPTION_LISTEN_TIMEOUT
- INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER
- INTERNET_OPTION_MAX_CONNS_PER_PROXY
- INTERNET_OPTION_MAX_CONNS_PER_SERVER
- INTERNET_OPTION_OFFLINE_MODE
- INTERNET_OPTION_OFFLINE_SEMANTICS
- INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE
- INTERNET_OPTION_PARENT_HANDLE
- INTERNET_OPTION_PASSWORD
- INTERNET_OPTION_PER_CONNECTION_OPTION
- INTERNET_OPTION_POLICY
- INTERNET_OPTION_PROXY
- INTERNET_OPTION_PROXY_PASSWORD
- INTERNET_OPTION_PROXY_SETTINGS_CHANGED
- INTERNET_OPTION_PROXY_USERNAME
- INTERNET_OPTION_READ_BUFFER_SIZE
- INTERNET_OPTION_RECEIVE_THROUGHPUT
- INTERNET_OPTION_RECEIVE_TIMEOUT
- INTERNET_OPTION_REFRESH
- INTERNET_OPTION_REMOVE_IDENTITY
- INTERNET_OPTION_REQUEST_FLAGS
- INTERNET_OPTION_REQUEST_PRIORITY
- INTERNET_OPTION_RESET_URLCACHE_SESSION
- INTERNET_OPTION_SECONDARY_CACHE_KEY
- INTERNET_OPTION_SECURITY_CERTIFICATE
- INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT
- INTERNET_OPTION_SECURITY_FLAGS
- INTERNET_OPTION_SECURITY_KEY_BITNESS
- INTERNET_OPTION_SEND_THROUGHPUT
- INTERNET_OPTION_SEND_TIMEOUT
- INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT
- INTERNET_OPTION_SETTINGS_CHANGED
- INTERNET_OPTION_SUPPRESS_SERVER_AUTH
- INTERNET_OPTION_SUPPRESS_BEHAVIOR
- INTERNET_OPTION_URL
- INTERNET_OPTION_USER_AGENT
- INTERNET_OPTION_USERNAME
- INTERNET_OPTION_VERSION
- INTERNET_OPTION_WRITE_BUFFER_SIZE
api_location:
- Wininet.h
- Winineti.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0c99ca6f12836c620ed7c952e0ceb1844aee3b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105789727"
---
# <a name="option-flags-winineth"></a><span data-ttu-id="38db0-104">Sinalizadores de opção (Wininet. h)</span><span class="sxs-lookup"><span data-stu-id="38db0-104">Option Flags (Wininet.h)</span></span>

<span data-ttu-id="38db0-105">Os sinalizadores de opção a seguir são usados com as funções [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) .</span><span class="sxs-lookup"><span data-stu-id="38db0-105">The following option flags are used with the [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) functions.</span></span> <span data-ttu-id="38db0-106">Todos os sinalizadores de opção válidos têm um valor maior ou igual **à \_ \_ opção Internet First** e menor ou igual à **\_ última \_ opção Internet**.</span><span class="sxs-lookup"><span data-stu-id="38db0-106">All valid option flags have a value greater than or equal to **INTERNET\_FIRST\_OPTION** and less than or equal to **INTERNET\_LAST\_OPTION**.</span></span>

<dl> <dt>

<span data-ttu-id="38db0-107"><span id="INTERNET_OPTION_ALTER_IDENTITY"></span><span id="internet_option_alter_identity"></span>**\_opção de \_ alteração de \_ identidade da Internet**</span><span class="sxs-lookup"><span data-stu-id="38db0-107"><span id="INTERNET_OPTION_ALTER_IDENTITY"></span><span id="internet_option_alter_identity"></span>**INTERNET\_OPTION\_ALTER\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-108">80</span><span class="sxs-lookup"><span data-stu-id="38db0-108">80</span></span>
</dt> <dt>



<span data-ttu-id="38db0-109">Não implementado</span><span class="sxs-lookup"><span data-stu-id="38db0-109">Not implemented</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-110"><span id="INTERNET_OPTION_ASYNC"></span><span id="internet_option_async"></span>**opção da INTERNET \_ \_ assíncrona**</span><span class="sxs-lookup"><span data-stu-id="38db0-110"><span id="INTERNET_OPTION_ASYNC"></span><span id="internet_option_async"></span>**INTERNET\_OPTION\_ASYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-111">30</span><span class="sxs-lookup"><span data-stu-id="38db0-111">30</span></span>
</dt> <dt>



<span data-ttu-id="38db0-112">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="38db0-112">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-113"><span id="INTERNET_OPTION_ASYNC_ID"></span><span id="internet_option_async_id"></span>**\_ \_ ID assíncrona da opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-113"><span id="INTERNET_OPTION_ASYNC_ID"></span><span id="internet_option_async_id"></span>**INTERNET\_OPTION\_ASYNC\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-114">15</span><span class="sxs-lookup"><span data-stu-id="38db0-114">15</span></span>
</dt> <dt>



<span data-ttu-id="38db0-115">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="38db0-115">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-116"><span id="INTERNET_OPTION_ASYNC_PRIORITY"></span><span id="internet_option_async_priority"></span>**\_ \_ prioridade assíncrona da opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-116"><span id="INTERNET_OPTION_ASYNC_PRIORITY"></span><span id="internet_option_async_priority"></span>**INTERNET\_OPTION\_ASYNC\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-117">16</span><span class="sxs-lookup"><span data-stu-id="38db0-117">16</span></span>
</dt> <dt>



<span data-ttu-id="38db0-118">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="38db0-118">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-119"><span id="INTERNET_OPTION_BYPASS_EDITED_ENTRY"></span><span id="internet_option_bypass_edited_entry"></span>**opção da INTERNET para \_ \_ ignorar a \_ entrada editada \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-119"><span id="INTERNET_OPTION_BYPASS_EDITED_ENTRY"></span><span id="internet_option_bypass_edited_entry"></span>**INTERNET\_OPTION\_BYPASS\_EDITED\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-120">64</span><span class="sxs-lookup"><span data-stu-id="38db0-120">64</span></span>
</dt> <dt>



<span data-ttu-id="38db0-121">Define ou recupera o valor booliano que determina se o sistema deve verificar a rede quanto ao conteúdo mais recente e substituir as entradas de cache editadas se uma versão mais recente for encontrada.</span><span class="sxs-lookup"><span data-stu-id="38db0-121">Sets or retrieves the Boolean value that determines if the system should check the network for newer content and overwrite edited cache entries if a newer version is found.</span></span> <span data-ttu-id="38db0-122">Se definido como **true**, o sistema verificará a rede em busca de conteúdo mais recente e substituirá a entrada de cache editada pela versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="38db0-122">If set to **True**, the system checks the network for newer content and overwrites the edited cache entry with the newer version.</span></span> <span data-ttu-id="38db0-123">O padrão é **false**, que indica que a entrada de cache editada deve ser usada sem verificar a rede.</span><span class="sxs-lookup"><span data-stu-id="38db0-123">The default is **False**, which indicates that the edited cache entry should be used without checking the network.</span></span> <span data-ttu-id="38db0-124">Isso é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-124">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="38db0-125">Ele só é válido no Microsoft Internet Explorer 5 e posterior.</span><span class="sxs-lookup"><span data-stu-id="38db0-125">It is valid only in Microsoft Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-126"><span id="INTERNET_OPTION_CACHE_STREAM_HANDLE"></span><span id="internet_option_cache_stream_handle"></span>**\_identificador de \_ fluxo do cache de opção de Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-126"><span id="INTERNET_OPTION_CACHE_STREAM_HANDLE"></span><span id="internet_option_cache_stream_handle"></span>**INTERNET\_OPTION\_CACHE\_STREAM\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-127">27</span><span class="sxs-lookup"><span data-stu-id="38db0-127">27</span></span>
</dt> <dt>



<span data-ttu-id="38db0-128">Não tem mais suporte.</span><span class="sxs-lookup"><span data-stu-id="38db0-128">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-129"><span id="INTERNET_OPTION_CACHE_TIMESTAMPS"></span><span id="internet_option_cache_timestamps"></span>**\_ \_ carimbos de data/hora do cache de opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-129"><span id="INTERNET_OPTION_CACHE_TIMESTAMPS"></span><span id="internet_option_cache_timestamps"></span>**INTERNET\_OPTION\_CACHE\_TIMESTAMPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-130">69</span><span class="sxs-lookup"><span data-stu-id="38db0-130">69</span></span>
</dt> <dt>



<span data-ttu-id="38db0-131">Recupera uma estrutura de [**\_ \_ carimbos de data**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_timestamps) /hora de cache da Internet que contém a hora de LastModified e expira o tempo do recurso armazenado no cache da Internet.</span><span class="sxs-lookup"><span data-stu-id="38db0-131">Retrieves an [**INTERNET\_CACHE\_TIMESTAMPS**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_timestamps) structure that contains the LastModified time and Expires time from the resource stored in the Internet cache.</span></span> <span data-ttu-id="38db0-132">Esse valor é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-132">This value is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-133"><span id="INTERNET_OPTION_CALLBACK"></span><span id="internet_option_callback"></span>**retorno de chamada de \_ opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-133"><span id="INTERNET_OPTION_CALLBACK"></span><span id="internet_option_callback"></span>**INTERNET\_OPTION\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-134">1</span><span class="sxs-lookup"><span data-stu-id="38db0-134">1</span></span>
</dt> <dt>



<span data-ttu-id="38db0-135">Define ou recupera o endereço da função de retorno de chamada definida para este identificador.</span><span class="sxs-lookup"><span data-stu-id="38db0-135">Sets or retrieves the address of the callback function defined for this handle.</span></span> <span data-ttu-id="38db0-136">Essa opção pode ser usada em todos os identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="38db0-136">This option can be used on all [**HINTERNET**](appendix-a-hinternet-handles.md) handles.</span></span> <span data-ttu-id="38db0-137">Usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-137">Used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-138"><span id="INTERNET_OPTION_CALLBACK_FILTER"></span><span id="internet_option_callback_filter"></span>**\_filtro de \_ retorno de chamada de opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-138"><span id="INTERNET_OPTION_CALLBACK_FILTER"></span><span id="internet_option_callback_filter"></span>**INTERNET\_OPTION\_CALLBACK\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-139">54</span><span class="sxs-lookup"><span data-stu-id="38db0-139">54</span></span>
</dt> <dt>



<span data-ttu-id="38db0-140">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="38db0-140">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-141"><span id="INTERNET_OPTION_CLIENT_CERT_CONTEXT"></span><span id="internet_option_client_cert_context"></span>**\_contexto de \_ certificado de cliente de opção de Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-141"><span id="INTERNET_OPTION_CLIENT_CERT_CONTEXT"></span><span id="internet_option_client_cert_context"></span>**INTERNET\_OPTION\_CLIENT\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-142">84</span><span class="sxs-lookup"><span data-stu-id="38db0-142">84</span></span>
</dt> <dt>



<span data-ttu-id="38db0-143">Não há suporte para esse sinalizador no [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-143">This flag is not supported by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="38db0-144">O parâmetro *lpBuffer* deve ser um ponteiro para uma estrutura de [**\_ contexto de certificado**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) e não um ponteiro para um ponteiro de **\_ contexto de certificado** .</span><span class="sxs-lookup"><span data-stu-id="38db0-144">The *lpBuffer* parameter must be a pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structure and not a pointer to a **CERT\_CONTEXT** pointer.</span></span> <span data-ttu-id="38db0-145">Se um aplicativo receber um **erro de certificado de autenticação de cliente de \_ Internet \_ \_ \_ \_ necessário**, ele deverá chamar [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) ou usar [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) para fornecer um certificado antes de repetir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="38db0-145">If an application receives **ERROR\_INTERNET\_CLIENT\_AUTH\_CERT\_NEEDED**, it must call [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) or use [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) to supply a certificate before retrying the request.</span></span> <span data-ttu-id="38db0-146">Em seguida, [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) é chamado para que o contexto de certificado passado possa ser liberado independentemente pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="38db0-146">[**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) is then called so that the certificate context passed can be independently released by the application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-147"><span id="INTERNET_OPTION_CODEPAGE"></span><span id="internet_option_codepage"></span>**página de código da \_ opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-147"><span id="INTERNET_OPTION_CODEPAGE"></span><span id="internet_option_codepage"></span>**INTERNET\_OPTION\_CODEPAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-148">68</span><span class="sxs-lookup"><span data-stu-id="38db0-148">68</span></span>
</dt> <dt>



<span data-ttu-id="38db0-149">Por padrão, a parte de host ou autoridade da URL Unicode é codificada de acordo com a especificação de IDN.</span><span class="sxs-lookup"><span data-stu-id="38db0-149">By default, the host or authority portion of the Unicode URL is encoded according to the IDN specification.</span></span> <span data-ttu-id="38db0-150">Definir essa opção na solicitação ou no identificador de conexão, quando o IDN estiver desabilitado, especifica um esquema de codificação de página de código para a parte do host da URL.</span><span class="sxs-lookup"><span data-stu-id="38db0-150">Setting this option on the request, or connection handle, when IDN is disabled, specifies a code page encoding scheme for the host portion of the URL.</span></span> <span data-ttu-id="38db0-151">O parâmetro *lpBuffer* na chamada a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contém a página de código DBCS desejada.</span><span class="sxs-lookup"><span data-stu-id="38db0-151">The *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contains the desired DBCS code page.</span></span> <span data-ttu-id="38db0-152">Se nenhuma página de código for especificada em *lpBuffer*, o WinInet usará a página de código do sistema padrão (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="38db0-152">If no code page is specified in *lpBuffer*, WinINet uses the default system code page (CP\_ACP).</span></span> <span data-ttu-id="38db0-153">Observação: essa opção será ignorada se o IDN não estiver desabilitado.</span><span class="sxs-lookup"><span data-stu-id="38db0-153">Note: This option is ignored if IDN is not disabled.</span></span> <span data-ttu-id="38db0-154">Para obter mais informações sobre como desabilitar o IDN, consulte a opção **Internet \_ Option \_ IDN** .</span><span class="sxs-lookup"><span data-stu-id="38db0-154">For more information about how to disable IDN, see the **INTERNET\_OPTION\_IDN** option.</span></span>

<span data-ttu-id="38db0-155">**Windows XP com SP2 e Windows Server 2003 com SP1:** Não há suporte para esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="38db0-155">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="38db0-156">**Versão:** Requer o Internet Explorer 7,0.</span><span class="sxs-lookup"><span data-stu-id="38db0-156">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-157"><span id="INTERNET_OPTION_CODEPAGE_PATH"></span><span id="internet_option_codepage_path"></span>**\_caminho de \_ página de código de opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-157"><span id="INTERNET_OPTION_CODEPAGE_PATH"></span><span id="internet_option_codepage_path"></span>**INTERNET\_OPTION\_CODEPAGE\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-158">100</span><span class="sxs-lookup"><span data-stu-id="38db0-158">100</span></span>
</dt> <dt>



<span data-ttu-id="38db0-159">Por padrão, a parte do caminho da URL é codificada em UTF8.</span><span class="sxs-lookup"><span data-stu-id="38db0-159">By default, the path portion of the URL is UTF8 encoded.</span></span> <span data-ttu-id="38db0-160">A API do WinINet executa o caractere de escape (%) codificação nos caracteres de bit alto.</span><span class="sxs-lookup"><span data-stu-id="38db0-160">The WinINet API performs escape character (%) encoding on the high-bit characters.</span></span> <span data-ttu-id="38db0-161">Definir essa opção na solicitação, ou identificador de conexão, desabilita a codificação UTF8 e define uma página de código específica.</span><span class="sxs-lookup"><span data-stu-id="38db0-161">Setting this option on the request, or connection handle, disables the UTF8 encoding and sets a specific code page.</span></span> <span data-ttu-id="38db0-162">O parâmetro *lpBuffer* na chamada a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contém a página de código DBCS desejada para o caminho.</span><span class="sxs-lookup"><span data-stu-id="38db0-162">The *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contains the desired DBCS codepage for the path.</span></span> <span data-ttu-id="38db0-163">Se nenhuma página de código for especificada em *lpBuffer*, o WinInet usará o CP \_ UTF8 padrão.</span><span class="sxs-lookup"><span data-stu-id="38db0-163">If no code page is specified in *lpBuffer*, WinINet uses the default CP\_UTF8.</span></span>

<span data-ttu-id="38db0-164">**Windows XP com SP2 e Windows Server 2003 com SP1:** Não há suporte para esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="38db0-164">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="38db0-165">**Versão:** Requer o Internet Explorer 7,0.</span><span class="sxs-lookup"><span data-stu-id="38db0-165">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-166"><span id="INTERNET_OPTION_CODEPAGE_EXTRA"></span><span id="internet_option_codepage_extra"></span>**opção de página de código de INTERNET \_ \_ \_ extra**</span><span class="sxs-lookup"><span data-stu-id="38db0-166"><span id="INTERNET_OPTION_CODEPAGE_EXTRA"></span><span id="internet_option_codepage_extra"></span>**INTERNET\_OPTION\_CODEPAGE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-167">101</span><span class="sxs-lookup"><span data-stu-id="38db0-167">101</span></span>
</dt> <dt>



<span data-ttu-id="38db0-168">Por padrão, a parte do caminho da URL é a página de código padrão do sistema (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="38db0-168">By default, the path portion of the URL is the default system code page (CP\_ACP).</span></span> <span data-ttu-id="38db0-169">O caractere de escape (%) as conversões não são executadas na parte extra.</span><span class="sxs-lookup"><span data-stu-id="38db0-169">The escape character (%) conversions are not performed on the extra portion.</span></span> <span data-ttu-id="38db0-170">Definir essa opção na solicitação ou o identificador de conexão desabilita a codificação de configuração de instalação CP \_ .</span><span class="sxs-lookup"><span data-stu-id="38db0-170">Setting this option on the request, or connection handle disables the CP\_ACP encoding.</span></span> <span data-ttu-id="38db0-171">O parâmetro *lpBuffer* na chamada a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contém a página de código DBCS desejada para a parte extra da URL.</span><span class="sxs-lookup"><span data-stu-id="38db0-171">The *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contains the desired DBCS codepage for the extra portion of the URL.</span></span> <span data-ttu-id="38db0-172">Se nenhuma página de código for especificada em *lpBuffer*, o WinInet usará a página de código do sistema padrão (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="38db0-172">If no code page is specified in *lpBuffer*, WinINet uses the default system code page (CP\_ACP).</span></span>

<span data-ttu-id="38db0-173">**Windows XP com SP2 e Windows Server 2003 com SP1:** Não há suporte para esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="38db0-173">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="38db0-174">**Versão:** Requer o Internet Explorer 7,0.</span><span class="sxs-lookup"><span data-stu-id="38db0-174">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-175"><span id="INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH_"></span><span id="internet_option_compressed_content_length_"></span>**\_tamanho de \_ conteúdo compactado da opção \_ da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-175"><span id="INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH_"></span><span id="internet_option_compressed_content_length_"></span>**INTERNET\_OPTION\_COMPRESSED\_CONTENT\_LENGTH**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-176">147</span><span class="sxs-lookup"><span data-stu-id="38db0-176">147</span></span>
</dt> <dt>



<span data-ttu-id="38db0-177">Para uma solicitação em que o WinInet descompactou a codificação de conteúdo fornecida pelo servidor, o recupera o tamanho de conteúdo relatado pelo servidor do corpo da resposta como um ULONGLONG.</span><span class="sxs-lookup"><span data-stu-id="38db0-177">For a request where WinInet decompressed the server s supplied Content-Encoding, retrieves the server-reported Content-Length of the response body as a ULONGLONG.</span></span> <span data-ttu-id="38db0-178">Com suporte no Windows 10, versão 1507 e posterior.</span><span class="sxs-lookup"><span data-stu-id="38db0-178">Supported in Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-179"><span id="INTERNET_OPTION_CONNECT_BACKOFF"></span><span id="internet_option_connect_backoff"></span>**\_retirada da opção de \_ conexão com a Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-179"><span id="INTERNET_OPTION_CONNECT_BACKOFF"></span><span id="internet_option_connect_backoff"></span>**INTERNET\_OPTION\_CONNECT\_BACKOFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-180">4</span><span class="sxs-lookup"><span data-stu-id="38db0-180">4</span></span>
</dt> <dt>



<span data-ttu-id="38db0-181">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="38db0-181">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-182"><span id="INTERNET_OPTION_CONNECT_RETRIES"></span><span id="internet_option_connect_retries"></span>**\_ \_ novas tentativas de conexão de opção de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-182"><span id="INTERNET_OPTION_CONNECT_RETRIES"></span><span id="internet_option_connect_retries"></span>**INTERNET\_OPTION\_CONNECT\_RETRIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-183">3</span><span class="sxs-lookup"><span data-stu-id="38db0-183">3</span></span>
</dt> <dt>



<span data-ttu-id="38db0-184">Define ou recupera um valor inteiro longo sem sinal que contém o número de vezes que o WinINet tenta resolver e se conectar a um host.</span><span class="sxs-lookup"><span data-stu-id="38db0-184">Sets or retrieves an unsigned long integer value that contains the number of times WinINet attempts to resolve and connect to a host.</span></span> <span data-ttu-id="38db0-185">Ele só tenta uma vez por endereço IP.</span><span class="sxs-lookup"><span data-stu-id="38db0-185">It only attempts once per IP address.</span></span> <span data-ttu-id="38db0-186">Por exemplo, se você tentar se conectar a um host de hospedagem múltipla que tem dez endereços IP e \_ as \_ novas tentativas de conexão de opção \_ de Internet estiverem definidas como sete, o WinInet só tentará resolver e se conectar aos primeiros sete endereços IP.</span><span class="sxs-lookup"><span data-stu-id="38db0-186">For example, if you attempt to connect to a multihome host that has ten IP addresses and INTERNET\_OPTION\_CONNECT\_RETRIES is set to seven, WinINet only attempts to resolve and connect to the first seven IP addresses.</span></span> <span data-ttu-id="38db0-187">Por outro lado, considerando o mesmo conjunto de dez endereços IP, se a \_ opção da Internet \_ \_ tentar repetições for definida como 20, o WinInet tentará cada uma das dez apenas uma vez.</span><span class="sxs-lookup"><span data-stu-id="38db0-187">Conversely, given the same set of ten IP addresses, if INTERNET\_OPTION\_CONNECT\_RETRIES is set to 20, WinINet attempts each of the ten only once.</span></span> <span data-ttu-id="38db0-188">Se um host tiver apenas um endereço IP e a primeira tentativa de conexão falhar, não haverá mais nenhuma tentativa.</span><span class="sxs-lookup"><span data-stu-id="38db0-188">If a host has only one IP address and the first connection attempt fails, there are no further attempts.</span></span> <span data-ttu-id="38db0-189">Se uma tentativa de conexão ainda falhar após o número especificado de tentativas, a solicitação será cancelada.</span><span class="sxs-lookup"><span data-stu-id="38db0-189">If a connection attempt still fails after the specified number of attempts, the request is canceled.</span></span> <span data-ttu-id="38db0-190">O valor padrão para as \_ repetições de conexão de opção de Internet \_ \_ é de cinco tentativas.</span><span class="sxs-lookup"><span data-stu-id="38db0-190">The default value for INTERNET\_OPTION\_CONNECT\_RETRIES is five attempts.</span></span> <span data-ttu-id="38db0-191">Essa opção pode ser usada em qualquer identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) , incluindo um identificador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="38db0-191">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="38db0-192">Ele é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-192">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-193"><span id="INTERNET_OPTION_CONNECT_TIME"></span><span id="internet_option_connect_time"></span>**\_tempo de \_ conexão da opção de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-193"><span id="INTERNET_OPTION_CONNECT_TIME"></span><span id="internet_option_connect_time"></span>**INTERNET\_OPTION\_CONNECT\_TIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-194">55</span><span class="sxs-lookup"><span data-stu-id="38db0-194">55</span></span>
</dt> <dt>



<span data-ttu-id="38db0-195">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="38db0-195">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-196"><span id="INTERNET_OPTION_CONNECT_TIMEOUT"></span><span id="internet_option_connect_timeout"></span>**\_ \_ tempo limite de conexão de opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-196"><span id="INTERNET_OPTION_CONNECT_TIMEOUT"></span><span id="internet_option_connect_timeout"></span>**INTERNET\_OPTION\_CONNECT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-197">2</span><span class="sxs-lookup"><span data-stu-id="38db0-197">2</span></span>
</dt> <dt>



<span data-ttu-id="38db0-198">Define ou recupera um valor inteiro longo sem sinal que contém o valor de tempo limite, em milissegundos, a ser usado para solicitações de conexão com a Internet.</span><span class="sxs-lookup"><span data-stu-id="38db0-198">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to use for Internet connection requests.</span></span> <span data-ttu-id="38db0-199">Definir essa opção como infinito (0xFFFFFFFF) desabilitará esse temporizador.</span><span class="sxs-lookup"><span data-stu-id="38db0-199">Setting this option to infinite (0xFFFFFFFF) will disable this timer.</span></span>

<span data-ttu-id="38db0-200">Se uma solicitação de conexão demorar mais do que esse valor de tempo limite, a solicitação será cancelada.</span><span class="sxs-lookup"><span data-stu-id="38db0-200">If a connection request takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="38db0-201">Ao tentar se conectar a vários endereços IP para um único host (um host multihome), o tempo limite é cumulativo para todos os endereços IP.</span><span class="sxs-lookup"><span data-stu-id="38db0-201">When attempting to connect to multiple IP addresses for a single host (a multihome host), the timeout limit is cumulative for all of the IP addresses.</span></span> <span data-ttu-id="38db0-202">Essa opção pode ser usada em qualquer identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) , incluindo um identificador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="38db0-202">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="38db0-203">Ele é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-203">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-204"><span id="INTERNET_OPTION_CONNECTED_STATE"></span><span id="internet_option_connected_state"></span>**\_ \_ estado conectado da opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-204"><span id="INTERNET_OPTION_CONNECTED_STATE"></span><span id="internet_option_connected_state"></span>**INTERNET\_OPTION\_CONNECTED\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-205">50</span><span class="sxs-lookup"><span data-stu-id="38db0-205">50</span></span>
</dt> <dt>



<span data-ttu-id="38db0-206">Define ou recupera um valor inteiro longo sem sinal que contém o estado conectado.</span><span class="sxs-lookup"><span data-stu-id="38db0-206">Sets or retrieves an unsigned long integer value that contains the connected state.</span></span> <span data-ttu-id="38db0-207">Isso é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-207">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-208"><span id="INTERNET_OPTION_CONTEXT_VALUE"></span><span id="internet_option_context_value"></span>**\_valor de \_ contexto de opção de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-208"><span id="INTERNET_OPTION_CONTEXT_VALUE"></span><span id="internet_option_context_value"></span>**INTERNET\_OPTION\_CONTEXT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-209">45</span><span class="sxs-lookup"><span data-stu-id="38db0-209">45</span></span>
</dt> <dt>



<span data-ttu-id="38db0-210">Define ou recupera um \_ PTR de DWORD que contém o endereço do valor de contexto associado a esse identificador [**HINTERNET**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="38db0-210">Sets or retrieves a DWORD\_PTR that contains the address of the context value associated with this [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span> <span data-ttu-id="38db0-211">Essa opção pode ser usada em qualquer identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="38db0-211">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span> <span data-ttu-id="38db0-212">Isso é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-212">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="38db0-213">Anteriormente, isso definiu o valor de contexto para o endereço armazenado no ponteiro **lpBuffer** .</span><span class="sxs-lookup"><span data-stu-id="38db0-213">Previously, this set the context value to the address stored in the **lpBuffer** pointer.</span></span> <span data-ttu-id="38db0-214">Isso foi corrigido para que o valor armazenado no buffer seja usado e o sinalizador de [ \_ valor do \_ contexto \_ de opção da Internet](/windows) seja atribuído a um novo valor.</span><span class="sxs-lookup"><span data-stu-id="38db0-214">This has been corrected so that the value stored in the buffer is used and the [INTERNET\_OPTION\_CONTEXT\_VALUE](/windows) flag is assigned a new value.</span></span> <span data-ttu-id="38db0-215">O valor antigo, 10, foi preservado para que os aplicativos escritos para o comportamento antigo ainda tenham suporte.</span><span class="sxs-lookup"><span data-stu-id="38db0-215">The old value, 10, has been preserved so that applications written for the old behavior are still supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-216"><span id="INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT"></span><span id="internet_option_control_receive_timeout"></span>**\_ \_ \_ tempo limite de recebimento de controle de opção de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-216"><span id="INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT"></span><span id="internet_option_control_receive_timeout"></span>**INTERNET\_OPTION\_CONTROL\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-217">6</span><span class="sxs-lookup"><span data-stu-id="38db0-217">6</span></span>
</dt> <dt>



<span data-ttu-id="38db0-218">[ \_ \_ \_ Tempo limite de recebimento de opção](/windows)idêntico ao da Internet.</span><span class="sxs-lookup"><span data-stu-id="38db0-218">Identical to [INTERNET\_OPTION\_RECEIVE\_TIMEOUT](/windows).</span></span> <span data-ttu-id="38db0-219">Isso é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-219">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-220"><span id="INTERNET_OPTION_CONTROL_SEND_TIMEOUT"></span><span id="internet_option_control_send_timeout"></span>**controle de opção da INTERNET- \_ \_ \_ \_ tempo limite de envio**</span><span class="sxs-lookup"><span data-stu-id="38db0-220"><span id="INTERNET_OPTION_CONTROL_SEND_TIMEOUT"></span><span id="internet_option_control_send_timeout"></span>**INTERNET\_OPTION\_CONTROL\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-221">5</span><span class="sxs-lookup"><span data-stu-id="38db0-221">5</span></span>
</dt> <dt>



<span data-ttu-id="38db0-222">[ \_ \_ \_ Tempo limite de envio de opção de Internet](/windows)idêntico a.</span><span class="sxs-lookup"><span data-stu-id="38db0-222">Identical to [INTERNET\_OPTION\_SEND\_TIMEOUT](/windows).</span></span> <span data-ttu-id="38db0-223">Isso é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-223">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-224"><span id="INTERNET_OPTION_DATA_RECEIVE_TIMEOUT"></span><span id="internet_option_data_receive_timeout"></span>**\_ \_ \_ tempo limite de recebimento de dados de opção de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-224"><span id="INTERNET_OPTION_DATA_RECEIVE_TIMEOUT"></span><span id="internet_option_data_receive_timeout"></span>**INTERNET\_OPTION\_DATA\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-225">8</span><span class="sxs-lookup"><span data-stu-id="38db0-225">8</span></span>
</dt> <dt>



<span data-ttu-id="38db0-226">Define ou recupera um valor inteiro longo sem sinal que contém o valor de tempo limite, em milissegundos, para receber uma resposta a uma solicitação para o canal de dados de uma transação de FTP.</span><span class="sxs-lookup"><span data-stu-id="38db0-226">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a response to a request for the data channel of an FTP transaction.</span></span> <span data-ttu-id="38db0-227">Se a resposta demorar mais do que esse valor de tempo limite, a solicitação será cancelada.</span><span class="sxs-lookup"><span data-stu-id="38db0-227">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="38db0-228">Essa opção pode ser usada em qualquer identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) , incluindo um identificador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="38db0-228">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="38db0-229">Ele é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-229">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="38db0-230">Esse sinalizador não tem impacto sobre a funcionalidade HTTP.</span><span class="sxs-lookup"><span data-stu-id="38db0-230">This flag has no impact on HTTP functionality.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-231"><span id="INTERNET_OPTION_DATA_SEND_TIMEOUT"></span><span id="internet_option_data_send_timeout"></span>**\_ \_ \_ tempo limite de envio de dados de opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-231"><span id="INTERNET_OPTION_DATA_SEND_TIMEOUT"></span><span id="internet_option_data_send_timeout"></span>**INTERNET\_OPTION\_DATA\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-232">7</span><span class="sxs-lookup"><span data-stu-id="38db0-232">7</span></span>
</dt> <dt>



<span data-ttu-id="38db0-233">Define ou recupera um valor inteiro longo sem sinal, em milissegundos, que contém o valor de tempo limite para enviar uma solicitação para o canal de dados de uma transação de FTP.</span><span class="sxs-lookup"><span data-stu-id="38db0-233">Sets or retrieves an unsigned long integer value, in milliseconds, that contains the time-out value to send a request for the data channel of an FTP transaction.</span></span> <span data-ttu-id="38db0-234">Se o envio demorar mais do que esse valor de tempo limite, o envio será cancelado.</span><span class="sxs-lookup"><span data-stu-id="38db0-234">If the send takes longer than this time-out value, the send is canceled.</span></span> <span data-ttu-id="38db0-235">Essa opção pode ser usada em qualquer identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) , incluindo um identificador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="38db0-235">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="38db0-236">Ele é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-236">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="38db0-237">Esse sinalizador não tem impacto sobre a funcionalidade HTTP.</span><span class="sxs-lookup"><span data-stu-id="38db0-237">This flag has no impact on HTTP functionality.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-238"><span id="INTERNET_OPTION_DATAFILE_NAME"></span><span id="internet_option_datafile_name"></span>**\_nome do \_ DataFile da opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-238"><span id="INTERNET_OPTION_DATAFILE_NAME"></span><span id="internet_option_datafile_name"></span>**INTERNET\_OPTION\_DATAFILE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-239">33</span><span class="sxs-lookup"><span data-stu-id="38db0-239">33</span></span>
</dt> <dt>



<span data-ttu-id="38db0-240">Recupera um valor de cadeia de caracteres que contém o nome do arquivo que faz o backup de uma entidade baixada.</span><span class="sxs-lookup"><span data-stu-id="38db0-240">Retrieves a string value that contains the name of the file backing a downloaded entity.</span></span> <span data-ttu-id="38db0-241">Esse sinalizador é válido após a conclusão de [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .</span><span class="sxs-lookup"><span data-stu-id="38db0-241">This flag is valid after [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) has completed.</span></span> <span data-ttu-id="38db0-242">Essa opção só pode ser consultada por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-242">This option can only be queried by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-243"><span id="INTERNET_OPTION_DATAFILE_EXT"></span><span id="internet_option_datafile_ext"></span>**\_extensão de \_ DataFile de opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-243"><span id="INTERNET_OPTION_DATAFILE_EXT"></span><span id="internet_option_datafile_ext"></span>**INTERNET\_OPTION\_DATAFILE\_EXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-244">96</span><span class="sxs-lookup"><span data-stu-id="38db0-244">96</span></span>
</dt> <dt>



<span data-ttu-id="38db0-245">Define um valor de cadeia de caracteres que contém a extensão do arquivo que faz o backup de uma entidade baixada.</span><span class="sxs-lookup"><span data-stu-id="38db0-245">Sets a string value that contains the extension of the file backing a downloaded entity.</span></span> <span data-ttu-id="38db0-246">Esse sinalizador deve ser definido antes de chamar [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="38db0-246">This flag should be set before calling [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="38db0-247">Essa opção só pode ser definida por [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-247">This option can only be set by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-248"><span id="INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO"></span><span id="internet_option_diagnostic_socket_info"></span>**\_informações de \_ soquete de diagnóstico de opção da Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-248"><span id="INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO"></span><span id="internet_option_diagnostic_socket_info"></span>**INTERNET\_OPTION\_DIAGNOSTIC\_SOCKET\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-249">67</span><span class="sxs-lookup"><span data-stu-id="38db0-249">67</span></span>
</dt> <dt>



<span data-ttu-id="38db0-250">Recupera uma estrutura de informações de soquete de diagnóstico da Internet que contém dados sobre uma solicitação HTTP especificada. [**\_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_diagnostic_socket_info)</span><span class="sxs-lookup"><span data-stu-id="38db0-250">Retrieves an [**INTERNET\_DIAGNOSTIC\_SOCKET\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_diagnostic_socket_info) structure that contains data about a specified HTTP Request.</span></span> <span data-ttu-id="38db0-251">Esse sinalizador é usado pelo [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-251">This flag is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

<span data-ttu-id="38db0-252">**Windows 7:** Não há mais suporte para essa opção.</span><span class="sxs-lookup"><span data-stu-id="38db0-252">**Windows 7:** This option is no longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-253"><span id="INTERNET_OPTION_DIGEST_AUTH_UNLOAD"></span><span id="internet_option_digest_auth_unload"></span>**\_descarregamento \_ de \_ autenticação \_ Digest de opção da Internet**</span><span class="sxs-lookup"><span data-stu-id="38db0-253"><span id="INTERNET_OPTION_DIGEST_AUTH_UNLOAD"></span><span id="internet_option_digest_auth_unload"></span>**INTERNET\_OPTION\_DIGEST\_AUTH\_UNLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-254">76</span><span class="sxs-lookup"><span data-stu-id="38db0-254">76</span></span>
</dt> <dt>



<span data-ttu-id="38db0-255">Faz com que o sistema faça logoff do pacote SSPI de autenticação Digest, limpando todas as credenciais criadas para o processo.</span><span class="sxs-lookup"><span data-stu-id="38db0-255">Causes the system to log off the Digest authentication SSPI package, purging all of the credentials created for the process.</span></span> <span data-ttu-id="38db0-256">Nenhum buffer é necessário para essa opção.</span><span class="sxs-lookup"><span data-stu-id="38db0-256">No buffer is required for this option.</span></span> <span data-ttu-id="38db0-257">Ele é usado por [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-257">It is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-258"><span id="INTERNET_OPTION_DISABLE_AUTODIAL"></span><span id="internet_option_disable_autodial"></span>**opção da INTERNET \_ \_ desabilitar a \_ discagem automática**</span><span class="sxs-lookup"><span data-stu-id="38db0-258"><span id="INTERNET_OPTION_DISABLE_AUTODIAL"></span><span id="internet_option_disable_autodial"></span>**INTERNET\_OPTION\_DISABLE\_AUTODIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-259">70</span><span class="sxs-lookup"><span data-stu-id="38db0-259">70</span></span>
</dt> <dt>



<span data-ttu-id="38db0-260">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="38db0-260">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-261"><span id="INTERNET_OPTION_DISCONNECTED_TIMEOUT"></span><span id="internet_option_disconnected_timeout"></span>**\_ \_ tempo limite desconectado da opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-261"><span id="INTERNET_OPTION_DISCONNECTED_TIMEOUT"></span><span id="internet_option_disconnected_timeout"></span>**INTERNET\_OPTION\_DISCONNECTED\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-262">49</span><span class="sxs-lookup"><span data-stu-id="38db0-262">49</span></span>
</dt> <dt>



<span data-ttu-id="38db0-263">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="38db0-263">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-264"><span id="INTERNET_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="internet_option_enable_http_protocol"></span>**opção de INTERNET \_ \_ habilitar \_ \_ protocolo http**</span><span class="sxs-lookup"><span data-stu-id="38db0-264"><span id="INTERNET_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="internet_option_enable_http_protocol"></span>**INTERNET\_OPTION\_ENABLE\_HTTP\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-265">148</span><span class="sxs-lookup"><span data-stu-id="38db0-265">148</span></span>
</dt> <dt>



<span data-ttu-id="38db0-266">Define um bitmask DWORD de versões HTTP avançadas aceitáveis.</span><span class="sxs-lookup"><span data-stu-id="38db0-266">Sets a DWORD bitmask of acceptable advanced HTTP versions.</span></span> <span data-ttu-id="38db0-267">Pode ser definido em qualquer tipo de identificador.</span><span class="sxs-lookup"><span data-stu-id="38db0-267">May be set on any handle type.</span></span> <span data-ttu-id="38db0-268">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="38db0-268">Possible values are:</span></span>

-   <span data-ttu-id="38db0-269">\_ \_ Sinalizador de protocolo http \_ HTTP2 (0x2).</span><span class="sxs-lookup"><span data-stu-id="38db0-269">HTTP\_PROTOCOL\_FLAG\_HTTP2 (0x2).</span></span> <span data-ttu-id="38db0-270">Com suporte no Windows 10, versão 1507 e posterior.</span><span class="sxs-lookup"><span data-stu-id="38db0-270">Supported on Windows 10, version 1507 and later.</span></span>

<span data-ttu-id="38db0-271">As versões herdadas do HTTP (1,1 e anteriores) não podem ser desabilitadas usando essa opção.</span><span class="sxs-lookup"><span data-stu-id="38db0-271">Legacy versions of HTTP (1.1 and prior) cannot be disabled using this option.</span></span> <span data-ttu-id="38db0-272">O padrão é 0x0.</span><span class="sxs-lookup"><span data-stu-id="38db0-272">The default is 0x0.</span></span> <span data-ttu-id="38db0-273">Com suporte no Windows 10, versão 1507 e posterior.</span><span class="sxs-lookup"><span data-stu-id="38db0-273">Supported in Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-274"><span id="INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ"></span><span id="internet_option_enable_redirect_cache_read"></span>**opção da INTERNET \_ \_ habilitar \_ leitura do cache de redirecionamento \_ \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-274"><span id="INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ"></span><span id="internet_option_enable_redirect_cache_read"></span>**INTERNET\_OPTION\_ENABLE\_REDIRECT\_CACHE\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-275">122</span><span class="sxs-lookup"><span data-stu-id="38db0-275">122</span></span>
</dt> <dt>



<span data-ttu-id="38db0-276">Em um identificador de solicitação, o define um booliano controlando se os redirecionamentos serão retornados do cache do WinInet para uma determinada solicitação.</span><span class="sxs-lookup"><span data-stu-id="38db0-276">On a request handle, sets a Boolean controlling whether redirects will be returned from the WinInet cache for a given request.</span></span> <span data-ttu-id="38db0-277">O padrão é FALSE.</span><span class="sxs-lookup"><span data-stu-id="38db0-277">The default is FALSE.</span></span> <span data-ttu-id="38db0-278">Com suporte no Windows 8 e posterior.</span><span class="sxs-lookup"><span data-stu-id="38db0-278">Supported in Windows 8 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-279"><span id="INTERNET_OPTION_ENCODE_EXTRA"></span><span id="internet_option_encode_extra"></span>**codificação de opção de INTERNET \_ \_ \_ extra**</span><span class="sxs-lookup"><span data-stu-id="38db0-279"><span id="INTERNET_OPTION_ENCODE_EXTRA"></span><span id="internet_option_encode_extra"></span>**INTERNET\_OPTION\_ENCODE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-280">155</span><span class="sxs-lookup"><span data-stu-id="38db0-280">155</span></span>
</dt> <dt>



<span data-ttu-id="38db0-281">Obtém/define um BOOL que indica se caracteres não ASCII na cadeia de caracteres de consulta devem ser codificados por percentual.</span><span class="sxs-lookup"><span data-stu-id="38db0-281">Gets/sets a BOOL indicating whether non-ASCII characters in the query string should be percent-encoded.</span></span> <span data-ttu-id="38db0-282">O padrão é FALSE.</span><span class="sxs-lookup"><span data-stu-id="38db0-282">The default is FALSE.</span></span> <span data-ttu-id="38db0-283">Com suporte no Windows 8.1 e posterior.</span><span class="sxs-lookup"><span data-stu-id="38db0-283">Supported in Windows 8.1 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-284"><span id="INTERNET_OPTION_END_BROWSER_SESSION"></span><span id="internet_option_end_browser_session"></span>**INTERNET \_ Option \_ end \_ browser \_ Session**</span><span class="sxs-lookup"><span data-stu-id="38db0-284"><span id="INTERNET_OPTION_END_BROWSER_SESSION"></span><span id="internet_option_end_browser_session"></span>**INTERNET\_OPTION\_END\_BROWSER\_SESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-285">42</span><span class="sxs-lookup"><span data-stu-id="38db0-285">42</span></span>
</dt> <dt>



<span data-ttu-id="38db0-286">Libera entradas que não estão em uso do cache de senha na unidade de disco rígido.</span><span class="sxs-lookup"><span data-stu-id="38db0-286">Flushes entries not in use from the password cache on the hard disk drive.</span></span> <span data-ttu-id="38db0-287">Também redefine o tempo de cache usado quando o modo de sincronização é de uma vez por sessão.</span><span class="sxs-lookup"><span data-stu-id="38db0-287">Also resets the cache time used when the synchronization mode is once-per-session.</span></span> <span data-ttu-id="38db0-288">Nenhum buffer é necessário para essa opção.</span><span class="sxs-lookup"><span data-stu-id="38db0-288">No buffer is required for this option.</span></span> <span data-ttu-id="38db0-289">Isso é usado por [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-289">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-290"><span id="INTERNET_OPTION_ERROR_MASK"></span><span id="internet_option_error_mask"></span>**\_máscara de \_ erro de opção de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-290"><span id="INTERNET_OPTION_ERROR_MASK"></span><span id="internet_option_error_mask"></span>**INTERNET\_OPTION\_ERROR\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-291">62</span><span class="sxs-lookup"><span data-stu-id="38db0-291">62</span></span>
</dt> <dt>



<span data-ttu-id="38db0-292">Define um valor inteiro longo sem sinal que contém as máscaras de erro que podem ser manipuladas pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="38db0-292">Sets an unsigned long integer value that contains the error masks that can be handled by the client application.</span></span> <span data-ttu-id="38db0-293">Isso pode ser uma combinação dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="38db0-293">This can be a combination of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="38db0-294"><span id="INTERNET_ERROR_MASK_COMBINED_SEC_CERT"></span><span id="internet_error_mask_combined_sec_cert"></span>máscara de erro da INTERNET com \_ \_ \_ certificado de \_ s combinado \_</span><span class="sxs-lookup"><span data-stu-id="38db0-294"><span id="INTERNET_ERROR_MASK_COMBINED_SEC_CERT"></span><span id="internet_error_mask_combined_sec_cert"></span>INTERNET\_ERROR\_MASK\_COMBINED\_SEC\_CERT</span></span>
</dt> <dd>

<span data-ttu-id="38db0-295">0x2</span><span class="sxs-lookup"><span data-stu-id="38db0-295">0x2</span></span>

<span data-ttu-id="38db0-296">Indica que todos os erros de certificado devem ser relatados usando o mesmo retorno de erro, ou seja, **\_ erros de certificado de Internet \_ SEC \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="38db0-296">Indicates that all certificate errors are to be reported using the same error return, namely **ERROR\_INTERNET\_SEC\_CERT\_ERRORS**.</span></span> <span data-ttu-id="38db0-297">Se esse sinalizador for definido, chame **InternetErrorDlg** ao receber o erro erro de **\_ erros de certificado da Internet \_ SEC \_ \_** , para que o usuário possa responder a uma caixa de diálogo familiar que descreve o problema.</span><span class="sxs-lookup"><span data-stu-id="38db0-297">If this flag is set, call **InternetErrorDlg** upon receiving the **ERROR\_INTERNET\_SEC\_CERT\_ERRORS** error, so that the user can respond to a familiar dialog describing the problem.</span></span>

> [!Caution]  
> <span data-ttu-id="38db0-298">Falha ao informar o usuário desse erro expõe o usuário a possíveis ataques de falsificação.</span><span class="sxs-lookup"><span data-stu-id="38db0-298">Failing to inform the user of this error exposes the user to potential spoofing attacks.</span></span>

 

</dd> <dt>

<span data-ttu-id="38db0-299"><span id="INTERNET_ERROR_MASK_INSERT_CDROM"></span><span id="internet_error_mask_insert_cdrom"></span>máscara de erro de INTERNET \_ \_ \_ Inserir \_ cdrom</span><span class="sxs-lookup"><span data-stu-id="38db0-299"><span id="INTERNET_ERROR_MASK_INSERT_CDROM"></span><span id="internet_error_mask_insert_cdrom"></span>INTERNET\_ERROR\_MASK\_INSERT\_CDROM</span></span>
</dt> <dd>

<span data-ttu-id="38db0-300">0x1</span><span class="sxs-lookup"><span data-stu-id="38db0-300">0x1</span></span>

<span data-ttu-id="38db0-301">Indica que o aplicativo cliente pode manipular o código de erro de **\_ inserção de \_ \_ cdrom da Internet de erro** .</span><span class="sxs-lookup"><span data-stu-id="38db0-301">Indicates that the client application can handle the **ERROR\_INTERNET\_INSERT\_CDROM** error code.</span></span>

</dd> <dt>

<span data-ttu-id="38db0-302"><span id="INTERNET_ERROR_MASK_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="internet_error_mask_login_failure_display_entity_body"></span>\_falha de \_ logon na máscara de erro de conexão da Internet do \_ corpo da \_ \_ \_ entidade \_</span><span class="sxs-lookup"><span data-stu-id="38db0-302"><span id="INTERNET_ERROR_MASK_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="internet_error_mask_login_failure_display_entity_body"></span>INTERNET\_ERROR\_MASK\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY</span></span>
</dt> <dd>

<span data-ttu-id="38db0-303">0x8</span><span class="sxs-lookup"><span data-stu-id="38db0-303">0x8</span></span>

<span data-ttu-id="38db0-304">Indica que o aplicativo cliente pode manipular o **erro \_ de \_ logon \_ na Internet falha ao \_ Exibir \_ \_** o código de erro do corpo da entidade.</span><span class="sxs-lookup"><span data-stu-id="38db0-304">Indicates that the client application can handle the **ERROR\_INTERNET\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY** error code.</span></span>

</dd> <dt>

<span data-ttu-id="38db0-305"><span id="INTERNET_ERROR_MASK_NEED_MSN_SSPI_PKG"></span><span id="internet_error_mask_need_msn_sspi_pkg"></span>a \_ máscara de erro da Internet \_ precisa do \_ \_ \_ pacote SSPI do MSN \_</span><span class="sxs-lookup"><span data-stu-id="38db0-305"><span id="INTERNET_ERROR_MASK_NEED_MSN_SSPI_PKG"></span><span id="internet_error_mask_need_msn_sspi_pkg"></span>INTERNET\_ERROR\_MASK\_NEED\_MSN\_SSPI\_PKG</span></span>
</dt> <dd>

<span data-ttu-id="38db0-306">0x4</span><span class="sxs-lookup"><span data-stu-id="38db0-306">0x4</span></span>

<span data-ttu-id="38db0-307">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="38db0-307">Not implemented.</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="38db0-308"><span id="INTERNET_OPTION_ENTERPRISE_CONTEXT"></span><span id="internet_option_enterprise_context"></span>**\_ \_ contexto empresarial da opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-308"><span id="INTERNET_OPTION_ENTERPRISE_CONTEXT"></span><span id="internet_option_enterprise_context"></span>**INTERNET\_OPTION\_ENTERPRISE\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-309">159</span><span class="sxs-lookup"><span data-stu-id="38db0-309">159</span></span>
</dt> <dt>



<span data-ttu-id="38db0-310">Define um PWSTR que contém a ID da empresa (consulte o https://msdn.microsoft.com/library/windows/desktop/mt759320(v=vs.85).aspx) que se aplica à solicitação.</span><span class="sxs-lookup"><span data-stu-id="38db0-310">Sets a PWSTR containing the Enterprise ID (see https://msdn.microsoft.com/library/windows/desktop/mt759320(v=vs.85).aspx) which applies to the request.</span></span> <span data-ttu-id="38db0-311">Com suporte no Windows 10, versão 1507 e posterior.</span><span class="sxs-lookup"><span data-stu-id="38db0-311">Supported in Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-312"><span id="INTERNET_OPTION_EXTENDED_ERROR"></span><span id="internet_option_extended_error"></span>**\_ \_ erro estendido de opção de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-312"><span id="INTERNET_OPTION_EXTENDED_ERROR"></span><span id="internet_option_extended_error"></span>**INTERNET\_OPTION\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-313">24</span><span class="sxs-lookup"><span data-stu-id="38db0-313">24</span></span>
</dt> <dt>



<span data-ttu-id="38db0-314">Recupera um valor inteiro longo sem sinal que contém um código de erro do Winsock mapeado para o erro mensagens de erro de **\_ Internet \_** retornado pela última vez neste contexto de thread.</span><span class="sxs-lookup"><span data-stu-id="38db0-314">Retrieves an unsigned long integer value that contains a Winsock error code mapped to the **ERROR\_INTERNET\_** error messages last returned in this thread context.</span></span> <span data-ttu-id="38db0-315">Essa opção é usada em um identificador [**HINTERNET**](appendix-a-hinternet-handles.md) **nulo** por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-315">This option is used on a **NULL**[**HINTERNET**](appendix-a-hinternet-handles.md) handle by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-316"><span id="INTERNET_OPTION_FROM_CACHE_TIMEOUT"></span><span id="internet_option_from_cache_timeout"></span>**\_opção \_ da Internet \_ do \_ tempo limite do cache**</span><span class="sxs-lookup"><span data-stu-id="38db0-316"><span id="INTERNET_OPTION_FROM_CACHE_TIMEOUT"></span><span id="internet_option_from_cache_timeout"></span>**INTERNET\_OPTION\_FROM\_CACHE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-317">63</span><span class="sxs-lookup"><span data-stu-id="38db0-317">63</span></span>
</dt> <dt>



<span data-ttu-id="38db0-318">Define ou recupera o valor inteiro longo sem sinal A1n que contém a quantidade de tempo que o sistema deve aguardar por uma resposta a uma solicitação de rede antes de verificar o cache em busca de uma cópia do recurso.</span><span class="sxs-lookup"><span data-stu-id="38db0-318">Sets or retrieves a1n unsigned long integer value that contains the amount of time the system should wait for a response to a network request before checking the cache for a copy of the resource.</span></span> <span data-ttu-id="38db0-319">Se uma solicitação de rede demorar mais do que o tempo especificado e o recurso solicitado estiver disponível no cache, o recurso será recuperado do cache.</span><span class="sxs-lookup"><span data-stu-id="38db0-319">If a network request takes longer than the time specified and the requested resource is available in the cache, the resource is retrieved from the cache.</span></span> <span data-ttu-id="38db0-320">Isso é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-320">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-321"><span id="INTERNET_OPTION_HANDLE_TYPE"></span><span id="internet_option_handle_type"></span>**\_tipo de \_ identificador de opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-321"><span id="INTERNET_OPTION_HANDLE_TYPE"></span><span id="internet_option_handle_type"></span>**INTERNET\_OPTION\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-322">9</span><span class="sxs-lookup"><span data-stu-id="38db0-322">9</span></span>
</dt> <dt>



<span data-ttu-id="38db0-323">Recupera um valor inteiro longo sem sinal que contém o tipo dos identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) passados.</span><span class="sxs-lookup"><span data-stu-id="38db0-323">Retrieves an unsigned long integer value that contains the type of the [**HINTERNET**](appendix-a-hinternet-handles.md) handles passed in.</span></span> <span data-ttu-id="38db0-324">Isso é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) em qualquer identificador de [HINTERNET](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="38db0-324">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) on any [HINTERNET](appendix-a-hinternet-handles.md) handle.</span></span> <span data-ttu-id="38db0-325">Os valores de retorno possíveis incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="38db0-325">Possible return values include the following.</span></span>

<dl> <dt>

<span data-ttu-id="38db0-326"><span id="INTERNET_HANDLE_TYPE_CONNECT_FTP"></span><span id="internet_handle_type_connect_ftp"></span>tipo de identificador da INTERNET \_ \_ \_ conectar \_ FTP</span><span class="sxs-lookup"><span data-stu-id="38db0-326"><span id="INTERNET_HANDLE_TYPE_CONNECT_FTP"></span><span id="internet_handle_type_connect_ftp"></span>INTERNET\_HANDLE\_TYPE\_CONNECT\_FTP</span></span>
</dt> <dd>

<span data-ttu-id="38db0-327">2</span><span class="sxs-lookup"><span data-stu-id="38db0-327">2</span></span>

</dd> <dt>

<span data-ttu-id="38db0-328"><span id="INTERNET_HANDLE_TYPE_CONNECT_GOPHER"></span><span id="internet_handle_type_connect_gopher"></span>tipo de identificador da INTERNET \_ \_ \_ conectar \_ Gopher</span><span class="sxs-lookup"><span data-stu-id="38db0-328"><span id="INTERNET_HANDLE_TYPE_CONNECT_GOPHER"></span><span id="internet_handle_type_connect_gopher"></span>INTERNET\_HANDLE\_TYPE\_CONNECT\_GOPHER</span></span>
</dt> <dd>

<span data-ttu-id="38db0-329">3</span><span class="sxs-lookup"><span data-stu-id="38db0-329">3</span></span>

</dd> <dt>

<span data-ttu-id="38db0-330"><span id="INTERNET_HANDLE_TYPE_CONNECT_HTTP"></span><span id="internet_handle_type_connect_http"></span>identificador de INTERNET do \_ \_ tipo \_ conectar \_ http</span><span class="sxs-lookup"><span data-stu-id="38db0-330"><span id="INTERNET_HANDLE_TYPE_CONNECT_HTTP"></span><span id="internet_handle_type_connect_http"></span>INTERNET\_HANDLE\_TYPE\_CONNECT\_HTTP</span></span>
</dt> <dd>

<span data-ttu-id="38db0-331">4</span><span class="sxs-lookup"><span data-stu-id="38db0-331">4</span></span>

</dd> <dt>

<span data-ttu-id="38db0-332"><span id="INTERNET_HANDLE_TYPE_FILE_REQUEST"></span><span id="internet_handle_type_file_request"></span>\_solicitação de \_ arquivo de tipo de identificador da Internet \_ \_</span><span class="sxs-lookup"><span data-stu-id="38db0-332"><span id="INTERNET_HANDLE_TYPE_FILE_REQUEST"></span><span id="internet_handle_type_file_request"></span>INTERNET\_HANDLE\_TYPE\_FILE\_REQUEST</span></span>
</dt> <dd>

<span data-ttu-id="38db0-333">14</span><span class="sxs-lookup"><span data-stu-id="38db0-333">14</span></span>

</dd> <dt>

<span data-ttu-id="38db0-334"><span id="INTERNET_HANDLE_TYPE_FTP_FILE"></span><span id="internet_handle_type_ftp_file"></span>tipo de identificador da INTERNET \_ \_ \_ \_ arquivo FTP</span><span class="sxs-lookup"><span data-stu-id="38db0-334"><span id="INTERNET_HANDLE_TYPE_FTP_FILE"></span><span id="internet_handle_type_ftp_file"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="38db0-335">7</span><span class="sxs-lookup"><span data-stu-id="38db0-335">7</span></span>

</dd> <dt>

<span data-ttu-id="38db0-336"><span id="INTERNET_HANDLE_TYPE_FTP_FILE_HTML"></span><span id="internet_handle_type_ftp_file_html"></span>tipo de identificador da INTERNET \_ \_ \_ HTML de \_ arquivo FTP \_</span><span class="sxs-lookup"><span data-stu-id="38db0-336"><span id="INTERNET_HANDLE_TYPE_FTP_FILE_HTML"></span><span id="internet_handle_type_ftp_file_html"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FILE\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="38db0-337">8</span><span class="sxs-lookup"><span data-stu-id="38db0-337">8</span></span>

</dd> <dt>

<span data-ttu-id="38db0-338"><span id="INTERNET_HANDLE_TYPE_FTP_FIND"></span><span id="internet_handle_type_ftp_find"></span>tipo de identificador de INTERNET \_ \_ \_ FTP \_ Localizar</span><span class="sxs-lookup"><span data-stu-id="38db0-338"><span id="INTERNET_HANDLE_TYPE_FTP_FIND"></span><span id="internet_handle_type_ftp_find"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FIND</span></span>
</dt> <dd>

<span data-ttu-id="38db0-339">5</span><span class="sxs-lookup"><span data-stu-id="38db0-339">5</span></span>

</dd> <dt>

<span data-ttu-id="38db0-340"><span id="INTERNET_HANDLE_TYPE_FTP_FIND_HTML"></span><span id="internet_handle_type_ftp_find_html"></span>INTERNET \_ Handle \_ tipo \_ FTP \_ localizar \_ HTML</span><span class="sxs-lookup"><span data-stu-id="38db0-340"><span id="INTERNET_HANDLE_TYPE_FTP_FIND_HTML"></span><span id="internet_handle_type_ftp_find_html"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FIND\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="38db0-341">6</span><span class="sxs-lookup"><span data-stu-id="38db0-341">6</span></span>

</dd> <dt>

<span data-ttu-id="38db0-342"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE"></span><span id="internet_handle_type_gopher_file"></span>\_ \_ arquivo gopher do tipo de identificador da \_ Internet \_</span><span class="sxs-lookup"><span data-stu-id="38db0-342"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE"></span><span id="internet_handle_type_gopher_file"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="38db0-343">11</span><span class="sxs-lookup"><span data-stu-id="38db0-343">11</span></span>

</dd> <dt>

<span data-ttu-id="38db0-344"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML"></span><span id="internet_handle_type_gopher_file_html"></span>tipo de identificador da INTERNET \_ \_ \_ HTML do \_ arquivo gopher \_</span><span class="sxs-lookup"><span data-stu-id="38db0-344"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML"></span><span id="internet_handle_type_gopher_file_html"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FILE\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="38db0-345">12</span><span class="sxs-lookup"><span data-stu-id="38db0-345">12</span></span>

</dd> <dt>

<span data-ttu-id="38db0-346"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND"></span><span id="internet_handle_type_gopher_find"></span>tipo de identificador da INTERNET do \_ \_ \_ Gopher \_ Localizar</span><span class="sxs-lookup"><span data-stu-id="38db0-346"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND"></span><span id="internet_handle_type_gopher_find"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FIND</span></span>
</dt> <dd>

<span data-ttu-id="38db0-347">9</span><span class="sxs-lookup"><span data-stu-id="38db0-347">9</span></span>

</dd> <dt>

<span data-ttu-id="38db0-348"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML"></span><span id="internet_handle_type_gopher_find_html"></span>tipo de identificador da INTERNET \_ \_ \_ Gopher \_ localizar \_ HTML</span><span class="sxs-lookup"><span data-stu-id="38db0-348"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML"></span><span id="internet_handle_type_gopher_find_html"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FIND\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="38db0-349">10</span><span class="sxs-lookup"><span data-stu-id="38db0-349">10</span></span>

</dd> <dt>

<span data-ttu-id="38db0-350"><span id="INTERNET_HANDLE_TYPE_HTTP_REQUEST"></span><span id="internet_handle_type_http_request"></span>\_ \_ solicitação HTTP de tipo de identificador de \_ Internet \_</span><span class="sxs-lookup"><span data-stu-id="38db0-350"><span id="INTERNET_HANDLE_TYPE_HTTP_REQUEST"></span><span id="internet_handle_type_http_request"></span>INTERNET\_HANDLE\_TYPE\_HTTP\_REQUEST</span></span>
</dt> <dd>

<span data-ttu-id="38db0-351">13</span><span class="sxs-lookup"><span data-stu-id="38db0-351">13</span></span>

</dd> <dt>

<span data-ttu-id="38db0-352"><span id="INTERNET_HANDLE_TYPE_INTERNET"></span><span id="internet_handle_type_internet"></span>Internet \_ Handle \_ tipo \_ Internet</span><span class="sxs-lookup"><span data-stu-id="38db0-352"><span id="INTERNET_HANDLE_TYPE_INTERNET"></span><span id="internet_handle_type_internet"></span>INTERNET\_HANDLE\_TYPE\_INTERNET</span></span>
</dt> <dd>

<span data-ttu-id="38db0-353">1</span><span class="sxs-lookup"><span data-stu-id="38db0-353">1</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="38db0-354"><span id="INTERNET_OPTION_HSTS"></span><span id="internet_option_hsts"></span>**opção da INTERNET \_ \_ HSTS**</span><span class="sxs-lookup"><span data-stu-id="38db0-354"><span id="INTERNET_OPTION_HSTS"></span><span id="internet_option_hsts"></span>**INTERNET\_OPTION\_HSTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-355">157</span><span class="sxs-lookup"><span data-stu-id="38db0-355">157</span></span>
</dt> <dt>



<span data-ttu-id="38db0-356">Obtém/define um BOOL que indica se o WinInet deve seguir as diretivas de segurança de transporte HSTS (HTTP estrito) dos servidores.</span><span class="sxs-lookup"><span data-stu-id="38db0-356">Gets/sets a BOOL indicating whether WinInet should follow HTTP Strict Transport Security (HSTS) directives from servers.</span></span> <span data-ttu-id="38db0-357">Se habilitada, as solicitações de esquema https://para domínios que têm uma política HSTS armazenada em cache pelo WinInet serão redirecionadas para URLs https://correspondentes.</span><span class="sxs-lookup"><span data-stu-id="38db0-357">If enabled, https:// schemed requests to domains which have an HSTS policy cached by WinInet will be redirected to matching https:// URLs.</span></span> <span data-ttu-id="38db0-358">O padrão é FALSE.</span><span class="sxs-lookup"><span data-stu-id="38db0-358">The default is FALSE.</span></span> <span data-ttu-id="38db0-359">Com suporte no Windows 8.1 e posterior.</span><span class="sxs-lookup"><span data-stu-id="38db0-359">Supported in Windows 8.1 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-360"><span id="INTERNET_OPTION_HTTP_DECODING"></span><span id="internet_option_http_decoding"></span>**\_decodificação http de opção da Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-360"><span id="INTERNET_OPTION_HTTP_DECODING"></span><span id="internet_option_http_decoding"></span>**INTERNET\_OPTION\_HTTP\_DECODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-361">65</span><span class="sxs-lookup"><span data-stu-id="38db0-361">65</span></span>
</dt> <dt>



<span data-ttu-id="38db0-362">Permite que o WinINet execute a decodificação para os esquemas de codificação gzip e deflate.</span><span class="sxs-lookup"><span data-stu-id="38db0-362">Enables WinINet to perform decoding for the gzip and deflate encoding schemes.</span></span> <span data-ttu-id="38db0-363">Para obter mais informações, consulte [**codificação de conteúdo**](content-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="38db0-363">For more information, see [**Content Encoding**](content-encoding.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-364"><span id="INTERNET_OPTION_HTTP_PROTOCOL_USED"></span><span id="internet_option_http_protocol_used"></span>**\_protocolo http de opção de Internet \_ \_ \_ usado**</span><span class="sxs-lookup"><span data-stu-id="38db0-364"><span id="INTERNET_OPTION_HTTP_PROTOCOL_USED"></span><span id="internet_option_http_protocol_used"></span>**INTERNET\_OPTION\_HTTP\_PROTOCOL\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-365">149</span><span class="sxs-lookup"><span data-stu-id="38db0-365">149</span></span>
</dt> <dt>



<span data-ttu-id="38db0-366">Obtém um DWORD que indica qual versão HTTP avançada foi usada em uma determinada solicitação.</span><span class="sxs-lookup"><span data-stu-id="38db0-366">Gets a DWORD indicating which advanced HTTP version was used on a given request.</span></span> <span data-ttu-id="38db0-367">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="38db0-367">Possible values are:</span></span>

-   <span data-ttu-id="38db0-368">\_ \_ Sinalizador de protocolo http \_ HTTP2 (0x2).</span><span class="sxs-lookup"><span data-stu-id="38db0-368">HTTP\_PROTOCOL\_FLAG\_HTTP2 (0x2).</span></span> <span data-ttu-id="38db0-369">Com suporte no Windows 10, versão 1507 e posterior.</span><span class="sxs-lookup"><span data-stu-id="38db0-369">Supported on Windows 10, version 1507 and later.</span></span>

<span data-ttu-id="38db0-370">0x0 indica HTTP/1.1 ou anterior; consulte INTERNET \_ Option \_ http \_ version se for necessário mais precisão sobre qual versão herdada foi usada.</span><span class="sxs-lookup"><span data-stu-id="38db0-370">0x0 indicates HTTP/1.1 or earlier; see INTERNET\_OPTION\_HTTP\_VERSION if more precision is needed about which legacy version was used.</span></span> <span data-ttu-id="38db0-371">Com suporte no Windows 10, versão 1507 e posterior.</span><span class="sxs-lookup"><span data-stu-id="38db0-371">Supported on Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-372"><span id="INTERNET_OPTION_HTTP_VERSION"></span><span id="internet_option_http_version"></span>**\_ \_ versão http da opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-372"><span id="INTERNET_OPTION_HTTP_VERSION"></span><span id="internet_option_http_version"></span>**INTERNET\_OPTION\_HTTP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-373">59</span><span class="sxs-lookup"><span data-stu-id="38db0-373">59</span></span>
</dt> <dt>



<span data-ttu-id="38db0-374">Define ou recupera uma estrutura de [**\_ \_ informações de versão http**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) que contém a versão de http com suporte.</span><span class="sxs-lookup"><span data-stu-id="38db0-374">Sets or retrieves an [**HTTP\_VERSION\_INFO**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) structure that contains the supported HTTP version.</span></span> <span data-ttu-id="38db0-375">Isso deve ser usado em um identificador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="38db0-375">This must be used on a **NULL** handle.</span></span> <span data-ttu-id="38db0-376">Isso é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-376">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="38db0-377">No Windows 7, no Windows Server 2008 R2 e posterior, o valor do membro **dwMinorVersion** na estrutura de [**\_ \_ informações de versão http**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) é substituído pelas configurações do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="38db0-377">On Windows 7, Windows Server 2008 R2, and later, the value of the **dwMinorVersion** member in the [**HTTP\_VERSION\_INFO**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) structure is overridden by Internet Explorer settings.</span></span> <span data-ttu-id="38db0-378">**EnableHttp1 \_ 1** é um valor de registro em **HKLM \\ software \\ Microsoft \\ InternetExplorer \\ AdvacnedOptions \\ http \\ GENABLE** controlado pelas opções da Internet definidas no Internet Explorer para o sistema.</span><span class="sxs-lookup"><span data-stu-id="38db0-378">**EnableHttp1\_1** is a registry value under **HKLM\\Software\\Microsoft\\InternetExplorer\\AdvacnedOptions\\HTTP\\GENABLE** controlled by Internet Options set in Internet Explorer for the system.</span></span> <span data-ttu-id="38db0-379">O valor padrão de **EnableHttp1 \_ 1** é 1.</span><span class="sxs-lookup"><span data-stu-id="38db0-379">The **EnableHttp1\_1** value defaults to 1.</span></span> <span data-ttu-id="38db0-380">A estrutura de **\_ \_ informações de versão http** é ignorada para qualquer versão de http inferior a 1,1 se **EnableHttp1 \_ 1** for definido como 1.</span><span class="sxs-lookup"><span data-stu-id="38db0-380">The **HTTP\_VERSION\_INFO** structure is ignored for any HTTP version less than 1.1 if **EnableHttp1\_1** is set to 1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-381"><span id="INTERNET_OPTION_IDENTITY"></span><span id="internet_option_identity"></span>**\_identidade de opção de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-381"><span id="INTERNET_OPTION_IDENTITY"></span><span id="internet_option_identity"></span>**INTERNET\_OPTION\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-382">78</span><span class="sxs-lookup"><span data-stu-id="38db0-382">78</span></span>
</dt> <dt>



<span data-ttu-id="38db0-383">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="38db0-383">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-384"><span id="INTERNET_OPTION_IDLE_STATE"></span><span id="internet_option_idle_state"></span>**\_ \_ estado ocioso da opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-384"><span id="INTERNET_OPTION_IDLE_STATE"></span><span id="internet_option_idle_state"></span>**INTERNET\_OPTION\_IDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-385">51</span><span class="sxs-lookup"><span data-stu-id="38db0-385">51</span></span>
</dt> <dt>



<span data-ttu-id="38db0-386">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="38db0-386">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-387"><span id="INTERNET_OPTION_IDN"></span><span id="internet_option_idn"></span>**opção de INTERNET \_ \_ IDN**</span><span class="sxs-lookup"><span data-stu-id="38db0-387"><span id="INTERNET_OPTION_IDN"></span><span id="internet_option_idn"></span>**INTERNET\_OPTION\_IDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-388">102</span><span class="sxs-lookup"><span data-stu-id="38db0-388">102</span></span>
</dt> <dt>



<span data-ttu-id="38db0-389">Por padrão, a parte de host ou autoridade da URL é codificada de acordo com a especificação de IDN para conexões diretas e de proxy.</span><span class="sxs-lookup"><span data-stu-id="38db0-389">By default, the host or authority portion of the URL is encoded according to the IDN specification for both direct and proxy connections.</span></span> <span data-ttu-id="38db0-390">Essa opção pode ser usada na solicitação ou no identificador de conexão para habilitar ou desabilitar o IDN.</span><span class="sxs-lookup"><span data-stu-id="38db0-390">This option can be used on the request, or connection handle to enable or disable IDN.</span></span> <span data-ttu-id="38db0-391">Quando o IDN é desabilitado, o WinINet usa a página de código do sistema para codificar a parte de host ou autoridade da URL.</span><span class="sxs-lookup"><span data-stu-id="38db0-391">When IDN is disabled, WinINet uses the system codepage to encode the host or authority portion of the URL.</span></span> <span data-ttu-id="38db0-392">Para desabilitar a conversão de host IDN, defina o parâmetro *lpBuffer* na chamada de [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) como zero.</span><span class="sxs-lookup"><span data-stu-id="38db0-392">To disable IDN host conversion, set the *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) to zero.</span></span> <span data-ttu-id="38db0-393">Para habilitar a conversão de IDN somente na conexão direta, especifique **sinalizador de Internet de \_ \_ IDN \_ direto** no parâmetro *lpBuffer* na chamada para **InternetSetOption**.</span><span class="sxs-lookup"><span data-stu-id="38db0-393">To enable IDN conversion on only the direct connection, specify **INTERNET\_FLAG\_IDN\_DIRECT** in the *lpBuffer* parameter in the call to **InternetSetOption**.</span></span> <span data-ttu-id="38db0-394">Para habilitar a conversão de IDN somente na conexão de proxy, especifique o **\_ \_ \_ proxy IDN do sinalizador da Internet** no parâmetro *lpBuffer* na chamada para **InternetSetOption**.</span><span class="sxs-lookup"><span data-stu-id="38db0-394">To enable IDN conversion on only the proxy connection, specify **INTERNET\_FLAG\_IDN\_PROXY** in the *lpBuffer* parameter in the call to **InternetSetOption**.</span></span>

<span data-ttu-id="38db0-395">**Windows XP com SP2 e Windows Server 2003 com SP1:** Não há suporte para esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="38db0-395">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="38db0-396">**Versão:** Requer o Internet Explorer 7,0.</span><span class="sxs-lookup"><span data-stu-id="38db0-396">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-397"><span id="INTERNET_OPTION_IGNORE_OFFLINE"></span><span id="internet_option_ignore_offline"></span>**opção da INTERNET \_ \_ ignorar \_ offline**</span><span class="sxs-lookup"><span data-stu-id="38db0-397"><span id="INTERNET_OPTION_IGNORE_OFFLINE"></span><span id="internet_option_ignore_offline"></span>**INTERNET\_OPTION\_IGNORE\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-398">77</span><span class="sxs-lookup"><span data-stu-id="38db0-398">77</span></span>
</dt> <dt>



<span data-ttu-id="38db0-399">Define ou recupera se o sinalizador offline global deve ser ignorado para o identificador de solicitação especificado.</span><span class="sxs-lookup"><span data-stu-id="38db0-399">Sets or retrieves whether the global offline flag should be ignored for the specified request handle.</span></span> <span data-ttu-id="38db0-400">Nenhum buffer é necessário para essa opção.</span><span class="sxs-lookup"><span data-stu-id="38db0-400">No buffer is required for this option.</span></span> <span data-ttu-id="38db0-401">Isso é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) com um identificador de solicitação.</span><span class="sxs-lookup"><span data-stu-id="38db0-401">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) with a request handle.</span></span> <span data-ttu-id="38db0-402">Essa opção só é válida no Internet Explorer 5 e posterior.</span><span class="sxs-lookup"><span data-stu-id="38db0-402">This option is only valid in Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-403"><span id="INTERNET_OPTION_KEEP_CONNECTION"></span><span id="internet_option_keep_connection"></span>**\_opção de \_ manter \_ conexão com a Internet**</span><span class="sxs-lookup"><span data-stu-id="38db0-403"><span id="INTERNET_OPTION_KEEP_CONNECTION"></span><span id="internet_option_keep_connection"></span>**INTERNET\_OPTION\_KEEP\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-404">22</span><span class="sxs-lookup"><span data-stu-id="38db0-404">22</span></span>
</dt> <dt>



<span data-ttu-id="38db0-405">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="38db0-405">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-406"><span id="INTERNET_OPTION_LISTEN_TIMEOUT"></span><span id="internet_option_listen_timeout"></span>**\_ \_ tempo limite de escuta de opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-406"><span id="INTERNET_OPTION_LISTEN_TIMEOUT"></span><span id="internet_option_listen_timeout"></span>**INTERNET\_OPTION\_LISTEN\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-407">11</span><span class="sxs-lookup"><span data-stu-id="38db0-407">11</span></span>
</dt> <dt>



<span data-ttu-id="38db0-408">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="38db0-408">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-409"><span id="INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="internet_option_max_conns_per_1_0_server"></span>**Opção máxima de Conn. da INTERNET \_ \_ \_ \_ por \_ \_ servidor 1 0 \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-409"><span id="INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="internet_option_max_conns_per_1_0_server"></span>**INTERNET\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-410">74</span><span class="sxs-lookup"><span data-stu-id="38db0-410">74</span></span>
</dt> <dt>



<span data-ttu-id="38db0-411">Define ou recupera um valor inteiro longo sem sinal que contém o número máximo de conexões permitidas por servidor HTTP/1.0.</span><span class="sxs-lookup"><span data-stu-id="38db0-411">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per HTTP/1.0 server.</span></span> <span data-ttu-id="38db0-412">Isso é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-412">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="38db0-413">Essa opção só é válida no Internet Explorer 5 e posterior.</span><span class="sxs-lookup"><span data-stu-id="38db0-413">This option is only valid in Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-414"><span id="INTERNET_OPTION_MAX_CONNS_PER_PROXY"></span><span id="internet_option_max_conns_per_proxy"></span>**\_opção \_ máxima de \_ Conns \_ por \_ proxy na Internet**</span><span class="sxs-lookup"><span data-stu-id="38db0-414"><span id="INTERNET_OPTION_MAX_CONNS_PER_PROXY"></span><span id="internet_option_max_conns_per_proxy"></span>**INTERNET\_OPTION\_MAX\_CONNS\_PER\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-415">103</span><span class="sxs-lookup"><span data-stu-id="38db0-415">103</span></span>
</dt> <dt>



<span data-ttu-id="38db0-416">Define ou recupera um valor inteiro longo sem sinal que contém o número máximo de conexões permitidas por proxy de CERN.</span><span class="sxs-lookup"><span data-stu-id="38db0-416">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per CERN proxy.</span></span> <span data-ttu-id="38db0-417">Quando essa opção é definida ou recuperada, o parâmetro *hInternet* deve ser definido como um valor de identificador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="38db0-417">When this option is set or retrieved, the *hInternet* parameter must set to a **null** handle value.</span></span> <span data-ttu-id="38db0-418">Um valor de identificador **nulo** indica que a opção deve ser definida ou consultada para o processo atual.</span><span class="sxs-lookup"><span data-stu-id="38db0-418">A **null** handle value indicates that the option should be set or queried for the current process.</span></span> <span data-ttu-id="38db0-419">Ao chamar o [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) com essa opção, todos os objetos de proxy existentes receberão o novo valor.</span><span class="sxs-lookup"><span data-stu-id="38db0-419">When calling [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) with this option, all existing proxy objects will receive the new value.</span></span> <span data-ttu-id="38db0-420">Esse valor é limitado a um intervalo de 2 a 128, inclusive.</span><span class="sxs-lookup"><span data-stu-id="38db0-420">This value is limited to a range of 2 to 128, inclusive.</span></span>

<span data-ttu-id="38db0-421">**Versão:** Requer o Internet Explorer 8,0.</span><span class="sxs-lookup"><span data-stu-id="38db0-421">**Version:** Requires Internet Explorer 8.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-422"><span id="INTERNET_OPTION_MAX_CONNS_PER_SERVER"></span><span id="internet_option_max_conns_per_server"></span>**opção máxima de Conn. da INTERNET \_ \_ \_ \_ por \_ servidor**</span><span class="sxs-lookup"><span data-stu-id="38db0-422"><span id="INTERNET_OPTION_MAX_CONNS_PER_SERVER"></span><span id="internet_option_max_conns_per_server"></span>**INTERNET\_OPTION\_MAX\_CONNS\_PER\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-423">73</span><span class="sxs-lookup"><span data-stu-id="38db0-423">73</span></span>
</dt> <dt>



<span data-ttu-id="38db0-424">Define ou recupera um valor inteiro longo sem sinal que contém o número máximo de conexões permitidas por servidor.</span><span class="sxs-lookup"><span data-stu-id="38db0-424">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per server.</span></span> <span data-ttu-id="38db0-425">Isso é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-425">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="38db0-426">Essa opção só é válida no Internet Explorer 5 e posterior.</span><span class="sxs-lookup"><span data-stu-id="38db0-426">This option is only valid in Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-427"><span id="INTERNET_OPTION_OFFLINE_MODE"></span><span id="internet_option_offline_mode"></span>**\_ \_ modo offline de opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-427"><span id="INTERNET_OPTION_OFFLINE_MODE"></span><span id="internet_option_offline_mode"></span>**INTERNET\_OPTION\_OFFLINE\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-428">26</span><span class="sxs-lookup"><span data-stu-id="38db0-428">26</span></span>
</dt> <dt>



<span data-ttu-id="38db0-429">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="38db0-429">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-430"><span id="INTERNET_OPTION_OFFLINE_SEMANTICS"></span><span id="internet_option_offline_semantics"></span>**\_ \_ semântica offline de opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-430"><span id="INTERNET_OPTION_OFFLINE_SEMANTICS"></span><span id="internet_option_offline_semantics"></span>**INTERNET\_OPTION\_OFFLINE\_SEMANTICS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-431">52</span><span class="sxs-lookup"><span data-stu-id="38db0-431">52</span></span>
</dt> <dt>



<span data-ttu-id="38db0-432">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="38db0-432">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-433"><span id="INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE"></span><span id="internet_option_opt_in_weak_signature"></span>**\_opção \_ da Internet \_ aceitar \_ \_ assinatura fraca**</span><span class="sxs-lookup"><span data-stu-id="38db0-433"><span id="INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE"></span><span id="internet_option_opt_in_weak_signature"></span>**INTERNET\_OPTION\_OPT\_IN\_WEAK\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-434">176</span><span class="sxs-lookup"><span data-stu-id="38db0-434">176</span></span>
</dt> <dt>



<span data-ttu-id="38db0-435">Aceitação de assinaturas fracas (por exemplo, SHA-1) a serem tratadas como inseguras.</span><span class="sxs-lookup"><span data-stu-id="38db0-435">Opt-in for weak signatures (e.g. SHA-1) to be treated as insecure.</span></span> <span data-ttu-id="38db0-436">Isso instruirá o WinInet a chamar [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) usando o parâmetro de **\_ \_ \_ \_ \_ assinatura fraca de aceitação da cadeia de certificados** .</span><span class="sxs-lookup"><span data-stu-id="38db0-436">This will instruct WinInet to call [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) using the **CERT\_CHAIN\_OPT\_IN\_WEAK\_SIGNATURE** parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-437"><span id="INTERNET_OPTION_PARENT_HANDLE"></span><span id="internet_option_parent_handle"></span>**\_ \_ identificador pai da opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-437"><span id="INTERNET_OPTION_PARENT_HANDLE"></span><span id="internet_option_parent_handle"></span>**INTERNET\_OPTION\_PARENT\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-438">21</span><span class="sxs-lookup"><span data-stu-id="38db0-438">21</span></span>
</dt> <dt>



<span data-ttu-id="38db0-439">Recupera o identificador pai para esse identificador.</span><span class="sxs-lookup"><span data-stu-id="38db0-439">Retrieves the parent handle to this handle.</span></span> <span data-ttu-id="38db0-440">Essa opção pode ser usada em qualquer identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-440">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-441"><span id="INTERNET_OPTION_PASSWORD"></span><span id="internet_option_password"></span>**\_senha da opção de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-441"><span id="INTERNET_OPTION_PASSWORD"></span><span id="internet_option_password"></span>**INTERNET\_OPTION\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-442">29</span><span class="sxs-lookup"><span data-stu-id="38db0-442">29</span></span>
</dt> <dt>



<span data-ttu-id="38db0-443">Define ou recupera um valor de cadeia de caracteres que contém a senha associada a um identificador retornado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="38db0-443">Sets or retrieves a string value that contains the password associated with a handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="38db0-444">Isso é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-444">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-445"><span id="INTERNET_OPTION_PER_CONNECTION_OPTION"></span><span id="internet_option_per_connection_option"></span>**opção da INTERNET \_ \_ por \_ opção de conexão \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-445"><span id="INTERNET_OPTION_PER_CONNECTION_OPTION"></span><span id="internet_option_per_connection_option"></span>**INTERNET\_OPTION\_PER\_CONNECTION\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-446">75</span><span class="sxs-lookup"><span data-stu-id="38db0-446">75</span></span>
</dt> <dt>



<span data-ttu-id="38db0-447">Define ou recupera uma estrutura de lista de opções de [**Internet \_ por \_ Conn \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) que especifica uma lista de opções para uma conexão específica.</span><span class="sxs-lookup"><span data-stu-id="38db0-447">Sets or retrieves an [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) structure that specifies a list of options for a particular connection.</span></span> <span data-ttu-id="38db0-448">Isso é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-448">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="38db0-449">Essa opção só é válida no Internet Explorer 5 e posterior.</span><span class="sxs-lookup"><span data-stu-id="38db0-449">This option is only valid in Internet Explorer 5 and later.</span></span>

> [!Note]  
> <span data-ttu-id="38db0-450">**Internet \_ OPÇÃO \_ por \_ \_ opção de conexão** faz com que as configurações sejam alteradas em todo o sistema quando um identificador **nulo** é usado na chamada para [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-450">**INTERNET\_OPTION\_PER\_CONNECTION\_OPTION** causes the settings to be changed on a system-wide basis when a **NULL** handle is used in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="38db0-451">Para atualizar as configurações de proxy globais, você deve chamar **InternetSetOption** com o sinalizador de opção de **\_ \_ atualização de opção da Internet** .</span><span class="sxs-lookup"><span data-stu-id="38db0-451">To refresh the global proxy settings, you must call **InternetSetOption** with the **INTERNET\_OPTION\_REFRESH** option flag.</span></span>

 

> [!Note]  
> <span data-ttu-id="38db0-452">Para alterar as informações de proxy para todo o processo sem afetar as configurações globais no Internet Explorer 5 e posterior, use essa opção no identificador que é retornado de [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="38db0-452">To change proxy information for the entire process without affecting the global settings in Internet Explorer 5 and later, use this option on the handle that is returned from [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="38db0-453">O exemplo de código a seguir altera o proxy para todo o processo, embora o identificador [**HINTERNET**](appendix-a-hinternet-handles.md) seja fechado e não seja usado por nenhuma solicitação.</span><span class="sxs-lookup"><span data-stu-id="38db0-453">The following code example changes the proxy for the whole process even though the [**HINTERNET**](appendix-a-hinternet-handles.md) handle is closed and is not used by any requests.</span></span>

 

<span data-ttu-id="38db0-454">Para obter mais informações e exemplos de código, consulte o [artigo 226473 da base](https://support.microsoft.com/kb/226473)de dados de conhecimento.</span><span class="sxs-lookup"><span data-stu-id="38db0-454">For more information and code examples, see [KB article 226473](https://support.microsoft.com/kb/226473).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-455"><span id="INTERNET_OPTION_POLICY"></span><span id="internet_option_policy"></span>**\_diretiva de opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-455"><span id="INTERNET_OPTION_POLICY"></span><span id="internet_option_policy"></span>**INTERNET\_OPTION\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-456">48</span><span class="sxs-lookup"><span data-stu-id="38db0-456">48</span></span>
</dt> <dt>



<span data-ttu-id="38db0-457">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="38db0-457">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-458"><span id="INTERNET_OPTION_PROXY"></span><span id="internet_option_proxy"></span>**\_proxy de opção de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-458"><span id="INTERNET_OPTION_PROXY"></span><span id="internet_option_proxy"></span>**INTERNET\_OPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-459">38</span><span class="sxs-lookup"><span data-stu-id="38db0-459">38</span></span>
</dt> <dt>



<span data-ttu-id="38db0-460">Define ou recupera uma estrutura de [**\_ \_ informações de proxy da Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_proxy_info) que contém os dados de proxy para um identificador [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) existente quando o identificador [**HINTERNET**](appendix-a-hinternet-handles.md) não é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="38db0-460">Sets or retrieves an [**INTERNET\_PROXY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_proxy_info) structure that contains the proxy data for an existing [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) handle when the [**HINTERNET**](appendix-a-hinternet-handles.md) handle is not **NULL**.</span></span> <span data-ttu-id="38db0-461">Se o identificador [**HINTERNET**](appendix-a-hinternet-handles.md) for **nulo**, a função definirá ou consultará os dados do proxy global.</span><span class="sxs-lookup"><span data-stu-id="38db0-461">If the [**HINTERNET**](appendix-a-hinternet-handles.md) handle is **NULL**, the function sets or queries the global proxy data.</span></span> <span data-ttu-id="38db0-462">Essa opção pode ser usada no identificador retornado por **InternetOpen**.</span><span class="sxs-lookup"><span data-stu-id="38db0-462">This option can be used on the handle returned by **InternetOpen**.</span></span> <span data-ttu-id="38db0-463">Ele é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-463">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

> [!Note]  
> <span data-ttu-id="38db0-464">É recomendável que a opção \_ opção \_ de Internet por \_ conexão \_ seja usada em vez do proxy de opção de Internet \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="38db0-464">It is recommended that INTERNET\_OPTION\_PER\_CONNECTION\_OPTION be used instead of INTERNET\_OPTION\_PROXY.</span></span> <span data-ttu-id="38db0-465">Para obter mais informações, consulte o [artigo 226473 da base](https://support.microsoft.com/kb/226473)de dados de conhecimento.</span><span class="sxs-lookup"><span data-stu-id="38db0-465">For more information, see [KB article 226473](https://support.microsoft.com/kb/226473).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-466"><span id="INTERNET_OPTION_PROXY_PASSWORD"></span><span id="internet_option_proxy_password"></span>**\_senha do \_ proxy de opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-466"><span id="INTERNET_OPTION_PROXY_PASSWORD"></span><span id="internet_option_proxy_password"></span>**INTERNET\_OPTION\_PROXY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-467">44</span><span class="sxs-lookup"><span data-stu-id="38db0-467">44</span></span>
</dt> <dt>



<span data-ttu-id="38db0-468">Define ou recupera um valor de cadeia de caracteres que contém a senha usada para acessar o proxy.</span><span class="sxs-lookup"><span data-stu-id="38db0-468">Sets or retrieves a string value that contains the password used to access the proxy.</span></span> <span data-ttu-id="38db0-469">Isso é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-469">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="38db0-470">Essa opção pode ser definida no identificador retornado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="38db0-470">This option can be set on the handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-471"><span id="INTERNET_OPTION_PROXY_SETTINGS_CHANGED"></span><span id="internet_option_proxy_settings_changed"></span>**configurações de proxy de opção de INTERNET \_ \_ \_ \_ alteradas**</span><span class="sxs-lookup"><span data-stu-id="38db0-471"><span id="INTERNET_OPTION_PROXY_SETTINGS_CHANGED"></span><span id="internet_option_proxy_settings_changed"></span>**INTERNET\_OPTION\_PROXY\_SETTINGS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-472">95</span><span class="sxs-lookup"><span data-stu-id="38db0-472">95</span></span> 
</dt> <dt>



<span data-ttu-id="38db0-473">Alerta a instância atual do WinInet de que as configurações de proxy foram alteradas e que devem ser atualizadas com as novas configurações.</span><span class="sxs-lookup"><span data-stu-id="38db0-473">Alerts the current WinInet instance that proxy settings have changed and that they must update with the new settings.</span></span> <span data-ttu-id="38db0-474">Para alertar todas as instâncias do WinInet disponíveis, defina o parâmetro *buffer* de [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) como **NULL** e *BufferLength* como 0 ao passar essa opção.</span><span class="sxs-lookup"><span data-stu-id="38db0-474">To alert all available WinInet instances, set the *Buffer* parameter of [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) to **NULL** and *BufferLength* to 0 when passing this option.</span></span> <span data-ttu-id="38db0-475">Essa opção pode ser definida no identificador retornado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="38db0-475">This option can be set on the handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-476"><span id="INTERNET_OPTION_PROXY_USERNAME"></span><span id="internet_option_proxy_username"></span>**\_nome de \_ usuário do proxy de opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-476"><span id="INTERNET_OPTION_PROXY_USERNAME"></span><span id="internet_option_proxy_username"></span>**INTERNET\_OPTION\_PROXY\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-477">43</span><span class="sxs-lookup"><span data-stu-id="38db0-477">43</span></span>
</dt> <dt>



<span data-ttu-id="38db0-478">Define ou recupera um valor de cadeia de caracteres que contém o nome de usuário usado para acessar o proxy.</span><span class="sxs-lookup"><span data-stu-id="38db0-478">Sets or retrieves a string value that contains the user name used to access the proxy.</span></span> <span data-ttu-id="38db0-479">Isso é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-479">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="38db0-480">Essa opção pode ser definida no identificador retornado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="38db0-480">This option can be set on the handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-481"><span id="INTERNET_OPTION_READ_BUFFER_SIZE"></span><span id="internet_option_read_buffer_size"></span>**\_tamanho do \_ buffer de leitura da opção da Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-481"><span id="INTERNET_OPTION_READ_BUFFER_SIZE"></span><span id="internet_option_read_buffer_size"></span>**INTERNET\_OPTION\_READ\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-482">12</span><span class="sxs-lookup"><span data-stu-id="38db0-482">12</span></span>
</dt> <dt>



<span data-ttu-id="38db0-483">Define ou recupera um valor inteiro longo sem sinal que contém o tamanho do buffer de leitura.</span><span class="sxs-lookup"><span data-stu-id="38db0-483">Sets or retrieves an unsigned long integer value that contains the size of the read buffer.</span></span> <span data-ttu-id="38db0-484">Essa opção pode ser usada em identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) retornados por [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)e [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (somente sessão de FTP).</span><span class="sxs-lookup"><span data-stu-id="38db0-484">This option can be used on [**HINTERNET**](appendix-a-hinternet-handles.md) handles returned by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), and [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (FTP session only).</span></span> <span data-ttu-id="38db0-485">Essa opção é usada por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-485">This option is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-486"><span id="INTERNET_OPTION_RECEIVE_THROUGHPUT"></span><span id="internet_option_receive_throughput"></span>**\_taxa de \_ transferência de recepção de opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-486"><span id="INTERNET_OPTION_RECEIVE_THROUGHPUT"></span><span id="internet_option_receive_throughput"></span>**INTERNET\_OPTION\_RECEIVE\_THROUGHPUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-487">57</span><span class="sxs-lookup"><span data-stu-id="38db0-487">57</span></span>
</dt> <dt>



<span data-ttu-id="38db0-488">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="38db0-488">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-489"><span id="INTERNET_OPTION_RECEIVE_TIMEOUT"></span><span id="internet_option_receive_timeout"></span>**\_ \_ tempo limite de recebimento de opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-489"><span id="INTERNET_OPTION_RECEIVE_TIMEOUT"></span><span id="internet_option_receive_timeout"></span>**INTERNET\_OPTION\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-490">6</span><span class="sxs-lookup"><span data-stu-id="38db0-490">6</span></span>
</dt> <dt>



<span data-ttu-id="38db0-491">Define ou recupera um valor inteiro longo sem sinal que contém o valor de tempo limite, em milissegundos, para receber uma resposta a uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="38db0-491">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a response to a request.</span></span> <span data-ttu-id="38db0-492">Se a resposta demorar mais do que esse valor de tempo limite, a solicitação será cancelada.</span><span class="sxs-lookup"><span data-stu-id="38db0-492">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="38db0-493">Essa opção pode ser usada em qualquer identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) , incluindo um identificador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="38db0-493">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="38db0-494">Ele é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-494">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="38db0-495">Essa opção não se destina a representar um tempo limite refinado e imediato.</span><span class="sxs-lookup"><span data-stu-id="38db0-495">This option is not intended to represent a fine-grained, immediate timeout.</span></span> <span data-ttu-id="38db0-496">Você pode esperar que o tempo limite ocorra até seis segundos após o valor de tempo limite definido.</span><span class="sxs-lookup"><span data-stu-id="38db0-496">You can expect the timeout to occur up to six seconds after the set timeout value.</span></span>

<span data-ttu-id="38db0-497">Quando usado em referência a uma transação de FTP, essa opção se refere ao canal de controle.</span><span class="sxs-lookup"><span data-stu-id="38db0-497">When used in reference to an FTP transaction, this option refers to the control channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-498"><span id="INTERNET_OPTION_REFRESH"></span><span id="internet_option_refresh"></span>**\_atualização da opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-498"><span id="INTERNET_OPTION_REFRESH"></span><span id="internet_option_refresh"></span>**INTERNET\_OPTION\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-499">37</span><span class="sxs-lookup"><span data-stu-id="38db0-499">37</span></span>
</dt> <dt>



<span data-ttu-id="38db0-500">Faz com que os dados do proxy sejam lidos novamente do registro para um identificador.</span><span class="sxs-lookup"><span data-stu-id="38db0-500">Causes the proxy data to be reread from the registry for a handle.</span></span> <span data-ttu-id="38db0-501">Nenhum buffer é necessário.</span><span class="sxs-lookup"><span data-stu-id="38db0-501">No buffer is required.</span></span> <span data-ttu-id="38db0-502">Essa opção pode ser usada no identificador [**HINTERNET**](appendix-a-hinternet-handles.md) retornado por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="38db0-502">This option can be used on the [**HINTERNET**](appendix-a-hinternet-handles.md) handle returned by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="38db0-503">Ele é usado por [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-503">It is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-504"><span id="INTERNET_OPTION_REMOVE_IDENTITY"></span><span id="internet_option_remove_identity"></span>**\_opção de \_ remoção de \_ identidade da Internet**</span><span class="sxs-lookup"><span data-stu-id="38db0-504"><span id="INTERNET_OPTION_REMOVE_IDENTITY"></span><span id="internet_option_remove_identity"></span>**INTERNET\_OPTION\_REMOVE\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-505">79</span><span class="sxs-lookup"><span data-stu-id="38db0-505">79</span></span>
</dt> <dt>



<span data-ttu-id="38db0-506">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="38db0-506">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-507"><span id="INTERNET_OPTION_REQUEST_FLAGS"></span><span id="internet_option_request_flags"></span>**\_sinalizadores de \_ solicitação de opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-507"><span id="INTERNET_OPTION_REQUEST_FLAGS"></span><span id="internet_option_request_flags"></span>**INTERNET\_OPTION\_REQUEST\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-508">23</span><span class="sxs-lookup"><span data-stu-id="38db0-508">23</span></span>
</dt> <dt>



<span data-ttu-id="38db0-509">Recupera um valor inteiro longo sem sinal que contém os sinalizadores de status especiais que indicam o status do download em andamento.</span><span class="sxs-lookup"><span data-stu-id="38db0-509">Retrieves an unsigned long integer value that contains the special status flags that indicate the status of the download in progress.</span></span> <span data-ttu-id="38db0-510">Isso é usado pelo [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-510">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="38db0-511">A [opção \_ \_ \_ sinalizadores de solicitação de opção da Internet](/windows) pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="38db0-511">The [INTERNET\_OPTION\_REQUEST\_FLAGS](/windows) option can be one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="38db0-512"><span id="INTERNET_REQFLAG_ASYNC"></span><span id="internet_reqflag_async"></span>\_REQFLAG \_ assíncrona da Internet</span><span class="sxs-lookup"><span data-stu-id="38db0-512"><span id="INTERNET_REQFLAG_ASYNC"></span><span id="internet_reqflag_async"></span>INTERNET\_REQFLAG\_ASYNC</span></span>
</dt> <dd>

<span data-ttu-id="38db0-513">0x00000002</span><span class="sxs-lookup"><span data-stu-id="38db0-513">0x00000002</span></span>

<span data-ttu-id="38db0-514">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="38db0-514">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="38db0-515"><span id="INTERNET_REQFLAG_CACHE_WRITE_DISABLED"></span><span id="internet_reqflag_cache_write_disabled"></span>\_gravação de cache REQFLAG da Internet \_ \_ \_ desabilitada</span><span class="sxs-lookup"><span data-stu-id="38db0-515"><span id="INTERNET_REQFLAG_CACHE_WRITE_DISABLED"></span><span id="internet_reqflag_cache_write_disabled"></span>INTERNET\_REQFLAG\_CACHE\_WRITE\_DISABLED</span></span>
</dt> <dd>

<span data-ttu-id="38db0-516">0x00000040</span><span class="sxs-lookup"><span data-stu-id="38db0-516">0x00000040</span></span>

<span data-ttu-id="38db0-517">A solicitação da Internet não pode ser armazenada em cache (uma solicitação HTTPS, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="38db0-517">Internet request cannot be cached (an HTTPS request, for example).</span></span>

</dd> <dt>

<span data-ttu-id="38db0-518"><span id="INTERNET_REQFLAG_FROM_CACHE"></span><span id="internet_reqflag_from_cache"></span>\_REQFLAG \_ da Internet do \_ cache</span><span class="sxs-lookup"><span data-stu-id="38db0-518"><span id="INTERNET_REQFLAG_FROM_CACHE"></span><span id="internet_reqflag_from_cache"></span>INTERNET\_REQFLAG\_FROM\_CACHE</span></span>
</dt> <dd>

<span data-ttu-id="38db0-519">0x00000001</span><span class="sxs-lookup"><span data-stu-id="38db0-519">0x00000001</span></span>

<span data-ttu-id="38db0-520">A resposta veio do cache.</span><span class="sxs-lookup"><span data-stu-id="38db0-520">Response came from the cache.</span></span>

</dd> <dt>

<span data-ttu-id="38db0-521"><span id="INTERNET_REQFLAG_NET_TIMEOUT"></span><span id="internet_reqflag_net_timeout"></span>\_ \_ tempo limite de rede REQFLAG da Internet \_</span><span class="sxs-lookup"><span data-stu-id="38db0-521"><span id="INTERNET_REQFLAG_NET_TIMEOUT"></span><span id="internet_reqflag_net_timeout"></span>INTERNET\_REQFLAG\_NET\_TIMEOUT</span></span>
</dt> <dd>

<span data-ttu-id="38db0-522">0x00000080</span><span class="sxs-lookup"><span data-stu-id="38db0-522">0x00000080</span></span>

<span data-ttu-id="38db0-523">A solicitação da Internet atingiu o tempo limite.</span><span class="sxs-lookup"><span data-stu-id="38db0-523">Internet request timed out.</span></span>

</dd> <dt>

<span data-ttu-id="38db0-524"><span id="INTERNET_REQFLAG_NO_HEADERS"></span><span id="internet_reqflag_no_headers"></span>REQFLAG de INTERNET \_ \_ sem \_ cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="38db0-524"><span id="INTERNET_REQFLAG_NO_HEADERS"></span><span id="internet_reqflag_no_headers"></span>INTERNET\_REQFLAG\_NO\_HEADERS</span></span>
</dt> <dd>

<span data-ttu-id="38db0-525">0x00000008</span><span class="sxs-lookup"><span data-stu-id="38db0-525">0x00000008</span></span>

<span data-ttu-id="38db0-526">A resposta original não continha nenhum cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="38db0-526">Original response contained no headers.</span></span>

</dd> <dt>

<span data-ttu-id="38db0-527"><span id="INTERNET_REQFLAG_PASSIVE"></span><span id="internet_reqflag_passive"></span>INTERNET \_ REQFLAG \_ passivo</span><span class="sxs-lookup"><span data-stu-id="38db0-527"><span id="INTERNET_REQFLAG_PASSIVE"></span><span id="internet_reqflag_passive"></span>INTERNET\_REQFLAG\_PASSIVE</span></span>
</dt> <dd>

<span data-ttu-id="38db0-528">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38db0-528">0x00000010</span></span>

<span data-ttu-id="38db0-529">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="38db0-529">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="38db0-530"><span id="INTERNET_REQFLAG_VIA_PROXY"></span><span id="internet_reqflag_via_proxy"></span>REQFLAG da INTERNET \_ \_ via \_ proxy</span><span class="sxs-lookup"><span data-stu-id="38db0-530"><span id="INTERNET_REQFLAG_VIA_PROXY"></span><span id="internet_reqflag_via_proxy"></span>INTERNET\_REQFLAG\_VIA\_PROXY</span></span>
</dt> <dd>

<span data-ttu-id="38db0-531">0x00000004</span><span class="sxs-lookup"><span data-stu-id="38db0-531">0x00000004</span></span>

<span data-ttu-id="38db0-532">A solicitação foi feita por meio de um proxy.</span><span class="sxs-lookup"><span data-stu-id="38db0-532">Request was made through a proxy.</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="38db0-533"><span id="INTERNET_OPTION_REQUEST_PRIORITY"></span><span id="internet_option_request_priority"></span>**\_prioridade de \_ solicitação de opção de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-533"><span id="INTERNET_OPTION_REQUEST_PRIORITY"></span><span id="internet_option_request_priority"></span>**INTERNET\_OPTION\_REQUEST\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-534">58</span><span class="sxs-lookup"><span data-stu-id="38db0-534">58</span></span>
</dt> <dt>



<span data-ttu-id="38db0-535">Define ou recupera um valor inteiro longo sem sinal que contém a prioridade das solicitações que conpetem por uma conexão em um identificador HTTP.</span><span class="sxs-lookup"><span data-stu-id="38db0-535">Sets or retrieves an unsigned long integer value that contains the priority of requests that compete for a connection on an HTTP handle.</span></span> <span data-ttu-id="38db0-536">Isso é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-536">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-537"><span id="INTERNET_OPTION_RESET_URLCACHE_SESSION"></span><span id="internet_option_reset_urlcache_session"></span>**\_ \_ sessão URLCACHE de redefinição de opção da \_ Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-537"><span id="INTERNET_OPTION_RESET_URLCACHE_SESSION"></span><span id="internet_option_reset_urlcache_session"></span>**INTERNET\_OPTION\_RESET\_URLCACHE\_SESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-538">60</span><span class="sxs-lookup"><span data-stu-id="38db0-538">60</span></span>
</dt> <dt>



<span data-ttu-id="38db0-539">Inicia uma nova sessão de cache para o processo.</span><span class="sxs-lookup"><span data-stu-id="38db0-539">Starts a new cache session for the process.</span></span> <span data-ttu-id="38db0-540">Nenhum buffer é necessário.</span><span class="sxs-lookup"><span data-stu-id="38db0-540">No buffer is required.</span></span> <span data-ttu-id="38db0-541">Isso é usado por [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-541">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="38db0-542">Esta opção é reservada somente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="38db0-542">This option is reserved for internal use only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-543"><span id="INTERNET_OPTION_SECONDARY_CACHE_KEY"></span><span id="internet_option_secondary_cache_key"></span>**\_chave de \_ \_ cache secundária de opção \_ de Internet**</span><span class="sxs-lookup"><span data-stu-id="38db0-543"><span id="INTERNET_OPTION_SECONDARY_CACHE_KEY"></span><span id="internet_option_secondary_cache_key"></span>**INTERNET\_OPTION\_SECONDARY\_CACHE\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-544">53</span><span class="sxs-lookup"><span data-stu-id="38db0-544">53</span></span>
</dt> <dt>



<span data-ttu-id="38db0-545">Define ou recupera um valor de cadeia de caracteres que contém a chave de cache secundária.</span><span class="sxs-lookup"><span data-stu-id="38db0-545">Sets or retrieves a string value that contains the secondary cache key.</span></span> <span data-ttu-id="38db0-546">Isso é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-546">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="38db0-547">Esta opção é reservada somente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="38db0-547">This option is reserved for internal use only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-548"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE"></span><span id="internet_option_security_certificate"></span>**\_certificado de \_ segurança de opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-548"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE"></span><span id="internet_option_security_certificate"></span>**INTERNET\_OPTION\_SECURITY\_CERTIFICATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-549">35</span><span class="sxs-lookup"><span data-stu-id="38db0-549">35</span></span>
</dt> <dt>



<span data-ttu-id="38db0-550">Recupera o certificado para um servidor SSL/PCT (protocolo SSL/tecnologia de comunicação privada) em uma cadeia de caracteres formatada.</span><span class="sxs-lookup"><span data-stu-id="38db0-550">Retrieves the certificate for an SSL/PCT (Secure Sockets Layer/Private Communications Technology) server into a formatted string.</span></span> <span data-ttu-id="38db0-551">Isso é usado pelo [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-551">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-552"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="internet_option_security_certificate_struct"></span>**\_estrutura de \_ certificado de segurança de opção da Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-552"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="internet_option_security_certificate_struct"></span>**INTERNET\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-553">32</span><span class="sxs-lookup"><span data-stu-id="38db0-553">32</span></span>
</dt> <dt>



<span data-ttu-id="38db0-554">Recupera o certificado para um servidor SSL/PCT na estrutura de \_ informações do certificado de Internet \_ .</span><span class="sxs-lookup"><span data-stu-id="38db0-554">Retrieves the certificate for an SSL/PCT server into the INTERNET\_CERTIFICATE\_INFO structure.</span></span> <span data-ttu-id="38db0-555">Isso é usado pelo [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-555">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-556"><span id="INTERNET_OPTION_SECURITY_FLAGS"></span><span id="internet_option_security_flags"></span>**\_sinalizadores de \_ segurança de opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-556"><span id="INTERNET_OPTION_SECURITY_FLAGS"></span><span id="internet_option_security_flags"></span>**INTERNET\_OPTION\_SECURITY\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-557">31</span><span class="sxs-lookup"><span data-stu-id="38db0-557">31</span></span>
</dt> <dt>



<span data-ttu-id="38db0-558">Recupera um valor inteiro longo sem sinal que contém os sinalizadores de segurança para um identificador.</span><span class="sxs-lookup"><span data-stu-id="38db0-558">Retrieves an unsigned long integer value that contains the security flags for a handle.</span></span> <span data-ttu-id="38db0-559">Essa opção é usada pelo [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-559">This option is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="38db0-560">Pode ser uma combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="38db0-560">It can be a combination of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="38db0-561"><span id="SECURITY_FLAG_128BIT"></span><span id="security_flag_128bit"></span>Sinalizador de segurança \_ \_ 128bit</span><span class="sxs-lookup"><span data-stu-id="38db0-561"><span id="SECURITY_FLAG_128BIT"></span><span id="security_flag_128bit"></span>SECURITY\_FLAG\_128BIT</span></span>
</dt> <dd>

<span data-ttu-id="38db0-562">0x20000000</span><span class="sxs-lookup"><span data-stu-id="38db0-562">0x20000000</span></span>

<span data-ttu-id="38db0-563">Idêntico ao valor preferencial de [intensidade de sinalizador de segurança \_ \_ \_ forte](/windows).</span><span class="sxs-lookup"><span data-stu-id="38db0-563">Identical to the preferred value [SECURITY\_FLAG\_STRENGTH\_STRONG](/windows).</span></span> <span data-ttu-id="38db0-564">Isso só é retornado em uma chamada para [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-564">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="38db0-565"><span id="SECURITY_FLAG_40BIT"></span><span id="security_flag_40bit"></span>Sinalizador de segurança \_ \_ 40BIT</span><span class="sxs-lookup"><span data-stu-id="38db0-565"><span id="SECURITY_FLAG_40BIT"></span><span id="security_flag_40bit"></span>SECURITY\_FLAG\_40BIT</span></span>
</dt> <dd>

<span data-ttu-id="38db0-566">0x10000000</span><span class="sxs-lookup"><span data-stu-id="38db0-566">0x10000000</span></span>

<span data-ttu-id="38db0-567">Idêntico à intensidade de sinalizador de segurança de valor preferencial [ \_ \_ \_ fraca](/windows).</span><span class="sxs-lookup"><span data-stu-id="38db0-567">Identical to the preferred value [SECURITY\_FLAG\_STRENGTH\_WEAK](/windows).</span></span> <span data-ttu-id="38db0-568">Isso só é retornado em uma chamada para [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-568">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="38db0-569"><span id="SECURITY_FLAG_56BIT"></span><span id="security_flag_56bit"></span>Sinalizador de segurança \_ \_ 56BIT</span><span class="sxs-lookup"><span data-stu-id="38db0-569"><span id="SECURITY_FLAG_56BIT"></span><span id="security_flag_56bit"></span>SECURITY\_FLAG\_56BIT</span></span>
</dt> <dd>

<span data-ttu-id="38db0-570">0x40000000</span><span class="sxs-lookup"><span data-stu-id="38db0-570">0x40000000</span></span>

<span data-ttu-id="38db0-571">Idêntico ao valor preferido de [ \_ intensidade de \_ sinalizador \_ de segurança](/windows).</span><span class="sxs-lookup"><span data-stu-id="38db0-571">Identical to the preferred value [SECURITY\_FLAG\_STRENGTH\_MEDIUM](/windows).</span></span> <span data-ttu-id="38db0-572">Isso só é retornado em uma chamada para [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-572">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="38db0-573"><span id="SECURITY_FLAG_FORTEZZA"></span><span id="security_flag_fortezza"></span>sinalizador de segurança \_ \_ Fortezza</span><span class="sxs-lookup"><span data-stu-id="38db0-573"><span id="SECURITY_FLAG_FORTEZZA"></span><span id="security_flag_fortezza"></span>SECURITY\_FLAG\_FORTEZZA</span></span>
</dt> <dd>

<span data-ttu-id="38db0-574">0x08000000</span><span class="sxs-lookup"><span data-stu-id="38db0-574">0x08000000</span></span>

<span data-ttu-id="38db0-575">Indica que o Fortezza foi usado para fornecer sigilo, autenticação e/ou integridade para a conexão especificada.</span><span class="sxs-lookup"><span data-stu-id="38db0-575">Indicates Fortezza has been used to provide secrecy, authentication, and/or integrity for the specified connection.</span></span>

</dd> <dt>

<span data-ttu-id="38db0-576"><span id="SECURITY_FLAG_IETFSSL4"></span><span id="security_flag_ietfssl4"></span>Sinalizador de segurança \_ \_ IETFSSL4</span><span class="sxs-lookup"><span data-stu-id="38db0-576"><span id="SECURITY_FLAG_IETFSSL4"></span><span id="security_flag_ietfssl4"></span>SECURITY\_FLAG\_IETFSSL4</span></span>
</dt> <dd>

<span data-ttu-id="38db0-577">0x00000020</span><span class="sxs-lookup"><span data-stu-id="38db0-577">0x00000020</span></span>

<span data-ttu-id="38db0-578">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="38db0-578">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="38db0-579"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>sinalizador de segurança \_ \_ ignorar \_ certificado \_ CN \_ inválido</span><span class="sxs-lookup"><span data-stu-id="38db0-579"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_CN\_INVALID</span></span>
</dt> <dd>

<span data-ttu-id="38db0-580">0x00001000</span><span class="sxs-lookup"><span data-stu-id="38db0-580">0x00001000</span></span>

<span data-ttu-id="38db0-581">Ignora a mensagem de erro [ \_ CN de certificado da Internet \_ SEC \_ \_ \_ inválida](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="38db0-581">Ignores the [ERROR\_INTERNET\_SEC\_CERT\_CN\_INVALID](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="38db0-582"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>sinalizador de segurança \_ \_ ignorar \_ data de certificado \_ \_ inválida</span><span class="sxs-lookup"><span data-stu-id="38db0-582"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_DATE\_INVALID</span></span>
</dt> <dd>

<span data-ttu-id="38db0-583">0x00002000</span><span class="sxs-lookup"><span data-stu-id="38db0-583">0x00002000</span></span>

<span data-ttu-id="38db0-584">Ignora a mensagem de erro [inválido da data de \_ certificado da Internet \_ SEC \_ \_ \_ ](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="38db0-584">Ignores the [ERROR\_INTERNET\_SEC\_CERT\_DATE\_INVALID](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="38db0-585"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="security_flag_ignore_redirect_to_http"></span>\_sinalizador \_ de segurança ignorar \_ redirecionamento \_ para \_ http</span><span class="sxs-lookup"><span data-stu-id="38db0-585"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="security_flag_ignore_redirect_to_http"></span>SECURITY\_FLAG\_IGNORE\_REDIRECT\_TO\_HTTP</span></span>
</dt> <dd>

<span data-ttu-id="38db0-586">0x00008000</span><span class="sxs-lookup"><span data-stu-id="38db0-586">0x00008000</span></span>

<span data-ttu-id="38db0-587">Ignora o [erro \_ Internet \_ https \_ para \_ http na mensagem de erro \_ do \_ REDIR](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="38db0-587">Ignores the [ERROR\_INTERNET\_HTTPS\_TO\_HTTP\_ON\_REDIR](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="38db0-588"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="security_flag_ignore_redirect_to_https"></span>\_sinalizador \_ de segurança ignorar \_ redirecionamento \_ para \_ https</span><span class="sxs-lookup"><span data-stu-id="38db0-588"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="security_flag_ignore_redirect_to_https"></span>SECURITY\_FLAG\_IGNORE\_REDIRECT\_TO\_HTTPS</span></span>
</dt> <dd>

<span data-ttu-id="38db0-589">0x00004000</span><span class="sxs-lookup"><span data-stu-id="38db0-589">0x00004000</span></span>

<span data-ttu-id="38db0-590">Ignora o [erro \_ Internet \_ http \_ para \_ https na mensagem de erro \_ \_ REDIR](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="38db0-590">Ignores the [ERROR\_INTERNET\_HTTP\_TO\_HTTPS\_ON\_REDIR](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="38db0-591"><span id="SECURITY_FLAG_IGNORE_REVOCATION"></span><span id="security_flag_ignore_revocation"></span>sinalizador de segurança \_ \_ ignorar \_ revogação</span><span class="sxs-lookup"><span data-stu-id="38db0-591"><span id="SECURITY_FLAG_IGNORE_REVOCATION"></span><span id="security_flag_ignore_revocation"></span>SECURITY\_FLAG\_IGNORE\_REVOCATION</span></span>
</dt> <dd>

<span data-ttu-id="38db0-592">0x00000080</span><span class="sxs-lookup"><span data-stu-id="38db0-592">0x00000080</span></span>

<span data-ttu-id="38db0-593">Ignora os problemas de revogação de certificado.</span><span class="sxs-lookup"><span data-stu-id="38db0-593">Ignores certificate revocation problems.</span></span>

</dd> <dt>

<span data-ttu-id="38db0-594"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>sinalizador de segurança \_ \_ ignorar \_ \_ AC desconhecida</span><span class="sxs-lookup"><span data-stu-id="38db0-594"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SECURITY\_FLAG\_IGNORE\_UNKNOWN\_CA</span></span>
</dt> <dd>

<span data-ttu-id="38db0-595">0x00000100</span><span class="sxs-lookup"><span data-stu-id="38db0-595">0x00000100</span></span>

<span data-ttu-id="38db0-596">Ignora problemas de autoridade de certificação desconhecida.</span><span class="sxs-lookup"><span data-stu-id="38db0-596">Ignores unknown certificate authority problems.</span></span>

</dd> <dt>

<span data-ttu-id="38db0-597"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>sinalizador de segurança \_ \_ ignorar \_ \_ assinatura fraca</span><span class="sxs-lookup"><span data-stu-id="38db0-597"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SECURITY\_FLAG\_IGNORE\_WEAK\_SIGNATURE</span></span>
</dt> <dd>

<span data-ttu-id="38db0-598">0x00010000</span><span class="sxs-lookup"><span data-stu-id="38db0-598">0x00010000</span></span>

<span data-ttu-id="38db0-599">Ignora problemas de assinatura de certificado fraco.</span><span class="sxs-lookup"><span data-stu-id="38db0-599">Ignores weak certificate signature problems.</span></span>

</dd> <dt>

<span data-ttu-id="38db0-600"><span id="SECURITY_FLAG_IGNORE_WRONG_USAGE"></span><span id="security_flag_ignore_wrong_usage"></span>sinalizador de segurança \_ \_ ignorar \_ \_ uso errado</span><span class="sxs-lookup"><span data-stu-id="38db0-600"><span id="SECURITY_FLAG_IGNORE_WRONG_USAGE"></span><span id="security_flag_ignore_wrong_usage"></span>SECURITY\_FLAG\_IGNORE\_WRONG\_USAGE</span></span>
</dt> <dd>

<span data-ttu-id="38db0-601">0x00000200</span><span class="sxs-lookup"><span data-stu-id="38db0-601">0x00000200</span></span>

<span data-ttu-id="38db0-602">Ignora problemas de uso incorretos.</span><span class="sxs-lookup"><span data-stu-id="38db0-602">Ignores incorrect usage problems.</span></span>

</dd> <dt>

<span data-ttu-id="38db0-603"><span id="SECURITY_FLAG_NORMALBITNESS"></span><span id="security_flag_normalbitness"></span>sinalizador de segurança \_ \_ NORMALBITNESS</span><span class="sxs-lookup"><span data-stu-id="38db0-603"><span id="SECURITY_FLAG_NORMALBITNESS"></span><span id="security_flag_normalbitness"></span>SECURITY\_FLAG\_NORMALBITNESS</span></span>
</dt> <dd>

<span data-ttu-id="38db0-604">0x10000000</span><span class="sxs-lookup"><span data-stu-id="38db0-604">0x10000000</span></span>

<span data-ttu-id="38db0-605">É idêntico ao valor [da \_ intensidade do sinalizador de segurança \_ \_ fraco](/windows).</span><span class="sxs-lookup"><span data-stu-id="38db0-605">Identical to the value [SECURITY\_FLAG\_STRENGTH\_WEAK](/windows).</span></span> <span data-ttu-id="38db0-606">Isso só é retornado em uma chamada para [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-606">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="38db0-607"><span id="SECURITY_FLAG_PCT"></span><span id="security_flag_pct"></span>sinalizador de segurança \_ \_ PCT</span><span class="sxs-lookup"><span data-stu-id="38db0-607"><span id="SECURITY_FLAG_PCT"></span><span id="security_flag_pct"></span>SECURITY\_FLAG\_PCT</span></span>
</dt> <dd>

<span data-ttu-id="38db0-608">0x00000008</span><span class="sxs-lookup"><span data-stu-id="38db0-608">0x00000008</span></span>

<span data-ttu-id="38db0-609">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="38db0-609">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="38db0-610"><span id="SECURITY_FLAG_PCT4"></span><span id="security_flag_pct4"></span>Sinalizador de segurança \_ \_ PCT4</span><span class="sxs-lookup"><span data-stu-id="38db0-610"><span id="SECURITY_FLAG_PCT4"></span><span id="security_flag_pct4"></span>SECURITY\_FLAG\_PCT4</span></span>
</dt> <dd>

<span data-ttu-id="38db0-611">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38db0-611">0x00000010</span></span>

<span data-ttu-id="38db0-612">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="38db0-612">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="38db0-613"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>sinalizador de segurança \_ \_ seguro</span><span class="sxs-lookup"><span data-stu-id="38db0-613"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SECURITY\_FLAG\_SECURE</span></span>
</dt> <dd>

<span data-ttu-id="38db0-614">0x00000001</span><span class="sxs-lookup"><span data-stu-id="38db0-614">0x00000001</span></span>

<span data-ttu-id="38db0-615">Usa transferências seguras.</span><span class="sxs-lookup"><span data-stu-id="38db0-615">Uses secure transfers.</span></span> <span data-ttu-id="38db0-616">Isso só é retornado em uma chamada para [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-616">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="38db0-617"><span id="SECURITY_FLAG_SSL"></span><span id="security_flag_ssl"></span>sinalizador de segurança \_ \_ SSL</span><span class="sxs-lookup"><span data-stu-id="38db0-617"><span id="SECURITY_FLAG_SSL"></span><span id="security_flag_ssl"></span>SECURITY\_FLAG\_SSL</span></span>
</dt> <dd>

<span data-ttu-id="38db0-618">0x00000002</span><span class="sxs-lookup"><span data-stu-id="38db0-618">0x00000002</span></span>

<span data-ttu-id="38db0-619">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="38db0-619">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="38db0-620"><span id="SECURITY_FLAG_SSL3"></span><span id="security_flag_ssl3"></span>Sinalizador de segurança \_ \_ SSL3</span><span class="sxs-lookup"><span data-stu-id="38db0-620"><span id="SECURITY_FLAG_SSL3"></span><span id="security_flag_ssl3"></span>SECURITY\_FLAG\_SSL3</span></span>
</dt> <dd>

<span data-ttu-id="38db0-621">0x00000004</span><span class="sxs-lookup"><span data-stu-id="38db0-621">0x00000004</span></span>

<span data-ttu-id="38db0-622">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="38db0-622">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="38db0-623"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>\_ \_ nível médio do sinalizador de segurança \_</span><span class="sxs-lookup"><span data-stu-id="38db0-623"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>SECURITY\_FLAG\_STRENGTH\_MEDIUM</span></span>
</dt> <dd>

<span data-ttu-id="38db0-624">0x40000000</span><span class="sxs-lookup"><span data-stu-id="38db0-624">0x40000000</span></span>

<span data-ttu-id="38db0-625">Usa a criptografia média (56 bits).</span><span class="sxs-lookup"><span data-stu-id="38db0-625">Uses medium (56-bit) encryption.</span></span> <span data-ttu-id="38db0-626">Isso só é retornado em uma chamada para [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-626">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="38db0-627"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>\_ \_ forte força do sinalizador de segurança \_</span><span class="sxs-lookup"><span data-stu-id="38db0-627"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SECURITY\_FLAG\_STRENGTH\_STRONG</span></span>
</dt> <dd>

<span data-ttu-id="38db0-628">0x20000000</span><span class="sxs-lookup"><span data-stu-id="38db0-628">0x20000000</span></span>

<span data-ttu-id="38db0-629">Usa criptografia forte (128 bits).</span><span class="sxs-lookup"><span data-stu-id="38db0-629">Uses strong (128-bit) encryption.</span></span> <span data-ttu-id="38db0-630">Isso só é retornado em uma chamada para [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-630">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="38db0-631"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>intensidade de sinalizador de segurança \_ \_ \_ fraca</span><span class="sxs-lookup"><span data-stu-id="38db0-631"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SECURITY\_FLAG\_STRENGTH\_WEAK</span></span>
</dt> <dd>

<span data-ttu-id="38db0-632">0x10000000</span><span class="sxs-lookup"><span data-stu-id="38db0-632">0x10000000</span></span>

<span data-ttu-id="38db0-633">Usa criptografia fraca (40 bits).</span><span class="sxs-lookup"><span data-stu-id="38db0-633">Uses weak (40-bit) encryption.</span></span> <span data-ttu-id="38db0-634">Isso só é retornado em uma chamada para [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-634">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="38db0-635"><span id="SECURITY_FLAG_UNKNOWNBIT"></span><span id="security_flag_unknownbit"></span>sinalizador de segurança \_ \_ UNKNOWNBIT</span><span class="sxs-lookup"><span data-stu-id="38db0-635"><span id="SECURITY_FLAG_UNKNOWNBIT"></span><span id="security_flag_unknownbit"></span>SECURITY\_FLAG\_UNKNOWNBIT</span></span>
</dt> <dd>

<span data-ttu-id="38db0-636">0x80000000</span><span class="sxs-lookup"><span data-stu-id="38db0-636">0x80000000</span></span>

<span data-ttu-id="38db0-637">O tamanho de bit usado na criptografia é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="38db0-637">The bit size used in the encryption is unknown.</span></span> <span data-ttu-id="38db0-638">Isso só é retornado em uma chamada para [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-638">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> </dl>

<span data-ttu-id="38db0-639">Lembre-se de que os dados recuperados dessa forma estão relacionados a uma transação que ocorreu, cujo nível de segurança não pode mais ser alterado.</span><span class="sxs-lookup"><span data-stu-id="38db0-639">Be aware that the data retrieved this way relates to a transaction that has occurred, whose security level can no longer be changed.</span></span>

</dl> </dd> <dt>

<span data-ttu-id="38db0-640"><span id="INTERNET_OPTION_SECURITY_KEY_BITNESS"></span><span id="internet_option_security_key_bitness"></span>**\_chave de \_ segurança da opção \_ de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-640"><span id="INTERNET_OPTION_SECURITY_KEY_BITNESS"></span><span id="internet_option_security_key_bitness"></span>**INTERNET\_OPTION\_SECURITY\_KEY\_BITNESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-641">36</span><span class="sxs-lookup"><span data-stu-id="38db0-641">36</span></span>
</dt> <dt>



<span data-ttu-id="38db0-642">Recupera um valor inteiro longo sem sinal que contém o tamanho do bit da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="38db0-642">Retrieves an unsigned long integer value that contains the bit size of the encryption key.</span></span> <span data-ttu-id="38db0-643">Quanto maior o número, maior a intensidade de criptografia usada.</span><span class="sxs-lookup"><span data-stu-id="38db0-643">The larger the number, the greater the encryption strength used.</span></span> <span data-ttu-id="38db0-644">Isso é usado pelo [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-644">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="38db0-645">Lembre-se de que os dados recuperados dessa forma estão relacionados a uma transação que já ocorreu, cujo nível de segurança não pode mais ser alterado.</span><span class="sxs-lookup"><span data-stu-id="38db0-645">Be aware that the data retrieved this way relates to a transaction that has already occurred, whose security level can no longer be changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-646"><span id="INTERNET_OPTION_SEND_THROUGHPUT"></span><span id="internet_option_send_throughput"></span>**\_taxa de \_ transferência de envio de opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-646"><span id="INTERNET_OPTION_SEND_THROUGHPUT"></span><span id="internet_option_send_throughput"></span>**INTERNET\_OPTION\_SEND\_THROUGHPUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-647">56</span><span class="sxs-lookup"><span data-stu-id="38db0-647">56</span></span>
</dt> <dt>



<span data-ttu-id="38db0-648">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="38db0-648">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-649"><span id="INTERNET_OPTION_SEND_TIMEOUT"></span><span id="internet_option_send_timeout"></span>**\_ \_ tempo limite de envio de opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-649"><span id="INTERNET_OPTION_SEND_TIMEOUT"></span><span id="internet_option_send_timeout"></span>**INTERNET\_OPTION\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-650">5</span><span class="sxs-lookup"><span data-stu-id="38db0-650">5</span></span>
</dt> <dt>



<span data-ttu-id="38db0-651">Define ou recupera um valor inteiro longo sem sinal, em milissegundos, que contém o valor de tempo limite para enviar uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="38db0-651">Sets or retrieves an unsigned long integer value, in milliseconds, that contains the time-out value to send a request.</span></span> <span data-ttu-id="38db0-652">Se o envio demorar mais do que esse valor de tempo limite, o envio será cancelado.</span><span class="sxs-lookup"><span data-stu-id="38db0-652">If the send takes longer than this time-out value, the send is canceled.</span></span> <span data-ttu-id="38db0-653">Essa opção pode ser usada em qualquer identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) , incluindo um identificador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="38db0-653">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="38db0-654">Ele é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-654">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="38db0-655">Quando usado em referência a uma transação de FTP, essa opção se refere ao canal de controle.</span><span class="sxs-lookup"><span data-stu-id="38db0-655">When used in reference to an FTP transaction, this option refers to the control channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-656"><span id="INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="internet_option_server_cert_chain_context"></span>**\_contexto da \_ cadeia de certificados do servidor de opção da \_ \_ Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-656"><span id="INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="internet_option_server_cert_chain_context"></span>**INTERNET\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-657">105</span><span class="sxs-lookup"><span data-stu-id="38db0-657">105</span></span>
</dt> <dt>



<span data-ttu-id="38db0-658">Recupera o contexto de cadeia de certificados do servidor como um [contexto de \_ cadeia \_ de PCCERT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context)duplicado.</span><span class="sxs-lookup"><span data-stu-id="38db0-658">Retrieves the server s certificate-chain context as a duplicated [PCCERT\_CHAIN\_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context).</span></span> <span data-ttu-id="38db0-659">Você pode passar esse contexto duplicado para qualquer função de API de criptografia que usa um [ \_ \_ contexto de cadeia de PCCERT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context).</span><span class="sxs-lookup"><span data-stu-id="38db0-659">You may pass this duplicated context to any Crypto API function which takes a [PCCERT\_CHAIN\_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context).</span></span> <span data-ttu-id="38db0-660">Você deve chamar [**CertFreeCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatechain) no [ \_ \_ contexto da cadeia de PCCERT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) retornado quando terminar com o contexto da cadeia de certificados.</span><span class="sxs-lookup"><span data-stu-id="38db0-660">You must call [**CertFreeCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatechain) on the returned [PCCERT\_CHAIN\_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) when you are done with the certificate-chain context.</span></span>

<span data-ttu-id="38db0-661">**Versão:** Requer o Internet Explorer 8,0.</span><span class="sxs-lookup"><span data-stu-id="38db0-661">**Version:** Requires Internet Explorer 8.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-662"><span id="INTERNET_OPTION_SETTINGS_CHANGED"></span><span id="internet_option_settings_changed"></span>**configurações de opção da INTERNET \_ \_ \_ alteradas**</span><span class="sxs-lookup"><span data-stu-id="38db0-662"><span id="INTERNET_OPTION_SETTINGS_CHANGED"></span><span id="internet_option_settings_changed"></span>**INTERNET\_OPTION\_SETTINGS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-663">39</span><span class="sxs-lookup"><span data-stu-id="38db0-663">39</span></span>
</dt> <dt>



<span data-ttu-id="38db0-664">Notifica o sistema de que as configurações do registro foram alteradas para que ele verifique as configurações na próxima chamada para [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="38db0-664">Notifies the system that the registry settings have been changed so that it verifies the settings on the next call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="38db0-665">Isso é usado por [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-665">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-666"><span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**opção de INTERNET \_ \_ suprimir \_ autenticação de servidor \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-666"><span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**INTERNET\_OPTION\_SUPPRESS\_SERVER\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-667">104</span><span class="sxs-lookup"><span data-stu-id="38db0-667">104</span></span>
</dt> <dt>



<span data-ttu-id="38db0-668">Define um objeto de solicitação HTTP de modo que ele não fará logon nos servidores de origem, mas executará o logon automático em servidores proxy HTTP.</span><span class="sxs-lookup"><span data-stu-id="38db0-668">Sets an HTTP request object such that it will not logon to origin servers, but will perform automatic logon to HTTP proxy servers.</span></span> <span data-ttu-id="38db0-669">Essa opção é diferente do sinalizador de solicitação **da \_ Internet \_ sem \_ autenticação**, o que impede a autenticação tanto nos servidores proxy quanto nos servidores de origem.</span><span class="sxs-lookup"><span data-stu-id="38db0-669">This option differs from the Request flag **INTERNET\_FLAG\_NO\_AUTH**, which prevents authentication to both proxy servers and origin servers.</span></span>

<span data-ttu-id="38db0-670">Definir esse modo irá suprimir o uso de qualquer material de credencial (anteriormente fornecido nome de usuário/senha ou certificado SSL de cliente) ao se comunicar com um servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="38db0-670">Setting this mode will suppress the use of any credential material (either previously provided username/password or client SSL certificate) when communicating with an origin server.</span></span> <span data-ttu-id="38db0-671">No entanto, se a solicitação precisar transitar por meio de um proxy de autenticação, o WinINet ainda executará a autenticação automática para o proxy HTTP de acordo com as configurações de zona da intranet do usuário.</span><span class="sxs-lookup"><span data-stu-id="38db0-671">However, if the request must transit via an authenticating proxy, WinINet will still perform automatic authentication to the HTTP proxy per the Intranet Zone settings for the user.</span></span> <span data-ttu-id="38db0-672">A configuração de zona da intranet padrão é permitir o logon automático usando as credenciais padrão do usuário.</span><span class="sxs-lookup"><span data-stu-id="38db0-672">The default Intranet Zone setting is to permit automatic logon using the user s default credentials.</span></span>

<span data-ttu-id="38db0-673">Para garantir a supressão de todas as informações de identificação, o chamador deve combinar a **opção da Internet \_ \_ suprimir a \_ \_ autenticação do servidor** com o sinalizador Internet sem sinalizador de solicitação de **\_ \_ \_ cookies** .</span><span class="sxs-lookup"><span data-stu-id="38db0-673">To ensure suppression of all identifying information, the caller should combine **INTERNET\_OPTION\_SUPPRESS\_SERVER\_AUTH** with the **INTERNET\_FLAG\_NO\_COOKIES** request flag.</span></span>

<span data-ttu-id="38db0-674">Essa opção só pode ser definida em objetos de solicitação antes de serem enviadas.</span><span class="sxs-lookup"><span data-stu-id="38db0-674">This option may only be set on request objects before they have been sent.</span></span> <span data-ttu-id="38db0-675">As tentativas de definir essa opção após a solicitação ter sido enviada retornarão um **\_ \_ \_ \_ estado de identificador incorreto da Internet**.</span><span class="sxs-lookup"><span data-stu-id="38db0-675">Attempts to set this option after the request has been sent will return **ERROR\_INTERNET\_INCORRECT\_HANDLE\_STATE**.</span></span>

<span data-ttu-id="38db0-676">Nenhum buffer é necessário para essa opção.</span><span class="sxs-lookup"><span data-stu-id="38db0-676">No buffer is required for this option.</span></span> <span data-ttu-id="38db0-677">Isso é usado por [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) em identificadores retornados apenas por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .</span><span class="sxs-lookup"><span data-stu-id="38db0-677">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) on handles returned by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) only.</span></span>

<span data-ttu-id="38db0-678">**Versão:** Requer o Internet Explorer 8,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="38db0-678">**Version:** Requires Internet Explorer 8.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-679"><span id="INTERNET_OPTION_SUPPRESS_BEHAVIOR"></span><span id="internet_option_suppress_behavior"></span>**\_comportamento de \_ supressão de opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-679"><span id="INTERNET_OPTION_SUPPRESS_BEHAVIOR"></span><span id="internet_option_suppress_behavior"></span>**INTERNET\_OPTION\_SUPPRESS\_BEHAVIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-680">81</span><span class="sxs-lookup"><span data-stu-id="38db0-680">81</span></span>
</dt> <dt>



<span data-ttu-id="38db0-681">Uma opção de uso geral que é usada para suprimir comportamentos em todo o processo.</span><span class="sxs-lookup"><span data-stu-id="38db0-681">A general purpose option that is used to suppress behaviors on a process-wide basis.</span></span> <span data-ttu-id="38db0-682">O parâmetro *lpBuffer* da função deve ser um ponteiro para um DWORD que contém o comportamento específico a ser suprimido.</span><span class="sxs-lookup"><span data-stu-id="38db0-682">The *lpBuffer* parameter of the function must be a pointer to a DWORD containing the specific behavior to suppress.</span></span> <span data-ttu-id="38db0-683">Esta opção não pode ser consultada com [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-683">This option cannot be queried with [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="38db0-684">Os valores permitidos são:</span><span class="sxs-lookup"><span data-stu-id="38db0-684">The permitted values are:</span></span>

<dl> <dt>

<span data-ttu-id="38db0-685"><span id="INTERNET_SUPPRESS_RESET_ALL"></span><span id="internet_suppress_reset_all"></span>\_suprimir \_ redefinição de Internet \_</span><span class="sxs-lookup"><span data-stu-id="38db0-685"><span id="INTERNET_SUPPRESS_RESET_ALL"></span><span id="internet_suppress_reset_all"></span>INTERNET\_SUPPRESS\_RESET\_ALL</span></span>
</dt> <dd>

<span data-ttu-id="38db0-686">0</span><span class="sxs-lookup"><span data-stu-id="38db0-686">0</span></span>

<span data-ttu-id="38db0-687">Desabilita todas as supressões, habilitando novamente o comportamento padrão e configurado.</span><span class="sxs-lookup"><span data-stu-id="38db0-687">Disables all suppressions, re-enabling default and configured behavior.</span></span> <span data-ttu-id="38db0-688">Essa opção é equivalente a configurar a política de supressão de cookies de Internet e a redefinição de **\_ \_ \_ \_ diretiva** de **supressão de \_ \_ cookies \_ \_ da Internet** .</span><span class="sxs-lookup"><span data-stu-id="38db0-688">This option is the equivalent of setting **INTERNET\_SUPPRESS\_COOKIE\_POLICY\_RESET** and **INTERNET\_SUPPRESS\_COOKIE\_PERSIST\_RESET** individually.</span></span>

<span data-ttu-id="38db0-689">**Versão:** Requer o Internet Explorer 6,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="38db0-689">**Version:** Requires Internet Explorer 6.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="38db0-690"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_"></span><span id="internet_suppress_cookie_policy_"></span>\_política de supressão de \_ Cookie da Internet \_</span><span class="sxs-lookup"><span data-stu-id="38db0-690"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_"></span><span id="internet_suppress_cookie_policy_"></span>INTERNET\_SUPPRESS\_COOKIE\_POLICY</span></span> 
</dt> <dd>

<span data-ttu-id="38db0-691">1</span><span class="sxs-lookup"><span data-stu-id="38db0-691">1</span></span>

<span data-ttu-id="38db0-692">Ignora todas as políticas de cookie configuradas e permite que os cookies sejam definidos.</span><span class="sxs-lookup"><span data-stu-id="38db0-692">Ignores any configured cookie policies and allows cookies to be set.</span></span>

<span data-ttu-id="38db0-693">**Versão:** Requer o Internet Explorer 6,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="38db0-693">**Version:** Requires Internet Explorer 6.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="38db0-694"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_RESET_"></span><span id="internet_suppress_cookie_policy_reset_"></span>redefinição de política de cookies de \_ supressão da Internet \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="38db0-694"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_RESET_"></span><span id="internet_suppress_cookie_policy_reset_"></span>INTERNET\_SUPPRESS\_COOKIE\_POLICY\_RESET</span></span> 
</dt> <dd>

<span data-ttu-id="38db0-695">2</span><span class="sxs-lookup"><span data-stu-id="38db0-695">2</span></span>

<span data-ttu-id="38db0-696">Desabilita a supressão da **\_ política de \_ Cookie \_ de supressão da Internet** , permitindo a avaliação de cookies de acordo com a política de cookie configurada.</span><span class="sxs-lookup"><span data-stu-id="38db0-696">Disables the **INTERNET\_SUPPRESS\_COOKIE\_POLICY** suppression, permitting the evaluation of cookies according to the configured cookie policy.</span></span>

<span data-ttu-id="38db0-697">**Versão:** Requer o Internet Explorer 6,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="38db0-697">**Version:** Requires Internet Explorer 6.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="38db0-698"><span id="__INTERNET_SUPPRESS_COOKIE_PERSIST"></span><span id="__internet_suppress_cookie_persist"></span>\_persistência de supressão de \_ cookies pela Internet \_</span><span class="sxs-lookup"><span data-stu-id="38db0-698"><span id="__INTERNET_SUPPRESS_COOKIE_PERSIST"></span><span id="__internet_suppress_cookie_persist"></span> INTERNET\_SUPPRESS\_COOKIE\_PERSIST</span></span>
</dt> <dd>

<span data-ttu-id="38db0-699">3</span><span class="sxs-lookup"><span data-stu-id="38db0-699">3</span></span>

<span data-ttu-id="38db0-700">Suprime a persistência de cookies, mesmo que o servidor os tenha especificado como persistente.</span><span class="sxs-lookup"><span data-stu-id="38db0-700">Suppresses the persistence of cookies, even if the server has specified them as persistent.</span></span>

<span data-ttu-id="38db0-701">**Versão:** Requer o Internet Explorer 8,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="38db0-701">**Version:** Requires Internet Explorer 8.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="38db0-702"><span id="INTERNET_SUPPRESS_COOKIE_PERSIST_RESET"></span><span id="internet_suppress_cookie_persist_reset"></span>\_ignorar \_ \_ redefinição de persistência de cookies de Internet \_</span><span class="sxs-lookup"><span data-stu-id="38db0-702"><span id="INTERNET_SUPPRESS_COOKIE_PERSIST_RESET"></span><span id="internet_suppress_cookie_persist_reset"></span>INTERNET\_SUPPRESS\_COOKIE\_PERSIST\_RESET</span></span>
</dt> <dd>

<span data-ttu-id="38db0-703">4</span><span class="sxs-lookup"><span data-stu-id="38db0-703">4</span></span>

<span data-ttu-id="38db0-704">Desabilita a supressão de **\_ persistência do \_ Cookie \_ de supressão da Internet** , habilitando novamente a persistência de cookies.</span><span class="sxs-lookup"><span data-stu-id="38db0-704">Disables the **INTERNET\_SUPPRESS\_COOKIE\_PERSIST** suppression, re-enabling the persistence of cookies.</span></span> <span data-ttu-id="38db0-705">Todos os cookies suprimidos anteriormente não se tornarão persistentes.</span><span class="sxs-lookup"><span data-stu-id="38db0-705">Any previously suppressed cookies will not become persistent.</span></span>

<span data-ttu-id="38db0-706">**Versão:** Requer o Internet Explorer 8,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="38db0-706">**Version:** Requires Internet Explorer 8.0 or later.</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="38db0-707"><span id="INTERNET_OPTION_URL"></span><span id="internet_option_url"></span>**\_URL de opção de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-707"><span id="INTERNET_OPTION_URL"></span><span id="internet_option_url"></span>**INTERNET\_OPTION\_URL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-708">34</span><span class="sxs-lookup"><span data-stu-id="38db0-708">34</span></span>
</dt> <dt>



<span data-ttu-id="38db0-709">Recupera um valor de cadeia de caracteres que contém a URL completa de um recurso baixado.</span><span class="sxs-lookup"><span data-stu-id="38db0-709">Retrieves a string value that contains the full URL of a downloaded resource.</span></span> <span data-ttu-id="38db0-710">Se a URL original contiver dados adicionais, como cadeias de caracteres de pesquisa ou âncoras, ou se a chamada tiver sido redirecionada, a URL retornada será diferente da original.</span><span class="sxs-lookup"><span data-stu-id="38db0-710">If the original URL contained any extra data, such as search strings or anchors, or if the call was redirected, the URL returned differs from the original.</span></span> <span data-ttu-id="38db0-711">Essa opção é válida em identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) retornados por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="38db0-711">This option is valid on [**HINTERNET**](appendix-a-hinternet-handles.md) handles returned by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="38db0-712">Ele é usado pelo [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-712">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-713"><span id="INTERNET_OPTION_USER_AGENT"></span><span id="internet_option_user_agent"></span>**\_agente do \_ usuário de opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-713"><span id="INTERNET_OPTION_USER_AGENT"></span><span id="internet_option_user_agent"></span>**INTERNET\_OPTION\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-714">41</span><span class="sxs-lookup"><span data-stu-id="38db0-714">41</span></span>
</dt> <dt>



<span data-ttu-id="38db0-715">Define ou recupera a cadeia de caracteres do agente do usuário nos identificadores fornecidos pelo [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) e usado em funções subsequentes do [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) , desde que ele não seja substituído por um cabeçalho adicionado por [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) ou [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="38db0-715">Sets or retrieves the user agent string on handles supplied by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) and used in subsequent [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) functions, as long as it is not overridden by a header added by [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) or [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="38db0-716">Isso é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-716">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-717"><span id="INTERNET_OPTION_USERNAME"></span><span id="internet_option_username"></span>**nome de usuário da \_ opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-717"><span id="INTERNET_OPTION_USERNAME"></span><span id="internet_option_username"></span>**INTERNET\_OPTION\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-718">28</span><span class="sxs-lookup"><span data-stu-id="38db0-718">28</span></span>
</dt> <dt>



<span data-ttu-id="38db0-719">Define ou recupera uma cadeia de caracteres que contém o nome de usuário associado a um identificador retornado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="38db0-719">Sets or retrieves a string that contains the user name associated with a handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="38db0-720">Isso é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-720">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-721"><span id="INTERNET_OPTION_VERSION"></span><span id="internet_option_version"></span>**\_versão da opção da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-721"><span id="INTERNET_OPTION_VERSION"></span><span id="internet_option_version"></span>**INTERNET\_OPTION\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-722">40</span><span class="sxs-lookup"><span data-stu-id="38db0-722">40</span></span>
</dt> <dt>



<span data-ttu-id="38db0-723">Recupera uma estrutura de **\_ \_ informações de versão da Internet** que contém o número de versão de Wininet.dll.</span><span class="sxs-lookup"><span data-stu-id="38db0-723">Retrieves an **INTERNET\_VERSION\_INFO** structure that contains the version number of Wininet.dll.</span></span> <span data-ttu-id="38db0-724">Essa opção pode ser usada em um identificador [**HINTERNET**](appendix-a-hinternet-handles.md) **nulo** por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-724">This option can be used on a **NULL**[**HINTERNET**](appendix-a-hinternet-handles.md) handle by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38db0-725"><span id="INTERNET_OPTION_WRITE_BUFFER_SIZE"></span><span id="internet_option_write_buffer_size"></span>**\_tamanho do \_ buffer de gravação da opção da Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="38db0-725"><span id="INTERNET_OPTION_WRITE_BUFFER_SIZE"></span><span id="internet_option_write_buffer_size"></span>**INTERNET\_OPTION\_WRITE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38db0-726">13</span><span class="sxs-lookup"><span data-stu-id="38db0-726">13</span></span>
</dt> <dt>



<span data-ttu-id="38db0-727">Define ou recupera um valor inteiro longo sem sinal que contém o tamanho, em bytes, do buffer de gravação.</span><span class="sxs-lookup"><span data-stu-id="38db0-727">Sets or retrieves an unsigned long integer value that contains the size, in bytes, of the write buffer.</span></span> <span data-ttu-id="38db0-728">Essa opção pode ser usada em identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) retornados por [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) e [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (somente sessão de FTP).</span><span class="sxs-lookup"><span data-stu-id="38db0-728">This option can be used on [**HINTERNET**](appendix-a-hinternet-handles.md) handles returned by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (FTP session only).</span></span> <span data-ttu-id="38db0-729">Ele é usado por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) e [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="38db0-729">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38db0-730">Comentários</span><span class="sxs-lookup"><span data-stu-id="38db0-730">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="38db0-731">O WinINet não oferece suporte a implementações de servidor.</span><span class="sxs-lookup"><span data-stu-id="38db0-731">WinINet does not support server implementations.</span></span> <span data-ttu-id="38db0-732">Além disso, ele não deve ser usado de um serviço.</span><span class="sxs-lookup"><span data-stu-id="38db0-732">In addition, it should not be used from a service.</span></span> <span data-ttu-id="38db0-733">Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="38db0-733">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="38db0-734">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38db0-734">Requirements</span></span>



| <span data-ttu-id="38db0-735">Requisito</span><span class="sxs-lookup"><span data-stu-id="38db0-735">Requirement</span></span> | <span data-ttu-id="38db0-736">Valor</span><span class="sxs-lookup"><span data-stu-id="38db0-736">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38db0-737">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38db0-737">Minimum supported client</span></span><br/> | <span data-ttu-id="38db0-738">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="38db0-738">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                             |
| <span data-ttu-id="38db0-739">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38db0-739">Minimum supported server</span></span><br/> | <span data-ttu-id="38db0-740">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="38db0-740">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                   |
| <span data-ttu-id="38db0-741">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="38db0-741">Header</span></span><br/>                   | <dl> <span data-ttu-id="38db0-742"><dt>WinInet. h; </dt> <dt>Winineti. h</dt></span><span class="sxs-lookup"><span data-stu-id="38db0-742"><dt>Wininet.h; </dt> <dt>Winineti.h</dt></span></span> </dl> |



 

