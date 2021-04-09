---
title: Atributos (AD DS)
description: Cada objeto no Active Directory Domain Services contém um conjunto de atributos que definem as características do objeto.
ms.assetid: 9efa7ae1-b6a9-4b95-b031-b502772c536c
ms.tgt_platform: multiple
keywords:
- AD de atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56579494cdc12c2d0ad6fadbb6395d07eaec80d2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007362"
---
# <a name="attributes-ad-ds"></a><span data-ttu-id="6daa3-104">Atributos (AD DS)</span><span class="sxs-lookup"><span data-stu-id="6daa3-104">Attributes (AD DS)</span></span>

<span data-ttu-id="6daa3-105">Cada objeto no Active Directory Domain Services contém um conjunto de atributos que definem as características do objeto.</span><span class="sxs-lookup"><span data-stu-id="6daa3-105">Each object in Active Directory Domain Services contains a set of attributes that define the characteristics of the object.</span></span> <span data-ttu-id="6daa3-106">Cada atributo é descrito por um objeto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) no contêiner de esquema que define o atributo.</span><span class="sxs-lookup"><span data-stu-id="6daa3-106">Each attribute is described by an [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object in the schema container that defines the attribute.</span></span> <span data-ttu-id="6daa3-107">A definição de atributo inclui uma variedade de dados, por exemplo, os tipos de objeto aos quais o atributo se aplica e o tipo de sintaxe do atributo.</span><span class="sxs-lookup"><span data-stu-id="6daa3-107">The attribute definition includes a variety of data, for example, what object types that the attribute applies to and the syntax type of the attribute.</span></span> <span data-ttu-id="6daa3-108">Para obter mais informações sobre definições de esquema de atributo, consulte [características de atributos](characteristics-of-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="6daa3-108">For more information about attribute schema definitions, see [Characteristics of Attributes](characteristics-of-attributes.md).</span></span>

<span data-ttu-id="6daa3-109">A lista a seguir lista os tipos de atributos que são armazenados em Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="6daa3-109">The following list lists the type of attributes that are stored in Active Directory Domain Services.</span></span>

<dl> <dt>

<span data-ttu-id="6daa3-110"><span id="Domain-replicated__stored_attributes"></span><span id="domain-replicated__stored_attributes"></span><span id="DOMAIN-REPLICATED__STORED_ATTRIBUTES"></span>Atributos armazenados replicados pelo domínio</span><span class="sxs-lookup"><span data-stu-id="6daa3-110"><span id="Domain-replicated__stored_attributes"></span><span id="domain-replicated__stored_attributes"></span><span id="DOMAIN-REPLICATED__STORED_ATTRIBUTES"></span>Domain-replicated, stored attributes</span></span>
</dt> <dd>

<span data-ttu-id="6daa3-111">Alguns atributos são armazenados no diretório (como [**CN**](/windows/desktop/ADSchema/a-cn), [**NTSECURITYDESCRIPTOR**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)e [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)) e replicados para todos os controladores de domínio em um domínio.</span><span class="sxs-lookup"><span data-stu-id="6daa3-111">Some attributes are stored in the directory (such as [**cn**](/windows/desktop/ADSchema/a-cn), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), and [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)) and replicated to all domain controllers in a domain.</span></span> <span data-ttu-id="6daa3-112">Um subconjunto desses atributos também é replicado para o catálogo global.</span><span class="sxs-lookup"><span data-stu-id="6daa3-112">A subset of these attributes is also replicated to the global catalog.</span></span> <span data-ttu-id="6daa3-113">Se você enumerar atributos de um objeto do catálogo global, somente os atributos replicados para o catálogo global serão retornados.</span><span class="sxs-lookup"><span data-stu-id="6daa3-113">If you enumerate attributes of an object from the global catalog, only the attributes replicated to the global catalog are returned.</span></span> <span data-ttu-id="6daa3-114">Alguns atributos também são indexados porque a inclusão de uma propriedade indexada em uma consulta melhora o desempenho da consulta.</span><span class="sxs-lookup"><span data-stu-id="6daa3-114">Some attributes are also indexed because including an indexed property in a query improves the query performance.</span></span>

</dd> <dt>

<span data-ttu-id="6daa3-115"><span id="Non-replicated__locally_stored_attributes"></span><span id="non-replicated__locally_stored_attributes"></span><span id="NON-REPLICATED__LOCALLY_STORED_ATTRIBUTES"></span>Atributos armazenados localmente e não replicados</span><span class="sxs-lookup"><span data-stu-id="6daa3-115"><span id="Non-replicated__locally_stored_attributes"></span><span id="non-replicated__locally_stored_attributes"></span><span id="NON-REPLICATED__LOCALLY_STORED_ATTRIBUTES"></span>Non-replicated, locally stored attributes</span></span>
</dt> <dd>

<span data-ttu-id="6daa3-116">Atributos não replicados, como [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**Last-login**](/windows/desktop/ADSchema/a-lastlogon)e [**Last-logoff**](/windows/desktop/ADSchema/a-lastlogoff) , são armazenados em cada controlador de domínio, mas não são replicados.</span><span class="sxs-lookup"><span data-stu-id="6daa3-116">Non-replicated attributes, such as [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**Last-Logon**](/windows/desktop/ADSchema/a-lastlogon), and [**Last-Logoff**](/windows/desktop/ADSchema/a-lastlogoff) are stored on each domain controller, but are not replicated.</span></span> <span data-ttu-id="6daa3-117">Os atributos não replicados são atributos que pertencem a um controlador de domínio específico.</span><span class="sxs-lookup"><span data-stu-id="6daa3-117">The non-replicated attributes are attributes that pertain to a particular domain controller.</span></span> <span data-ttu-id="6daa3-118">Por exemplo, o **último atributo de logon** é a última data e hora em que o logon de rede do usuário foi validado por esse controlador de domínio específico que retornou a propriedade.</span><span class="sxs-lookup"><span data-stu-id="6daa3-118">For example, **Last-Logon** attribute is the last date and time that the user's network logon was validated by that particular domain controller that returned the property.</span></span> <span data-ttu-id="6daa3-119">Esses atributos podem ser recuperados da mesma maneira que os atributos de todo o domínio descritos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="6daa3-119">These attributes can be retrieved in the same way as the domain-wide attributes described previously.</span></span> <span data-ttu-id="6daa3-120">No entanto, para esses atributos, cada controlador de domínio armazena apenas os valores que pertencem a esse controlador de domínio específico.</span><span class="sxs-lookup"><span data-stu-id="6daa3-120">However, for these attributes, each domain controller stores only values that pertain to that particular domain controller.</span></span> <span data-ttu-id="6daa3-121">Por exemplo, para obter a última vez que um usuário fez logon no domínio, recupere o último atributo de **logon** para o usuário de cada controlador de domínio no domínio e localize a data e a hora mais recentes.</span><span class="sxs-lookup"><span data-stu-id="6daa3-121">For example, to obtain the last time that a user logged on to the domain, retrieve the **Last-Logon** attribute for the user from every domain controller in the domain and find that latest date and time.</span></span>

</dd> <dt>

<span data-ttu-id="6daa3-122"><span id="Non-stored__constructed_attributes"></span><span id="non-stored__constructed_attributes"></span><span id="NON-STORED__CONSTRUCTED_ATTRIBUTES"></span>Atributos construídos e não armazenados</span><span class="sxs-lookup"><span data-stu-id="6daa3-122"><span id="Non-stored__constructed_attributes"></span><span id="non-stored__constructed_attributes"></span><span id="NON-STORED__CONSTRUCTED_ATTRIBUTES"></span>Non-stored, constructed attributes</span></span>
</dt> <dd>

<span data-ttu-id="6daa3-123">Um objeto de usuário também tem atributos construídos que não são armazenados no diretório, mas são calculados pelo controlador de domínio, como [**canônicaname**](/windows/desktop/ADSchema/a-canonicalname) e [**allowedattributes**](/windows/desktop/ADSchema/a-allowedattributes).</span><span class="sxs-lookup"><span data-stu-id="6daa3-123">A user object also has constructed attributes that are not stored in the directory, but are calculated by the domain controller, such as [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname) and [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes).</span></span>

</dd> </dl>

 

 