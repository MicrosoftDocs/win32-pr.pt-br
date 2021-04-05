---
title: Mensagens de erro (Wininet. h)
description: As funções WinINet retornam códigos de erro quando apropriado. Os erros a seguir são específicos para as funções do WinINet.
ms.assetid: 338bf65f-ebe5-4434-8407-9ab2a4c8d381
topic_type:
- apiref
api_name:
- ERROR_FTP_DROPPED
- ERROR_FTP_NO_PASSIVE_MODE
- ERROR_FTP_TRANSFER_IN_PROGRESS
- ERROR_GOPHER_ATTRIBUTE_NOT_FOUND
- ERROR_GOPHER_DATA_ERROR
- ERROR_GOPHER_END_OF_DATA
- ERROR_GOPHER_INCORRECT_LOCATOR_TYPE
- ERROR_GOPHER_INVALID_LOCATOR
- ERROR_GOPHER_NOT_FILE
- ERROR_GOPHER_NOT_GOPHER_PLUS
- ERROR_GOPHER_PROTOCOL_ERROR
- ERROR_GOPHER_UNKNOWN_LOCATOR
- ERROR_HTTP_COOKIE_DECLINED
- ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION
- ERROR_HTTP_DOWNLEVEL_SERVER
- ERROR_HTTP_HEADER_ALREADY_EXISTS
- ERROR_HTTP_HEADER_NOT_FOUND
- ERROR_HTTP_INVALID_HEADER
- ERROR_HTTP_INVALID_QUERY_REQUEST
- ERROR_HTTP_INVALID_SERVER_RESPONSE
- ERROR_HTTP_NOT_REDIRECTED
- ERROR_HTTP_REDIRECT_FAILED
- ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION
- ERROR_INTERNET_ASYNC_THREAD_FAILED
- ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT
- ERROR_INTERNET_BAD_OPTION_LENGTH
- ERROR_INTERNET_BAD_REGISTRY_PARAMETER
- ERROR_INTERNET_CANNOT_CONNECT
- ERROR_INTERNET_CHG_POST_IS_NON_SECURE
- ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED
- ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP
- ERROR_INTERNET_CONNECTION_ABORTED
- ERROR_INTERNET_CONNECTION_RESET
- ERROR_INTERNET_DECODING_FAILED
- ERROR_INTERNET_DIALOG_PENDING
- ERROR_INTERNET_DISCONNECTED
- ERROR_INTERNET_EXTENDED_ERROR
- ERROR_INTERNET_FAILED_DUETOSECURITYCHECK
- ERROR_INTERNET_FORCE_RETRY
- ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED
- ERROR_INTERNET_HANDLE_EXISTS
- ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR
- ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR
- ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR
- ERROR_INTERNET_INCORRECT_FORMAT
- ERROR_INTERNET_INCORRECT_HANDLE_STATE
- ERROR_INTERNET_INCORRECT_HANDLE_TYPE
- ERROR_INTERNET_INCORRECT_PASSWORD
- ERROR_INTERNET_INCORRECT_USER_NAME
- ERROR_INTERNET_INSERT_CDROM
- ERROR_INTERNET_INTERNAL_ERROR
- ERROR_INTERNET_INVALID_CA
- ERROR_INTERNET_INVALID_OPERATION
- ERROR_INTERNET_INVALID_OPTION
- ERROR_INTERNET_INVALID_PROXY_REQUEST
- ERROR_INTERNET_INVALID_URL
- ERROR_INTERNET_ITEM_NOT_FOUND
- ERROR_INTERNET_LOGIN_FAILURE
- ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY
- ERROR_INTERNET_MIXED_SECURITY
- ERROR_INTERNET_NAME_NOT_RESOLVED
- ERROR_INTERNET_NEED_MSN_SSPI_PKG
- ERROR_INTERNET_NEED_UI
- ERROR_INTERNET_NO_CALLBACK
- ERROR_INTERNET_NO_CONTEXT
- ERROR_INTERNET_NO_DIRECT_ACCESS
- ERROR_INTERNET_NOT_INITIALIZED
- ERROR_INTERNET_NOT_PROXY_REQUEST
- ERROR_INTERNET_OPERATION_CANCELLED
- ERROR_INTERNET_OPTION_NOT_SETTABLE
- ERROR_INTERNET_OUT_OF_HANDLES
- ERROR_INTERNET_POST_IS_NON_SECURE
- ERROR_INTERNET_PROTOCOL_NOT_FOUND
- ERROR_INTERNET_PROXY_SERVER_UNREACHABLE
- ERROR_INTERNET_REDIRECT_SCHEME_CHANGE
- ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND
- ERROR_INTERNET_REQUEST_PENDING
- ERROR_INTERNET_RETRY_DIALOG
- ERROR_INTERNET_SEC_CERT_CN_INVALID
- ERROR_INTERNET_SEC_CERT_DATE_INVALID
- ERROR_INTERNET_SEC_CERT_ERRORS
- ERROR_INTERNET_SEC_CERT_NO_REV
- ERROR_INTERNET_SEC_CERT_REV_FAILED
- ERROR_INTERNET_SEC_CERT_REVOKED
- ERROR_INTERNET_SEC_INVALID_CERT
- ERROR_INTERNET_SECURITY_CHANNEL_ERROR
- ERROR_INTERNET_SERVER_UNREACHABLE
- ERROR_INTERNET_SHUTDOWN
- ERROR_INTERNET_TCPIP_NOT_INSTALLED
- ERROR_INTERNET_TIMEOUT
- ERROR_INTERNET_UNABLE_TO_CACHE_FILE
- ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT
- ERROR_INTERNET_UNRECOGNIZED_SCHEME
- ERROR_INVALID_HANDLE
- ERROR_MORE_DATA
- ERROR_NO_MORE_FILES
- ERROR_NO_MORE_ITEMS
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43fcaba7f0404ad002d2a94ac8291c95b0f7440
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086482"
---
# <a name="error-messages-winineth"></a><span data-ttu-id="92834-104">Mensagens de erro (Wininet. h)</span><span class="sxs-lookup"><span data-stu-id="92834-104">Error Messages (Wininet.h)</span></span>

<span data-ttu-id="92834-105">As funções WinINet retornam códigos de erro quando apropriado.</span><span class="sxs-lookup"><span data-stu-id="92834-105">The WinINet functions return error codes where appropriate.</span></span> <span data-ttu-id="92834-106">Os erros a seguir são específicos para as funções do WinINet.</span><span class="sxs-lookup"><span data-stu-id="92834-106">The following errors are specific to the WinINet functions.</span></span>

<dl> <dt>

<span data-ttu-id="92834-107"><span id="ERROR_FTP_DROPPED"></span><span id="error_ftp_dropped"></span>**ERRO \_ FTP \_ ignorado**</span><span class="sxs-lookup"><span data-stu-id="92834-107"><span id="ERROR_FTP_DROPPED"></span><span id="error_ftp_dropped"></span>**ERROR\_FTP\_DROPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-108">12111</span><span class="sxs-lookup"><span data-stu-id="92834-108">12111</span></span>
</dt> <dt>



<span data-ttu-id="92834-109">A operação de FTP não foi concluída porque a sessão foi anulada.</span><span class="sxs-lookup"><span data-stu-id="92834-109">The FTP operation was not completed because the session was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-110"><span id="ERROR_FTP_NO_PASSIVE_MODE"></span><span id="error_ftp_no_passive_mode"></span>**ERRO \_ FTP \_ sem \_ \_ modo passivo**</span><span class="sxs-lookup"><span data-stu-id="92834-110"><span id="ERROR_FTP_NO_PASSIVE_MODE"></span><span id="error_ftp_no_passive_mode"></span>**ERROR\_FTP\_NO\_PASSIVE\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-111">12112</span><span class="sxs-lookup"><span data-stu-id="92834-111">12112</span></span>
</dt> <dt>



<span data-ttu-id="92834-112">O modo passivo não está disponível no servidor.</span><span class="sxs-lookup"><span data-stu-id="92834-112">Passive mode is not available on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-113"><span id="ERROR_FTP_TRANSFER_IN_PROGRESS"></span><span id="error_ftp_transfer_in_progress"></span>**ERRO \_ \_ na transferência \_ de FTP em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="92834-113"><span id="ERROR_FTP_TRANSFER_IN_PROGRESS"></span><span id="error_ftp_transfer_in_progress"></span>**ERROR\_FTP\_TRANSFER\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-114">12110</span><span class="sxs-lookup"><span data-stu-id="92834-114">12110</span></span>
</dt> <dt>



<span data-ttu-id="92834-115">A operação solicitada não pode ser feita no identificador de sessão de FTP porque uma operação já está em andamento.</span><span class="sxs-lookup"><span data-stu-id="92834-115">The requested operation cannot be made on the FTP session handle because an operation is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-116"><span id="ERROR_GOPHER_ATTRIBUTE_NOT_FOUND"></span><span id="error_gopher_attribute_not_found"></span>**ERRO \_ de \_ atributo Gopher \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="92834-116"><span id="ERROR_GOPHER_ATTRIBUTE_NOT_FOUND"></span><span id="error_gopher_attribute_not_found"></span>**ERROR\_GOPHER\_ATTRIBUTE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-117">12137</span><span class="sxs-lookup"><span data-stu-id="92834-117">12137</span></span>
</dt> <dt>



<span data-ttu-id="92834-118">Não foi possível localizar o atributo solicitado.</span><span class="sxs-lookup"><span data-stu-id="92834-118">The requested attribute could not be located.</span></span>

> [!Note]  
> <span data-ttu-id="92834-119">Somente Windows XP e Windows Server 2003 R2 e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="92834-119">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-120"><span id="ERROR_GOPHER_DATA_ERROR"></span><span id="error_gopher_data_error"></span>**ERRO de erro de \_ \_ dados Gopher \_**</span><span class="sxs-lookup"><span data-stu-id="92834-120"><span id="ERROR_GOPHER_DATA_ERROR"></span><span id="error_gopher_data_error"></span>**ERROR\_GOPHER\_DATA\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-121">12132</span><span class="sxs-lookup"><span data-stu-id="92834-121">12132</span></span>
</dt> <dt>



<span data-ttu-id="92834-122">Foi detectado um erro ao receber dados do servidor gopher.</span><span class="sxs-lookup"><span data-stu-id="92834-122">An error was detected while receiving data from the Gopher server.</span></span>

> [!Note]  
> <span data-ttu-id="92834-123">Somente Windows XP e Windows Server 2003 R2 e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="92834-123">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-124"><span id="ERROR_GOPHER_END_OF_DATA"></span><span id="error_gopher_end_of_data"></span>**ERRO \_ \_ de fim \_ de \_ dados do Gopher**</span><span class="sxs-lookup"><span data-stu-id="92834-124"><span id="ERROR_GOPHER_END_OF_DATA"></span><span id="error_gopher_end_of_data"></span>**ERROR\_GOPHER\_END\_OF\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-125">12133</span><span class="sxs-lookup"><span data-stu-id="92834-125">12133</span></span>
</dt> <dt>



<span data-ttu-id="92834-126">O fim dos dados foi atingido.</span><span class="sxs-lookup"><span data-stu-id="92834-126">The end of the data has been reached.</span></span>

> [!Note]  
> <span data-ttu-id="92834-127">Somente Windows XP e Windows Server 2003 R2 e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="92834-127">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-128"><span id="ERROR_GOPHER_INCORRECT_LOCATOR_TYPE"></span><span id="error_gopher_incorrect_locator_type"></span>**ERRO \_ do \_ \_ tipo de localizador incorreto do Gopher \_**</span><span class="sxs-lookup"><span data-stu-id="92834-128"><span id="ERROR_GOPHER_INCORRECT_LOCATOR_TYPE"></span><span id="error_gopher_incorrect_locator_type"></span>**ERROR\_GOPHER\_INCORRECT\_LOCATOR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-129">12135</span><span class="sxs-lookup"><span data-stu-id="92834-129">12135</span></span>
</dt> <dt>



<span data-ttu-id="92834-130">O tipo do localizador não está correto para esta operação.</span><span class="sxs-lookup"><span data-stu-id="92834-130">The type of the locator is not correct for this operation.</span></span>

> [!Note]  
> <span data-ttu-id="92834-131">Somente Windows XP e Windows Server 2003 R2 e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="92834-131">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-132"><span id="ERROR_GOPHER_INVALID_LOCATOR"></span><span id="error_gopher_invalid_locator"></span>**ERRO \_ Gopher \_ inválido no \_ localizador**</span><span class="sxs-lookup"><span data-stu-id="92834-132"><span id="ERROR_GOPHER_INVALID_LOCATOR"></span><span id="error_gopher_invalid_locator"></span>**ERROR\_GOPHER\_INVALID\_LOCATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-133">12134</span><span class="sxs-lookup"><span data-stu-id="92834-133">12134</span></span>
</dt> <dt>



<span data-ttu-id="92834-134">O localizador fornecido não é válido.</span><span class="sxs-lookup"><span data-stu-id="92834-134">The supplied locator is not valid.</span></span>

> [!Note]  
> <span data-ttu-id="92834-135">Somente Windows XP e Windows Server 2003 R2 e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="92834-135">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-136"><span id="ERROR_GOPHER_NOT_FILE"></span><span id="error_gopher_not_file"></span>**ERRO \_ Gopher \_ não \_ arquivo**</span><span class="sxs-lookup"><span data-stu-id="92834-136"><span id="ERROR_GOPHER_NOT_FILE"></span><span id="error_gopher_not_file"></span>**ERROR\_GOPHER\_NOT\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-137">12131</span><span class="sxs-lookup"><span data-stu-id="92834-137">12131</span></span>
</dt> <dt>



<span data-ttu-id="92834-138">A solicitação deve ser feita para um localizador de arquivo.</span><span class="sxs-lookup"><span data-stu-id="92834-138">The request must be made for a file locator.</span></span>

> [!Note]  
> <span data-ttu-id="92834-139">Somente Windows XP e Windows Server 2003 R2 e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="92834-139">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-140"><span id="ERROR_GOPHER_NOT_GOPHER_PLUS"></span><span id="error_gopher_not_gopher_plus"></span>**ERRO \_ Gopher \_ não \_ Gopher \_ Plus**</span><span class="sxs-lookup"><span data-stu-id="92834-140"><span id="ERROR_GOPHER_NOT_GOPHER_PLUS"></span><span id="error_gopher_not_gopher_plus"></span>**ERROR\_GOPHER\_NOT\_GOPHER\_PLUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-141">12136</span><span class="sxs-lookup"><span data-stu-id="92834-141">12136</span></span>
</dt> <dt>



<span data-ttu-id="92834-142">A operação solicitada pode ser feita somente em um servidor Gopher + ou com um localizador que especifica uma operação do Gopher +.</span><span class="sxs-lookup"><span data-stu-id="92834-142">The requested operation can be made only against a Gopher+ server, or with a locator that specifies a Gopher+ operation.</span></span>

> [!Note]  
> <span data-ttu-id="92834-143">Somente Windows XP e Windows Server 2003 R2 e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="92834-143">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-144"><span id="ERROR_GOPHER_PROTOCOL_ERROR"></span><span id="error_gopher_protocol_error"></span>**ERRO de erro de \_ \_ protocolo Gopher \_**</span><span class="sxs-lookup"><span data-stu-id="92834-144"><span id="ERROR_GOPHER_PROTOCOL_ERROR"></span><span id="error_gopher_protocol_error"></span>**ERROR\_GOPHER\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-145">12130</span><span class="sxs-lookup"><span data-stu-id="92834-145">12130</span></span>
</dt> <dt>



<span data-ttu-id="92834-146">Foi detectado um erro ao analisar os dados retornados do servidor gopher.</span><span class="sxs-lookup"><span data-stu-id="92834-146">An error was detected while parsing data returned from the Gopher server.</span></span>

> [!Note]  
> <span data-ttu-id="92834-147">Somente Windows XP e Windows Server 2003 R2 e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="92834-147">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-148"><span id="ERROR_GOPHER_UNKNOWN_LOCATOR"></span><span id="error_gopher_unknown_locator"></span>**ERRO \_ de \_ localizador desconhecido do Gopher \_**</span><span class="sxs-lookup"><span data-stu-id="92834-148"><span id="ERROR_GOPHER_UNKNOWN_LOCATOR"></span><span id="error_gopher_unknown_locator"></span>**ERROR\_GOPHER\_UNKNOWN\_LOCATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-149">12138</span><span class="sxs-lookup"><span data-stu-id="92834-149">12138</span></span>
</dt> <dt>



<span data-ttu-id="92834-150">O tipo de localizador é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="92834-150">The locator type is unknown.</span></span>

> [!Note]  
> <span data-ttu-id="92834-151">Somente Windows XP e Windows Server 2003 R2 e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="92834-151">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-152"><span id="ERROR_HTTP_COOKIE_DECLINED"></span><span id="error_http_cookie_declined"></span>**ERRO \_ de \_ Cookie http \_ recusado**</span><span class="sxs-lookup"><span data-stu-id="92834-152"><span id="ERROR_HTTP_COOKIE_DECLINED"></span><span id="error_http_cookie_declined"></span>**ERROR\_HTTP\_COOKIE\_DECLINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-153">12162</span><span class="sxs-lookup"><span data-stu-id="92834-153">12162</span></span>
</dt> <dt>



<span data-ttu-id="92834-154">O cookie HTTP foi recusado pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="92834-154">The HTTP cookie was declined by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-155"><span id="ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION"></span><span id="error_http_cookie_needs_confirmation"></span>**ERRO \_ o \_ Cookie http \_ precisa de \_ confirmação**</span><span class="sxs-lookup"><span data-stu-id="92834-155"><span id="ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION"></span><span id="error_http_cookie_needs_confirmation"></span>**ERROR\_HTTP\_COOKIE\_NEEDS\_CONFIRMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-156">12161</span><span class="sxs-lookup"><span data-stu-id="92834-156">12161</span></span>
</dt> <dt>



<span data-ttu-id="92834-157">O cookie HTTP requer confirmação.</span><span class="sxs-lookup"><span data-stu-id="92834-157">The HTTP cookie requires confirmation.</span></span>

> [!Note]  
> <span data-ttu-id="92834-158">Somente Windows Vista e Windows Server 2008 e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="92834-158">Windows Vista and Windows Server 2008 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-159"><span id="ERROR_HTTP_DOWNLEVEL_SERVER"></span><span id="error_http_downlevel_server"></span>**ERRO \_ de \_ servidor de nível inferior http \_**</span><span class="sxs-lookup"><span data-stu-id="92834-159"><span id="ERROR_HTTP_DOWNLEVEL_SERVER"></span><span id="error_http_downlevel_server"></span>**ERROR\_HTTP\_DOWNLEVEL\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-160">12151</span><span class="sxs-lookup"><span data-stu-id="92834-160">12151</span></span>
</dt> <dt>



<span data-ttu-id="92834-161">O servidor não retornou nenhum cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="92834-161">The server did not return any headers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-162"><span id="ERROR_HTTP_HEADER_ALREADY_EXISTS"></span><span id="error_http_header_already_exists"></span>**o \_ cabeçalho HTTP do erro \_ \_ já \_ existe**</span><span class="sxs-lookup"><span data-stu-id="92834-162"><span id="ERROR_HTTP_HEADER_ALREADY_EXISTS"></span><span id="error_http_header_already_exists"></span>**ERROR\_HTTP\_HEADER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-163">12155</span><span class="sxs-lookup"><span data-stu-id="92834-163">12155</span></span>
</dt> <dt>



<span data-ttu-id="92834-164">Não foi possível adicionar o cabeçalho porque ele já existe.</span><span class="sxs-lookup"><span data-stu-id="92834-164">The header could not be added because it already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-165"><span id="ERROR_HTTP_HEADER_NOT_FOUND"></span><span id="error_http_header_not_found"></span>**\_cabeçalho HTTP de erro \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="92834-165"><span id="ERROR_HTTP_HEADER_NOT_FOUND"></span><span id="error_http_header_not_found"></span>**ERROR\_HTTP\_HEADER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-166">12150</span><span class="sxs-lookup"><span data-stu-id="92834-166">12150</span></span>
</dt> <dt>



<span data-ttu-id="92834-167">Não foi possível localizar o cabeçalho solicitado.</span><span class="sxs-lookup"><span data-stu-id="92834-167">The requested header could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-168"><span id="ERROR_HTTP_INVALID_HEADER"></span><span id="error_http_invalid_header"></span>**ERRO \_ de \_ cabeçalho http inválido \_**</span><span class="sxs-lookup"><span data-stu-id="92834-168"><span id="ERROR_HTTP_INVALID_HEADER"></span><span id="error_http_invalid_header"></span>**ERROR\_HTTP\_INVALID\_HEADER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-169">12153</span><span class="sxs-lookup"><span data-stu-id="92834-169">12153</span></span>
</dt> <dt>



<span data-ttu-id="92834-170">O cabeçalho fornecido é inválido.</span><span class="sxs-lookup"><span data-stu-id="92834-170">The supplied header is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-171"><span id="ERROR_HTTP_INVALID_QUERY_REQUEST"></span><span id="error_http_invalid_query_request"></span>**ERRO \_ de \_ \_ solicitação de consulta http inválida \_**</span><span class="sxs-lookup"><span data-stu-id="92834-171"><span id="ERROR_HTTP_INVALID_QUERY_REQUEST"></span><span id="error_http_invalid_query_request"></span>**ERROR\_HTTP\_INVALID\_QUERY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-172">12154</span><span class="sxs-lookup"><span data-stu-id="92834-172">12154</span></span>
</dt> <dt>



<span data-ttu-id="92834-173">A solicitação feita ao [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) é inválida.</span><span class="sxs-lookup"><span data-stu-id="92834-173">The request made to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-174"><span id="ERROR_HTTP_INVALID_SERVER_RESPONSE"></span><span id="error_http_invalid_server_response"></span>**ERRO \_ de \_ resposta inválida \_ do servidor http \_**</span><span class="sxs-lookup"><span data-stu-id="92834-174"><span id="ERROR_HTTP_INVALID_SERVER_RESPONSE"></span><span id="error_http_invalid_server_response"></span>**ERROR\_HTTP\_INVALID\_SERVER\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-175">12152</span><span class="sxs-lookup"><span data-stu-id="92834-175">12152</span></span>
</dt> <dt>



<span data-ttu-id="92834-176">Não foi possível analisar a resposta do servidor.</span><span class="sxs-lookup"><span data-stu-id="92834-176">The server response could not be parsed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-177"><span id="ERROR_HTTP_NOT_REDIRECTED"></span><span id="error_http_not_redirected"></span>**ERRO \_ http \_ não \_ Redirecionado**</span><span class="sxs-lookup"><span data-stu-id="92834-177"><span id="ERROR_HTTP_NOT_REDIRECTED"></span><span id="error_http_not_redirected"></span>**ERROR\_HTTP\_NOT\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-178">12160</span><span class="sxs-lookup"><span data-stu-id="92834-178">12160</span></span>
</dt> <dt>



<span data-ttu-id="92834-179">A solicitação HTTP não foi redirecionada.</span><span class="sxs-lookup"><span data-stu-id="92834-179">The HTTP request was not redirected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-180"><span id="ERROR_HTTP_REDIRECT_FAILED"></span><span id="error_http_redirect_failed"></span>**ERRO \_ \_ ao redirecionar http \_**</span><span class="sxs-lookup"><span data-stu-id="92834-180"><span id="ERROR_HTTP_REDIRECT_FAILED"></span><span id="error_http_redirect_failed"></span>**ERROR\_HTTP\_REDIRECT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-181">12156</span><span class="sxs-lookup"><span data-stu-id="92834-181">12156</span></span>
</dt> <dt>



<span data-ttu-id="92834-182">Falha no redirecionamento porque o esquema foi alterado (por exemplo, HTTP para FTP) ou todas as tentativas feitas para redirecionar falharam (o padrão é cinco tentativas).</span><span class="sxs-lookup"><span data-stu-id="92834-182">The redirection failed because either the scheme changed (for example, HTTP to FTP) or all attempts made to redirect failed (default is five attempts).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-183"><span id="ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION"></span><span id="error_http_redirect_needs_confirmation"></span>**ERRO \_ de \_ confirmação de redirecionamento http \_ necessário \_**</span><span class="sxs-lookup"><span data-stu-id="92834-183"><span id="ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION"></span><span id="error_http_redirect_needs_confirmation"></span>**ERROR\_HTTP\_REDIRECT\_NEEDS\_CONFIRMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-184">12168</span><span class="sxs-lookup"><span data-stu-id="92834-184">12168</span></span>
</dt> <dt>



<span data-ttu-id="92834-185">O redirecionamento requer confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="92834-185">The redirection requires user confirmation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-186"><span id="ERROR_INTERNET_ASYNC_THREAD_FAILED"></span><span id="error_internet_async_thread_failed"></span>**ERRO \_ \_ thread assíncrono da Internet \_ \_ com falha**</span><span class="sxs-lookup"><span data-stu-id="92834-186"><span id="ERROR_INTERNET_ASYNC_THREAD_FAILED"></span><span id="error_internet_async_thread_failed"></span>**ERROR\_INTERNET\_ASYNC\_THREAD\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-187">12047</span><span class="sxs-lookup"><span data-stu-id="92834-187">12047</span></span>
</dt> <dt>



<span data-ttu-id="92834-188">O aplicativo não pôde iniciar um thread assíncrono.</span><span class="sxs-lookup"><span data-stu-id="92834-188">The application could not start an asynchronous thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-189"><span id="ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_internet_bad_auto_proxy_script"></span>**ERRO \_ de \_ \_ script de \_ proxy \_ automático de Internet inválido**</span><span class="sxs-lookup"><span data-stu-id="92834-189"><span id="ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_internet_bad_auto_proxy_script"></span>**ERROR\_INTERNET\_BAD\_AUTO\_PROXY\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-190">12166</span><span class="sxs-lookup"><span data-stu-id="92834-190">12166</span></span>
</dt> <dt>



<span data-ttu-id="92834-191">Ocorreu um erro no script de configuração de proxy automático.</span><span class="sxs-lookup"><span data-stu-id="92834-191">There was an error in the automatic proxy configuration script.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-192"><span id="ERROR_INTERNET_BAD_OPTION_LENGTH"></span><span id="error_internet_bad_option_length"></span>**ERRO \_ de \_ \_ comprimento de opção inadequado da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="92834-192"><span id="ERROR_INTERNET_BAD_OPTION_LENGTH"></span><span id="error_internet_bad_option_length"></span>**ERROR\_INTERNET\_BAD\_OPTION\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-193">12010</span><span class="sxs-lookup"><span data-stu-id="92834-193">12010</span></span>
</dt> <dt>



<span data-ttu-id="92834-194">O comprimento de uma opção fornecida para [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) ou [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) está incorreto para o tipo de opção especificado.</span><span class="sxs-lookup"><span data-stu-id="92834-194">The length of an option supplied to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) or [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) is incorrect for the type of option specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-195"><span id="ERROR_INTERNET_BAD_REGISTRY_PARAMETER"></span><span id="error_internet_bad_registry_parameter"></span>**ERRO \_ de \_ \_ parâmetro de registro insatisfatório na Internet \_**</span><span class="sxs-lookup"><span data-stu-id="92834-195"><span id="ERROR_INTERNET_BAD_REGISTRY_PARAMETER"></span><span id="error_internet_bad_registry_parameter"></span>**ERROR\_INTERNET\_BAD\_REGISTRY\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-196">12022</span><span class="sxs-lookup"><span data-stu-id="92834-196">12022</span></span>
</dt> <dt>



<span data-ttu-id="92834-197">Um valor de registro necessário foi localizado, mas é um tipo incorreto ou tem um valor inválido.</span><span class="sxs-lookup"><span data-stu-id="92834-197">A required registry value was located but is an incorrect type or has an invalid value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-198"><span id="ERROR_INTERNET_CANNOT_CONNECT"></span><span id="error_internet_cannot_connect"></span>**ERRO a \_ Internet \_ não pode \_ se conectar**</span><span class="sxs-lookup"><span data-stu-id="92834-198"><span id="ERROR_INTERNET_CANNOT_CONNECT"></span><span id="error_internet_cannot_connect"></span>**ERROR\_INTERNET\_CANNOT\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-199">12029</span><span class="sxs-lookup"><span data-stu-id="92834-199">12029</span></span>
</dt> <dt>



<span data-ttu-id="92834-200">Falha na tentativa de conexão com o servidor.</span><span class="sxs-lookup"><span data-stu-id="92834-200">The attempt to connect to the server failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-201"><span id="ERROR_INTERNET_CHG_POST_IS_NON_SECURE"></span><span id="error_internet_chg_post_is_non_secure"></span>**ERRO o \_ Internet \_ CHG post não \_ \_ é \_ \_ seguro**</span><span class="sxs-lookup"><span data-stu-id="92834-201"><span id="ERROR_INTERNET_CHG_POST_IS_NON_SECURE"></span><span id="error_internet_chg_post_is_non_secure"></span>**ERROR\_INTERNET\_CHG\_POST\_IS\_NON\_SECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-202">12042</span><span class="sxs-lookup"><span data-stu-id="92834-202">12042</span></span>
</dt> <dt>



<span data-ttu-id="92834-203">O aplicativo está postando e tentando alterar várias linhas de texto em um servidor que não é seguro.</span><span class="sxs-lookup"><span data-stu-id="92834-203">The application is posting and attempting to change multiple lines of text on a server that is not secure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-204"><span id="ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_internet_client_auth_cert_needed"></span>**ERRO \_ de \_ certificado de autenticação de cliente de Internet \_ \_ \_ necessário**</span><span class="sxs-lookup"><span data-stu-id="92834-204"><span id="ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_internet_client_auth_cert_needed"></span>**ERROR\_INTERNET\_CLIENT\_AUTH\_CERT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-205">12044</span><span class="sxs-lookup"><span data-stu-id="92834-205">12044</span></span>
</dt> <dt>



<span data-ttu-id="92834-206">O servidor está solicitando a autenticação do cliente.</span><span class="sxs-lookup"><span data-stu-id="92834-206">The server is requesting client authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-207"><span id="ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP"></span><span id="error_internet_client_auth_not_setup"></span>**ERRO \_ autenticação do cliente da Internet \_ \_ \_ não \_ configurada**</span><span class="sxs-lookup"><span data-stu-id="92834-207"><span id="ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP"></span><span id="error_internet_client_auth_not_setup"></span>**ERROR\_INTERNET\_CLIENT\_AUTH\_NOT\_SETUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-208">12046</span><span class="sxs-lookup"><span data-stu-id="92834-208">12046</span></span>
</dt> <dt>



<span data-ttu-id="92834-209">A autorização do cliente não está configurada neste computador.</span><span class="sxs-lookup"><span data-stu-id="92834-209">Client authorization is not set up on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-210"><span id="ERROR_INTERNET_CONNECTION_ABORTED"></span><span id="error_internet_connection_aborted"></span>**ERRO \_ de \_ conexão com a Internet \_ abortado**</span><span class="sxs-lookup"><span data-stu-id="92834-210"><span id="ERROR_INTERNET_CONNECTION_ABORTED"></span><span id="error_internet_connection_aborted"></span>**ERROR\_INTERNET\_CONNECTION\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-211">12030</span><span class="sxs-lookup"><span data-stu-id="92834-211">12030</span></span>
</dt> <dt>



<span data-ttu-id="92834-212">A conexão com o servidor foi encerrada.</span><span class="sxs-lookup"><span data-stu-id="92834-212">The connection with the server has been terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-213"><span id="ERROR_INTERNET_CONNECTION_RESET"></span><span id="error_internet_connection_reset"></span>**ERRO \_ de \_ redefinição de conexão com a Internet \_**</span><span class="sxs-lookup"><span data-stu-id="92834-213"><span id="ERROR_INTERNET_CONNECTION_RESET"></span><span id="error_internet_connection_reset"></span>**ERROR\_INTERNET\_CONNECTION\_RESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-214">12031</span><span class="sxs-lookup"><span data-stu-id="92834-214">12031</span></span>
</dt> <dt>



<span data-ttu-id="92834-215">A conexão com o servidor foi redefinida.</span><span class="sxs-lookup"><span data-stu-id="92834-215">The connection with the server has been reset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-216"><span id="ERROR_INTERNET_DECODING_FAILED"></span><span id="error_internet_decoding_failed"></span>**ERRO \_ de \_ decodificação de Internet \_ com falha**</span><span class="sxs-lookup"><span data-stu-id="92834-216"><span id="ERROR_INTERNET_DECODING_FAILED"></span><span id="error_internet_decoding_failed"></span>**ERROR\_INTERNET\_DECODING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-217">12175</span><span class="sxs-lookup"><span data-stu-id="92834-217">12175</span></span>
</dt> <dt>



<span data-ttu-id="92834-218">O WinINet não pôde executar a decodificação de conteúdo na resposta.</span><span class="sxs-lookup"><span data-stu-id="92834-218">WinINet failed to perform content decoding on the response.</span></span> <span data-ttu-id="92834-219">Para obter mais informações, consulte o tópico [**codificação de conteúdo**](content-encoding.md) .</span><span class="sxs-lookup"><span data-stu-id="92834-219">For more information, see the [**Content Encoding**](content-encoding.md) topic.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-220"><span id="ERROR_INTERNET_DIALOG_PENDING"></span><span id="error_internet_dialog_pending"></span>**diálogo de Internet de erro \_ \_ \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="92834-220"><span id="ERROR_INTERNET_DIALOG_PENDING"></span><span id="error_internet_dialog_pending"></span>**ERROR\_INTERNET\_DIALOG\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-221">12049</span><span class="sxs-lookup"><span data-stu-id="92834-221">12049</span></span>
</dt> <dt>



<span data-ttu-id="92834-222">Outro thread tem uma caixa de diálogo de senha em andamento.</span><span class="sxs-lookup"><span data-stu-id="92834-222">Another thread has a password dialog box in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-223"><span id="ERROR_INTERNET_DISCONNECTED"></span><span id="error_internet_disconnected"></span>**ERRO de \_ Internet \_ desconectado**</span><span class="sxs-lookup"><span data-stu-id="92834-223"><span id="ERROR_INTERNET_DISCONNECTED"></span><span id="error_internet_disconnected"></span>**ERROR\_INTERNET\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-224">12163</span><span class="sxs-lookup"><span data-stu-id="92834-224">12163</span></span>
</dt> <dt>



<span data-ttu-id="92834-225">A conexão com a Internet foi perdida.</span><span class="sxs-lookup"><span data-stu-id="92834-225">The Internet connection has been lost.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-226"><span id="ERROR_INTERNET_EXTENDED_ERROR"></span><span id="error_internet_extended_error"></span>**erro \_ \_ estendido pela Internet \_**</span><span class="sxs-lookup"><span data-stu-id="92834-226"><span id="ERROR_INTERNET_EXTENDED_ERROR"></span><span id="error_internet_extended_error"></span>**ERROR\_INTERNET\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-227">12003</span><span class="sxs-lookup"><span data-stu-id="92834-227">12003</span></span>
</dt> <dt>



<span data-ttu-id="92834-228">Um erro estendido foi retornado do servidor.</span><span class="sxs-lookup"><span data-stu-id="92834-228">An extended error was returned from the server.</span></span> <span data-ttu-id="92834-229">Normalmente, é uma cadeia de caracteres ou um buffer que contém uma mensagem de erro detalhada.</span><span class="sxs-lookup"><span data-stu-id="92834-229">This is typically a string or buffer containing a verbose error message.</span></span> <span data-ttu-id="92834-230">Chame [**InternetGetLastResponseInfo**](/windows/desktop/api/Wininet/nf-wininet-internetgetlastresponseinfoa) para recuperar o texto do erro.</span><span class="sxs-lookup"><span data-stu-id="92834-230">Call [**InternetGetLastResponseInfo**](/windows/desktop/api/Wininet/nf-wininet-internetgetlastresponseinfoa) to retrieve the error text.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-231"><span id="ERROR_INTERNET_FAILED_DUETOSECURITYCHECK"></span><span id="error_internet_failed_duetosecuritycheck"></span>**ERRO \_ de \_ falha na Internet \_ DUETOSECURITYCHECK**</span><span class="sxs-lookup"><span data-stu-id="92834-231"><span id="ERROR_INTERNET_FAILED_DUETOSECURITYCHECK"></span><span id="error_internet_failed_duetosecuritycheck"></span>**ERROR\_INTERNET\_FAILED\_DUETOSECURITYCHECK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-232">12171</span><span class="sxs-lookup"><span data-stu-id="92834-232">12171</span></span>
</dt> <dt>



<span data-ttu-id="92834-233">A função falhou devido a uma verificação de segurança.</span><span class="sxs-lookup"><span data-stu-id="92834-233">The function failed due to a security check.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-234"><span id="ERROR_INTERNET_FORCE_RETRY"></span><span id="error_internet_force_retry"></span>**ERRO de \_ repetição de Internet \_ Force \_**</span><span class="sxs-lookup"><span data-stu-id="92834-234"><span id="ERROR_INTERNET_FORCE_RETRY"></span><span id="error_internet_force_retry"></span>**ERROR\_INTERNET\_FORCE\_RETRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-235">12032</span><span class="sxs-lookup"><span data-stu-id="92834-235">12032</span></span>
</dt> <dt>



<span data-ttu-id="92834-236">A função precisa refazer a solicitação.</span><span class="sxs-lookup"><span data-stu-id="92834-236">The function needs to redo the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-237"><span id="ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED"></span><span id="error_internet_fortezza_login_needed"></span>**ERRO \_ de \_ logon do Internet Fortezza \_ \_ necessário**</span><span class="sxs-lookup"><span data-stu-id="92834-237"><span id="ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED"></span><span id="error_internet_fortezza_login_needed"></span>**ERROR\_INTERNET\_FORTEZZA\_LOGIN\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-238">12054</span><span class="sxs-lookup"><span data-stu-id="92834-238">12054</span></span>
</dt> <dt>



<span data-ttu-id="92834-239">O recurso solicitado requer autenticação Fortezza.</span><span class="sxs-lookup"><span data-stu-id="92834-239">The requested resource requires Fortezza authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-240"><span id="ERROR_INTERNET_HANDLE_EXISTS"></span><span id="error_internet_handle_exists"></span>**ERRO \_ o \_ identificador da Internet \_ existe**</span><span class="sxs-lookup"><span data-stu-id="92834-240"><span id="ERROR_INTERNET_HANDLE_EXISTS"></span><span id="error_internet_handle_exists"></span>**ERROR\_INTERNET\_HANDLE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-241">12036</span><span class="sxs-lookup"><span data-stu-id="92834-241">12036</span></span>
</dt> <dt>



<span data-ttu-id="92834-242">A solicitação falhou porque o identificador já existe.</span><span class="sxs-lookup"><span data-stu-id="92834-242">The request failed because the handle already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-243"><span id="ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR"></span><span id="error_internet_http_to_https_on_redir"></span>**ERRO \_ \_ de http \_ da Internet para \_ https \_ no \_ REDIR**</span><span class="sxs-lookup"><span data-stu-id="92834-243"><span id="ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR"></span><span id="error_internet_http_to_https_on_redir"></span>**ERROR\_INTERNET\_HTTP\_TO\_HTTPS\_ON\_REDIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-244">12039</span><span class="sxs-lookup"><span data-stu-id="92834-244">12039</span></span>
</dt> <dt>



<span data-ttu-id="92834-245">O aplicativo está mudando de um não SSL para uma conexão SSL devido a um redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="92834-245">The application is moving from a non-SSL to an SSL connection because of a redirect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-246"><span id="ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR"></span><span id="error_internet_https_http_submit_redir"></span>**ERRO \_ de \_ \_ envio de http https \_ de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="92834-246"><span id="ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR"></span><span id="error_internet_https_http_submit_redir"></span>**ERROR\_INTERNET\_HTTPS\_HTTP\_SUBMIT\_REDIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-247">12052</span><span class="sxs-lookup"><span data-stu-id="92834-247">12052</span></span>
</dt> <dt>



<span data-ttu-id="92834-248">Os dados que estão sendo enviados para uma conexão SSL estão sendo redirecionados para uma conexão não SSL.</span><span class="sxs-lookup"><span data-stu-id="92834-248">The data being submitted to an SSL connection is being redirected to a non-SSL connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-249"><span id="ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR"></span><span id="error_internet_https_to_http_on_redir"></span>**ERRO de \_ Internet \_ https \_ para \_ http \_ em \_ REDIR**</span><span class="sxs-lookup"><span data-stu-id="92834-249"><span id="ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR"></span><span id="error_internet_https_to_http_on_redir"></span>**ERROR\_INTERNET\_HTTPS\_TO\_HTTP\_ON\_REDIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-250">12040</span><span class="sxs-lookup"><span data-stu-id="92834-250">12040</span></span>
</dt> <dt>



<span data-ttu-id="92834-251">O aplicativo está mudando de um SSL para uma conexão não SSL devido a um redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="92834-251">The application is moving from an SSL to an non-SSL connection because of a redirect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-252"><span id="ERROR_INTERNET_INCORRECT_FORMAT"></span><span id="error_internet_incorrect_format"></span>**ERRO \_ de \_ formato incorreto da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="92834-252"><span id="ERROR_INTERNET_INCORRECT_FORMAT"></span><span id="error_internet_incorrect_format"></span>**ERROR\_INTERNET\_INCORRECT\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-253">12027</span><span class="sxs-lookup"><span data-stu-id="92834-253">12027</span></span>
</dt> <dt>



<span data-ttu-id="92834-254">O formato da solicitação é inválido.</span><span class="sxs-lookup"><span data-stu-id="92834-254">The format of the request is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-255"><span id="ERROR_INTERNET_INCORRECT_HANDLE_STATE"></span><span id="error_internet_incorrect_handle_state"></span>**ERRO \_ no \_ \_ estado do identificador incorreto da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="92834-255"><span id="ERROR_INTERNET_INCORRECT_HANDLE_STATE"></span><span id="error_internet_incorrect_handle_state"></span>**ERROR\_INTERNET\_INCORRECT\_HANDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-256">12019</span><span class="sxs-lookup"><span data-stu-id="92834-256">12019</span></span>
</dt> <dt>



<span data-ttu-id="92834-257">A operação solicitada não pode ser executada porque o identificador fornecido não está no estado correto.</span><span class="sxs-lookup"><span data-stu-id="92834-257">The requested operation cannot be carried out because the handle supplied is not in the correct state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-258"><span id="ERROR_INTERNET_INCORRECT_HANDLE_TYPE"></span><span id="error_internet_incorrect_handle_type"></span>**ERRO \_ de \_ \_ tipo de identificador incorreto da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="92834-258"><span id="ERROR_INTERNET_INCORRECT_HANDLE_TYPE"></span><span id="error_internet_incorrect_handle_type"></span>**ERROR\_INTERNET\_INCORRECT\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-259">12018</span><span class="sxs-lookup"><span data-stu-id="92834-259">12018</span></span>
</dt> <dt>



<span data-ttu-id="92834-260">O tipo de identificador fornecido está incorreto para esta operação.</span><span class="sxs-lookup"><span data-stu-id="92834-260">The type of handle supplied is incorrect for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-261"><span id="ERROR_INTERNET_INCORRECT_PASSWORD"></span><span id="error_internet_incorrect_password"></span>**ERRO \_ de \_ senha incorreta na Internet \_**</span><span class="sxs-lookup"><span data-stu-id="92834-261"><span id="ERROR_INTERNET_INCORRECT_PASSWORD"></span><span id="error_internet_incorrect_password"></span>**ERROR\_INTERNET\_INCORRECT\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-262">12014</span><span class="sxs-lookup"><span data-stu-id="92834-262">12014</span></span>
</dt> <dt>



<span data-ttu-id="92834-263">A solicitação para se conectar e fazer logon em um servidor FTP não pôde ser concluída porque a senha fornecida está incorreta.</span><span class="sxs-lookup"><span data-stu-id="92834-263">The request to connect and log on to an FTP server could not be completed because the supplied password is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-264"><span id="ERROR_INTERNET_INCORRECT_USER_NAME"></span><span id="error_internet_incorrect_user_name"></span>**ERRO \_ de \_ \_ nome de usuário incorreto da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="92834-264"><span id="ERROR_INTERNET_INCORRECT_USER_NAME"></span><span id="error_internet_incorrect_user_name"></span>**ERROR\_INTERNET\_INCORRECT\_USER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-265">12013</span><span class="sxs-lookup"><span data-stu-id="92834-265">12013</span></span>
</dt> <dt>



<span data-ttu-id="92834-266">A solicitação para se conectar e fazer logon em um servidor FTP não pôde ser concluída porque o nome de usuário fornecido está incorreto.</span><span class="sxs-lookup"><span data-stu-id="92834-266">The request to connect and log on to an FTP server could not be completed because the supplied user name is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-267"><span id="ERROR_INTERNET_INSERT_CDROM"></span><span id="error_internet_insert_cdrom"></span>**ERRO \_ ao \_ Inserir \_ CD-ROM**</span><span class="sxs-lookup"><span data-stu-id="92834-267"><span id="ERROR_INTERNET_INSERT_CDROM"></span><span id="error_internet_insert_cdrom"></span>**ERROR\_INTERNET\_INSERT\_CDROM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-268">12053</span><span class="sxs-lookup"><span data-stu-id="92834-268">12053</span></span>
</dt> <dt>



<span data-ttu-id="92834-269">A solicitação exige que um CD-ROM seja inserido na unidade de CD-ROM para localizar o recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="92834-269">The request requires a CD-ROM to be inserted in the CD-ROM drive to locate the resource requested.</span></span>

> [!Note]  
> <span data-ttu-id="92834-270">Somente Windows Vista e Windows Server 2008 e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="92834-270">Windows Vista and Windows Server 2008 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-271"><span id="ERROR_INTERNET_INTERNAL_ERROR"></span><span id="error_internet_internal_error"></span>**erro \_ interno da Internet de erro \_ \_**</span><span class="sxs-lookup"><span data-stu-id="92834-271"><span id="ERROR_INTERNET_INTERNAL_ERROR"></span><span id="error_internet_internal_error"></span>**ERROR\_INTERNET\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-272">12004</span><span class="sxs-lookup"><span data-stu-id="92834-272">12004</span></span>
</dt> <dt>



<span data-ttu-id="92834-273">Ocorreu um erro interno.</span><span class="sxs-lookup"><span data-stu-id="92834-273">An internal error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-274"><span id="ERROR_INTERNET_INVALID_CA"></span><span id="error_internet_invalid_ca"></span>**ERRO \_ de \_ AC inválida \_ da Internet**</span><span class="sxs-lookup"><span data-stu-id="92834-274"><span id="ERROR_INTERNET_INVALID_CA"></span><span id="error_internet_invalid_ca"></span>**ERROR\_INTERNET\_INVALID\_CA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-275">12045</span><span class="sxs-lookup"><span data-stu-id="92834-275">12045</span></span>
</dt> <dt>



<span data-ttu-id="92834-276">A função não está familiarizada com a autoridade de certificação que gerou o certificado do servidor.</span><span class="sxs-lookup"><span data-stu-id="92834-276">The function is unfamiliar with the Certificate Authority that generated the server's certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-277"><span id="ERROR_INTERNET_INVALID_OPERATION"></span><span id="error_internet_invalid_operation"></span>**ERRO \_ de \_ operação inválida na Internet \_**</span><span class="sxs-lookup"><span data-stu-id="92834-277"><span id="ERROR_INTERNET_INVALID_OPERATION"></span><span id="error_internet_invalid_operation"></span>**ERROR\_INTERNET\_INVALID\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-278">12016</span><span class="sxs-lookup"><span data-stu-id="92834-278">12016</span></span>
</dt> <dt>



<span data-ttu-id="92834-279">A operação solicitada é inválida.</span><span class="sxs-lookup"><span data-stu-id="92834-279">The requested operation is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-280"><span id="ERROR_INTERNET_INVALID_OPTION"></span><span id="error_internet_invalid_option"></span>**ERRO de \_ opção de Internet \_ inválida \_**</span><span class="sxs-lookup"><span data-stu-id="92834-280"><span id="ERROR_INTERNET_INVALID_OPTION"></span><span id="error_internet_invalid_option"></span>**ERROR\_INTERNET\_INVALID\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-281">12009</span><span class="sxs-lookup"><span data-stu-id="92834-281">12009</span></span>
</dt> <dt>



<span data-ttu-id="92834-282">Uma solicitação para [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) ou [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) especificou um valor de opção inválido.</span><span class="sxs-lookup"><span data-stu-id="92834-282">A request to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) or [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) specified an invalid option value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-283"><span id="ERROR_INTERNET_INVALID_PROXY_REQUEST"></span><span id="error_internet_invalid_proxy_request"></span>**ERRO \_ na \_ \_ solicitação de proxy inválida da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="92834-283"><span id="ERROR_INTERNET_INVALID_PROXY_REQUEST"></span><span id="error_internet_invalid_proxy_request"></span>**ERROR\_INTERNET\_INVALID\_PROXY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-284">12033</span><span class="sxs-lookup"><span data-stu-id="92834-284">12033</span></span>
</dt> <dt>



<span data-ttu-id="92834-285">A solicitação para o proxy era inválida.</span><span class="sxs-lookup"><span data-stu-id="92834-285">The request to the proxy was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-286"><span id="ERROR_INTERNET_INVALID_URL"></span><span id="error_internet_invalid_url"></span>**\_ \_ URL inválida da Internet de erro \_**</span><span class="sxs-lookup"><span data-stu-id="92834-286"><span id="ERROR_INTERNET_INVALID_URL"></span><span id="error_internet_invalid_url"></span>**ERROR\_INTERNET\_INVALID\_URL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-287">12005</span><span class="sxs-lookup"><span data-stu-id="92834-287">12005</span></span>
</dt> <dt>



<span data-ttu-id="92834-288">A URL é inválida.</span><span class="sxs-lookup"><span data-stu-id="92834-288">The URL is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-289"><span id="ERROR_INTERNET_ITEM_NOT_FOUND"></span><span id="error_internet_item_not_found"></span>**ITEM de Internet de erro \_ \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="92834-289"><span id="ERROR_INTERNET_ITEM_NOT_FOUND"></span><span id="error_internet_item_not_found"></span>**ERROR\_INTERNET\_ITEM\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-290">12028</span><span class="sxs-lookup"><span data-stu-id="92834-290">12028</span></span>
</dt> <dt>



<span data-ttu-id="92834-291">Não foi possível localizar o item solicitado.</span><span class="sxs-lookup"><span data-stu-id="92834-291">The requested item could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-292"><span id="ERROR_INTERNET_LOGIN_FAILURE"></span><span id="error_internet_login_failure"></span>**ERRO \_ de \_ logon \_ na Internet**</span><span class="sxs-lookup"><span data-stu-id="92834-292"><span id="ERROR_INTERNET_LOGIN_FAILURE"></span><span id="error_internet_login_failure"></span>**ERROR\_INTERNET\_LOGIN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-293">12015</span><span class="sxs-lookup"><span data-stu-id="92834-293">12015</span></span>
</dt> <dt>



<span data-ttu-id="92834-294">A solicitação para se conectar e fazer logon em um servidor FTP falhou.</span><span class="sxs-lookup"><span data-stu-id="92834-294">The request to connect and log on to an FTP server failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-295"><span id="ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="error_internet_login_failure_display_entity_body"></span>**ERRO \_ de \_ logon \_ na Internet falha ao \_ Exibir o \_ corpo da entidade \_**</span><span class="sxs-lookup"><span data-stu-id="92834-295"><span id="ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="error_internet_login_failure_display_entity_body"></span>**ERROR\_INTERNET\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-296">12174</span><span class="sxs-lookup"><span data-stu-id="92834-296">12174</span></span>
</dt> <dt>



<span data-ttu-id="92834-297">O cabeçalho do Resumo de MS-Logoff foi retornado do site.</span><span class="sxs-lookup"><span data-stu-id="92834-297">The MS-Logoff digest header has been returned from the website.</span></span> <span data-ttu-id="92834-298">Esse cabeçalho instrui especificamente o pacote de resumo para limpar as credenciais do Realm associado.</span><span class="sxs-lookup"><span data-stu-id="92834-298">This header specifically instructs the digest package to purge credentials for the associated realm.</span></span> <span data-ttu-id="92834-299">Esse erro será retornado somente se a opção de [ \_ falha de logon máscara de erro da Internet exibir o \_ \_ \_ \_ \_ \_ corpo da entidade](option-flags.md) tiver sido definida; caso contrário, será retornada uma falha de **\_ \_ logon \_ na Internet** .</span><span class="sxs-lookup"><span data-stu-id="92834-299">This error will only be returned if [INTERNET\_ERROR\_MASK\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY](option-flags.md) option has been set; otherwise, **ERROR\_INTERNET\_LOGIN\_FAILURE** is returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-300"><span id="ERROR_INTERNET_MIXED_SECURITY"></span><span id="error_internet_mixed_security"></span>**ERRO \_ de \_ segurança mista na Internet \_**</span><span class="sxs-lookup"><span data-stu-id="92834-300"><span id="ERROR_INTERNET_MIXED_SECURITY"></span><span id="error_internet_mixed_security"></span>**ERROR\_INTERNET\_MIXED\_SECURITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-301">12041</span><span class="sxs-lookup"><span data-stu-id="92834-301">12041</span></span>
</dt> <dt>



<span data-ttu-id="92834-302">O conteúdo não é totalmente seguro.</span><span class="sxs-lookup"><span data-stu-id="92834-302">The content is not entirely secure.</span></span> <span data-ttu-id="92834-303">Parte do conteúdo visualizado pode ter vindo de servidores não seguros.</span><span class="sxs-lookup"><span data-stu-id="92834-303">Some of the content being viewed may have come from unsecured servers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-304"><span id="ERROR_INTERNET_NAME_NOT_RESOLVED"></span><span id="error_internet_name_not_resolved"></span>**ERRO \_ nome da Internet \_ \_ não \_ resolvido**</span><span class="sxs-lookup"><span data-stu-id="92834-304"><span id="ERROR_INTERNET_NAME_NOT_RESOLVED"></span><span id="error_internet_name_not_resolved"></span>**ERROR\_INTERNET\_NAME\_NOT\_RESOLVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-305">12007</span><span class="sxs-lookup"><span data-stu-id="92834-305">12007</span></span>
</dt> <dt>



<span data-ttu-id="92834-306">Não foi possível resolver o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="92834-306">The server name could not be resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-307"><span id="ERROR_INTERNET_NEED_MSN_SSPI_PKG"></span><span id="error_internet_need_msn_sspi_pkg"></span>**ERRO a \_ Internet \_ precisa do \_ \_ pacote SSPI do MSN \_**</span><span class="sxs-lookup"><span data-stu-id="92834-307"><span id="ERROR_INTERNET_NEED_MSN_SSPI_PKG"></span><span id="error_internet_need_msn_sspi_pkg"></span>**ERROR\_INTERNET\_NEED\_MSN\_SSPI\_PKG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-308">12173</span><span class="sxs-lookup"><span data-stu-id="92834-308">12173</span></span>
</dt> <dt>



<span data-ttu-id="92834-309">Não implementado atualmente.</span><span class="sxs-lookup"><span data-stu-id="92834-309">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-310"><span id="ERROR_INTERNET_NEED_UI"></span><span id="error_internet_need_ui"></span>**ERRO \_ na \_ \_ interface do usuário da Internet**</span><span class="sxs-lookup"><span data-stu-id="92834-310"><span id="ERROR_INTERNET_NEED_UI"></span><span id="error_internet_need_ui"></span>**ERROR\_INTERNET\_NEED\_UI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-311">12034</span><span class="sxs-lookup"><span data-stu-id="92834-311">12034</span></span>
</dt> <dt>



<span data-ttu-id="92834-312">Uma interface do usuário ou outra operação de bloqueio foi solicitada.</span><span class="sxs-lookup"><span data-stu-id="92834-312">A user interface or other blocking operation has been requested.</span></span>

> [!Note]  
> <span data-ttu-id="92834-313">Somente Windows Vista e Windows Server 2008 e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="92834-313">Windows Vista and Windows Server 2008 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-314"><span id="ERROR_INTERNET_NO_CALLBACK"></span><span id="error_internet_no_callback"></span>**ERRO de \_ Internet \_ sem retorno de \_ chamada**</span><span class="sxs-lookup"><span data-stu-id="92834-314"><span id="ERROR_INTERNET_NO_CALLBACK"></span><span id="error_internet_no_callback"></span>**ERROR\_INTERNET\_NO\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-315">12025</span><span class="sxs-lookup"><span data-stu-id="92834-315">12025</span></span>
</dt> <dt>



<span data-ttu-id="92834-316">Uma solicitação assíncrona não pôde ser feita porque uma função de retorno de chamada não foi definida.</span><span class="sxs-lookup"><span data-stu-id="92834-316">An asynchronous request could not be made because a callback function has not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-317"><span id="ERROR_INTERNET_NO_CONTEXT"></span><span id="error_internet_no_context"></span>**ERRO de \_ Internet \_ sem \_ contexto**</span><span class="sxs-lookup"><span data-stu-id="92834-317"><span id="ERROR_INTERNET_NO_CONTEXT"></span><span id="error_internet_no_context"></span>**ERROR\_INTERNET\_NO\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-318">12024</span><span class="sxs-lookup"><span data-stu-id="92834-318">12024</span></span>
</dt> <dt>



<span data-ttu-id="92834-319">Uma solicitação assíncrona não pôde ser feita porque um valor de contexto zero foi fornecido.</span><span class="sxs-lookup"><span data-stu-id="92834-319">An asynchronous request could not be made because a zero context value was supplied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-320"><span id="ERROR_INTERNET_NO_DIRECT_ACCESS"></span><span id="error_internet_no_direct_access"></span>**ERRO \_ de \_ Internet \_ sem \_ acesso direto**</span><span class="sxs-lookup"><span data-stu-id="92834-320"><span id="ERROR_INTERNET_NO_DIRECT_ACCESS"></span><span id="error_internet_no_direct_access"></span>**ERROR\_INTERNET\_NO\_DIRECT\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-321">12023</span><span class="sxs-lookup"><span data-stu-id="92834-321">12023</span></span>
</dt> <dt>



<span data-ttu-id="92834-322">O acesso direto à rede não pode ser feito neste momento.</span><span class="sxs-lookup"><span data-stu-id="92834-322">Direct network access cannot be made at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-323"><span id="ERROR_INTERNET_NOT_INITIALIZED"></span><span id="error_internet_not_initialized"></span>**ERRO na \_ Internet \_ não \_ inicializado**</span><span class="sxs-lookup"><span data-stu-id="92834-323"><span id="ERROR_INTERNET_NOT_INITIALIZED"></span><span id="error_internet_not_initialized"></span>**ERROR\_INTERNET\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-324">12172</span><span class="sxs-lookup"><span data-stu-id="92834-324">12172</span></span>
</dt> <dt>



<span data-ttu-id="92834-325">A inicialização da API do WinINet não ocorreu.</span><span class="sxs-lookup"><span data-stu-id="92834-325">Initialization of the WinINet API has not occurred.</span></span> <span data-ttu-id="92834-326">Indica que uma função de nível superior, como [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), ainda não foi chamada.</span><span class="sxs-lookup"><span data-stu-id="92834-326">Indicates that a higher-level function, such as [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), has not been called yet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-327"><span id="ERROR_INTERNET_NOT_PROXY_REQUEST"></span><span id="error_internet_not_proxy_request"></span>**ERRO \_ na \_ \_ solicitação de proxy \_ da Internet**</span><span class="sxs-lookup"><span data-stu-id="92834-327"><span id="ERROR_INTERNET_NOT_PROXY_REQUEST"></span><span id="error_internet_not_proxy_request"></span>**ERROR\_INTERNET\_NOT\_PROXY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-328">12020</span><span class="sxs-lookup"><span data-stu-id="92834-328">12020</span></span>
</dt> <dt>



<span data-ttu-id="92834-329">A solicitação não pode ser feita por meio de um proxy.</span><span class="sxs-lookup"><span data-stu-id="92834-329">The request cannot be made via a proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-330"><span id="ERROR_INTERNET_OPERATION_CANCELLED"></span><span id="error_internet_operation_cancelled"></span>**ERRO \_ na \_ operação de Internet \_ cancelada**</span><span class="sxs-lookup"><span data-stu-id="92834-330"><span id="ERROR_INTERNET_OPERATION_CANCELLED"></span><span id="error_internet_operation_cancelled"></span>**ERROR\_INTERNET\_OPERATION\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-331">12017</span><span class="sxs-lookup"><span data-stu-id="92834-331">12017</span></span>
</dt> <dt>



<span data-ttu-id="92834-332">A operação foi cancelada, geralmente porque o identificador no qual a solicitação estava operando foi fechado antes da operação ser concluída.</span><span class="sxs-lookup"><span data-stu-id="92834-332">The operation was canceled, usually because the handle on which the request was operating was closed before the operation completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-333"><span id="ERROR_INTERNET_OPTION_NOT_SETTABLE"></span><span id="error_internet_option_not_settable"></span>**ERRO \_ na \_ opção da Internet \_ não \_ configurável**</span><span class="sxs-lookup"><span data-stu-id="92834-333"><span id="ERROR_INTERNET_OPTION_NOT_SETTABLE"></span><span id="error_internet_option_not_settable"></span>**ERROR\_INTERNET\_OPTION\_NOT\_SETTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-334">12011</span><span class="sxs-lookup"><span data-stu-id="92834-334">12011</span></span>
</dt> <dt>



<span data-ttu-id="92834-335">A opção solicitada não pode ser definida, somente consultada.</span><span class="sxs-lookup"><span data-stu-id="92834-335">The requested option cannot be set, only queried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-336"><span id="ERROR_INTERNET_OUT_OF_HANDLES"></span><span id="error_internet_out_of_handles"></span>**ERRO \_ \_ de Internet fora \_ de \_ identificadores**</span><span class="sxs-lookup"><span data-stu-id="92834-336"><span id="ERROR_INTERNET_OUT_OF_HANDLES"></span><span id="error_internet_out_of_handles"></span>**ERROR\_INTERNET\_OUT\_OF\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-337">12001</span><span class="sxs-lookup"><span data-stu-id="92834-337">12001</span></span>
</dt> <dt>



<span data-ttu-id="92834-338">Não foi possível gerar mais identificadores neste momento.</span><span class="sxs-lookup"><span data-stu-id="92834-338">No more handles could be generated at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-339"><span id="ERROR_INTERNET_POST_IS_NON_SECURE"></span><span id="error_internet_post_is_non_secure"></span>**ERRO \_ a \_ postagem na Internet \_ \_ não é \_ segura**</span><span class="sxs-lookup"><span data-stu-id="92834-339"><span id="ERROR_INTERNET_POST_IS_NON_SECURE"></span><span id="error_internet_post_is_non_secure"></span>**ERROR\_INTERNET\_POST\_IS\_NON\_SECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-340">12043</span><span class="sxs-lookup"><span data-stu-id="92834-340">12043</span></span>
</dt> <dt>



<span data-ttu-id="92834-341">O aplicativo está postando dados em um servidor que não é seguro.</span><span class="sxs-lookup"><span data-stu-id="92834-341">The application is posting data to a server that is not secure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-342"><span id="ERROR_INTERNET_PROTOCOL_NOT_FOUND"></span><span id="error_internet_protocol_not_found"></span>**ERRO \_ de \_ protocolo de Internet \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="92834-342"><span id="ERROR_INTERNET_PROTOCOL_NOT_FOUND"></span><span id="error_internet_protocol_not_found"></span>**ERROR\_INTERNET\_PROTOCOL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-343">12008</span><span class="sxs-lookup"><span data-stu-id="92834-343">12008</span></span>
</dt> <dt>



<span data-ttu-id="92834-344">Não foi possível localizar o protocolo solicitado.</span><span class="sxs-lookup"><span data-stu-id="92834-344">The requested protocol could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-345"><span id="ERROR_INTERNET_PROXY_SERVER_UNREACHABLE"></span><span id="error_internet_proxy_server_unreachable"></span>**ERRO \_ de \_ servidor proxy da Internet \_ \_ inacessível**</span><span class="sxs-lookup"><span data-stu-id="92834-345"><span id="ERROR_INTERNET_PROXY_SERVER_UNREACHABLE"></span><span id="error_internet_proxy_server_unreachable"></span>**ERROR\_INTERNET\_PROXY\_SERVER\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-346">12165</span><span class="sxs-lookup"><span data-stu-id="92834-346">12165</span></span>
</dt> <dt>



<span data-ttu-id="92834-347">O servidor proxy designado não pode ser acessado.</span><span class="sxs-lookup"><span data-stu-id="92834-347">The designated proxy server cannot be reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-348"><span id="ERROR_INTERNET_REDIRECT_SCHEME_CHANGE"></span><span id="error_internet_redirect_scheme_change"></span>**ERRO \_ de \_ \_ alteração do esquema de redirecionamento da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="92834-348"><span id="ERROR_INTERNET_REDIRECT_SCHEME_CHANGE"></span><span id="error_internet_redirect_scheme_change"></span>**ERROR\_INTERNET\_REDIRECT\_SCHEME\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-349">12048</span><span class="sxs-lookup"><span data-stu-id="92834-349">12048</span></span>
</dt> <dt>



<span data-ttu-id="92834-350">A função não pôde lidar com o redirecionamento, pois o esquema foi alterado (por exemplo, HTTP para FTP).</span><span class="sxs-lookup"><span data-stu-id="92834-350">The function could not handle the redirection, because the scheme changed (for example, HTTP to FTP).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-351"><span id="ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND"></span><span id="error_internet_registry_value_not_found"></span>**ERRO \_ o \_ valor do registro da Internet \_ \_ não \_ foi encontrado**</span><span class="sxs-lookup"><span data-stu-id="92834-351"><span id="ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND"></span><span id="error_internet_registry_value_not_found"></span>**ERROR\_INTERNET\_REGISTRY\_VALUE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-352">12021</span><span class="sxs-lookup"><span data-stu-id="92834-352">12021</span></span>
</dt> <dt>



<span data-ttu-id="92834-353">Um valor de registro necessário não pôde ser localizado.</span><span class="sxs-lookup"><span data-stu-id="92834-353">A required registry value could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-354"><span id="ERROR_INTERNET_REQUEST_PENDING"></span><span id="error_internet_request_pending"></span>**ERRO \_ de \_ solicitação de Internet \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="92834-354"><span id="ERROR_INTERNET_REQUEST_PENDING"></span><span id="error_internet_request_pending"></span>**ERROR\_INTERNET\_REQUEST\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-355">12026</span><span class="sxs-lookup"><span data-stu-id="92834-355">12026</span></span>
</dt> <dt>



<span data-ttu-id="92834-356">A operação necessária não pôde ser concluída porque uma ou mais solicitações estão pendentes.</span><span class="sxs-lookup"><span data-stu-id="92834-356">The required operation could not be completed because one or more requests are pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-357"><span id="ERROR_INTERNET_RETRY_DIALOG"></span><span id="error_internet_retry_dialog"></span>**\_diálogo de \_ repetição de Internet de erro \_**</span><span class="sxs-lookup"><span data-stu-id="92834-357"><span id="ERROR_INTERNET_RETRY_DIALOG"></span><span id="error_internet_retry_dialog"></span>**ERROR\_INTERNET\_RETRY\_DIALOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-358">12050</span><span class="sxs-lookup"><span data-stu-id="92834-358">12050</span></span>
</dt> <dt>



<span data-ttu-id="92834-359">A caixa de diálogo deve ser repetida.</span><span class="sxs-lookup"><span data-stu-id="92834-359">The dialog box should be retried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-360"><span id="ERROR_INTERNET_SEC_CERT_CN_INVALID"></span><span id="error_internet_sec_cert_cn_invalid"></span>**ERRO \_ CN do certificado da Internet \_ SEC \_ \_ \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="92834-360"><span id="ERROR_INTERNET_SEC_CERT_CN_INVALID"></span><span id="error_internet_sec_cert_cn_invalid"></span>**ERROR\_INTERNET\_SEC\_CERT\_CN\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-361">12038</span><span class="sxs-lookup"><span data-stu-id="92834-361">12038</span></span>
</dt> <dt>



<span data-ttu-id="92834-362">O nome comum do certificado SSL (campo nome do host) está incorreto por exemplo, se você inseriu www.server.com e o nome comum no certificado diz www.different.com.</span><span class="sxs-lookup"><span data-stu-id="92834-362">SSL certificate common name (host name field) is incorrect for example, if you entered www.server.com and the common name on the certificate says www.different.com.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-363"><span id="ERROR_INTERNET_SEC_CERT_DATE_INVALID"></span><span id="error_internet_sec_cert_date_invalid"></span>**ERRO de data de CERT. de \_ Internet \_ \_ \_ \_ inválida**</span><span class="sxs-lookup"><span data-stu-id="92834-363"><span id="ERROR_INTERNET_SEC_CERT_DATE_INVALID"></span><span id="error_internet_sec_cert_date_invalid"></span>**ERROR\_INTERNET\_SEC\_CERT\_DATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-364">12037</span><span class="sxs-lookup"><span data-stu-id="92834-364">12037</span></span>
</dt> <dt>



<span data-ttu-id="92834-365">A data do certificado SSL que foi recebida do servidor é inadequada.</span><span class="sxs-lookup"><span data-stu-id="92834-365">SSL certificate date that was received from the server is bad.</span></span> <span data-ttu-id="92834-366">O certificado expirou.</span><span class="sxs-lookup"><span data-stu-id="92834-366">The certificate is expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-367"><span id="ERROR_INTERNET_SEC_CERT_ERRORS"></span><span id="error_internet_sec_cert_errors"></span>**\_erros de certificados da Internet \_ SEC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="92834-367"><span id="ERROR_INTERNET_SEC_CERT_ERRORS"></span><span id="error_internet_sec_cert_errors"></span>**ERROR\_INTERNET\_SEC\_CERT\_ERRORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-368">12055</span><span class="sxs-lookup"><span data-stu-id="92834-368">12055</span></span>
</dt> <dt>



<span data-ttu-id="92834-369">O certificado SSL contém erros.</span><span class="sxs-lookup"><span data-stu-id="92834-369">The SSL certificate contains errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-370"><span id="ERROR_INTERNET_SEC_CERT_NO_REV"></span><span id="error_internet_sec_cert_no_rev"></span>**ERRO na \_ Internet \_ s CERT. \_ \_ sem \_ Rev.**</span><span class="sxs-lookup"><span data-stu-id="92834-370"><span id="ERROR_INTERNET_SEC_CERT_NO_REV"></span><span id="error_internet_sec_cert_no_rev"></span>**ERROR\_INTERNET\_SEC\_CERT\_NO\_REV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-371">12056</span><span class="sxs-lookup"><span data-stu-id="92834-371">12056</span></span>
</dt> <dt>



<span data-ttu-id="92834-372">O certificado SSL não foi revogado.</span><span class="sxs-lookup"><span data-stu-id="92834-372">The SSL certificate was not revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-373"><span id="ERROR_INTERNET_SEC_CERT_REV_FAILED"></span><span id="error_internet_sec_cert_rev_failed"></span>**ERRO a Rev. de \_ certificado da Internet \_ SEC \_ \_ \_ falhou**</span><span class="sxs-lookup"><span data-stu-id="92834-373"><span id="ERROR_INTERNET_SEC_CERT_REV_FAILED"></span><span id="error_internet_sec_cert_rev_failed"></span>**ERROR\_INTERNET\_SEC\_CERT\_REV\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-374">12057</span><span class="sxs-lookup"><span data-stu-id="92834-374">12057</span></span>
</dt> <dt>



<span data-ttu-id="92834-375">Falha na revogação do certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="92834-375">Revocation of the SSL certificate failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-376"><span id="ERROR_INTERNET_SEC_CERT_REVOKED"></span><span id="error_internet_sec_cert_revoked"></span>**ERRO na \_ Internet \_ SEC \_ CERT \_ revogado**</span><span class="sxs-lookup"><span data-stu-id="92834-376"><span id="ERROR_INTERNET_SEC_CERT_REVOKED"></span><span id="error_internet_sec_cert_revoked"></span>**ERROR\_INTERNET\_SEC\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-377">12170</span><span class="sxs-lookup"><span data-stu-id="92834-377">12170</span></span>
</dt> <dt>



<span data-ttu-id="92834-378">O certificado SSL foi revogado.</span><span class="sxs-lookup"><span data-stu-id="92834-378">The SSL certificate was revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-379"><span id="ERROR_INTERNET_SEC_INVALID_CERT"></span><span id="error_internet_sec_invalid_cert"></span>**ERRO na \_ Internet \_ SEC \_ inválida \_**</span><span class="sxs-lookup"><span data-stu-id="92834-379"><span id="ERROR_INTERNET_SEC_INVALID_CERT"></span><span id="error_internet_sec_invalid_cert"></span>**ERROR\_INTERNET\_SEC\_INVALID\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-380">12169</span><span class="sxs-lookup"><span data-stu-id="92834-380">12169</span></span>
</dt> <dt>



<span data-ttu-id="92834-381">O certificado SSL é inválido.</span><span class="sxs-lookup"><span data-stu-id="92834-381">The SSL certificate is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-382"><span id="ERROR_INTERNET_SECURITY_CHANNEL_ERROR"></span><span id="error_internet_security_channel_error"></span>**erro no erro de canal de segurança da \_ Internet \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="92834-382"><span id="ERROR_INTERNET_SECURITY_CHANNEL_ERROR"></span><span id="error_internet_security_channel_error"></span>**ERROR\_INTERNET\_SECURITY\_CHANNEL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-383">12157</span><span class="sxs-lookup"><span data-stu-id="92834-383">12157</span></span>
</dt> <dt>



<span data-ttu-id="92834-384">O aplicativo sofreu um erro interno ao carregar as bibliotecas SSL.</span><span class="sxs-lookup"><span data-stu-id="92834-384">The application experienced an internal error loading the SSL libraries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-385"><span id="ERROR_INTERNET_SERVER_UNREACHABLE"></span><span id="error_internet_server_unreachable"></span>**ERRO \_ de \_ servidor de Internet \_ inacessível**</span><span class="sxs-lookup"><span data-stu-id="92834-385"><span id="ERROR_INTERNET_SERVER_UNREACHABLE"></span><span id="error_internet_server_unreachable"></span>**ERROR\_INTERNET\_SERVER\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-386">12164</span><span class="sxs-lookup"><span data-stu-id="92834-386">12164</span></span>
</dt> <dt>



<span data-ttu-id="92834-387">O site ou servidor indicado está inacessível.</span><span class="sxs-lookup"><span data-stu-id="92834-387">The website or server indicated is unreachable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-388"><span id="ERROR_INTERNET_SHUTDOWN"></span><span id="error_internet_shutdown"></span>**ERRO \_ de \_ desligamento da Internet**</span><span class="sxs-lookup"><span data-stu-id="92834-388"><span id="ERROR_INTERNET_SHUTDOWN"></span><span id="error_internet_shutdown"></span>**ERROR\_INTERNET\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-389">12012</span><span class="sxs-lookup"><span data-stu-id="92834-389">12012</span></span>
</dt> <dt>



<span data-ttu-id="92834-390">O suporte a WinINet está sendo desligado ou descarregado.</span><span class="sxs-lookup"><span data-stu-id="92834-390">WinINet support is being shut down or unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-391"><span id="ERROR_INTERNET_TCPIP_NOT_INSTALLED"></span><span id="error_internet_tcpip_not_installed"></span>**ERRO \_ tcpip de Internet \_ \_ não \_ instalado**</span><span class="sxs-lookup"><span data-stu-id="92834-391"><span id="ERROR_INTERNET_TCPIP_NOT_INSTALLED"></span><span id="error_internet_tcpip_not_installed"></span>**ERROR\_INTERNET\_TCPIP\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-392">12159</span><span class="sxs-lookup"><span data-stu-id="92834-392">12159</span></span>
</dt> <dt>



<span data-ttu-id="92834-393">A pilha de protocolos necessária não está carregada e o aplicativo não pode iniciar o WinSock.</span><span class="sxs-lookup"><span data-stu-id="92834-393">The required protocol stack is not loaded and the application cannot start WinSock.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-394"><span id="ERROR_INTERNET_TIMEOUT"></span><span id="error_internet_timeout"></span>**\_tempo limite da Internet de erro \_**</span><span class="sxs-lookup"><span data-stu-id="92834-394"><span id="ERROR_INTERNET_TIMEOUT"></span><span id="error_internet_timeout"></span>**ERROR\_INTERNET\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-395">12002</span><span class="sxs-lookup"><span data-stu-id="92834-395">12002</span></span>
</dt> <dt>



<span data-ttu-id="92834-396">O tempo limite da solicitação foi atingido.</span><span class="sxs-lookup"><span data-stu-id="92834-396">The request has timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-397"><span id="ERROR_INTERNET_UNABLE_TO_CACHE_FILE"></span><span id="error_internet_unable_to_cache_file"></span>**ERRO \_ \_ na Internet não é possível \_ armazenar o \_ arquivo em cache \_**</span><span class="sxs-lookup"><span data-stu-id="92834-397"><span id="ERROR_INTERNET_UNABLE_TO_CACHE_FILE"></span><span id="error_internet_unable_to_cache_file"></span>**ERROR\_INTERNET\_UNABLE\_TO\_CACHE\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-398">12158</span><span class="sxs-lookup"><span data-stu-id="92834-398">12158</span></span>
</dt> <dt>



<span data-ttu-id="92834-399">A função não pôde armazenar o arquivo em cache.</span><span class="sxs-lookup"><span data-stu-id="92834-399">The function was unable to cache the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-400"><span id="ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_internet_unable_to_download_script"></span>**ERRO \_ \_ na Internet não é possível \_ baixar o \_ \_ script**</span><span class="sxs-lookup"><span data-stu-id="92834-400"><span id="ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_internet_unable_to_download_script"></span>**ERROR\_INTERNET\_UNABLE\_TO\_DOWNLOAD\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-401">12167</span><span class="sxs-lookup"><span data-stu-id="92834-401">12167</span></span>
</dt> <dt>



<span data-ttu-id="92834-402">Não foi possível baixar o script de configuração de proxy automático.</span><span class="sxs-lookup"><span data-stu-id="92834-402">The automatic proxy configuration script could not be downloaded.</span></span> <span data-ttu-id="92834-403">O sinalizador da INTERNET deve ter o \_ \_ sinalizador de solicitação de \_ cache \_ definido.</span><span class="sxs-lookup"><span data-stu-id="92834-403">The INTERNET\_FLAG\_MUST\_CACHE\_REQUEST flag was set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-404"><span id="ERROR_INTERNET_UNRECOGNIZED_SCHEME"></span><span id="error_internet_unrecognized_scheme"></span>**ERRO \_ de \_ esquema não reconhecido da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="92834-404"><span id="ERROR_INTERNET_UNRECOGNIZED_SCHEME"></span><span id="error_internet_unrecognized_scheme"></span>**ERROR\_INTERNET\_UNRECOGNIZED\_SCHEME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92834-405">12006</span><span class="sxs-lookup"><span data-stu-id="92834-405">12006</span></span>
</dt> <dt>



<span data-ttu-id="92834-406">O esquema de URL não pôde ser reconhecido ou não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="92834-406">The URL scheme could not be recognized, or is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-407"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**\_identificador inválido do erro \_**</span><span class="sxs-lookup"><span data-stu-id="92834-407"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR\_INVALID\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92834-408">O identificador que foi passado para a API foi invalidado ou fechado.</span><span class="sxs-lookup"><span data-stu-id="92834-408">The handle that was passed to the API has been either invalidated or closed.</span></span>

<span data-ttu-id="92834-409">**Cabeçalho:** Declarado em Winerror. h</span><span class="sxs-lookup"><span data-stu-id="92834-409">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-410"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERRO de \_ mais \_ dados**</span><span class="sxs-lookup"><span data-stu-id="92834-410"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERROR\_MORE\_DATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92834-411">Mais dados disponíveis.</span><span class="sxs-lookup"><span data-stu-id="92834-411">More data is available.</span></span>

<span data-ttu-id="92834-412">**Cabeçalho:** Declarado em Winerror. h</span><span class="sxs-lookup"><span data-stu-id="92834-412">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-413"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERRO \_ não há \_ mais \_ arquivos**</span><span class="sxs-lookup"><span data-stu-id="92834-413"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR\_NO\_MORE\_FILES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92834-414">Não foram encontrados mais arquivos.</span><span class="sxs-lookup"><span data-stu-id="92834-414">No more files have been found.</span></span>

<span data-ttu-id="92834-415">**Cabeçalho:** Declarado em Winerror. h</span><span class="sxs-lookup"><span data-stu-id="92834-415">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92834-416"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERRO \_ não há \_ mais \_ itens**</span><span class="sxs-lookup"><span data-stu-id="92834-416"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERROR\_NO\_MORE\_ITEMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92834-417">Não foram encontrados mais itens.</span><span class="sxs-lookup"><span data-stu-id="92834-417">No more items have been found.</span></span>

<span data-ttu-id="92834-418">**Cabeçalho:** Declarado em Winerror. h</span><span class="sxs-lookup"><span data-stu-id="92834-418">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92834-419">Comentários</span><span class="sxs-lookup"><span data-stu-id="92834-419">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="92834-420">O WinINet não oferece suporte a implementações de servidor.</span><span class="sxs-lookup"><span data-stu-id="92834-420">WinINet does not support server implementations.</span></span> <span data-ttu-id="92834-421">Além disso, ele não deve ser usado de um serviço.</span><span class="sxs-lookup"><span data-stu-id="92834-421">In addition, it should not be used from a service.</span></span> <span data-ttu-id="92834-422">Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="92834-422">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="92834-423">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92834-423">Requirements</span></span>



| <span data-ttu-id="92834-424">Requisito</span><span class="sxs-lookup"><span data-stu-id="92834-424">Requirement</span></span> | <span data-ttu-id="92834-425">Valor</span><span class="sxs-lookup"><span data-stu-id="92834-425">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="92834-426">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92834-426">Minimum supported client</span></span><br/> | <span data-ttu-id="92834-427">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="92834-427">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="92834-428">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92834-428">Minimum supported server</span></span><br/> | <span data-ttu-id="92834-429">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="92834-429">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="92834-430">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="92834-430">Header</span></span><br/>                   | <dl> <span data-ttu-id="92834-431"><dt>WinInet. h</dt></span><span class="sxs-lookup"><span data-stu-id="92834-431"><dt>Wininet.h</dt></span></span> </dl> |



 

