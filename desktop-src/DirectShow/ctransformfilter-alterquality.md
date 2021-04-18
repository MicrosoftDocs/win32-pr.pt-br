---
description: O método AlterQuality notifica o filtro de que uma alteração de qualidade é solicitada.
ms.assetid: 46743d6b-65cf-4d63-8913-114277d76da4
title: Método CTransformFilter. AlterQuality (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.AlterQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 592fc67dd5cee5e4f76b8171b6e842532d71371b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752691"
---
# <a name="ctransformfilteralterquality-method"></a><span data-ttu-id="e2f0d-103">Método CTransformFilter. AlterQuality</span><span class="sxs-lookup"><span data-stu-id="e2f0d-103">CTransformFilter.AlterQuality method</span></span>

<span data-ttu-id="e2f0d-104">O `AlterQuality` método notifica o filtro de que uma alteração de qualidade é solicitada.</span><span class="sxs-lookup"><span data-stu-id="e2f0d-104">The `AlterQuality` method notifies the filter that a quality change is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2f0d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2f0d-105">Syntax</span></span>


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a><span data-ttu-id="e2f0d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2f0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2f0d-107">*perguntas*</span><span class="sxs-lookup"><span data-stu-id="e2f0d-107">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="e2f0d-108">Estrutura de [**qualidade**](/windows/win32/api/strmif/ns-strmif-quality) que contém a mensagem de controle de qualidade.</span><span class="sxs-lookup"><span data-stu-id="e2f0d-108">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2f0d-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e2f0d-109">Return value</span></span>

<span data-ttu-id="e2f0d-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e2f0d-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e2f0d-111">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e2f0d-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="e2f0d-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e2f0d-112">Return code</span></span>                                                                             | <span data-ttu-id="e2f0d-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="e2f0d-113">Description</span></span>                                                                           |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e2f0d-114"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="e2f0d-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="e2f0d-115">Não foi tratada a mensagem de qualidade.</span><span class="sxs-lookup"><span data-stu-id="e2f0d-115">Did not handle the quality message.</span></span> <span data-ttu-id="e2f0d-116">A mensagem deve ser passada para upstream.</span><span class="sxs-lookup"><span data-stu-id="e2f0d-116">The message should be passed upstream.</span></span><br/> |
| <dl> <span data-ttu-id="e2f0d-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e2f0d-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="e2f0d-118">Manipulado a mensagem de qualidade.</span><span class="sxs-lookup"><span data-stu-id="e2f0d-118">Handled the quality message.</span></span> <span data-ttu-id="e2f0d-119">Nenhuma ação posterior é necessária.</span><span class="sxs-lookup"><span data-stu-id="e2f0d-119">No further action is necessary.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="e2f0d-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2f0d-120">Remarks</span></span>

<span data-ttu-id="e2f0d-121">Substitua esse método se o filtro puder executar o controle de qualidade.</span><span class="sxs-lookup"><span data-stu-id="e2f0d-121">Override this method if the filter can perform quality control.</span></span> <span data-ttu-id="e2f0d-122">Para obter mais informações, consulte [Gerenciamento de controle de qualidade](quality-control-management.md).</span><span class="sxs-lookup"><span data-stu-id="e2f0d-122">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2f0d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2f0d-123">Requirements</span></span>



| <span data-ttu-id="e2f0d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2f0d-124">Requirement</span></span> | <span data-ttu-id="e2f0d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e2f0d-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2f0d-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e2f0d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e2f0d-127"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2f0d-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e2f0d-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e2f0d-128">Library</span></span><br/> | <dl> <span data-ttu-id="e2f0d-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e2f0d-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2f0d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2f0d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2f0d-131">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="e2f0d-131">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




