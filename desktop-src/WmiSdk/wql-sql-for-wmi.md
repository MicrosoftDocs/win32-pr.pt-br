---
description: O linguagem WQL (WQL) é um subconjunto do American National Standards Institute linguagem SQL (ANSI SQL)&\# 8212;com pequenas alterações semânticas. A tabela a seguir lista as palavras-chave WQL.
ms.assetid: 72a7ec04-9af3-41ae-9189-6e1d46803fa9
ms.tgt_platform: multiple
title: WQL (de SQL WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9a1a3b0db3f383bd8ba44aeb1e433b5aab02b4e9b4773ea221e1a0254ae037
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738815"
---
# <a name="wql-sql-for-wmi"></a>WQL (de SQL WMI)

O linguagem WQL (WQL) é um subconjunto do American National Standards Institute linguagem SQL (ansi SQL) com pequenas alterações semânticas. A tabela a seguir lista as palavras-chave WQL.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Palavra-chave WQL</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AND<br/></td>
<td>Combina duas expressões boolianas e retorna <strong>TRUE quando</strong> ambas as expressões são <strong>TRUE.</strong><br/></td>
</tr>
<tr class="even">
<td><a href="associators-of-statement.md">ASSOCIADORES DE</a></td>
<td>Recupera todas as instâncias associadas a uma instância de origem.<br/> Use essa instrução com consultas de esquema e consultas de dados.<br/></td>
</tr>
<tr class="odd">
<td><a href="--class-identifier.md">__CLASS</a></td>
<td>Faz referência à classe do objeto em uma consulta.<br/></td>
</tr>
<tr class="even">
<td>FROM<br/></td>
<td>Especifica a classe que contém as propriedades listadas em uma instrução SELECT. Windows A Instrumentação de Gerenciamento (WMI) dá suporte a consultas de dados de apenas uma classe por vez.<br/></td>
</tr>
<tr class="odd">
<td><a href="group-clause.md">Cláusula GROUP</a></td>
<td>Faz com que o WMI gere uma notificação para representar um grupo de eventos.<br/> Use essa cláusula com consultas de evento.<br/></td>
</tr>
<tr class="even">
<td><a href="having-clause.md">HAVING</a></td>
<td>Filtra os eventos recebidos durante o intervalo de agrupamento especificado na <a href="within-clause.md">cláusula WITHIN</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="wql-operators.md">IS</a></td>
<td>Operador de comparação usado com NOT e <strong>NULL.</strong> A sintaxe dessa instrução é a seguinte:<br/> IS [NOT] <strong>NULL</strong><br/> (em que NOT é opcional)<br/></td>
</tr>
<tr class="even">
<td><a href="wql-operators.md">ISA</a></td>
<td>Operador que aplica uma consulta às subclasses de uma classe especificada. Para obter mais informações, consulte <a href="isa-operator-for-event-queries.md">Operador ISA</a>para consultas de evento , <a href="isa-operator-for-data-queries.md">Operador ISA</a>para consultas de dados e Operador <a href="isa-operator-for-schema-queries.md">ISA</a>para consultas de esquema .<br/></td>
</tr>
<tr class="odd">
<td>KEYSONLY<br/></td>
<td>Usado em <a href="references-of-statement.md">consultas REFERENCES OF</a> e <a href="associators-of-statement.md">ASSOCIATORS OF</a> para garantir que as instâncias resultantes sejam preenchidas apenas com as chaves das instâncias, o que reduz a sobrecarga da chamada.<br/></td>
</tr>
<tr class="even">
<td><a href="wql-operators.md">LIKE</a></td>
<td>Operador que determina se uma determinada cadeia de caracteres corresponde ou não a um padrão especificado.<br/></td>
</tr>
<tr class="odd">
<td>NOT<br/></td>
<td>Operador de comparação que usa em uma consulta SELECT WQL, por exemplo:<br/>
<pre data-space="preserve"><code>SELECT * FROM meta_class WHERE NOT __class < &quot;Win32&quot; AND NOT __this ISA &quot;Win32_Account&quot;</code></pre></td>
</tr>
<tr class="even">
<td><strong>NULL</strong></td>
<td>Indica que um objeto não tem um valor atribuído explicitamente. <strong>NULL</strong> não é equivalente a zero (0) ou em branco.<br/></td>
</tr>
<tr class="odd">
<td>OU<br/></td>
<td>Combina duas condições.<br/> Quando mais de um operador lógico é usado em uma instrução , os operadores OR são avaliados após os operadores AND.<br/></td>
</tr>
<tr class="even">
<td><a href="references-of-statement.md">REFERÊNCIAS DE</a></td>
<td>Recupera todas as instâncias de associação que se referem a uma instância de origem específica. Use essa instrução com consultas de esquema e dados. A <a href="references-of-statement.md">instrução REFERENCES OF</a> é semelhante à <a href="associators-of-statement.md">instrução ASSOCIATORS OF.</a> No entanto, ele não recupera instâncias de ponto de extremidade; ele recupera as instâncias de associação.<br/></td>
</tr>
<tr class="odd">
<td>SELECT<br/></td>
<td>Especifica as propriedades usadas em uma consulta.<br/> Para obter mais informações, <a href="select-statement-for-data-queries.md">consulte instrução SELECT para consultas</a>de dados , <a href="select-statement-for-event-queries.md">instrução SELECT</a>para consultas de evento ou <a href="select-statement-for-schema-queries.md">instrução SELECT para consultas de esquema</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>TRUE</strong></td>
<td>Operador booliana que é avaliada como -1 (menos um).<br/></td>
</tr>
<tr class="odd">
<td><a href="where-clause.md">WHERE</a></td>
<td>Restringe o escopo de uma consulta de dados, eventos ou esquemas.<br/></td>
</tr>
<tr class="even">
<td><a href="within-clause.md">WITHIN</a></td>
<td>Especifica um intervalo de sondagem ou de agrupação.<br/> Use essa cláusula com consultas de evento.<br/></td>
</tr>
<tr class="odd">
<td>FALSE<br/></td>
<td>Operador booliana que é avaliada como 0 (zero).</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Usar uma palavra-chave WQL como um nome de objeto pode resultar em uma consulta que não pode ser analisado mesmo quando a consulta é compilada sem erro.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Operadores WQL](wql-operators.md)
</dt> <dt>

[Formatos de data com suporte do WQL](wql-supported-date-formats.md)
</dt> <dt>

[Formatos de tempo com suporte do WQL](wql-supported-time-formats.md)
</dt> </dl>

 

 




