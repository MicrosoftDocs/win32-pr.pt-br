---
title: Nomeando atributos e classes
description: Este tópico inclui diretrizes para nomear atributos e classes.
ms.assetid: ccbc2859-332f-4ded-9125-5bf507cad960
ms.tgt_platform: multiple
keywords:
- Nomeando atributos e classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bfd2614033e12f68ba2727cc7aec689c16071e
ms.sourcegitcommit: 02e6e0b58720bf6b77797dd7a9ddc11c95f42b33
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2020
ms.locfileid: "105752988"
---
# <a name="naming-attributes-and-classes"></a><span data-ttu-id="dcad6-104">Nomeando atributos e classes</span><span class="sxs-lookup"><span data-stu-id="dcad6-104">Naming Attributes and Classes</span></span>

<span data-ttu-id="dcad6-105">Este tópico inclui diretrizes para nomear atributos e classes.</span><span class="sxs-lookup"><span data-stu-id="dcad6-105">This topic includes guidelines for naming attributes and classes.</span></span>

<span data-ttu-id="dcad6-106">Para criar uma nova classe ou atributo, siga as seguintes regras de nomenclatura:</span><span class="sxs-lookup"><span data-stu-id="dcad6-106">To create a new class or attribute, adhere to the following naming rules:</span></span>

-   <span data-ttu-id="dcad6-107">Use o mesmo nome para as propriedades **CN** e **lDAPDisplayName** de um novo objeto **attributeSchema** ou **classSchema** .</span><span class="sxs-lookup"><span data-stu-id="dcad6-107">Use the same name for both the **cn** and **lDAPDisplayName** properties of a new **attributeSchema** or **classSchema** object.</span></span>
-   <span data-ttu-id="dcad6-108">Identifique a empresa com um prefixo em minúsculas na primeira seção do nome.</span><span class="sxs-lookup"><span data-stu-id="dcad6-108">Identify the company with a lower-case prefix in the first section of the name.</span></span> <span data-ttu-id="dcad6-109">Esse prefixo pode ser um nome DNS, acrônimo ou outra cadeia de caracteres que identifica exclusivamente a empresa.</span><span class="sxs-lookup"><span data-stu-id="dcad6-109">This prefix can be a DNS name, acronym, or other string that uniquely identifies the company.</span></span> <span data-ttu-id="dcad6-110">O prefixo garante que todos os atributos e classes de uma empresa específica sejam exibidos consecutivamente ao navegar no esquema.</span><span class="sxs-lookup"><span data-stu-id="dcad6-110">The prefix ensures that all attributes and classes for a specific company are displayed consecutively when browsing the schema.</span></span>
-   <span data-ttu-id="dcad6-111">Se você estiver desenvolvendo uma extensão de esquema como um fornecedor de software independente, adicione uma abreviação do nome do produto do prefixo.</span><span class="sxs-lookup"><span data-stu-id="dcad6-111">If you are developing a schema extension as an independent software vendor, add an abbreviation of the product name of the prefix.</span></span> <span data-ttu-id="dcad6-112">Isso adiciona distinção entre vários produtos que contêm extensões de esquema LDAP.</span><span class="sxs-lookup"><span data-stu-id="dcad6-112">This adds distinction between multiple products that contain LDAP schema extensions.</span></span>
-   <span data-ttu-id="dcad6-113">Use um hífen como o próximo caractere após o prefixo.</span><span class="sxs-lookup"><span data-stu-id="dcad6-113">Use a hyphen as the next character after the prefix.</span></span>
-   <span data-ttu-id="dcad6-114">Especifique um nome de atributo ou classe que seja exclusivo dentro dos atributos da empresa após o hífen.</span><span class="sxs-lookup"><span data-stu-id="dcad6-114">Specify an attribute or class name that is unique within the company's attributes after the hyphen.</span></span> <span data-ttu-id="dcad6-115">Essa parte do nome comum deve ser descritiva.</span><span class="sxs-lookup"><span data-stu-id="dcad6-115">This part of the common-name should be descriptive.</span></span> <span data-ttu-id="dcad6-116">Não use nomes de ilógico que não sejam de sentido para desenvolvedores e visualizadores do esquema.</span><span class="sxs-lookup"><span data-stu-id="dcad6-116">Do not use illogical names that are meaningless to developers and viewers of the schema.</span></span>

<span data-ttu-id="dcad6-117">Por exemplo, se a empresa fictícia Fabrikam estendeu o esquema adicionando um atributo para armazenar um identificador de correio de voz, o **CN** e o **lDAPDisplayName** do novo atributo poderiam ser "fabrikam-postalid".</span><span class="sxs-lookup"><span data-stu-id="dcad6-117">For example, if the fictitious Fabrikam company extended the schema by adding an attribute for storing a voice-mail identifier, the **cn** and **lDAPDisplayName** of the new attribute could be "fabrikam-VoiceMailID".</span></span>

<span data-ttu-id="dcad6-118">Se o **lDAPDisplayName** de um atributo ou classe não for especificado, o sistema usará o **CN** para gerar um.</span><span class="sxs-lookup"><span data-stu-id="dcad6-118">If the **lDAPDisplayName** of an attribute or class is not specified, the system uses the **cn** to generate one.</span></span> <span data-ttu-id="dcad6-119">No entanto, o algoritmo do sistema para gerar o nome pode resultar em colisões de nome ou nomes que são difíceis de ler.</span><span class="sxs-lookup"><span data-stu-id="dcad6-119">However, the system algorithm for generating the name may result in name collisions or names that are difficult to read.</span></span> <span data-ttu-id="dcad6-120">Para evitar esses problemas, é recomendável que um **lDAPDisplayName** seja explicitamente especificado para todos os atributos e classes.</span><span class="sxs-lookup"><span data-stu-id="dcad6-120">To avoid these problems, it is recommended that an **lDAPDisplayName** be explicitly specified for all attributes and classes.</span></span>

<span data-ttu-id="dcad6-121">Para fins de desenvolvimento e teste, pode ser desejável acrescentar um sufixo de versão ao **CN** e ao **lDAPDisplayName**, por exemplo, "fabrikam-correio de voz-001".</span><span class="sxs-lookup"><span data-stu-id="dcad6-121">For development and testing purposes, it may be desirable to append a version suffix to the **cn** and **lDAPDisplayName**, for example, "fabrikam-VoiceMailID-001".</span></span> <span data-ttu-id="dcad6-122">Em um ambiente de desenvolvimento/teste distribuído, um sufixo de versão permite que os desenvolvedores executem várias versões de seu software simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="dcad6-122">In a distributed development/test environment, a version suffix enables developers to run multiple versions of their software simultaneously.</span></span> <span data-ttu-id="dcad6-123">Após a conclusão do teste, renomeie o atributo ou a classe para remover o sufixo.</span><span class="sxs-lookup"><span data-stu-id="dcad6-123">After testing is complete, rename the attribute or class to remove the suffix.</span></span>

<span data-ttu-id="dcad6-124">Não é possível excluir versões expiradas de extensões de esquema, mas é possível desabilitá-las e renomeá-las com nomes obscuros.</span><span class="sxs-lookup"><span data-stu-id="dcad6-124">It is not possible to delete defunct versions of a schema extensions, but it is possible to disable them and rename them with obscure names.</span></span> <span data-ttu-id="dcad6-125">Para obter mais informações, consulte [desabilitando classes e atributos existentes](disabling-existing-classes-and-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="dcad6-125">For more information, see [Disabling Existing Classes and Attributes](disabling-existing-classes-and-attributes.md).</span></span>

 

 




