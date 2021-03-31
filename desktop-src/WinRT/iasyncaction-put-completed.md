---
description: Define o método que é chamado quando a ação assíncrona é concluída.
ms.assetid: 632800E4-D02B-4D45-8A9B-B373AC938558
title: 'IAsyncAction: método de ut_Completed de:p'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.put_Completed
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: ec26401aeeed61445b0f244880864366fd5c6118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920918"
---
# <a name="iasyncactionput_completed-method"></a><span data-ttu-id="5c9a2-103">IAsyncAction::p o \_ método UT Completed</span><span class="sxs-lookup"><span data-stu-id="5c9a2-103">IAsyncAction::put\_Completed method</span></span>

<span data-ttu-id="5c9a2-104">Define o método que é chamado quando a ação assíncrona é concluída.</span><span class="sxs-lookup"><span data-stu-id="5c9a2-104">Sets the method that is called when the asynchronous action completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c9a2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c9a2-105">Syntax</span></span>


```C++
HRESULT put_Completed(
  [out] AsyncActionCompletedHandler *handler
);
```



## <a name="parameters"></a><span data-ttu-id="5c9a2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c9a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c9a2-107">*manipulador* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5c9a2-107">*handler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c9a2-108">Tipo: \**[**AsyncActionCompletedHandler**](asyncactioncompletedhandler.md) \** _</span><span class="sxs-lookup"><span data-stu-id="5c9a2-108">Type: \**[**AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)\** _</span></span>

<span data-ttu-id="5c9a2-109">O método que manipula a notificação de conclusão.</span><span class="sxs-lookup"><span data-stu-id="5c9a2-109">The method that handles the completion notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c9a2-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5c9a2-110">Return value</span></span>

<span data-ttu-id="5c9a2-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="5c9a2-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="5c9a2-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5c9a2-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5c9a2-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5c9a2-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c9a2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c9a2-114">Requirements</span></span>



| <span data-ttu-id="5c9a2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c9a2-115">Requirement</span></span> | <span data-ttu-id="5c9a2-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5c9a2-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c9a2-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c9a2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5c9a2-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5c9a2-118">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="5c9a2-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c9a2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5c9a2-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5c9a2-120">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="5c9a2-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5c9a2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c9a2-122"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5c9a2-122"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c9a2-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c9a2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c9a2-124">**IAsyncAction**</span><span class="sxs-lookup"><span data-stu-id="5c9a2-124">**IAsyncAction**</span></span>](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
