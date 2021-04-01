---
title: Características das classes de objeto
description: Cada classe de objeto no Active Directory Domain Services é definida por um objeto classSchema no contêiner de esquema.
ms.assetid: 88a2b2a3-e8e2-4be1-9784-9709cbea08d6
ms.tgt_platform: multiple
keywords:
- Características do AD de classes de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00c7e750d53597d1532d48c3c463315f8a48bd6d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640432"
---
# <a name="characteristics-of-object-classes"></a>Características das classes de objeto

Cada classe de objeto no Active Directory Domain Services é definida por um objeto **classSchema** no contêiner de esquema. Os atributos de um objeto **classSchema** especificam as características da classe, como:

-   Identificadores de classe: as classes têm vários identificadores, incluindo **ldapDisplayName**, que são usados por clientes LDAP para identificar a classe em filtros de pesquisa e **schemaIDGUID**, que são usados em descritores de segurança para controlar o acesso à classe.
-   Atributos possíveis: uma definição de classe de objeto inclui listas dos atributos obrigatórios e opcionais que podem ser definidos em uma instância da classe.
-   Possíveis pais: cada instância de objeto, exceto a raiz da hierarquia de diretórios, tem exatamente um pai. Uma definição de classe de objeto inclui listas de possíveis pais, ou seja, das classes de objeto que podem conter uma instância da classe.
-   Superclasses e classes auxiliares: cada classe de objeto (exceto a [*parte superior*](/previous-versions/windows/desktop/legacy/ms681941(v=vs.85))) é derivada de outra classe. Uma classe herda possíveis atributos e possíveis pais das classes acima dela na hierarquia de classes. Uma classe também pode ter qualquer número de classes auxiliares da qual ela herda listas de possíveis atributos. Para obter mais informações, consulte [herança de classe no esquema de Active Directory](class-inheritance-in-the-active-directory-schema.md).

A tabela a seguir lista o **lDAPDisplayName** e a descrição dos principais atributos de um objeto **classSchema** . Para obter mais informações e uma lista completa dos atributos obrigatórios e opcionais de um objeto **classSchema** , consulte [**classSchema**](/windows/desktop/ADSchema/c-classschema).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>lDAPDisplayName</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>cn</strong></td>
<td>Cada objeto no Active Directory Domain Services tem um atributo de nomenclatura do qual seu nome distinto relativo (RDN) é formado. O atributo de nomenclatura para objetos <strong>classSchema</strong> é <strong>CN</strong> (Common-Name). O valor atribuído a <strong>CN</strong> é o valor que a classe de objeto terá como seu RDN. Por exemplo, o <strong>CN</strong> da classe de objeto <strong>OrganizationalUnit</strong> é Organization-Unit, que apareceria em um nome distinto como CN = Organization-Unit. O <strong>CN</strong> deve ser exclusivo no contêiner de esquema.</td>
</tr>
<tr class="even">
<td><strong>lDAPDisplayName</strong></td>
<td>O nome usado por clientes LDAP, como o provedor de LDAP ADSI, para se referir à classe, por exemplo, para especificar a classe em um filtro de pesquisa. O <strong>lDAPDisplayName</strong> de uma classe deve ser exclusivo no contêiner de esquema, o que significa que ele deve ser exclusivo em todos os objetos <strong>classSchema</strong> e <strong>attributeSchema</strong> . Para obter mais informações sobre como compor um <strong>CN</strong> e um <strong>lDAPDisplayName</strong> para uma nova classe, consulte <a href="naming-attributes-and-classes.md">nomenclatura de atributos e classes</a>.</td>
</tr>
<tr class="odd">
<td><strong>schemaIDGUID</strong></td>
<td>Um GUID armazenado como uma cadeia de caracteres de octeto. Esse GUID identifica exclusivamente a classe. Esse GUID pode ser usado em entradas de controle de acesso para controlar o acesso a objetos dessa classe. Para obter mais informações, consulte <a href="setting-permissions-on-child-object-operations.md">definindo permissões em operações de objeto filho</a>. Na criação do objeto <strong>classSchema</strong> , o servidor Active Directory gerará esse valor se ele não for especificado. Se você criar uma nova classe, gere seu próprio GUID para cada classe para que todas as instalações da extensão usem o mesmo <strong>schemaIDGUID</strong> para fazer referência à classe.<br/></td>
</tr>
<tr class="even">
<td><strong>adminDisplayName</strong></td>
<td>Um nome de exibição da classe para uso em ferramentas administrativas. Se <strong>adminDisplayName</strong> não for especificado quando uma classe for criada, o sistema usará o valor Common-Name como o nome de exibição. Esse nome de exibição será usado somente se um mapeamento não existir na propriedade <strong>classDisplayName</strong> do especificador de exibição para a classe. Para obter mais informações, consulte <a href="display-specifiers.md">especificadores de exibição</a> e <a href="class-and-attribute-display-names.md">nomes de exibição de classe e atributo</a>.<br/></td>
</tr>
<tr class="odd">
<td><strong>governsID</strong></td>
<td>O OID da classe. Esse valor deve ser exclusivo entre o <strong>governsIDs</strong> de todos os objetos <strong>ClassSchema</strong> e os <strong>attributeids</strong> de todos os objetos <strong>attributeSchema</strong> . Para obter mais informações, consulte <a href="object-identifiers.md">identificadores de objeto</a>.</td>
</tr>
<tr class="even">
<td><strong>rDnAttId</strong></td>
<td>Identifica o atributo de nomenclatura, que é o atributo que fornece o RDN para essa classe se for diferente do padrão (<strong>CN</strong>). O uso de um atributo de nomenclatura diferente de <strong>CN</strong> não é recomendado. Os atributos de nomenclatura devem ser extraídos do conjunto conhecido (OU, CN, O, L e DC) que são compreendidos por todos os clientes do LDAP versão 3. Para obter mais informações, consulte <a href="object-names-and-identities.md">nomes de objetos e identidades</a> e <a href="syntaxes-for-attributes-in-active-directory-domain-services.md">sintaxes para atributos em Active Directory Domain Services</a>. Um atributo de nomenclatura deve ter a sintaxe de cadeia de caracteres de diretório. Para obter mais informações, consulte <a href="syntaxes-for-attributes-in-active-directory-domain-services.md">sintaxes para atributos em Active Directory Domain Services</a>.<br/></td>
</tr>
<tr class="odd">
<td><strong>mustContain</strong>, <strong>systemMustContain</strong></td>
<td>Um par de propriedades com valores múltiplos que especificam os atributos que devem estar presentes em instâncias dessa classe. Esses são atributos obrigatórios que devem estar presentes durante a criação e não podem ser limpos após a criação. Após a criação da classe, essas propriedades não podem ser alteradas. O conjunto completo de atributos obrigatórios para uma classe é a União dos valores <strong>systemMustContain</strong> e <strong>mustContain</strong> nessa classe e todas as classes herdadas.<br/></td>
</tr>
<tr class="even">
<td><strong>mayContain</strong>, <strong>systemMayContain</strong></td>
<td>Um par de propriedades com valores múltiplos que especificam os atributos que podem estar presentes em instâncias dessa classe. Esses são atributos opcionais que não são obrigatórios e, portanto, podem ou não estar presentes em uma instância dessa classe. Você pode adicionar ou remover valores de <strong>mayContain</strong> de um objeto <strong>classSchema</strong> de categoria 1 ou categoria 2 existente. Antes de remover um valor de <strong>mayContain</strong> de um objeto <strong>classSchema</strong> , você deve pesquisar instâncias da classe Object e limpar quaisquer valores para o atributo que você está removendo. Após a criação da classe, a propriedade <strong>systemMayContain</strong> não pode ser alterada o conjunto completo de atributos opcionais para uma classe é a União dos valores <strong>systemMayContain</strong> e <strong>mayContain</strong> nessa classe e todas as classes herdadas.<br/></td>
</tr>
<tr class="odd">
<td><strong>possSuperior</strong>, <strong>systemPossSuperiors</strong></td>
<td>Um par de propriedades com valores múltiplos que especificam as classes estruturais que podem ser pais legais de instâncias dessa classe. O conjunto completo de superiores possíveis é a União dos valores <strong>systemPossSuperiors</strong> e <strong>possSuperior</strong> nessa classe e quaisquer classes estruturais ou abstratas herdadas. os valores <strong>systemPossSuperiors</strong> e <strong>possSuperior</strong> não são herdados de classes auxiliares. Você pode adicionar ou remover valores de <strong>possSuperior</strong> de um objeto <strong>classSchema</strong> de categoria 1 ou categoria 2 existente. Após a criação da classe, a propriedade <strong>systemPossSuperiors</strong> não pode ser alterada.<br/></td>
</tr>
<tr class="even">
<td><strong>objectClassCategory</strong></td>
<td>Um valor inteiro que especifica a categoria da classe, que pode ser uma das seguintes:
<ul>
<li>Estrutural, o que significa que ele pode ser instanciado no diretório.</li>
<li>Abstract, o que significa que a classe fornece uma definição básica de uma classe que pode ser usada para formar classes estruturais.</li>
<li>Auxiliar, o que significa que uma classe que pode ser usada para estender a definição de uma classe que herda dela, mas não pode ser usada para formar uma classe por si só.</li>
</ul>
Para obter mais informações, consulte <a href="structural-abstract-and-auxiliary-classes.md">classes estruturais, abstratas e auxiliares</a>.<br/></td>
</tr>
<tr class="odd">
<td><strong>subClassOf</strong></td>
<td>Um OID para a superclasse imediata dessa classe, ou seja, a classe da qual essa classe é derivada. Para classes estruturais, <strong>listas SubClassOf</strong> pode ser uma classe estrutural ou abstrata.<br/> Para classes abstratas, <strong>listas SubClassOf</strong> pode ser apenas uma classe abstrata.<br/> Para classes auxiliares, <strong>listas SubClassOf</strong> pode ser uma classe abstrata ou auxiliar.<br/> Se você definir uma nova classe, verifique se a classe <strong>listas SubClassOf</strong> existe ou se ela existirá quando a nova classe for gravada no diretório. Se a classe não existir, o objeto <strong>classSchema</strong> não será adicionado ao diretório.<br/></td>
</tr>
<tr class="even">
<td><strong>auxiliaryClass</strong>, <strong>systemAuxiliaryClass</strong></td>
<td>Um par de propriedades com valores múltiplos que especificam as classes auxiliares das quais essa classe herda. O conjunto completo de classes auxiliares é a União dos valores <strong>systemAuxiliaryClass</strong> e <strong>auxiliaryClass</strong> nessa classe e todas as classes herdadas. Para um objeto <strong>classSchema</strong> existente, os valores podem ser adicionados à propriedade <strong>auxiliaryClass</strong> , mas não removidos. Após a criação da classe, a propriedade <strong>systemAuxiliaryClass</strong> não pode ser alterada.<br/></td>
</tr>
<tr class="odd">
<td><strong>defaultObjectCategory</strong></td>
<td>O nome distinto dessa classe de objeto ou de uma de suas superclasses. Quando uma instância dessa classe de objeto é criada, o sistema define a propriedade <strong>objectCategory</strong> da nova instância para o valor especificado na propriedade <strong>defaultObjectCategory</strong> de sua classe de objeto. A propriedade <strong>objectCategory</strong> é uma propriedade indexada usada para aumentar a eficiência das pesquisas de classe de objeto. Se <strong>defaultObjectCategory</strong> não for especificado quando uma classe for criada, o sistema o definirá como o DN (nome distinto) do objeto <strong>classSchema</strong> para essa classe. Se esse objeto for consultado com frequência pelo valor de uma superclasse em vez da própria classe do objeto, você poderá definir <strong>defaultObjectCategory</strong> como o DN da superclasse. Por exemplo, se você estiver subclassendo uma classe predefinida (categoria 1), a prática recomendada é definir <strong>defaultObjectCategory</strong> como o mesmo valor da superclasse. Isso permite que a interface do usuário padrão &quot; localize &quot; sua subclasse.<br/> Para obter mais informações, consulte <a href="object-class-and-object-category.md">classe de objeto e categoria de objeto</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>defaultocultarvalue</strong></td>
<td>Um valor booliano que especifica a configuração padrão da propriedade <strong>showInAdvancedViewOnly</strong> de novas instâncias dessa classe. Muitos objetos de diretório não são interessantes para os usuários finais. Para evitar que esses objetos desorganizem a interface do usuário, cada objeto tem um atributo booleano chamado <strong>showInAdvancedViewOnly</strong>. Se <strong>Defaultocultarvalue</strong> for definido como <strong>true</strong>, novas instâncias de objeto ficarão ocultas nos snap-ins administrativos e no Shell do Windows. Um item de menu para a classe de objeto não será exibido no <strong>novo</strong> menu de contexto dos snap-ins administrativos, mesmo que as propriedades apropriadas do assistente de criação sejam definidas no objeto <strong>displaySpecifier</strong> da classe de objeto.<br/> Se <strong>Defaultocultarvalue</strong> for definido como <strong>false</strong>, novas instâncias do objeto serão exibidas nos snap-ins administrativos e no Shell do Windows. Defina essa propriedade como <strong>false</strong> para ver as instâncias da classe nos snap-ins administrativos e no Shell e habilitar um assistente de criação e seu item de menu no <strong>novo</strong> menu de snap-ins administrativos.<br/> Se o valor <strong>Defaultocultarvalue</strong> não estiver definido, o padrão será <strong>true</strong>.<br/></td>
</tr>
<tr class="odd">
<td><strong>systemFlags</strong></td>
<td>Um valor inteiro que contém sinalizadores que definem propriedades adicionais da classe. O bit 0x10 identifica uma classe Category 1 (uma classe que faz parte do esquema base que está incluído no sistema). Você não pode definir esse bit, o que significa que o bit não está definido nas classes Category 2 (que são extensões para o esquema).</td>
</tr>
<tr class="even">
<td><strong>systemOnly</strong></td>
<td>Um valor booliano que especifica se apenas o servidor Active Directory pode modificar a classe. As classes somente do sistema podem ser criadas ou excluídas somente pelo DSA (agente do sistema de diretório). As classes somente de sistema são aquelas das quais o sistema depende para operações normais.</td>
</tr>
<tr class="odd">
<td><strong>defaultSecurityDescriptor</strong></td>
<td>Especifica o descritor de segurança padrão para novos objetos desta classe. Para obter mais informações, consulte <a href="default-security-descriptor.md">descritor de segurança padrão</a> e <a href="how-security-descriptors-are-set-on-new-directory-objects.md">como os descritores de segurança são definidos em novos objetos de diretório</a>.</td>
</tr>
<tr class="even">
<td><strong>isDefunct</strong></td>
<td>Um valor booliano que indica se a classe expirou. Para obter mais informações, consulte <a href="disabling-existing-classes-and-attributes.md">desabilitando classes e atributos existentes</a>.</td>
</tr>
<tr class="odd">
<td><strong>descrição</strong></td>
<td>Uma descrição de texto da classe para uso por aplicativos administrativos.</td>
</tr>
<tr class="even">
<td><strong>objectClass</strong></td>
<td>Identifica a classe de objeto da qual esse objeto é uma instância, que é a classe de objeto <strong>classSchema</strong> para todas as definições de classe e a classe de objeto <strong>attributeSchema</strong> para todas as definições de atributo.</td>
</tr>
</tbody>
</table>



 

 

