---
title: Método IMsTscAxEvents OnChannelReceivedData
description: Chamado quando o cliente recebe dados em um canal virtual programável.
ms.assetid: 38e6c33c-6a79-4760-818e-445e33d8e0ec
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnChannelReceivedData
- Método OnChannelReceivedData Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnChannelReceivedData
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnChannelReceivedData
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1cae4f35435138e219c628dd504c595939adfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085485"
---
# <a name="imstscaxeventsonchannelreceiveddata-method"></a><span data-ttu-id="4dff8-106">Método IMsTscAxEvents:: OnChannelReceivedData</span><span class="sxs-lookup"><span data-stu-id="4dff8-106">IMsTscAxEvents::OnChannelReceivedData method</span></span>

<span data-ttu-id="4dff8-107">Chamado quando o cliente recebe dados em um canal virtual programável.</span><span class="sxs-lookup"><span data-stu-id="4dff8-107">Called when the client receives data on a scriptable virtual channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dff8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4dff8-108">Syntax</span></span>


```C++
void OnChannelReceivedData(
  [in] BSTR chanName,
  [in] BSTR data
);
```



## <a name="parameters"></a><span data-ttu-id="4dff8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4dff8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dff8-110">*canalname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4dff8-110">*chanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4dff8-111">O nome do canal virtual em que os dados foram recebidos.</span><span class="sxs-lookup"><span data-stu-id="4dff8-111">The name of the virtual channel on which data was received.</span></span> <span data-ttu-id="4dff8-112">Esse nome corresponde a um dos canais criados pela chamada para [**IMsTscAx:: CreateVirtualChannels**](imstscax-createvirtualchannels.md).</span><span class="sxs-lookup"><span data-stu-id="4dff8-112">This name matches one of the channels created by the call to [**IMsTscAx::CreateVirtualChannels**](imstscax-createvirtualchannels.md).</span></span>

</dd> <dt>

<span data-ttu-id="4dff8-113">*dados* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="4dff8-113">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4dff8-114">Os dados recebidos no canal virtual programável.</span><span class="sxs-lookup"><span data-stu-id="4dff8-114">The data received on the scriptable virtual channel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dff8-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4dff8-115">Return value</span></span>

<span data-ttu-id="4dff8-116">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4dff8-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dff8-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="4dff8-117">Remarks</span></span>

<span data-ttu-id="4dff8-118">Consulte [implementando canais virtuais programáveis usando conexão Web de área de trabalho remota](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md) para obter mais informações sobre esse evento.</span><span class="sxs-lookup"><span data-stu-id="4dff8-118">Refer to [Implementing Scriptable Virtual Channels using Remote Desktop Web Connection](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md) for more information about this event.</span></span>

<span data-ttu-id="4dff8-119">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="4dff8-119">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4dff8-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4dff8-120">Requirements</span></span>



| <span data-ttu-id="4dff8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4dff8-121">Requirement</span></span> | <span data-ttu-id="4dff8-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4dff8-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4dff8-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4dff8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4dff8-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4dff8-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4dff8-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4dff8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4dff8-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4dff8-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4dff8-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4dff8-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="4dff8-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4dff8-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4dff8-129">DLL</span><span class="sxs-lookup"><span data-stu-id="4dff8-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4dff8-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4dff8-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4dff8-131">IID</span><span class="sxs-lookup"><span data-stu-id="4dff8-131">IID</span></span><br/>                      | <span data-ttu-id="4dff8-132">IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="4dff8-132">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="4dff8-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="4dff8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dff8-134">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="4dff8-134">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





