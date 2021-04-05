---
description: Contém os intrínsecos da câmera pinhole para o fluxo.
ms.assetid: 7E5E7C60-9C3F-406B-A7DD-A953181CD314
title: Atributo MFStreamExtension_PinholeCameraIntrinsics (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ee9ad848f0b8cc12c2496544d98b4ef17332151
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921355"
---
# <a name="mfstreamextension_pinholecameraintrinsics-attribute"></a><span data-ttu-id="507c2-103">\_Atributo MFStreamExtension PinholeCameraIntrinsics</span><span class="sxs-lookup"><span data-stu-id="507c2-103">MFStreamExtension\_PinholeCameraIntrinsics attribute</span></span>

<span data-ttu-id="507c2-104">Contém os intrínsecos da câmera pinhole para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="507c2-104">Contains the pinhole camera intrinsics for the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="507c2-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="507c2-105">Data type</span></span>

<span data-ttu-id="507c2-106">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="507c2-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="507c2-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="507c2-107">Get/set</span></span>

<span data-ttu-id="507c2-108">Para obter esse atributo, chame [**IMFMediaSourceEx:: Getstreamattributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes).</span><span class="sxs-lookup"><span data-stu-id="507c2-108">To get this attribute, call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes).</span></span>

## <a name="remarks"></a><span data-ttu-id="507c2-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="507c2-109">Remarks</span></span>

<span data-ttu-id="507c2-110">O valor do atributo é um [**MFPinholeCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).</span><span class="sxs-lookup"><span data-stu-id="507c2-110">The value of the attribute is a [**MFPinholeCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).</span></span>

## <a name="requirements"></a><span data-ttu-id="507c2-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="507c2-111">Requirements</span></span>



| <span data-ttu-id="507c2-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="507c2-112">Requirement</span></span> | <span data-ttu-id="507c2-113">Valor</span><span class="sxs-lookup"><span data-stu-id="507c2-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="507c2-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="507c2-114">Minimum supported client</span></span><br/> | <span data-ttu-id="507c2-115">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="507c2-115">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="507c2-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="507c2-116">Minimum supported server</span></span><br/> | <span data-ttu-id="507c2-117">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="507c2-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="507c2-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="507c2-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="507c2-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="507c2-119"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




