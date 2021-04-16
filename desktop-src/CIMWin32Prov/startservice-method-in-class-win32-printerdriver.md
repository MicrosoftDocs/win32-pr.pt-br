---
description: O método StartService coloca o serviço no estado iniciado.
ms.assetid: 0f221db1-29ad-4071-98d3-6d06e4f5e026
ms.tgt_platform: multiple
title: Método StartService da classe Win32_PrinterDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44e6fedb9e1d0edd9f355c654c7fe2cd25760ec7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753804"
---
# <a name="startservice-method-of-the-win32_printerdriver-class"></a><span data-ttu-id="0530d-103">Método StartService da classe Win32 \_ PrinterDriver</span><span class="sxs-lookup"><span data-stu-id="0530d-103">StartService method of the Win32\_PrinterDriver class</span></span>

<span data-ttu-id="0530d-104">O método **StartService** coloca o serviço no estado iniciado.</span><span class="sxs-lookup"><span data-stu-id="0530d-104">The **StartService** method places the service in the started state.</span></span>

<span data-ttu-id="0530d-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="0530d-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0530d-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0530d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0530d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0530d-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="0530d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0530d-108">Parameters</span></span>

<span data-ttu-id="0530d-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0530d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0530d-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0530d-110">Return value</span></span>

<span data-ttu-id="0530d-111">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="0530d-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="0530d-112">Para valores diferentes daqueles listados na lista a seguir, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants).</span><span class="sxs-lookup"><span data-stu-id="0530d-112">For values different from those listed in the following list, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants).</span></span>

<dl> <dt>

<span data-ttu-id="0530d-113">**0**</span><span class="sxs-lookup"><span data-stu-id="0530d-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="0530d-114">Serviço iniciado com êxito.</span><span class="sxs-lookup"><span data-stu-id="0530d-114">Service successfully started.</span></span>

</dd> <dt>

<span data-ttu-id="0530d-115">**1**</span><span class="sxs-lookup"><span data-stu-id="0530d-115">**1**</span></span>
</dt> <dd>

<span data-ttu-id="0530d-116">Não há suporte para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="0530d-116">Request not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0530d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0530d-117">Requirements</span></span>



| <span data-ttu-id="0530d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0530d-118">Requirement</span></span> | <span data-ttu-id="0530d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="0530d-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0530d-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0530d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0530d-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0530d-121">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="0530d-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0530d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0530d-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0530d-123">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="0530d-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="0530d-124">Namespace</span></span><br/>                | <span data-ttu-id="0530d-125">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0530d-125">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="0530d-126">MOF</span><span class="sxs-lookup"><span data-stu-id="0530d-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0530d-127"><dt>\_Impressora. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="0530d-127"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="0530d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0530d-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0530d-129"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0530d-129"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="0530d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="0530d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0530d-131">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="0530d-131">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="0530d-132">**\_PrinterDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="0530d-132">**Win32\_PrinterDriver**</span></span>](win32-printerdriver.md)
</dt> </dl>

 

