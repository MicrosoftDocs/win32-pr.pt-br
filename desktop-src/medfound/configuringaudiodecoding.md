---
description: Configurando a decodificação de áudio
ms.assetid: 362bd3bc-1474-4132-a8a8-e5dc0bba80e7
title: Configurando a decodificação de áudio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da4d6a9d41b5c504ff60f25db20265072218caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646607"
---
# <a name="configuring-audio-decoding-microsoft-media-foundation"></a><span data-ttu-id="b07cf-103">Configurando a decodificação de áudio (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="b07cf-103">Configuring Audio Decoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="b07cf-104">A decodificação do conteúdo de áudio do Windows Media é muito mais fácil do que codificá-lo.</span><span class="sxs-lookup"><span data-stu-id="b07cf-104">Decoding Windows Media Audio content is much easier than encoding it.</span></span> <span data-ttu-id="b07cf-105">Depois de criar um objeto de decodificador de áudio, defina o tipo de entrada usando o método **IMediaObject:: SetInputType** ou **IMFTransform:: SetInputType** .</span><span class="sxs-lookup"><span data-stu-id="b07cf-105">After creating an audio decoder object, set the input type by using the **IMediaObject::SetInputType** or **IMFTransform::SetInputType** method.</span></span> <span data-ttu-id="b07cf-106">O tipo de mídia que você usa para a entrada do decodificador deve corresponder ao tipo de saída que foi usado quando o conteúdo foi codificado.</span><span class="sxs-lookup"><span data-stu-id="b07cf-106">The media type that you use for the decoder input must match the output type that was used when the content was encoded.</span></span> <span data-ttu-id="b07cf-107">Isso inclui os dados de formato estendidos anexados à estrutura **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="b07cf-107">This includes the extended format data appended to the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="b07cf-108">Você deve garantir que esses dados estejam corretos, pois o decodificador não pode processar amostras sem ele.</span><span class="sxs-lookup"><span data-stu-id="b07cf-108">You must ensure that this data is correct, because the decoder cannot process samples without it.</span></span>

<span data-ttu-id="b07cf-109">Depois de definir o tipo de entrada, você pode configurar os recursos de decodificador que deseja usar.</span><span class="sxs-lookup"><span data-stu-id="b07cf-109">After setting the input type, you can configure any decoder features you want to use.</span></span> <span data-ttu-id="b07cf-110">Os recursos do decodificador, como os usados para codificação, são definidos usando os métodos de **IPropertyBag** ou **IPropertyStore**.</span><span class="sxs-lookup"><span data-stu-id="b07cf-110">Decoder features, like those used for encoding, are set using the methods of **IPropertyBag** or **IPropertyStore**.</span></span>

<span data-ttu-id="b07cf-111">Depois que o tipo de entrada é definido e todos os recursos do decodificador são configurados, você pode enumerar os tipos de saída com suporte pelo decodificador fazendo chamadas para **IMediaObject:: GetOutputType** ou **IMFTransform:: GetOutputType**.</span><span class="sxs-lookup"><span data-stu-id="b07cf-111">After the input type is set and all decoder features are configured, you can enumerate the output types supported by the decoder by making calls to **IMediaObject::GetOutputType** or **IMFTransform::GetOutputType**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b07cf-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b07cf-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b07cf-113">Trabalhando com áudio</span><span class="sxs-lookup"><span data-stu-id="b07cf-113">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



