---
title: Criando e excluindo objetos no Active Directory Domain Services
description: O procedimento usado para criar e excluir objetos programaticamente no Active Directory Domain Services depende da tecnologia de programação usada.
ms.assetid: 13f83aea-ad39-4737-af3c-24316a31046d
ms.tgt_platform: multiple
keywords:
- Criando e excluindo objetos do Active Directory Active Directory Active Directory
- Active Directory Domain Services Active Directory usando a criação e a exclusão de objetos
- objetos do Active Directory , criando e excluindo Active Directory Domain Services objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b681f7e4d193a248a8846ad8f02d1b3c222d735194bfe57940bd7e787710035d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118020427"
---
# <a name="creating-and-deleting-objects-in-active-directory-domain-services"></a>Criando e excluindo objetos no Active Directory Domain Services

O procedimento usado para criar e excluir objetos programaticamente no Active Directory Domain Services depende da tecnologia de programação usada. Para obter mais informações sobre como criar e excluir objetos Active Directory Domain Services com uma tecnologia de programação específica, consulte os tópicos listados na tabela a seguir.



| Tecnologia de programação                                                                       | Para obter mais informações                                                            |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Active Directory Service Interfaces](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)         | [Criando e excluindo objetos](/windows/desktop/ADSI/creating-and-deleting-objects)             |
| [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) | [Modificando uma entrada de diretório](/previous-versions/windows/desktop/ldap/modifying-a-directory-entry)                 |
| [System.DirectoryServices](/dotnet/api/system.directoryservices) | [Criar, excluir, renomear e mover objetos](https://msdn.microsoft.com/library/ms180850(v=VS.80).aspx) |



 

## <a name="creating-an-object"></a>Criando um objeto

Em geral, os únicos atributos necessários para um objeto a ser criado são os **atributos cn** e **objectClass.** No entanto, apenas criar um objeto não o torna um objeto funcional. Determinados tipos de objetos, como usuários e grupos, têm atributos adicionais necessários para torná-los funcionais. Para obter mais informações sobre como criar tipos específicos de objetos, consulte [Criando um usuário e](creating-a-user.md) criando grupos em um [domínio](creating-groups-in-a-domain.md).

**Windows Server 2003:** Quando um objeto da [](/windows/desktop/ADSchema/c-group)classe [](/windows/desktop/ADSchema/c-computer) de usuário [**,**](/windows/desktop/ADSchema/c-user)grupo ou computador é criado em um controlador de domínio que está em execução no WWindows Server 2003 ou posterior, o controlador de domínio define automaticamente o atributo [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) para o objeto como uma cadeia de caracteres exclusiva, se não for especificado.

## <a name="deleting-an-object"></a>Excluindo um objeto

O servidor do Active Directory executa as seguintes ações quando um objeto é excluído:

-   O **atributo isDeleted** do objeto excluído é definido como **TRUE.** Objetos com um **valor de atributo isDeleted** definido como **TRUE** são chamados [*de tombstones*](/previous-versions/windows/desktop/legacy/ms681941(v=vs.85)).
-   O objeto excluído é movido para o contêiner Objetos Excluídos para seu contexto de nomentura. Se a propriedade **systemFlags** do objeto contiver o sinalizador 0x02000000, o objeto não será movido para o contêiner Objetos Excluídos. Para obter mais informações sobre como vincular e enumerar o conteúdo do contêiner Objetos Excluídos, consulte [Recuperando objetos excluídos.](retrieving-deleted-objects.md)
-   O contêiner Objetos Excluídos é simples, portanto, todos os objetos residem no mesmo nível dentro do contêiner Objetos Excluídos. Portanto, o nome diferenciado relativo do objeto excluído é alterado para garantir que o nome seja exclusivo dentro do contêiner Objetos Excluídos. Se o nome original tiver mais de 75 caracteres, ele será truncado para 75 caracteres. Em seguida, os seguintes são anexados ao novo nome:
    1.  Um 0x0A caractere
    2.  A cadeia de caracteres "DEL:"
    3.  A forma de cadeia de caracteres de um GUID exclusivo, como "947e3228-70c9-4311-8b7a-e5c9b5bd4432"

    Um exemplo de um nome de objeto excluído é:
    ```C++
    Jeff Smith\0ADEL:947e3228-70c9-4311-8b7a-e5c9b5bd4432
    ```

    

-   A maioria dos valores de atributo para o objeto excluído é removida. Os seguintes atributos são retidos automaticamente:

    -   **Attributeid**
    -   **attributeSyntax**
    -   **Distinguishedname**
    -   **dNReferenceUpdate**
    -   **flatName**
    -   **governsID**
    -   **groupType**
    -   **instanceType**
    -   **lDAPDisplayName**
    -   **legacyExchangeDN**
    -   **mS-DS-CreatorSID**
    -   **mSMQOwnerID**
    -   **name**
    -   **Ncname**
    -   **Objectclass**
    -   **Objectguid**
    -   **Objectsid**
    -   **oMSyntax**
    -   **proxiedObjectName**
    -   **replPropertyMetaData**
    -   **Samaccountname**
    -   **Securityidentifier**
    -   **subClassOf**
    -   **systemFlags**
    -   **trustAttributes**
    -   **Trustdirection**
    -   **trustPartner**
    -   **trustType**
    -   **userAccountControl**
    -   **uSNChanged**
    -   **uSNCreated**
    -   **whenCreated**

    Outros atributos que têm um **valor de atributo searchFlags** que contém 0x00000008 também são mantidos.

    Os seguintes valores de atributo são sempre removidos de um objeto excluído:

    -   **objectCategory**
    -   **samAccountType**

-   O descritor de segurança do objeto excluído é mantido e as entradas de controle de acesso herdáveis não são propagadas. O descritor de segurança é mantido no estado em que se está no momento em que o objeto é excluído.
-   Os links para e do objeto excluído são limpos. Isso é executado em segundo plano depois que o objeto é excluído. Se o objeto excluído for restaurado antes que todos os links sejam limpos, um erro será recebido.
-   Se o objeto for excluído em um controlador de domínio do Windows Server 2003, o atributo **lastKnownParent** do objeto excluído será definido como o nome diferenciado do contêiner em que o objeto estava contido quando foi excluído.

O objeto excluído permanece no contêiner Objetos Excluídos por um período de tempo conhecido como tempo de vida *da chave de exclusão.* Por padrão, o tempo de vida da lápis é de 60 dias, mas esse valor pode ser alterado pelo administrador do sistema. Depois que o tempo de vida da lápis expirar, o objeto será removido permanentemente do Serviço de Diretório. Para evitar a falta de uma operação de exclusão, um aplicativo deve executar sincronizações incrementais com mais frequência do que o tempo de vida da chave de exclusão.

Windows O Server 2003 adiciona a capacidade de restaurar objetos excluídos. Para obter mais informações sobre a restauração de objeto excluído, consulte [Restaurando objetos excluídos.](restoring-deleted-objects.md)

Quando um item é excluído, nenhum dos atributos do objeto pode ser modificado. No Windows Server 2003, é possível modificar o descritor de segurança (o atributo **ntSecurityDescriptor)** em um objeto excluído. Isso é para permitir a restauração de objetos quando a pessoa que restaura o objeto não tem permissões de gravação para atributos obrigatórios. Para atualizar o descritor de segurança em um objeto excluído, o chamador deve ter o direito de acesso de controle "Reanimar Tombstone" no contexto de nomeação, além do acesso regular **WRITE \_ DAC** e **WRITE \_ OWNER.** Mesmo que o descritor de segurança seja restritivo, o administrador poderá primeiro assumir a propriedade do objeto, supondo que o administrador tenha o privilégio **ES \_ TAKE \_ OWNERSHIP \_ NAME** e, em seguida, modifique o descritor de segurança. Para fazer isso, use a [**função ldap \_ modify ext \_ \_ s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) com o controle [**OID LDAP \_ SERVER SHOW \_ \_ DELETED. \_**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) A lista de modificação deve conter uma única substituição de atributo para o **atributo ntSecurityDescriptor.**

 

 