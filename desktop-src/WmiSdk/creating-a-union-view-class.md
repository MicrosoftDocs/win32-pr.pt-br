---
description: Uma classe de exibição Union é uma união lógica de instâncias de classe de origem. Uma classe de exibição Union inclui todas as instâncias das classes de origem, a menos que você limite as instâncias, incluindo uma cláusula WHERE na consulta de origem.
ms.assetid: 54a9804d-644d-4ab6-a3d5-c9c4f7761967
ms.tgt_platform: multiple
title: Criando uma classe de exibição Union
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2ff9327645828c3db78a82811831f058cc27f202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791517"
---
# <a name="creating-a-union-view-class"></a><span data-ttu-id="163df-104">Criando uma classe de exibição Union</span><span class="sxs-lookup"><span data-stu-id="163df-104">Creating a Union View Class</span></span>

<span data-ttu-id="163df-105">Uma classe de exibição Union é uma união lógica de instâncias de classe de origem.</span><span class="sxs-lookup"><span data-stu-id="163df-105">A union view class is a logical union of source class instances.</span></span> <span data-ttu-id="163df-106">Uma classe de exibição Union inclui todas as instâncias das classes de origem, a menos que você limite as instâncias, incluindo uma cláusula WHERE na consulta de origem.</span><span class="sxs-lookup"><span data-stu-id="163df-106">A union view class includes all the instances of the source classes unless you limit the instances by including a WHERE clause on the source query.</span></span>

<span data-ttu-id="163df-107">As classes de exibição de União são úteis quando você deseja ver instâncias de classes semelhantes ou idênticas que estão localizadas em namespaces diferentes ou em computadores diferentes.</span><span class="sxs-lookup"><span data-stu-id="163df-107">Union view classes are useful when you want to see instances of similar or identical classes that are located in different namespaces or on different computers.</span></span> <span data-ttu-id="163df-108">Por exemplo, você pode criar uma classe Union que contém instâncias de unidades de disco diferentes para monitorar.</span><span class="sxs-lookup"><span data-stu-id="163df-108">For example, you can create a union class that contains instances of different disk drives to monitor.</span></span>

<span data-ttu-id="163df-109">Você também pode basear as propriedades de uma classe de exibição Union em propriedades que não estão presentes em todas as instâncias de classe de origem.</span><span class="sxs-lookup"><span data-stu-id="163df-109">You can also base the properties of a union view class on properties not present in all of the source class instances.</span></span> <span data-ttu-id="163df-110">Se as instâncias da classe de origem não tiverem a mesma propriedade, as propriedades das instâncias da classe Union terão um valor de **NULL**.</span><span class="sxs-lookup"><span data-stu-id="163df-110">If the source class instances do not have the same property, the properties of union class instances have a value of **NULL**.</span></span> <span data-ttu-id="163df-111">Por exemplo, se uma unidade de disco rígido tiver uma propriedade de **temperatura** , mas outra não, você ainda poderá criar uma União entre as duas.</span><span class="sxs-lookup"><span data-stu-id="163df-111">For example, if one hard disk drive has a **temperature** property but another does not, you can still create a union between the two.</span></span>

<span data-ttu-id="163df-112">O procedimento a seguir descreve como criar uma classe de exibição Union.</span><span class="sxs-lookup"><span data-stu-id="163df-112">The following procedure describes how to create a union view class.</span></span>

<span data-ttu-id="163df-113">**Para criar uma classe de exibição Union**</span><span class="sxs-lookup"><span data-stu-id="163df-113">**To create a union view class**</span></span>

1.  <span data-ttu-id="163df-114">Comece sua definição de classe com o qualificador de cadeia de caracteres [**Union**](qualifiers-specific-to-the-view-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="163df-114">Begin your class definition with the [**Union**](qualifiers-specific-to-the-view-provider.md) string qualifier.</span></span>

    <span data-ttu-id="163df-115">Os qualificadores [**junção**](qualifiers-specific-to-the-view-provider.md), **Associação** e **União** são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="163df-115">The [**JoinOn**](qualifiers-specific-to-the-view-provider.md), **Association**, and **Union** qualifiers are mutually exclusive.</span></span>

2.  <span data-ttu-id="163df-116">Crie as consultas que definem as classes de origem usadas na classe View com o qualificador [**ViewSources**](viewsources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="163df-116">Create the queries that define source classes used in the view class with the [**ViewSources**](viewsources-qualifier.md) qualifier.</span></span>
3.  <span data-ttu-id="163df-117">Defina os nomes e o local dos namespaces nos quais as classes de origem estão localizadas com o qualificador [**ViewSpaces**](viewspaces-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="163df-117">Define the names and location of the namespaces in which the source classes are located with the [**ViewSpaces**](viewspaces-qualifier.md) qualifier.</span></span>
4.  <span data-ttu-id="163df-118">Defina as propriedades que são mapeadas para as propriedades nas classes de origem com o qualificador [**PropertySources**](propertysources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="163df-118">Define the properties that map to the properties in the source classes with the [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="163df-119">Se necessário, você pode marcar qualquer uma das propriedades como pertencente a uma classe de origem usando o qualificador [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="163df-119">If necessary, you can tag any of the properties as belonging to a source class by using the [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) qualifier.</span></span>

5.  <span data-ttu-id="163df-120">Defina as propriedades de chave das classes de origem da classe de exibição Union.</span><span class="sxs-lookup"><span data-stu-id="163df-120">Define the key properties of the source classes of your union view class.</span></span>

    <span data-ttu-id="163df-121">Cada classe de origem deve ter o mesmo número de propriedades de chave correspondidas por [**CIMType**](swbemproperty-cimtype.md).</span><span class="sxs-lookup"><span data-stu-id="163df-121">Each source class must have the same number of key properties matched by [**CIMType**](swbemproperty-cimtype.md).</span></span> <span data-ttu-id="163df-122">Além disso, as chaves da sua classe de exibição Union devem identificar exclusivamente todas as instâncias de origem.</span><span class="sxs-lookup"><span data-stu-id="163df-122">Also, the keys of your union view class must uniquely identify all source instances.</span></span> <span data-ttu-id="163df-123">Em alguns casos, talvez seja necessário especificar as propriedades do sistema para garantir que as instâncias sejam exclusivas.</span><span class="sxs-lookup"><span data-stu-id="163df-123">In some cases, you might need to specify system properties to ensure that instances are unique.</span></span> <span data-ttu-id="163df-124">Por exemplo, se você criar uma exibição da União de duas classes idênticas em dois namespaces diferentes, você poderá incluir a propriedade [**\_ \_ namespace**](--namespace.md) como uma chave na classe de exibição para diferenciar entre as duas instâncias.</span><span class="sxs-lookup"><span data-stu-id="163df-124">For example, if you create a view from the union of two identical classes in two different namespaces, you could include the [**\_\_Namespace**](--namespace.md) property as a key in the view class to differentiate between the two instances.</span></span> <span data-ttu-id="163df-125">Se você usar duas classes semelhantes do mesmo namespace para criar uma exibição, poderá usar a propriedade **\_ \_ Class** para distinguir entre as duas.</span><span class="sxs-lookup"><span data-stu-id="163df-125">If you use two similar classes from the same namespace to create a view, you could use the **\_\_Class** property to distinguish between the two.</span></span> <span data-ttu-id="163df-126">Renomeie as propriedades do sistema na exibição para que você possa evitar um conflito com as propriedades do sistema da classe View.</span><span class="sxs-lookup"><span data-stu-id="163df-126">Rename any system properties in the view so you can avoid a conflict with the system properties of the view class.</span></span>

6.  <span data-ttu-id="163df-127">Defina os métodos desejados usando o qualificador [**MethodName**](qualifiers-specific-to-the-view-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="163df-127">Define any methods you want using the [**MethodSource**](qualifiers-specific-to-the-view-provider.md) qualifier.</span></span>

    <span data-ttu-id="163df-128">Ao contrário de outras classes de exibição, você pode criar métodos para modificar uma exibição de União.</span><span class="sxs-lookup"><span data-stu-id="163df-128">Unlike other view classes, you can create methods to modify a union view.</span></span>

<span data-ttu-id="163df-129">O exemplo de código a seguir descreve uma classe de exibição Union.</span><span class="sxs-lookup"><span data-stu-id="163df-129">The following code example describes a union view class.</span></span>

``` syntax
[Union, ViewSources{"SELECT Description, DeviceID, __Namespace, FileSystem, FreeSpace, VolumeName FROM LocalDisk", 
    "SELECT Description, DeviceID, __Namespace, FileSystem, FreeSpace, VolumeName FROM RemoteDisk"}, 
    ViewSpaces{"\\\\.\\Root\\LocalNamespace","\\\\.\\Root\\RemoteNamespace"}, 
    dynamic: ToInstance, provider("MS_VIEW_INSTANCE_PROVIDER")]

class UnionOfDrives

{
    [PropertySources{"Description", "Description"}] string des;
    [PropertySources{"DeviceID", "DeviceID"}, key] String did;
    [PropertySources{"__Namespace", "__Namespace"}, key] String KEYID;
    [PropertySources{"FileSystem", "FileSystem"}] String fsystem ;
    [PropertySources{"FreeSpace", "FreeSpace"}] uint64 fspace;
    [PropertySources{"VolumeName", "VolumeName"}] String vname;
};
```

 

 



