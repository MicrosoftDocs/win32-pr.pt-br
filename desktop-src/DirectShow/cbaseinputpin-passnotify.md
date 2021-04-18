---
description: O método PassNotify Passa uma mensagem de controle de qualidade para o objeto apropriado.
ms.assetid: dbc9a4b7-a522-4fbf-8e3a-af50e11c1d80
title: Método CBaseInputPin. PassNotify (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.PassNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36316815ae1d9fde1a18fb36029da92ae6263f20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771871"
---
# <a name="cbaseinputpinpassnotify-method"></a><span data-ttu-id="bf88d-103">Método CBaseInputPin. PassNotify</span><span class="sxs-lookup"><span data-stu-id="bf88d-103">CBaseInputPin.PassNotify method</span></span>

<span data-ttu-id="bf88d-104">O `PassNotify` método passa uma mensagem de controle de qualidade para o objeto apropriado.</span><span class="sxs-lookup"><span data-stu-id="bf88d-104">The `PassNotify` method passes a quality-control message to the appropriate object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf88d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf88d-105">Syntax</span></span>


```C++
HRESULT PassNotify(
   Quality q
);
```



## <a name="parameters"></a><span data-ttu-id="bf88d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf88d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf88d-107">*perguntas*</span><span class="sxs-lookup"><span data-stu-id="bf88d-107">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="bf88d-108">Estrutura de [**qualidade**](/windows/win32/api/strmif/ns-strmif-quality) que contém a mensagem de controle de qualidade.</span><span class="sxs-lookup"><span data-stu-id="bf88d-108">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf88d-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bf88d-109">Return value</span></span>

<span data-ttu-id="bf88d-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bf88d-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="bf88d-111">Os valores possíveis incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="bf88d-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="bf88d-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="bf88d-112">Return code</span></span>                                                                                       | <span data-ttu-id="bf88d-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf88d-113">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="bf88d-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bf88d-114"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="bf88d-115">Êxito.</span><span class="sxs-lookup"><span data-stu-id="bf88d-115">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="bf88d-116"><dt>**VFW \_ E \_ não \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="bf88d-116"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="bf88d-117">Não foi possível encontrar um objeto para aceitar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="bf88d-117">Could not find an object to accept the message.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bf88d-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf88d-118">Remarks</span></span>

<span data-ttu-id="bf88d-119">Chame esse método se o filtro não manipular mensagens de controle de qualidade.</span><span class="sxs-lookup"><span data-stu-id="bf88d-119">Call this method if the filter does not handle quality-control messages.</span></span> <span data-ttu-id="bf88d-120">Esse método passa a mensagem para um dos seguintes objetos, em ordem de preferência:</span><span class="sxs-lookup"><span data-stu-id="bf88d-120">This method passes the message to one of the following objects, in order of preference:</span></span>

-   <span data-ttu-id="bf88d-121">Um Gerenciador de controle de qualidade externo, se o método [**IQualityControl:: SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) foi chamado.</span><span class="sxs-lookup"><span data-stu-id="bf88d-121">An external quality-control manager, if the [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) method was called.</span></span>
-   <span data-ttu-id="bf88d-122">O pino de saída upstream.</span><span class="sxs-lookup"><span data-stu-id="bf88d-122">The upstream output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf88d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf88d-123">Requirements</span></span>



| <span data-ttu-id="bf88d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf88d-124">Requirement</span></span> | <span data-ttu-id="bf88d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="bf88d-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf88d-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf88d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="bf88d-127"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf88d-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bf88d-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf88d-128">Library</span></span><br/> | <dl> <span data-ttu-id="bf88d-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="bf88d-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf88d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf88d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf88d-131">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="bf88d-131">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> <dt>

[<span data-ttu-id="bf88d-132">Gerenciamento de controle de qualidade</span><span class="sxs-lookup"><span data-stu-id="bf88d-132">Quality-Control Management</span></span>](quality-control-management.md)
</dt> </dl>

 

 




