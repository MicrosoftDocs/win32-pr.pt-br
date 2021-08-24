---
title: Cache de modo kernel
description: Cache de modo kernel
ms.assetid: f9a46ff4-779b-4b3a-b8f5-1ae10a3c0a61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c34296ae6d0bca81988437478eb5893f1a7cb1b3c8a0dc2ae461356499bbfe10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119340496"
---
# <a name="kernel-mode-cache"></a>Cache de modo kernel

A API do SERVIDOR HTTP versão 2.0 permite que os aplicativos armazenam em cache as respostas com conteúdo estático no modo kernel. O maior desempenho é obtido quando as solicitações são atendidas do cache do kernel sem fazer a transição para o modo de usuário.

A API do Servidor HTTP aplica as configurações de propriedade apropriadas a todas as solicitações atendidas do cache do kernel, incluindo respostas de log. As solicitações que exigem autenticação, no entanto, não serão atendidas do cache.

A API do Servidor HTTP limita o cache do modo kernel a solicitações que atendem às seguintes condições:

-   O verbo de solicitação é GET e toda a solicitação é recebida.
-   A solicitação não deve ter um corpo de entidade.
-   O protocolo HTTP é a versão 1.0 ou posterior.
-   O header "Translate: f" não está presente.
-   Os headers esperados que não sejam "Esperar: 100-Continuar" não estão presentes.
-   O header de autorização não está presente.
-   Os headers Range e If-Range não estão presentes.

Além das restrições na solicitação, a resposta também deve atender às seguintes condições:

-   O tamanho da resposta é limitado a 256 KB, por padrão. Para alterar o tamanho da resposta armazenada em cache, de definir o valor do Registro **UriMaxUriBytes** como o número necessário de bytes.

    ```
    HKEY_LOCAL_MACHINE
       System
          CurrentControlSet
             Services
                HTTP
                   Parameters
                      UriMaxUriBytes
    ```

-   Toda a resposta deve ser fornecida em uma única chamada para [**HttpSendHttpResponse.**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)
-   O header de data na resposta não deve ser suprimido.
-   Se o header da última modificação estiver presente, o valor do header deverá ter a sintaxe correta. O valor de hora nesse header é usado para verificação de controle de cache.
-   O cache do modo kernel tem espaço suficiente para armazenar a resposta.

Por padrão, o cache de resposta do modo kernel está habilitado. Se qualquer uma das condições para a solicitação ou resposta listada acima não for atendida, a resposta será enviada, mas não será armazenada em cache. Na API do Servidor HTTP versão 2.0, [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) inclui um parâmetro *pCachePolicy* opcional para passar a estrutura [**HTTP CACHE \_ \_ POLICY.**](/windows/desktop/api/Http/ns-http-http_cache_policy) Os aplicativos usam a estrutura de política de cache para configurar o cache.

 

 




