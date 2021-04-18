---
description: Por que um decodificador não aceita o formato de entrada que eu defini?
ms.assetid: 19aa5677-bc3f-41d7-ad64-7c75021d907b
title: Por que um decodificador não aceita o formato de entrada que eu defini?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32ae4506fb6ed940bf0b4fffcf82ab78562872d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781376"
---
# <a name="why-does-a-decoder-not-accept-the-input-format-that-i-set"></a><span data-ttu-id="b7a67-103">Por que um decodificador não aceita o formato de entrada que eu defini?</span><span class="sxs-lookup"><span data-stu-id="b7a67-103">Why does a decoder not accept the input format that I set?</span></span>

<span data-ttu-id="b7a67-104">Há muitas razões pelas quais um decodificador pode rejeitar um formato.</span><span class="sxs-lookup"><span data-stu-id="b7a67-104">There are many reasons why a decoder might reject a format.</span></span> <span data-ttu-id="b7a67-105">O mais comum são dados de formato estendidos ausentes ou incorretos.</span><span class="sxs-lookup"><span data-stu-id="b7a67-105">The most common is missing or incorrect extended format data.</span></span> <span data-ttu-id="b7a67-106">Os dados de formato estendido são informações específicas do codec que são acrescentadas à estrutura que descreve o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="b7a67-106">The extended format data is codec-specific information that is appended to the structure describing the media type.</span></span>

<span data-ttu-id="b7a67-107">Quando você enumera um tipo de saída usando um objeto de codificador, o membro **pbFormat** da estrutura do [**\_ \_ tipo de mídia DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) apontará para uma estrutura **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="b7a67-107">When you enumerate an output type using an encoder object, the **pbFormat** member of the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure will point to a **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="b7a67-108">Essa estrutura tem dados de formato estendidos anexados a ele, e o tamanho desses dados é armazenado no membro **WAVEFORMATEX. cbSize** .</span><span class="sxs-lookup"><span data-stu-id="b7a67-108">This structure has extended format data appended to it, and the size of that data is stored in the **WAVEFORMATEX.cbSize** member.</span></span> <span data-ttu-id="b7a67-109">Independentemente do contêiner usado para armazenar os dados compactados, você deve persistir a estrutura **WAVEFORMATEX** e usá-la no tipo de entrada para o decodificador.</span><span class="sxs-lookup"><span data-stu-id="b7a67-109">Regardless of the container used to store the compressed data, you must persist the **WAVEFORMATEX** structure and use it in the input type for the decoder.</span></span> <span data-ttu-id="b7a67-110">Sem os dados de formato estendidos, o decodificador não pode descompactar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="b7a67-110">Without the extended format data, the decoder cannot decompress the content.</span></span>

<span data-ttu-id="b7a67-111">Para formatos de vídeo, você deve recuperar manualmente os dados de formato estendido e acrescentá-los à estrutura **VIDEOINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="b7a67-111">For video formats, you must manually retrieve the extended format data and append it to the **VIDEOINFOHEADER** structure.</span></span> <span data-ttu-id="b7a67-112">Para obter mais informações, consulte [usando dados privados do codec de vídeo](usingvideocodecprivatedata.md).</span><span class="sxs-lookup"><span data-stu-id="b7a67-112">For more information, see [Using Video Codec Private Data](usingvideocodecprivatedata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7a67-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b7a67-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7a67-114">Perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="b7a67-114">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 
