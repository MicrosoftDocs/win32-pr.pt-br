---
description: A tabela a seguir contém códigos de erro específicos para o Microsoft DirectX Media Objects (DMOs). Esses códigos de erro são definidos no arquivo de cabeçalho Mediaerr. h.
ms.assetid: 1ded5656-084d-4315-a414-aebf4a1820dc
title: Códigos de erro DMO (Mediaerr. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76c8cd5e7001751cd2cf9eb7da4d88b2dc100bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747573"
---
# <a name="dmo-error-codes"></a><span data-ttu-id="bdc7c-104">Códigos de erro do DMO</span><span class="sxs-lookup"><span data-stu-id="bdc7c-104">DMO Error Codes</span></span>

<span data-ttu-id="bdc7c-105">A tabela a seguir contém códigos de erro específicos para o Microsoft DirectX Media Objects (DMOs).</span><span class="sxs-lookup"><span data-stu-id="bdc7c-105">The following table contains error codes that are specific to Microsoft DirectX Media Objects (DMOs).</span></span> <span data-ttu-id="bdc7c-106">Esses códigos de erro são definidos no arquivo de cabeçalho Mediaerr. h.</span><span class="sxs-lookup"><span data-stu-id="bdc7c-106">These error codes are defined in the header file Mediaerr.h.</span></span>



| <span data-ttu-id="bdc7c-107">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="bdc7c-107">Constant/value</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="bdc7c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="bdc7c-108">Description</span></span>                                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMO_E_INVALIDSTREAMINDEX"></span><span id="dmo_e_invalidstreamindex"></span><dl> <span data-ttu-id="bdc7c-109"><dt>**DMO \_ E \_ INVALIDSTREAMINDEX**</dt> <dt>0x80040201</dt></span><span class="sxs-lookup"><span data-stu-id="bdc7c-109"><dt>**DMO\_E\_INVALIDSTREAMINDEX**</dt> <dt>0x80040201</dt></span></span> </dl> | <span data-ttu-id="bdc7c-110">Índice de fluxo inválido.</span><span class="sxs-lookup"><span data-stu-id="bdc7c-110">Invalid stream index.</span></span><br/>                                                                                                                                    |
| <span id="DMO_E_INVALIDTYPE"></span><span id="dmo_e_invalidtype"></span><dl> <span data-ttu-id="bdc7c-111"><dt>**DMO \_ E \_ INvalidatype**</dt> <dt>0x80040202</dt></span><span class="sxs-lookup"><span data-stu-id="bdc7c-111"><dt>**DMO\_E\_INVALIDTYPE**</dt> <dt>0x80040202</dt></span></span> </dl>                      | <span data-ttu-id="bdc7c-112">Tipo de mídia inválido.</span><span class="sxs-lookup"><span data-stu-id="bdc7c-112">Invalid media type.</span></span><br/>                                                                                                                                      |
| <span id="DMO_E_TYPE_NOT_SET"></span><span id="dmo_e_type_not_set"></span><dl> <span data-ttu-id="bdc7c-113"><dt>**DMO \_ \_Tipo E \_ não \_ definido**</dt> <dt>0x80040203</dt></span><span class="sxs-lookup"><span data-stu-id="bdc7c-113"><dt>**DMO\_E\_TYPE\_NOT\_SET**</dt> <dt>0x80040203</dt></span></span> </dl>                 | <span data-ttu-id="bdc7c-114">O tipo de mídia não foi definido.</span><span class="sxs-lookup"><span data-stu-id="bdc7c-114">Media type was not set.</span></span> <span data-ttu-id="bdc7c-115">Um ou mais fluxos exigem um tipo de mídia para que essa operação possa ser executada.</span><span class="sxs-lookup"><span data-stu-id="bdc7c-115">One or more streams require a media type before this operation can be performed.</span></span><br/>                                                 |
| <span id="DMO_E_NOTACCEPTING"></span><span id="dmo_e_notaccepting"></span><dl> <span data-ttu-id="bdc7c-116"><dt>**DMO \_ E não \_ aceitar**</dt> <dt>0x80040204</dt></span><span class="sxs-lookup"><span data-stu-id="bdc7c-116"><dt>**DMO\_E\_NOTACCEPTING**</dt> <dt>0x80040204</dt></span></span> </dl>                   | <span data-ttu-id="bdc7c-117">Os dados não podem ser aceitos neste fluxo.</span><span class="sxs-lookup"><span data-stu-id="bdc7c-117">Data cannot be accepted on this stream.</span></span> <span data-ttu-id="bdc7c-118">Talvez seja necessário processar mais dados de saída; consulte [**IMediaObject::P rocessinput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput).</span><span class="sxs-lookup"><span data-stu-id="bdc7c-118">You might need to process more output data; see [**IMediaObject::ProcessInput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput).</span></span><br/> |
| <span id="DMO_E_TYPE_NOT_ACCEPTED"></span><span id="dmo_e_type_not_accepted"></span><dl> <span data-ttu-id="bdc7c-119"><dt>**DMO \_ \_Tipo E \_ não \_ aceito**</dt> <dt>0x80040205</dt></span><span class="sxs-lookup"><span data-stu-id="bdc7c-119"><dt>**DMO\_E\_TYPE\_NOT\_ACCEPTED**</dt> <dt>0x80040205</dt></span></span> </dl>  | <span data-ttu-id="bdc7c-120">O tipo de mídia não foi aceito.</span><span class="sxs-lookup"><span data-stu-id="bdc7c-120">Media type was not accepted.</span></span><br/>                                                                                                                             |
| <span id="DMO_E_NO_MORE_ITEMS"></span><span id="dmo_e_no_more_items"></span><dl> <span data-ttu-id="bdc7c-121"><dt>**DMO \_ E \_ não há \_ mais \_ itens**</dt> <dt>0x80040206</dt></span><span class="sxs-lookup"><span data-stu-id="bdc7c-121"><dt>**DMO\_E\_NO\_MORE\_ITEMS**</dt> <dt>0x80040206</dt></span></span> </dl>              | <span data-ttu-id="bdc7c-122">O índice do tipo de mídia está fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="bdc7c-122">Media-type index is out of range.</span></span><br/>                                                                                                                        |



## <a name="requirements"></a><span data-ttu-id="bdc7c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdc7c-123">Requirements</span></span>



| <span data-ttu-id="bdc7c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdc7c-124">Requirement</span></span> | <span data-ttu-id="bdc7c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="bdc7c-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bdc7c-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bdc7c-126">Header</span></span><br/> | <dl> <span data-ttu-id="bdc7c-127"><dt>Mediaerr. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdc7c-127"><dt>Mediaerr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdc7c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="bdc7c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdc7c-129">Constantes do DMO</span><span class="sxs-lookup"><span data-stu-id="bdc7c-129">DMO Constants</span></span>](dmo-constants.md)
</dt> </dl>

 

 




