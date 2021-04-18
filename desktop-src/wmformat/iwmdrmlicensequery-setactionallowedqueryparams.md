---
title: Método IWMDRMLicenseQuery SetActionAllowedQueryParams (wmdrmsdk. h)
description: O método SetActionAllowedQueryParams define informações específicas do ambiente para obter resultados de consulta mais precisos ao usar o método QueryActionAllowed.
ms.assetid: 1c8f9d4e-999d-4d7c-87fd-9d30e432350c
keywords:
- Formato de mídia do Windows do método SetActionAllowedQueryParams
- Método SetActionAllowedQueryParams Windows Media Format, interface IWMDRMLicenseQuery
- Formato de mídia do Windows de interface IWMDRMLicenseQuery, método SetActionAllowedQueryParams
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.SetActionAllowedQueryParams
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a83a28c4d9f3758b711c43ddd83a509c58f8ea8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812792"
---
# <a name="iwmdrmlicensequerysetactionallowedqueryparams-method"></a><span data-ttu-id="9a56f-106">Método IWMDRMLicenseQuery:: SetActionAllowedQueryParams</span><span class="sxs-lookup"><span data-stu-id="9a56f-106">IWMDRMLicenseQuery::SetActionAllowedQueryParams method</span></span>

<span data-ttu-id="9a56f-107">O método **SetActionAllowedQueryParams** define informações específicas do ambiente para obter resultados de consulta mais precisos ao usar o método [**QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) .</span><span class="sxs-lookup"><span data-stu-id="9a56f-107">The **SetActionAllowedQueryParams** method sets environment-specific information for more accurate query results when using the [**QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a56f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a56f-108">Syntax</span></span>


```C++
HRESULT SetActionAllowedQueryParams(
  [in] BOOL  fIsMF,
  [in] DWORD dwAppSecLevel,
  [in] BOOL  fHasSerialNumber,
  [in] BSTR  bstrDeviceCert
);
```



## <a name="parameters"></a><span data-ttu-id="9a56f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a56f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a56f-110">*fIsMF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9a56f-110">*fIsMF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a56f-111">Especifica se o conteúdo será renderizado usando os objetos do SDK do Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="9a56f-111">Specifies whether the content will be rendered by using the objects of the Microsoft Media Foundation SDK.</span></span> <span data-ttu-id="9a56f-112">**False** indica a renderização pelos objetos do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="9a56f-112">**FALSE** indicates rendering by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="9a56f-113">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="9a56f-113">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="9a56f-114">*dwAppSecLevel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9a56f-114">*dwAppSecLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a56f-115">Nível de segurança do aplicativo de consulta.</span><span class="sxs-lookup"><span data-stu-id="9a56f-115">Security level of the querying application.</span></span> <span data-ttu-id="9a56f-116">Esse valor só será importante se os objetos do Windows Media Format SDK forem usados, caso em que *fIsMF* deve ser definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="9a56f-116">This value is only important if the objects of the Windows Media Format SDK will be used, in which case *fIsMF* should be set to **FALSE**.</span></span> <span data-ttu-id="9a56f-117">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="9a56f-117">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="9a56f-118">*fHasSerialNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9a56f-118">*fHasSerialNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a56f-119">Especifica se o dispositivo de destino para uma operação de cópia tem um número de série.</span><span class="sxs-lookup"><span data-stu-id="9a56f-119">Specifies whether the target device for a copy operation has a serial number.</span></span> <span data-ttu-id="9a56f-120">Esse parâmetro é opcional e só se aplica a consultas para operações de cópia.</span><span class="sxs-lookup"><span data-stu-id="9a56f-120">This parameter is optional and only applies to queries for copy operations.</span></span>

</dd> <dt>

<span data-ttu-id="9a56f-121">*bstrDeviceCert* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9a56f-121">*bstrDeviceCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a56f-122">Certificado de dispositivo do dispositivo de destino ao usar o DRM do Windows Media para dispositivos portáteis.</span><span class="sxs-lookup"><span data-stu-id="9a56f-122">Device certificate of the target device when using Windows Media DRM for Portable Devices.</span></span> <span data-ttu-id="9a56f-123">Esse parâmetro é opcional e só se aplica a consultas para operações de cópia.</span><span class="sxs-lookup"><span data-stu-id="9a56f-123">This parameter is optional and only applies to queries for copy operations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a56f-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9a56f-124">Return value</span></span>

<span data-ttu-id="9a56f-125">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9a56f-125">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9a56f-126">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9a56f-126">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9a56f-127">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9a56f-127">Return code</span></span>                                                                          | <span data-ttu-id="9a56f-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a56f-128">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="9a56f-129"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9a56f-129"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9a56f-130">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="9a56f-130">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9a56f-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a56f-131">Remarks</span></span>

<span data-ttu-id="9a56f-132">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="9a56f-132">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a56f-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a56f-133">Requirements</span></span>



| <span data-ttu-id="9a56f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a56f-134">Requirement</span></span> | <span data-ttu-id="9a56f-135">Valor</span><span class="sxs-lookup"><span data-stu-id="9a56f-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a56f-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9a56f-136">Header</span></span><br/>  | <dl> <span data-ttu-id="9a56f-137"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a56f-137"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="9a56f-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9a56f-138">Library</span></span><br/> | <dl> <span data-ttu-id="9a56f-139"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a56f-139"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a56f-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a56f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a56f-141">**Interface IWMDRMLicenseQuery**</span><span class="sxs-lookup"><span data-stu-id="9a56f-141">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> <dt>

[<span data-ttu-id="9a56f-142">**Consultando informações detalhadas sobre direitos**</span><span class="sxs-lookup"><span data-stu-id="9a56f-142">**Querying for Detailed Rights Information**</span></span>](querying-for-detailed-rights-information.md)
</dt> </dl>

 

 





