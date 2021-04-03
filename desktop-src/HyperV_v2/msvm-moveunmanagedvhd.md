---
description: Move um disco rígido virtual da origem para o caminho de destino.
ms.assetid: f51f7bf3-585a-442d-b84d-51d633c38dea
title: Classe Msvm_MoveUnmanagedVhd
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MoveUnmanagedVhd
- Msvm_MoveUnmanagedVhd.VhdSourcePath
- Msvm_MoveUnmanagedVhd.VhdDestinationPath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e98139b747f4b32265e27bc84ca240f496dea715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837129"
---
# <a name="msvm_moveunmanagedvhd-class"></a><span data-ttu-id="31e18-103">\_Classe Msvm MoveUnmanagedVhd</span><span class="sxs-lookup"><span data-stu-id="31e18-103">Msvm\_MoveUnmanagedVhd class</span></span>

<span data-ttu-id="31e18-104">Move um disco rígido virtual da origem para o caminho de destino.</span><span class="sxs-lookup"><span data-stu-id="31e18-104">Moves a virtual hard drive from the source to the destination path.</span></span>

<span data-ttu-id="31e18-105">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="31e18-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="31e18-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31e18-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_MoveUnmanagedVhd : CIM_ManagedElement
{
  string VhdSourcePath;
  string VhdDestinationPath;
};
```

## <a name="members"></a><span data-ttu-id="31e18-107">Membros</span><span class="sxs-lookup"><span data-stu-id="31e18-107">Members</span></span>

<span data-ttu-id="31e18-108">A classe **Msvm \_ MoveUnmanagedVhd** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="31e18-108">The **Msvm\_MoveUnmanagedVhd** class has these types of members:</span></span>

-   [<span data-ttu-id="31e18-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="31e18-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="31e18-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="31e18-110">Properties</span></span>

<span data-ttu-id="31e18-111">A classe **Msvm \_ MoveUnmanagedVhd** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="31e18-111">The **Msvm\_MoveUnmanagedVhd** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="31e18-112">**VhdDestinationPath**</span><span class="sxs-lookup"><span data-stu-id="31e18-112">**VhdDestinationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31e18-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="31e18-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31e18-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31e18-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31e18-115">O caminho de destino.</span><span class="sxs-lookup"><span data-stu-id="31e18-115">The destination path.</span></span>

</dd> <dt>

<span data-ttu-id="31e18-116">**VhdSourcePath**</span><span class="sxs-lookup"><span data-stu-id="31e18-116">**VhdSourcePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31e18-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="31e18-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31e18-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31e18-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31e18-119">O caminho de origem do disco rígido virtual a ser movido.</span><span class="sxs-lookup"><span data-stu-id="31e18-119">The source path of the virtual hard drive to move.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31e18-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31e18-120">Requirements</span></span>



| <span data-ttu-id="31e18-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="31e18-121">Requirement</span></span> | <span data-ttu-id="31e18-122">Valor</span><span class="sxs-lookup"><span data-stu-id="31e18-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31e18-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31e18-123">Minimum supported client</span></span><br/> | <span data-ttu-id="31e18-124">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="31e18-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="31e18-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31e18-125">Minimum supported server</span></span><br/> | <span data-ttu-id="31e18-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="31e18-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="31e18-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="31e18-127">Namespace</span></span><br/>                | <span data-ttu-id="31e18-128">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="31e18-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="31e18-129">MOF</span><span class="sxs-lookup"><span data-stu-id="31e18-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31e18-130"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31e18-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="31e18-131">DLL</span><span class="sxs-lookup"><span data-stu-id="31e18-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31e18-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="31e18-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="31e18-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="31e18-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31e18-134">**\_Managedelement do CIM**</span><span class="sxs-lookup"><span data-stu-id="31e18-134">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

 




