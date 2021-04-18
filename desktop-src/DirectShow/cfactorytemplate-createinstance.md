---
description: O método CreateInstance chama a função de criação de objeto para a classe.
ms.assetid: 8a7d5c56-867d-432d-a0c2-97b8e3cf8a69
title: Método CFactoryTemplate. CreateInstance (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0f67ba528943bc2a468419fc84db44359745d4a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750046"
---
# <a name="cfactorytemplatecreateinstance-method"></a><span data-ttu-id="baed9-103">Método CFactoryTemplate. CreateInstance</span><span class="sxs-lookup"><span data-stu-id="baed9-103">CFactoryTemplate.CreateInstance method</span></span>

<span data-ttu-id="baed9-104">O `CreateInstance` método chama a função de criação de objeto para a classe.</span><span class="sxs-lookup"><span data-stu-id="baed9-104">The `CreateInstance` method calls the object-creation function for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="baed9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="baed9-105">Syntax</span></span>


```C++
CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="baed9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="baed9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baed9-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="baed9-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="baed9-108">Ponteiro para a interface **IUnknown** de agregação.</span><span class="sxs-lookup"><span data-stu-id="baed9-108">Pointer to the aggregating **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="baed9-109">*phr*</span><span class="sxs-lookup"><span data-stu-id="baed9-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="baed9-110">Ponteiro para uma variável que recebe um valor **HRESULT** que indica o êxito ou a falha do método.</span><span class="sxs-lookup"><span data-stu-id="baed9-110">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baed9-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="baed9-111">Return value</span></span>

<span data-ttu-id="baed9-112">Retorna uma instância do objeto de classe.</span><span class="sxs-lookup"><span data-stu-id="baed9-112">Returns an instance of the class object.</span></span>

## <a name="remarks"></a><span data-ttu-id="baed9-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="baed9-113">Remarks</span></span>

<span data-ttu-id="baed9-114">O método **IClassFactory:: CreateInstance** chama esse método de classe.</span><span class="sxs-lookup"><span data-stu-id="baed9-114">The **IClassFactory::CreateInstance** method calls this class method.</span></span> <span data-ttu-id="baed9-115">Esse método chama a função apontada pela variável de membro [**CFactoryTemplate:: m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md) .</span><span class="sxs-lookup"><span data-stu-id="baed9-115">This method calls the function pointed to by the [**CFactoryTemplate::m\_lpfnNew**](cfactorytemplate-m-lpfnnew.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="baed9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="baed9-116">Requirements</span></span>



| <span data-ttu-id="baed9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="baed9-117">Requirement</span></span> | <span data-ttu-id="baed9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="baed9-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="baed9-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="baed9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="baed9-120"><dt>Combase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="baed9-120"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="baed9-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="baed9-121">Library</span></span><br/> | <dl> <span data-ttu-id="baed9-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="baed9-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baed9-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="baed9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baed9-124">**Classe CFactoryTemplate**</span><span class="sxs-lookup"><span data-stu-id="baed9-124">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




