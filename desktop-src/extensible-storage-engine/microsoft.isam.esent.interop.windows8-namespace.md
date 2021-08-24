---
description: 'Saiba mais sobre: namespace Microsoft.Isam.Esent.Interop.Windows8'
title: Namespace Microsoft.Isam.Esent.Interop.Windows8 ()
TOCTitle: '@NoTitle'
ms:assetid: N:Microsoft.Isam.Esent.Interop.Windows8
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8(v=EXCHG.10)
ms:contentKeyID: 55104389
ms.date: 07/30/2014
ms.topic: article
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8
dev_langs:
- CSharp
- JScript
- VB
- other
ms.openlocfilehash: 768064e19af76a03aa0d4f11c087f8d7ff7086b04cd1de46edfb504ba8e6be2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614467"
---
# <a name="microsoftisamesentinteropwindows8-namespace"></a>Namespace Microsoft.Isam.Esent.Interop.Windows8

## <a name="classes"></a>Classes

<table>
<thead>
<tr class="header">
<th> </th>
<th>Classe</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="Classe pública" alt="Public class" /></td>
<td><a href="dn335323(v=exchg.10).md">DurableCommitCallback</a></td>
<td>Envolve o retorno de chamada que lida com confirmações duráveis.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="Classe pública" alt="Public class" /></td>
<td><a href="dn335448(v=exchg.10).md">JET_COMMIT_ID</a></td>
<td>O contexto de informações cerca os dados emitidos JET_PFNEMITLOGDATA.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="Classe pública" alt="Public class" /></td>
<td><a href="dn335334(v=exchg.10).md">JET_ERRINFOBASIC</a></td>
<td>Contém as informações sobre um erro.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="Classe pública" alt="Public class" /></td>
<td><a href="dn335349(v=exchg.10).md">JET_INDEX_COLUMN</a></td>
<td>Contém a definição de filtro <a href="dn335382(v=exchg.10).md">para JetPrereadIndexRanges(JET_SESID, JET_TABLEID, [], Int32, Int32, Int32, [], PrereadIndexRangesGrbit)</a> e <a href="dn335383(v=exchg.10).md">JetSetCursorFilter(JET_SESID, JET_TABLEID, [], CursorFilterGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="Classe pública" alt="Public class" /></td>
<td><a href="dn335481(v=exchg.10).md">JET_INDEX_RANGE</a></td>
<td>Contém <a href="dn335382(v=exchg.10).md">definição para JetPrereadIndexRanges(JET_SESID, JET_TABLEID, [], Int32, Int32, Int32, [], PrereadIndexRangesGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="Classe pública" alt="Public class" /></td>
<td><a href="dn335490(v=exchg.10).md">Windows8Api</a></td>
<td>Chamadas à API introduzidas Windows 8.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="Classe pública" alt="Public class" /></td>
<td><a href="dn335391(v=exchg.10).md">Windows8Grbits</a></td>
<td>Parâmetros do sistema que foram introduzidos no Windows 8.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="Classe pública" alt="Public class" /></td>
<td><a href="dn335399(v=exchg.10).md">Windows8IdxInfo</a></td>
<td>Níveis de informações de coluna que foram adicionados à Windows 8 do ESENT.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292085.pubclass(EXCHG.10).gif" title="Classe pública" alt="Public class" /></td>
<td><a href="dn335398(v=exchg.10).md">Windows8Param</a></td>
<td>Parâmetros do sistema que foram introduzidos no Windows 8.</td>
</tr>
</tbody>
</table>


## <a name="delegates"></a>Delegados

<table>
<thead>
<tr class="header">
<th> </th>
<th>Delegar</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596136.pubdelegate(exchg.10).gif" title="Delegado público" alt="Public delegate" /></td>
<td><a href="dn335363(v=exchg.10).md">JET_PFNDURABLECOMMITCALLBACK</a></td>
<td>Retorno de chamada para JET_paramDurableCommitCallback.</td>
</tr>
</tbody>
</table>


## <a name="enumerations"></a>Enumerações

<table>
<thead>
<tr class="header">
<th> </th>
<th>Enumeração</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="Enumeração pública" alt="Public enumeration" /></td>
<td><a href="dn335440(v=exchg.10).md">CursorFilterGrbit</a></td>
<td>Opções passadas durante a configuração de filtros de cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="Enumeração pública" alt="Public enumeration" /></td>
<td><a href="dn335446(v=exchg.10).md">DurableCommitCallbackGrbit</a></td>
<td>Opções passadas para o retorno de chamada de liberação de log.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="Enumeração pública" alt="Public enumeration" /></td>
<td><a href="dn335447(v=exchg.10).md">ErrorInfoGrbit</a></td>
<td>Opções para <a href="dn335493(v=exchg.10).md">JetGetErrorInfo(JET_err, JET_ERRINFOBASIC)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="Enumeração pública" alt="Public enumeration" /></td>
<td><a href="dn335469(v=exchg.10).md">JET_ERRCAT</a></td>
<td>A categoria de erro. A hierarquia é a seguinte: JET_errcatError | |-- JET_errcatOperation | |-- JET_errcatFatal | |-- JET_errcatIO // problemas de E/S ruins, podem ou não ser transitórios. | |-- JET_errcatResource | |-- JET_errcatMemory // sem memória (todas as variantes) | |-- JET_errcatQuota | |-- JET_errcatDisk // sem espaço em disco (todas as variantes) |-- JET_errcatData | |-- JET_errcatCorruption | |-- JET_errcatInconsistent // normalmente causado por | | JET_errcatFragmentation |-- JET_errcatFragmentation |-- JET_errcatApi |-- JET_errcatUsage |-- JET_errcatState |-- JET_errcatObsolete</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="Enumeração pública" alt="Public enumeration" /></td>
<td><a href="dn335352(v=exchg.10).md">JET_ErrorInfo</a></td>
<td>Os valores válidos de InfoLevel para JetGetErrorInfo.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="Enumeração pública" alt="Public enumeration" /></td>
<td><a href="dn335486(v=exchg.10).md">JET_sesparam</a></td>
<td>Parâmetros de sessão ESENT.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="Enumeração pública" alt="Public enumeration" /></td>
<td><a href="dn335365(v=exchg.10).md">JetIndexColumnGrbit</a></td>
<td>Opções para <a href="dn335349(v=exchg.10).md">JET_INDEX_COLUMN</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="Enumeração pública" alt="Public enumeration" /></td>
<td><a href="dn335491(v=exchg.10).md">JetReope</a></td>
<td>Operação de comparação para filtro definido como <a href="dn335349(v=exchg.10).md">JET_INDEX_COLUMN</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="Enumeração pública" alt="Public enumeration" /></td>
<td><a href="dn335366(v=exchg.10).md">PrereadIndexRangesGrbit</a></td>
<td>Opções para <a href="dn335382(v=exchg.10).md">JetPrereadIndexRanges(JET_SESID, JET_TABLEID, [], Int32, Int32, Int32, [], PrereadIndexRangesGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="Enumeração pública" alt="Public enumeration" /></td>
<td><a href="dn335369(v=exchg.10).md">ResizeDatabaseGrbit</a></td>
<td>Opções para <a href="dn335496(v=exchg.10).md">JetResizeDatabase(JET_SESID, JET_DBID, Int32, Int32, ResizeDatabaseGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596136.pubenumeration(exchg.10).gif" title="Enumeração pública" alt="Public enumeration" /></td>
<td><a href="dn335370(v=exchg.10).md">StopServiceGrbit</a></td>
<td>Opções para <a href="dn335494(v=exchg.10).md">JetStopServiceInstance2(JET_INSTANCE, StopServiceGrbit)</a>.</td>
</tr>
</tbody>
</table>

