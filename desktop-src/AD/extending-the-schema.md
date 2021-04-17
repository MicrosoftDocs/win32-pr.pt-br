---
title: Estendendo o esquema
description: O esquema do serviço de diretório Active Directory define os atributos e as classes usados no Active Directory Domain Services.
ms.assetid: 1c7c1fa7-56d9-4b2d-9c48-aa10464064bc
ms.tgt_platform: multiple
keywords:
- Active Directory, usando, esquema, estendendo o esquema
- esquema de AD, estendendo o esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90c03d57468fb5275c55ce0d725a2decd7cfbf0f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "105762807"
---
# <a name="extending-the-schema"></a><span data-ttu-id="93b44-105">Estendendo o esquema</span><span class="sxs-lookup"><span data-stu-id="93b44-105">Extending the Schema</span></span>

<span data-ttu-id="93b44-106">O esquema do serviço de diretório Active Directory define os atributos e as classes usados no Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="93b44-106">The Active Directory directory service schema defines the attributes and classes used in Active Directory Domain Services.</span></span> <span data-ttu-id="93b44-107">O esquema base incluído no sistema contém um conjunto avançado de definições de classe, como **User**, **Computer** e **OrganizationalUnit**, e definições de atributo, como **userPrincipalName**, **telephoneNumber** e **objectSid**.</span><span class="sxs-lookup"><span data-stu-id="93b44-107">The base schema that is included the system contains a rich set of class definitions, such as **user**, **computer**, and **organizationalUnit**, and attribute definitions, such as **userPrincipalName**, **telephoneNumber**, and **objectSid**.</span></span> <span data-ttu-id="93b44-108">O conjunto existente de classes e atributos será suficiente para a maioria dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="93b44-108">The existing set of classes and attributes will be sufficient for most applications.</span></span> <span data-ttu-id="93b44-109">No entanto, o esquema é extensível, o que significa que você pode definir novas classes e atributos.</span><span class="sxs-lookup"><span data-stu-id="93b44-109">However, the schema is extensible, which means that you can define new classes and attributes.</span></span> <span data-ttu-id="93b44-110">Esta seção discute como estender o esquema de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="93b44-110">This section discusses how to extend the Active Directory schema.</span></span>

## <a name="when-to-extend-the-schema"></a><span data-ttu-id="93b44-111">Quando estender o esquema</span><span class="sxs-lookup"><span data-stu-id="93b44-111">When to Extend the Schema</span></span>

<span data-ttu-id="93b44-112">Se as classes e os atributos existentes não couberem com o tipo de dados que você deseja armazenar, você deverá estender o esquema.</span><span class="sxs-lookup"><span data-stu-id="93b44-112">If the existing classes and attributes do not fit with the type of data you want to store, you should extend the schema.</span></span> <span data-ttu-id="93b44-113">É importante observar que as adições de esquema são permanentes; Você pode desabilitar classes e atributos, mas nunca pode removê-los do esquema.</span><span class="sxs-lookup"><span data-stu-id="93b44-113">It is important to note that schema additions are permanent; you can disable classes and attributes, but you can never remove them from the schema.</span></span> <span data-ttu-id="93b44-114">Tenha isso em mente ao testar o código.</span><span class="sxs-lookup"><span data-stu-id="93b44-114">Keep this in mind when you are testing code.</span></span>

<span data-ttu-id="93b44-115">Considere também o tamanho dos dados que você deseja armazenar.</span><span class="sxs-lookup"><span data-stu-id="93b44-115">Also consider the size of the data that you want to store.</span></span> <span data-ttu-id="93b44-116">A Microsoft recomenda que nenhum valor de atributo exceda 500 quilobytes, incluindo a soma de atributos com valores de multivalor.</span><span class="sxs-lookup"><span data-stu-id="93b44-116">Microsoft recommends that no attribute value exceed 500 kilobytes, including the sum of multivalued attributes.</span></span> <span data-ttu-id="93b44-117">Além disso, os objetos não devem exceder 1 megabyte de tamanho.</span><span class="sxs-lookup"><span data-stu-id="93b44-117">Also, objects should not exceed 1 megabyte in size.</span></span> <span data-ttu-id="93b44-118">Considere também o número de instâncias dos dados; Se você adicionar um novo atributo à classe de [**usuário**](/windows/desktop/ADSchema/c-user) em um sistema que tenha 100.000 usuários, isso poderá usar um espaço considerável.</span><span class="sxs-lookup"><span data-stu-id="93b44-118">Consider also the number of instances of the data; if you add a new attribute to the [**User**](/windows/desktop/ADSchema/c-user) class on a system that has 100,000 users, this can use up considerable space.</span></span>

<span data-ttu-id="93b44-119">Os tópicos desta seção incluem:</span><span class="sxs-lookup"><span data-stu-id="93b44-119">Topics in this section include:</span></span>

-   <span data-ttu-id="93b44-120">Como associar ao contêiner de esquema e ler as propriedades de classes e atributos existentes.</span><span class="sxs-lookup"><span data-stu-id="93b44-120">How to bind to the schema container and read the properties of existing classes and attributes.</span></span>
-   <span data-ttu-id="93b44-121">Como e quando estender o esquema definindo novos atributos e classes.</span><span class="sxs-lookup"><span data-stu-id="93b44-121">How and when to extend the schema by defining new attributes and classes.</span></span>
-   <span data-ttu-id="93b44-122">Como instalar extensões de esquema usando LDIFDE, CSVDE ou programaticamente com ADSI.</span><span class="sxs-lookup"><span data-stu-id="93b44-122">How to install schema extensions using LDIFDE, CSVDE, or programmatically with ADSI.</span></span>

<span data-ttu-id="93b44-123">Para obter mais informações e uma visão geral do esquema de Active Directory, incluindo informações sobre a implementação do esquema, definições de classe e definições de atributo, consulte [Active Directory esquema](active-directory-schema.md).</span><span class="sxs-lookup"><span data-stu-id="93b44-123">For more information and an overview of the Active Directory schema, including information about the schema implementation, class definitions, and attribute definitions, see [Active Directory Schema](active-directory-schema.md).</span></span>

<span data-ttu-id="93b44-124">Para obter mais informações, incluindo páginas de referência para as classes de esquema predefinidas, atributos e sintaxes de atributo, consulte a referência de esquema de Active Directory na [referência de Active Directory Domain Services](active-directory-domain-services-reference.md).</span><span class="sxs-lookup"><span data-stu-id="93b44-124">For more information, including reference pages for the predefined schema classes, attributes, and attribute syntaxes, see the Active Directory Schema Reference in the [Active Directory Domain Services Reference](active-directory-domain-services-reference.md).</span></span>

 

 