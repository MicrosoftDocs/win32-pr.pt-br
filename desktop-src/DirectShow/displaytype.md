---
description: A função DisplayType envia informações sobre um tipo de mídia para o local de saída de depuração. Ignorado em compilações de varejo.
ms.assetid: 63a88508-dff8-4869-97e5-0f75f4a9dca0
title: Função TipoDeExibição (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DisplayType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3d83bbe7a24463fc4cfaed4ace3adec9d6fcf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775563"
---
# <a name="displaytype-function"></a><span data-ttu-id="76569-104">Função DisplayType</span><span class="sxs-lookup"><span data-stu-id="76569-104">DisplayType function</span></span>

<span data-ttu-id="76569-105">A `DisplayType` função envia informações sobre um tipo de mídia para o local de saída de depuração.</span><span class="sxs-lookup"><span data-stu-id="76569-105">The `DisplayType` function sends information about a media type to the debug output location.</span></span> <span data-ttu-id="76569-106">Ignorado em compilações de varejo.</span><span class="sxs-lookup"><span data-stu-id="76569-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="76569-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76569-107">Syntax</span></span>


```C++
void DisplayType(
         LPTSTR        label,
   const AM_MEDIA_TYPE *pmtIn
);
```



## <a name="parameters"></a><span data-ttu-id="76569-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76569-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76569-109">*label*</span><span class="sxs-lookup"><span data-stu-id="76569-109">*label*</span></span> 
</dt> <dd>

<span data-ttu-id="76569-110">Cadeia de caracteres que contém uma mensagem a ser exibida com as informações do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="76569-110">String that contains a message to display with the media type information.</span></span>

</dd> <dt>

<span data-ttu-id="76569-111">*pmtIn*</span><span class="sxs-lookup"><span data-stu-id="76569-111">*pmtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="76569-112">ointer para a estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que contém o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="76569-112">ointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that contains the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76569-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="76569-113">Return value</span></span>

<span data-ttu-id="76569-114">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="76569-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="76569-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="76569-115">Remarks</span></span>

<span data-ttu-id="76569-116">Essa função gera várias mensagens de rastreamento de LOG \_ .</span><span class="sxs-lookup"><span data-stu-id="76569-116">This function generates several LOG\_TRACE messages.</span></span> <span data-ttu-id="76569-117">No nível de log 2 ou superior, a função exibe o tipo principal, subtipo e tipo de formato e dados do bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="76569-117">At logging level 2 or higher, the function displays the major type, subtype, and format type, and data from the format block.</span></span> <span data-ttu-id="76569-118">No nível de log 5 ou superior, a função exibe informações adicionais, como os retângulos de origem e de destino para tipos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="76569-118">At logging level 5 or higher, the function displays additional information, such as the source and target rectangles for video types.</span></span>

## <a name="requirements"></a><span data-ttu-id="76569-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76569-119">Requirements</span></span>



| <span data-ttu-id="76569-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="76569-120">Requirement</span></span> | <span data-ttu-id="76569-121">Valor</span><span class="sxs-lookup"><span data-stu-id="76569-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76569-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="76569-122">Header</span></span><br/>  | <dl> <span data-ttu-id="76569-123"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="76569-123"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="76569-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="76569-124">Library</span></span><br/> | <dl> <span data-ttu-id="76569-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="76569-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76569-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="76569-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76569-127">Funções de saída de depuração</span><span class="sxs-lookup"><span data-stu-id="76569-127">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




