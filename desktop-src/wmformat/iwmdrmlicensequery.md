---
title: Interface IWMDRMLicenseQuery
description: A interface IWMDRMLicenseQuery permite que os aplicativos consultem os direitos e o estado da licença para um arquivo protegido.
ms.assetid: 4ec8ff9f-0acb-4389-8995-65f24736491b
keywords:
- Formato de mídia do Windows da interface IWMDRMLicenseQuery
- Formato de mídia do Windows da interface IWMDRMLicenseQuery, descrito
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6463f405bf50d4d4ecb037dc542e3af0e5b7df46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641453"
---
# <a name="iwmdrmlicensequery-interface"></a><span data-ttu-id="3fc9e-105">Interface IWMDRMLicenseQuery</span><span class="sxs-lookup"><span data-stu-id="3fc9e-105">IWMDRMLicenseQuery interface</span></span>

<span data-ttu-id="3fc9e-106">A interface **IWMDRMLicenseQuery** permite que os aplicativos consultem os direitos e o estado da licença para um arquivo protegido.</span><span class="sxs-lookup"><span data-stu-id="3fc9e-106">The **IWMDRMLicenseQuery** interface enables applications to query the rights and license state for a protected file.</span></span> <span data-ttu-id="3fc9e-107">Essa interface usa a ID da chave para executar consultas no repositório de licenças local.</span><span class="sxs-lookup"><span data-stu-id="3fc9e-107">This interface uses the Key ID to perform queries on the local license store.</span></span>

<span data-ttu-id="3fc9e-108">Para obter uma instância dessa interface, chame [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="3fc9e-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="3fc9e-109">Passe **\_ IWMDRMLicenseQuery IID** como o parâmetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="3fc9e-109">Pass **IID\_IWMDRMLicenseQuery** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="3fc9e-110">Membros</span><span class="sxs-lookup"><span data-stu-id="3fc9e-110">Members</span></span>

<span data-ttu-id="3fc9e-111">A interface **IWMDRMLicenseQuery** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3fc9e-111">The **IWMDRMLicenseQuery** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3fc9e-112">**IWMDRMLicenseQuery** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3fc9e-112">**IWMDRMLicenseQuery** also has these types of members:</span></span>

-   [<span data-ttu-id="3fc9e-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="3fc9e-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3fc9e-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="3fc9e-114">Methods</span></span>

<span data-ttu-id="3fc9e-115">A interface **IWMDRMLicenseQuery** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="3fc9e-115">The **IWMDRMLicenseQuery** interface has these methods.</span></span>



| <span data-ttu-id="3fc9e-116">Método</span><span class="sxs-lookup"><span data-stu-id="3fc9e-116">Method</span></span>                                                                                | <span data-ttu-id="3fc9e-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="3fc9e-117">Description</span></span>                                                                                      |
|:--------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3fc9e-118">**QueryActionAllowed**</span><span class="sxs-lookup"><span data-stu-id="3fc9e-118">**QueryActionAllowed**</span></span>](iwmdrmlicensequery-queryactionallowed.md)                   | <span data-ttu-id="3fc9e-119">Consulta o repositório de licenças local para obter permissões para executar ações por ID de chave.</span><span class="sxs-lookup"><span data-stu-id="3fc9e-119">Queries the local license store for permissions to perform actions by Key ID.</span></span><br/>         |
| [<span data-ttu-id="3fc9e-120">**QueryLicenseState**</span><span class="sxs-lookup"><span data-stu-id="3fc9e-120">**QueryLicenseState**</span></span>](iwmdrmlicensequery-querylicensestate.md)                     | <span data-ttu-id="3fc9e-121">Consulta o repositório de licenças local para dados de estado da licença por ID de chave e direitos específicos.</span><span class="sxs-lookup"><span data-stu-id="3fc9e-121">Queries the local license store for license state data by Key ID and specific rights.</span></span><br/> |
| [<span data-ttu-id="3fc9e-122">**SetActionAllowedQueryParams**</span><span class="sxs-lookup"><span data-stu-id="3fc9e-122">**SetActionAllowedQueryParams**</span></span>](iwmdrmlicensequery-setactionallowedqueryparams.md) | <span data-ttu-id="3fc9e-123">Define os parâmetros ambientais para melhorar a precisão das consultas de licença.</span><span class="sxs-lookup"><span data-stu-id="3fc9e-123">Sets environmental parameters to improve the accuracy of license queries.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="3fc9e-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="3fc9e-124">Remarks</span></span>

<span data-ttu-id="3fc9e-125">Os métodos de **IWMDRMLicenseQuery** não fornecem informações sobre licenças individuais.</span><span class="sxs-lookup"><span data-stu-id="3fc9e-125">The methods of **IWMDRMLicenseQuery** do not provide information about individual licenses.</span></span> <span data-ttu-id="3fc9e-126">Em vez disso, os dados de licença são agregados pelo subsistema DRM antes que os resultados da consulta sejam retornados.</span><span class="sxs-lookup"><span data-stu-id="3fc9e-126">Instead, the license data is aggregated by the DRM subsystem before the query results are returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="3fc9e-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3fc9e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fc9e-128">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="3fc9e-128">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

