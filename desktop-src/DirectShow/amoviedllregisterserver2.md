---
description: A função AMovieDllRegisterServer2 registra e cancela o registro de filtros.
ms.assetid: 2122949d-0117-4c68-bfcd-c717b14dc970
title: Função AMovieDllRegisterServer2 (Dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer2
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec36290b7cad66b2b5f27633d30ae76c3331eba9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748842"
---
# <a name="amoviedllregisterserver2-function"></a><span data-ttu-id="1087d-103">Função AMovieDllRegisterServer2</span><span class="sxs-lookup"><span data-stu-id="1087d-103">AMovieDllRegisterServer2 function</span></span>

<span data-ttu-id="1087d-104">A função **AMovieDllRegisterServer2** registra e cancela o registro de filtros.</span><span class="sxs-lookup"><span data-stu-id="1087d-104">The **AMovieDllRegisterServer2** function registers and unregisters filters.</span></span>

## <a name="syntax"></a><span data-ttu-id="1087d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1087d-105">Syntax</span></span>


```C++
HRESULT AMovieDllRegisterServer2(
   BOOL bRegister
);
```



## <a name="parameters"></a><span data-ttu-id="1087d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1087d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1087d-107">*bRegister*</span><span class="sxs-lookup"><span data-stu-id="1087d-107">*bRegister*</span></span> 
</dt> <dd>

<span data-ttu-id="1087d-108">**Verdadeiro** indica registrar o filtro; **falso** indica cancelar o registro.</span><span class="sxs-lookup"><span data-stu-id="1087d-108">**TRUE** indicates register the filter, **FALSE** indicates unregister it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1087d-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1087d-109">Return value</span></span>

<span data-ttu-id="1087d-110">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1087d-110">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1087d-111">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1087d-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1087d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="1087d-112">Remarks</span></span>

<span data-ttu-id="1087d-113">Use essa função para configurar seus filtros.</span><span class="sxs-lookup"><span data-stu-id="1087d-113">Use this function to set up your filters.</span></span> <span data-ttu-id="1087d-114">Para obter mais informações, consulte [como registrar filtros do DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="1087d-114">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1087d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1087d-115">Requirements</span></span>



| <span data-ttu-id="1087d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1087d-116">Requirement</span></span> | <span data-ttu-id="1087d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1087d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1087d-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1087d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1087d-119"><dt>Dllsetup. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1087d-119"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1087d-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1087d-120">Library</span></span><br/> | <dl> <span data-ttu-id="1087d-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1087d-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1087d-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="1087d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1087d-123">**Funções de instalação de DLL**</span><span class="sxs-lookup"><span data-stu-id="1087d-123">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




