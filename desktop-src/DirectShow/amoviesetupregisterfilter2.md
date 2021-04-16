---
description: A função AMovieSetupRegisterFilter2 registra o mérito, os PINs e os tipos de mídia do filtro no registro usando a interface IFilterMapper2.
ms.assetid: 8e0f3485-9e5d-4b22-853d-4ad9b1fb71d2
title: Função AMovieSetupRegisterFilter2 (Dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 272b781cf70f1dede9d4eea64b45d3d9d793a119
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750918"
---
# <a name="amoviesetupregisterfilter2-function"></a><span data-ttu-id="f139d-103">Função AMovieSetupRegisterFilter2</span><span class="sxs-lookup"><span data-stu-id="f139d-103">AMovieSetupRegisterFilter2 function</span></span>

<span data-ttu-id="f139d-104">A função **AMovieSetupRegisterFilter2** registra o mérito, os PINs e os tipos de mídia do filtro no registro usando a interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .</span><span class="sxs-lookup"><span data-stu-id="f139d-104">The **AMovieSetupRegisterFilter2** function registers a filter's merit, pins, and media types in the registry using the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f139d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f139d-105">Syntax</span></span>


```C++
HRESULT AMovieDllRegisterServer(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper2             *pIFM2,
         BOOL                       bRegister
);
```



## <a name="parameters"></a><span data-ttu-id="f139d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f139d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f139d-107">*psetupdata*</span><span class="sxs-lookup"><span data-stu-id="f139d-107">*psetupdata*</span></span> 
</dt> <dd>

<span data-ttu-id="f139d-108">Ponteiro para os dados do [**\_ filtro AMOVIESETUP**](amoviesetup-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="f139d-108">Pointer to the [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) data.</span></span>

</dd> <dt>

<span data-ttu-id="f139d-109">*pIFM2*</span><span class="sxs-lookup"><span data-stu-id="f139d-109">*pIFM2*</span></span> 
</dt> <dd>

<span data-ttu-id="f139d-110">Ponteiro para a interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .</span><span class="sxs-lookup"><span data-stu-id="f139d-110">Pointer to [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface.</span></span>

</dd> <dt>

<span data-ttu-id="f139d-111">*bRegister*</span><span class="sxs-lookup"><span data-stu-id="f139d-111">*bRegister*</span></span> 
</dt> <dd>

<span data-ttu-id="f139d-112">Valor que indica se o filtro deve ser registrado; **Verdadeiro** indica registrar o filtro; **falso** indica cancelar o registro.</span><span class="sxs-lookup"><span data-stu-id="f139d-112">Value indicating whether to register the filter; **TRUE** indicates register the filter, **FALSE** indicates unregister it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f139d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f139d-113">Return value</span></span>

<span data-ttu-id="f139d-114">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f139d-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f139d-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f139d-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f139d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f139d-116">Remarks</span></span>

<span data-ttu-id="f139d-117">A função [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) chama essa função auxiliar para registrar um filtro após o registro do servidor com.</span><span class="sxs-lookup"><span data-stu-id="f139d-117">The [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function calls this helper function to register a filter after the COM server has been registered.</span></span>

<span data-ttu-id="f139d-118">Normalmente, um filtro usará [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) e não chamará essa função diretamente.</span><span class="sxs-lookup"><span data-stu-id="f139d-118">Typically, a filter will use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) and will not call this function directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="f139d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f139d-119">Requirements</span></span>



| <span data-ttu-id="f139d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f139d-120">Requirement</span></span> | <span data-ttu-id="f139d-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f139d-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f139d-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f139d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f139d-123"><dt>Dllsetup. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f139d-123"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f139d-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f139d-124">Library</span></span><br/> | <dl> <span data-ttu-id="f139d-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f139d-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f139d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f139d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f139d-127">**Funções de instalação de DLL**</span><span class="sxs-lookup"><span data-stu-id="f139d-127">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




