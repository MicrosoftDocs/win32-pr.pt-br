---
description: Define ou recupera o local de pesquisa do Active Directory.
ms.assetid: 43320799-1c01-4e09-bed9-f3576baadcce
title: Propriedade Settings. ActiveDirectorySearchLocation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.ActiveDirectorySearchLocation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d218b3d589b76980d468395a39452613aa57ada5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753395"
---
# <a name="settingsactivedirectorysearchlocation-property"></a><span data-ttu-id="9287a-103">Propriedade Settings. ActiveDirectorySearchLocation</span><span class="sxs-lookup"><span data-stu-id="9287a-103">Settings.ActiveDirectorySearchLocation property</span></span>

<span data-ttu-id="9287a-104">\[A propriedade **ActiveDirectorySearchLocation** está disponível para uso nos sistemas operacionais especificados na seção requisitos.\]</span><span class="sxs-lookup"><span data-stu-id="9287a-104">\[The **ActiveDirectorySearchLocation** property is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="9287a-105">A propriedade **ActiveDirectorySearchLocation** define ou recupera o local de pesquisa Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9287a-105">The **ActiveDirectorySearchLocation** property sets or retrieves the Active Directory search location.</span></span>

## <a name="syntax"></a><span data-ttu-id="9287a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9287a-106">Syntax</span></span>


```VB
Settings.ActiveDirectorySearchLocation As CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
```



## <a name="property-value"></a><span data-ttu-id="9287a-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="9287a-107">Property value</span></span>

<span data-ttu-id="9287a-108">Um valor da enumeração [**de \_ \_ local de \_ pesquisa \_ do Active Directory CAPICOM**](capicom-active-directory-search-location.md) que especifica o local de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9287a-108">A value of the [**CAPICOM\_ACTIVE\_DIRECTORY\_SEARCH\_LOCATION**](capicom-active-directory-search-location.md) enumeration that specifies the search location.</span></span> <span data-ttu-id="9287a-109">O valor padrão é capicote \_ Search \_ any.</span><span class="sxs-lookup"><span data-stu-id="9287a-109">The default value is CAPICOM\_SEARCH\_ANY.</span></span> <span data-ttu-id="9287a-110">A tabela a seguir mostra os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="9287a-110">The following table shows the possible values.</span></span>



| <span data-ttu-id="9287a-111">Valor</span><span class="sxs-lookup"><span data-stu-id="9287a-111">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="9287a-112">Significado</span><span class="sxs-lookup"><span data-stu-id="9287a-112">Meaning</span></span>                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="CAPICOM_SEARCH_ANY"></span><span id="capicom_search_any"></span><dl> <span data-ttu-id="9287a-113"><dt>**capicote \_ Search \_ any**</dt></span><span class="sxs-lookup"><span data-stu-id="9287a-113"><dt>**CAPICOM\_SEARCH\_ANY**</dt></span></span> </dl>                                   | <span data-ttu-id="9287a-114">Pesquisar todos os locais disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9287a-114">Search all available locations.</span></span><br/> |
| <span id="CAPICOM_SEARCH_DEFAULT_DOMAIN"></span><span id="capicom_search_default_domain"></span><dl> <span data-ttu-id="9287a-115"><dt>**CAPICOM de \_ pesquisa de \_ \_ domínio padrão**</dt></span><span class="sxs-lookup"><span data-stu-id="9287a-115"><dt>**CAPICOM\_SEARCH\_DEFAULT\_DOMAIN**</dt></span></span> </dl> | <span data-ttu-id="9287a-116">Pesquise somente o domínio padrão.</span><span class="sxs-lookup"><span data-stu-id="9287a-116">Search only the default domain.</span></span><br/> |
| <span id="CAPICOM_SEARCH_GLOBAL_CATALOG"></span><span id="capicom_search_global_catalog"></span><dl> <span data-ttu-id="9287a-117"><dt>**CAPICOM de \_ pesquisa do \_ \_ catálogo global**</dt></span><span class="sxs-lookup"><span data-stu-id="9287a-117"><dt>**CAPICOM\_SEARCH\_GLOBAL\_CATALOG**</dt></span></span> </dl> | <span data-ttu-id="9287a-118">Pesquise somente o catálogo global.</span><span class="sxs-lookup"><span data-stu-id="9287a-118">Search only the global catalog.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9287a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9287a-119">Requirements</span></span>



| <span data-ttu-id="9287a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9287a-120">Requirement</span></span> | <span data-ttu-id="9287a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="9287a-121">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9287a-122">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="9287a-122">Redistributable</span></span><br/> | <span data-ttu-id="9287a-123">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="9287a-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9287a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="9287a-124">DLL</span></span><br/>             | <dl> <span data-ttu-id="9287a-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9287a-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9287a-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="9287a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9287a-127">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="9287a-127">**Settings**</span></span>](settings.md)
</dt> </dl>

 

 




