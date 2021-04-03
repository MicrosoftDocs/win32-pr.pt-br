---
title: Interfaces de esquema
description: Interfaces de esquema
ms.assetid: b3427202-352b-4b35-877e-d28fb3d3906a
ms.tgt_platform: multiple
keywords:
- ADSI de interfaces de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f414fdea2418fb92a0a3c8c9e8bf88eb6d7f00b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915889"
---
# <a name="schema-interfaces"></a><span data-ttu-id="ba515-104">Interfaces de esquema</span><span class="sxs-lookup"><span data-stu-id="ba515-104">Schema Interfaces</span></span>

<span data-ttu-id="ba515-105">O contêiner de esquema contém um conjunto de definições de esquema que são anexadas a parte da árvore de namespace do provedor.</span><span class="sxs-lookup"><span data-stu-id="ba515-105">The schema container contains a set of schema definitions that are attached to part of the namespace tree of the provider.</span></span> <span data-ttu-id="ba515-106">Normalmente, cada instância de um namespace tem seu próprio esquema.</span><span class="sxs-lookup"><span data-stu-id="ba515-106">Typically, each instance of a namespace has its own schema.</span></span> <span data-ttu-id="ba515-107">Por exemplo, na figura a seguir, o provedor de exemplo ADSI define um contêiner de esquema em cada um dos nós raiz "Seattle" e "Toronto".</span><span class="sxs-lookup"><span data-stu-id="ba515-107">For example, in the following figure, the ADSI example provider defines a schema container in each of the root nodes "Seattle" and "Toronto".</span></span>

![contenção do esquema](images/schemacont.png)

<span data-ttu-id="ba515-109">Para criar uma implementação de ADSI para um provedor, você precisa fornecer objetos de gerenciamento de esquema que reflitam o namespace subjacente do provedor e que dão suporte a interfaces de esquema ADSI.</span><span class="sxs-lookup"><span data-stu-id="ba515-109">To create an ADSI implementation for a provider, you need to supply schema management objects that reflect the underlying namespace of the provider and which support ADSI schema interfaces.</span></span> <span data-ttu-id="ba515-110">A seguir está uma lista das interfaces de esquema ADSI, que estão contidas no contêiner de esquema.</span><span class="sxs-lookup"><span data-stu-id="ba515-110">The following is a list of the ADSI schema interfaces, which are contained in the schema container.</span></span>

-   <span data-ttu-id="ba515-111">[**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) representa classes de serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="ba515-111">[**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) represents directory service classes.</span></span>
-   <span data-ttu-id="ba515-112">[**Iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) representa as propriedades do serviço de diretório que têm um ou vários valores.</span><span class="sxs-lookup"><span data-stu-id="ba515-112">[**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) represents directory service properties that have single or multiple values.</span></span>
-   <span data-ttu-id="ba515-113">[**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) representa o tipo de variante única.</span><span class="sxs-lookup"><span data-stu-id="ba515-113">[**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) represents the single VARIANT type.</span></span>

<span data-ttu-id="ba515-114">As interfaces definidas pelo ADSI podem dar suporte a propriedades e sintaxes específicas para seu provedor.</span><span class="sxs-lookup"><span data-stu-id="ba515-114">Interfaces defined by ADSI can support specific properties and syntaxes for your provider.</span></span> <span data-ttu-id="ba515-115">Os provedores podem optar por estender uma definição de ADSI usando os métodos que criam e acessam Propriedades, por exemplo, você pode usar os métodos da interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) , como [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) e [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex).</span><span class="sxs-lookup"><span data-stu-id="ba515-115">Providers can choose to extend an ADSI definition by using the methods that create and access properties, for example, you can use the methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface such as [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) and [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex).</span></span> <span data-ttu-id="ba515-116">Os provedores também podem dar suporte a propriedades adicionais por meio de interfaces adicionais.</span><span class="sxs-lookup"><span data-stu-id="ba515-116">Providers can also support additional properties through additional interfaces.</span></span> <span data-ttu-id="ba515-117">Para obter uma lista completa de interfaces ADSI, consulte [interfaces ADSI](adsi-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="ba515-117">For a complete list of ADSI interfaces, see [ADSI Interfaces](adsi-interfaces.md).</span></span>

<span data-ttu-id="ba515-118">Um componente de provedor ADSI com um namespace complexo pode permitir que vários esquemas existam em uma instância de namespace, cada um em uma parte diferente da árvore.</span><span class="sxs-lookup"><span data-stu-id="ba515-118">An ADSI provider component with a complex namespace might allow multiple schemas to exist in a namespace instance, each at a different part of the tree.</span></span> <span data-ttu-id="ba515-119">A propriedade [**IADs:: Schema**](iads-property-methods.md) de um objeto, no entanto, sempre nomeia sua própria definição de esquema.</span><span class="sxs-lookup"><span data-stu-id="ba515-119">The [**IADs::Schema**](iads-property-methods.md) property of an object, however, always names its own schema definition.</span></span>

 

 




