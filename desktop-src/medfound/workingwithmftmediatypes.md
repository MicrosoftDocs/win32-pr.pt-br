---
description: Trabalhando com tipos de mídia MFT
ms.assetid: 16c270ee-f246-4222-97e9-d8d0fe009155
title: Trabalhando com tipos de mídia MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98bfc996704f6069ca1d16570b33f456ea1cc115
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104172466"
---
# <a name="working-with-mft-media-types"></a><span data-ttu-id="e8a82-103">Trabalhando com tipos de mídia MFT</span><span class="sxs-lookup"><span data-stu-id="e8a82-103">Working with MFT Media Types</span></span>

<span data-ttu-id="e8a82-104">Um tipo de mídia é uma maneira de descrever o formato de um fluxo de mídia.</span><span class="sxs-lookup"><span data-stu-id="e8a82-104">A media type is a way to describe the format of a media stream.</span></span> <span data-ttu-id="e8a82-105">No Media Foundation, os tipos de mídia são representados pela interface **IMFMediaType** .</span><span class="sxs-lookup"><span data-stu-id="e8a82-105">In Media Foundation, media types are represented by the **IMFMediaType** interface.</span></span> <span data-ttu-id="e8a82-106">Essa interface herda a interface **IMFAttributes** .</span><span class="sxs-lookup"><span data-stu-id="e8a82-106">This interface inherits the **IMFAttributes** interface.</span></span> <span data-ttu-id="e8a82-107">Os detalhes de um tipo de mídia são especificados como atributos.</span><span class="sxs-lookup"><span data-stu-id="e8a82-107">The details of a media type are specified as attributes.</span></span>

<span data-ttu-id="e8a82-108">Para criar um novo tipo de mídia, chame a função **MFCreateMediaType** .</span><span class="sxs-lookup"><span data-stu-id="e8a82-108">To create a new media type, call the **MFCreateMediaType** function.</span></span> <span data-ttu-id="e8a82-109">Essa função retorna um ponteiro para a interface **IMFMediaType** .</span><span class="sxs-lookup"><span data-stu-id="e8a82-109">This function returns a pointer to the **IMFMediaType** interface.</span></span> <span data-ttu-id="e8a82-110">O tipo de mídia inicialmente não tem nenhum atributo.</span><span class="sxs-lookup"><span data-stu-id="e8a82-110">The media type initially has no attributes.</span></span>

<span data-ttu-id="e8a82-111">O SDK do Media Foundation fornece várias funções auxiliares para inicializar tipos de mídia a partir de estruturas de formato.</span><span class="sxs-lookup"><span data-stu-id="e8a82-111">The Media Foundation SDK provides several helper functions for initializing Media Types from format structures.</span></span> <span data-ttu-id="e8a82-112">Por exemplo, a função **MFInitMediaTypeFromVideoInfoHeader** Inicializa um tipo de vídeo de uma estrutura **VIDEOINFOHEADER** e a função **MFInitMediaTypeFromWaveFormatEx** Inicializa um tipo de vídeo de uma estrutura **WAVEFORMATEX** ou **WAVEFORMATEXTENSIBLE** .</span><span class="sxs-lookup"><span data-stu-id="e8a82-112">For example the function **MFInitMediaTypeFromVideoInfoHeader** initializes a video type from a **VIDEOINFOHEADER** structure, and the function **MFInitMediaTypeFromWaveFormatEx** initializes a video type from a **WAVEFORMATEX** or **WAVEFORMATEXTENSIBLE** structure.</span></span>

<span data-ttu-id="e8a82-113">Os tipos de formato usados pelos codecs geralmente são limitados aos descritos pelas estruturas **VIDEOINFOHEADER** e **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="e8a82-113">The format types that are used by the codecs are generally limited to those described by the **VIDEOINFOHEADER** and **WAVEFORMATEX** structures.</span></span>

<span data-ttu-id="e8a82-114">Mais informações sobre como criar e acessar Media Foundation tipos de mídia estão disponíveis na documentação do SDK do Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="e8a82-114">More information on creating and accessing Media Foundation media types is available in the Media Foundation SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8a82-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e8a82-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8a82-116">Trabalhando com codec MFTs</span><span class="sxs-lookup"><span data-stu-id="e8a82-116">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



