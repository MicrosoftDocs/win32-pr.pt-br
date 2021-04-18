---
description: Você pode filtrar as instâncias de uma classe de exibição de junção atribuindo uma consulta WQL ao qualificador PostJoinFilter.
ms.assetid: 926a7262-ea6b-4a5a-8aa7-6ec0ae389031
ms.tgt_platform: multiple
title: Qualificador PostJoinFilter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostJoinFilter
api_type:
- NA
api_location: ''
ms.openlocfilehash: ac86aeafefc8057a1612c5007e55e7633c655c59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105786138"
---
# <a name="postjoinfilter-qualifier"></a><span data-ttu-id="b4d57-103">Qualificador PostJoinFilter</span><span class="sxs-lookup"><span data-stu-id="b4d57-103">PostJoinFilter Qualifier</span></span>

<span data-ttu-id="b4d57-104">Você pode filtrar as instâncias de uma classe de exibição de junção atribuindo uma consulta WQL ao qualificador **PostJoinFilter** .</span><span class="sxs-lookup"><span data-stu-id="b4d57-104">You can filter the instances of a join view class by assigning a WQL query to the **PostJoinFilter** qualifier.</span></span> <span data-ttu-id="b4d57-105">O valor da consulta WQL é aplicado às instâncias da classe de exibição de junção.</span><span class="sxs-lookup"><span data-stu-id="b4d57-105">The value of the WQL query is applied to the instances of the join view class.</span></span> <span data-ttu-id="b4d57-106">Você pode usar esse qualificador para restringir as instâncias de sua classe de exibição àquelas que atendem a condições específicas.</span><span class="sxs-lookup"><span data-stu-id="b4d57-106">You can use this qualifier to restrict the instances of your view class to those that meet specific conditions.</span></span> <span data-ttu-id="b4d57-107">A consulta WQL a seguir filtra instâncias de uma classe de junção chamada com base em instâncias do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="b4d57-107">The following WQL query filters instances of a join class called based on instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span>


```C++
PostJoinFilter("SELECT * FROM JoinDrive" +
    " WHERE FreeSpace > 1000000" +
    " and Description = \"3 1/2 Inch Floppy Drive\"")
```



<span data-ttu-id="b4d57-108">Há várias restrições ao uso deste qualificador:</span><span class="sxs-lookup"><span data-stu-id="b4d57-108">There are several restrictions to the use of this qualifier:</span></span>

-   <span data-ttu-id="b4d57-109">**PostJoinFilter** só está disponível para unir classes de exibição.</span><span class="sxs-lookup"><span data-stu-id="b4d57-109">**PostJoinFilter** is only available to join view classes.</span></span>
-   <span data-ttu-id="b4d57-110">O nome da classe e os nomes de propriedade especificados na consulta referem-se às propriedades da classe View, não à classe Source.</span><span class="sxs-lookup"><span data-stu-id="b4d57-110">The class name and property names specified in the query refer to the properties of the view class, not the source class.</span></span>
-   <span data-ttu-id="b4d57-111">Nenhuma exclusão de propriedades é permitida; somente `SELECT *` consultas de tipo são permitidas.</span><span class="sxs-lookup"><span data-stu-id="b4d57-111">No exclusion of properties is permitted; only `SELECT *` type queries are allowed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4d57-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4d57-112">Requirements</span></span>



| <span data-ttu-id="b4d57-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4d57-113">Requirement</span></span> | <span data-ttu-id="b4d57-114">Valor</span><span class="sxs-lookup"><span data-stu-id="b4d57-114">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b4d57-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4d57-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b4d57-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b4d57-116">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b4d57-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4d57-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b4d57-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4d57-118">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b4d57-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4d57-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4d57-120">**Qualificadores específicos para o provedor de exibição**</span><span class="sxs-lookup"><span data-stu-id="b4d57-120">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

