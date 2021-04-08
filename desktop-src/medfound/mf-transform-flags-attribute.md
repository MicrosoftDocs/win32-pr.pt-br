---
description: Contém sinalizadores para um objeto de ativação de Media Foundation transformação (MFT).
ms.assetid: de377132-19b0-4c8c-882e-193c31420739
title: Atributo MF_TRANSFORM_FLAGS_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2f3e334b83bbe8ce50f8770eb33e1e7a4c799c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921125"
---
# <a name="mf_transform_flags_attribute-attribute"></a><span data-ttu-id="b02b5-103">\_Atributo de \_ atributo de sinalizadores de transformação MF \_</span><span class="sxs-lookup"><span data-stu-id="b02b5-103">MF\_TRANSFORM\_FLAGS\_Attribute attribute</span></span>

<span data-ttu-id="b02b5-104">Contém sinalizadores para um objeto de ativação de Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="b02b5-104">Contains flags for a Media Foundation transform (MFT) activation object.</span></span>

## <a name="data-type"></a><span data-ttu-id="b02b5-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b02b5-105">Data type</span></span>

<span data-ttu-id="b02b5-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b02b5-106">**UINT32**</span></span>

<span data-ttu-id="b02b5-107">O valor é um or **bit a** bit de sinalizadores da enumeração de [**\_ \_ \_ sinalizador de enumeração de MFT**](/windows/win32/api/mfapi/ne-mfapi-_mft_enum_flag) .</span><span class="sxs-lookup"><span data-stu-id="b02b5-107">The value is a bitwise **OR** of flags from the [**\_MFT\_ENUM\_FLAG**](/windows/win32/api/mfapi/ne-mfapi-_mft_enum_flag) enumeration.</span></span>

## <a name="getset"></a><span data-ttu-id="b02b5-108">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="b02b5-108">Get/set</span></span>

<span data-ttu-id="b02b5-109">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b02b5-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b02b5-110">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="b02b5-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="b02b5-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b02b5-111">Remarks</span></span>

<span data-ttu-id="b02b5-112">Esse atributo é definido nos ponteiros do [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retornados pela função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="b02b5-112">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span> <span data-ttu-id="b02b5-113">O atributo contém sinalizadores que descrevem o MFT.</span><span class="sxs-lookup"><span data-stu-id="b02b5-113">The attribute contains flags that describe the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="b02b5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b02b5-114">Requirements</span></span>



| <span data-ttu-id="b02b5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b02b5-115">Requirement</span></span> | <span data-ttu-id="b02b5-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b02b5-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b02b5-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b02b5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b02b5-118">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b02b5-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="b02b5-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b02b5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b02b5-120">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="b02b5-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="b02b5-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b02b5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b02b5-122"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="b02b5-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b02b5-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="b02b5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b02b5-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b02b5-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b02b5-125">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="b02b5-125">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 
