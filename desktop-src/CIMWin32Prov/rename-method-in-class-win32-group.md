---
description: Permite que o nome do grupo seja alterado.
ms.assetid: 7eb1360e-7416-4a90-abc6-c9a85a114316
ms.tgt_platform: multiple
title: Método Rename da classe Win32_Group
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Group.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c111a0c12d0fdc1ce3f6d6bcaa0e7b0f57831054
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755840"
---
# <a name="rename-method-of-the-win32_group-class"></a><span data-ttu-id="5793d-103">Método Rename da classe de \_ grupo Win32</span><span class="sxs-lookup"><span data-stu-id="5793d-103">Rename method of the Win32\_Group class</span></span>

<span data-ttu-id="5793d-104">O método **Rename** da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) permite que o nome do grupo seja alterado.</span><span class="sxs-lookup"><span data-stu-id="5793d-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method allows the group name to be changed.</span></span>

<span data-ttu-id="5793d-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="5793d-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5793d-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5793d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5793d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5793d-107">Syntax</span></span>


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="5793d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5793d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5793d-109">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="5793d-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5793d-110">Nome da conta de usuário do Windows no domínio especificado pela propriedade de **domínio** dessa classe.</span><span class="sxs-lookup"><span data-stu-id="5793d-110">Name of the Windows user account on the domain specified by the **Domain** property of this class.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5793d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5793d-111">Return value</span></span>

<span data-ttu-id="5793d-112">O método **Rename** pode retornar os códigos de erro listados na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="5793d-112">The **Rename** method can return the error codes listed in the following list.</span></span> <span data-ttu-id="5793d-113">Para valores inteiros diferentes daqueles listados, consulte códigos de [ \_ retorno do WMI](/windows/desktop/WmiSdk/wmi-return-codes).</span><span class="sxs-lookup"><span data-stu-id="5793d-113">For integer values other than those listed, refer to [WMI\_Return Codes](/windows/desktop/WmiSdk/wmi-return-codes).</span></span>

<dl> <dt>

<span data-ttu-id="5793d-114">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="5793d-114">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="5793d-115">0</span><span class="sxs-lookup"><span data-stu-id="5793d-115">0</span></span>

<span data-ttu-id="5793d-116">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="5793d-116">Success.</span></span>

</dd> <dt>

<span data-ttu-id="5793d-117">**Instância não encontrada**</span><span class="sxs-lookup"><span data-stu-id="5793d-117">**Instance not found**</span></span>
</dt> <dd>

<span data-ttu-id="5793d-118">1</span><span class="sxs-lookup"><span data-stu-id="5793d-118">1</span></span>

</dd> <dt>

<span data-ttu-id="5793d-119">**Instância necessária**</span><span class="sxs-lookup"><span data-stu-id="5793d-119">**Instance required**</span></span>
</dt> <dd>

<span data-ttu-id="5793d-120">2</span><span class="sxs-lookup"><span data-stu-id="5793d-120">2</span></span>

</dd> <dt>

<span data-ttu-id="5793d-121">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="5793d-121">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="5793d-122">3</span><span class="sxs-lookup"><span data-stu-id="5793d-122">3</span></span>

</dd> <dt>

<span data-ttu-id="5793d-123">**Grupo não encontrado**</span><span class="sxs-lookup"><span data-stu-id="5793d-123">**Group not found**</span></span>
</dt> <dd>

<span data-ttu-id="5793d-124">4</span><span class="sxs-lookup"><span data-stu-id="5793d-124">4</span></span>

</dd> <dt>

<span data-ttu-id="5793d-125">**Domínio não encontrado**</span><span class="sxs-lookup"><span data-stu-id="5793d-125">**Domain not found**</span></span>
</dt> <dd>

<span data-ttu-id="5793d-126">5</span><span class="sxs-lookup"><span data-stu-id="5793d-126">5</span></span>

</dd> <dt>

<span data-ttu-id="5793d-127">**A operação é permitida somente no controlador de domínio primário do domínio**</span><span class="sxs-lookup"><span data-stu-id="5793d-127">**Operation is allowed only on the primary domain controller of the domain**</span></span>
</dt> <dd>

<span data-ttu-id="5793d-128">6</span><span class="sxs-lookup"><span data-stu-id="5793d-128">6</span></span>

</dd> <dt>

<span data-ttu-id="5793d-129">**A operação não é permitida em grupos especiais especificados; usuário, administrador, local ou convidado.**</span><span class="sxs-lookup"><span data-stu-id="5793d-129">**Operation is not allowed on specified special groups; user, admin, local or guest.**</span></span>
</dt> <dd>

<span data-ttu-id="5793d-130">7</span><span class="sxs-lookup"><span data-stu-id="5793d-130">7</span></span>

</dd> <dt>

<span data-ttu-id="5793d-131">**Outro erro de API**</span><span class="sxs-lookup"><span data-stu-id="5793d-131">**Other API error**</span></span>
</dt> <dd>

<span data-ttu-id="5793d-132">8</span><span class="sxs-lookup"><span data-stu-id="5793d-132">8</span></span>

</dd> <dt>

<span data-ttu-id="5793d-133">**Erro interno**</span><span class="sxs-lookup"><span data-stu-id="5793d-133">**Internal error**</span></span>
</dt> <dd>

<span data-ttu-id="5793d-134">9</span><span class="sxs-lookup"><span data-stu-id="5793d-134">9</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5793d-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5793d-135">Requirements</span></span>



| <span data-ttu-id="5793d-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="5793d-136">Requirement</span></span> | <span data-ttu-id="5793d-137">Valor</span><span class="sxs-lookup"><span data-stu-id="5793d-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5793d-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5793d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5793d-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5793d-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5793d-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5793d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5793d-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5793d-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5793d-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="5793d-142">Namespace</span></span><br/>                | <span data-ttu-id="5793d-143">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5793d-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5793d-144">MOF</span><span class="sxs-lookup"><span data-stu-id="5793d-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5793d-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5793d-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5793d-146">DLL</span><span class="sxs-lookup"><span data-stu-id="5793d-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5793d-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5793d-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5793d-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="5793d-148">See also</span></span>

<dl> <dt>

<span data-ttu-id="5793d-149">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5793d-149">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5793d-150">**\_Grupo Win32**</span><span class="sxs-lookup"><span data-stu-id="5793d-150">**Win32\_Group**</span></span>](win32-group.md)
</dt> <dt>

[<span data-ttu-id="5793d-151">**\_LogicalFileSecuritySetting Win32**</span><span class="sxs-lookup"><span data-stu-id="5793d-151">**Win32\_LogicalFileSecuritySetting**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)
</dt> </dl>

 

