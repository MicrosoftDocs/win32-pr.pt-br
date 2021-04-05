---
description: Todas as classes de exibição devem ter um qualificador de matriz de cadeia de caracteres chamado ViewSources.
ms.assetid: aefa8cda-962f-4f6c-92a0-a8825d48db60
ms.tgt_platform: multiple
title: Qualificador ViewSources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ViewSources
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1f39146f8065401052c352472b28c4946cca6b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662575"
---
# <a name="viewsources-qualifier"></a><span data-ttu-id="3c5cb-103">Qualificador ViewSources</span><span class="sxs-lookup"><span data-stu-id="3c5cb-103">ViewSources Qualifier</span></span>

<span data-ttu-id="3c5cb-104">Todas as classes de exibição devem ter um qualificador de matriz de cadeia de caracteres chamado **ViewSources**.</span><span class="sxs-lookup"><span data-stu-id="3c5cb-104">All view classes must have a string array qualifier called **ViewSources**.</span></span> <span data-ttu-id="3c5cb-105">O qualificador **ViewSources** contém as consultas de origem que definem as instâncias de origem usadas na classe View.</span><span class="sxs-lookup"><span data-stu-id="3c5cb-105">The **ViewSources** qualifier contains the source queries that define the source instances used in the view class.</span></span> <span data-ttu-id="3c5cb-106">O valor do qualificador **ViewSources** é uma matriz de cadeia de caracteres que contém consultas [*linguagem WQL (WQL)*](gloss-w.md) .</span><span class="sxs-lookup"><span data-stu-id="3c5cb-106">The value of the **ViewSources** qualifier is a string array containing [*WMI Query Language (WQL)*](gloss-w.md) queries.</span></span> <span data-ttu-id="3c5cb-107">Você pode definir as classes de origem e restringir as instâncias de origem usadas pela sua classe de exibição com a[cláusula WHERE](where-clause.md) da [consulta com WQL](querying-with-wql.md)para criar uma exibição filtrada.</span><span class="sxs-lookup"><span data-stu-id="3c5cb-107">You can define source classes and restrict the source instances your view class uses with the [Querying with WQL](querying-with-wql.md)[WHERE Clause](where-clause.md) to create a filtered view.</span></span>

<span data-ttu-id="3c5cb-108">O [provedor de exibição](view-provider.md) corresponde às consultas de origem no qualificador **ViewSources** para os namespaces listados no [qualificador ViewSpaces](viewspaces-qualifier.md) na ordem em que as consultas e os namespaces são listados.</span><span class="sxs-lookup"><span data-stu-id="3c5cb-108">The [View Provider](view-provider.md) matches the source queries in the **ViewSources** qualifier to the namespaces listed in the [ViewSpaces qualifier](viewspaces-qualifier.md) in the order the queries and namespaces are listed.</span></span> <span data-ttu-id="3c5cb-109">O número de consultas de origem deve corresponder ao número de namespaces listados no qualificador ViewSpaces.</span><span class="sxs-lookup"><span data-stu-id="3c5cb-109">The number of source queries must match the number of namespaces listed in the ViewSpaces qualifier.</span></span> <span data-ttu-id="3c5cb-110">A ordem na qual você lista as consultas de origem determina os namespaces dos quais as instâncias de origem são desenhadas.</span><span class="sxs-lookup"><span data-stu-id="3c5cb-110">The order in which you list the source queries determines the namespaces from which the source instances are drawn.</span></span>

<span data-ttu-id="3c5cb-111">O exemplo a seguir seleciona apenas as instâncias da classe **LocalDisk** em que o valor da propriedade **FileSystem** é "NTFS" e as instâncias da classe **RemoteDisk** em que o valor da propriedade **FreeSpace** é maior que 45 megabytes:</span><span class="sxs-lookup"><span data-stu-id="3c5cb-111">The following example selects only instances of the **LocalDisk** class where the value of the **FileSystem** property is "NTFS" and instances of the **RemoteDisk** class where the value of the **FreeSpace** property is greater than 45 megabytes:</span></span>


```sql
ViewSources{
"SELECT __Namespace, 
   Description, 
   DeviceID, 
   FileSystem, 
   FreeSpace, 
   VolumeName FROM LocalDisk 
 WHERE FileSystem = \"NTFS\"", 
   "SELECT __Namespace, 
   Description,
   DeviceID, 
   FileSystem, 
   FreeSpace, 
   VolumeName FROM RemoteDisk 
 WHERE FreeSpace > 45000000"}
```



> [!Note]  
> <span data-ttu-id="3c5cb-112">O número de consultas de origem que você pode definir para classes de exibição de junção depende do número de instâncias que essas consultas retornam e de quantas maneiras essas instâncias podem ser Unidas.</span><span class="sxs-lookup"><span data-stu-id="3c5cb-112">The number of source queries you can define for join view classes depends on the number of instances these queries return and how many ways these instances can be joined.</span></span> <span data-ttu-id="3c5cb-113">O número de combinações possíveis de instâncias de origem para classes de exibição aumenta exponencialmente, portanto, mantenha as consultas de origem para as classes de exibição de junção o mais simples possível.</span><span class="sxs-lookup"><span data-stu-id="3c5cb-113">The number of possible combinations of source instances for view classes grows exponentially, so keep source queries for join view classes as simple as possible.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3c5cb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c5cb-114">Requirements</span></span>



| <span data-ttu-id="3c5cb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c5cb-115">Requirement</span></span> | <span data-ttu-id="3c5cb-116">Valor</span><span class="sxs-lookup"><span data-stu-id="3c5cb-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="3c5cb-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c5cb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3c5cb-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c5cb-118">Windows Vista</span></span><br/>       |
| <span data-ttu-id="3c5cb-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c5cb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3c5cb-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c5cb-120">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3c5cb-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c5cb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c5cb-122">**Qualificadores específicos para o provedor de exibição**</span><span class="sxs-lookup"><span data-stu-id="3c5cb-122">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




