---
description: Um qualificador é uma cadeia de caracteres de dados que fornece mais informações sobre uma classe, instância, propriedade, método ou parâmetro.
ms.assetid: 6984b575-b365-49dd-aeab-a763430f434c
ms.tgt_platform: multiple
title: Adicionando um qualificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5a6f18f2b79bcd25b2b4ca75811157c9091e6eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105794591"
---
# <a name="adding-a-qualifier"></a><span data-ttu-id="04ee1-103">Adicionando um qualificador</span><span class="sxs-lookup"><span data-stu-id="04ee1-103">Adding a Qualifier</span></span>

<span data-ttu-id="04ee1-104">Um qualificador é uma cadeia de caracteres de dados que fornece mais informações sobre uma classe, instância, propriedade, método ou parâmetro.</span><span class="sxs-lookup"><span data-stu-id="04ee1-104">A qualifier is a data string that provides more information about a class, instance, property, method, or parameter.</span></span>

<span data-ttu-id="04ee1-105">A definição de classe a seguir é um exemplo de uma classe derivada que tem qualificadores de classe.</span><span class="sxs-lookup"><span data-stu-id="04ee1-105">The following class definition is an example of a derived class that has class qualifiers.</span></span>

``` syntax
[Dynamic, Provider ("ProviderX")] 
class MyDerivedClass : MyClass
{
    [key] string sKey;
    [Implemented] sint32 ValueMethod();
    [Implemented] sint32 MyMethod ([in, Id(0)] sint32 Param);
};
```

<span data-ttu-id="04ee1-106">Os qualificadores podem ser divididos em qualificadores padrão, qualificadores CIM e qualificadores exclusivos incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="04ee1-106">Qualifiers can be divided into standard qualifiers, CIM qualifiers, and unique qualifiers include the following:</span></span>

-   <span data-ttu-id="04ee1-107">Qualificador padrão</span><span class="sxs-lookup"><span data-stu-id="04ee1-107">Standard qualifier</span></span>

    <span data-ttu-id="04ee1-108">Um qualificador padrão é um qualificador definido pelo WMI e comumente usado no código MOF.</span><span class="sxs-lookup"><span data-stu-id="04ee1-108">A standard qualifier is a qualifier defined by WMI and commonly used in MOF code.</span></span> <span data-ttu-id="04ee1-109">Por exemplo, os qualificadores [**dinâmico**](dynamic-qualifier.md) e de [**leitura**](standard-qualifiers.md) são qualificadores padrão.</span><span class="sxs-lookup"><span data-stu-id="04ee1-109">For example, the [**Dynamic**](dynamic-qualifier.md) and [**Read**](standard-qualifiers.md) qualifiers are both standard qualifiers.</span></span> <span data-ttu-id="04ee1-110">Para obter mais informações, consulte [qualificadores WMI](wmi-qualifiers.md).</span><span class="sxs-lookup"><span data-stu-id="04ee1-110">For more information, see [WMI Qualifiers](wmi-qualifiers.md).</span></span>

-   <span data-ttu-id="04ee1-111">Qualificador CIM</span><span class="sxs-lookup"><span data-stu-id="04ee1-111">CIM qualifier</span></span>

    <span data-ttu-id="04ee1-112">Um qualificador CIM é um qualificador incluído na especificação CIM.</span><span class="sxs-lookup"><span data-stu-id="04ee1-112">A CIM qualifier is a qualifier included in the CIM specification.</span></span> <span data-ttu-id="04ee1-113">Ao usar qualificadores CIM no código MOF, os qualificadores padrão são projetados especificamente com o WMI em mente.</span><span class="sxs-lookup"><span data-stu-id="04ee1-113">While use CIM qualifiers in MOF code, the standard qualifiers are designed specifically with WMI in mind.</span></span> <span data-ttu-id="04ee1-114">Para obter mais informações, consulte a [especificação CIM](https://www.dmtf.org/spec/cims.html/)do DMTF.</span><span class="sxs-lookup"><span data-stu-id="04ee1-114">For more information, see the DMTF [CIM Specification](https://www.dmtf.org/spec/cims.html/).</span></span>

-   <span data-ttu-id="04ee1-115">Qualificador exclusivo</span><span class="sxs-lookup"><span data-stu-id="04ee1-115">Unique qualifier</span></span>

    <span data-ttu-id="04ee1-116">Um qualificador exclusivo é um qualificador definido especificamente para uma nova classe por um provedor de classe.</span><span class="sxs-lookup"><span data-stu-id="04ee1-116">A unique qualifier is a qualifier defined specifically for a new class by a class provider.</span></span> <span data-ttu-id="04ee1-117">Por exemplo, o qualificador de [**unidades**](standard-qualifiers.md) é um qualificador não padrão específico do provedor.</span><span class="sxs-lookup"><span data-stu-id="04ee1-117">For example, the [**Units**](standard-qualifiers.md) qualifier is a nonstandard, provider-specific qualifier.</span></span> <span data-ttu-id="04ee1-118">Você pode criar seus próprios qualificadores para uso com seu provedor.</span><span class="sxs-lookup"><span data-stu-id="04ee1-118">You can create your own qualifiers for use with your provider.</span></span> <span data-ttu-id="04ee1-119">Para obter mais informações sobre como criar um provedor, consulte [desenvolvendo um provedor WMI](developing-a-wmi-provider.md).</span><span class="sxs-lookup"><span data-stu-id="04ee1-119">For more information about creating a provider, see [Developing a WMI Provider](developing-a-wmi-provider.md).</span></span>

<span data-ttu-id="04ee1-120">Seja qual for o seu qualificador, o processo principal que você executa é usar o qualificador em seu código MOF.</span><span class="sxs-lookup"><span data-stu-id="04ee1-120">Whatever your qualifier does, the main process you perform is to use the qualifier in your MOF code.</span></span> <span data-ttu-id="04ee1-121">Para obter mais informações, consulte [aplicando um qualificador](applying-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="04ee1-121">For more information, see [Applying a Qualifier](applying-a-qualifier.md).</span></span> <span data-ttu-id="04ee1-122">Você pode descrever ainda mais um qualificador com um tipo de qualificador.</span><span class="sxs-lookup"><span data-stu-id="04ee1-122">You can further describe a qualifier with a qualifier flavor.</span></span> <span data-ttu-id="04ee1-123">Um tipo de qualificador contém mais informações sobre como um provedor deve usar um qualificador.</span><span class="sxs-lookup"><span data-stu-id="04ee1-123">A qualifier flavor contains more information regarding how a provider should use a qualifier.</span></span> <span data-ttu-id="04ee1-124">Para obter mais informações, consulte [descrevendo um qualificador com um tipo de qualificador](describing-a-qualifier-with-a-qualifier-flavor.md).</span><span class="sxs-lookup"><span data-stu-id="04ee1-124">For more information, see [Describing a Qualifier with a Qualifier Flavor](describing-a-qualifier-with-a-qualifier-flavor.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="04ee1-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="04ee1-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04ee1-126">Criando classes formato MOF (MOF)</span><span class="sxs-lookup"><span data-stu-id="04ee1-126">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



