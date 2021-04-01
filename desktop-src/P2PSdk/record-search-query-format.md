---
description: Uma chamada para a função PeerGroupSearchRecords requer um parâmetro de cadeia de caracteres de consulta XML que é usado para determinar os critérios básicos de uma pesquisa.
ms.assetid: 2c5ab425-6959-418a-8d9a-c8155257fc7e
title: Gravar formato de consulta de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b475c8a449e3bcd360df5757fef508b1a744d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829333"
---
# <a name="record-search-query-format"></a><span data-ttu-id="3e5ee-103">Gravar formato de consulta de pesquisa</span><span class="sxs-lookup"><span data-stu-id="3e5ee-103">Record Search Query Format</span></span>

<span data-ttu-id="3e5ee-104">Uma chamada para a função [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) requer um parâmetro de cadeia de caracteres de consulta XML que é usado para determinar os critérios básicos de uma pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-104">A call to the [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) function requires an XML query string parameter that is used to determine the basic criteria of a search.</span></span> <span data-ttu-id="3e5ee-105">Use o esquema a seguir para formular uma cadeia de caracteres XML:</span><span class="sxs-lookup"><span data-stu-id="3e5ee-105">Use the following schema to formulate an XML string:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema">

  <xs:simpleType name="alphanumType">
     <xs:restriction base="xs:string">
        <xs:pattern value="\c+"/>
     </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="operatorType">
      <xs:choice maxOccurs="unbounded">
         <xs:element ref="and" />
         <xs:element ref="or" />
         <xs:element ref="clause" />
      </xs:choice>
  </xs:complexType>

  <xs:element name="and" type="operatorType"/>

  <xs:element name="or" type="operatorType"/>

  <xs:element name="clause">
      <xs:complexType>
          <xs:simpleContent>
              <xs:extension base="xs:string">
        <xs:attribute name="attrib" type="alphanumType" />
        <xs:attribute name="type">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="string"/>
                      <xs:enumeration value="date"/>
                      <xs:enumeration value="int"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:attribute>
        <xs:attribute name="compare" default="equal">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="equal"/>
                      <xs:enumeration value="greater"/>
                      <xs:enumeration value="less"/>
                      <xs:enumeration value="notequal"/>
                      <xs:enumeration value="greaterorequal"/>
                      <xs:enumeration value="lessorequal"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:attribute>
              </xs:extension>
          </xs:simpleContent>
      </xs:complexType>
  </xs:element>

  <xs:element name="peersearch">
      <xs:complexType>
          <xs:choice>
              <xs:element ref="clause" />
              <xs:element ref="and" />
              <xs:element ref="or" />
          </xs:choice>
      </xs:complexType>
  </xs:element>
</xs:schema> 
```

### <a name="elements-to-use-for-a-record-search"></a><span data-ttu-id="3e5ee-106">Elementos a serem usados para uma pesquisa de registro</span><span class="sxs-lookup"><span data-stu-id="3e5ee-106">Elements to Use for a Record Search</span></span>

<span data-ttu-id="3e5ee-107">O elemento principal em uma pesquisa de registro é **peersearch**, que contém a Uniform Resource Identifier (URI) do esquema associado no atributo **xmlns** .</span><span class="sxs-lookup"><span data-stu-id="3e5ee-107">The primary element in a record search is **peersearch**, which contains the Uniform Resource Identifier (URI) of the associated schema in the **xmlns** attribute.</span></span> <span data-ttu-id="3e5ee-108">Quando **peersearch** é usado como um elemento filho, você pode usar **e**, **cláusula** e **ou** como elementos filho.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-108">When **peersearch** is used as a child element, you can use **and**, **clause**, and **or** as child elements.</span></span>

-   <span data-ttu-id="3e5ee-109">**e** -o elemento **and** executa uma operação and lógica em uma ou mais cláusulas contidas entre as marcas de abertura e de fechamento.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-109">**and** - The **and** element performs a logical AND operation on one or more clauses contained between the opening and closing tags.</span></span> <span data-ttu-id="3e5ee-110">Outras marcas **e** e **ou** podem ser filhas, e os resultados recursivos de suas cláusulas filho são incluídos na operação.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-110">Other **and** and **or** tags can be children, and recursive results of their child clauses are included in the operation.</span></span>

    <span data-ttu-id="3e5ee-111">Por exemplo, se você quiser obter um registro que contém um nome igual a James Peters e uma última atualização maior que 2/28/2003, ou uma data de criação menor que 1/31/2003, use a seguinte cadeia de caracteres de consulta XML:</span><span class="sxs-lookup"><span data-stu-id="3e5ee-111">For example, if you want to obtain a record that contains a name equal to James Peters, and a last update that is greater than 2/28/2003, or a creation date that is less than 1/31/2003, use the following XML query string:</span></span>

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <and>
          <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
          <or>
             <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
             <clause attrib="peercreationtime" type="date" compare="less">2003-02-328</clause>
          </or>
       </and>
    </peersearch>
    ```

<!-- -->

-   <span data-ttu-id="3e5ee-112">**cláusula** -o elemento **Clause** especifica uma regra comparativa básica que compara o valor de um atributo de registro específico com o valor contido entre as marcas de abertura e de fechamento.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-112">**clause** - The **clause** element specifies a basic comparative rule that compares the value of a specific record attribute with the value contained between the opening and closing tags.</span></span> <span data-ttu-id="3e5ee-113">Os atributos **Type** e **Compare** devem ser fornecidos **Compare** indica a operação de comparação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-113">The **type** and **compare** attributes must be provided **compare** indicates the comparison operation to be performed.</span></span> <span data-ttu-id="3e5ee-114">Por exemplo, uma pesquisa simples que indica que todos os registros correspondentes deve ter um valor de **peercreatorid** igual a James Peters aparece na cadeia de caracteres de consulta XML como a seguir:</span><span class="sxs-lookup"><span data-stu-id="3e5ee-114">For example, a simple search that indicates all matched records must have a **peercreatorid** value equal to James Peters appears in the XML query string as the following:</span></span>

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
    </peersearch>
    ```

    <span data-ttu-id="3e5ee-115">Os atributos de **tipo** comum incluem **int**, **String** e **Date**.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-115">Common **type** attributes include **int**, **string**, and **date**.</span></span> <span data-ttu-id="3e5ee-116">O atributo **Date** pode ser um dos formatos de data padrão descritos em [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .</span><span class="sxs-lookup"><span data-stu-id="3e5ee-116">The **date** attribute can be one of the standard date formats described at [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime).</span></span>

    <span data-ttu-id="3e5ee-117">Os valores para o atributo de **comparação** são **igual**, não **igual**, **menor**, **maior**, **lessorequal** e **greaterorequal**.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-117">Values for the **compare** attribute are **equal**, **notequal**, **less**, **greater**, **lessorequal**, and **greaterorequal**.</span></span>

<!-- -->

-   <span data-ttu-id="3e5ee-118">**or** -o elemento **or** executa uma operação OR lógica em uma ou mais cláusulas contidas entre as marcas de abertura e de fechamento.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-118">**or** - The **or** element performs a logical OR operation on one or more clauses contained between the opening and closing tags.</span></span> <span data-ttu-id="3e5ee-119">Outros elementos **ou** e **e** podem ser filhos, e os resultados recursivos das cláusulas filho são incluídos na operação.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-119">Other **or** and **and** elements can be children, and recursive results of the child clauses are included in the operation.</span></span> <span data-ttu-id="3e5ee-120">Por exemplo, se você quiser obter um registro que contenha um nome igual a James Peters ou uma última atualização que esteja entre 1/31/2003 e 2/28/2003, use a seguinte cadeia de caracteres de consulta XML:</span><span class="sxs-lookup"><span data-stu-id="3e5ee-120">For example, if you want to obtain a record that contains a name equal to James Peters, or a last update that is between 1/31/2003 and 2/28/2003, use the following XML query string:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <or>
      <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
      <and>
         <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
         <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
      </and>
   </or>
</peersearch>
```

## <a name="more-information-about-a-record-search"></a><span data-ttu-id="3e5ee-121">Mais informações sobre uma pesquisa de registro</span><span class="sxs-lookup"><span data-stu-id="3e5ee-121">More Information About a Record Search</span></span>

<span data-ttu-id="3e5ee-122">O primeiro nível de nós após **peersearch** pode ter apenas um elemento.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-122">The first level of nodes after **peersearch** can have only one element.</span></span> <span data-ttu-id="3e5ee-123">No entanto, os filhos subsequentes desse elemento podem ter muitos elementos no mesmo nível.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-123">However, subsequent children of that element can have many elements at the same level.</span></span>

<span data-ttu-id="3e5ee-124">A seguinte consulta de pesquisa está incorreta:</span><span class="sxs-lookup"><span data-stu-id="3e5ee-124">The following search query is incorrect:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
   <and>
      <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
      <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
   </and>
</peersearch>
```

<span data-ttu-id="3e5ee-125">A consulta falha porque dois valores são retornados para a correspondência sem serem resolvidos em um valor verdadeiro/falso, o que significa que uma cláusula é uma consulta para o nome de um registro que é igual a James Peters, e a operação AND corresponde às duas cláusulas de componente.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-125">The query fails because two values are returned for the match without being resolved into one true/false value, which means that one clause is a query for the name of a record that equals James Peters, and the AND operation matches the two component clauses.</span></span> <span data-ttu-id="3e5ee-126">O resultado são dois valores lógicos true/false que são contraditórias.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-126">The result is two logical true/false values that are contradictory.</span></span>

<span data-ttu-id="3e5ee-127">Para obter todos os registros que contêm um nome igual a James Peters e uma última atualização entre 1/31/2003 e 2/28/2003, coloque a **cláusula** **e as marcas que** estão no mesmo nível entre abertura e fechamento **e** marcas.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-127">To obtain all records that contain a name equal to James Peters, and a last update that is between 1/31/2003 and 2/28/2003, place the **clause** and **and** tags that are at the same level between opening and closing **and** tags.</span></span> <span data-ttu-id="3e5ee-128">O exemplo a seguir mostra a consulta bem-sucedida:</span><span class="sxs-lookup"><span data-stu-id="3e5ee-128">The following example shows you the successful query:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
    <and>
      <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
      <and>
         <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
         <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
      </and>
   </and>
</peersearch>
```

<span data-ttu-id="3e5ee-129">A lista a seguir identifica outras informações específicas que você deve saber para escrever uma consulta bem-sucedida:</span><span class="sxs-lookup"><span data-stu-id="3e5ee-129">The following list identifies other specific information that you must know to write a successful query:</span></span>

-   <span data-ttu-id="3e5ee-130">As marcas **e** e **ou** não podem ser localizadas entre marcas de **cláusula** de abertura e fechamento porque, nessa configuração, elas são interpretadas como parte do valor para correspondência, o que resulta em um erro ou uma correspondência com falha.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-130">The **and** and **or** tags cannot be located between opening and closing **clause** tags because, in that configuration, they are interpreted as part of the value to match against, which results in an error or a failed match.</span></span>
-   <span data-ttu-id="3e5ee-131">Cada **par de marcas e/** **ou** abertura e fechamento deve incluir pelo menos um ou mais nós filho.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-131">Each pair of **and** and **or** opening and closing tags must include at least one or more child nodes.</span></span>
-   <span data-ttu-id="3e5ee-132">Um conjunto zero de elementos não é permitido neste esquema.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-132">A zero set of elements is not allowed in this schema.</span></span>

## <a name="record-attributes"></a><span data-ttu-id="3e5ee-133">Atributos de registro</span><span class="sxs-lookup"><span data-stu-id="3e5ee-133">Record Attributes</span></span>

<span data-ttu-id="3e5ee-134">Usando o [esquema de atributo de registro](record-attribute-schema.md), um usuário pode criar atributos de registro que o atributo XML **attrib** em um elemento de cláusula especifica.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-134">By using the [Record Attribute Schema](record-attribute-schema.md), a user can create record attributes that the **attrib** XML attribute in a clause element specifies.</span></span> <span data-ttu-id="3e5ee-135">Os atributos para um novo registro são adicionados definindo o membro **pszAttributes** do [**\_ registro de pares**](/windows/desktop/api/P2P/ns-p2p-peer_record) para uma cadeia de caracteres XML usando o formato especificado no esquema.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-135">Attributes for a new record are added by setting the **pszAttributes** member of [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) to an XML string using the format specified in the schema.</span></span>

<span data-ttu-id="3e5ee-136">A infraestrutura de pares reserva os seguintes nomes de atributo:</span><span class="sxs-lookup"><span data-stu-id="3e5ee-136">The Peer Infrastructure reserves the following attribute names:</span></span>

-   <span data-ttu-id="3e5ee-137">**peerlastmodifiedby**</span><span class="sxs-lookup"><span data-stu-id="3e5ee-137">**peerlastmodifiedby**</span></span>
-   <span data-ttu-id="3e5ee-138">**peercreatorid**</span><span class="sxs-lookup"><span data-stu-id="3e5ee-138">**peercreatorid**</span></span>
-   <span data-ttu-id="3e5ee-139">**peerlastmodificationtime**</span><span class="sxs-lookup"><span data-stu-id="3e5ee-139">**peerlastmodificationtime**</span></span>
-   <span data-ttu-id="3e5ee-140">**peerrecordid**</span><span class="sxs-lookup"><span data-stu-id="3e5ee-140">**peerrecordid**</span></span>
-   <span data-ttu-id="3e5ee-141">**peerrecordtype**</span><span class="sxs-lookup"><span data-stu-id="3e5ee-141">**peerrecordtype**</span></span>
-   <span data-ttu-id="3e5ee-142">**peercreationtime**</span><span class="sxs-lookup"><span data-stu-id="3e5ee-142">**peercreationtime**</span></span>
-   <span data-ttu-id="3e5ee-143">**peerlastmodificationtime**</span><span class="sxs-lookup"><span data-stu-id="3e5ee-143">**peerlastmodificationtime**</span></span>

## <a name="special-characters"></a><span data-ttu-id="3e5ee-144">Caracteres Especiais</span><span class="sxs-lookup"><span data-stu-id="3e5ee-144">Special Characters</span></span>

<span data-ttu-id="3e5ee-145">Determinados caracteres podem ser usados para expressar padrões de correspondência ou para escapar outros caracteres especiais.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-145">Certain characters can be used to express matching patterns, or to escape other special characters.</span></span> <span data-ttu-id="3e5ee-146">Esses caracteres são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-146">These characters are described in the table below.</span></span> 

| <span data-ttu-id="3e5ee-147">Padrão de caractere</span><span class="sxs-lookup"><span data-stu-id="3e5ee-147">Character pattern</span></span> | <span data-ttu-id="3e5ee-148">Descrição</span><span class="sxs-lookup"><span data-stu-id="3e5ee-148">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*                | <span data-ttu-id="3e5ee-149">O caractere curinga.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-149">The wildcard character.</span></span> <span data-ttu-id="3e5ee-150">Quando esse caractere é encontrado em um valor de cláusula, ele corresponde a 0-n caracteres de qualquer valor, incluindo caracteres de espaço em branco e não alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-150">When this character is encountered in a clause value, it matches 0-n characters of any value, including whitespace and nonalphanumeric characters.</span></span> <span data-ttu-id="3e5ee-151">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="3e5ee-151">For example:</span></span><br/> <span data-ttu-id="3e5ee-152">"<clause attrib="peercreatorid" type="string" compare="equal">James P \* </clause>"</span><span class="sxs-lookup"><span data-stu-id="3e5ee-152">"<clause attrib="peercreatorid" type="string" compare="equal">James P\*</clause>"</span></span><br/> <span data-ttu-id="3e5ee-153">Essa cláusula corresponde a todos os valores de **peercreatorid** com um nome "James" e um sobrenome começando com "P".</span><span class="sxs-lookup"><span data-stu-id="3e5ee-153">This clause matches all **peercreatorid** values with a first name of "James" and a last name starting with "P".</span></span><br/> |
| \\\*              | <span data-ttu-id="3e5ee-154">Um asterisco com escape.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-154">An escaped asterisk.</span></span> <span data-ttu-id="3e5ee-155">Essa sequência corresponde a um caractere de asterisco.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-155">This sequence matches an asterisk character.</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="3e5ee-156">?</span><span class="sxs-lookup"><span data-stu-id="3e5ee-156">?</span></span>                 | <span data-ttu-id="3e5ee-157">O caractere curinga de caractere único.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-157">The single-character wildcard character.</span></span> <span data-ttu-id="3e5ee-158">Quando esse caractere é encontrado em um valor de cláusula, ele corresponde a qualquer caractere único, incluindo caracteres de espaço em branco e não alfanuméricos. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="3e5ee-158">When this character is encountered in a clause value, it matches any single character, including whitespace and nonalphanumeric characters.For example:</span></span><br/> <span data-ttu-id="3e5ee-159">"<clause attrib="filename" type="string" compare="equal">data-0?. XML</clause>"</span><span class="sxs-lookup"><span data-stu-id="3e5ee-159">"<clause attrib="filename" type="string" compare="equal">data-0?.xml</clause>"</span></span><br/> <span data-ttu-id="3e5ee-160">Essa cláusula corresponde aos valores de **nome de arquivo** como "data-01.xml" e "data-0B.xml".</span><span class="sxs-lookup"><span data-stu-id="3e5ee-160">This clause matches **filename** values like "data-01.xml" and "data-0B.xml".</span></span><br/>                              |
| <span data-ttu-id="3e5ee-161">\\?</span><span class="sxs-lookup"><span data-stu-id="3e5ee-161">\\?</span></span>               | <span data-ttu-id="3e5ee-162">Um ponto de interrogação de escape.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-162">An escaped question mark.</span></span> <span data-ttu-id="3e5ee-163">Essa sequência corresponde a um caractere de ponto de interrogação.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-163">This sequence matches a question mark character.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| \\\\              | <span data-ttu-id="3e5ee-164">Uma barra invertida de escape.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-164">An escaped backslash.</span></span> <span data-ttu-id="3e5ee-165">Essa sequência corresponde a um caractere de barra invertida simples.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-165">This sequence matches a single backslash character.</span></span>                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="3e5ee-166">Se a sequência de caracteres não for válida, a função [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) retornará o erro **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="3e5ee-166">If the character sequence is not valid, the [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) function returns the error **E\_INVALIDARG**.</span></span> <span data-ttu-id="3e5ee-167">Uma sequência inválida é qualquer sequência que contenha um \\ caractere "" (barra invertida) não seguido imediatamente por um \* caractere "" (asterisco), um "?" (ponto de interrogação) ou outro \\ caractere "" (barra invertida).</span><span class="sxs-lookup"><span data-stu-id="3e5ee-167">An invalid sequence is any sequence that contains a "\\" (backslash) character not immediately followed by either an "\*" (asterisk) character, a "?" (question mark) character, or another "\\" (backslash) character.</span></span>

 

 




