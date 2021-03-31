---
title: Procurando grupos por escopo ou tipo em um domínio
description: Em domínios do Windows 2000, há uma classe única chamada grupo para todos os escopos de grupo (domínio local, global, universal) e tipos (segurança, distribuição).
ms.assetid: e32629d9-aa62-4953-aa49-43af726b7deb
ms.tgt_platform: multiple
keywords:
- Procurando grupos por escopo ou tipo em um AD de domínio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee9aae5e2c7be7b9cba590f9bc80f0517bca918
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640381"
---
# <a name="searching-for-groups-by-scope-or-type-in-a-domain"></a><span data-ttu-id="74adf-104">Procurando grupos por escopo ou tipo em um domínio</span><span class="sxs-lookup"><span data-stu-id="74adf-104">Searching for Groups by Scope or Type in a Domain</span></span>

<span data-ttu-id="74adf-105">Em domínios do Windows 2000, há uma classe única chamada [**grupo**](/windows/desktop/ADSchema/c-group) para todos os escopos de grupo (domínio local, global, universal) e tipos (segurança, distribuição).</span><span class="sxs-lookup"><span data-stu-id="74adf-105">In Windows 2000 domains, there is single class called [**group**](/windows/desktop/ADSchema/c-group) for all group scopes (Domain Local, Global, Universal) and types (security, distribution).</span></span> <span data-ttu-id="74adf-106">O atributo [**GroupType**](/windows/desktop/ADSchema/a-grouptype) do objeto Group especifica o tipo e o escopo do grupo.</span><span class="sxs-lookup"><span data-stu-id="74adf-106">The [**groupType**](/windows/desktop/ADSchema/a-grouptype) attribute of the group object specifies the group type and scope.</span></span>

<span data-ttu-id="74adf-107">Para usar tipo ou escopo para pesquisar grupos em domínios do Windows 2000, use um filtro que contenha uma regra de correspondência para o atributo [**GroupType**](/windows/desktop/ADSchema/a-grouptype) .</span><span class="sxs-lookup"><span data-stu-id="74adf-107">To use type or scope to search for groups on Windows 2000 domains, use a filter that contains a matching rule for the [**groupType**](/windows/desktop/ADSchema/a-grouptype) attribute.</span></span> <span data-ttu-id="74adf-108">Para obter mais informações sobre regras de correspondência, consulte [sintaxe do filtro de pesquisa](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="74adf-108">For more information about matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

<span data-ttu-id="74adf-109">Para obter mais informações e um exemplo de código que mostra como procurar grupos em um domínio, consulte [exemplo de código para pesquisar grupos em um domínio](example-code-for-performing-a-query-in-a-domain.md).</span><span class="sxs-lookup"><span data-stu-id="74adf-109">For more information and a code example that shows how to search for groups in a domain, see [Example Code for Searching for Groups in a Domain](example-code-for-performing-a-query-in-a-domain.md).</span></span>

## <a name="example-ldap-query-strings"></a><span data-ttu-id="74adf-110">Exemplo de cadeias de consulta LDAP</span><span class="sxs-lookup"><span data-stu-id="74adf-110">Example LDAP Query Strings</span></span>

<span data-ttu-id="74adf-111">Os exemplos de cadeia de caracteres de consulta a seguir mostram como construir uma cadeia de caracteres de consulta LDAP usada para pesquisar ou filtrar tipos de grupos específicos.</span><span class="sxs-lookup"><span data-stu-id="74adf-111">The following query string examples show how to construct an LDAP query string used to search for or filter specific group types.</span></span>

<span data-ttu-id="74adf-112">A cadeia de caracteres de consulta a seguir pesquisará grupos de segurança.</span><span class="sxs-lookup"><span data-stu-id="74adf-112">The following query string will search for security groups.</span></span> <span data-ttu-id="74adf-113">Este exemplo usa "-2147483648" como o equivalente Decimal do sinalizador **de \_ segurança de tipo de grupo ADS \_ \_ \_ habilitado** .</span><span class="sxs-lookup"><span data-stu-id="74adf-113">This example uses "-2147483648" as the decimal equivalent of the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag.</span></span>


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=-2147483648))
```



<span data-ttu-id="74adf-114">A cadeia de caracteres de consulta a seguir pesquisará grupos de distribuição universal; ou seja, os grupos que contêm o sinalizador de **\_ \_ \_ \_ grupo de tipos de grupo ADS** e não contêm o sinalizador de segurança de tipo de **\_ grupo ADS \_ \_ \_ habilitado** .</span><span class="sxs-lookup"><span data-stu-id="74adf-114">The following query string will search for universal distribution groups; that is, groups that contain the **ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** flag and do not contain the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag.</span></span> <span data-ttu-id="74adf-115">Este exemplo usa "8" como o equivalente Decimal do **tipo de grupo do ADS \_ \_ \_ \_ grupo universal** e "-2147483648" como o equivalente Decimal do sinalizador de **segurança de tipo de \_ grupo ADS \_ \_ \_ habilitado** .</span><span class="sxs-lookup"><span data-stu-id="74adf-115">This example uses "8" as the decimal equivalent of **ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** and "-2147483648" as the decimal equivalent of the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag.</span></span>


```C++
(&(objectCategory=group)((&(groupType:1.2.840.113556.1.4.803:=8)(!(groupType:1.2.840.113556.1.4.803:=-2147483648)))))
```



 

 