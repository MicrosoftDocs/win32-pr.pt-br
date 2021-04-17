---
description: O método BreakConnect libera o pino de entrada de uma conexão.
ms.assetid: e295cec1-8c8f-471c-8832-075ac7708cb1
title: Método CBaseRenderer. BreakConnect (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98c1e01c15740616541706ca4d9da3ab5e66538c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787417"
---
# <a name="cbaserendererbreakconnect-method"></a><span data-ttu-id="5ad18-103">Método CBaseRenderer. BreakConnect</span><span class="sxs-lookup"><span data-stu-id="5ad18-103">CBaseRenderer.BreakConnect method</span></span>

<span data-ttu-id="5ad18-104">O `BreakConnect` método libera o pino de entrada de uma conexão.</span><span class="sxs-lookup"><span data-stu-id="5ad18-104">The `BreakConnect` method releases the input pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ad18-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ad18-105">Syntax</span></span>


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="5ad18-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ad18-106">Parameters</span></span>

<span data-ttu-id="5ad18-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5ad18-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5ad18-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5ad18-108">Return value</span></span>

<span data-ttu-id="5ad18-109">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5ad18-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="5ad18-110">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5ad18-110">Return code</span></span>                                                                                         | <span data-ttu-id="5ad18-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ad18-111">Description</span></span>                            |
|-----------------------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="5ad18-112"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="5ad18-112"><dt>**S\_FALSE**</dt></span></span> </dl>             | <span data-ttu-id="5ad18-113">O PIN não foi conectado.</span><span class="sxs-lookup"><span data-stu-id="5ad18-113">The pin was not connected.</span></span><br/>  |
| <dl> <span data-ttu-id="5ad18-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5ad18-114"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="5ad18-115">Êxito.</span><span class="sxs-lookup"><span data-stu-id="5ad18-115">Success.</span></span><br/>                    |
| <dl> <span data-ttu-id="5ad18-116"><dt>**VFW \_ E \_ não \_ parado**</dt></span><span class="sxs-lookup"><span data-stu-id="5ad18-116"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="5ad18-117">O filtro ainda está ativo.</span><span class="sxs-lookup"><span data-stu-id="5ad18-117">The filter is still active.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5ad18-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ad18-118">Remarks</span></span>

<span data-ttu-id="5ad18-119">O pino de entrada do filtro chama esse método de dentro de seu próprio `BreakConnect` método.</span><span class="sxs-lookup"><span data-stu-id="5ad18-119">The filter's input pin calls this method from inside its own `BreakConnect` method.</span></span> <span data-ttu-id="5ad18-120">(Para obter mais informações, consulte [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md).) O filtro executa alguma escrituração interna, como redefinir o sinalizador de fim de fluxo.</span><span class="sxs-lookup"><span data-stu-id="5ad18-120">(For more information, see [**CBasePin::BreakConnect**](cbasepin-breakconnect.md).) The filter performs some internal bookkeeping, such as resetting the end-of-stream flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ad18-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ad18-121">Requirements</span></span>



| <span data-ttu-id="5ad18-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ad18-122">Requirement</span></span> | <span data-ttu-id="5ad18-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5ad18-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ad18-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ad18-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5ad18-125"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ad18-125"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5ad18-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5ad18-126">Library</span></span><br/> | <dl> <span data-ttu-id="5ad18-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5ad18-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ad18-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ad18-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ad18-129">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="5ad18-129">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




