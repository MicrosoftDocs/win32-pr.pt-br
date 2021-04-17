---
description: A função DbgInitialise Inicializa a biblioteca de depuração. Ignorado em compilações de varejo.
ms.assetid: d4ca739e-cd39-4692-81da-c5a88a09d546
title: Função DbgInitialise (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgInitialise
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 33a62c8dad7ef6e15b9b11461303b1bced977a96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754767"
---
# <a name="dbginitialise-function"></a><span data-ttu-id="1c9f7-104">Função DbgInitialise</span><span class="sxs-lookup"><span data-stu-id="1c9f7-104">DbgInitialise function</span></span>

<span data-ttu-id="1c9f7-105">A função **DbgInitialise** Inicializa a biblioteca de depuração.</span><span class="sxs-lookup"><span data-stu-id="1c9f7-105">The **DbgInitialise** function initializes the debug library.</span></span> <span data-ttu-id="1c9f7-106">Ignorado em compilações de varejo.</span><span class="sxs-lookup"><span data-stu-id="1c9f7-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c9f7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1c9f7-107">Syntax</span></span>


```C++
void DbgInitialise(
   HINSTANCE hInst
);
```



## <a name="parameters"></a><span data-ttu-id="1c9f7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1c9f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c9f7-109">*hInst*</span><span class="sxs-lookup"><span data-stu-id="1c9f7-109">*hInst*</span></span> 
</dt> <dd>

<span data-ttu-id="1c9f7-110">Identificador para a instância do módulo.</span><span class="sxs-lookup"><span data-stu-id="1c9f7-110">Handle to the module instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c9f7-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1c9f7-111">Return value</span></span>

<span data-ttu-id="1c9f7-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1c9f7-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c9f7-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c9f7-113">Remarks</span></span>

<span data-ttu-id="1c9f7-114">Em um executável, chame esse método antes de usar os recursos de depuração do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1c9f7-114">In an executable, call this method before using the DirectShow debug facilities.</span></span> <span data-ttu-id="1c9f7-115">Antes de o executável sair, chame a função [**DbgTerminate**](dbgterminate.md) para limpar a biblioteca de depuração.</span><span class="sxs-lookup"><span data-stu-id="1c9f7-115">Before the executable quits, call the [**DbgTerminate**](dbgterminate.md) function to clean up the debug library.</span></span>

<span data-ttu-id="1c9f7-116">Em uma DLL que vincula à biblioteca de classe base (Strmbase. lib), não é necessário chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="1c9f7-116">In a DLL that links to the base-class library (Strmbase.lib), it is not necessary to call this function.</span></span> <span data-ttu-id="1c9f7-117">A função é chamada automaticamente quando a DLL é carregada.</span><span class="sxs-lookup"><span data-stu-id="1c9f7-117">The function is called automatically when the DLL is loaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c9f7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c9f7-118">Requirements</span></span>



| <span data-ttu-id="1c9f7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c9f7-119">Requirement</span></span> | <span data-ttu-id="1c9f7-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1c9f7-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c9f7-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1c9f7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1c9f7-122"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c9f7-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1c9f7-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1c9f7-123">Library</span></span><br/> | <dl> <span data-ttu-id="1c9f7-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1c9f7-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c9f7-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c9f7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c9f7-126">Funções de saída de depuração</span><span class="sxs-lookup"><span data-stu-id="1c9f7-126">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




