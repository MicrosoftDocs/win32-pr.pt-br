---
description: Representa uma ACE (entrada de controle de acesso) que determina o acesso à sessão interativa de uma máquina virtual.
ms.assetid: dfec83d6-8033-47b5-aa6f-fc7447a29f43
title: Classe Msvm_InteractiveSessionACE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InteractiveSessionACE
- Msvm_InteractiveSessionACE.Trustee
- Msvm_InteractiveSessionACE.AccessType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6c4b63e769b04092323cd2da7362ef6b156886b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105792519"
---
# <a name="msvm_interactivesessionace-class"></a><span data-ttu-id="cd16c-103">\_Classe Msvm InteractiveSessionACE</span><span class="sxs-lookup"><span data-stu-id="cd16c-103">Msvm\_InteractiveSessionACE class</span></span>

<span data-ttu-id="cd16c-104">Representa uma ACE ( *entrada de controle de acesso* ) que determina o acesso à sessão interativa de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cd16c-104">Represents an *access control entry* (ACE) that determines access to the interactive session of a virtual machine.</span></span>

<span data-ttu-id="cd16c-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="cd16c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd16c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd16c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InteractiveSessionACE
{
  string Trustee;
  uint16 AccessType;
};
```

## <a name="members"></a><span data-ttu-id="cd16c-107">Membros</span><span class="sxs-lookup"><span data-stu-id="cd16c-107">Members</span></span>

<span data-ttu-id="cd16c-108">A classe **Msvm \_ InteractiveSessionACE** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cd16c-108">The **Msvm\_InteractiveSessionACE** class has these types of members:</span></span>

-   [<span data-ttu-id="cd16c-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cd16c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd16c-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cd16c-110">Properties</span></span>

<span data-ttu-id="cd16c-111">A classe **Msvm \_ InteractiveSessionACE** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cd16c-111">The **Msvm\_InteractiveSessionACE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd16c-112">**AccessType**</span><span class="sxs-lookup"><span data-stu-id="cd16c-112">**AccessType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd16c-113">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd16c-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd16c-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd16c-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd16c-115">Indica se a ACE concede ou nega o acesso ao Trustee.</span><span class="sxs-lookup"><span data-stu-id="cd16c-115">Indicates whether the ACE grants or denies access to the trustee.</span></span>

<dt>

<span id="Access_Allowed"></span><span id="access_allowed"></span><span id="ACCESS_ALLOWED"></span>

<span data-ttu-id="cd16c-116">**Acesso permitido** (0)</span><span class="sxs-lookup"><span data-stu-id="cd16c-116">**Access Allowed** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Access_Denied"></span><span id="access_denied"></span><span id="ACCESS_DENIED"></span>

<span data-ttu-id="cd16c-117">**Acesso negado** (1)</span><span class="sxs-lookup"><span data-stu-id="cd16c-117">**Access Denied** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cd16c-118">**Confiança**</span><span class="sxs-lookup"><span data-stu-id="cd16c-118">**Trustee**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd16c-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd16c-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd16c-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd16c-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd16c-121">Identifica a entidade de segurança que o ACE concede ou nega acesso ao.</span><span class="sxs-lookup"><span data-stu-id="cd16c-121">Identifies the security principal that the ACE grants or denies access to.</span></span> <span data-ttu-id="cd16c-122">Os formatos válidos para essa propriedade incluem o formato de nome de usuário compatível com o Windows SAM e o formato de cadeia de caracteres SID do Windows.</span><span class="sxs-lookup"><span data-stu-id="cd16c-122">Valid formats for this property include the Windows SAM-compatible user name format and the Windows SID string format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd16c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd16c-123">Requirements</span></span>



| <span data-ttu-id="cd16c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd16c-124">Requirement</span></span> | <span data-ttu-id="cd16c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="cd16c-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd16c-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd16c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cd16c-127">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="cd16c-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cd16c-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd16c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cd16c-129">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="cd16c-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cd16c-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="cd16c-130">Namespace</span></span><br/>                | <span data-ttu-id="cd16c-131">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="cd16c-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cd16c-132">MOF</span><span class="sxs-lookup"><span data-stu-id="cd16c-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd16c-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd16c-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd16c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="cd16c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd16c-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cd16c-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cd16c-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd16c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd16c-137">**GetInteractiveSessionACL**</span><span class="sxs-lookup"><span data-stu-id="cd16c-137">**GetInteractiveSessionACL**</span></span>](getinteractivesessionacl-msvm-terminalservice.md)
</dt> </dl>

 

 




