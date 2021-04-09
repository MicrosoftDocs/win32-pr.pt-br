---
description: Obtém a posição no vetor em que a alteração ocorreu.
ms.assetid: 00756d77-aae0-45f0-8bd4-cf68af9bdc7c
title: 'Método IVectorChangedEventArgs:: get_Index (IVectorChangedEventArgs. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_Index
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: 5c131567ec7fc2861ce11db9e5d7ec581f6f663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010496"
---
# <a name="ivectorchangedeventargsget_index-method"></a><span data-ttu-id="c8bed-103">Método de índice IVectorChangedEventArgs:: get \_</span><span class="sxs-lookup"><span data-stu-id="c8bed-103">IVectorChangedEventArgs::get\_Index method</span></span>

<span data-ttu-id="c8bed-104">Obtém a posição no vetor em que a alteração ocorreu.</span><span class="sxs-lookup"><span data-stu-id="c8bed-104">Gets the position in the vector where the change occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8bed-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8bed-105">Syntax</span></span>


```C++
HRESULT get_Index(
  [out, retval] unsigned *value
);
```



## <a name="parameters"></a><span data-ttu-id="c8bed-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8bed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8bed-107">*valor* \[ do out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c8bed-107">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c8bed-108">Tipo: \**não assinado \** _</span><span class="sxs-lookup"><span data-stu-id="c8bed-108">Type: \**unsigned\** _</span></span>

<span data-ttu-id="c8bed-109">A posição de base zero no vetor em que a alteração ocorreu, se aplicável.</span><span class="sxs-lookup"><span data-stu-id="c8bed-109">The zero-based position in the vector where the change occurred, if applicable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8bed-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c8bed-110">Return value</span></span>

<span data-ttu-id="c8bed-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="c8bed-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="c8bed-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c8bed-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c8bed-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c8bed-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8bed-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8bed-114">Requirements</span></span>



| <span data-ttu-id="c8bed-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8bed-115">Requirement</span></span> | <span data-ttu-id="c8bed-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c8bed-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8bed-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8bed-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c8bed-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c8bed-118">Windows 8</span></span><br/>                                                                                 |
| <span data-ttu-id="c8bed-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8bed-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c8bed-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c8bed-120">Windows Server 2012</span></span><br/>                                                                       |
| <span data-ttu-id="c8bed-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c8bed-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8bed-122"><dt>IVectorChangedEventArgs. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8bed-122"><dt>IVectorChangedEventArgs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8bed-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8bed-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8bed-124">**IVectorChangedEventArgs**</span><span class="sxs-lookup"><span data-stu-id="c8bed-124">**IVectorChangedEventArgs**</span></span>](ivectorchangedeventargs.md)
</dt> </dl>

 

 




