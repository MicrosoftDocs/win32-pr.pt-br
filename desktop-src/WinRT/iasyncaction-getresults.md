---
description: Obtém o resultado de uma ação assíncrona.
ms.assetid: E5AF357D-B1EE-4581-AEBC-6F1C89D7DBB0
title: 'Método IAsyncAction:: GetResults'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.GetResults
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 292c73846227f1bb8884b24b7e709bc6b2296e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164484"
---
# <a name="iasyncactiongetresults-method"></a><span data-ttu-id="03ce3-103">Método IAsyncAction:: GetResults</span><span class="sxs-lookup"><span data-stu-id="03ce3-103">IAsyncAction::GetResults method</span></span>

<span data-ttu-id="03ce3-104">Obtém o resultado de uma ação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="03ce3-104">Gets the outcome of an asynchronous action.</span></span>

## <a name="syntax"></a><span data-ttu-id="03ce3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03ce3-105">Syntax</span></span>


```C++
HRESULT GetResults();
```



## <a name="parameters"></a><span data-ttu-id="03ce3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="03ce3-106">Parameters</span></span>

<span data-ttu-id="03ce3-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="03ce3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="03ce3-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="03ce3-108">Return value</span></span>

<span data-ttu-id="03ce3-109">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="03ce3-109">Type: **HRESULT**</span></span>

<span data-ttu-id="03ce3-110">Esse método sempre retorna **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="03ce3-110">This method always returns **S\_OK**.</span></span>

## <a name="remarks"></a><span data-ttu-id="03ce3-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="03ce3-111">Remarks</span></span>

<span data-ttu-id="03ce3-112">Chamar o método **GetResults** não terá efeito se a implementação atual tiver um tipo dinâmico de [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction).</span><span class="sxs-lookup"><span data-stu-id="03ce3-112">Calling the **GetResults** method has no effect if the current implementation has a dynamic type of [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction).</span></span>

## <a name="requirements"></a><span data-ttu-id="03ce3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03ce3-113">Requirements</span></span>



| <span data-ttu-id="03ce3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="03ce3-114">Requirement</span></span> | <span data-ttu-id="03ce3-115">Valor</span><span class="sxs-lookup"><span data-stu-id="03ce3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03ce3-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03ce3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="03ce3-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="03ce3-117">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="03ce3-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03ce3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="03ce3-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="03ce3-119">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="03ce3-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="03ce3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="03ce3-121"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="03ce3-121"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03ce3-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="03ce3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03ce3-123">**IAsyncAction**</span><span class="sxs-lookup"><span data-stu-id="03ce3-123">**IAsyncAction**</span></span>](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
