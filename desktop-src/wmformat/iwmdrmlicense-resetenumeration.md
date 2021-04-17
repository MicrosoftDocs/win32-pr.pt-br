---
title: Método IWMDRMLicense ResetEnumeration (wmdrmsdk. h)
description: O método ResetEnumeration redefine a lista de licenças para seu estado original. A licença ativa torna-se a primeira licença da lista.
ms.assetid: cb5a31a8-ee25-44d6-81ca-746c379cb99e
keywords:
- Formato de mídia do Windows do método ResetEnumeration
- Método ResetEnumeration Windows Media Format, interface IWMDRMLicense
- Formato de mídia do Windows de interface IWMDRMLicense, método ResetEnumeration
topic_type:
- apiref
api_name:
- IWMDRMLicense.ResetEnumeration
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6510c05b4c974051d9902ed2d30d9cdf99956af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813678"
---
# <a name="iwmdrmlicenseresetenumeration-method"></a><span data-ttu-id="cf050-107">Método IWMDRMLicense:: ResetEnumeration</span><span class="sxs-lookup"><span data-stu-id="cf050-107">IWMDRMLicense::ResetEnumeration method</span></span>

<span data-ttu-id="cf050-108">O método **ResetEnumeration** redefine a lista de licenças para seu estado original.</span><span class="sxs-lookup"><span data-stu-id="cf050-108">The **ResetEnumeration** method resets the license list to its original state.</span></span> <span data-ttu-id="cf050-109">A licença ativa torna-se a primeira licença da lista.</span><span class="sxs-lookup"><span data-stu-id="cf050-109">The active license becomes the first license in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf050-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cf050-110">Syntax</span></span>


```C++
HRESULT ResetEnumeration();
```



## <a name="parameters"></a><span data-ttu-id="cf050-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf050-111">Parameters</span></span>

<span data-ttu-id="cf050-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cf050-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cf050-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cf050-113">Return value</span></span>

<span data-ttu-id="cf050-114">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="cf050-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="cf050-115">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="cf050-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="cf050-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="cf050-116">Return code</span></span>                                                                                                | <span data-ttu-id="cf050-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf050-117">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="cf050-118"><dt>**RIV do NS \_ E \_ DRM \_ \_ muito \_ pequeno**</dt></span><span class="sxs-lookup"><span data-stu-id="cf050-118"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="cf050-119">Uma lista de revogação de conteúdo atualizada é necessária.</span><span class="sxs-lookup"><span data-stu-id="cf050-119">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="cf050-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cf050-120"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="cf050-121">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="cf050-121">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="cf050-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf050-122">Remarks</span></span>

<span data-ttu-id="cf050-123">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="cf050-123">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf050-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf050-124">Requirements</span></span>



| <span data-ttu-id="cf050-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf050-125">Requirement</span></span> | <span data-ttu-id="cf050-126">Valor</span><span class="sxs-lookup"><span data-stu-id="cf050-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf050-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cf050-127">Header</span></span><br/>  | <dl> <span data-ttu-id="cf050-128"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf050-128"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="cf050-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cf050-129">Library</span></span><br/> | <dl> <span data-ttu-id="cf050-130"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf050-130"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf050-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf050-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf050-132">**Interface IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="cf050-132">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





