---
description: Relata o status de integridade de um aplicativo que está sendo executado em uma máquina virtual para os componentes de integração do Hyper-V em execução na mesma máquina virtual.
ms.assetid: C463391B-669C-4CBA-9EC7-7E0ABC5A63A1
title: Interface IVmApplicationHealthMonitor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: ac9f6574dd8261a120e434cc0351fd07985c71a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759877"
---
# <a name="ivmapplicationhealthmonitor-interface"></a><span data-ttu-id="d7b50-103">Interface IVmApplicationHealthMonitor</span><span class="sxs-lookup"><span data-stu-id="d7b50-103">IVmApplicationHealthMonitor interface</span></span>

<span data-ttu-id="d7b50-104">Relata o status de integridade de um aplicativo que está sendo executado em uma máquina virtual para os componentes de integração do Hyper-V em execução na mesma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d7b50-104">Reports the health status of an application that is running in a virtual machine to the Hyper-V integration components running in the same virtual machine.</span></span> <span data-ttu-id="d7b50-105">O estado dos aplicativos em execução na máquina virtual é refletido no valor da propriedade **OperationalStatus** \[ 1 \] da classe [**Msvm \_ HeartbeatComponent**](msvm-heartbeatcomponent.md) .</span><span class="sxs-lookup"><span data-stu-id="d7b50-105">The state of the applications running in the virtual machine are reflected in the **OperationalStatus**\[1\] property value of the [**Msvm\_HeartbeatComponent**](msvm-heartbeatcomponent.md) class.</span></span> <span data-ttu-id="d7b50-106">Essa interface também fornece uma maneira de redefinir todo o estado do aplicativo acumulado no Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="d7b50-106">This interface also provides a way to reset all of the application state accumulated in Hyper-V.</span></span>

<span data-ttu-id="d7b50-107">Essa interface é implementada pelos componentes de integração do Hyper-V do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d7b50-107">This interface is implemented by the Windows 8 Hyper-V integration components.</span></span> <span data-ttu-id="d7b50-108">Uma instância dessa interface é obtida com a criação de uma instância do CLSID do **397a2e5f-348c-482D-b9a3-57d383b483cd** .</span><span class="sxs-lookup"><span data-stu-id="d7b50-108">An instance of this interface is obtained by creating an instance of the **397a2e5f-348c-482d-b9a3-57d383b483cd** CLSID.</span></span>

## <a name="members"></a><span data-ttu-id="d7b50-109">Membros</span><span class="sxs-lookup"><span data-stu-id="d7b50-109">Members</span></span>

<span data-ttu-id="d7b50-110">A interface **IVmApplicationHealthMonitor** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="d7b50-110">The **IVmApplicationHealthMonitor** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="d7b50-111">**IVmApplicationHealthMonitor** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d7b50-111">**IVmApplicationHealthMonitor** also has these types of members:</span></span>

-   [<span data-ttu-id="d7b50-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="d7b50-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d7b50-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="d7b50-113">Methods</span></span>

<span data-ttu-id="d7b50-114">A interface **IVmApplicationHealthMonitor** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d7b50-114">The **IVmApplicationHealthMonitor** interface has these methods.</span></span>



| <span data-ttu-id="d7b50-115">Método</span><span class="sxs-lookup"><span data-stu-id="d7b50-115">Method</span></span>                                                                                   | <span data-ttu-id="d7b50-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7b50-116">Description</span></span>                                                                              |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7b50-117">**ResetAllApplicationState**</span><span class="sxs-lookup"><span data-stu-id="d7b50-117">**ResetAllApplicationState**</span></span>](ivmapplicationhealthmonitor-resetallapplicationstate.md) | <span data-ttu-id="d7b50-118">Redefine o estado de integridade de todos os aplicativos em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d7b50-118">Resets the health state for all applications in a virtual machine.</span></span><br/>            |
| [<span data-ttu-id="d7b50-119">**Setapplicationstate**</span><span class="sxs-lookup"><span data-stu-id="d7b50-119">**SetApplicationState**</span></span>](ivmapplicationhealthmonitor-setapplicationstate.md)           | <span data-ttu-id="d7b50-120">Define o estado de integridade de um aplicativo que está sendo executado em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d7b50-120">Sets the health state of an application that is running in a virtual machine.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d7b50-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7b50-121">Remarks</span></span>

<span data-ttu-id="d7b50-122">Para usar esse elemento de programação, os componentes de integração do Windows 8 devem ser instalados na máquina virtual em que o aplicativo está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="d7b50-122">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7b50-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7b50-123">Requirements</span></span>



| <span data-ttu-id="d7b50-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7b50-124">Requirement</span></span> | <span data-ttu-id="d7b50-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d7b50-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7b50-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7b50-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d7b50-127">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d7b50-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="d7b50-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7b50-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d7b50-129">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d7b50-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                                                                                           |
| <span data-ttu-id="d7b50-130">Versão</span><span class="sxs-lookup"><span data-stu-id="d7b50-130">Version</span></span><br/>                  | <span data-ttu-id="d7b50-131">Componentes de integração do Windows 8</span><span class="sxs-lookup"><span data-stu-id="d7b50-131">Integration components for Windows 8</span></span><br/>                                                                                                                                |
| <span data-ttu-id="d7b50-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="d7b50-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d7b50-133"><dt>VmApplicationHealthMonitor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d7b50-133"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="d7b50-134">IID</span><span class="sxs-lookup"><span data-stu-id="d7b50-134">IID</span></span><br/>                      | <span data-ttu-id="d7b50-135">IID \_ IVmApplicationHealthMonitor é definido como 267a0284-848f-447e-a096-5e10a1a76bca</span><span class="sxs-lookup"><span data-stu-id="d7b50-135">IID\_IVmApplicationHealthMonitor is defined as 267a0284-848f-447e-a096-5e10a1a76bca</span></span><br/> <span data-ttu-id="d7b50-136">O identificador de objeto é definido como 397a2e5f-348c-482D-b9a3-57d383b483cd</span><span class="sxs-lookup"><span data-stu-id="d7b50-136">Object Identifier is defined as 397a2e5f-348c-482d-b9a3-57d383b483cd</span></span><br/> |



 

