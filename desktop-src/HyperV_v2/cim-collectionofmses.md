---
description: Uma classe abstrata para subclasses que representam uma coleção de \_ objetos CIM ManagedSystemElement. Essas coleções permitem que os elementos do sistema gerenciado sejam agrupados para fins de identificação e para simplificar a associação de definições e configurações.
ms.assetid: f47bf1d6-6d89-4d9f-82d1-99a7343481bc
title: Classe CIM_CollectionOfMSEs (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.CollectionID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e467e775c78364718f25cc732d6689d9fb2b9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827891"
---
# <a name="cim_collectionofmses-class-hyper-v-management"></a><span data-ttu-id="bbbf0-104">Classe CIM_CollectionOfMSEs (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="bbbf0-104">CIM_CollectionOfMSEs class (Hyper-V management)</span></span>

<span data-ttu-id="bbbf0-105">Uma classe abstrata para subclasses que representam uma coleção de objetos [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="bbbf0-105">An abstract class for subclasses that represent a collection of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects.</span></span> <span data-ttu-id="bbbf0-106">Essas coleções permitem que os elementos do sistema gerenciado sejam agrupados para fins de identificação e para simplificar a associação de definições e configurações.</span><span class="sxs-lookup"><span data-stu-id="bbbf0-106">These collections allow managed system elements to be grouped for identification purposes and to simplify the association of settings and configurations.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbbf0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbbf0-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_CollectionOfMSEs : CIM_Collection
{
  string CollectionID;
};
```

## <a name="members"></a><span data-ttu-id="bbbf0-108">Membros</span><span class="sxs-lookup"><span data-stu-id="bbbf0-108">Members</span></span>

<span data-ttu-id="bbbf0-109">A classe **CIM \_ CollectionOfMSEs** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bbbf0-109">The **CIM\_CollectionOfMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="bbbf0-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bbbf0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bbbf0-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bbbf0-111">Properties</span></span>

<span data-ttu-id="bbbf0-112">A classe **CIM \_ CollectionOfMSEs** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bbbf0-112">The **CIM\_CollectionOfMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bbbf0-113">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="bbbf0-113">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbbf0-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bbbf0-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbbf0-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bbbf0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbbf0-116">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="bbbf0-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bbbf0-117">A identificação do objeto de coleção.</span><span class="sxs-lookup"><span data-stu-id="bbbf0-117">The identification of the collection object.</span></span> <span data-ttu-id="bbbf0-118">Quando uma subclasse, a propriedade **CollectionId** pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="bbbf0-118">When subclassed, the **CollectionID** property can be overridden as a key property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bbbf0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbbf0-119">Requirements</span></span>



| <span data-ttu-id="bbbf0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbbf0-120">Requirement</span></span> | <span data-ttu-id="bbbf0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="bbbf0-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbbf0-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bbbf0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bbbf0-123">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="bbbf0-123">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="bbbf0-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bbbf0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bbbf0-125">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="bbbf0-125">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="bbbf0-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="bbbf0-126">Namespace</span></span><br/>                | <span data-ttu-id="bbbf0-127">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="bbbf0-127">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bbbf0-128">MOF</span><span class="sxs-lookup"><span data-stu-id="bbbf0-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bbbf0-129"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bbbf0-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bbbf0-130">DLL</span><span class="sxs-lookup"><span data-stu-id="bbbf0-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbbf0-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bbbf0-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bbbf0-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="bbbf0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbbf0-133">**\_Coleção CIM**</span><span class="sxs-lookup"><span data-stu-id="bbbf0-133">**CIM\_Collection**</span></span>](cim-collection.md)
</dt> </dl>

 

