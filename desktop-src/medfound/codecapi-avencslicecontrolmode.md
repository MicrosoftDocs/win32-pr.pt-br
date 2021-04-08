---
description: Especifica o modo de controle de fatia. Os valores válidos são 0, 1 e 2.
ms.assetid: 5269DB79-639C-4F67-B885-BF1274CDB635
title: Propriedade CODECAPI_AVEncSliceControlMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0aef928a3938b2f0756d2e84b6836da194823dab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920636"
---
# <a name="codecapi_avencslicecontrolmode-property"></a><span data-ttu-id="69455-104">\_Propriedade CODECAPI AVEncSliceControlMode</span><span class="sxs-lookup"><span data-stu-id="69455-104">CODECAPI\_AVEncSliceControlMode property</span></span>

<span data-ttu-id="69455-105">Especifica o modo de controle de fatia.</span><span class="sxs-lookup"><span data-stu-id="69455-105">Specifies the slice control mode.</span></span> <span data-ttu-id="69455-106">Os valores válidos são 0, 1 e 2.</span><span class="sxs-lookup"><span data-stu-id="69455-106">Valid values are 0, 1, and 2.</span></span>

## <a name="data-type"></a><span data-ttu-id="69455-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="69455-107">Data type</span></span>

<span data-ttu-id="69455-108">**ULONG** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="69455-108">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="69455-109">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="69455-109">Property GUID</span></span>

<span data-ttu-id="69455-110">**CODECAPI \_ AVEncSliceControlMode**</span><span class="sxs-lookup"><span data-stu-id="69455-110">**CODECAPI\_AVEncSliceControlMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="69455-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="69455-111">Property value</span></span>

<span data-ttu-id="69455-112">Valores do modo de controle de fatia:</span><span class="sxs-lookup"><span data-stu-id="69455-112">Slice control mode values:</span></span>



| <span data-ttu-id="69455-113">Valor</span><span class="sxs-lookup"><span data-stu-id="69455-113">Value</span></span>                                                                        | <span data-ttu-id="69455-114">Significado</span><span class="sxs-lookup"><span data-stu-id="69455-114">Meaning</span></span>                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="69455-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="69455-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="69455-116">Definir esse valor como 0 indica que a propriedade [CODECAPI \_ AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) especificará o tamanho da fatia em unidades de macroblocos por fatia.</span><span class="sxs-lookup"><span data-stu-id="69455-116">Setting this value to 0 indicates that the [CODECAPI\_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) property will specify the slice size in units of macroblocks per slice.</span></span><br/>     |
| <dl> <span data-ttu-id="69455-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="69455-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="69455-118">Definir esse valor como 1 indica que a propriedade [CODECAPI \_ AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) especificará o tamanho da fatia em unidades de bits por fatia.</span><span class="sxs-lookup"><span data-stu-id="69455-118">Setting this value to 1 indicates that the [CODECAPI\_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) property will specify the slice size in units of bits per slice.</span></span><br/>            |
| <dl> <span data-ttu-id="69455-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="69455-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="69455-120">Definir esse valor como 2 indica que a propriedade [CODECAPI \_ AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) especificará o tamanho da fatia em unidades de macrobloco linhas por fatia.</span><span class="sxs-lookup"><span data-stu-id="69455-120">Setting this value to 2 indicates that the [CODECAPI\_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) property will specify the slice size in units of macroblock rows per slice.</span></span><br/> |



 

<span data-ttu-id="69455-121">O codificador retorna os valores que ele suporta.</span><span class="sxs-lookup"><span data-stu-id="69455-121">The encoder returns the values that it supports.</span></span>

## <a name="remarks"></a><span data-ttu-id="69455-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="69455-122">Remarks</span></span>

<span data-ttu-id="69455-123">**Codificadores H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="69455-123">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="69455-124">É recomendável que o codificador ofereça suporte a [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)e [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="69455-124">It is recommended that the encoder supports [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="69455-125">Se [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) não for chamado para CODECAPI \_ AVEncSliceControlMode, [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) para CODECAPI \_ AVEncSliceControlMode poderá retornar **VFW \_ E \_ CODECAPI \_ nenhum \_ \_ valor atual**.</span><span class="sxs-lookup"><span data-stu-id="69455-125">If [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) is not called for CODECAPI\_AVEncSliceControlMode, [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) for CODECAPI\_AVEncSliceControlMode can return **VFW\_E\_CODECAPI\_NO\_CURRENT\_VALUE**.</span></span> <span data-ttu-id="69455-126">[**Getdefaultvalue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getdefaultvalue) pode retornar **VFW \_ E \_ CODECAPI \_ nenhum \_ padrão** para CODECAPI \_ AVEncSliceControlMode.</span><span class="sxs-lookup"><span data-stu-id="69455-126">[**GetDefaultValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getdefaultvalue) may return **VFW\_E\_CODECAPI\_NO\_DEFAULT** for CODECAPI\_AVEncSliceControlMode.</span></span>

<span data-ttu-id="69455-127">O valor padrão recomendado é 2 (tamanho em MB de linha por fatia).</span><span class="sxs-lookup"><span data-stu-id="69455-127">Recommended default value is 2 (size in MB row per slice).</span></span>

<span data-ttu-id="69455-128">Essa é uma API estática, o que significa que o aplicativo ganhou t altere isso enquanto o codificador estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="69455-128">This is a static API, which means the application won t change this while the encoder is running.</span></span>

## <a name="examples"></a><span data-ttu-id="69455-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="69455-129">Examples</span></span>


```C++
if (pCodecAPI->IsSupported(&CODECAPI_AVEncSliceControlMode) == S_OK) {                
     VARIANT var;
     var.vt = VT_UI4;
     var.ulVal =ulSliceMode;
     pCodecAPI->SetValue(&CODECAPI_AVEncSliceControlMode, &var);
}
```



## <a name="requirements"></a><span data-ttu-id="69455-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69455-130">Requirements</span></span>



| <span data-ttu-id="69455-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="69455-131">Requirement</span></span> | <span data-ttu-id="69455-132">Valor</span><span class="sxs-lookup"><span data-stu-id="69455-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69455-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69455-133">Minimum supported client</span></span><br/> | <span data-ttu-id="69455-134">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="69455-134">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="69455-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69455-135">Minimum supported server</span></span><br/> | <span data-ttu-id="69455-136">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="69455-136">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="69455-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="69455-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="69455-138"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="69455-138"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69455-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="69455-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69455-140">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="69455-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

