---
description: 'Saiba mais sobre: JET_SNP'
title: JET_SNP
TOCTitle: JET_SNP
ms:assetid: 7f3d1cc5-7b27-454d-8dd1-584ab4b60ab0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269311(v=EXCHG.10)
ms:contentKeyID: 32765601
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 35ffb2d17c01c3d157fc7ed66a320529f844ff9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771783"
---
# <a name="jet_snp"></a>JET_SNP


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_snp"></a>JET_SNP

O **JET_SNP** grupo de constantes descreve o tipo da operação para a qual as informações de progresso serão obtidas. Essas constantes são usadas como o parâmetro *SNP* da função de retorno de chamada [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante/valor</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_snpRepair<br />
2</p></td>
<td><p>O retorno de chamada é para uma operação de reparo.</p></td>
</tr>
<tr class="even">
<td><p>JET_snpCompact<br />
4</p></td>
<td><p>O retorno de chamada é para desfragmentação de banco de dados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_snpRestore<br />
8</p></td>
<td><p>O retorno de chamada é para uma operação de restauração.</p></td>
</tr>
<tr class="even">
<td><p>JET_snpBackup<br />
9</p></td>
<td><p>O retorno de chamada é para uma operação de backup.</p></td>
</tr>
<tr class="odd">
<td><p>JET_snpUpgrade<br />
10</p></td>
<td><p>Não há suporte.</p>
<p><strong>Windows 2000:</strong>  O retorno de chamada é para a operação de atualização de formato de banco de dados.</p></td>
</tr>
<tr class="even">
<td><p>JET_snpScrub<br />
11</p></td>
<td><p>O retorno de chamada é para uma operação de zero (ou seja, depuração) do banco de dados.</p>
<p><strong>Windows server 2003 e windows 2000 Server:</strong>  Sem suporte.</p></td>
</tr>
<tr class="odd">
<td><p>JET_snpUpgradeRecordFormat<br />
12</p></td>
<td><p>O retorno de chamada é para o processo de atualização do formato de registro de todas as páginas de banco de dados.</p>
<p><strong>Windows server 2003 e windows 2000 Server:</strong>  Sem suporte.</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_SNPROG](./jet-snprog-structure.md)  
[JET_SNT](./jet-snt.md)
