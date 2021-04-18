---
title: Método getchallenge IWMDRMNonSilentLicenseAquisition (wmdrmsdk. h)
description: O método getchallenge recupera o desafio de licença que deve ser postado no servidor de licença.
ms.assetid: f2ff8484-8fe2-4c74-82c1-9bc14f8197e0
keywords:
- Método getchallenge formato de mídia do Windows
- Método getchallenge Windows Media Format, interface IWMDRMNonSilentLicenseAquisition
- IWMDRMNonSilentLicenseAquisition interface formato Windows Media, método getchallenge
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetChallenge
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa0dc63c63e5d7a62c06cbe791d9a5e5e8d09c5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789912"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongetchallenge-method"></a><span data-ttu-id="5a3ea-106">Método IWMDRMNonSilentLicenseAquisition:: getchallenge</span><span class="sxs-lookup"><span data-stu-id="5a3ea-106">IWMDRMNonSilentLicenseAquisition::GetChallenge method</span></span>

<span data-ttu-id="5a3ea-107">O método **getchallenge** recupera o desafio de licença que deve ser postado no servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="5a3ea-107">The **GetChallenge** method retrieves the license challenge that should be posted to the license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a3ea-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a3ea-108">Syntax</span></span>


```C++
HRESULT GetChallenge(
  [out] BSTR *pbstrChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="5a3ea-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a3ea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a3ea-110">*pbstrChallenge* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5a3ea-110">*pbstrChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a3ea-111">Endereço de uma variável que recebe o desafio de licença.</span><span class="sxs-lookup"><span data-stu-id="5a3ea-111">Address of a variable that receives the license challenge.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a3ea-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5a3ea-112">Return value</span></span>

<span data-ttu-id="5a3ea-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5a3ea-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5a3ea-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5a3ea-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5a3ea-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5a3ea-115">Return code</span></span>                                                                          | <span data-ttu-id="5a3ea-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a3ea-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5a3ea-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5a3ea-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5a3ea-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="5a3ea-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5a3ea-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a3ea-119">Remarks</span></span>

<span data-ttu-id="5a3ea-120">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="5a3ea-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a3ea-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a3ea-121">Requirements</span></span>



| <span data-ttu-id="5a3ea-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a3ea-122">Requirement</span></span> | <span data-ttu-id="5a3ea-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5a3ea-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a3ea-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5a3ea-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5a3ea-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a3ea-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a3ea-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5a3ea-126">Library</span></span><br/> | <dl> <span data-ttu-id="5a3ea-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a3ea-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a3ea-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a3ea-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a3ea-129">**Interface IWMDRMNonSilentLicenseAquisition**</span><span class="sxs-lookup"><span data-stu-id="5a3ea-129">**IWMDRMNonSilentLicenseAquisition Interface**</span></span>](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 





