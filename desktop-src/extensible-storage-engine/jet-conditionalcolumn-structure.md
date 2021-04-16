---
description: 'Saiba mais sobre: estrutura de JET_CONDITIONALCOLUMN'
title: Estrutura de JET_CONDITIONALCOLUMN
TOCTitle: JET_CONDITIONALCOLUMN Structure
ms:assetid: 2ca6b4ba-0dc4-47d5-b072-324e5a381d0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269214(v=EXCHG.10)
ms:contentKeyID: 32765517
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
ms.openlocfilehash: 27d0add64adeb7b609e84d6102a06230df55ebbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779932"
---
# <a name="jet_conditionalcolumn-structure"></a>Estrutura de JET_CONDITIONALCOLUMN


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_conditionalcolumn-structure"></a>Estrutura de JET_CONDITIONALCOLUMN

A estrutura de **JET_CONDITIONALCOLUMN** define como a indexação condicional é executada para um determinado índice. Um índice condicional contém uma entrada de índice somente para as linhas que correspondem à condição especificada. No entanto, a coluna condicional não faz parte da chave do índice, ela controla apenas a presença da entrada de índice.

```cpp
    typedef struct tagJET_CONDITIONALCOLUMN {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_GRBIT grbit;
    } JET_CONDITIONALCOLUMN;
```

### <a name="members"></a>Membros

**cbStruct**

Esse campo deve ser inicializado para sizeof (JET_CONDITIONALCOLUMN), em bytes.

**szColumnName**

O nome da coluna que contém os dados nos quais o mecanismo de banco de dados está indexando condicionalmente a linha.

**grbit** Um grupo de bits que fornece as opções para o índice condicional. A passagem de zero ou valores logicamente **ou** Ed não é válida para **JET_CONDITIONALCOLUMN**. O campo de bits deve ser exatamente um dos seguintes:

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
<td><p>JET_bitIndexColumnMustBeNull</p></td>
<td><p>A coluna especificada pelo parâmetro <em>szColumnName</em> deve ser nula para que uma entrada de índice de uma determinada linha apareça neste índice.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexColumnMustBeNonNull</p></td>
<td><p>A coluna especificada pelo parâmetro <em>szColumnName</em> deve ser não nula para uma entrada de índice para que uma determinada linha apareça nesse índice.</p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a>Comentários

Um índice condicional contém uma entrada de índice somente para as linhas que correspondem à condição especificada. Por exemplo, uma coluna pode ser nomeada "marcada" e, quando uma linha é marcada, a coluna é definida como um valor não nulo. Um JET_bitIndexColumnMustBeNonNull índice condicional nessa coluna mostrará todas as linhas marcadas e um JET_bitIndexColumnMustBeNull índice condicional mostrará as linhas que não estão marcadas. Essa também é uma maneira conveniente de executar uma exclusão de sinalizador e um índice de coleta de lixo.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementado como <strong>JET_CONDITIONALCOLUMN_W</strong> (Unicode) e <strong>JET_CONDITIONALCOLUMN_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)
