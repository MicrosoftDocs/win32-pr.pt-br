---
title: Método IWMDRMLicenseManagement CreateLicenseEnumeration (wmdrmsdk. h)
description: O método CreateLicenseEnumeration cria um objeto de enumerador de licença com o qual você pode obter informações sobre licenças no repositório de licenças local.
ms.assetid: 48da1ef4-89bc-4cba-b5c9-0e202eb2986f
keywords:
- Formato de mídia do Windows do método CreateLicenseEnumeration
- Método CreateLicenseEnumeration Windows Media Format, interface IWMDRMLicenseManagement
- Formato de mídia do Windows de interface IWMDRMLicenseManagement, método CreateLicenseEnumeration
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseEnumeration
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bb75d21cc640da39c3679ac118ead629b24f719
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787682"
---
# <a name="iwmdrmlicensemanagementcreatelicenseenumeration-method"></a><span data-ttu-id="fb1fc-106">Método IWMDRMLicenseManagement:: CreateLicenseEnumeration</span><span class="sxs-lookup"><span data-stu-id="fb1fc-106">IWMDRMLicenseManagement::CreateLicenseEnumeration method</span></span>

<span data-ttu-id="fb1fc-107">O método **CreateLicenseEnumeration** cria um objeto de enumerador de licença com o qual você pode obter informações sobre licenças no repositório de licenças local.</span><span class="sxs-lookup"><span data-stu-id="fb1fc-107">The **CreateLicenseEnumeration** method creates a license enumerator object with which you can get information about licenses in the local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb1fc-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb1fc-108">Syntax</span></span>


```C++
HRESULT CreateLicenseEnumeration(
  [in]  WMDRM_LICENSE_FILTER *pLicenseFilter,
  [out] IWMDRMLicense        **pEnumerator
);
```



## <a name="parameters"></a><span data-ttu-id="fb1fc-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb1fc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb1fc-110">*pLicenseFilter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fb1fc-110">*pLicenseFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb1fc-111">Ponteiro para uma estrutura de [**\_ \_ filtro de licença WMDRM**](wmdrm-license-filter.md) que contém os parâmetros de filtragem para a lista de licenças no enumerador.</span><span class="sxs-lookup"><span data-stu-id="fb1fc-111">Pointer to a [**WMDRM\_LICENSE\_FILTER**](wmdrm-license-filter.md) structure containing the filtering parameters for the list of licenses in the enumerator.</span></span>

</dd> <dt>

<span data-ttu-id="fb1fc-112">*pEnumerator* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fb1fc-112">*pEnumerator* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb1fc-113">Ponteiro que recebe o endereço da interface [**IWMDRMLicense**](iwmdrmlicense.md) do objeto enumerador de licença recém-criado.</span><span class="sxs-lookup"><span data-stu-id="fb1fc-113">Pointer that receives the address of the [**IWMDRMLicense**](iwmdrmlicense.md) interface of the newly created license enumerator object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb1fc-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fb1fc-114">Return value</span></span>

<span data-ttu-id="fb1fc-115">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fb1fc-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="fb1fc-116">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="fb1fc-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="fb1fc-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fb1fc-117">Return code</span></span>                                                                                                | <span data-ttu-id="fb1fc-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb1fc-118">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="fb1fc-119"><dt>**RIV do NS \_ E \_ DRM \_ \_ muito \_ pequeno**</dt></span><span class="sxs-lookup"><span data-stu-id="fb1fc-119"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="fb1fc-120">Uma lista de revogação de conteúdo atualizada é necessária.</span><span class="sxs-lookup"><span data-stu-id="fb1fc-120">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="fb1fc-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fb1fc-121"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="fb1fc-122">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="fb1fc-122">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="fb1fc-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb1fc-123">Remarks</span></span>

<span data-ttu-id="fb1fc-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="fb1fc-124">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb1fc-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb1fc-125">Requirements</span></span>



| <span data-ttu-id="fb1fc-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb1fc-126">Requirement</span></span> | <span data-ttu-id="fb1fc-127">Valor</span><span class="sxs-lookup"><span data-stu-id="fb1fc-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb1fc-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb1fc-128">Header</span></span><br/>  | <dl> <span data-ttu-id="fb1fc-129"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb1fc-129"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="fb1fc-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb1fc-130">Library</span></span><br/> | <dl> <span data-ttu-id="fb1fc-131"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb1fc-131"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb1fc-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb1fc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb1fc-133">**Enumerando licenças no repositório de licenças local**</span><span class="sxs-lookup"><span data-stu-id="fb1fc-133">**Enumerating Licenses in the Local License Store**</span></span>](enumerating-licenses-in-the-local-license-store.md)
</dt> <dt>

[<span data-ttu-id="fb1fc-134">**Interface IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="fb1fc-134">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





