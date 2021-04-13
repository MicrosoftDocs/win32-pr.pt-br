---
description: Especifica o formato de saída para o decodificador.
ms.assetid: fdccdbfa-2814-4d21-9a7f-4121b79718e6
title: Propriedade AVDecCommonOutputFormat (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b69c536b3c9f1bf75e2a5741d0cdd16569b3dd8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500657"
---
# <a name="avdeccommonoutputformat-property"></a><span data-ttu-id="65951-103">Propriedade AVDecCommonOutputFormat</span><span class="sxs-lookup"><span data-stu-id="65951-103">AVDecCommonOutputFormat property</span></span>

<span data-ttu-id="65951-104">Especifica o formato de saída para o decodificador.</span><span class="sxs-lookup"><span data-stu-id="65951-104">Specifies the output format for the decoder.</span></span>

<span data-ttu-id="65951-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="65951-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="65951-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="65951-106">Data type</span></span>

<span data-ttu-id="65951-107">**BSTR** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="65951-107">**BSTR** (**VT\_BSTR**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="65951-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="65951-108">Property GUID</span></span>

<span data-ttu-id="65951-109">**CODECAPI \_ AVDecCommonOutputFormat**</span><span class="sxs-lookup"><span data-stu-id="65951-109">**CODECAPI\_AVDecCommonOutputFormat**</span></span>

## <a name="property-value"></a><span data-ttu-id="65951-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="65951-110">Property value</span></span>



| <span data-ttu-id="65951-111">GUID</span><span class="sxs-lookup"><span data-stu-id="65951-111">GUID</span></span>                                                               | <span data-ttu-id="65951-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="65951-112">Description</span></span>                                                                                                                                                                                                         |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65951-113">CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM</span><span class="sxs-lookup"><span data-stu-id="65951-113">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM</span></span>                        | <span data-ttu-id="65951-114">Áudio PCM, usando qualquer número de canais</span><span class="sxs-lookup"><span data-stu-id="65951-114">PCM audio, using any number of channels</span></span>                                                                                                                                                                             |
| <span data-ttu-id="65951-115">CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ fone de ouvido</span><span class="sxs-lookup"><span data-stu-id="65951-115">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM\_Headphones</span></span>            | <span data-ttu-id="65951-116">Áudio PCM estéreo, usando somente à esquerda/à direita (lo/ro) downmix</span><span class="sxs-lookup"><span data-stu-id="65951-116">Stereo PCM audio, using left-only/right-only (Lo/Ro) downmix</span></span>                                                                                                                                                        |
| <span data-ttu-id="65951-117">CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ estéreo \_ auto</span><span class="sxs-lookup"><span data-stu-id="65951-117">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM\_Stereo\_Auto</span></span>          | <span data-ttu-id="65951-118">Áudio PCM estéreo, usando a seleção automática do modo estéreo downmix (lo/ro ou lt/RT).</span><span class="sxs-lookup"><span data-stu-id="65951-118">Stereo PCM audio, using automatic selection of the stereo downmix mode (Lo/Ro or Lt/Rt).</span></span> <span data-ttu-id="65951-119">Você pode usar esse valor para formatos de áudio nos quais o fluxo de entrada define o modo downmix preferencial, como Dolby AC-3.</span><span class="sxs-lookup"><span data-stu-id="65951-119">You can use this value for audio formats in which the input stream defines the preferred downmix mode, such as Dolby AC-3.</span></span> |
| <span data-ttu-id="65951-120">CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ estéreo \_ MatrixEncoded</span><span class="sxs-lookup"><span data-stu-id="65951-120">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM\_Stereo\_MatrixEncoded</span></span> | <span data-ttu-id="65951-121">Áudio PCM estéreo, usando estéreo downmix codificado em matriz (LT/RT)</span><span class="sxs-lookup"><span data-stu-id="65951-121">Stereo PCM audio, using matrix-encoded stereo downmix (Lt/Rt)</span></span>                                                                                                                                                       |
| <span data-ttu-id="65951-122">CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ SPDIF \_ fragmentado</span><span class="sxs-lookup"><span data-stu-id="65951-122">CODECAPI\_GUID\_AVDecAudioOutputFormat\_SPDIF\_Bitstream</span></span>           | <span data-ttu-id="65951-123">S/PDIF (formato de interface digital Sony/Philips) fragmentado compactados, conforme definido pelo IEC-60958</span><span class="sxs-lookup"><span data-stu-id="65951-123">S/PDIF (Sony/Philips Digital Interface Format) compressed bitstream, as defined by IEC-60958</span></span>                                                                                                                        |
| <span data-ttu-id="65951-124">CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ SPDIF \_ PCM</span><span class="sxs-lookup"><span data-stu-id="65951-124">CODECAPI\_GUID\_AVDecAudioOutputFormat\_SPDIF\_PCM</span></span>                 | <span data-ttu-id="65951-125">Estéreo PCM S/PDIF, conforme definido por IEC-60958</span><span class="sxs-lookup"><span data-stu-id="65951-125">S/PDIF PCM stereo, as defined by IEC-60958</span></span>                                                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="65951-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65951-126">Requirements</span></span>



| <span data-ttu-id="65951-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="65951-127">Requirement</span></span> | <span data-ttu-id="65951-128">Valor</span><span class="sxs-lookup"><span data-stu-id="65951-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65951-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65951-129">Minimum supported client</span></span><br/> | <span data-ttu-id="65951-130">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="65951-130">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="65951-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65951-131">Minimum supported server</span></span><br/> | <span data-ttu-id="65951-132">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="65951-132">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="65951-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="65951-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="65951-134"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="65951-134"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65951-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="65951-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65951-136">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="65951-136">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="65951-137">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="65951-137">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




