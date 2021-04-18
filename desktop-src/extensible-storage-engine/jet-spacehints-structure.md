---
description: 'Saiba mais sobre: estrutura de JET_SPACEHINTS'
title: Estrutura de JET_SPACEHINTS
TOCTitle: JET_SPACEHINTS Structure
ms:assetid: 23328993-93c9-4a23-892b-e6a9f434d1d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269205(v=EXCHG.10)
ms:contentKeyID: 32765508
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
ms.openlocfilehash: cf786d1f47b5eaae3f9540c8635853020f9b0521
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762191"
---
# <a name="jet_spacehints-structure"></a>Estrutura de JET_SPACEHINTS


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_spacehints-structure"></a>Estrutura de JET_SPACEHINTS

A estrutura de **JET_SPACEHINTS** contém informações sobre padrões de alocação de espaço quando uma árvore b cresce por meio de divisões de Append ou Hotpoint. As divisões de acréscimo acontecem quando os registros são adicionados ao final de uma árvore b e as divisões de Hotpoint acontecem quando vários registros são adicionados ao mesmo ponto de inserção virtual (por exemplo, adicionar ' Maria ', ' Mark ', ' Martin' ', ' Mary ' ao meio de uma árvore b que é classificada alfabeticamente).

**Windows 7:** A estrutura de **JET_SPACEHINTS** é introduzida no Windows 7.

```cpp
    typedef struct tagJET_SPACEHINTS {
      unsigned long cbStruct;
      unsigned long ulInitialDensity;
      unsigned long cbInitial;
      JET_GRBIT grbit;
      unsigned long ulMaintDensity;
      unsigned long ulGrowth;
      unsigned long cbMinExtent;
      unsigned long cbMaxExtent;
    } JET_SPACEHINTS;
```

### <a name="members"></a>Membros

**cbStruct**

O tamanho, em bytes, dessa estrutura. Defina este membro como sizeof (JET_SPACEHINTS).

**ulInitialDensity**

O layout de densidade em (acréscimo).

**cbInitial**

O tamanho inicial (em bytes) do objeto que está sendo criado. Deve ser um múltiplo do tamanho da página do banco de dados.

**grbit**

Um grupo de bits que contém as opções a serem usadas para esta estrutura, que incluem zero ou mais das ações a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitSpaceHintsUtilizeParentSpace<br />
0x00000001</p></td>
<td><p>Altera a política de alocação interna para obter espaço heirarchically do pai imediato de uma árvore b.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitCreateHintAppendSequential<br />
0x00000002</p></td>
<td><p>Permite que o comportamento da divisão de acréscimo cresça de acordo com a dinâmica de crescimento da tabela (definida por cbMinExtent, ulGrowth, cbMaxExtent).</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitCreateHintHotpointSequential<br />
0x00000004</p></td>
<td><p>Permite que o comportamento de divisão de Hotpoint cresça de acordo com a dinâmica de crescimento da tabela (definida por cbMinExtent, ulGrowth, cbMaxExtent).</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveHintTableScanForward<br />
0x00000010</p></td>
<td><p>Se definido, o cliente indica que a verificação sequencial de encaminhamento é o padrão de uso predominante desta tabela.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveHintTableScanBackward<br />
0x00000020</p></td>
<td><p>Se definido, o cliente indica que a verificação sequencial retroativa é o padrão de uso predominante desta tabela.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDeleteHintTableSequential<br />
0x00000100</p></td>
<td><p>Se definido, o aplicativo espera que essa tabela seja limpa em ordem sequencial, da chave mais baixa para a chave mais alta.</p></td>
</tr>
</tbody>
</table>


**ulMaintDensity**

densidade para mulMaintDensity

Densidade a ser mantida em. Se as dicas de espaço especificarem JET_bitRetrieveHintTableScanForward ou JET_bitRetrieveHintTableScanBackward, a desfragmentação da tabela será disparada quando o espaço usado na tabela cair abaixo desse limite. A desfragmentação de tabela pode ser desabilitada definindo esse membro como zero. Definir esse membro como 100 fará com que a desfragmentação da tabela seja executada assim que uma página for liberada.

**ulGrowth**

O percentual de crescimento do último crescimento ou tamanho inicial, arredondado para o tamanho de alocação mais próximo do JET nativo.

**cbMinExtent muito pequeno**

Isso substitui ulGrowth se for muito pequeno.

**cbMaxExtent**

O valor máximo para crescimento em bytes. Este ulGrowth de Caps.

### <a name="when-a-b-tree-grows-through-append-or-hotpoint-splits-as-opposed-to-random-record-insertions-the-amount-of-space-the-table-will-grow-by-is-calculated-as-follows"></a>Quando uma árvore b cresce através de divisões de Append ou Hotpoint (em oposição às inserções de registros aleatórios), a quantidade de espaço que a tabela aumentará é calculada da seguinte maneira:

1.  Na criação, fornecemos o cbInitial da árvore b, sempre.

2.  Durante a primeira alocação de uma determinada área, alocaremos: cbInitial \* ulGrowth/100 (arredondado para o tamanho da página do banco de dados) ou cbMinExtent se for maior.

3.  Durante a próxima alocação, cbLastAlloc \* ulGrowth/100 (arredondado para o tamanho da página do DB) ou cbMinExtent se for maior.

4.  Em alguma alocação (que pode ser a primeira alocação), o tamanho calculado excederá cbMaxExtent e esse será o tamanho de crescimento depois disso.

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

[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TABLECREATE3](./jet-tablecreate3-structure.md)
