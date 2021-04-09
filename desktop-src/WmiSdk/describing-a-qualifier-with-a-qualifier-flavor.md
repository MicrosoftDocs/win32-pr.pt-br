---
description: Um tipo de qualificador é um sinalizador que descreve mais informações sobre um qualificador.
ms.assetid: a7d9d1c0-9386-4c90-9788-993b35ed12db
ms.tgt_platform: multiple
title: Descrevendo um qualificador com um tipo de qualificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525cfc2c590ec8916e2e9538b3e8224e97b3b5dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165332"
---
# <a name="describing-a-qualifier-with-a-qualifier-flavor"></a><span data-ttu-id="af6a7-103">Descrevendo um qualificador com um tipo de qualificador</span><span class="sxs-lookup"><span data-stu-id="af6a7-103">Describing a Qualifier with a Qualifier Flavor</span></span>

<span data-ttu-id="af6a7-104">Um [*tipo de qualificador*](gloss-q.md) é um sinalizador que descreve mais informações sobre um qualificador.</span><span class="sxs-lookup"><span data-stu-id="af6a7-104">A [*qualifier flavor*](gloss-q.md) is a flag that describes more information about a qualifier.</span></span> <span data-ttu-id="af6a7-105">Por exemplo, o tipo de qualificador restrito informa que o WMI não deve propagar o qualificador associado para quaisquer classes ou instâncias derivadas.</span><span class="sxs-lookup"><span data-stu-id="af6a7-105">For example, the Restricted qualifier flavor states that WMI should not propagate the associated qualifier to any derived classes or instances.</span></span> <span data-ttu-id="af6a7-106">Você pode definir tipos usando o código MOF ou programaticamente.</span><span class="sxs-lookup"><span data-stu-id="af6a7-106">You can set flavors using either MOF code or programmatically.</span></span> <span data-ttu-id="af6a7-107">Embora você possa descrever uma variedade de efeitos com versões, as principais finalidades dos sinalizadores de tipo é definir como o WMI propaga qualificadores por meio de herança.</span><span class="sxs-lookup"><span data-stu-id="af6a7-107">While you can describe a variety of effects with flavors, the main purposes of flavor flags is to define how WMI propagates qualifiers through inheritance.</span></span>

<span data-ttu-id="af6a7-108">O WMI define vários tipos de qualificador que você pode anexar a qualquer qualificador, independentemente da origem do qualificador.</span><span class="sxs-lookup"><span data-stu-id="af6a7-108">WMI defines several qualifier flavors that you can attach to any qualifier, regardless of the origin of the qualifier.</span></span> <span data-ttu-id="af6a7-109">No entanto, algumas versões não são apropriadas para todos os tipos de qualificador.</span><span class="sxs-lookup"><span data-stu-id="af6a7-109">However, some flavors are not appropriate for all qualifier types.</span></span> <span data-ttu-id="af6a7-110">O tipo **ToSubClass** , por exemplo, é apropriado apenas para qualificadores definidos para uma classe.</span><span class="sxs-lookup"><span data-stu-id="af6a7-110">The **ToSubClass** flavor, for example, is appropriate only for qualifiers defined for a class.</span></span> <span data-ttu-id="af6a7-111">Não é possível anexar **ToSubClass** a um qualificador usado para descrever uma instância.</span><span class="sxs-lookup"><span data-stu-id="af6a7-111">You cannot attach **ToSubClass** to a qualifier used to describe an instance.</span></span>

<span data-ttu-id="af6a7-112">Você pode usar tipos para descrever uma variedade de efeitos diferentes para qualificadores.</span><span class="sxs-lookup"><span data-stu-id="af6a7-112">You can use flavors to describe a variety of different effects for qualifiers.</span></span> <span data-ttu-id="af6a7-113">Por exemplo, flavor pode indicar se um qualificador pode ser localizado.</span><span class="sxs-lookup"><span data-stu-id="af6a7-113">For example, flavor can indicate if a qualifier can be localized.</span></span> <span data-ttu-id="af6a7-114">No entanto, uma das principais finalidades de um tipo de qualificador é descrever se uma classe pai pode passar qualificadores para uma subclasse ou instância de classe.</span><span class="sxs-lookup"><span data-stu-id="af6a7-114">However, one of the main purposes of a qualifier flavor is to describe whether a parent class can pass qualifiers to a subclass or class instance.</span></span> <span data-ttu-id="af6a7-115">Você também pode usar tipos para determinar se uma propriedade de classe passa um qualificador para uma propriedade de instância.</span><span class="sxs-lookup"><span data-stu-id="af6a7-115">You can also use flavors to determine if a class property passes a qualifier on to an instance property.</span></span> <span data-ttu-id="af6a7-116">Por fim, use os tipos para indicar se uma subclasse pode substituir o valor original de um qualificador herdado.</span><span class="sxs-lookup"><span data-stu-id="af6a7-116">Finally, use flavors to state whether a subclass can override the original value of an inherited qualifier.</span></span> <span data-ttu-id="af6a7-117">No entanto, os qualificadores que você declara para uma classe ou instância não se propagam para as propriedades dessa classe ou instância.</span><span class="sxs-lookup"><span data-stu-id="af6a7-117">However, qualifiers that you declare for a class or instance do not propagate to the properties of that class or instance.</span></span> <span data-ttu-id="af6a7-118">Além disso, os tipos que estabelecem permissões de substituição serão válidos somente se você também definir os tipos **ToInstance** ou **ToSubClass** .</span><span class="sxs-lookup"><span data-stu-id="af6a7-118">Further, flavors that establish override permissions are valid only if you also set the **ToInstance** or **ToSubClass** flavors.</span></span>

<span data-ttu-id="af6a7-119">Um tipo pode ser atribuído globalmente a um qualificador para um arquivo MOF inteiro usando a sintaxe a seguir, na qual o espaço em branco atua como o delimitador quando vários tipos são especificados.</span><span class="sxs-lookup"><span data-stu-id="af6a7-119">A flavor can be globally assigned to a qualifier for an entire MOF file using the following syntax in which white space acts as the delimiter when multiple flavors are specified.</span></span>

``` syntax
Qualifier QualifierName : flavor1 <flavor2...>;
```

<span data-ttu-id="af6a7-120">Os tipos globais se aplicam a todos os usos subsequentes do qualificador no arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="af6a7-120">Global flavors apply to all subsequent uses of the qualifier in the MOF file.</span></span> <span data-ttu-id="af6a7-121">As instruções de tipo global podem ocorrer em qualquer lugar no arquivo fora de um bloco de declaração de objeto.</span><span class="sxs-lookup"><span data-stu-id="af6a7-121">Global flavor statements may occur anywhere in the file outside of an object declaration block.</span></span> <span data-ttu-id="af6a7-122">Os tipos redefinidos no nível de classe, instância ou propriedade substituem as declarações de tipo global para o escopo desse objeto.</span><span class="sxs-lookup"><span data-stu-id="af6a7-122">Flavors redefined at the class, instance, or property level override the global flavor declarations for the scope of that object.</span></span>

<span data-ttu-id="af6a7-123">Não é possível definir um novo tipo.</span><span class="sxs-lookup"><span data-stu-id="af6a7-123">You cannot define a new flavor.</span></span> <span data-ttu-id="af6a7-124">Embora você possa criar um novo qualificador, use somente os [tipos de qualificador](qualifier-flavors.md) existentes para descrever o novo qualificador.</span><span class="sxs-lookup"><span data-stu-id="af6a7-124">Although you can create a new qualifier, use only existing [Qualifier Flavors](qualifier-flavors.md) to describe your new qualifier.</span></span>

<span data-ttu-id="af6a7-125">**Para definir os tipos de qualificador no MOF**</span><span class="sxs-lookup"><span data-stu-id="af6a7-125">**To define qualifier flavors in MOF**</span></span>

-   <span data-ttu-id="af6a7-126">Declare os tipos que descrevem um determinado qualificador após o nome do qualificador, entre os colchetes do qualificador.</span><span class="sxs-lookup"><span data-stu-id="af6a7-126">Declare the flavors that describe a given qualifier after the qualifier name, between the qualifier brackets.</span></span> <span data-ttu-id="af6a7-127">Use o espaço em branco como o delimitador entre vários tipos.</span><span class="sxs-lookup"><span data-stu-id="af6a7-127">Use white space as the delimiter between multiple flavors.</span></span>

    <span data-ttu-id="af6a7-128">O exemplo a seguir mostra o padrão para anexar qualificadores predefinidos.</span><span class="sxs-lookup"><span data-stu-id="af6a7-128">The following example shows the pattern for attaching predefined qualifiers.</span></span>

    ``` syntax
    [qualifier1 : flavor1 flavor2 flavor3, qualifier2 : flavor1]
    ```

<span data-ttu-id="af6a7-129">Você pode adicionar o qualificador tipos programaticamente apenas em C++.</span><span class="sxs-lookup"><span data-stu-id="af6a7-129">You can add qualifier flavors programmatically only in C++.</span></span> <span data-ttu-id="af6a7-130">Essa operação não está disponível na [API de script para WMI](scripting-api-for-wmi.md), embora você possa adicionar um novo qualificador chamando [**SWbemQualifierSet. Add**](swbemqualifierset-add.md).</span><span class="sxs-lookup"><span data-stu-id="af6a7-130">This operation is not available in the [Scripting API for WMI](scripting-api-for-wmi.md), although you can add a new qualifier by calling [**SWbemQualifierSet.Add**](swbemqualifierset-add.md).</span></span>

<span data-ttu-id="af6a7-131">**Para atribuir um tipo usando C++**</span><span class="sxs-lookup"><span data-stu-id="af6a7-131">**To assign a flavor using C++**</span></span>

-   <span data-ttu-id="af6a7-132">Chame o método [**IWbemQualifierSet::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) com o parâmetro *lFlavor* definido como uma das constantes definidas para o método.</span><span class="sxs-lookup"><span data-stu-id="af6a7-132">Call the [**IWbemQualifierSet::Put**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) method with the *lFlavor* parameter set to one of the constants defined for the method.</span></span>

 

 



