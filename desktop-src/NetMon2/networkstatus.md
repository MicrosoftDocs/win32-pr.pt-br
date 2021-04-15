---
description: A estrutura NETWORKSTATUS descreve o status atual do NPP.
ms.assetid: e5e07480-cfc3-408f-9ca2-48a697e4b875
title: Estrutura NETWORKSTATUS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 067a57dabfb5222deb27de44c60c6eb121cd8c36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506252"
---
# <a name="networkstatus-structure"></a><span data-ttu-id="41fad-103">Estrutura NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="41fad-103">NETWORKSTATUS structure</span></span>

<span data-ttu-id="41fad-104">A estrutura **NETWORKSTATUS** descreve o status atual do NPP.</span><span class="sxs-lookup"><span data-stu-id="41fad-104">The **NETWORKSTATUS** structure describes the current status of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="41fad-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41fad-105">Syntax</span></span>


```C++
typedef struct _NETWORKSTATUS {
  DWORD State;
  DWORD Flags;
} NETWORKSTATUS, *LPNETWORKSTATUS;
```



## <a name="members"></a><span data-ttu-id="41fad-106">Membros</span><span class="sxs-lookup"><span data-stu-id="41fad-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="41fad-107">**State**</span><span class="sxs-lookup"><span data-stu-id="41fad-107">**State**</span></span>
</dt> <dd>

<span data-ttu-id="41fad-108">Indica o estado atual do NPP.</span><span class="sxs-lookup"><span data-stu-id="41fad-108">Indicates the current state of the NPP.</span></span>



| <span data-ttu-id="41fad-109">Valor</span><span class="sxs-lookup"><span data-stu-id="41fad-109">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="41fad-110">Significado</span><span class="sxs-lookup"><span data-stu-id="41fad-110">Meaning</span></span>                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="NETWORKSTATUS_STATE_VOID"></span><span id="networkstatus_state_void"></span><dl> <span data-ttu-id="41fad-111"><dt>**NETWORKSTATUS de \_ estado \_ nulo**</dt></span><span class="sxs-lookup"><span data-stu-id="41fad-111"><dt>**NETWORKSTATUS\_STATE\_VOID**</dt></span></span> </dl>                | <span data-ttu-id="41fad-112">O NPP não está conectado ou está conectado e a captura não foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="41fad-112">The NPP is not connected, or it is connected and the capture is not started.</span></span><br/> |
| <span id="NETWORKSTATUS_STATE_CAPTURING"></span><span id="networkstatus_state_capturing"></span><dl> <span data-ttu-id="41fad-113"><dt>**\_captura de estado NETWORKSTATUS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="41fad-113"><dt>**NETWORKSTATUS\_STATE\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="41fad-114">O NPP está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="41fad-114">The NPP is capturing data.</span></span><br/>                                                   |
| <span id="NETWORKSTATUS_STATE_PAUSED"></span><span id="networkstatus_state_paused"></span><dl> <span data-ttu-id="41fad-115"><dt>**Estado de NETWORKSTATUS \_ \_ pausado**</dt></span><span class="sxs-lookup"><span data-stu-id="41fad-115"><dt>**NETWORKSTATUS\_STATE\_PAUSED**</dt></span></span> </dl>          | <span data-ttu-id="41fad-116">O NPP foi pausado durante a captura de dados.</span><span class="sxs-lookup"><span data-stu-id="41fad-116">The NPP has paused while capturing data.</span></span><br/>                                     |



 

</dd> <dt>

<span data-ttu-id="41fad-117">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="41fad-117">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="41fad-118">Sinalizadores que descrevem o estado atual do NPP.</span><span class="sxs-lookup"><span data-stu-id="41fad-118">Flags that describe the current state of the NPP.</span></span>



| <span data-ttu-id="41fad-119">Valor</span><span class="sxs-lookup"><span data-stu-id="41fad-119">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="41fad-120">Significado</span><span class="sxs-lookup"><span data-stu-id="41fad-120">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="NETWORKSTATUS_FLAGS_TRIGGER_PENDING"></span><span id="networkstatus_flags_trigger_pending"></span><dl> <span data-ttu-id="41fad-121"><dt>**\_gatilho de sinalizadores NETWORKSTATUS \_ \_ pendentes**</dt></span><span class="sxs-lookup"><span data-stu-id="41fad-121"><dt>**NETWORKSTATUS\_FLAGS\_TRIGGER\_PENDING**</dt></span></span> </dl> | <span data-ttu-id="41fad-122">Há um gatilho pendente para o NPP.</span><span class="sxs-lookup"><span data-stu-id="41fad-122">There is a trigger pending for the NPP.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41fad-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="41fad-123">Remarks</span></span>

<span data-ttu-id="41fad-124">Ao usar essa estrutura, você deve alocar a memória para a estrutura antes que ela possa ser usada e liberar a memória quando a estrutura não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="41fad-124">When using this structure, you must allocate the memory for the structure before it can be used and free the memory when the structure is no longer needed.</span></span>

<span data-ttu-id="41fad-125">A lista ver também na parte inferior deste tópico lista todos os métodos que usam essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="41fad-125">The See Also list at the bottom of this topic lists all the methods that use this structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="41fad-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41fad-126">Requirements</span></span>



| <span data-ttu-id="41fad-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="41fad-127">Requirement</span></span> | <span data-ttu-id="41fad-128">Valor</span><span class="sxs-lookup"><span data-stu-id="41fad-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="41fad-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41fad-129">Minimum supported client</span></span><br/> | <span data-ttu-id="41fad-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="41fad-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="41fad-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41fad-131">Minimum supported server</span></span><br/> | <span data-ttu-id="41fad-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="41fad-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="41fad-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="41fad-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="41fad-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="41fad-134"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41fad-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="41fad-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41fad-136">IDelaydC:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="41fad-136">IDelaydC::QueryStatus</span></span>](idelaydc-querystatus.md)
</dt> <dt>

[<span data-ttu-id="41fad-137">IESP:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="41fad-137">IESP::QueryStatus</span></span>](iesp-querystatus.md)
</dt> <dt>

[<span data-ttu-id="41fad-138">IRTC:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="41fad-138">IRTC::QueryStatus</span></span>](irtc-querystatus.md)
</dt> <dt>

[<span data-ttu-id="41fad-139">IStats:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="41fad-139">IStats::QueryStatus</span></span>](istats-querystatus.md)
</dt> </dl>

 

 




