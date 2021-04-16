---
description: Cada propriedade em uma classe de exibição deve ter um qualificador de matriz de cadeia de caracteres chamado PropertySources.
ms.assetid: df89680b-8ea7-4f38-81ba-c4132b944f37
ms.tgt_platform: multiple
title: Qualificador PropertySources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertySources
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3809977282a2bdf82d0b51ef8f566541b74fe28a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765126"
---
# <a name="propertysources-qualifier"></a><span data-ttu-id="60600-103">Qualificador PropertySources</span><span class="sxs-lookup"><span data-stu-id="60600-103">PropertySources Qualifier</span></span>

<span data-ttu-id="60600-104">Cada propriedade em uma classe de exibição deve ter um qualificador de matriz de cadeia de caracteres chamado **PropertySources**.</span><span class="sxs-lookup"><span data-stu-id="60600-104">Every property in a view class must have a string array qualifier called **PropertySources**.</span></span> <span data-ttu-id="60600-105">O qualificador **PropertySources** contém o nome da propriedade de classe de origem ou propriedades das quais essa propriedade de classe de exibição obtém dados.</span><span class="sxs-lookup"><span data-stu-id="60600-105">The **PropertySources** qualifier contains the name of the source class property or properties from which this view class property gets data.</span></span> <span data-ttu-id="60600-106">A ordem dos valores nessa matriz corresponde à ordem das classes de origem definidas para o [qualificador ViewSources](viewsources-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="60600-106">The order of the values in this array correspond to the order of the source classes defined for the [ViewSources qualifier](viewsources-qualifier.md).</span></span> <span data-ttu-id="60600-107">O exemplo a seguir mostra como definir uma propriedade para uma classe de exibição Union que é a União da classe do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) de dois computadores diferentes:</span><span class="sxs-lookup"><span data-stu-id="60600-107">The following example shows how to define a property for a union view class that is the union of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class from two different computers:</span></span>


```mof
[PropertySources{"DeviceID", "DeviceID"},key] String Devname;
```



<span data-ttu-id="60600-108">A primeira propriedade **DeviceID** corresponde à propriedade **DeviceID** da classe na primeira consulta de origem.</span><span class="sxs-lookup"><span data-stu-id="60600-108">The first **DeviceID** property corresponds to the **DeviceID** property from the class in the first source query.</span></span> <span data-ttu-id="60600-109">A segunda propriedade **DeviceID** é a propriedade **DeviceID** da classe na segunda consulta de origem.</span><span class="sxs-lookup"><span data-stu-id="60600-109">The second **DeviceID** property is the **DeviceID** property from the class in the second source query.</span></span>

<span data-ttu-id="60600-110">Ao definir propriedades para classes de exibição de junção, você deve definir uma propriedade de exibição separada para cada uma das propriedades de classe de origem, a menos que as propriedades de classe de origem sejam a base da classe de exibição de junção.</span><span class="sxs-lookup"><span data-stu-id="60600-110">When defining properties for join view classes, you must define a separate view property for each of the source class properties unless the source class properties are the basis of the join view class.</span></span> <span data-ttu-id="60600-111">O exemplo a seguir cria propriedades em uma classe de exibição de junção em propriedades semelhantes da classe de origem da [**\_ impressora Win32**](/windows/desktop/CIMWin32Prov/win32-printer) e da classe de origem [**Win32 \_ PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) :</span><span class="sxs-lookup"><span data-stu-id="60600-111">The following example creates properties in a join view class on similar properties from the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) source class and the [**Win32\_PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) source class:</span></span>


```mof
[PropertySources{"VerticalResolution", ""}] Uint32 Vres;
[PropertySources{"", "YResolution"}] Uint32 Yres;
```



<span data-ttu-id="60600-112">Se as duas classes de origem estiverem sendo Unidas por uma propriedade comum, você só poderá definir uma única propriedade de classe de exibição porque o valor de ambas as propriedades da classe de origem é sempre o mesmo.</span><span class="sxs-lookup"><span data-stu-id="60600-112">If the two source classes are being joined by a common property, you can only define a single view class property because the value of both source class properties is always the same.</span></span> <span data-ttu-id="60600-113">O exemplo a seguir mostra como unir a classe de [**\_ impressora do Win32**](/windows/desktop/CIMWin32Prov/win32-printer) e o [**\_ PrinterConfiguration do Win32**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) por um valor de propriedade comum:</span><span class="sxs-lookup"><span data-stu-id="60600-113">The following example shows how to join the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class and the [**Win32\_PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) by a common property value:</span></span>


```mof
[PropertySources{"DeviceId", "DeviceName "}] String Name;
```



## <a name="requirements"></a><span data-ttu-id="60600-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60600-114">Requirements</span></span>



| <span data-ttu-id="60600-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="60600-115">Requirement</span></span> | <span data-ttu-id="60600-116">Valor</span><span class="sxs-lookup"><span data-stu-id="60600-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="60600-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60600-117">Minimum supported client</span></span><br/> | <span data-ttu-id="60600-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60600-118">Windows Vista</span></span><br/>       |
| <span data-ttu-id="60600-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60600-119">Minimum supported server</span></span><br/> | <span data-ttu-id="60600-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60600-120">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="60600-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="60600-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60600-122">**Qualificadores específicos para o provedor de exibição**</span><span class="sxs-lookup"><span data-stu-id="60600-122">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

