---
title: Método IWMDRMLicenseManagement DeleteLicense (wmdrmsdk. h)
description: O método DeleteLicense remove uma licença do armazenamento de licença local temporário.
ms.assetid: 0aa7143a-845a-41a4-8b3c-a04c68ee280a
keywords:
- Formato de mídia do Windows do método DeleteLicense
- Método DeleteLicense Windows Media Format, interface IWMDRMLicenseManagement
- Formato de mídia do Windows de interface IWMDRMLicenseManagement, método DeleteLicense
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.DeleteLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d5b52f6277459f147285f46fc791669e56061a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812300"
---
# <a name="iwmdrmlicensemanagementdeletelicense-method"></a><span data-ttu-id="28934-106">IWMDRMLicenseManagement: método eleteLicense de:D</span><span class="sxs-lookup"><span data-stu-id="28934-106">IWMDRMLicenseManagement::DeleteLicense method</span></span>

<span data-ttu-id="28934-107">O método **DeleteLicense** remove uma licença do armazenamento de licença local temporário.</span><span class="sxs-lookup"><span data-stu-id="28934-107">The **DeleteLicense** method removes a license from the temporary local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="28934-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28934-108">Syntax</span></span>


```C++
HRESULT DeleteLicense(
  [in] BSTR  bstrKID,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="28934-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28934-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28934-110">*bstrKID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="28934-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28934-111">ID da chave (KID) da licença a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="28934-111">Key ID (KID) of the license to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="28934-112">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="28934-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28934-113">Sinalizadores de opção de exclusão de licença.</span><span class="sxs-lookup"><span data-stu-id="28934-113">License deletion option flags.</span></span> <span data-ttu-id="28934-114">Defina como um dos valores na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="28934-114">Set to one of the values in the following table.</span></span>



| <span data-ttu-id="28934-115">Valor</span><span class="sxs-lookup"><span data-stu-id="28934-115">Value</span></span>                                    | <span data-ttu-id="28934-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="28934-116">Description</span></span>                                                                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28934-117">licença de exclusão de WMDRM \_ \_ \_ imediatamente</span><span class="sxs-lookup"><span data-stu-id="28934-117">WMDRM\_DELETE\_LICENSE\_IMMEDIATELY</span></span>      | <span data-ttu-id="28934-118">Especifica que a licença deve ser removida do repositório imediatamente.</span><span class="sxs-lookup"><span data-stu-id="28934-118">Specifies that the license should be removed from the store immediately.</span></span>                                                                                                                              |
| <span data-ttu-id="28934-119">\_exclusão \_ \_ \_ de marca de licença do WMDRM para \_ limpeza</span><span class="sxs-lookup"><span data-stu-id="28934-119">WMDRM\_DELETE\_LICENSE\_MARK\_FOR\_PURGE</span></span> | <span data-ttu-id="28934-120">Especifica que a licença deve ser marcada para exclusão, mas não deve ser removida da loja até que o método [**CleanLicenseStore**](iwmdrmlicensemanagement-cleanlicensestore.md) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="28934-120">Specifies that the license should be marked for deletion, but should not be removed from the store until the [**CleanLicenseStore**](iwmdrmlicensemanagement-cleanlicensestore.md) method is called.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28934-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="28934-121">Return value</span></span>

<span data-ttu-id="28934-122">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="28934-122">The method returns an **HRESULT**.</span></span> <span data-ttu-id="28934-123">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="28934-123">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="28934-124">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="28934-124">Return code</span></span>                                                                                            | <span data-ttu-id="28934-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="28934-125">Description</span></span>                                                                                                         |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="28934-126"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="28934-126"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="28934-127">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="28934-127">The method succeeded.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="28934-128"><dt>**DRM \_ E \_ LICENSENOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="28934-128"><dt>**DRM\_E\_LICENSENOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="28934-129">A licença especificada não existe no repositório.</span><span class="sxs-lookup"><span data-stu-id="28934-129">The specified license does not exist in the store.</span></span><br/> <span data-ttu-id="28934-130">- OU –</span><span class="sxs-lookup"><span data-stu-id="28934-130">- OR -</span></span><br/> <span data-ttu-id="28934-131">O repositório não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="28934-131">The store was not found.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="28934-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="28934-132">Remarks</span></span>

<span data-ttu-id="28934-133">Para excluir licenças do armazenamento de licença local permanente, você deve usar a revogação de licença.</span><span class="sxs-lookup"><span data-stu-id="28934-133">To delete licenses from the permanent local license store, you must use license revocation.</span></span>

## <a name="requirements"></a><span data-ttu-id="28934-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28934-134">Requirements</span></span>



| <span data-ttu-id="28934-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="28934-135">Requirement</span></span> | <span data-ttu-id="28934-136">Valor</span><span class="sxs-lookup"><span data-stu-id="28934-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28934-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="28934-137">Header</span></span><br/>  | <dl> <span data-ttu-id="28934-138"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="28934-138"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="28934-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="28934-139">Library</span></span><br/> | <dl> <span data-ttu-id="28934-140"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28934-140"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28934-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="28934-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28934-142">**Interface IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="28934-142">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





