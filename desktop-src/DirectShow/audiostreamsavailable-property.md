---
description: A propriedade AudioStreamsAvailable recupera o número de fluxos de áudio disponíveis no título atual.
ms.assetid: 4359ec30-920a-4b34-8e27-4cf1d9452aa8
title: Propriedade AudioStreamsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb68020b30f4349fcbbb464150624d75250a0dbf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825712"
---
# <a name="audiostreamsavailable-property"></a><span data-ttu-id="4cc1f-103">Propriedade AudioStreamsAvailable</span><span class="sxs-lookup"><span data-stu-id="4cc1f-103">AudioStreamsAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="4cc1f-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="4cc1f-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="4cc1f-106">A `AudioStreamsAvailable` propriedade recupera o número de fluxos de áudio disponíveis no título atual.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-106">The `AudioStreamsAvailable` property retrieves the number of audio streams available in the current title.</span></span>

``` syntax
[ iStreams = ] MSWebDVD.AudioStreamsAvailable
```

## <a name="return-value"></a><span data-ttu-id="4cc1f-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="4cc1f-107">Return Value</span></span>

<span data-ttu-id="4cc1f-108">Retorna um valor inteiro de 1 a 8 que representa o número de fluxos de áudio disponíveis no título atual.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-108">Returns an integer value from 1 through 8 representing the number of audio streams available in the current title.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cc1f-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="4cc1f-109">Remarks</span></span>

<span data-ttu-id="4cc1f-110">Esta propriedade é somente leitura sem valor padrão.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-110">This property is read-only with no default value.</span></span> <span data-ttu-id="4cc1f-111">O uso principal de vários fluxos de áudio é fornecer as trilhas sonoras do filme em mais de um idioma.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-111">The primary use of multiple audio streams is to provide movie soundtracks in more than one language.</span></span> <span data-ttu-id="4cc1f-112">Normalmente, nem todos os títulos em um disco têm todos os fluxos de áudio habilitados.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-112">Typically, not every title on a disc has all audio streams enabled.</span></span> <span data-ttu-id="4cc1f-113">Por exemplo, o filme de recursos pode ter trilhas sonoras em três idiomas diferentes, mas os trailers podem ter apenas uma trilha sonora em inglês.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-113">For example, the feature movie might have soundtracks in three different languages, but the trailers might have only an English soundtrack.</span></span> <span data-ttu-id="4cc1f-114">Antes que um usuário possa selecionar um fluxo, o aplicativo deve determinar quais fluxos estão disponíveis no título atual.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-114">Before a user can select a stream, the application must determine which streams are available within the current title.</span></span> <span data-ttu-id="4cc1f-115">Observe que os fluxos específicos são identificados por um índice de zero a 7.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-115">Note that particular streams are identified by an index from zero through 7.</span></span>

<span data-ttu-id="4cc1f-116">Os discos geralmente apresentam um menu mostrando as trilhas sonoras disponíveis, permitindo que o usuário selecione o fluxo de áudio a ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="4cc1f-116">Discs generally present a menu showing the available soundtracks, enabling the user to select the audio stream to enable.</span></span>

## <a name="see-also"></a><span data-ttu-id="4cc1f-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="4cc1f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cc1f-118">**GetAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="4cc1f-118">**GetAudioLanguage**</span></span>](getaudiolanguage-method.md)
</dt> </dl>

 

 



