---
description: .
ms.assetid: 24617b5f-14f1-4f1b-a288-7d20a8166da0
title: Alterações de classificação NLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0805eae753c1e312d26f8c84e13d19041458cf26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506225"
---
# <a name="nls-sorting-changes"></a><span data-ttu-id="f1970-103">Alterações de classificação NLS</span><span class="sxs-lookup"><span data-stu-id="f1970-103">NLS Sorting Changes</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="f1970-104">Plataformas afetadas</span><span class="sxs-lookup"><span data-stu-id="f1970-104">Affected Platforms</span></span>

 <span data-ttu-id="f1970-105">**Clientes** -Windows XP Windows \| Vista Windows \| 7</span><span class="sxs-lookup"><span data-stu-id="f1970-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="f1970-106">**Servidores** -windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f1970-106">**Servers** - Windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="f1970-107">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="f1970-107">Feature Impact</span></span>

 <span data-ttu-id="f1970-108">**Severidade** -alta</span><span class="sxs-lookup"><span data-stu-id="f1970-108">**Severity** - High</span></span>  
<span data-ttu-id="f1970-109">**Frequência** -baixa (poucos aplicativos impactados, mas se impactado, sempre interrompido)</span><span class="sxs-lookup"><span data-stu-id="f1970-109">**Frequency** - Low (few apps impacted, but if impacted, always broken)</span></span>  


## <a name="description"></a><span data-ttu-id="f1970-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1970-110">Description</span></span>

<span data-ttu-id="f1970-111">As funções NLS (suporte ao idioma nacional) ajudam os aplicativos a dar suporte às diferentes necessidades específicas de idioma e localidade de usuários em todo o mundo.</span><span class="sxs-lookup"><span data-stu-id="f1970-111">The National Language Support (NLS) functions help applications support the different language- and locale-specific needs of users around the world.</span></span> <span data-ttu-id="f1970-112">As novas versões do Windows quase invariavelmente incluem alterações de NLS.</span><span class="sxs-lookup"><span data-stu-id="f1970-112">New Windows versions almost invariably include NLS changes.</span></span> <span data-ttu-id="f1970-113">Essa alteração afeta agrupamento e classificação e, portanto, aplicativos que têm índices persistentes.</span><span class="sxs-lookup"><span data-stu-id="f1970-113">This change affects collation and sorting, and therefore applications that have persistent indexes.</span></span>

<span data-ttu-id="f1970-114">Uma tabela de agrupamento tem dois números que identificam sua versão (revisão): a versão definida e a versão do NLS.</span><span class="sxs-lookup"><span data-stu-id="f1970-114">A collation table has two numbers that identify its version (revision): the defined version and the NLS version.</span></span> <span data-ttu-id="f1970-115">Ambas as versões são valores DWORD, compostos de uma versão principal e uma versão secundária.</span><span class="sxs-lookup"><span data-stu-id="f1970-115">Both versions are DWORD values, composed of a major version and a minor version.</span></span> <span data-ttu-id="f1970-116">O primeiro byte de um valor é reservado, os próximos dois bytes representam a versão principal e o último byte representa a versão secundária.</span><span class="sxs-lookup"><span data-stu-id="f1970-116">The first byte of a value is reserved, the next two bytes represent the major version, and the last byte represents the minor version.</span></span> <span data-ttu-id="f1970-117">Em termos hexadecimais, o padrão é 0xRRMMMMmm, em que R é igual a reservado, M é igual a Major e m é igual a Minor.</span><span class="sxs-lookup"><span data-stu-id="f1970-117">In hexadecimal terms, the pattern is 0xRRMMMMmm, where R equals Reserved, M equals major, and m equals minor.</span></span> <span data-ttu-id="f1970-118">Por exemplo, uma versão principal de 3 com uma versão secundária de 4 é representada como 0x304.</span><span class="sxs-lookup"><span data-stu-id="f1970-118">For example, a major version of 3 with a minor version of 4 is represented as 0x304.</span></span>

<span data-ttu-id="f1970-119">Para uma versão principal, um ou mais pontos de código são alterados para que o aplicativo precise indexar novamente todos os dados para que as comparações sejam válidas.</span><span class="sxs-lookup"><span data-stu-id="f1970-119">For a major version, one or more code points change so that the application must re-index all data for comparisons to be valid.</span></span> <span data-ttu-id="f1970-120">Para uma versão secundária, nada se move, mas os pontos de código são adicionados.</span><span class="sxs-lookup"><span data-stu-id="f1970-120">For a minor version, nothing moves, but code points are added.</span></span> <span data-ttu-id="f1970-121">Para esse tipo de versão, o aplicativo precisa apenas reindexar cadeias de caracteres com valores não classificados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f1970-121">For this type of version, the application only has to re-index strings with previously unsortable values.</span></span> <span data-ttu-id="f1970-122">Em resumo, aqui está o que os números de versão significam em relação às alterações de dados nas tabelas de exceção específicas de localidade e tabelas padrão:</span><span class="sxs-lookup"><span data-stu-id="f1970-122">In summary, here is what the version numbers mean in relation to the data changes in the locale-specific exception tables and default tables:</span></span>

<span data-ttu-id="f1970-123">**NLSVersion principal** – pontos de código alterados nas tabelas ' Exception, ' ou específicas de localidade</span><span class="sxs-lookup"><span data-stu-id="f1970-123">**NLSVersion Major** – Changed code points in the 'exception,' or locale-specific tables</span></span>  
<span data-ttu-id="f1970-124">**NLSVersion Minor** – adicionou novos pontos de código nas tabelas ' Exception, ' ou específicas de localidade</span><span class="sxs-lookup"><span data-stu-id="f1970-124">**NLSVersion Minor** – Added new code points in the 'exception,' or locale-specific tables</span></span>  
<span data-ttu-id="f1970-125">**DefinedVersion principal** – pontos de código alterados na tabela padrão</span><span class="sxs-lookup"><span data-stu-id="f1970-125">**DefinedVersion Major** – Changed code points in the default table</span></span>  
<span data-ttu-id="f1970-126">**DefinedVersion Minor** – adicionou novos pontos de código na tabela padrão</span><span class="sxs-lookup"><span data-stu-id="f1970-126">**DefinedVersion Minor** – Added new code points in the default table</span></span>  


<span data-ttu-id="f1970-127">**Classificando números de versão para versões liberadas:**</span><span class="sxs-lookup"><span data-stu-id="f1970-127">**Sorting version numbers for released versions:**</span></span>



| <span data-ttu-id="f1970-128">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="f1970-128">Operating System</span></span>    | <span data-ttu-id="f1970-129">Versão</span><span class="sxs-lookup"><span data-stu-id="f1970-129">Release</span></span>           | <span data-ttu-id="f1970-130">Versão (0xRRMMMMmm)</span><span class="sxs-lookup"><span data-stu-id="f1970-130">Version (0xRRMMMMmm)</span></span>         |
|---------------------|-------------------|------------------------------|
| <span data-ttu-id="f1970-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f1970-131">Windows XP</span></span>          | <span data-ttu-id="f1970-132">RTM/SP1/SP2/SP3/...</span><span class="sxs-lookup"><span data-stu-id="f1970-132">RTM/SP1/SP2/SP3/…</span></span> | <span data-ttu-id="f1970-133">N/A-sem API GetNLSVersion ()</span><span class="sxs-lookup"><span data-stu-id="f1970-133">N/A - no GetNLSVersion() API</span></span> |
| <span data-ttu-id="f1970-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f1970-134">Windows Server 2003</span></span> | <span data-ttu-id="f1970-135">RTM/SP1</span><span class="sxs-lookup"><span data-stu-id="f1970-135">RTM/SP1</span></span>           | <span data-ttu-id="f1970-136">0x00 0000 01</span><span class="sxs-lookup"><span data-stu-id="f1970-136">0x00 0000 01</span></span>                 |
| <span data-ttu-id="f1970-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1970-137">Windows Vista</span></span>       | <span data-ttu-id="f1970-138">RTM/SP1</span><span class="sxs-lookup"><span data-stu-id="f1970-138">RTM/SP1</span></span>           | <span data-ttu-id="f1970-139">0x00 0405 00</span><span class="sxs-lookup"><span data-stu-id="f1970-139">0x00 0405 00</span></span>                 |
| <span data-ttu-id="f1970-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1970-140">Windows Server 2008</span></span> | <span data-ttu-id="f1970-141">RTM</span><span class="sxs-lookup"><span data-stu-id="f1970-141">RTM</span></span>               | <span data-ttu-id="f1970-142">0x00 0501 00/0x00 5001 00</span><span class="sxs-lookup"><span data-stu-id="f1970-142">0x00 0501 00 / 0x00 5001 00</span></span>  |
| <span data-ttu-id="f1970-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f1970-143">Windows 7</span></span>           | <span data-ttu-id="f1970-144">RTM</span><span class="sxs-lookup"><span data-stu-id="f1970-144">RTM</span></span>               | <span data-ttu-id="f1970-145">0x00060100</span><span class="sxs-lookup"><span data-stu-id="f1970-145">0x00060100</span></span>                   |



 

## <a name="manifestation"></a><span data-ttu-id="f1970-146">Manifestação</span><span class="sxs-lookup"><span data-stu-id="f1970-146">Manifestation</span></span>

<span data-ttu-id="f1970-147">Aplicativos (como bancos de dados) com índices persistentes que não verificam a versão NLS e reindexam após a alteração da versão não serão classificados corretamente ou poderão falhar em fornecer os resultados solicitados.</span><span class="sxs-lookup"><span data-stu-id="f1970-147">Applications (such as databases) with persistent indexes that do not check the NLS version and re-index upon version change will fail to sort correctly or may fail to provide requested results.</span></span>

<span data-ttu-id="f1970-148">No caso de interfaces do usuário, as listas (por exemplo, alfabéticos, numéricos, alfanuméricos, símbolos e assim por diante) podem ser classificadas incorretamente.</span><span class="sxs-lookup"><span data-stu-id="f1970-148">In the case of user interfaces, lists (for example, alphabetical, numeric, alphanumeric, symbols, and so on) may sort incorrectly.</span></span>

## <a name="solution"></a><span data-ttu-id="f1970-149">Solução</span><span class="sxs-lookup"><span data-stu-id="f1970-149">Solution</span></span>

<span data-ttu-id="f1970-150">Seu aplicativo pode chamar **GetNLSVersionEx** (Windows Vista ou posterior) ou **GetNLSVersion** (antes do Windows Vista) para recuperar a versão definida e a versão do NLS para uma tabela de agrupamento.</span><span class="sxs-lookup"><span data-stu-id="f1970-150">Your application can call either **GetNLSVersionEx** (Windows Vista or later) or **GetNLSVersion** (prior to Windows Vista) to retrieve both the defined version and the NLS version for a collation table.</span></span>

-   <span data-ttu-id="f1970-151">GetNLSVersionEx:</span><span class="sxs-lookup"><span data-stu-id="f1970-151">GetNLSVersionEx:</span></span>

<span data-ttu-id="f1970-152">*Recupera informações sobre a versão atual de um recurso NLS especificado para uma localidade especificada pelo nome*</span><span class="sxs-lookup"><span data-stu-id="f1970-152">*Retrieves information about the current version of a specified NLS capability for a locale specified by name*</span></span>  
<span data-ttu-id="f1970-153">Essa função permite que um aplicativo como Active Directory determine se uma alteração NLS afeta a localidade usada para uma tabela de índice específica.</span><span class="sxs-lookup"><span data-stu-id="f1970-153">This function allows an application such as Active Directory to determine whether an NLS change affects the locale used for a particular index table.</span></span> <span data-ttu-id="f1970-154">Se não tiver, não será necessário reindexar a tabela.</span><span class="sxs-lookup"><span data-stu-id="f1970-154">If it does not, there is no need to re-index the table.</span></span> <span data-ttu-id="f1970-155">Para obter mais informações, consulte Manipulando informações de localidade e idioma.</span><span class="sxs-lookup"><span data-stu-id="f1970-155">For more information, see Handling Locale and Language Information.</span></span>  
<span data-ttu-id="f1970-156">Essa função dá suporte a localidades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="f1970-156">This function supports custom locales.</span></span> <span data-ttu-id="f1970-157">Se *lpLocaleName* especificar uma localidade suplementar, os dados recuperados serão os dados corretos para a ordem de agrupamento associada a essa localidade complementar.</span><span class="sxs-lookup"><span data-stu-id="f1970-157">If *lpLocaleName* specifies a supplemental locale, the data retrieved is the correct data for the collation order associated with that supplemental locale.</span></span>  

<span data-ttu-id="f1970-158">**Observação:** Versões do Windows anteriores ao Windows Vista não dão suporte a **GetNLSVersionEx**.</span><span class="sxs-lookup"><span data-stu-id="f1970-158">**Note:** Versions of Windows prior to Windows Vista do not support **GetNLSVersionEx**.</span></span>  


-   <span data-ttu-id="f1970-159">GetNLSVersion (use para aplicativos executados em versões do Windows anteriores ao Windows Vista):</span><span class="sxs-lookup"><span data-stu-id="f1970-159">GetNLSVersion (use for applications running on versions of Windows prior to Windows Vista):</span></span>

<span data-ttu-id="f1970-160">*Recupera informações sobre a versão atual de um recurso NLS especificado para uma localidade especificada pelo identificador*</span><span class="sxs-lookup"><span data-stu-id="f1970-160">*Retrieves information about the current version of a specified NLS capability for a locale specified by identifier*</span></span>  
<span data-ttu-id="f1970-161">Essa função permite que um aplicativo como Active Directory determine se uma alteração NLS afeta o identificador de localidade usado para uma tabela de índice específica.</span><span class="sxs-lookup"><span data-stu-id="f1970-161">This function allows an application such as Active Directory to determine if an NLS change affects the locale identifier used for a particular index table.</span></span> <span data-ttu-id="f1970-162">Se não tiver, não será necessário reindexar a tabela.</span><span class="sxs-lookup"><span data-stu-id="f1970-162">If it does not, there is no need to re-index the table.</span></span> <span data-ttu-id="f1970-163">Para obter mais informações, consulte Manipulando informações de localidade e idioma.</span><span class="sxs-lookup"><span data-stu-id="f1970-163">For more information, see Handling Locale and Language Information.</span></span>  
<span data-ttu-id="f1970-164">**Observação:** Essa função recupera informações apenas sobre uma localidade especificada pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="f1970-164">**Note:** This function retrieves information only about a locale specified by identifier.</span></span> <span data-ttu-id="f1970-165">A função **GetNLSVersionEx** dá suporte a localidades adicionais, recursos e nomes RFC 4646.</span><span class="sxs-lookup"><span data-stu-id="f1970-165">The **GetNLSVersionEx** function supports additional locales, features, and RFC 4646 names.</span></span> <span data-ttu-id="f1970-166">No entanto, as versões do Windows anteriores ao Windows Vista não dão suporte a **GetNLSVersionEx**.</span><span class="sxs-lookup"><span data-stu-id="f1970-166">However, versions of Windows prior to Windows Vista do not support **GetNLSVersionEx**.</span></span>  
<span data-ttu-id="f1970-167">Os aplicativos destinam-se a ser executados somente no Windows Vista e posterior devem usar **GetNLSVersionEx** em preferência para essa função.</span><span class="sxs-lookup"><span data-stu-id="f1970-167">Applications meant to run only on Windows Vista and later should use **GetNLSVersionEx** in preference to this function.</span></span> <span data-ttu-id="f1970-168">O **GetNLSVersionEx** fornece um bom suporte para localidades complementares.</span><span class="sxs-lookup"><span data-stu-id="f1970-168">**GetNLSVersionEx** provides good support for supplemental locales.</span></span>  


## <a name="compatibility-test"></a><span data-ttu-id="f1970-169">Teste de compatibilidade</span><span class="sxs-lookup"><span data-stu-id="f1970-169">Compatibility Test</span></span>

<span data-ttu-id="f1970-170">**Etapas para saber se uma versão de agrupamento foi alterada (ou seja, você precisa reindexar):**</span><span class="sxs-lookup"><span data-stu-id="f1970-170">**Steps to tell if a collation version changed (that is, you need to re-index):**</span></span>

-   <span data-ttu-id="f1970-171">**Use GetNLSVersionEx ()** para recuperar uma estrutura **NLSVERSIONINFOEX** ao fazer a indexação original de seus dados.</span><span class="sxs-lookup"><span data-stu-id="f1970-171">**Use GetNLSVersionEx()** to retrieve an **NLSVERSIONINFOEX** structure when doing the original indexing of your data.</span></span>
-   <span data-ttu-id="f1970-172">Armazene as seguintes propriedades com seu índice para identificar a versão:  **NLSVERSIONINFOEX. dwNLSVersion** e **NLSVERSIONINFOEX. dwDefinedVersion** – essas duas propriedades juntas especificam a versão da tabela de classificação que você está usando.</span><span class="sxs-lookup"><span data-stu-id="f1970-172">Store the following properties with your index to identify the version:  **NLSVERSIONINFOEX.dwNLSVersion** and **NLSVERSIONINFOEX.dwDefinedVersion** – These two properties together specify the version of the sorting table you are using.</span></span>  
    <span data-ttu-id="f1970-173">**NLSVERSIONINFOEX. dwEffectiveId** -especifica a localidade efetiva do seu tipo.</span><span class="sxs-lookup"><span data-stu-id="f1970-173">**NLSVERSIONINFOEX.dwEffectiveId** - This specifies the effective locale of your sort.</span></span> <span data-ttu-id="f1970-174">Uma localidade personalizada apontará para uma classificação de localidade na caixa.</span><span class="sxs-lookup"><span data-stu-id="f1970-174">A custom locale will point to an in-box locale's sort.</span></span>  
    
-   <span data-ttu-id="f1970-175">Ao usar o índice, use **GetNlsVersionEx ()** para descobrir a versão dos seus dados.</span><span class="sxs-lookup"><span data-stu-id="f1970-175">When using the index use **GetNlsVersionEx()** to discover the version of your data.</span></span>
-   <span data-ttu-id="f1970-176">Se qualquer uma das três propriedades for alterada, os dados de classificação que você está usando podem retornar resultados diferentes e qualquer indexação que você tenha pode falhar ao localizar registros.</span><span class="sxs-lookup"><span data-stu-id="f1970-176">If any of the three properties has changed, the sorting data you are using could return different results and any indexing you have may fail to find records.</span></span>
-   <span data-ttu-id="f1970-177">Se você souber que seus dados não contêm pontos de código Unicode inválidos (ou seja, todas as cadeias de caracteres retornadas **true** de uma chamada para **IsNLSDefinedString ()**), você poderá considerá-los os mesmos se apenas o byte baixo de **dwNLSVersion** e **dwDefinedVersion** forem alterados (as versões secundárias descritas acima).</span><span class="sxs-lookup"><span data-stu-id="f1970-177">If you KNOW that your data does not contain invalid Unicode code points (that is, all of your strings returned **TRUE** from a call to **IsNLSDefinedString()**), then you may consider them the same if ONLY the low byte of **dwNLSVersion** and **dwDefinedVersion** changed (the minor versions described above).</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="f1970-178">Links para outros recursos</span><span class="sxs-lookup"><span data-stu-id="f1970-178">Links to Other Resources</span></span>

-   [<span data-ttu-id="f1970-179">Internacionalização para aplicativos do Windows</span><span class="sxs-lookup"><span data-stu-id="f1970-179">Internationalization for Windows Applications</span></span>](../intl/international-support.md)
-   [<span data-ttu-id="f1970-180">Função GetNLSVersionEx</span><span class="sxs-lookup"><span data-stu-id="f1970-180">GetNLSVersionEx Function</span></span>](/windows/win32/api/winnls/nf-winnls-getnlsversionex)
-   [<span data-ttu-id="f1970-181">Função GetNLSVersion</span><span class="sxs-lookup"><span data-stu-id="f1970-181">GetNLSVersion Function</span></span>](/windows/win32/api/winnls/nf-winnls-getnlsversion)
-   [<span data-ttu-id="f1970-182">Como saber se a versão do agrupamento foi alterada</span><span class="sxs-lookup"><span data-stu-id="f1970-182">How to tell if the collation version changed</span></span>](/archive/blogs/shawnste/)

 

 
