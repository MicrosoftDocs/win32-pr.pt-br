---
description: O método IsEnabled da classe Win32 \_ TPM indica se o dispositivo está habilitado. Esse valor pode ser alterado pelos métodos Enable e Disable.
ms.assetid: e1d5513f-33eb-49e3-9582-d6c103ca5d03
title: Método IsEnabled da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d808bb68e53b1a24ff668d1b7a9680b5d57b5e9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782936"
---
# <a name="isenabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="20991-104">Método IsEnabled da classe do \_ TPM do Win32</span><span class="sxs-lookup"><span data-stu-id="20991-104">IsEnabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="20991-105">O método **IsEnabled** da classe [**Win32 \_ TPM**](win32-tpm.md) indica se o dispositivo está habilitado.</span><span class="sxs-lookup"><span data-stu-id="20991-105">The **IsEnabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device is enabled.</span></span> <span data-ttu-id="20991-106">Esse valor pode ser alterado pelos métodos [**Enable**](enable-win32-tpm.md) e [**Disable**](disable-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="20991-106">This value can be changed by the [**Enable**](enable-win32-tpm.md) and [**Disable**](disable-win32-tpm.md) methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="20991-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20991-107">Syntax</span></span>


```mof
uint32 IsEnabled(
  [out] boolean IsEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="20991-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20991-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20991-109">*IsEnabled* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="20991-109">*IsEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20991-110">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="20991-110">Type: **boolean**</span></span>

<span data-ttu-id="20991-111">Se for **true**, o dispositivo será habilitado.</span><span class="sxs-lookup"><span data-stu-id="20991-111">If **true**, the device is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20991-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="20991-112">Return value</span></span>

<span data-ttu-id="20991-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20991-113">Type: **uint32**</span></span>

<span data-ttu-id="20991-114">Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="20991-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="20991-115">Os códigos de retorno comuns são listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="20991-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="20991-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="20991-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="20991-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="20991-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="20991-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="20991-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="20991-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="20991-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="20991-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="20991-120">Remarks</span></span>

<span data-ttu-id="20991-121">De acordo com a especificação de TCG (Trusted Computing Group) v 1.2, somente os comandos a seguir estão disponíveis quando o dispositivo está em um estado desativado.</span><span class="sxs-lookup"><span data-stu-id="20991-121">According to the Trusted Computing Group (TCG) v1.2 specification only the following commands are available when the device is in a deactivated state.</span></span>

-   <span data-ttu-id="20991-122">\_CONTINUESELFTEST TPM</span><span class="sxs-lookup"><span data-stu-id="20991-122">TPM\_ContinueSelfTest</span></span>
-   <span data-ttu-id="20991-123">\_DSAP TPM</span><span class="sxs-lookup"><span data-stu-id="20991-123">TPM\_DSAP</span></span>
-   <span data-ttu-id="20991-124">\_FLUSHSPECIFIC TPM</span><span class="sxs-lookup"><span data-stu-id="20991-124">TPM\_FlushSpecific</span></span>
-   <span data-ttu-id="20991-125">GetCapability do TPM \_</span><span class="sxs-lookup"><span data-stu-id="20991-125">TPM\_GetCapability</span></span>
-   <span data-ttu-id="20991-126">GetResult do TPM \_</span><span class="sxs-lookup"><span data-stu-id="20991-126">TPM\_GetTestResult</span></span>
-   <span data-ttu-id="20991-127">Inicialização do TPM \_</span><span class="sxs-lookup"><span data-stu-id="20991-127">TPM\_Init</span></span>
-   <span data-ttu-id="20991-128">\_OIAP TPM</span><span class="sxs-lookup"><span data-stu-id="20991-128">TPM\_OIAP</span></span>
-   <span data-ttu-id="20991-129">\_oSAP TPM</span><span class="sxs-lookup"><span data-stu-id="20991-129">TPM\_OSAP</span></span>
-   <span data-ttu-id="20991-130">\_OWNERSETDISABLE TPM</span><span class="sxs-lookup"><span data-stu-id="20991-130">TPM\_OwnerSetDisable</span></span>
-   <span data-ttu-id="20991-131">Redefinição de TPM \_ PCR \_</span><span class="sxs-lookup"><span data-stu-id="20991-131">TPM\_PCR\_Reset</span></span>
-   <span data-ttu-id="20991-132">\_PHYSICALDISABLE TPM</span><span class="sxs-lookup"><span data-stu-id="20991-132">TPM\_PhysicalDisable</span></span>
-   <span data-ttu-id="20991-133">\_PHYSICALENABLE TPM</span><span class="sxs-lookup"><span data-stu-id="20991-133">TPM\_PhysicalEnable</span></span>
-   <span data-ttu-id="20991-134">\_PHYSICALSETDEACTIVATED TPM</span><span class="sxs-lookup"><span data-stu-id="20991-134">TPM\_PhysicalSetDeactivated</span></span>
-   <span data-ttu-id="20991-135">Redefinição do TPM \_</span><span class="sxs-lookup"><span data-stu-id="20991-135">TPM\_Reset</span></span>
-   <span data-ttu-id="20991-136">\_SAVESTATE TPM</span><span class="sxs-lookup"><span data-stu-id="20991-136">TPM\_SaveState</span></span>
-   <span data-ttu-id="20991-137">\_SELFTESTFULL TPM</span><span class="sxs-lookup"><span data-stu-id="20991-137">TPM\_SelfTestFull</span></span>
-   <span data-ttu-id="20991-138">Recurso do TPM \_</span><span class="sxs-lookup"><span data-stu-id="20991-138">TPM\_SetCapability</span></span>
-   <span data-ttu-id="20991-139">\_SHA1COMPLETE TPM</span><span class="sxs-lookup"><span data-stu-id="20991-139">TPM\_SHA1Complete</span></span>
-   <span data-ttu-id="20991-140">\_SHA1START TPM</span><span class="sxs-lookup"><span data-stu-id="20991-140">TPM\_SHA1Start</span></span>
-   <span data-ttu-id="20991-141">\_SHA1UPDATE TPM</span><span class="sxs-lookup"><span data-stu-id="20991-141">TPM\_SHA1Update</span></span>
-   <span data-ttu-id="20991-142">Inicialização do TPM \_</span><span class="sxs-lookup"><span data-stu-id="20991-142">TPM\_Startup</span></span>
-   <span data-ttu-id="20991-143">\_TAKEOWNERSHIP TPM</span><span class="sxs-lookup"><span data-stu-id="20991-143">TPM\_TakeOwnership</span></span>
-   <span data-ttu-id="20991-144">\_Identificador de término do TPM \_</span><span class="sxs-lookup"><span data-stu-id="20991-144">TPM\_Terminate\_Handle</span></span>

<span data-ttu-id="20991-145">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="20991-145">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="20991-146">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="20991-146">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="20991-147">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="20991-147">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="20991-148">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="20991-148">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20991-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20991-149">Requirements</span></span>



| <span data-ttu-id="20991-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="20991-150">Requirement</span></span> | <span data-ttu-id="20991-151">Valor</span><span class="sxs-lookup"><span data-stu-id="20991-151">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="20991-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20991-152">Minimum supported client</span></span><br/> | <span data-ttu-id="20991-153">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="20991-153">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="20991-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20991-154">Minimum supported server</span></span><br/> | <span data-ttu-id="20991-155">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="20991-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="20991-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="20991-156">Namespace</span></span><br/>                | <span data-ttu-id="20991-157">\\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="20991-157">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="20991-158">MOF</span><span class="sxs-lookup"><span data-stu-id="20991-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20991-159"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="20991-159"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="20991-160">DLL</span><span class="sxs-lookup"><span data-stu-id="20991-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20991-161"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="20991-161"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20991-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="20991-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20991-163">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="20991-163">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="20991-164">**Desabilitar**</span><span class="sxs-lookup"><span data-stu-id="20991-164">**Disable**</span></span>](disable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="20991-165">**Habilitar**</span><span class="sxs-lookup"><span data-stu-id="20991-165">**Enable**</span></span>](enable-win32-tpm.md)
</dt> </dl>

 

 
