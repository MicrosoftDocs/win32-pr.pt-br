---
description: Identifica a combinação de dispositivos de áudio que o aplicativo está usando no momento com o DSP de captura de voz.
ms.assetid: f87bef33-9a48-4568-b554-7eec34f0bd55
title: Propriedade MFPKEY_WMAAECMA_DEVICEPAIR_GUID (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a586d7d31f29b20eb7ca39320d5fa57b9943715a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091069"
---
# <a name="mfpkey_wmaaecma_devicepair_guid-property"></a><span data-ttu-id="911a8-103">\_Propriedade MFPKEY WMAAECMA \_ DEVICEPAIR \_ GUID</span><span class="sxs-lookup"><span data-stu-id="911a8-103">MFPKEY\_WMAAECMA\_DEVICEPAIR\_GUID Property</span></span>

<span data-ttu-id="911a8-104">Identifica a combinação de dispositivos de áudio que o aplicativo está usando no momento com o DSP de captura de voz.</span><span class="sxs-lookup"><span data-stu-id="911a8-104">Identifies the combination of audio devices that the application is currently using with the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="911a8-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="911a8-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="911a8-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="911a8-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="911a8-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="911a8-107">Data Type</span></span>

<span data-ttu-id="911a8-108">CLSID do VT \_</span><span class="sxs-lookup"><span data-stu-id="911a8-108">VT\_CLSID</span></span>

## <a name="applies-to"></a><span data-ttu-id="911a8-109">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="911a8-109">Applies To</span></span>

-   [<span data-ttu-id="911a8-110">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="911a8-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="911a8-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="911a8-111">Remarks</span></span>

<span data-ttu-id="911a8-112">Defina essa propriedade se você estiver usando o DSP no modo de filtro e o valor da propriedade [MFPKEY \_ WMAAECMA \_ recuperar \_ TS \_ stats](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) for Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="911a8-112">Set this property if you are using the DSP in filter mode and the value of the [MFPKEY\_WMAAECMA\_RETRIEVE\_TS\_STATS](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) property is VARIANT\_TRUE.</span></span>

<span data-ttu-id="911a8-113">Quando a propriedade [**MFPKEY \_ WMAAECMA \_ recuperar \_ TS \_ stats**](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) é Variant \_ true, o DSP coleta estatísticas sobre os carimbos de data/hora dos dispositivos de áudio e armazena essas informações no registro.</span><span class="sxs-lookup"><span data-stu-id="911a8-113">When the [**MFPKEY\_WMAAECMA\_RETRIEVE\_TS\_STATS**](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) property is VARIANT\_TRUE, the DSP collects statistics about the time stamps from the audio devices and stores this information in the registry.</span></span> <span data-ttu-id="911a8-114">Essas estatísticas podem ser alteradas para cada combinação de dispositivo de captura de áudio e dispositivo de renderização de áudio.</span><span class="sxs-lookup"><span data-stu-id="911a8-114">These statistics can change for each combination of audio capture device and audio rendering device.</span></span> <span data-ttu-id="911a8-115">Portanto, o aplicativo deve atribuir um GUID para identificar a combinação específica de dispositivos em uso.</span><span class="sxs-lookup"><span data-stu-id="911a8-115">Therefore, the application must assign a GUID to identify the particular combination of devices in use.</span></span> <span data-ttu-id="911a8-116">O aplicativo deve manter o controle desse GUID, para que ele possa atribuir o mesmo GUID sempre que usar o mesmo par de dispositivos de áudio.</span><span class="sxs-lookup"><span data-stu-id="911a8-116">The application should keep track of this GUID, so that it can assign the same GUID whenever it uses the same pair of audio devices.</span></span>

<span data-ttu-id="911a8-117">Se você estiver usando o DSP no modo de origem, não será necessário definir essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="911a8-117">If you are using the DSP in source mode, you do not need to set this property.</span></span> <span data-ttu-id="911a8-118">O DSP gera automaticamente um GUID com base no valor da propriedade [de \_ \_ \_ índices de dispositivo MFPKEY WMAAECMA](mfpkey-wmaaecma-device-indexesproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="911a8-118">The DSP automatically generates a GUID based on the value of the [MFPKEY\_WMAAECMA\_DEVICE\_INDEXES](mfpkey-wmaaecma-device-indexesproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="911a8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="911a8-119">Requirements</span></span>



| <span data-ttu-id="911a8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="911a8-120">Requirement</span></span> | <span data-ttu-id="911a8-121">Valor</span><span class="sxs-lookup"><span data-stu-id="911a8-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="911a8-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="911a8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="911a8-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="911a8-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="911a8-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="911a8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="911a8-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="911a8-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="911a8-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="911a8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="911a8-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="911a8-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="911a8-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="911a8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="911a8-129">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="911a8-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="911a8-130">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="911a8-130">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
