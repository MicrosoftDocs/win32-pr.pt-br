---
description: O método de classe WMI SetDefaultPrinter define a impressora padrão do sistema para o usuário que está chamando o método.
ms.assetid: 7e896961-363d-4b8b-9d22-bbfc9681e97b
ms.tgt_platform: multiple
title: Método SetDefaultPrinter da classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.SetDefaultPrinter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a18c6d7771eb0e95d86142f41262d721509eb6f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826699"
---
# <a name="setdefaultprinter-method-of-the-win32_printer-class"></a><span data-ttu-id="7a072-103">Método SetDefaultPrinter da classe de \_ impressora Win32</span><span class="sxs-lookup"><span data-stu-id="7a072-103">SetDefaultPrinter method of the Win32\_Printer class</span></span>

<span data-ttu-id="7a072-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDefaultPrinter** define a impressora padrão do sistema para o usuário que está chamando o método.</span><span class="sxs-lookup"><span data-stu-id="7a072-104">The **SetDefaultPrinter** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the default system printer for the user calling the method.</span></span>

<span data-ttu-id="7a072-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="7a072-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7a072-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7a072-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7a072-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a072-107">Syntax</span></span>


```mof
uint32 SetDefaultPrinter();
```



## <a name="parameters"></a><span data-ttu-id="7a072-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a072-108">Parameters</span></span>

<span data-ttu-id="7a072-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7a072-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7a072-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7a072-110">Return value</span></span>

<span data-ttu-id="7a072-111">Retorna 0 (zero) se for bem-sucedido e algum outro valor se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="7a072-111">Returns 0 (zero) if successful, and some other value if an error occurs.</span></span> <span data-ttu-id="7a072-112">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="7a072-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="7a072-113">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="7a072-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

## <a name="examples"></a><span data-ttu-id="7a072-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7a072-114">Examples</span></span>

<span data-ttu-id="7a072-115">O exemplo [instalar uma porta de impressora TCP/IP e uma impressora](https://Gallery.TechNet.Microsoft.Com/41a4c996-b7f7-4d58-808d-2acac20ddbf7) VBScript instala uma porta de impressora TCP/IP, instala uma impressora e, em seguida, define a impressora como padrão.</span><span class="sxs-lookup"><span data-stu-id="7a072-115">The [Install a TCP/IP Printer Port and Printer](https://Gallery.TechNet.Microsoft.Com/41a4c996-b7f7-4d58-808d-2acac20ddbf7) VBScript sample installs a TCP/IP printer port, installs a printer, and then sets the printer to be default.</span></span>

<span data-ttu-id="7a072-116">O exemplo de código VBScript a seguir define a impressora padrão em um computador.</span><span class="sxs-lookup"><span data-stu-id="7a072-116">The following VBScript code sample sets the default printer on a computer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where Name = 'ScriptedPrinter'") 
 
For Each objPrinter in colInstalledPrinters 
    objPrinter.SetDefaultPrinter() 
Next 
```



## <a name="requirements"></a><span data-ttu-id="7a072-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a072-117">Requirements</span></span>



| <span data-ttu-id="7a072-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a072-118">Requirement</span></span> | <span data-ttu-id="7a072-119">Valor</span><span class="sxs-lookup"><span data-stu-id="7a072-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a072-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a072-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7a072-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a072-121">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="7a072-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a072-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7a072-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a072-123">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="7a072-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="7a072-124">Namespace</span></span><br/>                | <span data-ttu-id="7a072-125">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7a072-125">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="7a072-126">MOF</span><span class="sxs-lookup"><span data-stu-id="7a072-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a072-127"><dt>\_Impressora. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="7a072-127"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a072-128">DLL</span><span class="sxs-lookup"><span data-stu-id="7a072-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a072-129"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a072-129"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="7a072-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a072-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a072-131">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="7a072-131">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="7a072-132">Tarefas do WMI: impressoras e impressão</span><span class="sxs-lookup"><span data-stu-id="7a072-132">WMI Tasks: Printers and Printing</span></span>](/windows/desktop/WmiSdk/wmi-tasks--printers-and-printing)
</dt> <dt>

[<span data-ttu-id="7a072-133">**\_Impressora Win32**</span><span class="sxs-lookup"><span data-stu-id="7a072-133">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

