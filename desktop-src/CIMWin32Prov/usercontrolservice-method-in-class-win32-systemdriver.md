---
description: Tenta enviar um código de controle definido pelo usuário para um serviço gerenciado por um driver de sistema.
ms.assetid: 62e66c35-f264-43d0-9e94-fb5e85f936e0
ms.tgt_platform: multiple
title: Método UserControlService da classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 99974206f6487d90e1660f5a64c1d00904912c66
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920530"
---
# <a name="usercontrolservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="8cb27-103">Método UserControlService da \_ classe SystemDriver Win32</span><span class="sxs-lookup"><span data-stu-id="8cb27-103">UserControlService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="8cb27-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UserControlService** tenta enviar um código de controle definido pelo usuário para um serviço gerenciado por um driver de sistema.</span><span class="sxs-lookup"><span data-stu-id="8cb27-104">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to a service managed by a system driver.</span></span>

<span data-ttu-id="8cb27-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="8cb27-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8cb27-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8cb27-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8cb27-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8cb27-107">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="8cb27-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8cb27-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cb27-109">*ControlCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8cb27-109">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cb27-110">Especifica os valores definidos (de 128 a 255) que fornecem comandos de controle específicos para um usuário.</span><span class="sxs-lookup"><span data-stu-id="8cb27-110">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cb27-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8cb27-111">Return value</span></span>

<span data-ttu-id="8cb27-112">Retorna um valor de 0 (zero) se a solicitação **UserControlService** tiver sido aceita, 1 (uma) se a solicitação não tiver suporte e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="8cb27-112">Returns a value of 0 (zero) if the **UserControlService** request was accepted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cb27-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cb27-113">Requirements</span></span>



| <span data-ttu-id="8cb27-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cb27-114">Requirement</span></span> | <span data-ttu-id="8cb27-115">Valor</span><span class="sxs-lookup"><span data-stu-id="8cb27-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cb27-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cb27-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8cb27-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8cb27-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8cb27-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cb27-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8cb27-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8cb27-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8cb27-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="8cb27-120">Namespace</span></span><br/>                | <span data-ttu-id="8cb27-121">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8cb27-121">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8cb27-122">MOF</span><span class="sxs-lookup"><span data-stu-id="8cb27-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8cb27-123"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8cb27-123"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8cb27-124">DLL</span><span class="sxs-lookup"><span data-stu-id="8cb27-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cb27-125"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cb27-125"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cb27-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="8cb27-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="8cb27-127">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8cb27-127">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8cb27-128">**Systemdrive do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="8cb27-128">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

