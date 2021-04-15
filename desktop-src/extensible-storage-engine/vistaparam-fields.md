---
description: 'Saiba mais sobre: campos VistaParam'
title: Campos VistaParam (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: VistaParam fields
ms:assetid: Fields.T:Microsoft.Isam.Esent.Interop.Vista.VistaParam
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam_fields(v=EXCHG.10)
ms:contentKeyID: 55104336
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 6e20c4b784b9a4421c447f24d5736d7c6ef67f41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568118"
---
# <a name="vistaparam-fields"></a><span data-ttu-id="ce36d-103">Campos VistaParam</span><span class="sxs-lookup"><span data-stu-id="ce36d-103">VistaParam fields</span></span>

<span data-ttu-id="ce36d-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="ce36d-104">Include protected members</span></span>  
<span data-ttu-id="ce36d-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="ce36d-105">Include inherited members</span></span>  

<span data-ttu-id="ce36d-106">O tipo [VistaParam](./vistaparam-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="ce36d-106">The [VistaParam](./vistaparam-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="ce36d-107">Campos</span><span class="sxs-lookup"><span data-stu-id="ce36d-107">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ce36d-108">Nome</span><span class="sxs-lookup"><span data-stu-id="ce36d-108">Name</span></span></th>
<th><span data-ttu-id="ce36d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce36d-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="ce36d-112"><a href="dn335379(v=exchg.10).md">CachedClosedTables</a></span><span class="sxs-lookup"><span data-stu-id="ce36d-112"><a href="dn335379(v=exchg.10).md">CachedClosedTables</a></span></span></td>
<td><span data-ttu-id="ce36d-113">Esse parâmetro controla o número de recursos da árvore B + em cache pela instância depois que as tabelas que eles representam foram fechadas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ce36d-113">This parameter controls the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="ce36d-114">Valores grandes para esse parâmetro farão com que o mecanismo de banco de dados use mais memória, mas aumentará a velocidade com que um grande número de tabelas pode ser aberto aleatoriamente pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ce36d-114">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="ce36d-115">Isso é útil para aplicativos que têm um esquema com um número muito grande de tabelas.</span><span class="sxs-lookup"><span data-stu-id="ce36d-115">This is useful for applications that have a schema with a very large number of tables.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="ce36d-118"><a href="dn335289(v=exchg.10).md">Configuration</a></span><span class="sxs-lookup"><span data-stu-id="ce36d-118"><a href="dn335289(v=exchg.10).md">Configuration</a></span></span></td>
<td><span data-ttu-id="ce36d-119">Esse parâmetro expõe vários conjuntos de valores padrão para todo o conjunto de parâmetros do sistema.</span><span class="sxs-lookup"><span data-stu-id="ce36d-119">This parameter exposes multiple sets of default values for the entire set of system parameters.</span></span> <span data-ttu-id="ce36d-120">Quando esse parâmetro é definido como uma configuração específica, todos os valores de parâmetro do sistema são redefinidos para seus valores padrão para essa configuração.</span><span class="sxs-lookup"><span data-stu-id="ce36d-120">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="ce36d-121">Se a configuração for definida para uma instância específica, os parâmetros do sistema global não serão redefinidos para seus valores padrão.</span><span class="sxs-lookup"><span data-stu-id="ce36d-121">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="ce36d-122">Configuração pequena (0): o mecanismo de banco de dados é otimizado para uso de memória.</span><span class="sxs-lookup"><span data-stu-id="ce36d-122">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="ce36d-123">Configuração herdada (1): o mecanismo de banco de dados tem seus padrões tradicionais.</span><span class="sxs-lookup"><span data-stu-id="ce36d-123">Legacy Configuration (1): The database engine has its traditional defaults.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="ce36d-126"><a href="dn335380(v=exchg.10).md">EnableAdvanced</a></span><span class="sxs-lookup"><span data-stu-id="ce36d-126"><a href="dn335380(v=exchg.10).md">EnableAdvanced</a></span></span></td>
<td><span data-ttu-id="ce36d-127">Esse parâmetro é usado para controlar quando o mecanismo de banco de dados aceita ou rejeita alterações em um subconjunto dos parâmetros do sistema.</span><span class="sxs-lookup"><span data-stu-id="ce36d-127">This parameter is used to control when the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="ce36d-128">Esse parâmetro é usado em conjunto com a <a href="dn335289(v=exchg.10).md">configuração</a> para impedir que alguns parâmetros do sistema sejam definidos fora dos padrões da configuração selecionada.</span><span class="sxs-lookup"><span data-stu-id="ce36d-128">This parameter is used in conjunction with <a href="dn335289(v=exchg.10).md">Configuration</a> to prevent some system parameters from being set away from the selected configuration's defaults.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="ce36d-131"><a href="dn335291(v=exchg.10).md">EnableFileCache</a></span><span class="sxs-lookup"><span data-stu-id="ce36d-131"><a href="dn335291(v=exchg.10).md">EnableFileCache</a></span></span></td>
<td><span data-ttu-id="ce36d-132">Habilite o uso do cache de arquivos do so para todos os arquivos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="ce36d-132">Enable the use of the OS file cache for all managed files.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="ce36d-135"><a href="dn335381(v=exchg.10).md">EnableViewCache</a></span><span class="sxs-lookup"><span data-stu-id="ce36d-135"><a href="dn335381(v=exchg.10).md">EnableViewCache</a></span></span></td>
<td><span data-ttu-id="ce36d-136">Habilite o uso de e/s de arquivo mapeado de memória para arquivos de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ce36d-136">Enable the use of memory mapped file I/O for database files.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="ce36d-139"><a href="dn335292(v=exchg.10).md">Mais</a></span><span class="sxs-lookup"><span data-stu-id="ce36d-139"><a href="dn335292(v=exchg.10).md">KeyMost</a></span></span></td>
<td><span data-ttu-id="ce36d-140">Esse parâmetro somente leitura indica o comprimento máximo de chave de índice permitido que pode ser selecionado para o tamanho da página do banco de dados atual (conforme configurado por <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>).</span><span class="sxs-lookup"><span data-stu-id="ce36d-140">This read-only parameter indicates the maximum allowable index key length that can be selected for the current database page size (as configured by <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="ce36d-143"><a href="dn335384(v=exchg.10).md">LegacyFileNames</a></span><span class="sxs-lookup"><span data-stu-id="ce36d-143"><a href="dn335384(v=exchg.10).md">LegacyFileNames</a></span></span></td>
<td><span data-ttu-id="ce36d-144">Esse parâmetro fornece compatibilidade com versões anteriores do mecanismo de banco de dados para as convenções de nomenclatura do arquivo.</span><span class="sxs-lookup"><span data-stu-id="ce36d-144">This parameter provides backwards compatibility with the file naming conventions of earlier releases of the database engine.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="ce36d-147"><a href="dn335294(v=exchg.10).md">TableClass10Name</a></span><span class="sxs-lookup"><span data-stu-id="ce36d-147"><a href="dn335294(v=exchg.10).md">TableClass10Name</a></span></span></td>
<td><span data-ttu-id="ce36d-148">Defina o nome associado à classe de tabela 10.</span><span class="sxs-lookup"><span data-stu-id="ce36d-148">Set the name associated with table class 10.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="ce36d-151"><a href="dn335385(v=exchg.10).md">TableClass11Name</a></span><span class="sxs-lookup"><span data-stu-id="ce36d-151"><a href="dn335385(v=exchg.10).md">TableClass11Name</a></span></span></td>
<td><span data-ttu-id="ce36d-152">Defina o nome associado à tabela classe 11.</span><span class="sxs-lookup"><span data-stu-id="ce36d-152">Set the name associated with table class 11.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="ce36d-155"><a href="dn335387(v=exchg.10).md">TableClass12Name</a></span><span class="sxs-lookup"><span data-stu-id="ce36d-155"><a href="dn335387(v=exchg.10).md">TableClass12Name</a></span></span></td>
<td><span data-ttu-id="ce36d-156">Defina o nome associado à classe de tabela 12.</span><span class="sxs-lookup"><span data-stu-id="ce36d-156">Set the name associated with table class 12.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="ce36d-159"><a href="dn335388(v=exchg.10).md">TableClass13Name</a></span><span class="sxs-lookup"><span data-stu-id="ce36d-159"><a href="dn335388(v=exchg.10).md">TableClass13Name</a></span></span></td>
<td><span data-ttu-id="ce36d-160">Defina o nome associado à classe de tabela 13.</span><span class="sxs-lookup"><span data-stu-id="ce36d-160">Set the name associated with table class 13.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="ce36d-163"><a href="dn335295(v=exchg.10).md">TableClass14Name</a></span><span class="sxs-lookup"><span data-stu-id="ce36d-163"><a href="dn335295(v=exchg.10).md">TableClass14Name</a></span></span></td>
<td><span data-ttu-id="ce36d-164">Defina o nome associado à classe de tabela 14.</span><span class="sxs-lookup"><span data-stu-id="ce36d-164">Set the name associated with table class 14.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="ce36d-167"><a href="dn335390(v=exchg.10).md">TableClass15Name</a></span><span class="sxs-lookup"><span data-stu-id="ce36d-167"><a href="dn335390(v=exchg.10).md">TableClass15Name</a></span></span></td>
<td><span data-ttu-id="ce36d-168">Defina o nome associado à classe de tabela 15.</span><span class="sxs-lookup"><span data-stu-id="ce36d-168">Set the name associated with table class 15.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="ce36d-171"><a href="dn335297(v=exchg.10).md">TableClass1Name</a></span><span class="sxs-lookup"><span data-stu-id="ce36d-171"><a href="dn335297(v=exchg.10).md">TableClass1Name</a></span></span></td>
<td><span data-ttu-id="ce36d-172">Defina o nome associado à tabela classe 1.</span><span class="sxs-lookup"><span data-stu-id="ce36d-172">Set the name associated with table class 1.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="ce36d-175"><a href="dn335389(v=exchg.10).md">TableClass2Name</a></span><span class="sxs-lookup"><span data-stu-id="ce36d-175"><a href="dn335389(v=exchg.10).md">TableClass2Name</a></span></span></td>
<td><span data-ttu-id="ce36d-176">Defina o nome associado à tabela classe 2.</span><span class="sxs-lookup"><span data-stu-id="ce36d-176">Set the name associated with table class 2.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="ce36d-179"><a href="dn335296(v=exchg.10).md">TableClass3Name</a></span><span class="sxs-lookup"><span data-stu-id="ce36d-179"><a href="dn335296(v=exchg.10).md">TableClass3Name</a></span></span></td>
<td><span data-ttu-id="ce36d-180">Defina o nome associado à tabela classe 3.</span><span class="sxs-lookup"><span data-stu-id="ce36d-180">Set the name associated with table class 3.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="ce36d-183"><a href="dn335395(v=exchg.10).md">TableClass4Name</a></span><span class="sxs-lookup"><span data-stu-id="ce36d-183"><a href="dn335395(v=exchg.10).md">TableClass4Name</a></span></span></td>
<td><span data-ttu-id="ce36d-184">Defina o nome associado à tabela classe 4.</span><span class="sxs-lookup"><span data-stu-id="ce36d-184">Set the name associated with table class 4.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="ce36d-187"><a href="dn335401(v=exchg.10).md">TableClass5Name</a></span><span class="sxs-lookup"><span data-stu-id="ce36d-187"><a href="dn335401(v=exchg.10).md">TableClass5Name</a></span></span></td>
<td><span data-ttu-id="ce36d-188">Defina o nome associado à tabela classe 5.</span><span class="sxs-lookup"><span data-stu-id="ce36d-188">Set the name associated with table class 5.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="ce36d-191"><a href="dn335298(v=exchg.10).md">TableClass6Name</a></span><span class="sxs-lookup"><span data-stu-id="ce36d-191"><a href="dn335298(v=exchg.10).md">TableClass6Name</a></span></span></td>
<td><span data-ttu-id="ce36d-192">Defina o nome associado à tabela classe 6.</span><span class="sxs-lookup"><span data-stu-id="ce36d-192">Set the name associated with table class 6.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="ce36d-195"><a href="dn335402(v=exchg.10).md">TableClass7Name</a></span><span class="sxs-lookup"><span data-stu-id="ce36d-195"><a href="dn335402(v=exchg.10).md">TableClass7Name</a></span></span></td>
<td><span data-ttu-id="ce36d-196">Defina o nome associado à tabela classe 7.</span><span class="sxs-lookup"><span data-stu-id="ce36d-196">Set the name associated with table class 7.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="ce36d-199"><a href="dn335299(v=exchg.10).md">TableClass8Name</a></span><span class="sxs-lookup"><span data-stu-id="ce36d-199"><a href="dn335299(v=exchg.10).md">TableClass8Name</a></span></span></td>
<td><span data-ttu-id="ce36d-200">Defina o nome associado à classe de tabela 8.</span><span class="sxs-lookup"><span data-stu-id="ce36d-200">Set the name associated with table class 8.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="ce36d-203"><a href="dn335404(v=exchg.10).md">TableClass9Name</a></span><span class="sxs-lookup"><span data-stu-id="ce36d-203"><a href="dn335404(v=exchg.10).md">TableClass9Name</a></span></span></td>
<td><span data-ttu-id="ce36d-204">Defina o nome associado à classe de tabela 9.</span><span class="sxs-lookup"><span data-stu-id="ce36d-204">Set the name associated with table class 9.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ce36d-205">Parte superior</span><span class="sxs-lookup"><span data-stu-id="ce36d-205">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="ce36d-206">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce36d-206">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ce36d-207">Referência</span><span class="sxs-lookup"><span data-stu-id="ce36d-207">Reference</span></span>

[<span data-ttu-id="ce36d-208">Classe VistaParam</span><span class="sxs-lookup"><span data-stu-id="ce36d-208">VistaParam class</span></span>](./vistaparam-class.md)

[<span data-ttu-id="ce36d-209">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="ce36d-209">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
