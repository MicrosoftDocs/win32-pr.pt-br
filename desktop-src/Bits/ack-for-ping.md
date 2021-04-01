---
title: ACK para ping
description: Use o ACK para o pacote de ping para confirmar a solicitação de ping do cliente.
ms.assetid: 2e288564-d06f-4b45-b0c0-7aab1897da40
keywords:
- ACK para BITS de ping
topic_type:
- apiref
api_name:
- Ack for Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5a3ca765c8bd7758f19abe396ad0449a5895d8e
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "103917769"
---
# <a name="ack-for-ping"></a><span data-ttu-id="579ce-104">ACK para ping</span><span class="sxs-lookup"><span data-stu-id="579ce-104">Ack for Ping</span></span>

<span data-ttu-id="579ce-105">Use o **ACK para o pacote de ping** para confirmar a solicitação de [**ping**](ping.md) do cliente.</span><span class="sxs-lookup"><span data-stu-id="579ce-105">Use the **Ack for Ping** packet to acknowledge the client's [**Ping**](ping.md) request.</span></span>

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a><span data-ttu-id="579ce-106">Cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="579ce-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="579ce-107"><span id="reason-code"></span><span id="REASON-CODE"></span>código de motivo</span><span class="sxs-lookup"><span data-stu-id="579ce-107"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="579ce-108">Substitua o código de motivo pelo código de motivo HTTP.</span><span class="sxs-lookup"><span data-stu-id="579ce-108">Replace reason-code with the HTTP reason code.</span></span> <span data-ttu-id="579ce-109">Por exemplo, defina código de motivo como 200 se êxito.</span><span class="sxs-lookup"><span data-stu-id="579ce-109">For example, set reason-code to 200 if success.</span></span> <span data-ttu-id="579ce-110">Para obter uma lista de códigos de motivo HTTP, consulte [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="579ce-110">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

</dd> <dt>

<span data-ttu-id="579ce-111"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>motivo-descrição</span><span class="sxs-lookup"><span data-stu-id="579ce-111"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="579ce-112">Substitua Reason-Description pela descrição de HTTP associada ao código de motivo.</span><span class="sxs-lookup"><span data-stu-id="579ce-112">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="579ce-113">Por exemplo, defina Reason-Description como OK se o código de motivo for 200.</span><span class="sxs-lookup"><span data-stu-id="579ce-113">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="579ce-114"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo de pacote</span><span class="sxs-lookup"><span data-stu-id="579ce-114"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="579ce-115">Identifica esse pacote de resposta como um pacote ACK.</span><span class="sxs-lookup"><span data-stu-id="579ce-115">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="579ce-116"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Comprimento do conteúdo</span><span class="sxs-lookup"><span data-stu-id="579ce-116"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="579ce-117">Substitua Length pelo número de bytes incluídos no corpo da resposta.</span><span class="sxs-lookup"><span data-stu-id="579ce-117">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="579ce-118">Necessário mesmo se o corpo da resposta não incluir conteúdo.</span><span class="sxs-lookup"><span data-stu-id="579ce-118">Required even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="579ce-119"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-erro-código</span><span class="sxs-lookup"><span data-stu-id="579ce-119"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="579ce-120">Substitua o código de erro por um número hexadecimal que representa um valor HRESULT associado a um erro do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="579ce-120">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="579ce-121">Inclua este cabeçalho somente se o código de motivo não for 200 ou 201.</span><span class="sxs-lookup"><span data-stu-id="579ce-121">Include this header only if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="579ce-122"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-erro-contexto</span><span class="sxs-lookup"><span data-stu-id="579ce-122"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="579ce-123">Substitua o contexto de erro por um número hexadecimal que represente o contexto no qual o erro ocorreu.</span><span class="sxs-lookup"><span data-stu-id="579ce-123">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="579ce-124">Especifique o número hexadecimal para [**o \_ \_ \_ \_ arquivo remoto de contexto de erro BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) se o servidor gerou o erro.</span><span class="sxs-lookup"><span data-stu-id="579ce-124">Specify the hexadecimal number for [**BG\_ERROR\_CONTEXT\_REMOTE\_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="579ce-125">Caso contrário, especifique o número hexadecimal para o **\_ \_ \_ \_ aplicativo remoto de contexto de erro BG** (0x7) se o erro foi gerado pelo aplicativo para o qual o arquivo de carregamento é passado.</span><span class="sxs-lookup"><span data-stu-id="579ce-125">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="579ce-126">Inclua este cabeçalho somente se o código de motivo não for 200 ou 201.</span><span class="sxs-lookup"><span data-stu-id="579ce-126">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="579ce-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="579ce-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="579ce-128">**Executar**</span><span class="sxs-lookup"><span data-stu-id="579ce-128">**Ping**</span></span>](ping.md)
</dt> </dl>

 

 




