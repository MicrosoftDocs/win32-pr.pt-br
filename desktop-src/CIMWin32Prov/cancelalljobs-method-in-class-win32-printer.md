---
description: Remove todos os trabalhos, incluindo o que está imprimindo na fila no momento.
ms.assetid: d7466513-b123-43af-ab17-b3213ba80284
ms.tgt_platform: multiple
title: Método CancelAllJobs da classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.CancelAllJobs
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d2d816dab837aafd7b6e9c6beff75c4e62b19b2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826213"
---
# <a name="cancelalljobs-method-of-the-win32_printer-class"></a><span data-ttu-id="d6028-103">Método CancelAllJobs da classe de \_ impressora Win32</span><span class="sxs-lookup"><span data-stu-id="d6028-103">CancelAllJobs method of the Win32\_Printer class</span></span>

<span data-ttu-id="d6028-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CancelAllJobs** remove todos os trabalhos, incluindo o que atualmente está imprimindo da fila.</span><span class="sxs-lookup"><span data-stu-id="d6028-104">The **CancelAllJobs** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method removes all jobs, including the one currently printing from the queue.</span></span>

<span data-ttu-id="d6028-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="d6028-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d6028-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d6028-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d6028-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6028-107">Syntax</span></span>


```mof
uint32 CancelAllJobs();
```



## <a name="parameters"></a><span data-ttu-id="d6028-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6028-108">Parameters</span></span>

<span data-ttu-id="d6028-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d6028-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d6028-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d6028-110">Return value</span></span>

<span data-ttu-id="d6028-111">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="d6028-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="d6028-112">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d6028-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d6028-113">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="d6028-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d6028-114">**0**</span><span class="sxs-lookup"><span data-stu-id="d6028-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="d6028-115">Sucesso</span><span class="sxs-lookup"><span data-stu-id="d6028-115">Success</span></span>

</dd> <dt>

<span data-ttu-id="d6028-116">**5**</span><span class="sxs-lookup"><span data-stu-id="d6028-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="d6028-117">Acesso negado</span><span class="sxs-lookup"><span data-stu-id="d6028-117">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="d6028-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d6028-118">Examples</span></span>

<span data-ttu-id="d6028-119">O [notificar os usuários quando uma fila de impressão é limpa](https://Gallery.TechNet.Microsoft.Com/9f8ad84e-239d-45bf-a14f-ad8f3fc4988a) usa Msg.exe para enviar um alerta de rede a qualquer usuário que tenha documentos em uma fila de impressão prestes a ser limpo.</span><span class="sxs-lookup"><span data-stu-id="d6028-119">The [Notify Users When a Print Queue is Purged](https://Gallery.TechNet.Microsoft.Com/9f8ad84e-239d-45bf-a14f-ad8f3fc4988a) uses Msg.exe to send a network alert to any users who had documents in a print queue about to be purged.</span></span> <span data-ttu-id="d6028-120">Depois de enviar os alertas, o script limpa a fila de impressão.</span><span class="sxs-lookup"><span data-stu-id="d6028-120">After sending the alerts, the script purges the print queue.</span></span>

<span data-ttu-id="d6028-121">O exemplo de código [excluir todos os trabalhos de impressão](https://Gallery.TechNet.Microsoft.Com/0e89fa7c-a837-4607-b421-c870142e7323) do VBScript exclui todos os trabalhos de impressão no computador local.</span><span class="sxs-lookup"><span data-stu-id="d6028-121">The [Delete all print jobs](https://Gallery.TechNet.Microsoft.Com/0e89fa7c-a837-4607-b421-c870142e7323) VBScript code sample deletes all print jobs on the local computer.</span></span>

<span data-ttu-id="d6028-122">O exemplo de VBScript a seguir exclui todos os trabalhos de impressão de uma impressora chamada HP QuietJet.</span><span class="sxs-lookup"><span data-stu-id="d6028-122">The following VBScript sample deletes all the print jobs for a printer named HP QuietJet.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where Name = 'HP QuietJet'") 
 
For Each objPrinter in colInstalledPrinters 
    objPrinter.CancelAllJobs() 
Next 
```



## <a name="requirements"></a><span data-ttu-id="d6028-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6028-123">Requirements</span></span>



| <span data-ttu-id="d6028-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6028-124">Requirement</span></span> | <span data-ttu-id="d6028-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d6028-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6028-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6028-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d6028-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6028-127">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="d6028-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6028-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d6028-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6028-129">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="d6028-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="d6028-130">Namespace</span></span><br/>                | <span data-ttu-id="d6028-131">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d6028-131">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="d6028-132">MOF</span><span class="sxs-lookup"><span data-stu-id="d6028-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6028-133"><dt>\_Impressora. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="d6028-133"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6028-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d6028-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6028-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6028-135"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="d6028-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6028-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6028-137">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="d6028-137">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="d6028-138">**\_Impressora Win32**</span><span class="sxs-lookup"><span data-stu-id="d6028-138">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

