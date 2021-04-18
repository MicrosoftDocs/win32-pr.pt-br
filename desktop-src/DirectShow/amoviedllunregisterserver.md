---
description: Obsoleto. Use AMovieDllRegisterServer2 em vez disso.
ms.assetid: 80f52109-6239-4e3d-a395-eb69f5278cd2
title: Função AMovieDllUnregisterServer (Dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllUnregisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4cab526a69f14cdd4c4f48767ca34722f61002eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760101"
---
# <a name="amoviedllunregisterserver-function"></a><span data-ttu-id="4b7e2-104">Função AMovieDllUnregisterServer</span><span class="sxs-lookup"><span data-stu-id="4b7e2-104">AMovieDllUnregisterServer function</span></span>

<span data-ttu-id="4b7e2-105">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="4b7e2-105">Obsolete.</span></span> <span data-ttu-id="4b7e2-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="4b7e2-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b7e2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b7e2-107">Syntax</span></span>


```C++
HRESULT AMovieDllUnregisterServer(void);
```



## <a name="parameters"></a><span data-ttu-id="4b7e2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b7e2-108">Parameters</span></span>

<span data-ttu-id="4b7e2-109">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4b7e2-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b7e2-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4b7e2-110">Return value</span></span>

<span data-ttu-id="4b7e2-111">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4b7e2-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4b7e2-112">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4b7e2-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b7e2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b7e2-113">Requirements</span></span>



| <span data-ttu-id="4b7e2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b7e2-114">Requirement</span></span> | <span data-ttu-id="4b7e2-115">Valor</span><span class="sxs-lookup"><span data-stu-id="4b7e2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b7e2-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4b7e2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4b7e2-117"><dt>Dllsetup. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b7e2-117"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4b7e2-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4b7e2-118">Library</span></span><br/> | <dl> <span data-ttu-id="4b7e2-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4b7e2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b7e2-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b7e2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b7e2-121">**Funções de instalação de DLL**</span><span class="sxs-lookup"><span data-stu-id="4b7e2-121">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




