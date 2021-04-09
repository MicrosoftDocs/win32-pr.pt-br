---
description: 'Saiba mais sobre: membros do DurableCommitCallback'
title: Membros DurableCommitCallback (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: DurableCommitCallback members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.durablecommitcallback_members(v=EXCHG.10)
ms:contentKeyID: 55104391
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 47086ba03982e21703ca89c2da41121824121cb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011501"
---
# <a name="durablecommitcallback-members"></a>Membros do DurableCommitCallback

Incluir membros protegidos  
Incluir membros herdados  

Encapsula o retorno de chamada lidando com confirmações duráveis.

O tipo [DurableCommitCallback](./durablecommitcallback-class.md) expõe os membros a seguir.

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
<td><a href="dn335324(v=exchg.10).md">DurableCommitCallback</a></td>
<td>Inicializa uma nova instância da classe <a href="dn335323(v=exchg.10).md">DurableCommitCallback</a> .</td>
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
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Propriedade protegida" alt="Protected property" /></td>
<td><a href="dn350578(v=exchg.10).md">HasResource</a></td>
<td>Obtém um valor que indica se o recurso subjacente está alocado no momento. (Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</td>
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
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></td>
<td>Gerar uma exceção se esse objeto tiver sido descartado. (Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn350553(v=exchg.10).md">Dispose ()</a></td>
<td>Descartar este objeto, liberando o recurso ESENT subjacente. (Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="dn350543(v=exchg.10).md">Dispose (booliano)</a></td>
<td>Chamado por Dispose e o finalizador. (Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn335442(v=exchg.10).md">Completo</a></td>
<td>Encerra a sessão de confirmação durável.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Igual a</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="dn350552(v=exchg.10).md">Finalizar</a></td>
<td>Finaliza uma instância da classe EsentResource. (Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="dn335327(v=exchg.10).md">ReleaseResource</a></td>
<td>Libera a sessão de confirmação durável. (Substitui <a href="dn350545(v=exchg.10).md">EsentResource. ReleaseResource ()</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></td>
<td>Chamado por uma subclasse quando um recurso é alocado. (Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></td>
<td>Chamado por uma subclasse quando um recurso é liberado. (Herdado de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn335445(v=exchg.10).md">ToString</a></td>
<td>Gera uma representação de cadeia de caracteres da estrutura. (Substitui <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe DurableCommitCallback](./durablecommitcallback-class.md)

[Namespace Microsoft. ISAM. ESENT. Interop. windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
