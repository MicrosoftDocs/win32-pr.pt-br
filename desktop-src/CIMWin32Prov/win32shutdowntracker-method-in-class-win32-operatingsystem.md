---
description: O método Win32ShutdownTracker fornece o mesmo conjunto de opções de desligamento com suporte do método Win32Shutdown no sistema \_ operacional Win32, mas também permite que você especifique comentários, um motivo para o desligamento ou um tempo limite.
ms.assetid: 2c5502c9-9ec0-4f9e-b661-1f8015556008
ms.tgt_platform: multiple
title: Método Win32ShutdownTracker da classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32ShutdownTracker
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44c86972d014da906b98ad8d3bd8e98d01f1cfcb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088962"
---
# <a name="win32shutdowntracker-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="3d174-103">Método Win32ShutdownTracker da classe de sistema \_ operacional Win32</span><span class="sxs-lookup"><span data-stu-id="3d174-103">Win32ShutdownTracker method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="3d174-104">O método **Win32ShutdownTracker** fornece o mesmo conjunto de opções de desligamento com suporte do método [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) no sistema [**\_ operacional Win32**](win32-operatingsystem.md), mas também permite que você especifique comentários, um motivo para o desligamento ou um tempo limite.</span><span class="sxs-lookup"><span data-stu-id="3d174-104">The **Win32ShutdownTracker** method provides the same set of shutdown options supported by the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method in [**Win32\_OperatingSystem**](win32-operatingsystem.md), but it also allows you to specify comments, a reason for shutdown, or a timeout.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d174-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3d174-105">Syntax</span></span>


```mof
uint32 Win32ShutdownTracker(
  [in] uint32 Timeout,
  [in] string Comment,
  [in] uint32 ReasonCode,
  [in] sint32 Flags
);
```



## <a name="parameters"></a><span data-ttu-id="3d174-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d174-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d174-107">*Tempo limite* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3d174-107">*Timeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d174-108">Tempo, em segundos, antes de o desligamento ocorrer.</span><span class="sxs-lookup"><span data-stu-id="3d174-108">Time, in seconds, before shutdown takes place.</span></span> <span data-ttu-id="3d174-109">O valor padrão é 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="3d174-109">The default value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="3d174-110">*Comentário* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3d174-110">*Comment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d174-111">Mensagem a ser exibida na caixa de diálogo de desligamento que também é armazenada como um comentário na entrada do log de eventos.</span><span class="sxs-lookup"><span data-stu-id="3d174-111">Message to display in the shutdown dialog box that is also stored as a comment in the event log entry.</span></span>

</dd> <dt>

<span data-ttu-id="3d174-112">*ReasonCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3d174-112">*ReasonCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d174-113">Motivo para iniciar o desligamento.</span><span class="sxs-lookup"><span data-stu-id="3d174-113">Reason for initiating the shutdown.</span></span>

</dd> <dt>

<span data-ttu-id="3d174-114">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="3d174-114">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d174-115">Conjunto de sinalizadores de bitmap para desligar o computador.</span><span class="sxs-lookup"><span data-stu-id="3d174-115">Bitmapped set of flags to shut the computer down.</span></span> <span data-ttu-id="3d174-116">Para forçar um comando, adicione o sinalizador Force (4) ao valor do comando.</span><span class="sxs-lookup"><span data-stu-id="3d174-116">To force a command, add the Force flag (4) to the command value.</span></span> <span data-ttu-id="3d174-117">O uso da força em conjunto com o desligamento ou reinicialização em um computador remoto desliga imediatamente tudo (incluindo WMI, COM e assim por diante) ou reinicia o computador remoto.</span><span class="sxs-lookup"><span data-stu-id="3d174-117">Using Force in conjunction with Shutdown or Reboot on a remote computer immediately shuts down everything (including WMI, COM, and so on), or reboots the remote computer.</span></span> <span data-ttu-id="3d174-118">Isso resulta em um valor de retorno indeterminado.</span><span class="sxs-lookup"><span data-stu-id="3d174-118">This results in an indeterminate return value.</span></span>

<dt>

<span data-ttu-id="3d174-119">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="3d174-119">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="3d174-120">Fazer logoff</span><span class="sxs-lookup"><span data-stu-id="3d174-120">Log Off</span></span>

</dd> <dt>

<span data-ttu-id="3d174-121">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="3d174-121">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="3d174-122">Logoff forçado (0 + 4)</span><span class="sxs-lookup"><span data-stu-id="3d174-122">Forced Log Off (0 + 4)</span></span>

</dd> <dt>

<span data-ttu-id="3d174-123">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="3d174-123">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="3d174-124">Desligar</span><span class="sxs-lookup"><span data-stu-id="3d174-124">Shutdown</span></span>

</dd> <dt>

<span data-ttu-id="3d174-125">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="3d174-125">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="3d174-126">Desligamento forçado (1 + 4)</span><span class="sxs-lookup"><span data-stu-id="3d174-126">Forced Shutdown (1 + 4)</span></span>

</dd> <dt>

<span data-ttu-id="3d174-127">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="3d174-127">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="3d174-128">Reboot</span><span class="sxs-lookup"><span data-stu-id="3d174-128">Reboot</span></span>

</dd> <dt>

<span data-ttu-id="3d174-129">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="3d174-129">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="3d174-130">Reinicialização forçada (2 + 4)</span><span class="sxs-lookup"><span data-stu-id="3d174-130">Forced Reboot (2 + 4)</span></span>

</dd> <dt>

<span data-ttu-id="3d174-131">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="3d174-131">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="3d174-132">Desligar</span><span class="sxs-lookup"><span data-stu-id="3d174-132">Power Off</span></span>

</dd> <dt>

<span data-ttu-id="3d174-133">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="3d174-133">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="3d174-134">Desligamento forçado (8 + 4)</span><span class="sxs-lookup"><span data-stu-id="3d174-134">Forced Power Off (8 + 4)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d174-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3d174-135">Return value</span></span>

<span data-ttu-id="3d174-136">Retorna zero (0) para indicar êxito.</span><span class="sxs-lookup"><span data-stu-id="3d174-136">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="3d174-137">Qualquer outro número indica um erro.</span><span class="sxs-lookup"><span data-stu-id="3d174-137">Any other number indicates an error.</span></span> <span data-ttu-id="3d174-138">Para códigos de erro, consulte [**constantes de erro WMI**](../wmisdk/wmi-error-constants.md) ou [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3d174-138">For error codes, see [**WMI Error Constants**](../wmisdk/wmi-error-constants.md) or [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="3d174-139">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](../debug/system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3d174-139">For general **HRESULT** values, see [System Error Codes](../debug/system-error-codes.md).</span></span>

<dl> <dt>

<span data-ttu-id="3d174-140">**Êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="3d174-140">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3d174-141">**Outro** (1 a 4294967295)</span><span class="sxs-lookup"><span data-stu-id="3d174-141">**Other** (1–4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="3d174-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d174-142">Remarks</span></span>

<span data-ttu-id="3d174-143">O processo de chamada deve ter o privilégio de **\_ \_ nome de desligamento se** .</span><span class="sxs-lookup"><span data-stu-id="3d174-143">The calling process must have the **SE\_SHUTDOWN\_NAME** privilege.</span></span>

## <a name="examples"></a><span data-ttu-id="3d174-144">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3d174-144">Examples</span></span>

<span data-ttu-id="3d174-145">O exemplo de código VBScript a seguir descreve como chamar **Win32ShutdownTracker**.</span><span class="sxs-lookup"><span data-stu-id="3d174-145">The following VBScript code sample describes how to call **Win32ShutdownTracker**.</span></span>


```VB
Set objArgs = Wscript.Arguments 

intTimeOut = objArgs(0) 'Countdown time (in seconds) before action
strComment = objArgs(1) 'Message to display
intFlags = objArgs(2) 'Set of flags to shutdown the computer:
'0 = Logoff, 4 = Forced Logoff (0+4), 1 = Shutdown, 2 = Reboot, 6 = Forced Reboot (2+4), 8 = Power Off, 12 = Forced Power Off (8+4) - 2 (Reboot) 

strComputer = "." 

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate,(Shutdown)}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery ("Select * from Win32_OperatingSystem") 

For Each objOperatingSystem in colOperatingSystems 
objOperatingSystem.Win32ShutdownTracker intTimeOut,strComment,0,intFlags 
Next
```



## <a name="requirements"></a><span data-ttu-id="3d174-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d174-146">Requirements</span></span>



| <span data-ttu-id="3d174-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d174-147">Requirement</span></span> | <span data-ttu-id="3d174-148">Valor</span><span class="sxs-lookup"><span data-stu-id="3d174-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d174-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d174-149">Minimum supported client</span></span><br/> | <span data-ttu-id="3d174-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d174-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3d174-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d174-151">Minimum supported server</span></span><br/> | <span data-ttu-id="3d174-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d174-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3d174-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="3d174-153">Namespace</span></span><br/>                | <span data-ttu-id="3d174-154">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3d174-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3d174-155">MOF</span><span class="sxs-lookup"><span data-stu-id="3d174-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d174-156"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d174-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d174-157">DLL</span><span class="sxs-lookup"><span data-stu-id="3d174-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d174-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d174-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d174-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d174-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d174-160">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="3d174-160">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="3d174-161">**Sistema \_ operacional Win32**</span><span class="sxs-lookup"><span data-stu-id="3d174-161">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="3d174-162">**Win32Shutdown**</span><span class="sxs-lookup"><span data-stu-id="3d174-162">**Win32Shutdown**</span></span>](win32shutdown-method-in-class-win32-operatingsystem.md)
</dt> </dl>

 

 
