---
title: Confirmação para fragmento
description: Use o ACK para o pacote de fragmento para reconhecer a solicitação de fragmento do cliente.
ms.assetid: f5466489-2d5e-4850-a39c-37bc4923a7ac
keywords:
- ACK para BITS de fragmento
topic_type:
- apiref
api_name:
- Ack for Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef28381313ce00fd6089ebf845ed342ccae455c7
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "103917770"
---
# <a name="ack-for-fragment"></a><span data-ttu-id="6c510-104">Confirmação para fragmento</span><span class="sxs-lookup"><span data-stu-id="6c510-104">Ack for Fragment</span></span>

<span data-ttu-id="6c510-105">Use o **ACK para** o pacote de fragmento para reconhecer a solicitação de [**fragmento**](fragment.md) do cliente.</span><span class="sxs-lookup"><span data-stu-id="6c510-105">Use the **Ack for Fragment** packet to acknowledge the client's [**Fragment**](fragment.md) request.</span></span>

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Session-Id: {guid}
BITS-Received-Content-Range: range
BITS-Reply-URL: url
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a><span data-ttu-id="6c510-106">Cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="6c510-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="6c510-107"><span id="reason-code"></span><span id="REASON-CODE"></span>código de motivo</span><span class="sxs-lookup"><span data-stu-id="6c510-107"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="6c510-108">Substitua o código de motivo por um código de motivo HTTP.</span><span class="sxs-lookup"><span data-stu-id="6c510-108">Replace reason-code with an HTTP reason code.</span></span> <span data-ttu-id="6c510-109">A tabela a seguir mostra os códigos de motivo típicos para uma resposta a uma solicitação de [**fragmento**](fragment.md) .</span><span class="sxs-lookup"><span data-stu-id="6c510-109">The following table shows the typical reason codes for a response to a [**Fragment**](fragment.md) request.</span></span> <span data-ttu-id="6c510-110">Para obter uma lista de códigos de motivo HTTP, consulte [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="6c510-110">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>



| <span data-ttu-id="6c510-111">Código do motivo</span><span class="sxs-lookup"><span data-stu-id="6c510-111">Reason code</span></span>    | <span data-ttu-id="6c510-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c510-112">Description</span></span>                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c510-113">200</span><span class="sxs-lookup"><span data-stu-id="6c510-113">200</span></span><br/> | <span data-ttu-id="6c510-114">OK.</span><span class="sxs-lookup"><span data-stu-id="6c510-114">OK.</span></span> <span data-ttu-id="6c510-115">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6c510-115">The request was successful.</span></span><br/>                                                                             |
| <span data-ttu-id="6c510-116">416</span><span class="sxs-lookup"><span data-stu-id="6c510-116">416</span></span><br/> | <span data-ttu-id="6c510-117">Intervalo-não satisfatório.</span><span class="sxs-lookup"><span data-stu-id="6c510-117">Range-Not-Satisfiable.</span></span> <span data-ttu-id="6c510-118">O cliente enviou um fragmento cujo intervalo não é contíguo com o fragmento anterior.</span><span class="sxs-lookup"><span data-stu-id="6c510-118">The client sent a fragment whose range is not contiguous with the previous fragment.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6c510-119"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>motivo-descrição</span><span class="sxs-lookup"><span data-stu-id="6c510-119"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="6c510-120">Substitua Reason-Description pela descrição de HTTP associada ao código de motivo.</span><span class="sxs-lookup"><span data-stu-id="6c510-120">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="6c510-121">Por exemplo, defina Reason-Description como OK se o código de motivo for 200.</span><span class="sxs-lookup"><span data-stu-id="6c510-121">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="6c510-122"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo de pacote</span><span class="sxs-lookup"><span data-stu-id="6c510-122"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="6c510-123">Identifica esse pacote de resposta como um pacote ACK.</span><span class="sxs-lookup"><span data-stu-id="6c510-123">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="6c510-124"><span id="BITS-Received-Content-Range"></span><span id="bits-received-content-range"></span><span id="BITS-RECEIVED-CONTENT-RANGE"></span>BITS-recebido-intervalo de conteúdo</span><span class="sxs-lookup"><span data-stu-id="6c510-124"><span id="BITS-Received-Content-Range"></span><span id="bits-received-content-range"></span><span id="BITS-RECEIVED-CONTENT-RANGE"></span>BITS-Received-Content-Range</span></span>
</dt> <dd>

<span data-ttu-id="6c510-125">Deslocamento de base zero para o próximo byte que o servidor espera que o cliente envie.</span><span class="sxs-lookup"><span data-stu-id="6c510-125">Zero-based offset to the next byte the server expects the client to send.</span></span> <span data-ttu-id="6c510-126">Por exemplo, se o fragmento contiver o intervalo de 128 212, você definiria intervalo como 213.</span><span class="sxs-lookup"><span data-stu-id="6c510-126">For example, if the fragment contained the range 128 212, you would set range to 213.</span></span>

</dd> <dt>

<span data-ttu-id="6c510-127"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-ID da sessão</span><span class="sxs-lookup"><span data-stu-id="6c510-127"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="6c510-128">GUID de cadeia de caracteres que identifica a sessão para o cliente.</span><span class="sxs-lookup"><span data-stu-id="6c510-128">String GUID that identifies the session to the client.</span></span> <span data-ttu-id="6c510-129">Substitua {GUID} pelo identificador de sessão que o cliente enviou no pacote de solicitação de [**fragmento**](fragment.md) .</span><span class="sxs-lookup"><span data-stu-id="6c510-129">Replace {guid} with the session identifier that the client sent in the [**Fragment**](fragment.md) request packet.</span></span> <span data-ttu-id="6c510-130">Se você não reconhece o identificador de sessão, defina o cabeçalho BITS-erro-código para a \_ sessão BG E \_ \_ não \_ encontrada.</span><span class="sxs-lookup"><span data-stu-id="6c510-130">If you do not recognize the session identifier, set the BITS-Error-Code header to BG\_E\_SESSION\_NOT\_FOUND.</span></span>

</dd> <dt>

<span data-ttu-id="6c510-131"><span id="BITS-Reply-URL"></span><span id="bits-reply-url"></span><span id="BITS-REPLY-URL"></span>BITS-responder-URL</span><span class="sxs-lookup"><span data-stu-id="6c510-131"><span id="BITS-Reply-URL"></span><span id="bits-reply-url"></span><span id="BITS-REPLY-URL"></span>BITS-Reply-URL</span></span>
</dt> <dd>

<span data-ttu-id="6c510-132">Contém a URL para os dados de resposta de um trabalho de upload-resposta.</span><span class="sxs-lookup"><span data-stu-id="6c510-132">Contains the URL to the reply data of an upload-reply job.</span></span> <span data-ttu-id="6c510-133">Inclua esse cabeçalho na resposta de fragmento final após a conclusão do upload e você receberá uma resposta do aplicativo de servidor, se aplicável.</span><span class="sxs-lookup"><span data-stu-id="6c510-133">Include this header in the final fragment response after the upload is complete and you receive a response from the server application, if applicable.</span></span>

<span data-ttu-id="6c510-134">Use o cabeçalho Content-Range da solicitação de fragmento para determinar se o carregamento foi concluído.</span><span class="sxs-lookup"><span data-stu-id="6c510-134">Use the Content-Range header from the Fragment request to determine whether the upload is complete.</span></span> <span data-ttu-id="6c510-135">O carregamento será concluído se o deslocamento final do valor do intervalo for igual ao valor de comprimento total menos um.</span><span class="sxs-lookup"><span data-stu-id="6c510-135">The upload is complete if the end offset of the range value equals the total-length value minus one.</span></span>

<span data-ttu-id="6c510-136">O servidor BITS posta o arquivo de upload no aplicativo de servidor depois de determinar que o carregamento foi concluído.</span><span class="sxs-lookup"><span data-stu-id="6c510-136">The BITS server posts the upload file to the server application after it determines the upload is complete.</span></span> <span data-ttu-id="6c510-137">O aplicativo de servidor processa o arquivo e gera a resposta.</span><span class="sxs-lookup"><span data-stu-id="6c510-137">The server application processes the file and generates the reply.</span></span> <span data-ttu-id="6c510-138">O servidor BITS define o valor de BITS-Reply-URL para a URL do arquivo de resposta do aplicativo de servidor.</span><span class="sxs-lookup"><span data-stu-id="6c510-138">The BITS server sets the value of BITS-Reply-URL to the URL of the reply file from the server application.</span></span>

</dd> <dt>

<span data-ttu-id="6c510-139"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Comprimento do conteúdo</span><span class="sxs-lookup"><span data-stu-id="6c510-139"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="6c510-140">Substitua Length pelo número de bytes incluídos no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="6c510-140">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="6c510-141">O comprimento do conteúdo é necessário, mesmo que o corpo da resposta não inclua conteúdo.</span><span class="sxs-lookup"><span data-stu-id="6c510-141">Content-Length is required, even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="6c510-142"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-erro-código</span><span class="sxs-lookup"><span data-stu-id="6c510-142"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="6c510-143">Substitua o código de erro por um número hexadecimal que representa um valor HRESULT associado a um erro do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="6c510-143">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="6c510-144">Inclua este cabeçalho somente se o código de motivo não for 200 ou 201.</span><span class="sxs-lookup"><span data-stu-id="6c510-144">Only include this header if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="6c510-145"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-erro-contexto</span><span class="sxs-lookup"><span data-stu-id="6c510-145"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="6c510-146">Substitua o contexto de erro por um número hexadecimal que represente o contexto no qual o erro ocorreu.</span><span class="sxs-lookup"><span data-stu-id="6c510-146">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="6c510-147">Especifique o número hexadecimal para [**o \_ \_ \_ \_ arquivo remoto de contexto de erro BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) se o servidor gerou o erro.</span><span class="sxs-lookup"><span data-stu-id="6c510-147">Specify the hexadecimal number for [**BG\_ERROR\_CONTEXT\_REMOTE\_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="6c510-148">Caso contrário, especifique o número hexadecimal para o **\_ \_ \_ \_ aplicativo remoto de contexto de erro BG** (0x7) se o erro foi gerado pelo aplicativo para o qual o arquivo de carregamento é passado.</span><span class="sxs-lookup"><span data-stu-id="6c510-148">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="6c510-149">Inclua este cabeçalho somente se o código de motivo não for 200 ou 201.</span><span class="sxs-lookup"><span data-stu-id="6c510-149">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c510-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c510-150">Remarks</span></span>

<span data-ttu-id="6c510-151">Se a sessão for para um trabalho de resposta de upload, pode haver um atraso antes que o cliente receba a **confirmação final para** a resposta do fragmento.</span><span class="sxs-lookup"><span data-stu-id="6c510-151">If the session is for an upload-reply job, there may be a delay before the client receives the final **Ack for Fragment** response.</span></span> <span data-ttu-id="6c510-152">O comprimento do atraso depende da quantidade de tempo que o aplicativo de servidor (aplicativo no qual o servidor posta o arquivo de upload) leva para gerar a resposta.</span><span class="sxs-lookup"><span data-stu-id="6c510-152">The length of the delay depends on the amount of time the server application (application to which the server posts the upload file) takes to generate the reply.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c510-153">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6c510-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c510-154">**Criar sessão**</span><span class="sxs-lookup"><span data-stu-id="6c510-154">**Create-Session**</span></span>](create-session.md)
</dt> <dt>

[<span data-ttu-id="6c510-155">**Fragmento**</span><span class="sxs-lookup"><span data-stu-id="6c510-155">**Fragment**</span></span>](fragment.md)
</dt> </dl>

 

 





