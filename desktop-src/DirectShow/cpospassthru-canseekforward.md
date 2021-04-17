---
description: 'O método CanSeekForward determina se o fluxo pode ser buscado em frente. Esse método implementa o método IMediaPosition:: CanSeekForward.'
ms.assetid: ccb2db8d-b52e-4e3d-b49b-9689197a974a
title: Método CPosPassThru. CanSeekForward (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekForward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 701bfdff1d3a3a37dc0e3935aa82bfca2e01cfcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768654"
---
# <a name="cpospassthrucanseekforward-method"></a><span data-ttu-id="a4caf-104">Método CPosPassThru. CanSeekForward</span><span class="sxs-lookup"><span data-stu-id="a4caf-104">CPosPassThru.CanSeekForward method</span></span>

<span data-ttu-id="a4caf-105">O `CanSeekForward` método determina se o fluxo pode ser buscado em frente.</span><span class="sxs-lookup"><span data-stu-id="a4caf-105">The `CanSeekForward` method determines whether the stream can be seeked forward.</span></span> <span data-ttu-id="a4caf-106">Esse método implementa o método [**IMediaPosition:: CanSeekForward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekforward) .</span><span class="sxs-lookup"><span data-stu-id="a4caf-106">This method implements the [**IMediaPosition::CanSeekForward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekforward) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4caf-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4caf-107">Syntax</span></span>


```C++
HRESULT CanSeekForward(
   LONG *pCanSeekForward
);
```



## <a name="parameters"></a><span data-ttu-id="a4caf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4caf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4caf-109">*pCanSeekForward*</span><span class="sxs-lookup"><span data-stu-id="a4caf-109">*pCanSeekForward*</span></span> 
</dt> <dd>

<span data-ttu-id="a4caf-110">Ponteiro para uma variável que recebe o valor OATRUE se o filtro puder ser encaminhado ou OAFALSE caso contrário.</span><span class="sxs-lookup"><span data-stu-id="a4caf-110">Pointer to a variable that receives the value OATRUE if the filter can seek forward, or OAFALSE otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4caf-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a4caf-111">Return value</span></span>

<span data-ttu-id="a4caf-112">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="a4caf-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4caf-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4caf-113">Requirements</span></span>



| <span data-ttu-id="a4caf-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4caf-114">Requirement</span></span> | <span data-ttu-id="a4caf-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a4caf-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4caf-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a4caf-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a4caf-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a4caf-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a4caf-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a4caf-118">Library</span></span><br/> | <dl> <span data-ttu-id="a4caf-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a4caf-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4caf-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4caf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4caf-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="a4caf-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




