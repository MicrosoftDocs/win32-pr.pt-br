---
title: Função WMDRMShutdown (wmdrmsdk. h)
description: A função WMDRMShutdown libera recursos usados pelas APIs estendidas do cliente DRM do Windows Media.
ms.assetid: fa99a07a-2f07-464b-b7a2-e8f3110389b5
keywords:
- Formato de mídia do Windows da função WMDRMShutdown
topic_type:
- apiref
api_name:
- WMDRMShutdown
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb49049a593699a4071eefea9c5cf7c61571fc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779503"
---
# <a name="wmdrmshutdown-function"></a><span data-ttu-id="1ecc0-104">Função WMDRMShutdown</span><span class="sxs-lookup"><span data-stu-id="1ecc0-104">WMDRMShutdown function</span></span>

<span data-ttu-id="1ecc0-105">A função **WMDRMShutdown** libera recursos usados pelas APIs estendidas do cliente DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1ecc0-105">The **WMDRMShutdown** function releases resources used by the Windows Media DRM Client Extended APIs.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ecc0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ecc0-106">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMShutdown(void);
```



## <a name="parameters"></a><span data-ttu-id="1ecc0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ecc0-107">Parameters</span></span>

<span data-ttu-id="1ecc0-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1ecc0-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1ecc0-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1ecc0-109">Return value</span></span>

<span data-ttu-id="1ecc0-110">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1ecc0-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1ecc0-111">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1ecc0-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1ecc0-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1ecc0-112">Return code</span></span>                                                                          | <span data-ttu-id="1ecc0-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ecc0-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="1ecc0-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1ecc0-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1ecc0-115">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="1ecc0-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1ecc0-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ecc0-116">Remarks</span></span>

<span data-ttu-id="1ecc0-117">Para evitar vazamentos de memória, você deve chamar essa função para cada chamada da função [**WMDRMStartup**](wmdrmstartup.md) .</span><span class="sxs-lookup"><span data-stu-id="1ecc0-117">To avoid memory leaks, you must call this function for every call of the [**WMDRMStartup**](wmdrmstartup.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ecc0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ecc0-118">Requirements</span></span>



| <span data-ttu-id="1ecc0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ecc0-119">Requirement</span></span> | <span data-ttu-id="1ecc0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1ecc0-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ecc0-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ecc0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1ecc0-122"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ecc0-122"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="1ecc0-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1ecc0-123">Library</span></span><br/> | <dl> <span data-ttu-id="1ecc0-124"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ecc0-124"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |
| <span data-ttu-id="1ecc0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1ecc0-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="1ecc0-126"><dt>Wmdrmsdk.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ecc0-126"><dt>Wmdrmsdk.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ecc0-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ecc0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ecc0-128">**Funções**</span><span class="sxs-lookup"><span data-stu-id="1ecc0-128">**Functions**</span></span>](drm-functions.md)
</dt> </dl>

 

 





