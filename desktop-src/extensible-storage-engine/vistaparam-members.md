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
# <a name="vistaparam-members"></a>Membros do VistaParam

Incluir membros protegidos  
Incluir membros herdados  

Parâmetros do sistema que foram adicionados à versão vista do ESENT.

O tipo [VistaParam](./vistaparam-class.md) expõe os membros a seguir.

## <a name="fields"></a>Campos

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nome</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335379(v=exchg.10).md">CachedClosedTables</a></td>
<td>Esse parâmetro controla o número de recursos da árvore B + em cache pela instância depois que as tabelas que eles representam foram fechadas pelo aplicativo. Valores grandes para esse parâmetro farão com que o mecanismo de banco de dados use mais memória, mas aumentará a velocidade com que um grande número de tabelas pode ser aberto aleatoriamente pelo aplicativo. Isso é útil para aplicativos que têm um esquema com um número muito grande de tabelas.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335289(v=exchg.10).md">Configuration</a></td>
<td>Esse parâmetro expõe vários conjuntos de valores padrão para todo o conjunto de parâmetros do sistema. Quando esse parâmetro é definido como uma configuração específica, todos os valores de parâmetro do sistema são redefinidos para seus valores padrão para essa configuração. Se a configuração for definida para uma instância específica, os parâmetros do sistema global não serão redefinidos para seus valores padrão. Configuração pequena (0): o mecanismo de banco de dados é otimizado para uso de memória. Configuração herdada (1): o mecanismo de banco de dados tem seus padrões tradicionais.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335380(v=exchg.10).md">EnableAdvanced</a></td>
<td>Esse parâmetro é usado para controlar quando o mecanismo de banco de dados aceita ou rejeita alterações em um subconjunto dos parâmetros do sistema. Esse parâmetro é usado em conjunto com a <a href="dn335289(v=exchg.10).md">configuração</a> para impedir que alguns parâmetros do sistema sejam definidos fora dos padrões da configuração selecionada.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335291(v=exchg.10).md">EnableFileCache</a></td>
<td>Habilite o uso do cache de arquivos do so para todos os arquivos gerenciados.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335381(v=exchg.10).md">EnableViewCache</a></td>
<td>Habilite o uso de e/s de arquivo mapeado de memória para arquivos de banco de dados.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335292(v=exchg.10).md">Mais</a></td>
<td>Esse parâmetro somente leitura indica o comprimento máximo de chave de índice permitido que pode ser selecionado para o tamanho da página do banco de dados atual (conforme configurado por <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335384(v=exchg.10).md">LegacyFileNames</a></td>
<td>Esse parâmetro fornece compatibilidade com versões anteriores do mecanismo de banco de dados para as convenções de nomenclatura do arquivo.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335294(v=exchg.10).md">TableClass10Name</a></td>
<td>Defina o nome associado à classe de tabela 10.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335385(v=exchg.10).md">TableClass11Name</a></td>
<td>Defina o nome associado à tabela classe 11.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335387(v=exchg.10).md">TableClass12Name</a></td>
<td>Defina o nome associado à classe de tabela 12.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335388(v=exchg.10).md">TableClass13Name</a></td>
<td>Defina o nome associado à classe de tabela 13.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335295(v=exchg.10).md">TableClass14Name</a></td>
<td>Defina o nome associado à classe de tabela 14.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335390(v=exchg.10).md">TableClass15Name</a></td>
<td>Defina o nome associado à classe de tabela 15.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335297(v=exchg.10).md">TableClass1Name</a></td>
<td>Defina o nome associado à tabela classe 1.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335389(v=exchg.10).md">TableClass2Name</a></td>
<td>Defina o nome associado à tabela classe 2.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335296(v=exchg.10).md">TableClass3Name</a></td>
<td>Defina o nome associado à tabela classe 3.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335395(v=exchg.10).md">TableClass4Name</a></td>
<td>Defina o nome associado à tabela classe 4.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335401(v=exchg.10).md">TableClass5Name</a></td>
<td>Defina o nome associado à tabela classe 5.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335298(v=exchg.10).md">TableClass6Name</a></td>
<td>Defina o nome associado à tabela classe 6.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335402(v=exchg.10).md">TableClass7Name</a></td>
<td>Defina o nome associado à tabela classe 7.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335299(v=exchg.10).md">TableClass8Name</a></td>
<td>Defina o nome associado à classe de tabela 8.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335404(v=exchg.10).md">TableClass9Name</a></td>
<td>Defina o nome associado à classe de tabela 9.</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe VistaParam](./vistaparam-class.md)

[Namespace Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
