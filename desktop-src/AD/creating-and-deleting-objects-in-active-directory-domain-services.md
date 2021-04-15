---
title: Criando e excluindo objetos no Active Directory Domain Services
description: O procedimento usado para criar e excluir objetos programaticamente no Active Directory Domain Services depende da tecnologia de programação usada.
ms.assetid: 13f83aea-ad39-4737-af3c-24316a31046d
ms.tgt_platform: multiple
keywords:
- Criando e excluindo objetos de Active Directory Active Directory
- Active Directory Domain Services Active Directory, usando a criação e exclusão de objetos
- objetos Active Directory, criando e excluindo objetos Active Directory Domain Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d3e85ef3c356978faeab059e3969bb657185bd
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453940"
---
# <a name="creating-and-deleting-objects-in-active-directory-domain-services"></a>Criando e excluindo objetos no Active Directory Domain Services

O procedimento usado para criar e excluir objetos programaticamente no Active Directory Domain Services depende da tecnologia de programação usada. Para obter mais informações sobre como criar e excluir objetos no Active Directory Domain Services com uma tecnologia de programação específica, consulte os tópicos listados na tabela a seguir.



| Tecnologia de programação                                                                       | Para obter mais informações                                                            |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Active Directory Service Interfaces](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)         | [Criando e excluindo objetos](/windows/desktop/ADSI/creating-and-deleting-objects)             |
| [Protocolo Lightweight Directory Access](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) | [Modificando uma entrada de diretório](/previous-versions/windows/desktop/ldap/modifying-a-directory-entry)                 |
| [System.DirectoryServices](/dotnet/api/system.directoryservices) | [Criar, excluir, renomear e mover objetos](https://msdn.microsoft.com/library/ms180850(v=VS.80).aspx) |



 

## <a name="creating-an-object"></a>Criando um objeto

Em geral, os únicos atributos necessários para um objeto a ser criado são os atributos **CN** e **objectClass** . No entanto, apenas criar um objeto não o torna necessariamente um objeto funcional. Determinados tipos de objetos, como usuários e grupos, têm atributos adicionais necessários para torná-los funcionais. Para obter mais informações sobre como criar tipos específicos de objetos, consulte [criando um usuário](creating-a-user.md) e [criando grupos em um domínio](creating-groups-in-a-domain.md).

**Windows Server 2003:** Quando um objeto do [**usuário**](/windows/desktop/ADSchema/c-user), [**grupo**](/windows/desktop/ADSchema/c-group)ou classe de [**computador**](/windows/desktop/ADSchema/c-computer) é criado em um controlador de domínio que está sendo executado no comparação Server 2003 ou posterior, o controlador de domínio define automaticamente o atributo [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) para o objeto como uma cadeia de caracteres exclusiva, se um não for especificado.

## <a name="deleting-an-object"></a>Excluindo um objeto

O servidor de Active Directory executa as seguintes ações quando um objeto é excluído:

-   O atributo **IsDeleted** do objeto excluído é definido como **true**. Objetos com um valor de atributo **IsDeleted** definido como **true** são chamados de [*marcas para exclusão*](/previous-versions/windows/desktop/legacy/ms681941(v=vs.85)).
-   O objeto excluído é movido para o contêiner objetos excluídos para seu contexto de nomenclatura. Se a propriedade **systemFlags** do objeto contiver o sinalizador 0x02000000, o objeto não será movido para o contêiner objetos excluídos. Para obter mais informações sobre como associar e enumerar o conteúdo do contêiner de objetos excluídos, consulte [recuperando objetos excluídos](retrieving-deleted-objects.md).
-   O contêiner objetos excluídos é simples, de modo que todos os objetos residem no mesmo nível dentro do contêiner objetos excluídos. Assim, o nome distinto relativo do objeto excluído é alterado para garantir que o nome seja exclusivo dentro do contêiner objetos excluídos. Se o nome original tiver mais de 75 caracteres, ele será truncado para 75 caracteres. Em seguida, os itens a seguir são anexados ao novo nome:
    1.  Um caractere 0x0A
    2.  A cadeia de caracteres "DEL:"
    3.  A forma de cadeia de caracteres de um GUID exclusivo, como "947e3228-70c9-4311-8b7a-e5c9b5bd4432"

    Um exemplo de um nome de objeto excluído é:
    ```C++
    Jeff Smith\0ADEL:947e3228-70c9-4311-8b7a-e5c9b5bd4432
    ```

    

-   A maioria dos valores de atributo para o objeto excluído é removida. Os seguintes atributos são retidos automaticamente:

    -   **attributeID**
    -   **attributeSyntax**
    -   **distinguishedName**
    -   **dNReferenceUpdate**
    -   **flatname**
    -   **governsID**
    -   **groupType**
    -   **instanceType**
    -   **lDAPDisplayName**
    -   **legacyExchangeDN**
    -   **mS-DS-CreatorSID**
    -   **mSMQOwnerID**
    -   **name**
    -   **nCName**
    -   **objectClass**
    -   **objectGUID**
    -   **objectSid**
    -   **oMSyntax**
    -   **proxiedObjectName**
    -   **replPropertyMetaData**
    -   **sAMAccountName**
    -   **securityIdentifier**
    -   **subClassOf**
    -   **systemFlags**
    -   **trustattributes**
    -   **trustDirection**
    -   **trustPartner**
    -   **TrustType**
    -   **userAccountControl**
    -   **uSNChanged**
    -   **uSNCreated**
    -   **whenCreated**

    Outros atributos que têm um valor de atributo **searchFlags** que contém 0x00000008 também são retidos.

    Os seguintes valores de atributo são sempre removidos de um objeto excluído:

    -   **objectCategory**
    -   **samAccountType**

-   O descritor de segurança do objeto excluído é retido e as entradas de controle de acesso herdáveis não são propagadas. O descritor de segurança é mantido como está no momento em que o objeto é excluído.
-   Os links para e do objeto excluído são apagados. Isso é executado em segundo plano depois que o objeto é excluído. Se o objeto excluído for restaurado antes que todos os links sejam limpos, um erro será recebido.
-   Se o objeto for excluído em um controlador de domínio do Windows Server 2003, o atributo **lastKnownParent** do objeto excluído será definido como o nome distinto do contêiner em que o objeto foi contido quando ele foi excluído.

O objeto excluído permanece no contêiner objetos excluídos por um período de tempo conhecido como a *vida útil da marca de exclusão*. Por padrão, o tempo de vida da marca para exclusão é de 60 dias, mas esse valor pode ser alterado pelo administrador do sistema. Depois que o tempo de vida da marca de exclusão expirar, o objeto será removido permanentemente do serviço de diretório. Para evitar a falta de uma operação de exclusão, um aplicativo deve executar sincronizações incrementais com mais frequência do que o tempo de vida da marca de exclusão.

O Windows Server 2003 adiciona a capacidade de restaurar objetos excluídos. Para obter mais informações sobre a restauração de objetos excluídos, consulte [restaurando objetos excluídos](restoring-deleted-objects.md).

Quando um item é excluído, nenhum dos atributos do objeto pode ser modificado. No Windows Server 2003, é possível modificar o descritor de segurança (o atributo **ntSecurityDescriptor** ) em um objeto excluído. Isso é para permitir a restauração de objetos quando a pessoa que está restaurando o objeto não tem permissões de gravação para atributos obrigatórios. Para atualizar o descritor de segurança em um objeto excluído, o chamador deve ter o direito de acesso de controle "reanimar a marca de exclusão" no contexto de nomenclatura, além do **\_ DAC de gravação** regular e do acesso de **\_ proprietário de gravação** . Mesmo que o descritor de segurança seja restritivo, o administrador pode primeiro assumir a propriedade do objeto, supondo que o administrador tenha o privilégio se você tem o **\_ \_ \_ nome de propriedade** e, em seguida, modifique o descritor de segurança. Para fazer isso, use a [**função \_ LDAP \_ Modify \_ ext**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) com o [**servidor LDAP \_ Mostrar controle de \_ \_ \_ OID excluído**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) . A lista de modificação deve conter uma única substituição de atributo para o atributo **ntSecurityDescriptor** .

 

 