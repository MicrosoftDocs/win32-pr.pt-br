---
description: O tipo de caixa de diálogo do tipo semântico é um dos tipos de formato de chave. Esse tipo consiste em uma chave estrangeira na tabela de diálogo fornecida pelo usuário.
ms.assetid: 3656684a-de95-45e1-9c78-5c1cc8ca879a
title: Tipo de Caixa de Diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ed04dece5702d232f252caa7c0ee02e7576246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778725"
---
# <a name="dialog-type"></a><span data-ttu-id="17af9-104">Tipo de Caixa de Diálogo</span><span class="sxs-lookup"><span data-stu-id="17af9-104">Dialog Type</span></span>

<span data-ttu-id="17af9-105">O tipo de caixa de diálogo do [tipo semântico](semantic-types.md) é um dos [tipos de formato de chave](key-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="17af9-105">The Dialog Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="17af9-106">Esse tipo consiste em uma chave estrangeira na [tabela de diálogo](dialog-table.md) fornecida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="17af9-106">This type consists of a foreign key into the [Dialog table](dialog-table.md) provided by the user.</span></span>

<span data-ttu-id="17af9-107">A ferramenta de mesclagem deve substituir um [identificador](identifier.md) de Windows Installer válido para itens desse tipo.</span><span class="sxs-lookup"><span data-stu-id="17af9-107">The merge tool must substitute a valid Windows Installer [Identifier](identifier.md) for items of this type.</span></span> <span data-ttu-id="17af9-108">Mergemod.dll não impõe essa restrição e cabe à ferramenta de mesclagem garantir que o usuário forneça uma chave válida para a tabela de diálogo.</span><span class="sxs-lookup"><span data-stu-id="17af9-108">Mergemod.dll does not enforce this restriction and it is up to the merge tool to ensure that the user provides a valid key into the Dialog table.</span></span>

<span data-ttu-id="17af9-109">NULL é um valor válido para esse tipo, a menos que o msmConfigItemNonNullable tenha sido incluído no campo Attributes da [Tabela ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="17af9-109">Null is a valid value for this type unless the msmConfigItemNonNullable has been included in the Attributes field of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="17af9-110">O tipo de caixa de diálogo pode ser usado com os seguintes tipos de ContextData.</span><span class="sxs-lookup"><span data-stu-id="17af9-110">The Dialog type may be used with the following kinds of ContextData.</span></span>

<span data-ttu-id="17af9-111">**DialogNext ContextData**</span><span class="sxs-lookup"><span data-stu-id="17af9-111">**DialogNext ContextData**</span></span>

<span data-ttu-id="17af9-112">Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça uma chave estrangeira na tabela de diálogo.</span><span class="sxs-lookup"><span data-stu-id="17af9-112">A configurable merge module may use this type to enable the user to provide a foreign key into the Dialog Table.</span></span> <span data-ttu-id="17af9-113">Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do item configurável na coluna nome, inserir "1" na coluna de formato, inserir "caixa de diálogo" na coluna tipo e digitar "DialogNext" na coluna ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="17af9-113">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Dialog" into the Type column, and enter "DialogNext" into the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="17af9-114">**DialogPrev ContextData**</span><span class="sxs-lookup"><span data-stu-id="17af9-114">**DialogPrev ContextData**</span></span>

<span data-ttu-id="17af9-115">Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça uma chave estrangeira na tabela de diálogo.</span><span class="sxs-lookup"><span data-stu-id="17af9-115">A configurable merge module may use this type to enable the user to provide a foreign key into the Dialog Table.</span></span> <span data-ttu-id="17af9-116">Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do item configurável na coluna nome, inserir "1" na coluna de formato, inserir "caixa de diálogo" na coluna tipo e digitar "DialogPrev" na coluna ContextData da Tabela ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="17af9-116">To specify a configurable item of this type, module authors should enter the name of the configurable item into the Name column, enter "1" into the Format column, enter "Dialog" into the Type column, and enter "DialogPrev" into the ContextData column of the ModuleConfiguration table.</span></span>

 

 



