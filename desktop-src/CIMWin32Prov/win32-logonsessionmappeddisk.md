---
description: A \_ classe Win32 LogonSessionMappedDisk representa uma associação entre uma sessão de logon e os discos lógicos mapeados definidos na sessão.
ms.assetid: 013ae55e-6dd1-42fb-bcba-74d6afa1b905
ms.tgt_platform: multiple
title: Classe Win32_LogonSessionMappedDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogonSessionMappedDisk
- Win32_LogonSessionMappedDisk.Antecedent
- Win32_LogonSessionMappedDisk.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: 203c9dd783dece52fa19905d51ece3bc26584dc6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501104"
---
# <a name="win32_logonsessionmappeddisk-class"></a><span data-ttu-id="1a740-103">\_Classe Win32 LogonSessionMappedDisk</span><span class="sxs-lookup"><span data-stu-id="1a740-103">Win32\_LogonSessionMappedDisk class</span></span>

<span data-ttu-id="1a740-104">A \_ classe Win32 LogonSessionMappedDisk representa uma associação entre uma sessão de logon e os discos lógicos mapeados definidos na sessão.</span><span class="sxs-lookup"><span data-stu-id="1a740-104">The Win32\_LogonSessionMappedDisk class represents an association between a logon session and the mapped logical disks defined within the session.</span></span>

<span data-ttu-id="1a740-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1a740-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a740-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a740-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32a"), AMENDMENT]
class Win32_LogonSessionMappedDisk : CIM_Dependency
{
  Win32_LogonSession      REF Antecedent;
  Win32_MappedLogicalDisk REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="1a740-107">Membros</span><span class="sxs-lookup"><span data-stu-id="1a740-107">Members</span></span>

<span data-ttu-id="1a740-108">A classe **Win32 \_ LogonSessionMappedDisk** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1a740-108">The **Win32\_LogonSessionMappedDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="1a740-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1a740-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a740-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1a740-110">Properties</span></span>

<span data-ttu-id="1a740-111">A classe **Win32 \_ LogonSessionMappedDisk** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1a740-111">The **Win32\_LogonSessionMappedDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1a740-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="1a740-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a740-113">Tipo de dados: **Win32 \_ LogonSession**</span><span class="sxs-lookup"><span data-stu-id="1a740-113">Data type: **Win32\_LogonSession**</span></span>
</dt> <dt>

<span data-ttu-id="1a740-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a740-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a740-115">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1a740-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1a740-116">A propriedade Antecedent faz referência a uma sessão de logon.</span><span class="sxs-lookup"><span data-stu-id="1a740-116">The Antecedent property references a logon session.</span></span>

</dd> <dt>

<span data-ttu-id="1a740-117">**Depende**</span><span class="sxs-lookup"><span data-stu-id="1a740-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a740-118">Tipo de dados: **Win32 \_ MappedLogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="1a740-118">Data type: **Win32\_MappedLogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="1a740-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a740-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a740-120">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1a740-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1a740-121">A Propriedade Dependent faz referência a um disco lógico mapeado definido na sessão referenciada pela propriedade Antecedent.</span><span class="sxs-lookup"><span data-stu-id="1a740-121">The Dependent property references a mapped logical disk defined within the session referenced by the Antecedent property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1a740-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a740-122">Requirements</span></span>



| <span data-ttu-id="1a740-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a740-123">Requirement</span></span> | <span data-ttu-id="1a740-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1a740-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a740-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a740-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1a740-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1a740-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1a740-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a740-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1a740-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a740-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1a740-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="1a740-129">Namespace</span></span><br/>                | <span data-ttu-id="1a740-130">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1a740-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1a740-131">MOF</span><span class="sxs-lookup"><span data-stu-id="1a740-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a740-132"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a740-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a740-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1a740-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a740-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a740-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a740-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a740-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a740-136">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="1a740-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

