---
description: 'O método CanSeekBackward determina se o fluxo pode ser buscado retroativamente. Esse método implementa o método IMediaPosition:: CanSeekBackward.'
ms.assetid: 6443980f-6863-4941-b2dd-4a31257b5810
title: Método CPosPassThru. CanSeekBackward (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekBackward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a016f5cfeea7ca1e63bb4d0e603784b8f95a85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775622"
---
# <a name="cpospassthrucanseekbackward-method"></a><span data-ttu-id="eab62-104">Método CPosPassThru. CanSeekBackward</span><span class="sxs-lookup"><span data-stu-id="eab62-104">CPosPassThru.CanSeekBackward method</span></span>

<span data-ttu-id="eab62-105">O `CanSeekBackward` método determina se o fluxo pode ser buscado retroativamente.</span><span class="sxs-lookup"><span data-stu-id="eab62-105">The `CanSeekBackward` method determines whether the stream can be seeked backward.</span></span> <span data-ttu-id="eab62-106">Esse método implementa o método [**IMediaPosition:: CanSeekBackward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekbackward) .</span><span class="sxs-lookup"><span data-stu-id="eab62-106">This method implements the [**IMediaPosition::CanSeekBackward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekbackward) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="eab62-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eab62-107">Syntax</span></span>


```C++
HRESULT CanSeekBackward(
   LONG *pCanSeekBackward
);
```



## <a name="parameters"></a><span data-ttu-id="eab62-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eab62-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eab62-109">*pCanSeekBackward*</span><span class="sxs-lookup"><span data-stu-id="eab62-109">*pCanSeekBackward*</span></span> 
</dt> <dd>

<span data-ttu-id="eab62-110">Ponteiro para uma variável que recebe o valor OATRUE se o filtro puder ser revertido ou OAFALSE caso contrário.</span><span class="sxs-lookup"><span data-stu-id="eab62-110">Pointer to a variable that receives the value OATRUE if the filter can seek backward, or OAFALSE otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eab62-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eab62-111">Return value</span></span>

<span data-ttu-id="eab62-112">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="eab62-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="eab62-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eab62-113">Requirements</span></span>



| <span data-ttu-id="eab62-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="eab62-114">Requirement</span></span> | <span data-ttu-id="eab62-115">Valor</span><span class="sxs-lookup"><span data-stu-id="eab62-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eab62-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eab62-116">Header</span></span><br/>  | <dl> <span data-ttu-id="eab62-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eab62-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="eab62-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eab62-118">Library</span></span><br/> | <dl> <span data-ttu-id="eab62-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="eab62-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eab62-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="eab62-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eab62-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="eab62-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




