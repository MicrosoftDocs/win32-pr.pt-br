---
description: Agenda o Autochk a ser executado na unidade de disco representada pelo LogicalDisk do Win32 \_ na próxima reinicialização se o bit sujo estiver definido.
ms.assetid: 34f4c26b-6bfb-45d9-9d6c-0a9b735355f3
ms.tgt_platform: multiple
title: Método ScheduleAutoChk da classe Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ScheduleAutoChk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2707810d919c119aff35f2313e9aa5218f7948f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920248"
---
# <a name="scheduleautochk-method-of-the-win32_logicaldisk-class"></a><span data-ttu-id="5648d-103">Método ScheduleAutoChk da classe do \_ LogicalDisk do Win32</span><span class="sxs-lookup"><span data-stu-id="5648d-103">ScheduleAutoChk method of the Win32\_LogicalDisk class</span></span>

<span data-ttu-id="5648d-104">O método de classe **ScheduleAutoChk** agenda o Autochk para ser executado na unidade de disco representada [**pelo \_ LogicalDisk do Win32**](win32-logicaldisk.md) na próxima reinicialização se o bit sujo estiver definido.</span><span class="sxs-lookup"><span data-stu-id="5648d-104">The **ScheduleAutoChk** class method schedules Autochk to be run on the disk drive represented by the [**Win32\_LogicalDisk**](win32-logicaldisk.md) at the next reboot if the dirty bit is set.</span></span>

<span data-ttu-id="5648d-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="5648d-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5648d-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5648d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5648d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5648d-107">Syntax</span></span>


```mof
uint32 ScheduleAutoChk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a><span data-ttu-id="5648d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5648d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5648d-109">*LogicalDisk* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5648d-109">*LogicalDisk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5648d-110">Especifica a lista de unidades a serem agendadas para autochk na próxima reinicialização.</span><span class="sxs-lookup"><span data-stu-id="5648d-110">Specifies the list of drives to schedule for Autochk at the next reboot.</span></span> <span data-ttu-id="5648d-111">A sintaxe da cadeia de caracteres consiste na letra da unidade seguida por dois-pontos para o disco lógico, por exemplo: "C:"</span><span class="sxs-lookup"><span data-stu-id="5648d-111">The string syntax consists of the drive letter followed by a colon for the logical disk, for example: "C:"</span></span>

> [!Note]  
> <span data-ttu-id="5648d-112">Sempre verifique a validade das letras da unidade na matriz do *LogicalDisk* quando os dados vierem de uma fonte desconhecida ou uma fonte na qual você não confia.</span><span class="sxs-lookup"><span data-stu-id="5648d-112">Always check the validity of the drive letters in the *LogicalDisk* array when the data comes from an unknown source, or a source that you do not trust.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5648d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5648d-113">Return value</span></span>

<span data-ttu-id="5648d-114">Retorna um valor de 0 (zero) se for bem-sucedido e algum outro valor se ocorrer qualquer outro erro.</span><span class="sxs-lookup"><span data-stu-id="5648d-114">Returns a value of 0 (zero) if successful, and some other value if any other error occurs.</span></span> <span data-ttu-id="5648d-115">Os valores são listados na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="5648d-115">Values are listed in the following list.</span></span> <span data-ttu-id="5648d-116">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="5648d-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="5648d-117">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="5648d-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="5648d-118">**Sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="5648d-118">**No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5648d-119">**Erro-unidade remota** (1)</span><span class="sxs-lookup"><span data-stu-id="5648d-119">**Error - Remote Drive** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5648d-120">**Erro-unidade removível** (2)</span><span class="sxs-lookup"><span data-stu-id="5648d-120">**Error - Removable Drive** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5648d-121">**Erro-unidade não diretório raiz** (3)</span><span class="sxs-lookup"><span data-stu-id="5648d-121">**Error - Drive Not Root Directory** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5648d-122">**Erro-unidade desconhecida** (4)</span><span class="sxs-lookup"><span data-stu-id="5648d-122">**Error - Unknown Drive** (4)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="5648d-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="5648d-123">Remarks</span></span>

<span data-ttu-id="5648d-124">Esse método só é aplicável a essas instâncias de disco lógico que representam um disco físico no computador.</span><span class="sxs-lookup"><span data-stu-id="5648d-124">This method is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="5648d-125">Esse método não é aplicável a unidades lógicas mapeadas.</span><span class="sxs-lookup"><span data-stu-id="5648d-125">This method is not applicable to mapped logical drives.</span></span>

## <a name="examples"></a><span data-ttu-id="5648d-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5648d-126">Examples</span></span>

<span data-ttu-id="5648d-127">Os exemplos do VBScript e do PowerShell a seguir agendam Autochk.exe para serem executados na unidade C na próxima vez em que o computador for reinicializado.</span><span class="sxs-lookup"><span data-stu-id="5648d-127">The following VBScript and PowerShell samples schedule Autochk.exe to run against drive C the next time the computer reboots.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ScheduleAutoChk(Array("C:")) 
```


```PowerShell

Invoke-WmiMethod -path win32_logicaldisk -Name ScheduleAutoChk -ArgumentList @(&quot;C:&quot;)
```





## <a name="requirements"></a><span data-ttu-id="5648d-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5648d-128">Requirements</span></span>



| <span data-ttu-id="5648d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5648d-129">Requirement</span></span> | <span data-ttu-id="5648d-130">Valor</span><span class="sxs-lookup"><span data-stu-id="5648d-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5648d-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5648d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5648d-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5648d-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5648d-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5648d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5648d-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5648d-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5648d-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="5648d-135">Namespace</span></span><br/>                | <span data-ttu-id="5648d-136">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5648d-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5648d-137">MOF</span><span class="sxs-lookup"><span data-stu-id="5648d-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5648d-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5648d-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5648d-139">DLL</span><span class="sxs-lookup"><span data-stu-id="5648d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5648d-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5648d-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5648d-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="5648d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5648d-142">**Disco \_ lógico do Win32**</span><span class="sxs-lookup"><span data-stu-id="5648d-142">**Win32\_LogicalDisk**</span></span>](win32-logicaldisk.md)
</dt> </dl>

 

