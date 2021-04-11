---
description: Obtém o tipo de alteração que ocorreu no vetor.
ms.assetid: 213f4794-b972-44e3-a400-8a24b1583ddd
title: 'Método IVectorChangedEventArgs:: get_CollectionChange (IVectorChangedEventArgs. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_CollectionChange
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: a843574bcaf93ec524173ba76800cc15012c89fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164481"
---
# <a name="ivectorchangedeventargsget_collectionchange-method"></a><span data-ttu-id="c5b05-103">Método IVectorChangedEventArgs:: get \_ CollectionChange</span><span class="sxs-lookup"><span data-stu-id="c5b05-103">IVectorChangedEventArgs::get\_CollectionChange method</span></span>

<span data-ttu-id="c5b05-104">Obtém o tipo de alteração que ocorreu no vetor.</span><span class="sxs-lookup"><span data-stu-id="c5b05-104">Gets the type of change that occurred in the vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5b05-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5b05-105">Syntax</span></span>


```C++
HRESULT get_CollectionChange(
  [out, retval] CollectionChange *value
);
```



## <a name="parameters"></a><span data-ttu-id="c5b05-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5b05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5b05-107">*valor* \[ do out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c5b05-107">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c5b05-108">Tipo: \**CollectionChange \** _</span><span class="sxs-lookup"><span data-stu-id="c5b05-108">Type: \**CollectionChange\** _</span></span>

<span data-ttu-id="c5b05-109">Um valor da enumeração [_ *CollectionChange* \*](/uwp/api/Windows.Foundation.Collections.CollectionChange?view=winrt-19041) que descreve a alteração.</span><span class="sxs-lookup"><span data-stu-id="c5b05-109">A value from the [_ *CollectionChange*\*](/uwp/api/Windows.Foundation.Collections.CollectionChange?view=winrt-19041) enumeration that describes the change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5b05-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c5b05-110">Return value</span></span>

<span data-ttu-id="c5b05-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c5b05-111">Type: **HRESULT**</span></span>

<span data-ttu-id="c5b05-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c5b05-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c5b05-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c5b05-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5b05-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5b05-114">Requirements</span></span>



| <span data-ttu-id="c5b05-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5b05-115">Requirement</span></span> | <span data-ttu-id="c5b05-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c5b05-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5b05-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5b05-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c5b05-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c5b05-118">Windows 8</span></span><br/>                                                                                 |
| <span data-ttu-id="c5b05-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5b05-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c5b05-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c5b05-120">Windows Server 2012</span></span><br/>                                                                       |
| <span data-ttu-id="c5b05-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c5b05-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5b05-122"><dt>IVectorChangedEventArgs. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5b05-122"><dt>IVectorChangedEventArgs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5b05-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5b05-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5b05-124">**IVectorChangedEventArgs**</span><span class="sxs-lookup"><span data-stu-id="c5b05-124">**IVectorChangedEventArgs**</span></span>](ivectorchangedeventargs.md)
</dt> </dl>

 

 
