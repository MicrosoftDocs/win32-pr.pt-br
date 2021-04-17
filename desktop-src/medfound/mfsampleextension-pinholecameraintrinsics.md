---
description: Contém os intrínsecos da câmera pinhole para o exemplo.
ms.assetid: AF7EA6A0-90C5-49A8-AD68-776BF770A448
title: Atributo MFSampleExtension_PinholeCameraIntrinsics (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb9e78641c0baab0e9eda3083aafaf8fe92229f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790397"
---
# <a name="mfsampleextension_pinholecameraintrinsics-attribute"></a><span data-ttu-id="5c7d3-103">\_Atributo MFSampleExtension PinholeCameraIntrinsics</span><span class="sxs-lookup"><span data-stu-id="5c7d3-103">MFSampleExtension\_PinholeCameraIntrinsics attribute</span></span>

<span data-ttu-id="5c7d3-104">Contém os intrínsecos da câmera pinhole para o exemplo.</span><span class="sxs-lookup"><span data-stu-id="5c7d3-104">Contains the pinhole camera intrinsics for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="5c7d3-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5c7d3-105">Data type</span></span>

<span data-ttu-id="5c7d3-106">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="5c7d3-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="5c7d3-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="5c7d3-107">Get/set</span></span>

<span data-ttu-id="5c7d3-108">Para obter esse atributo, chame [**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="5c7d3-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="5c7d3-109">Para definir esse atributo, chame [**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="5c7d3-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="5c7d3-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="5c7d3-110">Applies to</span></span>

[<span data-ttu-id="5c7d3-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="5c7d3-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="5c7d3-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c7d3-112">Remarks</span></span>

<span data-ttu-id="5c7d3-113">O valor do atributo é um [**MFPinholeCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).</span><span class="sxs-lookup"><span data-stu-id="5c7d3-113">The value of the attribute is a [**MFPinholeCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).</span></span>

<span data-ttu-id="5c7d3-114">Esse atributo é opcional para dar suporte a câmeras que não são calibradas.</span><span class="sxs-lookup"><span data-stu-id="5c7d3-114">This attribute is optional to support cameras that are not calibrated.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c7d3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c7d3-115">Requirements</span></span>



| <span data-ttu-id="5c7d3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c7d3-116">Requirement</span></span> | <span data-ttu-id="5c7d3-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5c7d3-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5c7d3-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c7d3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5c7d3-119">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5c7d3-119">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5c7d3-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c7d3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5c7d3-121">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="5c7d3-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5c7d3-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5c7d3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c7d3-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c7d3-123"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




