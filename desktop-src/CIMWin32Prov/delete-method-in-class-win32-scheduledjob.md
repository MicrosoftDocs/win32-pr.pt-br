---
description: A exclusão&\# 8194; O método de classe WMI exclui um trabalho agendado.
ms.assetid: 064ff3f8-6d41-4f8d-a511-6c051bb48a5b
ms.tgt_platform: multiple
title: Método Delete da classe Win32_ScheduledJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd375c3da85bd72bddfc97ed3f57e52103578441
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089676"
---
# <a name="delete-method-of-the-win32_scheduledjob-class"></a><span data-ttu-id="ba53b-103">Método Delete da classe Win32 \_ ScheduledJob</span><span class="sxs-lookup"><span data-stu-id="ba53b-103">Delete method of the Win32\_ScheduledJob class</span></span>

<span data-ttu-id="ba53b-104">O método **excluir** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) exclui um trabalho agendado.</span><span class="sxs-lookup"><span data-stu-id="ba53b-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes a scheduled job.</span></span>

<span data-ttu-id="ba53b-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="ba53b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ba53b-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ba53b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ba53b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba53b-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="ba53b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba53b-108">Parameters</span></span>

<span data-ttu-id="ba53b-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ba53b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ba53b-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ba53b-110">Return value</span></span>

<span data-ttu-id="ba53b-111">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="ba53b-111">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="ba53b-112">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ba53b-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ba53b-113">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ba53b-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ba53b-114">**Conclusão bem-sucedida**</span><span class="sxs-lookup"><span data-stu-id="ba53b-114">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="ba53b-115">0</span><span class="sxs-lookup"><span data-stu-id="ba53b-115">0</span></span>

<span data-ttu-id="ba53b-116">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="ba53b-116">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="ba53b-117">**Sem suporte**</span><span class="sxs-lookup"><span data-stu-id="ba53b-117">**Not supported**</span></span>
</dt> <dd>

<span data-ttu-id="ba53b-118">1</span><span class="sxs-lookup"><span data-stu-id="ba53b-118">1</span></span>

<span data-ttu-id="ba53b-119">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="ba53b-119">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ba53b-120">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="ba53b-120">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="ba53b-121">2</span><span class="sxs-lookup"><span data-stu-id="ba53b-121">2</span></span>

<span data-ttu-id="ba53b-122">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="ba53b-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="ba53b-123">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="ba53b-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="ba53b-124">8</span><span class="sxs-lookup"><span data-stu-id="ba53b-124">8</span></span>

<span data-ttu-id="ba53b-125">Processo interativo.</span><span class="sxs-lookup"><span data-stu-id="ba53b-125">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="ba53b-126">**demarcador não localizado**</span><span class="sxs-lookup"><span data-stu-id="ba53b-126">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="ba53b-127">9</span><span class="sxs-lookup"><span data-stu-id="ba53b-127">9</span></span>

<span data-ttu-id="ba53b-128">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="ba53b-128">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="ba53b-129">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="ba53b-129">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ba53b-130">21</span><span class="sxs-lookup"><span data-stu-id="ba53b-130">21</span></span>

<span data-ttu-id="ba53b-131">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="ba53b-131">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="ba53b-132">**Serviço não iniciado**</span><span class="sxs-lookup"><span data-stu-id="ba53b-132">**Service not started**</span></span>
</dt> <dd>

<span data-ttu-id="ba53b-133">22</span><span class="sxs-lookup"><span data-stu-id="ba53b-133">22</span></span>

<span data-ttu-id="ba53b-134">A conta na qual esse serviço deve ser executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="ba53b-134">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="ba53b-135">**Outras**</span><span class="sxs-lookup"><span data-stu-id="ba53b-135">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="ba53b-136">23 4294967295</span><span class="sxs-lookup"><span data-stu-id="ba53b-136">23 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba53b-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba53b-137">Requirements</span></span>



| <span data-ttu-id="ba53b-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba53b-138">Requirement</span></span> | <span data-ttu-id="ba53b-139">Valor</span><span class="sxs-lookup"><span data-stu-id="ba53b-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba53b-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba53b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ba53b-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba53b-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ba53b-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba53b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ba53b-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba53b-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ba53b-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="ba53b-144">Namespace</span></span><br/>                | <span data-ttu-id="ba53b-145">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ba53b-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ba53b-146">MOF</span><span class="sxs-lookup"><span data-stu-id="ba53b-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba53b-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba53b-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba53b-148">DLL</span><span class="sxs-lookup"><span data-stu-id="ba53b-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba53b-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba53b-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba53b-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba53b-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="ba53b-151">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ba53b-151">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ba53b-152">**\_ScheduledJob Win32**</span><span class="sxs-lookup"><span data-stu-id="ba53b-152">**Win32\_ScheduledJob**</span></span>](win32-scheduledjob.md)
</dt> </dl>

 

