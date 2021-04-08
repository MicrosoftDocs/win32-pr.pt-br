---
title: Consultando grupos em um domínio
description: Os grupos podem ser colocados em qualquer contêiner ou unidade organizacional em um domínio, bem como a raiz do domínio.
ms.assetid: 338a93dd-445d-4f74-a6d6-e5c8ba2e765e
ms.tgt_platform: multiple
keywords:
- Consultando grupos em um AD de domínio
- Grupos de anúncios, consultando grupos em um domínio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3abd4ec393fbeca1308ed59e08131b9b73e6b1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103823636"
---
# <a name="querying-for-groups-in-a-domain"></a><span data-ttu-id="efa84-105">Consultando grupos em um domínio</span><span class="sxs-lookup"><span data-stu-id="efa84-105">Querying for Groups in a Domain</span></span>

<span data-ttu-id="efa84-106">Os grupos podem ser colocados em qualquer contêiner ou unidade organizacional em um domínio, bem como a raiz do domínio.</span><span class="sxs-lookup"><span data-stu-id="efa84-106">Groups can be placed in any container or organizational unit in a domain as well as the root of the domain.</span></span> <span data-ttu-id="efa84-107">Os grupos não podem estar sempre em um contêiner.</span><span class="sxs-lookup"><span data-stu-id="efa84-107">Groups may not always be in one container.</span></span> <span data-ttu-id="efa84-108">Portanto, é necessário pesquisar todo o domínio para localizar todos os grupos no domínio.</span><span class="sxs-lookup"><span data-stu-id="efa84-108">Therefore, it is necessary to search the entire domain to find all groups in the domain.</span></span>

<span data-ttu-id="efa84-109">Para pesquisar todos os grupos em um domínio, defina o ponto de início da pesquisa para a raiz do domínio, defina o escopo da pesquisa como subárvore e pesquise todos os objetos que tenham um valor de [**objectClass**](/windows/desktop/ADSchema/a-objectclass) de "grupo".</span><span class="sxs-lookup"><span data-stu-id="efa84-109">To search for all groups in a domain, set the search start point to the root of the domain, set the search scope to subtree and search for all objects that have an [**objectClass**](/windows/desktop/ADSchema/a-objectclass) value of "group".</span></span>

<span data-ttu-id="efa84-110">Se os grupos que contêm valores de [**\_ enumeração de \_ tipo \_ de grupo ADS**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) específicos tiverem sido encontrados, o operador de **regra de \_ correspondência LDAP \_ \_ \_ e** a regra de correspondência poderão ser usados para pesquisar grupos que tenham bits específicos definidos no atributo [**GroupType**](/windows/desktop/ADSchema/a-grouptype) .</span><span class="sxs-lookup"><span data-stu-id="efa84-110">If groups that contain particular [**ADS\_GROUP\_TYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) values must be found, the **LDAP\_MATCHING\_RULE\_BIT\_AND** matching rule operator can be used to search for groups that have particular bits set in the [**groupType**](/windows/desktop/ADSchema/a-grouptype) attribute.</span></span> <span data-ttu-id="efa84-111">Para obter mais informações sobre como usar regras de correspondência, consulte [sintaxe do filtro de pesquisa](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="efa84-111">For more information about using matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

<span data-ttu-id="efa84-112">Para obter mais informações e um exemplo de código que mostra como procurar grupos em um domínio, consulte [exemplo de código para pesquisar grupos em um domínio](example-code-for-performing-a-query-in-a-domain.md).</span><span class="sxs-lookup"><span data-stu-id="efa84-112">For more information and a code example that shows how to search for groups in a domain, see [Example Code for Searching for Groups in a Domain](example-code-for-performing-a-query-in-a-domain.md).</span></span>

 

 