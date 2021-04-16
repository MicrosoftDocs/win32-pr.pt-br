---
title: Enumeração WMDMMessage
description: O tipo de enumeração WMDMMessage define os tipos e os Estados de mensagens.
ms.assetid: 49a77100-8890-4e40-852f-c6fd436f22c5
keywords:
- WMDMMessage de enumeração do Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDMMessage
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7489dc7059f10e1a6f61d1a290f8f664a385f96c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789588"
---
# <a name="wmdmmessage-enumeration"></a><span data-ttu-id="b7c0b-104">Enumeração WMDMMessage</span><span class="sxs-lookup"><span data-stu-id="b7c0b-104">WMDMMessage enumeration</span></span>

<span data-ttu-id="b7c0b-105">O tipo de enumeração **WMDMMessage** define os tipos e os Estados de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b7c0b-105">The **WMDMMessage** enumeration type defines message types and states.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7c0b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7c0b-106">Syntax</span></span>


```C++
enum WMDMMessage {
  WMDM_MSG_DEVICE_ARRIVAL, 
  WMDM_MSG_DEVICE_REMOVAL, 
  WMDM_MSG_MEDIA_ARRIVAL, 
  WMDM_MSG_MEDIA_REMOVAL 

};
```



## <a name="constants"></a><span data-ttu-id="b7c0b-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="b7c0b-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b7c0b-108"><span id="WMDM_MSG_DEVICE_ARRIVAL"></span><span id="wmdm_msg_device_arrival"></span>**\_chegada do \_ dispositivo de msg do WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="b7c0b-108"><span id="WMDM_MSG_DEVICE_ARRIVAL"></span><span id="wmdm_msg_device_arrival"></span>**WMDM\_MSG\_DEVICE\_ARRIVAL**</span></span>
</dt> <dd>

<span data-ttu-id="b7c0b-109">Um dispositivo Windows Media Gerenciador de Dispositivos foi conectado.</span><span class="sxs-lookup"><span data-stu-id="b7c0b-109">A Windows Media Device Manager device has been plugged in.</span></span>

</dd> <dt>

<span data-ttu-id="b7c0b-110"><span id="WMDM_MSG_DEVICE_REMOVAL"></span><span id="wmdm_msg_device_removal"></span>**\_remoção do \_ dispositivo de msg do WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="b7c0b-110"><span id="WMDM_MSG_DEVICE_REMOVAL"></span><span id="wmdm_msg_device_removal"></span>**WMDM\_MSG\_DEVICE\_REMOVAL**</span></span>
</dt> <dd>

<span data-ttu-id="b7c0b-111">Um dispositivo Windows Media Gerenciador de Dispositivos foi removido.</span><span class="sxs-lookup"><span data-stu-id="b7c0b-111">A Windows Media Device Manager device has been removed.</span></span>

</dd> <dt>

<span data-ttu-id="b7c0b-112"><span id="WMDM_MSG_MEDIA_ARRIVAL"></span><span id="wmdm_msg_media_arrival"></span>**\_chegada de \_ mídia de mensagem WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="b7c0b-112"><span id="WMDM_MSG_MEDIA_ARRIVAL"></span><span id="wmdm_msg_media_arrival"></span>**WMDM\_MSG\_MEDIA\_ARRIVAL**</span></span>
</dt> <dd>

<span data-ttu-id="b7c0b-113">A mídia foi inserida em um dispositivo Windows Media Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b7c0b-113">Media has been inserted in a Windows Media Device Manager device.</span></span>

</dd> <dt>

<span data-ttu-id="b7c0b-114"><span id="WMDM_MSG_MEDIA_REMOVAL"></span><span id="wmdm_msg_media_removal"></span>**\_remoção de \_ mídia de mensagem WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="b7c0b-114"><span id="WMDM_MSG_MEDIA_REMOVAL"></span><span id="wmdm_msg_media_removal"></span>**WMDM\_MSG\_MEDIA\_REMOVAL**</span></span>
</dt> <dd>

<span data-ttu-id="b7c0b-115">A mídia foi removida de um dispositivo Windows Media Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b7c0b-115">Media has been removed from a Windows Media Device Manager device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7c0b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7c0b-116">Requirements</span></span>



| <span data-ttu-id="b7c0b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7c0b-117">Requirement</span></span> | <span data-ttu-id="b7c0b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b7c0b-118">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b7c0b-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b7c0b-119">Header</span></span><br/> | <dl> <span data-ttu-id="b7c0b-120"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b7c0b-120"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7c0b-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7c0b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7c0b-122">**Tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="b7c0b-122">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





