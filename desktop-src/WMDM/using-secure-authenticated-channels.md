---
title: Usando canais autenticados seguros
description: Usando canais autenticados seguros
ms.assetid: ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7
keywords:
- Windows Media Gerenciador de Dispositivos, autenticação
- Gerenciador de Dispositivos, autenticação
- aplicativos de área de trabalho, autenticação
- provedores de serviços, autenticação
- Guia de programação, autenticação
- autenticação
- Windows Media Gerenciador de Dispositivos, comunicação segura
- Gerenciador de Dispositivos, comunicação segura
- aplicativos de área de trabalho, comunicação segura
- provedores de serviços, comunicação segura
- Guia de programação, comunicação segura
- comunicação segura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f88c271cecc2e9252a3f7af0540beef3dc57d2b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005147"
---
# <a name="using-secure-authenticated-channels"></a><span data-ttu-id="c6842-115">Usando canais autenticados seguros</span><span class="sxs-lookup"><span data-stu-id="c6842-115">Using Secure Authenticated Channels</span></span>

<span data-ttu-id="c6842-116">O Windows Media Gerenciador de Dispositivos permite a autenticação e a comunicação segura entre os componentes, fornecendo duas classes auxiliares, [CSecureChannelClient](csecurechannelclient-class.md) (para aplicativos) e [CSecureChannelServer](csecurechannelserver-class.md) (para provedores de serviço) e uma interface, [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) (para ambos).</span><span class="sxs-lookup"><span data-stu-id="c6842-116">Windows Media Device Manager enables authentication and secure communication between components by providing two helper classes, [CSecureChannelClient](csecurechannelclient-class.md) (for applications) and [CSecureChannelServer](csecurechannelserver-class.md) (for service providers), and one interface, [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) (for both).</span></span> <span data-ttu-id="c6842-117">Juntos, eles compõem uma API para o uso de canais autenticados seguros (SAC).</span><span class="sxs-lookup"><span data-stu-id="c6842-117">Together these make up an API for the use of secure authenticated channels (SAC).</span></span> <span data-ttu-id="c6842-118">O SAC lida com as três tarefas a seguir para provedores de serviços ou aplicativos usando o Windows Media Gerenciador de Dispositivos:</span><span class="sxs-lookup"><span data-stu-id="c6842-118">SAC handles the following three tasks for service providers or applications using Windows Media Device Manager:</span></span>

-   [<span data-ttu-id="c6842-119">Autenticação de componente</span><span class="sxs-lookup"><span data-stu-id="c6842-119">Component Authentication</span></span>](component-authentication.md)
-   [<span data-ttu-id="c6842-120">Criptografia e descriptografia</span><span class="sxs-lookup"><span data-stu-id="c6842-120">Encryption and Decryption</span></span>](encryption-and-decryption.md)
-   [<span data-ttu-id="c6842-121">Autenticação de mensagens</span><span class="sxs-lookup"><span data-stu-id="c6842-121">Message Authentication</span></span>](message-authentication.md)

<span data-ttu-id="c6842-122">Um aplicativo ou provedor de serviços deve tratar da autenticação, criptografia e descriptografia de componentes; a autenticação de mensagens é opcional.</span><span class="sxs-lookup"><span data-stu-id="c6842-122">An application or service provider must handle component authentication, encryption, and decryption; message authentication is optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6842-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c6842-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6842-124">**Tarefas comuns a aplicativos e provedores de serviços**</span><span class="sxs-lookup"><span data-stu-id="c6842-124">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




