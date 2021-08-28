---
description: o linguagem WQL (WQL) é um subconjunto do American National Standards Institute linguagem SQL (ANSI SQL) &\# 8212; com pequenas mudanças semânticas. A tabela a seguir lista as palavras-chave WQL.
ms.assetid: 72a7ec04-9af3-41ae-9189-6e1d46803fa9
ms.tgt_platform: multiple
title: WQL (de SQL WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e2c80473874390851e81a5f2acebcd6d7e1497
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626752"
---
# <a name="wql-sql-for-wmi"></a>WQL (de SQL WMI)

o linguagem WQL (WQL) é um subconjunto do linguagem SQL de American National Standards Institute (SQL ANSI) com pequenas alterações semânticas. A tabela a seguir lista as palavras-chave WQL.



<table>
<colgroup>
<col  />
<col  />
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
<td>Combina duas expressões booleanas e retorna <strong>true</strong> quando ambas as expressões são <strong>true</strong>.<br/></td>
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
<td>Especifica a classe que contém as propriedades listadas em uma instrução SELECT. Windows A instrumentação de gerenciamento (WMI) dá suporte a consultas de dados de apenas uma classe por vez.<br/></td>
</tr>
<tr class="odd">
<td><a href="group-clause.md">Cláusula GROUP</a></td>
<td>Faz com que o WMI gere uma notificação para representar um grupo de eventos.<br/> Use essa cláusula com consultas de evento.<br/></td>
</tr>
<tr class="even">
<td><a href="having-clause.md">HAVING</a></td>
<td>Filtra os eventos que são recebidos durante o intervalo de Agrupamento especificado na <a href="within-clause.md">cláusula Within</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="wql-operators.md">IS</a></td>
<td>Operador de comparação usado com NOT e <strong>NULL</strong>. A sintaxe dessa instrução é a seguinte:<br/> IS [NOT] <strong>NULL</strong><br/> (onde não é opcional)<br/></td>
</tr>
<tr class="even">
<td><a href="wql-operators.md">ISA</a></td>
<td>Operador que aplica uma consulta às subclasses de uma classe especificada. Para obter mais informações, consulte <a href="isa-operator-for-event-queries.md">operador ISA para consultas de eventos</a>, <a href="isa-operator-for-data-queries.md">operador ISA para consultas de dados</a>e <a href="isa-operator-for-schema-queries.md">operador ISA para consultas de esquema</a>.<br/></td>
</tr>
<tr class="odd">
<td>KEYSONLY<br/></td>
<td>Usado em <a href="references-of-statement.md">referências de</a> e <a href="associators-of-statement.md">ASSOCIADORES de</a> consultas para garantir que as instâncias resultantes sejam populadas apenas com as chaves das instâncias, o que reduz a sobrecarga da chamada.<br/></td>
</tr>
<tr class="even">
<td><a href="wql-operators.md">LIKE</a></td>
<td>Operador que determina se uma determinada cadeia de caracteres corresponde ou não a um padrão especificado.<br/></td>
</tr>
<tr class="odd">
<td>NOT<br/></td>
<td>Operador de comparação que usa em uma consulta de seleção WQL, por exemplo:<br/>
<pre data-space="preserve"><code>SELECT * FROM meta_class WHERE NOT __class < &quot;Win32&quot; AND NOT __this ISA &quot;Win32_Account&quot;</code></pre></td>
</tr>
<tr class="even">
<td><strong>NULL</strong></td>
<td>Indica que um objeto não tem um valor atribuído explicitamente. <strong>NULL</strong> não é equivalente a zero (0) ou em branco.<br/></td>
</tr>
<tr class="odd">
<td>OU<br/></td>
<td>Combina duas condições.<br/> Quando mais de um operador lógico é usado em uma instrução, os operadores ou são avaliados após os operadores e.<br/></td>
</tr>
<tr class="even">
<td><a href="references-of-statement.md">REFERÊNCIAS DE</a></td>
<td>Recupera todas as instâncias de associação que se referem a uma instância de origem específica. Use essa instrução com consultas de esquema e dados. As <a href="references-of-statement.md">referências da</a> instrução são semelhantes à instrução <a href="associators-of-statement.md">ASSOCIATORS of</a> . No entanto, ele não recupera instâncias de ponto de extremidade; Ele recupera as instâncias de associação.<br/></td>
</tr>
<tr class="odd">
<td>SELECT<br/></td>
<td>Especifica as propriedades que são usadas em uma consulta.<br/> Para obter mais informações, consulte <a href="select-statement-for-data-queries.md">instrução SELECT para consultas de dados</a>, <a href="select-statement-for-event-queries.md">instrução SELECT para consultas de evento</a>ou <a href="select-statement-for-schema-queries.md">instrução SELECT para consultas de esquema</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>TRUE</strong></td>
<td>Operador booliano que é avaliado como-1 (menos um).<br/></td>
</tr>
<tr class="odd">
<td><a href="where-clause.md">WHERE</a></td>
<td>Restringe o escopo de uma consulta de dados, evento ou esquema.<br/></td>
</tr>
<tr class="even">
<td><a href="within-clause.md">WITHIN</a></td>
<td>Especifica um intervalo de sondagem ou Agrupamento.<br/> Use essa cláusula com consultas de evento.<br/></td>
</tr>
<tr class="odd">
<td>FALSE<br/></td>
<td>Operador booliano que é avaliado como 0 (zero).</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Usar uma palavra-chave WQL como um nome de objeto pode resultar em uma consulta que não pode ser analisada mesmo quando a consulta é compilada sem erro.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Operadores WQL](wql-operators.md)
</dt> <dt>

[WQL-formatos de data com suporte](wql-supported-date-formats.md)
</dt> <dt>

[WQL-formatos de tempo com suporte](wql-supported-time-formats.md)
</dt> </dl>

 

 




