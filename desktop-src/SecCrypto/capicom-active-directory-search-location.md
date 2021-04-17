---
description: Indica o local a ser procurado em um repositório de certificados Active Directory.
ms.assetid: 56b9695e-7ab9-405b-9cae-d78c43071186
title: Enumeração de CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: cd630bdc0c09a6bb57a9163ec972451011f3e826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748398"
---
# <a name="capicom_active_directory_search_location-enumeration"></a><span data-ttu-id="b9cae-103">\_ \_ \_ Enumeração do local de pesquisa do Active Directory CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="b9cae-103">CAPICOM\_ACTIVE\_DIRECTORY\_SEARCH\_LOCATION enumeration</span></span>

<span data-ttu-id="b9cae-104">O tipo de enumeração do **local de \_ pesquisa do Active \_ Directory \_ \_ CAPICOM** indica o local a ser procurado em um [*repositório de certificados*](../secgloss/c-gly.md)Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b9cae-104">The **CAPICOM\_ACTIVE\_DIRECTORY\_SEARCH\_LOCATION** enumeration type indicates the location to be searched for an Active Directory [*certificate store*](../secgloss/c-gly.md).</span></span>

## <a name="members"></a><span data-ttu-id="b9cae-105">Membros</span><span class="sxs-lookup"><span data-stu-id="b9cae-105">Members</span></span>



| <span data-ttu-id="b9cae-106">Membro</span><span class="sxs-lookup"><span data-stu-id="b9cae-106">Member</span></span>                               | <span data-ttu-id="b9cae-107">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="b9cae-107">Description</span></span>                                  | <span data-ttu-id="b9cae-108">Valor</span><span class="sxs-lookup"><span data-stu-id="b9cae-108">Value</span></span> |
|--------------------------------------|----------------------------------------------|-------|
| <span data-ttu-id="b9cae-109">**capicote \_ Search \_ any**</span><span class="sxs-lookup"><span data-stu-id="b9cae-109">**CAPICOM\_SEARCH\_ANY**</span></span>             | <span data-ttu-id="b9cae-110">Pesquisa todos os locais disponíveis.</span><span class="sxs-lookup"><span data-stu-id="b9cae-110">Searches all available locations.</span></span><br/> | <span data-ttu-id="b9cae-111">0</span><span class="sxs-lookup"><span data-stu-id="b9cae-111">0</span></span>     |
| <span data-ttu-id="b9cae-112">**CAPICOM de \_ pesquisa do \_ \_ catálogo global**</span><span class="sxs-lookup"><span data-stu-id="b9cae-112">**CAPICOM\_SEARCH\_GLOBAL\_CATALOG**</span></span> | <span data-ttu-id="b9cae-113">Pesquisa apenas o catálogo global.</span><span class="sxs-lookup"><span data-stu-id="b9cae-113">Searches only the global catalog.</span></span><br/> | <span data-ttu-id="b9cae-114">1</span><span class="sxs-lookup"><span data-stu-id="b9cae-114">1</span></span>     |
| <span data-ttu-id="b9cae-115">**CAPICOM de \_ pesquisa de \_ \_ domínio padrão**</span><span class="sxs-lookup"><span data-stu-id="b9cae-115">**CAPICOM\_SEARCH\_DEFAULT\_DOMAIN**</span></span> | <span data-ttu-id="b9cae-116">Pesquisa apenas o domínio padrão.</span><span class="sxs-lookup"><span data-stu-id="b9cae-116">Searches only the default domain.</span></span><br/> | <span data-ttu-id="b9cae-117">2</span><span class="sxs-lookup"><span data-stu-id="b9cae-117">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="b9cae-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9cae-118">Remarks</span></span>

<span data-ttu-id="b9cae-119">Esse tipo de enumeração é usado pela seguinte propriedade:</span><span class="sxs-lookup"><span data-stu-id="b9cae-119">This enumeration type is used by the following property:</span></span>

-   [<span data-ttu-id="b9cae-120">**Settings. ActiveDirectorySearchLocation**</span><span class="sxs-lookup"><span data-stu-id="b9cae-120">**Settings.ActiveDirectorySearchLocation**</span></span>](settings-activedirectorysearchlocation.md)

## <a name="requirements"></a><span data-ttu-id="b9cae-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9cae-121">Requirements</span></span>



| <span data-ttu-id="b9cae-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9cae-122">Requirement</span></span> | <span data-ttu-id="b9cae-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b9cae-123">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b9cae-124">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="b9cae-124">Redistributable</span></span><br/> | <span data-ttu-id="b9cae-125">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="b9cae-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="b9cae-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b9cae-126">Header</span></span><br/>          | <dl> <span data-ttu-id="b9cae-127"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9cae-127"><dt>Capicom.h</dt></span></span> </dl> |



 

 
