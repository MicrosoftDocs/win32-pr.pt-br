---
title: Criando grupos em um domínio
description: Um objeto de grupo é criado Active Directory Domain Services no contêiner de domínio em que o novo grupo estará contido.
ms.assetid: 40792878-4219-4242-8cf7-b092b28f2ff4
ms.tgt_platform: multiple
keywords:
- grupos do AD, criando grupos em um domínio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e2f0811e54707d0cfcc2e2efecfac33199e47d1bebd70ac7ee7e2900d8779bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118020333"
---
# <a name="creating-groups-in-a-domain"></a>Criando grupos em um domínio

Um objeto de grupo é criado Active Directory Domain Services no contêiner de domínio em que o novo grupo estará contido. Os grupos podem ser criados na raiz do domínio, em uma unidade organizacional ou em um contêiner. Para criar um objeto de grupo, use [**o método IADsContainer::Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) ou [**IDirectoryObject::CreateDSObject.**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject)

Os atributos a seguir são necessários para tornar o objeto de grupo um grupo legal que o servidor do Active Directory e o Windows de segurança reconhecerão:

<dl> <dt>

<span id="cn"></span><span id="CN"></span>**Cn**
</dt> <dd>

Especifica o nome do objeto de grupo no diretório . Esse será o nome diferenciado relativo do objeto dentro do contêiner em que o grupo é criado.

</dd> <dt>

<span id="groupType"></span><span id="grouptype"></span><span id="GROUPTYPE"></span>**Grouptype**
</dt> <dd>

Contém um inteiro que especifica o tipo de grupo e o escopo. A [**\_ enumeração \_ ADS GROUP TYPE \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) define os valores possíveis para o **atributo groupType.**

A lista a seguir define tipos e valores de grupo comuns para esse atributo.

<dl> <dt>

<span id="Domain_Local_Distribution"></span><span id="domain_local_distribution"></span><span id="DOMAIN_LOCAL_DISTRIBUTION"></span>Distribuição local do domínio
</dt> <dd>

**GRUPO ADS \_ GRUPO \_ DE \_ \_ DOMÍNIOS GRUPO LOCAL \_**

</dd> <dt>

<span id="Domain_Local_Security"></span><span id="domain_local_security"></span><span id="DOMAIN_LOCAL_SECURITY"></span>Segurança local do domínio
</dt> <dd>

**ADS \_ TIPO \_ DE GRUPO DOMÍNIO LOCAL GRUPO \_ \_ \_ ADS** SEGURANÇA DE TIPO DE GRUPO \| **\_ \_ \_ \_ HABILITADA**

</dd> <dt>

<span id="Global_Distribution"></span><span id="global_distribution"></span><span id="GLOBAL_DISTRIBUTION"></span>Distribuição global
</dt> <dd>

**GRUPO GLOBAL \_ \_ TIPO ADS \_ \_**

</dd> <dt>

<span id="Global_Security"></span><span id="global_security"></span><span id="GLOBAL_SECURITY"></span>Segurança global
</dt> <dd>

**ADS \_ SEGURANÇA DE \_ TIPO \_ DE \_ GRUPO GLOBAL** DE ANÚNCIOS DE GRUPO \| **\_ \_ \_ \_ HABILITADA**

</dd> <dt>

<span id="Universal_Distribution"></span><span id="universal_distribution"></span><span id="UNIVERSAL_DISTRIBUTION"></span>Distribuição Universal
</dt> <dd>

**GRUPO UNIVERSAL \_ \_ DO TIPO \_ ADS \_**

</dd> <dt>

<span id="Universal_Security"></span><span id="universal_security"></span><span id="UNIVERSAL_SECURITY"></span>Segurança Universal
</dt> <dd>

**ADS \_ SEGURANÇA DE \_ TIPO \_ DE \_ GRUPO UNIVERSAL** DE ANÚNCIOS DE GRUPO \| **\_ \_ \_ \_ HABILITADA**

</dd> <dt>


</dt> <dd>

</dd> </dl>

Se o grupo for destinado à configuração do controle de acesso em objetos de diretório, o grupo deverá ser um grupo de Segurança Global ou Segurança Universal.

Esteja ciente de que os grupos de Segurança Universal só podem ser criados Windows 2000 domínios em execução no modo nativo. Para obter mais informações sobre como detectar o modo misto e nativo, consulte [Detectando o modo de operação de um domínio](detecting-the-operation-mode-of-a-domain.md).

</dd> <dt>

<span id="sAMAccountName"></span><span id="samaccountname"></span><span id="SAMACCOUNTNAME"></span>**Samaccountname**
</dt> <dd>

Contém uma cadeia de caracteres que é o nome usado para dar suporte a clientes e servidores de uma versão anterior. O **sAMAccountName** deve ter menos de 20 caracteres para dar suporte a clientes de uma versão anterior do Windows.

O **sAMAccountName** deve ser exclusivo entre todos os objetos de entidade de segurança dentro do domínio. Uma consulta deve ser executada no domínio para verificar se **o sAMAccountName** é exclusivo dentro do domínio.

</dd> </dl>

Os membros do grupo podem ser adicionados no momento da criação usando o [**método IDirectoryObject::CreateDSObject.**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) Opcionalmente, os membros podem ser adicionados ao grupo após a criação usando o [**método IADsGroup::Add.**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) Para obter mais informações sobre como adicionar membros a um grupo, consulte [Adicionando membros a grupos em um domínio](adding-members-to-groups-in-a-domain.md).

 

 