---
description: As classes base do DirectShow fornecem funções auxiliares para lidar com a \_ estrutura do tipo de mídia am \_ .
ms.assetid: 4dbea5b4-bf78-4253-be48-d81b77be6e77
title: Funções de tipo de mídia (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Media
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a39fe9a9599a1d85c14a226106f5c8d7080b721f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784117"
---
# <a name="media-type-functions"></a><span data-ttu-id="929da-103">Funções de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="929da-103">Media Type Functions</span></span>

<span data-ttu-id="929da-104">As classes base do DirectShow fornecem funções auxiliares para lidar com a estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="929da-104">The DirectShow base classes provides helper functions for handling the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

<span data-ttu-id="929da-105">A estrutura do **\_ \_ tipo de mídia am** contém um ponteiro (o membro **pbFormat** ) para outro bloco de memória, que é chamado de *bloco de formato*.</span><span class="sxs-lookup"><span data-stu-id="929da-105">The **AM\_MEDIA\_TYPE** structure contains a pointer (the **pbFormat** member) to another block of memory, which is called the *format block*.</span></span> <span data-ttu-id="929da-106">Ao trabalhar com essa estrutura, portanto, você deve ter cuidado com a alocação de memória para evitar vazamentos de memória.</span><span class="sxs-lookup"><span data-stu-id="929da-106">When you work with this structure, therefore, you must be careful about memory allocation in order to avoid memory leaks.</span></span>

<span data-ttu-id="929da-107">As seguintes funções alocam memória:</span><span class="sxs-lookup"><span data-stu-id="929da-107">The following functions allocate memory:</span></span>

-   <span data-ttu-id="929da-108">**CreateMediaType** aloca uma nova estrutura de **\_ \_ tipo de mídia am** e o bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="929da-108">**CreateMediaType** allocates a new **AM\_MEDIA\_TYPE** structure and the format block.</span></span>
-   <span data-ttu-id="929da-109">**CopyMediaType** copia para uma estrutura **de \_ \_ tipo de mídia am** existente, mas aloca o bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="929da-109">**CopyMediaType** copies to an existing **AM\_MEDIA\_TYPE** structure, but allocates the format block.</span></span>
-   <span data-ttu-id="929da-110">**CreateAudioMediaType** Inicializa uma estrutura **de \_ \_ tipo de mídia am** existente e, opcionalmente, aloca o bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="929da-110">**CreateAudioMediaType** initializes an existing **AM\_MEDIA\_TYPE** structure, and optionally allocates the format block.</span></span>

<span data-ttu-id="929da-111">As seguintes funções liberam a memória:</span><span class="sxs-lookup"><span data-stu-id="929da-111">The following functions free memory:</span></span>

-   <span data-ttu-id="929da-112">**FreeMediaType** libera o bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="929da-112">**FreeMediaType** releases the format block.</span></span>
-   <span data-ttu-id="929da-113">O **DeleteMediaType** libera uma estrutura de **\_ \_ tipo de mídia am** , incluindo o bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="929da-113">**DeleteMediaType** frees an **AM\_MEDIA\_TYPE** structure, including the format block.</span></span>



| <span data-ttu-id="929da-114">Função</span><span class="sxs-lookup"><span data-stu-id="929da-114">Function</span></span>                                             | <span data-ttu-id="929da-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="929da-115">Description</span></span>                                                                                                 |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="929da-116">**CopyMediaType**</span><span class="sxs-lookup"><span data-stu-id="929da-116">**CopyMediaType**</span></span>](copymediatype.md)               | <span data-ttu-id="929da-117">Copia uma estrutura de **tipo de \_ mídia \_ am** alocada para tarefa.</span><span class="sxs-lookup"><span data-stu-id="929da-117">Copies a task-allocated **AM\_MEDIA\_TYPE** structure.</span></span>                                                      |
| [<span data-ttu-id="929da-118">**CreateAudioMediaType**</span><span class="sxs-lookup"><span data-stu-id="929da-118">**CreateAudioMediaType**</span></span>](createaudiomediatype.md) | <span data-ttu-id="929da-119">Inicializa uma estrutura de tipo de mídia de acordo com uma estrutura de formato Wave.</span><span class="sxs-lookup"><span data-stu-id="929da-119">Initializes a media type structure given a wave format structure.</span></span>                                           |
| [<span data-ttu-id="929da-120">**CreateMediaType**</span><span class="sxs-lookup"><span data-stu-id="929da-120">**CreateMediaType**</span></span>](createmediatype.md)           | <span data-ttu-id="929da-121">Aloca e Inicializa uma estrutura de **\_ \_ tipo de mídia am** de uma estrutura de **\_ \_ tipo de mídia am** existente.</span><span class="sxs-lookup"><span data-stu-id="929da-121">Allocates and initializes an **AM\_MEDIA\_TYPE** structure, from an existing **AM\_MEDIA\_TYPE** structure.</span></span> |
| [<span data-ttu-id="929da-122">**DeleteMediaType**</span><span class="sxs-lookup"><span data-stu-id="929da-122">**DeleteMediaType**</span></span>](deletemediatype.md)           | <span data-ttu-id="929da-123">Exclui uma estrutura de **tipo de \_ mídia \_ am** alocada para tarefa.</span><span class="sxs-lookup"><span data-stu-id="929da-123">Deletes a task-allocated **AM\_MEDIA\_TYPE** structure.</span></span>                                                     |
| [<span data-ttu-id="929da-124">**FreeMediaType**</span><span class="sxs-lookup"><span data-stu-id="929da-124">**FreeMediaType**</span></span>](freemediatype.md)               | <span data-ttu-id="929da-125">Libera uma estrutura de **\_ \_ tipo de mídia am** alocada para tarefa da memória.</span><span class="sxs-lookup"><span data-stu-id="929da-125">Frees a task-allocated **AM\_MEDIA\_TYPE** structure from memory.</span></span>                                           |



 

## <a name="requirements"></a><span data-ttu-id="929da-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="929da-126">Requirements</span></span>



| <span data-ttu-id="929da-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="929da-127">Requirement</span></span> | <span data-ttu-id="929da-128">Valor</span><span class="sxs-lookup"><span data-stu-id="929da-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="929da-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="929da-129">Header</span></span><br/>  | <dl> <span data-ttu-id="929da-130"><dt>Mtype. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="929da-130"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="929da-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="929da-131">Library</span></span><br/> | <dl> <span data-ttu-id="929da-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="929da-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




