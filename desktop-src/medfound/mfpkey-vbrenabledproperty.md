---
description: Especifica se o codificador usa a codificação de taxa de bits variável (VBR).
ms.assetid: e6826802-99b7-4a38-9b58-8a9cb8b753fb
title: Propriedade MFPKEY_VBRENABLED (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9061abcc6ac7d7338b63eb5a7cd1a13ad22bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827894"
---
# <a name="mfpkey_vbrenabled-property"></a><span data-ttu-id="31a9b-103">\_Propriedade MFPKEY VBRENABLED</span><span class="sxs-lookup"><span data-stu-id="31a9b-103">MFPKEY\_VBRENABLED Property</span></span>

<span data-ttu-id="31a9b-104">Especifica se o codificador usa a codificação de taxa de bits variável (VBR).</span><span class="sxs-lookup"><span data-stu-id="31a9b-104">Specifies whether the encoder uses variable-bit-rate (VBR) encoding.</span></span> <span data-ttu-id="31a9b-105">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="31a9b-105">Read-write.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="31a9b-106">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="31a9b-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="31a9b-107">**g \_ wszWMVCVBREnabled**, **g \_ wszWMCPAudioVBRSupported**</span><span class="sxs-lookup"><span data-stu-id="31a9b-107">**g\_wszWMVCVBREnabled**, **g\_wszWMCPAudioVBRSupported**</span></span>

## <a name="data-type"></a><span data-ttu-id="31a9b-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="31a9b-108">Data Type</span></span>

<span data-ttu-id="31a9b-109">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="31a9b-109">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="31a9b-110">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="31a9b-110">Default Value</span></span>

<span data-ttu-id="31a9b-111">**VARIANTE \_ falso**</span><span class="sxs-lookup"><span data-stu-id="31a9b-111">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="31a9b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="31a9b-112">Remarks</span></span>

<span data-ttu-id="31a9b-113">Esse valor deve ser definido como **Variant \_ true** para qualquer uma das outras propriedades de VBR a ser usada pelo codec.</span><span class="sxs-lookup"><span data-stu-id="31a9b-113">This value must be set to **VARIANT\_TRUE** for any of the other VBR properties to be used by the codec.</span></span>

<span data-ttu-id="31a9b-114">Depois de definir esse valor como **Variant \_ true** no codificador de áudio, os tipos de saída recuperados usando o método [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) são tipos de VBR.</span><span class="sxs-lookup"><span data-stu-id="31a9b-114">After you set this value to **VARIANT\_TRUE** on the audio encoder, the output types retrieved by using the [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) method are VBR types.</span></span>

## <a name="requirements"></a><span data-ttu-id="31a9b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31a9b-115">Requirements</span></span>



| <span data-ttu-id="31a9b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="31a9b-116">Requirement</span></span> | <span data-ttu-id="31a9b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="31a9b-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31a9b-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31a9b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="31a9b-119">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="31a9b-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="31a9b-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31a9b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="31a9b-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="31a9b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="31a9b-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="31a9b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="31a9b-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="31a9b-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31a9b-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="31a9b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31a9b-125">**MFPKEY \_ restringir \_ VBRQUALITY enumerado \_**</span><span class="sxs-lookup"><span data-stu-id="31a9b-125">**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**</span></span>](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[<span data-ttu-id="31a9b-126">**MFPKEY \_ desired \_ VBRQUALITY**</span><span class="sxs-lookup"><span data-stu-id="31a9b-126">**MFPKEY\_DESIRED\_VBRQUALITY**</span></span>](mfpkey-desired-vbrqualityproperty.md)
</dt> <dt>

[<span data-ttu-id="31a9b-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="31a9b-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
