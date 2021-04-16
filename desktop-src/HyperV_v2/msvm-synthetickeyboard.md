---
description: Representa um dispositivo de teclado sintético.
ms.assetid: 8fe9bdd5-59e8-421d-812a-08aa3c54c88f
title: Classe Msvm_SyntheticKeyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticKeyboard
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 64ac153a2c20815891d8a39fd10f58562ed8d81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751224"
---
# <a name="msvm_synthetickeyboard-class"></a><span data-ttu-id="0aab5-103">\_Classe Msvm SyntheticKeyboard</span><span class="sxs-lookup"><span data-stu-id="0aab5-103">Msvm\_SyntheticKeyboard class</span></span>

<span data-ttu-id="0aab5-104">Representa um dispositivo de teclado sintético.</span><span class="sxs-lookup"><span data-stu-id="0aab5-104">Represents a synthetic keyboard device.</span></span>

<span data-ttu-id="0aab5-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0aab5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0aab5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0aab5-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticKeyboard : CIM_UserDevice
{
};
```

## <a name="members"></a><span data-ttu-id="0aab5-107">Membros</span><span class="sxs-lookup"><span data-stu-id="0aab5-107">Members</span></span>

<span data-ttu-id="0aab5-108">A classe **Msvm \_ SyntheticKeyboard** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0aab5-108">The **Msvm\_SyntheticKeyboard** class has these types of members:</span></span>

-   [<span data-ttu-id="0aab5-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="0aab5-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0aab5-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="0aab5-110">Methods</span></span>

<span data-ttu-id="0aab5-111">A classe **Msvm \_ SyntheticKeyboard** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="0aab5-111">The **Msvm\_SyntheticKeyboard** class has these methods.</span></span>



| <span data-ttu-id="0aab5-112">Método</span><span class="sxs-lookup"><span data-stu-id="0aab5-112">Method</span></span>                                                                  | <span data-ttu-id="0aab5-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="0aab5-113">Description</span></span>                         |
|:------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="0aab5-114">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="0aab5-114">**RequestStateChange**</span></span>](msvm-synthetickeyboard-requeststatechange.md) | <span data-ttu-id="0aab5-115">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="0aab5-115">Requests a state change.</span></span><br/> |
| [<span data-ttu-id="0aab5-116">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="0aab5-116">**Reset**</span></span>](msvm-synthetickeyboard-reset.md)                           | <span data-ttu-id="0aab5-117">Redefine o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0aab5-117">resets the device.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="0aab5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0aab5-118">Requirements</span></span>



| <span data-ttu-id="0aab5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0aab5-119">Requirement</span></span> | <span data-ttu-id="0aab5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0aab5-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aab5-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0aab5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0aab5-122">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0aab5-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="0aab5-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0aab5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0aab5-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0aab5-124">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0aab5-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="0aab5-125">Namespace</span></span><br/>                | <span data-ttu-id="0aab5-126">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="0aab5-126">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0aab5-127">MOF</span><span class="sxs-lookup"><span data-stu-id="0aab5-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0aab5-128"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0aab5-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0aab5-129">DLL</span><span class="sxs-lookup"><span data-stu-id="0aab5-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0aab5-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0aab5-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0aab5-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="0aab5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aab5-132">**Userdevice do CIM \_**</span><span class="sxs-lookup"><span data-stu-id="0aab5-132">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> </dl>

 

 




