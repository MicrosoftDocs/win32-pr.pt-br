---
description: Configura a fonte de mídia do ASF para usar a busca iterativa se o arquivo de origem não tiver nenhum índice.
ms.assetid: 0dd6f202-cdbc-4a28-8907-5530a0a2141b
title: Propriedade MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cdc22f0b4f5490c7691cc40166cf929a16ba64
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103663805"
---
# <a name="mfpkey_asfmediasource_iterativeseekifnoindex-property"></a><span data-ttu-id="d7dfa-103">\_Propriedade MFPKEY ASFMediaSource \_ IterativeSeekIfNoIndex</span><span class="sxs-lookup"><span data-stu-id="d7dfa-103">MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex property</span></span>

<span data-ttu-id="d7dfa-104">Configura a fonte de mídia do ASF para usar a busca iterativa se o arquivo de origem não tiver nenhum índice.</span><span class="sxs-lookup"><span data-stu-id="d7dfa-104">Configures the ASF media source to use iterative seeking if the source file has no index.</span></span>



<span data-ttu-id="d7dfa-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d7dfa-105">Data type</span></span>

<span data-ttu-id="d7dfa-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="d7dfa-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="d7dfa-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="d7dfa-107">PROPVARIANT member</span></span>

<span data-ttu-id="d7dfa-108">**BOOL de variante \_**</span><span class="sxs-lookup"><span data-stu-id="d7dfa-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="d7dfa-109">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="d7dfa-109">VT\_BOOL</span></span>

<span data-ttu-id="d7dfa-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="d7dfa-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="d7dfa-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7dfa-111">Remarks</span></span>

<span data-ttu-id="d7dfa-112">Use essa propriedade para configurar a origem da mídia ASF.</span><span class="sxs-lookup"><span data-stu-id="d7dfa-112">Use this property to configure the ASF media source.</span></span> <span data-ttu-id="d7dfa-113">Para definir a propriedade, passe um ponteiro **IPropertyStore** para o *resolvedor de origem*.</span><span class="sxs-lookup"><span data-stu-id="d7dfa-113">To set the property, pass an **IPropertyStore** pointer to the *source resolver*.</span></span> <span data-ttu-id="d7dfa-114">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="d7dfa-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="d7dfa-115">A *busca iterativa* é um algoritmo para localizar uma posição em um arquivo ASF sem índice.</span><span class="sxs-lookup"><span data-stu-id="d7dfa-115">*Iterative seeking* is an algorithm to find a position in an ASF file with no index.</span></span> <span data-ttu-id="d7dfa-116">Ele usa uma série de aproximações, com base na taxa média de bits, para ficar progressivamente mais próximo do tempo de busca de destino.</span><span class="sxs-lookup"><span data-stu-id="d7dfa-116">It uses a series of approximations, based on the average bit rate, to get progressively closer to the target seek time.</span></span> <span data-ttu-id="d7dfa-117">(O algoritmo é semelhante a uma pesquisa binária.) A busca iterativa pode levar mais tempo do que procurar por índice, portanto, ela está desabilitada por padrão.</span><span class="sxs-lookup"><span data-stu-id="d7dfa-117">(The algorithm is similar to a binary search.) Iterative seeking can take longer than seeking by index, so it is disabled by default.</span></span>

<span data-ttu-id="d7dfa-118">Se você definir essa propriedade, use as seguintes propriedades para definir os parâmetros de pesquisa:</span><span class="sxs-lookup"><span data-stu-id="d7dfa-118">If you set this property, use the following properties to set the search parameters:</span></span>

-   [<span data-ttu-id="d7dfa-119">Contagem máxima de MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ \_</span><span class="sxs-lookup"><span data-stu-id="d7dfa-119">MFPKEY\_ASFMediaSource\_IterativeSeek\_Max\_Count</span></span>](mfpkey-asfmediasource-iterativeseek-max-count.md)
-   [<span data-ttu-id="d7dfa-120">MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ tolerância \_ a \_ milissegundos</span><span class="sxs-lookup"><span data-stu-id="d7dfa-120">MFPKEY\_ASFMediaSource\_IterativeSeek\_Tolerance\_In\_MilliSecond</span></span>](mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md)

<span data-ttu-id="d7dfa-121">Essas propriedades definem o número máximo de iterações e a tolerância, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d7dfa-121">These properties set the maximum number of iterations and the tolerance, respectively.</span></span> <span data-ttu-id="d7dfa-122">O algoritmo é interrompido quando atinge o número máximo de iterações ou quando encontra um pacote cuja distância do tempo de busca está dentro da tolerância especificada.</span><span class="sxs-lookup"><span data-stu-id="d7dfa-122">The algorithm halts when it reaches the maximum number of iterations, or when it finds a packet whose distance from the seek time is within the specified tolerance.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7dfa-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7dfa-123">Requirements</span></span>



| <span data-ttu-id="d7dfa-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7dfa-124">Requirement</span></span> | <span data-ttu-id="d7dfa-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d7dfa-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d7dfa-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7dfa-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d7dfa-127">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d7dfa-127">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="d7dfa-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7dfa-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d7dfa-129">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="d7dfa-129">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d7dfa-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7dfa-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7dfa-131"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7dfa-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7dfa-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7dfa-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7dfa-133">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d7dfa-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




