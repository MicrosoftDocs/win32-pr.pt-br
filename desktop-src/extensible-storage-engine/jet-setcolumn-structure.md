---
description: 'Saiba mais sobre: estrutura de JET_SETCOLUMN'
title: Estrutura de JET_SETCOLUMN
TOCTitle: JET_SETCOLUMN Structure
ms:assetid: 3fdb8ec0-3c40-44f3-9859-72e22a504b90
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269233(v=EXCHG.10)
ms:contentKeyID: 32765535
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
ms.openlocfilehash: a170132fd4d832133e0f0bcad4a3499fa743db38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646904"
---
# <a name="jet_setcolumn-structure"></a>Estrutura de JET_SETCOLUMN


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_setcolumn-structure"></a>Estrutura de JET_SETCOLUMN

A estrutura de **JET_SETCOLUMN** contém parâmetros de entrada e saída para [JetSetColumns](./jetsetcolumns-function.md). Os campos na estrutura descrevem o valor da coluna a ser definido, como defini-lo e onde obter os dados do conjunto de colunas.

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      const void* pvData;
      unsigned long cbData;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_ERR err;
    } JET_SETCOLUMN;
```

### <a name="members"></a>Membros

**columnid**

O identificador de coluna para uma coluna a ser definida.

**pvData**

Um ponteiro para os dados a serem definidos em uma coluna.

**cbData**

O tamanho da alocação, em bytes, começando em **pvData** em bytes.

**grbit**

Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais das ações a seguir.

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
<td><p>JET_bitSetAppendLV</p></td>
<td><p>Anexa dados a uma coluna do tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>. O mesmo comportamento pode ser obtido determinando o tamanho do valor longo existente e especificando <strong>ibLongValue</strong> em <strong>psetinfo</strong>. No entanto, é mais simples usar esse <em>grbit</em>, já que saber o tamanho do valor da coluna existente não é necessário.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetOverwriteLV</p></td>
<td><p>Substitui o valor longo existente pelos novos dados. Quando essa opção é usada, é como se o valor longo existente tiver sido definido como 0 (zero) comprimento antes da definição dos novos dados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetSizeLV</p></td>
<td><p>Interpreta o buffer de entrada como um número inteiro de bytes a serem definidos como o comprimento do valor longo descrito pelo columnid fornecido e, se fornecido, o número de sequência em psetinfo- &gt; itagSequence. Se o tamanho fornecido for maior que o valor da coluna existente, a coluna será estendida com 0s. Se o tamanho for menor do que o valor da coluna existente, o valor será truncado.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetZeroLength</p></td>
<td><p>Define um valor como comprimento zero. Normalmente, um valor de coluna é definido como NULL passando um cbMax de 0. No entanto, para alguns tipos, como <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, um valor de coluna pode ter 0 comprimento em vez de NULL, e essa opção é usada para diferenciar entre NULL e 0 comprimento.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetSeparateLV</p></td>
<td><p>Força um valor longo, as colunas do tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, a serem armazenadas separadamente do restante dos dados de registro. Isso ocorre normalmente quando o tamanho do valor longo impede que ele seja armazenado com os dados de registro restantes. No entanto, essa opção pode ser usada para forçar o valor longo a ser armazenado separadamente. Observe que valores longos de quatro bytes de tamanho ou menores não podem ser forçados a serem separados. Nesses casos, a opção é ignorada.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetUniqueMultiValues</p></td>
<td><p>Impõe valores distintos em uma coluna com valores múltiplos. Essa opção compara os dados da coluna de origem, sem nenhuma transformação, com outros valores de coluna existentes e um erro será retornado se uma duplicata for encontrada. Se essa opção for fornecida, JET_bitSetAppendLv, JET_bitSetOverwriteLV e JET_bitSetSizeLV também não puderem ser fornecidos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetUniqueNormalizedMultiValues</p></td>
<td><p>Impõe valores distintos em uma coluna com valores múltiplos. Essa opção compara a transformação normalizada da chave de dados de coluna com outros valores de coluna existentes transformados de forma semelhante e um erro será retornado se uma duplicata for encontrada. Se essa opção for fornecida, JET_bitSetAppendLv, JET_bitSetOverwriteLV e JET_bitSetSizeLV também não puderem ser fornecidos.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetRevertToDefaultValue</p></td>
<td><p>Faz com que a coluna retorne o valor de coluna padrão em operações de recuperação de coluna subsequentes. Todos os valores de coluna existentes são removidos. Essa opção só é aplicável a colunas marcadas, esparsas ou com vários valores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetIntrinsicLV</p></td>
<td><p>Mantém o valor longo, colunas do tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou JET_coltypeLongBinary, armazenados com os dados de registro restantes, se possível. Normalmente, as colunas longas são armazenadas separadamente quando seu comprimento excede 1024 bytes ou faria com que o tamanho do registro exceda o limite de tamanho relacionado à página. No entanto, se essa opção for definida, a operação definir coluna falhará com o erro JET_errColumnTooBig em vez de armazenar esse valor de coluna separado dos dados de registro restantes.</p></td>
</tr>
</tbody>
</table>


**ibLongValue**

O deslocamento para o primeiro byte a ser recuperado de uma coluna do tipo [JET_coltypLongBinary](./jet-coltyp.md)ou [JET_coltypLongText](./jet-coltyp.md).

**itagSequence**

Descreve o número de sequência do valor em uma coluna com vários valores. Um **itagSequence** de 0 indica que o valor da coluna definido deve ser adicionado como uma nova instância de uma coluna com vários valores.

**erra**

Códigos de erro e avisos retornados da operação definir coluna.

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

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetSetColumns](./jetsetcolumns-function.md)
