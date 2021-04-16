---
title: Método IWMDRMLicenseQuery QueryActionAllowed (wmdrmsdk. h)
description: O método QueryActionAllowed executa uma consulta no repositório de licenças local para recuperar o status da licença para uma ou mais ações de DRM que se aplicam a uma ID de chave especificada.
ms.assetid: 814c2850-c036-4c44-a64e-861e88f16fb1
keywords:
- Formato de mídia do Windows do método QueryActionAllowed
- Método QueryActionAllowed Windows Media Format, interface IWMDRMLicenseQuery
- Formato de mídia do Windows de interface IWMDRMLicenseQuery, método QueryActionAllowed
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryActionAllowed
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6564062fc9f76a840b37f6e134e960480d67a2ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775573"
---
# <a name="iwmdrmlicensequeryqueryactionallowed-method"></a><span data-ttu-id="06416-106">Método IWMDRMLicenseQuery:: QueryActionAllowed</span><span class="sxs-lookup"><span data-stu-id="06416-106">IWMDRMLicenseQuery::QueryActionAllowed method</span></span>

<span data-ttu-id="06416-107">O método **QueryActionAllowed** executa uma consulta no repositório de licenças local para recuperar o status da licença para uma ou mais ações de DRM que se aplicam a uma ID de chave especificada.</span><span class="sxs-lookup"><span data-stu-id="06416-107">The **QueryActionAllowed** method performs a query on the local license store to retrieve the license status for one or more DRM actions that apply to a specified Key ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="06416-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06416-108">Syntax</span></span>


```C++
HRESULT QueryActionAllowed(
  [in]  BSTR  bstrKID,
  [in]  BSTR  bstrMinReqIndivVersion,
  [in]  DWORD cActionsToQuery,
  [in]  BSTR  rgbstrActionsToQuery[],
  [out] DWORD rgdwQueryResult[]
);
```



## <a name="parameters"></a><span data-ttu-id="06416-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06416-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06416-110">*bstrKID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="06416-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06416-111">ID de chave para consulta.</span><span class="sxs-lookup"><span data-stu-id="06416-111">Key ID for which to query.</span></span> <span data-ttu-id="06416-112">Somente as licenças que se aplicam a essa ID de chave serão avaliadas.</span><span class="sxs-lookup"><span data-stu-id="06416-112">Only licenses that apply to this Key ID will be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="06416-113">*bstrMinReqIndivVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="06416-113">*bstrMinReqIndivVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06416-114">A versão de segurança mínima especificada no cabeçalho do arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="06416-114">The minimum security version specified in the header of the ASF file.</span></span> <span data-ttu-id="06416-115">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="06416-115">This parameter is optional.</span></span> <span data-ttu-id="06416-116">Passe **NULL** para executar a consulta sem essas informações.</span><span class="sxs-lookup"><span data-stu-id="06416-116">Pass **NULL** to perform the query without this information.</span></span>

</dd> <dt>

<span data-ttu-id="06416-117">*cActionsToQuery* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="06416-117">*cActionsToQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06416-118">O número de ações para consulta.</span><span class="sxs-lookup"><span data-stu-id="06416-118">The number of actions for which to query.</span></span> <span data-ttu-id="06416-119">Esse valor deve ser definido como o número de elementos nas matrizes passadas para os parâmetros *rgbstrActionsToQuery* e *rgdwQueryResult* .</span><span class="sxs-lookup"><span data-stu-id="06416-119">This value must be set to the number of elements in the arrays passed for the *rgbstrActionsToQuery* and *rgdwQueryResult* parameters.</span></span>

</dd> <dt>

<span data-ttu-id="06416-120">*\[ rgbstrActionsToQuery \]* \[em\]</span><span class="sxs-lookup"><span data-stu-id="06416-120">*rgbstrActionsToQuery\[\]* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06416-121">Matriz de um ou mais direitos para consulta.</span><span class="sxs-lookup"><span data-stu-id="06416-121">Array of one or more rights for which to query.</span></span> <span data-ttu-id="06416-122">Essa matriz deve conter tantos elementos quantos forem especificados por *cActionsToQuery*.</span><span class="sxs-lookup"><span data-stu-id="06416-122">This array must contain as many elements as specified by *cActionsToQuery*.</span></span> <span data-ttu-id="06416-123">Cada elemento deve ser definido como uma das seguintes constantes:</span><span class="sxs-lookup"><span data-stu-id="06416-123">Each element must be set to one of the following constants:</span></span>



| <span data-ttu-id="06416-124">Constante</span><span class="sxs-lookup"><span data-stu-id="06416-124">Constant</span></span>                                         | <span data-ttu-id="06416-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="06416-125">Description</span></span>                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="06416-126">reprodução do g \_ wszWMDRM \_ ActionAllowed \_</span><span class="sxs-lookup"><span data-stu-id="06416-126">g\_wszWMDRM\_ActionAllowed\_Playback</span></span>             | <span data-ttu-id="06416-127">Inclua para consultar o direito de reproduzir o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="06416-127">Include to query for the right to play the content.</span></span>                              |
| <span data-ttu-id="06416-128">cópia do g \_ wszWMDRM \_ ActionAllowed \_</span><span class="sxs-lookup"><span data-stu-id="06416-128">g\_wszWMDRM\_ActionAllowed\_Copy</span></span>                 | <span data-ttu-id="06416-129">Inclua para consultar o direito de copiar o conteúdo para dispositivos externos ou mídia.</span><span class="sxs-lookup"><span data-stu-id="06416-129">Include to query for the right to copy the content to external devices or media.</span></span> |
| <span data-ttu-id="06416-130">g \_ wszWMDRM \_ ActionAllowed \_ PlaylistBurn</span><span class="sxs-lookup"><span data-stu-id="06416-130">g\_wszWMDRM\_ActionAllowed\_PlaylistBurn</span></span>         | <span data-ttu-id="06416-131">Inclua para consultar o direito de copiar o conteúdo para o CD como parte de uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="06416-131">Include to query for the right to copy the content to CD as part of a playlist.</span></span>  |
| <span data-ttu-id="06416-132">g \_ wszWMDRM \_ ActionAllowed \_ CreateThumbnailImage</span><span class="sxs-lookup"><span data-stu-id="06416-132">g\_wszWMDRM\_ActionAllowed\_CreateThumbnailImage</span></span> | <span data-ttu-id="06416-133">Inclua para consultar o direito de criar uma imagem em miniatura a partir do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="06416-133">Include to query for the right to create a thumbnail image from the content.</span></span>     |
| <span data-ttu-id="06416-134">g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD</span><span class="sxs-lookup"><span data-stu-id="06416-134">g\_wszWMDRM\_ActionAllowed\_CopyToCD</span></span>             | <span data-ttu-id="06416-135">Inclua para consultar o direito de copiar o conteúdo para o CD.</span><span class="sxs-lookup"><span data-stu-id="06416-135">Include to query for the right to copy the content to CD.</span></span>                        |



 

</dd> <dt>

<span data-ttu-id="06416-136">*\[ rgdwQueryResult \]* \[out\]</span><span class="sxs-lookup"><span data-stu-id="06416-136">*rgdwQueryResult\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06416-137">Matriz de uma ou mais variáveis DWORD que recebem os resultados da consulta para os direitos especificados por *rgbstrActionsToQuery*.</span><span class="sxs-lookup"><span data-stu-id="06416-137">Array of one or more DWORD variables that receive the results of the query for the rights specified by *rgbstrActionsToQuery*.</span></span> <span data-ttu-id="06416-138">Se uma ação for permitida, o elemento correspondente será definido como zero.</span><span class="sxs-lookup"><span data-stu-id="06416-138">If an action is allowed, the corresponding element is set to zero.</span></span> <span data-ttu-id="06416-139">Se uma ação não for permitida, o elemento será definido como um ou mais valores da enumeração [**de \_ \_ resultados de \_ consulta \_ permitida da ação DRM**](drm-action-allowed-query-results.md) combinadas com o uso da operação OR.</span><span class="sxs-lookup"><span data-stu-id="06416-139">If an action is not allowed, the element is set to one or more values of the [**DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS**](drm-action-allowed-query-results.md) enumeration combined by using the bitwise OR operation.</span></span> <span data-ttu-id="06416-140">Essa matriz deve conter tantos elementos quantos forem especificados por *cActionsToQuery*.</span><span class="sxs-lookup"><span data-stu-id="06416-140">This array must contain as many elements as specified by *cActionsToQuery*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06416-141">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="06416-141">Return value</span></span>

<span data-ttu-id="06416-142">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="06416-142">The method returns an **HRESULT**.</span></span> <span data-ttu-id="06416-143">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="06416-143">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="06416-144">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="06416-144">Return code</span></span>                                                                          | <span data-ttu-id="06416-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="06416-145">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="06416-146"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="06416-146"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="06416-147">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="06416-147">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="06416-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="06416-148">Remarks</span></span>

<span data-ttu-id="06416-149">Ao consultar direitos de reprodução e cópia, você obterá resultados mais precisos primeiro definindo parâmetros ambientais.</span><span class="sxs-lookup"><span data-stu-id="06416-149">When querying for play and copy rights, you will get more accurate results by first setting environmental parameters.</span></span> <span data-ttu-id="06416-150">Use o método [**SetActionAllowedQueryParams**](iwmdrmlicensequery-setactionallowedqueryparams.md) para definir os parâmetros ambientais.</span><span class="sxs-lookup"><span data-stu-id="06416-150">Use the [**SetActionAllowedQueryParams**](iwmdrmlicensequery-setactionallowedqueryparams.md) method to set the environmental parameters.</span></span> <span data-ttu-id="06416-151">Os resultados das consultas para o direito de gravação não são afetados pelos parâmetros ambientais; Você pode usar os padrões com segurança.</span><span class="sxs-lookup"><span data-stu-id="06416-151">The results of queries for the burn right are unaffected by the environmental parameters; you can safely use the defaults.</span></span>

<span data-ttu-id="06416-152">Os resultados retornados pelo método **QueryActionAllowed** são agregados de zero ou mais licenças no repositório de licenças local.</span><span class="sxs-lookup"><span data-stu-id="06416-152">The results returned by the **QueryActionAllowed** method are aggregated from zero or more licenses in the local license store.</span></span> <span data-ttu-id="06416-153">O método pode não Pesquisar todas as licenças que se aplicam à ID da chave se encontrar um resultado habilitado.</span><span class="sxs-lookup"><span data-stu-id="06416-153">The method may not search all of the licenses that apply to the Key ID if it encounters an enabled result.</span></span>

## <a name="requirements"></a><span data-ttu-id="06416-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06416-154">Requirements</span></span>



| <span data-ttu-id="06416-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="06416-155">Requirement</span></span> | <span data-ttu-id="06416-156">Valor</span><span class="sxs-lookup"><span data-stu-id="06416-156">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06416-157">parâmetro</span><span class="sxs-lookup"><span data-stu-id="06416-157">Header</span></span><br/>  | <dl> <span data-ttu-id="06416-158"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="06416-158"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="06416-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="06416-159">Library</span></span><br/> | <dl> <span data-ttu-id="06416-160"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06416-160"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06416-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="06416-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06416-162">**Interface IWMDRMLicenseQuery**</span><span class="sxs-lookup"><span data-stu-id="06416-162">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> <dt>

[<span data-ttu-id="06416-163">**Consultando informações de direitos simples**</span><span class="sxs-lookup"><span data-stu-id="06416-163">**Querying for Simple Rights Information**</span></span>](querying-for-simple-rights-information.md)
</dt> </dl>

 

 





