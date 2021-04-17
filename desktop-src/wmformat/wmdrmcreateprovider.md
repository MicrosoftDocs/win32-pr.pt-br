---
title: Função WMDRMCreateProvider (wmdrmsdk. h)
description: A função WMDRMCreateProvider cria uma fábrica de classes que pode criar os outros objetos das APIs estendidas do cliente DRM do Windows Media.
ms.assetid: 25ec2fbf-136a-4f40-b2d3-f35b42178c60
keywords:
- Formato de mídia do Windows da função WMDRMCreateProvider
topic_type:
- apiref
api_name:
- WMDRMCreateProvider
api_location:
- Wmdrmsdk.dll
- Ext-MS-Win-mm-wmdrmsdk-l1-1-0.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cdf7a102d969ce916f8a5692d994c183305409a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771310"
---
# <a name="wmdrmcreateprovider-function"></a><span data-ttu-id="67d2d-104">Função WMDRMCreateProvider</span><span class="sxs-lookup"><span data-stu-id="67d2d-104">WMDRMCreateProvider function</span></span>

<span data-ttu-id="67d2d-105">A função **WMDRMCreateProvider** cria uma fábrica de classes que pode criar os outros objetos das APIs estendidas do cliente DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="67d2d-105">The **WMDRMCreateProvider** function creates a class factory that can create the other objects of the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="67d2d-106">Essa função não requer uma biblioteca de stub da Microsoft e cria objetos que não dão suporte aos recursos protegidos do DRM.</span><span class="sxs-lookup"><span data-stu-id="67d2d-106">This function does not require a stub library from Microsoft and creates objects that do not support the protected DRM features.</span></span>

## <a name="syntax"></a><span data-ttu-id="67d2d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67d2d-107">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProvider(
  _Out_ IWMDRMProvider **ppDRMProvider
);
```



## <a name="parameters"></a><span data-ttu-id="67d2d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67d2d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67d2d-109">*ppDRMProvider* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="67d2d-109">*ppDRMProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67d2d-110">Recebe um ponteiro para a interface [**IWMDRMProvider**](iwmdrmprovider.md) do objeto recém-criado.</span><span class="sxs-lookup"><span data-stu-id="67d2d-110">Receives a pointer to the [**IWMDRMProvider**](iwmdrmprovider.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67d2d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="67d2d-111">Return value</span></span>

<span data-ttu-id="67d2d-112">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="67d2d-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="67d2d-113">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="67d2d-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="67d2d-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="67d2d-114">Return code</span></span>                                                                          | <span data-ttu-id="67d2d-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="67d2d-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="67d2d-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="67d2d-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="67d2d-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="67d2d-117">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="67d2d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67d2d-118">Requirements</span></span>



| <span data-ttu-id="67d2d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="67d2d-119">Requirement</span></span> | <span data-ttu-id="67d2d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="67d2d-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67d2d-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="67d2d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="67d2d-122"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="67d2d-122"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="67d2d-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="67d2d-123">Library</span></span><br/> | <dl> <span data-ttu-id="67d2d-124"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67d2d-124"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |
| <span data-ttu-id="67d2d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="67d2d-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="67d2d-126"><dt>Wmdrmsdk.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67d2d-126"><dt>Wmdrmsdk.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67d2d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="67d2d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67d2d-128">**Funções**</span><span class="sxs-lookup"><span data-stu-id="67d2d-128">**Functions**</span></span>](drm-functions.md)
</dt> <dt>

[<span data-ttu-id="67d2d-129">**WMDRMCreateProtectedProvider**</span><span class="sxs-lookup"><span data-stu-id="67d2d-129">**WMDRMCreateProtectedProvider**</span></span>](wmdrmcreateprotectedprovider.md)
</dt> </dl>

 

 





