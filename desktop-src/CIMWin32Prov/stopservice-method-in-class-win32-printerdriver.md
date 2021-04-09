---
description: Coloca o serviço representado pelo \_ objeto PrinterDriver do Win32 no estado parado.
ms.assetid: 0e730fe6-ff9f-4866-a255-be6d372f2d7d
ms.tgt_platform: multiple
title: Método StopService da classe Win32_PrinterDriver (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: faed7e9ed22ddcacbd8720e589463fd9a75fd87a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010201"
---
# <a name="stopservice-method-of-the-win32_printerdriver-class"></a><span data-ttu-id="b9df8-103">Método StopService da classe Win32 \_ PrinterDriver</span><span class="sxs-lookup"><span data-stu-id="b9df8-103">StopService method of the Win32\_PrinterDriver class</span></span>

<span data-ttu-id="b9df8-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** coloca o serviço representado pelo [**objeto \_ PrinterDriver do Win32**](win32-printerdriver.md) no estado parado.</span><span class="sxs-lookup"><span data-stu-id="b9df8-104">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method places the service represented by the [**Win32\_PrinterDriver**](win32-printerdriver.md) object in the stopped state.</span></span>

<span data-ttu-id="b9df8-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="b9df8-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b9df8-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b9df8-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b9df8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9df8-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="b9df8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9df8-108">Parameters</span></span>

<span data-ttu-id="b9df8-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b9df8-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b9df8-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b9df8-110">Return value</span></span>

<span data-ttu-id="b9df8-111">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="b9df8-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="b9df8-112">Para valores diferentes daqueles listados na lista a seguir, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants).</span><span class="sxs-lookup"><span data-stu-id="b9df8-112">For values different from those listed in the following list, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants).</span></span>

<dl> <dt>

<span data-ttu-id="b9df8-113">**0**</span><span class="sxs-lookup"><span data-stu-id="b9df8-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="b9df8-114">Serviço parado com êxito.</span><span class="sxs-lookup"><span data-stu-id="b9df8-114">Service successfully stopped.</span></span>

</dd> <dt>

<span data-ttu-id="b9df8-115">**1**</span><span class="sxs-lookup"><span data-stu-id="b9df8-115">**1**</span></span>
</dt> <dd>

<span data-ttu-id="b9df8-116">Não há suporte para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="b9df8-116">Request not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b9df8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9df8-117">Requirements</span></span>



| <span data-ttu-id="b9df8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9df8-118">Requirement</span></span> | <span data-ttu-id="b9df8-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b9df8-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9df8-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9df8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b9df8-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9df8-121">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="b9df8-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9df8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b9df8-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9df8-123">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="b9df8-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="b9df8-124">Namespace</span></span><br/>                | <span data-ttu-id="b9df8-125">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b9df8-125">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="b9df8-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b9df8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9df8-127"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9df8-127"><dt>Sdoias.h</dt></span></span> </dl>           |
| <span data-ttu-id="b9df8-128">MOF</span><span class="sxs-lookup"><span data-stu-id="b9df8-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9df8-129"><dt>\_Impressora. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="b9df8-129"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9df8-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b9df8-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9df8-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9df8-131"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="b9df8-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9df8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9df8-133">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="b9df8-133">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="b9df8-134">**\_PrinterDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="b9df8-134">**Win32\_PrinterDriver**</span></span>](win32-printerdriver.md)
</dt> </dl>

 

