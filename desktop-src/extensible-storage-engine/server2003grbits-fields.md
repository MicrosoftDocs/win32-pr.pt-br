---
description: 'Saiba mais sobre: campos Server2003Grbits'
title: Campos Server2003Grbits (Microsoft.Isam.Esent.Interop.Server2003)
TOCTitle: Server2003Grbits fields
ms:assetid: Fields.T:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits_fields(v=EXCHG.10)
ms:contentKeyID: 55104210
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 77db94da9f3a5dbec982b31c0ea3d673ffb6228a58f81adf644ff498a2cf4f84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118071668"
---
# <a name="server2003grbits-fields"></a>Campos Server2003Grbits

Incluir membros protegidos  
Incluir membros herdados  

O [tipo Server2003Grbits](./server2003grbits-class.md) expõe os membros a seguir.

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
<td>Se uma determinada coluna não estiver presente no registro e tiver um valor padrão definido pelo usuário, nenhum valor de coluna será retornado. Essa opção impedirá que o retorno de chamada que calcula o valor padrão definido pelo usuário para a coluna seja chamado ao enumerar os valores dessa coluna.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351284(v=exchg.10).md">ForwardOnly</a></td>
<td>Essa opção solicita que a tabela temporária seja criada somente se o gerenciador de tabela temporário puder usar a implementação otimizada para resultados intermediários da consulta. Se qualquer característica da tabela temporária impedir o uso dessa otimização, a operação falhará com JET_errCannotMaterializeForwardOnlySort. Um efeito colateral dessa opção é permitir que a tabela temporária contenha registros com chaves de índice duplicadas. Consulte <a href="hh558517(v=exchg.10).md">Exclusivo</a> para obter mais informações.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></td>
<td>Todas as transações confirmadas anteriormente por qualquer sessão que ainda não foram liberados para o arquivo de log de transações serão liberados imediatamente. Essa API aguardará até que as transações tenham sido liberados antes de retornar ao chamador. Essa opção pode ser usada mesmo se a sessão não estiver atualmente em uma transação. Essa opção não pode ser usada em combinação com qualquer outra opção.</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe Server2003Grbits](./server2003grbits-class.md)

[Namespace Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
