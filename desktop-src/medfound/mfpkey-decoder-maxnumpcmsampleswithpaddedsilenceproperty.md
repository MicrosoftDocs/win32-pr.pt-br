---
description: Especifica o número máximo de amostras de PCM adicionais que podem ser retornadas ao final de após a decodificação de um arquivo.
ms.assetid: 82b3676c-7653-421c-aac7-7f20a642779f
title: Propriedade MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b1f97b55c2eedd8cc7d6d524379569073fa35d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793927"
---
# <a name="mfpkey_decoder_maxnumpcmsampleswithpaddedsilence-property"></a><span data-ttu-id="25a89-103">\_Propriedade MaxNumPCMSamplesWithPaddedSilence do decodificador MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="25a89-103">MFPKEY\_Decoder\_MaxNumPCMSamplesWithPaddedSilence Property</span></span>

<span data-ttu-id="25a89-104">Especifica o número máximo de amostras de PCM adicionais que podem ser retornadas ao final de após a decodificação de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="25a89-104">Specifies the maximum number of additional PCM samples that might be returned at the end of after decoding a file.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="25a89-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="25a89-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="25a89-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="25a89-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="25a89-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="25a89-107">Data Type</span></span>

<span data-ttu-id="25a89-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="25a89-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="25a89-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="25a89-109">Default Value</span></span>

<span data-ttu-id="25a89-110">2.048</span><span class="sxs-lookup"><span data-stu-id="25a89-110">2048</span></span>

## <a name="remarks"></a><span data-ttu-id="25a89-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="25a89-111">Remarks</span></span>

<span data-ttu-id="25a89-112">Essa propriedade pode ser usada para estimar o silêncio artificial que é inserido entre as músicas à medida que elas são alimentadas no decodificador, uma após a outra.</span><span class="sxs-lookup"><span data-stu-id="25a89-112">This property can be used to estimate artificial silence that gets is inserted between songs as they are fed to the decoder one after another.</span></span>

<span data-ttu-id="25a89-113">Para os decodificadores de áudio do Windows Media 10 Professional e Windows Media 9 sem perdas, essa propriedade é sempre igual a 0.</span><span class="sxs-lookup"><span data-stu-id="25a89-113">For the Windows Media Audio 10 Professional and Windows Media Audio 9 Lossless decoders, this property is always equal to 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="25a89-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25a89-114">Requirements</span></span>



| <span data-ttu-id="25a89-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="25a89-115">Requirement</span></span> | <span data-ttu-id="25a89-116">Valor</span><span class="sxs-lookup"><span data-stu-id="25a89-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25a89-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25a89-117">Minimum supported client</span></span><br/> | <span data-ttu-id="25a89-118">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="25a89-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="25a89-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25a89-119">Minimum supported server</span></span><br/> | <span data-ttu-id="25a89-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="25a89-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="25a89-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="25a89-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="25a89-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="25a89-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25a89-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="25a89-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25a89-124">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="25a89-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
