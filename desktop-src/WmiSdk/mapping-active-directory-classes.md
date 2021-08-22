---
description: Fornece regras para mapear classes WMI para o Active Directory.
ms.assetid: 295d3233-5729-4eb0-9fa3-1cf64fef2909
ms.tgt_platform: multiple
title: Mapeando classes do Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc38e91d52b59a206a0b64465d0f9710f6d515c9487853824477b7f4f6a126aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992896"
---
# <a name="mapping-active-directory-classes"></a>Mapeando classes do Active Directory

Como o Active Directory tem uma ampla variedade de objetos possíveis, o WMI não pode criar um mapeamento direto de um para um. Em vez disso, o provedor de Serviços de Diretório usa regras para mapear classes entre as duas tecnologias.

As seções a seguir são discutidas neste tópico:

-   [Classes de mapeamento](#mapping-classes)
-   [Atributos de mapeamento](#mapping-attributes)
-   [Classes de associação](#association-classes)

> [!Note]  
> Para obter mais informações sobre o suporte e a instalação desse componente em um sistema operacional específico, consulte Disponibilidade do sistema operacional [de componentes WMI](operating-system-availability-of-wmi-components.md).

 

## <a name="mapping-classes"></a>Classes de mapeamento

A lista a seguir descreve as diretrizes que o provedor de Serviços de Diretório usa para mapear classes do Active Directory para classes WMI:

-   Cada classe abstrata no esquema do Active Directory é mapeado para uma classe abstrata no esquema WMI.

    No esquema WMI, cada classe abstrata é prefixada com DS \_ . Por exemplo, a **classe person** do esquema do Active Directory é mapeado para a **classe WMI de \_ pessoa DS.**

-   Cada classe nãoabstrata do esquema do Active Directory é mapeado para as duas classes a seguir no esquema WMI:

    -   A primeira classe mapeada é prefixada com \_ ADS. Essas são classes abstratas, mapeadas de acordo com as regras abaixo.
    -   A segunda classe mapeada é uma classe nãoabstrata com o prefixo de \_ nome DS. Essa classe é derivada da classe \_ abstrata ADS, com a adição do [**qualificador provider.**](/windows/desktop/api/Provider/nl-provider-provider)

    Por exemplo, a **classe de** usuário do esquema do Active Directory é mapeado para duas classes. A primeira classe é a classe **\_ abstrata de** usuário ADS, mapeada de acordo com as regras abaixo. A segunda classe é a classe nãoabstrata de usuário **DS. \_** Ele é derivado do usuário **ads \_ e** tem o qualificador [**de**](/windows/desktop/api/Provider/nl-provider-provider) Provedor adicionado.

-   A menos que especificado de outra forma, o nome de uma classe mapeada é o valor emaranhado da propriedade **LDAP-Display-Name** na classe do Active Directory.
-   Se a **propriedade Sub-Class-Of** estiver presente na classe active directory, a classe mapeada por WMI será derivada da classe especificada.

    Se a **propriedade Sub-Class-Of** não estiver presente, a classe mapeada por WMI será derivada da classe **raiz \_ LDAP \_ \_ DS,** conforme especificado no arquivo MOF.

    > [!Note]  
    > Essa classe tem a **propriedade de chave ADSIPath,** com um **tipo VT \_ BSTR**. Esse é o caminho ADSI exclusivo que identifica essa instância. O Active Directory dá suporte apenas à herança única, portanto, isso funciona.

     

-   Um **qualificador** dinâmico do tipo **\_ BOOL VT** e flavor definido como `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` **TRUE** é criado para cada classe. Esse é um qualificador WMI padrão que indica que as instâncias dessa classe são fornecidas dinamicamente.
-   Se [**a**](/windows/desktop/api/Provider/nl-provider-provider) classe não for abstrata, o provedor criará um qualificador de Provedor do tipo **\_ BOOL VT BSTR** e tipo de qualificador definido como `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` "Provedor de Instância DS" para cada classe. Esse é um qualificador WMI padrão que indica o nome do provedor fornecendo dinamicamente instâncias dessa classe.

O restante das propriedades ADSI é mapeada para qualificadores de classe e propriedades de acordo com as tabelas a seguir. Todos os qualificadores são mapeadores com um valor de sinalizador qualificador de `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` .

A seguir, são listadas informações de mapeamento para a classe do Active Directory, mostrando o qualificador WMI e o tipo de qualificador WMI para cada propriedade do Active Directory.

<dl> <dt>

**Common-Name**
</dt> <dd>

**CN** (**VT \_ BSTR**)

Mapeado diretamente do valor da cadeia de caracteres.

</dd> <dt>

**Default-Object-Category**
</dt> <dd>

**DefaultObjectCategory** (**VT \_ BSTR**)

Mapeado diretamente do valor da cadeia de caracteres.

</dd> <dt>

**Descritor de segurança padrão**
</dt> <dd>

**DefaultSecurityDescriptor** (**VT \_ BSTR**)

Mapeado diretamente do valor da cadeia de caracteres.

</dd> <dt>

**Governs-Id**
</dt> <dd>

**GovernsId** (**VT \_ BSTR**)

Mapeado da representação de cadeia de caracteres do OID; por exemplo, "{ 1 3 3 6 }".

</dd> <dt>

**Classe de objeto**
</dt> <dd>

N/D

Não mapeado.

</dd> <dt>

**Object-Class-Category**
</dt> <dd>

**ObjectClassCategory** (**VT \_ I4**)

Mapeado diretamente do valor inteiro. Além disso, se o valor for Abstract(2), o qualificador CIM **\_ BOOL** da VT padrão, chamado de **qualificador** "Abstrato", também será criado.

</dd> <dt>

**RDN-ATT-ID**
</dt> <dd>

**RDNATTID** (**VT \_ BSTR**)

Mapeado da representação de cadeia de caracteres do valor OID; por exemplo, "{ 1 3 3 6 }". Além disso, a propriedade identificada aqui é anotada com o qualificador CIM **indexado** padrão definido como **TRUE.**

</dd> <dt>

**Somente sistema**
</dt> <dd>

**SystemOnly** (**VT \_ BOOL**)

Mapeado diretamente do valor booliana.

</dd> </dl>

 

O exemplo a seguir lista as propriedades de classe do Active Directory mapeadas para propriedades da classe WMI.

<dl> <dt>

**May-Contain**
</dt> <dd>

Cada propriedade nessa lista é mapeada para uma propriedade WMI.

</dd> <dt>

**Must-Contain**
</dt> <dd>

Cada propriedade nessa lista é mapeada para uma propriedade WMI. O **qualificador \_** cim não nulo padrão é criado para cada um deles.

</dd> <dt>

**System-May-Contain**
</dt> <dd>

Cada propriedade nessa lista é mapeada para uma propriedade WMI. Além disso, cada propriedade é anotada com um **qualificador System,** definido como **TRUE.**

</dd> <dt>

**System-Must-Contain**
</dt> <dd>

Cada propriedade nessa lista é mapeada para uma propriedade WMI. O **qualificador \_** cim não nulo padrão é criado para cada um deles. Além disso, cada propriedade é anotada com um **qualificador System,** definido como **TRUE.**

</dd> </dl>

## <a name="mapping-attributes"></a>Atributos de mapeamento

O provedor de Serviços de Diretório mapeia cada atributo de uma classe do Active Directory para exatamente uma propriedade da classe WMI correspondente de acordo com as regras nesta seção. Em geral, o Provedor de Serviços de Diretório nomeia a propriedade WMI como a versão emaranhada do valor **LDAP-Display-Name** do atributo do Active Directory.

Se a propriedade **Is-Single-Valued** do Active Directory for **FALSE,** essa propriedade WMI será combinada com o operador OR com **CIM FLAG \_ \_ ARRAY**. Observe que cada propriedade é marcada com o qualificador **\_ BSTR VT,** **ADSyntax**. Ele representa a sintaxe subjacente do Active Directory.

A tabela a seguir lista o mapeamento da sintaxe do Active Directory para o tipo de dados da propriedade WMI.



| Elemento Active Directory                                      | Tipo de dados WMI                                                           |
|---------------------------------------------------------------|-------------------------------------------------------------------------|
| [**Ponto de acesso**](/windows/desktop/ADSchema/s-object-access-point)            | **CADEIA DE \_ CARACTERES CIM**                                                         |
| [**Boolean**](/windows/desktop/ADSchema/s-boolean)                             | **CIM \_ BOOLEAN**                                                        |
| **Cadeia de caracteres sem maiúsculas e minúsculas**                                   | **CADEIA DE \_ CARACTERES CIM**                                                         |
| [**Cadeia de caracteres que pode ser sensível a minúsculas**](/windows/desktop/ADSchema/s-string-case-sensitive) | **CADEIA DE \_ CARACTERES CIM**                                                         |
| [**Nome diferenciado**](/windows/desktop/ADSchema/s-object-ds-dn)             | **CADEIA DE \_ CARACTERES CIM**                                                         |
| [**DN-Binary**](/windows/desktop/ADSchema/s-object-dn-binary)                  | Objeto inserido da classe **DN \_ Com Binário \_ definido** abaixo.<br/> |
| [**Cadeia de caracteres DN**](/windows/desktop/ADSchema/s-object-dn-string)                  | Objeto inserido da classe **DN \_ Com Cadeia de \_ Caracteres** definida abaixo.<br/> |
| [**Enumeração**](/windows/desktop/ADSchema/s-enumeration)                     | **\_Sint32 CIM**                                                         |
| [**Enumeração**](/windows/desktop/ADSchema/s-enumeration)                     | **\_cadeia de caracteres CIM**                                                         |
| [**Integer**](/windows/desktop/ADSchema/s-integer)                             | **\_Sint32 CIM**                                                         |
| [**LargeInteger**](/windows/desktop/ADSchema/s-largeinteger)                   | **\_cadeia de caracteres CIM**                                                         |
| Descritor de Segurança                                           | Objeto inserido da classe **Uint8Array** definido abaixo.<br/>       |
| Cadeia de caracteres numérica                                                | **\_cadeia de caracteres CIM**                                                         |
| ID de objeto                                                     | **\_cadeia de caracteres CIM**                                                         |
| Cadeia de caracteres de octeto                                                  | Objeto inserido da classe **Uint8Array** definido abaixo.<br/>       |
| OU nome                                                       | **\_cadeia de caracteres CIM**                                                         |
| Presentation-Address                                          | Objeto inserido da classe **Uint8Array** definido abaixo.<br/>       |
| Imprimir cadeia de caracteres de caso                                             | **\_cadeia de caracteres CIM**                                                         |
| Link de réplica                                                  | Objeto inserido da classe **Uint8Array** definido abaixo.<br/>       |
| [**Cadeia de caracteres (SID)**](/windows/desktop/ADSchema/s-string-sid)                      | Objeto inserido da classe **Uint8Array** definido abaixo.<br/>       |
| Tempo                                                          | **\_data e hora CIM**                                                       |
| Hora codificada UTC                                                | **\_data e hora CIM**                                                       |
| Cadeia de caracteres Unicode                                                | **\_cadeia de caracteres CIM**                                                         |



 

A sintaxe de cadeia de caracteres de octeto, que se refere a uma matriz de valores **uint8** , apresenta um problema quando mapeada para o WMI, pois o WMI permite Propriedades de tipos **uint8** e matrizes de **uint8**, enquanto Active Directory permite Propriedades do tipo cadeia de caracteres de octeto, bem como matrizes de cadeia de caracteres de octeto.

O exemplo a seguir mostra a classe de provedor de serviços de diretório que é usada para mapear uma matriz de propriedades de tipo de cadeia de caracteres de octeto.

``` syntax
Class Uint8Array 
{
    uint8 values[];
    uint32 numberOfValues;
};
```

O WMI mapeia todas as cadeias de caracteres de octeto Active Directory valores de propriedade para instâncias inseridas de **Uint8Array**. Da mesma forma, o WMI mapeia matrizes de cadeia de caracteres de octeto para matrizes de objetos **Uint8Array** inseridos.

O exemplo a seguir mostra as classes que são mapeadas pelo WMI para DN-Binary e DN-String valores de propriedade DS.

``` syntax
Class DN_With_String
{
    string dnString;
    string value;
};

Class DN_With_Binary
{
    string dnString;
    uint8 value[];
};
```

A tabela a seguir lista como o WMI mapeia o restante das propriedades de interface de atributo Active Directory para qualificadores de propriedade WMI.



| Atributo de Active Directory-nome da propriedade | Qualificador WMI       | Tipo de dados    | Informações de mapeamento                               |
|------------------------------------------|---------------------|--------------|---------------------------------------------------|
| **Sintaxe de atributo**                     | **AttributeSyntax** | **VT \_ BSTR** | Mapeado a partir da representação de cadeia de caracteres do OID. |
| **Nome comum**                          | **CN**              | **VT \_ BSTR** | Mapeado a partir do valor da cadeia de caracteres.                     |
| **Somente sistema**                          | **System**          | **BOOL do VT \_** | Mapeado a partir do valor booliano.                    |



 

> [!Note]  
> O WMI mapeia todos os qualificadores Active Directory com os `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` tipos de qualificador.

 

## <a name="association-classes"></a>Classes de associação

O serviço de diretório é essencialmente um repositório hierárquico de objetos. Os objetos que podem aparecer em um nível não folha na hierarquia são chamados de "contêineres". A estrutura dessa hierarquia é mais controlada pelas propriedades "poss-superiores" e "System-poss-superior" de uma classe no esquema. Eles, juntos, especificam o conjunto de classes cujas instâncias podem estar contidas em uma instância de uma classe de contêiner.

O exemplo a seguir modela uma associação CIM como instâncias da classe de associação estática, [**\_ \_ \_ contenção de classe LDAP do DS**](/previous-versions/windows/desktop/dsprov/ds-ldap-class-containment).

``` syntax
//  DS Class Associations Provider 

// Create a class of which instances are
// provided by this provider

[
  Association : ToInstance,
  dynamic,
  HasClassRefs,
  Provider("Microsoft|DSLDAPClassAssociationProvider|V1.0")
]
class DS_LDAP_Class_Containment
{
    [key, classref{"DS_LDAP_Root_Class"} : ToInstance ToSubClass]
    object Ref ChildClass;

    [key, classref{"DS_LDAP_Root_Class"} : ToInstance ToSubClass] 
    object Ref ParentClass; // The parent DS Class
};


// Create an instance of the provider class for registration
instance of __Win32Provider as $AssociationsProvider
{
    Name = "Microsoft|DSLDAPClassAssociationProvider|V1.0";
    Clsid = "{33831ED4-42B8-11d2-93AD-00805F853771}";
    ImpersonationLevel = 1;
};    

// Specification of the instances and operation
// provided by the provider
instance of __InstanceProviderRegistration
{
    Provider = $AssociationsProvider;
    SupportsGet = TRUE;
    SupportsPut = FALSE;
    SupportsDelete = FALSE;
    SupportsEnumeration = TRUE;
};
```

O provedor de classe de associação dá suporte aos métodos [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) e [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) .

 

