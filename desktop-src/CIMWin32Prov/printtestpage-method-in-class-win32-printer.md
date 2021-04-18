---
description: Imprime uma página de teste.
ms.assetid: 7968e637-9817-4111-89f5-d3c6961395e5
ms.tgt_platform: multiple
title: Método PrintTestPage da classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.PrintTestPage
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: abf31237918d533ec43586ddd3d71204f2c8ae21
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752961"
---
# <a name="printtestpage-method-of-the-win32_printer-class"></a><span data-ttu-id="1ca01-103">Método PrintTestPage da classe de \_ impressora Win32</span><span class="sxs-lookup"><span data-stu-id="1ca01-103">PrintTestPage method of the Win32\_Printer class</span></span>

<span data-ttu-id="1ca01-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **PrintTestPage** imprime uma página de teste.</span><span class="sxs-lookup"><span data-stu-id="1ca01-104">The **PrintTestPage** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method prints a test page.</span></span>

<span data-ttu-id="1ca01-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="1ca01-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1ca01-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1ca01-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1ca01-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ca01-107">Syntax</span></span>


```mof
uint32 PrintTestPage();
```



## <a name="parameters"></a><span data-ttu-id="1ca01-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ca01-108">Parameters</span></span>

<span data-ttu-id="1ca01-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1ca01-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1ca01-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ca01-110">Return value</span></span>

<span data-ttu-id="1ca01-111">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="1ca01-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="1ca01-112">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="1ca01-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="1ca01-113">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="1ca01-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="1ca01-114">**0**</span><span class="sxs-lookup"><span data-stu-id="1ca01-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="1ca01-115">Sucesso</span><span class="sxs-lookup"><span data-stu-id="1ca01-115">Success</span></span>

</dd> <dt>

<span data-ttu-id="1ca01-116">**5**</span><span class="sxs-lookup"><span data-stu-id="1ca01-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="1ca01-117">Acesso negado</span><span class="sxs-lookup"><span data-stu-id="1ca01-117">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="1ca01-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1ca01-118">Examples</span></span>

<span data-ttu-id="1ca01-119">O exemplo de código do PowerShell a seguir imprime uma página de teste.</span><span class="sxs-lookup"><span data-stu-id="1ca01-119">The following PowerShell code sample prints a test page.</span></span>


```PowerShell
# Get printer objects from  WMI
$printers=Get-WmiObject Win32_Printer
"{0} Printers defined on this system" -f $printers.count

# Get a specific printer
$printer = $printers | where {$_.name -eq "\\smallguy\HP LaserJet 5M"}

# Display info
"Printer share name: {0}\{1}" -f $printer.servername, $printer.sharename
"Printer Port      : {0}    " -f $printer.PortName
  
# Print a test page
$printer.PrintTestPage()
```



## <a name="requirements"></a><span data-ttu-id="1ca01-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ca01-120">Requirements</span></span>



| <span data-ttu-id="1ca01-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ca01-121">Requirement</span></span> | <span data-ttu-id="1ca01-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1ca01-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ca01-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ca01-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1ca01-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1ca01-124">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="1ca01-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ca01-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1ca01-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ca01-126">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="1ca01-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="1ca01-127">Namespace</span></span><br/>                | <span data-ttu-id="1ca01-128">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1ca01-128">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="1ca01-129">MOF</span><span class="sxs-lookup"><span data-stu-id="1ca01-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ca01-130"><dt>\_Impressora. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="1ca01-130"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ca01-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1ca01-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ca01-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ca01-132"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="1ca01-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ca01-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ca01-134">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="1ca01-134">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="1ca01-135">**\_Impressora Win32**</span><span class="sxs-lookup"><span data-stu-id="1ca01-135">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

