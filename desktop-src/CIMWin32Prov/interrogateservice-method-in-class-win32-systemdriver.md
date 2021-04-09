---
description: Solicita que o serviço de driver do sistema atualize seu estado para o Service Manager.
ms.assetid: 350d9044-39fd-436f-ab15-b30324b2b2e9
ms.tgt_platform: multiple
title: Método InterrogateService da classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.InterrogateService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 666a261dfe3fac7dd62e6253c5eb4804b3a55677
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089098"
---
# <a name="interrogateservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="ab0c8-103">Método InterrogateService da \_ classe SystemDriver Win32</span><span class="sxs-lookup"><span data-stu-id="ab0c8-103">InterrogateService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="ab0c8-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **InterrogateService** solicita que o serviço de driver do sistema atualize seu estado para o Service Manager.</span><span class="sxs-lookup"><span data-stu-id="ab0c8-104">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the system driver service update its state to the service manager.</span></span>

<span data-ttu-id="ab0c8-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="ab0c8-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ab0c8-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ab0c8-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ab0c8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab0c8-107">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="ab0c8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab0c8-108">Parameters</span></span>

<span data-ttu-id="ab0c8-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ab0c8-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ab0c8-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ab0c8-110">Return value</span></span>

<span data-ttu-id="ab0c8-111">Retorna um valor de 0 (zero) se a solicitação **InterrogateService** tiver sido aceita, 1 (uma) se a solicitação não tiver suporte e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="ab0c8-111">Returns a value of 0 (zero) if the **InterrogateService** request was accepted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab0c8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab0c8-112">Requirements</span></span>



| <span data-ttu-id="ab0c8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab0c8-113">Requirement</span></span> | <span data-ttu-id="ab0c8-114">Valor</span><span class="sxs-lookup"><span data-stu-id="ab0c8-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab0c8-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab0c8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ab0c8-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ab0c8-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ab0c8-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab0c8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ab0c8-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab0c8-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ab0c8-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="ab0c8-119">Namespace</span></span><br/>                | <span data-ttu-id="ab0c8-120">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ab0c8-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ab0c8-121">MOF</span><span class="sxs-lookup"><span data-stu-id="ab0c8-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab0c8-122"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab0c8-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab0c8-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ab0c8-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab0c8-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab0c8-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab0c8-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab0c8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab0c8-126">**Systemdrive do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="ab0c8-126">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> <dt>

<span data-ttu-id="ab0c8-127">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ab0c8-127">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ab0c8-128">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="ab0c8-128">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

