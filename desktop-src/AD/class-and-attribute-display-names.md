---
title: Nomes de exibição de classe e atributo
description: Este tópico contém informações e diretrizes para nomes de exibição de classe e atributo.
ms.assetid: c85905b2-ed8b-4032-8c54-fd4de8b34ecf
ms.tgt_platform: multiple
keywords:
- exibir nomes de exibição de AD, classe e atributo de especificadores de exibição
- ANÚNCIOS de nomes de exibição de classe
- nome de exibição do atributo AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d65cd6ac6fc3077ff0d2bba15ffa9904b147654
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453953"
---
# <a name="class-and-attribute-display-names"></a><span data-ttu-id="2e643-106">Nomes de exibição de classe e atributo</span><span class="sxs-lookup"><span data-stu-id="2e643-106">Class and Attribute Display Names</span></span>

<span data-ttu-id="2e643-107">O especificador de exibição para uma classe de objeto contém os seguintes atributos que podem ser usados para especificar os nomes de exibição localizados usados na interface do usuário para objetos dessa classe:</span><span class="sxs-lookup"><span data-stu-id="2e643-107">The display specifier for an object class contains the following attributes that can be used to specify the localized display names used in the UI for objects of that class:</span></span>

-   <span data-ttu-id="2e643-108">O atributo **classDisplayName** é uma cadeia de caracteres Unicode de valor único que especifica o nome de exibição da classe.</span><span class="sxs-lookup"><span data-stu-id="2e643-108">The **classDisplayName** attribute is a single-value Unicode string that specifies the class display name.</span></span>
-   <span data-ttu-id="2e643-109">O atributo **attributeDisplayNames** é uma propriedade com vários valores que especifica os nomes a serem usados na interface do usuário para os atributos da classe de objeto.</span><span class="sxs-lookup"><span data-stu-id="2e643-109">The **attributeDisplayNames** attribute is a multi-value property that specifies the names to use in the UI for attributes of the object class.</span></span>

<span data-ttu-id="2e643-110">Os valores de **attributeDisplayNames** são cadeias de caracteres Unicode; cada elemento consiste em um par de nomes delimitados por vírgula:</span><span class="sxs-lookup"><span data-stu-id="2e643-110">The **attributeDisplayNames** values are Unicode strings; each element consists of a comma-delimited name pair:</span></span>


```C++
<attribute name>,<display text>
```



<span data-ttu-id="2e643-111">Neste exemplo, " &lt; nome do atributo &gt; " é o **lDAPDisplayName** do atributo e " &lt; texto de exibição &gt; " é o texto a ser exibido como o nome desse atributo na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="2e643-111">In this example, "&lt;attribute name&gt;" is the **lDAPDisplayName** of the attribute and "&lt;display text&gt;" is the text to display as the name of that attribute in the user interface.</span></span>

## <a name="guidelines-for-class-and-attribute-display-names"></a><span data-ttu-id="2e643-112">Diretrizes para nomes de exibição de classe e atributo</span><span class="sxs-lookup"><span data-stu-id="2e643-112">Guidelines for Class and Attribute Display Names</span></span>

<span data-ttu-id="2e643-113">Como muitos fornecedores podem estender classes com novos atributos ou criar classes totalmente novas, é importante que os nomes de exibição de classe e atributo sejam inequívocas e não resultem em conflitos.</span><span class="sxs-lookup"><span data-stu-id="2e643-113">Because many vendors may extend classes with new attributes or creating entirely new classes, it is important that the class and attribute display names are unambiguous and do not result in conflicts.</span></span>

<span data-ttu-id="2e643-114">Cada fornecedor deve prefixar o nome de exibição da classe com um identificador amigável exclusivo com base no nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="2e643-114">Each vendor should prefix the class display name with a unique friendly identifier based on the vendor name.</span></span> <span data-ttu-id="2e643-115">Por exemplo, se a empresa fictícia, a Fabrikam Inc., criar uma nova classe derivada da classe "Contact", ela poderá ter um nome de exibição de classe exclusivo "fabrikam Contact".</span><span class="sxs-lookup"><span data-stu-id="2e643-115">For example, if the fictitious company, Fabrikam Inc., creates a new class derived from the "contact" class, they can have a unique class display name "Fabrikam Contact."</span></span>

<span data-ttu-id="2e643-116">Se um fornecedor estende uma classe existente com novos atributos, ele deve novamente identificar exclusivamente o nome de exibição do atributo para que nenhum conflito ocorra com outros nomes de exibição de atributo.</span><span class="sxs-lookup"><span data-stu-id="2e643-116">If a vendor extends an existing class with new attributes, they should again uniquely identify the attribute display name so that no conflicts occur with other attribute display names.</span></span> <span data-ttu-id="2e643-117">Novamente, a prefixação do nome de exibição do atributo com identificador amigável exclusivo com base no nome do fornecedor é uma prática recomendada.</span><span class="sxs-lookup"><span data-stu-id="2e643-117">Again, prefixing the attribute display name with unique friendly identifier based on the vendor name is good practice.</span></span> <span data-ttu-id="2e643-118">Por exemplo, se a empresa Fabrikam estende a classe user com um novo atributo HR, ela poderia exibir exclusivamente o atributo como "informações da Fabrikam HR".</span><span class="sxs-lookup"><span data-stu-id="2e643-118">For example, if the Fabrikam company extends the user class with a new HR attribute, they could uniquely display the attribute as "Fabrikam HR Information."</span></span>

<span data-ttu-id="2e643-119">Além disso, de uma perspectiva de localização, cada fornecedor deve localizar os nomes de exibição de classe e atributo em cada idioma com suporte no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="2e643-119">In addition, from a localization perspective, each vendor should localize the class and attribute display names into each language supported by Windows 2000.</span></span>

## <a name="adding-a-value-to-the-attributedisplaynames-attribute"></a><span data-ttu-id="2e643-120">Adicionando um valor ao atributo attributeDisplayNames</span><span class="sxs-lookup"><span data-stu-id="2e643-120">Adding a Value to the attributeDisplayNames Attribute</span></span>

<span data-ttu-id="2e643-121">\*\*Para adicionar um valor de mapeamento de nome ao atributo \*\*attributeDisplayNames\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2e643-121">**To add a name mapping value to the **attributeDisplayNames** attribute**</span></span>

1.  <span data-ttu-id="2e643-122">Determine se o valor de mapeamento de nome para o atributo existe.</span><span class="sxs-lookup"><span data-stu-id="2e643-122">Determine if the name mapping value for the attribute exists.</span></span> <span data-ttu-id="2e643-123">Se um valor de mapeamento de nome for substituído, primeiro exclua o valor existente, usando o método [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) , com o parâmetro *lnControlCode* definido **como \_ Propriedade ADS \_ delete** e o parâmetro *vProp* definido como o valor a ser removido.</span><span class="sxs-lookup"><span data-stu-id="2e643-123">If a name mapping value is to be replaced, first deleted the existing value, using the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method, with the *lnControlCode* parameter set to **ADS\_PROPERTY\_DELETE** and the *vProp* parameter set to the value to be removed.</span></span> <span data-ttu-id="2e643-124">Não use a **\_ Propriedade ADS \_ Clear** ou **a \_ \_ atualização da propriedade ADS** para *lnControlCode*.</span><span class="sxs-lookup"><span data-stu-id="2e643-124">Do not use **ADS\_PROPERTY\_CLEAR** or **ADS\_PROPERTY\_UPDATE** for *lnControlCode*.</span></span>
2.  <span data-ttu-id="2e643-125">Crie a cadeia de caracteres que representa o nome de exibição do atributo.</span><span class="sxs-lookup"><span data-stu-id="2e643-125">Create the string that represents the attribute display name.</span></span> <span data-ttu-id="2e643-126">Para obter um exemplo, consulte o formato acima.</span><span class="sxs-lookup"><span data-stu-id="2e643-126">For an example, see the format above.</span></span>
3.  <span data-ttu-id="2e643-127">Use o método [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) com o parâmetro *lnControlCode* definido como **Propriedade do ADS \_ \_ Append** para adicionar o novo valor.</span><span class="sxs-lookup"><span data-stu-id="2e643-127">Use the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method with the *lnControlCode* parameter set to **ADS\_PROPERTY\_APPEND** to add the new value.</span></span>
4.  <span data-ttu-id="2e643-128">Chame [**IADs:: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para confirmar as alterações no diretório.</span><span class="sxs-lookup"><span data-stu-id="2e643-128">Call [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the changes to the directory.</span></span>

<span data-ttu-id="2e643-129">Para obter mais informações sobre como nomear novas classes e atributos, consulte [nomenclatura de atributos e classes](naming-attributes-and-classes.md).</span><span class="sxs-lookup"><span data-stu-id="2e643-129">For more information about naming new classes and attributes, see [Naming Attributes and Classes](naming-attributes-and-classes.md).</span></span>

 

 