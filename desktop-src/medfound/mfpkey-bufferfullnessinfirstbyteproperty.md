---
description: Especifica se o fluxo de bits de vídeo codificado contém um valor de total de buffer com cada quadro-chave.
ms.assetid: 5574ee3c-ccb3-4ff6-8280-efe5626e6dd6
title: Propriedade MFPKEY_BUFFERFULLNESSINFIRSTBYTE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10fbcdb6306faeb7481f1cc7be20088ff0cedd5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796125"
---
# <a name="mfpkey_bufferfullnessinfirstbyte-property"></a><span data-ttu-id="4a056-103">\_Propriedade MFPKEY BUFFERFULLNESSINFIRSTBYTE</span><span class="sxs-lookup"><span data-stu-id="4a056-103">MFPKEY\_BUFFERFULLNESSINFIRSTBYTE Property</span></span>

<span data-ttu-id="4a056-104">Especifica se o fluxo de bits de vídeo codificado contém um valor de total de buffer com cada quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="4a056-104">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="4a056-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="4a056-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="4a056-106">g \_ wszWMVCBufferFullnessInFirstByte</span><span class="sxs-lookup"><span data-stu-id="4a056-106">g\_wszWMVCBufferFullnessInFirstByte</span></span>

## <a name="data-type"></a><span data-ttu-id="4a056-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="4a056-107">Data Type</span></span>

<span data-ttu-id="4a056-108">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="4a056-108">VT\_BOOL</span></span>

## <a name="remarks"></a><span data-ttu-id="4a056-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a056-109">Remarks</span></span>

<span data-ttu-id="4a056-110">Você deve definir um tipo de saída antes de obter esse valor.</span><span class="sxs-lookup"><span data-stu-id="4a056-110">You must set an output type before getting this value.</span></span>

<span data-ttu-id="4a056-111">Você pode obter o valor dessa propriedade usando [IWMCodecProps:: GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop).</span><span class="sxs-lookup"><span data-stu-id="4a056-111">You can get the value of this property using [IWMCodecProps::GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop).</span></span> <span data-ttu-id="4a056-112">Se você usar **IPropertyBag**, deverá primeiro definir o valor FOURCC do formato compactado desejado com a propriedade [ \_ FOURCC MFPKEY](mfpkey-fourccproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="4a056-112">If you use **IPropertyBag**, you must first set the FOURCC value of the desired compressed format with the [MFPKEY\_FOURCC](mfpkey-fourccproperty.md) property.</span></span>

<span data-ttu-id="4a056-113">Ter a totalidade do buffer no primeiro byte de todos os quadros-chave permite que você determine o tamanho do buffer necessário ao concatenar fluxos de vídeo compactados.</span><span class="sxs-lookup"><span data-stu-id="4a056-113">Having the buffer fullness in the first byte of all key frames enables you to determine the buffer size required when concatenating compressed video streams.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a056-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a056-114">Requirements</span></span>



| <span data-ttu-id="4a056-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a056-115">Requirement</span></span> | <span data-ttu-id="4a056-116">Valor</span><span class="sxs-lookup"><span data-stu-id="4a056-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a056-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a056-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4a056-118">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4a056-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4a056-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a056-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4a056-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4a056-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4a056-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4a056-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a056-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a056-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a056-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a056-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a056-124">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4a056-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




