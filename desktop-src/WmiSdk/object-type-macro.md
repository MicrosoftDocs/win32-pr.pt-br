---
description: A macro do tipo de objeto contém cláusulas obrigatórias e opcionais que descrevem as características básicas de um objeto MIB. O provedor SNMP converte uma MIB nas partes correspondentes da macro do tipo de objeto.
ms.assetid: ad76a4fc-354e-4270-862c-062aa523bf7e
ms.tgt_platform: multiple
title: Macro de tipo de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c605a414c402f2cf2d18be2d966db6408f23cdc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089835"
---
# <a name="object-type-macro"></a><span data-ttu-id="47bcb-104">Macro de tipo de objeto</span><span class="sxs-lookup"><span data-stu-id="47bcb-104">OBJECT-TYPE Macro</span></span>

<span data-ttu-id="47bcb-105">A macro do tipo de objeto contém cláusulas obrigatórias e opcionais que descrevem as características básicas de um objeto MIB.</span><span class="sxs-lookup"><span data-stu-id="47bcb-105">The OBJECT-TYPE macro contains mandatory and optional clauses that describe the basic characteristics of a MIB object.</span></span> <span data-ttu-id="47bcb-106">O provedor SNMP converte uma MIB nas partes correspondentes da macro do tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="47bcb-106">The SNMP Provider converts an MIB to the corresponding parts of the OBJECT-TYPE macro.</span></span>

> [!Note]  
> <span data-ttu-id="47bcb-107">Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="47bcb-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

## <a name="components"></a><span data-ttu-id="47bcb-108">Componentes</span><span class="sxs-lookup"><span data-stu-id="47bcb-108">Components</span></span>

<dl> <dt>

<span data-ttu-id="47bcb-109"><span id="MIB_object"></span><span id="mib_object"></span><span id="MIB_OBJECT"></span>Objeto MIB</span><span class="sxs-lookup"><span data-stu-id="47bcb-109"><span id="MIB_object"></span><span id="mib_object"></span><span id="MIB_OBJECT"></span>MIB object</span></span>
</dt> <dd>

<span data-ttu-id="47bcb-110">Objeto que contém a maioria dos dados em questão.</span><span class="sxs-lookup"><span data-stu-id="47bcb-110">Object that contains most of the data in question.</span></span>

</dd> <dt>

<span data-ttu-id="47bcb-111"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Descritor de objeto</span><span class="sxs-lookup"><span data-stu-id="47bcb-111"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Object descriptor</span></span>
</dt> <dd>

<span data-ttu-id="47bcb-112">Nome exclusivo ou descritor de objeto identificando cada objeto MIB.</span><span class="sxs-lookup"><span data-stu-id="47bcb-112">Unique name or object descriptor identifying each MIB object.</span></span> <span data-ttu-id="47bcb-113">Cada descritor de objeto MIB é mapeado exatamente para um nome de propriedade CIM.</span><span class="sxs-lookup"><span data-stu-id="47bcb-113">Each MIB object descriptor maps exactly to a CIM property name.</span></span> <span data-ttu-id="47bcb-114">Por exemplo, **ifIndex** é convertido em **ifIndex**.</span><span class="sxs-lookup"><span data-stu-id="47bcb-114">For example, **ifIndex** translates to **ifIndex**.</span></span>

</dd> <dt>

<span data-ttu-id="47bcb-115"><span id="SYNTAX_Clause"></span><span id="syntax_clause"></span><span id="SYNTAX_CLAUSE"></span>[Cláusula de sintaxe](syntax-clause.md)</span><span class="sxs-lookup"><span data-stu-id="47bcb-115"><span id="SYNTAX_Clause"></span><span id="syntax_clause"></span><span id="SYNTAX_CLAUSE"></span>[SYNTAX Clause](syntax-clause.md)</span></span>
</dt> <dd>

<span data-ttu-id="47bcb-116">Define os dados e o tipo de um objeto MIB.</span><span class="sxs-lookup"><span data-stu-id="47bcb-116">Defines the data and type of an MIB object.</span></span>

</dd> <dt>

<span data-ttu-id="47bcb-117"><span id="INDEX_clause"></span><span id="index_clause"></span><span id="INDEX_CLAUSE"></span>[Cláusula de índice](index-clause.md)</span><span class="sxs-lookup"><span data-stu-id="47bcb-117"><span id="INDEX_clause"></span><span id="index_clause"></span><span id="INDEX_CLAUSE"></span>[INDEX clause](index-clause.md)</span></span>
</dt> <dd>

<span data-ttu-id="47bcb-118">Define uma chave para selecionar uma linha de tabela exclusiva.</span><span class="sxs-lookup"><span data-stu-id="47bcb-118">Defines a key for selecting a unique table row.</span></span>

</dd> <dt>

<span data-ttu-id="47bcb-119"><span id="AUGMENTS_clause"></span><span id="augments_clause"></span><span id="AUGMENTS_CLAUSE"></span>AUMENTA a cláusula</span><span class="sxs-lookup"><span data-stu-id="47bcb-119"><span id="AUGMENTS_clause"></span><span id="augments_clause"></span><span id="AUGMENTS_CLAUSE"></span>AUGMENTS clause</span></span>
</dt> <dd>

<span data-ttu-id="47bcb-120">Indica que a coleção de tabelas que ele especifica pode ser considerada uma extensão de outra coleção de tabelas e pode substituir a cláusula de índice em SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="47bcb-120">Indicates that the table collection it specifies can be considered an extension of another table collection, and can replace the INDEX clause in SNMPv2.</span></span> <span data-ttu-id="47bcb-121">As coleções referenciadas pela cláusula reaumentás podem ser combinadas com a outra coleção de tabelas para formar uma coleção.</span><span class="sxs-lookup"><span data-stu-id="47bcb-121">The collections referred to by the AUGMENTS clause can be combined with the other table collection to form one collection.</span></span> <span data-ttu-id="47bcb-122">A coleção resultante compartilha as propriedades de chave primária especificadas na última coleção de tabelas na cadeia.</span><span class="sxs-lookup"><span data-stu-id="47bcb-122">The resulting collection shares the primary key properties specified in the last table collection in the chain.</span></span>

<span data-ttu-id="47bcb-123">Nesse caso, as regras de mapeamento anteriores especificadas para a cláusula INDEX são aplicadas à última coleção de tabelas na cadeia.</span><span class="sxs-lookup"><span data-stu-id="47bcb-123">In this case, the previous mapping rules specified for the INDEX clause are applied to the last table collection in the chain.</span></span> <span data-ttu-id="47bcb-124">Em seguida, a coleção de objetos é mapeada para uma definição de classe CIM.</span><span class="sxs-lookup"><span data-stu-id="47bcb-124">The collection of objects then maps to one CIM class definition.</span></span>

</dd> <dt>

<span data-ttu-id="47bcb-125"><span id="OBJECT-IDENTIFIER_clause"></span><span id="object-identifier_clause"></span><span id="OBJECT-IDENTIFIER_CLAUSE"></span>Cláusula do identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="47bcb-125"><span id="OBJECT-IDENTIFIER_clause"></span><span id="object-identifier_clause"></span><span id="OBJECT-IDENTIFIER_CLAUSE"></span>OBJECT-IDENTIFIER clause</span></span>
</dt> <dd>

<span data-ttu-id="47bcb-126">Contém um identificador de objeto exclusivo para um objeto MIB.</span><span class="sxs-lookup"><span data-stu-id="47bcb-126">Contains a unique object identifier for an MIB object.</span></span> <span data-ttu-id="47bcb-127">Esse identificador de objeto é mapeado para o **\_ identificador de objeto** de qualificador de propriedade CIM.</span><span class="sxs-lookup"><span data-stu-id="47bcb-127">This object identifier maps to the CIM property qualifier **object\_identifier**.</span></span>

</dd> <dt>

<span data-ttu-id="47bcb-128"><span id="ACCESS_and_MAX-ACCESS_Clauses"></span><span id="access_and_max-access_clauses"></span><span id="ACCESS_AND_MAX-ACCESS_CLAUSES"></span>[Cláusulas ACCESS e MAX-ACCESS](access-and-max-access-clauses.md)</span><span class="sxs-lookup"><span data-stu-id="47bcb-128"><span id="ACCESS_and_MAX-ACCESS_Clauses"></span><span id="access_and_max-access_clauses"></span><span id="ACCESS_AND_MAX-ACCESS_CLAUSES"></span>[ACCESS and MAX-ACCESS Clauses](access-and-max-access-clauses.md)</span></span>
</dt> <dd>

<span data-ttu-id="47bcb-129">Defina os direitos de acesso ao objeto MIB.</span><span class="sxs-lookup"><span data-stu-id="47bcb-129">Define the access rights to the MIB object.</span></span>

</dd> <dt>

<span data-ttu-id="47bcb-130"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>Cláusula de descrição</span><span class="sxs-lookup"><span data-stu-id="47bcb-130"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>DESCRIPTION clause</span></span>
</dt> <dd>

<span data-ttu-id="47bcb-131">Fornece uma descrição de texto do objeto, que é mapeada para a **Descrição** do qualificador de propriedade CIM.</span><span class="sxs-lookup"><span data-stu-id="47bcb-131">Provides a text description of the object, which maps to the CIM property qualifier **Description**.</span></span> <span data-ttu-id="47bcb-132">Essa cláusula pode estar vazia.</span><span class="sxs-lookup"><span data-stu-id="47bcb-132">This clause may be empty.</span></span>

<span data-ttu-id="47bcb-133">Cada **tabela** e objeto de **entrada** em uma definição de tabela SNMP também contém uma cláusula Description, que também pode estar vazia.</span><span class="sxs-lookup"><span data-stu-id="47bcb-133">Each **TABLE** and **ENTRY** object in an SNMP table definition also contains a DESCRIPTION clause, which also may be empty.</span></span> <span data-ttu-id="47bcb-134">As cláusulas de descrição de tabela e entrada são concatenadas e o resultado é mapeado para a **Descrição** do qualificador de classe CIM.</span><span class="sxs-lookup"><span data-stu-id="47bcb-134">The TABLE and ENTRY DESCRIPTION clauses are concatenated and the result maps to the CIM class qualifier **Description**.</span></span>

</dd> <dt>

<span data-ttu-id="47bcb-135"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>Cláusula de STATUS</span><span class="sxs-lookup"><span data-stu-id="47bcb-135"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>STATUS clause</span></span>
</dt> <dd>

<span data-ttu-id="47bcb-136">Indica se o objeto deve ter suporte.</span><span class="sxs-lookup"><span data-stu-id="47bcb-136">Indicates whether the object must be supported.</span></span> <span data-ttu-id="47bcb-137">Quando o valor da cláusula STATUS é **obsoleto**, o provedor descarta o objeto MIB do mapeamento.</span><span class="sxs-lookup"><span data-stu-id="47bcb-137">When the value of the STATUS clause is **obsolete**, the provider discards the MIB object from the mapping.</span></span> <span data-ttu-id="47bcb-138">Caso contrário, a cláusula de STATUS será mapeada para o **status** do qualificador de propriedade CIM.</span><span class="sxs-lookup"><span data-stu-id="47bcb-138">Otherwise, the STATUS clause maps to the CIM property qualifier **Status**.</span></span>

<span data-ttu-id="47bcb-139">Para SNMPv1, o valor preferencial do **status** é **obrigatório** ou **opcional**, mas o qualificador pode conter algum outro valor.</span><span class="sxs-lookup"><span data-stu-id="47bcb-139">For SNMPv1, the preferred value of **Status** is either **mandatory** or **optional**, but the qualifier can contain some other value.</span></span> <span data-ttu-id="47bcb-140">Para o SNMPv2C, o valor preferencial do **status** é **atual** ou **preterido**, mas o qualificador pode conter algum outro valor.</span><span class="sxs-lookup"><span data-stu-id="47bcb-140">For SNMPv2C, the preferred value of **Status** is either **current** or **deprecated**, but the qualifier can contain some other value.</span></span>

</dd> <dt>

<span data-ttu-id="47bcb-141"><span id="DEFVAL_clause"></span><span id="defval_clause"></span><span id="DEFVAL_CLAUSE"></span>Cláusula DEFVAL</span><span class="sxs-lookup"><span data-stu-id="47bcb-141"><span id="DEFVAL_clause"></span><span id="defval_clause"></span><span id="DEFVAL_CLAUSE"></span>DEFVAL clause</span></span>
</dt> <dd>

<span data-ttu-id="47bcb-142">Atribui um valor padrão a uma variável em uma linha de tabela lógica e mapeia para o qualificador de propriedade CIM de cadeia de caracteres **defval**.</span><span class="sxs-lookup"><span data-stu-id="47bcb-142">Assigns a default value to a variable in a logical table row, and maps to the string CIM property qualifier **Defval**.</span></span>

</dd> <dt>

<span data-ttu-id="47bcb-143"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>Cláusula de referência</span><span class="sxs-lookup"><span data-stu-id="47bcb-143"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>REFERENCE clause</span></span>
</dt> <dd>

<span data-ttu-id="47bcb-144">Refere-se a outro documento que contém mais informações sobre o objeto.</span><span class="sxs-lookup"><span data-stu-id="47bcb-144">Refers to another document that contains more information about the object.</span></span> <span data-ttu-id="47bcb-145">Essa cláusula é mapeada para a **referência** do qualificador de propriedade CIM, que é do tipo cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="47bcb-145">This clause maps to the CIM property qualifier **Reference**, which is of type string.</span></span>

</dd> <dt>

<span data-ttu-id="47bcb-146"><span id="UNITS_clause"></span><span id="units_clause"></span><span id="UNITS_CLAUSE"></span>Cláusula UNITs</span><span class="sxs-lookup"><span data-stu-id="47bcb-146"><span id="UNITS_clause"></span><span id="units_clause"></span><span id="UNITS_CLAUSE"></span>UNITS clause</span></span>
</dt> <dd>

<span data-ttu-id="47bcb-147">Fornece uma definição precisa do que o objeto representa.</span><span class="sxs-lookup"><span data-stu-id="47bcb-147">Provides a precise definition of what the object represents.</span></span> <span data-ttu-id="47bcb-148">Essa cláusula é mapeada para as **unidades** de qualificador de propriedade CIM, que é do tipo cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="47bcb-148">This clause maps to the CIM property qualifier **Units**, which is of type string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47bcb-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="47bcb-149">Remarks</span></span>

<span data-ttu-id="47bcb-150">A macro do tipo de objeto descreve as características básicas de um objeto MIB individual.</span><span class="sxs-lookup"><span data-stu-id="47bcb-150">The OBJECT-TYPE macro describes the basic characteristics of an individual MIB object.</span></span> <span data-ttu-id="47bcb-151">Um conjunto de macros de tipo de objeto pode ser considerado um grupo de objetos relacionados.</span><span class="sxs-lookup"><span data-stu-id="47bcb-151">A set of OBJECT-TYPE macros can be considered as a group of related objects.</span></span> <span data-ttu-id="47bcb-152">No SNMPv2C, use a macro do grupo de objetos para agrupar formalmente os conjuntos de objetos relacionados em uma coleção.</span><span class="sxs-lookup"><span data-stu-id="47bcb-152">In SNMPv2C, use the OBJECT-GROUP macro to formally group sets of related objects into a collection.</span></span> <span data-ttu-id="47bcb-153">No entanto, não há um mecanismo formal para a criação de coleções em SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="47bcb-153">However, there is no formal mechanism for creating collections in SNMPv1.</span></span> <span data-ttu-id="47bcb-154">Para os fins do provedor SNMP, a macro do grupo de objetos é ignorada, mas você pode inventar o agrupamento de relações e as coleções de malha.</span><span class="sxs-lookup"><span data-stu-id="47bcb-154">For the purposes of the SNMP Provider, the OBJECT-GROUP macro is ignored, but you can invent grouping relationships and fabricate collections.</span></span>

 

 



