---
title: Lendo o esquema abstrato
description: Este tópico fornece um exemplo de código e diretrizes para leitura do esquema abstrato, que fornece um subconjunto dos dados armazenados nos objetos attributeSchema e classSchema no contêiner de esquema.
ms.assetid: f31fc0ae-048f-413c-9370-96367dc68df8
ms.tgt_platform: multiple
keywords:
- Active Directory de esquema, lendo o esquema abstrato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d7fadba33bcc5e93bf2b9e89934e8b440d559b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103823633"
---
# <a name="reading-the-abstract-schema"></a><span data-ttu-id="88833-104">Lendo o esquema abstrato</span><span class="sxs-lookup"><span data-stu-id="88833-104">Reading the Abstract Schema</span></span>

<span data-ttu-id="88833-105">Este tópico fornece um exemplo de código e diretrizes para leitura do esquema abstrato, que fornece um subconjunto dos dados armazenados nos objetos **attributeSchema** e **classSchema** no contêiner de esquema.</span><span class="sxs-lookup"><span data-stu-id="88833-105">This topic provides a code example and guidelines for reading from the abstract schema, which provides a subset of the data stored in the **attributeSchema** and **classSchema** objects in the schema container.</span></span> <span data-ttu-id="88833-106">Para recuperar dados que não estão disponíveis no esquema abstrato, leia os dados diretamente do contêiner de esquema, conforme descrito em [lendo objetos attributeSchema e classSchema](reading-attributeschema-and-classschema-objects.md).</span><span class="sxs-lookup"><span data-stu-id="88833-106">To retrieve data that is unavailable in the abstract schema, read the data directly from the schema container as described in [Reading attributeSchema and classSchema Objects](reading-attributeschema-and-classschema-objects.md).</span></span>

<span data-ttu-id="88833-107">Use a cadeia de vinculação "LDAP://schema" para associar a um ponteiro [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) no esquema abstrato.</span><span class="sxs-lookup"><span data-stu-id="88833-107">Use the "LDAP://schema" binding string to bind to an [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) pointer on the abstract schema.</span></span> <span data-ttu-id="88833-108">Use esse ponteiro para enumerar as entradas de classe, atributo e sintaxe no esquema abstrato.</span><span class="sxs-lookup"><span data-stu-id="88833-108">Use this pointer to enumerate the class, attribute, and syntax entries in the abstract schema.</span></span> <span data-ttu-id="88833-109">Você também pode usar o método [**IADsContainer. GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) para recuperar entradas individuais.</span><span class="sxs-lookup"><span data-stu-id="88833-109">You can also use the [**IADsContainer.GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) method to retrieve individual entries.</span></span>


```C++
// Bind to the abstract schema.
IADsContainer *pAbsSchema = NULL;
hr = ADsGetObject(L"LDAP://schema",
                  IID_IADsContainer,
                  (void**)&pAbsSchema);
```




```VB
' Bind to the abstract schema.
Dim adschema As IADsContainer
Set adschema = GetObject("LDAP://schema")
```



<span data-ttu-id="88833-110">Use uma cadeia de vinculação semelhante, "LDAP://schema/ <object> ", para associar diretamente a uma classe ou a uma entrada de atributo no esquema abstrato.</span><span class="sxs-lookup"><span data-stu-id="88833-110">Use a similar binding string, "LDAP://schema/<object>", to bind directly to a class or attribute entry in the abstract schema.</span></span> <span data-ttu-id="88833-111">Nessa cadeia de caracteres, " &lt; Object &gt; " é o **lDAPDisplayName** de uma classe ou atributo.</span><span class="sxs-lookup"><span data-stu-id="88833-111">In this string, "&lt;object&gt;" is the **lDAPDisplayName** of a class or attribute.</span></span> <span data-ttu-id="88833-112">Para classes, associe-se à interface [**IADsClass**](/windows/desktop/api/iads/nn-iads-iadsclass) ; para atributos, associe à interface [**iadsproperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) .</span><span class="sxs-lookup"><span data-stu-id="88833-112">For classes bind to the [**IADsClass**](/windows/desktop/api/iads/nn-iads-iadsclass) interface; for attributes, bind to [**IADsProperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) interface.</span></span>


```C++
// Bind to the user class entry in the abstract schema.
IADsClass *pClass;
hr = ADsGetObject(L"LDAP://schema/user",
                  IID_IADsClass,
                  (void**)&pClass);
```




```VB
Bind to the user class entry in the abstract schema.
Dim userclass As IADsClass
Set userclass = GetObject("LDAP://schema/user")
```



<span data-ttu-id="88833-113">Além disso, a interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) fornece a propriedade [**IADs. Schema**](/windows/desktop/ADSI/iads-property-methods) .</span><span class="sxs-lookup"><span data-stu-id="88833-113">In addition, the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface provides the [**IADs.Schema**](/windows/desktop/ADSI/iads-property-methods) property.</span></span> <span data-ttu-id="88833-114">Essa propriedade retorna o ADsPath para a classe de objeto no formato de cadeia de vinculação de esquema abstrato.</span><span class="sxs-lookup"><span data-stu-id="88833-114">This property returns the ADsPath for the object class in abstract schema binding string format.</span></span> <span data-ttu-id="88833-115">Se você tiver um ponteiro **IADs** para um objeto, poderá associar a sua classe no esquema abstrato usando o ADsPath retornado de **IADs. Schema**.</span><span class="sxs-lookup"><span data-stu-id="88833-115">If you have an **IADs** pointer to an object, you can bind to its class in the abstract schema using the ADsPath returned from **IADs.Schema**.</span></span>

<span data-ttu-id="88833-116">Para classes, a tabela a seguir lista as principais propriedades fornecidas pelo esquema abstrato.</span><span class="sxs-lookup"><span data-stu-id="88833-116">For classes, the following table lists key properties provided by the abstract schema.</span></span>



| <span data-ttu-id="88833-117">Propriedade</span><span class="sxs-lookup"><span data-stu-id="88833-117">Property</span></span>                                                             | <span data-ttu-id="88833-118">Significado</span><span class="sxs-lookup"><span data-stu-id="88833-118">Meaning</span></span>                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88833-119">**IADsClass. Abstract**</span><span class="sxs-lookup"><span data-stu-id="88833-119">**IADsClass.Abstract**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)            | <span data-ttu-id="88833-120">Indica se esta é uma classe abstrata.</span><span class="sxs-lookup"><span data-stu-id="88833-120">Indicates whether this is an abstract class.</span></span>                                                                                                                                                                                                                                            |
| [<span data-ttu-id="88833-121">**IADsClass. auxiliar**</span><span class="sxs-lookup"><span data-stu-id="88833-121">**IADsClass.Auxiliary**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)           | <span data-ttu-id="88833-122">Indica se esta é uma classe auxiliar.</span><span class="sxs-lookup"><span data-stu-id="88833-122">Indicates whether this is an auxiliary class.</span></span>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="88833-123">**IADsClass.AuxDerivedFrom**</span><span class="sxs-lookup"><span data-stu-id="88833-123">**IADsClass.AuxDerivedFrom**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)      | <span data-ttu-id="88833-124">Matriz de classes auxiliares da qual essa classe deriva.</span><span class="sxs-lookup"><span data-stu-id="88833-124">Array of auxiliary classes this class derives from.</span></span>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="88833-125">**IADsClass. Container**</span><span class="sxs-lookup"><span data-stu-id="88833-125">**IADsClass.Container**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)           | <span data-ttu-id="88833-126">Indica se os objetos dessa classe podem conter outros objetos, o que será verdadeiro se qualquer classe incluir essa classe em sua lista de **possibleSuperiors**.</span><span class="sxs-lookup"><span data-stu-id="88833-126">Indicates whether objects of this class can contain other objects, which is true if any class includes this class in its list of **possibleSuperiors**.</span></span>                                                                                                                                 |
| [<span data-ttu-id="88833-127">**IADsClass.DerivedFrom**</span><span class="sxs-lookup"><span data-stu-id="88833-127">**IADsClass.DerivedFrom**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)         | <span data-ttu-id="88833-128">Matriz de classes da qual essa classe é derivada.</span><span class="sxs-lookup"><span data-stu-id="88833-128">Array of classes that this class is derived from.</span></span>                                                                                                                                                                                                                                       |
| [<span data-ttu-id="88833-129">**IADsClass. Obrigatórioproperties**</span><span class="sxs-lookup"><span data-stu-id="88833-129">**IADsClass.MandatoryProperties**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods) | <span data-ttu-id="88833-130">Recupera uma matriz das propriedades obrigatórias que devem ser definidas para uma instância da classe.</span><span class="sxs-lookup"><span data-stu-id="88833-130">Retrieves an array of the mandatory properties that must be set for an instance of the class.</span></span> <span data-ttu-id="88833-131">A lista retornada inclui todos os valores **mustContain** e **systemMustContain** para a classe e as classes das quais ele é derivado, incluindo as superclasses e as classes auxiliares.</span><span class="sxs-lookup"><span data-stu-id="88833-131">The returned list includes all the **mustContain** and **systemMustContain** values for the class and the classes from which it is derived, including superclasses and auxiliary classes.</span></span> |
| [<span data-ttu-id="88833-132">**IADsClass. OID**</span><span class="sxs-lookup"><span data-stu-id="88833-132">**IADsClass.OID**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)                 | <span data-ttu-id="88833-133">Recupera o governsID da classe.</span><span class="sxs-lookup"><span data-stu-id="88833-133">Retrieves the governsID of the class.</span></span>                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="88833-134">**IADsClass. OptionalProperties**</span><span class="sxs-lookup"><span data-stu-id="88833-134">**IADsClass.OptionalProperties**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)  | <span data-ttu-id="88833-135">Recupera uma matriz das propriedades opcionais que podem ser definidas para uma instância da classe.</span><span class="sxs-lookup"><span data-stu-id="88833-135">Retrieves an array of the optional properties that might be set for an instance of the class.</span></span> <span data-ttu-id="88833-136">A lista retornada inclui todos os valores **mayContain** e **systemMayContain** para a classe e as classes das quais ele é derivado, incluindo as superclasses e as classes auxiliares.</span><span class="sxs-lookup"><span data-stu-id="88833-136">The returned list includes all the **mayContain** and **systemMayContain** values for the class and the classes from which it is derived, including superclasses and auxiliary classes.</span></span>   |
| [<span data-ttu-id="88833-137">**IADsClass.PossibleSuperiors**</span><span class="sxs-lookup"><span data-stu-id="88833-137">**IADsClass.PossibleSuperiors**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)   | <span data-ttu-id="88833-138">Recupera uma matriz dos valores de **possibleSuperiors** para a classe, que indica as classes de objeto que podem conter objetos dessa classe.</span><span class="sxs-lookup"><span data-stu-id="88833-138">Retrieves an array of the **possibleSuperiors** values for the class, which indicates the object classes that can contain objects of this class.</span></span>                                                                                                                                        |



 

<span data-ttu-id="88833-139">O esquema abstrato é armazenado no objeto de **subesquema** no contêiner de esquema.</span><span class="sxs-lookup"><span data-stu-id="88833-139">The abstract schema is stored in the **subSchema** object in the schema container.</span></span> <span data-ttu-id="88833-140">Para obter o nome distinto do objeto de **subesquema** , associe-o a RootDSE e leia o atributo **subSchemaSubEntry** , conforme descrito em [associação sem servidor e RootDSE](serverless-binding-and-rootdse.md).</span><span class="sxs-lookup"><span data-stu-id="88833-140">To get the distinguished name of the **subSchema** object, bind to rootDSE and read the **subSchemaSubEntry** attribute, as described in [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span> <span data-ttu-id="88833-141">Lembre-se de que é mais eficiente ler o esquema abstrato ligando-se a "LDAP://schema", do que associando diretamente ao objeto de **subesquema** .</span><span class="sxs-lookup"><span data-stu-id="88833-141">Be aware that it is more efficient to read the abstract schema by binding to "LDAP://schema", than by binding directly to the **subSchema** object.</span></span>

 

 