---
description: Especifica se o DSP de captura de voz armazena estatísticas de carimbo de data/hora no registro.
ms.assetid: c44462be-ccdf-4a49-bb77-6e816def4849
title: Propriedade MFPKEY_WMAAECMA_RETRIEVE_TS_STATS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8e4efad8def035c7282e3ade8045bdbfd7e34d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810687"
---
# <a name="mfpkey_wmaaecma_retrieve_ts_stats-property"></a><span data-ttu-id="ee4aa-103">MFPKEY \_ WMAAECMA \_ recuperar \_ \_ Propriedade TS stats</span><span class="sxs-lookup"><span data-stu-id="ee4aa-103">MFPKEY\_WMAAECMA\_RETRIEVE\_TS\_STATS Property</span></span>

<span data-ttu-id="ee4aa-104">Especifica se o DSP de captura de voz armazena estatísticas de carimbo de data/hora no registro.</span><span class="sxs-lookup"><span data-stu-id="ee4aa-104">Specifies whether the Voice Capture DSP stores time stamp statistics in the registry.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ee4aa-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="ee4aa-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ee4aa-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="ee4aa-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="ee4aa-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="ee4aa-107">Data Type</span></span>

<span data-ttu-id="ee4aa-108">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="ee4aa-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="ee4aa-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="ee4aa-109">Default Value</span></span>

<span data-ttu-id="ee4aa-110">VARIANTE \_ falso</span><span class="sxs-lookup"><span data-stu-id="ee4aa-110">VARIANT\_FALSE</span></span>

## <a name="applies-to"></a><span data-ttu-id="ee4aa-111">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="ee4aa-111">Applies To</span></span>

-   [<span data-ttu-id="ee4aa-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="ee4aa-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="ee4aa-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee4aa-113">Remarks</span></span>

<span data-ttu-id="ee4aa-114">Os algoritmos de cancelamento de eco acústico (AEC) dependem de carimbos de data/hora precisos nos fluxos de áudio.</span><span class="sxs-lookup"><span data-stu-id="ee4aa-114">Acoustic echo cancellation (AEC) algorithms depend on accurate time stamps on the audio streams.</span></span> <span data-ttu-id="ee4aa-115">Na realidade, os carimbos de data/hora geralmente são imperfeitos e diferentes dispositivos de áudio podem apresentar taxas diferentes de variação e descompasso.</span><span class="sxs-lookup"><span data-stu-id="ee4aa-115">In reality, time stamps are often imperfect, and different audio devices can exhibit different rates of variance and drift.</span></span> <span data-ttu-id="ee4aa-116">Quando o AEC está habilitado, o DSP coleta estatísticas sobre os carimbos de data e hora e usa essas informações para compensar as imprecisões.</span><span class="sxs-lookup"><span data-stu-id="ee4aa-116">When AEC is enabled, the DSP collects statistics about the time stamps and uses this information to compensate for inaccuracies.</span></span>

<span data-ttu-id="ee4aa-117">Se o valor dessa propriedade for VARIANT \_ true, o DSP salvará as estatísticas coletadas no registro.</span><span class="sxs-lookup"><span data-stu-id="ee4aa-117">If the value of this property is VARIANT\_TRUE, the DSP saves the statistics that it collects in the registry.</span></span> <span data-ttu-id="ee4aa-118">Na próxima vez que o DSP executar o AEC usando o mesmo par de dispositivos de áudio, ele lerá as informações estatísticas do registro, o que permite que o DSP seja executado com mais eficiência.</span><span class="sxs-lookup"><span data-stu-id="ee4aa-118">The next time the DSP performs AEC using the same pair of audio devices, it reads the statistical information from the registry, which enables the DSP to perform more efficiently.</span></span>

<span data-ttu-id="ee4aa-119">Se você definir o valor dessa propriedade como VARIANT \_ true e estiver usando o DSP no modo de filtro, também deverá definir a propriedade [MFPKEY \_ WMAAECMA \_ DEVICEPAIR \_ GUID](mfpkey-wmaaecma-devicepair-guidproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="ee4aa-119">If you set the value of this property to VARIANT\_TRUE and you are using the DSP in filter mode, you should also set the [MFPKEY\_WMAAECMA\_DEVICEPAIR\_GUID](mfpkey-wmaaecma-devicepair-guidproperty.md) property.</span></span> <span data-ttu-id="ee4aa-120">No modo de origem, isso não é necessário.</span><span class="sxs-lookup"><span data-stu-id="ee4aa-120">In source mode, this is not required.</span></span>

<span data-ttu-id="ee4aa-121">O valor padrão dessa propriedade é VARIANT \_ false.</span><span class="sxs-lookup"><span data-stu-id="ee4aa-121">The default value of this property is VARIANT\_FALSE.</span></span> <span data-ttu-id="ee4aa-122">O DSP usa essa propriedade somente quando o processamento de AEC está habilitado.</span><span class="sxs-lookup"><span data-stu-id="ee4aa-122">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee4aa-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee4aa-123">Requirements</span></span>



| <span data-ttu-id="ee4aa-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee4aa-124">Requirement</span></span> | <span data-ttu-id="ee4aa-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ee4aa-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee4aa-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee4aa-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ee4aa-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ee4aa-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ee4aa-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee4aa-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ee4aa-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ee4aa-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ee4aa-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ee4aa-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee4aa-131"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee4aa-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee4aa-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee4aa-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee4aa-133">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ee4aa-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="ee4aa-134">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="ee4aa-134">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
