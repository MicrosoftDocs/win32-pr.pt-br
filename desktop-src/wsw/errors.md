---
title: Errors
description: Esta seção descreve um erro que pode ser emitido por funções de serviços Web do Windows em virtude de uma falha ao executar o comando.
ms.assetid: 2e5b853f-589c-4f89-9d7e-cd02263a2247
keywords:
- Serviços Web de erros para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70f10d673bf8f37664d792d8cf969f0329dc363
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822409"
---
# <a name="errors"></a><span data-ttu-id="a25d1-106">Errors</span><span class="sxs-lookup"><span data-stu-id="a25d1-106">Errors</span></span>

<span data-ttu-id="a25d1-107">Esta seção descreve um erro que pode ser emitido por funções de serviços Web do Windows em virtude de uma falha ao executar o comando.</span><span class="sxs-lookup"><span data-stu-id="a25d1-107">This section outlines error that may be issues by Windows Web Services functions in result of a failure to execute the command.</span></span>

-   [<span data-ttu-id="a25d1-108">Parâmetros de saída</span><span class="sxs-lookup"><span data-stu-id="a25d1-108">Out Parameters</span></span>](#out-parameters)
-   [<span data-ttu-id="a25d1-109">Códigos de Erro</span><span class="sxs-lookup"><span data-stu-id="a25d1-109">Error Codes</span></span>](#error-codes)
-   [<span data-ttu-id="a25d1-110">Erros avançados</span><span class="sxs-lookup"><span data-stu-id="a25d1-110">Rich Errors</span></span>](#rich-errors)
-   [<span data-ttu-id="a25d1-111">Falhas e erros</span><span class="sxs-lookup"><span data-stu-id="a25d1-111">Faults and Errors</span></span>](#faults-and-errors)
-   [<span data-ttu-id="a25d1-112">Informações de erro sensíveis à linguagem</span><span class="sxs-lookup"><span data-stu-id="a25d1-112">Language Sensitive Error Information</span></span>](#language-sensitive-error-information)
-   [<span data-ttu-id="a25d1-113">Códigos de erro canônicos</span><span class="sxs-lookup"><span data-stu-id="a25d1-113">Canonical Error Codes</span></span>](#canonical-error-codes)
-   [<span data-ttu-id="a25d1-114">Uso de API inválido</span><span class="sxs-lookup"><span data-stu-id="a25d1-114">Invalid API Usage</span></span>](#invalid-api-usage)
-   [<span data-ttu-id="a25d1-115">Segurança</span><span class="sxs-lookup"><span data-stu-id="a25d1-115">Security</span></span>](#security)

## <a name="out-parameters"></a><span data-ttu-id="a25d1-116">Parâmetros de saída</span><span class="sxs-lookup"><span data-stu-id="a25d1-116">Out Parameters</span></span>

<span data-ttu-id="a25d1-117">Como regra geral, o valor de parâmetros de saída não será modificado se uma função falhar.</span><span class="sxs-lookup"><span data-stu-id="a25d1-117">As a general rule, the value of out parameters are not modified if a function fails.</span></span>

<span data-ttu-id="a25d1-118">Há algumas instâncias em que parâmetros de saída são modificados se a função falhar.</span><span class="sxs-lookup"><span data-stu-id="a25d1-118">There are a few instances where out parameters are modified if the function fails.</span></span> <span data-ttu-id="a25d1-119">Esses casos são explicitamente chamados na documentação para cada parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a25d1-119">These cases are explicitly called out in the documentation for each parameter.</span></span> <span data-ttu-id="a25d1-120">Se a documentação não mencionar nada sobre a modificação de parâmetros em caso de falha, você pode pressupor com segurança que a função não os modificará.</span><span class="sxs-lookup"><span data-stu-id="a25d1-120">If the documentation does not mention anything about modifying out parameters in the case of failure, then you can safely assume that the function will not modify them.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a25d1-121">Códigos de erro</span><span class="sxs-lookup"><span data-stu-id="a25d1-121">Error Codes</span></span>

<span data-ttu-id="a25d1-122">Todos os códigos de retorno de erro são HRESULTs.</span><span class="sxs-lookup"><span data-stu-id="a25d1-122">All error return codes are HRESULTs.</span></span> <span data-ttu-id="a25d1-123">Essa API define um conjunto de HRESULTs no intervalo de \_ WEBservices de instalação, mas também retorna erros definidos em outro lugar na API do Windows.</span><span class="sxs-lookup"><span data-stu-id="a25d1-123">This API defines a set of HRESULTs in the FACILITY\_WEBSERVICES range, but also returns errors defined elsewhere in the Windows API.</span></span>

<span data-ttu-id="a25d1-124">Consulte a documentação para obter uma API específica para saber mais sobre quais códigos de erro são retornados.</span><span class="sxs-lookup"><span data-stu-id="a25d1-124">Refer to the documentation for specific API's to learn about which error codes are returned.</span></span> <span data-ttu-id="a25d1-125">A lista não deve ser exaustiva para cada API, mas sim uma lista de códigos de erro para os quais há cenários comuns de manipulação explícita.</span><span class="sxs-lookup"><span data-stu-id="a25d1-125">The list is not intended to be exhaustive for each API, but rather a list of error codes for which there are common scenarios for explicit handling.</span></span> <span data-ttu-id="a25d1-126">Um chamador deve sempre supor que outros códigos de erro sejam possíveis de qualquer API.</span><span class="sxs-lookup"><span data-stu-id="a25d1-126">A caller should always assume other error codes are possible from any API.</span></span>

<span data-ttu-id="a25d1-127">Essa API define um número relativamente pequeno de códigos de erro, que correspondem a cenários em que um programa desejará agir com base no erro.</span><span class="sxs-lookup"><span data-stu-id="a25d1-127">This API defines a relatively small number of error codes, which correspond to scenarios where a program will want to take action based on the error.</span></span> <span data-ttu-id="a25d1-128">Os códigos de erro sozinhos podem não ser suficientes para determinar o que deu errado ou para fornecer uma boa descrição do problema ao usuário.</span><span class="sxs-lookup"><span data-stu-id="a25d1-128">Error codes alone may not be sufficient in order to determine what went wrong, or in order to provide a good description of the problem to the user.</span></span> <span data-ttu-id="a25d1-129">A melhor compreensão do problema vem do uso de erros avançados, conforme descrito abaixo.</span><span class="sxs-lookup"><span data-stu-id="a25d1-129">The best understanding of the problem comes from using Rich Errors, as described below.</span></span>

## <a name="rich-errors"></a><span data-ttu-id="a25d1-130">Erros avançados</span><span class="sxs-lookup"><span data-stu-id="a25d1-130">Rich Errors</span></span>

<span data-ttu-id="a25d1-131">Além de retornar um código de erro, um chamador pode opcionalmente solicitar informações de erro ricas para qualquer chamada à API, passando um objeto de [ \_ erro WS](ws-error.md) não **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a25d1-131">In additional to returning an error code, a caller may optionally request rich error information for any API call by passing a non-**NULL**[WS\_ERROR](ws-error.md) object.</span></span> <span data-ttu-id="a25d1-132">Para criar um objeto de erro, use [**WsCreateError**](/windows/desktop/api/WebServices/nf-webservices-wscreateerror).</span><span class="sxs-lookup"><span data-stu-id="a25d1-132">To create an error object, use [**WsCreateError**](/windows/desktop/api/WebServices/nf-webservices-wscreateerror).</span></span> <span data-ttu-id="a25d1-133">Se houver um erro, a API que causou o erro preencherá o objeto de erro com contexto adicional sobre a situação de erro.</span><span class="sxs-lookup"><span data-stu-id="a25d1-133">If there is an error, then the API that caused the error will fill the error object with additional context about the error situation.</span></span> <span data-ttu-id="a25d1-134">Se não houver nenhum erro, o objeto de erro não será modificado.</span><span class="sxs-lookup"><span data-stu-id="a25d1-134">If there is no error, then the error object is unmodified.</span></span> <span data-ttu-id="a25d1-135">A passagem de um objeto de erro **nulo** indica que o chamador não está interessado em informações de erro avançadas.</span><span class="sxs-lookup"><span data-stu-id="a25d1-135">Passing a **NULL** error object indicates that the caller is not interested in rich error information.</span></span> <span data-ttu-id="a25d1-136">Os chamadores (incluindo retornos de chamada) devem estar preparados para lidar com objetos de erro **nulos** .</span><span class="sxs-lookup"><span data-stu-id="a25d1-136">Callees (including callbacks) must be prepared to handle **NULL** error objects.</span></span>

<span data-ttu-id="a25d1-137">Observe que o mesmo objeto de erro pode ser usado para várias chamadas de API, mas pode ser usado apenas para uma chamada de API por vez (como é um thread único).</span><span class="sxs-lookup"><span data-stu-id="a25d1-137">Note that the same error object can be used for multiple API calls, but may only be used for one API call at a time (as it is single threaded).</span></span> <span data-ttu-id="a25d1-138">Cada vez que ocorre um erro, as informações de erro são acrescentadas ao objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="a25d1-138">Each time an error occurs, error information is appended to the error object.</span></span> <span data-ttu-id="a25d1-139">Como uma cadeia de chamada se desenrola, várias funções podem adicionar informações ao objeto de erro para fornecer contexto adicional sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="a25d1-139">As a call chain unwinds, multiple functions may add information to the error object to provide additional context about the error.</span></span> <span data-ttu-id="a25d1-140">Para limpar o conteúdo do objeto de erro antes de reutilizá-lo (após ocorrer um erro), use [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror).</span><span class="sxs-lookup"><span data-stu-id="a25d1-140">To clear the contents of the error object before reusing it (after an error occurs), use [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror).</span></span> <span data-ttu-id="a25d1-141">Se nenhum erro ocorrer, não será necessário redefinir o objeto de erro antes de reusá-lo.</span><span class="sxs-lookup"><span data-stu-id="a25d1-141">If no error occurs, it is not necessary to reset the error object before reusing it.</span></span>

<span data-ttu-id="a25d1-142">As informações de erro avançadas consistem no seguinte:</span><span class="sxs-lookup"><span data-stu-id="a25d1-142">Rich error information consists of the following:</span></span>

-   <span data-ttu-id="a25d1-143">Um conjunto de valores de propriedade, que fornece informações adicionais sobre o erro, se presente.</span><span class="sxs-lookup"><span data-stu-id="a25d1-143">A set of property values, which provide additional information about the error if present.</span></span> <span data-ttu-id="a25d1-144">Consulte [**\_ \_ propriedade de erro WS**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property).</span><span class="sxs-lookup"><span data-stu-id="a25d1-144">See [**WS\_ERROR\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property).</span></span>
-   <span data-ttu-id="a25d1-145">Zero ou mais cadeias de caracteres de erro.</span><span class="sxs-lookup"><span data-stu-id="a25d1-145">Zero or more error strings.</span></span> <span data-ttu-id="a25d1-146">As cadeias de caracteres são adicionadas usando [**WsAddErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring)e podem ser consultadas usando o [**WsGetErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsgeterrorstring).</span><span class="sxs-lookup"><span data-stu-id="a25d1-146">The strings are added using [**WsAddErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring), and can be queried using using [**WsGetErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsgeterrorstring).</span></span> <span data-ttu-id="a25d1-147">O número de cadeias de caracteres pode ser consultado usando a [**\_ \_ \_ \_ contagem de cadeias da propriedade de erro WS**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).</span><span class="sxs-lookup"><span data-stu-id="a25d1-147">The number of strings can be queried using [**WS\_ERROR\_PROPERTY\_STRING\_COUNT**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).</span></span>

## <a name="faults-and-errors"></a><span data-ttu-id="a25d1-148">Falhas e erros</span><span class="sxs-lookup"><span data-stu-id="a25d1-148">Faults and Errors</span></span>

<span data-ttu-id="a25d1-149">Confira [falhas](faults.md) para obter informações sobre como os erros e as falhas estão relacionados.</span><span class="sxs-lookup"><span data-stu-id="a25d1-149">See [Faults](faults.md) for information about how errors and faults relate.</span></span>

## <a name="language-sensitive-error-information"></a><span data-ttu-id="a25d1-150">Informações de erro sensíveis à linguagem</span><span class="sxs-lookup"><span data-stu-id="a25d1-150">Language Sensitive Error Information</span></span>

<span data-ttu-id="a25d1-151">Ao criar um objeto de erro, é especificado o LANGid da tradução de idioma desejada para informações de erro.</span><span class="sxs-lookup"><span data-stu-id="a25d1-151">When creating an error object, the LANGID of the desired language translation for error information is specified.</span></span> <span data-ttu-id="a25d1-152">Isso é usado ao adicionar informações de erro ao objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="a25d1-152">This is used when adding error information to the error object.</span></span>

<span data-ttu-id="a25d1-153">Esse valor de idioma pode ser recuperado ou definido usando o [**WS \_ Error \_ Property \_ LangID**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).</span><span class="sxs-lookup"><span data-stu-id="a25d1-153">This language value can be retrieved or set using [**WS\_ERROR\_PROPERTY\_LANGID**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).</span></span>

## <a name="canonical-error-codes"></a><span data-ttu-id="a25d1-154">Códigos de erro canônicos</span><span class="sxs-lookup"><span data-stu-id="a25d1-154">Canonical Error Codes</span></span>

<span data-ttu-id="a25d1-155">Essa API fornece um conjunto canônico de códigos de erro (WS \_ E \_ \* ) que permitem que diferentes tecnologias de comunicação sejam usadas sem precisar depender dos códigos de erro específicos da implementação subjacente específica.</span><span class="sxs-lookup"><span data-stu-id="a25d1-155">This API provides a canonical set of error codes (WS\_E\_\*) that allow for different communication technologies to be used without having to depend on the specific error codes of the specific underlying implementation.</span></span> <span data-ttu-id="a25d1-156">Para obter uma lista completa desses códigos de erro, consulte [valores de retorno dos serviços Web do Windows](windows-web-services-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a25d1-156">For a complete list of these error codes, see [Windows Web Services Return Values](windows-web-services-return-values.md).</span></span>

<span data-ttu-id="a25d1-157">Isso permite, por exemplo, que um programa Verifique o código de erro **do \_ ponto de extremidade WS E \_ \_ não \_ encontrado** se estiver usando TCP, UDP ou http e executar alguma ação (como tentar usar um ponto de extremidade diferente).</span><span class="sxs-lookup"><span data-stu-id="a25d1-157">This allows, for example, a program to check for the error code **WS\_E\_ENDPOINT\_NOT\_FOUND** whether using TCP, UDP, or HTTP, and take some action (like attempting to use a different endpoint).</span></span>

<span data-ttu-id="a25d1-158">Quando um código de erro específico de implementação é mapeado para um erro canônico, o código de erro original é salvo no objeto de erro e ainda pode ser acessado para fins de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="a25d1-158">When an implementation specific error code is mapped to a canonical error, the original error code is saved in the error object, and may still be accessed for diagnostic purposes.</span></span> <span data-ttu-id="a25d1-159">Consulte [**o \_ \_ código de \_ \_ erro \_ original da propriedade de erro WS**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="a25d1-159">See [**WS\_ERROR\_PROPERTY\_ORIGINAL\_ERROR\_CODE**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id) for more information.</span></span>

## <a name="invalid-api-usage"></a><span data-ttu-id="a25d1-160">Uso de API inválido</span><span class="sxs-lookup"><span data-stu-id="a25d1-160">Invalid API Usage</span></span>

<span data-ttu-id="a25d1-161">Os códigos de erro a seguir são reservados para uso inválido de API e não serão retornados em outras circunstâncias.</span><span class="sxs-lookup"><span data-stu-id="a25d1-161">The following error codes are reserved for invalid API usage, and will not be returned in other circumstances.</span></span> <span data-ttu-id="a25d1-162">Se qualquer um desses erros for retornado, ele poderá ser uma indicação de um bug de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a25d1-162">If any of these errors are returned it may be an indication of an application bug.</span></span>

-   <span data-ttu-id="a25d1-163">**\_operação WS E \_ inválida \_**</span><span class="sxs-lookup"><span data-stu-id="a25d1-163">**WS\_E\_INVALID\_OPERATION**</span></span>
-   <span data-ttu-id="a25d1-164">**E \_ INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="a25d1-164">**E\_INVALIDARG**</span></span>

<span data-ttu-id="a25d1-165">As seguintes enumerações fazem parte do rastreamento:</span><span class="sxs-lookup"><span data-stu-id="a25d1-165">The following enumerations are part of tracing:</span></span>

-   [<span data-ttu-id="a25d1-166">**\_ID da \_ propriedade de erro WS \_**</span><span class="sxs-lookup"><span data-stu-id="a25d1-166">**WS\_ERROR\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [<span data-ttu-id="a25d1-167">**\_código de exceção WS \_**</span><span class="sxs-lookup"><span data-stu-id="a25d1-167">**WS\_EXCEPTION\_CODE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

<span data-ttu-id="a25d1-168">Os códigos de erro a seguir fazem parte do rastreamento:</span><span class="sxs-lookup"><span data-stu-id="a25d1-168">The following error codes are part of tracing:</span></span>

-   <span data-ttu-id="a25d1-169">**CERT \_ E \_ CN \_ sem \_ correspondência**</span><span class="sxs-lookup"><span data-stu-id="a25d1-169">**CERT\_E\_CN\_NO\_MATCH**</span></span>
-   <span data-ttu-id="a25d1-170">**CERTIFICADO \_ E \_ expirado**</span><span class="sxs-lookup"><span data-stu-id="a25d1-170">**CERT\_E\_EXPIRED**</span></span>
-   <span data-ttu-id="a25d1-171">**CERTIFICADO \_ E \_ UNTRUSTEDROOT**</span><span class="sxs-lookup"><span data-stu-id="a25d1-171">**CERT\_E\_UNTRUSTEDROOT**</span></span>
-   <span data-ttu-id="a25d1-172">**CERTIFICADO \_ E \_ uso incorreto \_**</span><span class="sxs-lookup"><span data-stu-id="a25d1-172">**CERT\_E\_WRONG\_USAGE**</span></span>
-   <span data-ttu-id="a25d1-173">**\_revogação criptografada E \_ \_ offline**</span><span class="sxs-lookup"><span data-stu-id="a25d1-173">**CRYPT\_E\_REVOCATION\_OFFLINE**</span></span>
-   <span data-ttu-id="a25d1-174">**E \_ INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="a25d1-174">**E\_INVALIDARG**</span></span>
-   <span data-ttu-id="a25d1-175">**E \_ OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="a25d1-175">**E\_OUTOFMEMORY**</span></span>
-   <span data-ttu-id="a25d1-176">**\_endereço WS \_ E \_ em \_ uso**</span><span class="sxs-lookup"><span data-stu-id="a25d1-176">**WS\_E\_ADDRESS\_IN\_USE**</span></span>
-   <span data-ttu-id="a25d1-177">**o \_ endereço WS E \_ \_ não \_ está disponível**</span><span class="sxs-lookup"><span data-stu-id="a25d1-177">**WS\_E\_ADDRESS\_NOT\_AVAILABLE**</span></span>
-   <span data-ttu-id="a25d1-178">**\_acesso ao ponto de extremidade WS E \_ \_ \_ negado**</span><span class="sxs-lookup"><span data-stu-id="a25d1-178">**WS\_E\_ENDPOINT\_ACCESS\_DENIED**</span></span>
-   <span data-ttu-id="a25d1-179">**\_ação de ponto de extremidade WS E \_ \_ \_ sem \_ suporte**</span><span class="sxs-lookup"><span data-stu-id="a25d1-179">**WS\_E\_ENDPOINT\_ACTION\_NOT\_SUPPORTED**</span></span>
-   <span data-ttu-id="a25d1-180">**\_ponto de extremidade WS E \_ \_ desconectado**</span><span class="sxs-lookup"><span data-stu-id="a25d1-180">**WS\_E\_ENDPOINT\_DISCONNECTED**</span></span>
-   <span data-ttu-id="a25d1-181">**\_falha de \_ ponto de extremidade WS E \_**</span><span class="sxs-lookup"><span data-stu-id="a25d1-181">**WS\_E\_ENDPOINT\_FAILURE**</span></span>
-   <span data-ttu-id="a25d1-182">**\_falha de \_ ponto de extremidade WS E \_ \_ recebida**</span><span class="sxs-lookup"><span data-stu-id="a25d1-182">**WS\_E\_ENDPOINT\_FAULT\_RECEIVED**</span></span>
-   <span data-ttu-id="a25d1-183">**\_ponto de extremidade WS E \_ \_ não \_ disponível**</span><span class="sxs-lookup"><span data-stu-id="a25d1-183">**WS\_E\_ENDPOINT\_NOT\_AVAILABLE**</span></span>
-   <span data-ttu-id="a25d1-184">**\_ponto de extremidade WS E \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="a25d1-184">**WS\_E\_ENDPOINT\_NOT\_FOUND**</span></span>
-   <span data-ttu-id="a25d1-185">**\_ponto de extremidade WS E \_ \_ muito \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="a25d1-185">**WS\_E\_ENDPOINT\_TOO\_BUSY**</span></span>
-   <span data-ttu-id="a25d1-186">**\_ponto de extremidade WS E \_ \_ inacessível**</span><span class="sxs-lookup"><span data-stu-id="a25d1-186">**WS\_E\_ENDPOINT\_UNREACHABLE**</span></span>
-   <span data-ttu-id="a25d1-187">**\_URL de \_ ponto de \_ extremidade inválido \_ WS E**</span><span class="sxs-lookup"><span data-stu-id="a25d1-187">**WS\_E\_INVALID\_ENDPOINT\_URL**</span></span>
-   <span data-ttu-id="a25d1-188">**\_ \_ formato inválido de WS E \_**</span><span class="sxs-lookup"><span data-stu-id="a25d1-188">**WS\_E\_INVALID\_FORMAT**</span></span>
-   <span data-ttu-id="a25d1-189">**\_operação WS E \_ inválida \_**</span><span class="sxs-lookup"><span data-stu-id="a25d1-189">**WS\_E\_INVALID\_OPERATION**</span></span>
-   <span data-ttu-id="a25d1-190">**WS \_ E \_ sem \_ suporte**</span><span class="sxs-lookup"><span data-stu-id="a25d1-190">**WS\_E\_NOT\_SUPPORTED**</span></span>
-   <span data-ttu-id="a25d1-191">**WS \_ E \_ nenhuma \_ tradução \_ disponível**</span><span class="sxs-lookup"><span data-stu-id="a25d1-191">**WS\_E\_NO\_TRANSLATION\_AVAILABLE**</span></span>
-   <span data-ttu-id="a25d1-192">**\_ \_ estouro numérico de WS E \_**</span><span class="sxs-lookup"><span data-stu-id="a25d1-192">**WS\_E\_NUMERIC\_OVERFLOW**</span></span>
-   <span data-ttu-id="a25d1-193">**\_falha no \_ objeto WS E \_**</span><span class="sxs-lookup"><span data-stu-id="a25d1-193">**WS\_E\_OBJECT\_FAULTED**</span></span>
-   <span data-ttu-id="a25d1-194">**\_operação WS \_ E \_ abandonada**</span><span class="sxs-lookup"><span data-stu-id="a25d1-194">**WS\_E\_OPERATION\_ABANDONED**</span></span>
-   <span data-ttu-id="a25d1-195">**\_operação WS \_ E \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="a25d1-195">**WS\_E\_OPERATION\_ABORTED**</span></span>
-   <span data-ttu-id="a25d1-196">**a \_ operação WS E \_ \_ atingiu o tempo \_ limite**</span><span class="sxs-lookup"><span data-stu-id="a25d1-196">**WS\_E\_OPERATION\_TIMED\_OUT**</span></span>
-   <span data-ttu-id="a25d1-197">**\_outros WS E \_**</span><span class="sxs-lookup"><span data-stu-id="a25d1-197">**WS\_E\_OTHER**</span></span>
-   <span data-ttu-id="a25d1-198">**acesso a proxy do WS \_ E \_ \_ \_ negado**</span><span class="sxs-lookup"><span data-stu-id="a25d1-198">**WS\_E\_PROXY\_ACCESS\_DENIED**</span></span>
-   <span data-ttu-id="a25d1-199">**\_falha de \_ proxy WS E \_**</span><span class="sxs-lookup"><span data-stu-id="a25d1-199">**WS\_E\_PROXY\_FAILURE**</span></span>
-   <span data-ttu-id="a25d1-200">**o \_ proxy WS E \_ \_ requer \_ \_ autenticação básica**</span><span class="sxs-lookup"><span data-stu-id="a25d1-200">**WS\_E\_PROXY\_REQUIRES\_BASIC\_AUTH**</span></span>
-   <span data-ttu-id="a25d1-201">**o \_ proxy WS E \_ \_ requer \_ \_ autenticação Digest**</span><span class="sxs-lookup"><span data-stu-id="a25d1-201">**WS\_E\_PROXY\_REQUIRES\_DIGEST\_AUTH**</span></span>
-   <span data-ttu-id="a25d1-202">**o \_ proxy WS E \_ \_ requer \_ Negotiate \_ auth**</span><span class="sxs-lookup"><span data-stu-id="a25d1-202">**WS\_E\_PROXY\_REQUIRES\_NEGOTIATE\_AUTH**</span></span>
-   <span data-ttu-id="a25d1-203">**o \_ proxy WS E \_ \_ requer \_ \_ autenticação NTLM**</span><span class="sxs-lookup"><span data-stu-id="a25d1-203">**WS\_E\_PROXY\_REQUIRES\_NTLM\_AUTH**</span></span>
-   <span data-ttu-id="a25d1-204">**cota de WS \_ E \_ \_ excedida**</span><span class="sxs-lookup"><span data-stu-id="a25d1-204">**WS\_E\_QUOTA\_EXCEEDED**</span></span>
-   <span data-ttu-id="a25d1-205">**\_ \_ \_ falha no sistema de segurança WS E \_**</span><span class="sxs-lookup"><span data-stu-id="a25d1-205">**WS\_E\_SECURITY\_SYSTEM\_FAILURE**</span></span>
-   <span data-ttu-id="a25d1-206">**TOKEN de segurança do WS \_ E \_ \_ \_ expirado**</span><span class="sxs-lookup"><span data-stu-id="a25d1-206">**WS\_E\_SECURITY\_TOKEN\_EXPIRED**</span></span>
-   <span data-ttu-id="a25d1-207">**\_ \_ \_ falha na verificação de segurança do WS E \_**</span><span class="sxs-lookup"><span data-stu-id="a25d1-207">**WS\_E\_SECURITY\_VERIFICATION\_FAILURE**</span></span>
-   <span data-ttu-id="a25d1-208">**o \_ WS \_ E \_ Server \_ requer \_ autenticação básica**</span><span class="sxs-lookup"><span data-stu-id="a25d1-208">**WS\_E\_SERVER\_REQUIRES\_BASIC\_AUTH**</span></span>
-   <span data-ttu-id="a25d1-209">**o \_ WS \_ E \_ Server \_ requer \_ autenticação Digest**</span><span class="sxs-lookup"><span data-stu-id="a25d1-209">**WS\_E\_SERVER\_REQUIRES\_DIGEST\_AUTH**</span></span>
-   <span data-ttu-id="a25d1-210">**o WS \_ E \_ Server \_ requer \_ Negotiate \_ auth**</span><span class="sxs-lookup"><span data-stu-id="a25d1-210">**WS\_E\_SERVER\_REQUIRES\_NEGOTIATE\_AUTH**</span></span>
-   <span data-ttu-id="a25d1-211">**o \_ WS \_ E \_ Server \_ requer \_ autenticação NTLM**</span><span class="sxs-lookup"><span data-stu-id="a25d1-211">**WS\_E\_SERVER\_REQUIRES\_NTLM\_AUTH**</span></span>
-   <span data-ttu-id="a25d1-212">**WS \_ S \_ Async**</span><span class="sxs-lookup"><span data-stu-id="a25d1-212">**WS\_S\_ASYNC**</span></span>
-   <span data-ttu-id="a25d1-213">**fim do WS- \_ S \_**</span><span class="sxs-lookup"><span data-stu-id="a25d1-213">**WS\_S\_END**</span></span>

<span data-ttu-id="a25d1-214">As funções a seguir fazem parte do rastreamento:</span><span class="sxs-lookup"><span data-stu-id="a25d1-214">The following functions are part of tracing:</span></span>

-   [<span data-ttu-id="a25d1-215">**\_ID da \_ propriedade de erro WS \_**</span><span class="sxs-lookup"><span data-stu-id="a25d1-215">**WS\_ERROR\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [<span data-ttu-id="a25d1-216">**\_código de exceção WS \_**</span><span class="sxs-lookup"><span data-stu-id="a25d1-216">**WS\_EXCEPTION\_CODE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

<span data-ttu-id="a25d1-217">O seguinte identificador é parte do rastreamento:</span><span class="sxs-lookup"><span data-stu-id="a25d1-217">The following handle is part of tracing:</span></span>

-   [<span data-ttu-id="a25d1-218">\_erro WS</span><span class="sxs-lookup"><span data-stu-id="a25d1-218">WS\_ERROR</span></span>](ws-error.md)

<span data-ttu-id="a25d1-219">A seguinte estrutura faz parte do rastreamento:</span><span class="sxs-lookup"><span data-stu-id="a25d1-219">The following structure is part of tracing:</span></span>

-   [<span data-ttu-id="a25d1-220">**\_propriedade de erro WS \_**</span><span class="sxs-lookup"><span data-stu-id="a25d1-220">**WS\_ERROR\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_error_property)

## <a name="security"></a><span data-ttu-id="a25d1-221">Segurança</span><span class="sxs-lookup"><span data-stu-id="a25d1-221">Security</span></span>

<span data-ttu-id="a25d1-222">Há várias considerações de segurança que o usuário do objeto de erro deve estar ciente:</span><span class="sxs-lookup"><span data-stu-id="a25d1-222">There are a number of security considerations that the user of the error object should be aware of:</span></span>

-   <span data-ttu-id="a25d1-223">O objeto de erro pode conter dados não confiáveis.</span><span class="sxs-lookup"><span data-stu-id="a25d1-223">The error object may contain untrusted data.</span></span> <span data-ttu-id="a25d1-224">Exemplos disso são: a falha do WS \_ e as cadeias de caracteres de erro, que podem ser armazenadas no objeto de erro com base nas informações recebidas por um canal não confiável.</span><span class="sxs-lookup"><span data-stu-id="a25d1-224">Examples of this are: the WS\_FAULT, and the error strings, both of which can be stored in the error object based on information received over an untrusted channel.</span></span> <span data-ttu-id="a25d1-225">O usuário do objeto de erro deve ser cuidadoso ao inspecionar as informações no objeto de erro e tomar decisões com base em seus valores.</span><span class="sxs-lookup"><span data-stu-id="a25d1-225">The user of the error object should be careful when inspecting the information in the error object and making decisions based on its values.</span></span>
-   <span data-ttu-id="a25d1-226">Um usuário do objeto de erro deve chamar [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror) depois de inspecionar as informações sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="a25d1-226">A user of the error object should call [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror) after inspecting the information about the error.</span></span> <span data-ttu-id="a25d1-227">A falha ao fazer isso pode levar à acumulação de memória.</span><span class="sxs-lookup"><span data-stu-id="a25d1-227">Failing to do so can lead to memory accumulation.</span></span>
-   <span data-ttu-id="a25d1-228">Um usuário do objeto de erro deve ser muito cuidadoso ao usar o \_ valor de \_ \_ divulgação de falha completa do WS da enumeração de [**\_ \_ divulgação de falha do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure) , pois a falha gerada pode conter informações privadas que foram acumuladas como parte do processo de gravação de erros.</span><span class="sxs-lookup"><span data-stu-id="a25d1-228">A user of the error object should be very careful when using the WS\_FULL\_FAULT\_DISCLOSURE value of the [**WS\_FAULT\_DISCLOSURE**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure) enumeration, because the generated fault could contain private information that was accumulated as part of the error recording process.</span></span>

 

 




