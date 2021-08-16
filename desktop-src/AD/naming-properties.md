---
title: Atributos de nomeação de usuário
description: Atributos de nomeação de usuário identificam objetos de usuário, como nomes de logon e IDs usados para fins de segurança.
ms.assetid: 2192743c-cedd-4b03-a402-3992d64a4801
ms.tgt_platform: multiple
keywords:
- AD de atributos de nomen por nome de usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8548178bba8012231a803d476699e8ebb386b6fa9a29015f3721e7b32d94158
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185926"
---
# <a name="user-naming-attributes"></a>Atributos de nomeação de usuário

Atributos de nomeação de usuário identificam objetos de usuário, como nomes de logon e IDs usados para fins de segurança. Os **atributos cn**, **name** e **distinguishedName** são exemplos de atributos de nomeação de usuário. Um objeto de usuário é um objeto de entidade de segurança, portanto, ele também inclui os seguintes atributos de nomeação de usuário:

-   [userPrincipalName](#userprincipalname) — o nome de logon do usuário
-   [objectGUID](#objectguid) — o identificador exclusivo de um usuário
-   [sAMAccountName](#samaccountname) — um nome de logon que dá suporte à versão anterior do Windows
-   [objectSid](#objectsid) — SID (identificador de segurança) do usuário
-   [sIDHistory](#sidhistory) — os SIDs anteriores para o objeto de usuário

> [!Note]  
> Você pode exibir e gerenciar esses atributos usando o snap-in MMC usuário e computadores do Active Directory, que está disponível no [rsat (Ferramentas de Administração de Servidor Remoto)](https://www.microsoft.com/download/details.aspx?id=45520).

 

## <a name="userprincipalname"></a>userPrincipalName

O **atributo userPrincipalName** é o nome de logon do usuário. O atributo consiste em um NOME UPN, que é o nome de logon mais comum para Windows usuários. Normalmente, os usuários usam seu UPN para fazer logon em um domínio. Esse atributo é uma cadeia de caracteres indexada com valor único.

Um UPN é um nome de logon no estilo da Internet para um usuário com base no RFC 822 padrão da Internet. O UPN é menor que um nome diferenciado e é mais fácil de lembrar. Por convenção, ele deve ser mapeado para o nome de email do usuário. O objetivo do UPN é consolidar os namespaces de email e logon para que o usuário só precise se lembrar de um único nome.

### <a name="upn-format"></a>Formato UPN

Um UPN consiste em um prefixo UPN (o nome da conta de usuário) e um sufixo UPN (um nome de domínio de DNS). O prefixo é unido ao sufixo com o uso do símbolo "@". Por exemplo, "someone@ example.com". Um UPN deve ser exclusivo entre todos os objetos de entidade de segurança em uma floresta de diretórios. Isso significa que o prefixo de um UPN pode ser reutilizado, mas não com o mesmo sufixo.

Um sufixo UPN tem as seguintes restrições:

-   Ele deve ser o nome DNS de um domínio, mas não precisa ser o nome do domínio que contém o usuário.
-   Ele deve ser o nome de um domínio na floresta de domínio atual ou um nome alternativo listado no atributo **upnSuffixes** do contêiner Partitions dentro do contêiner De configuração.

### <a name="upn-management"></a>Gerenciamento de UPN

Um UPN pode ser atribuído, mas não é necessário, quando uma conta de usuário é criada. Quando um UPN é criado, ele não é afetado por alterações em outros atributos do objeto de usuário, como o usuário que está sendo renomeado ou movido. Isso permite que o usuário mantenha o mesmo nome de logon se um diretório for reestruturado. No entanto, um administrador pode alterar um UPN. Ao criar um novo objeto de usuário, você deve verificar o domínio local e o catálogo global do nome proposto para garantir que ele ainda não exista.

Quando um usuário usa um UPN para fazer logon em um domínio, o UPN é validado pesquisando o domínio local e, em seguida, o catálogo global. Se o UPN não for encontrado no catálogo global, a tentativa de logon falhará.

## <a name="objectguid"></a>objectGUID

O **atributo objectGUID** é o identificador exclusivo de um usuário. O atributo é um GUID (Identificador Global Exclusivo) de 128 bits de valor único e é armazenado como uma estrutura [**ADS \_ OCTET \_ STRING.**](/windows/win32/api/iads/ns-iads-ads_octet_string) O GUID é criado pelo servidor do Active Directory quando um objeto de usuário é criado.

Como o nome diferenciado de um objeto muda se o objeto é renomeado ou movido, o nome diferenciado não é um identificador confiável de um objeto. No Active Directory Domain Services, o atributo **objectGUID** de um objeto nunca muda, mesmo que o objeto seja renomeado ou movido. Você pode recuperar a forma de cadeia de caracteres **do objectGUID** usando o **método de** propriedade GUID em Métodos de [Propriedade IADs](/windows/desktop/ADSI/iads-property-methods).

## <a name="samaccountname"></a>sAMAccountName

O **atributo sAMAccountName** é um nome de logon usado para dar suporte a clientes e servidores da versão anterior do Windows, como Windows NT 4.0, Windows 95, Windows 98 e LAN Manager. O nome de logon deve ter 20 ou menos caracteres e ser exclusivo entre todos os objetos de entidade de segurança dentro do domínio.

## <a name="objectsid"></a>objectSid

O **atributo objectSid** é o SID (identificador de segurança) do usuário. O SID é usado pelo sistema para identificar um usuário e suas associações de grupo durante interações com Windows segurança. O atributo tem valor único. O SID é um valor binário exclusivo usado para identificar o usuário como uma entidade de segurança.

O SID é definido pelo sistema quando o usuário é criado. Cada usuário tem um SID exclusivo emitido por um domínio Windows e armazenado no atributo **objectSid** do objeto de usuário no diretório . Sempre que um usuário faz login, o sistema recupera o SID do usuário do diretório e o coloca no token de acesso do usuário. O SID do usuário também é usado para recuperar os SIDs dos grupos dos quais o usuário é membro e os coloca no token de acesso do usuário. Quando um SID tiver sido usado como o identificador exclusivo de um usuário ou grupo, ele não poderá ser usado novamente para identificar outro usuário ou grupo.

## <a name="sidhistory"></a>Sidhistory

O **atributo sIDHistory** contém os SIDs anteriores para o objeto de usuário. Esse é um atributo com vários valores. Um objeto de usuário terá SIDs anteriores se o usuário tiver sido movido para outro domínio. Sempre que um objeto de usuário é movido para um novo domínio, um novo SID é criado e atribuído ao atributo **objectSid** e o SID anterior é adicionado ao atributo **sIDHistory.**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos de objeto de usuário](user-object-attributes.md)
</dt> </dl>

 

 