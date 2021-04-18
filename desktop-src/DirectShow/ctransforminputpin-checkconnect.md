---
description: O método CheckConnect determina se uma conexão de PIN é adequada.
ms.assetid: b8ace40d-31f5-49b0-a4cd-6ece0f883d96
title: Método CTransformInputPin. CheckConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e10c174a4e295576cfa9ce902faeac889f5a6a9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751675"
---
# <a name="ctransforminputpincheckconnect-method"></a><span data-ttu-id="dbccb-103">Método CTransformInputPin. CheckConnect</span><span class="sxs-lookup"><span data-stu-id="dbccb-103">CTransformInputPin.CheckConnect method</span></span>

<span data-ttu-id="dbccb-104">O `CheckConnect` método determina se uma conexão de PIN é adequada.</span><span class="sxs-lookup"><span data-stu-id="dbccb-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbccb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dbccb-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="dbccb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dbccb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbccb-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="dbccb-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="dbccb-108">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de saída.</span><span class="sxs-lookup"><span data-stu-id="dbccb-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbccb-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dbccb-109">Return value</span></span>

<span data-ttu-id="dbccb-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dbccb-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="dbccb-111">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="dbccb-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="dbccb-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="dbccb-112">Return code</span></span>                                                                                               | <span data-ttu-id="dbccb-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="dbccb-113">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="dbccb-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dbccb-114"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="dbccb-115">Sucesso</span><span class="sxs-lookup"><span data-stu-id="dbccb-115">Success</span></span><br/>             |
| <dl> <span data-ttu-id="dbccb-116"><dt>**VFW \_ E \_ direção inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dbccb-116"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="dbccb-117">Direção do PIN incorreta</span><span class="sxs-lookup"><span data-stu-id="dbccb-117">Wrong pin direction</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dbccb-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="dbccb-118">Remarks</span></span>

<span data-ttu-id="dbccb-119">Esse método substitui o método [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="dbccb-119">This method overrides the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method.</span></span> <span data-ttu-id="dbccb-120">Ele chama o método [**CTransformFilter:: CheckConnect**](ctransformfilter-checkconnect.md) do filtro, que retorna s \_ OK na classe base.</span><span class="sxs-lookup"><span data-stu-id="dbccb-120">It calls the filter's [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="dbccb-121">A classe derivada pode substituir o método **CTransformFilter:: CheckConnect** para executar verificações adicionais.</span><span class="sxs-lookup"><span data-stu-id="dbccb-121">The derived class can override the **CTransformFilter::CheckConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbccb-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbccb-122">Requirements</span></span>



| <span data-ttu-id="dbccb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbccb-123">Requirement</span></span> | <span data-ttu-id="dbccb-124">Valor</span><span class="sxs-lookup"><span data-stu-id="dbccb-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbccb-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dbccb-125">Header</span></span><br/>  | <dl> <span data-ttu-id="dbccb-126"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dbccb-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dbccb-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dbccb-127">Library</span></span><br/> | <dl> <span data-ttu-id="dbccb-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="dbccb-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




