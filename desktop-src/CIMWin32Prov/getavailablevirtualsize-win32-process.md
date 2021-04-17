---
description: Recupera o tamanho atual, em bytes, do espaço de endereço virtual livre disponível para o processo.
ms.assetid: 13b3b347-5db1-484f-bd1d-3a604eb6bc5b
ms.tgt_platform: multiple
title: Método GetAvailableVirtualSize da classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetAvailableVirtualSize
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ee6e798b8df32822de481f3af1dc6b21a81d1024
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756254"
---
# <a name="getavailablevirtualsize-method-of-the-win32_process-class"></a><span data-ttu-id="38b9f-103">Método GetAvailableVirtualSize da \_ classe Process do Win32</span><span class="sxs-lookup"><span data-stu-id="38b9f-103">GetAvailableVirtualSize method of the Win32\_Process class</span></span>

<span data-ttu-id="38b9f-104">Recupera o tamanho atual, em bytes, do espaço de endereço virtual livre disponível para o processo.</span><span class="sxs-lookup"><span data-stu-id="38b9f-104">Retrieves the current size, in bytes, of the free virtual address space available to the process.</span></span>

## <a name="syntax"></a><span data-ttu-id="38b9f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38b9f-105">Syntax</span></span>


```mof
uint32 GetAvailableVirtualSize(
  [out] uint64 AvailableVirtualSize
);
```



## <a name="parameters"></a><span data-ttu-id="38b9f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38b9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38b9f-107">*AvailableVirtualSize* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="38b9f-107">*AvailableVirtualSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38b9f-108">O parâmetro *AvailableVirtualSize* retorna o espaço de endereço virtual livre disponível para esse processo.</span><span class="sxs-lookup"><span data-stu-id="38b9f-108">The *AvailableVirtualSize* parameter returns the free virtual address space available to this process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38b9f-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="38b9f-109">Return value</span></span>

<span data-ttu-id="38b9f-110">Retorna zero (0) para indicar êxito.</span><span class="sxs-lookup"><span data-stu-id="38b9f-110">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="38b9f-111">Qualquer outro número indica um erro.</span><span class="sxs-lookup"><span data-stu-id="38b9f-111">Any other number indicates an error.</span></span> <span data-ttu-id="38b9f-112">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="38b9f-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="38b9f-113">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="38b9f-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="38b9f-114">**Conclusão bem-sucedida**</span><span class="sxs-lookup"><span data-stu-id="38b9f-114">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="38b9f-115">0</span><span class="sxs-lookup"><span data-stu-id="38b9f-115">0</span></span>

<span data-ttu-id="38b9f-116">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="38b9f-116">The operation completed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="38b9f-117">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="38b9f-117">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="38b9f-118">2</span><span class="sxs-lookup"><span data-stu-id="38b9f-118">2</span></span>

<span data-ttu-id="38b9f-119">O usuário não tem acesso às informações solicitadas</span><span class="sxs-lookup"><span data-stu-id="38b9f-119">The user does not have access to the requested information</span></span>

</dd> <dt>

<span data-ttu-id="38b9f-120">**Privilégio insuficiente**</span><span class="sxs-lookup"><span data-stu-id="38b9f-120">**Insufficient privilege**</span></span>
</dt> <dd>

<span data-ttu-id="38b9f-121">3</span><span class="sxs-lookup"><span data-stu-id="38b9f-121">3</span></span>

<span data-ttu-id="38b9f-122">O usuário não tem privilégios suficientes.</span><span class="sxs-lookup"><span data-stu-id="38b9f-122">The user does not have sufficient privilege.</span></span>

</dd> <dt>

<span data-ttu-id="38b9f-123">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="38b9f-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="38b9f-124">8</span><span class="sxs-lookup"><span data-stu-id="38b9f-124">8</span></span>

<span data-ttu-id="38b9f-125">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="38b9f-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="38b9f-126">**demarcador não localizado**</span><span class="sxs-lookup"><span data-stu-id="38b9f-126">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="38b9f-127">9</span><span class="sxs-lookup"><span data-stu-id="38b9f-127">9</span></span>

<span data-ttu-id="38b9f-128">O caminho especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="38b9f-128">The path specified does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="38b9f-129">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="38b9f-129">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="38b9f-130">21</span><span class="sxs-lookup"><span data-stu-id="38b9f-130">21</span></span>

<span data-ttu-id="38b9f-131">O parâmetro especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="38b9f-131">The specified parameter is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="38b9f-132">**Outras**</span><span class="sxs-lookup"><span data-stu-id="38b9f-132">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="38b9f-133">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="38b9f-133">22 4294967295</span></span>

<span data-ttu-id="38b9f-134">Para valores diferentes daqueles listados, consulte a documentação de [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="38b9f-134">For values other than those listed, refer to the [System Error Codes](/windows/desktop/Debug/system-error-codes) documentation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="38b9f-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38b9f-135">Requirements</span></span>



| <span data-ttu-id="38b9f-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="38b9f-136">Requirement</span></span> | <span data-ttu-id="38b9f-137">Valor</span><span class="sxs-lookup"><span data-stu-id="38b9f-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38b9f-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38b9f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="38b9f-139">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="38b9f-139">Windows 8.1</span></span><br/>                                                                  |
| <span data-ttu-id="38b9f-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38b9f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="38b9f-141">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="38b9f-141">Windows Server 2012 R2</span></span><br/>                                                       |
| <span data-ttu-id="38b9f-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="38b9f-142">Namespace</span></span><br/>                | <span data-ttu-id="38b9f-143">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="38b9f-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="38b9f-144">MOF</span><span class="sxs-lookup"><span data-stu-id="38b9f-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38b9f-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38b9f-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="38b9f-146">DLL</span><span class="sxs-lookup"><span data-stu-id="38b9f-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38b9f-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38b9f-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38b9f-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="38b9f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38b9f-149">**\_Processo Win32**</span><span class="sxs-lookup"><span data-stu-id="38b9f-149">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

