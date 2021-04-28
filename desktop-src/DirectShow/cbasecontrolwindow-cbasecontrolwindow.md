---
description: Construtor de CBaseControlWindow. CBaseControlWindow-método de construtor.
ms.assetid: 575f7f94-5f55-4834-bdb6-0db877187388
title: Construtor CBaseControlWindow. CBaseControlWindow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.CBaseControlWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 47c8277a76dbf0fbb9e05262eea5b419466044cc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096334"
---
# <a name="cbasecontrolwindowcbasecontrolwindow-constructor"></a><span data-ttu-id="049b4-103">Construtor CBaseControlWindow. CBaseControlWindow</span><span class="sxs-lookup"><span data-stu-id="049b4-103">CBaseControlWindow.CBaseControlWindow constructor</span></span>

<span data-ttu-id="049b4-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="049b4-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="049b4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="049b4-105">Syntax</span></span>


```C++
CBaseControlWindow(
   CBaseMediaFilter *pFilter,
   CCritSec         *pInterfaceLock,
   TCHAR            *pName,
   LPUNKNOWN        pUnk,
   HRESULT          *phr
);
```



## <a name="parameters"></a><span data-ttu-id="049b4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="049b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="049b4-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="049b4-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="049b4-108">Ponteiro para o objeto de filtro de mídia proprietário.</span><span class="sxs-lookup"><span data-stu-id="049b4-108">Pointer to the owning media filter object.</span></span>

</dd> <dt>

<span data-ttu-id="049b4-109">*pInterfaceLock*</span><span class="sxs-lookup"><span data-stu-id="049b4-109">*pInterfaceLock*</span></span> 
</dt> <dd>

<span data-ttu-id="049b4-110">Ponteiro para a seção crítica a ser usada para bloqueio.</span><span class="sxs-lookup"><span data-stu-id="049b4-110">Pointer to the critical section to use for locking.</span></span>

</dd> <dt>

<span data-ttu-id="049b4-111">*pName*</span><span class="sxs-lookup"><span data-stu-id="049b4-111">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="049b4-112">Ponteiro para a descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="049b4-112">Pointer to the object description.</span></span>

</dd> <dt>

<span data-ttu-id="049b4-113">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="049b4-113">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="049b4-114">Ponteiro para a interface **IUnknown** de controle, se o objeto fizer parte de uma agregação; caso contrário, deve ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="049b4-114">Pointer to the controlling **IUnknown** interface, if the object is part of an aggregate; otherwise, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="049b4-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="049b4-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="049b4-116">Ponteiro para uma variável que recebe um valor HRESULT que indica o êxito ou a falha do método de construtor.</span><span class="sxs-lookup"><span data-stu-id="049b4-116">Pointer to a variable that receives an HRESULT value indicating the success or failure of the constructor method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="049b4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="049b4-117">Requirements</span></span>



| <span data-ttu-id="049b4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="049b4-118">Requirement</span></span> | <span data-ttu-id="049b4-119">Valor</span><span class="sxs-lookup"><span data-stu-id="049b4-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="049b4-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="049b4-120">Header</span></span><br/>  | <dl> <span data-ttu-id="049b4-121"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="049b4-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="049b4-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="049b4-122">Library</span></span><br/> | <dl> <span data-ttu-id="049b4-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="049b4-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="049b4-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="049b4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="049b4-125">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="049b4-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




