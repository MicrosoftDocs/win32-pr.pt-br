---
title: Função WMDRMStartup (wmdrmsdk. h)
description: A função WMDRMStartup Inicializa os recursos usados pelas APIs estendidas do cliente DRM do Windows Media.
ms.assetid: 2fd26bcc-8106-4356-933a-d4cf3536f4fb
keywords:
- Formato de mídia do Windows da função WMDRMStartup
topic_type:
- apiref
api_name:
- WMDRMStartup
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c152a5160750f3c1943b455a8877b4615781b6ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752324"
---
# <a name="wmdrmstartup-function"></a><span data-ttu-id="3fa20-104">Função WMDRMStartup</span><span class="sxs-lookup"><span data-stu-id="3fa20-104">WMDRMStartup function</span></span>

<span data-ttu-id="3fa20-105">A função **WMDRMStartup** Inicializa os recursos usados pelas APIs estendidas do cliente DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3fa20-105">The **WMDRMStartup** function initializes resources used by the Windows Media DRM Client Extended APIs.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fa20-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3fa20-106">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMStartup(void);
```



## <a name="parameters"></a><span data-ttu-id="3fa20-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3fa20-107">Parameters</span></span>

<span data-ttu-id="3fa20-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3fa20-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3fa20-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="3fa20-109">Return value</span></span>

<span data-ttu-id="3fa20-110">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3fa20-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3fa20-111">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3fa20-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3fa20-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3fa20-112">Return code</span></span>                                                                          | <span data-ttu-id="3fa20-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="3fa20-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3fa20-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3fa20-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3fa20-115">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="3fa20-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3fa20-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3fa20-116">Remarks</span></span>

<span data-ttu-id="3fa20-117">Para cada chamada dessa função, você deve chamar [**WMDRMShutdown**](wmdrmshutdown.md) para liberar os recursos usados.</span><span class="sxs-lookup"><span data-stu-id="3fa20-117">For every call of this function, you must call [**WMDRMShutdown**](wmdrmshutdown.md) to release the resources used.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fa20-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fa20-118">Requirements</span></span>



| <span data-ttu-id="3fa20-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fa20-119">Requirement</span></span> | <span data-ttu-id="3fa20-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3fa20-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fa20-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3fa20-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3fa20-122"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fa20-122"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="3fa20-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3fa20-123">Library</span></span><br/> | <dl> <span data-ttu-id="3fa20-124"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3fa20-124"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |
| <span data-ttu-id="3fa20-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3fa20-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="3fa20-126"><dt>Wmdrmsdk.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fa20-126"><dt>Wmdrmsdk.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fa20-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="3fa20-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fa20-128">**Funções**</span><span class="sxs-lookup"><span data-stu-id="3fa20-128">**Functions**</span></span>](drm-functions.md)
</dt> </dl>

 

 





