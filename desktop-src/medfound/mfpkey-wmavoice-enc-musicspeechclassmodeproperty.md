---
description: Especifica o modo do codec de voz.
ms.assetid: 8425cdab-e43c-41ca-9c20-09ab6a5f06f4
title: Propriedade MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9776c76f2a8863afe73626f5a2940de2c0ccb7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761051"
---
# <a name="mfpkey_wmavoice_enc_musicspeechclassmode-property"></a><span data-ttu-id="8c2d5-103">\_Propriedade MFPKEY WMAVOICE \_ ENC \_ MusicSpeechClassMode</span><span class="sxs-lookup"><span data-stu-id="8c2d5-103">MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode Property</span></span>

<span data-ttu-id="8c2d5-104">Especifica o modo do codec de voz.</span><span class="sxs-lookup"><span data-stu-id="8c2d5-104">Specifies the mode of the voice codec.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="8c2d5-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="8c2d5-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="8c2d5-106">g \_ wszWMACMusicSpeechClassMode</span><span class="sxs-lookup"><span data-stu-id="8c2d5-106">g\_wszWMACMusicSpeechClassMode</span></span>

## <a name="data-type"></a><span data-ttu-id="8c2d5-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="8c2d5-107">Data Type</span></span>

<span data-ttu-id="8c2d5-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="8c2d5-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="8c2d5-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="8c2d5-109">Default Value</span></span>

<span data-ttu-id="8c2d5-110">1</span><span class="sxs-lookup"><span data-stu-id="8c2d5-110">1</span></span>

## <a name="remarks"></a><span data-ttu-id="8c2d5-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c2d5-111">Remarks</span></span>

<span data-ttu-id="8c2d5-112">Um valor de 1 informa ao codec que o conteúdo é somente de voz, um valor de 2 tem o codec determinar o modo automaticamente e qualquer outro valor informa o codec para usar o modo de música.</span><span class="sxs-lookup"><span data-stu-id="8c2d5-112">A value of 1 informs the codec that the content is voice-only, a value of 2 has the codec determine the mode automatically, and any other value informs the codec to use music mode.</span></span>

<span data-ttu-id="8c2d5-113">Se o modo automático não estiver codificando voz mista e música corretamente, você poderá especificar a codificação para seções individuais do arquivo usando a propriedade [MFPKEY \_ WMAVOICE \_ ENC \_ EDL](mfpkey-wmavoice-enc-edlproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="8c2d5-113">If automatic mode is not encoding mixed voice and music properly, you can specify encoding for individual sections of the file by using the [MFPKEY\_WMAVOICE\_ENC\_EDL](mfpkey-wmavoice-enc-edlproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c2d5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c2d5-114">Requirements</span></span>



| <span data-ttu-id="8c2d5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c2d5-115">Requirement</span></span> | <span data-ttu-id="8c2d5-116">Valor</span><span class="sxs-lookup"><span data-stu-id="8c2d5-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c2d5-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c2d5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8c2d5-118">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8c2d5-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8c2d5-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c2d5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8c2d5-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8c2d5-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8c2d5-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8c2d5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c2d5-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c2d5-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c2d5-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c2d5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c2d5-124">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8c2d5-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




