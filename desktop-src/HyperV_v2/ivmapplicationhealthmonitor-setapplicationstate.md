---
description: Define o estado de integridade de um aplicativo que está sendo executado em uma máquina virtual.
ms.assetid: 012190CA-9CBF-47B6-9C5D-F75D73B0499B
title: 'Método IVmApplicationHealthMonitor:: setapplicationstate'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.SetApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 8e6c64ecec827f6f75f382fbca7aadf8fc0c7dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758802"
---
# <a name="ivmapplicationhealthmonitorsetapplicationstate-method"></a><span data-ttu-id="8ee01-103">Método IVmApplicationHealthMonitor:: setapplicationstate</span><span class="sxs-lookup"><span data-stu-id="8ee01-103">IVmApplicationHealthMonitor::SetApplicationState method</span></span>

<span data-ttu-id="8ee01-104">Define o estado de integridade de um aplicativo que está sendo executado em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8ee01-104">Sets the health state of an application that is running in a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ee01-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8ee01-105">Syntax</span></span>


```C++
HRESULT SetApplicationState(
  [in] BSTR              Id,
  [in] BSTR              Name,
  [in] APPLICATION_STATE State
);
```



## <a name="parameters"></a><span data-ttu-id="8ee01-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ee01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ee01-107">*ID* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="8ee01-107">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ee01-108">Uma representação **BSTR** do **GUID** que identifica o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8ee01-108">A **BSTR** representation of the **GUID** that identifies the application.</span></span> <span data-ttu-id="8ee01-109">É responsabilidade do aplicativo de chamada criar e manter os identificadores que ele usa para os aplicativos que estão sendo monitorados.</span><span class="sxs-lookup"><span data-stu-id="8ee01-109">It is the calling application's responsibility to create and maintain the identifiers it uses for the applications being monitored.</span></span>

</dd> <dt>

<span data-ttu-id="8ee01-110">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="8ee01-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ee01-111">O nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8ee01-111">The display name of the application.</span></span> <span data-ttu-id="8ee01-112">Esse nome é usado em uma entrada de log de eventos informativa para a alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="8ee01-112">This name is used in an informational event log entry for the state change.</span></span>

</dd> <dt>

<span data-ttu-id="8ee01-113">*Estado* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8ee01-113">*State* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ee01-114">Um valor da enumeração [**de \_ estado do aplicativo**](application-state.md) que especifica o novo estado de integridade do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8ee01-114">A value of the [**APPLICATION\_STATE**](application-state.md) enumeration that specifies the new health state of the application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ee01-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8ee01-115">Return value</span></span>

<span data-ttu-id="8ee01-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8ee01-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8ee01-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8ee01-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ee01-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ee01-118">Remarks</span></span>

<span data-ttu-id="8ee01-119">O estado dos aplicativos em execução na máquina virtual é refletido no valor da propriedade **OperationalStatus** \[ 1 \] da classe [**Msvm \_ HeartbeatComponent**](msvm-heartbeatcomponent.md) .</span><span class="sxs-lookup"><span data-stu-id="8ee01-119">The state of the applications running in the virtual machine are reflected in the **OperationalStatus**\[1\] property value of the [**Msvm\_HeartbeatComponent**](msvm-heartbeatcomponent.md) class.</span></span>

<span data-ttu-id="8ee01-120">Para usar esse elemento de programação, os componentes de integração do Windows 8 devem ser instalados na máquina virtual em que o aplicativo está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="8ee01-120">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ee01-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ee01-121">Requirements</span></span>



| <span data-ttu-id="8ee01-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ee01-122">Requirement</span></span> | <span data-ttu-id="8ee01-123">Valor</span><span class="sxs-lookup"><span data-stu-id="8ee01-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ee01-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ee01-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8ee01-125">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8ee01-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="8ee01-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ee01-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8ee01-127">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8ee01-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8ee01-128">Versão</span><span class="sxs-lookup"><span data-stu-id="8ee01-128">Version</span></span><br/>                  | <span data-ttu-id="8ee01-129">Componentes de integração do Windows 8</span><span class="sxs-lookup"><span data-stu-id="8ee01-129">Integration components for Windows 8</span></span><br/>                                                           |
| <span data-ttu-id="8ee01-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="8ee01-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8ee01-131"><dt>VmApplicationHealthMonitor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8ee01-131"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ee01-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ee01-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ee01-133">**IVmApplicationHealthMonitor**</span><span class="sxs-lookup"><span data-stu-id="8ee01-133">**IVmApplicationHealthMonitor**</span></span>](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




