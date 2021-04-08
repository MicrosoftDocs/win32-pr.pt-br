---
description: 'Saiba mais sobre: membros do Server2003Grbits'
title: Membros Server2003Grbits (Microsoft. ISAM. ESENT. Interop. Server2003)
TOCTitle: Server2003Grbits members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits_members(v=EXCHG.10)
ms:contentKeyID: 55107767
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 21008153606a6c35c76daf3c2758211f3fcdd42e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828636"
---
# <a name="server2003grbits-members"></a>Membros do Server2003Grbits

Incluir membros protegidos  
Incluir membros herdados  

Grbits que foram adicionados à versão 2003 do Windows Server do ESENT.

O tipo [Server2003Grbits](./server2003grbits-class.md) expõe os membros a seguir.

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
<td><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></td>
<td>Se uma determinada coluna não estiver presente no registro e tiver um valor padrão definido pelo usuário, nenhum valor de coluna será retornado. Essa opção impedirá o retorno de chamada que computa o valor padrão definido pelo usuário para que a coluna seja chamada ao enumerar os valores para essa coluna.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351284(v=exchg.10).md">ForwardOnly</a></td>
<td>Essa opção solicita que a tabela temporária só seja criada se o Gerenciador de tabelas temporárias puder usar a implementação otimizada para resultados de consulta intermediários. Se qualquer característica da tabela temporária impedir o uso dessa otimização, a operação falhará com JET_errCannotMaterializeForwardOnlySort. Um efeito colateral dessa opção é permitir que a tabela temporária contenha registros com chaves de índice duplicadas. Consulte <a href="hh558517(v=exchg.10).md">exclusivo</a> para obter mais informações.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></td>
<td>Todas as transações confirmadas anteriormente por qualquer sessão que ainda não foram liberadas para o arquivo de log de transações serão liberadas imediatamente. Essa API aguardará até que as transações sejam liberadas antes de retornar ao chamador. Essa opção pode ser usada mesmo que a sessão não esteja em uma transação no momento. Essa opção não pode ser usada em combinação com nenhuma outra opção.</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe Server2003Grbits](./server2003grbits-class.md)

[Namespace Microsoft. ISAM. ESENT. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
