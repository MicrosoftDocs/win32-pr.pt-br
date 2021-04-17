---
title: Função WMDRMCreateProtectedProvider (wmdrmsdk. h)
description: A função WMDRMCreateProtectedProvider cria uma fábrica de classes que pode criar os outros objetos das APIs estendidas do cliente DRM do Windows Media.
ms.assetid: 0882062f-48a2-43bc-8853-a8a3d6bc2f52
keywords:
- Formato de mídia do Windows da função WMDRMCreateProtectedProvider
topic_type:
- apiref
api_name:
- WMDRMCreateProtectedProvider
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1f046de906c7753fa200de5075cf2064721940b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783778"
---
# <a name="wmdrmcreateprotectedprovider-function"></a><span data-ttu-id="0d024-104">Função WMDRMCreateProtectedProvider</span><span class="sxs-lookup"><span data-stu-id="0d024-104">WMDRMCreateProtectedProvider function</span></span>

<span data-ttu-id="0d024-105">A função **WMDRMCreateProtectedProvider** cria uma fábrica de classes que pode criar os outros objetos das APIs estendidas do cliente DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0d024-105">The **WMDRMCreateProtectedProvider** function creates a class factory that can create the other objects of the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="0d024-106">Essa função requer uma biblioteca de stub da Microsoft e cria objetos que dão suporte aos recursos protegidos do DRM.</span><span class="sxs-lookup"><span data-stu-id="0d024-106">This function requires a stub library from Microsoft and creates objects that support the protected DRM features.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d024-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d024-107">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProtectedProvider(
  _Out_ IWMDRMProvider **ppDRMProvider
);
```



## <a name="parameters"></a><span data-ttu-id="0d024-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d024-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d024-109">*ppDRMProvider* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0d024-109">*ppDRMProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d024-110">Recebe um ponteiro para a interface [**IWMDRMProvider**](iwmdrmprovider.md) do objeto recém-criado.</span><span class="sxs-lookup"><span data-stu-id="0d024-110">Receives a pointer to the [**IWMDRMProvider**](iwmdrmprovider.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d024-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0d024-111">Return value</span></span>

<span data-ttu-id="0d024-112">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0d024-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0d024-113">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0d024-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0d024-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0d024-114">Return code</span></span>                                                                          | <span data-ttu-id="0d024-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d024-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0d024-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0d024-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0d024-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0d024-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0d024-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d024-118">Remarks</span></span>

<span data-ttu-id="0d024-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="0d024-119">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d024-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d024-120">Requirements</span></span>



| <span data-ttu-id="0d024-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d024-121">Requirement</span></span> | <span data-ttu-id="0d024-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0d024-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d024-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0d024-123">Header</span></span><br/> | <dl> <span data-ttu-id="0d024-124"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d024-124"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d024-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d024-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d024-126">**Funções**</span><span class="sxs-lookup"><span data-stu-id="0d024-126">**Functions**</span></span>](drm-functions.md)
</dt> <dt>

[<span data-ttu-id="0d024-127">**WMDRMCreateProvider**</span><span class="sxs-lookup"><span data-stu-id="0d024-127">**WMDRMCreateProvider**</span></span>](wmdrmcreateprovider.md)
</dt> </dl>

 

 





