---
description: Contém as extrínsecos da câmera para o exemplo.
ms.assetid: C970E958-3866-491A-9806-DB300834360E
title: Atributo MFSampleExtension_CameraExtrinsics (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3340f1ab84061fa00e12fa65960f1b2902690816
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755764"
---
# <a name="mfsampleextension_cameraextrinsics-attribute"></a><span data-ttu-id="8523c-103">\_Atributo MFSampleExtension CameraExtrinsics</span><span class="sxs-lookup"><span data-stu-id="8523c-103">MFSampleExtension\_CameraExtrinsics attribute</span></span>

<span data-ttu-id="8523c-104">Contém as extrínsecos da câmera para o exemplo.</span><span class="sxs-lookup"><span data-stu-id="8523c-104">Contains the camera extrinsics for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="8523c-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="8523c-105">Data type</span></span>

<span data-ttu-id="8523c-106">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="8523c-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="8523c-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="8523c-107">Get/set</span></span>

<span data-ttu-id="8523c-108">Para obter esse atributo, chame [**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="8523c-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="8523c-109">Para definir esse atributo, chame [**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="8523c-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="8523c-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="8523c-110">Applies to</span></span>

[<span data-ttu-id="8523c-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="8523c-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="8523c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="8523c-112">Remarks</span></span>

<span data-ttu-id="8523c-113">O valor do atributo é um [**MFCameraExtrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).</span><span class="sxs-lookup"><span data-stu-id="8523c-113">The value of the attribute is a [**MFCameraExtrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).</span></span>

<span data-ttu-id="8523c-114">Esse atributo é opcional para dar suporte a câmeras que não são calibradas.</span><span class="sxs-lookup"><span data-stu-id="8523c-114">This attribute is optional to support cameras that are not calibrated.</span></span>

## <a name="requirements"></a><span data-ttu-id="8523c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8523c-115">Requirements</span></span>



| <span data-ttu-id="8523c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8523c-116">Requirement</span></span> | <span data-ttu-id="8523c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="8523c-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8523c-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8523c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8523c-119">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8523c-119">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8523c-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8523c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8523c-121">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="8523c-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8523c-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8523c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8523c-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8523c-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8523c-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="8523c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8523c-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8523c-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




