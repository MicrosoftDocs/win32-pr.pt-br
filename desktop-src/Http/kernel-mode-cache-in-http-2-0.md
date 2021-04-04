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
# <a name="kernel-mode-cache"></a>Cache de modo kernel

A API do servidor HTTP versão 2,0 permite que os aplicativos armazenem em cache as respostas com conteúdo estático no modo kernel. O aumento do desempenho é obtido quando as solicitações são servidas do cache do kernel sem fazer a transição para o modo de usuário.

A API do servidor HTTP aplica as configurações de propriedade apropriadas a todas as solicitações servidas do cache do kernel, incluindo as respostas de log. As solicitações que exigem autenticação, no entanto, não serão servidas do cache.

A API do servidor HTTP limita o cache do modo kernel a solicitações que atendam às seguintes condições:

-   O verbo de solicitação é GET e toda a solicitação é recebida.
-   A solicitação não deve ter um corpo de entidade.
-   O protocolo HTTP é a versão 1,0 ou posterior.
-   O cabeçalho "Translate: f" não está presente.
-   Espera-se que cabeçalhos diferentes de "espera: 100-Continue" não estejam presentes.
-   O cabeçalho de autorização não está presente.
-   O intervalo e os cabeçalhos de If-Range não estão presentes.

Além das restrições na solicitação, a resposta também deve atender às seguintes condições:

-   O tamanho da resposta é limitado a 256 KB, por padrão. Para alterar o tamanho da resposta armazenada em cache, defina o valor do registro **UriMaxUriBytes** para o número necessário de bytes.

    ```
    HKEY_LOCAL_MACHINE
       System
          CurrentControlSet
             Services
                HTTP
                   Parameters
                      UriMaxUriBytes
    ```

-   A resposta inteira deve ser fornecida em uma única chamada para [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse).
-   O cabeçalho de data na resposta não deve ser suprimido.
-   Se o cabeçalho Last-Modified estiver presente, o valor do cabeçalho deverá ter a sintaxe correta. O valor de hora neste cabeçalho é usado para verificação de controle de cache.
-   O cache de modo kernel tem espaço suficiente restante para armazenar a resposta.

Por padrão, o cache de resposta do modo kernel está habilitado. Se qualquer uma das condições para a solicitação ou resposta listada acima não for atendida, a resposta será enviada, mas não será armazenada em cache. Na API do servidor HTTP versão 2,0, [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) inclui um parâmetro *pCachePolicy* opcional para passar a estrutura de [**\_ \_ política de cache http**](/windows/desktop/api/Http/ns-http-http_cache_policy) . Os aplicativos usam a estrutura de política de cache para configurar o cache.

 

 




