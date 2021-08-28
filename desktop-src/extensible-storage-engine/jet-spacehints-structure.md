---
description: 'Saiba mais sobre: estrutura JET_SPACEHINTS dados'
title: estrutura JET_SPACEHINTS dados
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
ms.openlocfilehash: 812fc683e24e6b2401ce72d99e3537549e3d30d0
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985139"
---
# <a name="jet_spacehints-structure"></a>estrutura JET_SPACEHINTS dados


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_spacehints-structure"></a>estrutura JET_SPACEHINTS dados

A **JET_SPACEHINTS** contém informações sobre padrões de alocação de espaço quando uma árvore B cresce por meio de divisão de ponto de hotpoint ou de anexação. As divisãos de acréscimo ocorrem quando os registros são adicionados ao final de uma árvore b e as divisãos de ponto de hotpoint ocorrem quando vários registros são adicionados ao mesmo ponto de inserção virtual (por exemplo, adicionando 'Dice', 'Mark', 'Martin', 'Mary' ao meio de uma árvore b que é classificação alfabética).

**Windows 7:** A **estrutura JET_SPACEHINTS** é introduzida no Windows 7.

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

**Cbstruct**

O tamanho, em bytes, dessa estrutura. De definir esse membro como sizeof( JET_SPACEHINTS ).

**ulInitialDensity**

A densidade no layout (anexar).

**cbInitial**

O tamanho inicial (em bytes) do objeto que está sendo criado. Deve ser um múltiplo do tamanho da página do banco de dados.

**grbit**

Um grupo de bits que contém as opções a serem usadas para essa estrutura, que incluem zero ou mais dos seguintes.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitSpaceHintsUtilizeParentSpace<br />0x00000001</p> | <p>Altera a política de alocação interna para obter espaço de forma significativa do pai imediato de uma árvore b.</p> | 
| <p>JET_bitCreateHintAppendSequential<br />0x00000002</p> | <p>Permite que o comportamento de divisão de anexação cresça de acordo com a dinâmica de crescimento da tabela (definida por cbMinExtent, ulGrowth, cbMaxExtent).</p> | 
| <p>JET_bitCreateHintHotpointSequential<br />0x00000004</p> | <p>Permite que o comportamento de divisão de ponto de acesso cresça de acordo com a dinâmica de crescimento da tabela (definida por cbMinExtent, ulGrowth, cbMaxExtent).</p> | 
| <p>JET_bitRetrieveHintTableScanForward<br />0x00000010</p> | <p>Se definido, o cliente indica que a verificação sequencial de encaminhamento é o padrão de uso predominante desta tabela.</p> | 
| <p>JET_bitRetrieveHintTableScanBackward<br />0x00000020</p> | <p>Se definido, o cliente indica que a verificação sequencial para trás é o padrão de uso predominante desta tabela.</p> | 
| <p>JET_bitDeleteHintTableSequential<br />0x00000100</p> | <p>Se definido, o aplicativo espera que essa tabela seja limpa em ordem sequencial, da chave mais baixa para a chave mais alta.</p> | 



**ulMaintDensity**

densidade para mulMaintDensity

Densidade a ser mantida em. Se as dicas de espaço especificarem JET_bitRetrieveHintTableScanForward ou JET_bitRetrieveHintTableScanBackward, a desfragmentação de tabela será disparada quando o espaço usado na tabela ficar abaixo desse limite. A desfragmentação de tabela pode ser desabilitada definindo esse membro como zero. Definir esse membro como 100 fará com que a desfragmentação de tabela seja executado assim que uma página for liberada.

**ulGrowth**

O percentual de crescimento do último crescimento ou tamanho inicial, arredondado para o tamanho de alocação do JET nativo mais próximo.

**cbMinExtent muito pequeno**

Isso substituirá ulGrowth se for muito pequeno.

**cbMaxExtent**

O valor máximo para o crescimento em bytes. Isso se trata de ulGrowth.

### <a name="when-a-b-tree-grows-through-append-or-hotpoint-splits-as-opposed-to-random-record-insertions-the-amount-of-space-the-table-will-grow-by-is-calculated-as-follows"></a>Quando uma árvore b cresce por meio de divisão de ponto de hotpoint ou de anexação (em vez de inserções de registro aleatórias), a quantidade de espaço que a tabela aumentará é calculada da seguinte forma:

1.  Na criação, damos à árvore b cbInitial, sempre.

2.  Durante a primeira alocação de uma determinada área, alocamos: cbInitial ulGrowth/100 (arredondado para o tamanho da página do BD) ou \* cbMinExtent se maior.

3.  Durante a próxima alocação, cbLastAlloc ulGrowth /100 (arredondado para o tamanho da página do \* BD) ou cbMinExtent se maior.

4.  Em alguma alocação (que pode ser a primeira alocação), o tamanho calculado excederá cbMaxExtent e esse será o tamanho do crescimento depois disso.

### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TABLECREATE3](./jet-tablecreate3-structure.md)
