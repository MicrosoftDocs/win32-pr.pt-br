---
description: O método pause WMI da classe suspende um trabalho de impressão.
ms.assetid: f1e3906f-1ca2-45c0-9863-5762e4e2119a
ms.tgt_platform: multiple
title: Método Pause da classe Win32_PrintJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrintJob.Pause
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 785ba54b56c65fd298b6ef763ec2d7eca0d8f61a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826704"
---
# <a name="pause-method-of-the-win32_printjob-class"></a><span data-ttu-id="be0e6-103">Método Pause da \_ classe PrintJob do Win32</span><span class="sxs-lookup"><span data-stu-id="be0e6-103">Pause method of the Win32\_PrintJob class</span></span>

<span data-ttu-id="be0e6-104">O método **Pause** [WMI da classe](/windows/desktop/WmiSdk/retrieving-a-class) suspende um trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="be0e6-104">The **Pause** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method suspends a print job.</span></span>

<span data-ttu-id="be0e6-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="be0e6-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="be0e6-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="be0e6-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="be0e6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be0e6-107">Syntax</span></span>


```mof
uint32 Pause();
```



## <a name="parameters"></a><span data-ttu-id="be0e6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be0e6-108">Parameters</span></span>

<span data-ttu-id="be0e6-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="be0e6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="be0e6-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="be0e6-110">Return value</span></span>

<span data-ttu-id="be0e6-111">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="be0e6-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="be0e6-112">**0**</span><span class="sxs-lookup"><span data-stu-id="be0e6-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="be0e6-113">Sucesso</span><span class="sxs-lookup"><span data-stu-id="be0e6-113">Success</span></span>

</dd> <dt>

<span data-ttu-id="be0e6-114">**5**</span><span class="sxs-lookup"><span data-stu-id="be0e6-114">**5**</span></span>
</dt> <dd>

<span data-ttu-id="be0e6-115">Acesso negado</span><span class="sxs-lookup"><span data-stu-id="be0e6-115">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="be0e6-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="be0e6-116">Examples</span></span>

<span data-ttu-id="be0e6-117">O exemplo de código [Pausar todas as impressoras com filas de impressão vazias](https://Gallery.TechNet.Microsoft.Com/cf2b6b61-8ffe-444b-857b-e3a205bc693c) do VBScript pausa as impressoras que não têm trabalhos de impressão pendentes.</span><span class="sxs-lookup"><span data-stu-id="be0e6-117">The [Pause All Printers with Empty Print Queues](https://Gallery.TechNet.Microsoft.Com/cf2b6b61-8ffe-444b-857b-e3a205bc693c) VBScript code sample pauses any printers that have no pending print jobs.</span></span>

<span data-ttu-id="be0e6-118">O exemplo de código VBScript a seguir pausa todos os trabalhos de impressão em um servidor de impressão.</span><span class="sxs-lookup"><span data-stu-id="be0e6-118">The following VBScript code sample pauses all the print jobs on a print server.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrintJobs =  objWMIService.ExecQuery _ 
    ("Select * from Win32_PrintJob") 
 
For Each objPrintJob in colPrintJobs  
    objPrintJob.Pause 
Next 
```



## <a name="requirements"></a><span data-ttu-id="be0e6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be0e6-119">Requirements</span></span>



| <span data-ttu-id="be0e6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="be0e6-120">Requirement</span></span> | <span data-ttu-id="be0e6-121">Valor</span><span class="sxs-lookup"><span data-stu-id="be0e6-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="be0e6-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be0e6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="be0e6-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be0e6-123">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="be0e6-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be0e6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="be0e6-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be0e6-125">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="be0e6-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="be0e6-126">Namespace</span></span><br/>                | <span data-ttu-id="be0e6-127">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="be0e6-127">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="be0e6-128">MOF</span><span class="sxs-lookup"><span data-stu-id="be0e6-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be0e6-129"><dt>\_Impressora. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="be0e6-129"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="be0e6-130">DLL</span><span class="sxs-lookup"><span data-stu-id="be0e6-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be0e6-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be0e6-131"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="be0e6-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="be0e6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be0e6-133">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="be0e6-133">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="be0e6-134">**PrintJob do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="be0e6-134">**Win32\_PrintJob**</span></span>](win32-printjob.md)
</dt> </dl>

 

