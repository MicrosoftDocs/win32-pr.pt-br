---
description: O linguagem WQL (WQL) é um subconjunto do American National Standards Institute linguagem SQL (ANSI SQL) &\# 8212; com pequenas alterações semânticas. A tabela a seguir lista as palavras-chave WQL.
ms.assetid: 72a7ec04-9af3-41ae-9189-6e1d46803fa9
ms.tgt_platform: multiple
title: WQL (de SQL WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87498b6e8e37ab900e21eedf2c15d5cdba9f9bd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165315"
---
# <a name="wql-sql-for-wmi"></a><span data-ttu-id="01599-104">WQL (de SQL WMI)</span><span class="sxs-lookup"><span data-stu-id="01599-104">WQL (SQL for WMI)</span></span>

<span data-ttu-id="01599-105">A linguagem WQL (WQL) é um subconjunto da linguagem SQL de American National Standards Institute (ANSI SQL) com alterações de semântica secundárias.</span><span class="sxs-lookup"><span data-stu-id="01599-105">The WMI Query Language (WQL) is a subset of the American National Standards Institute Structured Query Language (ANSI SQL) with minor semantic changes.</span></span> <span data-ttu-id="01599-106">A tabela a seguir lista as palavras-chave WQL.</span><span class="sxs-lookup"><span data-stu-id="01599-106">The following table lists the WQL keywords.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01599-107">Palavra-chave WQL</span><span class="sxs-lookup"><span data-stu-id="01599-107">WQL keyword</span></span></th>
<th><span data-ttu-id="01599-108">Significado</span><span class="sxs-lookup"><span data-stu-id="01599-108">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="01599-109">AND</span><span class="sxs-lookup"><span data-stu-id="01599-109">AND</span></span><br/></td>
<td><span data-ttu-id="01599-110">Combina duas expressões booleanas e retorna <strong>true</strong> quando ambas as expressões são <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="01599-110">Combines two Boolean expressions, and returns <strong>TRUE</strong> when both expressions are <strong>TRUE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01599-111"><a href="associators-of-statement.md">ASSOCIADORES DE</a></span><span class="sxs-lookup"><span data-stu-id="01599-111"><a href="associators-of-statement.md">ASSOCIATORS OF</a></span></span></td>
<td><span data-ttu-id="01599-112">Recupera todas as instâncias associadas a uma instância de origem.</span><span class="sxs-lookup"><span data-stu-id="01599-112">Retrieves all instances that are associated with a source instance.</span></span><br/> <span data-ttu-id="01599-113">Use essa instrução com consultas de esquema e consultas de dados.</span><span class="sxs-lookup"><span data-stu-id="01599-113">Use this statement with schema queries and data queries.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01599-114"><a href="--class-identifier.md">__CLASS</a></span><span class="sxs-lookup"><span data-stu-id="01599-114"><a href="--class-identifier.md">__CLASS</a></span></span></td>
<td><span data-ttu-id="01599-115">Faz referência à classe do objeto em uma consulta.</span><span class="sxs-lookup"><span data-stu-id="01599-115">References the class of the object in a query.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01599-116">FROM</span><span class="sxs-lookup"><span data-stu-id="01599-116">FROM</span></span><br/></td>
<td><span data-ttu-id="01599-117">Especifica a classe que contém as propriedades listadas em uma instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="01599-117">Specifies the class that contains the properties listed in a SELECT statement.</span></span> <span data-ttu-id="01599-118">Instrumentação de Gerenciamento do Windows (WMI) dá suporte a consultas de dados de apenas uma classe por vez.</span><span class="sxs-lookup"><span data-stu-id="01599-118">Windows Management Instrumentation (WMI) supports data queries from only one class at a time.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01599-119"><a href="group-clause.md">Cláusula GROUP</a></span><span class="sxs-lookup"><span data-stu-id="01599-119"><a href="group-clause.md">GROUP Clause</a></span></span></td>
<td><span data-ttu-id="01599-120">Faz com que o WMI gere uma notificação para representar um grupo de eventos.</span><span class="sxs-lookup"><span data-stu-id="01599-120">Causes WMI to generate one notification to represent a group of events.</span></span><br/> <span data-ttu-id="01599-121">Use essa cláusula com consultas de evento.</span><span class="sxs-lookup"><span data-stu-id="01599-121">Use this clause with event queries.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01599-122"><a href="having-clause.md">HAVING</a></span><span class="sxs-lookup"><span data-stu-id="01599-122"><a href="having-clause.md">HAVING</a></span></span></td>
<td><span data-ttu-id="01599-123">Filtra os eventos que são recebidos durante o intervalo de Agrupamento especificado na <a href="within-clause.md">cláusula Within</a>.</span><span class="sxs-lookup"><span data-stu-id="01599-123">Filters the events that are received during the grouping interval that is specified in the <a href="within-clause.md">WITHIN clause</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01599-124"><a href="wql-operators.md">IS</a></span><span class="sxs-lookup"><span data-stu-id="01599-124"><a href="wql-operators.md">IS</a></span></span></td>
<td><span data-ttu-id="01599-125">Operador de comparação usado com NOT e <strong>NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="01599-125">Comparison operator used with NOT and <strong>NULL</strong>.</span></span> <span data-ttu-id="01599-126">A sintaxe dessa instrução é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="01599-126">The syntax for this statement is the following:</span></span><br/> <span data-ttu-id="01599-127">IS [NOT] <strong>NULL</strong></span><span class="sxs-lookup"><span data-stu-id="01599-127">IS [NOT] <strong>NULL</strong></span></span><br/> <span data-ttu-id="01599-128">(onde não é opcional)</span><span class="sxs-lookup"><span data-stu-id="01599-128">(where NOT is optional)</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01599-129"><a href="wql-operators.md">ISA</a></span><span class="sxs-lookup"><span data-stu-id="01599-129"><a href="wql-operators.md">ISA</a></span></span></td>
<td><span data-ttu-id="01599-130">Operador que aplica uma consulta às subclasses de uma classe especificada.</span><span class="sxs-lookup"><span data-stu-id="01599-130">Operator that applies a query to the subclasses of a specified class.</span></span> <span data-ttu-id="01599-131">Para obter mais informações, consulte <a href="isa-operator-for-event-queries.md">operador ISA para consultas de eventos</a>, <a href="isa-operator-for-data-queries.md">operador ISA para consultas de dados</a>e <a href="isa-operator-for-schema-queries.md">operador ISA para consultas de esquema</a>.</span><span class="sxs-lookup"><span data-stu-id="01599-131">For more information, see <a href="isa-operator-for-event-queries.md">ISA Operator for Event Queries</a>, <a href="isa-operator-for-data-queries.md">ISA Operator for Data Queries</a>, and <a href="isa-operator-for-schema-queries.md">ISA Operator for Schema Queries</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01599-132">KEYSONLY</span><span class="sxs-lookup"><span data-stu-id="01599-132">KEYSONLY</span></span><br/></td>
<td><span data-ttu-id="01599-133">Usado em <a href="references-of-statement.md">referências de</a> e <a href="associators-of-statement.md">ASSOCIADORES de</a> consultas para garantir que as instâncias resultantes sejam populadas apenas com as chaves das instâncias, o que reduz a sobrecarga da chamada.</span><span class="sxs-lookup"><span data-stu-id="01599-133">Used in <a href="references-of-statement.md">REFERENCES OF</a> and <a href="associators-of-statement.md">ASSOCIATORS OF</a> queries to ensure that the resulting instances are only populated with the keys of the instances, which reduces the overhead of the call.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01599-134"><a href="wql-operators.md">LIKE</a></span><span class="sxs-lookup"><span data-stu-id="01599-134"><a href="wql-operators.md">LIKE</a></span></span></td>
<td><span data-ttu-id="01599-135">Operador que determina se uma determinada cadeia de caracteres corresponde ou não a um padrão especificado.</span><span class="sxs-lookup"><span data-stu-id="01599-135">Operator that determines whether or not a given character string matches a specified pattern.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01599-136">NOT</span><span class="sxs-lookup"><span data-stu-id="01599-136">NOT</span></span><br/></td>
<td><span data-ttu-id="01599-137">Operador de comparação que usa em uma consulta de seleção WQL, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="01599-137">Comparison operator that use in a WQL SELECT query, for example:</span></span><br/>
<pre data-space="preserve"><code>SELECT * FROM meta_class WHERE NOT __class < &quot;Win32&quot; AND NOT __this ISA &quot;Win32_Account&quot;</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01599-138"><strong>NULL</strong></span><span class="sxs-lookup"><span data-stu-id="01599-138"><strong>NULL</strong></span></span></td>
<td><span data-ttu-id="01599-139">Indica que um objeto não tem um valor atribuído explicitamente.</span><span class="sxs-lookup"><span data-stu-id="01599-139">Indicates an object does not have an explicitly assigned value.</span></span> <span data-ttu-id="01599-140"><strong>NULL</strong> não é equivalente a zero (0) ou em branco.</span><span class="sxs-lookup"><span data-stu-id="01599-140"><strong>NULL</strong> is not equivalent to zero (0) or blank.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01599-141">OU</span><span class="sxs-lookup"><span data-stu-id="01599-141">OR</span></span><br/></td>
<td><span data-ttu-id="01599-142">Combina duas condições.</span><span class="sxs-lookup"><span data-stu-id="01599-142">Combines two conditions.</span></span><br/> <span data-ttu-id="01599-143">Quando mais de um operador lógico é usado em uma instrução, os operadores ou são avaliados após os operadores e.</span><span class="sxs-lookup"><span data-stu-id="01599-143">When more than one logical operator is used in a statement, the OR operators are evaluated after the AND operators.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01599-144"><a href="references-of-statement.md">REFERÊNCIAS DE</a></span><span class="sxs-lookup"><span data-stu-id="01599-144"><a href="references-of-statement.md">REFERENCES OF</a></span></span></td>
<td><span data-ttu-id="01599-145">Recupera todas as instâncias de associação que se referem a uma instância de origem específica.</span><span class="sxs-lookup"><span data-stu-id="01599-145">Retrieves all association instances that refer to a specific source instance.</span></span> <span data-ttu-id="01599-146">Use essa instrução com consultas de esquema e dados.</span><span class="sxs-lookup"><span data-stu-id="01599-146">Use this statement with schema and data queries.</span></span> <span data-ttu-id="01599-147">As <a href="references-of-statement.md">referências da</a> instrução são semelhantes à instrução <a href="associators-of-statement.md">ASSOCIATORS of</a> .</span><span class="sxs-lookup"><span data-stu-id="01599-147">The <a href="references-of-statement.md">REFERENCES OF</a> statement is similar to the <a href="associators-of-statement.md">ASSOCIATORS OF</a> statement.</span></span> <span data-ttu-id="01599-148">No entanto, ele não recupera instâncias de ponto de extremidade; Ele recupera as instâncias de associação.</span><span class="sxs-lookup"><span data-stu-id="01599-148">However, it does not retrieve endpoint instances; it retrieves the association instances.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01599-149">SELECT</span><span class="sxs-lookup"><span data-stu-id="01599-149">SELECT</span></span><br/></td>
<td><span data-ttu-id="01599-150">Especifica as propriedades que são usadas em uma consulta.</span><span class="sxs-lookup"><span data-stu-id="01599-150">Specifies the properties that are used in a query.</span></span><br/> <span data-ttu-id="01599-151">Para obter mais informações, consulte <a href="select-statement-for-data-queries.md">instrução SELECT para consultas de dados</a>, <a href="select-statement-for-event-queries.md">instrução SELECT para consultas de evento</a>ou <a href="select-statement-for-schema-queries.md">instrução SELECT para consultas de esquema</a>.</span><span class="sxs-lookup"><span data-stu-id="01599-151">For more information, see <a href="select-statement-for-data-queries.md">SELECT Statement for Data Queries</a>, <a href="select-statement-for-event-queries.md">SELECT Statement for Event Queries</a>, or <a href="select-statement-for-schema-queries.md">SELECT Statement for Schema Queries</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01599-152"><strong>TRUE</strong></span><span class="sxs-lookup"><span data-stu-id="01599-152"><strong>TRUE</strong></span></span></td>
<td><span data-ttu-id="01599-153">Operador booliano que é avaliado como-1 (menos um).</span><span class="sxs-lookup"><span data-stu-id="01599-153">Boolean operator that evaluates to -1 (minus one).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01599-154"><a href="where-clause.md">WHERE</a></span><span class="sxs-lookup"><span data-stu-id="01599-154"><a href="where-clause.md">WHERE</a></span></span></td>
<td><span data-ttu-id="01599-155">Restringe o escopo de uma consulta de dados, evento ou esquema.</span><span class="sxs-lookup"><span data-stu-id="01599-155">Narrows the scope of a data, event, or schema query.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01599-156"><a href="within-clause.md">WITHIN</a></span><span class="sxs-lookup"><span data-stu-id="01599-156"><a href="within-clause.md">WITHIN</a></span></span></td>
<td><span data-ttu-id="01599-157">Especifica um intervalo de sondagem ou Agrupamento.</span><span class="sxs-lookup"><span data-stu-id="01599-157">Specifies a polling or grouping interval.</span></span><br/> <span data-ttu-id="01599-158">Use essa cláusula com consultas de evento.</span><span class="sxs-lookup"><span data-stu-id="01599-158">Use this clause with event queries.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01599-159">FALSE</span><span class="sxs-lookup"><span data-stu-id="01599-159">FALSE</span></span><br/></td>
<td><span data-ttu-id="01599-160">Operador booliano que é avaliado como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="01599-160">Boolean operator that evaluates to 0 (zero).</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="01599-161">Usar uma palavra-chave WQL como um nome de objeto pode resultar em uma consulta que não pode ser analisada mesmo quando a consulta é compilada sem erro.</span><span class="sxs-lookup"><span data-stu-id="01599-161">Using a WQL key word as an object name can result in a query that cannot be parsed even when the query compiles without error.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="01599-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="01599-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01599-163">Operadores WQL</span><span class="sxs-lookup"><span data-stu-id="01599-163">WQL Operators</span></span>](wql-operators.md)
</dt> <dt>

[<span data-ttu-id="01599-164">WQL-formatos de data com suporte</span><span class="sxs-lookup"><span data-stu-id="01599-164">WQL-Supported Date Formats</span></span>](wql-supported-date-formats.md)
</dt> <dt>

[<span data-ttu-id="01599-165">WQL-formatos de tempo com suporte</span><span class="sxs-lookup"><span data-stu-id="01599-165">WQL-Supported Time Formats</span></span>](wql-supported-time-formats.md)
</dt> </dl>

 

 




