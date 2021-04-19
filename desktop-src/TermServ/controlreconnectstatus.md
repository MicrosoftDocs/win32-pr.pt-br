---
title: Enumeração ControlReconnectStatus
description: Especifica o resultado do método de reconexão IMsRdpClient8.
ms.assetid: FB0AC4CF-18F5-4CDD-A75C-59A7CF716688
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de enumeração ControlReconnectStatus
topic_type:
- apiref
api_name:
- ControlReconnectStatus
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5638cbdda268dd453881ee1d88085728479aada6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105766954"
---
# <a name="controlreconnectstatus-enumeration"></a><span data-ttu-id="85eb0-104">Enumeração ControlReconnectStatus</span><span class="sxs-lookup"><span data-stu-id="85eb0-104">ControlReconnectStatus enumeration</span></span>

<span data-ttu-id="85eb0-105">Especifica o resultado do método [**IMsRdpClient8:: Reconnect**](imsrdpclient8-reconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="85eb0-105">Specifies the result of the [**IMsRdpClient8::Reconnect**](imsrdpclient8-reconnect.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="85eb0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="85eb0-106">Syntax</span></span>


```C++
typedef enum  { 
  controlReconnectStarted  = 0x0000,
  controlReconnectBlocked  = 0x0001
} ControlReconnectStatus;
```



## <a name="constants"></a><span data-ttu-id="85eb0-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="85eb0-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="85eb0-108"><span id="controlReconnectStarted"></span><span id="controlreconnectstarted"></span><span id="CONTROLRECONNECTSTARTED"></span>**controlReconnectStarted**</span><span class="sxs-lookup"><span data-stu-id="85eb0-108"><span id="controlReconnectStarted"></span><span id="controlreconnectstarted"></span><span id="CONTROLRECONNECTSTARTED"></span>**controlReconnectStarted**</span></span>
</dt> <dd>

<span data-ttu-id="85eb0-109">A operação de reconexão foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="85eb0-109">The reconnect operation was started.</span></span>

</dd> <dt>

<span data-ttu-id="85eb0-110"><span id="controlReconnectBlocked"></span><span id="controlreconnectblocked"></span><span id="CONTROLRECONNECTBLOCKED"></span>**controlReconnectBlocked**</span><span class="sxs-lookup"><span data-stu-id="85eb0-110"><span id="controlReconnectBlocked"></span><span id="controlreconnectblocked"></span><span id="CONTROLRECONNECTBLOCKED"></span>**controlReconnectBlocked**</span></span>
</dt> <dd>

<span data-ttu-id="85eb0-111">Não foi possível iniciar a operação de reconexão.</span><span class="sxs-lookup"><span data-stu-id="85eb0-111">The reconnect operation could not be started.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="85eb0-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85eb0-112">Requirements</span></span>



| <span data-ttu-id="85eb0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="85eb0-113">Requirement</span></span> | <span data-ttu-id="85eb0-114">Valor</span><span class="sxs-lookup"><span data-stu-id="85eb0-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85eb0-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85eb0-115">Minimum supported client</span></span><br/> | <span data-ttu-id="85eb0-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="85eb0-116">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="85eb0-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85eb0-117">Minimum supported server</span></span><br/> | <span data-ttu-id="85eb0-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="85eb0-118">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="85eb0-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="85eb0-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="85eb0-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85eb0-120"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85eb0-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="85eb0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85eb0-122">**IMsRdpClient8:: reconectar**</span><span class="sxs-lookup"><span data-stu-id="85eb0-122">**IMsRdpClient8::Reconnect**</span></span>](imsrdpclient8-reconnect.md)
</dt> </dl>

 

 





