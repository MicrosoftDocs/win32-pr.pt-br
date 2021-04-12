---
description: Os serviços de transliteração ELS mapeiam o texto UTF-16 de um sistema de escrita para outro sistema de escrita.
ms.assetid: 32e46c52-5c3c-4e22-8f4e-05286ee213ba
title: Serviços de transliteração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc00b96d56e6b05e70b352c81da0280e9ef35043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091664"
---
# <a name="transliteration-services"></a><span data-ttu-id="092a0-103">Serviços de transliteração</span><span class="sxs-lookup"><span data-stu-id="092a0-103">Transliteration Services</span></span>

<span data-ttu-id="092a0-104">Os serviços de transliteração ELS mapeiam o texto UTF-16 de um sistema de escrita para outro sistema de escrita.</span><span class="sxs-lookup"><span data-stu-id="092a0-104">The ELS transliteration services map UTF-16 text from one writing system to another writing system.</span></span> <span data-ttu-id="092a0-105">Cada serviço é realmente uma aplicação de dados a um conjunto específico de scripts Unicode de entrada e saída, e a transliteração real é interna à plataforma ELS.</span><span class="sxs-lookup"><span data-stu-id="092a0-105">Each service is really data applying to a specific set of input and output Unicode scripts, and the actual transliteration is internal to the ELS platform.</span></span> <span data-ttu-id="092a0-106">O aplicativo pode, opcionalmente, enumerar os serviços disponíveis para scripts de entrada e saída específicos e selecionar o serviço que ele requer.</span><span class="sxs-lookup"><span data-stu-id="092a0-106">The application can optionally enumerate the available services for specific input and output scripts and select the service that it requires.</span></span>

<span data-ttu-id="092a0-107">A plataforma mantém metadados para os serviços de transliteração de ELS.</span><span class="sxs-lookup"><span data-stu-id="092a0-107">The platform maintains metadata for the ELS transliteration services.</span></span> <span data-ttu-id="092a0-108">Os metadados de cada serviço fornecem uma descrição do serviço e lista os scripts de entrada e saída aos quais o serviço dá suporte.</span><span class="sxs-lookup"><span data-stu-id="092a0-108">Metadata for each service provides a description of the service and lists the input and output scripts that the service supports.</span></span> <span data-ttu-id="092a0-109">Os metadados são representados por uma estrutura de [**\_ \_ informações de serviço de mapeamento**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) recuperada pela função [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) .</span><span class="sxs-lookup"><span data-stu-id="092a0-109">The metadata is represented by a [**MAPPING\_SERVICE\_INFO**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) structure retrieved by the [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) function.</span></span>

## <a name="input-to-a-transliteration-service"></a><span data-ttu-id="092a0-110">Entrada para um serviço de transliteração</span><span class="sxs-lookup"><span data-stu-id="092a0-110">Input to a Transliteration Service</span></span>

<span data-ttu-id="092a0-111">A entrada para um serviço de transliteração é o texto UTF-16 em um sistema de escrita.</span><span class="sxs-lookup"><span data-stu-id="092a0-111">The input to a transliteration service is UTF-16 text in one writing system.</span></span>

## <a name="output-of-a-transliteration-service"></a><span data-ttu-id="092a0-112">Saída de um serviço de transliteração</span><span class="sxs-lookup"><span data-stu-id="092a0-112">Output of a Transliteration Service</span></span>

<span data-ttu-id="092a0-113">A saída de um serviço de transliteração é o texto UTF-16 mapeado para um segundo sistema de escrita.</span><span class="sxs-lookup"><span data-stu-id="092a0-113">The output of a transliteration service is UTF-16 text mapped to a second writing system.</span></span> <span data-ttu-id="092a0-114">Se nenhum mapeamento de transliteração apropriado estiver disponível para qualquer parte determinada do texto de entrada, a parte permanecerá inalterada.</span><span class="sxs-lookup"><span data-stu-id="092a0-114">If no appropriate transliteration mapping is available for any given chunk of the input text, the chunk remains unchanged.</span></span>

## <a name="transliteration-service-operation"></a><span data-ttu-id="092a0-115">Operação do serviço de transliteração</span><span class="sxs-lookup"><span data-stu-id="092a0-115">Transliteration Service Operation</span></span>

<span data-ttu-id="092a0-116">Um serviço de transliteração mapeia o texto Unicode de um script de entrada para um script de saída, caractere por caractere ou termo por termo, conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="092a0-116">A transliteration service maps Unicode text from an input script to an output script, character by character or term by term, as appropriate.</span></span> <span data-ttu-id="092a0-117">O aplicativo pode optar por obter o serviço de transliteração específico de interesse especificando scripts de entrada e saída ao chamar [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)ou fornecendo o GUID do serviço.</span><span class="sxs-lookup"><span data-stu-id="092a0-117">The application can choose to obtain the specific transliteration service of interest by specifying input and output scripts when calling [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices), or by providing the service GUID.</span></span> <span data-ttu-id="092a0-118">Outra opção para o aplicativo é enumerar todos os serviços de transliteração disponíveis especificando a categoria de serviço "transliteração" ao chamar **MappingGetServices**.</span><span class="sxs-lookup"><span data-stu-id="092a0-118">Another option for the application is to enumerate all available transliteration services by specifying the service category "Transliteration" when calling **MappingGetServices**.</span></span> <span data-ttu-id="092a0-119">Nesse caso, o aplicativo chama cada serviço e compara os resultados com o texto original para ver se os resultados foram alterados pela operação de um serviço específico.</span><span class="sxs-lookup"><span data-stu-id="092a0-119">In this case, the application calls each service and compares the results with the original text to see if the results have been changed by the operation of a particular service.</span></span>

<span data-ttu-id="092a0-120">O aplicativo pode solicitar reconhecimento de texto para um serviço de transliteração de ELS com uma chamada para [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext).</span><span class="sxs-lookup"><span data-stu-id="092a0-120">The application can request text recognition for an ELS transliteration service with a call to [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext).</span></span> <span data-ttu-id="092a0-121">Quando ele recebe a solicitação, o serviço de transliteração aloca um buffer para conter os dados transliterados e, em seguida, executa o reconhecimento de texto para cada ponto de código na cadeia de caracteres de entrada fornecida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="092a0-121">When it receives the request, the transliteration service allocates a buffer to contain the transliterated data, and then performs text recognition for each code point in the input string supplied by the application.</span></span>

> [!Note]  
> <span data-ttu-id="092a0-122">O texto original e o texto transliterado podem ter comprimentos diferentes.</span><span class="sxs-lookup"><span data-stu-id="092a0-122">The original text and the transliterated text might have different lengths.</span></span>

 

## <a name="transliteration-service-guids"></a><span data-ttu-id="092a0-123">GUIDs do serviço de transliteração</span><span class="sxs-lookup"><span data-stu-id="092a0-123">Transliteration Service GUIDs</span></span>

<span data-ttu-id="092a0-124">Os GUIDs dos serviços de transliteração são declarados em Elssrvc. h, conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="092a0-124">The GUIDs for the transliteration services are declared in Elssrvc.h, as shown in the following code.</span></span>


```C++
// {A3A8333B-F4FC-42f6-A0C4-0462FE7317CB}
static const GUID ELS_GUID_TRANSLITERATION_HANT_TO_HANS =
    { 0xA3A8333B, 0xF4FC, 0x42f6, { 0xA0, 0xC4, 0x04, 0x62, 0xFE, 0x73, 0x17, 0xCB } };

// {3CACCDC8-5590-42dc-9A7B-B5A6B5B3B63B}
static const GUID ELS_GUID_TRANSLITERATION_HANS_TO_HANT =
    { 0x3CACCDC8, 0x5590, 0x42dc, { 0x9A, 0x7B, 0xB5, 0xA6, 0xB5, 0xB3, 0xB6, 0x3B } };

// {D8B983B1-F8BF-4a2b-BCD5-5B5EA20613E1}
static const GUID ELS_GUID_TRANSLITERATION_MALAYALAM_TO_LATIN =
    { 0xD8B983B1, 0xF8BF, 0x4a2b, { 0xBC, 0xD5, 0x5B, 0x5E, 0xA2, 0x06, 0x13, 0xE1 } };

// {C4A4DCFE-2661-4d02-9835-F48187109803}
static const GUID ELS_GUID_TRANSLITERATION_DEVANAGARI_TO_LATIN =
    { 0xC4A4DCFE, 0x2661, 0x4d02, { 0x98, 0x35, 0xF4, 0x81, 0x87, 0x10, 0x98, 0x03 } };

// {3DD12A98-5AFD-4903-A13F-E17E6C0BFE01}
static const GUID ELS_GUID_TRANSLITERATION_CYRILLIC_TO_LATIN =
    { 0x3DD12A98, 0x5AFD, 0x4903, { 0xA1, 0x3F, 0xE1, 0x7E, 0x6C, 0x0B, 0xFE, 0x01 } };

// {F4DFD825-91A4-489f-855E-9AD9BEE55727}
static const GUID ELS_GUID_TRANSLITERATION_BENGALI_TO_LATIN =
    { 0xF4DFD825, 0x91A4, 0x489f, { 0x85, 0x5E, 0x9A, 0xD9, 0xBE, 0xE5, 0x57, 0x27 } };
```



## <a name="related-topics"></a><span data-ttu-id="092a0-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="092a0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="092a0-126">Sobre os serviços lingüísticos estendidos</span><span class="sxs-lookup"><span data-stu-id="092a0-126">About Extended Linguistic Services</span></span>](about-extended-linguistic-services.md)
</dt> </dl>

 

 



