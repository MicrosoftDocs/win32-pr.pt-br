---
description: Retoma uma fila de impressão em pausa.
ms.assetid: 6d6d21e9-f469-4e2c-9a89-3e9febe229fc
ms.tgt_platform: multiple
title: Método resume da classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.Resume
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3eca8849fd1c5c449261dac1a9530f4da42e9482
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753805"
---
# <a name="resume-method-of-the-win32_printer-class"></a><span data-ttu-id="f6422-103">Método resume da classe de \_ impressora do Win32</span><span class="sxs-lookup"><span data-stu-id="f6422-103">Resume method of the Win32\_Printer class</span></span>

<span data-ttu-id="f6422-104">O método **retomar** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) retoma uma fila de impressão em pausa.</span><span class="sxs-lookup"><span data-stu-id="f6422-104">The **Resume** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method resumes a paused print queue.</span></span>

<span data-ttu-id="f6422-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="f6422-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f6422-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f6422-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f6422-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6422-107">Syntax</span></span>


```mof
uint32 Resume();
```



## <a name="parameters"></a><span data-ttu-id="f6422-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6422-108">Parameters</span></span>

<span data-ttu-id="f6422-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f6422-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f6422-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f6422-110">Return value</span></span>

<span data-ttu-id="f6422-111">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="f6422-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="f6422-112">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f6422-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f6422-113">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f6422-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f6422-114">**0**</span><span class="sxs-lookup"><span data-stu-id="f6422-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="f6422-115">Sucesso</span><span class="sxs-lookup"><span data-stu-id="f6422-115">Success</span></span>

</dd> <dt>

<span data-ttu-id="f6422-116">**5**</span><span class="sxs-lookup"><span data-stu-id="f6422-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="f6422-117">Acesso negado</span><span class="sxs-lookup"><span data-stu-id="f6422-117">Access Denied</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6422-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6422-118">Requirements</span></span>



| <span data-ttu-id="f6422-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6422-119">Requirement</span></span> | <span data-ttu-id="f6422-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f6422-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6422-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6422-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f6422-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6422-122">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="f6422-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6422-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f6422-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6422-124">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="f6422-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="f6422-125">Namespace</span></span><br/>                | <span data-ttu-id="f6422-126">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f6422-126">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="f6422-127">MOF</span><span class="sxs-lookup"><span data-stu-id="f6422-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6422-128"><dt>\_Impressora. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="f6422-128"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6422-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f6422-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6422-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6422-130"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="f6422-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6422-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6422-132">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="f6422-132">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="f6422-133">**\_Impressora Win32**</span><span class="sxs-lookup"><span data-stu-id="f6422-133">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="f6422-134">**Método Pause**</span><span class="sxs-lookup"><span data-stu-id="f6422-134">**Pause Method**</span></span>](pause-method-in-class-win32-printer.md)
</dt> </dl>

 

