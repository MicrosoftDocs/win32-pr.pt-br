---
title: Configurando a sessão do servidor
description: Configurando a sessão do servidor
ms.assetid: 1e4e9440-8d70-44df-90a7-2d5e25b2f680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d41c1606cce397c49a15c62dae10531edfde93f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090934"
---
# <a name="configuring-the-server-session"></a><span data-ttu-id="791b6-103">Configurando a sessão do servidor</span><span class="sxs-lookup"><span data-stu-id="791b6-103">Configuring the Server Session</span></span>

<span data-ttu-id="791b6-104">A ID de sessão de servidor é criada com a função [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) e usada na chamada para [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty).</span><span class="sxs-lookup"><span data-stu-id="791b6-104">The server session ID is created with the [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) function, and used in the call to [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty).</span></span> <span data-ttu-id="791b6-105">O parâmetro *pPropertyInformation* aponta para a estrutura de configuração para o tipo de propriedade definido.</span><span class="sxs-lookup"><span data-stu-id="791b6-105">The *pPropertyInformation* parameter points to the configuration structure for the property type that is set.</span></span> <span data-ttu-id="791b6-106">O parâmetro *PropertyInformationLength* especifica o tamanho, em bytes, da estrutura de configuração.</span><span class="sxs-lookup"><span data-stu-id="791b6-106">The *PropertyInformationLength* parameter specifies the size, in bytes, of the configuration structure.</span></span> <span data-ttu-id="791b6-107">Por exemplo, ao definir **HttpServerTimeoutsProperty** , o parâmetro **pPropertyInformation** deve apontar para um buffer que tenha pelo menos o tamanho da estrutura [**de \_ \_ \_ informações de limite de tempo limite http**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) .</span><span class="sxs-lookup"><span data-stu-id="791b6-107">For example, when setting the **HttpServerTimeoutsProperty** the **pPropertyInformation** parameter must point to a buffer that is at least the size of the [**HTTP\_TIMEOUT\_LIMIT\_INFO**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) structure.</span></span>

<span data-ttu-id="791b6-108">Normalmente, um aplicativo HTTP cria uma única sessão de servidor e pode definir propriedades de todo o aplicativo, como o limite de limitação de largura de banda global ou habilitar o log centralizado nessa sessão de servidor.</span><span class="sxs-lookup"><span data-stu-id="791b6-108">Typically an HTTP application creates a single server session and may set application wide properties such as global bandwidth throttling limit or enable centralized logging on this server session.</span></span> <span data-ttu-id="791b6-109">[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) substitui as configurações de API do servidor http para o aplicativo de chamada; Ele não afeta as propriedades de toda a API do servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="791b6-109">[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) overrides the HTTP Server API configurations for the calling application; it does not affect the HTTP Server API-wide properties.</span></span> <span data-ttu-id="791b6-110">As configurações de sessão de servidor são consultadas chamando [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty).</span><span class="sxs-lookup"><span data-stu-id="791b6-110">The server session configurations are queried by calling [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty).</span></span>

 

 




