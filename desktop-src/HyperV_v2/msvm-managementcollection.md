---
description: Representa uma coleção de outras coleções.
ms.assetid: 1f7f5517-55d9-44a3-b0ca-444a9d7d5941
title: Classe Msvm_ManagementCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ManagementCollection
- Msvm_ManagementCollection.CollectionID
- Msvm_ManagementCollection.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2d3499bb161495152b6de4b8aebd7c64d041d069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105767636"
---
# <a name="msvm_managementcollection-class"></a><span data-ttu-id="fda51-103">\_Classe Msvm managementcollection</span><span class="sxs-lookup"><span data-stu-id="fda51-103">Msvm\_ManagementCollection class</span></span>

<span data-ttu-id="fda51-104">Representa uma coleção de outras coleções.</span><span class="sxs-lookup"><span data-stu-id="fda51-104">Represents a collection of other collections.</span></span>

<span data-ttu-id="fda51-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="fda51-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fda51-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fda51-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ManagementCollection : CIM_CollectionOfMSEs
{
  string CollectionID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="fda51-107">Membros</span><span class="sxs-lookup"><span data-stu-id="fda51-107">Members</span></span>

<span data-ttu-id="fda51-108">A classe **Msvm \_ managementcollection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fda51-108">The **Msvm\_ManagementCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="fda51-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fda51-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fda51-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fda51-110">Properties</span></span>

<span data-ttu-id="fda51-111">A classe **Msvm \_ managementcollection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fda51-111">The **Msvm\_ManagementCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fda51-112">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="fda51-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda51-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fda51-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fda51-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fda51-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fda51-115">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionId"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="fda51-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="fda51-116">A identificação exclusiva do objeto de coleção.</span><span class="sxs-lookup"><span data-stu-id="fda51-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="fda51-117">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="fda51-117">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fda51-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fda51-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fda51-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fda51-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fda51-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="fda51-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="fda51-121">Um nome definido pelo usuário para a coleção.</span><span class="sxs-lookup"><span data-stu-id="fda51-121">An user-defined name for the collection.</span></span> <span data-ttu-id="fda51-122">Observe que isso não é garantido como exclusivo.</span><span class="sxs-lookup"><span data-stu-id="fda51-122">Note this is not guaranteed to be unique.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fda51-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fda51-123">Requirements</span></span>



| <span data-ttu-id="fda51-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fda51-124">Requirement</span></span> | <span data-ttu-id="fda51-125">Valor</span><span class="sxs-lookup"><span data-stu-id="fda51-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fda51-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fda51-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fda51-127">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="fda51-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="fda51-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fda51-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fda51-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fda51-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="fda51-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="fda51-130">Namespace</span></span><br/>                | <span data-ttu-id="fda51-131">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="fda51-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fda51-132">MOF</span><span class="sxs-lookup"><span data-stu-id="fda51-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fda51-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fda51-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fda51-134">DLL</span><span class="sxs-lookup"><span data-stu-id="fda51-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fda51-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fda51-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fda51-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="fda51-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fda51-137">**CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="fda51-137">**CIM\_CollectionOfMSEs**</span></span>](cim-collectionofmses.md)
</dt> </dl>

 

