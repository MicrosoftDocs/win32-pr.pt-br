---
description: Especifica se uma fonte de dispositivo de hardware usa a hora do sistema para carimbos de data/hora.
ms.assetid: 54cdfa13-955a-4e92-b337-f645d526a1b8
title: Atributo MFT_HW_TIMESTAMP_WITH_QPC_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94f6f7d50db89e99e76e7b7ea509f444c3998bb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789610"
---
# <a name="mft_hw_timestamp_with_qpc_attribute-attribute"></a><span data-ttu-id="63b55-103">\_ \_ Carimbo de data/hora do HW \_ de MFT com \_ atributo de \_ atributo QPC</span><span class="sxs-lookup"><span data-stu-id="63b55-103">MFT\_HW\_TIMESTAMP\_WITH\_QPC\_Attribute attribute</span></span>

<span data-ttu-id="63b55-104">Especifica se uma fonte de dispositivo de hardware usa a hora do sistema para carimbos de data/hora.</span><span class="sxs-lookup"><span data-stu-id="63b55-104">Specifies whether a hardware device source uses the system time for time stamps.</span></span>

## <a name="data-type"></a><span data-ttu-id="63b55-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="63b55-105">Data type</span></span>

<span data-ttu-id="63b55-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="63b55-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="63b55-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="63b55-107">Get/set</span></span>

<span data-ttu-id="63b55-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="63b55-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="63b55-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="63b55-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="63b55-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="63b55-110">Remarks</span></span>

<span data-ttu-id="63b55-111">Se esse atributo for **true**, a origem do dispositivo usará a hora do sistema, conforme retornado pelo **QueryPerformanceCounter**, para carimbos de data/hora.</span><span class="sxs-lookup"><span data-stu-id="63b55-111">If this attribute is **TRUE**, the device source uses the system time, as returned by the **QueryPerformanceCounter**, for time stamps.</span></span> <span data-ttu-id="63b55-112">Caso contrário, a origem do dispositivo usará o relógio do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63b55-112">Otherwise, the device source uses the device's clock.</span></span> <span data-ttu-id="63b55-113">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="63b55-113">The default value is **FALSE**.</span></span>

<span data-ttu-id="63b55-114">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="63b55-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="63b55-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63b55-115">Requirements</span></span>



| <span data-ttu-id="63b55-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="63b55-116">Requirement</span></span> | <span data-ttu-id="63b55-117">Valor</span><span class="sxs-lookup"><span data-stu-id="63b55-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="63b55-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63b55-118">Minimum supported client</span></span><br/> | <span data-ttu-id="63b55-119">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="63b55-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="63b55-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63b55-120">Minimum supported server</span></span><br/> | <span data-ttu-id="63b55-121">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="63b55-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="63b55-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="63b55-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="63b55-123"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="63b55-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63b55-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="63b55-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63b55-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="63b55-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="63b55-126">Capturar atributos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="63b55-126">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




