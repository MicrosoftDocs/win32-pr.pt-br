---
description: A \_ classe WMI de associação GroupUser do Win32 relaciona um grupo e uma conta que é membro desse grupo.
ms.assetid: 46dd65f0-b729-4b23-8a00-bc33d1a4868b
ms.tgt_platform: multiple
title: Classe Win32_GroupUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_GroupUser
- Win32_GroupUser.GroupComponent
- Win32_GroupUser.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 79035ff3c56331a240704cf6605fdf72efa4e81c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457119"
---
# <a name="win32_groupuser-class"></a><span data-ttu-id="a2c6a-103">\_Classe Win32 GroupUser</span><span class="sxs-lookup"><span data-stu-id="a2c6a-103">Win32\_GroupUser class</span></span>

<span data-ttu-id="a2c6a-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ GroupUser do Win32** relaciona um grupo e uma conta que é membro desse grupo.</span><span class="sxs-lookup"><span data-stu-id="a2c6a-104">The **Win32\_GroupUser** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a group and an account that is a member of that group.</span></span>

<span data-ttu-id="a2c6a-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a2c6a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a2c6a-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="a2c6a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2c6a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2c6a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C508-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_GroupUser : CIM_Component
{
  Win32_Group   REF GroupComponent;
  Win32_Account REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="a2c6a-108">Membros</span><span class="sxs-lookup"><span data-stu-id="a2c6a-108">Members</span></span>

<span data-ttu-id="a2c6a-109">A classe **Win32 \_ GroupUser** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a2c6a-109">The **Win32\_GroupUser** class has these types of members:</span></span>

-   [<span data-ttu-id="a2c6a-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a2c6a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a2c6a-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a2c6a-111">Properties</span></span>

<span data-ttu-id="a2c6a-112">A classe **Win32 \_ GroupUser** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a2c6a-112">The **Win32\_GroupUser** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a2c6a-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="a2c6a-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c6a-114">Tipo de dados **: \_ grupo Win32**</span><span class="sxs-lookup"><span data-stu-id="a2c6a-114">Data type: **Win32\_Group**</span></span>
</dt> <dt>

<span data-ttu-id="a2c6a-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c6a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2c6a-116">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| grupo WMI Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="a2c6a-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Group")</span></span>
</dt> </dl>

<span data-ttu-id="a2c6a-117">Referência à instância que representa o grupo do qual a conta é membro.</span><span class="sxs-lookup"><span data-stu-id="a2c6a-117">Reference to the instance representing the group of which the account is a member.</span></span>

</dd> <dt>

<span data-ttu-id="a2c6a-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="a2c6a-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2c6a-119">Tipo de dados **: \_ conta Win32**</span><span class="sxs-lookup"><span data-stu-id="a2c6a-119">Data type: **Win32\_Account**</span></span>
</dt> <dt>

<span data-ttu-id="a2c6a-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2c6a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2c6a-121">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| conta WMI Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="a2c6a-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Account")</span></span>
</dt> </dl>

<span data-ttu-id="a2c6a-122">Referência à instância que representa a conta de usuário ou sistema que faz parte de um grupo de contas.</span><span class="sxs-lookup"><span data-stu-id="a2c6a-122">Reference to the instance representing the user or system account that is a part of a group of accounts.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2c6a-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2c6a-123">Remarks</span></span>

<span data-ttu-id="a2c6a-124">A classe **Win32 \_ GroupUser** é derivada do [**\_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="a2c6a-124">The **Win32\_GroupUser** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a2c6a-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a2c6a-125">Examples</span></span>

<span data-ttu-id="a2c6a-126">Para obter um exemplo do PowerShell de \_ como usar o Win32 GroupUser para recuperar uma lista de membros do grupo local, consulte o [exemplo listar membros do grupo local em um computador remoto usando o WMI e o PowerShell](https://Gallery.TechNet.Microsoft.Com/List-local-group-members-762b48c5) na galeria do TechNet.</span><span class="sxs-lookup"><span data-stu-id="a2c6a-126">For a PowerShell example of using Win32\_GroupUser to retrieve a list of local group members, see the [List local group members on a remote computer using WMI and PowerShell sample](https://Gallery.TechNet.Microsoft.Com/List-local-group-members-762b48c5) on TechNet Gallery.</span></span>

<span data-ttu-id="a2c6a-127">O exemplo de código VBScript do [recuperador de informações do WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) na galeria do TechNet usa a classe **Win32 \_ GroupUser** para recuperar informações do usuário de vários computadores remotos.</span><span class="sxs-lookup"><span data-stu-id="a2c6a-127">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_GroupUser** class to retrieve user information from a number of remote computers.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2c6a-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2c6a-128">Requirements</span></span>



| <span data-ttu-id="a2c6a-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2c6a-129">Requirement</span></span> | <span data-ttu-id="a2c6a-130">Valor</span><span class="sxs-lookup"><span data-stu-id="a2c6a-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2c6a-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2c6a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a2c6a-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a2c6a-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a2c6a-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2c6a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a2c6a-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2c6a-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a2c6a-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="a2c6a-135">Namespace</span></span><br/>                | <span data-ttu-id="a2c6a-136">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a2c6a-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a2c6a-137">MOF</span><span class="sxs-lookup"><span data-stu-id="a2c6a-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2c6a-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a2c6a-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2c6a-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a2c6a-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2c6a-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2c6a-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2c6a-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2c6a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2c6a-142">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="a2c6a-142">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="a2c6a-143">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a2c6a-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

