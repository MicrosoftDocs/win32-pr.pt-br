---
description: Invoca a operação chkdsk no disco.
ms.assetid: 65942702-b660-46cd-b614-e3e1ec3df7b9
ms.tgt_platform: multiple
title: Método chkdsk da classe Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.Chkdsk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 662fc8739f90eea15295b762edc446ac16677aef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089408"
---
# <a name="chkdsk-method-of-the-win32_logicaldisk-class"></a><span data-ttu-id="368e4-103">Método chkdsk da classe do \_ LogicalDisk do Win32</span><span class="sxs-lookup"><span data-stu-id="368e4-103">Chkdsk method of the Win32\_LogicalDisk class</span></span>

<span data-ttu-id="368e4-104">O método de instância **chkdsk** invoca a operação **chkdsk** no disco.</span><span class="sxs-lookup"><span data-stu-id="368e4-104">The **Chkdsk** instance method invokes the **chkdsk** operation on the disk.</span></span>

<span data-ttu-id="368e4-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="368e4-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="368e4-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="368e4-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="368e4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="368e4-107">Syntax</span></span>


```mof
uint32 Chkdsk(
  [in] boolean FixErrors = ,
  [in] boolean VigorousIndexCheck = ,
  [in] boolean SkipFolderCycle = ,
  [in] boolean ForceDismount = ,
  [in] boolean RecoverBadSectors = ,
  [in] boolean OKToRunAtBootUp = 
);
```



## <a name="parameters"></a><span data-ttu-id="368e4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="368e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="368e4-109">*FixErrors* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="368e4-109">*FixErrors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="368e4-110">Indica o que deve ser feito para erros encontrados no disco.</span><span class="sxs-lookup"><span data-stu-id="368e4-110">Indicates what should be done to errors found on the disk.</span></span> <span data-ttu-id="368e4-111">Se **for true**, os erros serão corrigidos.</span><span class="sxs-lookup"><span data-stu-id="368e4-111">If **true**, then errors are fixed.</span></span> <span data-ttu-id="368e4-112">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="368e4-112">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="368e4-113">*VigorousIndexCheck* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="368e4-113">*VigorousIndexCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="368e4-114">Se **for true**, uma verificação menos rigorosa de entradas de índice deverá ser executada.</span><span class="sxs-lookup"><span data-stu-id="368e4-114">If **true**, a less vigorous check of index entries should be performed.</span></span> <span data-ttu-id="368e4-115">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="368e4-115">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="368e4-116">*SkipFolderCycle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="368e4-116">*SkipFolderCycle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="368e4-117">Se **for true**, a verificação de ciclo de pastas deverá ser ignorada.</span><span class="sxs-lookup"><span data-stu-id="368e4-117">If **true**, the folder cycle checking should be skipped.</span></span> <span data-ttu-id="368e4-118">O padrão é **true**.</span><span class="sxs-lookup"><span data-stu-id="368e4-118">The default is **true**.</span></span>

</dd> <dt>

<span data-ttu-id="368e4-119">*ForceDismount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="368e4-119">*ForceDismount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="368e4-120">Se **for true**, a unidade deverá ser forçada a desmontar antes de verificar.</span><span class="sxs-lookup"><span data-stu-id="368e4-120">If **true**, the drive should be forced to dismount before checking.</span></span> <span data-ttu-id="368e4-121">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="368e4-121">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="368e4-122">*RecoverBadSectors* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="368e4-122">*RecoverBadSectors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="368e4-123">Se **for verdadeiro**, os setores inválidos devem ser localizados e as informações legíveis devem ser recuperadas desses setores.</span><span class="sxs-lookup"><span data-stu-id="368e4-123">If **true**, the bad sectors should be located and the readable information should be recovered from these sectors.</span></span> <span data-ttu-id="368e4-124">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="368e4-124">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="368e4-125">*OKToRunAtBootUp* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="368e4-125">*OKToRunAtBootUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="368e4-126">Se **for true**, a operação **chkdsk** deverá ser executada no próximo tempo de inicialização, caso a operação não possa ser executada porque o disco está bloqueado no momento em que esse método é chamado.</span><span class="sxs-lookup"><span data-stu-id="368e4-126">If **true**, the **chkdsk** operation should be performed at next boot up time, in case the operation could not be performed because the disk is locked at time this method is called.</span></span> <span data-ttu-id="368e4-127">O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="368e4-127">The default is **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="368e4-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="368e4-128">Return value</span></span>

<span data-ttu-id="368e4-129">Retorna um valor de 0 (zero) se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="368e4-129">Returns a value of 0 (zero) if successful.</span></span> <span data-ttu-id="368e4-130">Outros valores são listados na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="368e4-130">Other values are listed in the following list.</span></span> <span data-ttu-id="368e4-131">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="368e4-131">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="368e4-132">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="368e4-132">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="368e4-133">**Êxito-chkdsk concluído**</span><span class="sxs-lookup"><span data-stu-id="368e4-133">**Success - Chkdsk completed**</span></span>
</dt> <dd>

<span data-ttu-id="368e4-134">0</span><span class="sxs-lookup"><span data-stu-id="368e4-134">0</span></span>

<span data-ttu-id="368e4-135">Êxito- [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) concluído</span><span class="sxs-lookup"><span data-stu-id="368e4-135">Success - [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) Completed</span></span>

</dd> <dt>

<span data-ttu-id="368e4-136">**Êxito-bloqueado e chkdsk agendado na reinicialização**</span><span class="sxs-lookup"><span data-stu-id="368e4-136">**Success - Locked and chkdsk scheduled on reboot**</span></span>
</dt> <dd>

<span data-ttu-id="368e4-137">1</span><span class="sxs-lookup"><span data-stu-id="368e4-137">1</span></span>

</dd> <dt>

<span data-ttu-id="368e4-138">**Falha-sistema de arquivos desconhecido**</span><span class="sxs-lookup"><span data-stu-id="368e4-138">**Failure - Unknown file system**</span></span>
</dt> <dd>

<span data-ttu-id="368e4-139">2</span><span class="sxs-lookup"><span data-stu-id="368e4-139">2</span></span>

</dd> <dt>

<span data-ttu-id="368e4-140">**Falha-erro desconhecido**</span><span class="sxs-lookup"><span data-stu-id="368e4-140">**Failure - Unknown error**</span></span>
</dt> <dd>

<span data-ttu-id="368e4-141">3</span><span class="sxs-lookup"><span data-stu-id="368e4-141">3</span></span>

</dd> <dt>

<span data-ttu-id="368e4-142">**Falha-sistema de arquivos sem suporte**</span><span class="sxs-lookup"><span data-stu-id="368e4-142">**Failure - Unsupported File System**</span></span>
</dt> <dd>

<span data-ttu-id="368e4-143">4</span><span class="sxs-lookup"><span data-stu-id="368e4-143">4</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="368e4-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="368e4-144">Remarks</span></span>

<span data-ttu-id="368e4-145">Esse método só é aplicável a essas instâncias de disco lógico que representam um disco físico no computador.</span><span class="sxs-lookup"><span data-stu-id="368e4-145">This method is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="368e4-146">Ele não é aplicável a unidades lógicas mapeadas.</span><span class="sxs-lookup"><span data-stu-id="368e4-146">It is not applicable to mapped logical drives.</span></span>

## <a name="examples"></a><span data-ttu-id="368e4-147">Exemplos</span><span class="sxs-lookup"><span data-stu-id="368e4-147">Examples</span></span>

<span data-ttu-id="368e4-148">O[é o conjunto de bits sujos chkdsk definido em uma](https://Gallery.TechNet.Microsoft.Com/57076851-97fb-4af6-8c5c-1e34156ceab4) amostra de código do PowerShell do servidor examina o sistema remoto e retorna um verdadeiro ou falso se o sinalizador chkdsk/f foi definido.</span><span class="sxs-lookup"><span data-stu-id="368e4-148">The[Is CHKDSK Dirty Bit Set on a server](https://Gallery.TechNet.Microsoft.Com/57076851-97fb-4af6-8c5c-1e34156ceab4) PowerShell code sample examines the remote system and returns a true or false if the chkdsk /f flag was set.</span></span>

<span data-ttu-id="368e4-149">O exemplo de código do PowerShell de [verificação](https://Gallery.TechNet.Microsoft.Com/Remotely-scan-disk-dd4fc267) remota inicia ou agenda o disco de verificação remotamente.</span><span class="sxs-lookup"><span data-stu-id="368e4-149">The [Remotely scan disk](https://Gallery.TechNet.Microsoft.Com/Remotely-scan-disk-dd4fc267) PowerShell code sample remotely starts or schedules Scan Disk.</span></span>

<span data-ttu-id="368e4-150">O exemplo de código VBScript a seguir executa ChkDsk.exe na unidade D em um computador.</span><span class="sxs-lookup"><span data-stu-id="368e4-150">The following VBScript code sample Runs ChkDsk.exe against drive D on a computer.</span></span>


```VB
Const FIX_ERRORS = True 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk.DeviceID='D:'") 
 
errReturn = objDisk.ChkDsk(FIX_ERRORS) 
```



## <a name="requirements"></a><span data-ttu-id="368e4-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="368e4-151">Requirements</span></span>



| <span data-ttu-id="368e4-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="368e4-152">Requirement</span></span> | <span data-ttu-id="368e4-153">Valor</span><span class="sxs-lookup"><span data-stu-id="368e4-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="368e4-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="368e4-154">Minimum supported client</span></span><br/> | <span data-ttu-id="368e4-155">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="368e4-155">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="368e4-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="368e4-156">Minimum supported server</span></span><br/> | <span data-ttu-id="368e4-157">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="368e4-157">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="368e4-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="368e4-158">Namespace</span></span><br/>                | <span data-ttu-id="368e4-159">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="368e4-159">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="368e4-160">MOF</span><span class="sxs-lookup"><span data-stu-id="368e4-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="368e4-161"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="368e4-161"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="368e4-162">DLL</span><span class="sxs-lookup"><span data-stu-id="368e4-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="368e4-163"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="368e4-163"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="368e4-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="368e4-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="368e4-165">**Disco \_ lógico do Win32**</span><span class="sxs-lookup"><span data-stu-id="368e4-165">**Win32\_LogicalDisk**</span></span>](win32-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="368e4-166">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="368e4-166">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

