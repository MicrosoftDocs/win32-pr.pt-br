---
title: Caça de referência com IDirectorySearch
description: Uma referência é o mecanismo que um servidor de diretório usa para direcionar um cliente para outro servidor quando ele não contém dados suficientes sobre o objeto solicitado por uma consulta.
ms.assetid: ef97eafd-5227-4dd7-9f8a-6b4591261f79
ms.tgt_platform: multiple
keywords:
- Caça de referência com IDirectorySearch ADSI
- ADSI, pesquisa, IDirectorySearch, outras opções de pesquisa, caça de referência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fae76139dc1a68c9345cd7a7b3bb894a50a2d7b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917676"
---
# <a name="referral-chasing-with-idirectorysearch"></a><span data-ttu-id="40794-105">Caça de referência com IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="40794-105">Referral Chasing with IDirectorySearch</span></span>

<span data-ttu-id="40794-106">Uma referência é o mecanismo que um servidor de diretório usa para direcionar um cliente para outro servidor quando ele não contém dados suficientes sobre o objeto solicitado por uma consulta.</span><span class="sxs-lookup"><span data-stu-id="40794-106">A referral is the mechanism that a directory server uses to direct a client to another server when it does not contain sufficient data about the object requested by a query.</span></span>

<span data-ttu-id="40794-107">Em uma pesquisa de um nível ou de subárvore, as referências são retornadas apenas para contêineres de domínio, esquema ou configuração conhecidos, imediatamente subordinados; ou seja, os domínios filho que são descendentes diretos.</span><span class="sxs-lookup"><span data-stu-id="40794-107">In a one-level or subtree search, referrals are returned for known, immediately subordinate domain, schema, or configuration containers only; that is, child domains that are direct descendants.</span></span> <span data-ttu-id="40794-108">Para obter mais informações, consulte [escopo da pesquisa](/windows/desktop/AD/search-scope).</span><span class="sxs-lookup"><span data-stu-id="40794-108">For more information, see [Search Scope](/windows/desktop/AD/search-scope).</span></span>

<span data-ttu-id="40794-109">Em um diretório, nem todos os dados estão disponíveis em um único servidor, em vez disso, eles são distribuídos por vários servidores diferentes pela rede.</span><span class="sxs-lookup"><span data-stu-id="40794-109">In a directory, not all data is available on a single server, rather, it is distributed over several different servers across the network.</span></span> <span data-ttu-id="40794-110">Se os servidores compartilharem os dados que outros servidores podem fornecer, eles poderão fornecer referências a um cliente quando uma consulta solicitada não puder ser resolvida no servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="40794-110">If the servers share the data that other servers can provide, they can provide referrals to a client when a requested query cannot be resolved on the originating server.</span></span> <span data-ttu-id="40794-111">Por exemplo, quando um cliente solicita ao servidor A para consultar um objeto de usuário (U), um pode sugerir que o cliente continue a pesquisa no servidor B se U não residir em um, mas é identificado como em B. O cliente tem a opção de buscar a referência ou não.</span><span class="sxs-lookup"><span data-stu-id="40794-111">For example, when a client asks Server A to query a user object (U), then A can suggest that the client continue the search on Server B if U does not reside on A, but is identified to be on B. The client has the choice to pursue the referral or not.</span></span> <span data-ttu-id="40794-112">As referências liberam o cliente de ter que ter conhecimento prévio da capacidade de cada servidor, mas o cliente deve especificar o tipo de referências que um servidor deve executar.</span><span class="sxs-lookup"><span data-stu-id="40794-112">Referrals free the client from having to possess previous knowledge of the capability of each server, but the client must specify the type of referrals a server should perform.</span></span>

<span data-ttu-id="40794-113">Para habilitar ou desabilitar a busca de referência, defina uma opção de pesquisa de **referências do ADS \_ SEARCHPREF \_ Chase \_** com um valor **\_ inteiro ADSTYPE** que contenha um dos [**anúncios \_ Chase \_ referências \_ enum**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) valores de enumeração na matriz de [**\_ \_ informações de SEARCHPREF do ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passada para o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="40794-113">To enable or disable referral chasing, set an **ADS\_SEARCHPREF\_CHASE\_REFERRALS** search option with an **ADSTYPE\_INTEGER** value that contains one of the [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) enumeration values in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="40794-114">O exemplo de código a seguir mostra como habilitar referências de Chase.</span><span class="sxs-lookup"><span data-stu-id="40794-114">The following code example shows how to enable chase referrals.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CHASE_REFERRALS;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = ADS_CHASE_REFERRALS_ALWAYS;
```



<span data-ttu-id="40794-115">Para obter mais informações sobre referências no Active Directory, consulte [referências](/windows/desktop/AD/referrals).</span><span class="sxs-lookup"><span data-stu-id="40794-115">For more information about referrals in Active Directory, see [Referrals](/windows/desktop/AD/referrals).</span></span>

 

 