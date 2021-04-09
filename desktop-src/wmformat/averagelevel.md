---
title: AverageLevel
description: O atributo AverageLevel contém um valor de amplitude de 16 bits que designa o nível médio de volume de conteúdo de áudio.
ms.assetid: e6270ac8-5de3-4dee-824c-ba25fdd272c8
keywords:
- Formato de mídia do Windows AverageLevel
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 632379e42fa6c64e44018173b9d40340add4ee61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006519"
---
# <a name="averagelevel"></a><span data-ttu-id="7edc4-104">AverageLevel</span><span class="sxs-lookup"><span data-stu-id="7edc4-104">AverageLevel</span></span>

<span data-ttu-id="7edc4-105">O atributo **AverageLevel** contém um valor de amplitude de 16 bits que designa o nível médio de volume de conteúdo de áudio.</span><span class="sxs-lookup"><span data-stu-id="7edc4-105">The **AverageLevel** attribute contains a 16-bit amplitude value designating the average volume level of audio content.</span></span> <span data-ttu-id="7edc4-106">Com o [**picovalue**](peakvalue.md), esse atributo é usado para normalização.</span><span class="sxs-lookup"><span data-stu-id="7edc4-106">With [**PeakValue**](peakvalue.md), this attribute is used for normalization.</span></span> <span data-ttu-id="7edc4-107">A normalização é o processo de ajustar o nível de volume de reprodução de arquivos de áudio para que as partes mais alta da reprodução de arquivos no mesmo nível e o volume médio de cada um seja o mesmo.</span><span class="sxs-lookup"><span data-stu-id="7edc4-107">Normalization is the process of adjusting the playback volume level of audio files so that the loudest parts of files playback at the same level and the average volume for each is the same.</span></span>

## <a name="global-constant"></a><span data-ttu-id="7edc4-108">Constante global</span><span class="sxs-lookup"><span data-stu-id="7edc4-108">Global Constant</span></span>

<span data-ttu-id="7edc4-109">g \_ wszAverageLevel</span><span class="sxs-lookup"><span data-stu-id="7edc4-109">g\_wszAverageLevel</span></span>

## <a name="data-type"></a><span data-ttu-id="7edc4-110">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="7edc4-110">Data Type</span></span>

<span data-ttu-id="7edc4-111">**WMT \_ tipo \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="7edc4-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="7edc4-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="7edc4-112">Remarks</span></span>

<span data-ttu-id="7edc4-113">Esse atributo é definido pelo objeto do gravador com base nas informações do codec.</span><span class="sxs-lookup"><span data-stu-id="7edc4-113">This attribute is set by the writer object based on information from the codec.</span></span> <span data-ttu-id="7edc4-114">Somente os fluxos compactados com um dos codecs de áudio do Windows Media têm um valor definido automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7edc4-114">Only streams compressed with one of the Windows Media Audio codecs have an automatically set value.</span></span>

<span data-ttu-id="7edc4-115">**AverageLevel** não é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="7edc4-115">**AverageLevel** is not read-only.</span></span> <span data-ttu-id="7edc4-116">No entanto, se o arquivo for reproduzido pelo Windows Media Player, você não deverá alterar esse valor.</span><span class="sxs-lookup"><span data-stu-id="7edc4-116">However, if the file will be played by the Windows Media Player, you should not alter this value.</span></span> <span data-ttu-id="7edc4-117">O Windows Media Player usa isso para normalizar os níveis de arquivos em uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="7edc4-117">The Windows Media Player uses this for normalizing the levels of files in a playlist.</span></span>

## <a name="see-also"></a><span data-ttu-id="7edc4-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="7edc4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7edc4-119">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="7edc4-119">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




