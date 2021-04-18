---
description: O método SetMediaType especifica o tipo de mídia para a conexão no pino de entrada do exemplo de apoio.
ms.assetid: 9568832f-6666-45c9-9421-485c877affb3
title: 'Método ISampleGrabber:: SetMediaType (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a39aa79e9311fe3491d0925fdc1b2dd3b1cc65c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757672"
---
# <a name="isamplegrabbersetmediatype-method"></a><span data-ttu-id="f3ab1-103">Método ISampleGrabber:: SetMediaType</span><span class="sxs-lookup"><span data-stu-id="f3ab1-103">ISampleGrabber::SetMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="f3ab1-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="f3ab1-104">\[Deprecated.</span></span> <span data-ttu-id="f3ab1-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f3ab1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f3ab1-106">O `SetMediaType` método especifica o tipo de mídia para a conexão no pino de entrada do exemplo de apoio.</span><span class="sxs-lookup"><span data-stu-id="f3ab1-106">The `SetMediaType` method specifies the media type for the connection on the input pin of the Sample Grabber.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3ab1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f3ab1-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a><span data-ttu-id="f3ab1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3ab1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3ab1-109">*pType*</span><span class="sxs-lookup"><span data-stu-id="f3ab1-109">*pType*</span></span> 
</dt> <dd>

<span data-ttu-id="f3ab1-110">Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) especifica o tipo de mídia necessário.</span><span class="sxs-lookup"><span data-stu-id="f3ab1-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure specifies the required media type.</span></span> <span data-ttu-id="f3ab1-111">Não é necessário definir todos os membros da estrutura; consulte comentários para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="f3ab1-111">It is not necessary to set all the structure members; see Remarks for details.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3ab1-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f3ab1-112">Return value</span></span>

<span data-ttu-id="f3ab1-113">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f3ab1-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3ab1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3ab1-114">Remarks</span></span>

<span data-ttu-id="f3ab1-115">Por padrão, o exemplo de apoio não tem nenhum tipo de mídia preferencial.</span><span class="sxs-lookup"><span data-stu-id="f3ab1-115">By default, the Sample Grabber has no preferred media type.</span></span> <span data-ttu-id="f3ab1-116">Para garantir que o exemplo de apoio se conecte ao filtro correto, chame esse método antes de criar o grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="f3ab1-116">To ensure that the Sample Grabber connects to the correct filter, call this method before building the filter graph.</span></span>

<span data-ttu-id="f3ab1-117">Esse método restringe o intervalo de tipos de mídia que o filtro aceitará.</span><span class="sxs-lookup"><span data-stu-id="f3ab1-117">This method restricts the range of media types that the filter will accept.</span></span> <span data-ttu-id="f3ab1-118">Quando o filtro se conecta, ele tenta corresponder ao tipo de mídia fornecido em *pType*.</span><span class="sxs-lookup"><span data-stu-id="f3ab1-118">When the filter connects, it tries to match the media type given in *pType*.</span></span> <span data-ttu-id="f3ab1-119">Para fazer isso, ele compara o tipo principal, subtipo e os GUIDs de tipo de formato, nessa ordem.</span><span class="sxs-lookup"><span data-stu-id="f3ab1-119">To do so, it compares the major type, subtype, and format type GUIDs, in that order.</span></span> <span data-ttu-id="f3ab1-120">Para cada um desses GUIDs, se *pType* tiver o valor GUID \_ NULL, o exemplo de apoio aceitará o tipo de mídia sem nenhuma verificação adicional.</span><span class="sxs-lookup"><span data-stu-id="f3ab1-120">For each of these GUIDs, if *pType* has the value GUID\_NULL, the Sample Grabber accepts the media type without any further checks.</span></span> <span data-ttu-id="f3ab1-121">Se *pType* tiver qualquer outro valor, o exemplo de apoio o comparará ao GUID no tipo de conexão.</span><span class="sxs-lookup"><span data-stu-id="f3ab1-121">If *pType* has any other value, the Sample Grabber compares it to the GUID in the connection type.</span></span> <span data-ttu-id="f3ab1-122">A menos que os dois GUIDs correspondam exatamente, o exemplo de apoio rejeita a conexão.</span><span class="sxs-lookup"><span data-stu-id="f3ab1-122">Unless the two GUIDs match exactly, the Sample Grabber rejects the connection.</span></span>

<span data-ttu-id="f3ab1-123">Para tipos de mídia de vídeo, o exemplo de apoio ignora o bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="f3ab1-123">For video media types, the Sample Grabber ignores the format block.</span></span> <span data-ttu-id="f3ab1-124">Portanto, ele aceitará qualquer tamanho de vídeo e taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="f3ab1-124">Therefore, it will accept any video size and frame rate.</span></span> <span data-ttu-id="f3ab1-125">Ao chamar `SetMediaType` , defina o bloco de formato (**pbFormat**) como **nulo** e o tamanho (**cbFormat**) como zero.</span><span class="sxs-lookup"><span data-stu-id="f3ab1-125">When you call `SetMediaType`, set the format block (**pbFormat**) to **NULL** and the size (**cbFormat**) to zero.</span></span> <span data-ttu-id="f3ab1-126">Para tipos de mídia de áudio, o exemplo de apoio examinará a estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) e exigirá que o outro filtro se conecte com esse formato — a menos que o bloco de formato em *pType* seja **nulo** ou a marca de formato seja o \_ formato Wave \_ PCM e os outros membros da estrutura sejam zero.</span><span class="sxs-lookup"><span data-stu-id="f3ab1-126">For audio media types, the Sample Grabber will examine the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure and will require the other filter to connect with that format — unless the format block in *pType* is **NULL**, or the format tag is WAVE\_FORMAT\_PCM and the other structure members are zero.</span></span>

<span data-ttu-id="f3ab1-127">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="f3ab1-127">Example 1:</span></span>

-   <span data-ttu-id="f3ab1-128">Tipo principal: vídeo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="f3ab1-128">Major type: MEDIATYPE\_Video</span></span>
-   <span data-ttu-id="f3ab1-129">Subtipo: GUID \_ NULL</span><span class="sxs-lookup"><span data-stu-id="f3ab1-129">Subtype: GUID\_NULL</span></span>
-   <span data-ttu-id="f3ab1-130">Tipo de formato: GUID \_ NULL</span><span class="sxs-lookup"><span data-stu-id="f3ab1-130">Format type: GUID\_NULL</span></span>

<span data-ttu-id="f3ab1-131">O exemplo de apoio aceitará qualquer tipo de vídeo em que o tipo principal é igual ao vídeo de MEDIATYPE \_ .</span><span class="sxs-lookup"><span data-stu-id="f3ab1-131">The Sample Grabber will accept any video type where the major type equals MEDIATYPE\_Video.</span></span> <span data-ttu-id="f3ab1-132">Ele não verificará o subtipo.</span><span class="sxs-lookup"><span data-stu-id="f3ab1-132">It will not check the subtype.</span></span>

<span data-ttu-id="f3ab1-133">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="f3ab1-133">Example 2:</span></span>

-   <span data-ttu-id="f3ab1-134">Tipo principal: vídeo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="f3ab1-134">Major type: MEDIATYPE\_Video</span></span>
-   <span data-ttu-id="f3ab1-135">Subtipo: MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="f3ab1-135">Subtype: MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="f3ab1-136">Tipo de formato: GUID \_ NULL</span><span class="sxs-lookup"><span data-stu-id="f3ab1-136">Format type: GUID\_NULL</span></span>

<span data-ttu-id="f3ab1-137">Agora, o exemplo de apoio verificará o subtipo e aceitará apenas vídeo RGB 24.</span><span class="sxs-lookup"><span data-stu-id="f3ab1-137">Now the Sample Grabber will check the subtype, and accept only RGB 24 video.</span></span>

<span data-ttu-id="f3ab1-138">**Limitações:** Independentemente do tipo que você definir, o filtro de apoio de exemplo rejeita todos os tipos de vídeo com orientação superior ( *monoheight*) ou com um tipo de formato de formato \_ VideoInfo2.</span><span class="sxs-lookup"><span data-stu-id="f3ab1-138">**Limitations:** Regardless of what type you set, the Sample Grabber Filter rejects any video types with top-down orientation (negative *biHeight*), or with a format type of FORMAT\_VideoInfo2.</span></span> <span data-ttu-id="f3ab1-139">Nesse caso, embora o `SetMediaType` método tenha sucesso, o filtro não se conectará.</span><span class="sxs-lookup"><span data-stu-id="f3ab1-139">In this case, although the `SetMediaType` method succeeds, the filter will not connect.</span></span>

> [!Note]  
> <span data-ttu-id="f3ab1-140">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="f3ab1-140">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f3ab1-141">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f3ab1-141">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f3ab1-142">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f3ab1-142">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f3ab1-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3ab1-143">Requirements</span></span>



| <span data-ttu-id="f3ab1-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3ab1-144">Requirement</span></span> | <span data-ttu-id="f3ab1-145">Valor</span><span class="sxs-lookup"><span data-stu-id="f3ab1-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3ab1-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f3ab1-146">Header</span></span><br/>  | <dl> <span data-ttu-id="f3ab1-147"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3ab1-147"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f3ab1-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f3ab1-148">Library</span></span><br/> | <dl> <span data-ttu-id="f3ab1-149"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3ab1-149"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3ab1-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3ab1-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3ab1-151">Usando o exemplo de apoio</span><span class="sxs-lookup"><span data-stu-id="f3ab1-151">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="f3ab1-152">**Interface ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="f3ab1-152">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 
