---
description: 'Saiba mais sobre: membros do VistaParam'
title: Membros VistaParam (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: VistaParam members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.VistaParam
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam_members(v=EXCHG.10)
ms:contentKeyID: 55104333
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c56c8ad3a64eb08654ee893e86683e95e32af443
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826794"
---
# <a name="vistaparam-members"></a><span data-ttu-id="83c85-103">Membros do VistaParam</span><span class="sxs-lookup"><span data-stu-id="83c85-103">VistaParam members</span></span>

<span data-ttu-id="83c85-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="83c85-104">Include protected members</span></span>  
<span data-ttu-id="83c85-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="83c85-105">Include inherited members</span></span>  

<span data-ttu-id="83c85-106">Parâmetros do sistema que foram adicionados à versão vista do ESENT.</span><span class="sxs-lookup"><span data-stu-id="83c85-106">System parameters that have been added to the Vista version of ESENT.</span></span>

<span data-ttu-id="83c85-107">O tipo [VistaParam](./vistaparam-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="83c85-107">The [VistaParam](./vistaparam-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="83c85-108">Campos</span><span class="sxs-lookup"><span data-stu-id="83c85-108">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="83c85-109">Nome</span><span class="sxs-lookup"><span data-stu-id="83c85-109">Name</span></span></th>
<th><span data-ttu-id="83c85-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="83c85-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="83c85-113"><a href="dn335379(v=exchg.10).md">CachedClosedTables</a></span><span class="sxs-lookup"><span data-stu-id="83c85-113"><a href="dn335379(v=exchg.10).md">CachedClosedTables</a></span></span></td>
<td><span data-ttu-id="83c85-114">Esse parâmetro controla o número de recursos da árvore B + em cache pela instância depois que as tabelas que eles representam foram fechadas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="83c85-114">This parameter controls the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="83c85-115">Valores grandes para esse parâmetro farão com que o mecanismo de banco de dados use mais memória, mas aumentará a velocidade com que um grande número de tabelas pode ser aberto aleatoriamente pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="83c85-115">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="83c85-116">Isso é útil para aplicativos que têm um esquema com um número muito grande de tabelas.</span><span class="sxs-lookup"><span data-stu-id="83c85-116">This is useful for applications that have a schema with a very large number of tables.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="83c85-119"><a href="dn335289(v=exchg.10).md">Configuration</a></span><span class="sxs-lookup"><span data-stu-id="83c85-119"><a href="dn335289(v=exchg.10).md">Configuration</a></span></span></td>
<td><span data-ttu-id="83c85-120">Esse parâmetro expõe vários conjuntos de valores padrão para todo o conjunto de parâmetros do sistema.</span><span class="sxs-lookup"><span data-stu-id="83c85-120">This parameter exposes multiple sets of default values for the entire set of system parameters.</span></span> <span data-ttu-id="83c85-121">Quando esse parâmetro é definido como uma configuração específica, todos os valores de parâmetro do sistema são redefinidos para seus valores padrão para essa configuração.</span><span class="sxs-lookup"><span data-stu-id="83c85-121">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="83c85-122">Se a configuração for definida para uma instância específica, os parâmetros do sistema global não serão redefinidos para seus valores padrão.</span><span class="sxs-lookup"><span data-stu-id="83c85-122">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="83c85-123">Configuração pequena (0): o mecanismo de banco de dados é otimizado para uso de memória.</span><span class="sxs-lookup"><span data-stu-id="83c85-123">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="83c85-124">Configuração herdada (1): o mecanismo de banco de dados tem seus padrões tradicionais.</span><span class="sxs-lookup"><span data-stu-id="83c85-124">Legacy Configuration (1): The database engine has its traditional defaults.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="83c85-127"><a href="dn335380(v=exchg.10).md">EnableAdvanced</a></span><span class="sxs-lookup"><span data-stu-id="83c85-127"><a href="dn335380(v=exchg.10).md">EnableAdvanced</a></span></span></td>
<td><span data-ttu-id="83c85-128">Esse parâmetro é usado para controlar quando o mecanismo de banco de dados aceita ou rejeita alterações em um subconjunto dos parâmetros do sistema.</span><span class="sxs-lookup"><span data-stu-id="83c85-128">This parameter is used to control when the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="83c85-129">Esse parâmetro é usado em conjunto com a <a href="dn335289(v=exchg.10).md">configuração</a> para impedir que alguns parâmetros do sistema sejam definidos fora dos padrões da configuração selecionada.</span><span class="sxs-lookup"><span data-stu-id="83c85-129">This parameter is used in conjunction with <a href="dn335289(v=exchg.10).md">Configuration</a> to prevent some system parameters from being set away from the selected configuration's defaults.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="83c85-132"><a href="dn335291(v=exchg.10).md">EnableFileCache</a></span><span class="sxs-lookup"><span data-stu-id="83c85-132"><a href="dn335291(v=exchg.10).md">EnableFileCache</a></span></span></td>
<td><span data-ttu-id="83c85-133">Habilite o uso do cache de arquivos do so para todos os arquivos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="83c85-133">Enable the use of the OS file cache for all managed files.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="83c85-136"><a href="dn335381(v=exchg.10).md">EnableViewCache</a></span><span class="sxs-lookup"><span data-stu-id="83c85-136"><a href="dn335381(v=exchg.10).md">EnableViewCache</a></span></span></td>
<td><span data-ttu-id="83c85-137">Habilite o uso de e/s de arquivo mapeado de memória para arquivos de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="83c85-137">Enable the use of memory mapped file I/O for database files.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="83c85-140"><a href="dn335292(v=exchg.10).md">Mais</a></span><span class="sxs-lookup"><span data-stu-id="83c85-140"><a href="dn335292(v=exchg.10).md">KeyMost</a></span></span></td>
<td><span data-ttu-id="83c85-141">Esse parâmetro somente leitura indica o comprimento máximo de chave de índice permitido que pode ser selecionado para o tamanho da página do banco de dados atual (conforme configurado por <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>).</span><span class="sxs-lookup"><span data-stu-id="83c85-141">This read-only parameter indicates the maximum allowable index key length that can be selected for the current database page size (as configured by <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="83c85-144"><a href="dn335384(v=exchg.10).md">LegacyFileNames</a></span><span class="sxs-lookup"><span data-stu-id="83c85-144"><a href="dn335384(v=exchg.10).md">LegacyFileNames</a></span></span></td>
<td><span data-ttu-id="83c85-145">Esse parâmetro fornece compatibilidade com versões anteriores do mecanismo de banco de dados para as convenções de nomenclatura do arquivo.</span><span class="sxs-lookup"><span data-stu-id="83c85-145">This parameter provides backwards compatibility with the file naming conventions of earlier releases of the database engine.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="83c85-148"><a href="dn335294(v=exchg.10).md">TableClass10Name</a></span><span class="sxs-lookup"><span data-stu-id="83c85-148"><a href="dn335294(v=exchg.10).md">TableClass10Name</a></span></span></td>
<td><span data-ttu-id="83c85-149">Defina o nome associado à classe de tabela 10.</span><span class="sxs-lookup"><span data-stu-id="83c85-149">Set the name associated with table class 10.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="83c85-152"><a href="dn335385(v=exchg.10).md">TableClass11Name</a></span><span class="sxs-lookup"><span data-stu-id="83c85-152"><a href="dn335385(v=exchg.10).md">TableClass11Name</a></span></span></td>
<td><span data-ttu-id="83c85-153">Defina o nome associado à tabela classe 11.</span><span class="sxs-lookup"><span data-stu-id="83c85-153">Set the name associated with table class 11.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="83c85-156"><a href="dn335387(v=exchg.10).md">TableClass12Name</a></span><span class="sxs-lookup"><span data-stu-id="83c85-156"><a href="dn335387(v=exchg.10).md">TableClass12Name</a></span></span></td>
<td><span data-ttu-id="83c85-157">Defina o nome associado à classe de tabela 12.</span><span class="sxs-lookup"><span data-stu-id="83c85-157">Set the name associated with table class 12.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="83c85-160"><a href="dn335388(v=exchg.10).md">TableClass13Name</a></span><span class="sxs-lookup"><span data-stu-id="83c85-160"><a href="dn335388(v=exchg.10).md">TableClass13Name</a></span></span></td>
<td><span data-ttu-id="83c85-161">Defina o nome associado à classe de tabela 13.</span><span class="sxs-lookup"><span data-stu-id="83c85-161">Set the name associated with table class 13.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="83c85-164"><a href="dn335295(v=exchg.10).md">TableClass14Name</a></span><span class="sxs-lookup"><span data-stu-id="83c85-164"><a href="dn335295(v=exchg.10).md">TableClass14Name</a></span></span></td>
<td><span data-ttu-id="83c85-165">Defina o nome associado à classe de tabela 14.</span><span class="sxs-lookup"><span data-stu-id="83c85-165">Set the name associated with table class 14.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="83c85-168"><a href="dn335390(v=exchg.10).md">TableClass15Name</a></span><span class="sxs-lookup"><span data-stu-id="83c85-168"><a href="dn335390(v=exchg.10).md">TableClass15Name</a></span></span></td>
<td><span data-ttu-id="83c85-169">Defina o nome associado à classe de tabela 15.</span><span class="sxs-lookup"><span data-stu-id="83c85-169">Set the name associated with table class 15.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="83c85-172"><a href="dn335297(v=exchg.10).md">TableClass1Name</a></span><span class="sxs-lookup"><span data-stu-id="83c85-172"><a href="dn335297(v=exchg.10).md">TableClass1Name</a></span></span></td>
<td><span data-ttu-id="83c85-173">Defina o nome associado à tabela classe 1.</span><span class="sxs-lookup"><span data-stu-id="83c85-173">Set the name associated with table class 1.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="83c85-176"><a href="dn335389(v=exchg.10).md">TableClass2Name</a></span><span class="sxs-lookup"><span data-stu-id="83c85-176"><a href="dn335389(v=exchg.10).md">TableClass2Name</a></span></span></td>
<td><span data-ttu-id="83c85-177">Defina o nome associado à tabela classe 2.</span><span class="sxs-lookup"><span data-stu-id="83c85-177">Set the name associated with table class 2.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="83c85-180"><a href="dn335296(v=exchg.10).md">TableClass3Name</a></span><span class="sxs-lookup"><span data-stu-id="83c85-180"><a href="dn335296(v=exchg.10).md">TableClass3Name</a></span></span></td>
<td><span data-ttu-id="83c85-181">Defina o nome associado à tabela classe 3.</span><span class="sxs-lookup"><span data-stu-id="83c85-181">Set the name associated with table class 3.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="83c85-184"><a href="dn335395(v=exchg.10).md">TableClass4Name</a></span><span class="sxs-lookup"><span data-stu-id="83c85-184"><a href="dn335395(v=exchg.10).md">TableClass4Name</a></span></span></td>
<td><span data-ttu-id="83c85-185">Defina o nome associado à tabela classe 4.</span><span class="sxs-lookup"><span data-stu-id="83c85-185">Set the name associated with table class 4.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="83c85-188"><a href="dn335401(v=exchg.10).md">TableClass5Name</a></span><span class="sxs-lookup"><span data-stu-id="83c85-188"><a href="dn335401(v=exchg.10).md">TableClass5Name</a></span></span></td>
<td><span data-ttu-id="83c85-189">Defina o nome associado à tabela classe 5.</span><span class="sxs-lookup"><span data-stu-id="83c85-189">Set the name associated with table class 5.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="83c85-192"><a href="dn335298(v=exchg.10).md">TableClass6Name</a></span><span class="sxs-lookup"><span data-stu-id="83c85-192"><a href="dn335298(v=exchg.10).md">TableClass6Name</a></span></span></td>
<td><span data-ttu-id="83c85-193">Defina o nome associado à tabela classe 6.</span><span class="sxs-lookup"><span data-stu-id="83c85-193">Set the name associated with table class 6.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="83c85-196"><a href="dn335402(v=exchg.10).md">TableClass7Name</a></span><span class="sxs-lookup"><span data-stu-id="83c85-196"><a href="dn335402(v=exchg.10).md">TableClass7Name</a></span></span></td>
<td><span data-ttu-id="83c85-197">Defina o nome associado à tabela classe 7.</span><span class="sxs-lookup"><span data-stu-id="83c85-197">Set the name associated with table class 7.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="83c85-200"><a href="dn335299(v=exchg.10).md">TableClass8Name</a></span><span class="sxs-lookup"><span data-stu-id="83c85-200"><a href="dn335299(v=exchg.10).md">TableClass8Name</a></span></span></td>
<td><span data-ttu-id="83c85-201">Defina o nome associado à classe de tabela 8.</span><span class="sxs-lookup"><span data-stu-id="83c85-201">Set the name associated with table class 8.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="83c85-204"><a href="dn335404(v=exchg.10).md">TableClass9Name</a></span><span class="sxs-lookup"><span data-stu-id="83c85-204"><a href="dn335404(v=exchg.10).md">TableClass9Name</a></span></span></td>
<td><span data-ttu-id="83c85-205">Defina o nome associado à classe de tabela 9.</span><span class="sxs-lookup"><span data-stu-id="83c85-205">Set the name associated with table class 9.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="83c85-206">Parte superior</span><span class="sxs-lookup"><span data-stu-id="83c85-206">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="83c85-207">Confira também</span><span class="sxs-lookup"><span data-stu-id="83c85-207">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="83c85-208">Referência</span><span class="sxs-lookup"><span data-stu-id="83c85-208">Reference</span></span>

[<span data-ttu-id="83c85-209">Classe VistaParam</span><span class="sxs-lookup"><span data-stu-id="83c85-209">VistaParam class</span></span>](./vistaparam-class.md)

[<span data-ttu-id="83c85-210">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="83c85-210">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
