---
description: Obtém o método que é chamado quando a ação assíncrona é concluída.
ms.assetid: 5050BF84-F9E0-4B3E-9252-6C5C1060826E
title: 'Método IAsyncAction:: get_Completed'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.get_Completed
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: bc018912b2b4643cc4ef2f48cc76eb997a2627fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090416"
---
# <a name="iasyncactionget_completed-method"></a><span data-ttu-id="6d550-103">Método IAsyncAction:: get \_ Completed</span><span class="sxs-lookup"><span data-stu-id="6d550-103">IAsyncAction::get\_Completed method</span></span>

<span data-ttu-id="6d550-104">Obtém o método que é chamado quando a ação assíncrona é concluída.</span><span class="sxs-lookup"><span data-stu-id="6d550-104">Gets the method that is called when the asynchronous action completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d550-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d550-105">Syntax</span></span>


```C++
HRESULT get_Completed(
  [out] AsyncActionCompletedHandler **handler
);
```



## <a name="parameters"></a><span data-ttu-id="6d550-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d550-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d550-107">*manipulador* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6d550-107">*handler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d550-108">Tipo: **[ **AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="6d550-108">Type: **[**AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)\*\***</span></span>

<span data-ttu-id="6d550-109">O método que manipula a notificação de conclusão.</span><span class="sxs-lookup"><span data-stu-id="6d550-109">The method that handles the completion notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d550-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6d550-110">Return value</span></span>

<span data-ttu-id="6d550-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6d550-111">Type: **HRESULT**</span></span>

<span data-ttu-id="6d550-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6d550-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6d550-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6d550-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d550-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d550-114">Requirements</span></span>



| <span data-ttu-id="6d550-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d550-115">Requirement</span></span> | <span data-ttu-id="6d550-116">Valor</span><span class="sxs-lookup"><span data-stu-id="6d550-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d550-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d550-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6d550-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6d550-118">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="6d550-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d550-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6d550-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6d550-120">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="6d550-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6d550-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d550-122"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6d550-122"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d550-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d550-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d550-124">**IAsyncAction**</span><span class="sxs-lookup"><span data-stu-id="6d550-124">**IAsyncAction**</span></span>](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
