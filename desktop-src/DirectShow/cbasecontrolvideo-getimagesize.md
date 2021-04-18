---
description: O método getimageize recupera informações de tamanho de imagem de vídeo.
ms.assetid: a6d7f949-c6a9-49e9-b10a-f6f5bd73dc00
title: Método CBaseControlVideo. getimageize (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed7795e3998bc101e907bce87c9981e86f51fcb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782853"
---
# <a name="cbasecontrolvideogetimagesize-method"></a><span data-ttu-id="0f7bb-103">Método CBaseControlVideo. getimageize</span><span class="sxs-lookup"><span data-stu-id="0f7bb-103">CBaseControlVideo.GetImageSize method</span></span>

<span data-ttu-id="0f7bb-104">O `GetImageSize` método recupera informações de tamanho da imagem de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0f7bb-104">The `GetImageSize` method retrieves video image size information.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f7bb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f7bb-105">Syntax</span></span>


```C++
HRESULT GetImageSize(
   VIDEOINFOHEADER *pVideoInfo,
   long            *pBufferSize,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="0f7bb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f7bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f7bb-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="0f7bb-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="0f7bb-108">Ponteiro para uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) a ser preenchida.</span><span class="sxs-lookup"><span data-stu-id="0f7bb-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure to be filled in.</span></span>

</dd> <dt>

<span data-ttu-id="0f7bb-109">*pBufferSize*</span><span class="sxs-lookup"><span data-stu-id="0f7bb-109">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="0f7bb-110">Ponteiro para o tamanho do buffer de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0f7bb-110">Pointer to the size of the video buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0f7bb-111">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="0f7bb-111">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="0f7bb-112">Ponteiro para as dimensões de retângulo do vídeo de origem.</span><span class="sxs-lookup"><span data-stu-id="0f7bb-112">Pointer to the rectangle dimensions of the source video.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f7bb-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0f7bb-113">Return value</span></span>

<span data-ttu-id="0f7bb-114">Retorna um valor **HRESULT** que depende da implementação; pode ser um dos valores a seguir ou outros valores não listados.</span><span class="sxs-lookup"><span data-stu-id="0f7bb-114">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="0f7bb-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0f7bb-115">Return code</span></span>                                                                                  | <span data-ttu-id="0f7bb-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f7bb-116">Description</span></span>                                                               |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0f7bb-117"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="0f7bb-117"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="0f7bb-118">Falha.</span><span class="sxs-lookup"><span data-stu-id="0f7bb-118">Failure.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="0f7bb-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0f7bb-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="0f7bb-120">Argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="0f7bb-120">Invalid argument.</span></span> <span data-ttu-id="0f7bb-121">O formato de dados não é compatível.</span><span class="sxs-lookup"><span data-stu-id="0f7bb-121">The data format is not compatible.</span></span><br/>           |
| <dl> <span data-ttu-id="0f7bb-122"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="0f7bb-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="0f7bb-123">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="0f7bb-123">Unexpected error occurred.</span></span> <span data-ttu-id="0f7bb-124">Um ou mais argumentos são **nulos**.</span><span class="sxs-lookup"><span data-stu-id="0f7bb-124">One or more arguments are **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="0f7bb-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="0f7bb-125"><dt>**NOERROR**</dt></span></span> </dl>       | <span data-ttu-id="0f7bb-126">Êxito.</span><span class="sxs-lookup"><span data-stu-id="0f7bb-126">Success.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="0f7bb-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f7bb-127">Remarks</span></span>

<span data-ttu-id="0f7bb-128">Essa função de membro é uma função auxiliar usada para criar processamentos de imagem de memória de imagens DIB.</span><span class="sxs-lookup"><span data-stu-id="0f7bb-128">This member function is a helper function used for creating memory image renderings of DIB images.</span></span> <span data-ttu-id="0f7bb-129">Ele é chamado da implementação da classe base de [**CBaseControlVideo:: GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) quando um parâmetro _pVideoImage_ **nulo** é passado para essa função de membro.</span><span class="sxs-lookup"><span data-stu-id="0f7bb-129">It is called from the base class implementation of [**CBaseControlVideo::GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) when a **NULL**_pVideoImage_ parameter is passed to that member function.</span></span> <span data-ttu-id="0f7bb-130">Como resultado, essa função de membro constrói e retorna uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , usando as informações em *pBufferSize* e *pSourceRect*.</span><span class="sxs-lookup"><span data-stu-id="0f7bb-130">As a result, this member function constructs and returns a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure, using the information in *pBufferSize* and *pSourceRect*.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f7bb-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f7bb-131">Requirements</span></span>



| <span data-ttu-id="0f7bb-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f7bb-132">Requirement</span></span> | <span data-ttu-id="0f7bb-133">Valor</span><span class="sxs-lookup"><span data-stu-id="0f7bb-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f7bb-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0f7bb-134">Header</span></span><br/>  | <dl> <span data-ttu-id="0f7bb-135"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f7bb-135"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0f7bb-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0f7bb-136">Library</span></span><br/> | <dl> <span data-ttu-id="0f7bb-137"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0f7bb-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f7bb-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f7bb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f7bb-139">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="0f7bb-139">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




