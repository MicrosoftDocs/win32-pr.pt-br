---
description: O método retomar classe WMI continua um trabalho de impressão em pausa.
ms.assetid: acfbca2b-19af-4339-bbca-834db50c3d8d
ms.tgt_platform: multiple
title: Método resume da classe Win32_PrintJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrintJob.Resume
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f8ca1602eb29e1e18d83d2e8b79760d13f63e101
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811154"
---
# <a name="resume-method-of-the-win32_printjob-class"></a><span data-ttu-id="f5aaa-103">Método resume da \_ classe PrintJob do Win32</span><span class="sxs-lookup"><span data-stu-id="f5aaa-103">Resume method of the Win32\_PrintJob class</span></span>

<span data-ttu-id="f5aaa-104">O método **retomar** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) continua um trabalho de impressão em pausa.</span><span class="sxs-lookup"><span data-stu-id="f5aaa-104">The **Resume** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method continues a paused print job.</span></span>

<span data-ttu-id="f5aaa-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="f5aaa-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f5aaa-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f5aaa-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f5aaa-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5aaa-107">Syntax</span></span>


```mof
uint32 Resume();
```



## <a name="parameters"></a><span data-ttu-id="f5aaa-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5aaa-108">Parameters</span></span>

<span data-ttu-id="f5aaa-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f5aaa-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f5aaa-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f5aaa-110">Return value</span></span>

<span data-ttu-id="f5aaa-111">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="f5aaa-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="f5aaa-112">**0**</span><span class="sxs-lookup"><span data-stu-id="f5aaa-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="f5aaa-113">Sucesso</span><span class="sxs-lookup"><span data-stu-id="f5aaa-113">Success</span></span>

</dd> <dt>

<span data-ttu-id="f5aaa-114">**5**</span><span class="sxs-lookup"><span data-stu-id="f5aaa-114">**5**</span></span>
</dt> <dd>

<span data-ttu-id="f5aaa-115">Acesso negado</span><span class="sxs-lookup"><span data-stu-id="f5aaa-115">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="f5aaa-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f5aaa-116">Examples</span></span>

<span data-ttu-id="f5aaa-117">O exemplo de código VBScript a seguir retoma todos os trabalhos de impressão em um computador.</span><span class="sxs-lookup"><span data-stu-id="f5aaa-117">The following VBScript code sample resumes all the print jobs on a computer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrintJobs =  objWMIService.ExecQuery _ 
    ("Select * from Win32_PrintJob") 
 
For Each objPrintJob in colPrintJobs  
    objPrintJob.Resume 
Next 
```



## <a name="requirements"></a><span data-ttu-id="f5aaa-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5aaa-118">Requirements</span></span>



| <span data-ttu-id="f5aaa-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5aaa-119">Requirement</span></span> | <span data-ttu-id="f5aaa-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f5aaa-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5aaa-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5aaa-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f5aaa-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5aaa-122">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="f5aaa-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5aaa-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f5aaa-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5aaa-124">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="f5aaa-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="f5aaa-125">Namespace</span></span><br/>                | <span data-ttu-id="f5aaa-126">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f5aaa-126">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="f5aaa-127">MOF</span><span class="sxs-lookup"><span data-stu-id="f5aaa-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5aaa-128"><dt>\_Impressora. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="f5aaa-128"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5aaa-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f5aaa-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5aaa-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5aaa-130"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="f5aaa-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5aaa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5aaa-132">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="f5aaa-132">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="f5aaa-133">**PrintJob do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="f5aaa-133">**Win32\_PrintJob**</span></span>](win32-printjob.md)
</dt> </dl>

 

