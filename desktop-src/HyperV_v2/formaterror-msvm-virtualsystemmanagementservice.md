---
description: Retorna uma cadeia de caracteres de mensagem de erro formatada para a matriz especificada de instâncias de erro Msvm inseridas \_ .
ms.assetid: 477EF4AE-00A8-4F2D-A335-E41A2EF620BB
title: Método FormatError da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.FormatError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e768a6ea968d428d7809c7c322a80f3ad233aa2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755110"
---
# <a name="formaterror-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="95a68-103">Método FormatError da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="95a68-103">FormatError method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="95a68-104">Retorna uma cadeia de caracteres de mensagem de erro formatada para a matriz especificada de instâncias de [**\_ erro Msvm**](msvm-error.md) inseridas.</span><span class="sxs-lookup"><span data-stu-id="95a68-104">Returns a formatted error message string for the specified array of embedded [**Msvm\_Error**](msvm-error.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="95a68-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95a68-105">Syntax</span></span>


```mof
uint32 FormatError(
  [in]  string Errors[],
  [out] string ErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="95a68-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95a68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95a68-107">*Erros* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="95a68-107">*Errors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95a68-108">Tipo: **cadeia \[ \] de caracteres**</span><span class="sxs-lookup"><span data-stu-id="95a68-108">Type: **string\[\]**</span></span>

<span data-ttu-id="95a68-109">Uma matriz de cadeias de caracteres que contém instâncias de [**\_ erro Msvm**](msvm-error.md) usadas para gerar a mensagem de erro de saída.</span><span class="sxs-lookup"><span data-stu-id="95a68-109">An array of strings containing [**Msvm\_Error**](msvm-error.md) instances used to generate the output error message.</span></span>

</dd> <dt>

<span data-ttu-id="95a68-110">*ErrorMessage* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="95a68-110">*ErrorMessage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95a68-111">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="95a68-111">Type: **string**</span></span>

<span data-ttu-id="95a68-112">Na saída, uma cadeia de caracteres que contém as mensagens de erro concatenadas representadas pelas instâncias de [**\_ erro Msvm**](msvm-error.md) passadas no parâmetro *erros* .</span><span class="sxs-lookup"><span data-stu-id="95a68-112">On output, a string that contains the concatenated error messages represented by the [**Msvm\_Error**](msvm-error.md) instances passed in the *Errors* parameter.</span></span> <span data-ttu-id="95a68-113">Cada cadeia de caracteres de erro é separada por um par de caracteres de nova linha (' \\ n').</span><span class="sxs-lookup"><span data-stu-id="95a68-113">Each error string is separated by a pair of newline characters ('\\n').</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95a68-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="95a68-114">Return value</span></span>

<span data-ttu-id="95a68-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="95a68-115">Type: **uint32**</span></span>

<span data-ttu-id="95a68-116">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="95a68-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="95a68-117">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="95a68-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="95a68-118">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="95a68-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="95a68-119">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="95a68-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="95a68-120">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="95a68-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="95a68-121">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="95a68-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="95a68-122">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="95a68-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="95a68-123">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="95a68-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="95a68-124">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="95a68-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="95a68-125">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="95a68-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="95a68-126">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="95a68-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="95a68-127">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="95a68-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="95a68-128">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="95a68-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="95a68-129">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="95a68-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="95a68-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="95a68-130">Remarks</span></span>

<span data-ttu-id="95a68-131">O acesso à classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="95a68-131">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="95a68-132">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="95a68-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="95a68-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95a68-133">Requirements</span></span>



| <span data-ttu-id="95a68-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="95a68-134">Requirement</span></span> | <span data-ttu-id="95a68-135">Valor</span><span class="sxs-lookup"><span data-stu-id="95a68-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95a68-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95a68-136">Minimum supported client</span></span><br/> | <span data-ttu-id="95a68-137">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="95a68-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="95a68-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95a68-138">Minimum supported server</span></span><br/> | <span data-ttu-id="95a68-139">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="95a68-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="95a68-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="95a68-140">Namespace</span></span><br/>                | <span data-ttu-id="95a68-141">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="95a68-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="95a68-142">MOF</span><span class="sxs-lookup"><span data-stu-id="95a68-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95a68-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="95a68-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="95a68-144">DLL</span><span class="sxs-lookup"><span data-stu-id="95a68-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95a68-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="95a68-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="95a68-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="95a68-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95a68-147">**FormatError (v1)**</span><span class="sxs-lookup"><span data-stu-id="95a68-147">**FormatError (V1)**</span></span>](/previous-versions/windows/desktop/virtual/formaterror-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="95a68-148">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="95a68-148">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

