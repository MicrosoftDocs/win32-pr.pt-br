---
title: Terminologia de esquema do Active Directory
description: Os termos a seguir geralmente são usados para se referir ao esquema do Active Directory.
ms.assetid: 22c5756f-d663-4cb7-aab0-956b22a01e9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b48256d1df8f9c344fe0acceb2fb6a70ed3033260baea4db7df44dd71e1c3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117836432"
---
# <a name="active-directory-schema-terminology"></a>Terminologia de esquema do Active Directory

Os termos a seguir geralmente são usados para se referir ao esquema do Active Directory.


<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Atributo
</dt> <dd>

Itens de dados usados para descrever os objetos representados pelas classes definidas no esquema. Os atributos são definidos no esquema separadamente das classes ; isso permite que uma única definição de atributo seja aplicada a muitas classes. Por exemplo, [**Description**](a-description.md) é um atributo que pode ser aplicado a qualquer classe no esquema. O **atributo Description** é definido uma vez no esquema, garantindo a  consistência, em vez de ter uma definição diferente para Descrição de um usuário e Descrição **de** uma impressora.

> [!Note]  
> O termo *propriedade* é frequentemente usado de forma intercambiável com o atributo de *termo*.

 

</dd> <dt>

<span id="Attribute_Instance"></span><span id="attribute_instance"></span><span id="ATTRIBUTE_INSTANCE"></span>Instância de atributo
</dt> <dd>

Uma ocorrência de um atributo definido no esquema. Esse termo é usado para distinguir entre a definição de um atributo e uma ocorrência discreta do atributo. Por exemplo, armazenar um objeto User para "Jeff Smith" com o atributo [**Common-Name**](a-cn.md) definido como "Jeff Smith" cria uma instância [**de Common-Name**](a-cn.md).

</dd> <dt>

<span id="Class"></span><span id="class"></span><span id="CLASS"></span>Classe
</dt> <dd>

Uma descrição formal de um tipo discreto e identificável de objeto armazenado no serviço de diretório. Por exemplo, [**User**](c-user.md), [**Print-Queue**](c-printqueue.md)e [**Group são**](c-group.md) todas classes. Além disso, há três categorias distintas de classes: Classes [Estruturais,](classes-structural.md) [Classes](classes-abstract.md)Abstratas e [Classes Auxiliares](classes-auxiliary.md).

</dd> <dt>

<span id="Class_Instance"></span><span id="class_instance"></span><span id="CLASS_INSTANCE"></span>Instância de classe
</dt> <dd>

Uma ocorrência de uma classe definida no esquema. Esse termo é usado para distinguir entre a definição de uma classe e uma ocorrência discreta da classe . Por exemplo, armazenar um objeto [**User**](c-user.md) para "Jeff Smith" no serviço de diretório cria uma instância do [**Usuário**](c-user.md).

</dd> <dt>

<span id="Content_Rules"></span><span id="content_rules"></span><span id="CONTENT_RULES"></span>Regras de conteúdo
</dt> <dd>

A definição do conteúdo possível das instâncias de classe que são armazenadas no serviço de diretório. No NTDS (NT Directory Services), no qual o Active Directory se baseia, as regras de conteúdo são completamente expressas pelos atributos [**Must-Contain**](a-mustcontain.md) e [**May-Contain**](a-maycontain.md) das definições de esquema para cada classe.

</dd> <dt>

<span id="Derivation"></span><span id="derivation"></span><span id="DERIVATION"></span>Derivação
</dt> <dd>

Consulte *Herança*.

</dd> <dt>

<span id="Directory_Information_Tree"></span><span id="directory_information_tree"></span><span id="DIRECTORY_INFORMATION_TREE"></span>Árvore de informações do diretório
</dt> <dd>

O próprio diretório, representado como uma estrutura de árvore na qual os vértices são as entradas de diretório (instâncias de classe) e as linhas de conexão das relações pai-filho entre as entradas.

</dd> <dt>

<span id="DIT"></span><span id="dit"></span>Dit
</dt> <dd>

Consulte *Árvore de Informações do Diretório*.

</dd> <dt>

<span id="Control_Access_Rights"></span><span id="control_access_rights"></span><span id="CONTROL_ACCESS_RIGHTS"></span>Controlar direitos de acesso
</dt> <dd>

Uma classe que descreve um direito de acesso não vinculado a um recurso, mas a uma ação. Por exemplo, um usuário pode ter o direito de criar valores de ID relativos.

</dd> <dt>

<span id="Inheritance"></span><span id="inheritance"></span><span id="INHERITANCE"></span>Herança
</dt> <dd>

A capacidade de criar novas classes de objeto de classes de objeto existentes. O novo objeto é definido como uma *subclasse* do objeto pai. O objeto pai se torna *uma superclasse* do novo objeto. Uma subclasse herda os atributos do pai, incluindo regras de estrutura e regras de conteúdo.

</dd> <dt>

<span id="LDAP"></span><span id="ldap"></span>Ldap
</dt> <dd>

Consulte *Lightweight Directory Access Protocol*.

</dd> <dt>

<span id="Lightweight_Directory_Access_Protocol"></span><span id="lightweight_directory_access_protocol"></span><span id="LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL"></span>Lightweight Directory Access Protocol
</dt> <dd>

Um protocolo de comunicação padrão da Internet usado para se comunicar com o NTDS. Há suporte para lDAP versão 2 e 3.

</dd> <dt>

<span id="NT_Security_Descriptor"></span><span id="nt_security_descriptor"></span><span id="NT_SECURITY_DESCRIPTOR"></span>Descritor de segurança NT
</dt> <dd>

Consulte *Descritor de segurança*.

</dd> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>Objeto
</dt> <dd>

Uma unidade de armazenamento de dados no serviço de diretório. Os objetos de serviço de diretório não devem ser confundidos com objetos COM ou outros objetos do sistema orientados a objeto, que têm um componente executável e um comportamento de tempo de execução. Os objetos de serviço de diretório consistem apenas em dados. Um objeto de serviço de diretório é definido por um objeto [**Class-Schema**](c-classschema.md) e um grupo de objetos [**Attribute-Schema**](c-attributeschema.md) referenciados pelo [**objeto Class-Schema.**](c-classschema.md)

[**Os objetos Class-Schema**](c-classschema.md) [**e Attribute-Schema**](c-attributeschema.md) são os próprios objetos de serviço de diretório e têm definições no esquema como qualquer outro objeto. Consulte *Classe*.

</dd> <dt>

<span id="Object_Identifier"></span><span id="object_identifier"></span><span id="OBJECT_IDENTIFIER"></span>Identificador de Objeto
</dt> <dd>

Valores numéricos exclusivos, emitidos por várias autoridades emissoras, para identificar exclusivamente elementos de dados, sintaxes e várias outras partes de aplicativos distribuídos. Os OIDs (Identificadores de Objeto) são encontrados em aplicativos OSI, Diretórios X.500, SNMP e outros aplicativos em que a exclusividade é importante. Os OIDs se baseiam em uma estrutura de árvore, na qual uma autoridade de emissão superior, como o ISO, aloca um branch da árvore a uma sub-autoridade, que, por sua vez, pode alocar sub-branches.

Os OIDs no NTDS incluem alguns emitidos pelo ISO para classes e atributos X.500 e alguns emitidos pela Microsoft. A notação OID é uma cadeia de caracteres pontilhada de números, por exemplo "1.2.840.113556.1.5.4", que se traduz conforme listado na lista a seguir. 

| Valor  | Descrição                                                                                  |
|--------|----------------------------------------------------------------------------------------------|
| 1      | ISO – a "autoridade raiz", emitida "1.2" para ANSI, que por sua vez...                           |
| 2      | Ansi... emitiu "1.2.840" para os EUA, que, por sua vez...                                            |
| 840    | Eua... emitiu "1.2.840.113556" para a Microsoft...                                               |
| 113556 | Microsoft... em que a Microsoft gerencia internamente vários branches OID em "1.2.840.113556". |
| 1      | Microsoft DS                                                                                 |
| 5      | NTDS Classes                                                                                 |
| 4      | Builtin-Domain                                                                               |



 

</dd> <dt>

<span id="OID"></span><span id="oid"></span>Oid
</dt> <dd>

Consulte *Identificador de Objeto*.

</dd> <dt>

<span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>Esquema
</dt> <dd>

Uma definição formal do conteúdo e da estrutura do serviço de diretório. O esquema define todos os atributos e classes. Para cada classe, os [**atributos Poss-Superiors**](a-posssuperiors.md), [**Must-Contain**](a-mustcontain.md)e [**May-Contain**](a-maycontain.md) são definidos. [**Poss-Superiors**](a-posssuperiors.md) define as possíveis estruturas de árvore para o serviço de diretório especificando quais classes podem ser o pai de qualquer classe especificada. [**Must-Contain**](a-mustcontain.md) e [**May-Contain**](a-maycontain.md) listam os atributos de uma classe que deve estar presente para armazenar a classe e quais atributos adicionais podem estar presentes opcionalmente.

</dd> <dt>

<span id="Security_Descriptor"></span><span id="security_descriptor"></span><span id="SECURITY_DESCRIPTOR"></span>Descritor de segurança
</dt> <dd>

Informações sobre a propriedade de um objeto e as permissões que outros usuários têm nesse objeto. A [**propriedade NT-Security-Descriptor de**](a-ntsecuritydescriptor.md) uma entrada de esquema contém uma cadeia de caracteres que representa o descritor de segurança do objeto . Para obter mais informações sobre o formato das informações neste campo, consulte Formato de cadeia [de caracteres do descritor de segurança](/windows/desktop/SecAuthZ/security-descriptor-string-format).

</dd> <dt>

<span id="Structure_Rules"></span><span id="structure_rules"></span><span id="STRUCTURE_RULES"></span>Regras de estrutura
</dt> <dd>

A definição da estrutura ou estrutura de árvore possível. No NTDS, as regras de estrutura são completamente expressas pelo atributo Poss-superiors presente em cada [**objeto Class-Schema.**](c-classschema.md) Consulte *Esquema*.

</dd> <dt>

<span id="Subclass"></span><span id="subclass"></span><span id="SUBCLASS"></span>Subclasse
</dt> <dd>

Um [**objeto Class-Schema**](c-classschema.md) que herda de outro [**objeto Class-Schema.**](c-classschema.md) Consulte *Herança*.

</dd> <dt>

<span id="Superclass"></span><span id="superclass"></span><span id="SUPERCLASS"></span>Superclasse
</dt> <dd>

Um [**objeto Class-Schema**](c-classschema.md) do qual um ou mais outros [**objetos Class-Schema**](c-classschema.md) herdam. Consulte *Herança*.

</dd> <dt>

<span id="Tree"></span><span id="tree"></span><span id="TREE"></span>Árvore
</dt> <dd>

Consulte *Árvore de Informações do Diretório*.

</dd> <dt>

<span id="X.500"></span><span id="x.500"></span>X.500
</dt> <dd>

Uma família de padrões desenvolvida em conjunto pelo ISO e ITU, anteriormente conhecida como CCITT, que especificavam a nomenclatura, a representação de dados e os protocolos de comunicação para um serviço de diretório.

</dd> </dl>

 

 