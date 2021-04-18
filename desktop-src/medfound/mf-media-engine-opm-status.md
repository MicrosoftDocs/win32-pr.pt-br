---
description: Define o status do Gerenciador de proteção de saída (OPM).
ms.assetid: 7C4D88F6-369B-4364-90C4-6D0F8DD1523B
title: Enumeração de MF_MEDIA_ENGINE_OPM_STATUS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_OPM_STATUS
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 73585bf63bc559f30ce114730274e30518497b05
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105812802"
---
# <a name="mf_media_engine_opm_status-enumeration"></a><span data-ttu-id="d3d6b-103">\_Enumeração de \_ status de OPM do mecanismo de mídia MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="d3d6b-103">MF\_MEDIA\_ENGINE\_OPM\_STATUS enumeration</span></span>

<span data-ttu-id="d3d6b-104">Define o status do [Gerenciador de proteção de saída](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="d3d6b-104">Defines the status of the [Output Protection Manager](output-protection-manager.md) (OPM).</span></span>

## <a name="syntax"></a><span data-ttu-id="d3d6b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3d6b-105">Syntax</span></span>


```C++
typedef enum _MF_MEDIA_ENGINE_OPM_STATUS { 
  MF_MEDIA_ENGINE_OPM_NOT_REQUESTED           =  0,
  MF_MEDIA_ENGINE_OPM_ESTABLISHED             = 1,
  MF_MEDIA_ENGINE_OPM_FAILED_VM               = 2,
  MF_MEDIA_ENGINE_OPM_FAILED_BDA              = 3,
  MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER  = 4,
  MF_MEDIA_ENGINE_OPM_FAILED                  = 5
} MF_MEDIA_ENGINE_OPM_STATUS;
```



## <a name="constants"></a><span data-ttu-id="d3d6b-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="d3d6b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d3d6b-107"><span id="MF_MEDIA_ENGINE_OPM_NOT_REQUESTED"></span><span id="mf_media_engine_opm_not_requested"></span>**\_OPM do mecanismo de mídia MF \_ \_ \_ não \_ solicitado**</span><span class="sxs-lookup"><span data-stu-id="d3d6b-107"><span id="MF_MEDIA_ENGINE_OPM_NOT_REQUESTED"></span><span id="mf_media_engine_opm_not_requested"></span>**MF\_MEDIA\_ENGINE\_OPM\_NOT\_REQUESTED**</span></span>
</dt> <dd>

<span data-ttu-id="d3d6b-108">Status padrão.</span><span class="sxs-lookup"><span data-stu-id="d3d6b-108">Default status.</span></span> <span data-ttu-id="d3d6b-109">Usado para retornar o status correto quando o conteúdo está desprotegido.</span><span class="sxs-lookup"><span data-stu-id="d3d6b-109">Used to return the correct status when the content is unprotected.</span></span>

</dd> <dt>

<span data-ttu-id="d3d6b-110"><span id="MF_MEDIA_ENGINE_OPM_ESTABLISHED"></span><span id="mf_media_engine_opm_established"></span>**\_OPM do mecanismo de mídia MF \_ \_ \_ estabelecido**</span><span class="sxs-lookup"><span data-stu-id="d3d6b-110"><span id="MF_MEDIA_ENGINE_OPM_ESTABLISHED"></span><span id="mf_media_engine_opm_established"></span>**MF\_MEDIA\_ENGINE\_OPM\_ESTABLISHED**</span></span>
</dt> <dd>

<span data-ttu-id="d3d6b-111">OPM estabelecido com êxito.</span><span class="sxs-lookup"><span data-stu-id="d3d6b-111">OPM successfully established.</span></span>

</dd> <dt>

<span data-ttu-id="d3d6b-112"><span id="MF_MEDIA_ENGINE_OPM_FAILED_VM"></span><span id="mf_media_engine_opm_failed_vm"></span>**\_ \_ \_ \_ VM com falha em OPM do mecanismo de mídia \_ MF**</span><span class="sxs-lookup"><span data-stu-id="d3d6b-112"><span id="MF_MEDIA_ENGINE_OPM_FAILED_VM"></span><span id="mf_media_engine_opm_failed_vm"></span>**MF\_MEDIA\_ENGINE\_OPM\_FAILED\_VM**</span></span>
</dt> <dd>

<span data-ttu-id="d3d6b-113">OPM falhou porque está sendo executado em uma VM (máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="d3d6b-113">OPM failed because running in a virtual machined (VM).</span></span>

</dd> <dt>

<span data-ttu-id="d3d6b-114"><span id="MF_MEDIA_ENGINE_OPM_FAILED_BDA"></span><span id="mf_media_engine_opm_failed_bda"></span>**o \_ mecanismo de mídia MF \_ \_ OPM \_ falhou em \_ BDA**</span><span class="sxs-lookup"><span data-stu-id="d3d6b-114"><span id="MF_MEDIA_ENGINE_OPM_FAILED_BDA"></span><span id="mf_media_engine_opm_failed_bda"></span>**MF\_MEDIA\_ENGINE\_OPM\_FAILED\_BDA**</span></span>
</dt> <dd>

<span data-ttu-id="d3d6b-115">OPM falhou porque não há driver de gráficos e o sistema está usando o adaptador de vídeo básico (BDA).</span><span class="sxs-lookup"><span data-stu-id="d3d6b-115">OPM failed because there is no graphics driver and the system is using Basic Display Adapter (BDA).</span></span>

</dd> <dt>

<span data-ttu-id="d3d6b-116"><span id="MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER"></span><span id="mf_media_engine_opm_failed_unsigned_driver"></span>**o \_ Driver de mídia MF \_ \_ OPM \_ falhou \_ sem sinal \_**</span><span class="sxs-lookup"><span data-stu-id="d3d6b-116"><span id="MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER"></span><span id="mf_media_engine_opm_failed_unsigned_driver"></span>**MF\_MEDIA\_ENGINE\_OPM\_FAILED\_UNSIGNED\_DRIVER**</span></span>
</dt> <dd>

<span data-ttu-id="d3d6b-117">OPM falhou porque o driver de gráficos não é assinado por PE, voltando para distorção.</span><span class="sxs-lookup"><span data-stu-id="d3d6b-117">OPM failed because the graphics driver is not PE signed, falling back to WARP.</span></span>

</dd> <dt>

<span data-ttu-id="d3d6b-118"><span id="MF_MEDIA_ENGINE_OPM_FAILED"></span><span id="mf_media_engine_opm_failed"></span>**\_falha em \_ OPM do mecanismo de mídia MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d3d6b-118"><span id="MF_MEDIA_ENGINE_OPM_FAILED"></span><span id="mf_media_engine_opm_failed"></span>**MF\_MEDIA\_ENGINE\_OPM\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="d3d6b-119">OPM falhou por outros motivos.</span><span class="sxs-lookup"><span data-stu-id="d3d6b-119">OPM failed for other reasons.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d3d6b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3d6b-120">Requirements</span></span>



| <span data-ttu-id="d3d6b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3d6b-121">Requirement</span></span> | <span data-ttu-id="d3d6b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d3d6b-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3d6b-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3d6b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d3d6b-124">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d3d6b-124">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d3d6b-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3d6b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d3d6b-126">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="d3d6b-126">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d3d6b-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="d3d6b-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d3d6b-128"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d3d6b-128"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3d6b-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3d6b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3d6b-130">Enumerações de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d3d6b-130">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




