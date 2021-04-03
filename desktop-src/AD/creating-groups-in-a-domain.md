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
# <a name="creating-groups-in-a-domain"></a><span data-ttu-id="39437-104">Criando grupos em um domínio</span><span class="sxs-lookup"><span data-stu-id="39437-104">Creating Groups in a Domain</span></span>

<span data-ttu-id="39437-105">Um objeto de grupo é criado em Active Directory Domain Services no contêiner de domínio em que o novo grupo estará contido.</span><span class="sxs-lookup"><span data-stu-id="39437-105">A group object is created in Active Directory Domain Services in the domain container where the new group will be contained.</span></span> <span data-ttu-id="39437-106">Os grupos podem ser criados na raiz do domínio, em uma unidade organizacional ou em um contêiner.</span><span class="sxs-lookup"><span data-stu-id="39437-106">Groups can be created at the root of the domain, within an organizational unit, or within a container.</span></span> <span data-ttu-id="39437-107">Para criar um objeto de grupo, use o método [**IADsContainer:: Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) ou [**IDirectoryObject:: CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) .</span><span class="sxs-lookup"><span data-stu-id="39437-107">To create a group object, use the [**IADsContainer::Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) or the [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) method.</span></span>

<span data-ttu-id="39437-108">Os seguintes atributos são necessários para tornar o objeto de grupo um grupo legal que o servidor Active Directory e o sistema de segurança do Windows reconhecerão:</span><span class="sxs-lookup"><span data-stu-id="39437-108">The following attributes are required to make the group object a legal group that the Active Directory server and the Windows security system will recognize:</span></span>

<dl> <dt>

<span data-ttu-id="39437-109"><span id="cn"></span><span id="CN"></span>**Hong**</span><span class="sxs-lookup"><span data-stu-id="39437-109"><span id="cn"></span><span id="CN"></span>**cn**</span></span>
</dt> <dd>

<span data-ttu-id="39437-110">Especifica o nome do objeto de grupo no diretório.</span><span class="sxs-lookup"><span data-stu-id="39437-110">Specifies the name of the group object in the directory.</span></span> <span data-ttu-id="39437-111">Esse será o nome distinto relativo do objeto dentro do contêiner em que o grupo é criado.</span><span class="sxs-lookup"><span data-stu-id="39437-111">This will be the object's relative distinguished name within the container where the group is created.</span></span>

</dd> <dt>

<span data-ttu-id="39437-112"><span id="groupType"></span><span id="grouptype"></span><span id="GROUPTYPE"></span>**groupType**</span><span class="sxs-lookup"><span data-stu-id="39437-112"><span id="groupType"></span><span id="grouptype"></span><span id="GROUPTYPE"></span>**groupType**</span></span>
</dt> <dd>

<span data-ttu-id="39437-113">Contém um inteiro que especifica o tipo de grupo e o escopo.</span><span class="sxs-lookup"><span data-stu-id="39437-113">Contains an integer that specifies the group type and scope.</span></span> <span data-ttu-id="39437-114">A [**enumeração \_ \_ \_ enum do tipo de grupo ADS**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) define os valores possíveis para o atributo **GroupType** .</span><span class="sxs-lookup"><span data-stu-id="39437-114">The [**ADS\_GROUP\_TYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) enumeration defines the possible values for the **groupType** attribute.</span></span>

<span data-ttu-id="39437-115">A lista a seguir define os valores e tipos de grupo comuns para esse atributo.</span><span class="sxs-lookup"><span data-stu-id="39437-115">The following list defines common group types and values for this attribute.</span></span>

<dl> <dt>

<span data-ttu-id="39437-116"><span id="Domain_Local_Distribution"></span><span id="domain_local_distribution"></span><span id="DOMAIN_LOCAL_DISTRIBUTION"></span>Distribuição local de domínio</span><span class="sxs-lookup"><span data-stu-id="39437-116"><span id="Domain_Local_Distribution"></span><span id="domain_local_distribution"></span><span id="DOMAIN_LOCAL_DISTRIBUTION"></span>Domain Local Distribution</span></span>
</dt> <dd>

<span data-ttu-id="39437-117">**\_grupo de \_ grupos \_ locais de domínio do tipo de \_ grupo ADS \_**</span><span class="sxs-lookup"><span data-stu-id="39437-117">**ADS\_GROUP\_TYPE\_DOMAIN\_LOCAL\_GROUP**</span></span>

</dd> <dt>

<span data-ttu-id="39437-118"><span id="Domain_Local_Security"></span><span id="domain_local_security"></span><span id="DOMAIN_LOCAL_SECURITY"></span>Segurança local do domínio</span><span class="sxs-lookup"><span data-stu-id="39437-118"><span id="Domain_Local_Security"></span><span id="domain_local_security"></span><span id="DOMAIN_LOCAL_SECURITY"></span>Domain Local Security</span></span>
</dt> <dd>

<span data-ttu-id="39437-119">**Anúncios \_ do grupo \_ \_ local de \_ domínio \_ tipo** de grupo \| **ADS segurança de tipo de grupo \_ \_ \_ \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="39437-119">**ADS\_GROUP\_TYPE\_DOMAIN\_LOCAL\_GROUP** \| **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**</span></span>

</dd> <dt>

<span data-ttu-id="39437-120"><span id="Global_Distribution"></span><span id="global_distribution"></span><span id="GLOBAL_DISTRIBUTION"></span>Distribuição global</span><span class="sxs-lookup"><span data-stu-id="39437-120"><span id="Global_Distribution"></span><span id="global_distribution"></span><span id="GLOBAL_DISTRIBUTION"></span>Global Distribution</span></span>
</dt> <dd>

<span data-ttu-id="39437-121">**\_ \_ grupo global do tipo de grupo ADS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="39437-121">**ADS\_GROUP\_TYPE\_GLOBAL\_GROUP**</span></span>

</dd> <dt>

<span data-ttu-id="39437-122"><span id="Global_Security"></span><span id="global_security"></span><span id="GLOBAL_SECURITY"></span>Segurança global</span><span class="sxs-lookup"><span data-stu-id="39437-122"><span id="Global_Security"></span><span id="global_security"></span><span id="GLOBAL_SECURITY"></span>Global Security</span></span>
</dt> <dd>

<span data-ttu-id="39437-123">**Anúncios \_ do tipo de grupo grupo \_ \_ global \_** tipos de \| **\_ grupo ADS \_ \_ segurança \_ habilitada**</span><span class="sxs-lookup"><span data-stu-id="39437-123">**ADS\_GROUP\_TYPE\_GLOBAL\_GROUP** \| **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**</span></span>

</dd> <dt>

<span data-ttu-id="39437-124"><span id="Universal_Distribution"></span><span id="universal_distribution"></span><span id="UNIVERSAL_DISTRIBUTION"></span>Distribuição universal</span><span class="sxs-lookup"><span data-stu-id="39437-124"><span id="Universal_Distribution"></span><span id="universal_distribution"></span><span id="UNIVERSAL_DISTRIBUTION"></span>Universal Distribution</span></span>
</dt> <dd>

<span data-ttu-id="39437-125">**\_tipo de grupo ADS \_ \_ \_ grupo universal**</span><span class="sxs-lookup"><span data-stu-id="39437-125">**ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP**</span></span>

</dd> <dt>

<span data-ttu-id="39437-126"><span id="Universal_Security"></span><span id="universal_security"></span><span id="UNIVERSAL_SECURITY"></span>Segurança universal</span><span class="sxs-lookup"><span data-stu-id="39437-126"><span id="Universal_Security"></span><span id="universal_security"></span><span id="UNIVERSAL_SECURITY"></span>Universal Security</span></span>
</dt> <dd>

<span data-ttu-id="39437-127">**Anúncios \_ do grupo \_ \_ Universal de \_ tipos** de grupo \| **ADS segurança de tipo de grupo \_ \_ \_ \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="39437-127">**ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** \| **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**</span></span>

</dd> <dt>


</dt> <dd>

</dd> </dl>

<span data-ttu-id="39437-128">Se o grupo for destinado a configurar o controle de acesso em objetos de diretório, o grupo deverá ser um grupo de segurança global ou Universal Security.</span><span class="sxs-lookup"><span data-stu-id="39437-128">If the group is intended for setting access control on directory objects, the group should be a Global Security or Universal Security group.</span></span>

<span data-ttu-id="39437-129">Lembre-se de que os grupos de segurança universal só podem ser criados em domínios do Windows 2000 em execução no modo nativo.</span><span class="sxs-lookup"><span data-stu-id="39437-129">Be aware that Universal Security groups can only be created on Windows 2000 domains running in native mode.</span></span> <span data-ttu-id="39437-130">Para obter mais informações sobre como detectar o modo misto e nativo, consulte [detectando o modo de operação de um domínio](detecting-the-operation-mode-of-a-domain.md).</span><span class="sxs-lookup"><span data-stu-id="39437-130">For more information about detecting mixed and native mode, see [Detecting the Operation Mode of a Domain](detecting-the-operation-mode-of-a-domain.md).</span></span>

</dd> <dt>

<span data-ttu-id="39437-131"><span id="sAMAccountName"></span><span id="samaccountname"></span><span id="SAMACCOUNTNAME"></span>**sAMAccountName**</span><span class="sxs-lookup"><span data-stu-id="39437-131"><span id="sAMAccountName"></span><span id="samaccountname"></span><span id="SAMACCOUNTNAME"></span>**sAMAccountName**</span></span>
</dt> <dd>

<span data-ttu-id="39437-132">Contém uma cadeia de caracteres que é o nome usado para dar suporte a clientes e servidores de uma versão anterior.</span><span class="sxs-lookup"><span data-stu-id="39437-132">Contains a string that is the name used to support clients and servers from a previous version.</span></span> <span data-ttu-id="39437-133">O **sAMAccountName** deve ter menos de 20 caracteres para dar suporte a clientes de uma versão anterior do Windows.</span><span class="sxs-lookup"><span data-stu-id="39437-133">The **sAMAccountName** should be less than 20 characters to support clients of a previous version of Windows.</span></span>

<span data-ttu-id="39437-134">O **sAMAccountName** deve ser exclusivo entre todos os objetos de entidade de segurança no domínio.</span><span class="sxs-lookup"><span data-stu-id="39437-134">The **sAMAccountName** must be unique among all security principal objects within the domain.</span></span> <span data-ttu-id="39437-135">Uma consulta deve ser executada em relação ao domínio para verificar se **sAMAccountName** é exclusivo dentro do domínio.</span><span class="sxs-lookup"><span data-stu-id="39437-135">A query should be performed against the domain to verify that the **sAMAccountName** is unique within the domain.</span></span>

</dd> </dl>

<span data-ttu-id="39437-136">Os membros do grupo podem ser adicionados no momento da criação usando o método [**IDirectoryObject:: CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) .</span><span class="sxs-lookup"><span data-stu-id="39437-136">The members of the group can be added at creation time using the [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) method.</span></span> <span data-ttu-id="39437-137">Opcionalmente, os membros podem ser adicionados ao grupo após a criação usando o método [**IADs:: Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) .</span><span class="sxs-lookup"><span data-stu-id="39437-137">Optionally, members can be added to the group after creation using the [**IADsGroup::Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) method.</span></span> <span data-ttu-id="39437-138">Para obter mais informações sobre como adicionar membros a um grupo, consulte [adicionando membros a grupos em um domínio](adding-members-to-groups-in-a-domain.md).</span><span class="sxs-lookup"><span data-stu-id="39437-138">For more information about adding members to a group, see [Adding Members to Groups in a Domain](adding-members-to-groups-in-a-domain.md).</span></span>

 

 