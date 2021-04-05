---
description: Fornece uma conexão com uma impressora existente na rede e a adiciona à lista de impressoras disponíveis.
ms.assetid: 44149051-4abf-4428-8999-355dd0b0ce69
ms.tgt_platform: multiple
title: Método AddPrinterConnection da classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.AddPrinterConnection
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2ad9e225a60e33fdf51d5f677dd4342acd148b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826216"
---
# <a name="addprinterconnection-method-of-the-win32_printer-class"></a><span data-ttu-id="3b2cc-103">Método AddPrinterConnection da classe de \_ impressora Win32</span><span class="sxs-lookup"><span data-stu-id="3b2cc-103">AddPrinterConnection method of the Win32\_Printer class</span></span>

<span data-ttu-id="3b2cc-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **AddPrinterConnection** fornece uma conexão a uma impressora existente na rede e a adiciona à lista de impressoras disponíveis.</span><span class="sxs-lookup"><span data-stu-id="3b2cc-104">The **AddPrinterConnection** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method provides a connection to an existing printer on the network, and adds it to the list of available printers.</span></span>

<span data-ttu-id="3b2cc-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="3b2cc-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3b2cc-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3b2cc-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3b2cc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b2cc-107">Syntax</span></span>


```mof
uint32 AddPrinterConnection(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="3b2cc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b2cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b2cc-109">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="3b2cc-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b2cc-110">Nome amigável da impressora.</span><span class="sxs-lookup"><span data-stu-id="3b2cc-110">Friendly name for the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b2cc-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3b2cc-111">Return value</span></span>

<span data-ttu-id="3b2cc-112">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="3b2cc-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="3b2cc-113">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3b2cc-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="3b2cc-114">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="3b2cc-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="3b2cc-115">**0**</span><span class="sxs-lookup"><span data-stu-id="3b2cc-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="3b2cc-116">Sucesso</span><span class="sxs-lookup"><span data-stu-id="3b2cc-116">Success</span></span>

</dd> <dt>

<span data-ttu-id="3b2cc-117">**5**</span><span class="sxs-lookup"><span data-stu-id="3b2cc-117">**5**</span></span>
</dt> <dd>

<span data-ttu-id="3b2cc-118">Acesso negado</span><span class="sxs-lookup"><span data-stu-id="3b2cc-118">Access Denied</span></span>

</dd> <dt>

<span data-ttu-id="3b2cc-119">**1801**</span><span class="sxs-lookup"><span data-stu-id="3b2cc-119">**1801**</span></span>
</dt> <dd>

<span data-ttu-id="3b2cc-120">Nome de impressora inválido</span><span class="sxs-lookup"><span data-stu-id="3b2cc-120">Invalid Printer Name</span></span>

</dd> <dt>

<span data-ttu-id="3b2cc-121">**1930**</span><span class="sxs-lookup"><span data-stu-id="3b2cc-121">**1930**</span></span>
</dt> <dd>

<span data-ttu-id="3b2cc-122">Driver de impressora incompatível</span><span class="sxs-lookup"><span data-stu-id="3b2cc-122">Incompatible Printer Driver</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="3b2cc-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3b2cc-123">Examples</span></span>

<span data-ttu-id="3b2cc-124">O exemplo do PowerShell [Add-PrinterDriver](https://Gallery.TechNet.Microsoft.Com/1c8f4c0d-9439-4af0-8840-59686d9b4bc1) instala todos os drivers de impressora de um servidor de impressão especificado.</span><span class="sxs-lookup"><span data-stu-id="3b2cc-124">The [Add-PrinterDriver](https://Gallery.TechNet.Microsoft.Com/1c8f4c0d-9439-4af0-8840-59686d9b4bc1) PowerShell sample installs all printer drivers from a specified print server.</span></span>

<span data-ttu-id="3b2cc-125">O [ListSharedPrintersAddPrintConnection.ps1](https://Gallery.TechNet.Microsoft.Com/b7f74333-e78b-49d8-b23a-f1307d5b1ee6) exemplo do PowerShell lista impressoras compartilhadas em um computador remoto e oferece a você a capacidade de adicionar uma conexão de impressora do computador remoto ao seu.</span><span class="sxs-lookup"><span data-stu-id="3b2cc-125">The [ListSharedPrintersAddPrintConnection.ps1](https://Gallery.TechNet.Microsoft.Com/b7f74333-e78b-49d8-b23a-f1307d5b1ee6) PowerShell sample lists shared printers on a remote comptuer, and gives you the ability to add a printer connection from the remote computer to your computer.</span></span>

<span data-ttu-id="3b2cc-126">O exemplo de código VBScript a seguir adiciona uma impressora local.</span><span class="sxs-lookup"><span data-stu-id="3b2cc-126">The following VBScript code sample adds a local printer.</span></span>


```VB
Dim strPrinterName as String = "Isidoros Printer"
Dim strComputer AsString = My.Computer.Name
Dim objWMIService, objPrinter AsObject
objWMIService = GetObject(
"winmgmts:" _

& 
"{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

objPrinter = objWMIService.Get(
"Win32_Printer").SpawnInstance_
objPrinter.Name = strPrinterName
objPrinter.DriverName = "Generic / Text Only"
objPrinter.PortName = 
"c:\temp\file.prn"
objPrinter.DeviceID = strPrinterName
'objPrinter.Location = "Athens, Greece"
objPrinter.Network = 
False
objPrinter.Shared = 
False'objPrinter.ShareName = "MyShareName"
objPrinter.Put_()
```



## <a name="requirements"></a><span data-ttu-id="3b2cc-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b2cc-127">Requirements</span></span>



| <span data-ttu-id="3b2cc-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b2cc-128">Requirement</span></span> | <span data-ttu-id="3b2cc-129">Valor</span><span class="sxs-lookup"><span data-stu-id="3b2cc-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b2cc-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b2cc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3b2cc-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b2cc-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="3b2cc-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b2cc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3b2cc-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b2cc-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="3b2cc-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="3b2cc-134">Namespace</span></span><br/>                | <span data-ttu-id="3b2cc-135">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3b2cc-135">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="3b2cc-136">MOF</span><span class="sxs-lookup"><span data-stu-id="3b2cc-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b2cc-137"><dt>\_Impressora. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="3b2cc-137"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b2cc-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3b2cc-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b2cc-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b2cc-139"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="3b2cc-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b2cc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b2cc-141">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="3b2cc-141">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="3b2cc-142">Tarefas do WMI: impressoras e impressão</span><span class="sxs-lookup"><span data-stu-id="3b2cc-142">WMI Tasks: Printers and Printing</span></span>](/windows/desktop/WmiSdk/wmi-tasks--printers-and-printing)
</dt> <dt>

[<span data-ttu-id="3b2cc-143">**\_Impressora Win32**</span><span class="sxs-lookup"><span data-stu-id="3b2cc-143">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

