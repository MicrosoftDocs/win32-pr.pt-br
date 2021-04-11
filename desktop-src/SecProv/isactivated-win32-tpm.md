---
description: O método isActivated da classe Win32 \_ TPM indica se o dispositivo está ativado.
ms.assetid: 862c386c-c5b5-44d2-89a5-3735b99bf8bc
title: Método isActivated da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsActivated
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6482163a27f211b4f4ce24284a8339f2b7254f3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170912"
---
# <a name="isactivated-method-of-the-win32_tpm-class"></a><span data-ttu-id="95af9-103">Método isActivated da \_ classe TPM do Win32</span><span class="sxs-lookup"><span data-stu-id="95af9-103">IsActivated method of the Win32\_Tpm class</span></span>

<span data-ttu-id="95af9-104">O método **isActivated** da classe [**Win32 \_ TPM**](win32-tpm.md) indica se o dispositivo está ativado.</span><span class="sxs-lookup"><span data-stu-id="95af9-104">The **IsActivated** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="95af9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95af9-105">Syntax</span></span>


```mof
uint32 IsActivated(
  [out] boolean IsActivated
);
```



## <a name="parameters"></a><span data-ttu-id="95af9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95af9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95af9-107">*Isactivad* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="95af9-107">*IsActivated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95af9-108">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="95af9-108">Type: **boolean**</span></span>

<span data-ttu-id="95af9-109">Se **for true**, o dispositivo será ativado.</span><span class="sxs-lookup"><span data-stu-id="95af9-109">If **true**, the device is activated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95af9-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="95af9-110">Return value</span></span>

<span data-ttu-id="95af9-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="95af9-111">Type: **uint32**</span></span>

<span data-ttu-id="95af9-112">Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="95af9-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="95af9-113">Os códigos de retorno comuns são listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="95af9-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="95af9-114">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="95af9-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="95af9-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="95af9-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="95af9-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="95af9-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="95af9-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="95af9-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="95af9-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="95af9-118">Remarks</span></span>

<span data-ttu-id="95af9-119">A desativação é semelhante à desabilitada, mas as alterações de estado operacional são possíveis.</span><span class="sxs-lookup"><span data-stu-id="95af9-119">Deactivation is similar to disabled, but operational state changes are possible.</span></span> <span data-ttu-id="95af9-120">De acordo com a especificação de TCG (Trusted Computing Group) v 1.2, somente os comandos a seguir estão disponíveis quando o dispositivo está em um estado desativado.</span><span class="sxs-lookup"><span data-stu-id="95af9-120">According to the Trusted Computing Group (TCG) v1.2 specification only the following commands are available when the device is in a deactivated state.</span></span>

-   <span data-ttu-id="95af9-121">\_CONTINUESELFTEST TPM</span><span class="sxs-lookup"><span data-stu-id="95af9-121">TPM\_ContinueSelfTest</span></span>
-   <span data-ttu-id="95af9-122">\_DSAP TPM</span><span class="sxs-lookup"><span data-stu-id="95af9-122">TPM\_DSAP</span></span>
-   <span data-ttu-id="95af9-123">\_FLUSHSPECIFIC TPM</span><span class="sxs-lookup"><span data-stu-id="95af9-123">TPM\_FlushSpecific</span></span>
-   <span data-ttu-id="95af9-124">GetCapability do TPM \_</span><span class="sxs-lookup"><span data-stu-id="95af9-124">TPM\_GetCapability</span></span>
-   <span data-ttu-id="95af9-125">GetResult do TPM \_</span><span class="sxs-lookup"><span data-stu-id="95af9-125">TPM\_GetTestResult</span></span>
-   <span data-ttu-id="95af9-126">Inicialização do TPM \_</span><span class="sxs-lookup"><span data-stu-id="95af9-126">TPM\_Init</span></span>
-   <span data-ttu-id="95af9-127">\_OIAP TPM</span><span class="sxs-lookup"><span data-stu-id="95af9-127">TPM\_OIAP</span></span>
-   <span data-ttu-id="95af9-128">\_oSAP TPM</span><span class="sxs-lookup"><span data-stu-id="95af9-128">TPM\_OSAP</span></span>
-   <span data-ttu-id="95af9-129">\_OWNERSETDISABLE TPM</span><span class="sxs-lookup"><span data-stu-id="95af9-129">TPM\_OwnerSetDisable</span></span>
-   <span data-ttu-id="95af9-130">Redefinição de TPM \_ PCR \_</span><span class="sxs-lookup"><span data-stu-id="95af9-130">TPM\_PCR\_Reset</span></span>
-   <span data-ttu-id="95af9-131">\_PHYSICALDISABLE TPM</span><span class="sxs-lookup"><span data-stu-id="95af9-131">TPM\_PhysicalDisable</span></span>
-   <span data-ttu-id="95af9-132">\_PHYSICALENABLE TPM</span><span class="sxs-lookup"><span data-stu-id="95af9-132">TPM\_PhysicalEnable</span></span>
-   <span data-ttu-id="95af9-133">\_PHYSICALSETDEACTIVATED TPM</span><span class="sxs-lookup"><span data-stu-id="95af9-133">TPM\_PhysicalSetDeactivated</span></span>
-   <span data-ttu-id="95af9-134">Redefinição do TPM \_</span><span class="sxs-lookup"><span data-stu-id="95af9-134">TPM\_Reset</span></span>
-   <span data-ttu-id="95af9-135">\_SAVESTATE TPM</span><span class="sxs-lookup"><span data-stu-id="95af9-135">TPM\_SaveState</span></span>
-   <span data-ttu-id="95af9-136">\_SELFTESTFULL TPM</span><span class="sxs-lookup"><span data-stu-id="95af9-136">TPM\_SelfTestFull</span></span>
-   <span data-ttu-id="95af9-137">Recurso do TPM \_</span><span class="sxs-lookup"><span data-stu-id="95af9-137">TPM\_SetCapability</span></span>
-   <span data-ttu-id="95af9-138">\_SHA1COMPLETE TPM</span><span class="sxs-lookup"><span data-stu-id="95af9-138">TPM\_SHA1Complete</span></span>
-   <span data-ttu-id="95af9-139">\_SHA1START TPM</span><span class="sxs-lookup"><span data-stu-id="95af9-139">TPM\_SHA1Start</span></span>
-   <span data-ttu-id="95af9-140">\_SHA1UPDATE TPM</span><span class="sxs-lookup"><span data-stu-id="95af9-140">TPM\_SHA1Update</span></span>
-   <span data-ttu-id="95af9-141">Inicialização do TPM \_</span><span class="sxs-lookup"><span data-stu-id="95af9-141">TPM\_Startup</span></span>
-   <span data-ttu-id="95af9-142">\_TAKEOWNERSHIP TPM</span><span class="sxs-lookup"><span data-stu-id="95af9-142">TPM\_TakeOwnership</span></span>
-   <span data-ttu-id="95af9-143">\_Identificador de término do TPM \_</span><span class="sxs-lookup"><span data-stu-id="95af9-143">TPM\_Terminate\_Handle</span></span>

<span data-ttu-id="95af9-144">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="95af9-144">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="95af9-145">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="95af9-145">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="95af9-146">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="95af9-146">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="95af9-147">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="95af9-147">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95af9-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95af9-148">Requirements</span></span>



| <span data-ttu-id="95af9-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="95af9-149">Requirement</span></span> | <span data-ttu-id="95af9-150">Valor</span><span class="sxs-lookup"><span data-stu-id="95af9-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="95af9-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95af9-151">Minimum supported client</span></span><br/> | <span data-ttu-id="95af9-152">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="95af9-152">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="95af9-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95af9-153">Minimum supported server</span></span><br/> | <span data-ttu-id="95af9-154">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="95af9-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="95af9-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="95af9-155">Namespace</span></span><br/>                | <span data-ttu-id="95af9-156">\\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="95af9-156">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="95af9-157">MOF</span><span class="sxs-lookup"><span data-stu-id="95af9-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95af9-158"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="95af9-158"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="95af9-159">DLL</span><span class="sxs-lookup"><span data-stu-id="95af9-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95af9-160"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="95af9-160"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95af9-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="95af9-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95af9-162">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="95af9-162">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
