---
description: A classe CMediaType gerencia tipos de mídia. Essa classe herda a \_ estrutura do tipo de mídia am \_ . Ele pode ser convertido em uma variável do tipo de mídia do tipo AM \_ \_ .
ms.assetid: ea3d03a1-cca4-4a6e-9d1d-4cebe710f913
title: Classe CMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f91578f91840c316347c6266e678357e31c8a284
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755347"
---
# <a name="cmediatype-class"></a><span data-ttu-id="e0d39-105">Classe CMediaType</span><span class="sxs-lookup"><span data-stu-id="e0d39-105">CMediaType class</span></span>

![hierarquia de classe CMediaType](images/mtype01.png)

<span data-ttu-id="e0d39-107">A `CMediaType` classe gerencia os tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="e0d39-107">The `CMediaType` class manages media types.</span></span> <span data-ttu-id="e0d39-108">Essa classe herda a estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="e0d39-108">This class inherits the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="e0d39-109">Ele pode ser convertido em uma variável do tipo **de \_ mídia \_** do tipo am.</span><span class="sxs-lookup"><span data-stu-id="e0d39-109">It can be cast to a variable of type **AM\_MEDIA\_TYPE**.</span></span>



| <span data-ttu-id="e0d39-110">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="e0d39-110">Public Methods</span></span>                                                      | <span data-ttu-id="e0d39-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0d39-111">Description</span></span>                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="e0d39-112">**CMediaType**</span><span class="sxs-lookup"><span data-stu-id="e0d39-112">**CMediaType**</span></span>](cmediatype-cmediatype.md)                         | <span data-ttu-id="e0d39-113">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="e0d39-113">Constructor method.</span></span>                                                            |
| [<span data-ttu-id="e0d39-114">**~ CMediaType**</span><span class="sxs-lookup"><span data-stu-id="e0d39-114">**~CMediaType**</span></span>](cmediatype--cmediatype.md)                       | <span data-ttu-id="e0d39-115">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="e0d39-115">Destructor method.</span></span>                                                             |
| [<span data-ttu-id="e0d39-116">**Definir**</span><span class="sxs-lookup"><span data-stu-id="e0d39-116">**Set**</span></span>](cmediatype-set.md)                                       | <span data-ttu-id="e0d39-117">Define o tipo de mídia de outro tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="e0d39-117">Sets the media type from another media type.</span></span>                                   |
| [<span data-ttu-id="e0d39-118">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="e0d39-118">**IsValid**</span></span>](cmediatype-isvalid.md)                               | <span data-ttu-id="e0d39-119">Determina se um tipo principal foi atribuído a este objeto.</span><span class="sxs-lookup"><span data-stu-id="e0d39-119">Determines whether a major type has been assigned to this object.</span></span>              |
| [<span data-ttu-id="e0d39-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e0d39-120">**Type**</span></span>](cmediatype-type.md)                                     | <span data-ttu-id="e0d39-121">Recupera o tipo principal.</span><span class="sxs-lookup"><span data-stu-id="e0d39-121">Retrieves the major type.</span></span>                                                      |
| [<span data-ttu-id="e0d39-122">**Tipo de**</span><span class="sxs-lookup"><span data-stu-id="e0d39-122">**SetType**</span></span>](cmediatype-settype.md)                               | <span data-ttu-id="e0d39-123">Especifica o tipo principal.</span><span class="sxs-lookup"><span data-stu-id="e0d39-123">Specifies the major type.</span></span>                                                      |
| [<span data-ttu-id="e0d39-124">**Subtipo**</span><span class="sxs-lookup"><span data-stu-id="e0d39-124">**Subtype**</span></span>](cmediatype-subtype.md)                               | <span data-ttu-id="e0d39-125">Recupera o subtipo.</span><span class="sxs-lookup"><span data-stu-id="e0d39-125">Retrieves the subtype.</span></span>                                                         |
| [<span data-ttu-id="e0d39-126">**SetSubtype**</span><span class="sxs-lookup"><span data-stu-id="e0d39-126">**SetSubtype**</span></span>](cmediatype-setsubtype.md)                         | <span data-ttu-id="e0d39-127">Especifica o subtipo.</span><span class="sxs-lookup"><span data-stu-id="e0d39-127">Specifies the subtype.</span></span>                                                         |
| [<span data-ttu-id="e0d39-128">**IsFixedSize**</span><span class="sxs-lookup"><span data-stu-id="e0d39-128">**IsFixedSize**</span></span>](cmediatype-isfixedsize.md)                       | <span data-ttu-id="e0d39-129">Determina se os exemplos têm um tamanho fixo ou uma variável.</span><span class="sxs-lookup"><span data-stu-id="e0d39-129">Determines if the samples have a fixed size or a variable size.</span></span>                |
| [<span data-ttu-id="e0d39-130">**IsTemporalCompressed**</span><span class="sxs-lookup"><span data-stu-id="e0d39-130">**IsTemporalCompressed**</span></span>](cmediatype-istemporalcompressed.md)     | <span data-ttu-id="e0d39-131">Determina se o fluxo usa a compactação temporal.</span><span class="sxs-lookup"><span data-stu-id="e0d39-131">Determines if the stream uses temporal compression.</span></span>                            |
| [<span data-ttu-id="e0d39-132">**Getsampleize**</span><span class="sxs-lookup"><span data-stu-id="e0d39-132">**GetSampleSize**</span></span>](cmediatype-getsamplesize.md)                   | <span data-ttu-id="e0d39-133">Recupera o tamanho da amostra.</span><span class="sxs-lookup"><span data-stu-id="e0d39-133">Retrieves the sample size.</span></span>                                                     |
| [<span data-ttu-id="e0d39-134">**Setsampleize**</span><span class="sxs-lookup"><span data-stu-id="e0d39-134">**SetSampleSize**</span></span>](cmediatype-setsamplesize.md)                   | <span data-ttu-id="e0d39-135">Especifica um tamanho de amostra fixo ou especifica que os exemplos têm um tamanho variável.</span><span class="sxs-lookup"><span data-stu-id="e0d39-135">Specifies a fixed sample size, or specifies that samples have a variable size.</span></span> |
| [<span data-ttu-id="e0d39-136">**Setvariableize**</span><span class="sxs-lookup"><span data-stu-id="e0d39-136">**SetVariableSize**</span></span>](cmediatype-setvariablesize.md)               | <span data-ttu-id="e0d39-137">Especifica que os exemplos não têm um tamanho fixo.</span><span class="sxs-lookup"><span data-stu-id="e0d39-137">Specifies that samples do not have a fixed size.</span></span>                               |
| [<span data-ttu-id="e0d39-138">**SetTemporalCompression**</span><span class="sxs-lookup"><span data-stu-id="e0d39-138">**SetTemporalCompression**</span></span>](cmediatype-settemporalcompression.md) | <span data-ttu-id="e0d39-139">Especifica se os exemplos são compactados usando a compactação temporal.</span><span class="sxs-lookup"><span data-stu-id="e0d39-139">Specifies whether samples are compressed using temporal compression.</span></span>           |
| [<span data-ttu-id="e0d39-140">**Formatar**</span><span class="sxs-lookup"><span data-stu-id="e0d39-140">**Format**</span></span>](cmediatype-format.md)                                 | <span data-ttu-id="e0d39-141">Recupera um ponteiro para o bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="e0d39-141">Retrieves a pointer to the format block.</span></span>                                       |
| [<span data-ttu-id="e0d39-142">**FormatLength**</span><span class="sxs-lookup"><span data-stu-id="e0d39-142">**FormatLength**</span></span>](cmediatype-formatlength.md)                     | <span data-ttu-id="e0d39-143">Recupera o comprimento do bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="e0d39-143">Retrieves the length of the format block.</span></span>                                      |
| [<span data-ttu-id="e0d39-144">**Setformatype**</span><span class="sxs-lookup"><span data-stu-id="e0d39-144">**SetFormatType**</span></span>](cmediatype-setformattype.md)                   | <span data-ttu-id="e0d39-145">Especifica o tipo do formato.</span><span class="sxs-lookup"><span data-stu-id="e0d39-145">Specifies the format type.</span></span>                                                     |
| [<span data-ttu-id="e0d39-146">**FormatType**</span><span class="sxs-lookup"><span data-stu-id="e0d39-146">**FormatType**</span></span>](cmediatype-formattype.md)                         | <span data-ttu-id="e0d39-147">Recupera o tipo de formato.</span><span class="sxs-lookup"><span data-stu-id="e0d39-147">Retrieves the format type.</span></span>                                                     |
| [<span data-ttu-id="e0d39-148">**SetFormat**</span><span class="sxs-lookup"><span data-stu-id="e0d39-148">**SetFormat**</span></span>](cmediatype-setformat.md)                           | <span data-ttu-id="e0d39-149">Especifica o bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="e0d39-149">Specifies the format block.</span></span>                                                    |
| [<span data-ttu-id="e0d39-150">**ResetFormatBuffer**</span><span class="sxs-lookup"><span data-stu-id="e0d39-150">**ResetFormatBuffer**</span></span>](cmediatype-resetformatbuffer.md)           | <span data-ttu-id="e0d39-151">Exclui o bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="e0d39-151">Deletes the format block.</span></span>                                                      |
| [<span data-ttu-id="e0d39-152">**AllocFormatBuffer**</span><span class="sxs-lookup"><span data-stu-id="e0d39-152">**AllocFormatBuffer**</span></span>](cmediatype-allocformatbuffer.md)           | <span data-ttu-id="e0d39-153">Aloca memória para o bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="e0d39-153">Allocates memory for the format block.</span></span>                                         |
| [<span data-ttu-id="e0d39-154">**ReallocFormatBuffer**</span><span class="sxs-lookup"><span data-stu-id="e0d39-154">**ReallocFormatBuffer**</span></span>](cmediatype-reallocformatbuffer.md)       | <span data-ttu-id="e0d39-155">Realoca o bloco de formato para um novo tamanho.</span><span class="sxs-lookup"><span data-stu-id="e0d39-155">Reallocates the format block to a new size.</span></span>                                    |
| [<span data-ttu-id="e0d39-156">**InitMediaType**</span><span class="sxs-lookup"><span data-stu-id="e0d39-156">**InitMediaType**</span></span>](cmediatype-initmediatype.md)                   | <span data-ttu-id="e0d39-157">Inicializa o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="e0d39-157">Initializes the media type.</span></span>                                                    |
| [<span data-ttu-id="e0d39-158">**MatchesPartial**</span><span class="sxs-lookup"><span data-stu-id="e0d39-158">**MatchesPartial**</span></span>](cmediatype-matchespartial.md)                 | <span data-ttu-id="e0d39-159">Determina se esse tipo de mídia corresponde a um tipo de mídia parcialmente especificado.</span><span class="sxs-lookup"><span data-stu-id="e0d39-159">Determines if this media type matches a partially specified media type.</span></span>        |
| [<span data-ttu-id="e0d39-160">**IsPartiallySpecified**</span><span class="sxs-lookup"><span data-stu-id="e0d39-160">**IsPartiallySpecified**</span></span>](cmediatype-ispartiallyspecified.md)     | <span data-ttu-id="e0d39-161">Determina se o tipo de mídia está parcialmente definido.</span><span class="sxs-lookup"><span data-stu-id="e0d39-161">Determines if the media type is partially defined.</span></span>                             |
| <span data-ttu-id="e0d39-162">Operadores</span><span class="sxs-lookup"><span data-stu-id="e0d39-162">Operators</span></span>                                                           | <span data-ttu-id="e0d39-163">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0d39-163">Description</span></span>                                                                    |
| [<span data-ttu-id="e0d39-164">**operador =**</span><span class="sxs-lookup"><span data-stu-id="e0d39-164">**operator =**</span></span>](cmediatype-operator-.md)                          | <span data-ttu-id="e0d39-165">Sobrecarrega o operador de atribuição para copiar um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="e0d39-165">Overloads the assignment operator to copy a media type.</span></span>                        |
| [<span data-ttu-id="e0d39-166">**operador = =**</span><span class="sxs-lookup"><span data-stu-id="e0d39-166">**operator ==**</span></span>](cmediatype-operator--.md)                        | <span data-ttu-id="e0d39-167">Testa a igualdade entre objetos `CMediaType`.</span><span class="sxs-lookup"><span data-stu-id="e0d39-167">Tests for equality between `CMediaType` objects.</span></span>                               |
| [<span data-ttu-id="e0d39-168">**operador! =**</span><span class="sxs-lookup"><span data-stu-id="e0d39-168">**operator !=**</span></span>](cmediatype-operator-neq.md)                      | <span data-ttu-id="e0d39-169">Testa a desigualdade entre objetos `CMediaType`.</span><span class="sxs-lookup"><span data-stu-id="e0d39-169">Tests for inequality between `CMediaType` objects.</span></span>                             |



 

## <a name="requirements"></a><span data-ttu-id="e0d39-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0d39-170">Requirements</span></span>



| <span data-ttu-id="e0d39-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0d39-171">Requirement</span></span> | <span data-ttu-id="e0d39-172">Valor</span><span class="sxs-lookup"><span data-stu-id="e0d39-172">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0d39-173">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e0d39-173">Header</span></span><br/>  | <dl> <span data-ttu-id="e0d39-174"><dt>Mtype. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0d39-174"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="e0d39-175">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0d39-175">Library</span></span><br/> | <dl> <span data-ttu-id="e0d39-176"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e0d39-176"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




