---
description: Renomeia uma impressora.
ms.assetid: afbef871-5153-4b9e-9ad3-4d271a497c37
ms.tgt_platform: multiple
title: Método RenamePrinter da classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.RenamePrinter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6066dfd4280f7c43c9804933fb1ed5fb931bfa08
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163902"
---
# <a name="renameprinter-method-of-the-win32_printer-class"></a><span data-ttu-id="d9957-103">Método RenamePrinter da classe de \_ impressora Win32</span><span class="sxs-lookup"><span data-stu-id="d9957-103">RenamePrinter method of the Win32\_Printer class</span></span>

<span data-ttu-id="d9957-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **RenamePrinter** renomeia uma impressora.</span><span class="sxs-lookup"><span data-stu-id="d9957-104">The **RenamePrinter** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames a printer.</span></span>

<span data-ttu-id="d9957-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="d9957-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d9957-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d9957-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d9957-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d9957-107">Syntax</span></span>


```mof
uint32 RenamePrinter(
  [in] string NewPrinterName
);
```



## <a name="parameters"></a><span data-ttu-id="d9957-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9957-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9957-109">*NewPrinterName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d9957-109">*NewPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9957-110">Nome da nova impressora.</span><span class="sxs-lookup"><span data-stu-id="d9957-110">New printer name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9957-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d9957-111">Return value</span></span>

<span data-ttu-id="d9957-112">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="d9957-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="d9957-113">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d9957-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d9957-114">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="d9957-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d9957-115">**0**</span><span class="sxs-lookup"><span data-stu-id="d9957-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="d9957-116">Sucesso</span><span class="sxs-lookup"><span data-stu-id="d9957-116">Success</span></span>

</dd> <dt>

<span data-ttu-id="d9957-117">**5**</span><span class="sxs-lookup"><span data-stu-id="d9957-117">**5**</span></span>
</dt> <dd>

<span data-ttu-id="d9957-118">Acesso negado</span><span class="sxs-lookup"><span data-stu-id="d9957-118">Access Denied</span></span>

</dd> <dt>

<span data-ttu-id="d9957-119">**1801**</span><span class="sxs-lookup"><span data-stu-id="d9957-119">**1801**</span></span>
</dt> <dd>

<span data-ttu-id="d9957-120">Nome de impressora inválido</span><span class="sxs-lookup"><span data-stu-id="d9957-120">Invalid Printer Name</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="d9957-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d9957-121">Examples</span></span>

<span data-ttu-id="d9957-122">O exemplo de VBScript a seguir renomeia uma impressora e seu nome de compartilhamento de impressora.</span><span class="sxs-lookup"><span data-stu-id="d9957-122">The following VBScript example renames both a printer and its printer share name.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where DeviceID = 'HP LaserJet 4Si M'") 
 
For Each objPrinter in colPrinters 
    objPrinter.RenamePrinter("ArtDepartmentPrinter") 
Next 
 
Set colPrinters = objWMIService.ExecQuery _ 
    ("Select * From Win32_Printer Where DeviceID = 'ArtDepartmentPrinter' ") 
 
For Each objPrinter in colPrinters 
    objPrinter.ShareName = "ArtDepartmentPrinter" 
    objPrinter.Put_ 
Next 
```



## <a name="requirements"></a><span data-ttu-id="d9957-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9957-123">Requirements</span></span>



| <span data-ttu-id="d9957-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9957-124">Requirement</span></span> | <span data-ttu-id="d9957-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d9957-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9957-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9957-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d9957-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9957-127">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="d9957-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9957-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d9957-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9957-129">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="d9957-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="d9957-130">Namespace</span></span><br/>                | <span data-ttu-id="d9957-131">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d9957-131">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="d9957-132">MOF</span><span class="sxs-lookup"><span data-stu-id="d9957-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9957-133"><dt>\_Impressora. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="d9957-133"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="d9957-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d9957-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9957-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9957-135"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="d9957-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9957-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9957-137">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="d9957-137">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="d9957-138">**\_Impressora Win32**</span><span class="sxs-lookup"><span data-stu-id="d9957-138">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

