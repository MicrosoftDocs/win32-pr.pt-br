---
title: Método IWMDRMLicenseManagement StoreLicense (wmdrmsdk. h)
description: O método StoreLicense inclui uma licença que foi gerada fora do subsistema DRM local no repositório de licenças local.
ms.assetid: 2190ff8c-8969-4f03-9f90-331bff8f4da2
keywords:
- Formato de mídia do Windows do método StoreLicense
- Método StoreLicense Windows Media Format, interface IWMDRMLicenseManagement
- Formato de mídia do Windows de interface IWMDRMLicenseManagement, método StoreLicense
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.StoreLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcfde6347e099ceb9fc168e1183cbd62c90f9b9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105798174"
---
# <a name="iwmdrmlicensemanagementstorelicense-method"></a><span data-ttu-id="c1bbb-106">Método IWMDRMLicenseManagement:: StoreLicense</span><span class="sxs-lookup"><span data-stu-id="c1bbb-106">IWMDRMLicenseManagement::StoreLicense method</span></span>

<span data-ttu-id="c1bbb-107">O método **StoreLicense** inclui uma licença que foi gerada fora do subsistema DRM local no repositório de licenças local.</span><span class="sxs-lookup"><span data-stu-id="c1bbb-107">The **StoreLicense** method includes a license that was generated outside of the local DRM subsystem in the local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1bbb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1bbb-108">Syntax</span></span>


```C++
HRESULT StoreLicense(
  [in] BSTR bstrLicenseResponse
);
```



## <a name="parameters"></a><span data-ttu-id="c1bbb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1bbb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1bbb-110">*bstrLicenseResponse* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c1bbb-110">*bstrLicenseResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1bbb-111">Cadeia de caracteres de resposta de licença a ser decodificada e adicionada ao repositório de licenças local.</span><span class="sxs-lookup"><span data-stu-id="c1bbb-111">License response string to be decoded and added to the local license store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1bbb-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c1bbb-112">Return value</span></span>

<span data-ttu-id="c1bbb-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c1bbb-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c1bbb-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c1bbb-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c1bbb-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c1bbb-115">Return code</span></span>                                                                          | <span data-ttu-id="c1bbb-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1bbb-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c1bbb-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c1bbb-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c1bbb-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c1bbb-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c1bbb-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1bbb-119">Remarks</span></span>

<span data-ttu-id="c1bbb-120">Você pode usar esse método para adicionar licenças do XMR que você criou ao armazenamento de licença local.</span><span class="sxs-lookup"><span data-stu-id="c1bbb-120">You can use this method to add XMR licenses that you have created to the local license store.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1bbb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1bbb-121">Requirements</span></span>



| <span data-ttu-id="c1bbb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1bbb-122">Requirement</span></span> | <span data-ttu-id="c1bbb-123">Valor</span><span class="sxs-lookup"><span data-stu-id="c1bbb-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1bbb-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c1bbb-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c1bbb-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1bbb-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="c1bbb-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c1bbb-126">Library</span></span><br/> | <dl> <span data-ttu-id="c1bbb-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1bbb-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1bbb-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1bbb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1bbb-129">**Interface IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="c1bbb-129">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





