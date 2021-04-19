---
description: Obsoleto. Use AMovieDllRegisterServer2 em vez disso.
ms.assetid: d3be5fe0-f993-4a15-a3b8-3d761d51f289
title: Função AMovieDllRegisterServer (Dllsetup. h)
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
ms.openlocfilehash: d93724c0f1ea6ed8b6cd2fa2b683a5ba9d45f0d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779860"
---
# <a name="amoviedllregisterserver-function"></a><span data-ttu-id="b01c8-104">Função AMovieDllRegisterServer</span><span class="sxs-lookup"><span data-stu-id="b01c8-104">AMovieDllRegisterServer function</span></span>

<span data-ttu-id="b01c8-105">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="b01c8-105">Obsolete.</span></span> <span data-ttu-id="b01c8-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="b01c8-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="b01c8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b01c8-107">Syntax</span></span>


```C++
HRESULT AMovieDllRegisterServer(void);
```



## <a name="parameters"></a><span data-ttu-id="b01c8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b01c8-108">Parameters</span></span>

<span data-ttu-id="b01c8-109">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b01c8-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b01c8-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b01c8-110">Return value</span></span>

<span data-ttu-id="b01c8-111">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b01c8-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b01c8-112">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b01c8-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b01c8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b01c8-113">Requirements</span></span>



| <span data-ttu-id="b01c8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b01c8-114">Requirement</span></span> | <span data-ttu-id="b01c8-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b01c8-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b01c8-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b01c8-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b01c8-117"><dt>Dllsetup. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b01c8-117"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b01c8-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b01c8-118">Library</span></span><br/> | <dl> <span data-ttu-id="b01c8-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b01c8-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b01c8-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="b01c8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b01c8-121">**Funções de instalação de DLL**</span><span class="sxs-lookup"><span data-stu-id="b01c8-121">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




