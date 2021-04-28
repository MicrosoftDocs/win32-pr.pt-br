---
description: Função AMovieDllUnregisterServer – obsoleta. Use AMovieDllRegisterServer2 em vez disso.
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
ms.openlocfilehash: df7fb34246249298efc143b7ccc8e6332540867c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099924"
---
# <a name="amoviedllunregisterserver-function"></a><span data-ttu-id="1703e-104">Função AMovieDllUnregisterServer</span><span class="sxs-lookup"><span data-stu-id="1703e-104">AMovieDllUnregisterServer function</span></span>

<span data-ttu-id="1703e-105">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="1703e-105">Obsolete.</span></span> <span data-ttu-id="1703e-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="1703e-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="1703e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1703e-107">Syntax</span></span>


```C++
HRESULT AMovieDllUnregisterServer(void);
```



## <a name="parameters"></a><span data-ttu-id="1703e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1703e-108">Parameters</span></span>

<span data-ttu-id="1703e-109">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1703e-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1703e-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1703e-110">Return value</span></span>

<span data-ttu-id="1703e-111">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1703e-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1703e-112">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1703e-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1703e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1703e-113">Requirements</span></span>



| <span data-ttu-id="1703e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1703e-114">Requirement</span></span> | <span data-ttu-id="1703e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1703e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1703e-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1703e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="1703e-117"><dt>Dllsetup. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1703e-117"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1703e-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1703e-118">Library</span></span><br/> | <dl> <span data-ttu-id="1703e-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1703e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1703e-120">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1703e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1703e-121">**Funções de instalação de DLL**</span><span class="sxs-lookup"><span data-stu-id="1703e-121">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




