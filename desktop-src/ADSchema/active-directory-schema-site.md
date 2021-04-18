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
# <a name="active-directory-schema-terminology"></a>Terminologia de esquema de Active Directory

Os termos a seguir são comumente usados para se referir ao esquema de Active Directory.


<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute
</dt> <dd>

Itens de dados usados para descrever os objetos que são representados pelas classes que são definidas no esquema. Os atributos são definidos no esquema separadamente das classes; Isso permite que uma única definição de atributo seja aplicada a várias classes. Por exemplo, [**Descrição**](a-description.md) é um atributo que pode ser aplicado a qualquer classe no esquema. O atributo de **Descrição** é definido uma vez no esquema, garantindo a consistência, em vez de ter uma definição diferente para a **Descrição** de um usuário e uma **Descrição** de uma impressora.

> [!Note]  
> A *Propriedade* Term é frequentemente usada de forma intercambiável com o *atributo* Term.

 

</dd> <dt>

<span id="Attribute_Instance"></span><span id="attribute_instance"></span><span id="ATTRIBUTE_INSTANCE"></span>Instância de atributo
</dt> <dd>

Uma ocorrência de um atributo que é definido no esquema. Esse termo é usado para distinguir entre a definição de um atributo e uma ocorrência discreta do atributo. Por exemplo, armazenar um objeto de usuário para "Jeff Smith" com o atributo de [**nome comum**](a-cn.md) definido como "Jeff Smith" cria uma instância de [**nome comum**](a-cn.md).

</dd> <dt>

<span id="Class"></span><span id="class"></span><span id="CLASS"></span>Classes
</dt> <dd>

Uma descrição formal de um tipo discreto e identificável de objeto armazenado no serviço de diretório. Por exemplo, [**usuário**](c-user.md), [**fila de impressão**](c-printqueue.md)e [**grupo**](c-group.md) são todas as classes. Além disso, há 3 categorias distintas de classes: [classes estruturais](classes-structural.md), [classes abstratas](classes-abstract.md)e [classes auxiliares](classes-auxiliary.md).

</dd> <dt>

<span id="Class_Instance"></span><span id="class_instance"></span><span id="CLASS_INSTANCE"></span>Instância de classe
</dt> <dd>

Uma ocorrência de uma classe que é definida no esquema. Esse termo é usado para distinguir entre a definição de uma classe e uma ocorrência discreta da classe. Por exemplo, o armazenamento de um objeto de [**usuário**](c-user.md) para "Jeff Smith" no serviço de diretório cria uma instância de [**usuário**](c-user.md).

</dd> <dt>

<span id="Content_Rules"></span><span id="content_rules"></span><span id="CONTENT_RULES"></span>Regras de conteúdo
</dt> <dd>

A definição do conteúdo possível das instâncias de classe que são armazenadas no serviço de diretório. Nos serviços de diretório do NT (NTDS), no qual Active Directory é baseado, as regras de conteúdo são completamente expressas pelos atributos [**deve conter**](a-mustcontain.md) e [**pode conter**](a-maycontain.md) de definições de esquema para cada classe.

</dd> <dt>

<span id="Derivation"></span><span id="derivation"></span><span id="DERIVATION"></span>Derivação
</dt> <dd>

Consulte *herança*.

</dd> <dt>

<span id="Directory_Information_Tree"></span><span id="directory_information_tree"></span><span id="DIRECTORY_INFORMATION_TREE"></span>Árvore de informações do diretório
</dt> <dd>

O próprio diretório, representado como uma estrutura de árvore na qual os vértices são as entradas de diretório (instâncias de classe) e as linhas de conexão as relações pai-filho entre as entradas.

</dd> <dt>

<span id="DIT"></span><span id="dit"></span>DITA
</dt> <dd>

Consulte *árvore de informações do diretório*.

</dd> <dt>

<span id="Control_Access_Rights"></span><span id="control_access_rights"></span><span id="CONTROL_ACCESS_RIGHTS"></span>Controlar direitos de acesso
</dt> <dd>

Uma classe que descreve um direito de acesso não vinculado a um recurso, mas uma ação. Por exemplo, um usuário pode receber o direito de criar valores de ID relativos.

</dd> <dt>

<span id="Inheritance"></span><span id="inheritance"></span><span id="INHERITANCE"></span>Herda
</dt> <dd>

A capacidade de criar novas classes de objeto a partir de classes de objeto existentes. O novo objeto é definido como uma *subclasse* do objeto pai. O objeto pai se torna uma *superclasse* do novo objeto. Uma subclasse herda os atributos do pai, incluindo regras de estrutura e regras de conteúdo.

</dd> <dt>

<span id="LDAP"></span><span id="ldap"></span>LDAP
</dt> <dd>

Consulte *Lightweight Directory Access Protocol*.

</dd> <dt>

<span id="Lightweight_Directory_Access_Protocol"></span><span id="lightweight_directory_access_protocol"></span><span id="LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL"></span>Protocolo Lightweight Directory Access
</dt> <dd>

Um protocolo de comunicações padrão da Internet usado para se comunicar com o NTDS. Há suporte para LDAP versão 2 e versão 3.

</dd> <dt>

<span id="NT_Security_Descriptor"></span><span id="nt_security_descriptor"></span><span id="NT_SECURITY_DESCRIPTOR"></span>Descritor de segurança NT
</dt> <dd>

Consulte *descritor de segurança*.

</dd> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>Objeto
</dt> <dd>

Uma unidade de armazenamento de dados no serviço de diretório. Os objetos de serviço de diretório não devem ser confundidos com objetos COM ou outros objetos do sistema orientados a objeto, que têm um componente executável e um comportamento de tempo de execução. Os objetos de serviço de diretório consistem apenas em dados. Um objeto de serviço de diretório é definido por um objeto de [**esquema de classe**](c-classschema.md) e um grupo de objetos de [**esquema de atributo**](c-attributeschema.md) referenciados pelo objeto de esquema de [**classe**](c-classschema.md) .

Objetos de esquema e [**atributo de**](c-attributeschema.md) [**classe**](c-classschema.md) são objetos de serviço de diretório próprios, e têm definições no esquema como quaisquer outros objetos. Consulte *classe*.

</dd> <dt>

<span id="Object_Identifier"></span><span id="object_identifier"></span><span id="OBJECT_IDENTIFIER"></span>Identificador de objeto
</dt> <dd>

Valores numéricos exclusivos, emitidos por várias autoridades emissores, para identificar exclusivamente elementos de dados, sintaxes e várias outras partes de aplicativos distribuídos. Os identificadores de objeto (OIDs) são encontrados em aplicativos OSI, diretórios X. 500, SNMP e outros aplicativos onde a exclusividade é importante. Os OIDs se baseiam em uma estrutura de árvore, na qual uma autoridade emissora superior, como o ISO, aloca uma ramificação da árvore para uma subautoridade, que, por sua vez, pode alocar subramificações.

Os OIDs no NTDS incluem alguns emitidos pelo ISO para classes e atributos X. 500 e alguns emitidos pela Microsoft. A notação OID é uma cadeia de números pontilhada, por exemplo, "1.2.840.113556.1.5.4", que se traduz como listado na lista a seguir. 

| Valor  | Descrição                                                                                  |
|--------|----------------------------------------------------------------------------------------------|
| 1      | ISO-a "autoridade raiz", emitida "1,2" para ANSI, que por sua vez...                           |
| 2      | ANSI... "1.2.840" foi emitido para os EUA, que por sua vez...                                            |
| 840    | EUA... "1.2.840.113556" foi emitido para a Microsoft...                                               |
| 113556 | Microsoft... onde a Microsoft gerencia internamente várias ramificações de OID em "1.2.840.113556". |
| 1      | Microsoft DS                                                                                 |
| 5      | Classes NTDS                                                                                 |
| 4      | Builtin-Domain                                                                               |



 

</dd> <dt>

<span id="OID"></span><span id="oid"></span>OIDs
</dt> <dd>

Consulte *identificador de objeto*.

</dd> <dt>

<span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>Esquema
</dt> <dd>

Uma definição formal do conteúdo e da estrutura do serviço de diretório. O esquema define todos os atributos e classes. Para cada classe, os atributos [**poss-superior**](a-posssuperiors.md), [**deve-contém**](a-mustcontain.md)e [**pode-conter**](a-maycontain.md) são definidos. [**Poss-superior**](a-posssuperiors.md) define as estruturas de árvore possíveis para o serviço de diretório especificando quais classes podem ser pai para qualquer classe específica. [**Deve conter**](a-mustcontain.md) e [**pode incluir**](a-maycontain.md) a lista dos atributos de uma classe que deve estar presente para armazenar a classe e quais atributos adicionais podem, opcionalmente, estar presentes.

</dd> <dt>

<span id="Security_Descriptor"></span><span id="security_descriptor"></span><span id="SECURITY_DESCRIPTOR"></span>Descritor de segurança
</dt> <dd>

Informações sobre a propriedade de um objeto e as permissões que outros usuários têm sobre esse objeto. A propriedade [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md) de uma entrada de esquema contém uma cadeia de caracteres que representa o descritor de segurança do objeto. Para obter mais informações sobre o formato das informações nesse campo, consulte [formato de cadeia de caracteres do descritor de segurança](/windows/desktop/SecAuthZ/security-descriptor-string-format).

</dd> <dt>

<span id="Structure_Rules"></span><span id="structure_rules"></span><span id="STRUCTURE_RULES"></span>Regras de estrutura
</dt> <dd>

A definição da estrutura de árvore ou estruturas possíveis. No NTDS, as regras de estrutura são completamente expressas pelo atributo poss-superior presente em cada objeto [**de esquema de classe**](c-classschema.md) . Consulte *esquema*.

</dd> <dt>

<span id="Subclass"></span><span id="subclass"></span><span id="SUBCLASS"></span>Subclasse
</dt> <dd>

Um objeto de [**esquema de classe**](c-classschema.md) que herda de outro objeto de [**esquema de classe**](c-classschema.md) . Consulte *herança*.

</dd> <dt>

<span id="Superclass"></span><span id="superclass"></span><span id="SUPERCLASS"></span>Super
</dt> <dd>

Um objeto de [**esquema de classe**](c-classschema.md) do qual um ou mais objetos [**de esquema de classe**](c-classschema.md) herdam. Consulte *herança*.

</dd> <dt>

<span id="Tree"></span><span id="tree"></span><span id="TREE"></span>Três
</dt> <dd>

Consulte *árvore de informações do diretório*.

</dd> <dt>

<span id="X.500"></span><span id="x.500"></span>X. 500
</dt> <dd>

Uma família de padrões desenvolvida em conjunto pelo ISO e ITU, anteriormente conhecida como CCITT, que especificavam a nomenclatura, a representação de dados e os protocolos de comunicação para um serviço de diretório.

</dd> </dl>

 

 