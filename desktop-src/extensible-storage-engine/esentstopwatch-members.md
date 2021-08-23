---
description: 'Saiba mais sobre: membros EsentStopwatch'
title: Membros EsentStopwatch
TOCTitle: EsentStopwatch members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.EsentStopwatch
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstopwatch_members(v=EXCHG.10)
ms:contentKeyID: 55102990
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: ba85376cc636cc8ed3765e88c9f8aeada5e6b8e638b627e22e881d833e9e1f5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732396"
---
# <a name="esentstopwatch-members"></a>Membros EsentStopwatch

Incluir membros protegidos  
Incluir membros herdados  

Fornece um conjunto de métodos e propriedades que você pode usar para medir estatísticas de trabalho ESENT para um thread. Se a versão atual do ESENT não for suportada por [JetGetThreadStats(JET_THREADSTATS),](./vistaapi.jetgetthreadstats-method.md) todas as estatísticas do ESENT serão 0.

O [tipo EsentStopwatch](./esentstopwatch-class.md) expõe os membros a seguir.

## <a name="constructors"></a>Construtores

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn334872(v=exchg.10).md">EsentStopwatch</a></td>
<td></td>
</tr>
</tbody>
</table>


Parte superior

## <a name="properties"></a>Propriedades

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
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn334934(v=exchg.10).md">Decorrido</a></td>
<td>Obtém o tempo total decorrido, medido pela instância atual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn334933(v=exchg.10).md">Isrunning</a></td>
<td>Obtém um valor que indica se o temporizador EsentStopwatch está em execução.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="dn334930(v=exchg.10).md">ThreadStats</a></td>
<td>Obtém o total de estatísticas de trabalho do ESENT medida pela instância atual.</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="methods"></a>Métodos

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Igual a</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizar</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">Gettype</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">Memberwiseclone</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn334869(v=exchg.10).md">Redefinir</a></td>
<td>Interrompe a medição de intervalo de tempo e redefine as estatísticas de thread.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn334931(v=exchg.10).md">Iniciar</a></td>
<td>Começa a medir o trabalho do ESENT.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334877(v=exchg.10).md">Startnew</a></td>
<td>Inicializa uma nova instância EsentStopwatch e começa a medir o tempo decorrido.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn334932(v=exchg.10).md">Parar</a></td>
<td>Interrompe a medição do trabalho do ESENT.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn334873(v=exchg.10).md">ToString</a></td>
<td>Retorna uma <a href="/dotnet/api/system.string">Cadeia de</a> Caracteres que representa o <a href="/dotnet/api/system.diagnostics.stopwatch">Stopwatch atual.</a> (Substitui <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe EsentStopwatch](./esentstopwatch-class.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
