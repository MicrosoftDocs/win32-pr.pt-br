---
description: Especifica se o decodificador deve executar Lt-Rt dobra para baixo.
ms.assetid: ce1dc4ea-4326-40ab-bb30-ff1a34f06d79
title: Propriedade MFPKEY_WMADEC_LTRTOUTPUT (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f4a83d2529ce3b37282be35924b48288d4df45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091067"
---
# <a name="mfpkey_wmadec_ltrtoutput-property"></a><span data-ttu-id="e3572-103">\_Propriedade MFPKEY WMADEC \_ LTRTOUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3572-103">MFPKEY\_WMADEC\_LTRTOUTPUT Property</span></span>

<span data-ttu-id="e3572-104">Especifica se o decodificador deve executar Lt-Rt dobra para baixo.</span><span class="sxs-lookup"><span data-stu-id="e3572-104">Specifies whether the decoder should perform Lt-Rt fold down.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="e3572-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="e3572-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="e3572-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="e3572-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="e3572-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="e3572-107">Data Type</span></span>

<span data-ttu-id="e3572-108">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="e3572-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="e3572-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="e3572-109">Default Value</span></span>

<span data-ttu-id="e3572-110">**VARIANTE \_ falso**</span><span class="sxs-lookup"><span data-stu-id="e3572-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="e3572-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3572-111">Remarks</span></span>

<span data-ttu-id="e3572-112">Se essa propriedade tiver um valor de variante \_ false e a saída for estéreo, o decodificador de áudio usará a dobra de canal simples.</span><span class="sxs-lookup"><span data-stu-id="e3572-112">If this property has a value of VARIANT\_FALSE and the output is stereo, the audio decoder uses simple channel fold down.</span></span> <span data-ttu-id="e3572-113">Se essa propriedade tiver um valor de VARIANT \_ true, o decodificador de áudio executará Lt-Rt (em matriz) com dobra para estéreo e qualquer decodificador Dolby Surround poderá ser usado para decodificar o surround em matriz.</span><span class="sxs-lookup"><span data-stu-id="e3572-113">If this property has a value of VARIANT\_TRUE, the audio decoder performs Lt-Rt (matrixed) fold down to stereo, and then any Dolby Surround decoder can be used to decode the matrixed surround .</span></span> <span data-ttu-id="e3572-114">Por exemplo, o decodificador de áudio poderia executar Lt-Rt dobrar no conteúdo 5,1 ou 7,1.</span><span class="sxs-lookup"><span data-stu-id="e3572-114">For example, the audio decoder could perform Lt-Rt fold down on 5.1 or 7.1 content.</span></span>

<span data-ttu-id="e3572-115">Essa propriedade tem suporte apenas quando o decodificador está agindo como um DMO (objeto de mídia do DirectX).</span><span class="sxs-lookup"><span data-stu-id="e3572-115">This property is supported only when the decoder is acting as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="e3572-116">Não há suporte para nenhuma dobra de nenhum tipo quando o decodificador está agindo como uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="e3572-116">No fold down of any kind is supported when the decoder is acting as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="e3572-117">No Windows Vista, se você obtiver uma interface **IPropertyStore** em um decodificador de áudio, o decodificador atuará como um MFT.</span><span class="sxs-lookup"><span data-stu-id="e3572-117">On Windows Vista, if you obtain an **IPropertyStore** interface on an audio decoder, the decoder acts as an MFT.</span></span> <span data-ttu-id="e3572-118">Consequentemente, essa propriedade não pode ser usada no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e3572-118">Consequently, this property cannot be used on Windows Vista.</span></span> <span data-ttu-id="e3572-119">Para obter informações sobre quando um decodificador atua como um DMO ou uma MFT, consulte as páginas de referência do codec individual em [objetos de codec](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="e3572-119">For information on when a decoder acts as a DMO or an MFT, see the individual codec reference pages under [Codec Objects](codecobjects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3572-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3572-120">Requirements</span></span>



| <span data-ttu-id="e3572-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3572-121">Requirement</span></span> | <span data-ttu-id="e3572-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e3572-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3572-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3572-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e3572-124">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e3572-124">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e3572-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3572-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e3572-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e3572-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e3572-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e3572-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3572-128"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3572-128"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3572-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3572-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3572-130">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e3572-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
