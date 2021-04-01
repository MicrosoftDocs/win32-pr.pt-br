---
description: Os valores de erro identificados neste tópico são retornados por GetLastError quando uma das funções do Microsoft Windows HTTP Services (WinHTTP) falha.
ms.assetid: c8a863cd-d36c-4ec8-ac49-0b714a5e4cc2
title: Mensagens de erro (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eccdc8be4b1e7c3cc7f9a03403c2f8778ddd19b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828946"
---
# <a name="error-messages-winhttph"></a><span data-ttu-id="6a87d-103">Mensagens de erro (WinHTTP. h)</span><span class="sxs-lookup"><span data-stu-id="6a87d-103">Error Messages (Winhttp.h)</span></span>

<span data-ttu-id="6a87d-104">Os valores de erro listados abaixo são retornados por [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando uma das funções do Microsoft Windows http Services (WinHTTP) falha, e também são retornadas nos 16 bits inferiores do [**HRESULT**](../com/structure-of-com-error-codes.md) Error retornado do objeto [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="6a87d-104">The error values listed below are returned by [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) when one of the Microsoft Windows HTTP Services (WinHTTP) functions fails, and are also returned in the lower 16 bits of [**HRESULT**](../com/structure-of-com-error-codes.md) error returns from the [**WinHttpRequest**](winhttprequest.md) object.</span></span>

<span data-ttu-id="6a87d-105">Os valores de erro cujos nomes começam com "ERROR \_ WinHTTP \_ " são específicos para as funções de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="6a87d-105">Error values whose names begin with "ERROR\_WINHTTP\_" are specific to the WinHTTP functions.</span></span> <span data-ttu-id="6a87d-106">As funções WinHTTP também retornam mensagens de erro do Windows, quando apropriado.</span><span class="sxs-lookup"><span data-stu-id="6a87d-106">The WinHTTP functions also return Windows error messages where appropriate.</span></span>

<dl> <dt>

<span data-ttu-id="6a87d-107"><span id="ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR"></span><span id="error_winhttp_auto_proxy_service_error"></span>**ERRO \_ WinHTTP erro de \_ \_ serviço de proxy automático \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6a87d-107"><span id="ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR"></span><span id="error_winhttp_auto_proxy_service_error"></span>**ERROR\_WINHTTP\_AUTO\_PROXY\_SERVICE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-108">12178</span><span class="sxs-lookup"><span data-stu-id="6a87d-108">12178</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-109">Retornado por [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) quando um proxy para a URL especificada não pode ser localizado.</span><span class="sxs-lookup"><span data-stu-id="6a87d-109">Returned by [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) when a proxy for the specified URL cannot be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-110"><span id="ERROR_WINHTTP_AUTODETECTION_FAILED"></span><span id="error_winhttp_autodetection_failed"></span>**ERRO de detecção automática de \_ WinHTTP \_ \_ falhou**</span><span class="sxs-lookup"><span data-stu-id="6a87d-110"><span id="ERROR_WINHTTP_AUTODETECTION_FAILED"></span><span id="error_winhttp_autodetection_failed"></span>**ERROR\_WINHTTP\_AUTODETECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-111">12180</span><span class="sxs-lookup"><span data-stu-id="6a87d-111">12180</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-112">Retornado por [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) se o WinHTTP não puder descobrir a URL do Arquivo PAC (configuração automática de proxy).</span><span class="sxs-lookup"><span data-stu-id="6a87d-112">Returned by [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) if WinHTTP was unable to discover the URL of the Proxy Auto-Configuration (PAC) file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-113"><span id="ERROR_WINHTTP_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_winhttp_bad_auto_proxy_script"></span>**ERRO \_ WinHTTP \_ - \_ \_ script de proxy automático insatisfatório \_**</span><span class="sxs-lookup"><span data-stu-id="6a87d-113"><span id="ERROR_WINHTTP_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_winhttp_bad_auto_proxy_script"></span>**ERROR\_WINHTTP\_BAD\_AUTO\_PROXY\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-114">12166</span><span class="sxs-lookup"><span data-stu-id="6a87d-114">12166</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-115">Ocorreu um erro ao executar o código de script no arquivo PAC (configuração automática de proxy).</span><span class="sxs-lookup"><span data-stu-id="6a87d-115">An error occurred executing the script code in the Proxy Auto-Configuration (PAC) file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-116"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_OPEN"></span><span id="error_winhttp_cannot_call_after_open"></span>**ERRO \_ WinHTTP \_ não pode \_ chamar \_ após \_ abrir**</span><span class="sxs-lookup"><span data-stu-id="6a87d-116"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_OPEN"></span><span id="error_winhttp_cannot_call_after_open"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_AFTER\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-117">12103</span><span class="sxs-lookup"><span data-stu-id="6a87d-117">12103</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-118">Retornado pelo objeto [**HttpRequest**](winhttprequest.md) se uma opção especificada não puder ser solicitada depois que o método [**Open**](iwinhttprequest-open.md) tiver sido chamado.</span><span class="sxs-lookup"><span data-stu-id="6a87d-118">Returned by the [**HttpRequest**](winhttprequest.md) object if a specified option cannot be requested after the [**Open**](iwinhttprequest-open.md) method has been called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-119"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_SEND"></span><span id="error_winhttp_cannot_call_after_send"></span>**ERRO \_ WinHTTP \_ não pode \_ chamar \_ após \_ envio**</span><span class="sxs-lookup"><span data-stu-id="6a87d-119"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_SEND"></span><span id="error_winhttp_cannot_call_after_send"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_AFTER\_SEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-120">12102</span><span class="sxs-lookup"><span data-stu-id="6a87d-120">12102</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-121">Retornado pelo objeto [**HttpRequest**](winhttprequest.md) se uma operação solicitada não puder ser executada Depois de chamar o método [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="6a87d-121">Returned by the [**HttpRequest**](winhttprequest.md) object if a requested operation cannot be performed after calling the [**Send**](iwinhttprequest-send.md) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-122"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_OPEN"></span><span id="error_winhttp_cannot_call_before_open"></span>**ERRO \_ WinHTTP \_ não pode \_ chamar \_ antes de \_ abrir**</span><span class="sxs-lookup"><span data-stu-id="6a87d-122"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_OPEN"></span><span id="error_winhttp_cannot_call_before_open"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_BEFORE\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-123">12100</span><span class="sxs-lookup"><span data-stu-id="6a87d-123">12100</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-124">Retornado pelo objeto [**HttpRequest**](winhttprequest.md) se uma operação solicitada não puder ser executada antes de chamar o método [**Open**](iwinhttprequest-open.md) .</span><span class="sxs-lookup"><span data-stu-id="6a87d-124">Returned by the [**HttpRequest**](winhttprequest.md) object if a requested operation cannot be performed before calling the [**Open**](iwinhttprequest-open.md) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-125"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_SEND"></span><span id="error_winhttp_cannot_call_before_send"></span>**ERRO \_ WinHTTP \_ não pode \_ chamar \_ antes de \_ Enviar**</span><span class="sxs-lookup"><span data-stu-id="6a87d-125"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_SEND"></span><span id="error_winhttp_cannot_call_before_send"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_BEFORE\_SEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-126">12101</span><span class="sxs-lookup"><span data-stu-id="6a87d-126">12101</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-127">Retornado pelo objeto [**HttpRequest**](winhttprequest.md) se uma operação solicitada não puder ser executada antes de chamar o método [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="6a87d-127">Returned by the [**HttpRequest**](winhttprequest.md) object if a requested operation cannot be performed before calling the [**Send**](iwinhttprequest-send.md) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-128"><span id="ERROR_WINHTTP_CANNOT_CONNECT"></span><span id="error_winhttp_cannot_connect"></span>**ERRO \_ WinHTTP \_ não pode \_ conectar**</span><span class="sxs-lookup"><span data-stu-id="6a87d-128"><span id="ERROR_WINHTTP_CANNOT_CONNECT"></span><span id="error_winhttp_cannot_connect"></span>**ERROR\_WINHTTP\_CANNOT\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-129">12029</span><span class="sxs-lookup"><span data-stu-id="6a87d-129">12029</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-130">Retornado se a conexão com o servidor falhou.</span><span class="sxs-lookup"><span data-stu-id="6a87d-130">Returned if connection to the server failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-131"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERRO \_ de \_ certificado de autenticação de cliente WinHTTP \_ \_ \_ necessário**</span><span class="sxs-lookup"><span data-stu-id="6a87d-131"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a87d-132">O servidor requer autenticação de cliente SSL.</span><span class="sxs-lookup"><span data-stu-id="6a87d-132">The server requires SSL client Authentication.</span></span> <span data-ttu-id="6a87d-133">O aplicativo recupera a lista de emissores de certificado chamando [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) com a opção **WinHTTP lista de \_ emissor de \_ \_ certificado de \_ \_ cliente** .</span><span class="sxs-lookup"><span data-stu-id="6a87d-133">The application retrieves the list of certificate issuers by calling [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span> <span data-ttu-id="6a87d-134">Para obter mais informações, consulte **a \_ opção \_ WinHTTP \_ \_ \_ lista de emissor de certificado de cliente** .</span><span class="sxs-lookup"><span data-stu-id="6a87d-134">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>

<span data-ttu-id="6a87d-135">Se o servidor solicitar o certificado de cliente, mas não precisar dele, o aplicativo poderá chamar [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) alternadamente com a opção **WinHTTP de contexto de \_ \_ \_ certificado \_ de cliente** .</span><span class="sxs-lookup"><span data-stu-id="6a87d-135">If the server requests the client certificate, but does not require it, the application can alternately call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span> <span data-ttu-id="6a87d-136">Nesse caso, o aplicativo especifica a macro WINHTTP \_ no \_ \_ contexto de certificado do cliente \_ no parâmetro *lpBuffer* de **WinHttpSetOption**.</span><span class="sxs-lookup"><span data-stu-id="6a87d-136">In this case, the application specifies the WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT macro in the *lpBuffer* parameter of **WinHttpSetOption**.</span></span> <span data-ttu-id="6a87d-137">Para obter mais informações, consulte opção **WinHTTP de contexto de certificado de \_ \_ cliente \_ \_ de opção** .</span><span class="sxs-lookup"><span data-stu-id="6a87d-137">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span>

<span data-ttu-id="6a87d-138">**Windows Server 2003 com SP1 e Windows XP com SP2:** Não há suporte para esse erro.</span><span class="sxs-lookup"><span data-stu-id="6a87d-138">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-139"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_access_private_key"></span>**ERRO \_ WinHTTP \_ Client \_ CERT \_ sem \_ acesso \_ à \_ chave privada**</span><span class="sxs-lookup"><span data-stu-id="6a87d-139"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_access_private_key"></span>**ERROR\_WINHTTP\_CLIENT\_CERT\_NO\_ACCESS\_PRIVATE\_KEY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a87d-140">O aplicativo não tem os privilégios necessários para acessar a chave privada associada ao certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="6a87d-140">The application does not have the required privileges to access the private key associated with the client certificate.</span></span>

<span data-ttu-id="6a87d-141">**Windows Server 2003 com SP1 e Windows XP com SP2:** Não há suporte para esse erro.</span><span class="sxs-lookup"><span data-stu-id="6a87d-141">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-142"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_private_key"></span>**ERRO \_ WinHTTP \_ Client \_ CERT \_ sem \_ \_ chave privada**</span><span class="sxs-lookup"><span data-stu-id="6a87d-142"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_private_key"></span>**ERROR\_WINHTTP\_CLIENT\_CERT\_NO\_PRIVATE\_KEY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a87d-143">O contexto do certificado de cliente SSL não tem uma chave privada associada a ele.</span><span class="sxs-lookup"><span data-stu-id="6a87d-143">The context for the SSL client certificate does not have a private key associated with it.</span></span> <span data-ttu-id="6a87d-144">O certificado do cliente pode ter sido importado para o computador sem a chave privada.</span><span class="sxs-lookup"><span data-stu-id="6a87d-144">The client certificate may have been imported to the computer without the private key.</span></span>

<span data-ttu-id="6a87d-145">**Windows Server 2003 com SP1 e Windows XP com SP2:** Não há suporte para esse erro.</span><span class="sxs-lookup"><span data-stu-id="6a87d-145">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-146"><span id="ERROR_WINHTTP_CHUNKED_ENCODING_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_chunked_encoding_header_size_overflow"></span>**ERRO \_ WinHTTP de \_ tamanho do cabeçalho de codificação em partes \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6a87d-146"><span id="ERROR_WINHTTP_CHUNKED_ENCODING_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_chunked_encoding_header_size_overflow"></span>**ERROR\_WINHTTP\_CHUNKED\_ENCODING\_HEADER\_SIZE\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-147">12183</span><span class="sxs-lookup"><span data-stu-id="6a87d-147">12183</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-148">Retornado por [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) quando uma condição de estouro é encontrada no curso da análise de codificação em bloco.</span><span class="sxs-lookup"><span data-stu-id="6a87d-148">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when an overflow condition is encountered in the course of parsing chunked encoding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-149"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERRO \_ de \_ certificado de autenticação de cliente WinHTTP \_ \_ \_ necessário**</span><span class="sxs-lookup"><span data-stu-id="6a87d-149"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-150">12044</span><span class="sxs-lookup"><span data-stu-id="6a87d-150">12044</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-151">Retornado por [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) quando o servidor solicita autenticação de cliente.</span><span class="sxs-lookup"><span data-stu-id="6a87d-151">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when the server requests client authentication.</span></span>

<span data-ttu-id="6a87d-152">**Windows Server 2003 com SP1 e Windows XP com SP2:** Não há suporte para esse erro.</span><span class="sxs-lookup"><span data-stu-id="6a87d-152">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-153"><span id="ERROR_WINHTTP_CONNECTION_ERROR"></span><span id="error_winhttp_connection_error"></span>**erro \_ de \_ conexão de WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="6a87d-153"><span id="ERROR_WINHTTP_CONNECTION_ERROR"></span><span id="error_winhttp_connection_error"></span>**ERROR\_WINHTTP\_CONNECTION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-154">12030</span><span class="sxs-lookup"><span data-stu-id="6a87d-154">12030</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-155">A conexão com o servidor foi redefinida ou encerrada ou um protocolo SSL incompatível foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="6a87d-155">The connection with the server has been reset or terminated, or an incompatible SSL protocol was encountered.</span></span> <span data-ttu-id="6a87d-156">Por exemplo, o WinHTTP versão 5,1 não oferece suporte a SSL2, a menos que o cliente o habilite especificamente.</span><span class="sxs-lookup"><span data-stu-id="6a87d-156">For example, WinHTTP version 5.1 does not support SSL2 unless the client specifically enables it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-157"><span id="ERROR_WINHTTP_HEADER_ALREADY_EXISTS"></span><span id="error_winhttp_header_already_exists"></span>**o \_ cabeçalho WinHTTP de erro \_ \_ já \_ existe**</span><span class="sxs-lookup"><span data-stu-id="6a87d-157"><span id="ERROR_WINHTTP_HEADER_ALREADY_EXISTS"></span><span id="error_winhttp_header_already_exists"></span>**ERROR\_WINHTTP\_HEADER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-158">12155</span><span class="sxs-lookup"><span data-stu-id="6a87d-158">12155</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-159">Substituí Não é mais usado.</span><span class="sxs-lookup"><span data-stu-id="6a87d-159">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-160"><span id="ERROR_WINHTTP_HEADER_COUNT_EXCEEDED"></span><span id="error_winhttp_header_count_exceeded"></span>**ERRO \_ de \_ contagem de cabeçalho WinHTTP \_ \_ excedida**</span><span class="sxs-lookup"><span data-stu-id="6a87d-160"><span id="ERROR_WINHTTP_HEADER_COUNT_EXCEEDED"></span><span id="error_winhttp_header_count_exceeded"></span>**ERROR\_WINHTTP\_HEADER\_COUNT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-161">12181</span><span class="sxs-lookup"><span data-stu-id="6a87d-161">12181</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-162">Retornado por [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) quando um número maior de cabeçalhos estava presente em uma resposta do que o WinHTTP poderia receber.</span><span class="sxs-lookup"><span data-stu-id="6a87d-162">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when a larger number of headers were present in a response than WinHTTP could receive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-163"><span id="ERROR_WINHTTP_HEADER_NOT_FOUND"></span><span id="error_winhttp_header_not_found"></span>**ERRO \_ de \_ cabeçalho WinHTTP \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="6a87d-163"><span id="ERROR_WINHTTP_HEADER_NOT_FOUND"></span><span id="error_winhttp_header_not_found"></span>**ERROR\_WINHTTP\_HEADER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-164">12150</span><span class="sxs-lookup"><span data-stu-id="6a87d-164">12150</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-165">O cabeçalho solicitado não pode ser localizado.</span><span class="sxs-lookup"><span data-stu-id="6a87d-165">The requested header cannot be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-166"><span id="ERROR_WINHTTP_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_header_size_overflow"></span>**ERRO \_ de \_ \_ estouro no tamanho do cabeçalho WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="6a87d-166"><span id="ERROR_WINHTTP_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_header_size_overflow"></span>**ERROR\_WINHTTP\_HEADER\_SIZE\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-167">12182</span><span class="sxs-lookup"><span data-stu-id="6a87d-167">12182</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-168">Retornado por [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) quando o tamanho dos cabeçalhos recebidos excede o limite para o identificador de solicitação.</span><span class="sxs-lookup"><span data-stu-id="6a87d-168">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when the size of headers received exceeds the limit for the request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-169"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_STATE"></span><span id="error_winhttp_incorrect_handle_state"></span>**ERRO \_ WinHTTP \_ \_ estado de identificador incorreto \_**</span><span class="sxs-lookup"><span data-stu-id="6a87d-169"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_STATE"></span><span id="error_winhttp_incorrect_handle_state"></span>**ERROR\_WINHTTP\_INCORRECT\_HANDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-170">12019</span><span class="sxs-lookup"><span data-stu-id="6a87d-170">12019</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-171">A operação solicitada não pode ser executada porque o identificador fornecido não está no estado correto.</span><span class="sxs-lookup"><span data-stu-id="6a87d-171">The requested operation cannot be carried out because the handle supplied is not in the correct state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-172"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_TYPE"></span><span id="error_winhttp_incorrect_handle_type"></span>**ERRO \_ WinHTTP \_ \_ tipo de identificador incorreto \_**</span><span class="sxs-lookup"><span data-stu-id="6a87d-172"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_TYPE"></span><span id="error_winhttp_incorrect_handle_type"></span>**ERROR\_WINHTTP\_INCORRECT\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-173">12018</span><span class="sxs-lookup"><span data-stu-id="6a87d-173">12018</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-174">O tipo de identificador fornecido está incorreto para esta operação.</span><span class="sxs-lookup"><span data-stu-id="6a87d-174">The type of handle supplied is incorrect for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-175"><span id="ERROR_WINHTTP_INTERNAL_ERROR"></span><span id="error_winhttp_internal_error"></span>**erro \_ interno de WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6a87d-175"><span id="ERROR_WINHTTP_INTERNAL_ERROR"></span><span id="error_winhttp_internal_error"></span>**ERROR\_WINHTTP\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-176">12004</span><span class="sxs-lookup"><span data-stu-id="6a87d-176">12004</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-177">Ocorreu um erro interno.</span><span class="sxs-lookup"><span data-stu-id="6a87d-177">An internal error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-178"><span id="ERROR_WINHTTP_INVALID_OPTION"></span><span id="error_winhttp_invalid_option"></span>**ERRO \_ WinHTTP \_ opção inválida \_**</span><span class="sxs-lookup"><span data-stu-id="6a87d-178"><span id="ERROR_WINHTTP_INVALID_OPTION"></span><span id="error_winhttp_invalid_option"></span>**ERROR\_WINHTTP\_INVALID\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-179">12009</span><span class="sxs-lookup"><span data-stu-id="6a87d-179">12009</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-180">Uma solicitação para [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) ou [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) especificou um valor de opção inválido.</span><span class="sxs-lookup"><span data-stu-id="6a87d-180">A request to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) or [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) specified an invalid option value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-181"><span id="ERROR_WINHTTP_INVALID_QUERY_REQUEST"></span><span id="error_winhttp_invalid_query_request"></span>**ERRO \_ WinHTTP \_ \_ solicitação de consulta inválida \_**</span><span class="sxs-lookup"><span data-stu-id="6a87d-181"><span id="ERROR_WINHTTP_INVALID_QUERY_REQUEST"></span><span id="error_winhttp_invalid_query_request"></span>**ERROR\_WINHTTP\_INVALID\_QUERY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-182">12154</span><span class="sxs-lookup"><span data-stu-id="6a87d-182">12154</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-183">Substituí Não é mais usado.</span><span class="sxs-lookup"><span data-stu-id="6a87d-183">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-184"><span id="ERROR_WINHTTP_INVALID_SERVER_RESPONSE"></span><span id="error_winhttp_invalid_server_response"></span>**ERRO \_ WinHTTP \_ \_ resposta de servidor inválida \_**</span><span class="sxs-lookup"><span data-stu-id="6a87d-184"><span id="ERROR_WINHTTP_INVALID_SERVER_RESPONSE"></span><span id="error_winhttp_invalid_server_response"></span>**ERROR\_WINHTTP\_INVALID\_SERVER\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-185">12152</span><span class="sxs-lookup"><span data-stu-id="6a87d-185">12152</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-186">Não é possível analisar a resposta do servidor.</span><span class="sxs-lookup"><span data-stu-id="6a87d-186">The server response cannot be parsed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-187"><span id="ERROR_WINHTTP_INVALID_URL"></span><span id="error_winhttp_invalid_url"></span>**ERRO \_ ao \_ WinHTTP \_ URL inválido**</span><span class="sxs-lookup"><span data-stu-id="6a87d-187"><span id="ERROR_WINHTTP_INVALID_URL"></span><span id="error_winhttp_invalid_url"></span>**ERROR\_WINHTTP\_INVALID\_URL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-188">12005</span><span class="sxs-lookup"><span data-stu-id="6a87d-188">12005</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-189">A URL não é válida.</span><span class="sxs-lookup"><span data-stu-id="6a87d-189">The URL is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-190"><span id="ERROR_WINHTTP_LOGIN_FAILURE"></span><span id="error_winhttp_login_failure"></span>**ERRO \_ de \_ falha de logon WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="6a87d-190"><span id="ERROR_WINHTTP_LOGIN_FAILURE"></span><span id="error_winhttp_login_failure"></span>**ERROR\_WINHTTP\_LOGIN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-191">12015</span><span class="sxs-lookup"><span data-stu-id="6a87d-191">12015</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-192">Falha na tentativa de logon.</span><span class="sxs-lookup"><span data-stu-id="6a87d-192">The login attempt failed.</span></span> <span data-ttu-id="6a87d-193">Quando esse erro é encontrado, o identificador de solicitação deve ser fechado com [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle).</span><span class="sxs-lookup"><span data-stu-id="6a87d-193">When this error is encountered, the request handle should be closed with [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle).</span></span> <span data-ttu-id="6a87d-194">Um novo identificador de solicitação deve ser criado antes de tentar novamente a função que produziu esse erro originalmente.</span><span class="sxs-lookup"><span data-stu-id="6a87d-194">A new request handle must be created before retrying the function that originally produced this error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-195"><span id="ERROR_WINHTTP_NAME_NOT_RESOLVED"></span><span id="error_winhttp_name_not_resolved"></span>**ERRO \_ WinHTTP \_ nome \_ não \_ resolvido**</span><span class="sxs-lookup"><span data-stu-id="6a87d-195"><span id="ERROR_WINHTTP_NAME_NOT_RESOLVED"></span><span id="error_winhttp_name_not_resolved"></span>**ERROR\_WINHTTP\_NAME\_NOT\_RESOLVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-196">12007</span><span class="sxs-lookup"><span data-stu-id="6a87d-196">12007</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-197">O nome do servidor não pode ser resolvido.</span><span class="sxs-lookup"><span data-stu-id="6a87d-197">The server name cannot be resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-198"><span id="ERROR_WINHTTP_NOT_INITIALIZED"></span><span id="error_winhttp_not_initialized"></span>**ERRO \_ WinHTTP \_ não \_ inicializado**</span><span class="sxs-lookup"><span data-stu-id="6a87d-198"><span id="ERROR_WINHTTP_NOT_INITIALIZED"></span><span id="error_winhttp_not_initialized"></span>**ERROR\_WINHTTP\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-199">12172</span><span class="sxs-lookup"><span data-stu-id="6a87d-199">12172</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-200">Substituí Não é mais usado.</span><span class="sxs-lookup"><span data-stu-id="6a87d-200">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-201"><span id="ERROR_WINHTTP_OPERATION_CANCELLED"></span><span id="error_winhttp_operation_cancelled"></span>**ERRO \_ de \_ operação WinHTTP \_ cancelada**</span><span class="sxs-lookup"><span data-stu-id="6a87d-201"><span id="ERROR_WINHTTP_OPERATION_CANCELLED"></span><span id="error_winhttp_operation_cancelled"></span>**ERROR\_WINHTTP\_OPERATION\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-202">12017</span><span class="sxs-lookup"><span data-stu-id="6a87d-202">12017</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-203">A operação foi cancelada, geralmente porque o identificador no qual a solicitação estava operando foi fechado antes da operação ser concluída.</span><span class="sxs-lookup"><span data-stu-id="6a87d-203">The operation was canceled, usually because the handle on which the request was operating was closed before the operation completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-204"><span id="ERROR_WINHTTP_OPTION_NOT_SETTABLE"></span><span id="error_winhttp_option_not_settable"></span>**ERRO \_ de \_ opção WinHTTP \_ não \_ configurável**</span><span class="sxs-lookup"><span data-stu-id="6a87d-204"><span id="ERROR_WINHTTP_OPTION_NOT_SETTABLE"></span><span id="error_winhttp_option_not_settable"></span>**ERROR\_WINHTTP\_OPTION\_NOT\_SETTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-205">12011</span><span class="sxs-lookup"><span data-stu-id="6a87d-205">12011</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-206">A opção solicitada não pode ser definida, somente consultada.</span><span class="sxs-lookup"><span data-stu-id="6a87d-206">The requested option cannot be set, only queried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-207"><span id="ERROR_WINHTTP_OUT_OF_HANDLES"></span><span id="error_winhttp_out_of_handles"></span>**ERRO \_ WinHTTP \_ fora \_ de \_ identificadores**</span><span class="sxs-lookup"><span data-stu-id="6a87d-207"><span id="ERROR_WINHTTP_OUT_OF_HANDLES"></span><span id="error_winhttp_out_of_handles"></span>**ERROR\_WINHTTP\_OUT\_OF\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-208">12001</span><span class="sxs-lookup"><span data-stu-id="6a87d-208">12001</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-209">Substituí Não é mais usado.</span><span class="sxs-lookup"><span data-stu-id="6a87d-209">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-210"><span id="ERROR_WINHTTP_REDIRECT_FAILED"></span><span id="error_winhttp_redirect_failed"></span>**ERRO \_ \_ ao redirecionar WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="6a87d-210"><span id="ERROR_WINHTTP_REDIRECT_FAILED"></span><span id="error_winhttp_redirect_failed"></span>**ERROR\_WINHTTP\_REDIRECT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-211">12156</span><span class="sxs-lookup"><span data-stu-id="6a87d-211">12156</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-212">Falha no redirecionamento porque o esquema foi alterado ou todas as tentativas feitas para redirecionamento falharam (o padrão é cinco tentativas).</span><span class="sxs-lookup"><span data-stu-id="6a87d-212">The redirection failed because either the scheme changed or all attempts made to redirect failed (default is five attempts).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-213"><span id="ERROR_WINHTTP_RESEND_REQUEST"></span><span id="error_winhttp_resend_request"></span>**ERRO \_ de \_ solicitação de reenvio de WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="6a87d-213"><span id="ERROR_WINHTTP_RESEND_REQUEST"></span><span id="error_winhttp_resend_request"></span>**ERROR\_WINHTTP\_RESEND\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-214">12032</span><span class="sxs-lookup"><span data-stu-id="6a87d-214">12032</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-215">A função WinHTTP falhou.</span><span class="sxs-lookup"><span data-stu-id="6a87d-215">The WinHTTP function failed.</span></span> <span data-ttu-id="6a87d-216">A função desejada pode ser repetida no mesmo identificador de solicitação.</span><span class="sxs-lookup"><span data-stu-id="6a87d-216">The desired function can be retried on the same request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-217"><span id="ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW"></span><span id="error_winhttp_response_drain_overflow"></span>**ERRO \_ de \_ \_ estouro de esgotamento de resposta de WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="6a87d-217"><span id="ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW"></span><span id="error_winhttp_response_drain_overflow"></span>**ERROR\_WINHTTP\_RESPONSE\_DRAIN\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-218">12184</span><span class="sxs-lookup"><span data-stu-id="6a87d-218">12184</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-219">Retornado quando uma resposta de entrada excede um limite de tamanho de WinHTTP interno.</span><span class="sxs-lookup"><span data-stu-id="6a87d-219">Returned when an incoming response exceeds an internal WinHTTP size limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-220"><span id="ERROR_WINHTTP_SCRIPT_EXECUTION_ERROR"></span><span id="error_winhttp_script_execution_error"></span>**erro \_ de \_ \_ erro de execução de script WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="6a87d-220"><span id="ERROR_WINHTTP_SCRIPT_EXECUTION_ERROR"></span><span id="error_winhttp_script_execution_error"></span>**ERROR\_WINHTTP\_SCRIPT\_EXECUTION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-221">12177</span><span class="sxs-lookup"><span data-stu-id="6a87d-221">12177</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-222">Foi encontrado um erro ao executar um script.</span><span class="sxs-lookup"><span data-stu-id="6a87d-222">An error was encountered while executing a script.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-223"><span id="ERROR_WINHTTP_SECURE_CERT_CN_INVALID"></span><span id="error_winhttp_secure_cert_cn_invalid"></span>**ERRO \_ WinHTTP \_ Secure \_ CERT \_ CN \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="6a87d-223"><span id="ERROR_WINHTTP_SECURE_CERT_CN_INVALID"></span><span id="error_winhttp_secure_cert_cn_invalid"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_CN\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-224">12038</span><span class="sxs-lookup"><span data-stu-id="6a87d-224">12038</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-225">Retornado quando um nome CN do certificado não corresponde ao valor transmitido (equivalente a um erro de **certificado \_ E \_ CN \_ sem \_ correspondência** ).</span><span class="sxs-lookup"><span data-stu-id="6a87d-225">Returned when a certificate CN name does not match the passed value (equivalent to a **CERT\_E\_CN\_NO\_MATCH** error).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-226"><span id="ERROR_WINHTTP_SECURE_CERT_DATE_INVALID"></span><span id="error_winhttp_secure_cert_date_invalid"></span>**ERRO \_ WinHTTP \_ Secure \_ CERT \_ Date \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="6a87d-226"><span id="ERROR_WINHTTP_SECURE_CERT_DATE_INVALID"></span><span id="error_winhttp_secure_cert_date_invalid"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_DATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-227">12037</span><span class="sxs-lookup"><span data-stu-id="6a87d-227">12037</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-228">Indica que um certificado necessário não está dentro de seu período de validade ao verificar em relação ao relógio do sistema atual ou ao carimbo de data/hora no arquivo assinado, ou que os períodos de validade da cadeia de certificação não são aninhados corretamente (equivalente a um **certificado \_ e \_ expirado** ou a um erro **\_ e \_ VALIDITYPERIODNESTING** ).</span><span class="sxs-lookup"><span data-stu-id="6a87d-228">Indicates that a required certificate is not within its validity period when verifying against the current system clock or the timestamp in the signed file, or that the validity periods of the certification chain do not nest correctly (equivalent to a **CERT\_E\_EXPIRED** or a **CERT\_E\_VALIDITYPERIODNESTING** error).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-229"><span id="ERROR_WINHTTP_SECURE_CERT_REV_FAILED"></span><span id="error_winhttp_secure_cert_rev_failed"></span>**ERRO \_ WinHTTP \_ Secure \_ CERT \_ rev \_ falhou**</span><span class="sxs-lookup"><span data-stu-id="6a87d-229"><span id="ERROR_WINHTTP_SECURE_CERT_REV_FAILED"></span><span id="error_winhttp_secure_cert_rev_failed"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_REV\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-230">12057</span><span class="sxs-lookup"><span data-stu-id="6a87d-230">12057</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-231">Indica que a revogação não pode ser verificada porque o servidor de revogação estava offline (equivalente a **criptografada \_ E \_ revogação \_ offline**).</span><span class="sxs-lookup"><span data-stu-id="6a87d-231">Indicates that revocation cannot be checked because the revocation server was offline (equivalent to **CRYPT\_E\_REVOCATION\_OFFLINE**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-232"><span id="ERROR_WINHTTP_SECURE_CERT_REVOKED"></span><span id="error_winhttp_secure_cert_revoked"></span>**ERRO \_ WinHTTP \_ Secure \_ CERT \_ revogado**</span><span class="sxs-lookup"><span data-stu-id="6a87d-232"><span id="ERROR_WINHTTP_SECURE_CERT_REVOKED"></span><span id="error_winhttp_secure_cert_revoked"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-233">12170</span><span class="sxs-lookup"><span data-stu-id="6a87d-233">12170</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-234">Indica que um certificado foi revogado (equivalente a cript. **\_ E \_ revogado**).</span><span class="sxs-lookup"><span data-stu-id="6a87d-234">Indicates that a certificate has been revoked (equivalent to **CRYPT\_E\_REVOKED**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-235"><span id="ERROR_WINHTTP_SECURE_CERT_WRONG_USAGE"></span><span id="error_winhttp_secure_cert_wrong_usage"></span>**ERRO \_ WinHTTP \_ - \_ \_ uso errado de certificado seguro \_**</span><span class="sxs-lookup"><span data-stu-id="6a87d-235"><span id="ERROR_WINHTTP_SECURE_CERT_WRONG_USAGE"></span><span id="error_winhttp_secure_cert_wrong_usage"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_WRONG\_USAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-236">12179</span><span class="sxs-lookup"><span data-stu-id="6a87d-236">12179</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-237">Indica que um certificado não é válido para o uso solicitado (equivalente ao **certificado \_ E \_ \_ uso incorreto**).</span><span class="sxs-lookup"><span data-stu-id="6a87d-237">Indicates that a certificate is not valid for the requested usage (equivalent to **CERT\_E\_WRONG\_USAGE**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-238"><span id="ERROR_WINHTTP_SECURE_CHANNEL_ERROR"></span><span id="error_winhttp_secure_channel_error"></span>**erro de erro de \_ \_ canal seguro de WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6a87d-238"><span id="ERROR_WINHTTP_SECURE_CHANNEL_ERROR"></span><span id="error_winhttp_secure_channel_error"></span>**ERROR\_WINHTTP\_SECURE\_CHANNEL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-239">12157</span><span class="sxs-lookup"><span data-stu-id="6a87d-239">12157</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-240">Indica que ocorreu um erro ao fazer com um canal seguro (equivalente a códigos de erro que começam com "SEC \_ e \_ " e "s \_ I \_ " listados no arquivo de cabeçalho "Winerror. h").</span><span class="sxs-lookup"><span data-stu-id="6a87d-240">Indicates that an error occurred having to do with a secure channel (equivalent to error codes that begin with "SEC\_E\_" and "SEC\_I\_" listed in the "winerror.h" header file).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-241"><span id="ERROR_WINHTTP_SECURE_FAILURE"></span><span id="error_winhttp_secure_failure"></span>**ERRO de \_ falha de WinHTTP \_ seguro \_**</span><span class="sxs-lookup"><span data-stu-id="6a87d-241"><span id="ERROR_WINHTTP_SECURE_FAILURE"></span><span id="error_winhttp_secure_failure"></span>**ERROR\_WINHTTP\_SECURE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-242">12175</span><span class="sxs-lookup"><span data-stu-id="6a87d-242">12175</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-243">Um ou mais erros foram encontrados no certificado de protocolo SSL (SSL) enviado pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="6a87d-243">One or more errors were found in the Secure Sockets Layer (SSL) certificate sent by the server.</span></span> <span data-ttu-id="6a87d-244">Para determinar que tipo de erro foi encontrado, verifique se há uma notificação de [**\_ \_ \_ \_ falha segura de status de retorno de chamada do WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) em uma função de retorno de chamada de status.</span><span class="sxs-lookup"><span data-stu-id="6a87d-244">To determine what type of error was encountered, check for a [**WINHTTP\_CALLBACK\_STATUS\_SECURE\_FAILURE**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) notification in a status callback function.</span></span> <span data-ttu-id="6a87d-245">Para obter mais informações, [**consulte \_ retorno de \_ chamada de status do WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback).</span><span class="sxs-lookup"><span data-stu-id="6a87d-245">For more information, see [**WINHTTP\_STATUS\_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-246"><span id="ERROR_WINHTTP_SECURE_INVALID_CA"></span><span id="error_winhttp_secure_invalid_ca"></span>**ERRO \_ WinHTTP \_ Secure \_ AC inválida \_**</span><span class="sxs-lookup"><span data-stu-id="6a87d-246"><span id="ERROR_WINHTTP_SECURE_INVALID_CA"></span><span id="error_winhttp_secure_invalid_ca"></span>**ERROR\_WINHTTP\_SECURE\_INVALID\_CA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-247">12045</span><span class="sxs-lookup"><span data-stu-id="6a87d-247">12045</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-248">Indica que uma cadeia de certificados foi processada, mas terminada em um certificado raiz que não é confiável pelo provedor de confiança (equivalente a **CERT \_ E \_ UNTRUSTEDROOT**).</span><span class="sxs-lookup"><span data-stu-id="6a87d-248">Indicates that a certificate chain was processed, but terminated in a root certificate that is not trusted by the trust provider (equivalent to **CERT\_E\_UNTRUSTEDROOT**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-249"><span id="ERROR_WINHTTP_SECURE_INVALID_CERT"></span><span id="error_winhttp_secure_invalid_cert"></span>**ERRO \_ WinHTTP \_ Secure \_ \_ CERT inválido**</span><span class="sxs-lookup"><span data-stu-id="6a87d-249"><span id="ERROR_WINHTTP_SECURE_INVALID_CERT"></span><span id="error_winhttp_secure_invalid_cert"></span>**ERROR\_WINHTTP\_SECURE\_INVALID\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-250">12169</span><span class="sxs-lookup"><span data-stu-id="6a87d-250">12169</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-251">Indica que um certificado é inválido (equivalente a erros como a **\_ \_ função CERT e**, **CERT \_ e \_ PATHLENCONST**, **CERT \_ e \_ Critical**, CERT e **\_ \_ propósito**, **CERT \_ e \_ ISSUERCHAINING**, **CERT \_ e \_** **\_ \_ encadeado e CERT**).</span><span class="sxs-lookup"><span data-stu-id="6a87d-251">Indicates that a certificate is invalid (equivalent to errors such as **CERT\_E\_ROLE**, **CERT\_E\_PATHLENCONST**, **CERT\_E\_CRITICAL**, **CERT\_E\_PURPOSE**, **CERT\_E\_ISSUERCHAINING**, **CERT\_E\_MALFORMED** and **CERT\_E\_CHAINING**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-252"><span id="ERROR_WINHTTP_SHUTDOWN"></span><span id="error_winhttp_shutdown"></span>**ERRO \_ de \_ desligamento de WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="6a87d-252"><span id="ERROR_WINHTTP_SHUTDOWN"></span><span id="error_winhttp_shutdown"></span>**ERROR\_WINHTTP\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-253">12012</span><span class="sxs-lookup"><span data-stu-id="6a87d-253">12012</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-254">O suporte à função WinHTTP está sendo desligado ou descarregado.</span><span class="sxs-lookup"><span data-stu-id="6a87d-254">The WinHTTP function support is being shut down or unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-255"><span id="ERROR_WINHTTP_TIMEOUT"></span><span id="error_winhttp_timeout"></span>**ERRO de \_ WinHTTP \_ Timeout**</span><span class="sxs-lookup"><span data-stu-id="6a87d-255"><span id="ERROR_WINHTTP_TIMEOUT"></span><span id="error_winhttp_timeout"></span>**ERROR\_WINHTTP\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-256">12002</span><span class="sxs-lookup"><span data-stu-id="6a87d-256">12002</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-257">O tempo limite da solicitação foi atingido.</span><span class="sxs-lookup"><span data-stu-id="6a87d-257">The request has timed out.</span></span>

<span data-ttu-id="6a87d-258">Esse erro pode ser retornado como resultado do comportamento de tempo limite de TCP/IP, independentemente dos valores de tempo limite definidos nos serviços HTTP do Windows.</span><span class="sxs-lookup"><span data-stu-id="6a87d-258">This error can be returned as a result of TCP/IP time-out behavior, regardless of time-out values set in Windows HTTP Services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-259"><span id="ERROR_WINHTTP_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_winhttp_unable_to_download_script"></span>**ERRO \_ WinHTTP \_ não é possível \_ \_ baixar o \_ script**</span><span class="sxs-lookup"><span data-stu-id="6a87d-259"><span id="ERROR_WINHTTP_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_winhttp_unable_to_download_script"></span>**ERROR\_WINHTTP\_UNABLE\_TO\_DOWNLOAD\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-260">12167</span><span class="sxs-lookup"><span data-stu-id="6a87d-260">12167</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-261">Não é possível baixar o arquivo PAC.</span><span class="sxs-lookup"><span data-stu-id="6a87d-261">The PAC file cannot be downloaded.</span></span> <span data-ttu-id="6a87d-262">Por exemplo, o servidor referenciado pela URL de PAC pode não ter sido acessado ou o servidor retornou uma resposta 404 não encontrada.</span><span class="sxs-lookup"><span data-stu-id="6a87d-262">For example, the server referenced by the PAC URL may not have been reachable, or the server returned a 404 NOT FOUND response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-263"><span id="ERROR_WINHTTP_UNHANDLED_SCRIPT_TYPE"></span><span id="error_winhttp_unhandled_script_type"></span>**ERRO \_ WinHTTP \_ tipo de script sem tratamento \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6a87d-263"><span id="ERROR_WINHTTP_UNHANDLED_SCRIPT_TYPE"></span><span id="error_winhttp_unhandled_script_type"></span>**ERROR\_WINHTTP\_UNHANDLED\_SCRIPT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-264">12176</span><span class="sxs-lookup"><span data-stu-id="6a87d-264">12176</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-265">Não há suporte para o tipo de script.</span><span class="sxs-lookup"><span data-stu-id="6a87d-265">The script type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-266"><span id="ERROR_WINHTTP_UNRECOGNIZED_SCHEME"></span><span id="error_winhttp_unrecognized_scheme"></span>**ERRO \_ WinHTTP \_ esquema não reconhecido \_**</span><span class="sxs-lookup"><span data-stu-id="6a87d-266"><span id="ERROR_WINHTTP_UNRECOGNIZED_SCHEME"></span><span id="error_winhttp_unrecognized_scheme"></span>**ERROR\_WINHTTP\_UNRECOGNIZED\_SCHEME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a87d-267">12006</span><span class="sxs-lookup"><span data-stu-id="6a87d-267">12006</span></span>
</dt> <dt>



<span data-ttu-id="6a87d-268">A URL especificou um esquema diferente de "http:" ou "https:".</span><span class="sxs-lookup"><span data-stu-id="6a87d-268">The URL specified a scheme other than "http:" or "https:".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-269"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERRO \_ de \_ memória insuficiente \_**</span><span class="sxs-lookup"><span data-stu-id="6a87d-269"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a87d-270">Não havia memória suficiente disponível para concluir a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="6a87d-270">Not enough memory was available to complete the requested operation.</span></span>

<span data-ttu-id="6a87d-271">**Cabeçalho:** Declarado em Winerror. h</span><span class="sxs-lookup"><span data-stu-id="6a87d-271">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-272"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERRO \_ de \_ buffer insuficiente**</span><span class="sxs-lookup"><span data-stu-id="6a87d-272"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a87d-273">O tamanho, em bytes, do buffer fornecido a uma função era insuficiente para conter os dados retornados.</span><span class="sxs-lookup"><span data-stu-id="6a87d-273">The size, in bytes, of the buffer supplied to a function was insufficient to contain the returned data.</span></span> <span data-ttu-id="6a87d-274">Para obter mais informações, consulte a função específica.</span><span class="sxs-lookup"><span data-stu-id="6a87d-274">For more information, see the specific function.</span></span>

<span data-ttu-id="6a87d-275">**Cabeçalho:** Declarado em Winerror. h</span><span class="sxs-lookup"><span data-stu-id="6a87d-275">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-276"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**\_identificador inválido do erro \_**</span><span class="sxs-lookup"><span data-stu-id="6a87d-276"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR\_INVALID\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a87d-277">O identificador passado para a API (interface de programação de aplicativo) foi invalidado ou fechado.</span><span class="sxs-lookup"><span data-stu-id="6a87d-277">The handle passed to the application programming interface (API) has been either invalidated or closed.</span></span>

<span data-ttu-id="6a87d-278">**Cabeçalho:** Declarado em Winerror. h</span><span class="sxs-lookup"><span data-stu-id="6a87d-278">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-279"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERRO \_ não há \_ mais \_ arquivos**</span><span class="sxs-lookup"><span data-stu-id="6a87d-279"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR\_NO\_MORE\_FILES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a87d-280">Não foram encontrados mais arquivos.</span><span class="sxs-lookup"><span data-stu-id="6a87d-280">No more files have been found.</span></span>

<span data-ttu-id="6a87d-281">**Cabeçalho:** Declarado em Winerror. h</span><span class="sxs-lookup"><span data-stu-id="6a87d-281">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-282"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERRO \_ não há \_ mais \_ itens**</span><span class="sxs-lookup"><span data-stu-id="6a87d-282"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERROR\_NO\_MORE\_ITEMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a87d-283">Não foram encontrados mais itens.</span><span class="sxs-lookup"><span data-stu-id="6a87d-283">No more items have been found.</span></span>

<span data-ttu-id="6a87d-284">**Cabeçalho:** Declarado em Winerror. h</span><span class="sxs-lookup"><span data-stu-id="6a87d-284">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a87d-285"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERRO \_ sem \_ suporte**</span><span class="sxs-lookup"><span data-stu-id="6a87d-285"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERROR\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a87d-286">A pilha de protocolos necessária não está carregada e o aplicativo não pode iniciar o WinSock.</span><span class="sxs-lookup"><span data-stu-id="6a87d-286">The required protocol stack is not loaded and the application cannot start WinSock.</span></span>

<span data-ttu-id="6a87d-287">**Cabeçalho:** Declarado em Winerror. h</span><span class="sxs-lookup"><span data-stu-id="6a87d-287">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a87d-288">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a87d-288">Remarks</span></span>

<span data-ttu-id="6a87d-289">Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="6a87d-289">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a87d-290">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a87d-290">Requirements</span></span>



| <span data-ttu-id="6a87d-291">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a87d-291">Requirement</span></span> | <span data-ttu-id="6a87d-292">Valor</span><span class="sxs-lookup"><span data-stu-id="6a87d-292">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a87d-293">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a87d-293">Minimum supported client</span></span><br/> | <span data-ttu-id="6a87d-294">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="6a87d-294">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="6a87d-295">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a87d-295">Minimum supported server</span></span><br/> | <span data-ttu-id="6a87d-296">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="6a87d-296">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="6a87d-297">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="6a87d-297">Redistributable</span></span><br/>          | <span data-ttu-id="6a87d-298">WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="6a87d-298">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="6a87d-299">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6a87d-299">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a87d-300"><dt>WinHTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a87d-300"><dt>Winhttp.h</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="6a87d-301">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a87d-301">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a87d-302">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="6a87d-302">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

