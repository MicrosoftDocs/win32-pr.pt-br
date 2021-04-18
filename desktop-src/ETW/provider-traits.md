---
description: As características do provedor são um método para anexar mais dados a um registro de provedor individual.
ms.assetid: 97755D64-BF57-4C0D-8ED4-040FC375C4AF
title: Características do provedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c67b25857070edb6419be9a2898d2667f3a179d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968111"
---
# <a name="provider-traits"></a><span data-ttu-id="da876-103">Características do provedor</span><span class="sxs-lookup"><span data-stu-id="da876-103">Provider Traits</span></span>

<span data-ttu-id="da876-104">As características do provedor são um método para anexar mais dados a um registro de provedor individual.</span><span class="sxs-lookup"><span data-stu-id="da876-104">Provider Traits are a method of attaching more data to an individual provider registration.</span></span> <span data-ttu-id="da876-105">Eles podem ser usados para provedores baseados em manifesto ou TraceLogging.</span><span class="sxs-lookup"><span data-stu-id="da876-105">They can be used for manifest-based or TraceLogging providers.</span></span> <span data-ttu-id="da876-106">Atualmente, isso inclui suporte para adicionar um nome de provedor e/ou grupo de provedores a um registro de provedor individual.</span><span class="sxs-lookup"><span data-stu-id="da876-106">This currently includes support for adding a Provider Name and/or Provider Group to an individual provider registration.</span></span> <span data-ttu-id="da876-107">É provável que mais tipos de características sejam adicionados no futuro.</span><span class="sxs-lookup"><span data-stu-id="da876-107">More trait types are likely to be added in the future.</span></span> <span data-ttu-id="da876-108">Essas informações são armazenadas no kernel como um blob binário de um formato definido.</span><span class="sxs-lookup"><span data-stu-id="da876-108">This information is stored in the kernel as a binary blob of a set format.</span></span>

<span data-ttu-id="da876-109">As características só podem ser definidas uma vez para um registro.</span><span class="sxs-lookup"><span data-stu-id="da876-109">Traits can only be set once for a registration.</span></span> <span data-ttu-id="da876-110">Qualquer tentativa adicional de definir as características desse registro falhará.</span><span class="sxs-lookup"><span data-stu-id="da876-110">Any further attempts to set the traits on that registration will fail.</span></span>

<span data-ttu-id="da876-111">Para definir as características do provedor em um provedor baseado em manifesto, chame a função [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) com a classe de informações EventProviderSetTraits.</span><span class="sxs-lookup"><span data-stu-id="da876-111">To set Provider Traits on a manifest-based provider, call the [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) function with the EventProviderSetTraits information class.</span></span> <span data-ttu-id="da876-112">O buffer EventInformation deve conter um blob binário do seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="da876-112">The EventInformation buffer should contain a binary blob of the following format:</span></span>

``` syntax
{
   UINT16 TraitsSize   // Total size of the traits including this field
   CHAR[] ProviderName // Null terminated utf-8 provider name
   TRAIT[] Traits      // Zero or more individual traits
}
```

<span data-ttu-id="da876-113">As características individuais devem estar no seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="da876-113">Individual traits should be in the following format:</span></span>

``` syntax
TRAIT {
      UINT16 TraitSize // Size of this individual trait including this field
      UINT8 Type       // ETW_PROVIDER_TRAIT_TYPE
      BYTE[] Data
      }
```

<span data-ttu-id="da876-114">Da característica individual, o tipo de característica do provedor de ETW \_ \_ \_ é definido como:</span><span class="sxs-lookup"><span data-stu-id="da876-114">From the individual trait, ETW\_PROVIDER\_TRAIT\_TYPE is defined as:</span></span>

``` syntax
typedef enum {
    EtwProviderTraitTypeGroup = 1,
    EtwProviderTraitTypeMax
} ETW_PROVIDER_TRAIT_TYPE;
```

<span data-ttu-id="da876-115">Os provedores de TraceLogging definem automaticamente as características do provedor quando a função [**TraceLoggingRegister**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) é chamada.</span><span class="sxs-lookup"><span data-stu-id="da876-115">TraceLogging providers automatically set the Provider Traits when the [**TraceLoggingRegister**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) function is called.</span></span> <span data-ttu-id="da876-116">O nome do provedor TraceLogging sempre será incluído em suas características.</span><span class="sxs-lookup"><span data-stu-id="da876-116">The TraceLogging provider's name will always be included in its traits.</span></span> <span data-ttu-id="da876-117">Um grupo pode ser definido em um provedor TraceLogging usando a macro [**TraceLoggingOptionGroup**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup) na definição do provedor.</span><span class="sxs-lookup"><span data-stu-id="da876-117">A group can be set on a TraceLogging provider using the [**TraceLoggingOptionGroup**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup) macro in the provider definition.</span></span>

## <a name="custom-traits"></a><span data-ttu-id="da876-118">Características personalizadas</span><span class="sxs-lookup"><span data-stu-id="da876-118">Custom Traits</span></span>

<span data-ttu-id="da876-119">Embora a maioria dos 255 tipos de característica possíveis ainda não esteja definida, os tipos de característica 1-127 são reservados para definição pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="da876-119">Although most of the 255 possible trait types are not yet defined, trait types 1-127 are reserved for definition by Microsoft.</span></span> <span data-ttu-id="da876-120">Os valores de tipo mais indexados restantes podem ser usados por desenvolvedores externos como se comportarem.</span><span class="sxs-lookup"><span data-stu-id="da876-120">The remaining higher indexed type values can be used by external developers as they see fit.</span></span> <span data-ttu-id="da876-121">Qualquer pessoa que considere adicionar suas próprias características personalizadas ao provedor deve tentar manter seu tamanho total de características abaixo de 256 bytes pelos seguintes motivos:</span><span class="sxs-lookup"><span data-stu-id="da876-121">Anyone considering adding their own custom traits to their provider should try to keep their total trait size under 256 bytes for the following reasons:</span></span>

-   <span data-ttu-id="da876-122">As características são incluídas em todos os eventos escritos para o provedor.</span><span class="sxs-lookup"><span data-stu-id="da876-122">The traits are included in every event written for the provider.</span></span> <span data-ttu-id="da876-123">As características grandes podem levar a arquivos de log muito grandes.</span><span class="sxs-lookup"><span data-stu-id="da876-123">Large traits could lead to very large log files.</span></span>
-   <span data-ttu-id="da876-124">As características são armazenadas no pool de kernel não paginável durante o tempo de vida do provedor.</span><span class="sxs-lookup"><span data-stu-id="da876-124">The traits are stored in nonpaged kernel pool for the lifetime of the provider.</span></span>

## <a name="provider-groups"></a><span data-ttu-id="da876-125">Grupos de provedores</span><span class="sxs-lookup"><span data-stu-id="da876-125">Provider Groups</span></span>

<span data-ttu-id="da876-126">Um grupo de provedores é uma entidade controlável definida pelo GUID muito parecida com um provedor em si.</span><span class="sxs-lookup"><span data-stu-id="da876-126">A provider group is a GUID-defined controllable entity much like a provider itself.</span></span> <span data-ttu-id="da876-127">A principal diferença é que, embora um GUID de provedor seja usado para controlar os registros de apenas seu provedor, um grupo controlará todos os seus registros de membros.</span><span class="sxs-lookup"><span data-stu-id="da876-127">The key difference is that while a provider GUID is used to control registrations of just its provider, a group will control all of its member registrations.</span></span> <span data-ttu-id="da876-128">Por exemplo, habilitar um grupo de provedores com uma determinada palavra-chave e nível habilitará todos os registros de membro de grupos com essa palavra-chave e nível.</span><span class="sxs-lookup"><span data-stu-id="da876-128">For example, enabling a provider group with a given keyword and level will enable all of the groups member registrations with that keyword and level.</span></span>

<span data-ttu-id="da876-129">A associação de grupo pode ser restrita por permissões.</span><span class="sxs-lookup"><span data-stu-id="da876-129">Group membership may be restricted by permissions.</span></span> <span data-ttu-id="da876-130">Se o chamador de [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) não tiver permissões para ingressar no grupo especificado, a associação será negada.</span><span class="sxs-lookup"><span data-stu-id="da876-130">If the caller of [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) doesn't have permissions to join the specified group, then membership will be denied.</span></span>

<span data-ttu-id="da876-131">Em alguns casos, o controlador de sessão de rastreamento pode querer excluir alguns provedores da sua habilitação de um grupo.</span><span class="sxs-lookup"><span data-stu-id="da876-131">In some cases the trace session controller may want to exclude a few providers from its enable of a group.</span></span> <span data-ttu-id="da876-132">Isso pode ser feito definindo uma lista de não permitir.</span><span class="sxs-lookup"><span data-stu-id="da876-132">This can be done by setting a disallow list.</span></span> <span data-ttu-id="da876-133">Uma lista de não permitir é uma lista de GUIDs de provedor que não será habilitada com base nas configurações de grupo para uma única sessão de log.</span><span class="sxs-lookup"><span data-stu-id="da876-133">A disallow list is a list of provider GUIDs that will not be enabled based on the group settings for a single logging session.</span></span> <span data-ttu-id="da876-134">Não permitir que as listas possam ser alteradas dinamicamente com [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) e a classe de informações TraceSetDisallowList.</span><span class="sxs-lookup"><span data-stu-id="da876-134">Disallow lists can be changed dynamically with [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) and the TraceSetDisallowList information class.</span></span>

<span data-ttu-id="da876-135">Embora a maioria das ações de habilitação possa ser feita para grupos de provedores de maneira semelhante a provedores individuais, há algumas exceções.</span><span class="sxs-lookup"><span data-stu-id="da876-135">While most enable actions can be done for Provider Groups in a similar manner to individual providers, there are some exceptions.</span></span> <span data-ttu-id="da876-136">As exceções incluem:</span><span class="sxs-lookup"><span data-stu-id="da876-136">Exceptions include:</span></span>

-   <span data-ttu-id="da876-137">Os grupos de provedores não podem ser controlados por sessões de rastreamento particulares.</span><span class="sxs-lookup"><span data-stu-id="da876-137">Provider Groups cannot be controlled by private trace sessions.</span></span>
-   <span data-ttu-id="da876-138">O nome do evento, a ID do evento e os filtros de carga não são aplicáveis aos grupos de provedor, pois eles assumem informações específicas de um provedor individual.</span><span class="sxs-lookup"><span data-stu-id="da876-138">Event Name, Event ID, and Payload filters are not applicable to Provider Groups as they assume specific information of an individual provider.</span></span>

 

 
