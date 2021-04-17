---
description: Suporte de proxy para fontes de rede
ms.assetid: e739746d-2a09-4237-a7c1-0aed4e4516d7
title: Suporte de proxy para fontes de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97bc1172c072a54f9f76cbcd3a297a972efbde29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813302"
---
# <a name="proxy-support-for-network-sources"></a><span data-ttu-id="fc76c-103">Suporte de proxy para fontes de rede</span><span class="sxs-lookup"><span data-stu-id="fc76c-103">Proxy Support for Network Sources</span></span>

<span data-ttu-id="fc76c-104">Um servidor proxy é um servidor intermediário entre a intranet e a Internet, que roteia solicitações do aplicativo cliente para o servidor de mídia e recupera arquivos do servidor de mídia.</span><span class="sxs-lookup"><span data-stu-id="fc76c-104">A proxy server is an intermediate server between your intranet and the Internet, which routes requests from the client application to the media server and retrieves files from the media server.</span></span>

<span data-ttu-id="fc76c-105">Media Foundation Cria implicitamente um objeto de *localizador de proxy* quando um aplicativo cliente tenta acessar uma URL de origem.</span><span class="sxs-lookup"><span data-stu-id="fc76c-105">Media Foundation implicitly creates a *proxy locator* object when a client application tries to access a source URL.</span></span> <span data-ttu-id="fc76c-106">O objeto de localizador de proxy expõe a interface [**IMFNetProxyLocator**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="fc76c-106">The proxy locator object exposes the [**IMFNetProxyLocator**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator) interface.</span></span> <span data-ttu-id="fc76c-107">Durante a resolução da origem, Media Foundation verifica se o repositório de propriedades foi passado para o método do resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="fc76c-107">During source resolution, Media Foundation checks the property store passed to the source resolver method.</span></span>

<span data-ttu-id="fc76c-108">Se o repositório de propriedades contiver o conjunto de propriedades [MFNETSOURCE \_ PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) para um objeto de fábrica localizador de proxy implementado pelo aplicativo, ele invocará o método [**IMFNetProxyLocatorFactory:: CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) para criar um localizador de proxy com definições de configuração personalizadas.</span><span class="sxs-lookup"><span data-stu-id="fc76c-108">If the property store contains the [MFNETSOURCE\_PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) property set to a proxy locator factory object implemented by the application then, it invokes the [**IMFNetProxyLocatorFactory::CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) method to create a proxy locator with custom configuration settings.</span></span>

<span data-ttu-id="fc76c-109">Se o repositório de propriedades não estiver definido, Media Foundation criará o localizador de proxy com a configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="fc76c-109">If the property store is not set, then Media Foundation creates the proxy locator with default configuration.</span></span> <span data-ttu-id="fc76c-110">Essas configurações são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="fc76c-110">These settings are as follows:</span></span>

-   <span data-ttu-id="fc76c-111">Se a política de usuário estiver definida, o localizador de proxy usará as configurações especificadas no registro.</span><span class="sxs-lookup"><span data-stu-id="fc76c-111">If user policy is set, then the proxy locator uses settings specified in the registry.</span></span>

-   <span data-ttu-id="fc76c-112">Para HTTP, o localizador de proxy usa as configurações de proxy do navegador.</span><span class="sxs-lookup"><span data-stu-id="fc76c-112">For HTTP, the proxy locator uses browser proxy settings.</span></span>

-   <span data-ttu-id="fc76c-113">Para RTSP, o localizador de proxy é configurado para ignorar servidores proxy ao se conectar ao servidor de mídia.</span><span class="sxs-lookup"><span data-stu-id="fc76c-113">For RTSP, the proxy locator is configured to bypass proxy servers when connecting to the media server.</span></span>

<span data-ttu-id="fc76c-114">Essa configuração padrão pode ser alterada pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc76c-114">This default configuration can be changed by the application.</span></span> <span data-ttu-id="fc76c-115">Os tópicos a seguir contêm informações sobre as definições de configuração para um localizador de proxy:</span><span class="sxs-lookup"><span data-stu-id="fc76c-115">The following topics contain information about the configuration settings for a proxy locator:</span></span>

-   [<span data-ttu-id="fc76c-116">Definições de configuração do localizador de proxy</span><span class="sxs-lookup"><span data-stu-id="fc76c-116">Proxy Locator Configuration Settings</span></span>](proxy-locator-configuration-settings.md)

-   [<span data-ttu-id="fc76c-117">Como configurar o localizador de proxy</span><span class="sxs-lookup"><span data-stu-id="fc76c-117">How to Configure the Proxy Locator</span></span>](how-to-configure-the-proxy-locator.md)

<span data-ttu-id="fc76c-118">Media Foundation Inicializa o localizador de proxy para a URL de origem especificada para o [resolvedor de origem](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="fc76c-118">Media Foundation initializes the proxy locator for the source URL specified to the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="fc76c-119">O localizador de proxy detecta um servidor proxy a ser usado com base nas definições de configuração.</span><span class="sxs-lookup"><span data-stu-id="fc76c-119">The proxy locator detects a proxy server to use based on configuration settings.</span></span> <span data-ttu-id="fc76c-120">Quando o localizador de proxy tenta definir um servidor proxy, ele registra o resultado de êxito ou falha no registro.</span><span class="sxs-lookup"><span data-stu-id="fc76c-120">When the proxy locator attempts the set a proxy server, it records the success or failure result in the registry.</span></span> <span data-ttu-id="fc76c-121">Esse valor é verificado durante o próximo processo de detecção de proxy.</span><span class="sxs-lookup"><span data-stu-id="fc76c-121">This value is checked during the next proxy detection process.</span></span> <span data-ttu-id="fc76c-122">Se um determinado servidor proxy for conhecido por ter causado falhas no passado, o localizador de proxy o ignorará.</span><span class="sxs-lookup"><span data-stu-id="fc76c-122">If a certain proxy server is known to have caused failures in the past, the proxy locator skips it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc76c-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc76c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc76c-124">Atributos e propriedades</span><span class="sxs-lookup"><span data-stu-id="fc76c-124">Attributes and Properties</span></span>](attributes-and-properties.md)
</dt> <dt>

[<span data-ttu-id="fc76c-125">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fc76c-125">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 



