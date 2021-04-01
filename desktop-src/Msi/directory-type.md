---
description: O tipo de diretório do tipo semântico é um dos tipos de formato de chave, que consiste em uma chave estrangeira na tabela de diretórios fornecida pelo usuário.
ms.assetid: b5a0ed38-1dda-4c33-9429-0cbe87e13aef
title: Tipo de diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3ba336dd5de7cd45ef9215f0397ba51ce544d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828998"
---
# <a name="directory-type"></a><span data-ttu-id="e9e39-103">Tipo de diretório</span><span class="sxs-lookup"><span data-stu-id="e9e39-103">Directory Type</span></span>

<span data-ttu-id="e9e39-104">O tipo de diretório do [tipo semântico](semantic-types.md) é um dos [tipos de formato de chave](key-format-types.md), que consiste em uma chave estrangeira na tabela de [diretórios](directory-table.md) fornecida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="e9e39-104">The Directory Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md), which consists of a foreign key into the [Directory table](directory-table.md) provided by the user.</span></span>

<span data-ttu-id="e9e39-105">A ferramenta de mesclagem deve substituir um [identificador](identifier.md) de Windows Installer válido para itens desse tipo.</span><span class="sxs-lookup"><span data-stu-id="e9e39-105">The merge tool must substitute a valid Windows Installer [Identifier](identifier.md) for items of this type.</span></span> <span data-ttu-id="e9e39-106">Mergemod.dll não impõe essa restrição e cabe à ferramenta de mesclagem garantir que o usuário forneça uma chave válida para a tabela de diretórios.</span><span class="sxs-lookup"><span data-stu-id="e9e39-106">Mergemod.dll does not enforce this restriction and it is up to the merge tool to ensure that the user provides a valid key into the Directory table.</span></span>

<span data-ttu-id="e9e39-107">Um item configurável do tipo de diretório deve modificar apenas o diretório de destino da instalação e não modificar a imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="e9e39-107">A configurable item of the Directory type should only modify the destination directory of the installation and not modify the source image.</span></span> <span data-ttu-id="e9e39-108">Um item configurável desse tipo deve, portanto, modificar apenas as chaves estrangeiras para a tabela de diretório e não modificar a tabela de diretório diretamente.</span><span class="sxs-lookup"><span data-stu-id="e9e39-108">A configurable item of this type should therefore only modify foreign keys to the Directory table and not modify the Directory table directly.</span></span>

<span data-ttu-id="e9e39-109">Como a \_ coluna Directory da [tabela Component](component-table.md) é não anulável, NULL é um valor inválido para um item configurável desse tipo, mesmo que msmConfigItemNonNullable não esteja definido na coluna Attributes.</span><span class="sxs-lookup"><span data-stu-id="e9e39-109">Because the Directory\_ column of the [Component table](component-table.md) is non-nullable, null is an invalid value for a configurable item of this type even if the msmConfigItemNonNullable is not set in the Attributes column.</span></span>

<span data-ttu-id="e9e39-110">O tipo de diretório pode ser usado com dois tipos de ContextData.</span><span class="sxs-lookup"><span data-stu-id="e9e39-110">The Directory type may be used with two kinds of ContextData.</span></span>

<span data-ttu-id="e9e39-111">**IsolationDirectory ContextData**</span><span class="sxs-lookup"><span data-stu-id="e9e39-111">**IsolationDirectory ContextData**</span></span>

<span data-ttu-id="e9e39-112">Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça um diretório de destino para arquivos no módulo.</span><span class="sxs-lookup"><span data-stu-id="e9e39-112">A configurable merge module may use this type to enable the user to provide a destination directory for files in the module.</span></span> <span data-ttu-id="e9e39-113">A ferramenta de mesclagem substitui o identificador do diretório nos modelos na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="e9e39-113">The merge tool substitutes the directory's identifier into the templates in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="e9e39-114">Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do diretório na coluna nome, inserir "1" na coluna formato, inserir "diretório" na coluna tipo e digitar "IsolationDirectory" na coluna ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="e9e39-114">To specify a configurable item of this type, module authors should enter the name of the directory into the Name column, enter "1" into the Format column, enter "Directory" into the Type column, and enter "IsolationDirectory" into the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="e9e39-115">**ShortcutLocation ContextData**</span><span class="sxs-lookup"><span data-stu-id="e9e39-115">**ShortcutLocation ContextData**</span></span>

<span data-ttu-id="e9e39-116">Um módulo de mesclagem configurável pode usar esse tipo para permitir que o usuário forneça um diretório de destino para atalhos no módulo.</span><span class="sxs-lookup"><span data-stu-id="e9e39-116">A configurable merge module may use this type to enable the user to provide a destination directory for shortcuts in the module.</span></span> <span data-ttu-id="e9e39-117">A ferramenta de mesclagem substitui o identificador do atalho nos modelos na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="e9e39-117">The merge tool substitutes the shortcut's identifier into the templates in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="e9e39-118">Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do diretório na coluna nome, inserir "1" na coluna formato, inserir "diretório" na coluna tipo e digitar "ShortcutLocation" na coluna ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="e9e39-118">To specify a configurable item of this type, module authors should enter the name of the directory into the Name column, enter "1" into the Format column, enter "Directory" into the Type column, and enter "ShortcutLocation" into the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

 

 



