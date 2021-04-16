---
description: Os ELS (serviços lingüísticos estendidos) são implementados como uma DLL (biblioteca de vínculo dinâmico) que fornece uma variedade de funcionalidades lingüísticas de suporte para o texto especificado pelo aplicativo.
ms.assetid: 23d4e42a-a5bb-467c-a8b9-6a57ae39daa0
title: Sobre os serviços lingüísticos estendidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6594fcfe67954a56cb09e239221b2b529d4d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759396"
---
# <a name="about-extended-linguistic-services"></a><span data-ttu-id="661f1-103">Sobre os serviços lingüísticos estendidos</span><span class="sxs-lookup"><span data-stu-id="661f1-103">About Extended Linguistic Services</span></span>

<span data-ttu-id="661f1-104">Os ELS (serviços lingüísticos estendidos) são implementados como uma DLL (biblioteca de vínculo dinâmico) que fornece uma variedade de funcionalidades lingüísticas de suporte para o texto especificado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="661f1-104">Extended Linguistic Services (ELS) is implemented as a dynamic-link library (DLL) that provides a variety of linguistic support functionality for text that the application specifies.</span></span> <span data-ttu-id="661f1-105">A tecnologia inclui a plataforma ELS e os plug-ins para vários tipos de serviço linguísticos predefinidos acessíveis para o aplicativo por meio da plataforma.</span><span class="sxs-lookup"><span data-stu-id="661f1-105">The technology includes the ELS platform and plug-ins for several predefined linguistic service types accessible to the application through the platform.</span></span>

> [!Note]  
> <span data-ttu-id="661f1-106">O módulo ELS é instalado automaticamente com o Windows 7 e posterior.</span><span class="sxs-lookup"><span data-stu-id="661f1-106">The ELS module is installed automatically with Windows 7 and later.</span></span>

 

## <a name="els-platform"></a><span data-ttu-id="661f1-107">Plataforma ELS</span><span class="sxs-lookup"><span data-stu-id="661f1-107">ELS Platform</span></span>

<span data-ttu-id="661f1-108">A plataforma ELS é a interface entre seu aplicativo e os serviços do ELS.</span><span class="sxs-lookup"><span data-stu-id="661f1-108">The ELS platform is the interface between your application and the ELS services.</span></span> <span data-ttu-id="661f1-109">Ele fornece uma maneira simples de implementar vários tipos de funcionalidades linguísticas por meio da mesma API, que permite que o aplicativo acesse e use serviços específicos.</span><span class="sxs-lookup"><span data-stu-id="661f1-109">It provides a simple way to implement several kinds of linguistic functionality through the same API, which allows the application to access and use specific services.</span></span> <span data-ttu-id="661f1-110">Para obter mais informações sobre a API, consulte [referência de serviços linguísticas estendidos.](extended-linguistic-services-reference.md)</span><span class="sxs-lookup"><span data-stu-id="661f1-110">For more information about the API, see [Extended Linguistic Services Reference.](extended-linguistic-services-reference.md)</span></span>

> [!Note]  
> <span data-ttu-id="661f1-111">Quando o aplicativo chama qualquer uma das funções da API ELS, a plataforma aloca memória e recursos conforme necessário para comunicação com os serviços.</span><span class="sxs-lookup"><span data-stu-id="661f1-111">When the application calls any of the ELS API functions, the platform allocates memory and resources as needed for communication with the services.</span></span> <span data-ttu-id="661f1-112">O aplicativo é responsável por chamar a plataforma novamente para liberar esses recursos.</span><span class="sxs-lookup"><span data-stu-id="661f1-112">The application is responsible for calling the platform again to free these resources.</span></span>

 

<span data-ttu-id="661f1-113">A plataforma é executada dentro do espaço de memória virtual do aplicativo e toda a memória alocada faz parte desse espaço.</span><span class="sxs-lookup"><span data-stu-id="661f1-113">The platform runs inside the application virtual memory space, and all allocated memory is part of this space.</span></span> <span data-ttu-id="661f1-114">Portanto, seu aplicativo só precisa vincular à DLL do componente ELS (Elscore.dll) vinculando-se a Elscore. lib ou carregando dinamicamente Elscore.dll.</span><span class="sxs-lookup"><span data-stu-id="661f1-114">Thus your application only needs to link to the ELS component DLL (Elscore.dll) by linking to Elscore.lib or by dynamically loading Elscore.dll.</span></span>

## <a name="els-services"></a><span data-ttu-id="661f1-115">Serviços ELSs</span><span class="sxs-lookup"><span data-stu-id="661f1-115">ELS Services</span></span>

<span data-ttu-id="661f1-116">Para o Windows 7 e posterior, a plataforma ELS dá suporte apenas aos seguintes serviços predefinidos.</span><span class="sxs-lookup"><span data-stu-id="661f1-116">For Windows 7 and later, the ELS platform supports only the following predefined services.</span></span>

-   [<span data-ttu-id="661f1-117">Detecção de Idioma da Microsoft</span><span class="sxs-lookup"><span data-stu-id="661f1-117">Microsoft Language Detection</span></span>](microsoft-language-detection.md)
-   [<span data-ttu-id="661f1-118">Detecção de script da Microsoft</span><span class="sxs-lookup"><span data-stu-id="661f1-118">Microsoft Script Detection</span></span>](microsoft-script-detection.md)
-   [<span data-ttu-id="661f1-119">Serviços de transliteração</span><span class="sxs-lookup"><span data-stu-id="661f1-119">Transliteration services</span></span>](transliteration-services.md)

> [!Note]  
> <span data-ttu-id="661f1-120">As versões futuras do ELS terão suporte para serviços adicionais fornecidos pela Microsoft ou pelos provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="661f1-120">Future versions of ELS will support additional services provided by Microsoft or service providers.</span></span>

 

<span data-ttu-id="661f1-121">Cada serviço é associado a uma categoria de serviço que descreve o que o serviço faz.</span><span class="sxs-lookup"><span data-stu-id="661f1-121">Each service is associated with a service category describing what the service does.</span></span> <span data-ttu-id="661f1-122">A categoria é representada por uma cadeia de caracteres não localizável.</span><span class="sxs-lookup"><span data-stu-id="661f1-122">The category is represented by a nonlocalizable string.</span></span> <span data-ttu-id="661f1-123">Ele é usado por aplicativos para enumerar os serviços disponíveis.</span><span class="sxs-lookup"><span data-stu-id="661f1-123">It is used by applications to enumerate available services.</span></span> <span data-ttu-id="661f1-124">As categorias de serviço atuais são:</span><span class="sxs-lookup"><span data-stu-id="661f1-124">The current service categories are:</span></span>

-   <span data-ttu-id="661f1-125">"Detecção de Idioma"</span><span class="sxs-lookup"><span data-stu-id="661f1-125">"Language Detection"</span></span>
-   <span data-ttu-id="661f1-126">"Detecção de script"</span><span class="sxs-lookup"><span data-stu-id="661f1-126">"Script Detection"</span></span>
-   <span data-ttu-id="661f1-127">Transliteração</span><span class="sxs-lookup"><span data-stu-id="661f1-127">"Transliteration"</span></span>

<span data-ttu-id="661f1-128">A plataforma usa metadados de serviço para enumerar os serviços solicitados pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="661f1-128">The platform uses service metadata to enumerate the services requested by the application.</span></span> <span data-ttu-id="661f1-129">Propriedades como o GUID (identificador global exclusivo) de serviço, os scripts e os idiomas de entrada e saída com suporte e a categoria de serviço podem ser usados pelo aplicativo para enumerar os serviços ELS desejados.</span><span class="sxs-lookup"><span data-stu-id="661f1-129">Properties such as the service globally unique identifier (GUID), supported input and output languages and scripts, and the service category can be used by the application to enumerate the desired ELS services.</span></span>

<span data-ttu-id="661f1-130">Cada serviço ELS é implementado como um plug-in com suporte de uma DLL que pode ser instalada no sistema operacional para que a plataforma ELS possa detectá-la e usá-la.</span><span class="sxs-lookup"><span data-stu-id="661f1-130">Each ELS service is implemented as a plug-in supported by a DLL that can be installed on the operating system so that the ELS platform can detect and use it.</span></span> <span data-ttu-id="661f1-131">Os serviços podem expor seus próprios subserviços, se necessário.</span><span class="sxs-lookup"><span data-stu-id="661f1-131">Services can expose their own subservices, if required.</span></span>

## <a name="main-els-operations"></a><span data-ttu-id="661f1-132">Principais operações de ELS</span><span class="sxs-lookup"><span data-stu-id="661f1-132">Main ELS Operations</span></span>

<span data-ttu-id="661f1-133">Esta seção descreve as principais operações com suporte pela plataforma ELS.</span><span class="sxs-lookup"><span data-stu-id="661f1-133">This section describes the main operations supported by the ELS platform.</span></span> <span data-ttu-id="661f1-134">A plataforma dá suporte aos modos de chamada síncrono e assíncrono.</span><span class="sxs-lookup"><span data-stu-id="661f1-134">The platform supports both synchronous and asynchronous calling modes.</span></span> <span data-ttu-id="661f1-135">O modo de chamada assíncrona usa um pool de threads de aplicativo para agendar threads para processamento de solicitações.</span><span class="sxs-lookup"><span data-stu-id="661f1-135">The asynchronous calling mode uses an application thread pool to schedule threads for processing requests.</span></span>

> [!Note]  
> <span data-ttu-id="661f1-136">Como a plataforma dá suporte a um modo assíncrono, os serviços ELSs não precisam implementar esse tipo de funcionalidade por conta própria.</span><span class="sxs-lookup"><span data-stu-id="661f1-136">Since the platform supports an asynchronous mode, ELS services do not have to implement this type of functionality on their own.</span></span>

 

### <a name="service-enumeration"></a><span data-ttu-id="661f1-137">Enumeração de serviço</span><span class="sxs-lookup"><span data-stu-id="661f1-137">Service Enumeration</span></span>

<span data-ttu-id="661f1-138">A plataforma ELS carrega e gerencia todos os serviços do ELS, tornando a operação transparente para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="661f1-138">The ELS platform loads and manages all ELS services, making operation transparent to the application.</span></span> <span data-ttu-id="661f1-139">O aplicativo enumera os serviços disponíveis chamando [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices).</span><span class="sxs-lookup"><span data-stu-id="661f1-139">The application enumerates the available services by calling [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices).</span></span> <span data-ttu-id="661f1-140">Para obter instruções de programação, consulte [enumerando e liberando serviços](enumerating-and-freeing-services.md).</span><span class="sxs-lookup"><span data-stu-id="661f1-140">For programming instructions, see [Enumerating and Freeing Services](enumerating-and-freeing-services.md).</span></span>

> [!Note]  
> <span data-ttu-id="661f1-141">É aconselhável por motivos de desempenho para que seu aplicativo enumere os serviços disponíveis apenas uma vez.</span><span class="sxs-lookup"><span data-stu-id="661f1-141">It is advisable for performance reasons to have your application enumerate the available services only once.</span></span> <span data-ttu-id="661f1-142">A plataforma ELS verifica os serviços novamente na próxima enumeração para garantir que seus resultados de enumeração sejam sempre atuais.</span><span class="sxs-lookup"><span data-stu-id="661f1-142">The ELS platform checks the services again on the next enumeration to ensure that its enumeration results are always current.</span></span>

 

### <a name="text-recognition"></a><span data-ttu-id="661f1-143">Reconhecimento de texto</span><span class="sxs-lookup"><span data-stu-id="661f1-143">Text Recognition</span></span>

<span data-ttu-id="661f1-144">Após a enumeração de serviço, o aplicativo chama a função [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) para usar um serviço ELS específico para mapear qualquer intervalo de texto de texto de entrada para o texto de saída.</span><span class="sxs-lookup"><span data-stu-id="661f1-144">After service enumeration, the application calls the [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) function to use a particular ELS service to map any text range of input text to output text.</span></span> <span data-ttu-id="661f1-145">Um exemplo de reconhecimento de texto é o uso de um serviço de detecção de idioma que recebe um segmento de texto e detecta sua linguagem mais provável.</span><span class="sxs-lookup"><span data-stu-id="661f1-145">An example of text recognition is the use of a language detection service that receives a text segment and detects its most probable language.</span></span>

<span data-ttu-id="661f1-146">Depois que o serviço reconheceu o texto, [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) retorna com uma estrutura de [**recipiente de \_ Propriedades \_ de mapeamento**](/windows/desktop/api/Elscore/ns-elscore-mapping_property_bag) preenchida com os dados de saída e as propriedades produzidas pelo serviço.</span><span class="sxs-lookup"><span data-stu-id="661f1-146">After the service has recognized the text, [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) returns with a [**MAPPING\_PROPERTY\_BAG**](/windows/desktop/api/Elscore/ns-elscore-mapping_property_bag) structure populated with output data and properties produced by the service.</span></span> <span data-ttu-id="661f1-147">Para evitar vazamentos de memória, o aplicativo deve liberar o recipiente de propriedades chamando [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) para cada vez que o [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="661f1-147">To avoid memory leaks, the application must free the property bag by calling [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) for each time that the [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) returns S\_OK.</span></span> <span data-ttu-id="661f1-148">Normalmente, o aplicativo faz isso quando termina de usar os dados de saída ou quando os dados de saída não são mais relevantes porque a região de entrada do texto foi modificada, por exemplo, editada ou excluída.</span><span class="sxs-lookup"><span data-stu-id="661f1-148">Usually the application does this either when it finishes using the output data or when the output data is no longer relevant because the input region of text has been modified, for example, edited or deleted.</span></span> <span data-ttu-id="661f1-149">Quando o recipiente de propriedades é liberado, **MappingFreePropertyBag** retorna.</span><span class="sxs-lookup"><span data-stu-id="661f1-149">When the property bag is released, **MappingFreePropertyBag** returns.</span></span>

<span data-ttu-id="661f1-150">Instruções de programação para reconhecimento de texto são fornecidas na [solicitação de reconhecimento de texto](requesting-text-recognition.md).</span><span class="sxs-lookup"><span data-stu-id="661f1-150">Programming instructions for text recognition are provided in [Requesting Text Recognition](requesting-text-recognition.md).</span></span>

### <a name="service-termination"></a><span data-ttu-id="661f1-151">Término do serviço</span><span class="sxs-lookup"><span data-stu-id="661f1-151">Service Termination</span></span>

<span data-ttu-id="661f1-152">Quando o aplicativo não exigir mais serviços ELS, ele chamará [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) antes de ser encerrado.</span><span class="sxs-lookup"><span data-stu-id="661f1-152">When your application no longer requires ELS services, it calls [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) before it terminates.</span></span> <span data-ttu-id="661f1-153">Para obter mais informações, consulte [enumerando e liberando serviços](enumerating-and-freeing-services.md).</span><span class="sxs-lookup"><span data-stu-id="661f1-153">For more information, see [Enumerating and Freeing Services](enumerating-and-freeing-services.md).</span></span>

### <a name="versioning"></a><span data-ttu-id="661f1-154">Controle de versão</span><span class="sxs-lookup"><span data-stu-id="661f1-154">Versioning</span></span>

<span data-ttu-id="661f1-155">As versões futuras do ELS permitirão que os serviços do ELS sejam atualizados.</span><span class="sxs-lookup"><span data-stu-id="661f1-155">Future versions of ELS will allow the ELS services to be updated.</span></span> <span data-ttu-id="661f1-156">O aplicativo poderá verificar os números de versão da estrutura de [**informações do \_ serviço \_ de mapeamento**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) para detectar quaisquer alterações nos serviços.</span><span class="sxs-lookup"><span data-stu-id="661f1-156">The application will be able to check the version numbers of the [**MAPPING\_SERVICE\_INFO**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) structure to detect any changes in the services.</span></span>

> [!Note]  
> <span data-ttu-id="661f1-157">Seu aplicativo ELS não deve fazer a suposição de que diferentes versões do mesmo serviço possam recuperar exatamente os mesmos resultados.</span><span class="sxs-lookup"><span data-stu-id="661f1-157">Your ELS application should not make the assumption that different versions of the same service can retrieve exactly the same results.</span></span>

 

 

 



