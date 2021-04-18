---
description: O SetDateTime&\# 8194; O método de classe WMI define a hora atual do sistema no computador.
ms.assetid: b9b86a52-c3d7-489d-8632-b297970dbeac
ms.tgt_platform: multiple
title: Método SetDateTime da classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.SetDateTime
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 60316904d58ffec38aa912a1454082e7edfae5a8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756247"
---
# <a name="setdatetime-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="0204d-103">Método SetDateTime da classe do sistema \_ operacional Win32</span><span class="sxs-lookup"><span data-stu-id="0204d-103">SetDateTime method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="0204d-104">O método da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **setdatetimetime** define a hora atual do sistema no computador.</span><span class="sxs-lookup"><span data-stu-id="0204d-104">The **SetDateTime** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the current system time on the computer.</span></span>

<span data-ttu-id="0204d-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="0204d-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0204d-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0204d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0204d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0204d-107">Syntax</span></span>


```mof
uint32 SetDateTime(
  [in] datetime LocalDatetime
);
```



## <a name="parameters"></a><span data-ttu-id="0204d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0204d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0204d-109">*LocalDatetime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0204d-109">*LocalDatetime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0204d-110">Valor da hora atual.</span><span class="sxs-lookup"><span data-stu-id="0204d-110">Value of the current time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0204d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0204d-111">Return value</span></span>

<span data-ttu-id="0204d-112">Retorna zero (0) para indicar êxito.</span><span class="sxs-lookup"><span data-stu-id="0204d-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="0204d-113">Qualquer outro número indica um erro.</span><span class="sxs-lookup"><span data-stu-id="0204d-113">Any other number indicates an error.</span></span> <span data-ttu-id="0204d-114">Para códigos de erro, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="0204d-114">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="0204d-115">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="0204d-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="0204d-116">**Êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="0204d-116">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0204d-117">**Outro** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="0204d-117">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="0204d-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="0204d-118">Remarks</span></span>

<span data-ttu-id="0204d-119">O processo de chamada deve ter o \_ privilégio de nome SYSTEMTIME se \_ .</span><span class="sxs-lookup"><span data-stu-id="0204d-119">The calling process must have the SE\_SYSTEMTIME\_NAME privilege.</span></span>

## <a name="requirements"></a><span data-ttu-id="0204d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0204d-120">Requirements</span></span>



| <span data-ttu-id="0204d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0204d-121">Requirement</span></span> | <span data-ttu-id="0204d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0204d-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0204d-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0204d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0204d-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0204d-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0204d-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0204d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0204d-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0204d-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0204d-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="0204d-127">Namespace</span></span><br/>                | <span data-ttu-id="0204d-128">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0204d-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0204d-129">MOF</span><span class="sxs-lookup"><span data-stu-id="0204d-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0204d-130"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0204d-130"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0204d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="0204d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0204d-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0204d-132"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0204d-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="0204d-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="0204d-134">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0204d-134">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0204d-135">**Sistema \_ operacional Win32**</span><span class="sxs-lookup"><span data-stu-id="0204d-135">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="0204d-136">Tarefas do WMI: gerenciamento de desktop</span><span class="sxs-lookup"><span data-stu-id="0204d-136">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

