---
description: O método Init Inicializa o objeto.
ms.assetid: a919adfa-0ffb-4241-b709-ad0e8d55476a
title: Método t CSeekingPassThru.Ini(Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.Init
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 78176a6966f379240b5b7edd1ef5b73d7fa75b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751888"
---
# <a name="cseekingpassthruinit-method"></a><span data-ttu-id="0b22c-103">Método t CSeekingPassThru.Ini</span><span class="sxs-lookup"><span data-stu-id="0b22c-103">CSeekingPassThru.Init method</span></span>

<span data-ttu-id="0b22c-104">O `Init` método inicializa o objeto.</span><span class="sxs-lookup"><span data-stu-id="0b22c-104">The `Init` method initializes the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b22c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b22c-105">Syntax</span></span>


```C++
HRESULT Init(
  [in] BOOL bSupportRendering,
       IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="0b22c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b22c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b22c-107">*bSupportRendering* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0b22c-107">*bSupportRendering* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b22c-108">Valor booliano que especifica se o filtro é um renderizador.</span><span class="sxs-lookup"><span data-stu-id="0b22c-108">Boolean value that specifies whether the filter is a renderer.</span></span> <span data-ttu-id="0b22c-109">Use o valor **true** se o filtro for um renderizador ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="0b22c-109">Use the value **TRUE** if the filter is a renderer, or **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="0b22c-110">*pPin*</span><span class="sxs-lookup"><span data-stu-id="0b22c-110">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="0b22c-111">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) no pino de entrada do filtro.</span><span class="sxs-lookup"><span data-stu-id="0b22c-111">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface on the filter's input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b22c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0b22c-112">Return value</span></span>

<span data-ttu-id="0b22c-113">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0b22c-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="0b22c-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0b22c-114">Return code</span></span>                                                                                   | <span data-ttu-id="0b22c-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b22c-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="0b22c-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0b22c-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0b22c-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="0b22c-117">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="0b22c-118"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="0b22c-118"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="0b22c-119">O objeto já foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="0b22c-119">Object was already initialized.</span></span><br/>         |
| <dl> <span data-ttu-id="0b22c-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0b22c-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0b22c-121">Não há memória suficiente para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="0b22c-121">Not enough memory to create the object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0b22c-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b22c-122">Remarks</span></span>

<span data-ttu-id="0b22c-123">Se o valor de *bSupportRendering* for **true**, esse método criará uma instância da classe [**CRendererPosPassThru**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="0b22c-123">If the value of *bSupportRendering* is **TRUE**, this method creates an instance of the [**CRendererPosPassThru**](crendererpospassthru.md) class.</span></span> <span data-ttu-id="0b22c-124">Caso contrário, ele cria uma instância da classe [**CPosPassThru**](cpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="0b22c-124">Otherwise, it creates an instance of the [**CPosPassThru**](cpospassthru.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b22c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b22c-125">Requirements</span></span>



| <span data-ttu-id="0b22c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b22c-126">Requirement</span></span> | <span data-ttu-id="0b22c-127">Valor</span><span class="sxs-lookup"><span data-stu-id="0b22c-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b22c-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0b22c-128">Header</span></span><br/>  | <dl> <span data-ttu-id="0b22c-129"><dt>Seekpt. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b22c-129"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0b22c-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0b22c-130">Library</span></span><br/> | <dl> <span data-ttu-id="0b22c-131"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0b22c-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b22c-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b22c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b22c-133">**Classe CSeekingPassThru**</span><span class="sxs-lookup"><span data-stu-id="0b22c-133">**CSeekingPassThru Class**</span></span>](cseekingpassthru.md)
</dt> </dl>

 

 




