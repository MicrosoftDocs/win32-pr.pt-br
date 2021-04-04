---
title: Acessando o cache de propriedades com interfaces IADsproperty
description: As interfaces IADsproperty consistem em IADsPropertyList, IADsPropertyEntry e IADsPropertyValue.
ms.assetid: ff15eb50-01ab-4b45-bcfd-1df01172f274
ms.tgt_platform: multiple
keywords:
- Acessando o cache de propriedades diretamente com o ADSI de interfaces IADsproperty
- ADSI do cache de propriedades
- ADSI do cache de propriedades, usando as interfaces IADsproperty para acessar o cache de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b48cd8675f4c439e3d3597e2d4fa59dac57e0896
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/04/2019
ms.locfileid: "103916901"
---
# <a name="accessing-property-cache-with-iadsproperty-interfaces"></a><span data-ttu-id="87bb2-106">Acessando o cache de propriedades com interfaces IADsproperty</span><span class="sxs-lookup"><span data-stu-id="87bb2-106">Accessing Property Cache with IADsProperty Interfaces</span></span>

<span data-ttu-id="87bb2-107">As interfaces [**iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) consistem em [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)e [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue).</span><span class="sxs-lookup"><span data-stu-id="87bb2-107">The [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) interfaces consist of [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry), and [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue).</span></span> <span data-ttu-id="87bb2-108">Essas interfaces fornecem métodos para acessar e manipular diretamente as propriedades de um cache de objeto.</span><span class="sxs-lookup"><span data-stu-id="87bb2-108">These interfaces provide methods to directly access and manipulate the properties of an object cache.</span></span> <span data-ttu-id="87bb2-109">Uma propriedade é conhecida como uma entrada de propriedade e corresponde a um atributo definido no esquema.</span><span class="sxs-lookup"><span data-stu-id="87bb2-109">A property is known as a property entry and corresponds to an attribute defined in the schema.</span></span> <span data-ttu-id="87bb2-110">Uma entrada de propriedade pode ter um ou muitos valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="87bb2-110">A property entry can have one, or many, property values.</span></span> <span data-ttu-id="87bb2-111">Um conjunto de entradas de propriedade é organizado como uma lista de propriedades.</span><span class="sxs-lookup"><span data-stu-id="87bb2-111">A set of property entries are organized as a property list.</span></span>

<span data-ttu-id="87bb2-112">A interface [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) gerencia a lista de propriedades de um objeto ADSI.</span><span class="sxs-lookup"><span data-stu-id="87bb2-112">The [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) interface manages the property list of an ADSI object.</span></span> <span data-ttu-id="87bb2-113">A interface [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) executa essa operação para uma entrada de propriedade.</span><span class="sxs-lookup"><span data-stu-id="87bb2-113">The [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) interface performs this operation for a property entry.</span></span> <span data-ttu-id="87bb2-114">Da mesma forma, a interface [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) representa um ou mais valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="87bb2-114">Similarly, the [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) interface represents one, or more, property values.</span></span> <span data-ttu-id="87bb2-115">Juntos, eles fornecem um mecanismo para os usuários:</span><span class="sxs-lookup"><span data-stu-id="87bb2-115">Together, they provide a mechanism for users to:</span></span>

-   <span data-ttu-id="87bb2-116">Trabalhe diretamente com o cache de propriedades.</span><span class="sxs-lookup"><span data-stu-id="87bb2-116">Work directly with the property cache.</span></span>
-   <span data-ttu-id="87bb2-117">Trabalhe com diretórios que não contêm esquemas, como um servidor LDAP versão 2.</span><span class="sxs-lookup"><span data-stu-id="87bb2-117">Work with directories that do not contain schemas, such as an LDAP version 2 server.</span></span>

<span data-ttu-id="87bb2-118">As interfaces [**iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) \* operam estritamente no cache de propriedades e não fazem nenhuma tentativa de cooperar com o servidor para recuperar ou modificar os dados no repositório persistente.</span><span class="sxs-lookup"><span data-stu-id="87bb2-118">The [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)\* interfaces operate strictly on the property cache and do not make any attempt to cooperate with the server to retrieve or modify the data in the persistent store.</span></span> <span data-ttu-id="87bb2-119">Dessa forma, essas interfaces são usadas apenas para examinar e manipular as propriedades no cache do cliente.</span><span class="sxs-lookup"><span data-stu-id="87bb2-119">As such, these interfaces are used only to examine and manipulate properties in the client cache.</span></span> <span data-ttu-id="87bb2-120">Antes de usar essas interfaces, você deve chamar o método [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) ou o método [**IADs:: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) explicitamente para carregar as propriedades do objeto no cache, se o cache não tiver sido inicializado.</span><span class="sxs-lookup"><span data-stu-id="87bb2-120">Before using these interfaces, you must call the [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method or the [**IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method explicitly to load the object properties into the cache, if the cache has not been initialized.</span></span> <span data-ttu-id="87bb2-121">Depois de chamar os métodos dessas interfaces, você deve chamar [**IADs:: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) para persistir as alterações no repositório de diretórios subjacente.</span><span class="sxs-lookup"><span data-stu-id="87bb2-121">After calling the methods of these interfaces, you must call [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) to persist the changes to the underlying directory store.</span></span>

<span data-ttu-id="87bb2-122">Para obter mais informações e um exemplo de código que pode ser usado para implementar essas interfaces, consulte [código de exemplo para usar interfaces iadsproperty para acessar o cache de propriedades](example-code-for-using-iadsproperty-interfaces-to-access-the-property-cache.md).</span><span class="sxs-lookup"><span data-stu-id="87bb2-122">For more information and a code example that can used to implement these interfaces, see [Example Code for Using IADsProperty Interfaces to Access the Property Cache](example-code-for-using-iadsproperty-interfaces-to-access-the-property-cache.md).</span></span>

 

 




