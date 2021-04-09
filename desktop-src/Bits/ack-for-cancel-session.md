---
title: ACK para Cancel-Session
description: Use o ACK para Cancel-Session pacote para confirmar a solicitação de Cancel-Session do cliente. O servidor envia a confirmação depois de liberar todos os recursos associados à sessão de carregamento.
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- ACK para BITS de Cancel-Session
topic_type:
- apiref
api_name:
- Ack for Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b85ff937b720a69ee2722cef2f02b25273ea58d
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104008572"
---
# <a name="ack-for-cancel-session"></a><span data-ttu-id="f4f25-105">ACK para Cancel-Session</span><span class="sxs-lookup"><span data-stu-id="f4f25-105">Ack for Cancel-Session</span></span>

<span data-ttu-id="f4f25-106">Use o **ACK para o pacote Cancel-Session** para confirmar a solicitação de [**cancelamento da sessão**](cancel-session.md) do cliente.</span><span class="sxs-lookup"><span data-stu-id="f4f25-106">Use the **Ack for Cancel-Session** packet to acknowledge the client's [**Cancel-Session**](cancel-session.md) request.</span></span> <span data-ttu-id="f4f25-107">O servidor envia a confirmação depois de liberar todos os recursos associados à sessão de carregamento.</span><span class="sxs-lookup"><span data-stu-id="f4f25-107">The server sends the acknowledgment after releasing all resources associated with the upload session.</span></span>

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Session-Id: {guid}
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a><span data-ttu-id="f4f25-108">Cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="f4f25-108">Headers</span></span>

<dl> <dt>

<span data-ttu-id="f4f25-109"><span id="reason-code"></span><span id="REASON-CODE"></span>código de motivo</span><span class="sxs-lookup"><span data-stu-id="f4f25-109"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="f4f25-110">Substitua o código de motivo pelo código de motivo HTTP.</span><span class="sxs-lookup"><span data-stu-id="f4f25-110">Replace reason-code with the HTTP reason code.</span></span> <span data-ttu-id="f4f25-111">Por exemplo, defina código de motivo como 200 se êxito.</span><span class="sxs-lookup"><span data-stu-id="f4f25-111">For example, set reason-code to 200 if success.</span></span> <span data-ttu-id="f4f25-112">Para obter uma lista de códigos de motivo HTTP, consulte [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="f4f25-112">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

</dd> <dt>

<span data-ttu-id="f4f25-113"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>motivo-descrição</span><span class="sxs-lookup"><span data-stu-id="f4f25-113"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="f4f25-114">Substitua Reason-Description pela descrição de HTTP associada ao código de motivo.</span><span class="sxs-lookup"><span data-stu-id="f4f25-114">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="f4f25-115">Por exemplo, defina Reason-Description como OK se o código de motivo for 200.</span><span class="sxs-lookup"><span data-stu-id="f4f25-115">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="f4f25-116"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo de pacote</span><span class="sxs-lookup"><span data-stu-id="f4f25-116"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="f4f25-117">Identifica esse pacote de resposta como um pacote ACK.</span><span class="sxs-lookup"><span data-stu-id="f4f25-117">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="f4f25-118"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-ID da sessão</span><span class="sxs-lookup"><span data-stu-id="f4f25-118"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="f4f25-119">GUID de cadeia de caracteres que identifica a sessão para o cliente.</span><span class="sxs-lookup"><span data-stu-id="f4f25-119">String GUID that identifies the session to the client.</span></span> <span data-ttu-id="f4f25-120">Substitua {GUID} pelo identificador de sessão que o cliente enviou no pacote de solicitação de [**cancelamento de sessão**](cancel-session.md) .</span><span class="sxs-lookup"><span data-stu-id="f4f25-120">Replace {guid} with the session identifier that the client sent in the [**Cancel-Session**](cancel-session.md) request packet.</span></span> <span data-ttu-id="f4f25-121">Se você não reconhece o identificador de sessão, defina o cabeçalho BITS-erro-código para a \_ sessão BG E \_ \_ não \_ encontrada.</span><span class="sxs-lookup"><span data-stu-id="f4f25-121">If you do not recognize the session identifier, set the BITS-Error-Code header to BG\_E\_SESSION\_NOT\_FOUND.</span></span>

</dd> <dt>

<span data-ttu-id="f4f25-122"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Comprimento do conteúdo</span><span class="sxs-lookup"><span data-stu-id="f4f25-122"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="f4f25-123">Substitua Length pelo número de bytes incluídos no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="f4f25-123">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="f4f25-124">Necessário mesmo se o corpo da resposta não incluir conteúdo.</span><span class="sxs-lookup"><span data-stu-id="f4f25-124">Required even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="f4f25-125"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-erro-código</span><span class="sxs-lookup"><span data-stu-id="f4f25-125"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="f4f25-126">Substitua o código de erro por um número hexadecimal que representa um valor HRESULT associado a um erro do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="f4f25-126">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="f4f25-127">Inclua este cabeçalho somente se o código de motivo não for 200 ou 201.</span><span class="sxs-lookup"><span data-stu-id="f4f25-127">Only include this header if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="f4f25-128"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-erro-contexto</span><span class="sxs-lookup"><span data-stu-id="f4f25-128"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="f4f25-129">Substitua o contexto de erro por um número hexadecimal que represente o contexto no qual o erro ocorreu.</span><span class="sxs-lookup"><span data-stu-id="f4f25-129">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="f4f25-130">Especifique o número hexadecimal para [**BG_ERROR_CONTEXT_REMOTE_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) se o servidor tiver gerado o erro.</span><span class="sxs-lookup"><span data-stu-id="f4f25-130">Specify the hexadecimal number for [**BG_ERROR_CONTEXT_REMOTE_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="f4f25-131">Caso contrário, especifique o número hexadecimal para o **\_ \_ \_ \_ aplicativo remoto de contexto de erro BG** (0x7) se o erro foi gerado pelo aplicativo para o qual o arquivo de carregamento é passado.</span><span class="sxs-lookup"><span data-stu-id="f4f25-131">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="f4f25-132">Inclua este cabeçalho somente se o código de motivo não for 200 ou 201.</span><span class="sxs-lookup"><span data-stu-id="f4f25-132">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4f25-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4f25-133">Remarks</span></span>

<span data-ttu-id="f4f25-134">O cliente BITS reenviará o pacote de [**sessão cancelada**](cancel-session.md) se o código de motivo estiver no intervalo de 500 a 599, a menos que o cabeçalho bits-erro-código esteja presente com um valor de sessão de BG \_ E \_ \_ não \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="f4f25-134">The BITS client resends the [**Cancel-Session**](cancel-session.md) packet if the reason-code is in the range from 500 through 599, unless the BITS-Error-Code header is present with a value of BG\_E\_SESSION\_NOT\_FOUND.</span></span> <span data-ttu-id="f4f25-135">O cliente não tentará novamente os códigos de motivo 100 a 499.</span><span class="sxs-lookup"><span data-stu-id="f4f25-135">The client will not retry for reason codes 100 through 499.</span></span>

## <a name="see-also"></a><span data-ttu-id="f4f25-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4f25-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4f25-137">**ACK para fechamento de sessão**</span><span class="sxs-lookup"><span data-stu-id="f4f25-137">**Ack for Close-Session**</span></span>](ack-for-close-session.md)
</dt> <dt>

[<span data-ttu-id="f4f25-138">**Cancelar sessão**</span><span class="sxs-lookup"><span data-stu-id="f4f25-138">**Cancel-Session**</span></span>](cancel-session.md)
</dt> </dl>

 

 




