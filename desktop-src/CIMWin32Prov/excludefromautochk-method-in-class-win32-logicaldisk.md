---
description: Exclui os discos da operação de Autochk a serem executados na próxima reinicialização.
ms.assetid: 5df2bc3b-e149-4853-aa02-af4cb8af6da0
ms.tgt_platform: multiple
title: Método ExcludeFromAutochk da classe Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ExcludeFromAutochk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c41d93111742e975490d97169c7e9147ba5fb1ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755842"
---
# <a name="excludefromautochk-method-of-the-win32_logicaldisk-class"></a><span data-ttu-id="ed3d9-103">Método ExcludeFromAutochk da classe do \_ LogicalDisk do Win32</span><span class="sxs-lookup"><span data-stu-id="ed3d9-103">ExcludeFromAutochk method of the Win32\_LogicalDisk class</span></span>

<span data-ttu-id="ed3d9-104">O método **ExcludeFromAutochk** exclui discos da operação de **autochk** a serem executados na próxima reinicialização.</span><span class="sxs-lookup"><span data-stu-id="ed3d9-104">The **ExcludeFromAutochk** method excludes disks from the **autochk** operation to be run at the next reboot.</span></span>

<span data-ttu-id="ed3d9-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="ed3d9-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ed3d9-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ed3d9-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ed3d9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed3d9-107">Syntax</span></span>


```mof
uint32 ExcludeFromAutochk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a><span data-ttu-id="ed3d9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed3d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed3d9-109">*LogicalDisk* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ed3d9-109">*LogicalDisk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed3d9-110">Lista de unidades que devem ser excluídas do **autochk** na próxima reinicialização.</span><span class="sxs-lookup"><span data-stu-id="ed3d9-110">List of drives that should be excluded from **autochk** at the next reboot.</span></span> <span data-ttu-id="ed3d9-111">A sintaxe da cadeia de caracteres consiste na letra da unidade seguida por dois-pontos para o disco lógico.</span><span class="sxs-lookup"><span data-stu-id="ed3d9-111">The string syntax consists of the drive letter followed by a colon for the logical disk.</span></span>

<span data-ttu-id="ed3d9-112">Exemplo: "C:"</span><span class="sxs-lookup"><span data-stu-id="ed3d9-112">Example: "C:"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed3d9-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ed3d9-113">Return value</span></span>

<span data-ttu-id="ed3d9-114">Retorna um valor de 0 (zero) quando não ocorre nenhum erro.</span><span class="sxs-lookup"><span data-stu-id="ed3d9-114">Returns a value of 0 (zero) when no error occurs.</span></span> <span data-ttu-id="ed3d9-115">Os valores são listados na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="ed3d9-115">Values are listed in the following list.</span></span> <span data-ttu-id="ed3d9-116">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ed3d9-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ed3d9-117">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ed3d9-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ed3d9-118">**Êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="ed3d9-118">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ed3d9-119">**Erro-unidade remota** (1)</span><span class="sxs-lookup"><span data-stu-id="ed3d9-119">**Error - Remote Drive** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ed3d9-120">**Erro-unidade removível** (2)</span><span class="sxs-lookup"><span data-stu-id="ed3d9-120">**Error - Removable Drive** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ed3d9-121">**Erro-unidade não diretório raiz** (3)</span><span class="sxs-lookup"><span data-stu-id="ed3d9-121">**Error - Drive Not Root Directory** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ed3d9-122">**Erro-unidade desconhecida** (4)</span><span class="sxs-lookup"><span data-stu-id="ed3d9-122">**Error - Unknown Drive** (4)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="ed3d9-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed3d9-123">Remarks</span></span>

<span data-ttu-id="ed3d9-124">Se não for excluído, o **autochk** será executado no disco quando o bit sujo for definido para o disco.</span><span class="sxs-lookup"><span data-stu-id="ed3d9-124">If not excluded, **autochk** is performed on the disk when the dirty bit is set for the disk.</span></span> <span data-ttu-id="ed3d9-125">Observe que as chamadas para excluir discos não são cumulativas.</span><span class="sxs-lookup"><span data-stu-id="ed3d9-125">Note that the calls to exclude disks are not cumulative.</span></span> <span data-ttu-id="ed3d9-126">Se for feita uma chamada para excluir alguns discos, a nova lista não será adicionada à lista de discos que já estão marcados para exclusão.</span><span class="sxs-lookup"><span data-stu-id="ed3d9-126">If a call is made to exclude some disks, then the new list is not added to the list of disks that are already marked for exclusion.</span></span> <span data-ttu-id="ed3d9-127">A nova lista de discos substitui a lista anterior.</span><span class="sxs-lookup"><span data-stu-id="ed3d9-127">The new list of disks overwrites the previous list.</span></span> <span data-ttu-id="ed3d9-128">Esse método só é aplicável a essas instâncias de disco lógico que representam um disco físico no computador.</span><span class="sxs-lookup"><span data-stu-id="ed3d9-128">This method is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="ed3d9-129">Ele não é aplicável a unidades lógicas mapeadas.</span><span class="sxs-lookup"><span data-stu-id="ed3d9-129">It is not applicable to mapped logical drives.</span></span>

## <a name="examples"></a><span data-ttu-id="ed3d9-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ed3d9-130">Examples</span></span>

<span data-ttu-id="ed3d9-131">O exemplo de código VBScript a seguir garante que o Autochk.exe não será executado na unidade C na próxima vez em que o computador for reinicializado, mesmo que o "bit sujo" tenha sido definido na unidade C.</span><span class="sxs-lookup"><span data-stu-id="ed3d9-131">The following VBScript code sample ensures that Autochk.exe will not run against drive C the next time the computer reboots, even if the "dirty bit" has been set on drive C.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ExcludeFromAutoChk(Array("C:")) 
```



## <a name="requirements"></a><span data-ttu-id="ed3d9-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed3d9-132">Requirements</span></span>



| <span data-ttu-id="ed3d9-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed3d9-133">Requirement</span></span> | <span data-ttu-id="ed3d9-134">Valor</span><span class="sxs-lookup"><span data-stu-id="ed3d9-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed3d9-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed3d9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ed3d9-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ed3d9-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ed3d9-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed3d9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ed3d9-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed3d9-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ed3d9-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="ed3d9-139">Namespace</span></span><br/>                | <span data-ttu-id="ed3d9-140">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ed3d9-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ed3d9-141">MOF</span><span class="sxs-lookup"><span data-stu-id="ed3d9-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed3d9-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed3d9-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed3d9-143">DLL</span><span class="sxs-lookup"><span data-stu-id="ed3d9-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed3d9-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed3d9-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed3d9-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed3d9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed3d9-146">**Disco \_ lógico do Win32**</span><span class="sxs-lookup"><span data-stu-id="ed3d9-146">**Win32\_LogicalDisk**</span></span>](win32-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="ed3d9-147">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="ed3d9-147">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

