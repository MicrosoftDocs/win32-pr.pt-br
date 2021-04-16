---
title: Método IWMDRMLicenseQuery QueryLicenseState (wmdrmsdk. h)
description: O método QueryLicenseState consulta o repositório de licença local para obter informações de licença que se aplicam a uma ID de chave para um ou mais direitos específicos.
ms.assetid: 17f40c56-2266-4c94-9e95-a33a92ddef74
keywords:
- Formato de mídia do Windows do método QueryLicenseState
- Método QueryLicenseState Windows Media Format, interface IWMDRMLicenseQuery
- Formato de mídia do Windows de interface IWMDRMLicenseQuery, método QueryLicenseState
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryLicenseState
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e101d4ad9b5405906d05ba5e5f230326a1a3f13a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760986"
---
# <a name="iwmdrmlicensequeryquerylicensestate-method"></a><span data-ttu-id="768fe-106">Método IWMDRMLicenseQuery:: QueryLicenseState</span><span class="sxs-lookup"><span data-stu-id="768fe-106">IWMDRMLicenseQuery::QueryLicenseState method</span></span>

<span data-ttu-id="768fe-107">O método **QueryLicenseState** consulta o repositório de licença local para obter informações de licença que se aplicam a uma ID de chave para um ou mais direitos específicos.</span><span class="sxs-lookup"><span data-stu-id="768fe-107">The **QueryLicenseState** method queries the local license store for license information that applies to a Key ID for one or more specific rights.</span></span>

## <a name="syntax"></a><span data-ttu-id="768fe-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="768fe-108">Syntax</span></span>


```C++
HRESULT QueryLicenseState(
  [in]  BSTR                   bstrKID,
  [in]  DWORD                  cActionsToQuery,
  [in]  BSTR                   rgbstrActionsToQuery[],
  [out] DRM_LICENSE_STATE_DATA rgResultStateData[]
);
```



## <a name="parameters"></a><span data-ttu-id="768fe-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="768fe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="768fe-110">*bstrKID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="768fe-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="768fe-111">ID de chave para consulta.</span><span class="sxs-lookup"><span data-stu-id="768fe-111">Key ID for which to query.</span></span> <span data-ttu-id="768fe-112">Somente as licenças que se aplicam a essa ID de chave serão avaliadas.</span><span class="sxs-lookup"><span data-stu-id="768fe-112">Only licenses that apply to this Key ID will be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="768fe-113">*cActionsToQuery* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="768fe-113">*cActionsToQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="768fe-114">O número de ações para consulta.</span><span class="sxs-lookup"><span data-stu-id="768fe-114">The number of actions for which to query.</span></span> <span data-ttu-id="768fe-115">Esse valor deve ser definido como o número de elementos nas matrizes passadas para os parâmetros *rgbstrActionsToQuery* e *rgResultStateData* .</span><span class="sxs-lookup"><span data-stu-id="768fe-115">This value must be set to the number of elements in the arrays passed for the *rgbstrActionsToQuery* and *rgResultStateData* parameters.</span></span>

</dd> <dt>

<span data-ttu-id="768fe-116">*\[ rgbstrActionsToQuery \]* \[em\]</span><span class="sxs-lookup"><span data-stu-id="768fe-116">*rgbstrActionsToQuery\[\]* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="768fe-117">Matriz de um ou mais direitos para consulta.</span><span class="sxs-lookup"><span data-stu-id="768fe-117">Array of one or more rights for which to query.</span></span> <span data-ttu-id="768fe-118">Essa matriz deve conter tantos elementos quantos forem especificados por *cActionsToQuery*.</span><span class="sxs-lookup"><span data-stu-id="768fe-118">This array must contain as many elements as specified by *cActionsToQuery*.</span></span> <span data-ttu-id="768fe-119">Cada elemento deve ser definido como uma das constantes a seguir.</span><span class="sxs-lookup"><span data-stu-id="768fe-119">Each element must be set to one of the following constants.</span></span>



| <span data-ttu-id="768fe-120">Constante</span><span class="sxs-lookup"><span data-stu-id="768fe-120">Constant</span></span>                                        | <span data-ttu-id="768fe-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="768fe-121">Description</span></span>                                                                                                                                        |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="768fe-122">Backup do g \_ wszWMDRM \_ licensestate \_</span><span class="sxs-lookup"><span data-stu-id="768fe-122">g\_wszWMDRM\_LicenseState\_Backup</span></span>               | <span data-ttu-id="768fe-123">Inclua para consultar os detalhes sobre o direito de fazer backup e restaurar a licença.</span><span class="sxs-lookup"><span data-stu-id="768fe-123">Include to query for the details about the right to back up and restore the license.</span></span>                                                               |
| <span data-ttu-id="768fe-124">g \_ wszWMDRM \_ licensestate \_ CollaborativePlay</span><span class="sxs-lookup"><span data-stu-id="768fe-124">g\_wszWMDRM\_LicenseState\_CollaborativePlay</span></span>    | <span data-ttu-id="768fe-125">Inclua para consultar os detalhes sobre o direito de compartilhar o conteúdo com um grupo de usuários como parte de um cenário de reprodução colaborativa.</span><span class="sxs-lookup"><span data-stu-id="768fe-125">Include to query for the details about the right to share the content with a group of users as part of a collaborative playback scenario.</span></span>          |
| <span data-ttu-id="768fe-126">\_cópia de \_ licença g \_ wszWMDRM</span><span class="sxs-lookup"><span data-stu-id="768fe-126">g\_wszWMDRM\_LicenseState\_Copy</span></span>                 | <span data-ttu-id="768fe-127">Inclua para consultar os detalhes sobre o direito de copiar o conteúdo para dispositivos ou mídias externos.</span><span class="sxs-lookup"><span data-stu-id="768fe-127">Include to query for the details about the right to copy the content to external devices or media.</span></span>                                                 |
| <span data-ttu-id="768fe-128">g \_ wszWMDRM \_ licensestate \_ CopyToCD</span><span class="sxs-lookup"><span data-stu-id="768fe-128">g\_wszWMDRM\_LicenseState\_CopyToCD</span></span>             | <span data-ttu-id="768fe-129">Inclua para consultar os detalhes sobre o direito de copiar o conteúdo para o CD.</span><span class="sxs-lookup"><span data-stu-id="768fe-129">Include to query for the details about the right to copy the content to CD.</span></span>                                                                        |
| <span data-ttu-id="768fe-130">g \_ wszWMDRM \_ licensestate \_ CopyToNonSDMIDevice</span><span class="sxs-lookup"><span data-stu-id="768fe-130">g\_wszWMDRM\_LicenseState\_CopyToNonSDMIDevice</span></span>  | <span data-ttu-id="768fe-131">Inclua para consultar os detalhes sobre o direito de copiar o conteúdo para um dispositivo que não dá suporte à SDMI (Secure Digital Media Initiative).</span><span class="sxs-lookup"><span data-stu-id="768fe-131">Include to query for the details about the right to copy the content to a device that does not support the secure digital media initiative (SDMI).</span></span> |
| <span data-ttu-id="768fe-132">g \_ wszWMDRM \_ licensestate \_ CopyToSDMIDevice</span><span class="sxs-lookup"><span data-stu-id="768fe-132">g\_wszWMDRM\_LicenseState\_CopyToSDMIDevice</span></span>     | <span data-ttu-id="768fe-133">Inclua para consultar os detalhes sobre o direito de copiar o conteúdo para um dispositivo que dá suporte a SDMI.</span><span class="sxs-lookup"><span data-stu-id="768fe-133">Include to query for the details about the right to copy the content to a device that supports the SDMI.</span></span>                                           |
| <span data-ttu-id="768fe-134">g \_ wszWMDRM \_ licensestate \_ CreateThumbnailImage</span><span class="sxs-lookup"><span data-stu-id="768fe-134">g\_wszWMDRM\_LicenseState\_CreateThumbnailImage</span></span> | <span data-ttu-id="768fe-135">Inclua para consultar os detalhes sobre o direito de criar uma imagem em miniatura a partir do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="768fe-135">Include to query for the details about the right to create a thumbnail image from the content.</span></span>                                                     |
| <span data-ttu-id="768fe-136">wszWMDRM de licença do g para \_ \_ \_ reprodução</span><span class="sxs-lookup"><span data-stu-id="768fe-136">g\_wszWMDRM\_LicenseState\_Playback</span></span>             | <span data-ttu-id="768fe-137">Inclua para consultar os detalhes sobre o direito de reproduzir o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="768fe-137">Include to query for the details about the right to play the content.</span></span>                                                                              |
| <span data-ttu-id="768fe-138">g \_ wszWMDRM \_ licensestate \_ PlaylistBurn</span><span class="sxs-lookup"><span data-stu-id="768fe-138">g\_wszWMDRM\_LicenseState\_PlaylistBurn</span></span>         | <span data-ttu-id="768fe-139">Inclua para consultar os detalhes sobre o direito de copiar o conteúdo para o CD como parte de uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="768fe-139">Include to query for the details about the right to copy the content to CD as part of a playlist.</span></span>                                                  |



 

</dd> <dt>

<span data-ttu-id="768fe-140">*\[ rgResultStateData \]* \[out\]</span><span class="sxs-lookup"><span data-stu-id="768fe-140">*rgResultStateData\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="768fe-141">Matriz de uma ou mais estruturas de dados de estado de licença do DRM que recebem as informações de estado da licença que se aplicam à direita no elemento correspondente do parâmetro *rgbstrActionsToQuery* . [**\_ \_ \_**](drmdrm-license-state-data.md)</span><span class="sxs-lookup"><span data-stu-id="768fe-141">Array of one or more [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structures that receive the license state information that applies to the right in the corresponding element of the *rgbstrActionsToQuery* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="768fe-142">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="768fe-142">Return value</span></span>

<span data-ttu-id="768fe-143">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="768fe-143">The method returns an **HRESULT**.</span></span> <span data-ttu-id="768fe-144">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="768fe-144">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="768fe-145">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="768fe-145">Return code</span></span>                                                                          | <span data-ttu-id="768fe-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="768fe-146">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="768fe-147"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="768fe-147"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="768fe-148">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="768fe-148">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="768fe-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="768fe-149">Remarks</span></span>

<span data-ttu-id="768fe-150">Todas as licenças que se aplicam à ID de chave especificada serão pesquisadas e avaliadas.</span><span class="sxs-lookup"><span data-stu-id="768fe-150">All licenses that apply to the specified Key ID will be searched and evaluated.</span></span> <span data-ttu-id="768fe-151">Os resultados são agregados, portanto, cada estrutura de dados de estado de licença do DRM pode conter informações de várias licenças. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="768fe-151">The results are aggregated, so each **DRM\_LICENSE\_STATE\_DATA** structure may contain information from multiple licenses.</span></span>

## <a name="requirements"></a><span data-ttu-id="768fe-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="768fe-152">Requirements</span></span>



| <span data-ttu-id="768fe-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="768fe-153">Requirement</span></span> | <span data-ttu-id="768fe-154">Valor</span><span class="sxs-lookup"><span data-stu-id="768fe-154">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="768fe-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="768fe-155">Header</span></span><br/>  | <dl> <span data-ttu-id="768fe-156"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="768fe-156"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="768fe-157">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="768fe-157">Library</span></span><br/> | <dl> <span data-ttu-id="768fe-158"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="768fe-158"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="768fe-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="768fe-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="768fe-160">**Interface IWMDRMLicenseQuery**</span><span class="sxs-lookup"><span data-stu-id="768fe-160">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> </dl>

 

 





