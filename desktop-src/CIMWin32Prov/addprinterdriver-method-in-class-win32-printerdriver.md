---
description: Cria um novo driver de impressora.
ms.assetid: 23d9ec50-235a-4bf8-ab6b-be3509c3869f
ms.tgt_platform: multiple
title: Método AddPrinterDriver da classe Win32_PrinterDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.AddPrinterDriver
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 03c029d7689743150235d20b0658cd154ef64a4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370374"
---
# <a name="addprinterdriver-method-of-the-win32_printerdriver-class"></a><span data-ttu-id="618e1-103">Método AddPrinterDriver da classe Win32 \_ PrinterDriver</span><span class="sxs-lookup"><span data-stu-id="618e1-103">AddPrinterDriver method of the Win32\_PrinterDriver class</span></span>

<span data-ttu-id="618e1-104">O método da classe **AddPrinterDriver** cria um novo driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="618e1-104">The **AddPrinterDriver** class method creates a new printer driver.</span></span>

<span data-ttu-id="618e1-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="618e1-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="618e1-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="618e1-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="618e1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="618e1-107">Syntax</span></span>


```mof
uint32 AddPrinterDriver(
  [in] Win32_PrinterDriver DriverInfo
);
```



## <a name="parameters"></a><span data-ttu-id="618e1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="618e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="618e1-109">*DriverInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="618e1-109">*DriverInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="618e1-110">Uma instância da classe [**Win32 \_ PrinterDriver**](win32-printerdriver.md) que representa o driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="618e1-110">An instance of the [**Win32\_PrinterDriver**](win32-printerdriver.md) class that represents the printer driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="618e1-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="618e1-111">Return value</span></span>

<span data-ttu-id="618e1-112">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="618e1-112">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="618e1-113">Para valores diferentes daqueles listados na lista a seguir, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants).</span><span class="sxs-lookup"><span data-stu-id="618e1-113">For values different from those listed in the following list, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants).</span></span>

<dl> <dt>

<span data-ttu-id="618e1-114">**0**</span><span class="sxs-lookup"><span data-stu-id="618e1-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="618e1-115">Êxito.</span><span class="sxs-lookup"><span data-stu-id="618e1-115">Success.</span></span>

</dd> <dt>

<span data-ttu-id="618e1-116">**5**</span><span class="sxs-lookup"><span data-stu-id="618e1-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="618e1-117">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="618e1-117">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="618e1-118">**87**</span><span class="sxs-lookup"><span data-stu-id="618e1-118">**87**</span></span>
</dt> <dd>

<span data-ttu-id="618e1-119">O parâmetro está incorreto.</span><span class="sxs-lookup"><span data-stu-id="618e1-119">The parameter is incorrect.</span></span> <span data-ttu-id="618e1-120">Pode ocorrer quando o objeto não está preenchido corretamente ou quando o driver não pode ser encontrado no sistema.</span><span class="sxs-lookup"><span data-stu-id="618e1-120">May occur when the object is not correctly filled or when driver can not be found in the system.</span></span> <span data-ttu-id="618e1-121">Como alternativa, o atributo de nome pode ser diferente do modelo especificado no arquivo. inf.</span><span class="sxs-lookup"><span data-stu-id="618e1-121">Alternately, the name attribute may be different than the model specified in the .inf file.</span></span> <span data-ttu-id="618e1-122">Ou, pode haver uma barra invertida ausente (" \\ ") em um atributo Pathfile.</span><span class="sxs-lookup"><span data-stu-id="618e1-122">Or, there may be a missing backslash ("\\") on a PathFile attribute.</span></span>

</dd> <dt>

<span data-ttu-id="618e1-123">**1797**</span><span class="sxs-lookup"><span data-stu-id="618e1-123">**1797**</span></span>
</dt> <dd>

<span data-ttu-id="618e1-124">O driver de impressora é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="618e1-124">The printer driver is unknown.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="618e1-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="618e1-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="618e1-126">Ao usar o método **AddPrinterDriver** , você deve usar **SeLoadDriverPrivilege** para carregar ou descarregar um driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="618e1-126">When using the **AddPrinterDriver** method you must use **SeLoadDriverPrivilege** to load or unload a device driver.</span></span>

 

## <a name="examples"></a><span data-ttu-id="618e1-127">Exemplos</span><span class="sxs-lookup"><span data-stu-id="618e1-127">Examples</span></span>

<span data-ttu-id="618e1-128">O exemplo de código de[instalação de um driver de impressora não encontrado nos drivers cab](https://Gallery.TechNet.Microsoft.Com/1aac6333-a794-48d3-b7da-46d87df56ee1) VBScript instala uma impressora hipotética usando um driver de impressão não encontrado no Drivers.cab.</span><span class="sxs-lookup"><span data-stu-id="618e1-128">The[Install a Printer Driver not Found in Drivers Cab](https://Gallery.TechNet.Microsoft.Com/1aac6333-a794-48d3-b7da-46d87df56ee1) VBScript code example installs a hypothetical printer using a print driver not found in Drivers.cab.</span></span>

<span data-ttu-id="618e1-129">O exemplo de VBScript a seguir instala o driver de impressora para uma impressora Apple LaserWriter 8500.</span><span class="sxs-lookup"><span data-stu-id="618e1-129">The following VBScript sample installs the printer driver for an Apple LaserWriter 8500 printer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
objWMIService.Security_.Privileges.AddAsString "SeLoadDriverPrivilege", True 
 
Set objDriver = objWMIService.Get("Win32_PrinterDriver") 
 
objDriver.Name = "NewPrinter Model 2900" 
objDriver.SupportedPlatform = "Windows NT x86" 
objDriver.Version = "3" 
objDriver.DriverPath = "C:\Scripts\NewPrinter.dll" 
objDriver.Infname = "C:\Scripts\NewPrinter.inf" 
intResult = objDriver.AddPrinterDriver(objDriver) 
```



## <a name="requirements"></a><span data-ttu-id="618e1-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="618e1-130">Requirements</span></span>



| <span data-ttu-id="618e1-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="618e1-131">Requirement</span></span> | <span data-ttu-id="618e1-132">Valor</span><span class="sxs-lookup"><span data-stu-id="618e1-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="618e1-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="618e1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="618e1-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="618e1-134">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="618e1-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="618e1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="618e1-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="618e1-136">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="618e1-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="618e1-137">Namespace</span></span><br/>                | <span data-ttu-id="618e1-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="618e1-138">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="618e1-139">MOF</span><span class="sxs-lookup"><span data-stu-id="618e1-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="618e1-140"><dt>\_Impressora. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="618e1-140"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="618e1-141">DLL</span><span class="sxs-lookup"><span data-stu-id="618e1-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="618e1-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="618e1-142"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="618e1-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="618e1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="618e1-144">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="618e1-144">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="618e1-145">**\_PrinterDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="618e1-145">**Win32\_PrinterDriver**</span></span>](win32-printerdriver.md)
</dt> </dl>

 

