---
description: Desabilita o adaptador de rede.
ms.assetid: 6b328d7c-a9ef-4c9b-bc32-13fa2e0f65eb
ms.tgt_platform: multiple
title: Método Disable da classe Win32_NetworkAdapter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapter.Disable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a9c6b1a506310460d9131709092b739f68986e02
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756044"
---
# <a name="disable-method-of-the-win32_networkadapter-class"></a><span data-ttu-id="3d7f3-103">Método Disable da classe Win32 \_ adaptador</span><span class="sxs-lookup"><span data-stu-id="3d7f3-103">Disable method of the Win32\_NetworkAdapter class</span></span>

<span data-ttu-id="3d7f3-104">O método **Disable** desabilita o adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="3d7f3-104">The **Disable** method disables the network adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d7f3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3d7f3-105">Syntax</span></span>


```mof
uint32 Disable();
```



## <a name="parameters"></a><span data-ttu-id="3d7f3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d7f3-106">Parameters</span></span>

<span data-ttu-id="3d7f3-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3d7f3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3d7f3-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3d7f3-108">Return value</span></span>

<span data-ttu-id="3d7f3-109">Retorna zero (0) para indicar êxito.</span><span class="sxs-lookup"><span data-stu-id="3d7f3-109">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="3d7f3-110">Qualquer outro número indica um erro.</span><span class="sxs-lookup"><span data-stu-id="3d7f3-110">Any other number indicates an error.</span></span> <span data-ttu-id="3d7f3-111">Para códigos de erro, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3d7f3-111">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="3d7f3-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d7f3-112">Requirements</span></span>



| <span data-ttu-id="3d7f3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d7f3-113">Requirement</span></span> | <span data-ttu-id="3d7f3-114">Valor</span><span class="sxs-lookup"><span data-stu-id="3d7f3-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d7f3-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d7f3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3d7f3-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d7f3-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3d7f3-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d7f3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3d7f3-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d7f3-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3d7f3-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="3d7f3-119">Namespace</span></span><br/>                | <span data-ttu-id="3d7f3-120">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3d7f3-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3d7f3-121">MOF</span><span class="sxs-lookup"><span data-stu-id="3d7f3-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d7f3-122"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d7f3-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d7f3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="3d7f3-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d7f3-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d7f3-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d7f3-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d7f3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d7f3-126">**\_Adaptador Win32**</span><span class="sxs-lookup"><span data-stu-id="3d7f3-126">**Win32\_NetworkAdapter**</span></span>](win32-networkadapter.md)
</dt> <dt>

[<span data-ttu-id="3d7f3-127">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="3d7f3-127">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="3d7f3-128">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="3d7f3-128">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

