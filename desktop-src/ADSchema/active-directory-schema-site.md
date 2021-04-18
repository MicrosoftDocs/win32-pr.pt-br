---
title: Terminologia de esquema de Active Directory
description: Os termos a seguir são comumente usados para se referir ao esquema de Active Directory.
ms.assetid: 22c5756f-d663-4cb7-aab0-956b22a01e9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efca7057a79d87c45cc3e3da4b604e842143fedd
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "105771745"
---
# <a name="active-directory-schema-terminology"></a><span data-ttu-id="eb523-103">Terminologia de esquema de Active Directory</span><span class="sxs-lookup"><span data-stu-id="eb523-103">Active Directory Schema Terminology</span></span>

<span data-ttu-id="eb523-104">Os termos a seguir são comumente usados para se referir ao esquema de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="eb523-104">The following terms are commonly used to refer to the Active Directory schema.</span></span>


<dl> <dt>

<span data-ttu-id="eb523-105"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span><span class="sxs-lookup"><span data-stu-id="eb523-105"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="eb523-106">Itens de dados usados para descrever os objetos que são representados pelas classes que são definidas no esquema.</span><span class="sxs-lookup"><span data-stu-id="eb523-106">Data items used to describe the objects that are represented by the classes that are defined in the schema.</span></span> <span data-ttu-id="eb523-107">Os atributos são definidos no esquema separadamente das classes; Isso permite que uma única definição de atributo seja aplicada a várias classes.</span><span class="sxs-lookup"><span data-stu-id="eb523-107">Attributes are defined in the schema separately from the classes; this allows a single attribute definition to be applied to many classes.</span></span> <span data-ttu-id="eb523-108">Por exemplo, [**Descrição**](a-description.md) é um atributo que pode ser aplicado a qualquer classe no esquema.</span><span class="sxs-lookup"><span data-stu-id="eb523-108">For example, [**Description**](a-description.md) is an attribute that can be applied to any class in the schema.</span></span> <span data-ttu-id="eb523-109">O atributo de **Descrição** é definido uma vez no esquema, garantindo a consistência, em vez de ter uma definição diferente para a **Descrição** de um usuário e uma **Descrição** de uma impressora.</span><span class="sxs-lookup"><span data-stu-id="eb523-109">The **Description** attribute is defined once in the schema, assuring consistency, rather than having a different definition for **Description** of a user and **Description** of a printer.</span></span>

> [!Note]  
> <span data-ttu-id="eb523-110">A *Propriedade* Term é frequentemente usada de forma intercambiável com o *atributo* Term.</span><span class="sxs-lookup"><span data-stu-id="eb523-110">The term *property* is frequently used interchangeably with the term *attribute*.</span></span>

 

</dd> <dt>

<span data-ttu-id="eb523-111"><span id="Attribute_Instance"></span><span id="attribute_instance"></span><span id="ATTRIBUTE_INSTANCE"></span>Instância de atributo</span><span class="sxs-lookup"><span data-stu-id="eb523-111"><span id="Attribute_Instance"></span><span id="attribute_instance"></span><span id="ATTRIBUTE_INSTANCE"></span>Attribute Instance</span></span>
</dt> <dd>

<span data-ttu-id="eb523-112">Uma ocorrência de um atributo que é definido no esquema.</span><span class="sxs-lookup"><span data-stu-id="eb523-112">An occurrence of an attribute that is defined in the schema.</span></span> <span data-ttu-id="eb523-113">Esse termo é usado para distinguir entre a definição de um atributo e uma ocorrência discreta do atributo.</span><span class="sxs-lookup"><span data-stu-id="eb523-113">This term is used to distinguish between the definition of an attribute and a discrete occurrence of the attribute.</span></span> <span data-ttu-id="eb523-114">Por exemplo, armazenar um objeto de usuário para "Jeff Smith" com o atributo de [**nome comum**](a-cn.md) definido como "Jeff Smith" cria uma instância de [**nome comum**](a-cn.md).</span><span class="sxs-lookup"><span data-stu-id="eb523-114">For example, storing a User object for "Jeff Smith" with the [**Common-Name**](a-cn.md) attribute set to "Jeff Smith" creates an instance of [**Common-Name**](a-cn.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb523-115"><span id="Class"></span><span id="class"></span><span id="CLASS"></span>Classes</span><span class="sxs-lookup"><span data-stu-id="eb523-115"><span id="Class"></span><span id="class"></span><span id="CLASS"></span>Class</span></span>
</dt> <dd>

<span data-ttu-id="eb523-116">Uma descrição formal de um tipo discreto e identificável de objeto armazenado no serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="eb523-116">A formal description of a discrete, identifiable type of object stored in the directory service.</span></span> <span data-ttu-id="eb523-117">Por exemplo, [**usuário**](c-user.md), [**fila de impressão**](c-printqueue.md)e [**grupo**](c-group.md) são todas as classes.</span><span class="sxs-lookup"><span data-stu-id="eb523-117">For example, [**User**](c-user.md), [**Print-Queue**](c-printqueue.md), and [**Group**](c-group.md) are all classes.</span></span> <span data-ttu-id="eb523-118">Além disso, há 3 categorias distintas de classes: [classes estruturais](classes-structural.md), [classes abstratas](classes-abstract.md)e [classes auxiliares](classes-auxiliary.md).</span><span class="sxs-lookup"><span data-stu-id="eb523-118">Furthermore, there are 3 distinct categories of classes: [Structural Classes](classes-structural.md), [Abstract Classes](classes-abstract.md), and [Auxiliary Classes](classes-auxiliary.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb523-119"><span id="Class_Instance"></span><span id="class_instance"></span><span id="CLASS_INSTANCE"></span>Instância de classe</span><span class="sxs-lookup"><span data-stu-id="eb523-119"><span id="Class_Instance"></span><span id="class_instance"></span><span id="CLASS_INSTANCE"></span>Class Instance</span></span>
</dt> <dd>

<span data-ttu-id="eb523-120">Uma ocorrência de uma classe que é definida no esquema.</span><span class="sxs-lookup"><span data-stu-id="eb523-120">An occurrence of a class that is defined in the schema.</span></span> <span data-ttu-id="eb523-121">Esse termo é usado para distinguir entre a definição de uma classe e uma ocorrência discreta da classe.</span><span class="sxs-lookup"><span data-stu-id="eb523-121">This term is used to distinguish between the definition of a class and a discrete occurrence of the class.</span></span> <span data-ttu-id="eb523-122">Por exemplo, o armazenamento de um objeto de [**usuário**](c-user.md) para "Jeff Smith" no serviço de diretório cria uma instância de [**usuário**](c-user.md).</span><span class="sxs-lookup"><span data-stu-id="eb523-122">For example, storing a [**User**](c-user.md) object for "Jeff Smith" in the directory service creates an instance of [**User**](c-user.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb523-123"><span id="Content_Rules"></span><span id="content_rules"></span><span id="CONTENT_RULES"></span>Regras de conteúdo</span><span class="sxs-lookup"><span data-stu-id="eb523-123"><span id="Content_Rules"></span><span id="content_rules"></span><span id="CONTENT_RULES"></span>Content Rules</span></span>
</dt> <dd>

<span data-ttu-id="eb523-124">A definição do conteúdo possível das instâncias de classe que são armazenadas no serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="eb523-124">The definition of the possible contents of the class instances that are stored in the directory service.</span></span> <span data-ttu-id="eb523-125">Nos serviços de diretório do NT (NTDS), no qual Active Directory é baseado, as regras de conteúdo são completamente expressas pelos atributos [**deve conter**](a-mustcontain.md) e [**pode conter**](a-maycontain.md) de definições de esquema para cada classe.</span><span class="sxs-lookup"><span data-stu-id="eb523-125">In NT Directory Services (NTDS), upon which Active Directory is based, the content rules are completely expressed by the [**Must-Contain**](a-mustcontain.md) and [**May-Contain**](a-maycontain.md) attributes of the schema definitions for each class.</span></span>

</dd> <dt>

<span data-ttu-id="eb523-126"><span id="Derivation"></span><span id="derivation"></span><span id="DERIVATION"></span>Derivação</span><span class="sxs-lookup"><span data-stu-id="eb523-126"><span id="Derivation"></span><span id="derivation"></span><span id="DERIVATION"></span>Derivation</span></span>
</dt> <dd>

<span data-ttu-id="eb523-127">Consulte *herança*.</span><span class="sxs-lookup"><span data-stu-id="eb523-127">See *Inheritance*.</span></span>

</dd> <dt>

<span data-ttu-id="eb523-128"><span id="Directory_Information_Tree"></span><span id="directory_information_tree"></span><span id="DIRECTORY_INFORMATION_TREE"></span>Árvore de informações do diretório</span><span class="sxs-lookup"><span data-stu-id="eb523-128"><span id="Directory_Information_Tree"></span><span id="directory_information_tree"></span><span id="DIRECTORY_INFORMATION_TREE"></span>Directory Information Tree</span></span>
</dt> <dd>

<span data-ttu-id="eb523-129">O próprio diretório, representado como uma estrutura de árvore na qual os vértices são as entradas de diretório (instâncias de classe) e as linhas de conexão as relações pai-filho entre as entradas.</span><span class="sxs-lookup"><span data-stu-id="eb523-129">The directory itself, represented as a tree structure in which the vertices are the directory entries (class instances) and the connecting lines the parent-child relationships between the entries.</span></span>

</dd> <dt>

<span data-ttu-id="eb523-130"><span id="DIT"></span><span id="dit"></span>DITA</span><span class="sxs-lookup"><span data-stu-id="eb523-130"><span id="DIT"></span><span id="dit"></span>DIT</span></span>
</dt> <dd>

<span data-ttu-id="eb523-131">Consulte *árvore de informações do diretório*.</span><span class="sxs-lookup"><span data-stu-id="eb523-131">See *Directory Information Tree*.</span></span>

</dd> <dt>

<span data-ttu-id="eb523-132"><span id="Control_Access_Rights"></span><span id="control_access_rights"></span><span id="CONTROL_ACCESS_RIGHTS"></span>Controlar direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="eb523-132"><span id="Control_Access_Rights"></span><span id="control_access_rights"></span><span id="CONTROL_ACCESS_RIGHTS"></span>Control Access Rights</span></span>
</dt> <dd>

<span data-ttu-id="eb523-133">Uma classe que descreve um direito de acesso não vinculado a um recurso, mas uma ação.</span><span class="sxs-lookup"><span data-stu-id="eb523-133">A class that describes an access right not tied to a resource, but an action.</span></span> <span data-ttu-id="eb523-134">Por exemplo, um usuário pode receber o direito de criar valores de ID relativos.</span><span class="sxs-lookup"><span data-stu-id="eb523-134">For example, a user can be granted the right to create relative ID values.</span></span>

</dd> <dt>

<span data-ttu-id="eb523-135"><span id="Inheritance"></span><span id="inheritance"></span><span id="INHERITANCE"></span>Herda</span><span class="sxs-lookup"><span data-stu-id="eb523-135"><span id="Inheritance"></span><span id="inheritance"></span><span id="INHERITANCE"></span>Inheritance</span></span>
</dt> <dd>

<span data-ttu-id="eb523-136">A capacidade de criar novas classes de objeto a partir de classes de objeto existentes.</span><span class="sxs-lookup"><span data-stu-id="eb523-136">The ability to build new object classes from existing object classes.</span></span> <span data-ttu-id="eb523-137">O novo objeto é definido como uma *subclasse* do objeto pai.</span><span class="sxs-lookup"><span data-stu-id="eb523-137">The new object is defined as a *subclass* of the parent object.</span></span> <span data-ttu-id="eb523-138">O objeto pai se torna uma *superclasse* do novo objeto.</span><span class="sxs-lookup"><span data-stu-id="eb523-138">The parent object becomes a *superclass* of the new object.</span></span> <span data-ttu-id="eb523-139">Uma subclasse herda os atributos do pai, incluindo regras de estrutura e regras de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="eb523-139">A subclass inherits the attributes of the parent, including structure rules and content rules.</span></span>

</dd> <dt>

<span data-ttu-id="eb523-140"><span id="LDAP"></span><span id="ldap"></span>LDAP</span><span class="sxs-lookup"><span data-stu-id="eb523-140"><span id="LDAP"></span><span id="ldap"></span>LDAP</span></span>
</dt> <dd>

<span data-ttu-id="eb523-141">Consulte *Lightweight Directory Access Protocol*.</span><span class="sxs-lookup"><span data-stu-id="eb523-141">See *Lightweight Directory Access Protocol*.</span></span>

</dd> <dt>

<span data-ttu-id="eb523-142"><span id="Lightweight_Directory_Access_Protocol"></span><span id="lightweight_directory_access_protocol"></span><span id="LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL"></span>Protocolo Lightweight Directory Access</span><span class="sxs-lookup"><span data-stu-id="eb523-142"><span id="Lightweight_Directory_Access_Protocol"></span><span id="lightweight_directory_access_protocol"></span><span id="LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL"></span>Lightweight Directory Access Protocol</span></span>
</dt> <dd>

<span data-ttu-id="eb523-143">Um protocolo de comunicações padrão da Internet usado para se comunicar com o NTDS.</span><span class="sxs-lookup"><span data-stu-id="eb523-143">A standard Internet communications protocol used to communicate with the NTDS.</span></span> <span data-ttu-id="eb523-144">Há suporte para LDAP versão 2 e versão 3.</span><span class="sxs-lookup"><span data-stu-id="eb523-144">LDAP version 2 and version 3 are supported.</span></span>

</dd> <dt>

<span data-ttu-id="eb523-145"><span id="NT_Security_Descriptor"></span><span id="nt_security_descriptor"></span><span id="NT_SECURITY_DESCRIPTOR"></span>Descritor de segurança NT</span><span class="sxs-lookup"><span data-stu-id="eb523-145"><span id="NT_Security_Descriptor"></span><span id="nt_security_descriptor"></span><span id="NT_SECURITY_DESCRIPTOR"></span>NT Security Descriptor</span></span>
</dt> <dd>

<span data-ttu-id="eb523-146">Consulte *descritor de segurança*.</span><span class="sxs-lookup"><span data-stu-id="eb523-146">See *Security Descriptor*.</span></span>

</dd> <dt>

<span data-ttu-id="eb523-147"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>Objeto</span><span class="sxs-lookup"><span data-stu-id="eb523-147"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>Object</span></span>
</dt> <dd>

<span data-ttu-id="eb523-148">Uma unidade de armazenamento de dados no serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="eb523-148">A unit of data storage in the directory service.</span></span> <span data-ttu-id="eb523-149">Os objetos de serviço de diretório não devem ser confundidos com objetos COM ou outros objetos do sistema orientados a objeto, que têm um componente executável e um comportamento de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="eb523-149">Directory service objects are not to be confused with COM objects or other object-oriented system objects, which have an executable component and run-time behavior.</span></span> <span data-ttu-id="eb523-150">Os objetos de serviço de diretório consistem apenas em dados.</span><span class="sxs-lookup"><span data-stu-id="eb523-150">Directory service objects consist only of data.</span></span> <span data-ttu-id="eb523-151">Um objeto de serviço de diretório é definido por um objeto de [**esquema de classe**](c-classschema.md) e um grupo de objetos de [**esquema de atributo**](c-attributeschema.md) referenciados pelo objeto de esquema de [**classe**](c-classschema.md) .</span><span class="sxs-lookup"><span data-stu-id="eb523-151">A directory service object is defined by a [**Class-Schema**](c-classschema.md) object and a group of [**Attribute-Schema**](c-attributeschema.md) objects referenced by the [**Class-Schema**](c-classschema.md) object.</span></span>

<span data-ttu-id="eb523-152">Objetos de esquema e [**atributo de**](c-attributeschema.md) [**classe**](c-classschema.md) são objetos de serviço de diretório próprios, e têm definições no esquema como quaisquer outros objetos.</span><span class="sxs-lookup"><span data-stu-id="eb523-152">[**Class-Schema**](c-classschema.md) and [**Attribute-Schema**](c-attributeschema.md) objects are themselves directory service objects, and have definitions in the schema like any other objects.</span></span> <span data-ttu-id="eb523-153">Consulte *classe*.</span><span class="sxs-lookup"><span data-stu-id="eb523-153">See *Class*.</span></span>

</dd> <dt>

<span data-ttu-id="eb523-154"><span id="Object_Identifier"></span><span id="object_identifier"></span><span id="OBJECT_IDENTIFIER"></span>Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="eb523-154"><span id="Object_Identifier"></span><span id="object_identifier"></span><span id="OBJECT_IDENTIFIER"></span>Object Identifier</span></span>
</dt> <dd>

<span data-ttu-id="eb523-155">Valores numéricos exclusivos, emitidos por várias autoridades emissores, para identificar exclusivamente elementos de dados, sintaxes e várias outras partes de aplicativos distribuídos.</span><span class="sxs-lookup"><span data-stu-id="eb523-155">Unique numeric values, issued by various issuing authorities, to uniquely identify data elements, syntaxes, and various other parts of distributed applications.</span></span> <span data-ttu-id="eb523-156">Os identificadores de objeto (OIDs) são encontrados em aplicativos OSI, diretórios X. 500, SNMP e outros aplicativos onde a exclusividade é importante.</span><span class="sxs-lookup"><span data-stu-id="eb523-156">Object Identifiers (OIDs) are found in OSI applications, X.500 Directories, SNMP, and other applications where uniqueness is important.</span></span> <span data-ttu-id="eb523-157">Os OIDs se baseiam em uma estrutura de árvore, na qual uma autoridade emissora superior, como o ISO, aloca uma ramificação da árvore para uma subautoridade, que, por sua vez, pode alocar subramificações.</span><span class="sxs-lookup"><span data-stu-id="eb523-157">OIDs are based on a tree structure, in which a superior issuing authority, such as the ISO, allocates a branch of the tree to a sub-authority, which in turn can allocate sub-branches.</span></span>

<span data-ttu-id="eb523-158">Os OIDs no NTDS incluem alguns emitidos pelo ISO para classes e atributos X. 500 e alguns emitidos pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="eb523-158">OIDs in the NTDS include some issued by the ISO for X.500 classes and attributes, and some issued by Microsoft.</span></span> <span data-ttu-id="eb523-159">A notação OID é uma cadeia de números pontilhada, por exemplo, "1.2.840.113556.1.5.4", que se traduz como listado na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="eb523-159">OID notation is a dotted string of numbers, for example "1.2.840.113556.1.5.4", which translates as listed in the following list.</span></span> 

| <span data-ttu-id="eb523-160">Valor</span><span class="sxs-lookup"><span data-stu-id="eb523-160">Value</span></span>  | <span data-ttu-id="eb523-161">Descrição</span><span class="sxs-lookup"><span data-stu-id="eb523-161">Description</span></span>                                                                                  |
|--------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb523-162">1</span><span class="sxs-lookup"><span data-stu-id="eb523-162">1</span></span>      | <span data-ttu-id="eb523-163">ISO-a "autoridade raiz", emitida "1,2" para ANSI, que por sua vez...</span><span class="sxs-lookup"><span data-stu-id="eb523-163">ISO - the "root authority", issued "1.2" to ANSI, which in turn...</span></span>                           |
| <span data-ttu-id="eb523-164">2</span><span class="sxs-lookup"><span data-stu-id="eb523-164">2</span></span>      | <span data-ttu-id="eb523-165">ANSI... "1.2.840" foi emitido para os EUA, que por sua vez...</span><span class="sxs-lookup"><span data-stu-id="eb523-165">ANSI ...issued "1.2.840" to USA, which in turn...</span></span>                                            |
| <span data-ttu-id="eb523-166">840</span><span class="sxs-lookup"><span data-stu-id="eb523-166">840</span></span>    | <span data-ttu-id="eb523-167">EUA... "1.2.840.113556" foi emitido para a Microsoft...</span><span class="sxs-lookup"><span data-stu-id="eb523-167">USA ...issued "1.2.840.113556" to Microsoft...</span></span>                                               |
| <span data-ttu-id="eb523-168">113556</span><span class="sxs-lookup"><span data-stu-id="eb523-168">113556</span></span> | <span data-ttu-id="eb523-169">Microsoft... onde a Microsoft gerencia internamente várias ramificações de OID em "1.2.840.113556".</span><span class="sxs-lookup"><span data-stu-id="eb523-169">Microsoft ...where Microsoft internally manages several OID branches under "1.2.840.113556".</span></span> |
| <span data-ttu-id="eb523-170">1</span><span class="sxs-lookup"><span data-stu-id="eb523-170">1</span></span>      | <span data-ttu-id="eb523-171">Microsoft DS</span><span class="sxs-lookup"><span data-stu-id="eb523-171">Microsoft DS</span></span>                                                                                 |
| <span data-ttu-id="eb523-172">5</span><span class="sxs-lookup"><span data-stu-id="eb523-172">5</span></span>      | <span data-ttu-id="eb523-173">Classes NTDS</span><span class="sxs-lookup"><span data-stu-id="eb523-173">NTDS Classes</span></span>                                                                                 |
| <span data-ttu-id="eb523-174">4</span><span class="sxs-lookup"><span data-stu-id="eb523-174">4</span></span>      | <span data-ttu-id="eb523-175">Builtin-Domain</span><span class="sxs-lookup"><span data-stu-id="eb523-175">Builtin-Domain</span></span>                                                                               |



 

</dd> <dt>

<span data-ttu-id="eb523-176"><span id="OID"></span><span id="oid"></span>OIDs</span><span class="sxs-lookup"><span data-stu-id="eb523-176"><span id="OID"></span><span id="oid"></span>OID</span></span>
</dt> <dd>

<span data-ttu-id="eb523-177">Consulte *identificador de objeto*.</span><span class="sxs-lookup"><span data-stu-id="eb523-177">See *Object Identifier*.</span></span>

</dd> <dt>

<span data-ttu-id="eb523-178"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>Esquema</span><span class="sxs-lookup"><span data-stu-id="eb523-178"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>Schema</span></span>
</dt> <dd>

<span data-ttu-id="eb523-179">Uma definição formal do conteúdo e da estrutura do serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="eb523-179">A formal definition of the directory service contents and structure.</span></span> <span data-ttu-id="eb523-180">O esquema define todos os atributos e classes.</span><span class="sxs-lookup"><span data-stu-id="eb523-180">The schema defines all attributes and classes.</span></span> <span data-ttu-id="eb523-181">Para cada classe, os atributos [**poss-superior**](a-posssuperiors.md), [**deve-contém**](a-mustcontain.md)e [**pode-conter**](a-maycontain.md) são definidos.</span><span class="sxs-lookup"><span data-stu-id="eb523-181">For each class, the [**Poss-Superiors**](a-posssuperiors.md), [**Must-Contain**](a-mustcontain.md), and [**May-Contain**](a-maycontain.md) attributes are defined.</span></span> <span data-ttu-id="eb523-182">[**Poss-superior**](a-posssuperiors.md) define as estruturas de árvore possíveis para o serviço de diretório especificando quais classes podem ser pai para qualquer classe específica.</span><span class="sxs-lookup"><span data-stu-id="eb523-182">[**Poss-Superiors**](a-posssuperiors.md) defines the possible tree structures for the directory service by specifying what classes can be the parent for any given class.</span></span> <span data-ttu-id="eb523-183">[**Deve conter**](a-mustcontain.md) e [**pode incluir**](a-maycontain.md) a lista dos atributos de uma classe que deve estar presente para armazenar a classe e quais atributos adicionais podem, opcionalmente, estar presentes.</span><span class="sxs-lookup"><span data-stu-id="eb523-183">[**Must-Contain**](a-mustcontain.md) and [**May-Contain**](a-maycontain.md) list the attributes for a class that must be present to store the class and what additional attributes may optionally be present.</span></span>

</dd> <dt>

<span data-ttu-id="eb523-184"><span id="Security_Descriptor"></span><span id="security_descriptor"></span><span id="SECURITY_DESCRIPTOR"></span>Descritor de segurança</span><span class="sxs-lookup"><span data-stu-id="eb523-184"><span id="Security_Descriptor"></span><span id="security_descriptor"></span><span id="SECURITY_DESCRIPTOR"></span>Security Descriptor</span></span>
</dt> <dd>

<span data-ttu-id="eb523-185">Informações sobre a propriedade de um objeto e as permissões que outros usuários têm sobre esse objeto.</span><span class="sxs-lookup"><span data-stu-id="eb523-185">Information about the ownership of an object and the permissions that other users have on that object.</span></span> <span data-ttu-id="eb523-186">A propriedade [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md) de uma entrada de esquema contém uma cadeia de caracteres que representa o descritor de segurança do objeto.</span><span class="sxs-lookup"><span data-stu-id="eb523-186">The [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md) property of a schema entry contains a string that represents the security descriptor of the object.</span></span> <span data-ttu-id="eb523-187">Para obter mais informações sobre o formato das informações nesse campo, consulte [formato de cadeia de caracteres do descritor de segurança](/windows/desktop/SecAuthZ/security-descriptor-string-format).</span><span class="sxs-lookup"><span data-stu-id="eb523-187">For more information about the format of the information in this field, see [Security Descriptor String Format](/windows/desktop/SecAuthZ/security-descriptor-string-format).</span></span>

</dd> <dt>

<span data-ttu-id="eb523-188"><span id="Structure_Rules"></span><span id="structure_rules"></span><span id="STRUCTURE_RULES"></span>Regras de estrutura</span><span class="sxs-lookup"><span data-stu-id="eb523-188"><span id="Structure_Rules"></span><span id="structure_rules"></span><span id="STRUCTURE_RULES"></span>Structure Rules</span></span>
</dt> <dd>

<span data-ttu-id="eb523-189">A definição da estrutura de árvore ou estruturas possíveis.</span><span class="sxs-lookup"><span data-stu-id="eb523-189">The definition of the possible tree structure or structures.</span></span> <span data-ttu-id="eb523-190">No NTDS, as regras de estrutura são completamente expressas pelo atributo poss-superior presente em cada objeto [**de esquema de classe**](c-classschema.md) .</span><span class="sxs-lookup"><span data-stu-id="eb523-190">In the NTDS, the structure rules are completely expressed by the Poss-superiors attribute present on each [**Class-Schema**](c-classschema.md) object.</span></span> <span data-ttu-id="eb523-191">Consulte *esquema*.</span><span class="sxs-lookup"><span data-stu-id="eb523-191">See *Schema*.</span></span>

</dd> <dt>

<span data-ttu-id="eb523-192"><span id="Subclass"></span><span id="subclass"></span><span id="SUBCLASS"></span>Subclasse</span><span class="sxs-lookup"><span data-stu-id="eb523-192"><span id="Subclass"></span><span id="subclass"></span><span id="SUBCLASS"></span>Subclass</span></span>
</dt> <dd>

<span data-ttu-id="eb523-193">Um objeto de [**esquema de classe**](c-classschema.md) que herda de outro objeto de [**esquema de classe**](c-classschema.md) .</span><span class="sxs-lookup"><span data-stu-id="eb523-193">A [**Class-Schema**](c-classschema.md) object that inherits from another [**Class-Schema**](c-classschema.md) object.</span></span> <span data-ttu-id="eb523-194">Consulte *herança*.</span><span class="sxs-lookup"><span data-stu-id="eb523-194">See *Inheritance*.</span></span>

</dd> <dt>

<span data-ttu-id="eb523-195"><span id="Superclass"></span><span id="superclass"></span><span id="SUPERCLASS"></span>Super</span><span class="sxs-lookup"><span data-stu-id="eb523-195"><span id="Superclass"></span><span id="superclass"></span><span id="SUPERCLASS"></span>Superclass</span></span>
</dt> <dd>

<span data-ttu-id="eb523-196">Um objeto de [**esquema de classe**](c-classschema.md) do qual um ou mais objetos [**de esquema de classe**](c-classschema.md) herdam.</span><span class="sxs-lookup"><span data-stu-id="eb523-196">A [**Class-Schema**](c-classschema.md) object from which one or more other [**Class-Schema**](c-classschema.md) objects inherit.</span></span> <span data-ttu-id="eb523-197">Consulte *herança*.</span><span class="sxs-lookup"><span data-stu-id="eb523-197">See *Inheritance*.</span></span>

</dd> <dt>

<span data-ttu-id="eb523-198"><span id="Tree"></span><span id="tree"></span><span id="TREE"></span>Três</span><span class="sxs-lookup"><span data-stu-id="eb523-198"><span id="Tree"></span><span id="tree"></span><span id="TREE"></span>Tree</span></span>
</dt> <dd>

<span data-ttu-id="eb523-199">Consulte *árvore de informações do diretório*.</span><span class="sxs-lookup"><span data-stu-id="eb523-199">See *Directory Information Tree*.</span></span>

</dd> <dt>

<span data-ttu-id="eb523-200"><span id="X.500"></span><span id="x.500"></span>X. 500</span><span class="sxs-lookup"><span data-stu-id="eb523-200"><span id="X.500"></span><span id="x.500"></span>X.500</span></span>
</dt> <dd>

<span data-ttu-id="eb523-201">Uma família de padrões desenvolvida em conjunto pelo ISO e ITU, anteriormente conhecida como CCITT, que especificavam a nomenclatura, a representação de dados e os protocolos de comunicação para um serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="eb523-201">A family of standards developed jointly by the ISO and ITU, formerly known as the CCITT, that specify the naming, data representation, and communications protocols for a directory service.</span></span>

</dd> </dl>

 

 