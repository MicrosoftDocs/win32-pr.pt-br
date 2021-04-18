---
title: Método GetNext IWMDRMLicense (wmdrmsdk. h)
description: O método GetNext carrega as informações sobre o próximo item na lista.
ms.assetid: 5ef91751-2883-4a8e-9908-7a6dfe6d2af3
keywords:
- Formato do Windows Media do método GetNext
- Método GetNext Windows Media Format, interface IWMDRMLicense
- IWMDRMLicense interface formato Windows Media, método GetNext
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetNext
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da1dd1f8ce41648c7a67730d909058d10d616e7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771550"
---
# <a name="iwmdrmlicensegetnext-method"></a><span data-ttu-id="1949e-106">Método IWMDRMLicense:: GetNext</span><span class="sxs-lookup"><span data-stu-id="1949e-106">IWMDRMLicense::GetNext method</span></span>

<span data-ttu-id="1949e-107">O método **GetNext** carrega as informações sobre o próximo item na lista.</span><span class="sxs-lookup"><span data-stu-id="1949e-107">The **GetNext** method loads the information about the next item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="1949e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1949e-108">Syntax</span></span>


```C++
HRESULT GetNext();
```



## <a name="parameters"></a><span data-ttu-id="1949e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1949e-109">Parameters</span></span>

<span data-ttu-id="1949e-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1949e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1949e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1949e-111">Return value</span></span>

<span data-ttu-id="1949e-112">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1949e-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1949e-113">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1949e-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1949e-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1949e-114">Return code</span></span>                                                                                                | <span data-ttu-id="1949e-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="1949e-115">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="1949e-116"><dt>**RIV do NS \_ E \_ DRM \_ \_ muito \_ pequeno**</dt></span><span class="sxs-lookup"><span data-stu-id="1949e-116"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="1949e-117">Uma lista de revogação de conteúdo atualizada é necessária.</span><span class="sxs-lookup"><span data-stu-id="1949e-117">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="1949e-118"><dt>**ERRO \_ não há \_ mais \_ itens**</dt></span><span class="sxs-lookup"><span data-stu-id="1949e-118"><dt>**ERROR\_NO\_MORE\_ITEMS**</dt></span></span> </dl>      | <span data-ttu-id="1949e-119">Não há mais itens na lista.</span><span class="sxs-lookup"><span data-stu-id="1949e-119">There are no more items in the list.</span></span><br/>          |
| <dl> <span data-ttu-id="1949e-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1949e-120"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="1949e-121">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="1949e-121">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="1949e-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="1949e-122">Remarks</span></span>

<span data-ttu-id="1949e-123">Os métodos da interface [**IWMDRMLicense**](iwmdrmlicense.md) fornecem dados sobre uma única licença por vez.</span><span class="sxs-lookup"><span data-stu-id="1949e-123">The methods of the [**IWMDRMLicense**](iwmdrmlicense.md) interface provide data about a single license at a time.</span></span> <span data-ttu-id="1949e-124">O objeto subjacente contém uma lista de uma ou mais licenças.</span><span class="sxs-lookup"><span data-stu-id="1949e-124">The underlying object contains a list of one or more licenses.</span></span> <span data-ttu-id="1949e-125">Quando você chama esse método, a interface move suas referências internas para a próxima licença na lista.</span><span class="sxs-lookup"><span data-stu-id="1949e-125">When you call this method, the interface moves its internal references to the next license in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="1949e-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1949e-126">Requirements</span></span>



| <span data-ttu-id="1949e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="1949e-127">Requirement</span></span> | <span data-ttu-id="1949e-128">Valor</span><span class="sxs-lookup"><span data-stu-id="1949e-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1949e-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1949e-129">Header</span></span><br/>  | <dl> <span data-ttu-id="1949e-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="1949e-130"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="1949e-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1949e-131">Library</span></span><br/> | <dl> <span data-ttu-id="1949e-132"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1949e-132"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1949e-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="1949e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1949e-134">**Interface IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="1949e-134">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





