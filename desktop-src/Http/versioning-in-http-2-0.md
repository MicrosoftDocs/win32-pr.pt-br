---
title: Controle de versão (API do servidor HTTP)
description: A API do servidor HTTP versão 2,0 aplica o controle de versão com escopo de objeto para determinar a versão da API.
ms.assetid: 2c2d7501-85e0-44ec-aa42-01372b29266e
keywords:
- Controle de versão na API do servidor HTTP versão 2,0
- API do servidor HTTP versão 2,0, controle de versão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5221ff7a93bb24e7e0b8a1b9f7c2399012cdbe95
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085065"
---
# <a name="versioning-http-server-api"></a>Controle de versão (API do servidor HTTP)

A API do servidor HTTP versão 2,0 torna obsoleta as filas de solicitação da versão 1,0 e as associações de URL com a fila de solicitações. O controle de versão com escopo de objeto permite que os aplicativos forneçam informações de versão específicas do aplicativo. Os aplicativos podem chamar automaticamente a versão correta de estruturas para o sistema operacional no qual ele está sendo executado.

## <a name="request-queues"></a>Filas de solicitações

A partir da API do servidor HTTP versão 2,0, as filas de solicitação são criadas com [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) tornando obsoleta a função 1,0 [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) da versão. Os grupos de URLs são introduzidos na versão 2,0 com a função [**HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) . As URLs são adicionadas ao grupo usando [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) , o que torna obsoleto a função [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) da versão 1,0. Os grupos de URLs da versão 2,0 não devem ser usados com as filas de solicitação da versão 1,0.

A partir da versão 2,0, as seguintes funções da versão 1,0 são obsoletas e não podem ser usadas com a versão 2,0 das filas de solicitação:

-   [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle)
-   [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl)
-   [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl)

Para obter mais informações sobre como configurar grupos de URLs, consulte o tópico [Configurando o grupo de URLs](configuring-the-url-group.md) . Para obter mais informações sobre as filas de solicitações da versão 2,0, consulte o tópico [fila de solicitações nomeadas](named-request-queue.md) .

## <a name="object-scoped-versioning"></a>Object-Scoped controle de versão

Na versão 1,0, o aplicativo fornece a versão da API do servidor HTTP na chamada para [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize). As informações de versão são aceitas somente do primeiro aplicativo que chamou **HttpInitialize** e são aplicadas a todos os aplicativos de API do servidor http no mesmo processo. A partir da API da versão 2,0, as informações de versão global fornecidas na chamada para **HttpInitialize** não são usadas. Para aplicativos da versão 2,0, a versão da API do servidor HTTP é passada no parâmetro version quando a fila de solicitação ou sessão de servidor é criada por [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) ou [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession). Quando a fila de solicitações é criada com a versão 1,0 [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle), ela é marcada automaticamente como a versão 1,0. Os aplicativos da versão 1,0 e da versão 2,0 podem ser executados no mesmo processo.

As estruturas de [**\_ solicitação HTTP**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) e [**\_ resposta http**](http-response.md) são atualizadas para incluir informações de autenticação na API do servidor http versão 2,0. [**Http \_ A solicitação \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) e a [**\_ solicitação HTTP \_ v2**](/windows/desktop/api/Http/ns-http-http_request_v2) são específicas para a versão da API usada pelo aplicativo. No entanto, os aplicativos não devem usar essas estruturas diretamente em seu código; em vez disso, eles devem usar a **\_ solicitação HTTP** para obter a versão correta com base na versão da fila de solicitações em que a solicitação foi recebida. Além disso, lembre-se de que o tamanho da estrutura de **\_ solicitação HTTP** é baseado na versão do sistema operacional sob a qual o código é compilado.

 

 
