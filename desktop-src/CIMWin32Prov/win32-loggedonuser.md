---
description: A \_ classe WMI de associação LoggedOnUser do Win32 relaciona uma sessão e uma conta de usuário.
ms.assetid: b1233f90-4898-4ced-84d2-0858027e935a
ms.tgt_platform: multiple
title: Classe Win32_LoggedOnUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoggedOnUser
- Win32_LoggedOnUser.Dependent
- Win32_LoggedOnUser.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0f851c85563095a66197b0dde8e6cbddc9581f07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826625"
---
# <a name="win32_loggedonuser-class"></a><span data-ttu-id="5be85-103">\_Classe Win32 LoggedOnUser</span><span class="sxs-lookup"><span data-stu-id="5be85-103">Win32\_LoggedOnUser class</span></span>

<span data-ttu-id="5be85-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ LoggedOnUser do Win32** relaciona uma sessão e uma conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="5be85-104">The **Win32\_LoggedOnUser** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a session and a user account.</span></span>

<span data-ttu-id="5be85-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5be85-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5be85-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="5be85-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5be85-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5be85-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8BB5B3EC-E1F7-4b39-942A-605D5F55789A}"), AMENDMENT]
class Win32_LoggedOnUser : CIM_Dependency
{
  Win32_LogonSession REF Dependent;
  Win32_Account      REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="5be85-108">Membros</span><span class="sxs-lookup"><span data-stu-id="5be85-108">Members</span></span>

<span data-ttu-id="5be85-109">A classe **Win32 \_ LoggedOnUser** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5be85-109">The **Win32\_LoggedOnUser** class has these types of members:</span></span>

-   [<span data-ttu-id="5be85-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5be85-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5be85-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5be85-111">Properties</span></span>

<span data-ttu-id="5be85-112">A classe **Win32 \_ LoggedOnUser** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5be85-112">The **Win32\_LoggedOnUser** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5be85-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="5be85-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5be85-114">Tipo de dados **: \_ conta Win32**</span><span class="sxs-lookup"><span data-stu-id="5be85-114">Data type: **Win32\_Account**</span></span>
</dt> <dt>

<span data-ttu-id="5be85-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5be85-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5be85-116">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5be85-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5be85-117">Uma [**\_ conta Win32**](win32-account.md) que descreve a conta usada na inicialização desta sessão.</span><span class="sxs-lookup"><span data-stu-id="5be85-117">A [**Win32\_Account**](win32-account.md) that describes the account used in the initiation of this session.</span></span> <span data-ttu-id="5be85-118">A conta pode ser uma conta de usuário ou uma conta do sistema.</span><span class="sxs-lookup"><span data-stu-id="5be85-118">The account could be either a user account or a system account.</span></span>

</dd> <dt>

<span data-ttu-id="5be85-119">**Depende**</span><span class="sxs-lookup"><span data-stu-id="5be85-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5be85-120">Tipo de dados: **Win32 \_ LogonSession**</span><span class="sxs-lookup"><span data-stu-id="5be85-120">Data type: **Win32\_LogonSession**</span></span>
</dt> <dt>

<span data-ttu-id="5be85-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5be85-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5be85-122">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) (dependente), [**chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5be85-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Dependent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5be85-123">Um [**\_ LogonSession Win32**](win32-logonsessionmappeddisk.md) que descreve a sessão que a conta está usando no momento.</span><span class="sxs-lookup"><span data-stu-id="5be85-123">A [**Win32\_LogonSession**](win32-logonsessionmappeddisk.md) that describes the session that the account is currently using.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5be85-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="5be85-124">Remarks</span></span>

<span data-ttu-id="5be85-125">A classe **Win32 \_ LoggedOnUser** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="5be85-125">The **Win32\_LoggedOnUser** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5be85-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5be85-126">Examples</span></span>

<span data-ttu-id="5be85-127">O exemplo do PowerShell da [função Get-loggedonuser](https://Gallery.TechNet.Microsoft.Com/scriptcenter/0e43993a-895a-4afe-a2b2-045a5146048a) Obtém os usuários conectados em um computador local ou remoto, com informações de sessão.</span><span class="sxs-lookup"><span data-stu-id="5be85-127">The [get-loggedonuser function](https://Gallery.TechNet.Microsoft.Com/scriptcenter/0e43993a-895a-4afe-a2b2-045a5146048a) PowerShell sample gets the logged on users on a local or remote computer, with session information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5be85-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5be85-128">Requirements</span></span>



| <span data-ttu-id="5be85-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5be85-129">Requirement</span></span> | <span data-ttu-id="5be85-130">Valor</span><span class="sxs-lookup"><span data-stu-id="5be85-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5be85-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5be85-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5be85-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5be85-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5be85-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5be85-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5be85-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5be85-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5be85-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="5be85-135">Namespace</span></span><br/>                | <span data-ttu-id="5be85-136">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5be85-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5be85-137">MOF</span><span class="sxs-lookup"><span data-stu-id="5be85-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5be85-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5be85-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5be85-139">DLL</span><span class="sxs-lookup"><span data-stu-id="5be85-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5be85-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5be85-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5be85-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="5be85-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5be85-142">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="5be85-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="5be85-143">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5be85-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

