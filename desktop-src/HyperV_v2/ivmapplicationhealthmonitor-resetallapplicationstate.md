---
description: Redefine o estado de integridade de todos os aplicativos em uma máquina virtual.
ms.assetid: DB0B2FB3-87EB-44B2-9C4E-849BCE594E89
title: 'Método IVmApplicationHealthMonitor:: ResetAllApplicationState'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.ResetAllApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: b13781d26c256e41ea6685b19a3097236ebbdb91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827613"
---
# <a name="ivmapplicationhealthmonitorresetallapplicationstate-method"></a><span data-ttu-id="2e5a0-103">Método IVmApplicationHealthMonitor:: ResetAllApplicationState</span><span class="sxs-lookup"><span data-stu-id="2e5a0-103">IVmApplicationHealthMonitor::ResetAllApplicationState method</span></span>

<span data-ttu-id="2e5a0-104">Redefine o estado de integridade de todos os aplicativos em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2e5a0-104">Resets the health state for all applications in a virtual machine.</span></span> <span data-ttu-id="2e5a0-105">Se for bem-sucedido, o estado de integridade de todos os aplicativos monitorados será definido como **ApplicationStateHealthy**.</span><span class="sxs-lookup"><span data-stu-id="2e5a0-105">If successful, the health state for all monitored applications will be set to **ApplicationStateHealthy**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e5a0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e5a0-106">Syntax</span></span>


```C++
HRESULT ResetAllApplicationState();
```



## <a name="parameters"></a><span data-ttu-id="2e5a0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e5a0-107">Parameters</span></span>

<span data-ttu-id="2e5a0-108">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2e5a0-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2e5a0-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2e5a0-109">Return value</span></span>

<span data-ttu-id="2e5a0-110">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2e5a0-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2e5a0-111">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2e5a0-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e5a0-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e5a0-112">Remarks</span></span>

<span data-ttu-id="2e5a0-113">Para usar esse elemento de programação, os componentes de integração do Windows 8 devem ser instalados na máquina virtual em que o aplicativo está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="2e5a0-113">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e5a0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e5a0-114">Requirements</span></span>



| <span data-ttu-id="2e5a0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e5a0-115">Requirement</span></span> | <span data-ttu-id="2e5a0-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2e5a0-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e5a0-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e5a0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2e5a0-118">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2e5a0-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="2e5a0-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e5a0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2e5a0-120">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2e5a0-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2e5a0-121">Versão</span><span class="sxs-lookup"><span data-stu-id="2e5a0-121">Version</span></span><br/>                  | <span data-ttu-id="2e5a0-122">Componentes de integração do Windows 8</span><span class="sxs-lookup"><span data-stu-id="2e5a0-122">Integration components for Windows 8</span></span><br/>                                                           |
| <span data-ttu-id="2e5a0-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="2e5a0-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2e5a0-124"><dt>VmApplicationHealthMonitor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2e5a0-124"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e5a0-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e5a0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e5a0-126">**IVmApplicationHealthMonitor**</span><span class="sxs-lookup"><span data-stu-id="2e5a0-126">**IVmApplicationHealthMonitor**</span></span>](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




