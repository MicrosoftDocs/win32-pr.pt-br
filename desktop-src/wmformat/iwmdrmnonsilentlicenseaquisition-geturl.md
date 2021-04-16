---
title: Método GetURL IWMDRMNonSilentLicenseAquisition (wmdrmsdk. h)
description: O método GetURL recupera a URL para a qual o desafio de licença deve ser lançado.
ms.assetid: f65f1984-74bc-4cd0-957e-930aa6a6f6a5
keywords:
- Método GetURL Windows Media Format
- Método GetURL Windows Media Format, interface IWMDRMNonSilentLicenseAquisition
- Formato de mídia do Windows da interface IWMDRMNonSilentLicenseAquisition, método GetURL
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetURL
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79212d19d7dbf4a66e2b72dcbdeba9262a9aeddd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779504"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongeturl-method"></a><span data-ttu-id="5f62c-106">Método IWMDRMNonSilentLicenseAquisition:: GetURL</span><span class="sxs-lookup"><span data-stu-id="5f62c-106">IWMDRMNonSilentLicenseAquisition::GetURL method</span></span>

<span data-ttu-id="5f62c-107">O método **getURL** recupera a URL para a qual o desafio de licença deve ser lançado.</span><span class="sxs-lookup"><span data-stu-id="5f62c-107">The **GetURL** method retrieves the URL to which the license challenge should be posted.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f62c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f62c-108">Syntax</span></span>


```C++
HRESULT GetURL(
  [out] BSTR *pbstrURL
);
```



## <a name="parameters"></a><span data-ttu-id="5f62c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f62c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f62c-110">*pbstrURL* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5f62c-110">*pbstrURL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f62c-111">Endereço de uma variável que recebe a URL.</span><span class="sxs-lookup"><span data-stu-id="5f62c-111">Address of a variable that receives the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f62c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5f62c-112">Return value</span></span>

<span data-ttu-id="5f62c-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5f62c-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5f62c-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5f62c-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5f62c-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5f62c-115">Return code</span></span>                                                                          | <span data-ttu-id="5f62c-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f62c-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5f62c-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5f62c-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5f62c-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="5f62c-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5f62c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f62c-119">Remarks</span></span>

<span data-ttu-id="5f62c-120">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="5f62c-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f62c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f62c-121">Requirements</span></span>



| <span data-ttu-id="5f62c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f62c-122">Requirement</span></span> | <span data-ttu-id="5f62c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5f62c-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f62c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f62c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5f62c-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f62c-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="5f62c-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5f62c-126">Library</span></span><br/> | <dl> <span data-ttu-id="5f62c-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f62c-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f62c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f62c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f62c-129">**Interface IWMDRMNonSilentLicenseAquisition**</span><span class="sxs-lookup"><span data-stu-id="5f62c-129">**IWMDRMNonSilentLicenseAquisition Interface**</span></span>](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 





