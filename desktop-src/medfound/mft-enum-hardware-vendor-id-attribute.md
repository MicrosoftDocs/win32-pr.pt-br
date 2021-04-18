---
description: Especifica a ID do fornecedor para um Microsoft Media Foundation baseado em hardware.
ms.assetid: AA31639F-EF70-4454-AC61-60755CAA684A
title: MFT_ENUM_HARDWARE_VENDOR_ID_Attribute atributo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c4d92585936e52cbb0b9b65201a5de0d3a02b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771766"
---
# <a name="mft_enum_hardware_vendor_id_attribute-attribute"></a><span data-ttu-id="1b4d4-103">\_Atributo de \_ \_ \_ atributo ID de fornecedor de hardware de enumeração de MFT \_</span><span class="sxs-lookup"><span data-stu-id="1b4d4-103">MFT\_ENUM\_HARDWARE\_VENDOR\_ID\_Attribute attribute</span></span>

<span data-ttu-id="1b4d4-104">Especifica a ID do fornecedor para uma transformação de Microsoft Media Foundation baseada em hardware (MFT).</span><span class="sxs-lookup"><span data-stu-id="1b4d4-104">Specifies the vendor ID for a hardware-based Microsoft Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="1b4d4-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1b4d4-105">Data type</span></span>

<span data-ttu-id="1b4d4-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="1b4d4-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="1b4d4-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="1b4d4-107">Get/set</span></span>

<span data-ttu-id="1b4d4-108">Para obter esse atributo, chame [_ *IMFAttributes:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="1b4d4-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="1b4d4-109">Para definir esse atributo, chame [**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="1b4d4-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="1b4d4-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b4d4-110">Remarks</span></span>

<span data-ttu-id="1b4d4-111">Esse atributo é informativo e opcional.</span><span class="sxs-lookup"><span data-stu-id="1b4d4-111">This attribute is informational and optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b4d4-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b4d4-112">Requirements</span></span>



| <span data-ttu-id="1b4d4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b4d4-113">Requirement</span></span> | <span data-ttu-id="1b4d4-114">Valor</span><span class="sxs-lookup"><span data-stu-id="1b4d4-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b4d4-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b4d4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1b4d4-116">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1b4d4-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="1b4d4-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b4d4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1b4d4-118">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1b4d4-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="1b4d4-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1b4d4-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b4d4-120"><dt>Mftransform. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1b4d4-120"><dt>Mftransform.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b4d4-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b4d4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b4d4-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1b4d4-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1b4d4-123">MFTs de hardware</span><span class="sxs-lookup"><span data-stu-id="1b4d4-123">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="1b4d4-124">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="1b4d4-124">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




