---
description: Especifica as partes do conteúdo a serem codificadas como música pelo codec de voz.
ms.assetid: c63034ce-33d7-4f2f-9498-fc16e25b6d4d
title: Propriedade MFPKEY_WMAVOICE_ENC_EDL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f3ac85ebd3a0542fbcf6554205d0b2f2623957c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661833"
---
# <a name="mfpkey_wmavoice_enc_edl-property"></a><span data-ttu-id="ed1f3-103">\_Propriedade MFPKEY WMAVOICE \_ ENC \_ EDL</span><span class="sxs-lookup"><span data-stu-id="ed1f3-103">MFPKEY\_WMAVOICE\_ENC\_EDL Property</span></span>

<span data-ttu-id="ed1f3-104">Especifica as partes do conteúdo a serem codificadas como música pelo codec de voz.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-104">Specifies the portions of content to be encoded as music by the voice codec.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ed1f3-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="ed1f3-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ed1f3-106">g \_ wszWMACVoiceBuffer</span><span class="sxs-lookup"><span data-stu-id="ed1f3-106">g\_wszWMACVoiceBuffer</span></span>

## <a name="data-type"></a><span data-ttu-id="ed1f3-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="ed1f3-107">Data Type</span></span>

<span data-ttu-id="ed1f3-108">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="ed1f3-108">VT\_BSTR</span></span>

## <a name="default-value"></a><span data-ttu-id="ed1f3-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="ed1f3-109">Default Value</span></span>

<span data-ttu-id="ed1f3-110">Sem valor padrão.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-110">No default value.</span></span> <span data-ttu-id="ed1f3-111">Se essa propriedade não for definida, o codec usará o valor da propriedade [MFPKEY \_ WMAVOICE \_ ENC \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) para determinar como codificar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-111">If this property is not set, the codec will use the value of the [MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) property to determine how to encode the content.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed1f3-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed1f3-112">Remarks</span></span>

<span data-ttu-id="ed1f3-113">Você pode usar essa propriedade se o modo automático do codec não estiver fornecendo resultados satisfatórios.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-113">You can use this property if the automatic mode of the codec is not giving satisfactory results.</span></span>

<span data-ttu-id="ed1f3-114">Esse valor é uma cadeia de caracteres delimitada por vírgula que contém pelo menos quatro inteiros.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-114">This value is a comma-delimited string containing at least four integers.</span></span> <span data-ttu-id="ed1f3-115">O primeiro inteiro é o número de versão; Sempre use 1 para esse valor.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-115">The first integer is the version number; always use 1 for this value.</span></span> <span data-ttu-id="ed1f3-116">O segundo inteiro é o número de seções que precisam ser codificadas como música.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-116">The second integer is the number of sections that need to be encoded as music.</span></span> <span data-ttu-id="ed1f3-117">Seguindo o segundo inteiro há um número de pares de valores representando intervalos em milissegundos, um par para cada seção de conteúdo que precisa ser codificado como música.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-117">Following the second integer are a number of pairs of values representing ranges in milliseconds, one pair for each section of content that needs to be encoded as music.</span></span>

<span data-ttu-id="ed1f3-118">Por exemplo, "1, 2100200500600" informa o codificador para usar a versão 1 com 2 seções de música.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-118">For example, "1,2,100,200,500,600" informs the encoder to use version 1 with 2 sections of music.</span></span> <span data-ttu-id="ed1f3-119">A primeira seção de música começa às 100 ms e termina em 200 ms.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-119">The first music section starts at 100 ms and ends at 200 ms.</span></span> <span data-ttu-id="ed1f3-120">A segunda seção de música começa às 500 MS e termina em 600 MS.</span><span class="sxs-lookup"><span data-stu-id="ed1f3-120">The second music section starts at 500 ms and ends at 600 ms.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed1f3-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed1f3-121">Requirements</span></span>



| <span data-ttu-id="ed1f3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed1f3-122">Requirement</span></span> | <span data-ttu-id="ed1f3-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ed1f3-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed1f3-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed1f3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ed1f3-125">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ed1f3-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ed1f3-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed1f3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ed1f3-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ed1f3-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ed1f3-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ed1f3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed1f3-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed1f3-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed1f3-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed1f3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed1f3-131">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ed1f3-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




