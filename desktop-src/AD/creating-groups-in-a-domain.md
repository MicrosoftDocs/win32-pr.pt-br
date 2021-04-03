---
title: Criando grupos em um domínio
description: Um objeto de grupo é criado em Active Directory Domain Services no contêiner de domínio em que o novo grupo estará contido.
ms.assetid: 40792878-4219-4242-8cf7-b092b28f2ff4
ms.tgt_platform: multiple
keywords:
- grupos de anúncios, criando grupos em um domínio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100700b08fb82b750ee68dfed6bcb26060929e87
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007338"
---
# <a name="creating-groups-in-a-domain"></a>Criando grupos em um domínio

Um objeto de grupo é criado em Active Directory Domain Services no contêiner de domínio em que o novo grupo estará contido. Os grupos podem ser criados na raiz do domínio, em uma unidade organizacional ou em um contêiner. Para criar um objeto de grupo, use o método [**IADsContainer:: Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) ou [**IDirectoryObject:: CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) .

Os seguintes atributos são necessários para tornar o objeto de grupo um grupo legal que o servidor Active Directory e o sistema de segurança do Windows reconhecerão:

<dl> <dt>

<span id="cn"></span><span id="CN"></span>**Hong**
</dt> <dd>

Especifica o nome do objeto de grupo no diretório. Esse será o nome distinto relativo do objeto dentro do contêiner em que o grupo é criado.

</dd> <dt>

<span id="groupType"></span><span id="grouptype"></span><span id="GROUPTYPE"></span>**groupType**
</dt> <dd>

Contém um inteiro que especifica o tipo de grupo e o escopo. A [**enumeração \_ \_ \_ enum do tipo de grupo ADS**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) define os valores possíveis para o atributo **GroupType** .

A lista a seguir define os valores e tipos de grupo comuns para esse atributo.

<dl> <dt>

<span id="Domain_Local_Distribution"></span><span id="domain_local_distribution"></span><span id="DOMAIN_LOCAL_DISTRIBUTION"></span>Distribuição local de domínio
</dt> <dd>

**\_grupo de \_ grupos \_ locais de domínio do tipo de \_ grupo ADS \_**

</dd> <dt>

<span id="Domain_Local_Security"></span><span id="domain_local_security"></span><span id="DOMAIN_LOCAL_SECURITY"></span>Segurança local do domínio
</dt> <dd>

**Anúncios \_ do grupo \_ \_ local de \_ domínio \_ tipo** de grupo \| **ADS segurança de tipo de grupo \_ \_ \_ \_ habilitado**

</dd> <dt>

<span id="Global_Distribution"></span><span id="global_distribution"></span><span id="GLOBAL_DISTRIBUTION"></span>Distribuição global
</dt> <dd>

**\_ \_ grupo global do tipo de grupo ADS \_ \_**

</dd> <dt>

<span id="Global_Security"></span><span id="global_security"></span><span id="GLOBAL_SECURITY"></span>Segurança global
</dt> <dd>

**Anúncios \_ do tipo de grupo grupo \_ \_ global \_** tipos de \| **\_ grupo ADS \_ \_ segurança \_ habilitada**

</dd> <dt>

<span id="Universal_Distribution"></span><span id="universal_distribution"></span><span id="UNIVERSAL_DISTRIBUTION"></span>Distribuição universal
</dt> <dd>

**\_tipo de grupo ADS \_ \_ \_ grupo universal**

</dd> <dt>

<span id="Universal_Security"></span><span id="universal_security"></span><span id="UNIVERSAL_SECURITY"></span>Segurança universal
</dt> <dd>

**Anúncios \_ do grupo \_ \_ Universal de \_ tipos** de grupo \| **ADS segurança de tipo de grupo \_ \_ \_ \_ habilitado**

</dd> <dt>


</dt> <dd>

</dd> </dl>

Se o grupo for destinado a configurar o controle de acesso em objetos de diretório, o grupo deverá ser um grupo de segurança global ou Universal Security.

Lembre-se de que os grupos de segurança universal só podem ser criados em domínios do Windows 2000 em execução no modo nativo. Para obter mais informações sobre como detectar o modo misto e nativo, consulte [detectando o modo de operação de um domínio](detecting-the-operation-mode-of-a-domain.md).

</dd> <dt>

<span id="sAMAccountName"></span><span id="samaccountname"></span><span id="SAMACCOUNTNAME"></span>**sAMAccountName**
</dt> <dd>

Contém uma cadeia de caracteres que é o nome usado para dar suporte a clientes e servidores de uma versão anterior. O **sAMAccountName** deve ter menos de 20 caracteres para dar suporte a clientes de uma versão anterior do Windows.

O **sAMAccountName** deve ser exclusivo entre todos os objetos de entidade de segurança no domínio. Uma consulta deve ser executada em relação ao domínio para verificar se **sAMAccountName** é exclusivo dentro do domínio.

</dd> </dl>

Os membros do grupo podem ser adicionados no momento da criação usando o método [**IDirectoryObject:: CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) . Opcionalmente, os membros podem ser adicionados ao grupo após a criação usando o método [**IADs:: Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) . Para obter mais informações sobre como adicionar membros a um grupo, consulte [adicionando membros a grupos em um domínio](adding-members-to-groups-in-a-domain.md).

 

 