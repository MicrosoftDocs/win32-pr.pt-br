---
description: Método Delete da classe Win32_SystemDriver-a exclusão&\# 8194; O método de classe WMI exclui um serviço existente.
ms.assetid: 5e437d36-3582-448c-b568-45f7fb13b096
ms.tgt_platform: multiple
title: Método Delete da classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e1b7435a1bca561b19e7d85299413f88f1ae76c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097084"
---
# <a name="delete-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="aa1e5-103">Método Delete da \_ classe systemdrive do Win32</span><span class="sxs-lookup"><span data-stu-id="aa1e5-103">Delete method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="aa1e5-104">O método **excluir** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) exclui um serviço existente.</span><span class="sxs-lookup"><span data-stu-id="aa1e5-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes an existing service.</span></span>

<span data-ttu-id="aa1e5-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="aa1e5-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="aa1e5-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="aa1e5-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="aa1e5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa1e5-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="aa1e5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa1e5-108">Parameters</span></span>

<span data-ttu-id="aa1e5-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="aa1e5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aa1e5-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="aa1e5-110">Return value</span></span>

<span data-ttu-id="aa1e5-111">Retorna um valor de 0 (zero) se o serviço tiver sido excluído com êxito, 1 (um) se a solicitação não tiver suporte e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="aa1e5-111">Returns a value of 0 (zero) if the service was successfully deleted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa1e5-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa1e5-112">Requirements</span></span>



| <span data-ttu-id="aa1e5-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa1e5-113">Requirement</span></span> | <span data-ttu-id="aa1e5-114">Valor</span><span class="sxs-lookup"><span data-stu-id="aa1e5-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa1e5-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa1e5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="aa1e5-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa1e5-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aa1e5-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa1e5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="aa1e5-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa1e5-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aa1e5-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="aa1e5-119">Namespace</span></span><br/>                | <span data-ttu-id="aa1e5-120">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="aa1e5-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aa1e5-121">MOF</span><span class="sxs-lookup"><span data-stu-id="aa1e5-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa1e5-122"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aa1e5-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa1e5-123">DLL</span><span class="sxs-lookup"><span data-stu-id="aa1e5-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa1e5-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa1e5-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa1e5-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="aa1e5-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="aa1e5-126">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="aa1e5-126">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="aa1e5-127">**Systemdrive do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="aa1e5-127">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

