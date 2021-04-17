---
description: Fornece regras para mapeamento de classes WMI para Active Directory.
ms.assetid: 295d3233-5729-4eb0-9fa3-1cf64fef2909
ms.tgt_platform: multiple
title: Mapeando classes de Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a606cfacc2e9d56ef07973df182f5ce1a65be35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811988"
---
# <a name="mapping-active-directory-classes"></a>Mapeando classes de Active Directory

Como Active Directory tem uma ampla variedade de objetos possíveis, o WMI não pode criar um mapeamento direto de um para um. Em vez disso, o provedor de serviços de diretório usa regras para mapear classes entre as duas tecnologias.

As seções a seguir são discutidas neste tópico:

-   [Classes de mapeamento](#mapping-classes)
-   [Atributos de mapeamento](#mapping-attributes)
-   [Classes de associação](#association-classes)

> [!Note]  
> Para obter mais informações sobre o suporte e a instalação desse componente em um sistema operacional específico, consulte [disponibilidade do sistema operacional de componentes WMI](operating-system-availability-of-wmi-components.md).

 

## <a name="mapping-classes"></a>Classes de mapeamento

A lista a seguir descreve as diretrizes que o provedor de serviços de diretório usa para mapear Active Directory classes para classes WMI:

-   Cada classe abstrata no esquema de Active Directory é mapeada para uma classe abstrata no esquema WMI.

    No esquema WMI, cada classe abstrata é prefixada com DS \_ . Por exemplo, a classe **Person** do esquema de Active Directory é mapeada para a classe WMI **\_ Person do DS** .

-   Cada classe não abstrata do esquema de Active Directory mapeia para as duas classes a seguir no esquema WMI:

    -   A primeira classe mapeada é prefixada com anúncios \_ . Essas são classes abstratas, mapeadas de acordo com as regras abaixo.
    -   A segunda classe mapeada é uma classe não abstrata com o \_ prefixo de nome DS. Essa classe é derivada da \_ classe abstrata ADS, com a adição do qualificador do [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) .

    Por exemplo, a classe de **usuário** do esquema de Active Directory é mapeada para duas classes. A primeira classe é a classe abstrata do **\_ usuário ADS** , mapeada de acordo com as regras abaixo. A segunda classe é a classe não abstrata do **\_ usuário do DS** . Ele é derivado do **\_ usuário do ADS** e tem o qualificador do [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) adicionado.

-   A menos que especificado de outra forma, o nome de uma classe mapeada é o valor desconfigurado da propriedade **LDAP-Display-Name** na classe Active Directory.
-   Se a propriedade **subclasse-of** estiver presente na classe Active Directory, a classe MAPEADA por WMI será derivada da classe especificada.

    Se a propriedade **subclasse-of** não estiver presente, a classe MAPEADA por WMI será derivada da classe de **\_ \_ \_ classe raiz LDAP do DS** , conforme especificado no arquivo MOF.

    > [!Note]  
    > Essa classe tem a propriedade de chave **ADSIPath** , com um tipo **VT \_ BSTR**. Este é o caminho ADSI exclusivo que identifica essa instância. O Active Directory dá suporte apenas à herança única e, portanto, isso funciona.

     

-   Um qualificador **dinâmico** do tipo **VT \_ bool** e o tipo `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` definido como **true** são criados para cada classe. Esse é um qualificador WMI padrão que indica que as instâncias dessa classe são fornecidas dinamicamente.
-   Se a classe não for abstrata, o provedor criará um qualificador de [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) do tipo **VT \_ BSTR bool** e o tipo de qualificador `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` definido como "provedor de instância DS" para cada classe. Este é um qualificador WMI padrão que indica o nome do provedor que fornece dinamicamente instâncias dessa classe.

O restante das propriedades ADSI é mapeado para qualificadores de classe e propriedades de acordo com as tabelas a seguir. Todos os qualificadores são mapeados com um valor de sinalizador de qualificador de `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` .

O a seguir lista informações de mapeamento para a classe Active Directory, mostrando o qualificador WMI e o tipo de qualificador WMI para cada propriedade Active Directory.

<dl> <dt>

**Nome comum**
</dt> <dd>

**CN** (**VT \_ BSTR**)

Mapeado diretamente do valor da cadeia de caracteres.

</dd> <dt>

**Categoria de objeto-padrão**
</dt> <dd>

**DefaultObjectCategory** (**VT \_ BSTR**)

Mapeado diretamente do valor da cadeia de caracteres.

</dd> <dt>

**Padrão-descritor de segurança**
</dt> <dd>

**DefaultSecurityDescriptor** (**VT \_ BSTR**)

Mapeado diretamente do valor da cadeia de caracteres.

</dd> <dt>

**Regis-ID**
</dt> <dd>

**GovernsId** (**VT \_ BSTR**)

Mapeado da representação de cadeia de caracteres da OID; por exemplo, "{1 3 3 6}".

</dd> <dt>

**Classe de objeto**
</dt> <dd>

N/D

Não mapeado.

</dd> <dt>

**Categoria de classe de objeto**
</dt> <dd>

**ObjectClassCategory** (**VT \_ i4**)

Mapeado diretamente do valor inteiro. Além disso, se o valor for Abstract (2), o qualificador **CIM \_ bool Standard VT** , chamado de qualificador **"Abstract"** , também será criado.

</dd> <dt>

**RDN-ATT-ID**
</dt> <dd>

**RDNATTID** (**VT \_ BSTR**)

Mapeado da representação de cadeia de caracteres do valor de OID; por exemplo, "{1 3 3 6}". Além disso, a propriedade identificada aqui é anotada com o qualificador de CIM **indexado** padrão definido como **true**.

</dd> <dt>

**Somente sistema**
</dt> <dd>

**SystemOnly** (**VT \_ bool**)

Mapeado diretamente do valor booliano.

</dd> </dl>

 

O seguinte lista as propriedades de classe de Active Directory mapeadas para propriedades de classe WMI.

<dl> <dt>

**Pode-conter**
</dt> <dd>

Cada propriedade nessa lista é mapeada para uma propriedade WMI.

</dd> <dt>

**Deve conter**
</dt> <dd>

Cada propriedade nessa lista é mapeada para uma propriedade WMI. O qualificador CIM padrão **não \_ nulo** é criado para cada um deles.

</dd> <dt>

**Sistema-pode-conter**
</dt> <dd>

Cada propriedade nessa lista é mapeada para uma propriedade WMI. Além disso, cada propriedade é anotada com um qualificador de **sistema** , definida como **true**.

</dd> <dt>

**Sistema-deve conter**
</dt> <dd>

Cada propriedade nessa lista é mapeada para uma propriedade WMI. O qualificador CIM padrão **não \_ nulo** é criado para cada um deles. Além disso, cada propriedade é anotada com um qualificador de **sistema** , definida como **true**.

</dd> </dl>

## <a name="mapping-attributes"></a>Atributos de mapeamento

O provedor de serviços de diretório mapeia cada atributo de uma classe Active Directory para exatamente uma propriedade da classe WMI correspondente de acordo com as regras nesta seção. Em geral, o provedor de serviços de diretório nomeia a propriedade WMI como a versão desconfigurado do valor **LDAP-Display-Name** do atributo Active Directory.

Se a propriedade Active Directory **for de valor único** for **false**, essa propriedade WMI será combinada com o operador OR com a **matriz de \_ sinalizador \_ CIM**. Observe que cada propriedade é marcada com o qualificador **VT \_ BSTR** , **ADSyntax**. Representa a sintaxe de Active Directory subjacente.

A tabela a seguir lista o mapeamento da sintaxe de Active Directory para o tipo de dados de Propriedade do WMI.



| Elemento Active Directory                                      | Tipo de dados WMI                                                           |
|---------------------------------------------------------------|-------------------------------------------------------------------------|
| [**Ponto de acesso**](/windows/desktop/ADSchema/s-object-access-point)            | **\_cadeia de caracteres CIM**                                                         |
| [**Boolean**](/windows/desktop/ADSchema/s-boolean)                             | **\_booliano de CIM**                                                        |
| **Cadeia de caracteres sem diferenciação de maiúsculas**                                   | **\_cadeia de caracteres CIM**                                                         |
| [**Cadeia de caracteres diferencia maiúsculas de minúscula**](/windows/desktop/ADSchema/s-string-case-sensitive) | **\_cadeia de caracteres CIM**                                                         |
| [**Nome distinto**](/windows/desktop/ADSchema/s-object-ds-dn)             | **\_cadeia de caracteres CIM**                                                         |
| [**DN binário**](/windows/desktop/ADSchema/s-object-dn-binary)                  | Objeto inserido do DN de classe **\_ com \_ binário** definido abaixo.<br/> |
| [**Cadeia de caracteres DN**](/windows/desktop/ADSchema/s-object-dn-string)                  | Objeto inserido do DN de classe **\_ com a \_ cadeia de caracteres** definida abaixo.<br/> |
| [**Enumeração**](/windows/desktop/ADSchema/s-enumeration)                     | **\_Sint32 CIM**                                                         |
| [**Enumeração**](/windows/desktop/ADSchema/s-enumeration)                     | **\_cadeia de caracteres CIM**                                                         |
| [**Valores**](/windows/desktop/ADSchema/s-integer)                             | **\_Sint32 CIM**                                                         |
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
| Hora                                                          | **\_data e hora CIM**                                                       |
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
| **Nome comum**                          | **Hong**              | **VT \_ BSTR** | Mapeado a partir do valor da cadeia de caracteres.                     |
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

 

