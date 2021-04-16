---
description: Especifica se o IMFTransform está usando o DRM de hardware.
title: MFT_USING_HARDWARE_DRM (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e6dbacedbf5fd9298e4da5154bd82fcc9f39bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461216"
---
# <a name="mft_using_hardware_drm-attribute"></a><span data-ttu-id="bb99e-103">MFT \_ usando \_ atributo de DRM de hardware \_</span><span class="sxs-lookup"><span data-stu-id="bb99e-103">MFT\_USING\_HARDWARE\_DRM attribute</span></span>

<span data-ttu-id="bb99e-104">Especifica se o IMFTransform está usando o DRM de hardware.</span><span class="sxs-lookup"><span data-stu-id="bb99e-104">Specifies whether the IMFTransform is using hardware DRM.</span></span>

## <a name="data-type"></a><span data-ttu-id="bb99e-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="bb99e-105">Data type</span></span>

<span data-ttu-id="bb99e-106">**UINT32** (Tratado como **bool**)</span><span class="sxs-lookup"><span data-stu-id="bb99e-106">**UINT32** (treated as **BOOL**)</span></span>

## <a name="getset"></a><span data-ttu-id="bb99e-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="bb99e-107">Get/set</span></span>

<span data-ttu-id="bb99e-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="bb99e-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="bb99e-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="bb99e-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="bb99e-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="bb99e-110">Applies to</span></span>

[<span data-ttu-id="bb99e-111">**IMTransfrom**</span><span class="sxs-lookup"><span data-stu-id="bb99e-111">**IMTransfrom**</span></span>](/windows/win32/api/mftransform/nn-mftransform-imftransform)

## <a name="remarks"></a><span data-ttu-id="bb99e-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb99e-112">Remarks</span></span>

<span data-ttu-id="bb99e-113">Se um MFT Decrypter especificar esse atributo definido como 1, ele estará usando o DRM de hardware.</span><span class="sxs-lookup"><span data-stu-id="bb99e-113">If an MFT decrypter specifies this attribute set to 1, then it is using hardware DRM.</span></span> <span data-ttu-id="bb99e-114">Se um MFT Decrypter especificar esse atributo definido como 0, ele não estará usando o DRM de hardware.</span><span class="sxs-lookup"><span data-stu-id="bb99e-114">If an MFT decrypter specifies this attribute set to 0, then it is not using hardware DRM.</span></span> <span data-ttu-id="bb99e-115">Se um Decrypter MFT não especificar esse atributo ou especificá-lo com um valor diferente, ele não será (ou não poderá) indicar se está usando o DRM de hardware.</span><span class="sxs-lookup"><span data-stu-id="bb99e-115">If an MFT decrypter does not specify this attribute or specifies it with a different value, then it does not (or is unable to) indicate whether it is using hardware DRM.</span></span>


<span data-ttu-id="bb99e-116">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="bb99e-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb99e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb99e-117">Requirements</span></span>



| <span data-ttu-id="bb99e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb99e-118">Requirement</span></span> | <span data-ttu-id="bb99e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="bb99e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb99e-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb99e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bb99e-121">Atualização de abril de 2020 do Windows 10</span><span class="sxs-lookup"><span data-stu-id="bb99e-121">Windows 10 April 2020 Update</span></span>   <br/>                                       |
| <span data-ttu-id="bb99e-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb99e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bb99e-123">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="bb99e-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="bb99e-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bb99e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb99e-125"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb99e-125"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb99e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb99e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb99e-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bb99e-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[<span data-ttu-id="bb99e-128">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="bb99e-128">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




