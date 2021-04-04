---
title: Cache de modo kernel
description: .
ms.assetid: f9a46ff4-779b-4b3a-b8f5-1ae10a3c0a61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9264535a58c033d66fd3fcc39988a292afc2a27f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006058"
---
# <a name="kernel-mode-cache"></a><span data-ttu-id="05f33-103">Cache de modo kernel</span><span class="sxs-lookup"><span data-stu-id="05f33-103">Kernel Mode Cache</span></span>

<span data-ttu-id="05f33-104">A API do servidor HTTP versão 2,0 permite que os aplicativos armazenem em cache as respostas com conteúdo estático no modo kernel.</span><span class="sxs-lookup"><span data-stu-id="05f33-104">The HTTP Server version 2.0 API allows applications to cache responses with static content in kernel mode.</span></span> <span data-ttu-id="05f33-105">O aumento do desempenho é obtido quando as solicitações são servidas do cache do kernel sem fazer a transição para o modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="05f33-105">Increased performance is achieved when requests are served from the kernel cache without transitioning to user mode.</span></span>

<span data-ttu-id="05f33-106">A API do servidor HTTP aplica as configurações de propriedade apropriadas a todas as solicitações servidas do cache do kernel, incluindo as respostas de log.</span><span class="sxs-lookup"><span data-stu-id="05f33-106">The HTTP Server API applies the appropriate property configurations to all requests served from the kernel cache, including logging responses.</span></span> <span data-ttu-id="05f33-107">As solicitações que exigem autenticação, no entanto, não serão servidas do cache.</span><span class="sxs-lookup"><span data-stu-id="05f33-107">Requests that require authentication, however, will not be served from the cache.</span></span>

<span data-ttu-id="05f33-108">A API do servidor HTTP limita o cache do modo kernel a solicitações que atendam às seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="05f33-108">The HTTP Server API limits the kernel mode cache to requests that meet the following conditions:</span></span>

-   <span data-ttu-id="05f33-109">O verbo de solicitação é GET e toda a solicitação é recebida.</span><span class="sxs-lookup"><span data-stu-id="05f33-109">The request verb is GET and the entire request is received.</span></span>
-   <span data-ttu-id="05f33-110">A solicitação não deve ter um corpo de entidade.</span><span class="sxs-lookup"><span data-stu-id="05f33-110">The request must not have an entity body.</span></span>
-   <span data-ttu-id="05f33-111">O protocolo HTTP é a versão 1,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="05f33-111">The HTTP protocol is version 1.0 or later.</span></span>
-   <span data-ttu-id="05f33-112">O cabeçalho "Translate: f" não está presente.</span><span class="sxs-lookup"><span data-stu-id="05f33-112">The "Translate: f " header is not present.</span></span>
-   <span data-ttu-id="05f33-113">Espera-se que cabeçalhos diferentes de "espera: 100-Continue" não estejam presentes.</span><span class="sxs-lookup"><span data-stu-id="05f33-113">Expect headers other than "Expect: 100-Continue" are not present.</span></span>
-   <span data-ttu-id="05f33-114">O cabeçalho de autorização não está presente.</span><span class="sxs-lookup"><span data-stu-id="05f33-114">The authorization header is not present.</span></span>
-   <span data-ttu-id="05f33-115">O intervalo e os cabeçalhos de If-Range não estão presentes.</span><span class="sxs-lookup"><span data-stu-id="05f33-115">The Range and If-Range headers are not present.</span></span>

<span data-ttu-id="05f33-116">Além das restrições na solicitação, a resposta também deve atender às seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="05f33-116">In addition to the restrictions on the request, the response must also meet the following conditions:</span></span>

-   <span data-ttu-id="05f33-117">O tamanho da resposta é limitado a 256 KB, por padrão.</span><span class="sxs-lookup"><span data-stu-id="05f33-117">Response size is limited to 256 KB, by default.</span></span> <span data-ttu-id="05f33-118">Para alterar o tamanho da resposta armazenada em cache, defina o valor do registro **UriMaxUriBytes** para o número necessário de bytes.</span><span class="sxs-lookup"><span data-stu-id="05f33-118">To change the size of the response that is cached, set the **UriMaxUriBytes** registry value to the required number of bytes.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       System
          CurrentControlSet
             Services
                HTTP
                   Parameters
                      UriMaxUriBytes
    ```

-   <span data-ttu-id="05f33-119">A resposta inteira deve ser fornecida em uma única chamada para [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse).</span><span class="sxs-lookup"><span data-stu-id="05f33-119">The entire response must be provided in a single call to [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse).</span></span>
-   <span data-ttu-id="05f33-120">O cabeçalho de data na resposta não deve ser suprimido.</span><span class="sxs-lookup"><span data-stu-id="05f33-120">The date header on the response must not be suppressed.</span></span>
-   <span data-ttu-id="05f33-121">Se o cabeçalho Last-Modified estiver presente, o valor do cabeçalho deverá ter a sintaxe correta.</span><span class="sxs-lookup"><span data-stu-id="05f33-121">If the last-modified header is present, the value of the header must have the correct syntax.</span></span> <span data-ttu-id="05f33-122">O valor de hora neste cabeçalho é usado para verificação de controle de cache.</span><span class="sxs-lookup"><span data-stu-id="05f33-122">The time value in this header is used for cache control verification.</span></span>
-   <span data-ttu-id="05f33-123">O cache de modo kernel tem espaço suficiente restante para armazenar a resposta.</span><span class="sxs-lookup"><span data-stu-id="05f33-123">The kernel mode cache has enough space left to store the response.</span></span>

<span data-ttu-id="05f33-124">Por padrão, o cache de resposta do modo kernel está habilitado.</span><span class="sxs-lookup"><span data-stu-id="05f33-124">By default, kernel mode response cache is enabled.</span></span> <span data-ttu-id="05f33-125">Se qualquer uma das condições para a solicitação ou resposta listada acima não for atendida, a resposta será enviada, mas não será armazenada em cache.</span><span class="sxs-lookup"><span data-stu-id="05f33-125">If any of the conditions for the request or response listed above are not met, the response will be sent, but it will not be cached.</span></span> <span data-ttu-id="05f33-126">Na API do servidor HTTP versão 2,0, [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) inclui um parâmetro *pCachePolicy* opcional para passar a estrutura de [**\_ \_ política de cache http**](/windows/desktop/api/Http/ns-http-http_cache_policy) .</span><span class="sxs-lookup"><span data-stu-id="05f33-126">In HTTP Server version 2.0 API, [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) includes an optional *pCachePolicy* parameter to pass the [**HTTP\_CACHE\_POLICY**](/windows/desktop/api/Http/ns-http-http_cache_policy) structure.</span></span> <span data-ttu-id="05f33-127">Os aplicativos usam a estrutura de política de cache para configurar o cache.</span><span class="sxs-lookup"><span data-stu-id="05f33-127">Applications use the cache policy structure to configure the cache.</span></span>

 

 




