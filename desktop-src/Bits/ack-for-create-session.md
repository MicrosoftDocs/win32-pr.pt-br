---
title: ACK para Create-Session
description: Use o ACK para Create-Session pacote para confirmar a solicitação de Create-Session do cliente.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- ACK para BITS de Create-Session
topic_type:
- apiref
api_name:
- Ack for Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d978ec4c5693a5087734975c412b999ed7d5890
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "105748309"
---
# <a name="ack-for-create-session"></a><span data-ttu-id="6c557-104">ACK para Create-Session</span><span class="sxs-lookup"><span data-stu-id="6c557-104">Ack for Create-Session</span></span>

<span data-ttu-id="6c557-105">Use o **ACK para** o pacote de criação de sessão para confirmar a solicitação de [**criação de sessão**](create-session.md) do cliente.</span><span class="sxs-lookup"><span data-stu-id="6c557-105">Use the **Ack for Create-Session** packet to acknowledge the client's [**Create-Session**](create-session.md) request.</span></span>

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Protocol: {guid}
BITS-Session-Id: {guid}
BITS-Host-Id: PublicHostName
BITS-Host-Id-Fallback-Timeout: Timeout
Accept-Encoding: Identity
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a><span data-ttu-id="6c557-106">Cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="6c557-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="6c557-107"><span id="reason-code"></span><span id="REASON-CODE"></span>código de motivo</span><span class="sxs-lookup"><span data-stu-id="6c557-107"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="6c557-108">Substitua o código de motivo pelo código de motivo HTTP.</span><span class="sxs-lookup"><span data-stu-id="6c557-108">Replace reason-code with the HTTP reason code.</span></span> <span data-ttu-id="6c557-109">A tabela a seguir mostra os códigos de motivo típicos para uma resposta a uma solicitação de [**criação de sessão**](create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="6c557-109">The following table shows the typical reason codes for a response to a [**Create-Session**](create-session.md) request.</span></span> <span data-ttu-id="6c557-110">Para obter uma lista de códigos de motivo HTTP, consulte [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="6c557-110">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>



| <span data-ttu-id="6c557-111">Código do motivo</span><span class="sxs-lookup"><span data-stu-id="6c557-111">Reason code</span></span>    | <span data-ttu-id="6c557-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c557-112">Description</span></span>                                                                         |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6c557-113">200</span><span class="sxs-lookup"><span data-stu-id="6c557-113">200</span></span><br/> | <span data-ttu-id="6c557-114">OK.</span><span class="sxs-lookup"><span data-stu-id="6c557-114">OK.</span></span> <span data-ttu-id="6c557-115">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6c557-115">The request was successful.</span></span><br/>                                          |
| <span data-ttu-id="6c557-116">201</span><span class="sxs-lookup"><span data-stu-id="6c557-116">201</span></span><br/> | <span data-ttu-id="6c557-117">Criado.</span><span class="sxs-lookup"><span data-stu-id="6c557-117">Created.</span></span> <span data-ttu-id="6c557-118">A sessão foi criada.</span><span class="sxs-lookup"><span data-stu-id="6c557-118">The session was created.</span></span><br/>                                        |
| <span data-ttu-id="6c557-119">403</span><span class="sxs-lookup"><span data-stu-id="6c557-119">403</span></span><br/> | <span data-ttu-id="6c557-120">Negado.</span><span class="sxs-lookup"><span data-stu-id="6c557-120">Forbidden.</span></span> <span data-ttu-id="6c557-121">O usuário não tem permissão para carregar arquivos para a URL especificada.</span><span class="sxs-lookup"><span data-stu-id="6c557-121">The user is not allowed to upload files to the specified URL.</span></span><br/> |
| <span data-ttu-id="6c557-122">404</span><span class="sxs-lookup"><span data-stu-id="6c557-122">404</span></span><br/> | <span data-ttu-id="6c557-123">Não encontrado.</span><span class="sxs-lookup"><span data-stu-id="6c557-123">Not Found.</span></span> <span data-ttu-id="6c557-124">A URL especificada não existe.</span><span class="sxs-lookup"><span data-stu-id="6c557-124">The specified URL does not exist.</span></span><br/>                             |
| <span data-ttu-id="6c557-125">409</span><span class="sxs-lookup"><span data-stu-id="6c557-125">409</span></span><br/> | <span data-ttu-id="6c557-126">Conflito.</span><span class="sxs-lookup"><span data-stu-id="6c557-126">Conflict.</span></span> <span data-ttu-id="6c557-127">O arquivo existe no servidor e não pode ser substituído.</span><span class="sxs-lookup"><span data-stu-id="6c557-127">The file exists on the server and cannot be overwritten.</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="6c557-128"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>motivo-descrição</span><span class="sxs-lookup"><span data-stu-id="6c557-128"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="6c557-129">Substitua Reason-Description pela descrição de HTTP associada ao código de motivo.</span><span class="sxs-lookup"><span data-stu-id="6c557-129">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="6c557-130">Por exemplo, defina Reason-Description como OK se o código de motivo for 200.</span><span class="sxs-lookup"><span data-stu-id="6c557-130">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="6c557-131"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo de pacote</span><span class="sxs-lookup"><span data-stu-id="6c557-131"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="6c557-132">Identifica esse pacote de resposta como um pacote ACK.</span><span class="sxs-lookup"><span data-stu-id="6c557-132">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="6c557-133"><span id="BITS-Protocol"></span><span id="bits-protocol"></span><span id="BITS-PROTOCOL"></span>BITS-protocolo</span><span class="sxs-lookup"><span data-stu-id="6c557-133"><span id="BITS-Protocol"></span><span id="bits-protocol"></span><span id="BITS-PROTOCOL"></span>BITS-Protocol</span></span>
</dt> <dd>

<span data-ttu-id="6c557-134">GUID de cadeia de caracteres que identifica o protocolo que o servidor deseja usar para esta sessão.</span><span class="sxs-lookup"><span data-stu-id="6c557-134">String GUID that identifies the protocol that the server wants to use for this session.</span></span> <span data-ttu-id="6c557-135">Substitua {GUID} pelo identificador de protocolo da lista de protocolos que o cliente inclui na solicitação de [**criação de sessão**](create-session.md) ; o cabeçalho BITS-supported-Protocol contém a lista.</span><span class="sxs-lookup"><span data-stu-id="6c557-135">Replace {guid} with the protocol identifier from the list of protocols the client includes in the [**Create-Session**](create-session.md) request; the BITS-Supported-Protocol header contains the list.</span></span> <span data-ttu-id="6c557-136">Inclua este cabeçalho somente se o código de motivo for 200 ou 201.</span><span class="sxs-lookup"><span data-stu-id="6c557-136">Include this header only if the reason-code is 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="6c557-137"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-ID da sessão</span><span class="sxs-lookup"><span data-stu-id="6c557-137"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="6c557-138">GUID de cadeia de caracteres que identifica essa sessão para o cliente.</span><span class="sxs-lookup"><span data-stu-id="6c557-138">String GUID that identifies this session to the client.</span></span> <span data-ttu-id="6c557-139">Substitua {GUID} pelo identificador de sessão que o cliente envia em todos os pacotes de solicitação subsequentes.</span><span class="sxs-lookup"><span data-stu-id="6c557-139">Replace {guid} with the session identifier that the client sends in all subsequent request packets.</span></span>

<span data-ttu-id="6c557-140">O BITS usa um GUID para identificar a sessão, mas você pode usar qualquer cadeia de caracteres de HTTP-válido de até 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="6c557-140">BITS uses a GUID to identify the session, but you can use any HTTP-legal string up to 100 characters.</span></span>

</dd> <dt>

<span data-ttu-id="6c557-141"><span id="BITS-Host-Id"></span><span id="bits-host-id"></span><span id="BITS-HOST-ID"></span>BITS-host-ID</span><span class="sxs-lookup"><span data-stu-id="6c557-141"><span id="BITS-Host-Id"></span><span id="bits-host-id"></span><span id="BITS-HOST-ID"></span>BITS-Host-Id</span></span>
</dt> <dd>

<span data-ttu-id="6c557-142">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6c557-142">Optional.</span></span> <span data-ttu-id="6c557-143">Inclua este cabeçalho somente se a [propriedade de extensão do IIS do bits](bits-iis-extension-properties.md), BITSHostId, estiver definida.</span><span class="sxs-lookup"><span data-stu-id="6c557-143">Include this header only if the [BITS IIS extension property](bits-iis-extension-properties.md), BITSHostId, is set.</span></span> <span data-ttu-id="6c557-144">Substitua PublicHostName pelo nome do servidor ou endereço IP da propriedade BITSHostId.</span><span class="sxs-lookup"><span data-stu-id="6c557-144">Replace PublicHostName with the server name or IP address from the BITSHostId property.</span></span>

<span data-ttu-id="6c557-145">O cliente deve substituir a parte do servidor da URL remota em todos os pacotes subsequentes.</span><span class="sxs-lookup"><span data-stu-id="6c557-145">The client must replace the server portion of the remote-URL on all subsequent packets.</span></span> <span data-ttu-id="6c557-146">Se o cliente não especificar esse nome de host nos pacotes subsequentes, será possível que o trabalho comece novamente em outro servidor no farm, deixando um arquivo de carregamento parcial no servidor anterior.</span><span class="sxs-lookup"><span data-stu-id="6c557-146">If the client does not specify this host name on subsequent packets, it is possible that the job will begin again on another server in the farm, leaving a partial upload file on the previous server.</span></span>

</dd> <dt>

<span data-ttu-id="6c557-147"><span id="BITS-Host-Id-Fallback-Timeout"></span><span id="bits-host-id-fallback-timeout"></span><span id="BITS-HOST-ID-FALLBACK-TIMEOUT"></span>BITS-host-ID-fallback-tempo limite</span><span class="sxs-lookup"><span data-stu-id="6c557-147"><span id="BITS-Host-Id-Fallback-Timeout"></span><span id="bits-host-id-fallback-timeout"></span><span id="BITS-HOST-ID-FALLBACK-TIMEOUT"></span>BITS-Host-Id-Fallback-Timeout</span></span>
</dt> <dd>

<span data-ttu-id="6c557-148">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6c557-148">Optional.</span></span> <span data-ttu-id="6c557-149">Inclua este cabeçalho somente se o cabeçalho BITS-host-ID for especificado.</span><span class="sxs-lookup"><span data-stu-id="6c557-149">Include this header only if the BITS-Host-Id header is specified.</span></span> <span data-ttu-id="6c557-150">Substitua o tempo limite pelo valor de tempo limite da propriedade BITSHostIdFallbackTimeout.</span><span class="sxs-lookup"><span data-stu-id="6c557-150">Replace Timeout with the time-out value from the BITSHostIdFallbackTimeout property.</span></span> <span data-ttu-id="6c557-151">A propriedade BITSHostIdFallbackTimeout é uma das [Propriedades de extensão do IIS do bits](bits-iis-extension-properties.md).</span><span class="sxs-lookup"><span data-stu-id="6c557-151">The BITSHostIdFallbackTimeout property is one of the [BITS IIS extension properties](bits-iis-extension-properties.md).</span></span>

<span data-ttu-id="6c557-152">O cliente usa o período de tempo limite para determinar por quanto tempo ele tenta se reconectar ao nome do servidor especificado no cabeçalho BITS-host-ID antes de reverter para o nome de host especificado no nome de arquivo remoto do trabalho.</span><span class="sxs-lookup"><span data-stu-id="6c557-152">The client uses the time-out period to determine how long it tries to reconnect to the server name specified in the BITS-Host-Id header before reverting to the host name specified in the remote file name of the job.</span></span> <span data-ttu-id="6c557-153">O temporizador começa quando o BITS não consegue se conectar ao servidor BITS-host-ID.</span><span class="sxs-lookup"><span data-stu-id="6c557-153">The timer begins when BITS is unable to connect to the BITS-Host-Id server.</span></span> <span data-ttu-id="6c557-154">O temporizador é redefinido quando uma conexão com o servidor é restaurada.</span><span class="sxs-lookup"><span data-stu-id="6c557-154">The timer is reset when a connection to the server is restored.</span></span> <span data-ttu-id="6c557-155">Se um período de tempo limite não for especificado, o cliente nunca será revertido para o nome de host especificado no nome do arquivo remoto.</span><span class="sxs-lookup"><span data-stu-id="6c557-155">If a time-out period is not specified, the client never reverts to the host name specified in the remote file name.</span></span>

</dd> <dt>

<span data-ttu-id="6c557-156"><span id="Accept-Encoding"></span><span id="accept-encoding"></span><span id="ACCEPT-ENCODING"></span>Aceitação-codificação</span><span class="sxs-lookup"><span data-stu-id="6c557-156"><span id="Accept-Encoding"></span><span id="accept-encoding"></span><span id="ACCEPT-ENCODING"></span>Accept-Encoding</span></span>
</dt> <dd>

<span data-ttu-id="6c557-157">Identifica o esquema de codificação a ser usado nos fragmentos enviados ao servidor.</span><span class="sxs-lookup"><span data-stu-id="6c557-157">Identifies the encoding scheme to use on the fragments sent to the server.</span></span> <span data-ttu-id="6c557-158">O pacote de fragmento contém o fragmento codificado no corpo do pacote.</span><span class="sxs-lookup"><span data-stu-id="6c557-158">The Fragment packet contains the encoded fragment in the body of the packet.</span></span> <span data-ttu-id="6c557-159">O servidor BITS requer codificação de identidade (texto não criptografado).</span><span class="sxs-lookup"><span data-stu-id="6c557-159">The BITS server requires Identity encoding (plaintext).</span></span> <span data-ttu-id="6c557-160">Inclua este cabeçalho somente se o código de motivo for 200 ou 201.</span><span class="sxs-lookup"><span data-stu-id="6c557-160">Include this header only if the Reason-code is 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="6c557-161"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Comprimento do conteúdo</span><span class="sxs-lookup"><span data-stu-id="6c557-161"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="6c557-162">Substitua Length pelo número de bytes incluídos no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="6c557-162">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="6c557-163">Necessário mesmo se o corpo da resposta não incluir conteúdo.</span><span class="sxs-lookup"><span data-stu-id="6c557-163">Required even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="6c557-164"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-erro-código</span><span class="sxs-lookup"><span data-stu-id="6c557-164"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="6c557-165">Substitua o código de erro por um número hexadecimal que representa um valor HRESULT associado a um erro do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="6c557-165">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="6c557-166">Inclua este cabeçalho somente se o código de motivo não for 200 ou 201.</span><span class="sxs-lookup"><span data-stu-id="6c557-166">Include this header only if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="6c557-167"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-erro-contexto</span><span class="sxs-lookup"><span data-stu-id="6c557-167"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="6c557-168">Substitua o contexto de erro por um número hexadecimal que represente o contexto no qual o erro ocorreu.</span><span class="sxs-lookup"><span data-stu-id="6c557-168">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="6c557-169">Especifique o número hexadecimal para [**o \_ \_ \_ \_ arquivo remoto de contexto de erro BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) se o servidor gerou o erro.</span><span class="sxs-lookup"><span data-stu-id="6c557-169">Specify the hexadecimal number for [**BG\_ERROR\_CONTEXT\_REMOTE\_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="6c557-170">Caso contrário, especifique o número hexadecimal para o **\_ \_ \_ \_ aplicativo remoto de contexto de erro BG** (0x7) se o erro foi gerado pelo aplicativo para o qual o arquivo de carregamento é passado.</span><span class="sxs-lookup"><span data-stu-id="6c557-170">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="6c557-171">Inclua este cabeçalho somente se o código de motivo não for 200 ou 201.</span><span class="sxs-lookup"><span data-stu-id="6c557-171">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="6c557-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c557-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c557-173">**Criar sessão**</span><span class="sxs-lookup"><span data-stu-id="6c557-173">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 





