---
description: Passa uma mensagem de alteração de tamanho de vídeo do EC \_ \_ \_ para o Gerenciador do grafo de filtro.
ms.assetid: 39cb4f30-c12d-49bd-8d8a-70bf686b680d
title: Método CBaseControlVideo. OnVideoSizeChange (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.OnVideoSizeChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37caa05d164c23484c749730796d6a5f10d67d57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780892"
---
# <a name="cbasecontrolvideoonvideosizechange-method"></a><span data-ttu-id="12960-103">Método CBaseControlVideo. OnVideoSizeChange</span><span class="sxs-lookup"><span data-stu-id="12960-103">CBaseControlVideo.OnVideoSizeChange method</span></span>

<span data-ttu-id="12960-104">Passa uma mensagem de alteração de tamanho de vídeo do EC \_ \_ \_ para o Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="12960-104">Passes an EC\_VIDEO\_SIZE\_CHANGED message to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="12960-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12960-105">Syntax</span></span>


```C++
virtual HRESULT OnVideoSizeChange();
```



## <a name="parameters"></a><span data-ttu-id="12960-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12960-106">Parameters</span></span>

<span data-ttu-id="12960-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="12960-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="12960-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12960-108">Return value</span></span>

<span data-ttu-id="12960-109">Retorna um valor **HRESULT** que depende da implementação; pode ser um dos valores a seguir ou outros valores não listados.</span><span class="sxs-lookup"><span data-stu-id="12960-109">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="12960-110">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="12960-110">Return code</span></span>                                                                                   | <span data-ttu-id="12960-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="12960-111">Description</span></span>               |
|-----------------------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="12960-112"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="12960-112"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="12960-113">Falha.</span><span class="sxs-lookup"><span data-stu-id="12960-113">Failure.</span></span><br/>       |
| <dl> <span data-ttu-id="12960-114"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="12960-114"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="12960-115">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="12960-115">Out of memory.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="12960-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="12960-116">Remarks</span></span>

<span data-ttu-id="12960-117">Um processador de vídeo deve chamar essa função de membro toda vez que o tamanho do vídeo for alterado; Isso normalmente será chamado uma vez após a conexão inicial.</span><span class="sxs-lookup"><span data-stu-id="12960-117">A video renderer should call this member function each time the video size is changed; this will typically be called once after initial connection.</span></span> <span data-ttu-id="12960-118">Se o renderizador puder dar suporte a alterações de formato dinâmico (de 320 x 240 a 160 x 120), ele também deverá chamá-la após cada alteração.</span><span class="sxs-lookup"><span data-stu-id="12960-118">If the renderer can support dynamic format changes (from 320 x 240 to 160 x 120), it should also call it after each change.</span></span>

## <a name="requirements"></a><span data-ttu-id="12960-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12960-119">Requirements</span></span>



| <span data-ttu-id="12960-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="12960-120">Requirement</span></span> | <span data-ttu-id="12960-121">Valor</span><span class="sxs-lookup"><span data-stu-id="12960-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12960-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12960-122">Header</span></span><br/>  | <dl> <span data-ttu-id="12960-123"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="12960-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="12960-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="12960-124">Library</span></span><br/> | <dl> <span data-ttu-id="12960-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="12960-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12960-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="12960-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12960-127">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="12960-127">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




