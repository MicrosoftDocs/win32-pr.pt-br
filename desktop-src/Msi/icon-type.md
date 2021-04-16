---
description: O tipo de ícone de tipo semântico é um dos tipos de formato de chave. Esse tipo consiste em uma chave na tabela de ícones fornecida pelo usuário.
ms.assetid: 8e155846-cc29-43f4-b1f7-9880320edbec
title: Tipo de ícone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a7c90de925ff34977e7ff192dffe0b8614e5734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750239"
---
# <a name="icon-type"></a><span data-ttu-id="17ef0-104">Tipo de ícone</span><span class="sxs-lookup"><span data-stu-id="17ef0-104">Icon Type</span></span>

<span data-ttu-id="17ef0-105">O tipo de ícone de [tipo semântico](semantic-types.md) é um dos [tipos de formato de chave](key-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="17ef0-105">The Icon Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="17ef0-106">Esse tipo consiste em uma chave na [tabela de ícones](icon-table.md) fornecida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="17ef0-106">This type consists of a key into the [Icon table](icon-table.md) provided by the user.</span></span>

<span data-ttu-id="17ef0-107">A ferramenta de mesclagem deve substituir um [identificador](identifier.md) de Windows Installer válido para itens desse tipo.</span><span class="sxs-lookup"><span data-stu-id="17ef0-107">The merge tool must substitute a valid Windows Installer [Identifier](identifier.md) for items of this type.</span></span> <span data-ttu-id="17ef0-108">Mergemod.dll não impõe essa restrição e cabe à ferramenta de mesclagem garantir que o usuário forneça uma chave válida para a tabela de ícones.</span><span class="sxs-lookup"><span data-stu-id="17ef0-108">Mergemod.dll does not enforce this restriction and it is up to the merge tool to ensure that the user provides a valid key into the Icon table.</span></span>

<span data-ttu-id="17ef0-109">NULL é um valor válido para esse tipo, a menos que o msmConfigItemNonNullable tenha sido incluído no campo Attributes da [Tabela ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="17ef0-109">Null is a valid value for this type unless the msmConfigItemNonNullable has been included in the Attributes field of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="17ef0-110">O tipo binary pode ser usado com os seguintes tipos de ContextData.</span><span class="sxs-lookup"><span data-stu-id="17ef0-110">The Binary type may be used with the following kinds of ContextData.</span></span>

<span data-ttu-id="17ef0-111">**ShortcutIcon ContextData**</span><span class="sxs-lookup"><span data-stu-id="17ef0-111">**ShortcutIcon ContextData**</span></span>

<span data-ttu-id="17ef0-112">Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça uma chave estrangeira para uma linha na [tabela de ícones](icon-table.md) que contém uma imagem adequada para uso como um ícone de atalho.</span><span class="sxs-lookup"><span data-stu-id="17ef0-112">A configurable merge module may use this type to enable the user to provide a foreign key to a row in the [Icon Table](icon-table.md) that contains an image suitable for use as a shortcut icon.</span></span> <span data-ttu-id="17ef0-113">Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do item configurável na coluna Name, inserir "1" na coluna Format, digitar "Icon" na coluna type e digitar "ShorcutIcon" na coluna ContextData da Tabela ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="17ef0-113">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Icon" into the Type column, and enter "ShorcutIcon" into the ContextData column of the ModuleConfiguration table.</span></span> <span data-ttu-id="17ef0-114">Esse tipo não é apropriado para uso em uma tabela de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="17ef0-114">This type is not appropriate for use in a user interface table.</span></span> <span data-ttu-id="17ef0-115">Para modificar uma chave para a tabela de ícones nessas tabelas, consulte o ícone ContextData em [tipo binário](binary-type.md).</span><span class="sxs-lookup"><span data-stu-id="17ef0-115">To modify a key to the Icon table in these tables see Icon ContextData under [Binary Type](binary-type.md).</span></span>

 

 



