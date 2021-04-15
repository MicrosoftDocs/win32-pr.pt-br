---
description: Especifica o formato de entrada atual para o decodificador.
ms.assetid: 8fddf8c3-268e-4706-9003-e4bfb03d5278
title: Propriedade AVDecCommonInputFormat (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7432d2a48727ec144d4206d4a11bfe65ce2c5d2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456765"
---
# <a name="avdeccommoninputformat-property"></a><span data-ttu-id="44c45-103">Propriedade AVDecCommonInputFormat</span><span class="sxs-lookup"><span data-stu-id="44c45-103">AVDecCommonInputFormat property</span></span>

<span data-ttu-id="44c45-104">Especifica o formato de entrada atual para o decodificador.</span><span class="sxs-lookup"><span data-stu-id="44c45-104">Specifies the current input format for the decoder.</span></span>

<span data-ttu-id="44c45-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="44c45-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="44c45-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="44c45-106">Data type</span></span>

<span data-ttu-id="44c45-107">**BSTR** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="44c45-107">**BSTR** (**VT\_BSTR**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="44c45-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="44c45-108">Property GUID</span></span>

<span data-ttu-id="44c45-109">**CODECAPI \_ AVDecCommonInputFormat**</span><span class="sxs-lookup"><span data-stu-id="44c45-109">**CODECAPI\_AVDecCommonInputFormat**</span></span>

## <a name="property-value"></a><span data-ttu-id="44c45-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="44c45-110">Property value</span></span>

<span data-ttu-id="44c45-111">O valor dessa propriedade é um **BSTR** que contém a representação de cadeia de caracteres de um GUID.</span><span class="sxs-lookup"><span data-stu-id="44c45-111">The value of this property is a **BSTR** that contains the string representation of a GUID.</span></span> <span data-ttu-id="44c45-112">Os GUIDs a seguir são definidos.</span><span class="sxs-lookup"><span data-stu-id="44c45-112">The following GUIDs are defined.</span></span>



| <span data-ttu-id="44c45-113">**GUID**</span><span class="sxs-lookup"><span data-stu-id="44c45-113">**GUID**</span></span>                                            | <span data-ttu-id="44c45-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="44c45-114">Description</span></span>                                    |
|-----------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="44c45-115">**CODECAPI \_ GUID \_ AVDecAudioInputAAC**</span><span class="sxs-lookup"><span data-stu-id="44c45-115">**CODECAPI\_GUID\_AVDecAudioInputAAC**</span></span>              | <span data-ttu-id="44c45-116">AAC (codificação de áudio avançada)</span><span class="sxs-lookup"><span data-stu-id="44c45-116">Advanced Audio Coding (AAC)</span></span>                    |
| <span data-ttu-id="44c45-117">**CODECAPI \_ GUID \_ AVDecAudioInputDolbyDigitalPlus**</span><span class="sxs-lookup"><span data-stu-id="44c45-117">**CODECAPI\_GUID\_AVDecAudioInputDolbyDigitalPlus**</span></span> | <span data-ttu-id="44c45-118">Áudio Dolby Digital Plus</span><span class="sxs-lookup"><span data-stu-id="44c45-118">Dolby Digital Plus audio</span></span>                       |
| <span data-ttu-id="44c45-119">**CODECAPI \_ GUID \_ AVDecAudioInputDolby**</span><span class="sxs-lookup"><span data-stu-id="44c45-119">**CODECAPI\_GUID\_AVDecAudioInputDolby**</span></span>            | <span data-ttu-id="44c45-120">Áudio Dolby</span><span class="sxs-lookup"><span data-stu-id="44c45-120">Dolby audio</span></span>                                    |
| <span data-ttu-id="44c45-121">**CODECAPI \_ GUID \_ AVDecAudioInputDTS**</span><span class="sxs-lookup"><span data-stu-id="44c45-121">**CODECAPI\_GUID\_AVDecAudioInputDTS**</span></span>              | <span data-ttu-id="44c45-122">Áudio DTS</span><span class="sxs-lookup"><span data-stu-id="44c45-122">DTS audio</span></span>                                      |
| <span data-ttu-id="44c45-123">**CODECAPI \_ GUID \_ AVDecAudioInputHEAAC**</span><span class="sxs-lookup"><span data-stu-id="44c45-123">**CODECAPI\_GUID\_AVDecAudioInputHEAAC**</span></span>            | <span data-ttu-id="44c45-124">Codificação de áudio avançada High-Efficiency (HE-AAC)</span><span class="sxs-lookup"><span data-stu-id="44c45-124">High-Efficiency Advanced Audio Coding (HE-AAC)</span></span> |
| <span data-ttu-id="44c45-125">**CODECAPI \_ GUID \_ AVDecAudioInputMPEG**</span><span class="sxs-lookup"><span data-stu-id="44c45-125">**CODECAPI\_GUID\_AVDecAudioInputMPEG**</span></span>             | <span data-ttu-id="44c45-126">Áudio MPEG</span><span class="sxs-lookup"><span data-stu-id="44c45-126">MPEG audio</span></span>                                     |
| <span data-ttu-id="44c45-127">**CODECAPI \_ GUID \_ AVDecAudioInputPCM**</span><span class="sxs-lookup"><span data-stu-id="44c45-127">**CODECAPI\_GUID\_AVDecAudioInputPCM**</span></span>              | <span data-ttu-id="44c45-128">Áudio PCM</span><span class="sxs-lookup"><span data-stu-id="44c45-128">PCM audio</span></span>                                      |
| <span data-ttu-id="44c45-129">**CODECAPI \_ GUID \_ AVDecAudioInputWMA**</span><span class="sxs-lookup"><span data-stu-id="44c45-129">**CODECAPI\_GUID\_AVDecAudioInputWMA**</span></span>              | <span data-ttu-id="44c45-130">Áudio do Windows Media</span><span class="sxs-lookup"><span data-stu-id="44c45-130">Windows Media Audio</span></span>                            |
| <span data-ttu-id="44c45-131">**CODECAPI \_ GUID \_ AVDecAudioInputWMAPro**</span><span class="sxs-lookup"><span data-stu-id="44c45-131">**CODECAPI\_GUID\_AVDecAudioInputWMAPro**</span></span>           | <span data-ttu-id="44c45-132">Windows Media Audio 9 Professional (WMA pro)</span><span class="sxs-lookup"><span data-stu-id="44c45-132">Windows Media Audio 9 Professional (WMA Pro)</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="44c45-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44c45-133">Requirements</span></span>



| <span data-ttu-id="44c45-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="44c45-134">Requirement</span></span> | <span data-ttu-id="44c45-135">Valor</span><span class="sxs-lookup"><span data-stu-id="44c45-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44c45-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44c45-136">Minimum supported client</span></span><br/> | <span data-ttu-id="44c45-137">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="44c45-137">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="44c45-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44c45-138">Minimum supported server</span></span><br/> | <span data-ttu-id="44c45-139">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="44c45-139">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="44c45-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44c45-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="44c45-141"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="44c45-141"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44c45-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="44c45-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44c45-143">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="44c45-143">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="44c45-144">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="44c45-144">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




