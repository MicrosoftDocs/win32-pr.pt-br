---
description: 'Recupera um ponteiro de interface e incrementa a contagem de referência. Esse método implementa o método INonDelegatingUnknown:: NonDelegatingQueryInterface.'
ms.assetid: 451ca350-f40b-4cbf-ac39-e86dadb48a24
title: Método CUnknown. NonDelegatingQueryInterface (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingQueryInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b41810eb52db38644bda472907228cd812f76f6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812786"
---
# <a name="cunknownnondelegatingqueryinterface-method"></a><span data-ttu-id="35912-104">Método CUnknown. NonDelegatingQueryInterface</span><span class="sxs-lookup"><span data-stu-id="35912-104">CUnknown.NonDelegatingQueryInterface method</span></span>

<span data-ttu-id="35912-105">Recupera um ponteiro de interface e incrementa a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="35912-105">Retrieves an interface pointer and increments the reference count.</span></span> <span data-ttu-id="35912-106">Esse método implementa o método **INonDelegatingUnknown:: NonDelegatingQueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="35912-106">This method implements the **INonDelegatingUnknown::NonDelegatingQueryInterface** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="35912-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35912-107">Syntax</span></span>


```C++
HRESULT NonDelegatingQueryInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a><span data-ttu-id="35912-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35912-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35912-109">*riid*</span><span class="sxs-lookup"><span data-stu-id="35912-109">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="35912-110">Identificador da interface.</span><span class="sxs-lookup"><span data-stu-id="35912-110">Identifier of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="35912-111">*ppv*</span><span class="sxs-lookup"><span data-stu-id="35912-111">*ppv*</span></span> 
</dt> <dd>

<span data-ttu-id="35912-112">Endereço de um ponteiro para receber a interface.</span><span class="sxs-lookup"><span data-stu-id="35912-112">Address of a pointer to receive the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35912-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="35912-113">Return value</span></span>

<span data-ttu-id="35912-114">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="35912-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="35912-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="35912-115">Return code</span></span>                                                                                   | <span data-ttu-id="35912-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="35912-116">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="35912-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="35912-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="35912-118">Êxito.</span><span class="sxs-lookup"><span data-stu-id="35912-118">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="35912-119"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="35912-119"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="35912-120">O objeto não oferece suporte a essa interface.</span><span class="sxs-lookup"><span data-stu-id="35912-120">Object does not support this interface.</span></span><br/> |
| <dl> <span data-ttu-id="35912-121"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="35912-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="35912-122">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="35912-122">**NULL** pointer argument.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="35912-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="35912-123">Remarks</span></span>

<span data-ttu-id="35912-124">A classe **CUnknown** expõe apenas a interface **IUknown** .</span><span class="sxs-lookup"><span data-stu-id="35912-124">The **CUnknown** class exposes only the **IUknown** interface.</span></span> <span data-ttu-id="35912-125">Substitua esse método para expor interfaces adicionais.</span><span class="sxs-lookup"><span data-stu-id="35912-125">Override this method to expose additional interfaces.</span></span> <span data-ttu-id="35912-126">Para obter informações sobre como substituir esse método, consulte [como implementar IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="35912-126">For information on how to override this method, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35912-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35912-127">Requirements</span></span>



| <span data-ttu-id="35912-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="35912-128">Requirement</span></span> | <span data-ttu-id="35912-129">Valor</span><span class="sxs-lookup"><span data-stu-id="35912-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35912-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="35912-130">Header</span></span><br/>  | <dl> <span data-ttu-id="35912-131"><dt>Combase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35912-131"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="35912-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="35912-132">Library</span></span><br/> | <dl> <span data-ttu-id="35912-133"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="35912-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




