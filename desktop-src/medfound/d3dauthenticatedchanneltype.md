---
description: Especifica o tipo de canal do Direct3D autenticado.
ms.assetid: 99a7664e-b0c8-4e66-ad3b-c6ad039ef6eb
title: Enumeração D3DAUTHENTICATEDCHANNELTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNELTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5c0cab8a0a208bfb1a005166740dcc64c319c6e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811202"
---
# <a name="d3dauthenticatedchanneltype-enumeration"></a><span data-ttu-id="0fc10-103">Enumeração D3DAUTHENTICATEDCHANNELTYPE</span><span class="sxs-lookup"><span data-stu-id="0fc10-103">D3DAUTHENTICATEDCHANNELTYPE enumeration</span></span>

<span data-ttu-id="0fc10-104">Especifica o tipo de canal do Direct3D autenticado.</span><span class="sxs-lookup"><span data-stu-id="0fc10-104">Specifies the type of Direct3D authenticated channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fc10-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0fc10-105">Syntax</span></span>


```C++
typedef enum  { 
  D3DAUTHENTICATEDCHANNEL_D3D9             = 1,
  D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE  = 2,
  D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE  = 3
} D3DAUTHENTICATEDCHANNELTYPE;
```



## <a name="constants"></a><span data-ttu-id="0fc10-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="0fc10-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0fc10-107"><span id="D3DAUTHENTICATEDCHANNEL_D3D9"></span><span id="d3dauthenticatedchannel_d3d9"></span>**D3DAUTHENTICATEDCHANNEL \_ d3d9**</span><span class="sxs-lookup"><span data-stu-id="0fc10-107"><span id="D3DAUTHENTICATEDCHANNEL_D3D9"></span><span id="d3dauthenticatedchannel_d3d9"></span>**D3DAUTHENTICATEDCHANNEL\_D3D9**</span></span>
</dt> <dd>

<span data-ttu-id="0fc10-108">Canal do Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="0fc10-108">Direct3D 9 channel.</span></span> <span data-ttu-id="0fc10-109">Esse canal fornece comunicação com o tempo de execução do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="0fc10-109">This channel provides communication with the Direct3D runtime.</span></span>

</dd> <dt>

<span data-ttu-id="0fc10-110"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE"></span><span id="d3dauthenticatedchannel_driver_software"></span>**\_Software de driver D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="0fc10-110"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE"></span><span id="d3dauthenticatedchannel_driver_software"></span>**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>
</dt> <dd>

<span data-ttu-id="0fc10-111">Canal de driver de software.</span><span class="sxs-lookup"><span data-stu-id="0fc10-111">Software driver channel.</span></span> <span data-ttu-id="0fc10-112">Esse canal fornece comunicação com um driver que implementa mecanismos de proteção de conteúdo em software.</span><span class="sxs-lookup"><span data-stu-id="0fc10-112">This channel provides communication with a driver that implements content protection mechanisms in software.</span></span>

</dd> <dt>

<span data-ttu-id="0fc10-113"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE"></span><span id="d3dauthenticatedchannel_driver_hardware"></span>**\_Hardware do driver D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="0fc10-113"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE"></span><span id="d3dauthenticatedchannel_driver_hardware"></span>**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
</dt> <dd>

<span data-ttu-id="0fc10-114">Canal de driver de hardware.</span><span class="sxs-lookup"><span data-stu-id="0fc10-114">Hardware driver channel.</span></span> <span data-ttu-id="0fc10-115">Esse canal fornece comunicação com um driver que implementa mecanismos de proteção de conteúdo no hardware de GPU.</span><span class="sxs-lookup"><span data-stu-id="0fc10-115">This channel provides communication with a driver that implements content protection mechanisms in the GPU hardware.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0fc10-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fc10-116">Requirements</span></span>



| <span data-ttu-id="0fc10-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fc10-117">Requirement</span></span> | <span data-ttu-id="0fc10-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0fc10-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fc10-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fc10-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0fc10-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0fc10-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0fc10-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fc10-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0fc10-122">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="0fc10-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0fc10-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0fc10-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fc10-124"><dt>D3d9types. h (incluir D3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0fc10-124"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fc10-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="0fc10-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fc10-126">Enumerações de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="0fc10-126">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)
</dt> <dt>

[<span data-ttu-id="0fc10-127">**IDirect3DDevice9Video::CreateAuthenticatedChannel**</span><span class="sxs-lookup"><span data-stu-id="0fc10-127">**IDirect3DDevice9Video::CreateAuthenticatedChannel**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel)
</dt> </dl>

 

 




