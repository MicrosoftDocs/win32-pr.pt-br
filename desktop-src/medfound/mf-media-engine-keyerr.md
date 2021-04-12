---
description: Define códigos de erro de chave de mídia para o mecanismo de mídia.
ms.assetid: F6E13260-74A2-40D0-A704-4E1CDB16B8D8
title: Enumeração de MF_MEDIA_ENGINE_KEYERR
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_KEYERR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 22dd22a7771f5d1e9466709f0b0da9ee936ef2b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297918"
---
# <a name="mf_media_engine_keyerr-enumeration"></a><span data-ttu-id="9c87f-103">\_ \_ Enumeração KEYERR do mecanismo de mídia MF \_</span><span class="sxs-lookup"><span data-stu-id="9c87f-103">MF\_MEDIA\_ENGINE\_KEYERR enumeration</span></span>

<span data-ttu-id="9c87f-104">Define códigos de erro de chave de mídia para o mecanismo de mídia.</span><span class="sxs-lookup"><span data-stu-id="9c87f-104">Defines media key error codes for the media engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c87f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c87f-105">Syntax</span></span>


```C++
typedef enum _MF_MEDIA_ENGINE_KEYERR { 
  MF_MEDIAENGINE_KEYERR_UNKNOWN          = 1,
  MF_MEDIAENGINE_KEYERR_CLIENT           = 2,
  MF_MEDIAENGINE_KEYERR_SERVICE          = 3,
  MF_MEDIAENGINE_KEYERR_OUTPUT           = 4,
  MF_MEDIAENGINE_KEYERR_HARDWARECHANGE   = 5,
  MF_MEDIAENGINE_KEYERR_DOMAIN           = 6
} MF_MEDIA_ENGINE_KEYERR;
```



## <a name="constants"></a><span data-ttu-id="9c87f-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="9c87f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9c87f-107"><span id="MF_MEDIAENGINE_KEYERR_UNKNOWN"></span><span id="mf_mediaengine_keyerr_unknown"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="9c87f-107"><span id="MF_MEDIAENGINE_KEYERR_UNKNOWN"></span><span id="mf_mediaengine_keyerr_unknown"></span>**MF\_MEDIAENGINE\_KEYERR\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="9c87f-108">Ocorreu um erro desconhecido.</span><span class="sxs-lookup"><span data-stu-id="9c87f-108">Unknown error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="9c87f-109"><span id="MF_MEDIAENGINE_KEYERR_CLIENT"></span><span id="mf_mediaengine_keyerr_client"></span>**\_cliente MF MEDIAENGINE \_ KEYERR \_**</span><span class="sxs-lookup"><span data-stu-id="9c87f-109"><span id="MF_MEDIAENGINE_KEYERR_CLIENT"></span><span id="mf_mediaengine_keyerr_client"></span>**MF\_MEDIAENGINE\_KEYERR\_CLIENT**</span></span>
</dt> <dd>

<span data-ttu-id="9c87f-110">Ocorreu um erro com o cliente.</span><span class="sxs-lookup"><span data-stu-id="9c87f-110">An error with the client occurred.</span></span>

</dd> <dt>

<span data-ttu-id="9c87f-111"><span id="MF_MEDIAENGINE_KEYERR_SERVICE"></span><span id="mf_mediaengine_keyerr_service"></span>**\_serviço MEDIAENGINE \_ KEYERR \_ MF**</span><span class="sxs-lookup"><span data-stu-id="9c87f-111"><span id="MF_MEDIAENGINE_KEYERR_SERVICE"></span><span id="mf_mediaengine_keyerr_service"></span>**MF\_MEDIAENGINE\_KEYERR\_SERVICE**</span></span>
</dt> <dd>

<span data-ttu-id="9c87f-112">Ocorreu um erro com o serviço.</span><span class="sxs-lookup"><span data-stu-id="9c87f-112">An error with the service occurred.</span></span>

</dd> <dt>

<span data-ttu-id="9c87f-113"><span id="MF_MEDIAENGINE_KEYERR_OUTPUT"></span><span id="mf_mediaengine_keyerr_output"></span>**\_saída de \_ KEYERR \_ MEDIAENGINE MF**</span><span class="sxs-lookup"><span data-stu-id="9c87f-113"><span id="MF_MEDIAENGINE_KEYERR_OUTPUT"></span><span id="mf_mediaengine_keyerr_output"></span>**MF\_MEDIAENGINE\_KEYERR\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="9c87f-114">Ocorreu um erro com a saída.</span><span class="sxs-lookup"><span data-stu-id="9c87f-114">An error with the output occurred.</span></span>

</dd> <dt>

<span data-ttu-id="9c87f-115"><span id="MF_MEDIAENGINE_KEYERR_HARDWARECHANGE_"></span><span id="mf_mediaengine_keyerr_hardwarechange_"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ HARDWARECHANGE**</span><span class="sxs-lookup"><span data-stu-id="9c87f-115"><span id="MF_MEDIAENGINE_KEYERR_HARDWARECHANGE_"></span><span id="mf_mediaengine_keyerr_hardwarechange_"></span>**MF\_MEDIAENGINE\_KEYERR\_HARDWARECHANGE**</span></span> 
</dt> <dd>

<span data-ttu-id="9c87f-116">Ocorreu um erro relacionado a uma alteração de hardware.</span><span class="sxs-lookup"><span data-stu-id="9c87f-116">An error occurred related to a hardware change.</span></span>

</dd> <dt>

<span data-ttu-id="9c87f-117"><span id="MF_MEDIAENGINE_KEYERR_DOMAIN"></span><span id="mf_mediaengine_keyerr_domain"></span>**\_MEDIAENGINE MF \_ KEYERR \_ domínio**</span><span class="sxs-lookup"><span data-stu-id="9c87f-117"><span id="MF_MEDIAENGINE_KEYERR_DOMAIN"></span><span id="mf_mediaengine_keyerr_domain"></span>**MF\_MEDIAENGINE\_KEYERR\_DOMAIN**</span></span>
</dt> <dd>

<span data-ttu-id="9c87f-118">Ocorreu um erro com o domínio.</span><span class="sxs-lookup"><span data-stu-id="9c87f-118">An error with the domain occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c87f-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c87f-119">Remarks</span></span>

<span data-ttu-id="9c87f-120">**MF \_ O \_ mecanismo \_ de mídia KEYERR** é usado com o parâmetro de *código* de [**IMFMediaKeySessionNotify:: keyerror**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysessionnotify-keyerror) e o valor de *código* retornado de [**IMFMediaKeySession:: GetError**](imfmediakeysession-geterror.md).</span><span class="sxs-lookup"><span data-stu-id="9c87f-120">**MF\_MEDIA\_ENGINE\_KEYERR** is used with the *code* parameter of [**IMFMediaKeySessionNotify::KeyError**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysessionnotify-keyerror) and the *code* value returned from [**IMFMediaKeySession::GetError**](imfmediakeysession-geterror.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c87f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c87f-121">Requirements</span></span>



| <span data-ttu-id="9c87f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c87f-122">Requirement</span></span> | <span data-ttu-id="9c87f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="9c87f-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c87f-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c87f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9c87f-125">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9c87f-125">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9c87f-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c87f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9c87f-127">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="9c87f-127">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9c87f-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="9c87f-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9c87f-129"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9c87f-129"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c87f-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c87f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c87f-131">Enumerações de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9c87f-131">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




