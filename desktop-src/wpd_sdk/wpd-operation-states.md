---
description: A \_ operação WPD \_ declara valores de enumeração que descrevem o estado atual de uma operação em andamento.
ms.assetid: a002f735-e385-4c7c-b734-e70a9c6842ca
title: Enumeração de WPD_OPERATION_STATES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_OPERATION_STATES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1746ab6a798c74974708ac10b9c4d137bf6c1d42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763148"
---
# <a name="wpd_operation_states-enumeration"></a><span data-ttu-id="72016-103">Enumeração de Estados de \_ operação WPD \_</span><span class="sxs-lookup"><span data-stu-id="72016-103">WPD\_OPERATION\_STATES enumeration</span></span>

<span data-ttu-id="72016-104">A **\_ operação WPD \_ declara** valores de enumeração que descrevem o estado atual de uma operação em andamento.</span><span class="sxs-lookup"><span data-stu-id="72016-104">The **WPD\_OPERATION\_STATES** enumeration values describe the current state of an operation in progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="72016-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="72016-105">Syntax</span></span>


```C++
typedef enum tagWPD_OPERATION_STATES { 
  WPD_OPERATION_STATE_UNSPECIFIED  = 0,
  WPD_OPERATION_STATE_STARTED      = 1,
  WPD_OPERATION_STATE_RUNNING      = 2,
  WPD_OPERATION_STATE_PAUSED       = 3,
  WPD_OPERATION_STATE_CANCELLED    = 4,
  WPD_OPERATION_STATE_FINISHED     = 5,
  WPD_OPERATION_STATE_ABORTED      = 6
} WPD_OPERATION_STATES;
```



## <a name="constants"></a><span data-ttu-id="72016-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="72016-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="72016-107"><span id="WPD_OPERATION_STATE_UNSPECIFIED"></span><span id="wpd_operation_state_unspecified"></span>**\_estado da operação WPD \_ \_ não especificado**</span><span class="sxs-lookup"><span data-stu-id="72016-107"><span id="WPD_OPERATION_STATE_UNSPECIFIED"></span><span id="wpd_operation_state_unspecified"></span>**WPD\_OPERATION\_STATE\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="72016-108">A operação atual está em um estado não especificado (não definido) e desconhecido.</span><span class="sxs-lookup"><span data-stu-id="72016-108">The current operation is in an unspecified state (not set) and unknown.</span></span>

</dd> <dt>

<span data-ttu-id="72016-109"><span id="WPD_OPERATION_STATE_STARTED"></span><span id="wpd_operation_state_started"></span>**\_estado da operação WPD \_ \_ iniciado**</span><span class="sxs-lookup"><span data-stu-id="72016-109"><span id="WPD_OPERATION_STATE_STARTED"></span><span id="wpd_operation_state_started"></span>**WPD\_OPERATION\_STATE\_STARTED**</span></span>
</dt> <dd>

<span data-ttu-id="72016-110">A operação foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="72016-110">The operation is started.</span></span>

</dd> <dt>

<span data-ttu-id="72016-111"><span id="WPD_OPERATION_STATE_RUNNING"></span><span id="wpd_operation_state_running"></span>**\_estado da operação WPD \_ \_ em execução**</span><span class="sxs-lookup"><span data-stu-id="72016-111"><span id="WPD_OPERATION_STATE_RUNNING"></span><span id="wpd_operation_state_running"></span>**WPD\_OPERATION\_STATE\_RUNNING**</span></span>
</dt> <dd>

<span data-ttu-id="72016-112">A operação está em execução.</span><span class="sxs-lookup"><span data-stu-id="72016-112">The operation is running.</span></span>

</dd> <dt>

<span data-ttu-id="72016-113"><span id="WPD_OPERATION_STATE_PAUSED"></span><span id="wpd_operation_state_paused"></span>**\_estado de operação WPD \_ \_ pausado**</span><span class="sxs-lookup"><span data-stu-id="72016-113"><span id="WPD_OPERATION_STATE_PAUSED"></span><span id="wpd_operation_state_paused"></span>**WPD\_OPERATION\_STATE\_PAUSED**</span></span>
</dt> <dd>

<span data-ttu-id="72016-114">A operação está em pausa.</span><span class="sxs-lookup"><span data-stu-id="72016-114">The operation is paused.</span></span>

</dd> <dt>

<span data-ttu-id="72016-115"><span id="WPD_OPERATION_STATE_CANCELLED"></span><span id="wpd_operation_state_cancelled"></span>**\_estado da operação WPD \_ \_ cancelado**</span><span class="sxs-lookup"><span data-stu-id="72016-115"><span id="WPD_OPERATION_STATE_CANCELLED"></span><span id="wpd_operation_state_cancelled"></span>**WPD\_OPERATION\_STATE\_CANCELLED**</span></span>
</dt> <dd>

<span data-ttu-id="72016-116">A operação foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="72016-116">The operation is canceled.</span></span>

</dd> <dt>

<span data-ttu-id="72016-117"><span id="WPD_OPERATION_STATE_FINISHED"></span><span id="wpd_operation_state_finished"></span>**\_estado da operação WPD \_ \_ concluído**</span><span class="sxs-lookup"><span data-stu-id="72016-117"><span id="WPD_OPERATION_STATE_FINISHED"></span><span id="wpd_operation_state_finished"></span>**WPD\_OPERATION\_STATE\_FINISHED**</span></span>
</dt> <dd>

<span data-ttu-id="72016-118">A operação foi concluída.</span><span class="sxs-lookup"><span data-stu-id="72016-118">The operation is finished.</span></span>

</dd> <dt>

<span data-ttu-id="72016-119"><span id="WPD_OPERATION_STATE_ABORTED"></span><span id="wpd_operation_state_aborted"></span>**\_estado da operação WPD \_ \_ anulado**</span><span class="sxs-lookup"><span data-stu-id="72016-119"><span id="WPD_OPERATION_STATE_ABORTED"></span><span id="wpd_operation_state_aborted"></span>**WPD\_OPERATION\_STATE\_ABORTED**</span></span>
</dt> <dd>

<span data-ttu-id="72016-120">A operação foi anulada.</span><span class="sxs-lookup"><span data-stu-id="72016-120">The operation is aborted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72016-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="72016-121">Remarks</span></span>

<span data-ttu-id="72016-122">Esses valores são recebidos no retorno de chamada definido pelo aplicativo ([**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)).</span><span class="sxs-lookup"><span data-stu-id="72016-122">These values are received in the application-defined callback ([**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)).</span></span>

## <a name="requirements"></a><span data-ttu-id="72016-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72016-123">Requirements</span></span>



| <span data-ttu-id="72016-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="72016-124">Requirement</span></span> | <span data-ttu-id="72016-125">Valor</span><span class="sxs-lookup"><span data-stu-id="72016-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="72016-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="72016-126">Header</span></span><br/> | <dl> <span data-ttu-id="72016-127"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="72016-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72016-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="72016-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72016-129">**Estruturas e tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="72016-129">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




