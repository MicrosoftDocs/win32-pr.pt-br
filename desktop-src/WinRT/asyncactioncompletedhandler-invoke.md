---
description: Invoca o método que é chamado quando a ação assíncrona especificada é concluída.
ms.assetid: 97199C1A-7CE3-4BBD-86A3-2CA9B27CC05E
title: 'Método AsyncActionCompletedHandler:: Invoke'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncActionCompletedHandler.Invoke
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 1cba9c48fa955b82fdc337ba641acbd4c62f6406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090420"
---
# <a name="asyncactioncompletedhandlerinvoke-method"></a><span data-ttu-id="91e4b-103">Método AsyncActionCompletedHandler:: Invoke</span><span class="sxs-lookup"><span data-stu-id="91e4b-103">AsyncActionCompletedHandler::Invoke method</span></span>

<span data-ttu-id="91e4b-104">Invoca o método que é chamado quando a ação assíncrona especificada é concluída.</span><span class="sxs-lookup"><span data-stu-id="91e4b-104">Invokes the method that is called when the specified asynchronous action completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="91e4b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91e4b-105">Syntax</span></span>


```C++
HRESULT Invoke(
  [in] IAsyncAction *asyncInfo
);
```



## <a name="parameters"></a><span data-ttu-id="91e4b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91e4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91e4b-107">*asyncInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="91e4b-107">*asyncInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91e4b-108">Tipo: \**[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) \** _</span><span class="sxs-lookup"><span data-stu-id="91e4b-108">Type: \**[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)\** _</span></span>

<span data-ttu-id="91e4b-109">A ação assíncrona que relata a conclusão.</span><span class="sxs-lookup"><span data-stu-id="91e4b-109">The asynchronous action that reports completion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91e4b-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="91e4b-110">Return value</span></span>

<span data-ttu-id="91e4b-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="91e4b-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="91e4b-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="91e4b-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="91e4b-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="91e4b-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="91e4b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91e4b-114">Requirements</span></span>



| <span data-ttu-id="91e4b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="91e4b-115">Requirement</span></span> | <span data-ttu-id="91e4b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="91e4b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91e4b-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91e4b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="91e4b-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="91e4b-118">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="91e4b-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91e4b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="91e4b-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="91e4b-120">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="91e4b-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="91e4b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="91e4b-122"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="91e4b-122"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91e4b-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="91e4b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91e4b-124">**AsyncActionCompletedHandler**</span><span class="sxs-lookup"><span data-stu-id="91e4b-124">**AsyncActionCompletedHandler**</span></span>](asyncactioncompletedhandler.md)
</dt> </dl>

 

