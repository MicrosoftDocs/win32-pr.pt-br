---
description: O tipo de Propriedade do tipo semântico é um dos tipos de formato de chave. Esse tipo consiste em uma chave estrangeira na tabela de propriedades fornecida pelo usuário.
ms.assetid: 819e4e90-0bc3-41ba-851d-1d4c52b6eeea
title: Tipo de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36236c78160abbfe3ad64c6b801a3cdbdbb98b48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010996"
---
# <a name="property-type"></a><span data-ttu-id="9892b-104">Tipo de propriedade</span><span class="sxs-lookup"><span data-stu-id="9892b-104">Property Type</span></span>

<span data-ttu-id="9892b-105">O tipo de Propriedade do [tipo semântico](semantic-types.md) é um dos [tipos de formato de chave](key-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="9892b-105">The Property Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="9892b-106">Esse tipo consiste em uma chave estrangeira na [tabela de propriedades](property-table.md) fornecida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="9892b-106">This type consists of a foreign key into the [Property table](property-table.md) provided by the user.</span></span>

<span data-ttu-id="9892b-107">A ferramenta de mesclagem deve substituir um [identificador](identifier.md) de Windows Installer válido para itens desse tipo.</span><span class="sxs-lookup"><span data-stu-id="9892b-107">The merge tool must substitute a valid Windows Installer [Identifier](identifier.md) for items of this type.</span></span> <span data-ttu-id="9892b-108">Mergemod.dll não impõe essa restrição e cabe à ferramenta de mesclagem garantir que o usuário forneça uma chave válida para a tabela de propriedades.</span><span class="sxs-lookup"><span data-stu-id="9892b-108">Mergemod.dll does not enforce this restriction and it is up to the merge tool to ensure that the user provides a valid key into the Property table.</span></span> <span data-ttu-id="9892b-109">As chaves primárias da tabela de propriedades são os nomes de propriedade.</span><span class="sxs-lookup"><span data-stu-id="9892b-109">The primary keys of the Property table are the property names.</span></span>

<span data-ttu-id="9892b-110">NULL é um valor válido para esse tipo, a menos que o msmConfigItemNonNullable tenha sido incluído no campo Attributes da [Tabela ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="9892b-110">Null is a valid value for this type unless the msmConfigItemNonNullable has been included in the Attributes field of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="9892b-111">O tipo de propriedade pode ser usado com os seguintes tipos de ContextData.</span><span class="sxs-lookup"><span data-stu-id="9892b-111">The Property type may be used with the following kinds of ContextData.</span></span>

<span data-ttu-id="9892b-112">**ContextData nulo**</span><span class="sxs-lookup"><span data-stu-id="9892b-112">**Null ContextData**</span></span>

<span data-ttu-id="9892b-113">Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça um nome de propriedade para uma tabela de banco de dados no módulo.</span><span class="sxs-lookup"><span data-stu-id="9892b-113">A configurable merge module may use this type to enable the user to provide a property name to a database table in the module.</span></span> <span data-ttu-id="9892b-114">A ferramenta de mesclagem substitui o identificador da propriedade nos modelos na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="9892b-114">The merge tool substitutes the property's identifier into the templates in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="9892b-115">Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do item configurável na coluna Name, inserir "1" na coluna Format, inserir "Property" na coluna type e deixar em branco a coluna ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="9892b-115">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Property" into the Type column, and leave blank the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="9892b-116">**ContextData público**</span><span class="sxs-lookup"><span data-stu-id="9892b-116">**Public ContextData**</span></span>

<span data-ttu-id="9892b-117">Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça o nome de uma [propriedade pública](public-properties.md) a uma tabela de banco de dados no módulo.</span><span class="sxs-lookup"><span data-stu-id="9892b-117">A configurable merge module may use this type to enable the user to provide the name of a [public property](public-properties.md) to a database table in the module.</span></span> <span data-ttu-id="9892b-118">A ferramenta de mesclagem substitui o identificador da propriedade nos modelos na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="9892b-118">The merge tool substitutes the property's identifier into the templates in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="9892b-119">Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do item configurável na coluna Name, inserir "1" na coluna Format, inserir "Property" na coluna type e digitar "Public" na coluna ContextData da Tabela ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9892b-119">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Property" into the Type column, and enter "Public" into the ContextData column of the ModuleConfiguration table.</span></span>

<span data-ttu-id="9892b-120">**ContextData particular**</span><span class="sxs-lookup"><span data-stu-id="9892b-120">**Private ContextData**</span></span>

<span data-ttu-id="9892b-121">Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça o nome de uma [propriedade privada](private-properties.md) a uma tabela de banco de dados no módulo.</span><span class="sxs-lookup"><span data-stu-id="9892b-121">A configurable merge module may use this type to enable the user to provide the name of a [private property](private-properties.md) to a database table in the module.</span></span> <span data-ttu-id="9892b-122">A ferramenta de mesclagem substitui o identificador da propriedade nos modelos na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="9892b-122">The merge tool substitutes the property's identifier into the templates in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="9892b-123">Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do item configurável na coluna Name, inserir "1" na coluna Format, inserir "Property" na coluna type e inserir "Private" na coluna ContextData da Tabela ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9892b-123">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Property" into the Type column, and enter "Private" into the ContextData column of the ModuleConfiguration table.</span></span>

 

 



