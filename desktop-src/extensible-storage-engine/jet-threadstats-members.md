---
description: 'Saiba mais sobre: JET_THREADSTATS membros'
title: JET_THREADSTATS (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: JET_THREADSTATS members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats_members(v=EXCHG.10)
ms:contentKeyID: 39514028
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 13713d00431337f5e2190e2f547729e96a7cfb634fe1a95dddba570a9236f1f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890276"
---
# <a name="jet_threadstats-members"></a>JET_THREADSTATS membros

Incluir membros protegidos  
Incluir membros herdados  

Contém estatísticas cumulativas sobre o trabalho executado pelo mecanismo de banco de dados no thread atual. Essas informações são retornadas por meio de JetGetThreadStats.

O [JET_THREADSTATS](./jet-threadstats-structure2.md) tipo expõe os membros a seguir.

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
<td><a href="hh578305(v=exchg.10).md">cbLogRecord</a></td>
<td>Obtém o tamanho total, em bytes, dos registros de log de transações que foram gerados pelo mecanismo de banco de dados no thread atual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="hh578110(v=exchg.10).md">cLogRecord</a></td>
<td>Obtém o número total de registros de log de transações que foram gerados pelo mecanismo de banco de dados no thread atual.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="hh578651(v=exchg.10).md">cPageDirtied</a></td>
<td>Obtém o número total de páginas de banco de dados, sem alterações não escritas, que foram modificadas pelo mecanismo de banco de dados no thread atual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="hh557376(v=exchg.10).md">cPagePreread</a></td>
<td>Obtém o número total de páginas de banco de dados pré-buscadas do disco pelo mecanismo de banco de dados no thread atual.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="hh163392(v=exchg.10).md">cPageRead</a></td>
<td>Obtém o número total de páginas de banco de dados buscadas do disco pelo mecanismo de banco de dados no thread atual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="hh596234(v=exchg.10).md">cPageRedirtied</a></td>
<td>Obtém o número total de páginas de banco de dados, com alterações não escritas, que foram modificadas pelo mecanismo de banco de dados no thread atual.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /></td>
<td><a href="hh557174(v=exchg.10).md">cPageReferenced</a></td>
<td>Obtém o número total de páginas de banco de dados visitadas pelo mecanismo de banco de dados no thread atual.</td>
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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="hh565584(v=exchg.10).md">Adicionar</a></td>
<td>Adicione as estatísticas em duas estruturas JET_THREADSTATS dados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="hh538903(v=exchg.10).md">Criar</a></td>
<td>Crie um <a href="hh578565(v=exchg.10).md">novo JET_THREADSTATS</a> struct com o valor especificado.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="hh557146(v=exchg.10).md">Equals(Object)</a></td>
<td>Retorna um valor que indica se essa instância é igual a outra instância. (Substitui <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType.Equals(Object)</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="hh596601(v=exchg.10).md">Equals(JET_THREADSTATS)</a></td>
<td>Retorna um valor que indica se essa instância é igual a outra instância.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizar</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="hh579156(v=exchg.10).md">GetHashCode</a></td>
<td>Retorna o código hash para a instância. (Substitui <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType.GetHashCode()</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">Gettype</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">Memberwiseclone</a></td>
<td>(Herdado do <a href="/dotnet/api/system.object">objeto</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="hh579433(v=exchg.10).md">Subtract</a></td>
<td>Calcule a diferença nas estatísticas entre duas estruturas JET_THREADSTATS dados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="hh558249(v=exchg.10).md">ToString</a></td>
<td>Obtém uma representação de cadeia de caracteres desse objeto. (Substitui <a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ValueType.ToString()</a>.)</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="operators"></a>Operadores

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
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operador público" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="hh163281(v=exchg.10).md">Adição</a></td>
<td>Adicione as estatísticas em duas estruturas JET_THREADSTATS dados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operador público" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="hh558521(v=exchg.10).md">Igualitário</a></td>
<td>Determina se duas instâncias especificadas do JET_THREADSTATS são iguais.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operador público" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="hh577527(v=exchg.10).md">Desigualdade</a></td>
<td>Determina se duas instâncias especificadas do JET_THREADSTATS são iguais.</td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operador público" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="hh557686(v=exchg.10).md">Subtração</a></td>
<td>Calcule a diferença nas estatísticas entre duas estruturas JET_THREADSTATS dados.</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[JET_THREADSTATS estrutura](./jet-threadstats-structure2.md)

[Namespace Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
