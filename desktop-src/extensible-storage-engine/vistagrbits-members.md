---
description: 'Saiba mais sobre: Membros do VistaGrbits'
title: Membros do VistaGrbits (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: VistaGrbits members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits_members(v=EXCHG.10)
ms:contentKeyID: 55104213
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: be9908627d4351ec710fa6b1791d24779ab501b8e61bb342d96a3a0ec4afa87b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978156"
---
# <a name="vistagrbits-members"></a>Membros do VistaGrbits

Incluir membros protegidos  
Incluir membros herdados  

Grbits que foram adicionados à versão vista do ESENT.

O [tipo VistaGrbits](./vistagrbits-class.md) expõe os membros a seguir.

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
<td><a href="dn351283(v=exchg.10).md">ContinueAfterThaw</a></td>
<td>A sessão de instantâneo continua após JetOSSnapshotThaw e exigirá uma chamada de função JetOSSnapshotEnd.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335364(v=exchg.10).md">IndexCrossProduct</a></td>
<td>Especificar esse sinalizador para um índice que tem mais de uma coluna de chave que é uma coluna com valores múltiplos resultará na criação de uma entrada de índice para cada resultado de um produto cruzado de todos os valores nessas colunas de chave. Caso contrário, o índice teria apenas uma entrada para cada valor múltiplo na coluna de chave mais significativa que é uma coluna com valores múltiplos e cada uma dessas entradas de índice usaria o primeiro valor múltiplo de qualquer outra coluna de chave que são colunas com valores múltiplos. Por exemplo, se você especificou esse sinalizador para um índice sobre a coluna A que tem os valores vermelho e azul e sobre a coluna B que tem os valores 1 e 2, as seguintes entradas de índice serão &quot; criadas: &quot; &quot; vermelho , &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; 1 &quot; ; &quot; vermelho, &quot; &quot; 2 &quot; ; &quot; azul &quot; , &quot; 1 &quot; ; &quot; azul &quot; , &quot; 2 &quot; . Caso contrário, as seguintes entradas de índice seriam criadas: &quot; vermelho &quot; , &quot; 1 &quot; ; &quot; azul &quot; , &quot; 1 &quot; .</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335368(v=exchg.10).md">IndexDisallowTruncation</a></td>
<td>Especificar esse sinalizador fará com que qualquer atualização no índice que resulte em uma chave truncada falhe com <a href="hh564840(v=exchg.10).md">KeyTruncated.</a> Caso contrário, as chaves serão silenciosamente truncadas.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351285(v=exchg.10).md">IndexNestedTable</a></td>
<td>Indexe em várias colunas com vários valores, mas apenas com valores do mesmo itagSequence.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335282(v=exchg.10).md">LogStreamMustExist</a></td>
<td>Os logs de transação devem existir no diretório do arquivo de log (ou seja, não podem iniciar automaticamente um novo fluxo).</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335367(v=exchg.10).md">RecoveryWithoutUndo</a></td>
<td>Execute a recuperação, mas pare na fase Desfazer. Permite que todos os logs presentes sejam reproduzidos e, em seguida, logs adicionais posteriores podem ser copiados e reproduzidos.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335375(v=exchg.10).md">ReplayMissingMapEntryDB</a></td>
<td>Entrada de mapa de banco de dados ausente padrão para o mesmo local.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335283(v=exchg.10).md">TruncateDone</a></td>
<td>O mecanismo pode marcar os headers de banco de dados conforme apropriado (por exemplo, um backup completo concluído), mesmo que a chamada para truncar não tenha sido concluída.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn335371(v=exchg.10).md">TruncateLogsAfterRecovery</a></td>
<td>Na recuperação suave bem-sucedida, truncar arquivos de log.</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe VistaGrbits](./vistagrbits-class.md)

[Namespace Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
