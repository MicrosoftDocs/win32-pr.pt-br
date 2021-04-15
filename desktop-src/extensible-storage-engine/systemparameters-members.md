---
description: 'Saiba mais sobre: membros do SystemParameters'
title: Membros do SystemParameters
TOCTitle: SystemParameters members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.SystemParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters_members(v=EXCHG.10)
ms:contentKeyID: 55104101
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: e317ef4e63a33951dc55e030718d226ae3eaeec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104554486"
---
# <a name="systemparameters-members"></a><span data-ttu-id="3658d-103">Membros do SystemParameters</span><span class="sxs-lookup"><span data-stu-id="3658d-103">SystemParameters members</span></span>

<span data-ttu-id="3658d-104">Incluir membros protegidos</span><span class="sxs-lookup"><span data-stu-id="3658d-104">Include protected members</span></span>  
<span data-ttu-id="3658d-105">Incluir membros herdados</span><span class="sxs-lookup"><span data-stu-id="3658d-105">Include inherited members</span></span>  

<span data-ttu-id="3658d-106">Constantes para a API ESENT.</span><span class="sxs-lookup"><span data-stu-id="3658d-106">Constants for the ESENT API.</span></span> <span data-ttu-id="3658d-107">Eles não precisam ser pesquisados por meio de parâmetros do sistema.</span><span class="sxs-lookup"><span data-stu-id="3658d-107">These don't have to be looked up via system parameters.</span></span> <span data-ttu-id="3658d-108">Essa classe fornece propriedades estáticas para definir e obter parâmetros de sistema ESENT globais.</span><span class="sxs-lookup"><span data-stu-id="3658d-108">This class provides static properties to set and get global ESENT system parameters.</span></span> <span data-ttu-id="3658d-109">Essa classe fornece propriedades estáticas para definir e obter parâmetros de sistema ESENT globais.</span><span class="sxs-lookup"><span data-stu-id="3658d-109">This class provides static properties to set and get global ESENT system parameters.</span></span>

<span data-ttu-id="3658d-110">O tipo [SystemParameters](./systemparameters-class.md) expõe os membros a seguir.</span><span class="sxs-lookup"><span data-stu-id="3658d-110">The [SystemParameters](./systemparameters-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="3658d-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3658d-111">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="3658d-112">Nome</span><span class="sxs-lookup"><span data-stu-id="3658d-112">Name</span></span></th>
<th><span data-ttu-id="3658d-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="3658d-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-116"><a href="dn351215(v=exchg.10).md">BookmarkMost</a></span><span class="sxs-lookup"><span data-stu-id="3658d-116"><a href="dn351215(v=exchg.10).md">BookmarkMost</a></span></span></td>
<td><span data-ttu-id="3658d-117">Obtém o tamanho máximo de um indicador.</span><span class="sxs-lookup"><span data-stu-id="3658d-117">Gets the maximum size of a bookmark.</span></span> <span data-ttu-id="3658d-118"><a href="dn292149(v=exchg.10).md">JetGetBookmark (JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</span><span class="sxs-lookup"><span data-stu-id="3658d-118"><a href="dn292149(v=exchg.10).md">JetGetBookmark(JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-121"><a href="dn351214(v=exchg.10).md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="3658d-121"><a href="dn351214(v=exchg.10).md">CacheSize</a></span></span></td>
<td><span data-ttu-id="3658d-122">Obtém ou define o tamanho do cache de banco de dados em páginas.</span><span class="sxs-lookup"><span data-stu-id="3658d-122">Gets or sets the size of the database cache in pages.</span></span> <span data-ttu-id="3658d-123">Por padrão, o cache do banco de dados ajustará automaticamente seu tamanho, a definição dessa propriedade com um valor diferente de zero fará com que o cache se ajuste ao tamanho do destino.</span><span class="sxs-lookup"><span data-stu-id="3658d-123">By default the database cache will automatically tune its size, setting this property to a non-zero value will cause the cache to adjust itself to the target size.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-126"><a href="dn351149(v=exchg.10).md">CacheSizeMax</a></span><span class="sxs-lookup"><span data-stu-id="3658d-126"><a href="dn351149(v=exchg.10).md">CacheSizeMax</a></span></span></td>
<td><span data-ttu-id="3658d-127">Obtém ou define o tamanho máximo do cache de página do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3658d-127">Gets or sets the maximum size of the database page cache.</span></span> <span data-ttu-id="3658d-128">O tamanho está em páginas de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3658d-128">The size is in database pages.</span></span> <span data-ttu-id="3658d-129">Se esse parâmetro for deixado para seu valor padrão, o tamanho máximo do cache será definido como o tamanho da memória física quando JetInit for chamado.</span><span class="sxs-lookup"><span data-stu-id="3658d-129">If this parameter is left to its default value, then the maximum size of the cache will be set to the size of physical memory when JetInit is called.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-132"><a href="dn351216(v=exchg.10).md">CacheSizeMin</a></span><span class="sxs-lookup"><span data-stu-id="3658d-132"><a href="dn351216(v=exchg.10).md">CacheSizeMin</a></span></span></td>
<td><span data-ttu-id="3658d-133">Obtém ou define o tamanho mínimo do cache de página de banco de dados, em páginas de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3658d-133">Gets or sets the minimum size of the database page cache, in database pages.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-136"><a href="dn351151(v=exchg.10).md">ColumnsKeyMost</a></span><span class="sxs-lookup"><span data-stu-id="3658d-136"><a href="dn351151(v=exchg.10).md">ColumnsKeyMost</a></span></span></td>
<td><span data-ttu-id="3658d-137">Obtém o número máximo de componentes em uma chave de classificação ou de índice.</span><span class="sxs-lookup"><span data-stu-id="3658d-137">Gets the maximum number of components in a sort or index key.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-140"><a href="dn351218(v=exchg.10).md">Configuration</a></span><span class="sxs-lookup"><span data-stu-id="3658d-140"><a href="dn351218(v=exchg.10).md">Configuration</a></span></span></td>
<td><span data-ttu-id="3658d-141">Obtém ou define um valor que especifica os valores padrão para o conjunto inteiro de parâmetros do sistema.</span><span class="sxs-lookup"><span data-stu-id="3658d-141">Gets or sets a value specifying the default values for the entire set of system parameters.</span></span> <span data-ttu-id="3658d-142">Quando esse parâmetro é definido como uma configuração específica, todos os valores de parâmetro do sistema são redefinidos para seus valores padrão para essa configuração.</span><span class="sxs-lookup"><span data-stu-id="3658d-142">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="3658d-143">Se a configuração for definida para uma instância específica, os parâmetros do sistema global não serão redefinidos para seus valores padrão.</span><span class="sxs-lookup"><span data-stu-id="3658d-143">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="3658d-144">Configuração pequena (0): o mecanismo de banco de dados é otimizado para uso de memória.</span><span class="sxs-lookup"><span data-stu-id="3658d-144">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="3658d-145">Configuração herdada (1): o mecanismo de banco de dados tem seus padrões tradicionais.</span><span class="sxs-lookup"><span data-stu-id="3658d-145">Legacy Configuration (1): The database engine has its traditional defaults.</span></span> <span data-ttu-id="3658d-146">Com suporte no Windows Vista e em cima.</span><span class="sxs-lookup"><span data-stu-id="3658d-146">Supported on Windows Vista and up.</span></span> <span data-ttu-id="3658d-147">Ignorado no Windows XP e no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3658d-147">Ignored on Windows XP and Windows Server 2003.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-150"><a href="dn351153(v=exchg.10).md">DatabasePageSize</a></span><span class="sxs-lookup"><span data-stu-id="3658d-150"><a href="dn351153(v=exchg.10).md">DatabasePageSize</a></span></span></td>
<td><span data-ttu-id="3658d-151">Obtém ou define o tamanho das páginas do banco de dados, em bytes.</span><span class="sxs-lookup"><span data-stu-id="3658d-151">Gets or sets the size of the database pages, in bytes.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-154"><a href="dn351221(v=exchg.10).md">EnableAdvanced</a></span><span class="sxs-lookup"><span data-stu-id="3658d-154"><a href="dn351221(v=exchg.10).md">EnableAdvanced</a></span></span></td>
<td><span data-ttu-id="3658d-155">Obtém ou define um valor que indica se o mecanismo de banco de dados aceita ou rejeita alterações em um subconjunto dos parâmetros do sistema.</span><span class="sxs-lookup"><span data-stu-id="3658d-155">Gets or sets a value indicating whether the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="3658d-156">Esse parâmetro é usado em conjunto com a <a href="dn351218(v=exchg.10).md">configuração</a> para impedir que alguns parâmetros do sistema sejam definidos fora dos padrões da configuração selecionada.</span><span class="sxs-lookup"><span data-stu-id="3658d-156">This parameter is used in conjunction with <a href="dn351218(v=exchg.10).md">Configuration</a> to prevent some system parameters from being set away from the selected configuration's defaults.</span></span> <span data-ttu-id="3658d-157">Com suporte no Windows Vista e em cima.</span><span class="sxs-lookup"><span data-stu-id="3658d-157">Supported on Windows Vista and up.</span></span> <span data-ttu-id="3658d-158">Ignorado no Windows XP e no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3658d-158">Ignored on Windows XP and Windows Server 2003.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-161"><a href="dn351152(v=exchg.10).md">EnableFileCache</a></span><span class="sxs-lookup"><span data-stu-id="3658d-161"><a href="dn351152(v=exchg.10).md">EnableFileCache</a></span></span></td>
<td><span data-ttu-id="3658d-162">Obtém ou define um valor que indica se o mecanismo de banco de dados deve usar o cache de arquivos do so para todos os arquivos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="3658d-162">Gets or sets a value indicating whether the database engine should use the OS file cache for all managed files.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-165"><a href="dn351220(v=exchg.10).md">EnableViewCache</a></span><span class="sxs-lookup"><span data-stu-id="3658d-165"><a href="dn351220(v=exchg.10).md">EnableViewCache</a></span></span></td>
<td><span data-ttu-id="3658d-166">Obtém ou define um valor que indica se o mecanismo de banco de dados deve usar a e/s de arquivo mapeada de memória para arquivos de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3658d-166">Gets or sets a value indicating whether the database engine should use memory mapped file I/O for database files.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-169"><a href="dn351223(v=exchg.10).md">EventLoggingLevel</a></span><span class="sxs-lookup"><span data-stu-id="3658d-169"><a href="dn351223(v=exchg.10).md">EventLoggingLevel</a></span></span></td>
<td><span data-ttu-id="3658d-170">Obtém ou define o nível de detalhe das mensagens de log de eventos emitidas para o log de eventos pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3658d-170">Gets or sets the detail level of eventlog messages that are emitted to the eventlog by the database engine.</span></span> <span data-ttu-id="3658d-171">Números mais altos resultarão em mensagens de log de eventos mais detalhadas.</span><span class="sxs-lookup"><span data-stu-id="3658d-171">Higher numbers will result in more detailed eventlog messages.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-174"><a href="dn351154(v=exchg.10).md">Exceçãoaction</a></span><span class="sxs-lookup"><span data-stu-id="3658d-174"><a href="dn351154(v=exchg.10).md">ExceptionAction</a></span></span></td>
<td><span data-ttu-id="3658d-175">Obtém ou define o valor que codifica o que fazer com exceções geradas no JET.</span><span class="sxs-lookup"><span data-stu-id="3658d-175">Gets or sets the value encoding what to do with exceptions generated within JET.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-178"><a href="dn351227(v=exchg.10).md">HungIOActions</a></span><span class="sxs-lookup"><span data-stu-id="3658d-178"><a href="dn351227(v=exchg.10).md">HungIOActions</a></span></span></td>
<td><span data-ttu-id="3658d-179">Obtém ou define o conjunto de ações a serem executadas no IOs que aparecem travadas.</span><span class="sxs-lookup"><span data-stu-id="3658d-179">Gets or sets the set of actions to be taken on IOs that appear hung.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-182"><a href="dn351155(v=exchg.10).md">HungIOThreshold</a></span><span class="sxs-lookup"><span data-stu-id="3658d-182"><a href="dn351155(v=exchg.10).md">HungIOThreshold</a></span></span></td>
<td><span data-ttu-id="3658d-183">Obtém ou define o limite para o que é considerado uma e/s suspensa que deve ser tratada.</span><span class="sxs-lookup"><span data-stu-id="3658d-183">Gets or sets the threshold for what is considered a hung IO that should be acted upon.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-186"><a href="dn351156(v=exchg.10).md">Mais</a></span><span class="sxs-lookup"><span data-stu-id="3658d-186"><a href="dn351156(v=exchg.10).md">KeyMost</a></span></span></td>
<td><span data-ttu-id="3658d-187">Obtém o tamanho máximo da chave.</span><span class="sxs-lookup"><span data-stu-id="3658d-187">Gets the maximum key size.</span></span> <span data-ttu-id="3658d-188">Isso depende da versão do ESENT e do tamanho da página do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3658d-188">This depends on the Esent version and database page size.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-191"><a href="dn351229(v=exchg.10).md">LegacyFileNames</a></span><span class="sxs-lookup"><span data-stu-id="3658d-191"><a href="dn351229(v=exchg.10).md">LegacyFileNames</a></span></span></td>
<td><span data-ttu-id="3658d-192">Obtém ou define a compatibilidade com versões anteriores do mecanismo de banco de dados com as convenções de nomenclatura de arquivo.</span><span class="sxs-lookup"><span data-stu-id="3658d-192">Gets or sets backwards compatibility with the file naming conventions of earlier releases of the database engine.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-195"><a href="dn351157(v=exchg.10).md">LVChunkSizeMost</a></span><span class="sxs-lookup"><span data-stu-id="3658d-195"><a href="dn351157(v=exchg.10).md">LVChunkSizeMost</a></span></span></td>
<td><span data-ttu-id="3658d-196">Obtém o tamanho dos blocos LV.</span><span class="sxs-lookup"><span data-stu-id="3658d-196">Gets the lv chunks size.</span></span> <span data-ttu-id="3658d-197">Isso depende do tamanho da página do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3658d-197">This depends on the database page size.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-200"><a href="dn351230(v=exchg.10).md">MaxInstances</a></span><span class="sxs-lookup"><span data-stu-id="3658d-200"><a href="dn351230(v=exchg.10).md">MaxInstances</a></span></span></td>
<td><span data-ttu-id="3658d-201">Obtém ou define o número máximo de instâncias que podem ser criadas.</span><span class="sxs-lookup"><span data-stu-id="3658d-201">Gets or sets the maximum number of instances that can be created.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-204"><a href="dn351160(v=exchg.10).md">MinDataForXpress</a></span><span class="sxs-lookup"><span data-stu-id="3658d-204"><a href="dn351160(v=exchg.10).md">MinDataForXpress</a></span></span></td>
<td><span data-ttu-id="3658d-205">Obtém ou define a menor quantidade de dados que devem ser compactados com a compactação do Xpress.</span><span class="sxs-lookup"><span data-stu-id="3658d-205">Gets or sets the smallest amount of data that should be compressed with xpress compression.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-208"><a href="dn351159(v=exchg.10).md">OutstandingIOMax</a></span><span class="sxs-lookup"><span data-stu-id="3658d-208"><a href="dn351159(v=exchg.10).md">OutstandingIOMax</a></span></span></td>
<td><span data-ttu-id="3658d-209">Esse parâmetro controla quantas e/SS de arquivo de banco de dados podem ser enfileiradas por disco no sistema operacional do host ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="3658d-209">This parameter controls how many database file I/Os can be queued per-disk in the host operating system at one time.</span></span> <span data-ttu-id="3658d-210">Um valor maior para esse parâmetro pode ajudar significativamente o desempenho de um aplicativo de banco de dados grande.</span><span class="sxs-lookup"><span data-stu-id="3658d-210">A larger value for this parameter can significantly help the performance of a large database application.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-213"><a href="dn351158(v=exchg.10).md">ProcessFriendlyName</a></span><span class="sxs-lookup"><span data-stu-id="3658d-213"><a href="dn351158(v=exchg.10).md">ProcessFriendlyName</a></span></span></td>
<td><span data-ttu-id="3658d-214">Obtém ou define o nome amigável para esta instância do processo.</span><span class="sxs-lookup"><span data-stu-id="3658d-214">Gets or sets the friendly name for this instance of the process.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-217"><a href="dn351161(v=exchg.10).md">StartFlushThreshold</a></span><span class="sxs-lookup"><span data-stu-id="3658d-217"><a href="dn351161(v=exchg.10).md">StartFlushThreshold</a></span></span></td>
<td><span data-ttu-id="3658d-218">Obtém ou define o limite no qual o cache da página do banco de dados começa a remover páginas do cache para liberar espaço para páginas que não estão armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="3658d-218">Gets or sets the threshold at which the database page cache begins evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="3658d-219">Quando o número de buffers de página no cache cair abaixo desse limite, um processo em segundo plano será iniciado para reabastecer o pool de buffers disponíveis.</span><span class="sxs-lookup"><span data-stu-id="3658d-219">When the number of page buffers in the cache drops below this threshold then a background process will be started to replenish that pool of available buffers.</span></span> <span data-ttu-id="3658d-220">Esse limite é sempre relativo ao tamanho máximo do cache, conforme definido por JET_paramCacheSizeMax.</span><span class="sxs-lookup"><span data-stu-id="3658d-220">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="3658d-221">Esse limite também deve ser menor que o limite de parada definido por JET_paramStopFlushThreshold.</span><span class="sxs-lookup"><span data-stu-id="3658d-221">This threshold must also always be less than the stop threshold as set by JET_paramStopFlushThreshold.</span></span> <span data-ttu-id="3658d-222">A altura da distância do limite inicial determinará o tempo de resposta que o cache da página do banco de dados deve ter para produzir os buffers disponíveis antes que o aplicativo precise deles.</span><span class="sxs-lookup"><span data-stu-id="3658d-222">The distance height of the start threshold will determine the response time that the database page cache must have to produce available buffers before the application needs them.</span></span> <span data-ttu-id="3658d-223">Um limite de início alto dará ao processo em segundo plano mais tempo para reagir.</span><span class="sxs-lookup"><span data-stu-id="3658d-223">A high start threshold will give the background process more time to react.</span></span> <span data-ttu-id="3658d-224">No entanto, um limite de início alto implica um limite de parada maior e reduzirá o tamanho efetivo do cache de página do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3658d-224">However, a high start threshold implies a higher stop threshold and that will reduce the effective size of the database page cache.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-227"><a href="dn351231(v=exchg.10).md">StopFlushThreshold</a></span><span class="sxs-lookup"><span data-stu-id="3658d-227"><a href="dn351231(v=exchg.10).md">StopFlushThreshold</a></span></span></td>
<td><span data-ttu-id="3658d-228">Obtém ou define o limite no qual o cache da página do banco de dados encerra a remoção de páginas do cache para liberar espaço para páginas que não são armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="3658d-228">Gets or sets the threshold at which the database page cache ends evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="3658d-229">Quando o número de buffers de página no cache ultrapassar esse limite, o processo em segundo plano que foi iniciado para reabastecer o pool de buffers disponíveis será interrompido.</span><span class="sxs-lookup"><span data-stu-id="3658d-229">When the number of page buffers in the cache rises above this threshold then the background process that was started to replenish that pool of available buffers is stopped.</span></span> <span data-ttu-id="3658d-230">Esse limite é sempre relativo ao tamanho máximo do cache, conforme definido por JET_paramCacheSizeMax.</span><span class="sxs-lookup"><span data-stu-id="3658d-230">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="3658d-231">Esse limite também deve ser maior que o limite de início definido por JET_paramStartFlushThreshold.</span><span class="sxs-lookup"><span data-stu-id="3658d-231">This threshold must also always be greater than the start threshold as set by JET_paramStartFlushThreshold.</span></span> <span data-ttu-id="3658d-232">A distância entre o limite inicial e o limite de interrupção afeta a eficiência com a qual as páginas de banco de dados são liberadas pelo processo em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="3658d-232">The distance between the start threshold and the stop threshold affects the efficiency with which database pages are flushed by the background process.</span></span> <span data-ttu-id="3658d-233">Um intervalo maior fará com que seja mais provável que as gravações nas páginas vizinhas possam ser combinadas.</span><span class="sxs-lookup"><span data-stu-id="3658d-233">A larger gap will make it more likely that writes to neighboring pages may be combined.</span></span> <span data-ttu-id="3658d-234">No entanto, um limite de interrupção alto reduzirá o tamanho efetivo do cache de página do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3658d-234">However, a high stop threshold will reduce the effective size of the database page cache.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3658d-235">Parte superior</span><span class="sxs-lookup"><span data-stu-id="3658d-235">Top</span></span>

## <a name="fields"></a><span data-ttu-id="3658d-236">Campos</span><span class="sxs-lookup"><span data-stu-id="3658d-236">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="3658d-237">Nome</span><span class="sxs-lookup"><span data-stu-id="3658d-237">Name</span></span></th>
<th><span data-ttu-id="3658d-238">Descrição</span><span class="sxs-lookup"><span data-stu-id="3658d-238">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-241"><a href="dn351208(v=exchg.10).md">BaseNameLength</a></span><span class="sxs-lookup"><span data-stu-id="3658d-241"><a href="dn351208(v=exchg.10).md">BaseNameLength</a></span></span></td>
<td><span data-ttu-id="3658d-242">O comprimento do prefixo usado para nomear arquivos usados pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3658d-242">The length of the prefix used to name files used by the database engine.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-245"><a href="dn351146(v=exchg.10).md">ColumnMost</a></span><span class="sxs-lookup"><span data-stu-id="3658d-245"><a href="dn351146(v=exchg.10).md">ColumnMost</a></span></span></td>
<td><span data-ttu-id="3658d-246">Tamanho máximo para colunas que não são JET_coltyp. LongBinary ou JET_coltyp. LONGTEXT.</span><span class="sxs-lookup"><span data-stu-id="3658d-246">Maximum size for columns which are not JET_coltyp.LongBinary or JET_coltyp.LongText.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-249"><a href="dn351210(v=exchg.10).md">ColumnsFixedMost</a></span><span class="sxs-lookup"><span data-stu-id="3658d-249"><a href="dn351210(v=exchg.10).md">ColumnsFixedMost</a></span></span></td>
<td><span data-ttu-id="3658d-250">Número máximo de colunas fixas permitidas em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="3658d-250">Maximum number of fixed columns allowed in a table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-253"><a href="dn351140(v=exchg.10).md">ColumnsMost</a></span><span class="sxs-lookup"><span data-stu-id="3658d-253"><a href="dn351140(v=exchg.10).md">ColumnsMost</a></span></span></td>
<td><span data-ttu-id="3658d-254">Número máximo de colunas permitidas em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="3658d-254">Maximum number of columns allowed in a table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-257"><a href="dn351148(v=exchg.10).md">ColumnsTaggedMost</a></span><span class="sxs-lookup"><span data-stu-id="3658d-257"><a href="dn351148(v=exchg.10).md">ColumnsTaggedMost</a></span></span></td>
<td><span data-ttu-id="3658d-258">Número máximo de colunas marcadas permitidas em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="3658d-258">Maximum number of tagged columns allowed in a table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-261"><a href="dn351212(v=exchg.10).md">ColumnsVarMost</a></span><span class="sxs-lookup"><span data-stu-id="3658d-261"><a href="dn351212(v=exchg.10).md">ColumnsVarMost</a></span></span></td>
<td><span data-ttu-id="3658d-262">Número máximo de colunas de comprimento variável permitido em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="3658d-262">Maximum number of variable-length columns allowed in a table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-265"><a href="dn351141(v=exchg.10).md">LocaleNameMaxLength</a></span><span class="sxs-lookup"><span data-stu-id="3658d-265"><a href="dn351141(v=exchg.10).md">LocaleNameMaxLength</a></span></span></td>
<td><span data-ttu-id="3658d-266">O comprimento máximo de um nome de localidade (LOCALE_NAME_MAX_LENGTH de Winnt. h).</span><span class="sxs-lookup"><span data-stu-id="3658d-266">The maximum length of a locale name (LOCALE_NAME_MAX_LENGTH from winnt.h).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-269"><a href="dn351213(v=exchg.10).md">NameMost</a></span><span class="sxs-lookup"><span data-stu-id="3658d-269"><a href="dn351213(v=exchg.10).md">NameMost</a></span></span></td>
<td><span data-ttu-id="3658d-270">Tamanho máximo de um nome de tabela/coluna/índice.</span><span class="sxs-lookup"><span data-stu-id="3658d-270">Maximum size of a table/column/index name.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><span data-ttu-id="3658d-273"><a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a></span><span class="sxs-lookup"><span data-stu-id="3658d-273"><a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a></span></span></td>
<td><span data-ttu-id="3658d-274">O número de páginas que fornece o menor banco de dados temporário possível.</span><span class="sxs-lookup"><span data-stu-id="3658d-274">The number of pages that gives the smallest possible temporary database.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3658d-275">Parte superior</span><span class="sxs-lookup"><span data-stu-id="3658d-275">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="3658d-276">Confira também</span><span class="sxs-lookup"><span data-stu-id="3658d-276">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3658d-277">Referência</span><span class="sxs-lookup"><span data-stu-id="3658d-277">Reference</span></span>

[<span data-ttu-id="3658d-278">Classe SystemParameters</span><span class="sxs-lookup"><span data-stu-id="3658d-278">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="3658d-279">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3658d-279">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
