---
title: Enumeração ControlCloseStatus
description: Indica se o aplicativo que contém o controle pode fechar o controle imediatamente.
ms.assetid: ac2e1c68-81b1-4b51-aa7e-0ff703e619a2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de enumeração ControlCloseStatus
topic_type:
- apiref
api_name:
- ControlCloseStatus
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b94e0ce5cd040a2ade970f566897d2eac339dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918082"
---
# <a name="controlclosestatus-enumeration"></a><span data-ttu-id="f4ec8-104">Enumeração ControlCloseStatus</span><span class="sxs-lookup"><span data-stu-id="f4ec8-104">ControlCloseStatus enumeration</span></span>

<span data-ttu-id="f4ec8-105">Indica se o aplicativo que contém o controle pode fechar o controle imediatamente.</span><span class="sxs-lookup"><span data-stu-id="f4ec8-105">Indicates whether the application containing the control can close the control immediately.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4ec8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4ec8-106">Syntax</span></span>


```C++
enum ControlCloseStatus {
  controlCloseCanProceed     = 0x0000, 
  controlCloseWaitForEvents  = 0x0001 

};
```



## <a name="constants"></a><span data-ttu-id="f4ec8-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="f4ec8-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f4ec8-108"><span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed**</span><span class="sxs-lookup"><span data-stu-id="f4ec8-108"><span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed**</span></span>
</dt> <dd>

<span data-ttu-id="f4ec8-109">O contêiner pode prosseguir com o próximo imediatamente.</span><span class="sxs-lookup"><span data-stu-id="f4ec8-109">Container can go ahead with close immediately.</span></span> <span data-ttu-id="f4ec8-110">Isso pode acontecer se o controle não estiver conectado.</span><span class="sxs-lookup"><span data-stu-id="f4ec8-110">This can happen if the control is not connected.</span></span>

</dd> <dt>

<span data-ttu-id="f4ec8-111"><span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents**</span><span class="sxs-lookup"><span data-stu-id="f4ec8-111"><span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents**</span></span>
</dt> <dd>

<span data-ttu-id="f4ec8-112">O contêiner deve aguardar eventos [**IMsTscAxEvents:: OnDisconnect**](imstscaxevents-ondisconnected.md) ou [**IMsTscAxEvents:: OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span><span class="sxs-lookup"><span data-stu-id="f4ec8-112">Container should wait for events [**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md) or [**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f4ec8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4ec8-113">Requirements</span></span>



| <span data-ttu-id="f4ec8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4ec8-114">Requirement</span></span> | <span data-ttu-id="f4ec8-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f4ec8-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4ec8-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4ec8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f4ec8-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f4ec8-117">Windows 8.1</span></span><br/>                                                                 |
| <span data-ttu-id="f4ec8-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4ec8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f4ec8-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f4ec8-119">Windows Server 2012 R2</span></span><br/>                                                      |
| <span data-ttu-id="f4ec8-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f4ec8-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="f4ec8-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4ec8-121"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4ec8-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4ec8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4ec8-123">**IMsRdpClient::RequestClose**</span><span class="sxs-lookup"><span data-stu-id="f4ec8-123">**IMsRdpClient::RequestClose**</span></span>](imsrdpclient-requestclose.md)
</dt> <dt>

[<span data-ttu-id="f4ec8-124">**IMsTscAxEvents::OnConfirmClose**</span><span class="sxs-lookup"><span data-stu-id="f4ec8-124">**IMsTscAxEvents::OnConfirmClose**</span></span>](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[<span data-ttu-id="f4ec8-125">**IMsTscAxEvents:: ondisconnectd**</span><span class="sxs-lookup"><span data-stu-id="f4ec8-125">**IMsTscAxEvents::OnDisconnected**</span></span>](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

 





