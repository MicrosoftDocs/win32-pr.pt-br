---
description: Inicia o depurador que está registrado atualmente para este processo.
ms.assetid: 63c30db8-6117-4353-9132-4f39c72a6637
ms.tgt_platform: multiple
title: Método AttachDebugger da classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.AttachDebugger
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 041bdeeab634ebed5c7ec2eccffe01f7cecce709
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826214"
---
# <a name="attachdebugger-method-of-the-win32_process-class"></a><span data-ttu-id="4aa2c-103">Método AttachDebugger da \_ classe Process do Win32</span><span class="sxs-lookup"><span data-stu-id="4aa2c-103">AttachDebugger method of the Win32\_Process class</span></span>

<span data-ttu-id="4aa2c-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **AttachDebugger** inicia o depurador que está atualmente registrado para esse processo.</span><span class="sxs-lookup"><span data-stu-id="4aa2c-104">The **AttachDebugger** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method starts the debugger that is currently registered for this process.</span></span>

<span data-ttu-id="4aa2c-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="4aa2c-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4aa2c-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4aa2c-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4aa2c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4aa2c-107">Syntax</span></span>


```mof
uint32 AttachDebugger();
```



## <a name="parameters"></a><span data-ttu-id="4aa2c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4aa2c-108">Parameters</span></span>

<span data-ttu-id="4aa2c-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4aa2c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4aa2c-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4aa2c-110">Return value</span></span>

<span data-ttu-id="4aa2c-111">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="4aa2c-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="4aa2c-112">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="4aa2c-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="4aa2c-113">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="4aa2c-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="4aa2c-114">**Conclusão bem-sucedida**</span><span class="sxs-lookup"><span data-stu-id="4aa2c-114">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="4aa2c-115">0</span><span class="sxs-lookup"><span data-stu-id="4aa2c-115">0</span></span>

<span data-ttu-id="4aa2c-116">Conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4aa2c-116">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="4aa2c-117">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="4aa2c-117">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="4aa2c-118">2</span><span class="sxs-lookup"><span data-stu-id="4aa2c-118">2</span></span>

<span data-ttu-id="4aa2c-119">O usuário não tem acesso às informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="4aa2c-119">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="4aa2c-120">**Privilégio insuficiente**</span><span class="sxs-lookup"><span data-stu-id="4aa2c-120">**Insufficient privilege**</span></span>
</dt> <dd>

<span data-ttu-id="4aa2c-121">3</span><span class="sxs-lookup"><span data-stu-id="4aa2c-121">3</span></span>

<span data-ttu-id="4aa2c-122">O usuário não tem privilégios suficientes.</span><span class="sxs-lookup"><span data-stu-id="4aa2c-122">The user does not have sufficient privilege.</span></span>

</dd> <dt>

<span data-ttu-id="4aa2c-123">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="4aa2c-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="4aa2c-124">8</span><span class="sxs-lookup"><span data-stu-id="4aa2c-124">8</span></span>

<span data-ttu-id="4aa2c-125">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="4aa2c-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="4aa2c-126">**demarcador não localizado**</span><span class="sxs-lookup"><span data-stu-id="4aa2c-126">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="4aa2c-127">9</span><span class="sxs-lookup"><span data-stu-id="4aa2c-127">9</span></span>

<span data-ttu-id="4aa2c-128">O caminho especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="4aa2c-128">The path specified does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="4aa2c-129">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="4aa2c-129">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="4aa2c-130">21</span><span class="sxs-lookup"><span data-stu-id="4aa2c-130">21</span></span>

<span data-ttu-id="4aa2c-131">O parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="4aa2c-131">The specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="4aa2c-132">**Outras**</span><span class="sxs-lookup"><span data-stu-id="4aa2c-132">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="4aa2c-133">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="4aa2c-133">22 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4aa2c-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4aa2c-134">Requirements</span></span>



| <span data-ttu-id="4aa2c-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="4aa2c-135">Requirement</span></span> | <span data-ttu-id="4aa2c-136">Valor</span><span class="sxs-lookup"><span data-stu-id="4aa2c-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4aa2c-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4aa2c-137">Minimum supported client</span></span><br/> | <span data-ttu-id="4aa2c-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4aa2c-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4aa2c-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4aa2c-139">Minimum supported server</span></span><br/> | <span data-ttu-id="4aa2c-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4aa2c-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4aa2c-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="4aa2c-141">Namespace</span></span><br/>                | <span data-ttu-id="4aa2c-142">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4aa2c-142">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4aa2c-143">MOF</span><span class="sxs-lookup"><span data-stu-id="4aa2c-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4aa2c-144"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4aa2c-144"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4aa2c-145">DLL</span><span class="sxs-lookup"><span data-stu-id="4aa2c-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4aa2c-146"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4aa2c-146"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aa2c-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="4aa2c-147">See also</span></span>

<dl> <dt>

<span data-ttu-id="4aa2c-148">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4aa2c-148">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4aa2c-149">**\_Processo Win32**</span><span class="sxs-lookup"><span data-stu-id="4aa2c-149">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

